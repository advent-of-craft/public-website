# Advent of Craft Public Website

This repository hosts the Advent of Craft public website as a static GitHub Pages hub.

GitHub Pages should serve the `docs/` directory. The root `CNAME` points the site to `adventofcraft.com`.

## Structure

```text
docs/
  index.html
  craft-monthly/
    index.html
  2024/
  2025/
  assets/
    css/
      style.css
```

The `2024/` and `2025/` folders under `docs/` are local archive copies served as `/2024/` and `/2025/`.

## Local Preview

Open `docs/index.html` directly in a browser, or run:

```powershell
python -m http.server 8000 -d docs
```

Then visit `http://localhost:8000`.

## Visible Test

Before publishing, verify these routes in a browser:

- `/`
- `/craft-monthly/`
- `/craft-monthly/#may-2026`
- `/2024/`
- `/2025/`

Check desktop and mobile widths, keyboard focus, image loading, and internal links.
