# Housing Navigator v1 Implementation Plan

> **For agentic workers:** Het subsequently authorized starting application implementation. Complete the slices in dependency order, with bounded review. This plan was originally a documentation-only handoff; its technical architecture remains proposed.

**Goal:** Extend the existing prototype into a recoverable, proposal-specific evidence and next-action workflow without representing missing coverage as permission.

**Architecture:** Recommended same-origin Vercel Node endpoints, Supabase Postgres/Auth, PostGIS geographic verification and browser IndexedDB drafts. Keep workflows as validated application transitions with relational dependencies. One generative model proposes intake and explanations; deterministic code owns findings and state changes. These engineering recommendations remain subject to design review.

**Tech stack:** Existing React 19, TypeScript, Vite, npm, Vitest and Playwright; selected Supabase Postgres/Auth; planned Vercel. No LangGraph or graph database is needed initially.

**Spec:** [Accepted specification](product-spec-v1-2026-09-26.md), [dated decisions](product-decisions-2026-09-26.md), [technical design](technical-design-v1-2026-09-26.md), [verified adapters and C01-C12 checks](source-adapter-verification-2026-09-26.md).

## Global constraints

- Application changes belong only in `/home/het/personal/ai-housing-navigator`; research and decisions remain in this wiki.
- Preserve tracked and untracked work. Recheck Git status and nearest instructions before implementation. Use feature branches; no main push, new purchase, top-up or public deployment is authorized here. The subsequent application publication and Rushi invitation were separately authorized and completed as recorded in the current handoff; no further invitation or external message is authorized by this plan.
- Preserve all five personas and all ten activity categories, mixed scopes, original wording, tentative intent and unknown answers. Role changes presentation only.
- Countywide identity and assessment plus verified exact-parcel permit coverage and a reviewed Pittsburgh subset remain the accepted launch minimum. A local demo is a smaller milestone, not a redefinition of v1.
- Keep applicability, coverage, finding status, provenance/completeness and task state separate. No averaged score, permission verdict or inferred financial feasibility.
- Keep immutable proposal versions and completed assessment runs; explicit refresh creates a new run. Unsupported proposals must never become repair proposals.
- Unknown legal use stays unknown. No permit record or assessment classification establishes current lawful use by itself.
- Preserve independent 412 identity, actual 2D parcel context, black/gold interaction, progressive evidence disclosure, keyboard access and mobile layouts. A striking procedural Three.js animated intro is authorized as illustration only. Keep it separate from sourced parcel context, label it illustrative and avoid survey, current-building or 3D-site claims. A later Blender GLB remains optional. No packet extraction, shared editing or pro forma work.
- No em dashes or credential inspection. No secrets, full prompts or source bodies in logs.

## Readiness and actual starting point

The current app has `src/App.tsx`, `src/domain.ts`, `src/assessment.ts`, a separate design-system walkthrough and browser scripts. `src/domain.ts` includes Lanark geometry, source snapshots, proposals, evaluator, comparison and Markdown export together. `evaluate(p: Proposal)` has no parcel argument and emits Lanark-specific findings. It must never be invoked for arbitrary parcels. `refreshAssessment` explicitly accepts only Lanark. Inputs currently reset on reload.

Fresh verification in this handoff established 41 passing tests, typecheck, lint and production build. Existing browser results are documented in the application handoff; they are not fresh hosted verification. Supabase, runtime AI, general property resolution and persistent tasks do not exist yet. Existing `/` and `/design-system` remain available while the new workflow is developed.

## Delivery boundary and dependencies

A two-person weekend should target slices 1 and 2 plus a bounded working AI integration from slice 3 if endpoint validation succeeds. That yields a useful local Lanark demonstration with saved device draft, honest assessment/actions, visible confirmed AI suggestions and an export. It does not establish countywide launch, cross-device saving, reviewed legal predicates or production readiness. If AI cannot be validated, label the demonstration a structured guided prototype with unavailable AI; it is not the accepted AI-native launch.

