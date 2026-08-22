# Known Issues — Nginx-File-Directory

Concrete defects and gaps found while writing this repository's documentation in
August 2026. **Nothing here was changed** — each one needs a code, configuration, or
licensing decision rather than a documentation one.

Ordered by severity. See [`docs/roadmap.md`](../roadmap.md) for the narrative version,
which also covers deliberate non-goals.

**3 open:** 1 medium, 2 low.

## 1. Nothing protects the whitespace the layout depends on

**Severity:** Medium
**Where:** `index.html`, repository root

**What:** The listing sits in a `<pre>` block and the columns align by literal spaces. There is no `.editorconfig` and no Prettier ignore rule.

**Why it matters:** Any formatter that touches the file reflows the block and visibly breaks the layout. This is the failure people will actually hit, and the repository does nothing to prevent it.

**Suggested fix:** Add an `.editorconfig` and a formatter ignore rule. Most valuable change here.

## 2. The directory name appears twice

**Severity:** Low
**Where:** `index.html`

**What:** Both the `<title>` tag and the `<h1>` carry it.

**Why it matters:** Changing one without the other is easy to miss.

**Suggested fix:** Note it in a comment, or single-source it.

## 3. Per-repo issue templates override the org-level forms

**Severity:** Low
**Where:** `.github/ISSUE_TEMPLATE/`

**What:** Same as the Apache and Chrome siblings.

**Why it matters:** This repository does not inherit the shared set.

**Suggested fix:** Delete them.

---

## Also, across every repository

**`.bandit` is present on disk but untracked in git.** Verified in PyWorkout, treklogger,
skyscanner-cli, booking-cli, piggy, and aibot — the config file exists locally in each but
`git ls-files` does not know about it, so none of it reached GitHub.

The August 2026 security sweep therefore looks complete locally and landed nowhere. Worth
checking across all 44 repositories it covered.
