# PublicOfferingShares Marketing Page Plan

## Idea Summary

공모주비서 iOS App Store Marketing URL로 사용할 수 있는 정적 마케팅 페이지를 `google-privacy` GitHub Pages 사이트에 추가한다.

## MVP Scope

### Core User Problem

App Store Connect의 Marketing URL과 AdMob app-ads.txt 검증에 사용할 공개 앱 소개 페이지가 필요하다.

### Must-Have Flows

- `publicofferingshares/index.html`에 앱 소개 랜딩 페이지를 만든다.
- 개인정보처리방침과 지원 페이지로 연결한다.
- 공모주 일정, 청약 기록, 알림, 공유 이미지 등 실제 앱 기능만 설명한다.
- AdMob 안내에 맞춘 `app-ads.txt` 파일을 이 repo에서 가능한 위치에 추가한다.

### Out-of-Scope Items

- 앱 바이너리 수정
- App Store Connect 직접 설정 변경
- 커스텀 도메인 설정
- 광고 계정 설정 자동화

### Success Criteria

- 정적 HTML로 바로 열리는 마케팅 페이지가 존재한다.
- App Store Marketing URL로 `https://qnqnckck.github.io/google-privacy/publicofferingshares/`를 사용할 수 있다.
- `app-ads.txt` 내용은 AdMob 안내 스니펫과 일치한다.
- 기존 개인정보/지원 페이지 링크가 유지된다.

## Feature Specification

### Marketing Landing Page

- Purpose: 앱의 핵심 가치와 기능을 App Store 사용자와 AdMob crawler가 볼 수 있는 공개 페이지로 제공한다.
- User Interaction Flow: 사용자가 App Store의 Developer Website/Marketing URL을 누르면 앱 소개, 주요 기능, 개인정보/지원 링크를 확인한다.
- Data/State Changes: 정적 HTML 파일만 추가된다.
- Error States: 페이지 URL이 App Store Marketing URL과 불일치하면 AdMob crawler가 다른 도메인을 확인할 수 있다.
- Acceptance Criteria: 브라우저에서 `publicofferingshares/index.html`이 정상 렌더링된다.

### App-ads.txt

- Purpose: AdMob publisher ID가 포함된 authorized seller 정보를 공개한다.
- User Interaction Flow: AdMob crawler가 store listing의 developer website hostname에서 `app-ads.txt`를 조회한다.
- Data/State Changes: `app-ads.txt` 파일을 추가한다.
- Error States: GitHub Pages project path에만 파일이 있으면 `https://qnqnckck.github.io/app-ads.txt` 루트 검증에는 충분하지 않을 수 있다.
- Acceptance Criteria: 파일 내용이 `google.com, pub-4069445075453135, DIRECT, f08c47fec0942fa0`와 정확히 일치한다.

### Store Download Router

- Purpose: 하나의 QR 링크에서 Android 사용자는 Google Play로, iOS 사용자는 App Store로 이동하게 한다.
- User Interaction Flow: 사용자가 QR을 스캔하면 `publicofferingshares/download.html`에 도착하고, 기기 종류에 따라 스토어로 자동 이동한다.
- Data/State Changes: 정적 HTML 라우터 파일만 추가된다.
- Error States: 스토어 URL이 변경되면 `download.html`의 iOS/Android 상수와 마케팅 페이지 버튼 링크를 함께 갱신해야 한다.
- Acceptance Criteria: QR 링크, App Store 버튼, Google Play 버튼, 수동 fallback 링크가 모두 존재한다.
- Placement: 데스크톱에서는 점신 참고처럼 설명 영역, 480px 앱 화면, QR 다운로드 영역을 3컬럼 비율로 배치한다.

## Wireframe

```text
[Hero: 공모주비서]
  앱 아이콘 / 캘린더형 비주얼
  일정, 분석, 기록을 한 곳에서
  [개인정보처리방침] [지원 페이지]

[Feature Grid]
  일정 캘린더 | 청약 판단 | 포트폴리오 | 알림/위젯

[Local-first Notice]
  기록은 기기 중심, 필요한 공개 데이터만 확인

[Store/Legal Links]
  Privacy Policy | Support | Contact
```

## Visual Direction Update

- Product metaphor: 공모주 청약을 챙겨주는 "작은 비서의 데스크 보드"로 잡는다.
- Structure: 첫 화면은 마케팅 문구보다 앱명, 일정표, 오늘의 체크리스트, 청약 진행 상태가 먼저 보이게 한다.
- Information hierarchy: 큰 앱명과 한 줄 가치 제안을 최상단에 두고, 실제 기능은 캘린더/체크리스트/기록 흐름으로 나눈다.
- Material direction: 노란 앱 아이콘 색상은 포인트로만 사용하고, 배경은 밝은 종이색과 짙은 잉크색을 섞어 금융 앱처럼 안정적으로 보이게 한다.
- Reusable UI primitives: memo chip, calendar tile, status rail, assistant note, compact feature panel.
- Risk: 투자 성과를 보장하는 표현은 피하고, 일정 관리와 기록 보조 도구임을 명확히 유지한다.

## Visual Direction Update 2

- Reference adjustment: 점신형 "왼쪽 브랜드 메시지 + 오른쪽 모바일 앱 화면"을 그대로 좁은 480px 프레임에 가두지 않고, 데스크톱에서는 1360px 폭을 적극 활용한다.
- Structure: 좌측에는 앱 가치와 CTA, 우측에는 실제 앱 코드의 주요 화면 축을 반영한 4개 스크린 월을 배치한다.
- App-code mapping: `공모주 대시보드`, `공모주 일정`, `청약 리포트`, `포트폴리오/알림` 화면을 정적 mock screenshot으로 표현한다.
- Reusable UI primitives: phone frame, dashboard list item, calendar day/event pill, report metric bar, portfolio chart, notification toggle.
- Risk: 실제 캡처 이미지는 아니므로, "앱 화면 예시"로만 표현하고 앱에 없는 기능을 추가로 암시하지 않는다.
