---
name: version-bump-release
description: Workflow command scaffold for version-bump-release in mdBook.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /version-bump-release

Use this workflow when working on **version-bump-release** in `mdBook`.

## Goal

Bump the version of mdBook and its crates, and update the changelog for a new release.

## Common Files

- `CHANGELOG.md`
- `Cargo.lock`
- `Cargo.toml`
- `crates/mdbook-core/Cargo.toml`
- `crates/mdbook-driver/Cargo.toml`
- `crates/mdbook-html/Cargo.toml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update the version number in Cargo.toml files for all crates.
- Update the root Cargo.toml and Cargo.lock.
- Update the CHANGELOG.md with release notes.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.