Slices 4-7 complete the launch requirements and release gates. Do not compress source permissions, auth isolation, outcome semantics or countywide verification to claim launch on Sunday. Estimates are sequencing judgments, not delivery promises.

| Slice | Depends on | Reviewable outcome | Suggested work split |
|---|---|---|---|
| 1. Safe local guided foundation | Implementation authorized; design review continues | Broad intake cannot accidentally invoke Lanark rules; recoverable draft | One implementer, one bounded domain/browser reviewer |
| 2. Lanark assessment and action brief | 1 | Primary assessment/actions, eight-pillar gaps, consistent export | UI implementer with domain reviewer |
| 3. Confirmable runtime AI | 1; operational Supabase ledger and restricted budget RPC; endpoint/budget validation | One working model operation end to end | Server/AI work can proceed beside slice 2 |
| 4. Countywide property and exact source evidence | 1; operational Supabase/PostGIS and restricted GIS RPC; geometry/terms gates for publication | Confirmed identity and municipality, assessment, City permit evidence | Source/geometry implementer with fixture review |
| 5. Owner saving and continuation | 1-2; configured Supabase/auth | Save, reopen, record outcomes, preserve versions and refresh | Data/auth implementer with independent isolation tests |
| 6. Reviewed checks and launch integration | 3-5; rule review | Bounded City checks, explicit gaps elsewhere, full accepted journey | Joint review of evidence and behavior |
| 7. Authorized hosted verification | 6; release prerequisites and later deployment authority | Hosted auth/source behavior proven | One deployer, one independent verifier |

## Common execution contract

For each slice, first add its named behavior tests and establish that new assertions fail for the intended missing behavior. Implement only that slice, then require exit code 0 from `npm test`, `npm run typecheck`, `npm run lint` and `npm run build`. Browser changes also require the relevant existing smoke suites and the new flow suite with a running local server. A test that tolerates source unavailability is a resilience check, not a successful live-connector gate. Keep actual live probe results separate from fixtures.

Paths below are proposed application paths, not files created in this documentation phase. Use the technical design's canonical types and wire contracts. Names below define internal TypeScript boundaries; endpoint handlers translate to those contracts. Preserve existing prototype imports with a facade until its regression tests pass.

## Slice 1: Recoverable local guided foundation

**Files:** Create `src/features/projects/contracts.ts`, `src/features/projects/draft-store.ts`, `src/features/projects/flow.ts`, `src/features/projects/GuidedProject.tsx`, `src/features/projects/contracts.test.ts`, `src/features/projects/draft-store.test.ts`, `src/features/projects/flow.test.ts`, `src/fixtures/lanark.ts`, `src/checks/lanark.ts`, `scripts/guided-flow-smoke.mjs`. Modify `src/domain.ts`, `src/main.tsx` and `package.json` only where needed for the seam and new route.

**Interfaces:** `parseProposalDraft(input: unknown): ValidationResult<ProposalDraft>`; `saveDraft(draft: LocalDraft): Promise<void>`; `loadDraft(id: string): Promise<LocalDraft | null>`; `clearDraft(id: string): Promise<void>`; `transition(state: FlowState, event: FlowEvent): TransitionResult`; `evaluateLanark(proposal: ConfirmedProposal, evidence: LanarkEvidence): AssessmentDraft`. Validation errors are typed field errors, never silent coercions. `LocalDraft` includes schema version, local ID, role/current decision, property selection, original wording, structured suggestions/confirmation, unknowns, current step and last successful save time.

