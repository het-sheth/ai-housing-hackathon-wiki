---
type: concept
title: Track 1 deep research brief
description: A workflow-first Pittsburgh research prompt for a two-person weekend build.
tags: [housing, discovery, track-1]
timestamp: 2026-09-26T00:00:00Z
status: researched
---

# Track 1 deep research brief

Track 1 is selected by Het on September 26, 2026. Target-user and product scope remain hypotheses. The prompt below is intended for a separate Deep Research session with the source packet, challenge brief, data catalog and Rushi's report attached.

## Copyable prompt

You are researching product discovery for a two-person team building a working AI housing prototype for the AI Horizons AI for Housing Hackathon. Produce a decision-ready research dossier, grounded in current primary sources, that lets us choose a narrow, useful workflow and start building. Investigate gaps in our evidence, challenge our assumptions, and recommend what to omit. We do not need another broad explanation of the American housing crisis.

### 1. Our context and constraints

- We have selected Track 1: Development Feasibility Navigator, also titled Development Feasibility & Pro Forma Navigator in its challenge brief.
- The direct challenge asks for an AI-driven Development Ease Score that exposes regulatory bottlenecks, required variances and infrastructure gaps to help prioritize sites or identify needed intervention. A variance is an exception sought from a zoning requirement; do not assume it is available or assured.
- The team is Het and Rushi. Het has Saturday and Sunday. The deadline is September 27, 2026 at 11:59 p.m. Eastern. Do not infer that Rushi has unlimited availability.
- We want a finished, usable workflow for real housing practitioners, with an actual Pittsburgh demonstration. We do not want a generic chatbot, a standalone analytics dashboard, a giant platform, or a thin wrapper around another AI product.
- Our leading user hypothesis is a staff member at a small nonprofit housing developer, community development corporation, or community land trust screening potential sites. This is a hypothesis to test, not a predetermined answer. Compare it against other plausible Track 1 users.
- Het works at Bloomerang, a nonprofit giving platform. We have no established relationships with housing nonprofits. Do not assume access to customers, customer records, interviews, internal systems, partnerships, or endorsements.
- Rushi supplied the attached research report. Its Parcel-to-Keys Evidence Graph concept is a long-term direction, not an approved implementation scope.
- We may use a TypeScript web stack and a generator such as Better T Stack, but architecture is undecided. Recommend product requirements before technologies. Do not spend this research choosing frameworks.
- We want compatibility with practitioners' current spreadsheets, email, meetings and existing systems. Discover which of these are actually used, by whom and at which step.
- We want a Pittsburgh-specific visual identity with restrained local Easter eggs. Functional locality, jurisdiction and credible data take priority over decoration.
- The research wiki is separate from the eventual public application repository. The hackathon permits libraries, frameworks and public data with disclosure; previous project code is prohibited. Do not invent organizer interpretations about ambiguous rules.

### 2. Read the supplied material and state what is already known

Read the Participant Packet, Track 1 brief, organizer Public Data Catalog CSV, and Rushi's report. The other two track briefs provide context only. The research report's PDF and Markdown versions overlap; the two catalog CSVs are duplicates. Do not count them as independent corroborating sources.

Established observations to build on:

- Parcel geometry, assessment attributes, zoning polygons and legal text are different sources. Parcel identifiers and spatial joins must be validated.
- Missing evidence is not proof that a constraint is absent. Zoning permission alone does not establish physical, infrastructure or financial feasibility.
- Neighborhood Census/HUD estimates are not measurements of an individual parcel or household.
- The organizer catalog contains 60 entries, including portals and reference pages rather than only downloadable datasets. Some catalog URLs are stale.
- No complete record-level parcel-to-zoning-to-hazard integration has yet been demonstrated by our team.
- The report proposes explaining evidence, dependencies, unknowns and next actions. Its invented delay percentages and illustrative financial numbers must never be presented as observations.
- Judging criteria are Problem Value; User Fit & Usability; Technical Execution; Data & AI Integrity; Actionability; Continuation Potential. The packet supplies no numeric weights.

Separate attachment claims, independently verified facts, your inferences and unresolved questions. If an attachment is missing, name it and continue with public sources instead of pretending to have read it. Use the actual current research date and identify the effective dates of rules, data and programs.

### 3. Investigate the practitioner workflow before proposing features

Reconstruct how a small Pittsburgh nonprofit evaluates a potential housing site, from the first lead to the decision to spend money on further diligence. Find direct evidence such as acquisition policies, board materials, project case studies, RFQs/RFPs, intake forms, feasibility reports, checklists and professional guidance.

Answer:

- How do opportunities arrive: land donation, public disposition, broker, community referral, existing ownership or another route?
- Who performs the initial screen, who reviews it, and who can approve the next expenditure?
- What must they decide during initial review, and what is deliberately deferred to an architect, engineer, lawyer, lender, utility or City staff?
- What information arrives with a lead? What information is usually missing?
- What tools and artifacts do they use? Which parts are documented, and which remain hypotheses?
- Which uncertainties cause rejection, delay, escalation or avoidable rework?
- How do nonprofit mission, affordability obligations, community plans and funder requirements change the assessment compared with a market-rate developer?
- How do scattered-site rehabilitation, new infill construction and larger multifamily projects differ? Which one is realistically supportable in a weekend prototype?

