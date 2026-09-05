# harn-adventures

## 0.1.0

### Minor Changes

- 5805a59: **Every build now emits this package's content index.** `build:db` gains
  `build:content-index`, so `build/content-index/harnadventures.jsonl` is produced
  whenever the content is built rather than whenever someone remembers to run the
  command by hand.

  Nothing generated it before — in this repository or any other — so the artifact
  existed only where a person had run `content-build content-index` themselves,
  and was as fresh as the last time they did. The editor tooling reads it, and
  compiled JournalEntry links resolve through it, so "as fresh as someone
  remembered" is not a state it can be in.

  1 note(s), and the file lands under `build/`, which is gitignored.

- e4e1736: **This repository moves to `@heroiclands/package-build@^16.0.0`**, seven majors
  on from `^9.0.0`. The declared range becomes `^16.0.0` and the lockfile
  resolves it; a caret does not cross a major, so Dependabot could never have
  offered any of them.

  One content change comes with it: `assets/content/homepage.md` gains
  `shortcode: root`. A `type: homepage` note is an ordinary addressed note since
  11.0.0 — published at `/<package>/homepage-<shortcode>/`, which is where
  `[[homepage-<shortcode>|Text]]` lands — and `root` is the shortcode every
  package's landing uses.

  `npm run lint` passes.

- 6aaab6a: **This repository moves to `@heroiclands/package-build@^17.2.0`**, the version
  whose content-index records carry a `foundry` block.

  Each record gains the UUID and anchor map the link manifest holds, and an item
  note emits a second record for its documentation journal — a document in its own
  right, with its own canonical address, so it is addressable by the same lookup
  as anything else rather than nested inside the item's record.

  `build/content-index/harnadventures.jsonl` is already emitted on every build; this is
  what makes it carry Foundry addresses as well as content.

  Verified: 1 record, the homepage, which compiles to no Foundry document.

### Patch Changes

- 46cbdef: **This repository moves to `@heroiclands/package-build@^17.0.0`**, whose major
  implements the content format the package publishes — five documented types
  that reached no schema, and three documented `data` properties that reached no
  vocabulary.

  Nothing here changes: this tree authors none of the affected types or
  properties, and `npm run lint` passes before and after. Taken to stay current
  with the toolchain rather than to fix anything.

## 0.0.1

### Patch Changes

- 862d604: Adopt `@heroiclands/package-build` 6.0.0, and let `lint:addresses` join the
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

