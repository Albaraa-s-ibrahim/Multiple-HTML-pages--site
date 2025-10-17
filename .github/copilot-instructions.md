This repository is a small static multi-page HTML site. The instructions below help an AI coding agent make productive, safe, and repository-appropriate changes.

Purpose
- Keep changes minimal and focused: this project contains static HTML/CSS (and possibly multiple pages). Avoid introducing heavy build tools or dependencies unless the user asks.

What I need to know about the codebase
- Single-page files: the repo currently contains `index.html` (root). Use that as the canonical example when adding pages or updating markup.
- Styling: `index.html` links to `styles.css` (expected at the repo root). If editing styles, prefer adding or editing `styles.css` rather than adding inline styles unless the change is small and component-scoped.

Editing rules
- Preserve whitespace, indentation and existing HTML semantics. This project appears to use simple, flat HTML — avoid introducing frameworks (React/Vue/etc.).
- When adding new pages, ensure they are linked from `index.html` (use relative URLs) and that `<head>` metadata (charset, viewport, title) follows the pattern in `index.html`.
- If you add scripts, prefer creating a `scripts/` folder and reference them with relative paths. Keep JS unobtrusive — avoid transpilers/build steps.

Examples (use these as templates)
- Creating a new page: copy `index.html` -> `about.html`, update `<title>` and link back to `index.html` in the navigation. Add page-specific CSS rules to `styles.css` under a clear comment block.
- Small markup fix: if fixing broken tags, keep the DOCTYPE and `<html lang="en">` intact; follow the meta order: charset, viewport, title, then styles.

Project-specific conventions
- Files live at repository root (flat structure). When adding folders, keep them shallow (e.g., `images/`, `scripts/`, `styles/`) and update any relative links accordingly.
- Use relative paths (no absolute URLs) for internal links so the site remains portable when opened locally.

Testing and verification
- Manual verification: instruct humans to open the edited HTML files in a browser (double-click or `file://` path) to check layout and links.
- Automated checks: none present. Do not add CI or build unless requested.

When to ask the user before proceeding
- Adding a build system (npm, webpack, parcel, etc.).
- Introducing server-side code or external hosting config.
- Large structural refactors that change link paths or file layout.

Safety and privacy
- Do not add telemetry, analytics, or third-party trackers without explicit consent.

If you modify `index.html` specifically
- Keep the existing head meta tags order and the linked `styles.css` reference.
- Fix truncated or malformed tags carefully (preserve encoding and `lang` attribute).

Helpful files to reference
- `index.html` — the canonical page and markup style to follow.

If anything here is unclear or you want more detailed guidance (for example adding CSS organization rules or a small local dev server), ask and I'll refine these instructions.
