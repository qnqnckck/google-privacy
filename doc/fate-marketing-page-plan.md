# Fate Marketing Page Plan

## Idea Summary

`fate/index.html`에 사주 앱 `운명/Fate`의 App Store Marketing URL로 사용할 정적 마케팅 페이지를 추가한다.

## MVP Scope

### Core User Problem

스토어 심사와 사용자가 확인할 수 있는 공개 앱 소개 페이지가 필요하다.

### Must-Have Flows

- 앱의 핵심 기능인 사주, 타로, 손금, 궁합, 오늘 운세, 별자리, 주역, 전생, 팬심, 홈 위젯을 소개한다.
- 기존 `fate/private-policy.html`과 `fate/support.html`로 연결한다.
- 운세 결과를 보장하거나 확정적으로 예측하는 표현을 피한다.
- 로컬 우선, 기기 중심 저장, 선택적 사진 기능을 명확히 안내한다.

### Out-of-Scope Items

- 앱 바이너리 수정
- 스토어 설정 변경
- 외부 분석/광고 스크립트 추가
- 서버 기반 기능 추가

### Success Criteria

- `fate/index.html`이 정적 HTML로 렌더링된다.
- 앱 아이콘 이미지가 `fate/assets/app-icon.png`로 표시된다.
- 실제 스토어 스크린샷이 `fate/assets/store-1.png`부터 `fate/assets/store-7.png`까지 표시된다.
- 언어 전환 UI가 앱 지원 언어인 한국어, 영어, 일본어, 중국어, 스페인어, 프랑스어, 독일어, 포르투갈어를 제공한다.
- 개인정보처리방침, 지원, 이메일 링크가 정상 연결된다.

## Feature Specification

### Marketing Landing Page

- Purpose: 앱의 운세 리딩 기능과 로컬 중심 개인정보 방향을 공개 페이지로 소개한다.
- User Interaction Flow: 사용자는 스토어의 Marketing URL에서 앱 소개, 주요 기능, 로컬 저장 안내, 정책/지원 링크를 확인한다.
- Data/State Changes: 정적 HTML, 앱 아이콘, 실제 스토어 스크린샷 자산, 클라이언트 측 언어 전환 스크립트가 추가된다.
- Error States: 링크 경로가 깨지면 스토어 사용자와 심사자가 정책/지원 페이지에 접근할 수 없다.
- Acceptance Criteria: 상대 링크와 이미지가 모두 존재하고 HTML 파싱 오류가 없다.

## Wireframe

```text
[Desktop Aside]
  App icon
  운명 / Fate headline
  [Support] [Privacy]
  Local-first note

[Mobile App-Like Page]
  Sticky header
  Hero gold fortune card
  Quick links
  Actual app screenshots
  Language switcher
  Reading modes
  Local-first notice
  Policy/support links

[Desktop QR]
  Marketing URL QR
  URL label
```

## Visual Direction

- Product metaphor: 작은 금박 운세 카드 folio.
- Structure: 점신 참고처럼 데스크톱은 좌측 브랜드 메시지, 우측은 모바일 앱 화면 프레임으로 구성한다.
- Palette: 앱 토큰의 warm paper background, oracle night, oracle gold를 중심으로 사용한다.
- Primitives: fortune card, seal badge, reading mode tile, saved reading strip, policy link row.
- App proof: `resource/fate/store-assets/ko/android_screeshot`의 현재 스토어 스크린샷 7개를 기준으로 배치한다.
- Language: 앱 README의 지원 로케일(`ko`, `en`, `ja`, `zh-CN`, `es`, `fr`, `de`, `pt`)에 맞춰 마케팅 페이지 주요 문구도 전환한다.
- Marketing URL QR: 스토어 ID가 확정되지 않은 상태에서는 QR을 마케팅 페이지 자체로 연결한다.
- Risk: 실제 점술 정확도나 미래 보장을 암시하지 않고, 사용자가 리딩을 탐색/기록하는 앱으로 표현한다.
