# PublicOfferingShares 1.1.26 public pages

## 1. Idea summary

Align the existing app pages with the release's verified behavior. This project Pages site takes precedence at /google-privacy/ over the mirrored folder in the central directory repository.

## 2. MVP scope

- Problem: static financial examples look current and external backups are not covered in deletion guidance.
- Must-have: truthful example labels, home/report feature split, safe restore support, backup file deletion guidance, existing HTTPS links and icon.
- Out of scope: redesign, screenshots replacement, locale expansion, tracking and runtime code.
- Success: scoped commit/push, successful Pages deployment, live product/support/privacy verification at desktop and mobile sizes.
- Monetization: existing contextual AdMob banners; no changes to data collection or purchases.

## 3. Feature specification

- Product: remove static current-week claims; identify legacy screen/example data; describe current home/report split without claiming store approval.
- Support: keep a separate backup before import; invalid formats are rejected without replacing records.
- Privacy: exported or automatic backup files can survive uninstall and require deletion in the file manager.
- Errors/acceptance: stop if unrelated changes or broken URLs are found; preserve all other apps.
- Cross-repository impact: identical app-specific copy is mirrored in packages/labhub-site; router and assets remain unchanged.

## 4. Wireframe

```text
router.html -> product -> stores
                     -> support -> contact / backup help
                     -> privacy -> storage / backup deletion
```

## Verification

Pending live deployment verification.
