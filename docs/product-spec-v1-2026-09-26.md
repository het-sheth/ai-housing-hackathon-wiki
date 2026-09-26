# Housing Navigator v1 product specification

Status: PRODUCT DECISIONS ACCEPTED; CONSOLIDATED SPEC FOR REVIEW. September 26, 2026. Owners: Het and Rushi.

This document preserves the product interview before context compaction. Accepted decisions are identified explicitly. The final interview choices are accepted. Detailed engineering recommendations and release verification remain to be reviewed. It is not authorization to implement all recommendations. No feature described here should be represented as implemented without verification.

## 1. Purpose and users

Help a nontechnical housing project lead understand how a proposed project interacts with property evidence, what remains uncertain and what to do next. The product supports deciding whether to pursue a site, comparing proposals, and preparing for review, in that priority order.

Accepted personas: Municipal Planner; Small/Mid-Size Developer; Housing Nonprofit/CDC; Policy Analyst; Other / exploring. Developers and housing nonprofits are initially prioritized, not exclusive users. Role changes language and emphasis, not the underlying evidence or rule result. Practitioner demand, saved time and willingness to pay remain unvalidated.

Positioning proposal: Housing Navigator helps housing project leads turn a proposed scope into a sourced list of barriers, missing evidence and next actions to discuss with the right professionals.

## 2. Accepted release boundaries

- Countywide intake: Allegheny County, including Pittsburgh. Resolve the municipality and disclose coverage for each source and check. The hackathon itself requires at least one Pittsburgh OR Allegheny County use case; countywide intake is our product choice.
- One site per initial workflow. Saved projects should not preclude future multiple-site support, but shortlist comparison is deferred. Multi-parcel assembly evaluation is not promised by one-site intake and needs an explicit unsupported state until designed.
- Accept and retain all housing work categories and combinations: repair/remodel, addition, interior conversion, additional dwellings, partial demolition/rebuild, demolition, new construction, site work, mixed use and other/uncertain work.
- Accepting a description does not establish automated evaluation coverage. Unsupported checks remain explicit and lead to next tasks; do not force a proposal into another category.
- V1 input: address or parcel ID, then natural-language description and confirmed structured answers. V2: packet uploads and extraction.
- Guided form with conversational assistance. AI leads understanding and clarification; selections remain visible and editable.
- Personal projects, one owner, exportable collaborator brief. No shared editing, invitations or public project links in v1.
- Explore anonymously, sign in to save/revisit. Browser-local drafts survive browser closure, with device-only disclosure and Clear draft.
- Signed-in projects and their history remain until deletion. Backup retention and deletion behavior require technical definition.
- Preserve proposal versions, assessment history, source observations and task outcomes. Offer explicit refresh when returning; never silently replace prior findings.
- No full pro forma engine, numerical approval probability, autonomous submissions, professional clearance or novelty claim.

## 3. Accepted experience direction

This section implements the accepted journey conceptually; detailed screen arrangement remains to be designed.

1. Start: ask role and current decision, both editable. Address or parcel ID is the main entry.
2. Confirm property: show candidate address, municipality and parcel identifier. Disambiguate matches before requesting jurisdiction-specific checks. Outside-county locations receive an explicit boundary message.
3. Describe work: a plain-language prompt, followed by AI-proposed activity selections. Retain original wording and show tentative/unknown interpretations. Never infer another dwelling from another bedroom.
4. Clarify: ask one relevant question at a time; allow direct editing of structured inputs and explicit unknown answers. Ask only questions that affect supported checks or a useful handoff.
5. Confirm proposal: show baseline, intended program, assumptions and unresolved details before running the assessment. User input does not override conflicting public records.
6. Results: the accepted primary view is a proposal-specific assessment and prioritized next actions. Evidence details expand on demand. Proposal comparison is offered when changing or duplicating a proposal.
7. Save/export: sign-in preserves the local draft and associates the saved project with its owner. Export does not require granting collaborators account access.
8. Return: show saved stage, next tasks, prior versions and source dates. Offer Refresh available sources; preserve the prior run and identify changed findings.