- 27d733f: Adopt package-build 7.0.0.

  `stats.systemId` was removed from this repository's configuration because
  7.0.0 derives it (HeroicLands/package-build#48) — but the pin was still
  `^6.1.0`, where the key is merely _optional_. Under 6 the deletion resolves
  to `systemId: null` beside a real `systemVersion`: a version stamped with no
  id, silently, which is the "plausible lie" the upstream change exists to
  prevent.

  ```text
  under ^6.1.0, systemId deleted: { "systemId": null, "systemVersion": "0.8.2" }
  ```

  Bumping the pin closes the window. Verified: every pack stamps exactly the
  `systemId` and `systemVersion` it stamped before the deletion.

- fa118aa: Adopt `@heroiclands/package-build` 9.0.0.

  The shared `printWidth` moves from 80 to 100. Nothing in this tree moves with
  it: the content here is a single homepage note, and both `content-build format`
  and a raw Prettier run already agree the tree is clean.

  The bump is taken anyway so this repository stays on the same toolchain version
  as its siblings — a repository left behind on a formatting config is one whose
  next contributor reformats half of it by accident.

  **Bump**

  _Patch._ A dependency version. No file in the tree changes.

- acc05d8: Lint the tree: add the `lint` and `format` scripts this repository never had,
  and gate pull requests on the three checks that pass today.

  This repository declared **no** lint or format script at all, and none of its
  four workflows ran anything on a pull request — `deploy-site.yml`,
  `labels-sync.yml`, `no-attribution.yml` and `release.yml` all fire at deploy or
  release, so every gate it had fired _after_ the merge that broke it. Both
  siblings have the same treatment: `harn-ensemble` in HeroicLands/harn-ensemble#4
  and `sohl-kethira-basic` in HeroicLands/sohl-kethira-basic#44.

  **Seven scripts, each a thin call into the installed toolchain.** Nothing here is
  new tooling; `@heroiclands/package-build` already provides all of it, under the
  same names the sibling content repositories use, so the script surface is one
  surface everywhere:

  | script               | command                        | what it checks                                  |
  | -------------------- | ------------------------------ | ----------------------------------------------- |
  | `lint:format`        | `content-build format`         | the shared Prettier configuration               |
  | `format`             | `content-build format --write` | rewrites what `lint:format` reports             |
  | `lint:markdown`      | `content-build markdown`       | the shared markdownlint rule set                |
  | `lint:markdown:fix`  | `content-build markdown --fix` | applies the fixes markdownlint can make         |
  | `lint:addresses`     | `content-build lint`           | every note's address and frontmatter            |
  | `lint:content-links` | `content-build links`          | every anchor link lands, every address resolves |
  | `lint`               | `run-s` over the four checks   | —                                               |

  One name per command: `format:check` is not declared, because it is a second
  spelling of `lint:format`, and a repository adopting these for the first time
  should carry one name rather than inherit the drift. `lint:lang` and
  `lint:labels` are absent too — there is no `lang/` directory here, and the label
  registry is synced from the organisation rather than checked locally.

  **Prettier does not own `assets/packs/`.** Fourteen of the fifteen findings the
  formatter reported were the module's prebuilt Adventure documents — the compiled
  compendium source `packs[].prebuilt` points the build at, written by the Foundry
  compendium tooling rather than by hand. `content-build package unpack` emits them
  with `JSON.stringify(…, null, 2)`; the shared configuration is `tabWidth: 4`, so
  formatting them would put the two writers permanently at odds and every
  re-extract would revert the format and re-redden the check. The churn is not
  small either: Prettier rewrites the _smallest_ of the fourteen from 306 KB to
  388 KB and restructures its line breaks, which across all fourteen is roughly
  430,000 lines — essentially every line — burying any real content change in
  review and in `git blame`. A new `.prettierignore` excludes the directory and
  records why, on the same rule and for the same reason as `**/packs` in
  `Song-of-Heroic-Lands-FoundryVTT` and `assets/manifests/*.json` in
  `sohl-thalorna` and `harn-ensemble`.

  **`README.md` is fixed rather than recorded.** It was the whole of the remaining
  backlog — the fifteenth format finding and both markdown findings
  (`MD034/no-bare-urls`) — so at this size there was nothing to be gained by
  carrying it. The two bare URLs became autolinks and Prettier reformatted the
  file: blank lines around headings, a padded source-material table, one collapsed
  double space, and one badge destination wrapped in `<…>` because the shields.io
  query string contains parentheses. No content note is touched.

  **CI gates three of the four, and the fourth is held back on a named
  dependency.** A new `Lint` workflow runs `lint:format`, `lint:markdown` and
  `lint:content-links` on every pull request. It does **not** run
  `lint:addresses`: this module ships prebuilt Adventures rather than a content
  tree, so `assets/content/` holds exactly one note — the package homepage — and
  the address linter currently reads that as an empty tree and fails as
  _"holds no keyed content, so every rule here is vacuous"_. That is a fact about
  the guard, not about this repository; HeroicLands/package-build#80 changes it
  from `byKey.size === 0` to `notes.length === 0` and is open and unmerged. Wiring
  it in now would install a check that cannot pass, which is worse than no check.
  The workflow says all of this in its own comment, so the condition for turning it
  on travels with the file: when #80 has merged and this repository takes the
  release carrying it, all three steps collapse into a single `npm run lint`.

  **`build:noci` is left alone.** The siblings run `lint` as its first stage and
  this repository should end up there too, but `lint` is red on `lint:addresses`
  until #80 lands, and prepending a red gate to the build would move a failure
  without fixing one.
