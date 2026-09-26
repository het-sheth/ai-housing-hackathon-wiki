> Review limitation: This is a bounded agent audit, not a production specification. Its point query does not validate whole-parcel zoning or hazards. Use full parcel geometry for the intended screen; never treat this commercial test record as a housing candidate.

# Pittsburgh infill data audit, 2026-09-26

Purpose: minimum public data for a weekend, single-site, small residential infill screen. This is a preliminary evidence screen, not a zoning determination, title search, engineering review, flood determination, or a statement about site availability.

## What was actually fetched and tested

| Test | Result | Evidence |
| --- | --- | --- |
| Assessment schema | Fetched from WPRDC CKAN datastore | `property_assessments_table`, one row requested |
| Parcel geometry schema | Fetched from WPRDC CKAN datastore | resource `858bbc0f-b949-4e22-b4bb-1a78fef24afc`, one row requested |
| Zoning schema | Fetched from City ArcGIS REST | `Zoning/MapServer/0?f=pjson` |
| Minimal join | Succeeded for one Pittsburgh parcel, using no owner/contact fields | `PARID = pin`, parcel WKT point queried against City zoning |
| Current PASDA parcel REST resource advertised by WPRDC | Failed | `pasda/AlleghenyCounty/MapServer/25` returned HTTP 500, “Service ... not started” |

### Sanitized one-parcel join evidence

This is a reproducible data-path demonstration, not a recommended or available site.

| Input/output | Value |
| --- | --- |
| Assessment `PARID` | `0001D00128000000` |
| Assessment city | `PITTSBURGH` |
| Assessment fields used | `CLASS=C`, `USEDESC=SMALL DETACHED RET(UNDER 10000)`, `LOTAREA=2400`, `YEARBLT=null`, `FAIRMARKETTOTAL=463300`, `ASOFDATE=2026-09-01` |
| Boundary lookup | `pin=0001D00128000000`, `map_block_lot=1-D-128`, `municode=101`, `calc_acreage=0.05` |
| Spatial method | A point inside the boundary WKT, EPSG:2272, was sent to the City zoning `intersects` endpoint. Production should use `ST_PointOnSurface` or area-overlap handling, not a hand-picked centroid. |
| Zoning result | `zon_new=GT-A`; `full_zoning_type=GOLDEN TRIANGLE DISTRICT A`; `status=Approved` |

The test establishes that current assessment `PARID` and parcel-boundary `pin` can match directly, including leading zeroes. It does not establish a universal one-to-one relationship. Preserve both as text, validate duplicates, and retain `map_block_lot` only as a readable derivative.

## Minimum source register

