---
name: single-file-css-front-end-tweak
description: Workflow command scaffold for single-file-css-front-end-tweak in mdBook.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /single-file-css-front-end-tweak

Use this workflow when working on **single-file-css-front-end-tweak** in `mdBook`.

## Goal

Make a visual or spacing adjustment to the sidebar or chrome via CSS.

## Common Files

- `crates/mdbook-html/front-end/css/chrome.css`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit crates/mdbook-html/front-end/css/chrome.css to adjust styles.
- Commit the change, often referencing an issue or improvement.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.