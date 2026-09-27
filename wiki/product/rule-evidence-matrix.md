---
type: concept
title: Pittsburgh one-detached-dwelling rule evidence matrix
description: Narrow source-backed applicability contract for one proposed new detached dwelling, with unresolved parcel and rule dependencies.
tags: [zoning, evidence, applicability, track-1]
status: researched
updated: 2026-09-27
---

# Pittsburgh one-detached-dwelling rule evidence matrix

Research draft checked September 27, 2026. This is a proposed applicability contract for a future deterministic check, not an implemented rule, a parcel finding, or a permission decision. The **zoning-use** and **zoning-other** rubric factors remain unassessed. No Development Ease Score or numeric contribution follows from this matrix. A practitioner must review the rule interpretation and a real case before either factor can become assessed. ADR 0008 in `docs/adr/0008-gate-preliminary-scoring-on-complete-evidence.md` controls the score gate.

## Supported proposal and stop conditions

The narrow candidate is **one newly proposed detached dwelling unit on one confirmed zoning lot wholly within Pittsburgh**, with no additional unit, attached form, mixed use, or other work activity that changes the use classification. Countywide intake still accepts every activity and combination. A proposal outside this candidate remains in the workspace with a specific unresolved rule task; it is never relabeled as this candidate.

Even for this candidate, the rule text alone cannot establish that an actual parcel is in R1D, that the lot and plans satisfy development standards, that no overlay or exception applies, or that the existing lawful condition is known. A mapped R1D label is only a district observation. The controlling zoning map is maintained by the Zoning Administrator, and the original map controls a classification dispute under Section 902.03. [S1, S2]

## Applicability and evidence matrix

| Gate | Official rule or authority located | Required case evidence | Current output and next action |
| --- | --- | --- | --- |
| Whole-lot City jurisdiction and mapped district | The City zoning page limits Title 9 to City boundaries. Section 902.03 makes the adopted Zoning District Map part of the Code and assigns disputed classification to the Administrator's original map. [S1, S2] | String parcel ID; validated full parcel geometry; whole-lot municipality result; map layer identity and retrieval time; complete zoning polygons and district suffix; any source conflict. | `unresolved` until the whole lot and municipality are established. If a boundary is split, ambiguous or disputed, request City confirmation rather than selecting a favorable polygon. GIS is an observation, not the controlling legal determination. |
| Proposed use classification in an R1D use subdistrict | Section 911.02 defines Single-Unit Detached Residential as one detached housing unit on a zoning lot and marks that use `P` in the R1D column. Section 911.01.B says `P` remains subject to every other applicable Code regulation. Section 903.02.A directs R1D primary uses to the use table. [S3, S4] | Confirmed proposal: one dwelling, detached form, one zoning lot, and no extra activity that changes classification; whole-lot R1D use-subdistrict observation; code text/version checked at run time. | At most `use_table_candidate` with section citations. Never translate `P` into project approval or a cleared zoning factor. If the form, unit count, lot count, district, or activities differ or are unknown, retain `outside_narrow_scope` or `unknown` and ask for the specific missing fact. |
| Development subdistrict and dimensional controls | Section 903.03 supplies different standards by suffix, including lot size, setbacks and height. It refers to contextual setback/height provisions in Sections 925.06 and 925.07 and environmental standards in Chapter 915. Section 925.01 contains limited small-lot provisions, including a potential Administrator's Exception; those are not automatic. [S4, S5] | Exact district suffix; surveyed lot dimensions and legal lot history; scaled plan with footprint, setbacks, height and ground disturbance; applicable contextual measurements and exception evidence. | `unassessed`. Do not infer compliance from parcel area, a GIS outline or a one-unit use-table mark. Request a plan and applicable standards review. Do not call an undersized lot prohibited or exempt without its legal history and City review. |
| Overlays and site-specific standards | The use table warns that overlay districts can add requirements. Title 9 contains environmental overlays in Chapter 906 and development overlays in Chapter 907. Chapter 906 includes floodplain, landslide-prone, undermined and steep-slope provisions. [S3, S6, S7] | Complete applicable overlay inventory for the whole lot, effective map/version, proposed work location and disturbance, site evidence where a mapped condition is relevant, and any City determination. | `unassessed`. An intersection is a review flag; no returned intersection is not a clearance. Request overlay applicability and any site/professional review before a zoning-other conclusion. |
| Existing condition, lawful use and nonconformity | Section 921.01.F places the burden of showing a lawful nonconforming use or structure on the owner when that status is claimed. The City's zoning page says a property's current Certificate of Occupancy documents legal use. The City's property-certification guidance says a property certificate alone does not prove legal occupancy or full Code compliance without a Certificate of Occupancy for the actual use. These occupancy records address an actual use, not a requirement to prove occupancy on a genuinely vacant lot. [S1, S8, S9] | Current on-site condition and relevant lot/City records to establish whether the lot is vacant; if an existing use, structure or nonconformity is claimed, the applicable Certificate of Occupancy, City records response, prior approvals and legal-history evidence; demolition/reconstruction scope and conflicting assessment or permit history when present. | `unknown` until the relevant baseline is established. A genuinely vacant lot with no existing-use or nonconformity claim can follow the current-condition and lot/City-records evidence path without a Certificate of Occupancy. County assessment classification or permit history alone cannot settle a conflicting condition or prove an existing right. Request owner/City evidence for any conflict or claimed exception. |
| Review authority and route dependency | Section 922.02 states that records of zoning approval generally cover regulated development and allows the Zoning Administrator to request plans or a survey when records are insufficient. This matrix does not encode a filing route. [S10] | Current City application guidance and scope-specific confirmation, documents and responsible reviewer. | `unassessed` process factor. Track the separate process matrix, including the new Building & Development Application guidance, before telling a user which application to file. |