- [ ] Add contracts tests that retain mixed demolition/addition/site work, tentative alternatives, unknown counts and all personas. Negative, fractional and nonfinite unit counts fail; string parcel IDs retain all leading zeros.
- [ ] Add evaluator guard tests: a different parcel, unmatched snapshot or unsupported scope cannot emit Lanark-specific conflict/zoning/slope findings. The old default comparison still has zero review-status and next-action changes.
- [ ] Extract the fixture and narrow evaluator behind the existing facade. Keep unsupported activity selections intact and return explicit unsupported scope rather than convert them to repair.
- [ ] Implement `/projects/new`: role/current decision, property confirmation, description and visible activity selections, relevant single clarification, proposal confirmation. The local demo clearly limits assessment to the Lanark fixture. Other entered properties remain drafts pending source support. Back/edit preserves answers; upstream edits invalidate dependent confirmation.
- [ ] Ask early, when relevant, whether the proposal has a preliminary budget, applicable sale/rental assumptions and an identified funding path. Each part accepts Unknown. Keep provided values as user assumptions with provenance; the question must not block progress or calculate viability.
- [ ] Implement versioned IndexedDB storage, serialized writes and visible saving/saved/error state. On schema migration failure preserve the original record and offer export/reset rather than overwrite. Clear draft removes that draft after confirmation. A blocked or quota-limited database leaves the in-memory draft usable with a persistent unsaved warning and export.
- [ ] Add browser assertions for close/reopen recovery, no loss on back/edit, tab reload during saving, Clear draft, corrupt/older draft handling, storage denial and narrow-screen keyboard order. No AI operation is pretended successful.
- [ ] Run the common checks plus the new guided browser script. Review the diff and record exact checks before a scoped feature commit if commits are authorized for execution.

**Acceptance:** Existing routes work; the new guided draft survives a fresh browser page/session on the same profile; every unsupported/mixed activity survives round-trip; a non-Lanark draft cannot access the Lanark evaluator. This is the first implementation slice ready for review.

## Slice 2: Assessment, tasks and export as the primary result

**Files:** Create `src/checks/registry.ts`, `src/checks/assessment.ts`, `src/checks/assessment.test.ts`, `src/features/projects/AssessmentView.tsx`, `src/features/projects/TaskPanel.tsx`, `src/features/projects/export.ts`, `src/features/projects/export.test.ts`. Reuse `src/design-system/components.tsx` and token CSS; extend the guided browser script.

**Interfaces:** `assessProposal(input: AssessmentInput): AssessmentDraft`; `prioritizeTasks(findings: Finding[]): TaskSuggestion[]`; `compareRuns(left: AssessmentRun, right: AssessmentRun): Comparison`; `exportProjectBrief(snapshot: ExportSnapshot): string`. C01-C12 check IDs and statuses come from the source/design documents. `ExportSnapshot` pins one proposal version and assessment run, referenced observations, relevant outcomes and overrides.

- [ ] Add tests for C06 housing arithmetic and C12 honest pillar gaps, including negative net-new homes, unknown existing units, affordability goal without a count, grocery-only zero homes, and unknown budget, applicable sale/rental assumptions or funding path. Financial viability remains Unassessed even when user estimates are present.
- [ ] Implement separate applicability/coverage/review/evidence indicators. Default result shows the proposal summary, housing outcomes, source dates, priority tasks and expandable evidence; eight pillars are a coverage checklist, not eight fabricated engines.
- [ ] Show one useful task detail with responsible party, requested evidence and dependencies. Preserve conflicts and keep applicable independent tasks available. Order by unresolved identity, adverse findings/dependencies, scope-specific missing evidence including relevant financial assumptions, then remaining gaps; stable IDs resolve ties. A missing budget, applicable sale/rental assumption or funding path yields a named financial diligence task ahead of generic gaps when it affects the next decision.
- [ ] Add a secondary change/duplicate action that creates a new proposal version. Comparison independently reports input, explanation, review-status and next-action differences. The Lanark repair/expansion pair explicitly reports unchanged next action.
- [ ] Generate Markdown and browser print from the same pinned snapshot. Include missing evidence, scope/coverage, version/date/source references and intended housing outcomes. Add tests comparing rendered/exported values and dates; export cannot silently use current draft inputs with an older assessment.
- [ ] Run common checks and both existing browser suites plus guided flow. Verify at 320 px and by keyboard that the current action appears before secondary map/evidence, status is not color-only and focus moves predictably.

**Acceptance:** A reviewer can name what is uncertain, who should resolve it and what evidence is requested without reading a long report. Lanark contradictions survive export. Changing wording is not counted as a changed decision.

## Slice 3: One validated AI operation from server to confirmation

