# Fate Privacy Policy Page Plan

## Idea Summary
- Product: Fate / 운명 privacy policy page for app store submission.
- Goal: provide a stable public privacy policy URL for the Saju Tarot 3D Guide app.
- Core user: the app publisher entering the App Store privacy policy URL.
- Product promise: a static, readable policy page that matches the current local-first Flutter app behavior.

## MVP Scope
- Core user problem: App Store registration requires a public privacy policy URL before the app can be submitted.
- Must-have flows:
  - open the hosted privacy policy URL directly
  - identify that the policy applies to Fate / 운명
  - jump to Korean, English, German, Spanish, Chinese, Japanese, or Portuguese policy text from the same URL
  - understand local storage, optional photo/camera use, notifications, purchases, ads, sharing, and third-party processing
  - find a contact path for privacy questions
- Out-of-scope items:
  - dynamic hosting
  - custom domain setup
  - app runtime code changes
  - support page creation unless separately requested
- Success criteria:
  - repository contains `fate/private-policy.html`
  - page includes Korean, English, German, Spanish, Chinese, Japanese, and Portuguese policy sections
  - README lists the live GitHub Pages URL
  - homepage links to the Fate privacy page
  - page is readable as static HTML without JavaScript

## Feature Specification
### 1. Static privacy policy page
- Purpose: satisfy App Store privacy policy URL requirements.
- User interaction flow: open URL -> read policy sections -> use contact link if needed.
- Data/state changes: none.
- Error states: missing app identity, dead contact links, or inaccurate claims about local storage/third-party SDKs.
- Acceptance criteria:
  - page title and heading include Fate / 운명
  - final update date is visible
  - language navigation links target all supported policy sections
  - sections cover collected/processed data, local storage, permissions, third-party services, sharing, retention/deletion, children, changes, and contact

### 2. Repository navigation update
- Purpose: make the new page discoverable from repository docs and homepage.
- User interaction flow: open homepage or README -> choose Fate privacy policy.
- Data/state changes: none.
- Error states: new page exists but is hard to find.
- Acceptance criteria:
  - README includes the direct Fate URL
  - homepage includes a visible Fate privacy link

## Wireframe
```text
+--------------------------------------------------+
| Fate / 운명 개인정보처리방침                      |
| 최종 업데이트                                    |
| [KO] [EN] [DE] [ES] [ZH] [JA] [PT]              |
|--------------------------------------------------|
| Korean policy section                            |
| English policy section                           |
| German policy section                            |
| Spanish policy section                           |
| Chinese policy section                           |
| Japanese policy section                          |
| Portuguese policy section                        |
+--------------------------------------------------+
```
