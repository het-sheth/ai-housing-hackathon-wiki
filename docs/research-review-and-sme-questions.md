# Research review and SME questions

Date: 2026-09-26. Status: discovery, not an accepted product specification.

## Immediate decision

Use the completed Deep Research as a hypothesis inventory. Do not commission another broad report. Ask the housing SMEs to describe the actual decision and artifact before selecting a project type or building a score.

Input reviewed: `/home/het/Downloads/deep-research-report.md`. The original has not been modified. Its numbered references do not resolve to a source register in the downloaded file. Its statement that no integrated database exists overreaches: the evidence only establishes that this report did not demonstrate an integration.

The supplied channel transcript confirms the organizer's question format and September 26-27 office hours, 10 a.m.-6 p.m. Eastern. It does not constitute an expert interview or validation. Steve Wray's tentative answer about unavailable data explicitly awaits organizer confirmation; do not treat it as an eligibility ruling.

## Corrections before implementation

| Report claim or assumption | Assessment | Consequence |
|---|---|---|
| High confidence in nonprofit demand because authoritative datasets exist | Data availability does not establish who needs an output, what they already use, or whether it changes a decision. No practitioner interview is documented. | Keep the user and workflow proposed. Ask for one actual case and artifact. |
| Finance and funder requirements enter after a site seems acceptable | Not a universal sequence. URA disposition asks for preliminary sources/uses and financial capacity early. This is a formal application process, not proof of every nonprofit's internal workflow. | Defer automated pro forma arithmetic for scope reasons, but retain funding-path and mission questions in intake. |
| Parcel and zoning integration is verified | The report explicitly says parcel boundaries and zoning were not fetched. Zoning is assigned spatially, not by assuming every zoning polygon has a parcel ID. | Require a real small join before promising automated coverage. Preserve IDs as strings and test whole parcel polygons, including splits and boundary intersections. |
| Unknown prior variance means assume none | Unsupported and unsafe. City guidance describes public ZBA decisions and obtaining copies. No returned record does not clear a site. | Display unknown; require relevant decision/occupancy review. |
| Stormwater plan required above 5,000 square feet of disturbance, attributed generally to PWSA | Overgeneralized. Current City PLI guidance lists 10,000 square feet disturbance, 5,000 square feet increased impervious area, and a separate RIV trigger. State erosion-control requirements are separate. | Use proposed work quantities, not parcel area as a proxy; keep authority and trigger distinct. |
| Simple R1/R2/R3 descriptions, HRC timing, permit timing, and floodway prohibition | These claims lack usable citations in the supplied export. District labels alone do not establish permission or a permit schedule. | Do not transcribe these statements into a rules engine or promise timelines. |
| Public domain likely; dataset current as of 2026 | Access date does not establish data vintage or reuse terms. | Verify each resource's terms and metadata; do not infer permission or freshness. |
| No free equivalent exists | Not demonstrated. County GIS, City zoning tools, and the Land Bank guide already cover important lookup steps. | Test whether the brief improves the handoff enough to justify another tool. |
| Small multifamily or large single-family as one MVP | These are different concepts with different rules and funding paths. | Select one explicit project type after the workflow question. |

## Bounded data result from parallel research

Terra reported one successful assessment `PARID` to parcel `pin` match for `0001D00128000000`, followed by an interior-point query returning `GT-A`. This is a commercial Golden Triangle test record, not a proposed housing site. The test demonstrates a partial data path only. It does not establish whole-parcel zoning coverage, a hazard join, a use permission, or general match rates. The advertised PASDA parcel service returned HTTP 500 during that audit; the WPRDC datastore supported the small lookup.

The audit is preserved in `docs/partial-data-audit-2026-09-26.md`. Its original point-query recipe must not be treated as the application's spatial method: even a guaranteed interior point can miss a second zoning district or overlay elsewhere on the parcel. Whole-polygon intersection and explicit split/boundary handling remain required before claiming parcel-level screening.

## Posting sequence

Het rejected question 1 as the starting point and requested a clearer understanding of the problem, all four personas, existing products and judging fit. Do not present that rejected draft as the agreed next action. The drafts below are retained as earlier options, not approved messages. A broader problem-discovery question is being prepared. Keep each question in its own thread, as requested by the organizer. The objective is useful correction, not posting volume. No evidence in the packet makes the number of channel posts a judging criterion.

No messages have been sent and no forms have been submitted. These drafts do not imply product approval, relationships, practitioner interest, or organizer endorsement.

### 1. Validate the actual handoff

```text
Team / track: Het and Rushi, Track 1: Development Feasibility Navigator

What we are building: We're exploring a one-page Pittsburgh site brief for a small nonprofit developer or community land trust, showing sourced findings, unknowns, and next checks before spending on due diligence.

Our question: Could someone walk us through one recent site you considered: what did the person screening it hand to whoever approved the first survey, title review, or other paid diligence? An anonymized description of the document or conversation would help.

What we currently believe: The useful output may be a brief someone can bring into an existing email or meeting, but we haven't validated who uses it or whether public-data lookups are actually the bottleneck.
```

### 2. Test whether funding is the earlier gate

```text
Team / track: Het and Rushi, Track 1: Development Feasibility Navigator

What we are building: We're considering a single-site screening brief for a small nonprofit evaluating affordable housing in Pittsburgh.

Our question: In a recent small infill or rehabilitation project, did funding or site control rule the site out before zoning and physical diligence? What was the minimum information needed to make that call?

What we currently believe: We can leave a full pro forma out of a weekend prototype, but we shouldn't assume financing only matters later. We want to choose one project type where the early screen can still be useful.
```

