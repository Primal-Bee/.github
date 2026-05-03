# Contributing to Primal Bee repos

A few rules that apply to every repo in this org. Each repo has its own `CONTRIBUTING.md` that adds repo-specific stuff (setup, version-bumping, etc.) — read that next.

If you're brand new, skim this whole page first. Five minutes. Then click into whichever repo you'll work in and read its own `CLAUDE.md` — that's where the hard rules and architectural picture for that repo live.

## How changes land

**Every change reaches `main` via a squash-merged PR.** Branch off `main`, commit as many times as you want, push, decide when it's time, open a PR, someone merges.

## Branch names

Pick a prefix that matches what you're doing, then a short slug:

| Prefix | For | Example |
| --- | --- | --- |
| `feat/` | A new feature or new content | `feat/inline-image-generation` |
| `fix/` | A bug fix | `fix/varroa-tray-typo` |
| `chore/` | Maintenance, refactors, dependency bumps | `chore/bump-deps` |
| `docs/` | Documentation only | `docs/clarify-bumping-flow` |
| `edit/` | Content edits in content repos | `edit/200-years-of-the-beehive` |

If your change doesn't fit one cleanly, pick the closest. Don't overthink it.

## PR descriptions

Every PR auto-fills with the org-level template — you'll see it the moment you click "Create pull request." Fill in the sections; don't replace it with free-form prose. The template covers what reviewers actually need (Summary / Why / What changed / Docs touched / Test plan).

If you've got something the template doesn't fit, expand a section, don't delete it. And if a section genuinely doesn't apply, say so in one short line — empty sections are fine, vanished sections aren't.

## Merging

- **Squash-and-merge** is the default merge style. Keeps `main`'s history readable.
- **Repo owners can self-merge their own PRs** once the PR template is filled in, the pre-commit hook has passed locally, and any required CI checks are green. No "stamp from a colleague" required for routine work on your own repo — but use judgment: structural changes still benefit from a second pair of eyes.
- **Non-owners need an owner's review** before merging.
- **AI agents don't self-merge.** If you're using Claude Code or another AI agent to make changes on your behalf, the agent **opens the PR and stops there** — it shares the PR URL and waits for you to merge yourself. The self-merge rule above is for humans on their own routine work; an AI doesn't get to decide a change is "routine enough" to ship without your eyes on the GitHub diff. Tell the agent "merge it" explicitly when you're ready, and only for the specific PR you mean.

If you're not sure whether you're an "owner" of a repo, ask. Usually it's whoever maintains it day to day.

## Pre-commit hooks

Some repos use git pre-commit hooks for things like version-drift checks. If a repo has a `.githooks/` folder, run this once after cloning:

```
git config core.hooksPath .githooks
```

Then commits run the checks automatically. The repo's own `CONTRIBUTING.md` will tell you what the hook is checking for and what to do if it fails.

## Where the rest of the rules live

- **Each repo's `CLAUDE.md`** carries safety rules, what the repo does, and the architectural picture. **Read this first** when you open a repo. Claude Code auto-loads it; if you're not using Claude Code, just open the file.
- **Each repo's `CONTRIBUTING.md`** carries the workflow specifics — how to set the repo up, how to bump a version, what NOT to change without coordination.
- **Each repo's `LEARNINGS.md`** carries the non-obvious gotchas — things that cost real debugging time, documented so the next person doesn't relearn them.

## Stuck?

Ask. Way better than re-reading these docs in circles or guessing. The team would rather answer five "obvious" questions than have one wrong assumption land on `main`.
