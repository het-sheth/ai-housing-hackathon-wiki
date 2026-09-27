# Chrome DevTools MCP in Codex CLI

Checked September 26, 2026 on het-legion. This is a local tooling note for the Housing Navigator, not a product or data-source decision.

## What is configured

The user-level Codex MCP configuration includes `chrome-devtools` as a stdio server. Verify it with `codex mcp get chrome-devtools` or `codex mcp list`. The configured command is:

```sh
npx -y chrome-devtools-mcp@latest \
  --executablePath=/usr/bin/chromium \
  --no-usage-statistics \
  --no-performance-crux
```

Node v25.2.1 and Chromium 148.0.7778.178 were installed; Google Chrome was not found on PATH. Chrome DevTools MCP officially supports Google Chrome and Chrome for Testing. The installed Chromium passed a limited local check, but upstream does not guarantee compatibility. A fresh Codex session loaded 30 Chrome DevTools tools, including `list_pages`.

## Current limitation and evidence

Calling `list_pages` through the native MCP tool failed twice with `Protocol error (Target.setDiscoverTargets): Target closed`. In the same session's command sandbox, a direct Chromium headless launch exited with code 133 and `setsockopt: Operation not permitted`. Adding Chromium's `--no-sandbox` flag did not change the result.

The same MCP server launched through an approval-reviewed command outside that sandbox. Its MCP handshake succeeded, `tools/list` returned 30 tools, and `list_pages` returned `about:blank`. A separately launched Chromium debugging endpoint worked outside the sandbox but was unreachable from a sandboxed command. These observations locate the present failure at the browser process and local socket boundary, not at MCP registration. They do not prove that every Codex CLI environment has the same restriction.

The CLI session does not provide the in-app browser. Do not suggest that as a fallback. OpenAI's permission documentation says MCP connections and local commands have separate controls, so changing the CLI command sandbox to Full Access is not a verified fix for native MCP calls.

## Working procedure for browser tasks

1. Use synthetic project data and an isolated browser profile. Do not attach to a personal Chrome profile or inspect credentials. Keep the project's no-paid-AI constraint.
2. For a browser task in this environment, request an approval-reviewed, elevated local command to launch the MCP server and communicate over stdio. The following probe starts an isolated headless Chromium instance and confirms browser access:

```sh
python - <<'PY'
import json
import select
import subprocess
import time

command = [
    'npx', '-y', 'chrome-devtools-mcp@latest',
    '--executablePath=/usr/bin/chromium', '--isolated', '--headless',
    '--no-usage-statistics', '--no-performance-crux',
]
process = subprocess.Popen(
    command, stdin=subprocess.PIPE, stdout=subprocess.PIPE,
    stderr=subprocess.PIPE, text=True, bufsize=1,
)

def request(identifier, method, params):
    payload = {'jsonrpc': '2.0', 'id': identifier, 'method': method, 'params': params}
    process.stdin.write(json.dumps(payload) + '\n')
    process.stdin.flush()
    deadline = time.monotonic() + 20
    while time.monotonic() < deadline:
        ready, _, _ = select.select([process.stdout], [], [], 1)
        if ready:
            line = process.stdout.readline()
            if line:
                response = json.loads(line)
                if response.get('id') == identifier:
                    return response
    raise TimeoutError(f'No MCP response for {method}')

try:
    result = request(1, 'initialize', {
        'protocolVersion': '2025-03-26', 'capabilities': {},
        'clientInfo': {'name': 'housing-browser-check', 'version': '1.0'},
    })
    if 'error' in result:
        raise RuntimeError(result['error'])
    process.stdin.write(json.dumps({
        'jsonrpc': '2.0', 'method': 'notifications/initialized',
    }) + '\n')
    process.stdin.flush()
    pages = request(2, 'tools/call', {
        'name': 'list_pages', 'arguments': {},
    })
    print(json.dumps(pages.get('result', pages), indent=2))
finally:
    process.terminate()
    try:
        process.wait(timeout=3)
    except subprocess.TimeoutExpired:
        process.kill()
PY
```

3. For real inspection, keep the MCP process alive and call the needed tool with the same JSON-RPC `tools/call` pattern. Get argument schemas from `tools/list`. `new_page`, `take_snapshot`, `list_network_requests`, and `list_console_messages` are useful for the app walkthrough. Record the URL and findings without copying personal page content into the wiki.
4. Recheck native `list_pages` after a Codex runtime or sandbox change. Once it succeeds, use the native tools and retire the shell workaround. Do not change the global sandbox policy solely on the assumption that it controls the MCP process.

## Sources

- [Chrome DevTools MCP readme](https://github.com/ChromeDevTools/chrome-devtools-mcp)
- [Chrome DevTools MCP configuration](https://github.com/ChromeDevTools/chrome-devtools-mcp/blob/main/docs/configuration.md)
- [Codex MCP setup](https://learn.chatgpt.com/docs/extend/mcp)
- [Codex permissions and MCP controls](https://learn.chatgpt.com/docs/permissions)
