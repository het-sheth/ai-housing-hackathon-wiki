# Current handoff: deployed checkpoint, work paused

September 26, 2026, Eastern. The user explicitly stopped all implementation and requested handoff/wiki updates before leaving. Resume only on user direction. Implementation and review agents were interrupted; preserve their unfinished work.

## For Humans

The website is live at https://ai-housing-navigator.vercel.app/projects/new . County property search, explicit parcel confirmation, real mapped boundaries and assessments work. A bounded Pittsburgh screen queries municipality, zoning, mapped slope and FEMA flood observations. Required checks remain missing, so no Development Ease Score is shown. Hosted AI is explicitly disabled. Accounts and cloud project storage are not connected.

The user rejects the walkthrough after Key questions, including Review and Next actions. Latest concrete defects: no obvious parcel correction action, generic tasks displayed before checks run, and a saved parcel appearing as a generic regional map because its geometry was not reloaded. Fixes are partially written locally, not deployed or verified. This checkpoint is not UI acceptance or complete feasibility coverage.

Latest scoring decision supersedes the older blanket no-score preference: Pittsburgh proposals first, with an explainable rubric, and no numeric result until all required factors are assessed. See [ADR 0008](../adr/0008-gate-preliminary-scoring-on-complete-evidence.md). Jev is not integrated. Noul is a yes/no probability primitive; Score is an ordered rubric primitive. Neither supplies missing records or an approval probability.

## For Agents

### Repositories and publication

- App: `/home/het/personal/ai-housing-navigator`, `feat/clear-project-results`, pushed head `40ad242`; application deployment built `12ee746`. [Draft PR #3](https://github.com/het-sheth/ai-housing-navigator/pull/3) is open, not merged. Earlier app PR #1 and #2 are merged. Never push main directly.
- Vercel: `hets-projects-aab6adc0/ai-housing-navigator`, deployment `dpl_EYscUyX6Rgo9hPrru49SWkFh5nLx`, production READY. Automatic GitHub linking failed; deployment succeeded manually through CLI. Do not assume pushes auto-deploy.
- Explorer: pushed `feat/property-explorer` at `2c5937e`, clean worktree `/tmp/ai-housing-property-explorer`. Scope document only; base predates the finished walkthrough. Planned flow: natural language, user-confirmed criteria, candidate parcels, selection and one-parcel proposal A/B comparison. A useful 3D map is proposed, not built; a mentioned reference screen was not attached.
- Wiki: `docs/technical-design-v1`, already ahead of origin by one commit with an existing modified handoff before this update. Preserve that work. This update does not push or merge the wiki. Remote wiki PR state was not rechecked during the stop.

### Preserved unfinished app changes

`src/features/projects/GuidedProject.tsx`, `PropertyStep.tsx`, `ResultsStep.tsx` and `SiteContextMap.tsx` have uncommitted edits. They add Change parcel/Edit proposal, clear stale parcel observations while preserving proposal answers, separate unrun/loading/error/incomplete states, suppress generic tasks before actual checks and show saved identity with explicit map loading. App handoffs and completion plan are also modified. Agents were stopped before completing browser scripts, fresh checks and final review. Do not claim this diff passes or is hosted.

Last verified deployed checkpoint: 117 tests, typecheck, lint and build passed. Hosted isolated Chromium confirmed Mountford search, explicit parcel selection, real boundary/assessment and pending screening with no numeric point fields. Desktop and 390px maps rendered without overflow or page errors; zero AI calls. These results do not validate the unfinished correction above.

### Evidence, AI and safety boundaries

The organizer supplied a 60-entry source catalog, not a fully ingested parcel database. Implemented live adapters use WPRDC assessments, County parcel/municipality services, City zoning/slope and FEMA flood services. Whole-parcel ambiguity, source failures and unknown dates remain explicit. Broader zoning, undermining, review process, utilities and finance remain unassessed. Historical Lanark is retained only as a labeled comparison/example; no live fallback.

Configured local model remains DeepSeek V4 Flash 0731 via OpenRouter, with the accepted $3 weekly key limit inside the $10 lifetime budget guard. One earlier paid request exposed an interpretation problem; the corrected prompt has not been verified with another paid request. A second attempt was blocked by automatic approval review, so renewed explicit approval is required. Hosted AI makes no provider calls. Do not inspect credentials or change the model.

The local API was accidentally restarted during property tests with bare `node server/dev.mjs`, which omitted loading the configured key and could cause the generic AI error. Startup was corrected to `npm run api:dev`. Let the server load credentials; do not read or print credential files. A GET health check does not verify AI interpretation.

### Exact next actions after user resumption

1. Read app AGENTS.md, the PAUSED section in `docs/current.md`, and `docs/walkthrough-completion-plan.md`; verify git state without discarding tracked or untracked work.
2. Inspect the unfinished parcel/result diff. Complete saved-map reload error handling, input preservation and stale-request behavior. Update meaningful browser regressions for changed states and labels.
3. Run all four app checks and isolated browser verification, then read-only review. Do not equate a functional fix with acceptance of the rejected Review/Next actions design.
4. Keep explorer work separate. Do not restart discovery or an old Lanark audit. Use Sol for implementation/review and Luna only for bounded support with clear current task names.
5. No deployment, publication, paid AI test or further feature work while paused. Resume only under the user's next instruction.

Resume prompt: Continue from the paused app diff and this handoff. Preserve both feature branches and unfinished work. Fix parcel correction and honest unrun results first; do not invent scores, change models or inspect credentials. Confirm the user has resumed work before acting.

Prior handoff, including pre-existing local edits, is preserved in [the snapshot](2026-09-26-before-deployed-checkpoint.md). Older product and implementation statements there are historical where superseded here.

### Sources

- [TypeSafe primitive documentation](https://docs.typesafe.ai/primitives)
- [App draft PR #3](https://github.com/het-sheth/ai-housing-navigator/pull/3)
- [Source verification](../source-adapter-verification-2026-09-26.md)
