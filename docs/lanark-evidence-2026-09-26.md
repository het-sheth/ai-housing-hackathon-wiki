# 1623 Lanark Street, Pittsburgh, manual evidence screen

Retrieved 2026-09-26. This is a narrow, reproducible public-data example for a known rehabilitation case. It does not establish availability, ownership, title, buildability, legal entitlement, financial feasibility, or an approval decision.

## Chosen parcel and source conflict

The exact assessment-address match is **1623 LANARK ST, PITTSBURGH, PA 15214**, parcel ID **`0023C00208000000`**. The assessment address had a blank `PROPERTYFRACTION`, so no suffix ambiguity was returned. Its matching boundary row has the same `pin`, `map_block_lot=23-C-208`, and a full polygon. The PLI records also use the same `parcel_num` and address string `1623 LANARK ST, Pittsburgh, PA 15214-`.

| Source | Current record | What it supports | What it does not support |
| --- | --- | --- | --- |
| Allegheny assessment, WPRDC datastore | `CLASS=R`, `CLASSDESC=RESIDENTIAL`, `USEDESC=VACANT LAND`, `LOTAREA=1657`, `YEARBLT=1900`, `FAIRMARKETTOTAL=136600`, `ASOFDATE=2026-09-01` | The current assessment record and its vintage | Present physical condition, sale price, availability, or development feasibility |
| PLI permits, WPRDC datastore | Six completed records attached to the exact parcel, including `BP-2023-19723`, issued 2024-01-29, `total_project_value=300000`, for alterations to an existing single-family dwelling; and `EP-2026-05647`, issued 2026-08-28, for a solar installation | Recorded permit history and the permit's declared project value | Actual completed cost, final physical condition, code compliance, or a current occupancy/legal-use determination |

The assessment use (`VACANT LAND`) conflicts with completed PLI records describing an existing single-family dwelling and later solar work. This screen preserves the conflict. It must be reported as **current-condition and assessment-classification review required**, not resolved in favor of either source.

## Parcel and whole-polygon zoning evidence

| Check | Result | Method and boundary treatment |
| --- | --- | --- |
| Parcel geometry | `pin=0023C00208000000`; 0.04 calculated acres; WKT polygon | WPRDC parcel datastore. CRS is Pennsylvania State Plane South, EPSG:2272, US survey feet. |
| Base zoning intersects parcel | One City feature: `R1D-H`, `SINGLE-UNIT DETACHED RESIDENTIAL HIGH DENSITY`, `status=Approved`, `OBJECTID=634` | The complete parcel polygon, not a point, was submitted with `esriSpatialRelIntersects`. |
| Boundary/sliver test | No parcel-boundary to zone-boundary intersections; all five unique parcel vertices were inside the returned zone ring | The returned zoning geometry was checked locally in EPSG:2272. This supports full geometric coverage of this simple parcel by that one feature. It is not a legal zoning determination. |

The City source is `https://pghbridgis.pittsburghpa.gov/federated/rest/services/Zoning/MapServer/0`. The service metadata did not establish an effective-date history or a verified open-data license in this screen. The zoning map result must not be translated into a permitted-use, density, dimensional-compliance, overlay, or variance conclusion without the current zoning code and City interpretation.

## Slope and remaining constraints

| Constraint | Result | Required interpretation |
| --- | --- | --- |
| City 25% or greater slope | The complete parcel polygon intersected one City slope feature where `slope25=Yes` | This is an intersection flag only. Overlap area/percentage was not calculated, and a derived slope layer is not a survey or geotechnical conclusion. |
| Flood | `UNKNOWN, not retrieved in this bounded screen` | Use an authoritative FEMA NFHL spatial intersection with panel/effective date before asserting a flood condition. |
| Historic | `UNKNOWN, no authoritative City district polygon/version was verified` | Do not infer historic review from neighborhood, permit history, or a missing result. Confirm with the City historic-preservation authority. |
| Utilities/infrastructure capacity | `UNKNOWN` | Manual PWSA/utility confirmation required. |

The slope source is `https://services1.arcgis.com/YZCmUqbcsUpOKfj7/arcgis/rest/services/PGHWebSlope25/FeatureServer/0`; WPRDC dataset metadata for `25-or-greater-slope` was modified 2026-09-23 and lists its license as unspecified. The source intersects are public screening data, not a certification.

