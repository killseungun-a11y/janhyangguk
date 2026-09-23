# Janhyangguk asset layout

`assets/` is the single canonical root for runtime/game assets.

## Canonical folders

- `assets/employees/<employee>/<state>/` — employee SD animation assets (`idle`, `walk`, `work`)
- `assets/anomalies/<anomaly>/codex/` — anomaly codex illustration
- `assets/anomalies/<anomaly>/work/` — anomaly work-room 2D (`normal`, `omen`, `unstable`, `meltdown`/`recovery` when needed)
- `assets/cutscenes/` — opening/cutscene illustrations
- `assets/ui/<group>/` — UI artwork and interface assets
- `assets/inbox/` — temporary landing zone for assets that have not been classified yet

## Shared routing contract

`assets/asset-routing.json` is the source of truth for both the browser uploader and GPT-assisted uploads.

The browser uploader resolves the destination from this file. GPT should read the same file before uploading and use the same destination rules.

Do not create new runtime asset roots under repository root, `resources/`, or `dist/assets/`. If an asset cannot be classified yet, upload it to `assets/inbox/` and move it later.

## Temporary visual fallback

Until dedicated `one-stroke` work-room 2D variants are produced, the management prototype may reuse the approved CUT03 artwork in the expected `assets/anomalies/one-stroke/work/` state paths so the live management screen does not fall back to CSS-only placeholders. Replace these aliases with dedicated work-room images as soon as they are available.
