# Janhyangguk asset layout

`assets/` is the single canonical root for runtime/game assets.

## Canonical folders

- `assets/employees/<employee>/<state>/` — employee SD, portraits and expressions
- `assets/anomalies/<anomaly>/<state>/` — anomaly art, SD, layers and manifests
- `assets/cutscenes/<cut>/` — opening/cutscene assets
- `assets/ui/<group>/` — UI artwork and interface assets
- `assets/inbox/` — temporary landing zone for assets that have not been classified yet

## Shared routing contract

`assets/asset-routing.json` is the source of truth for both the browser uploader and GPT-assisted uploads.

The browser uploader resolves the destination from this file. GPT should read the same file before uploading and use the same destination rules.

Do not create new runtime asset roots under repository root, `resources/`, or `dist/assets/`. If an asset cannot be classified yet, upload it to `assets/inbox/` and move it later.
