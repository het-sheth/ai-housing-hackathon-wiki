---
type: concept
title: Proposal comparison for a Pittsburgh housing site
description: A narrow product hypothesis for Het and Rushi to evaluate before implementation.
tags: [product, proposal, track-1]
status: stub
updated: 2026-09-26
---

# Proposed product: compare housing choices on one site

**Status: proposed for Het and Rushi's review.** Documentation is authorized; product scope, implementation and architecture are not approved. This updates the static-brief candidate rather than establishing a second product to build.

**Promise:** For this Pittsburgh property and housing proposal, explain the applicable zoning checks, show what changes when the proposal changes, and identify the next evidence or human review needed.

## New practitioner evidence from the video

[The ACTION-Housing caption analysis](/wiki/research/action-housing-video-findings.md) describes a real preference for one taller building over two, community/design discussions and paid diligence artifacts. It supports investigating proposal tradeoffs but comes from a 35-unit rental development context, not our candidate single-home rehabilitation workflow. Do not broaden the weekend app to reproduce that entire project. The transcript also explains why finance affects design: deferring a financial engine does not mean financing is irrelevant; financial feasibility must remain unassessed.

## Who, when and decision

Primary user hypothesis: a project lead at a small nonprofit housing developer considering further diligence. A small private developer is an alternative primary user if case review shows a better fit. The user wants to decide whether to retain or adjust a proposal and what to investigate next. We have not observed their actual workflow or established who approves spending.

Planners can review a targeted question; managers can read the resulting brief. Policy analysts need broader validated data than this weekend slice provides. Do not create four persona-specific interfaces.

## Concrete experience

1. Enter a City of Pittsburgh parcel ID or address and confirm the boundary and jurisdiction.
2. State the intended housing outcome and proposal: existing/proposed units, existing lawful-use evidence, expansion and land disturbance. Unknown is a supported answer.
3. Inspect a short review of relevant rule checks, evidence conflicts and missing facts.
4. Change one supported input. Compare the original and revised proposal side by side. Highlight which checks change and cite the specific rule; keep persistent constraints and unknowns visible.
5. Download a meeting-ready brief containing both proposals, their housing outcomes, assumptions, sources, dates, review points and next actions. Email/meeting handoff is a hypothesis to validate, not established adoption evidence.

Candidate first comparison: repair/remodel an existing lawful single dwelling versus a defined expansion. This is not a promise that either is permitted or that expansion requires a variance. Exact supported changes depend on a verified code trace and the facts needed to apply it. Lanark is a real evidence test; neither its current lawful use nor either proposed alternative has been approved or fully evaluated.

## What would make this worth building

The initial cited parcel brief overlaps Rescope. The proposed difference is making proposal-dependent rule changes understandable while preserving the user's housing objective. Novelty across the market is unverified. If a simpler proposal delivers fewer homes, show that tradeoff rather than silently optimize for ease.

Compare three approaches:

| Approach | Strength | Limitation |
|---|---|---|
| Static site brief | Smallest credible artifact; Lanark evidence exists | Substantial competitor overlap; utility unvalidated |
| Two proposals on one parcel, recommended for testing | Shows how user choices affect checks and next steps | Requires verified rule logic, adequate proposal inputs and evidence users actually iterate scope |
| Zoning plus full financial feasibility | Broader apparent coverage | No adequate budget/comps/funding inputs; too much uncertainty for the weekend |

## Weekend boundary

Essential if approved: one jurisdiction, one project family, two explicit scenarios, a small reviewed rule set, deterministic parcel joins and spatial checks, cited explanations, visible unknowns, a download and graceful failures. Reject unsupported geography/project types clearly; source failure produces unavailable evidence, never a clear result. Conflicting records stay visible.

AI responsibility: explain supported findings in accessible language and formulate evidence requests. Deterministic responsibility: joins, geometry, rule predicates and arithmetic. Human responsibility: lawful-use interpretation, ambiguous scope, exceptions, variances and final decisions. AI does not design a compliant building or promise approval.

Deferred: financial engine, automatic comps, subsidy eligibility, title/utility-capacity certification, generative building design, portfolio rankings, neighborhood policy scores and organization-wide integrations. Preserve current spreadsheet/email handoffs until interviews establish a need for more.

Development Ease remains a visible component scorecard, not a fabricated numerical result. Legal permissibility, physical flags and process complexity must stay distinguishable. Evidence coverage is separate; financial feasibility remains unassessed. No approved rubric or organizer acceptance of component-only scoring is established. Resolve this before claiming the final challenge requirement is met.

## Work split to agree, not an assumption about availability

Rushi could own one rule trace and its counterexamples: relevant current sections, necessary inputs, outcome changes, unresolved interpretations and a focused SME check. He could use selected video sections if they inform that question, rather than undertaking another broad research report.

Het could own the user journey, evidence handoff and real parcel demonstration. Agree availability and preferred responsibilities first. Architecture remains undecided and implementation belongs in a separate app repository.

## Validation and cut points

1. Ask an SME/practitioner about a recent case: did they change scope after an initial zoning finding, what did they change, and what artifact supported that decision?
2. Walk through a manually verified original/alternative pair. Have them identify an incorrect inference, a missing input and whether a next action actually changes.
3. Test unchanged input, unsupported scenario, ambiguous lawful use, mixed zoning/overlay coverage, missing source and contradictory records. Unknowns must never improve ease or disappear in comparison/export.

If a rule trace cannot be completed, reduce the supported comparison. If insufficient parcel facts exist, show conditional checks rather than answers. If practitioners do not iterate scope at this stage, abandon comparison and reassess whether the basic brief adds enough value. If it changes no action relative to existing tools or a spreadsheet, do not build it merely because the data joins work.

## Judging narrative, using the actual six criteria

| Criterion | What the demo must establish |
|---|---|
| Problem Value | One consequential initial-review decision; still needs practitioner evidence |
| User Fit & Usability | One person completes the review and takes away a usable artifact |
| Technical Execution | One real parcel, two supported proposals and working failures |
| Data & AI Integrity | Source-grounded changes, current rule versions, conflicts and explicit unknowns |
| Actionability | A specific next check and responsible authority |
| Continuation Potential | A manageable rule-maintenance and practitioner-testing path, with no invented pilot |

No numeric judging weights are supplied. A 3-5 minute demo should establish the proposal, show a real finding, change one input, explain the resulting change and export the evidence. The differentiation is a hypothesis demonstrated through the interaction, not a competitor incapability claim.

# Citations

[September 26 evidence and official links](/wiki/product/september-26-evidence-update.md), [Lanark worked example](/wiki/product/lanark-worked-example.md), [ACTION-Housing excerpts](/wiki/research/action-housing-presentation-excerpts.md), [event rules](/wiki/event/rules.md). Judging source: `raw/markdown/participant-packet.md`, pages 8-9. This page's product and work split are team proposals, not source observations.
