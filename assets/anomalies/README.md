# Anomaly Asset Pipeline

Canonical repository path:

`assets/anomalies/P0XX_slug/`

- `source/` — generated/high-resolution source assets.
- `game/` — optimized runtime PNG/WebP parts used by the game.
- `archive/` — superseded or rejected versions retained for history.

## Naming

Runtime parts should follow:

`P번호_영문슬러그_파트명_상태_v01.png`

Example:

`P027_night_cleaner_broom_marks_omen_v01.png`

## Automated ingest

Run the **Ingest Anomaly Assets** workflow from GitHub Actions and provide:

- anomaly_id: e.g. `P027`
- slug: e.g. `night_cleaner`
- source_url: a directly downloadable HTTPS URL
- filename
- bucket: `source`, `game`, or `archive`

The workflow validates inputs, downloads the asset, stores it under the canonical path, and commits it to `main`.

After ingest, the corresponding Notion anomaly page should record the repository path and runtime filenames.
