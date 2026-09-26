# Current handoff: technical design ready for review

Updated September 26, 2026. Stage: accepted product decisions and proposed technical design prepared for wiki publication; application implementation has not begun for the expanded design.

## Resume here

1. Read [the technical design](../technical-design-v1-2026-09-26.md), [source verification and C01-C12 inventory](../source-adapter-verification-2026-09-26.md), then [the phased implementation plan](../implementation-plan-v1-2026-09-26.md).
2. Treat [the product specification](../product-spec-v1-2026-09-26.md), [dated decision log](../product-decisions-2026-09-26.md) and [ADR 0006](../adr/0006-select-action-led-v1.md) as the accepted product record. [ADR 0007](../adr/0007-propose-persisted-workflow-architecture.md) is proposed architecture, not approval.
3. First implementation slice for review: typed broad activity/status contracts, fenced Lanark evaluator and recoverable guided local draft at `/projects/new`, preserving `/` and `/design-system`. No material product question blocks review. Obtain implementation direction before coding this expanded scope.

## State and publication

Research repository: `/home/het/personal/ai-housing-hackathon-wiki`, branch `docs/technical-design-v1` at this handoff update. Existing specification, decisions, ADR and research work plus new design/plan/evidence remain local and uncommitted until the pending publication batch is committed. Preserve all tracked and untracked work. Recheck branch/status before publication. [Wiki PR #3](https://github.com/het-sheth/ai-housing-hackathon-wiki/pull/3) merged September 26, 2026 at 20:13:53 UTC, merge commit `0aaec10`. The user authorized publication of this design batch through a new wiki PR; that publication is in progress, not complete at this update. Application publication completed: [public feature branch](https://github.com/het-sheth/ai-housing-navigator/tree/feat/first-prototype), [PR #1](https://github.com/het-sheth/ai-housing-navigator/pull/1), verified remote head `128aec4fc68e0c6639ada881f3ad2264857cad22`. App main remains the GitHub-generated README baseline; no push to main occurred. `Baburaoooo` has a write invitation pending acceptance at last check. Do not claim accepted collaborator access or send a duplicate invitation.

Application repository: `/home/het/personal/ai-housing-navigator`, branch `feat/first-prototype`, baseline inspected at `6288d5a`, published prototype head `128aec4` before this documentation update; application source was left unchanged. Publication added the four existing interview/research notes and a dated app handoff update, and joined the GitHub README baseline into the feature branch. It retains Lanark-only conditional evaluation, comparisons, Markdown/print export, design preview and one exact-assessment adapter. Runtime AI, generic countywide identity, durable drafts, accounts and task continuation remain unimplemented. No expanded-design infrastructure was provisioned or deployed. No new purchases were made. No merge or deployment occurred. Current app documentation edits are in progress; recheck Git state before any further publication.

The previous handoff is preserved in [the pre-design snapshot](2026-09-26-before-technical-design.md). Historical deployment requests and comparison-first suggestions do not supersede current instructions. The accepted scope makes assessment and prioritized actions primary, comparison secondary, and selects React/TypeScript/Vite, Supabase Postgres/Auth and planned Vercel. ADR 0007 remains proposed. The user explicitly requested bounded subagent use/reuse and lean parent context; continue with short focused assignments instead of broad context duplication.

## Findings and real release blockers

Actual public GET probes confirmed sampled assessment, parcel, municipality, zoning and City PLI responses, including unfamiliar Mountford and Sharpsburg fixtures. Mailing city PITTSBURGH does not establish City jurisdiction. API samples establish neither countywide reliability nor full polygon containment. See [probe evidence](../evidence/technical-design-2026-09-26/README.md).

1. Verify whole-polygon municipal coverage, boundary/multipart cases and complete authoritative municipality crosswalk before generic identity claims.
2. Resolve parcel, municipality, zoning and optional slope reuse terms before public geometry display/cache. No permitted substitute is verified.
3. Review Pittsburgh rule versions/dependencies. Certificate language in code and City dwelling guidance cannot be reduced to a universal certificate requirement; keep lawful-use evidence as a human task.
4. Validate an actual OpenRouter model/provider endpoint, strict schema and hard spending limits before runtime AI. No paid probe occurred here. Existing reported balances are separate; Cursor hosted suitability remains unverified.
5. Configure Supabase/Auth, approved email delivery/callbacks, retention/backups and later authorized hosting. Test owner isolation, task outcomes and deployed auth/source behavior before durable public launch.

A two-person weekend demo can target the local assessment/action flow with a bounded AI integration. It cannot honestly claim the full accepted launch minimum before these gates. Practitioner demand remains unvalidated. The plan specifies questions and a concrete pivot gate if the handoff adds no useful task or reviewer value.

## Verification

Fresh application verification during this handoff: 41 unit tests, typecheck, lint and production build each passed. Prior browser verification remains historical; it was not re-run this phase. Documentation check passed with 79 concepts and zero problems; `git diff --check` passed. The known sandbox subprocess failure recurred for `npm test`; the same suite passed outside the sandbox with 40 tests. Main design and source contracts received bounded subagent review; corrected parcel-ID length, ArcGIS completeness guards, source-evidence qualifications, privileged RPC identity binding, embedded-reference authorization and operational database prerequisites. No live deployed behavior is claimed.

## Resume prompt

Read this repository's AGENTS.md, then the accepted product spec and decisions, the three linked design/source/plan documents, and ADR 0007. Preserve existing unfinished work and keep application changes in the separate app repository. Do not reopen accepted personas, geography, activity intake, personal ownership, 2D, no-score, Supabase or outage behavior. Review the first implementation slice without coding until authorized. Before publication, inspect Git state and the latest user instructions. Wiki PR #3 is merged and the current design batch is authorized for a new wiki PR; verify that PR's actual state before claiming publication. Source/rule/model/auth prerequisites remain explicit release gates.
