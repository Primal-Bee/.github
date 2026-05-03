# Contributing — {{repo-name}}

> **Org-wide rules:** [`Primal-Bee/.github/CONTRIBUTING.md`](https://github.com/Primal-Bee/.github/blob/main/CONTRIBUTING.md). PR template: [`.github/PULL_REQUEST_TEMPLATE.md`](https://github.com/Primal-Bee/.github/blob/main/PULL_REQUEST_TEMPLATE.md). This file covers what's specific to {{repo-name}}.

Read `CLAUDE.md` first for the architectural picture and the safety rules. This file is the operational reference for actually making changes.

## Setup (per clone)

<!-- What does someone need to do once after cloning this repo to be able
     to work in it? Examples from other repos: install deps via uv sync,
     authenticate the Shopify CLI, set OPENAI_API_KEY in .env, run
     git config core.hooksPath .githooks. Be concrete and step-by-step. -->

1. {{step}}
2. {{step}}

<!-- If your repo has a pre-commit hook, mention it here so contributors
     remember to enable it: -->
<!--
3. Enable the pre-commit hook (once per clone):
   ```
   git config core.hooksPath .githooks
   ```
   The hook checks {{what it checks}}; if it fails, {{what to do}}.
-->

## Workflow

<!-- The day-to-day flow of working in this repo. Examples: how to author
     and publish a new blog article; how to add a reference image to the
     brand bundle; how to bump a plugin pin. Whatever the most common
     contributor activity is, document it here as a numbered walkthrough.
     If your repo only has one common workflow, just describe that one. -->

{{Step-by-step description of the most common contributor workflow.}}

## Bumping a version

<!-- Delete this whole section if your repo doesn't ship versioned
     releases. Otherwise: which files carry the version, what bump levels
     mean (patch / minor / major), how the release flow works (tag,
     update the registry pin in primalbee-internal-tools if it's a
     plugin, etc.). -->

{{If applicable: walk through the version-bump flow. Include: which
files agree on the version, what semver rules apply, how to tag and
push.}}

## What NOT to change without coordination

<!-- The "I'm about to do something with downstream effects — should I
     ask first?" list. Examples: renaming the plugin, changing a slash
     command name, moving a file the SKILL.md references, changing the
     marketplace pin URL. Things that are technically possible but would
     break worker installs or cross-repo contracts. -->

{{Bullet list of stable contracts other systems depend on. If you'd want
to give someone a heads-up before changing something, list it here.}}

## Help

Ask {{channel or person}}. Stuck > guessing.