**Files:** Create `supabase/migrations/202609260000_operation_ledger.sql`, `server/ai/contracts.ts`, `server/ai/provider.ts`, `server/ai/budget.ts`, `server/ai/evaluate.test.ts`, `server/ai/cases.ts`, `api/assist.ts`, `src/features/projects/ai-client.ts`, `src/features/projects/SuggestionReview.tsx`. Runtime validation library selection is an ordinary implementation choice; retain one schema definition across server and client.

**Interfaces:** `runAiOperation(request: AiRequest, context: AuthorizedAiContext): Promise<AiResult>`; `validateAiResult(raw: unknown, request: AiRequest): ValidationResult<AiResult>`; `confirmSuggestion(draft: ProposalDraft, suggestionId: string, decision: ConfirmationDecision): ProposalDraft`. Operations, schema fields, endpoint and cost reservation follow the technical design. Provider credentials remain server-side.

- [ ] Configure the operational Supabase database and server-only operation ledger/restricted reservation RPC before any runtime AI call. This is a prerequisite subset of database setup, not a dependency on the complete auth/project schema in slice 5. No paid request may run with only in-memory limits.
- [ ] Verify a single candidate's actual OpenRouter endpoint, strict schema behavior, provider route, context/output limit and token prices before configuring it. Metadata or a model name alone does not establish structured output. Any paid probe must stay inside a reviewed hard cap on the existing $10 balance; this handoff performs no paid probe.
- [ ] Build fixed cases for negation, tentative alternatives, bedrooms versus dwellings, mixed unsupported work, zero homes, conflicting records, unknown jurisdiction and source text containing malicious instructions. Require schema-valid outputs, preserved original wording and no invented evidence/rules or unauthorized state transitions.
- [ ] Implement one operation first: description to proposed activities plus at most one clarification. Suggestions carry explicit uncertainty and require user confirmation. Then reuse the same model adapter for supported finding explanations and suggested tasks; code-provided finding status and dependencies are immutable model inputs.
- [ ] Enforce request/body/token limits, authorization/anonymous session limits, atomic daily/global budget reservations, timeout and idempotency. Browser retries reuse operation IDs; retries cannot create unbounded calls. Unknown provider charge keeps the reservation conservatively consumed until reconciled.
- [ ] Exercise malformed JSON, extra fields, unknown source/check IDs, fabricated unit counts, timeout, 429, provider refusal, budget exhaustion and double click. Fail closed with named failed operation/retry; retain prior results and draft.
- [ ] Run common checks and an end-to-end local runtime probe only after configuration and probe authority. Record model/provider/schema versions, observed cost and outcome without storing full private prompts in logs.

**Acceptance:** One real model endpoint produces editable, user-confirmed suggestions and passes every critical safety case. A failed operation is visible and cannot fabricate an assessment. This slice cannot be called complete using fixture output alone.

## Slice 4: Countywide identity and bounded source retrieval

**Files:** Create `server/sources/contracts.ts`, `server/sources/assessment.ts`, `server/sources/parcels.ts`, `server/sources/municipalities.ts`, `server/sources/permits.ts`, `server/sources/zoning.ts`, `server/sources/registry.ts`, `server/property/resolve.ts`, corresponding `*.test.ts`, `api/property/resolve.ts`, `supabase/migrations/202609260001_geographic_verification.sql`. Preserve the original `src/assessment.ts` facade until old-route regression tests pass.

**Interfaces:** `searchProperty(query: PropertyQuery): Promise<PropertySearchResult>`; `confirmProperty(candidateId: string): Promise<PropertyResolution>`; `fetchObservation(request: SourceRequest): Promise<SourceResult>`; `verifyJurisdiction(parcel: ParcelGeometry, municipalities: MunicipalGeometry[], records: MunicipalityRecords): JurisdictionResult`. Use exact source contracts, limits and status unions in the adapter verification note. PostGIS procedures perform whole-polygon checks in EPSG:2272 with validated geometry.

