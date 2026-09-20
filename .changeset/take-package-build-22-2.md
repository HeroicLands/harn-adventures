---
"harn-adventures": patch
---

**This collection moves to `@heroiclands/package-build@^22.2.0`.**

The module's Foundry listing and the site's meta description are each written
for their own reader. The Foundry browser shows `descriptionHtml` from
`package-build.config.yaml`, while the website uses `site.description` from the
same file. `package.json`'s `description` key is removed — it is read by nothing
now, and the toolchain warns if it is present. Taken to stay current with the
toolchain.
