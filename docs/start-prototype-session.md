# Start the housing prototype in a fresh session

Copy everything below the separator into the new coding session. This is an execution handoff written September 26, 2026, not another research assignment.

---

You are helping Het and Rushi build a working AI housing prototype for Track 1, Development Feasibility Navigator, in the AI Horizons AI for Housing Hackathon. Start building a small local prototype now and iterate with me. Do not spend the session reopening broad discovery, producing another giant plan or asking whether you may create the repository. I explicitly authorized a separate local application and a quick prototype. Read the minimum relevant context, write a short build plan, then implement and verify a usable first slice.

## Outcome and time boundary

The event deadline is September 27, 2026 at 11:59 p.m. Eastern. The previous session was September 26. Check the actual current time. Het has Saturday and Sunday; Rushi's availability is unknown. This is a two-person prototype, not a production planning platform.

The direct Track 1 ask is an AI-driven Development Ease Score exposing bottlenecks, variance questions and infrastructure gaps. Judging criteria are Problem Value, User Fit & Usability, Technical Execution, Data & AI Integrity, Actionability and Continuation Potential, with no numeric weights supplied. Build towards a 3-5 minute real Pittsburgh demonstration. Be explicit about what the first iteration does not yet satisfy.

## Repository, authorization and stack

Create `/home/het/personal/ai-housing-navigator` as a NEW local Git repository if absent. If it now exists, inspect its instructions, status and current work instead of overwriting it. Start on a feature branch, for example `feat/first-prototype`. Preserve event-time history. Do not add an attribution trailer. Do not create an app remote, deploy or send messages without subsequent authorization. Do not merge research PRs as part of app setup.

Use React + TypeScript + Vite as the pragmatic default for this quick prototype unless I give a different preference. That stack was recommended, not previously installed or formally selected. Choose a package manager consistently and commit its lockfile. Keep infrastructure minimal. Add a small server-side API boundary only when needed for live source access or model calls. No authentication, database, billing, queues, workflow platform or generic chat interface is required for the first slice. Never put a model API key in Vite/browser code or a VITE_ variable. Do not read credential files, including .env files, under this machine's rules; ask me to configure needed credentials through an approved mechanism without pasting secrets into chat.

The research wiki is `/home/het/personal/ai-housing-hackathon-wiki`, separate from the app. Do not run a generator inside it. Its public PR is https://github.com/het-sheth/ai-housing-hackathon-wiki/pull/3 , last verified open. PRs #1 and #2 are merged and their branches deleted. Main tracks origin/main; auto-delete merged branches is enabled. Research branch: `docs/proposal-comparison`.

The hackathon permits libraries, frameworks and public data with disclosure, but prohibits previous project code. Write fresh application code. Do not copy code from Het's other apps, the wiki template, research scripts or old implementation plans. Research findings and cited public facts are inputs, not code to transplant. Preserve source licenses/terms; do not imply all downloaded data is public domain. No organizer ruling on ambiguous reuse questions has been obtained.

Read the nearest AGENTS.md/DIRECTORY.md and applicable machine rules before filesystem searches. Do not search the whole laptop. No em dashes in authored text. Keep progress updates brief and frequent. Existing approval to build is sufficient for ordinary reversible local implementation choices.

## Read only these starting documents

In the research wiki:

1. `docs/handoffs/current.md` for the latest state and any newer steering.
2. `wiki/product/proposal-comparison.md` for the working product hypothesis.
3. `wiki/product/lanark-worked-example.md` for the real case and safe statements.
4. `docs/initial-rule-contract.md` for the initial conditional rule trace and failure cases.
5. `docs/lanark-evidence-2026-09-26.md` and `docs/evidence/lanark-2026-09-26/manifest.json` when implementing adapters.

Consult `wiki/research/action-housing-video-findings.md` and `docs/typesafe-evaluation-2026-09-26.md` only for their relevant decisions. Do not reload every PDF, all 60 catalog entries, the full video transcript or the entire wiki. This prompt supersedes older blanket statements that no app start was authorized. It does not establish demand, finalized scope, a validated scoring rubric or Rushi's agreement.