## PLI evidence, sanitized

| Permit ID | Type | Issue date | Declared `total_project_value` | Status |
| --- | --- | --- | ---: | --- |
| `DP-2021-06343` | Demolition Permit, partial demolition | 2021-04-26 | $14,000 | Completed |
| `BP-2021-06707` | Building, exterior alteration | 2021-04-26 | $5,000 | Completed |
| `BP-2023-19723` | Building, addition/alteration | 2024-01-29 | $300,000 | Completed |
| `MP-2024-02581` | Mechanical, addition/alteration | 2024-02-20 | $1,000 | Completed |
| `EP-2024-05671` | Electrical, addition/alteration | 2024-04-15 | $1,000 | Completed |
| `EP-2026-05647` | Electrical, addition/alteration | 2026-08-28 | $6,100 | Completed |

PLI uses a Creative Commons Attribution license in its WPRDC metadata, is published daily, and covers current records from 2019. The relevant record fields are shown in the sanitized response. The output retains no owner or contractor data.

## Reproducibility and source files

All response files and request scope are under `docs/evidence/lanark-2026-09-26/`.

| File | Contents |
| --- | --- |
| `manifest.json` | Source endpoints, resource IDs, filters, requested field whitelists, and privacy scope |
| `assessment-1623.json` | Exact non-owner assessment address lookup |
| `parcel.json` | Exact boundary lookup with full WKT polygon |
| `zoning-intersects.json` | Full-polygon zoning intersection result |
| `zoning-feature-634.json` | Returned zoning feature geometry for boundary check |
| `zoning-overlap-check.json` | Local whole-polygon vertex and edge result |
| `slope-package.json`, `slope-layer.json`, `slope-intersects.json` | Slope metadata and full-polygon intersection result |
| `pli-by-parcel.json` | Exact parcel permit lookup with non-person fields only |

The property-assessment metadata endpoint is `https://data.wprdc.org/api/3/action/package_show?id=property-assessments`. It states CC0. The parcel-boundary metadata endpoint is `https://data.wprdc.org/api/3/action/package_show?id=allegheny-county-parcel-boundaries1`; it lists no license and says changes are as needed with monthly publishing. WPRDC portal terms apply to both.

## Suitable short-form display

**Verified data:** parcel key and polygon matched, base zoning mapped to `R1D-H`, the polygon is geometrically inside the returned zoning feature, the parcel intersects City 25% slope data, and permit history is present.

**Review required:** assessment says vacant land while completed permits document rehabilitation activity; slope intersection lacks an area percentage; zoning code and City confirmation are required for any use or variance conclusion.

**Unknown:** flood, historic review, utility capacity, title, site availability, survey/geotechnical conditions, and all financial feasibility conclusions.

## Reproduction limitations and failed lookups

The manifest records the retrieval date, source endpoints, field selections and query scope. It does not preserve exact request times or complete encoded ArcGIS request URLs. Reconstruct the polygon from `parcel.json`, set `geometryType=esriGeometryPolygon`, `inSR=2272`, `spatialRel=esriSpatialRelIntersects`, and request the listed fields. For the zoning feature request use `where=OBJECTID=634`, `returnGeometry=true`, and `outSR=2272`. Use `f=json` for ArcGIS and the listed resource IDs, filters and fields for CKAN. Response SHA-256 values are in `sha256.json`. This is reproducible query scope, not a complete network transaction archive.

An address-based PLI query returned zero while the exact parcel lookup returned six records. No address-only negative conclusion is safe. An initial ArcGIS contains query also returned no feature; containment query direction was not established, so that result was not interpreted as a boundary crossing. Full zoning geometry was fetched and locally tested using point-in-polygon and edge intersections instead. This bounded simple-polygon test is not a production GIS validation suite.

License metadata: assessment CC0; PLI Creative Commons Attribution; parcel and slope unspecified; zoning reuse license unverified. Public access alone does not establish unrestricted redistribution. Resolve terms before publishing a bundled application dataset. These local sanitized snapshots are research evidence. No ownership or contact fields were requested.
