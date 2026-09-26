---
type: concept
title: Live metadata checks
description: Access checks for six core data sources on September 26, 2026.
tags: [housing, data, verification]
timestamp: 2026-09-26T00:00:00Z
status: researched
---

# Live metadata checks

Six landing pages were inspected. No full datasets or underlying records were downloaded or validated. A reachable catalog page does not establish API success, completeness or joining accuracy.

| Source | Observed metadata | Practical implication |
|---|---|---|
| Property assessments | CSV and API-oriented resources; countywide parcels; daily data changes with monthly publication | The organizer sheet's update shorthand is not proof of daily refreshed downloads. |
| Parcel boundaries | Current WPRDC slug ends in boundaries1; polygons with county block/lot; GIS formats; WPRDC points to PASDA as most authoritative | Use a filtered extract; inspect coordinate reference system and parcel identifiers. |
| PLI permits | Pittsburgh since June 2019, historical sources linked; CSV/API; daily publication; BDA and legacy building record types | Permit classes and workflow changed; no plumbing permits in this feed. A permit is not proof of a completed housing unit. |
| Zoning | Current WPRDC slug is zoning; GIS/REST resources for city zoning districts | District polygons do not supply every applicable rule, overlay or exception. |
| HUD CHAS | Bulk downloads and API; page's latest visible release uses 2018-2022 ACS | Household needs estimates are aggregate and lagged; not parcel facts. |
| ACS 5-year | Detailed/subject/profile tables, geography examples and download/API resources; visible series through 2024 | Use correct geography/vintage and margins of error. |

The original catalog's parcel-boundary and zoning URLs did not resolve in the reader's web checks. Current landing pages below were reached. Original source files and their listed URLs remain preserved; these corrections are recorded separately.

# Citations

1. [Property assessments](https://data.wprdc.org/dataset/property-assessments)
2. [Parcel boundaries](https://data.wprdc.org/dataset/allegheny-county-parcel-boundaries1)
3. [PLI permits](https://data.wprdc.org/dataset/pli-permits)
4. [Zoning](https://data.wprdc.org/dataset/zoning)
5. [HUD CHAS](https://www.huduser.gov/portal/datasets/cp.html)
6. [ACS five-year](https://www.census.gov/data/developers/data-sets/acs-5year.html)
