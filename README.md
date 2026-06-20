# Eponym — Website

This repository is the standalone **Eponym website / landing page** repository. It is the
canonical home for the public Eponym landing page and is served directly via GitHub Pages
from this repository's root. It is **not** the `gh-pages` branch of the Eponym application
repository — the page now lives on its own here.

## What this is

- A single hand-authored `index.html` with all CSS and JS inline.
- An editorial / digital-magazine presentation that simulates several classic Eponym
  layout motifs: hero magazine cover, scatter→unify feature spread, three-column
  editorial, brand showcase with stacked covers, table-of-contents index, page-turn
  reading tabs, longread pull quote, and an ending-spread CTA.
- No build system, no npm dependencies, no external images, and no copied ELL SDK code
  or assets — it is an *inspired-by* simulation, not a reuse of the real layouts.
- The only external request is to Google Fonts (Noto Sans TC / Noto Serif TC), loaded
  for reliable Traditional Chinese rendering.

## Files

| File         | Purpose                                          |
|--------------|--------------------------------------------------|
| `index.html` | The entire landing page (HTML + inline CSS/JS).  |
| `.nojekyll`  | Tells GitHub Pages to serve files as-is.         |
| `README.md`  | This file.                                       |

## CTAs

Calls to action link to:

```
https://dev.eponym.online/
```

Edit that URL in `index.html` if the login path changes.

## Accessibility & behavior

- Semantic landmark sections, skip link, visible keyboard focus, ARIA tabs with
  arrow/Home/End key support.
- Responsive from mobile to desktop.
- Respects `prefers-reduced-motion` (animations and smooth scroll are disabled).
- The only external request is to Google Fonts; no other network calls and no console
  errors.

## Preview locally

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deployment

The static site is live at https://jacobleegithub.github.io/eponym-website/.

It is served via GitHub Pages from the **Settings → Pages** configuration:

- **Source:** Deploy from a branch
- **Branch:** `gh-pages`
- **Folder:** `/` (root)

`main` remains the source branch; the `gh-pages` branch mirrors `main` for GitHub Pages
publishing. `.nojekyll` ensures files are served as-is.