## Problem and user

Primary user hypothesis: a project lead at a small nonprofit housing developer considering a potential project before committing to further diligence. A small private developer may also fit, but do not build separate persona interfaces.

They need to understand: for this property and this proposed work, which rule checks matter, what changes if the scope changes, what remains uncertain, and who can resolve it?

Existing parcel reports already exist. Rescope advertises cited parcel zoning/overlays and screening workflows. We have not tested its Pittsburgh support or proven it lacks comparisons. Our differentiation hypothesis is a comparison of user-defined proposals that explains changed checks and preserves the housing objective. Do not claim market uniqueness or invented competitor weaknesses.

## First usable interaction

Build one connected flow, not an analytics dashboard:

1. Select the real Pittsburgh demonstration property. Make it obvious if the initial iteration supports only that case. A working demo selector is preferable to an address box that pretends to search.
2. Confirm the property and see a small parcel view, with jurisdiction and source date. A simple correctly projected parcel SVG is sufficient; do not spend the first iteration on a fancy basemap.
3. Describe a housing proposal through clear fields: existing and proposed unit count, lawful existing use known/unknown, repair versus expansion versus reconstruction, and whether land disturbance is proposed. Never default unknown to no.
4. Compare two proposed scopes on the SAME parcel. Candidate first pair: same-use repair/remodel within an existing footprint versus expansion. These are hypothetical scenarios, not claims of approved or feasible alternatives at Lanark.
5. Display what changed, what did not change and what cannot yet be determined. Each finding shows the relevant source, conditional reasoning, missing input and next action. Changes in proposal do not erase property-record conflicts.
6. Export a readable Markdown brief at minimum. Browser print styling is a useful small addition; a sophisticated PDF pipeline is not required initially. Include both proposals, facts, assumptions, conflicts, sources/dates and unresolved checks in the export.

Prefer a calm, accessible UI: clear labels, keyboard navigation, readable text, responsive layout, restrained Pittsburgh bridge/gold references. Plain language and correct jurisdiction come before decoration. No generic chatbot or generated massing simulator.

## What we have actually verified

Real demonstration: 1623 LANARK ST, Fineview, City of Pittsburgh. PARID/pin/parcel_num `0023C00208000000`, readable block-lot `23-C-208`. Keep identifiers as strings with leading zeroes.

- Exact assessment-to-boundary-to-permit matches were tested for this one case.
- Assessment ASOFDATE 2026-09-01: USEDESC `VACANT LAND`, lot area 1,657 sq ft.
- Whole parcel geometry against City zoning returned R1D-H, SINGLE-UNIT DETACHED RESIDENTIAL HIGH DENSITY, feature 634, status Approved. A bounded local vertex/edge test found the parcel inside that zoning feature. Approved is a layer attribute, NOT project approval. The H suffix is high density, not the separate H Hillside district.
- Whole parcel intersects the City >=25% slope layer. Overlap percentage and proposed disturbance were not determined. This is not a slope survey or automatic review verdict.
- Six completed PLI records were returned by parcel ID. BP-2023-19723, issued January 29, 2024, describes work to an existing single-family dwelling and lists total_project_value 300000. Permit status is not a current condition inspection, legal occupancy certificate or cost audit.
- The assessment classification and dwelling permit history conflict. Keep both. Do not label the site empty, clear, approved or rejected based on one source.
- A City of Bridges listing publishes a $197,500 asking price. It is not a achieved sale/market comp. $300,000 permit value minus $197,500 asking price is NOT a funding gap. Keep financial feasibility unassessed.
- Flood, historic designation, undermining, title, utility capacity, structural condition, contamination, existing lawful use and complete dimensional compliance are NOT verified by this screen.

Do not confuse 1623 Lanark with 21 Lanark, a different property in an advocacy article. No availability/acquisition recommendation is established for our demo property. Do not fabricate missing geometry or facts.