### 3. Ask about current authoritative records

```text
Team / track: Het and Rushi, Track 1: Development Feasibility Navigator

What we are building: A source-linked first screen for a City of Pittsburgh parcel and a proposed housing use.

Our question: When screening a parcel today, which City record should we check for prior zoning decisions or conditions that the zoning map alone would miss? Is there one public example we could use to test this?

What we currently believe: Parcel geometry and the district map are starting points. They don't establish legal use or tell us that no variance or approval condition exists, and missing records should stay unknown.
```

### 4. Clarify the direct challenge ask with an organizer

```text
Team / track: Het and Rushi, Track 1: Development Feasibility Navigator

What we are building: A Development Ease scorecard with separate zoning, physical, infrastructure, and process findings, each linked to evidence and unresolved questions.

Our question: For the Track 1 requirement, is a component scorecard without one aggregate number acceptable, or is a single numeric Development Ease Score expected? We'd appreciate an organizer clarification.

What we currently believe: Combining unknown utility capacity and known zoning facts into one number could imply certainty we don't have. We can show the barriers and next actions clearly, with evidence coverage separate from ease.
```

### 5. Obtain a useful public test case

```text
Team / track: Het and Rushi, Track 1: Development Feasibility Navigator

What we are building: A small Pittsburgh site-screening workflow, with a public example to test whether its findings and next steps are useful.

Our question: Can you point us to one public small housing project where an early issue changed whether or how the developer proceeded, with a decision, checklist, or project document we can inspect?

What we currently believe: A documented project is a better test than picking a vacant-looking lot and guessing its constraints. We won't imply the example site is currently available or approved for our proposed use.
```

## Record answers without overclaiming

For each answer record: question, date, respondent's stated role, source/thread reference, whether it describes firsthand behavior or general advice, anonymized case and artifact, what changed in our hypothesis, remaining uncertainty, and permission for any public attribution. Do not copy personal or confidential project details into this public wiki. An SME's product opinion is not an organizer rule interpretation unless they are authorized to give it.

If nobody answers, show a clearly labeled hypothesis-driven prototype using a public project precedent and manually checked source facts. Do not claim user validation. Keep unsupported legal and utility checks unknown. The smallest question blocking product selection remains: what exact information or artifact changes the decision to authorize the first paid diligence?

## Source register

Access date for all public sources below: 2026-09-26. Publication/update dates do not necessarily establish statutory effective dates.

| Title and publisher | URL | Date | Supports | Limits |
|---|---|---|---|---|
| Completed Deep Research export, supplied by Het | Local file `/home/het/Downloads/deep-research-report.md` | Supplied 2026-09-26; report research date not stated | Proposed brief, scope, and claims audited above | Missing bibliography; not independently verified evidence |
| Participant Packet, AI for Housing organizers | Local source `raw/markdown/participant-packet.md` | 2026 event; build September 26-27 | Six judging criteria, deadline, office hours, disclosures | No numerical judging weights; no ruling on component-only score |
| Housing SME channel transcript, supplied by Het | This conversation | Supplied 2026-09-26; individual message dates partly absent | Required posting format, thread guidance, tentative answer awaiting organizer | Not interviews or validation |
| How to Develop Property with the URA, URA | https://www.ura.org/media/W1siZiIsIjIwMjUvMDcvMjEvNXl2cWpneG1yc19EaXNwb1Byb2Nlc3NfQ2hlY2tsaXN0X0FwcjIwMjUucGRmIl1d/DispoProcess_Checklist_Apr2025.pdf | April 2025 | Preliminary financial and community materials in disposition | URA-owned land process, not universal nonprofit practice |
| Building & Development Application, City PLI | https://www.pittsburghpa.gov/Business-Development/Permits-Licenses-and-Inspections/Permitting/Building-Development-Application | Updated 2026-09-02 | Combined BDA replaces separate ZDR and building intake | Other City pages retain older terminology |
| Stormwater Permit, City PLI | https://www.pittsburghpa.gov/Business-Development/Permits-Licenses-and-Inspections/Permitting/Stormwater-Permit | Live guidance; effective date not established here | Disturbance and impervious-area thresholds; RIV exception | Does not cover all other environmental obligations |
| Chapter 102 Permit Resources, Allegheny County Conservation District | https://www.accdpa.org/chapter-102-permit-resources | Undated live guidance | Separate E&S and NPDES pathways | Confirm project-specific application and review authority |
| Zoning Board of Adjustment process guide, City Planning | https://www.pittsburghpa.gov/files/assets/city/v/1/dcp/documents/process-guides-and-handouts/process-guide-handout-zba-2024.pdf | December 2024 | Decision records, evidence and hearing process | Guidance, not a substitute for applicable code |
| How to Buy Vacant, Blighted, or Tax-Delinquent Property, Pittsburgh Land Bank | https://pghlandbank.org/how-to-buy-vacant-blighted-or-tax-delinquent-property-in-pittsburgh/ | Undated live guide | Existing free lookup workflow and different acquisition routes | No parcel-specific assurance or availability |
| Zoning, City Planning | https://www.pittsburghpa.gov/Business-Development/City-Planning/Zoning | Updated 2026-05-28 | City jurisdiction, official map, code and occupancy links | Map alone does not establish approval |
