# Issue Reporting — harn-adventures

This document defines how issues are created and classified in the
**`harn-adventures`** repository, which ships the Hârn Adventures module: unofficial
HârnWorld fan material, as Foundry compendium packs and nothing else.

**This repository is its own tracker.** File Hârn Adventures work here, not in a
system repository. Every repository in the project tracks its own work — the site
included.

> **This repository is a carve-out.** It is unofficial HârnWorld fan material —
> "Fanon" under Lythia.com's terms, derived from material copyrighted by Keléstia
> Productions Ltd, Columbia Games Inc, and N. Robin Crossby — licensed CC BY-NC-SA
> 4.0, separately from SoHL. Nothing elsewhere in the project may depend on it: it
> must stay withdrawable without affecting any system or package. **Its content is
> never published to heroiclands.org** — no journal text, artwork, item descriptions
> or compiled notes, and no site or knowledgebase pages generated from any of it.
> That is a licensing boundary, not a gap to fill.
>
> It is not a rule against the module being _named_ on the site. Every package has a
> top-level, human-authored homepage announcing it — this one's will be at
> `https://www.heroiclands.org/harnadventures/`, an address that derives from the
> package name rather than the repository name. Such a page says what the module is,
> which system it needs, where the source lives, and carries the licence notice: it
> discloses nothing licensed, and it creates no dependency, because nothing has to
> resolve through it — withdrawing the module costs a page. The **link manifest** is
> where the dependency edge would be, and it stays unpublished in both directions for
> that reason. A homepage is not that edge.
>
> An issue proposing a dependency **on** this repository, or publication of its
> **content**, is out of scope, and belongs as a discussion before it becomes an
> issue anywhere.

The core discipline is simple — four axes, each answering a different question:

- **Type** — _"what shape of work is this?"_ One per issue, from a closed set of five.
- **Priority** — _"how soon and how badly does this need doing?"_ A GitHub issue field, one value, defaults to Medium.
- **Labels** — _"what is this about?"_ Categorization only, chosen **only** from the registry below. Never invent a label.
- **Milestone** — _"which capability gate does this advance?"_ A native GitHub milestone (no due date), at most one, selected from a curated set (see §4).

Type, priority, and milestone are structured single values (one each). Labels
stack. Keep the roles separate: do not encode priority, urgency, or work-shape as a
label; do not encode subject matter as a type; and do not encode a capability gate
as a label when a milestone is its proper home.

## 1. Issue types

Exactly **one** type per issue. Choose using the decision procedure in §5 when in
doubt. Do not leave an issue untyped.

Issue types are **organization-level** in the `HeroicLands` org, so the same five
types — and their definitions — are shared with every other repository in the
project. They are not redefined here.

