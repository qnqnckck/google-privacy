# Google Privacy Repository MVP Plan

## Idea Summary
- Product: Google Privacy Repository
- Goal: publish a stable public privacy policy URL for Public Offering Shares so it can be used in Google Play store listing and app content fields.
- Core user: the app publisher preparing release materials.
- Product promise: a simple public page with accurate disclosures and no hosting friction.

## MVP Scope
- Core user problem: Google Play requires a public privacy policy URL, but the app currently has no published policy page.
- Must-have flows:
  - open the repository homepage and reach the nested policy path for the target app
  - read a Play-compatible privacy policy for Public Offering Shares
  - use the published URL in Play Console
- Out-of-scope items:
  - custom domain setup
  - multilingual localization
  - dynamic site generators
  - app runtime changes
- Success criteria:
  - repository contains a public static privacy-policy page at `publicofferingshares/private-policy.html`
  - policy names Public Offering Shares and reflects the stated app behavior
  - repository can be published with GitHub Pages

## Feature Specification
### 1. Static repository shell
- Purpose: provide a minimal public site structure.
- User interaction flow: open repo/site -> see title and policy link -> read the policy.
- Data/state changes: none.
- Error states: missing policy link or missing app identity would make the page unusable for store submission.
- Acceptance criteria:
  - repository includes README and a static entry page
  - repository can be hosted directly by GitHub Pages

### 2. Privacy policy content
- Purpose: explain what Public Offering Shares stores and does with user data.
- User interaction flow: read sections for data collected, storage, sharing, retention, deletion, security, and contact.
- Data/state changes: none.
- Error states: inaccurate claims or omitted required sections could cause review issues.
- Acceptance criteria:
  - policy is labeled Privacy Policy
  - app name is explicit
  - contact/inquiry mechanism, retention/deletion, security, and sharing disclosures are included

### 3. Publishing configuration
- Purpose: make the page accessible through a public non-editable URL.
- User interaction flow: repository is pushed -> GitHub Pages is enabled -> publisher receives live URL.
- Data/state changes: GitHub repository and Pages settings are created remotely.
- Error states: missing repository, failed Pages enablement, or unreachable URL.
- Acceptance criteria:
  - repository is public
  - Pages is enabled
  - live URL is returned to the user

## Wireframe
```text
+--------------------------------------------------+
| Google Privacy Repository                        |
|--------------------------------------------------|
| Public Offering Shares                          |
| Public privacy policy for Google Play            |
|                                                  |
| [ Read Privacy Policy ]                          |
+--------------------------------------------------+

+--------------------------------------------------+
| Privacy Policy                                   |
|--------------------------------------------------|
| 1. Overview                                      |
| 2. Market data and app features                  |
| 3. Notifications and widget behavior             |
| 4. Data collection / sharing / analytics         |
| 5. Retention and deletion                        |
| 6. Security                                      |
| 7. Children's privacy                            |
| 8. Contact                                       |
+--------------------------------------------------+
```
