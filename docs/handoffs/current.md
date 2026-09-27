# Current handoff: resumed work and split publication

September 26, 2026, Eastern. The user resumed work after the deployed checkpoint and authorized focused branches and PRs for the corrected walkthrough, source integration and wiki updates. The earlier stop instructions are historical. Preserve all existing app, explorer and proposal-comparison work. This handoff records the local state before the new publication branches are pushed.

## For Humans

The public site at https://ai-housing-navigator.vercel.app/projects/new is still the older manual Vercel deployment built from app commit `12ee746`. It supports guided parcel selection and bounded public-record checks. The corrected walkthrough and expanded source work are local, not hosted. The user rejected the old Review and Next actions experience; functional fixes and passing checks do not imply design acceptance.

The latest accepted scoring policy is [ADR 0008](../adr/0008-gate-preliminary-scoring-on-complete-evidence.md): withhold every numeric Development Ease Score and range until all required rubric factors are assessed. Current coverage is incomplete. Public records, map intersections, source metadata and completed form fields do not establish feasibility or permission. Jev is not integrated. The optional local intake uses configured DeepSeek through OpenRouter; hosted AI is disabled. No paid model call or credential inspection was made for this source work.

The organizer catalog has 60 entries. A bounded local source audit classified 36 as retrievable source or context data, 7 as public metadata only, and 17 as without retrievable data in this adapter set. These categories do not mean that all 60 underlying datasets are ingested or that their records apply to a selected parcel. The app's local `docs/source-coverage.md` distinguishes exact-parcel records, mapped observations, regional aggregates, reference documents and gaps.

## For Agents

### Repositories and publication

- App original checkout: `/home/het/personal/ai-housing-navigator`, `feat/clear-project-results`, pushed head `40ad242`. That checkout also contains uncommitted walkthrough, backend, docs and source work. Preserve it. The existing app draft PR #3 does not include the local changes. Separate worktrees carry the walkthrough recovery, property explorer and proposal comparison; verify their current heads before publishing.
- Walkthrough recovery: isolated verification of parcel correction, saved-stage resume and honest unrun/error results passed 117 tests plus typecheck, lint, build and guided/property/screening browser regressions before the PR split. Keep the four UI components and three browser scripts together. Backend source observations are a separate change. The corrected UI is not deployed.
- Backend source integration: the original checkout reached a local checkpoint with 188 tests passing. `GET /api/sources` describes all 60 catalog rows and `POST /api/sources/query` returns source-specific bounded outcomes. Supplementary permit and City map observations remain separate from the seven required screening checks. Re-run full checks on the final isolated branch before publication; no complete 60-dataset claim follows from route coverage.
- Wiki: design PR #4 last had published head `f08196d`. The local finance and illustrative-intro amendment is commit `d1ca0da`, based on `f08196d`. This scoring-policy and handoff update is stacked after that amendment in an isolated `/tmp` checkout. Neither local wiki layer is published by this handoff. Keep ADR 0007 proposed, preserve historical ADR text and do not mistake publication for implementation approval.
- Deployment: Vercel production deployment `dpl_EYscUyX6Rgo9hPrru49SWkFh5nLx` built app commit `12ee746`. No new deployment was made. GitHub-to-Vercel automatic linking was not verified; a branch push does not imply deployment.

### Product and evidence boundaries

Countywide intake accepts combinations of housing work, while Pittsburgh-only rules apply only after the whole parcel municipality is resolved. The current score remains null because zoning, process, infrastructure and other required factors are not completely assessed. Keep source dates and unknowns explicit. A PLI permit match is history, a mapped flag is map evidence, and a zero intersection is not a site clearance. Regional financial indexes, survey rates and listing aggregates are context, not a project budget, comparable sale, appraisal or financing offer.

Supabase Auth and cloud project storage are not connected. Drafts remain on the device. The historical Lanark comparison is not a live fallback. The explorer and proposal-comparison worktrees contain separate future UI work and must not be folded into the walkthrough or source PRs.

### Next actions

1. Finish isolated review and publish focused app walkthrough and source PR branches only after their final checks. Keep screening source-observation code with the source PR.
2. Publish the wiki finance and visual amendment from `d1ca0da` as its own PR based on `f08196d`, then publish ADR 0008, ADR currency and this handoff as a stacked PR. Do not push wiki main directly.
3. Compare each published PR head with these local snapshots. Update this handoff with actual PR links, verification and any deployment only after those events occur.
4. Continue source-specific gaps without claiming full feasibility coverage. Do not make paid AI calls or move credentials as part of this work.

The prior deployed and paused checkpoint is preserved in [the dated snapshot](2026-09-26-paused-deployed-checkpoint.md). Earlier technical-design and pre-deployment handoffs remain historical records.