| Type        | Use it when…                                                                                                                                                        | Do **not** use it for…                                                                                                 |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **bug**     | Existing, shipped behavior is wrong or broken relative to what it should do — an error, crash, incorrect result, or regression.                                     | Missing capability (that's a _feature_); known-incomplete work in progress; a chore.                                   |
| **feature** | A new capability or enhancement that does not exist yet, deliverable as one shippable unit of value.                                                                | Anything broken (_bug_); work large enough to need many sub-issues (_epic_); pure maintenance (_task_).                |
| **epic**    | A large body of work that only makes sense decomposed into multiple sub-issues; a coordinating container tracked by its children.                                   | Anything you can ship as a single issue. If it has no sub-issues, it is not an epic.                                   |
| **task**    | Necessary work that is neither a defect nor a new capability: chores, maintenance, refactors, dependency bumps, tooling, docs, releases. May or may not touch code. | Work whose outcome is uncertain and exploratory (_spike_); a defect (_bug_).                                           |
| **spike**   | A **timeboxed** investigation whose deliverable is a _decision, answer, or recommendation_ — not shipped code. Outcome is genuinely uncertain going in.             | Work whose steps are already known (that's a _task_). A spike that produces code instead of a conclusion was mistyped. |

**Type rules**

- **MUST** assign exactly one type.
- A **bug** is _broken_; a **feature** is _missing_. That distinction resolves most ambiguity — decide which word fits before anything else.
- An **epic** MUST link its sub-issues (native GitHub sub-issues; see §6) and SHOULD carry little implementation detail of its own. Its acceptance is "all sub-issues closed and the whole verified together."
- A **spike** MUST state (a) the question it answers and (b) its timebox. It closes when the question is answered, and it typically _spawns_ follow-up feature/task/bug issues rather than doing the work itself.
- A **refactor** that changes no external behavior is a **task**, tagged `tech-debt` — it is not a feature and not a bug.

**What "broken" means for content.** This repository ships prose and data, not
running code, so a bug is usually a wrong or unloadable _fact_: a dead link, a
shortcode collision, a note that fails to compile into its pack, an entry whose
document ID moved under an existing world. A note that is merely thin or unwritten
is not broken — that is a **feature** (the material is missing) or a **task** (it is
scheduled work).

**A licence problem is a bug.** Shipping third-party art, trade dress, or verbatim
rulebook text is broken behavior, not a missing feature — file it as a **bug**, and
prioritize it by exposure rather than by effort.

## 2. Priority (GitHub issue field)

Priority is a native **Priority** field on the issue itself — an
organization-level issue field, **not** a label and **not** tied to a Project. Set
it in the issue sidebar; the repo issue list filters on it
(`field.priority:high,medium`), and it is read/written through the GitHub issue
API. One value per issue, from: **Urgent · High · Medium · Low**.

Priority is about attention, not schedule — this project has no deadlines, so
priority answers "when I next sit down, what deserves my time?" not "what is due."

| Priority   | Meaning                                                      | Typical triggers                                                                                                                                       |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Urgent** | Do it next session. Active harm or a hard blocker.           | Content loss or corruption; packs that will not compile, so nothing ships; the published site is down or serving wrong pages; blocks the current gate. |
| **High**   | Wanted soon; the current gate leans on it.                   | A published address broken with no redirect; work the active milestone depends on.                                                                     |
| **Medium** | **Default.** Should get done; not blocking the current gate. | Most content and tooling work; defects with a workaround.                                                                                              |
| **Low**    | Deferrable indefinitely with little cost.                    | Cosmetic issues; nice-to-haves; long-tail edge cases; opportunistic cleanup.                                                                           |

**Priority rules**

- **MUST** set a priority on every issue.
- **Default to Medium.** Anything higher MUST be justified in the body (one line: why the impact warrants it). Do not inflate — not everything is High.
- Priority is independent of type, labels, **and** milestone. A `security`-labelled issue is **not** automatically Urgent: hardening with no known exploit can be Low; an exploit in the wild is Urgent. Judge impact, not the topic.
- An **epic**'s priority reflects the initiative's importance, not the max of its children.

## 3. Labels — the closed registry

Labels are for **categorization only**. The table below is the **complete,
authoritative set for this repository**. Its machine-readable twin is
`.github/labels.yml`, which the `labels-sync` workflow reconciles onto GitHub (the
set is _closed_ — a label not in the registry is deleted on sync). Nothing checks
the table below against that file, so the two are kept in step by hand.

> **MUST NOT invent, rename, or improvise labels.** If no existing label fits, add
> none and (if it matters) note the gap in the issue body for a maintainer to decide.
> Extending this registry is a deliberate decision made by editing **both** this
> table and `.github/labels.yml`, not something done at filing time.

**This registry is the narrowest in the project, on purpose.** Each repository's
registry describes only what that repository can hold. `system`, `tests`, `site`,
and `thalorna` are absent here: this repository ships no system code, no test
suite, and no website, and every issue in it is adventure material by definition.

| Label             | Scope                                                                                                                         |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `content`         | Adventure material — adventures, journals, scenes, maps, actors, roll tables, artwork.                                        |
| `documentation`   | Documentation about this repository — README, process, authoring guides.                                                      |
| `devops`          | Build, tooling, pack pipeline, release, repo config.                                                                          |
| `security`        | Touches an attack surface: data integrity, macro/script execution, injection, or anything warranting private disclosure (§7). |
| `tech-debt`       | Restructuring or cleanup of working content or tooling; refactors.                                                            |
| `regression`      | Something that previously worked and stopped. Pairs with type `bug`.                                                          |
| `breaking-change` | Alters a document ID, pack name, or compatibility in a way existing worlds will notice.                                       |
| `blocked`         | Cannot proceed until an external dependency or another issue clears.                                                          |
| `duplicate`       | This issue or pull request already exists.                                                                                    |
| `question`        | Further information is requested.                                                                                             |
| `wontfix`         | This will not be worked on.                                                                                                   |

> **No capability-gate labels.** Progress toward a capability is tracked by
> **milestones** (§4), not labels. Do not add `bestiary`-style or `v1.0`-style labels
> to mark what a milestone already carries.

**Label rules**

- Choose labels **only** from this file. No exceptions.
- Labels are additive and orthogonal — `content` + `devops` + `regression` on one bug is fine.
- Do not use a label to express something a type, the priority field, or a milestone already expresses.

## 4. Milestones — capability gates

Milestones here are **capability gates, not calendar dates.** Each milestone is a
demonstrable threshold the package crosses — a state you can point at and say "it
does this now" — and **crossing a gate is what triggers a release.** This project is
not date-driven and has no deadlines, and GitHub supports that directly: a
milestone's due date is optional, and its progress bar is computed from the ratio of
closed to open issues, not from any date. Leave due dates blank.

**Name milestones by the capability reached,** phrased as a state of the package —
"the core bestiary is playable", "the western kingdoms are covered" — rather than by a
date or a version number alone. If you want the order explicit, encode it in the
name (`M1 · …`, `M2 · …`); otherwise let the list carry it.

**An issue's milestone is the gate its work advances.** When every issue in a
milestone is closed, the package has crossed that gate. One milestone per issue
(GitHub enforces this); if an issue seems to serve two gates, it usually belongs to
the earlier one or is scoped too large.

**Milestone vs. epic — different lenses, keep them straight:**

|           | **Epic** (a type)                          | **Milestone** (a gate)                       |
| --------- | ------------------------------------------ | -------------------------------------------- |
| Groups by | work breakdown — a tree of sub-issues      | outcome — a capability the package gains     |
| Answers   | "what are all the pieces of _this build_?" | "how close is it to _doing this thing_?"     |
| Done when | all its sub-issues are closed              | all issues tagged to it are closed           |
| Shape     | vertical: one initiative, decomposed       | horizontal: a slice across the whole package |

**The milestone set is curated, like the label registry** — select from existing
gates and never invent one.

- You MAY assign an issue to a milestone when its work **unambiguously advances exactly one existing gate**.
- Leave the milestone **unset** when the issue advances none of the current gates (it is future/backlog), spans several, or the mapping is unclear. An unset milestone is a normal, correct state.
- You MUST NOT create a new milestone. If no gate fits and one seems warranted, note it in the body and raise it for awareness.

**This repository currently defines no milestones.** That is deliberate, not an
oversight: gates are named when the maintainer knows which capability the package is
driving at, and until then every issue's milestone is correctly unset. Do not invent
one to fill the field.

### Milestones and releases

**Reaching a gate is what cuts a release.** When every issue in a milestone is
closed, the package has demonstrably gained that capability — and that is the
trigger to cut a new release, versioned for the capability reached, not for any
date. There is no release calendar and no due dates: releases are **paced by
capability**, so the milestone progress bar is the only schedule the project keeps.

## 5. Choosing the type — decision procedure

Walk this in order; take the first match.

1. Is something **broken** relative to intended behavior? → **bug** (add `regression` if it used to work).
2. Is the outcome **genuinely uncertain** and the deliverable a **decision/answer**? → **spike** (state question + timebox).
3. Is this too large to ship as one issue, needing **multiple sub-issues** to coordinate? → **epic**.
4. Is it a **new capability or enhancement** that doesn't exist yet? → **feature**.
5. Otherwise — chore, maintenance, refactor, docs, tooling, release? → **task**.

Then, regardless of type: set **priority** (default Medium; justify higher), apply
any **labels** from §3 that categorize it, and set a **milestone** only when the issue
clearly advances one existing capability gate (§4) — otherwise leave it unset.

## 6. Body structure by type

Titles: imperative and specific. "Fix the deity pack referencing a retired
shortcode," not "link bug." No trailing punctuation.

Every issue body should give enough context that someone with repo familiarity but
no memory of the conversation can act on it. Use the shape for its type — the issue
forms in `.github/ISSUE_TEMPLATE/` pre-fill each of these.

### Bug

Bugs should describe the problem as fully as possible, so it may be easily
reproduced. The description should NOT contain a description of how to fix the
issue. Suggestions for fixes or approaches may be placed in comments.

**Acceptance criteria** is optional.

```
## Summary
One sentence: what's wrong.

## Steps to reproduce
1. …
2. …

## Expected vs. actual
Expected: …
Actual: …

## Acceptance criteria
- [ ] Observable condition 1
- [ ] Observable condition 2

## Environment
Foundry version · SoHL system version · module version · browser/OS if relevant

## Notes
Stack traces, console output, suspected cause.
```

### Feature

```
## Problem / motivation
What need or gap this addresses.

## Proposed solution
What to build. Sketch the approach if known.

## Acceptance criteria
- [ ] Observable condition 1
- [ ] Observable condition 2
```

### Epic

```
## Goal
The outcome this initiative delivers.

## Scope
In scope / out of scope.

## Sub-issues
(Linked as native sub-issues; list mirrors them.)
- [ ] #…
- [ ] #…

## Done when
All sub-issues closed and integration verified.
```

### Task

```
## What
The work to be done.

## Why
The reason it's needed (keeps chores from looking arbitrary).
```

### Spike

```
## Question
The specific thing we need to decide or learn.

## Timebox
e.g. 1 day / 4 hours. MUST be present.

## Deliverable
The form of the answer: a decision, a recommendation, a written finding,
a prototype-to-throw-away. NOT production code.

## Follow-up
Note that follow-up feature/task/bug issues will be filed from the outcome.
```

## 7. Security issues — special handling

If an issue would be labelled `security` **and** describes an exploitable weakness
(not merely hardening), **do not open a public issue**. Use GitHub's private
security advisories / vulnerability reporting instead — the "Report a
vulnerability" button on this repository's Security tab, also linked from the issue
chooser. This package ships into users' Foundry instances, so a macro-injection or
data-execution path in shipped content has a real (if small) attack surface. When in
doubt, disclose privately and let a maintainer decide whether to make it public.

A **licence** problem is not a security problem and does not go to an advisory —
file it as a public `bug`.

## 8. Worked examples

**Bug, Urgent**

> **Title:** Remove the official Columbia illustration still shipped in the Jedes Keep journals
> **Type:** bug · **Priority:** Urgent · **Labels:** `content` · **Milestone:** _(unset)_
> Body: third-party art is shipping in a released pack — a licence breach with active exposure → Urgent.

**Bug, Medium, regression**

> **Title:** Fix the adventure pack dropping its actors on import
> **Type:** bug · **Priority:** Medium · **Labels:** `content`, `devops`, `regression` · **Milestone:** _(unset)_
> Body: imported before, does not now; a manual drag from the actor pack works around it → Medium.

**Feature, Medium**

> **Title:** Add the Song of Heroic Lands actor stat blocks
> **Type:** feature · **Priority:** Medium · **Labels:** `content` · **Milestone:** _(unset)_
> Body: material that does not exist yet, shippable as one unit → Medium.

**Epic, Medium**

> **Title:** Cover the core bestiary
> **Type:** epic · **Priority:** Medium · **Labels:** `content`
> Body: coordinates a tree of sub-issues (one per creature family), each filed separately and linked.

**Task, Low**

> **Title:** Bump @heroiclands/package-build to the current release
> **Type:** task · **Priority:** Low · **Labels:** `devops` · **Milestone:** _(unset)_
> Body: routine maintenance, deferrable → Low.

**Spike, Medium**

> **Title:** Decide how far this module may reference sohl package content
> **Type:** spike · **Priority:** Medium · **Labels:** `content`
> Body: **Question** — which cross-package references keep the carve-out withdrawable? **Timebox** — 4 hours. **Deliverable** — a written rule. Follow-up issues filed from the finding.

## 9. Which repository does an issue belong in?

The project spans several repositories in the `HeroicLands` organization, and — as
of the process split — **each one tracks its own work.** There is no central
tracker.

| Repository                        | Tracks                                                                      |
| --------------------------------- | --------------------------------------------------------------------------- |
| `harn-adventures`                 | **This repository** — the Hârn Adventures module, Foundry packs only        |
| `HarnMaster-3-FoundryVTT`         | The HârnMaster 3 (`hm3`) Foundry system                                     |
| `Song-of-Heroic-Lands-FoundryVTT` | The Foundry system code, the `sohl` package's content, and the system build |
| `sohl-thalorna`                   | The `thalorna` package — original setting content and the `/thalorna` site  |
| `sohl-kethira-basic`              | The `kethira` package — Foundry compendium packs only                       |
| `heroiclands-site`                | heroiclands.org — its content, Cloudflare Pages, the CDN                    |
| `heroiclands-hugo-theme`          | The shared Hugo theme the project's sites render through                    |

**File the issue where the work will be done.** The rule is delivery, not subject: if
the fix is an edit to a file in this repository, the issue belongs here, even when the
symptom shows up elsewhere. An adventure whose actors load wrong because `hm3` or
`sohl` mishandles the data model is a system issue; the same actors loading wrong
because this repository's pack declares the wrong `system` is an issue here.

**Nothing outside this repository may depend on it.** If an issue here would require a
change in the system or another package to land first, that is a signal the carve-out
is being eroded — say so in the body rather than filing the dependent issue there.

**When work genuinely spans two repositories, file in each and link them.** Cross-repo
references work fine (`HeroicLands/<repo>#123`); what does **not** work is closing:

> **Closing keywords do not cross repositories.** A pull request here carrying
> `Closes HeroicLands/Song-of-Heroic-Lands-FoundryVTT#123` creates a reference but
> **does not close** that issue — GitHub only auto-closes within the same repository.
> A cross-repository issue is **closed by hand**, with a comment linking the delivering
> commit or pull request. Never assume the keyword did it; check.

**Historical note.** Until August 2026 this content lived in seventeen separate
repositories under `toastygm`, each tracking its own issues. They are superseded by
this one.

## Self-check before filing

You should confirm all of these before submitting an issue:

- [ ] This is the right repository — the work will be delivered here.
- [ ] Exactly **one type** assigned, chosen via the §5 procedure.
- [ ] A **priority** is set. If above Medium, the body justifies it in one line.
- [ ] Every label comes from the label registry. **Zero** invented labels.
- [ ] No label duplicates what the type, priority field, or milestone already says.
- [ ] **Milestone** set only when the issue clearly advances one existing capability gate (§4); otherwise unset. **Never** invented.
- [ ] Title is imperative and specific; body follows the appropriate shape for its type. Title should not encode labels or other field information.
- [ ] If `security` + exploitable → routed to **private advisory**, not a public issue.
- [ ] If **epic** → sub-issues are linked. If **spike** → question and timebox are present.