Produce a workflow table: stage, actor, trigger, inputs, existing tool or artifact, decision, output, pain, evidence, and confidence. Do not invent time saved, staff roles or market prevalence when sources are missing. For undocumented steps, provide the exact interview question needed.

### 4. Identify one adoption opportunity

Find the most valuable small task we could improve while fitting the current workflow. Compare at least three candidate interventions, such as a site-screening brief, a missing-information and next-action checklist, or a comparison of a few candidate sites. You may reject these and propose a better grounded alternative.

For each candidate explain:

- The user's job, the moment they would use it, and the concrete decision it supports.
- Inputs they already possess and inputs that would impose new work.
- The artifact they receive and the person or system it goes to next.
- How they could use it tomorrow without a new organization-wide software rollout.
- Whether simple paste/upload/download handoffs suffice; name integrations only when evidence shows they matter.
- What they already use instead and why switching would be worthwhile.
- The smallest credible test of utility and the evidence that would invalidate the idea.

Recommend one primary user and one workflow. Do not treat broad potential audience as proof of product value. Explain which adjacent users could benefit later without requiring us to serve them now.

### 5. Make the jurisdiction explicitly Pittsburgh

Separate the City of Pittsburgh from other Allegheny County municipalities. County parcel data does not establish a shared zoning regime. Prefer authoritative current City, county, utility and state sources.

For the recommended project type, investigate the initial relevance of zoning district and overlays, use permission, dimensional constraints, historic review, steep slopes, flood conditions, environmental screening, parcel assembly, title questions, utilities, stormwater, access and permitting pathways. Prioritize only those material to the chosen workflow.

For each potential check, report the responsible authority, official source, jurisdiction, triggering conditions, dependencies, current data access, safe machine-supported statement, uncertainty and human escalation. Distinguish rules from guidance, proposals, expired programs and old web pages. Surface conflicting sources explicitly.

Identify what cannot be determined from public data, especially utility capacity, title clearance, structural condition, contamination status, project approval and financing eligibility. Never turn a nearby utility line into confirmed service capacity or a nearby hazard into a parcel-specific diagnosis.

### 6. Audit the minimum useful data, not all 60 sources equally

Use the organizer CSV as the starting inventory. Audit the smallest set needed for the recommended workflow. Useful starting pages include:

- Assessments: https://data.wprdc.org/dataset/property-assessments
- Parcel boundaries: https://data.wprdc.org/dataset/allegheny-county-parcel-boundaries1
- Zoning polygons: https://data.wprdc.org/dataset/zoning
- Permits: https://data.wprdc.org/dataset/pli-permits
- HUD CHAS: https://www.huduser.gov/portal/datasets/cp.html
- ACS five-year: https://www.census.gov/data/developers/data-sets/acs-5year.html

Record source steward, actual endpoint/download, format, access conditions, license/reuse terms, geography, coordinate system when relevant, time coverage, update cadence, join keys, fields, nulls, and material limitations.

Where possible inspect a small permitted sample and a documented schema, not merely the landing page. State precisely whether you verified metadata, fetched records, tested a join or did none of those. Preserve parcel IDs as identifiers and investigate formatting issues. Test overlays on parcel geometry rather than assuming address points capture whole-parcel conditions.

Explain how we can obtain a small reproducible Pittsburgh extract for a demo. Avoid bulk extraction from interactive portals when a documented open data route exists. Do not infer availability from a search snippet. Prioritize public development attributes without collecting personal data we do not need.

Return a build-ready source matrix and a clear list of access or join blockers.

### 7. Design an honest Development Ease Score

We must address the direct Track 1 ask while avoiding a misleading number. Investigate existing screening practices or measures, then recommend an interpretable prototype approach with visible components, assumptions, evidence and coverage.

Explicitly distinguish legal permissibility, physical constraints, process complexity, financial feasibility, and completeness of evidence. Compare a component scorecard with any proposed aggregate score. Justify whether aggregation is useful at all and show how we could explain the choice to judges if it is not.

Explain treatment of unknown, conflicting, stale and inapplicable evidence. Missing data must never improve a site's score. An uncertainty or evidence-coverage measure should not be confused with the site's physical feasibility.

Do not present uncalibrated scores as approval probabilities, investment returns or legal determinations. Do not invent weights or thresholds as if validated. If you propose illustrative weights, label them, explain tradeoffs and specify required expert review. Investigate whether the approach systematically penalizes disinvested neighborhoods or mission-critical affordable projects. Ease and social value should remain distinguishable.

Propose a small evaluation set of sourced cases, expected findings, failure cases and checks against unsupported claims.

### 8. Determine whether financial scenarios belong in the MVP

Explain the pro forma inputs relevant to this user and stage. Distinguish acquisition/development cost, operating performance, financing sources, affordability targets and funding gap.

Determine whether a financial feature would change the initial decision enough to justify its data and implementation burden. If yes, recommend a narrow user-entered scenario with transparent arithmetic, assumption ranges and sensitivity. If no, explicitly recommend deferring it.

