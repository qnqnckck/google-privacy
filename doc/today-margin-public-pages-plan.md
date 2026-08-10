# Today Margin public pages plan

## Idea summary

Publish a small, static public home, support page, and bilingual privacy policy for Today Margin (오늘남김) so users and app-store reviewers can understand the product and contact the developer.

## MVP scope

- Core problem: Today Margin needs stable public URLs for Google Play and AdMob compliance.
- Must-have flows: open app page, open support, open privacy policy, contact the developer, return to the app list.
- Out of scope: accounts, analytics, forms, dynamic services, and downloads.
- Success criteria: all pages load over HTTPS, work on mobile, describe the verified app behavior, and expose working cross-links.

## Feature specification

### App page
- Purpose: explain the daily profit ledger and its local-first model.
- Flow: visitor reads product summary and follows support or privacy links.
- State changes: none.
- Error states: links remain plain relative URLs with no script dependency.
- Acceptance: app name, features, free/Pro model, support, and privacy links are visible.

### Support page
- Purpose: provide troubleshooting and a public contact route.
- Flow: visitor reads help topics or opens an email/GitHub issue.
- State changes: none.
- Error states: email and issue links remain usable without JavaScript.
- Acceptance: data deletion, purchase restoration, ads/privacy options, and CSV export are covered.

### Privacy policy
- Purpose: disclose local storage, AdMob, UMP consent, purchases, and CSV sharing.
- Flow: visitor switches between Korean and English or reads the system-language default.
- State changes: optional language preference stored in localStorage.
- Error states: Korean content is visible by default if JavaScript is unavailable.
- Acceptance: effective date, processed data, third parties, retention/deletion, children, changes, and contact are present.

## Wireframe

```text
[Today Margin mark]  [Apps] [Support] [Privacy]

[TODAY'S CLOSE / hero]
Daily sales - costs = margin
[Support] [Privacy policy]

[Sales] -> [Costs] -> [Close]
[Local-first] [Free + ads] [Pro without ads]

[Footer / contact]
```

