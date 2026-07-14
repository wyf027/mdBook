---
name: single-file-front-end-template-fix
description: Workflow command scaffold for single-file-front-end-template-fix in mdBook.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /single-file-front-end-template-fix

Use this workflow when working on **single-file-front-end-template-fix** in `mdBook`.

## Goal

Make a targeted fix or improvement to the front-end template for the table of contents (TOC).

## Common Files

- `crates/mdbook-html/front-end/templates/toc.js.hbs`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit crates/mdbook-html/front-end/templates/toc.js.hbs to fix or improve TOC behavior.
- Commit the change, sometimes with a brief message.
- Optionally merge via pull request.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.