Accepted spatial scope: useful 2D map/parcel context in v1. Defer 3D until reliable geometry/elevation and a concrete decision benefit are available.

Visual recommendation: retain Pittsburgh black/gold with the independent 412 identity, use a readable question panel beside a 2D site view, and make progress/back navigation obvious. Gold indicates interaction, not legal permission. On narrow screens, the current question/action precedes secondary map context. Keyboard access, explicit labels and text alternatives accompany visual indicators. The optional visual companion was declined; this does not waive eventual browser inspection.

## 4. Proposal and evidence model

Separate user intent from public record classification, physical observations and legal-use evidence. At minimum capture:

- Property: parcel ID preserved as a string, authoritative jurisdiction, address and geometry/CRS when available.
- Existing baseline: observed site/building state, recorded use, legal-use evidence, existing units and attached/detached/other form; unknown is valid.
- Program: proposed uses, work activities, proposed units, homes retained and net new homes, affordability goals where relevant, essential non-housing uses.
- Physical change: additions/demolition, relevant height/area/setback inputs and work location or ground disturbance where required. Do not demand dimensions irrelevant to the user's work.
- Evidence observation: provider/source identifier and URL, source vintage/effective date when known, retrieval time, spatial/record match method, selected attributes, terms and availability.
- Provenance: source observation, user assumption, model suggestion or deterministic derivation. Keep contradictory records separate.
- Proposal version and assessment run: immutable input/evidence/rule references for a completed assessment. A newer run does not rewrite the prior run.

Current records must not be used to reconstruct historical permissions without the appropriate historical rule/source versions.

## 5. Accepted feasibility presentation

Eight accepted product pillars: property control/rights; land use/design permission; site/building condition; environmental/health/climate hazards; utilities/access; market demand/affordability goals; capital/operating viability; approvals/delivery readiness. These are a product taxonomy, not an official rubric or a promise of eight implemented engines. Apply topic relevance according to proposal, stage, jurisdiction and funding.

Accepted presentation: named per-check statuses plus an evidence/action checklist, without an averaged score. Separate check applicability, finding/review status, evidence provenance/completeness and task status.

- Known adverse decisions and supported conflicts with requirements are prominent and proposal/version-specific.
- Required approvals are listed separately. An approval of one use does not approve the entire building.
- Missing evidence is Unknown or Verification required; unsupported evaluation is Not yet supported, never a favorable result.
- Financial feasibility stays Unassessed when necessary costs, rents/sales, subsidies, operating and lender assumptions are missing.
- Housing outcomes remain visible. A grocery-only alternative with zero new homes cannot silently win a housing comparison.
- No single reassuring number can average away an adverse decision, a hard barrier or absent finances.

A finding includes its explanation, review status, next action, missing information and source references. A comparison separately identifies changes in inputs, explanation, review status and next action. No change is a valid result.

## 6. Accepted tasks and continuation behavior

Each next action identifies the issue to resolve, responsible party, requested evidence/outcome and dependencies. The project lead confirms AI-suggested path changes.

Task completion requires an outcome. Request sent, response received and requirement satisfied are different. An inconclusive response leaves the finding unresolved and creates the next appropriate task. Unrelated work may continue.

Users may record their reason for proceeding with their own planning despite an unresolved dependency. The override remains visible and never changes the legal/evidence finding or authorizes regulated work. It does not bypass system validation or access controls.

Recommended initial task states: open, in progress, waiting, outcome recorded, superseded. Finding resolution is separate. Changing a proposal preserves completed work but marks affected findings/tasks for reassessment; it must not erase the history or reuse evidence outside its supported scope.

V1 outcomes can be structured notes and source references. General uploaded-packet interpretation remains v2.