| Use | Steward | Current endpoint and small-request pattern | Key fields, format, null/format risks | Coverage and cadence | License / terms status |
| --- | --- | --- | --- | --- | --- |
| Assessment facts and parcel key | Allegheny County Office of Property Assessments, published by WPRDC | Dataset metadata: `https://data.wprdc.org/api/3/action/package_show?id=property-assessments`. Datastore: `https://data.wprdc.org/api/3/action/datastore_search?resource_id=property_assessments_table&limit=1&filters={"PROPERTYCITY":"PITTSBURGH"}`. Download exists at `https://data.wprdc.org/dataset/2b3df818-601e-4f06-b150-643557229491/resource/9a1c60bd-f9f7-4aba-aeb7-af8c3aaa44e5/download/assessments.csv`. | `PARID` text, `PROPERTYCITY`, `MUNIDESC`, `CLASS`, `USEDESC`, `LOTAREA` float, `YEARBLT` float and nullable, values, `ASOFDATE` date. Do not retrieve or expose `OWNERDESC` or change-notice fields. Municipality description is not exactly `PITTSBURGH`, use `PROPERTYCITY` to filter. | Countywide. WPRDC metadata modified 2026-09-07; listed download last modified 2026-09-07. The organizer catalog says daily/periodic, so capture `ASOFDATE` and retrieval time. | CKAN metadata: Creative Commons CCZero. WPRDC access is subject to portal terms. Assessment value is not market value. |
| Parcel polygon | Allegheny County GIS, published by WPRDC | Dataset metadata: `https://data.wprdc.org/api/3/action/package_show?id=allegheny-county-parcel-boundaries1`. Small datastore request: `https://data.wprdc.org/api/3/action/datastore_search?resource_id=858bbc0f-b949-4e22-b4bb-1a78fef24afc&limit=1&filters={"pin":"0001D00128000000"}`. WPRDC GeoJSON release: `https://data.wprdc.org/dataset/709e4e52-6f82-4cd0-a848-f3e2b3f5d22b/resource/3f50d47a-ab54-4da2-9f03-8519006e9fc9/download/alleghenycounty_parcels202609.geojson`. | `pin` text, `map_block_lot` text, `municode` text, `calc_acreage` text, `wkt` text. Geometry is Pennsylvania State Plane South, EPSG:2272, US survey feet. Do not coerce ID strings to numbers. Blank `comments`, `notes`, `pseudono` occur. | Countywide. GeoJSON last modified 2026-09-22; WPRDC says changes as needed and publishing monthly. The advertised PASDA REST endpoint was down during this audit, so use the WPRDC datastore only for small requests and retain a degraded-source state. | CKAN metadata: License not specified. It is public access, but do not call it public domain or CC0. WPRDC terms apply. |
| Base zoning | City of Pittsburgh | Layer metadata: `https://pghbridgis.pittsburghpa.gov/federated/rest/services/Zoning/MapServer/0?f=pjson`. Point query: `https://pghbridgis.pittsburghpa.gov/federated/rest/services/Zoning/MapServer/0/query` with `f=json`, `geometryType=esriGeometryPoint`, `inSR=2272`, `spatialRel=esriSpatialRelIntersects`, `outFields=OBJECTID,zon_new,full_zoning_type,status`, `returnGeometry=false`. | `zon_new` is the base-code field, not `zoning_code`; `full_zoning_type`, `status`, `OBJECTID`. Service geometry source is EPSG:2272. Use boundary-aware logic because a point can lie on a zoning boundary. | Citywide. Metadata exposes edit fields, but this audit did not establish a published cadence or a binding effective-date history. Save service response retrieval time and `status`. | Public City service. No license was verified in this audit. Read the current zoning code and obtain City interpretation before stating permitted use, density, overlays, or variance need. |
| Permit history, optional red flag | City of Pittsburgh PLI, published by WPRDC | Metadata: `https://data.wprdc.org/api/3/action/package_show?id=pli-permits`. CSV: `https://data.wprdc.org/datastore/dump/f4d1177a-f597-4c32-8cbf-7885f56253f6`. Datastore resource ID: `f4d1177a-f597-4c32-8cbf-7885f56253f6`. | `permit_id` text is the unique ID documented as `ext_file_num` in dataset notes, `permit_type`, `work_type`, `commercial_or_residential`, `issue_date`, `parcel_num`, `address`, coordinates, status. Text was converted to uppercase. `parcel_num` needs a real match-rate test against `PARID`, not an assumption. Exclude `owner_name` and `contractor_name`. | Pittsburgh. Dataset description says 2019-06-01 to present; portal listed 2019-06-03 through 2026-09-21 and daily change/publishing. BDA went live June 2024, so include both `BUILDING` and `Building & Development Application` category logic. | CKAN metadata: Creative Commons Attribution. WPRDC terms apply. No permit record is an unknown, not evidence that a permit, approval, or constraint does not exist. |

## Reproducible join recipe

1. Accept an address or parcel ID. Resolve only the ID required for the screen. Keep raw and normalized values separately.
2. Fetch a minimal assessment record by exact text `PARID`; select only `PARID`, location/jurisdiction, class/use, lot area, build year, values, and `ASOFDATE`.
3. Fetch a minimal parcel record by exact text `pin = PARID`; require a non-empty WKT polygon and Pittsburgh municipality validation before proceeding.
4. Parse WKT as EPSG:2272. Calculate a guaranteed interior point. Query City zoning with that point and `esriSpatialRelIntersects`. If zero or multiple zones return, mark `ZONING_BOUNDARY_OR_MISSING`, retain all returned values, and do not infer a single district.
5. Label every absence as `UNKNOWN` or `SOURCE_UNAVAILABLE`. Never score it as clear. Store dataset endpoint, layer ID/resource ID, data `ASOFDATE` where supplied, retrieval timestamp, input key, and service response status.

