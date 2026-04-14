# Public Data Sources

Curated open-source geospatial demo datasets, served via [jsDelivr](https://www.jsdelivr.com/).

Consumed by our product's onboarding flow (`upload_from_url`) to let customers
explore features with real-looking data in under a minute.

## Using a dataset

Every dataset is a single GeoJSON file. Fetch it directly:

```
https://cdn.jsdelivr.net/gh/AndreEgeli/public-data-sources@main/datasets/<category>/<dataset-id>.geojson
```

The authoritative index is `manifest.json` at the repo root:

```
https://cdn.jsdelivr.net/gh/AndreEgeli/public-data-sources@main/manifest.json
```

It lists every dataset with title, description, category, columns, feature count,
bounding box, source, and license.

## Attribution

Each dataset carries its own license, declared in `manifest.json` under
`source.license` for each entry. This table is a consolidated view.

| Dataset | ID | Source | License |
|---|---|---|---|
| World Cities (Top 200 by Population) | `world-cities-top-200` | [Natural Earth — Populated Places (10m)](https://www.naturalearthdata.com/downloads/10m-cultural-vectors/10m-populated-places/); elevation joined from [GeoNames `cities15000`](https://www.geonames.org/) | CC0-1.0 |
| Wind Turbines (Denmark) | `wind-turbines-denmark` | [Energistyrelsen — Master Data Register of Wind Turbines](https://ens.dk/en/our-services/statistics-data-key-figures-and-energy-maps/register-wind-turbines) | CC-BY-4.0 |
| Building Footprints (Central Oslo Sample) | `building-footprints-sample` | [© OpenStreetMap contributors](https://www.openstreetmap.org/copyright) | ODbL-1.0 |
| Bike Routes (Oslo) | `bike-routes-oslo` | [© OpenStreetMap contributors](https://www.openstreetmap.org/copyright) | ODbL-1.0 |
| Protected Areas (Nordic Countries) | `protected-areas-nordic` | [© OpenStreetMap contributors](https://www.openstreetmap.org/copyright) | ODbL-1.0 |
| Agricultural Field Boundaries (Synthetic) | `field-boundaries` | Synthetic — generated procedurally with a fixed seed in this repo | CC0-1.0 |
| Property Parcels (Downtown Boston) | `property-parcels` | [City of Boston — Analyze Boston (Parcels + Property Assessment FY2026)](https://data.boston.gov/dataset/parcels-2025) | Open Data Commons Public Domain (City of Boston open data terms) |

### OpenStreetMap-derived data

Three datasets (`building-footprints-sample`, `bike-routes-oslo`, `protected-areas-nordic`)
are derived from OpenStreetMap and are licensed under the Open Database License 1.0
(ODbL-1.0). Use of these datasets requires attribution:

> © OpenStreetMap contributors — https://www.openstreetmap.org/copyright

Any derivative database must also be released under ODbL-1.0.

### Synthetic data

The `field-boundaries` dataset is procedurally generated within this repo using a
fixed random seed for reproducibility. Released to the public domain under
CC0-1.0 — no attribution required, use freely.

### A note on commercial use

All seven datasets in this repo are suitable for commercial use under their
respective licenses:
- **CC0-1.0** (Natural Earth, GeoNames, synthetic fields): public domain, no restrictions.
- **CC-BY-4.0** (Energistyrelsen): commercial use permitted with attribution.
- **ODbL-1.0** (OpenStreetMap): commercial use permitted with attribution and share-alike for derivative databases.
- **City of Boston open data terms**: explicitly permits commercial use.

WDPA (World Database on Protected Areas) was evaluated and rejected as a source
because its terms restrict commercial use without an IBAT subscription — OpenStreetMap
was used instead for `protected-areas-nordic`.

## Adding a dataset

1. Add the `.geojson` file under `datasets/<category>/<dataset-id>.geojson`.
2. Add a corresponding entry to `manifest.json`. See existing entries for shape.
3. Add attribution to the table in this README.
4. Open a PR.

## Repo license

The manifest, README, and repo tooling are MIT-licensed. Each dataset under
`datasets/` is licensed separately — see `manifest.json` for per-dataset licenses.
