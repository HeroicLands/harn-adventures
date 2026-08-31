---
"harn-adventures": patch
---

Adopt `@heroiclands/package-build` 9.0.0.

The shared `printWidth` moves from 80 to 100. Nothing in this tree moves with
it: the content here is a single homepage note, and both `content-build format`
and a raw Prettier run already agree the tree is clean.

The bump is taken anyway so this repository stays on the same toolchain version
as its siblings — a repository left behind on a formatting config is one whose
next contributor reformats half of it by accident.

**Bump**

_Patch._ A dependency version. No file in the tree changes.
