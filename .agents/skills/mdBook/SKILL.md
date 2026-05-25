```markdown
# mdBook Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns, coding conventions, and release workflows for contributing to the mdBook project. mdBook is a documentation tool written in Rust, but its front-end assets are managed with TypeScript and JavaScript. This guide covers file organization, code style, commit habits, and the main workflows for maintaining and releasing mdBook.

## Coding Conventions

### File Naming
- **PascalCase** is used for file names.
  - Example: `TableOfContents.ts`, `SidebarMenu.ts`

### Import Style
- **Relative imports** are preferred.
  - Example:
    ```typescript
    import { SidebarMenu } from './SidebarMenu';
    ```

### Export Style
- **Named exports** are standard.
  - Example:
    ```typescript
    export function renderTOC() { ... }
    export const SIDEBAR_WIDTH = 250;
    ```

### Commit Patterns
- Commit messages are generally freeform, sometimes prefixed with `fix`.
- Average commit message length: ~38 characters.
  - Example: `fix sidebar spacing in chrome.css`

## Workflows

### Version Bump & Release
**Trigger:** When preparing a new release version of mdBook  
**Command:** `/bump-version`

1. Update the version number in all `Cargo.toml` files for each crate.
2. Update the root `Cargo.toml` and `Cargo.lock`.
3. Add release notes to `CHANGELOG.md`.
4. Commit and push the changes.
5. (Optional) Tag the release and publish crates.

**Files involved:**
- `CHANGELOG.md`
- `Cargo.lock`
- `Cargo.toml`
- `crates/mdbook-core/Cargo.toml`
- `crates/mdbook-driver/Cargo.toml`
- `crates/mdbook-html/Cargo.toml`
- `crates/mdbook-markdown/Cargo.toml`
- `crates/mdbook-preprocessor/Cargo.toml`
- `crates/mdbook-renderer/Cargo.toml`
- `crates/mdbook-summary/Cargo.toml`

### Single-file Front-end Template Fix
**Trigger:** When a bug or improvement is needed in the TOC JavaScript template  
**Command:** `/fix-toc-template`

1. Edit `crates/mdbook-html/front-end/templates/toc.js.hbs` to fix or improve TOC behavior.
2. Commit the change with a brief message.
3. (Optional) Open a pull request for review and merging.

**Example:**
```handlebars
// toc.js.hbs
{{!-- Fix event bubbling in TOC --}}
document.querySelector('.toc').addEventListener('click', function(event) {
  event.stopPropagation();
  // ...rest of handler
});
```

### Single-file CSS Front-end Tweak
**Trigger:** When a UI/UX improvement is needed for sidebar or chrome appearance  
**Command:** `/tweak-css`

1. Edit `crates/mdbook-html/front-end/css/chrome.css` to adjust styles.
2. Commit the change, referencing the related issue or improvement.

**Example:**
```css
/* chrome.css */
.sidebar {
  padding-left: 1.5em; /* Increased for better spacing */
}
```

## Testing Patterns

- **Test files** use the pattern `*.test.*` (e.g., `SidebarMenu.test.ts`).
- **Testing framework** is not explicitly detected; check project documentation or dependencies for specifics.
- Typical test example:
  ```typescript
  // SidebarMenu.test.ts
  import { SidebarMenu } from './SidebarMenu';

  test('renders menu', () => {
    // ...test implementation
  });
  ```

## Commands

| Command             | Purpose                                                      |
|---------------------|--------------------------------------------------------------|
| /bump-version       | Bump crate versions and update changelog for a new release   |
| /fix-toc-template   | Apply a fix or improvement to the TOC front-end template     |
| /tweak-css          | Make a visual or spacing tweak to sidebar/chrome CSS         |
```
