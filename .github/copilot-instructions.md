# Copilot Instructions

## Project Overview

This is the personal academic website for Alexander C. Furnas, hosted via GitHub Pages at [alexanderfurnas.com](https://alexanderfurnas.com). It is a static site — no build step, no framework, no JavaScript. All pages are hand-authored HTML and a single shared CSS file.

## Architecture

- **Pages**: `index.html` (About/bio), `research.html`, `teaching.html`, `writing.html`, `service.html` — each is a standalone HTML file with its own `<head>`, nav, and footer.
- **Styling**: `style.css` is the single stylesheet shared across all pages. It uses CSS custom properties defined in `:root` for theming (colors, spacing, max-width).
- **Hosting**: Deployed from the repo root to GitHub Pages. `CNAME` maps to `alexanderfurnas.com`.
- **No build/test/lint tooling exists.** Changes are made directly to HTML/CSS and pushed.

## Key Conventions

- **Nav is duplicated** in every HTML page. The `class="active"` attribute must be set on the correct nav link for the current page. When editing navigation, update all five HTML files.
- **Design tokens**: Colors (`--accent: #b35c3a`), layout (`--max-width: 740px`), and spacing are all controlled via CSS custom properties in `:root`. Use these variables rather than hard-coding values.
- **Font**: Inter (loaded from Google Fonts) with system font fallback stack.
- **Publication entries** use a consistent structure: `.pub-item` containing `.pub-title`, `.pub-authors`, `.pub-venue`, and optional `.pub-note`, `.pub-award`, `.pub-status`. Highlighted publications get the `.highlight` class. Expandable abstracts use `<details class="pub-abstract">`.
- **Generic list items** (teaching, service, writing pages) use `.item` with `.item-year`, `.item-title`, `.item-detail`.
- **Mobile nav** is a CSS-only hamburger menu using a hidden checkbox toggle (`#nav-toggle`). No JavaScript is involved.
- **Open Graph / Twitter meta tags** are included in every page's `<head>` for social sharing. Keep these in sync when adding or changing pages.
