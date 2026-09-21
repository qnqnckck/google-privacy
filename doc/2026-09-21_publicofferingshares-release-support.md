# PublicOfferingShares release support - 2026-09-21

## 1. Idea summary

Keep the public support page useful for the 1.1.27 compact-header/calendar release without changing privacy claims or approved artwork.

## 2. MVP scope

- Problem: support requests need the installed app version and text-size setting to distinguish earlier layouts and reproduce clipping.
- Must-have: add these two diagnostics to the existing support checklist; preserve router, store links, privacy and other apps.
- Out of scope: new assets, tracking, new locales and legal-policy changes.
- Success: scoped commit/push/Pages publication, live text verified and desktop/mobile pages usable.

## 3. Feature specification

- Purpose: help users send actionable layout issue reports.
- Interaction: read checklist, then use the existing email or issue link.
- State: no runtime or personal data collection changes.
- Errors: keep static content readable without JavaScript and preserve current links.
- Acceptance: app version and display/text size are explicitly listed; no promise of store availability before review approval.
- Visual direction: existing support card, typography and spacing; no artwork replacement.

## 4. Wireframe

```text
Support -> existing help topics -> before contacting
  Device / OS
  App version
  Display and text size for layout issues
  Screen / reproduction steps / optional screenshot
```

## Results

- Scoped source commit `e622d72` pushed to main; GitHub Pages run `35550526669` succeeded.
- Browser reload of the public support URL shows both new checklist items.
- Router entry and app icon, product/support/privacy and download links verified on public HTTPS pages. Product, support and privacy inspected at desktop and 390x844 mobile widths; no horizontal document overflow, broken app images or captured console errors in the checked pages. Router carousel retains its intentional horizontal scroll.
- Existing approved artwork, policy date and other apps remain unchanged.
