---
"harn-adventures": patch
---

Adopt `@heroiclands/package-build` 6.0.0, and let `lint:addresses` join the
pull-request gate.

The bump is what retires the exception #18 recorded. That pull request gated on
three of the four checks `npm run lint` chains and held `lint:addresses` back,
because on 5.0.0 the address linter failed this repository outright:

```
assets/content: error: holds no keyed content, so every rule here is vacuous — check that the content tree is present and that this is its root
```

The guard tested `byKey.size === 0`, so a tree carrying notes but no _keyed_
content read as an absent tree. This module ships fourteen prebuilt Adventure
documents rather than a content tree, so `assets/content/` holds exactly one
note — the package homepage — and it tripped every time. That was a fact about
the guard rather than about this tree (HeroicLands/package-build#77); #80
changed it to `notes.length === 0` and 6.0.0 ships it. `lint:addresses` now
reports _"Addresses and frontmatter are well-formed (0 addresses across 1
note)"_ and exits 0.

**The gate is the chain now.** `.github/workflows/lint.yml` runs a single
`npm run lint` in place of its three separate steps, and the comment explaining
why the fourth was held back is gone — the file no longer describes a state it
has left. `run-s` stops at the first failure, so the log still names the check
that went red. Nothing in the workflow builds or compiles a pack; every check
reads the tree directly.

**The compiled output is unchanged, and that was measured rather than assumed.**
A full `build:noci` before and after the bump emits byte-identical results: the
935 staged non-pack files hash the same, `module.json` is identical, and the
compiled LevelDB pack holds the same 14 Adventure documents with identical
content when dumped and canonicalised. The homepage the site pass emits is
identical too.

**`packFolders` is clean on both counts.** 6.0.0 is a major because it compares
the declared `packFolders` against the packs a package actually ships
(HeroicLands/package-build#81): a folder naming a pack that does not exist is
now an error that stops the manifest write, and a pack named by no folder is a
warning. Here one folder names `adventures` and `adventures` is the one pack, so
the build emits neither finding. The check was confirmed to be live rather than
silent by mutating the declaration and watching both findings fire.

**Nothing else in the major reaches this repository.** `isEquipped` is no longer
emitted on gear items (#68), but that is the item builder's output, and this
module compiles no item notes — `packs[].prebuilt` passes the shipped JSON
through unchanged, which the identical pack dump confirms. Compile order derived
from what each pass reads (#73) leaves a single-pass build unmoved, and the
TypeDoc symbol map (#75) has nothing to resolve here. The homepage's own links
are now checked (#54), which does run against this repository, and
`lint:content-links` reports them resolvable.

**`build:noci` is left alone.** The changeset for #18 noted that the siblings
prepend `lint` to the build and that this repository was blocked from doing so.
It is unblocked now, but it is a separate decision and not one this issue asked
for: `build:noci` is what `release.yml` runs, so prepending a gate there changes
what a release can fail on. `harn-ensemble`, the sibling this module is shaped
like, does not lint in its build either.
