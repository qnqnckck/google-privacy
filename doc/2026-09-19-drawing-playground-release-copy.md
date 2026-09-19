# Drawing Playground canonical publication correction

## Idea summary

Publish the reviewed six-language Drawing Playground website to the repository
that actually serves its canonical public URL. The separate `google-privacy`
project Pages site shadows the same folder in the `qnqnckck.github.io` user site.

## MVP scope

Must-have: update only Drawing Playground's existing landing/support/privacy
pages, preserve its typo-policy alias and existing assets, publish reviewed
six-language copy, and verify HTTPS content. Out of scope: other apps, app
runtime, store binaries, prices, accounts, native-QA claims or new design assets.
Success: the live canonical pages return version1.9.5 content and six working
language sections; old root links from LABHUB resolve correctly.

## Feature specification

| Feature | Interaction and state | Acceptance |
| --- | --- | --- |
| Canonical pages | Existing Drawing Playground path; language selection | Mirror exact reviewed landing/support/privacy HTML and local CSS/JS |
| Compatibility | Existing private-policy alias and LABHUB root links | Keep old URLs and selected language working |
| Publication | main branch GitHub Pages | Correct deployed commit and live page content both verified |

## Wireframe

```text
qnqnckck.github.io (master): router + root compatibility pages
             |
             v
google-privacy (main): drawing-playground/{index,support,privacy-policy}.html
                         + six locale fragments and private-policy alias
```

## Evidence and bounded impact

The user-site commit5c94c5003f8568cbf331e04ea3e1bb8e66f7584a deployed
successfully, and its root compatibility pages were live. However canonical
URLs still returned August14 content and the newly added CSS returned404.
Read-only Pages configuration confirmed `qnqnckck/google-privacy` serves
https://qnqnckck.github.io/google-privacy/ from main. This is a separate
publication source, not simply browser/CDN caching.

Copy only the six app-specific reviewed text assets from the user-site mirror:
index.html, support.html, privacy-policy.html, private-policy.html, site.css,
languages.js. The existing app-icon hashes match; no image copy is needed.
The earlier local18-locale layout/linguistic/link checks remain applicable to
identical files. Recheck source parity, syntax, scoped diff and actual live URLs.
Native app testing and App Store submission remain separate pending gates.
