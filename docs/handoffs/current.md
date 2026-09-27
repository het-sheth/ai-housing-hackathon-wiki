# Current handoff: resumed work and split publication

September 26, 2026, Eastern. The user resumed work after the deployed checkpoint and authorized focused branches and PRs for the corrected walkthrough, source integration and wiki updates. The earlier stop instructions are historical. Preserve all existing app, explorer and proposal-comparison work. Two wiki and two app branches are now published as draft PRs; remaining source branches are under independent review. No new merge or deployment occurred.

## For Humans

The public site at https://ai-housing-navigator.vercel.app/projects/new is still the older manual Vercel deployment built from app commit `12ee746`. It supports guided parcel selection and bounded public-record checks. The corrected walkthrough is published for review, and expanded source work is split across published and still-local branches; none of it is hosted. The user rejected the old Review and Next actions experience; functional fixes and passing checks do not imply design acceptance.

The latest accepted scoring policy is [ADR 0008](../adr/0008-gate-preliminary-scoring-on-complete-evidence.md): withhold every numeric Development Ease Score and range until all required rubric factors are assessed. Current coverage is incomplete. Public records, map intersections, source metadata and completed form fields do not establish feasibility or permission. Jev is not integrated. The optional local intake uses configured DeepSeek through OpenRouter; hosted AI is disabled. No paid model call or credential inspection was made for this source work.

The organizer catalog has 60 entries. A bounded local source audit classified 36 as retrievable source or context data, 7 as public metadata only, and 17 as without retrievable data in this adapter set. These categories do not mean that all 60 underlying datasets are ingested or that their records apply to a selected parcel. The app's local `docs/source-coverage.md` distinguishes exact-parcel records, mapped observations, regional aggregates, reference documents and gaps.

## For Agents

### Repositories and publication

- App original checkout: `/home/het/personal/ai-housing-navigator`, `feat/clear-project-results`, pushed head `40ad242`. That checkout also contains uncommitted walkthrough, backend, docs and source work. Preserve it. Existing app draft PR #3 does not include these changes. The catalog registry is in [app draft PR #4](https://github.com/het-sheth/ai-housing-navigator/pull/4); the corrected walkthrough is in [app draft PR #5](https://github.com/het-sheth/ai-housing-navigator/pull/5). Explorer and proposal comparison remain separate worktrees.
- Walkthrough recovery: isolated verification of parcel correction, saved-stage resume and honest unrun/error results passed 117 tests plus typecheck, lint, build and guided/property/screening browser regressions. App PR #5 keeps the four UI components and three browser scripts together. Backend source observations are a separate change. The corrected UI is not deployed.
- Backend source integration: the original checkout reached a local checkpoint with 188 tests passing. Published app PR #4 lists all 60 catalog rows as metadata and labels its existing runtime subset. Source-detail queries and supplementary permit and City map observations remain in separately reviewed work. These observations remain separate from the seven required screening checks. Re-run full checks on each final isolated branch before publication; no complete 60-dataset claim follows from route coverage.
- Wiki: design PR #4 last had published head `f08196d`. The finance and illustrative-intro amendment at `d1ca0da` is [wiki draft PR #5](https://github.com/het-sheth/ai-housing-hackathon-wiki/pull/5), based on that design branch. Accepted ADR 0008, ADR currency and this handoff are stacked in [wiki draft PR #6](https://github.com/het-sheth/ai-housing-hackathon-wiki/pull/6). Neither is merged. Keep ADR 0007 proposed, preserve historical ADR text and do not mistake publication for implementation approval.
- Deployment: Vercel production deployment `dpl_EYscUyX6Rgo9hPrru49SWkFh5nLx` built app commit `12ee746`. No new deployment was made. GitHub-to-Vercel automatic linking was not verified; a branch push does not imply deployment.

### Product and evidence boundaries

Countywide intake accepts combinations of housing work, while Pittsburgh-only rules apply only after the whole parcel municipality is resolved. The current score remains null because zoning, process, infrastructure and other required factors are not completely assessed. Keep source dates and unknowns explicit. A PLI permit match is history, a mapped flag is map evidence, and a zero intersection is not a site clearance. Regional financial indexes, survey rates and listing aggregates are context, not a project budget, comparable sale, appraisal or financing offer.

Supabase Auth and cloud project storage are not connected. Drafts remain on the device. The historical Lanark comparison is not a live fallback. The explorer and proposal-comparison worktrees contain separate future UI work and must not be folded into the walkthrough or source PRs.

### Next actions

1. Review app draft PRs #4 and #5 independently. Finish isolated review of the remaining source branches, keeping screening source-observation code with the source PR.
2. Review wiki draft PR #5 before its stacked policy PR #6. Keep ADR 0007 proposed and do not push wiki main directly.
3. Compare each later PR head with these local snapshots. Update this handoff with actual merge, verification or deployment events only after they occur.
4. Continue source-specific gaps without claiming full feasibility coverage. Do not make paid AI calls or move credentials as part of this work.

The prior deployed and paused checkpoint is preserved in [the dated snapshot](2026-09-26-paused-deployed-checkpoint.md). Earlier technical-design and pre-deployment handoffs remain historical records.
