# Learnings — {{repo-name}}

Non-obvious things we've discovered. Read before editing the parts of the repo where past gotchas have lived; future-you will thank past-you.

A "learning" worth writing down is something that:

- Cost real debugging time to figure out the first time.
- Isn't obvious from reading the code.
- Will bite the next person if they don't know it.

If a thing has those three traits, write it up. If it's just trivia, skip it.

## Format

For each learning, capture:

- **What you observed** (the symptom).
- **Why it happens** (the cause, once you understood it).
- **What to do** (the fix, or the rule for next time).

Keep entries short — a paragraph or two each. Long-form explanations belong in CLAUDE.md or in code comments. This file is the index to "stuff I wish I'd known."

## Example entry (delete this once you have real ones)

### Example: `articleCreate` always re-uploads images, even from a CDN URL

<!-- Replace this whole example with your first real learning. Keeping it
     here as a template until then. -->

**Observed:** Every duplicate-as-draft creates a new file in Shopify Files, even when the source URL is already on `cdn.shopify.com`.

**Why:** When you pass a `url` to `articleCreate`'s `image` field, Shopify fetches the URL and creates a fresh `MediaImage` from the bytes — there's no API to pass an existing `MediaImage` GID by reference at create time.

**What to do:** Accept the storage waste; the alternative (omitting the image input) breaks any custom `templateSuffix` whose template expects `article.image` to be populated. If a "GID-reference instead of URL" input ever ships, switch to it.
