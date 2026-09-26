# Handoff snapshot: discovery setup, September 26, 2026

Updated: 2026-09-26. Stage: brainstorming and discovery. Product implementation has not started.

## For Humans

Het and Rushi are a two-person team. Track 1 is selected. Het has Saturday and Sunday, with submission due September 27 at 11:59 p.m. Eastern. We want a usable Pittsburgh housing product that fits practitioners' existing workflow. A nonprofit site-screening assistant is a hypothesis; target user, features and stack are not approved.

Deep Research is running in Het's separate ChatGPT session. Wait for or ask about its result; do not start another broad research report. Continue discussing real workflow, value, outputs and the smallest useful product in parallel.

## For Agents

### Read next

1. Root `AGENTS.md` and `docs/adr/README.md`.
2. `wiki/product/context-start.md` for compact research context.
3. Only the relevant topic/source section for the question at hand.

### Confirmed context

- Rushi supplied the long housing systems research. Its PDF and original Markdown overlap.
- Het works with nonprofit software, has no pre-existing housing-nonprofit relationships, and does not want a standalone analytics tool.
- Local design should be Pittsburgh-specific in data, jurisdiction, workflow and visual identity. Local Easter eggs are optional finishing details.
- Private customer conversations are outside this repository. Do not request or ingest them as wiki material.
- The $75 Cursor event credit is treated as development budget. Runtime model-provider funding is not established; event terms have not been independently confirmed.
- Participant Packet requires one track, public app repository, intact event-time code history, citations/tool disclosures, limitations and a public 3-5 minute demo. Six judging criteria have no specified weights.

### What exists

- Public research repo: https://github.com/het-sheth/ai-housing-hackathon-wiki . Local path: /home/het/personal/ai-housing-hackathon-wiki . No application repo yet.
- Initial research imported through PR #1, merged. Rushi (Baburaoooo) invited with write permission; last verified state was pending.
- Current follow-up branch: `docs/track-one-discovery`. Inspect Git status before editing; it contains the subsequent prompt, source conversions, ADRs and handoff work.
- Original eight downloads in `raw/hackathon/`; SHA-256 manifest records provenance. Five PDFs cover 62 pages. Two data catalog CSVs are identical, with 60 entries.
- Full page-marked PDF text and embedded hyperlinks in `raw/markdown/`; extraction checks preserve all non-whitespace characters from pdftotext. Layout-dependent tables/figures still need original PDF inspection.
- Curated catalog resource pages, three-track comparison, rules, Rushi interpretation, source corrections and open questions in `wiki/`.
- Copyable research prompt: `docs/deep-research-prompt.txt`. It is an assignment, not verified findings.
- Downloaded packet contains original Meet links but no separate recording link. An updated packet or direct organizer link is still needed.

### Data evidence and limits

Six priority source landing pages were checked, but no record-level data integration is proven. Current WPRDC slugs are `allegheny-county-parcel-boundaries1` and `zoning`; original catalog URLs remain preserved. Permit does not mean completed home; missing data does not mean no constraint. The report contains explicitly illustrative financial/delay figures. Current rules and financial assumptions need source verification before product use.

### Experience evidence

Available local repository history was inventoried; nine relevant projects' manifests and selected commits were read. Repeated patterns include React/TypeScript, Next.js, Tailwind/shadcn, Python/FastAPI and API integrations. Do not equate commit counts or dependency lists with expertise, deployment success or current preference. Rushi's technical responsibilities remain to be clarified. Do not reuse prior project code.

### Agent documentation

AGENTS.md, CLAUDE.md and the getting-started pages now describe this housing project. Old template implementation plans were removed. Template origin remains recorded as provenance.

### Next steps

1. Continue brainstorming the actual practitioner and decision; no further track-selection question is needed.
2. Ingest the finished Deep Research selectively: extract new verified facts, disagreements and decisions rather than loading the whole corpus again.
3. Validate a narrow workflow with housing experts or an actual prospective user; no interviews have been completed or endorsements obtained.
4. Define the minimum input, useful output, supported cases, failure behavior and how it fits current tools.
5. Test a small parcel-to-zoning/hazard join before promising broad coverage.
6. Select architecture and create the application repository only after product scope is agreed. Better T Stack remains an option.

### Verification and publication

Latest documentation check: `npm run check`, 74 concepts, 0 problems. Latest full test run: `npm test` outside the sandbox, 40 passed, exit 0. Full source extraction checks passed for all five PDFs. Sandboxed subprocess tests intermittently reported empty stdout/stderr and failures even with a TTY. The same suite passed outside the sandbox. Do not weaken tests to hide an execution-environment problem.

Run `git status --short` and inspect remotes to establish current publication state. Do not assume uncommitted local notes are on GitHub. Update this section when checks or publication change. Preserve immutable raw files; whitespace-only changes to original sources are not cleanup tasks.

### Resume prompt

Read AGENTS.md, docs/handoffs/current.md and docs/adr/README.md in /home/het/personal/ai-housing-hackathon-wiki. Continue Track 1 product brainstorming for Het and Rushi. Scope and stack remain open. Ask whether the separate Deep Research has finished, then address the next concrete workflow question. Load source sections selectively. Maintain ADRs and this handoff. Do not begin application implementation without an agreed design.
