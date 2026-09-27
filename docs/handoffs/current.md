# Current handoff: resumed work and split publication

September 26, 2026, Eastern. The user resumed work after the deployed checkpoint and authorized focused branches and PRs for the corrected walkthrough, source integration and wiki updates. The earlier stop instructions are historical. Preserve all existing app, explorer and proposal-comparison work. Two wiki and nine app branches are published as focused draft PRs. No new merge or deployment occurred.

## For Humans

The public site at https://ai-housing-navigator.vercel.app/projects/new is still the older manual Vercel deployment built from app commit `12ee746`. It supports guided parcel selection and bounded public-record checks. The corrected walkthrough and source adapters are published for review in separate draft PRs; none of those changes is hosted. The user rejected the old Review and Next actions experience; functional fixes and passing checks do not imply design acceptance.

The latest accepted scoring policy is [ADR 0008](../adr/0008-gate-preliminary-scoring-on-complete-evidence.md): withhold every numeric Development Ease Score and range until all required rubric factors are assessed. Current coverage is incomplete. Public records, map intersections, source metadata and completed form fields do not establish feasibility or permission. Jev is not integrated. The optional local intake uses configured DeepSeek through OpenRouter; hosted AI is disabled. No paid model call or credential inspection was made for this source work.

The organizer catalog has 60 entries. The final bounded source probe classified 35 as scoped source or context paths, 7 as public metadata paths, and 18 as no-data outcomes in this adapter set. These categories do not mean that all 60 underlying datasets are ingested or that their records apply to a selected parcel. USGS elevation first returned a transient error, then succeeded on one retry; the Pittsburgh zoning code page returned HTTP 403 to the bounded request. [App documentation PR #12](https://github.com/het-sheth/ai-housing-navigator/pull/12) records the architecture, flow, per-source scope and limits.

## For Agents

### Repositories and publication

- App original checkout: `/home/het/personal/ai-housing-navigator`, `feat/clear-project-results`, pushed head `40ad242`. That checkout also contains uncommitted walkthrough, backend, docs and source work. Preserve it. Existing app draft PR #3 does not include these changes. The focused app drafts are [#4 catalog](https://github.com/het-sheth/ai-housing-navigator/pull/4), [#5 walkthrough](https://github.com/het-sheth/ai-housing-navigator/pull/5), [#6 parcel queries](https://github.com/het-sheth/ai-housing-navigator/pull/6), [#7 screening observations](https://github.com/het-sheth/ai-housing-navigator/pull/7), [#8 regional context](https://github.com/het-sheth/ai-housing-navigator/pull/8), [#9 spatial sources](https://github.com/het-sheth/ai-housing-navigator/pull/9), [#10 GTFS](https://github.com/het-sheth/ai-housing-navigator/pull/10) and [#11 NCES](https://github.com/het-sheth/ai-housing-navigator/pull/11). Explorer and proposal comparison remain separate worktrees.
- Walkthrough recovery: isolated verification of parcel correction, saved-stage resume and honest unrun/error results passed 117 tests plus typecheck, lint, build and guided/property/screening browser regressions. App PR #5 keeps the four UI components and three browser scripts together. Backend source observations are a separate change. The corrected UI is not deployed.
- Backend source integration: backend head `e2d91aa` combined with walkthrough head `046ac96` passed 195 tests, typecheck, lint and build. Published app PR #4 lists all 60 catalog rows as metadata and labels its existing runtime subset. Later draft PRs add source-detail queries and supplementary permit and City map observations, separate from the seven required screening checks. The earlier 188-test local checkpoint is historical. No complete 60-dataset claim follows from route coverage.
- Wiki: design PR #4 last had published head `f08196d`. The finance and illustrative-intro amendment at `d1ca0da` is [wiki draft PR #5](https://github.com/het-sheth/ai-housing-hackathon-wiki/pull/5), based on that design branch. Accepted ADR 0008, ADR currency and this handoff are stacked in [wiki draft PR #6](https://github.com/het-sheth/ai-housing-hackathon-wiki/pull/6). Neither is merged. Keep ADR 0007 proposed, preserve historical ADR text and do not mistake publication for implementation approval.
- Deployment: Vercel production deployment `dpl_EYscUyX6Rgo9hPrru49SWkFh5nLx` built app commit `12ee746`. No new deployment was made. GitHub-to-Vercel automatic linking was not verified; a branch push does not imply deployment.

### Product and evidence boundaries

Countywide intake accepts combinations of housing work, while Pittsburgh-only rules apply only after the whole parcel municipality is resolved. The current score remains null because zoning, process, infrastructure and other required factors are not completely assessed. Keep source dates and unknowns explicit. A PLI permit match is history, a mapped flag is map evidence, and a zero intersection is not a site clearance. Regional financial indexes, survey rates and listing aggregates are context, not a project budget, comparable sale, appraisal or financing offer.

Supabase Auth and cloud project storage are not connected. Drafts remain on the device. The historical Lanark comparison is not a live fallback. The explorer and proposal-comparison worktrees contain separate future UI work and must not be folded into the walkthrough or source PRs.

### Next actions

1. Review app draft PRs #4 through #12 in their stated dependency order. Use the [published review map](https://github.com/het-sheth/ai-housing-navigator/blob/docs/source-architecture-flow/docs/pr-stack.md); walkthrough PR #5 is a sibling of the source stack.
2. Review wiki draft PR #5 before its stacked policy PR #6. Keep ADR 0007 proposed and do not push wiki main directly.
3. Compare each later PR head with these local snapshots. Update this handoff with actual merge, verification or deployment events only after they occur.
4. Continue source-specific gaps without claiming full feasibility coverage. Do not make paid AI calls or move credentials as part of this work.

The prior deployed and paused checkpoint is preserved in [the dated snapshot](2026-09-26-paused-deployed-checkpoint.md). Earlier technical-design and pre-deployment handoffs remain historical records.
