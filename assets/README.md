# Janhyangguk asset layout

`assets/` is the single canonical root for runtime/game assets.

## Canonical folders

- `assets/employees/<employee>/idle/` — employee SD idle animation frames
- `assets/employees/<employee>/walk/` — employee SD walk animation frames
- `assets/employees/<employee>/work/` — employee SD work animation frames
- `assets/anomalies/<anomaly>/codex/` — 잔향 도감용 일러스트
- `assets/anomalies/<anomaly>/work/` — 잔향 작업용 2D (`normal / omen / unstable / meltdown` 등 실제 필요한 상태)
- `assets/cutscenes/<cut>/` — 컷씬 일러스트
- `assets/illustrations/events/` — 이벤트 일러스트
- `assets/ui/<group>/` — UI artwork and interface assets
- `assets/inbox/` — temporary landing zone for assets that have not been classified yet

## Shared routing contract

`assets/asset-routing.json` is the source of truth for both the browser uploader and GPT-assisted uploads.

The browser uploader resolves the destination from this file. GPT should read the same file before uploading and use the same destination rules.

For game art, use the current production standard in `docs/ART_PRODUCTION_STANDARD.md`.

Do not create new runtime asset roots under repository root, `resources/`, or `dist/assets/`. If an asset cannot be classified yet, upload it to `assets/inbox/` and move it later.