## 7. AI contract

Accepted: one generative model initially. It proposes structured inputs, asks clarifications and explains sourced findings. Jev remains a candidate for later comparative classification tests. LangGraph is an orchestration option, not a selected requirement.

Code owns geographic joins, arithmetic, input validation, evaluated rule predicates and permitted state transitions. AI cannot manufacture missing rules, clear contradictory records or mark an unsupported check satisfied. Source text is evidence, not executable instructions. Validate model output and source references before applying suggestions.

Accepted outage behavior: preserve work, show failed AI operation and allow retry. Existing results remain accessible with their prior dates. Do not silently substitute canned output or imply that an old assessment was rerun successfully.

OpenRouter is the recommended runtime candidate to validate using the existing balance; no model or endpoint has been selected or tested. Cursor remains available for development and bounded probes. No final runtime provider is selected. Cursor's local Auto CLI probe succeeded in 8.91 seconds, reporting 13,348 input and 571 output tokens. Named-model access was rejected. This establishes one local response, not SDK/cloud access, grant billing, schema-enforced output reliability or suitability for the deployed product.

Available user-reported balances: $10 OpenRouter plus $75 Cursor hackathon grant, with the Cursor grant expiring October 26, 2026. Treat these as separate provider balances, not transferable funds. No new purchases or automatic top-ups are authorized. The balance report is not a verified billing observation. Model and email cost limits must be enforced server-side. Do not expose provider credentials to the browser.