## Data sources and authority boundaries

There is no demonstrated central database that certifies all project feasibility. WPRDC distributes several datasets; OneStopPGH handles City processes/records. Neither makes County assessment classification a City legal-use decision.

| Need | Source and implementation detail | Boundary |
|---|---|---|
| Assessment/address/ID | WPRDC https://data.wprdc.org/dataset/property-assessments . CKAN https://data.wprdc.org/api/3/action/datastore_search , resource_id `property_assessments_table`. Exact string PARID filter or whitelisted exact address fields. | County assessment/tax facts, not legal use or present physical condition. Postal city text alone is not proof of City jurisdiction. |
| Parcel geometry | https://data.wprdc.org/dataset/allegheny-county-parcel-boundaries1 . Same CKAN endpoint, resource_id `858bbc0f-b949-4e22-b4bb-1a78fef24afc`, filter pin. Fields pin, map_block_lot, municode, wkt. | WKT in EPSG:2272, US survey feet. Not a survey. Validate municipality and CRS; do not treat projected coordinates as longitude/latitude. |
| Base zoning | https://pghbridgis.pittsburghpa.gov/federated/rest/services/Zoning/MapServer/0/query | Polygon query with geometryType=esriGeometryPolygon, inSR=2272, spatialRel=esriSpatialRelIntersects, outFields=OBJECTID,zon_new,full_zoning_type,status, f=json. Retain all intersecting zones. Point/centroid hits cannot establish whole-parcel coverage. |
| Legal rules | https://ecode360.com/45474054 , uses https://ecode360.com/45476515 , nonconformities https://ecode360.com/45478965 | Current code sections and amendments govern the small rule set. Check effective dates and linked exceptions; do not feed the entire code to a model and accept its verdict. |
| City process/legal-use evidence | https://www.pittsburghpa.gov/Business-Development/City-Planning/Zoning ; City OneStopPGH Permit Center and Online Occupancy Search | City guidance says assessment is not legal-use authority. Some older single-family homes may have no required occupancy certificate; absence alone is not illegality. Detailed record review can remain a human next action. |
| Permit history | https://data.wprdc.org/dataset/pli-permits . CKAN resource_id `f4d1177a-f597-4c32-8cbf-7885f56253f6`, exact parcel_num filter. | Permit ID/date/description/status, not proof of actual cost, current occupancy or permission for a new proposal. Address-only search missed records in our test. |
| Slope flag | https://data.wprdc.org/dataset/25-or-greater-slope ; https://services1.arcgis.com/YZCmUqbcsUpOKfj7/arcgis/rest/services/PGHWebSlope25/FeatureServer/0/query | Whole parcel intersection in correct CRS; mapped slope is not a geotechnical conclusion or proof work affects it. |
| Flood, optional later | FEMA National Flood Hazard Layer: https://www.fema.gov/flood-maps/national-flood-hazard-layer | Endpoint, map effective date and actual join have NOT been tested in this prototype. Show not checked. |
| Historic/overlays, optional later | City zoning/historic preservation authorities and their authoritative GIS/records | Base zoning is not all overlays. No complete authoritative integration established. |
| Environmental/mining, optional later | PA DEP eMapPA, state mining information; WPRDC undermined-areas catalog | No parcel diagnosis, complete coverage or tested app adapter established. Do not infer contamination absence. |
| Title/access/easements | Recorded deeds/plans and qualified title/survey review | Assessment ownership or map lines do not establish clear title or lawful access. No title search performed. |
| Utility service/capacity | Relevant utility's project review | Nearby lines or prior permits do not confirm capacity for the proposal. Not machine-cleared in this prototype. |
| Budget/financing | Practitioner budget, costs, net proceeds, restrictions and confirmed funding | Do not substitute ACS/HUD neighborhood estimates or advertised financing terms. No financial engine in first slice. |