- [ ] Configure PostGIS and narrowly callable GIS procedures before server geometry checks. Reuse the operational database from slice 3 if available; this setup can proceed independently of personal project/auth storage.
- [ ] Add sanitized response fixtures for Lanark, Mountford and Sharpsburg plus six-way `100 MAIN ST`, zero matches, duplicate exact IDs, invalid schema and truncated pages. Test actual canonical IDs as strings; do not add numeric padding heuristics.
- [ ] Implement candidate selection followed by independent exact-ID assessment/boundary re-fetch, municipal polygon coverage and a verified code crosswalk. Street suffix aliases are explicit tested entries. Mailing city/ZIP cannot establish jurisdiction. Test boundary-only contact separately from positive-area multi-municipality overlap, holes, multipart polygons and invalid geometries.
- [ ] Add exact-parcel Pittsburgh PLI pagination/deduplication and mapped district observations. Empty City results, out-of-coverage municipality, timeout, incomplete pages and records found are distinct. A complete query is not a complete permit history.
- [ ] Add per-source failure/retry and observations with retrieval time, source vintage, match method and reuse metadata. Fixed source URLs/fields block arbitrary fetches and query injection. One failed source does not erase other observations or prior assessment runs.
- [ ] Re-run actual public GET probes for the unfamiliar Mountford parcel and non-City Sharpsburg. Test full containment, which the current sampled intersection probes do not prove. Record success separately from fixture coverage. Expand representative address/boundary fixtures until the source note's reliability gates are met.
- [ ] Integrate a useful 2D outline/context view from verified geometry. No fabricated map when geometry is absent. Resolve parcel/municipality/zoning reuse permissions before public display/cache; slope remains optional and permission-gated.
- [ ] Run common checks and source integration tests. Demo non-City intake retaining the full proposal with City rules disabled and a municipal next task.

**Acceptance:** Identity is confirmed only with exact keys, full geometry coverage and code agreement; ambiguous or incomplete identity blocks City checks. Countywide source availability is supported by a documented matrix, not three successful examples. PLI coverage remains explicitly Pittsburgh only.

## Slice 5: Owner-scoped saving and outcome-based continuation

**Files:** Create `supabase/migrations/202609260002_projects.sql`, `supabase/tests/ownership.sql`, `server/projects/repository.ts`, `server/projects/transitions.ts`, `server/projects/transitions.test.ts`, `api/projects/import.ts`, `api/projects/[id]/index.ts`, `api/projects/[id]/commands.ts`, `src/features/projects/auth.ts`, `src/features/projects/SaveProject.tsx`, `src/features/projects/ProjectHome.tsx`, `scripts/project-continuation-smoke.mjs`. Migration files implement the minimum schema in the technical design; do not add services for individual nouns.

**Interfaces:** `saveLocalDraft(draft: LocalDraft, idempotencyKey: string, actor: UserId): Promise<SaveReceipt>`; `recordTaskOutcome(input: OutcomeInput, actor: UserId): Promise<TransitionResult>`; `requestRefresh(projectId: string, expectedVersion: string, actor: UserId): Promise<AssessmentRun>`; `deleteProject(projectId: string, actor: UserId): Promise<DeletionReceipt>`. All ownership derives from validated auth, never a caller-supplied owner field.

