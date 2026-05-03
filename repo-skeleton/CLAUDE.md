# Project context — {{repo-name}}

This file is auto-loaded as project context whenever Claude Code is opened in this repo. Read it first, then read the companion files below as the task requires.

## What this repo is

<!-- Two or three sentences explaining what this repo does and how it fits
     into Primal Bee. Plain language. Pretend a coworker who's never seen
     it just landed in the directory. -->

{{Plain-language description of the repo. Include: what it produces, who
runs it, what other Primal Bee repos it depends on or feeds into.}}

## Companion files (read as the task warrants)

- **`CONTRIBUTING.md`** — read before any change. Setup, version-bumping flow (if applicable), what NOT to change without coordination.
- **`TODO.md`** — pending work, deferred decisions, done log. Read when continuing in-flight work or scoping new tasks.
- **`LEARNINGS.md`** — non-obvious gotchas. Read before editing the parts of the repo where past gotchas have lived.

Org-wide rules live in [`Primal-Bee/.github/CONTRIBUTING.md`](https://github.com/Primal-Bee/.github/blob/main/CONTRIBUTING.md). Read that once when you join the org; it covers branching, PRs, and the merge policy that applies to every repo here.

## Stay in sync with the org skeleton

Check occasionally whether [`Primal-Bee/.github/repo-skeleton/`](https://github.com/Primal-Bee/.github/tree/main/repo-skeleton) has changed since this repo was bootstrapped. If the upstream skeleton has new conventions, integrate them into this repo's `README.md` / `CLAUDE.md` / `CONTRIBUTING.md` / `TODO.md` / `LEARNINGS.md`.

## Hard rules (always apply, never override)

<!-- The rules in this section are inviolable for this repo. The first one
     is inherited from the org. Add repo-specific safety rules below it —
     things that, if violated, would cause real damage. Examples from
     other repos: "never call articleUpdate with isPublished: true",
     "don't rename files SKILL.md references", "never log API keys to
     stdout". Be specific. If you don't have any yet, leave just the org
     rule and add more as the repo matures. -->

1. **Every change goes through a PR.** No direct pushes to `main`. See [`Primal-Bee/.github/CONTRIBUTING.md`](https://github.com/Primal-Bee/.github/blob/main/CONTRIBUTING.md) for the full policy.

{{Add repo-specific hard rules here as they emerge.}}

## Quick orientation

<!-- A table mapping paths to what they are. Useful for fast navigation
     when Claude (or a contributor) is searching for where something
     lives. Delete if your repo is too small to need one. -->

| Path | What it is |
| --- | --- |
| `{{path}}` | {{description}} |

## Need help?

If you're unsure whether a change is safe — especially anything in the "Hard rules" list — stop and ask. The cost of pausing is near-zero; the cost of guessing wrong on a hard rule is high.
