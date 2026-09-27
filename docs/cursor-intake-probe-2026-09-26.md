# Cursor intake probe

September 26, 2026. One successful local CLI intake request following user installation and browser authentication. This is an isolated feasibility probe, not application integration or provider selection.

## Setup and result

- CLI: 2026.09.26-dd393fe. Authentication succeeded via the CLI; no credential files were read.
- Empty temporary workspace, ask mode, sandbox enabled, no force mode. Prompt instructed the agent to use no tools, files or network research.
- First attempt selected composer-2.5 and failed before generating a response: Named models unavailable; Free plans can only use Auto. This is an observed CLI entitlement, not proof the hackathon grant is absent.
- Retried the same prompt with Auto. Successful exit 0, 8.91 seconds wall time, CLI-reported API duration 7.335 seconds.
- Reported usage: 13,348 input tokens, 571 output tokens, 512 cache-read tokens, zero cache-write tokens. No monetary cost or grant attribution was included.
- Request ID: 0dd8edd2-a092-47f5-a5a0-9b23fffcf5b9.
- Artifacts: /tmp/housing-cursor-probe-grhiy148. Workspace remained empty. Neither application repository nor research source files were exposed as the probe workspace.

## Input and inspection

Input: Fix up the house, finish the basement, and maybe add a bedroom out back.

The response distinguished definite repair and basement work from a tentative rear bedroom, left both unit counts null and ground disturbance unknown, and made no permission or feasibility claim. The JSON envelope and the result's JSON object parsed successfully. This was prompt-requested JSON, not a tested schema-enforced API contract.

The next question asked whether the rear bedroom involved new construction/digging/foundation work or work inside the existing house. This is relevant, though the basement's potential separate-dwelling status was not raised in its unresolved-question list. One example cannot establish reliable coverage, calibrated uncertainty or which question should be prioritized.

## Limits and recommendation

Local CLI access and one meaningful intake response are verified. The actual model behind Auto, SDK/cloud access, hosted-app suitability, repeatability, edge-case behavior and the specific grant's billing remain unverified. The short prompt incurred substantial reported input-token overhead, but a baseline was not measured, so no exact overhead attribution or dollar cost is claimed.

Check the Cursor usage dashboard for this request and grant balance before expanding testing. A zero cash charge alone cannot distinguish grant-funded from plan-included usage. No additional requests were run. Do not treat the CLI test as proof that the deployed app can call a raw model endpoint through Cursor.
