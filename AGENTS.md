# Repository Guidelines

## Project Structure & Module Organization

This repository hosts the Advent of Craft public website as a static GitHub Pages hub. The current planning source is `aoc-website-restructuring.md`; use this layout:

- `docs/index.html` for the homepage served by GitHub Pages.
- `docs/craft-monthly/index.html` for the Craft Monthly season page.
- `docs/2024/` and `docs/2025/` for locally served archive copies.
- `docs/assets/css/` for shared stylesheets.
- `docs/assets/img/` for logos, banners, and other image assets.
- `CNAME` at the repository root when deploying `adventofcraft.com`.

Root folders such as `2024/`, `2025/`, and `craft-monthly/` may contain source material. Keep generated files, IDE metadata, and local-only artifacts out of commits unless they are intentionally part of the site.

## Build, Test, and Development Commands

There is no build system, package manager, framework, or Jekyll setup planned. Work directly with plain HTML and CSS.

- Open `docs/index.html` in a browser to preview the homepage directly.
- Run `python -m http.server 8000 -d docs` to serve the site locally, then visit `http://localhost:8000`.
- Run `git status` before committing to verify only intended files are staged.

## Coding Style & Naming Conventions

Use semantic HTML, accessible landmarks, and responsive CSS. Prefer 2-space indentation in HTML and CSS. Use lowercase, hyphenated names for files and directories, for example `craft-monthly-banner.png` and `style.css`.

Keep shared CSS under `docs/assets/css/`. Avoid inline styles except for minimal page-specific exceptions. Keep the site dependency-free: no npm packages, CDN fonts, JavaScript frameworks, or build-only tooling unless the repository direction changes.

## Testing Guidelines

No automated tests exist yet. Before opening a pull request, manually verify pages in desktop and mobile viewport sizes. Check internal links, external links, image paths, and anchor links such as `#may-2026`.

Also verify basic accessibility concerns: heading order, alt text, keyboard focus states, and sufficient color contrast.

## Commit & Pull Request Guidelines

Git history currently only shows `Initial commit`, so no established commit convention exists. Use short, imperative commit subjects such as `Add Craft Monthly page` or `Update homepage tiles`.

Pull requests should include a concise description, screenshots for visual changes, linked issues or decisions, and manual verification notes. Call out deployment-impacting changes, especially edits to `CNAME`, GitHub Pages paths, or external calendar links.

## Security & Configuration Tips

Do not commit secrets, private contact data, analytics tokens, or unpublished event links. Keep deployment configuration simple and explicit, and document any domain or GitHub Pages changes in the pull request.
