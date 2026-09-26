---
type: worked-example
title: "1623 Lanark: a manual rehabilitation screen"
description: "A sourced Pittsburgh example testing whether an evidence brief helps decide the next diligence step."
tags: [product, feasibility, pittsburgh, rehabilitation]
status: researched
updated: 2026-09-26
---

# 1623 Lanark: manual screening brief

**Decision supported:** What must a small nonprofit developer clarify before relying on an initial rehabilitation screen or commissioning further diligence?

**As of September 26, 2026.** City of Pittsburgh, Fineview. Parcel ID **`0023C00208000000`**, boundary label **`23-C-208`**. Exact assessment-to-boundary-to-permit identifier matches were tested. Whole parcel geometry was tested against City zoning and slope data. This is a documented project precedent, not an acquisition recommendation or confirmation of availability. [S1-S5]

**Hypothetical proposal:** Retain one existing lawful dwelling, rehabilitate it for an affordable community land trust sale, add no unit or footprint, and undertake no demolition/reconstruction. This is our test scenario, not an account of the actual developer's proposal or past decision. The actual permit history includes more extensive work.

**Screening outcome: reconcile existing-use and condition evidence, then define the work scope. Financial feasibility remains unassessed.** Do not reject the parcel solely because of its assessment classification, or treat permit history as proof of current lawful occupancy.

## Findings that change the next action

| Finding | Evidence and interpretation | Next action |
|---|---|---|
| Conflicting descriptions of the property | September 1, 2026 assessment says `VACANT LAND`. Six parcel-linked PLI records show completed permits; a January 29, 2024 permit describes alterations to an existing single-family dwelling. A CLT listing describes renovated homes. These sources have different purposes and do not establish present condition. [S1, S4, S5] | Obtain current site/structure evidence and City legal-use records. Ask PLI which records establish this dwelling's lawful use. |
| Base zoning mapped to R1D-H | One City zoning feature, ID 634, covers the parcel in a local vertex/edge geometry check. This means single-unit detached residential, high density. The H suffix here is not the separate Hillside district. [S3] | Establish whether the dwelling is attached or detached and whether its existing use is lawful before applying a use rule. |
| Conditional rehabilitation pathway | Current code permits detached single-unit use in R1D. Section 921.03.A.1 allows maintenance/remodeling/repair of lawful nonconforming structures without a variance or special exception if nonconformity does not increase. This does not establish that this structure or proposal qualifies. [S6, S7] | Have the practitioner define structural work, additions, reconstruction and changes of use. Escalate any unresolved classification or increase in nonconformity to City zoning staff. |
| Mapped slope requires attention | The entire parcel polygon was queried and intersects a City `slope25=Yes` feature. Overlap percentage was not calculated. This does not mean the whole site is steep or the work impacts a natural steep slope. [S8] | Locate proposed disturbance before deciding whether a survey, engineer or further City review is needed. |
| Other constraints remain open | Flood, historic designation, undermining, contamination, title, utility capacity, current structural condition and detailed dimensions were not established by this screen. | Mark each not checked or requiring professional evidence. Neither missing data nor completed permits clear these checks. |

A missing Certificate of Occupancy is not automatically evidence of illegal use: the City explains that some existing single-family homes did not require one. County assessment is not the City's legal-use authority. [S9] Current City intake uses the Building and Development Application to combine building and zoning review; permit requirements depend on the actual scope. Do not automatically prescribe both an old ZDR application and a new BDA. [S10]

## Financial evidence, without a fabricated pro forma

| Input | What we actually have | Safe use |
|---|---|---|
| Sale proceeds | CLT page publishes a **$197,500 asking price**, with mixed old/new schedule text. [S5] | A published project asking price, not an achieved sale or an unrestricted market comparable. Net proceeds and applicable affordability/ground-lease terms remain unknown. |
| Rehabilitation cost | Permit `BP-2023-19723` records **$300,000** as `total_project_value`. [S4] | Declared permit value, not verified actual cost or a complete development budget. Do not add permit values together. |
| Acquisition, site work, soft costs, financing/carry, selling costs, contingency | No parcel-specific budget verified. | Practitioner inputs required; unknown is not zero. |
| Grants, contributions, repayable loans, restrictions | No parcel-specific approved funding allocation verified. | Do not allocate pooled project funding to this home or count repayable construction loans as permanent subsidy. |

$300,000 minus $197,500 is $102,500. **That is not a verified funding gap.** The figures describe different things and omit important costs, proceeds and funding. This exercise cannot answer whether the project pencils. A financial module should wait until a practitioner can supply a usable budget and revenue/funding assumptions.

## Development Ease scorecard

This manual experiment tests components before a numerical scale. It does not yet satisfy a finalized scoring specification.

| Component | Current status | Reason |
|---|---|---|
| Legal permissibility | Conditional; review required | Mapped district known, lawful existing use and exact proposal unverified. |
| Physical constraints | Review required; incomplete | Mapped slope intersection; condition and other hazards not checked. |
| Process complexity | Undetermined | Review pathway depends on work scope, lawful use and other designations. |
| Financial feasibility | Unassessed | No complete parcel budget, net proceeds or allocated funding. |
| Evidence completeness | Partial, with an explicit conflict | Identifiers and selected joins verified; substantial checks remain open. |

