# Current handoff: Pittsburgh housing hackathon

Updated: 2026-09-26. Stage: fresh-session execution handoff prepared. Het explicitly requested a new local repo and a quick working prototype with iteration. Latest request is to stop this bloated session after saving a comprehensive build prompt. Do not start the app in this closing session.

**Start the next session with `docs/start-prototype-session.md`.** It is a self-contained execution prompt with source map, exact resource IDs, supported flow, provenance, scope limits and acceptance checks. It directs implementation rather than another discovery phase. The prompt now explicitly assigns Sol to ordinary implementation, Luna to bounded support, and Astra to hard reasoning/review, with at most two child agents active by default. The default is React + TypeScript + Vite unless Het changes it. The initial repo path remains `/home/het/personal/ai-housing-navigator`; no app has been created.

## For Humans

Het and Rushi are building Track 1, Development Feasibility Navigator. Submission is September 27, 2026 at 11:59 p.m. Eastern. Het has Saturday and Sunday; Rushi's availability and preferred responsibilities remain unknown.

Het asked to start building in a new local repository. This authorizes a separate local app start, not publication, deployment or claims of validated demand. The working direction is one Pittsburgh parcel, two supported housing proposals, source-backed zoning differences and a downloadable next-action brief. Detailed supported rules and the scoring rubric still require resolution. ADR 0005 remains a proposed detailed scope, not blanket permission to implement every suggested feature.

React + TypeScript with Vite was recommended as the fastest fit for the current UI scope. Het asked which option would be faster; he has not explicitly selected the stack. Better T Stack is an alternative, not an existing dependency. No app directory, framework scaffold, implementation plan, application code, AI endpoint or app remote has been created. Proposed location: `/home/het/personal/ai-housing-navigator`. Node v25.2.1 and npm 11.6.2 are installed.

## For Agents

### Read next

1. Root `AGENTS.md`, this handoff and `docs/adr/README.md`.
2. `wiki/product/proposal-comparison.md` for the proposed interaction and build boundary.
3. `wiki/product/lanark-worked-example.md` for the real parcel and evidence limitations.
4. `wiki/product/september-26-evidence-update.md` and `wiki/research/action-housing-presentation-excerpts.md` for the latest source findings.

### Repository and publication state

- Research repo: https://github.com/het-sheth/ai-housing-hackathon-wiki . Local: `/home/het/personal/ai-housing-hackathon-wiki`.
- PRs #1 and #2 are merged. Their branches were deleted locally and remotely at Het's request.
- PR #3 is open: https://github.com/het-sheth/ai-housing-hackathon-wiki/pull/3 . It contains the new research, Lanark evidence, proposed ADR 0005 and Rushi message draft.
- Active branch: `docs/proposal-comparison`. The only housing remote branches verified after cleanup were `main` and `docs/proposal-comparison`. Automatic branch deletion after merge is enabled.
- Local main now tracks origin/main. The separate template remote still exists as provenance; it is not another housing product.
- Rushi's GitHub account is Baburaoooo; collaborator invitation acceptance is not verified. No assistant outreach occurred. Whether Het sent the drafted Rushi proposal is unknown.
- Keep the app in a new repository with fresh code. Do not copy previous project implementation or research scripts. Public source facts can inform it with provenance and applicable reuse terms.

### Evidence already established

The full Deep Research export `/home/het/Downloads/deep-research-report.md` was read and reviewed. Its missing reference bibliography and unsupported assumptions are documented in `docs/research-review-and-sme-questions.md`. Do not restart broad research. Original source PDFs/Markdown and duplicated catalog CSVs are not independent corroboration.

User-supplied SME guidance emphasizes zoning and financial feasibility, then explicitly supports doing one dimension well. This is advice, not judging interpretation, demand validation or endorsement. Official links and anonymized paraphrases are in the evidence update. Do not publish raw channel messages or attributed quotes without permission.

Rescope advertises cited parcel rules, overlays, maps and pipeline screening. Static reports substantially overlap; product performance and Pittsburgh coverage are unverified. Proposal comparison is a differentiation hypothesis, not an established unique capability.

