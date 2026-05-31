# Loutine And Shift Canvas Public Pages Plan

## Idea Summary
Add static public pages for `Loutine` and `Shift Canvas` under the `google-privacy` GitHub Pages site. Each app needs a marketing introduction page, support page, and privacy policy page for store review and public user reference.

## MVP Scope
### Core User Problem
Store listings and app review forms need stable public URLs for app introduction, support, and privacy policy.

### Must-Have Flows
- Users can open an app marketing page and understand the app purpose.
- Users can open support instructions and find a developer contact email.
- Users can open the privacy policy and see concrete local-first data handling language.
- Pages work as static HTML without backend dependencies.

### Out Of Scope
- Store deep links before final store URLs are known.
- Account, backend, or sync claims.
- Generated screenshots for Shift Canvas where no store screenshot set exists yet.

### Success Criteria
- `loutine/index.html`, `loutine/support.html`, `loutine/private-policy.html` exist and resolve local assets.
- `shiftcanvas/index.html`, `shiftcanvas/support.html`, `shiftcanvas/private-policy.html` exist and resolve local assets.
- Root `index.html` links to both app sections.
- Static HTML parsing and link checks pass.

## Feature Specification
### Loutine Pages
- Purpose: present Loutine as an action-first, recovery-first routine app.
- User interaction flow: open intro page, view actual app screenshots, jump to support or privacy policy.
- Data/state changes: none.
- Error states: if screenshots are unavailable, page still shows copy and icon.
- Acceptance criteria: page uses the Loutine icon and existing Android store screenshot assets.

### Shift Canvas Pages
- Purpose: present Shift Canvas as a local-first shift work planner for rotating workers.
- User interaction flow: open intro page, scan Today Board, month ledger, pay snapshot, and widget concepts, jump to support or privacy policy.
- Data/state changes: none.
- Error states: no external store screenshot dependency.
- Acceptance criteria: page uses the Shift Canvas icon and concrete feature copy from project docs.

## Wireframe
```text
Desktop
[brand intro / actions] [phone-style static page] [QR or link rail]

Mobile
[sticky header]
[hero]
[feature proof]
[screens or product mock sections]
[support/privacy links]
```

