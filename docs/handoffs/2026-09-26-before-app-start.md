# Current handoff: Pittsburgh housing hackathon

Updated: 2026-09-26. Stage: brainstorming and discovery. Product implementation has not started.

## For Humans

Het and Rushi are a two-person team. Track 1 is selected. Het has Saturday and Sunday, with submission due September 27 at 11:59 p.m. Eastern. We want a usable Pittsburgh housing product that fits practitioners' existing workflow. A nonprofit site-screening assistant is a hypothesis; target user, features and stack are not approved.

Deep Research has finished. Het identified `/home/het/Downloads/deep-research-report.md` on September 26. The report was read and compared with targeted primary-source research. Do not restart broad research. Het subsequently posted the revised question himself and supplied SME replies emphasizing financial feasibility, comparable rents/sales, and zoning. The assistant has not contacted anyone. Product scope remains proposed. Do not publish raw channel messages or attributed quotations without permission.

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
- PR #2 was also verified merged on GitHub on September 26. Both research branches are historical merged PR heads; local main still tracks template/main; origin/main was refreshed before this PR. Do not merge or reset blindly. New research is prepared for publication through the proposal-comparison PR.
- Current follow-up branch: `docs/proposal-comparison`. Inspect Git status before editing; it contains the subsequent prompt, source conversions, ADRs and handoff work.
- Original eight downloads in `raw/hackathon/`; SHA-256 manifest records provenance. Five PDFs cover 62 pages. Two data catalog CSVs are identical, with 60 entries.
- Full page-marked PDF text and embedded hyperlinks in `raw/markdown/`; extraction checks preserve all non-whitespace characters from pdftotext. Layout-dependent tables/figures still need original PDF inspection.
- Curated catalog resource pages, three-track comparison, rules, Rushi interpretation, source corrections and open questions in `wiki/`.
- Copyable research prompt: `docs/deep-research-prompt.txt`. It is an assignment, not verified findings.
- Downloaded packet contains original Meet links but no separate recording link. An updated packet or direct organizer link is still needed.

### Data evidence and limits

Initial work checked six priority landing pages. A September 26 bounded agent audit subsequently matched one assessment PARID to parcel pin and queried an interior point against City zoning. See `docs/partial-data-audit-2026-09-26.md`. This commercial test record is not a housing demo candidate, and that earlier audit did not prove whole-parcel zoning/hazard integration or match rates. The subsequent approved Lanark experiment now demonstrates one exact assessment/boundary/permit join plus whole-parcel City zoning and slope checks. See `wiki/product/lanark-worked-example.md` and `docs/lanark-evidence-2026-09-26.md`. Assessment classification conflicts with permit history; legal use, current condition and financial feasibility remain unverified. No general match-rate or full-hazard validation is established. Current WPRDC slugs are `allegheny-county-parcel-boundaries1` and `zoning`; original catalog URLs remain preserved. Permit does not mean completed home; missing data does not mean no constraint. Current rules and financial assumptions need source verification before product use.

### Experience evidence

Available local repository history was inventoried; nine relevant projects' manifests and selected commits were read. Repeated patterns include React/TypeScript, Next.js, Tailwind/shadcn, Python/FastAPI and API integrations. Do not equate commit counts or dependency lists with expertise, deployment success or current preference. Rushi's technical responsibilities remain to be clarified. Do not reuse prior project code.

### Agent documentation

AGENTS.md, CLAUDE.md and the getting-started pages now describe this housing project. Old template implementation plans were removed. Template origin remains recorded as provenance.

### Next steps

Latest: Het requested recording the new information and proposing an idea to Rushi. Read `wiki/product/proposal-comparison.md` and proposed ADR 0005. Supporting SME/official-source findings are in `wiki/product/september-26-evidence-update.md`; screenshot findings in `wiki/research/action-housing-presentation-excerpts.md`. Draft, not sent: `docs/rushi-product-proposal.md`. No product acceptance, Rushi availability or external feedback on this proposal is established.

The manual experiment was approved by Het and completed on September 26. The concrete output is `wiki/product/lanark-worked-example.md`. Review it with a practitioner before approving an application scope. No outreach occurred. Do not restart the example or interpret this approval as permission to implement an app.

1. The revised SME question was posted by Het. Replies support investigating zoning and financial feasibility together, including comps, hard costs and soft costs, particularly for developers/nonprofits. This is expert guidance, not demonstrated demand or a project walkthrough. A follow-up asking whether comps or cost assumptions are harder to obtain was drafted and copied; whether Het posted it is unknown. Rescope and the linked Pittsburgh examples were reviewed. Read `docs/next-product-experiment-2026-09-26.md`, which links the evidence notes. Rescope has substantial overlap; Pittsburgh support and live output remain untested. That manual example has now been completed for 1623 Lanark; the next step is practitioner review of the actual output. No assistant outreach is authorized.
2. Treat the Deep Research as hypotheses: its numbered citations have no bibliography in the export, it does not demonstrate parcel/zoning joins, and several regulatory claims need correction. Preserve the downloaded original. Incorporate SME answers with their evidence type and remaining uncertainty.
3. Validate a narrow workflow through a recent actual case and output review. General SME feedback has been supplied, but no full practitioner interview, endorsement, or product validation is established.
4. Define the minimum input, useful output, supported cases, failure behavior and how it fits current tools.
5. Test a small parcel-to-zoning/hazard join before promising broad coverage.
6. Select architecture and create the application repository only after product scope is agreed. Better T Stack remains an option.

### Verification and publication

September 26 research-review additions: `npm run check` passed, exit 0, 74 concepts and 0 problems. Draft SME questions, corrections, and bounded data audit are local and uncommitted on `docs/track-one-discovery`. No outreach or application implementation. Clipboard delivery failed because the sandbox could not connect to Wayland; the draft remains in the research-review document.

Latest documentation check: `npm run check`, 78 concepts, 0 problems, exit 0. New evidence pages, proposed ADR 0005 and Rushi draft are included in the proposal-comparison PR batch. All 40 tests passed outside the sandbox; the sandbox reproduced the known subprocess failure. No outreach or application implementation occurred. Latest full test run: `npm test` outside the sandbox, 40 passed, exit 0. Full source extraction checks passed for all five PDFs. Sandboxed subprocess tests intermittently reported empty stdout/stderr and failures even with a TTY. The same suite passed outside the sandbox. Do not weaken tests to hide an execution-environment problem.

Run `git status --short` and inspect remotes to establish current publication state. Do not assume uncommitted local notes are on GitHub. Update this section when checks or publication change. Preserve immutable raw files; whitespace-only changes to original sources are not cleanup tasks.

### Resume prompt

Read AGENTS.md, docs/handoffs/current.md and docs/adr/README.md in /home/het/personal/ai-housing-hackathon-wiki. Deep Research is complete and reviewed in docs/research-review-and-sme-questions.md. Continue Track 1 discovery using actual SME answers if supplied. Scope and stack remain open. Do not repeat broad research or treat a proposed brief as an accepted design. Maintain this handoff and keep source claims separate from verified findings.
