# WorkLog Public Pages Plan

## Idea Summary
Replace the old Shift Canvas public pages with WorkLog pages for app store submission, using the multilingual structure of the Fate pages as the reference style.

## MVP Scope
Core user problem: App Store and public links should identify the app as WorkLog/근무로그, use the new icon, and provide marketing, privacy, and support pages in supported languages.

Must-have flows:
- Create `worklog/index.html`, `worklog/private-policy.html`, and `worklog/support.html`.
- Update the old `shiftcanvas` pages to redirect to `worklog`.
- Update the Google Privacy index and LABHUB router links from `shiftcanvas` naming to `worklog`.
- Replace the public icon with `resource/worklog/icon/icon.png`.
- Keep pages static and GitHub Pages compatible.

Out-of-scope items:
- Adding server-side routing.
- Publishing or committing the changes.
- Adding new app runtime behavior.

Success criteria:
- Public pages contain WorkLog/근무로그 copy and no Shift Canvas branding.
- WorkLog pages include Korean, English, Japanese, German, Chinese, Spanish, and Portuguese sections or language switching.
- The old `shiftcanvas` URL redirects to the new `worklog` URL.
- Static HTML files are parseable and key links are updated.

## Feature Specification
Marketing page:
- Purpose: provide a store marketing URL for WorkLog.
- User interaction flow: visitor chooses language and sees app features, privacy-first positioning, support and privacy links.
- Data/state changes: none.
- Error states: stale app naming or missing icon harms store review consistency.
- Acceptance criteria: page uses new icon, WorkLog naming, package id, and links to support/privacy pages.

Privacy page:
- Purpose: provide a public privacy policy URL.
- User interaction flow: visitor selects language and reads app-specific privacy terms.
- Data/state changes: none.
- Error states: policy claims must not exceed verified app behavior.
- Acceptance criteria: page states local-first storage, optional backup/share/export, notifications, widgets, ads/subscription readiness, and contact path.

Support page:
- Purpose: provide an App Store support URL.
- User interaction flow: visitor selects language, sees troubleshooting and contact links.
- Data/state changes: none.
- Error states: stale Shift Canvas naming or old links confuse users.
- Acceptance criteria: support page uses WorkLog naming and app-specific troubleshooting.

## Wireframe
```text
google-privacy/
├── worklog/
│   ├── assets/app-icon.png
│   ├── index.html
│   ├── private-policy.html
│   └── support.html
├── shiftcanvas/
│   ├── index.html -> redirect
│   ├── private-policy.html -> redirect
│   └── support.html -> redirect
└── index.html links -> worklog
```