Source steward/terms metadata in the research audit: assessment CC0; PLI Creative Commons Attribution; parcel/slope license unspecified; City zoning reuse license not verified. Use small documented requests and record provenance. Avoid owner/contact/contractor fields. Do not silently bulk-download portals. Do not assume licenses for application redistribution.

Implement a fresh source adapter, using URLSearchParams/encoded filters and field whitelists. Start with the known parcel ID rather than full fuzzy geocoding. Preserve `asOf`, `retrievedAt`, source URL/resource ID and whether evidence is live, a dated snapshot or user-provided. Exact record values can be referenced from research, but do not copy old implementation. If a source is unavailable, show that and allow a clearly labeled verified-date demo snapshot. No silent fixture substitution. A network error is not zero results, and zero results is not absence of constraint.

## Rule and score boundaries

Read and validate the small rule contract. Section 921.03.A.1 is a conditional maintenance/remodel/repair pathway for lawful nonconforming structures when nonconformity does not increase. Expansion invokes a different check, including section 921.03.D.1. Attached/detached classification and current/proposed use matter. Do not conclude either scenario is permitted, a variance is needed or a variance will be granted merely from the mapped district.

Use a transparent Development Ease component scorecard: legal permission, site constraints and process complexity, with financial feasibility explicitly unassessed. Use descriptive states such as conditional, review required and unknown. Keep evidence completeness separate. Do not invent numeric weights, convert model confidence into feasibility, or label it an approval probability. Overall not rated is valid for incomplete evidence in this iteration. Whether a component-only presentation satisfies organizers' final score expectation is unresolved; disclose it as a completion gap, not a solved requirement.

Known contradictions must block definitive clearance even if a user selects a favorable assumption. Show user-entered assumptions as assumptions, not verified facts. Allow comparing hypothetical branches without overriding the real evidence.

## AI and TypeSafe/Jev

Het asked about typesafe.ai. Docs show Jev produces typed Choice/Score/Noul decisions, not prose. An optional role is classifying an unstructured proposal into separate bounded fields with explicit unknown outcomes, followed by user confirmation. Code owns joins, geometry, arithmetic and reviewed rule predicates. If the inputs are already structured, do not add a redundant model call.

No model provider, account, API key, budget or access has been established. Do not let signup/access block a working deterministic UI. Build a clean optional adapter boundary and label AI unavailable if it is unavailable. Never pretend fixtures or templates are live AI. If a generative provider is available through an approved setup, explanations must cite retrieved evidence and not invent rules. Do not search secret files for keys.

TypeSafe sources: https://docs.typesafe.ai/introduction , https://docs.typesafe.ai/sdk/javascript , https://docs.typesafe.ai/model-jaggedness/jev-1.13 . SDK @typesafe-ai/sdk documents Node20+. Early access and actual housing-domain performance remain unverified. Model confidence is not site ease. Jev weaknesses include arithmetic, multi-hop reasoning and adversarial inputs. Do not make it the legal authority.

## Practitioner evidence and what not to overclaim

The ACTION-Housing YouTube video https://www.youtube.com/watch?v=vJ0ReB26gVA was uploaded April16,2024, duration71:01. We retrieved and reviewed the full automatic-caption track, not fully verified audio/video. The captions contain errors.

At roughly29-32min the speaker describes preferring one taller building to two because of duplicated costs, with actual design shaped by community discussions. Around41min he describes a utility-related delay. Around57-58min he names schematic design, environmental work and a market study as paid diligence artifacts. This supports the relevance of tradeoffs and staged diligence, but comes from multifamily rental development, not validation of our single-home workflow. Funding is material even though the financial engine is deferred. Do not quote old costs or parking rules as current facts. Full transcript stays out of the public repo.

No practitioner has reviewed our proposed interface. No endorsement, interview, willingness-to-pay or time savings is established. Rushi has not confirmed the suggested split. Penny/customer records are not authorized inputs.

## Build order and acceptance checks

Work in short iterations. First get a real local URL with one complete case-to-comparison-to-export flow. Do not spend the session only creating plans or mocks.

