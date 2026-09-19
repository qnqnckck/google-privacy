# Bible release disclosures

## Idea summary

Publish the existing reviewed Bible 1.2.8 landing, support and privacy drafts so
public information accurately describes local records, ads and purchases.

## MVP scope

Core problem: vague advertising and reset wording does not explain actual data
processing. Required flows: discover app -> read privacy/support -> store link.
Success: working public HTTPS pages, readable mobile/desktop layout, truthful
ad-removal/restore/export descriptions. No analytics, backend or redesign.

## Feature specification

- Keep the current page layout and bilingual Korean/English summaries.
- Describe the optional one-time ad-removal model and consent-gated Settings
  banner in 1.2.8, without claiming the pending iOS release is already approved.
- Name AdMob's identifier/IP/interaction/diagnostic processing and vendor links.
- Distinguish readable Markdown export from backup and local deletion from
  third-party retained records. Keep same-platform purchase restoration explicit.
- Preserve unrelated pages and changes. Verify all local relative links, render
  the affected pages, commit only these four pages and this release note.

## Wireframe

    LABHUB directory -> Bible landing -> App Store / Google Play
                              |
                         Support <-> Privacy (Korean / English)

## Authority

User approved related public-page commit and push on September 20, 2026.
Complete 28-language website localization is not claimed by these bilingual
disclosure corrections; the broader localization gate remains separate.

## Verification

- Relative href/src checks and `git diff --check -- bible`: passed.
- Rendered all four pages in the signed-in browser's local preview; text and
  icons load, and the landing page's six images load without console errors.
- Responsive viewport override did not change the observed 1280px page width;
  mobile rendering is therefore not claimed as verified in this pass.
- Existing landing screenshots are older app captures; this disclosure-only
  change does not claim that they demonstrate build 25's journal refinements.
