# John Harrington: portfolio site

A single static page: plain HTML and CSS plus about 1 KB of JavaScript. There's no build step and no frameworks, it loads no third-party scripts, fonts, or trackers, and it's ready for GitHub Pages.

## Contents

```text
index.html                 the page (hero, about, expertise, experience, projects, certifications, contact)
styles.css                 all styles (dark theme, responsive, prefers-reduced-motion, print styles)
script.js                  mobile menu toggle + footer year (the page works without it)
John_Harrington_Resume.pdf resume linked from the Download buttons
assets/favicon.svg         JH monogram favicon
assets/og-image.png        1200x630 social preview image (Open Graph / Twitter card)
assets/*.webp, *.jpg       project screenshots (WebP with JPEG fallback), generated from synthetic sample data
.nojekyll                  tells GitHub Pages to serve files as-is
robots.txt
```

First load is about 125 KB: HTML, CSS, JS, favicon, and two WebP screenshots, which are lazy-loaded. The page scored 0 violations in an axe-core WCAG 2.1 AA + best-practice audit at 1440 px and 390 px widths.

## Preview locally

```bash
cd site
python3 -m http.server 8000
# open http://localhost:8000
```

## Deployment

Live at **https://john-harrington-it.github.io/**, served by GitHub Pages from the `main` branch root of [`john-harrington-it/john-harrington-it.github.io`](https://github.com/john-harrington-it/john-harrington-it.github.io). Pushing to `main` redeploys the site within a minute or two.

The resume PDF published here is a copy of the all-purpose resume with the phone number removed. Contact is by email or LinkedIn.

Project links point to the three PowerShell repos:

- [ad-hygiene-toolkit](https://github.com/john-harrington-it/ad-hygiene-toolkit)
- [exchange-hybrid-healthcheck](https://github.com/john-harrington-it/exchange-hybrid-healthcheck)
- [m365-user-lifecycle](https://github.com/john-harrington-it/m365-user-lifecycle)

## Editing

- Content is all in `index.html`, one commented block per section.
- Colors are CSS variables at the top of `styles.css` (`--accent`, `--accent-2`, `--bg`, ...).
- Project screenshots were generated from synthetic sample data and converted to WebP/JPEG.
