# 세 번째 벨 · 2D Art Asset Package

잔향국 모바일 관리 게임용 분리형 2D 아트 자산입니다.

## 규격
- 기준 캔버스: 1024×1536
- 모든 레이어는 동일 캔버스/좌표계를 유지
- room_base만 불투명 배경
- 나머지 파츠는 투명 알파 레이어
- 웹 프로토타입용 WebP

## 에셋
- room_base.webp
- phone_body.webp
- receiver.webp
- cord_normal.webp
- cord_tension.webp
- indicator_light.webp
- vibration_fx.webp
- shadow_normal.webp
- shadow_long.webp

## 조합
`asset-manifest.json`의 `states`를 기준으로 조립합니다.

레이어는 동일한 1024×1536 컨테이너에 absolute/inset:0으로 겹치며, 상태 변화는 translate/rotate/opacity/scale/brightness와 레이어 교체만으로 구현합니다.

수화기를 들어 올리거나 전화를 받는 상호작용은 사용하지 않습니다.