Illustrative shell requests, with the parcel ID substituted by the application and URL encoding performed by its HTTP client:

```sh
curl -fsSLG 'https://data.wprdc.org/api/3/action/datastore_search' \
  --data-urlencode 'resource_id=property_assessments_table' \
  --data-urlencode 'limit=1' \
  --data-urlencode 'filters={"PARID":"0001D00128000000"}'

curl -fsSLG 'https://data.wprdc.org/api/3/action/datastore_search' \
  --data-urlencode 'resource_id=858bbc0f-b949-4e22-b4bb-1a78fef24afc' \
  --data-urlencode 'limit=1' \
  --data-urlencode 'filters={"pin":"0001D00128000000"}'

curl -fsSLG 'https://pghbridgis.pittsburghpa.gov/federated/rest/services/Zoning/MapServer/0/query' \
  --data-urlencode 'f=json' \
  --data-urlencode 'where=1=1' \
  --data-urlencode 'geometry=1341453,411575' \
  --data-urlencode 'geometryType=esriGeometryPoint' \
  --data-urlencode 'inSR=2272' \
  --data-urlencode 'spatialRel=esriSpatialRelIntersects' \
  --data-urlencode 'outFields=OBJECTID,zon_new,full_zoning_type,status' \
  --data-urlencode 'returnGeometry=false'
```

The coordinate in the third command is only the audit's sanitized test point. It must be computed from the parcel polygon for any new parcel.

## Constraint layers for the next increment

| Constraint | Feasible source | MVP treatment |
| --- | --- | --- |
| Flood | FEMA National Flood Hazard Layer, `https://www.fema.gov/flood-maps/national-flood-hazard-layer` | Use an authoritative FEMA spatial layer and record panel/effective date. Flag intersection as a screening item, not a flood determination. |
| Steep slope | WPRDC dataset `https://data.wprdc.org/dataset/25-or-greater-slope` | Spatially intersect with parcel geometry. The layer is a >=25% derived screen. Do not infer slope from zoning code alone. Survey and geotechnical review remain required. |
| Historic | City historic-preservation or designated-district geographic layer must be confirmed with the City | Treat as `UNKNOWN` until an authoritative polygon/version is selected. Do not use an absence in permit history or a neighborhood name as proof that review does not apply. |
| Mine influence | WPRDC `https://data.wprdc.org/dataset/undermined-areas` | Optional screen. Flag intersection and require engineering follow-up; historic mine maps can be incomplete. |

## Corrections to the downloaded deep research report

1. It says parcel geometry and zoning were not fetched, then calls their join verified. The audit fetched schemas and completed exactly one real `PARID -> pin -> zoning` test. The right status is “demonstrated once, no coverage or match-rate validation.”
2. It calls the parcel license “public domain likely.” Current WPRDC metadata says “License not specified.” That is not a license grant.
3. It presents a generic `zoning_code` field and says a centroid join is the intended method. The actual City layer's code field is `zon_new`; a production join needs an interior point or polygon-overlap policy and an explicit boundary/multiple-zone result.
4. It says joins require parsing block and lot. The tested record directly matched `assessment.PARID == parcel.pin`. Keep identifiers as fixed-width text, then validate duplicate and unmatched rates before adding a parser fallback.
5. It says prior variances are not public and proposes assuming none. Lack of a result must remain `UNKNOWN`; it cannot support “no variance” or “no constraint.” PLI's live schema also uses `parcel_num`, which needs a separate empirical match-rate test.

## One data-authority question for a Pittsburgh zoning SME

For a preliminary automated screen, which City-maintained layer or decision record, with what effective-date/version rule, is authoritative for base zoning plus historic, hillside, and other overlay applicability, and should the product treat any unavailable or conflicting layer as an automatic “manual City confirmation required” outcome?

## Current blockers and safe demo boundary

1. The advertised PASDA parcel REST service returned a live HTTP 500. The WPRDC datastore supports tiny parcel retrievals, but the team should display a source-unavailable state and should not plan a bulk download.
2. No actual permit-to-parcel match-rate was tested. Keep permits out of a positive/negative feasibility score until `parcel_num` normalization is measured.
3. Base zoning is a fact from the map service. Allowed use, dimensional compliance, overlay review, and variance need require current code and City interpretation.
