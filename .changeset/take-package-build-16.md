---
"harn-adventures": minor
---

**This repository moves to `@heroiclands/package-build@^16.0.0`**, seven majors
on from `^9.0.0`. The declared range becomes `^16.0.0` and the lockfile
resolves it; a caret does not cross a major, so Dependabot could never have
offered any of them.

One content change comes with it: `assets/content/homepage.md` gains
`shortcode: root`. A `type: homepage` note is an ordinary addressed note since
11.0.0 — published at `/<package>/homepage-<shortcode>/`, which is where
`[[homepage-<shortcode>|Text]]` lands — and `root` is the shortcode every
package's landing uses.

`npm run lint` passes.