OpenRouter supports schema-constrained output on compatible endpoints. Endpoint support and application validation must be checked; configure compatible routing and a server-side credit cap before runtime use. This is a technical recommendation, not a verified integration. Sources: [structured outputs](https://openrouter.ai/docs/guides/features/structured-outputs), [limits](https://openrouter.ai/docs/api_reference/limits).

## 8. Technical design recommendations

Accepted foundation: existing React/TypeScript/Vite app, Supabase Postgres and Supabase Auth, planned Vercel hosting. No infrastructure has been provisioned for this new design.

Recommended records: projects; proposal versions; evidence observations; assessment runs; findings; tasks; task outcomes; dependency links; recorded planning overrides; source/rule coverage registry. User-private records are owner-scoped. Shared public source caching must be separate from user descriptions and project outcomes.

Recommended boundaries:
- Browser handles presentation, editable inputs and temporary local drafts.
- Supabase handles authenticated identity and persistent owner-scoped records, with tested access policies.
- Server-side endpoints resolve property identity, call whitelisted source adapters, request AI assistance and create assessment runs. Do not accept arbitrary proxy URLs or trust a browser-supplied owner ID.
- Evidence and task dependencies are explicit relational records. Use application-controlled state transitions initially; adopt LangGraph only if a concrete branching/retry/resume need justifies it. This is a recommendation, not an accepted dependency choice.
- Supabase email links need a production-capable email delivery service and correct callback configuration. Sender/domain, provider and account availability remain technical prerequisites.
- A successful authenticated save acknowledges the server copy before retiring the local draft. Failed authentication/save preserves it. Local drafts do not automatically transfer between devices.
- Public-source cache refresh and assessment recalculation are separate operations. Partial connector failures return independent unavailable states; no silent snapshot fallback.
- Deletion removes active project records and history, including dependent records. Backup-retention limits and logs require explicit documented policies before deployment.

## 9. Source and coverage gate

Each connector/check has a named steward, supported geography/project scope, source/version, retrieval/match method, failure behavior and reuse status. No municipality can inherit Pittsburgh zoning rules through an address label. Every proposal type remains accepted even if its checks need human follow-up.

Existing implementation: one bounded live assessment request; Lanark parcel, permit, zoning and slope snapshots; narrow deterministic comparison and Markdown export. Generic countywide address/parcel resolution, municipal rule coverage, task storage and runtime AI are not implemented.

Accepted first-release minimum: reliable countywide parcel/jurisdiction identification and assessment retrieval, exact-parcel permit evidence where source coverage is verified, a reviewed subset of Pittsburgh checks, and explicit source-specific gaps/human tasks elsewhere. Exact adapters, rule list and tested municipality samples must be documented before claiming launch readiness.

Parcel, zoning and slope redistribution terms remain unresolved. Resolve them or select a documented permissible presentation/source before public deployment. Never silently replace real geometry with an illustrative shape.

## 10. Proposed verification and release criteria

- Complete an unfamiliar supported parcel flow, not only a hardcoded Lanark fixture.
- Check municipality boundaries and ambiguous addresses; preserve leading-zero identifiers.
- Retain unsupported activities and mixed proposals without routing them into false repair clearance.
- Validate AI on tentative work, negation, added bedrooms versus dwellings, combined activities, missing facts and adversarial source text. Show one useful question and editable interpretation.
- Verify anonymous draft recovery, sign-in continuity, cross-user isolation and deletion behavior.
- Verify task outcomes, inconclusive responses, dependencies and recorded planning overrides without converting them to clearances.
- Verify version history, affected-check reassessment, explicit refresh, changed-source explanations and export consistency.
- Preserve Lanark's conflict and default explanation-only change; do not manufacture a consequential difference.
- Use ShurSave as a dated historical stress test, not a claimed verified lower-rise solution or live general-purpose rule engine.
- Verify connector timeout/empty/unavailable distinctions and model failures.
- Validate the production URL, auth callback/email flow and source calls from the hosted origin, plus keyboard/mobile use and exports.
- Ask a practitioner to identify what they would do differently with the report. If comparison only changes wording, make it secondary; if the handoff itself adds no value, revisit the workflow.

## 11. Final interview resolution

Het accepted all six choices, adding: "agree with all. i have 10 dollars in openrouter balance + cursor".

1. Assessment and prioritized actions are primary; comparison is secondary when changing or duplicating a proposal.
2. Eight pillars, named statuses and evidence/action checklist; financial feasibility unassessed without inputs; no overall numerical score.
3. Countywide identity/assessment, verified permit coverage, a reviewed Pittsburgh check subset and explicit gaps elsewhere are the launch minimum, not a claim of implemented coverage.
4. Useful 2D site context in v1; 3D deferred pending reliable data and decision value.
5. AI failures preserve work, expose failure/retry and retain dated saved results without fabricated new analysis.
6. Use the existing reported OpenRouter and Cursor balances as the available funding boundary. No extra cash purchases or automatic top-ups are authorized.

These settle product choices, not source reuse rights, practitioner validation, model quality or infrastructure readiness.

## 12. Continuation instructions

The final interview is resolved. Do not reopen Q1-Q6. Resolve technical facts through bounded research/account checks; do not ask the user to design tables or endpoints. Present the consolidated spec for review with unresolved external blockers explicitly named, then prepare an implementation plan under the agreed skill workflow. Do not restart the persona interview or treat proposed defaults as approved.

Keep research/specification here; application work belongs in /home/het/personal/ai-housing-navigator. Preserve existing uncommitted work in both repositories. No implementation is authorized by this draft alone.

## References

- [Accepted interview decisions](product-decisions-2026-09-26.md)
- [Product critique, recommendations only](product-direction-critique-2026-09-26.md)
- [ShurSave source review](shursave-case-2026-09-26.md)
- [Comparison and competitor evidence](proposal-comparison-research-2026-09-26.md)
- [Cursor probe](cursor-intake-probe-2026-09-26.md)
- [Proposed comparison ADR](adr/0005-propose-project-comparison.md)
- [Current research handoff](handoffs/current.md)
- App implementation baseline: /home/het/personal/ai-housing-navigator/docs/current.md. Some authentication status text there is historical; Vercel CLI login was verified later, but the app remains undeployed.