Do not fabricate Pittsburgh construction costs, achievable rents, lender terms, subsidy eligibility or tax treatment. Identify source quality and currency, and distinguish advertised terms from approved financing. State where a qualified practitioner must supply an assumption.

### 9. Find reachable practitioners and ways to validate

Identify a short prioritized list of Pittsburgh nonprofit housing developers, community development corporations and community land trusts. Starting candidates include City of Bridges Community Land Trust, ACTION-Housing and Pittsburgh Community Reinvestment Group. Verify their current work and fit rather than assuming they need our product.

For each, supply an official public contact route, relevant role, why that role would understand the task, a relevant public project or artifact if available, and one useful question. Separate potential product users from organizations that can make introductions. Do not claim availability, interest, endorsement or a relationship.

Suggest a 15-minute discovery interview and a 15-minute prototype walkthrough. Ask about a recent actual case and current artifacts before asking for feature opinions. Provide tests that can falsify demand, expose harmful assumptions or show that a spreadsheet would suffice.

Our fastest access may be the hackathon housing experts during office hours. Provide five high-value questions for them. The deadline falls on a weekend; include a fallback if no outside organization replies. Never invent interviews, quotes, endorsements or feedback. Do not contact anyone or submit forms on our behalf.

### 10. Handle Penny conversation evidence appropriately

Het may be able to review conversations housing nonprofits had with Penny through his work. This is a possible future input, not data you have. Do not assume permission to access it, re-use it for the hackathon, upload it to another service, or publish it.

If authorized, analyze only provided de-identified workflow summaries. Distinguish observed user behavior from Penny's generated claims. Sales or fundraising discussions may not represent housing-development workflows. Note selection bias and avoid turning a handful of conversations into prevalence statistics.

Provide a minimal extraction template: organization type, user role, concrete task, trigger, current tools, handoffs, pain, workaround, desired outcome, evidence type and remaining uncertainty. Exclude names, contact details, donor/tenant information and confidential project details. Any verbatim quote needs appropriate permission; do not place raw conversations in a public repository.

### 11. Review alternatives and differentiation

Investigate existing public portals, professional services, screening products and ordinary manual workflows that solve this task. Ground claims in current official product documentation, sample outputs and documented capabilities. State when access prevents evaluation. Avoid unsupported statements that competitors cannot do something.

Explain whether our proposed tool duplicates an existing free solution, what missing handoff or evidence problem remains, and whether combining sources into an actionable artifact is valuable enough. A conclusion that our initial idea should change is welcome.

### 12. Recommend a two-person weekend product

Return one recommended workflow with a concrete user story, supported input, supported geography/project type, output artifact, source-backed steps, AI responsibility, deterministic calculations, human review and explicit unsupported cases.

Define a finished vertical slice that can be deployed and demonstrated in 3-5 minutes. Separate essential, optional and deferred work. Give two or three sourced Pittsburgh demo candidates if they can be established safely; do not invent parcel facts or imply sites are available for development. Public project precedents may be more reliable than guessing a site's condition.

Describe graceful behavior when a source fails, a parcel is outside jurisdiction, evidence is missing, or the project type is unsupported. Show how provenance survives into a downloaded or shared brief.

Suggest task division by role without assuming our skills, a sensible work sequence, and explicit cut points if data or interviews fail. Do not build an implementation roadmap for a large platform. Keep nonprofit tool adoption, accessible language and the direct challenge ask central.

Pittsburgh design ideas are a small finishing section: locally grounded examples, restrained visual motifs and optional Easter eggs. Do not let branding substitute for correct local functionality.

### 13. Required final output

Begin with a one-page decision memo: recommended user, job, workflow, why it matters, evidence strength, minimum data, largest unknown and next three actions. Then provide:

1. What was already known, newly verified, contradicted and still unknown.
2. Practitioner workflow and existing artifacts.
3. Comparison of candidate interventions and recommended MVP.
4. Pittsburgh jurisdiction/constraint matrix.
5. Data access and join matrix with verification level.
6. Explainable scoring recommendation and validation plan.
7. Pro forma include/defer decision.
8. Prioritized practitioner contacts, interview questions and no-response fallback.
9. Existing alternatives and differentiation.
10. Two-person build boundary and a short demonstration narrative mapped to the actual judging criteria.
11. A go/no-go list: what would make this idea impractical or not worth building.
12. Copyable plain-Markdown research notes and a source register suitable for our research wiki, with title, publisher, URL, publication/effective date, access date, supported claims and limitations.

Make clear where findings are documented, inferred or awaiting interviews. Attach a citation to consequential factual claims. Prefer primary sources; never fabricate citations or quotations. Use tables when they reduce ambiguity. Do not invent market sizes, time savings, budgets, customer willingness to pay, scoring weights or dataset quality. End by identifying the smallest remaining question that blocks product selection. Do not end with a generic list of dozens of possible features.

# Citations

User's Track 1 selection and workflow requirements, September 26, 2026. Participant Packet, Track 1 brief, Rushi's research and organizer catalog preserved in `raw/hackathon/`. This is a research assignment, not a set of verified research findings.