**Overall Development Ease: not rated.** Evidence completeness is separate from site ease. No approval probability, arbitrary weighted number, or financial return is inferred. Unknowns cannot improve a rating. Mission value is also separate: subsidy need or difficult conditions do not by themselves make an affordable housing project undesirable.

## Three next actions and the proposed handoff

1. **Developer/project lead with PLI and current site evidence:** reconcile the vacant-land classification with the documented dwelling and establish lawful use, unit count and current condition. Do not commission a new-building analysis merely because the assessment says vacant.
2. **Developer with its architect/contractor and City staff as needed:** write the precise work scope and locate any land disturbance. Confirm historic/flood and other applicable checks before assigning a permitting route. No variance has been established as required or available.
3. **Developer's finance/project lead:** supply a redacted parcel budget, expected net sale proceeds, affordability restrictions and confirmed funding. Until then, record financial feasibility as unassessed.

These are suggested responsibilities, not verified staff titles or approval authority at City of Bridges. The candidate handoff is a brief attached to an existing email or project meeting, with sources and unknowns intact. Whether this fits actual practice awaits a practitioner review.

## What this experiment supports, and what it does not

**Documented:** a narrow Pittsburgh record join is possible; actual sources can conflict; the zoning rule changes with lawful existing use and scope; public price and permit value do not provide a pro forma.

**Product inference:** a proposal-specific brief that preserves conflicts and assigns the next evidence request may be more useful than another parcel lookup. This remains unvalidated. One case does not demonstrate coverage, accuracy across Pittsburgh, demand or time saved.

**Smallest utility test:** give a practitioner this brief and ask which finding changes the next diligence action, what they already knew, and which source or document they would actually request. If it changes no action, or duplicates their existing checklist without reducing an evidence problem, do not build the workflow merely because the joins work.

Technical evidence: `docs/lanark-evidence-2026-09-26.md`. Sanitized response snapshots, request scope and hashes: `docs/evidence/lanark-2026-09-26/`. This page and those files must travel together if used as an evidence package. No public redistribution license has been established for every source.

# Citations

All sources accessed September 26, 2026. Webpage update dates identify guidance currency, not necessarily legal effective dates.

| ID | Publisher, title and URL | Date / version | Supports and limits |
|---|---|---|---|
| S1 | Allegheny County / WPRDC, [Property Assessments](https://data.wprdc.org/dataset/property-assessments) | Record ASOFDATE 2026-09-01 | Exact address, ID, assessment classification; not legal use or present condition. Saved selected record. |
| S2 | Allegheny County / WPRDC, [Parcel Boundaries](https://data.wprdc.org/dataset/allegheny-county-parcel-boundaries1) | Retrieved 2026-09-26; individual survey date not established | Exact pin, WKT, EPSG:2272; not a legal survey. Saved selected record. |
| S3 | City of Pittsburgh, [Zoning MapServer layer 0](https://pghbridgis.pittsburghpa.gov/federated/rest/services/Zoning/MapServer/0) | Live query 2026-09-26; feature effective date not supplied | Feature 634 and polygon test; not every overlay or legal determination. |
| S4 | City PLI / WPRDC, [PLI Permits](https://data.wprdc.org/dataset/pli-permits) | Six queried records issued 2021-2026 | Parcel-linked permit descriptions, status, declared values; not actual costs or current occupancy. Exact query scope in manifest. |
| S5 | City of Bridges CLT, [1623 Lanark Street](https://cityofbridgesclt.org/our-properties/lanark1/) | Undated live listing; mixed 2021-2027 schedule references | Published asking price and project description; no verified sale or current availability. |
| S6 | City Title 9, [Chapter 911, Uses](https://ecode360.com/45476515) | Current hosted code; section 911.02 shows amendment effective 2026-06-11 | Detached use permission; attached classification needs separate rule check. Not parcel approval. |
| S7 | City Title 9, [Chapter 921, Nonconformities](https://ecode360.com/45478965) | Current hosted code, accessed 2026-09-26 | Section 921.03.A.1 conditional repair/remodel rule; lawful status required. |
| S8 | City / WPRDC, [25% or Greater Slope](https://data.wprdc.org/dataset/25-or-greater-slope), [actual layer](https://services1.arcgis.com/YZCmUqbcsUpOKfj7/arcgis/rest/services/PGHWebSlope25/FeatureServer/0) | Catalog modified 2026-09-23; terrain observation date not established | Whole parcel intersects feature 636; not disturbance, instability, or a slope survey. |
| S9 | City PLI, [OneStopPGH Permit Center](https://www.pittsburghpa.gov/Business-Development/Permits-Licenses-and-Inspections/OneStopPGH-Permit-Center), [Online Occupancy Search](https://www.pittsburghpa.gov/Business-Development/Permits-Licenses-and-Inspections/References-Resources-and-Forms/Online-Occupancy-Search) | Pages updated 2026-09-23 and 2026-08-06 | Assessment/legal-use distinction and existing single-family occupancy caveat; no parcel search completed here. |
| S10 | City PLI, [Building and Development Application](https://www.pittsburghpa.gov/Business-Development/Permits-Licenses-and-Inspections/Permitting/Building-Development-Application) | Page updated 2026-09-02 | Current combined intake guidance; precise requirements depend on work scope. |
