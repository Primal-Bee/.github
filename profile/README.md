# Primal Bee

Welcome. We build the thermodynamically-engineered Primal Bee hive at [primalbee.com](https://primalbee.com), plus the internal tools and content we use to run the operation. This GitHub org is where all of that lives.

If you're reading this, you probably just got added to the org. Here's how to find your feet.

## If you're new here

1. **Start with [`CONTRIBUTING.md`](https://github.com/Primal-Bee/.github/blob/main/CONTRIBUTING.md)** in this repo. It's the few rules that apply to every Primal Bee repo. About five minutes of reading.
2. **Then click into whichever repo you'll be working in** and open its `CLAUDE.md`. Each repo has its own quirks, hard rules, and gotchas — they're all in there. If you use Claude Code, it auto-loads CLAUDE.md when you open the repo, so you don't have to remember to read it.
3. **Stuck?** Ask. Better than reading docs in circles.

## Setting up Claude Code (non-technical)

If you're not used to terminals and you just need to get the Primal Bee tools into Claude Code on your computer, follow the install steps in [`primalbee-internal-tools`](https://github.com/Primal-Bee/primalbee-internal-tools#install). Should take about a minute.

## Cloning a repo onto your computer

Easiest path — open Claude Code and ask it in plain English:

> *"Clone primalbee-kb."*

Claude handles auth, drops the repo in `~/projects/<repo-name>/`, and opens it for you. No git commands to remember. Swap `primalbee-kb` for whichever repo you want.

If you'd rather run it yourself in the terminal:

```bash
gh repo clone Primal-Bee/primalbee-kb ~/projects/primalbee-kb
```

Needs the [GitHub CLI](https://cli.github.com) — `brew install gh && gh auth login` if you don't have it yet. Then open the folder in your editor and you're set; each repo's `CLAUDE.md` auto-loads when Claude Code opens it.

## When to make a new repo

**Default to one repo per stack piece.** Each agent, each skill, each distinct surface area gets its own repo — `primalbee-website` and `primalbee-shopify-blog` are two separate sections of the site, so they're two repos. Same logic for skills: a skill that's substantial enough to evolve on its own (its own SKILL.md, its own scripts, its own learnings) belongs in its own repo, not bundled inside another. Small repos are easier to read, easier to grant access to selectively, and let each piece carry its own `CLAUDE.md` / `TODO.md` / `LEARNINGS.md` without competing.

If you're unsure, err toward a new repo. Splitting later is harder than starting clean.

## Starting a new repo here

When you spin up a new repo in this org, follow this walkthrough. It keeps things consistent across the org so the next person to land in your repo recognises the layout.

### 1. Make it private

Every repo in this org is **private**. No exceptions without explicit org-owner approval — we don't ship anything customer-facing through GitHub directly. When you click *New repository*, set visibility to Private.

### 2. Name it clearly

Use kebab-case (lowercase, hyphens). If it's a Primal Bee product surface or something customers might one day see, prefix with `primalbee-` (`primalbee-blog-publisher`, `primalbee-brand-guide`). For internal tooling, bare names are fine (`accounting`, `customer-service-kb`).

### 3. Write a clear "About"

GitHub asks for a description right under the repo name on the New Repository page. **Fill it in.** One short sentence that says what the repo *is* — that's the line people see when scrolling the org repo list trying to find the right one.

Good examples (already in the wild):

- *"Primal Bee brand system (visual + messaging) — distributed as a Claude Code plugin via primalbee-internal-tools"*
- *"Org-level conventions, PR template, and starter scaffold for new Primal-Bee repos"*

Bad: empty (the default). When most repos in the org have no description, the org page reads as a wall of names with no signal — the eye glazes over and people pick the wrong one.

If you forgot during creation, you can fix it from the repo's main page: click the ⚙ icon next to **About** in the right sidebar, type the description, save. Takes ten seconds.

### 4. Copy the scaffold

This `.github` repo ships a starter folder at [`repo-skeleton/`](https://github.com/Primal-Bee/.github/tree/main/repo-skeleton). Copy its contents into your new repo's root and replace the `{{placeholders}}` (repo name, one-line description). Five tiny files:

- `README.md` — what the repo is, in two or three lines.
- `CLAUDE.md` — the project context Claude Code auto-loads. Hard rules, dispatcher to the other docs.
- `CONTRIBUTING.md` — the repo-specific layer. Top-line points at the org-wide rules; the rest is yours.
- `TODO.md` — pending work, deferred decisions, done log.
- `LEARNINGS.md` — non-obvious gotchas you've discovered.

The placeholders walk you through what each section is for. None of these need to be perfect on day one — they grow with the repo.

### 5. First commit, first PR

Push the scaffold to `main`. Then branch off, fill in your repo-specific content, open a PR against `main`, merge. From here on every change goes through a PR — see [`CONTRIBUTING.md`](https://github.com/Primal-Bee/.github/blob/main/CONTRIBUTING.md).

### 6. Pre-commit hook (optional but recommended)

If your repo will ship plugin manifests, schema files, version-locked tooling, or anything else where two files have to agree on the same value, drop a `.githooks/pre-commit` plus a small Python or shell script that checks the invariant. The existing plugin repos (`primalbee-internal-tools`, `primalbee-shopify-blog`, `primalbee-brand-guide`) all have working examples — copy and adapt.

## Help

Ask the engineering channel. New to the team? Ask whoever onboarded you — that's faster than figuring it out alone.

All new repos are private. So is anything sensitive that ends up in them.