Lanark: 1623 LANARK ST, PARID `0023C00208000000`, exact boundary and PLI ID matches. Whole-polygon City zoning/slope queries were performed. R1D-H feature 634 covers the parcel in a bounded vertex/edge test; slope intersects a mapped >=25% feature. Assessment ASOFDATE 2026-09-01 says VACANT LAND while six completed PLI records describe dwelling rehabilitation and later work. Preserve this conflict. Neither source establishes present physical condition or lawful use. Full hazard, title, utilities and financial feasibility are unknown. $300,000 permit value and $197,500 CLT asking price are different quantities; their difference is not a funding gap. See saved records and query scope in `docs/evidence/lanark-2026-09-26/`.

### Exactly what was reviewed from YouTube

After the initial web fetch failed, yt-dlp successfully downloaded YouTube original English automatic captions on September 26. Metadata: uploaded April 16, 2024; duration 71:01. A timestamped transcript was generated in `/tmp/action-housing-video/transcript.txt`; original JSON captions are beside it. Parent and reused agents reviewed the text across the full duration. This is caption analysis, not full audio/visual verification. Do not publish the full transcript. Provenance/hash: `docs/action-housing-video-provenance.json`.

Read `wiki/research/action-housing-video-findings.md` for timestamped findings. Especially relevant: 29-32 minutes, one taller building versus two and community/design tradeoffs; 41 minutes, reported utility delay; 57-58 minutes, schematic design, environmental work and market study as paid diligence artifacts. The case is a multifamily rental project, not validation of a single-home CLT workflow. Funding affects design even if a financial engine is deferred. Current zoning/tax rules must come from current primary authorities, not the 2024 talk.

Captions contain obvious name/number errors. Near 62:49 the speaker says the current example did not have the veterans set-aside on the later slide, so do not merge all slide facts into one project. Screenshots accurately record slide text but lack this clarification. The exact $16.426m budget cannot be reassigned by guessing. Caption discussion dates construction to 2019; costs are not current benchmarks. Original screenshot notes now link the new analysis and preserve their original evidence boundary.

### Build boundary and next actions

1. Resume the authorized app start after incorporating the transcript findings and the pending model clarification. Use a feature branch in the new local repository. Do not request the same permission again.
2. Settle the stack preference if an answer arrives; Vite + React + TypeScript is the recommendation. Record a compact first-slice plan before code. Do not add auth/database/payment infrastructure without need. Keep any eventual provider API key server-side.
3. Complete one precise rule trace before automating a comparison. Use conditional statements, not approval verdicts. Same-use repair and expansion are distinct. Unknown lawful use prevents a definitive permission result; added unit/reconstruction must not accidentally enter the repair pathway.
4. Build the smallest honest interaction: confirm one real site, state proposal, inspect findings, change one supported input, see explained differences, export sources/unknowns. Do not present fixture data as live lookup or deterministic explanations as model-generated AI. AI integration is not yet implemented or selected.
5. Keep financial feasibility unassessed; unknown evidence cannot improve ease. Evidence completeness and social/mission value are separate from ease. A component-only score's acceptance by organizers is unresolved.
6. Rushi could validate a rule trace while Het handles UX/parcel demonstration, subject to his availability. Practitioner utility remains unvalidated. No external reply is required merely to create the local repo, but uncertainty must constrain product claims.

### Reusable agents and rule work

Existing agents: `/root/practitioner` (Sol), `/root/data` (Terra), `/root/alternatives` (Luna). Reuse relevant context rather than launching broad research. The practitioner agent supplied an initial rule contract after app-start authorization; it is captured in `docs/initial-rule-contract.md` and requires review before production logic.

### Verification

This handoff update: wiki check passed with 79 concepts and zero problems (exit 0); all 40 tests passed outside the sandbox (exit 0); git diff --check passed. Sandboxed subprocess tests reproduced the known execution-environment failure. Never weaken assertions to hide it. Run `npm run check` for docs and `npm test` for the publishing guidance batch; record actual exit status. No app tests exist because no app code exists.

### Resume prompt

Preferred complete handoff: `docs/start-prototype-session.md`. Read it and execute the first small local prototype. The text below is historical short context.


Read AGENTS.md and docs/handoffs/current.md in the research repository. Het has authorized starting a separate local application, but asked to update handoffs and explain YouTube findings first. The full automatic-caption text was subsequently retrieved and analyzed, with timestamps and quality caveats; see wiki/research/action-housing-video-findings.md. React/TypeScript/Vite is recommended, not explicitly selected. Preserve the evidence limitations, use fresh app code, and continue a small local build without reopening broad research or asking again whether a new repo is allowed. Keep research PR #3 separate from the app.