## Rule version and evidence record required for a future run

Store `jurisdiction`, `parcel_id` as a string, `proposal_version`, `rule_set_id`, each cited section URL, section or ordinance effective date if established, retrieval timestamp, map layer ID and retrieval timestamp, full-lot match method, observed district and suffix, conflicts, unknowns, and reviewer identity/version. The current draft uses `pittsburgh-one-detached-rule-research-2026-09-27`; it is **not** an approved production rule version. The eCode pages were accessible to this research check on September 27, 2026, but the application handoff records an HTTP 403 from an earlier bounded server request. Automated retrieval is therefore unverified. The pages list section amendment histories, but this review did not establish a complete point-in-time consolidated code snapshot or inspect later pending legislation. Recheck the applicable text and effective date before implementation and each rule update. [S3, S4, S10]

## Deterministic cases before practitioner review

1. One confirmed detached unit, full-lot Pittsburgh and one mapped R1D suffix: return only a cited use-table candidate; keep dimensions, overlays, lawful baseline, process and overall zoning factor unassessed.
2. County parcel in another municipality, split City boundary, split district, stale map response or conflicting district records: return unresolved jurisdiction/district, with no Pittsburgh use-table result.
3. Two units, attached form, additional dwelling, mixed use, demolition/reconstruction, or an unknown form: retain the user's proposal and return outside narrow scope or unknown with the missing fact; never substitute a one-unit detached proposal.
4. R1D observation with missing suffix, lot dimensions, plans or legal lot history: do not infer dimensional compliance or a small-lot exception.
5. Overlay intersection, no intersection, source error and unknown coverage: keep each distinct. Neither a zero intersection nor a map-layer error clears an overlay or site condition.
6. Current site evidence and relevant lot/City records support a genuinely vacant lot, with no existing-use or nonconformity claim: record that baseline without requiring a Certificate of Occupancy. If a vacant-land assessment conflicts with dwelling permit history or other use records, preserve both and seek City/owner clarification. Require a Certificate of Occupancy or other legal-use evidence for an actual-use claim and Section 921.01.F evidence only for a nonconformity claim. Do not infer that a new build, repair exemption or variance route is settled.
7. A code page that cannot be retrieved or whose version differs from the pinned review version: return a source/version error, retain the prior dated finding for reference and require re-review before any factor is assessed.

The next step is a practitioner review of these gates against the current Code and one real, consented case. Record corrections and source versions before proposing application logic. No outreach is authorized by this page.

# Citations

Official sources checked September 27, 2026. Links identify the page used; they do not certify a parcel-specific interpretation.

1. **S1:** City of Pittsburgh, [Zoning](https://www.pittsburghpa.gov/Business-Development/City-Planning/Zoning), City jurisdiction, map and Certificate of Occupancy guidance.
2. **S2:** City of Pittsburgh, [Title 9 Section 902.03, Zoning Map](https://ecode360.com/45474093), adopted map and disputed classification.
3. **S3:** City of Pittsburgh, [Title 9 Sections 911.01-911.02, Primary Uses](https://ecode360.com/45476538), single-unit detached definition, R1D use-table mark and other-regulations condition.
4. **S4:** City of Pittsburgh, [Title 9 Sections 903.02-903.03, Residential Zoning Districts](https://ecode360.com/45474194), R1D use reference and development-subdistrict standards.
5. **S5:** City of Pittsburgh, [Title 9 Section 925.01, Minimum Lot Size](https://ecode360.com/45479734), recorded-lot and Administrator's Exception provisions.
6. **S6:** City of Pittsburgh, [Title 9 Chapter 906, Environmental Overlay Districts](https://ecode360.com/45475180), overlay categories and conditions.
7. **S7:** City of Pittsburgh, [Title 9 Chapter 907, Development Overlay Districts](https://ecode360.com/45475328), additional overlay framework.
8. **S8:** City of Pittsburgh, [Title 9 Section 921.01.F, Nonconformities](https://ecode360.com/45479031), burden of showing lawful nonconforming status.
9. **S9:** City of Pittsburgh, [Property Certification](https://www.pittsburghpa.gov/Business-Development/City-Planning/Zoning/Planning-Applications-and-Processes/Property-Certification), limits of certification and occupancy evidence.
10. **S10:** City of Pittsburgh, [Title 9 Section 922.02, Record of Zoning Approval](https://ecode360.com/45479034), development review and plans or survey when needed.
