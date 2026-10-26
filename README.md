# Mask_In (Web)

Mask_In is a static storefront landing page for buying face masks and related cloth items. It presents a mask shop's collections in a single page, with a branded header, a decorative hero section and a collections grid.

## What it does

- **Navbar** — Mask_In logo with Home, Latest Collection and Login links (these links are placeholders and do not lead anywhere yet).
- **Hero** — A "Design is the trend" headline over decorative inline SVG artwork, with a separate layout for small screens.
- **Our Collections** — A grid of mask categories, each with its own SVG illustration: Classic Mask, Pattern Mask, Surgical Mask, N95 Mask, Neck Fleece and Bandanna Cloth. Desktop and mobile versions of the section are marked up separately.
- **Favicon** — Uses `medical-mask.png` as the page icon.

## Tech stack

- Plain HTML and CSS, with SCSS sources in `scss/` and compiled output in `css/` (the page loads `/css/app.css`)
- Bootstrap 5 (beta) and Popper.js via CDN, plus the Baloo 2 font from Google Fonts
- Inline SVG artwork throughout the page (no image files for the collection icons)
- `index.php` includes `index.html`, so the same page can be served from PHP hosting
- A `Procfile` is present for Heroku-style deployment

## How to run

The site is a static page, so the simplest way to view it is to serve the folder and open `index.html`:

```bash
npx serve .
```

Note: `package.json` still carries create-react-app style scripts (`dev`, `build`, `start`, `heroku-postbuild`) that reference react-scripts, but there is no React app in this repository — the site itself is the static `index.html` page, so those scripts do not apply to it.

## Project structure

```
.
├── index.html        # The whole storefront page
├── index.php         # Includes index.html (for PHP hosting)
├── Procfile          # Heroku-style process file
├── css/              # Compiled stylesheets (app.css)
├── scss/             # SCSS sources
├── medical-mask.png  # Favicon image
└── package.json      # Bootstrap/live-server deps (see note above)
```

## Status

A front-end landing page from 2021. There is no cart, checkout, login backend or product data behind it — the navigation links are placeholders, so the next step for a real shop would be product pages and a checkout flow.
