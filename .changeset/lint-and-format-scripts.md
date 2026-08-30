---
"harn-adventures": patch
---

Lint the tree: add the `lint` and `format` scripts this repository never had,
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