- [ ] Implement owner RLS and server ownership checks for every parent/child relation, source-reference access, tasks/outcomes and export. Add direct database and API tests with owner A, owner B and anonymous clients, including child-ID substitution and cross-project dependency links.
- [ ] Configure exact email-link callback URLs and approved email delivery. Test expired/reused links, interrupted callback and a link opened in another browser. Carry the local draft ID through the same-browser flow; never claim another device has unsynced local content.
- [ ] Implement idempotent transactional local-to-account migration. Retain the local draft until server read-back validates versions/counts; retries do not duplicate projects. Concurrent edits return a conflict and preserve both inputs, not silent last-writer loss.
- [ ] Implement immutable proposal/run snapshots and append-only outcomes. Distinguish request sent, response received, satisfied, inconclusive and adverse results. Completion requires a recorded outcome, and only a satisfied prerequisite releases dependent work. Inconclusive outcomes keep findings unresolved and propose a follow-up for confirmation.
- [ ] Validate dependency links for same owner/project and cycles. Preserve independent task execution. A planning-risk override records reason/scope/date and leaves findings and evidence unresolved; regulated-work authorization and access controls cannot be overridden.
- [ ] Add return view with prior results, outstanding tasks and explicit refresh. Refresh pins new evidence and check versions into a new run. Proposal changes flag only affected checks/tasks using registry dependencies; completed tasks remain historical and may be superseded.
- [ ] Implement deletion, backup retention disclosure and restore suppression as designed. Purge project content from live owner data; test idempotent deletion and stale session access. Verify actual hosting/database backup retention before publishing a concrete retention promise. Logs omit project text.
- [ ] Run common checks, database tests and continuation browser tests. Local integration uses synthetic users, not private records.

**Acceptance:** Save/reopen works across two authenticated browser profiles; cross-user access fails at API and database layers; unknown outcomes never release dependencies; refresh preserves the exact previous run; deletion cannot be undone by an ordinary client retry.

## Slice 6: Reviewed checks and full launch journey

**Files:** Extend `src/checks/registry.ts`; create `api/assessments.ts`, `src/checks/pittsburgh.ts`, `src/checks/pittsburgh.test.ts`, `server/checks/versions.ts`, `scripts/launch-flow-smoke.mjs`. Store human review evidence and effective source versions in the wiki and reference immutable IDs from the application registry.

- [ ] Review C07-C09 code edition, predicates, definitions and dependencies before enabling regulatory conclusions. Resolve the certificate-language issue in the adapter note; until resolved, lawful-use questions stay human verification. C10 current application terminology also needs direct verification.
- [ ] Test each enabled predicate with matching/nonmatching jurisdiction and use, unknown required inputs, contradictions, mixed scope, adverse authoritative decision and required discretionary approval. Every check names version, applicability, required observations and invalidation fields.
- [ ] Integrate C01-C10/C12 with explicit coverage and missing-evidence actions. Add C11 only if its terms, geometry and decision value justify it. No unchecked hazard receives a favorable status; no financial engine is implied.
- [ ] Exercise the entire accepted flow with an unfamiliar supported Pittsburgh parcel, non-City parcel and mixed unsupported proposal, including AI failure, save/reopen, task response, proposal edit, explicit refresh and export.
- [ ] Verify role changes only wording/emphasis by comparing underlying finding/evidence payloads for all five roles. Verify mobile/keyboard forms, visible labels/errors, focus after asynchronous operations and gold interaction meaning.
- [ ] Use ShurSave only as a historical fixture: preserve roughly 190-unit uncertainty, later 248 units, 3.25-to-3.1 FAR change, denied dimensional relief versus conditional grocery approval, and zero-new-home later outcome. Do not imply the live engine adjudicates that case.
- [ ] Run all common/browser/database gates. Publish a coverage matrix and unresolved limitations in the release checklist before claiming the launch minimum.

**Acceptance:** Countywide intake/assessment, geographically correct municipal behavior, verified exact-parcel permit scope, reviewed bounded Pittsburgh checks, runtime AI, personal saving and task continuation all work together. A local demo cannot waive any of these gates.

## Slice 7: Later authorized hosted verification

Deployment requires separate authority plus source reuse clearance, configured Supabase/Auth/email, validated model route and enforceable balance limits. No work in this plan sends invitations, messages or buys services.

- [ ] Review the exact Vercel/Supabase project, origin, secrets-entry mechanism and email callback configuration before authorized deployment. Never inspect or print credential files.
- [ ] Test hosted sign-in deliverability, callback completion, token expiry/logout, owner isolation and local-draft preservation with approved test accounts.
- [ ] Test real hosted source requests, timeout/response ceilings, correct CRS/municipality and schema validation. Browser-origin success and local success are insufficient evidence for hosted behavior.
- [ ] Verify anonymous AI abuse limits, budget concurrency, provider outage and operation retry. Check server logs for redaction using synthetic inputs.
- [ ] Verify deep links, 320 px/mobile layout, keyboard navigation, export/print consistency, no silent stale replacement and backup/deletion behavior from deployed configuration. Record date, URL, build revision and observed exits/results in the handoff.

