# Rang

*"Wear the Art of India."*

A front-end e-commerce storefront for Indian ethnic wear — kurtis, anarkalis, sarees, and lehengas — with product browsing, search & sort, category filters, and a working shopping cart. Pure HTML, CSS, and JavaScript, deployable straight to GitHub Pages.

## Features

- **Product catalog** — kurti/anarkali/printed/cotton-kurti products with images, pricing, discounts, color swatches, ratings, and review counts
- **Category filters** — filter the grid by product category
- **Search & sort** — live text search plus sort by price (low–high, high–low) or biggest discount
- **Shopping cart** — add/remove items, adjust quantity, live running total, cart badge count
- **Responsive nav** — desktop nav + slide-out mobile menu
- **Toast notifications** — confirmation toast on "add to cart"

## Tech stack

- Plain HTML, CSS, and vanilla JavaScript — no framework, no build step, no backend
- Fonts: Playfair Display, DM Sans (Google Fonts)
- Product and cart state live entirely in `script.js` (in-memory — cart does not persist across page reloads)

## Project structure

```
index.html        # Page structure — nav, hero, search bar, product grid, cart drawer
style.css           # All styling
script.js             # Product data, cart logic, filtering/search/sort, UI rendering
img1.jpeg–img7.png     # Product images
.github/workflows/
  static.yml           # GitHub Actions workflow — deploys to GitHub Pages on push to main
```

## Running locally

No build step or dependencies required — open `index.html` directly in a browser, or serve the folder with any static file server:

```bash
npx serve .
```

## Deployment

This repo ships with a GitHub Actions workflow (`.github/workflows/static.yml`) that deploys the whole repository to **GitHub Pages** automatically on every push to `main`. Enable GitHub Pages for the repo (Settings → Pages → Source: GitHub Actions) and it will deploy on the next push.

## Notes

- All product data is hardcoded in `script.js` — there's no backend, database, or real checkout. "Add to cart" only updates the in-page cart drawer; there's no payment or order flow wired up yet.
- Nav links (New Arrivals, Kurtis, Sarees, Lehengas, Sale) currently point to `#` — hook these up to real category filters or pages when the catalog grows beyond the current product set.

## Project name

The site already brands itself **Rang** (हिंदी: *rang* = "color") in its title and nav logo — a fitting name for a colorful ethnic-wear storefront, and one I'd keep rather than the generic repo name `E-Commerce-GIRLS-OUTFIT`. If you want alternatives: **Aanchal**, **Rangrez**, or **Kurti & Co.** would all fit the same ethnic-wear-boutique feel.