1. Create the isolated app repo, concise README/AGENTS, disclosure/limitations note and short implementation plan. State stack defaults. Record commits during event work.
2. Implement the minimal typed evidence model and safe deterministic rule states, with focused tests for consequential behavior.
3. Build the usable interface with the known demonstration case, honest data mode, editable proposal pair, changed/unchanged checks and provenance panel.
4. Wire one fresh small live data request where feasible. Resolve failures without losing the demo. Keep unsupported searches explicit. Expand adapters after the initial flow is working.
5. Implement export, then verify UI and downloaded output. Add an optional actual model integration only if access is available and it improves a named task.
6. Run typecheck, tests and production build; inspect the running interface. Use browser tooling if available, reading its skill. If browser verification is unavailable, say exactly what was and was not exercised.
7. Finish with local path, branch, exact run command/URL, what works, evidence mode, remaining gaps and the next smallest iteration. Do not push/deploy without separate authorization.

Meaningful tests must catch: leading-zero loss; unknown lawful use becoming permission; added unit/expansion entering repair-only logic; a persistent source conflict disappearing between proposals; network failure becoming no constraints; outside-City/unsupported input receiving a fake result; and export losing sources or assumptions. Test the implementation actually built, not imaginary broad coverage. Do not write redundant tests for every label/style change.

The first local slice is not the final hackathon submission. It must honestly identify remaining AI, score-rubric, live-data and practitioner-validation gaps. Make those gaps easy to close rather than pretending they are done.

## Collaboration and communication

You are the orchestrator. Use small, bounded agents when they save time, and reuse available agents with relevant context. Previous thread had practitioner (Sol), data (Terra) and alternatives (Luna); those may not exist in this fresh session. Do not assume cross-session access. Avoid a large swarm or repeated full-research dispatches. A code/source reviewer is more useful now than more generic market research.

### Delegate by task difficulty

Use Astra, Sol and Luna subagents where available. This is explicit authorization for bounded delegation, not a large swarm. These are coding/research assistants, not a choice of runtime model for the housing app.

| Model | Assignments | Boundary |
|---|---|---|
| Sol (`gpt-6-sol`) | Default implementation: UI flow, typed evidence model, source adapters, export, focused tests and ordinary debugging | Give one clear deliverable and owned files. Escalate a concrete blocker instead of reopening the whole design. |
| Luna (`gpt-6-luna`) | Bounded support: source-register checks, documentation consistency, UI copy/accessibility checklist and explicit smoke-test checklists | No sole responsibility for legal interpretation, geometry correctness or the scoring rubric. Verify consequential output. |
| Astra (`gpt-6-astra`) | Difficult cross-source/rule ambiguity, nontrivial geometry or reasoning bugs, and independent review of evidence handling and rule-state transitions | Use on a named hard question or focused review, not routine scaffolding. Review does not establish legal authority or replace practitioner confirmation. |

The orchestrator owns the plan, shared interfaces, integration, running the app and final verification. Do not delegate everything and wait. Start with Sol on a clearly bounded implementation task while the orchestrator handles an independent part. Add Luna or Astra only when a concrete useful task exists; all three need not run on every iteration. Keep at most two child agents active at once by default. Parallel work must have non-overlapping file ownership; sequence work with unresolved shared interfaces. Reuse agents with relevant context. In a new session, spawn fresh ones only if previous agents are unavailable, and pass a concise task brief plus exact relevant files instead of the entire research history.

For supported model overrides use the exact IDs above and the tool's compatible context/fork setting. If a model or subagent tool is unavailable, report the limitation briefly and use the closest available capability or implement directly. Do not let delegation setup delay the first running prototype. Never describe a review or test as completed without its actual result.

Keep the main branch of the research wiki out of application work. Avoid unrelated cleanup. Do not send messages to SMEs or Rushi on my behalf. Do not ask me to confirm routine choices already authorized here. If something genuinely blocks the app, ask one precise question while completing independent work. The goal is a working small prototype I can react to, then quick iteration.