**Acceptance:** A deployed release is described as verified only after actual hosted tests pass. A failed external prerequisite blocks the relevant feature/release claim and preserves a usable dated local demonstration.

## Practitioner validation and pivot criterion

No interview or demand claim is made here. Use an existing response if one arrives; ask Het before any new outreach. With permission, test one recent real project by a small developer and one by a housing nonprofit, including at least one case beyond Lanark. These are proposed small-sample tests, not statistical validation.

1. Before showing the output, what was the next decision, task, responsible person and evidence request? What uncertainty made it difficult?
2. After seeing the brief, which exact task, requested evidence, order or responsible party would change? If nothing changes, does it improve the handoff enough to use, and what concrete artifact demonstrates that?
3. Which source conflict or missing fact was already known? Which inference is misleading, too broad or outside the practitioner's responsibility?
4. Can the practitioner act on the task as written without translating it into another request? What would count as a conclusive response?
5. Does a changed proposal change the next task or only the wording? Can they distinguish the two without explanation from the team?
6. Can they recover the project, record an inconclusive reply and identify what remains blocked? Does the exported brief preserve the information their reviewer actually needs?

Record the initial task and post-output task verbatim where sharing is authorized, whether the proposed change is correct, and why a proposed task was rejected. Do not replace that evidence with satisfaction scores or estimated time savings.

**Recommended decision rule:** Keep comparison secondary unless at least one observed comparison changes a justified next action. If neither of the two practitioner walkthroughs identifies a correct new/reordered evidence request or a demonstrably more usable reviewer handoff, stop expanding automated checks. Pivot the next experiment to a structured municipal/pre-application brief assembler: confirmed proposal, contradictory records, user-selected questions and sourced attachments/links. Test whether a recipient can answer that brief without follow-up clarification before investing in broader evaluation. If that also adds no value, pause the product thesis rather than invent differentiation. Two cases are a directional gate, not proof of market fit.

## Verification coverage map

| Required case | Owning slice and expected behavior |
|---|---|
| Unfamiliar supported parcel | 4/6: Mountford produces its own observations, never Lanark conflict/slope defaults |
| Municipality boundaries and ambiguous addresses | 4: whole-polygon/crosswalk verification; six-way address requires selection; partial geometry stays unresolved |
| Leading-zero IDs | 1/4: opaque string survives input, source query, storage and export |
| Mixed/unsupported scope | 1/3/6: all activities retained; unsupported check coverage explicit |
| Negation/tentative/bedrooms vs dwellings | 3: no silent committed intent or added unit; confirm suggestions |
| Malformed model output and malicious source text | 3: reject invalid/unauthorized output, no rule or state override |
| Connector failure/stale evidence | 4/5: partial observation failure and dated prior run remain visible |
| Draft recovery and sign-in continuity | 1/5: reload survives; failed migration preserves local draft |
| Cross-user isolation | 5/7: API and direct RLS deny reads/writes and forged child links |
| Inconclusive outcomes/dependencies | 5: unresolved prerequisite stays blocked; independent tasks continue |
| Versions/explicit refresh | 2/5: prior run unchanged, affected checks flagged, fresh run separately dated |
| Export consistency | 2/6: same pinned data as screen; no fresh draft/old result mixing |
| Keyboard/mobile | 1/2/6/7: labeled controls, focus/error feedback and no horizontal action-panel overflow |
| Hosted auth/source behavior | 7: real deployed evidence only after authorization |

## Review focus

The highest-risk conditions are fenced in explicit tests above: a non-Lanark parcel reaching hardcoded findings (1/4), partial jurisdiction evidence enabling City rules (4), an AI retry spending twice (3), a sign-in/migration interruption destroying the only draft (5), and an inconclusive outcome releasing dependent work (5). These gates must be demonstrated before expanding each boundary.
