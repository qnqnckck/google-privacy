# Bible Public Pages Plan

## Idea Summary
Add a public marketing page and support page for the Bible app, and refresh the existing privacy pages so store review and public users have stable, product-aligned URLs.

## MVP Scope
### Core User Problem
The app already has privacy policy pages, but it needs a polished app introduction page and a support URL that explain the current `성경 / Bible` app surfaces.

### Must-Have Flows
- Users can open the Bible introduction page and understand the four-tab app: Listen, Read, Study, Settings.
- Users can open support instructions and contact the developer.
- Users can open Korean and English privacy policies.
- Pages work as static GitHub Pages content.

### Out Of Scope
- App code changes.
- Store download deep links before final store URLs are provided.
- New screenshot generation.

### Success Criteria
- `bible/index.html` exists and uses current app screenshots.
- `bible/support.html` exists.
- `bible/private-policy.html` and `bible/private-policy-en.html` are aligned with current app behavior.
- Root `index.html` links to Bible pages.
- Static HTML parsing and link checks pass.

## Feature Specification
### Marketing Page
- Purpose: introduce the Bible app as a multilingual Bible reading, listening, study, prayer, and widget app.
- User interaction flow: open page, scan hero, view real app screenshots, open support/privacy pages.
- Data/state changes: none.
- Error states: page must still work if external network is unavailable.
- Acceptance criteria: all referenced assets resolve locally.

### Support Page
- Purpose: give basic troubleshooting and contact path.
- User interaction flow: user opens support page, checks common issues, contacts developer if needed.
- Data/state changes: none.
- Error states: none.
- Acceptance criteria: support email and privacy link are visible.

### Privacy Policy
- Purpose: explain local settings, Bible text/audio network access, cache, reminders, widgets, and optional purchase/ad SDK behavior.
- User interaction flow: user opens policy and checks data handling.
- Data/state changes: none.
- Error states: outdated feature names avoided.
- Acceptance criteria: Korean and English pages mention `성경 / Bible` app name.

## Wireframe
```text
[brand intro] [mobile app preview] [support/privacy rail]

Mobile:
[sticky header]
[hero]
[Listen / Read / Study screenshots]
[local data note]
[official links]
```

