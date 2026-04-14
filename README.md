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

(Filled in by Task 9 — do not edit this section manually before then.)

## Adding a dataset

1. Add the `.geojson` file under `datasets/<category>/<dataset-id>.geojson`.
2. Add a corresponding entry to `manifest.json`. See existing entries for shape.
3. Add attribution to the table in this README.
4. Open a PR.

## Repo license

The manifest, README, and repo tooling are MIT-licensed. Each dataset under
`datasets/` is licensed separately — see `manifest.json` for per-dataset licenses.
