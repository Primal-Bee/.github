# Project context — {{repo-name}}

This file is auto-loaded as project context whenever Claude Code is opened in this repo. Read it first, then read the companion files below as the task requires.

## What this repo is

<!-- Two or three sentences explaining what this repo does and how it fits
     into Primal Bee. Plain language. Pretend a coworker who's never seen
     it just landed in the directory. -->

{{Plain-language description of the repo. Include: what it produces, who
runs it, what other Primal Bee repos it depends on or feeds into.}}

## Companion files

Read the companion files below before any task that touches the area they cover (`CONTRIBUTING.md` for any change; `TODO.md` if continuing in-flight work; `LEARNINGS.md` before editing areas with prior gotchas).

- **`CONTRIBUTING.md`** — read before any change. Setup, version-bumping flow (if applicable), what NOT to change without coordination.
- **`TODO.md`** — pending work, deferred decisions, done log. Read when continuing in-flight work or scoping new tasks. When you hit a non-obvious gotcha worth saving, append it to `LEARNINGS.md` before moving on.
- **`LEARNINGS.md`** — non-obvious gotchas. Read before editing the parts of the repo where past gotchas have lived.

Org-wide rules live in [`Primal-Bee/.github/CONTRIBUTING.md`](https://github.com/Primal-Bee/.github/blob/main/CONTRIBUTING.md). Read that once when you join the org; it covers branching, PRs, and the merge policy that applies to every repo here.

## Hard rules (always apply, never override)

<!-- The rules in this section are inviolable for this repo. The first one
     is inherited from the org. Add repo-specific safety rules below it —
     things that, if violated, would cause real damage. Examples from
     other repos: "never call articleUpdate with isPublished: true",
     "don't rename files SKILL.md references", "never log API keys to
     stdout". Be specific. If you don't have any yet, leave just the org
     rule and add more as the repo matures. -->

1. **Every change goes through a PR.** No direct pushes to `main`. See [`Primal-Bee/.github/CONTRIBUTING.md`](https://github.com/Primal-Bee/.github/blob/main/CONTRIBUTING.md) for the full policy.

2. **When creating a new repo (any org), copy `repo-skeleton/` before adding project content.** Land the skeleton via PR — the no-direct-push-to-main rule (#1) applies from commit one.

3. **Ask before opening a PR.** Don't open one autonomously, even if you think the work is done. Plan approval doesn't imply PR approval — ask again when the branch is ready to push.

{{Add repo-specific hard rules here as they emerge.}}

## Working agreements

How AI agents (Claude Code, etc.) and humans should collaborate in this repo:

- **Ask clarifying questions before complex tasks.** If the task isn't trivial, surface ambiguities before starting. Five "obvious" questions answered beats one wrong assumption landing in a PR.
- **Use plan mode before complex tasks.** For anything beyond a one-line edit, write the plan first, get alignment, then execute.
- **Make minimal changes.** Don't refactor unrelated code. Stay in the lane the task asked for; flag anything else as a follow-up rather than folding it in.
- **Run tests after every change, fix failures before moving on.** Don't pile change on top of a broken state.
- **Atomic commits.** For documentation changes (`.md`, `.txt`, `.csv`, etc.) — one commit per file. For code changes that span multiple files but represent one logical change — one commit per logical change. Either way, no giant catch-all commits.
- **PRs are batched commits, reviewed as a whole.** A PR collects related work into a reviewable unit. (Asking before opening a PR is now Hard rule #3.)
- **Never silently choose between two viable approaches.** Lay out the tradeoffs and wait for the human to pick.

## Quick orientation

<!-- A table mapping paths to what they are. Useful for fast navigation
     when Claude (or a contributor) is searching for where something
     lives. Delete if your repo is too small to need one. -->

| Path | What it is |
| --- | --- |
| `{{path}}` | {{description}} |

## Need help?

If you're unsure whether a change is safe — especially anything in the "Hard rules" list — stop and ask. The cost of pausing is near-zero; the cost of guessing wrong on a hard rule is high.
