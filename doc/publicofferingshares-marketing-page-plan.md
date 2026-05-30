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
