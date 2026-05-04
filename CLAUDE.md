# Project context — Primal-Bee/.github

This file is auto-loaded as project context whenever Claude Code is opened in this repo. Read it first, then read the companion files below as the task requires.

## What this repo is

The org-level `.github` repo for [Primal-Bee](https://github.com/Primal-Bee). It holds the small set of files GitHub auto-applies across every repo in the org — the org landing page, the org-wide `CONTRIBUTING.md`, the auto-applied PR template — plus a `repo-skeleton/` folder of starter docs that get hand-copied into new repos.

The repo is **public**. Anything committed here is visible at github.com/Primal-Bee/.github. It does not contain plugin or product source code; each Primal Bee plugin/product (e.g. `primalbee-shopify-blog`, `primalbee-brand-guide`, `primalbee-internal-tools`) lives in its own repo.

## Companion files (read as the task warrants)

- **`CONTRIBUTING.md`** — note: the root `CONTRIBUTING.md` here is the **org-wide** document GitHub serves as the fallback to every other Primal-Bee repo. There is no separate per-repo `CONTRIBUTING.md`; the org-wide one covers what applies here too.
- **`TODO.md`** — pending work, deferred decisions, done log. **Gitignored — local-only by design.** Won't exist in a fresh clone; create from `repo-skeleton/TODO.md` if you need it.
- **`LEARNINGS.md`** — non-obvious gotchas. **Gitignored — local-only by design.** Same as `TODO.md`: not present in a fresh clone. The intent is to avoid overexposing internal scheduling and gotchas on a public repo.

Org-wide rules live in this repo's own [`CONTRIBUTING.md`](./CONTRIBUTING.md). Read it once; it covers branching, PRs, and the merge policy that applies to every repo here.

## Hard rules (always apply, never override)

1. **Every change goes through a PR.** No direct pushes to `main`. The bootstrap commit was the one-time exception (empty repo, no `main` to protect). See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for the full policy.

2. **Changes here ripple to every repo in the org.** `CONTRIBUTING.md`, `PULL_REQUEST_TEMPLATE.md`, and the `repo-skeleton/` files are inherited (or copied) by every Primal-Bee repo. Default to extra caution: a wording change here can subtly change the rules every plugin and product repo operates under. When the change is structural — renaming a file GitHub specifically looks for, removing a section other repos may link to — loop in a collaborator before merging.

3. **Don't commit `TODO.md` or `LEARNINGS.md`.** They're gitignored on purpose for this public repo. If you need to track something visible to the org, put it in an issue, not these files.

## Working agreements

How AI agents (Claude Code, etc.) and humans should collaborate in this repo:

- **Ask clarifying questions before complex tasks.** If the task isn't trivial, surface ambiguities before starting. Five "obvious" questions answered beats one wrong assumption landing in a PR.
- **Use plan mode before complex tasks.** For anything beyond a one-line edit, write the plan first, get alignment, then execute.
- **Make minimal changes.** Don't refactor unrelated code. Stay in the lane the task asked for; flag anything else as a follow-up rather than folding it in.
- **Run tests after every change, fix failures before moving on.** Don't pile change on top of a broken state.
- **Atomic commits.** For documentation changes (`.md`, `.txt`, `.csv`, etc.) — one commit per file. For code changes that span multiple files but represent one logical change — one commit per logical change. Either way, no giant catch-all commits.
- **PRs are batched commits, reviewed as a whole.** A PR collects related work into a reviewable unit. **Ask before opening a PR** — don't open one autonomously, even if you think the work is done.
- **When unsure between two approaches, explain both and let the human choose.** Don't silently pick. Lay out the tradeoffs.

## Quick orientation

| Path | What it is |
| --- | --- |
| `profile/README.md` | Public landing page rendered at github.com/Primal-Bee. |
| `CONTRIBUTING.md` | Org-wide rules; auto-served as the fallback `CONTRIBUTING.md` to every repo in the org. |
| `PULL_REQUEST_TEMPLATE.md` | Auto-applied to every PR opened in any Primal-Bee repo. |
| `repo-skeleton/` | Starter docs (`README`, `CLAUDE`, `CONTRIBUTING`, `TODO`, `LEARNINGS`) plus `LICENSE-PROPRIETARY`, hand-copied into new repos. |
| `LICENSE` | All rights reserved. Repo is public-visible for transparency; not open source. |

## Need help?

If you're unsure whether a change is safe — especially anything that's inherited org-wide — stop and ask. The cost of pausing is near-zero; the cost of a wrong assumption ripples across every repo in the org.
