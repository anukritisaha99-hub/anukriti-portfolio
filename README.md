# Anukriti Saha — Portfolio

A horizontal-scroll rebuild of the portfolio, matching the original Canva site's
look (dark charcoal background, Helvetica Neue, holographic 3D icons, pill-shaped
tags) with:

- A cleaner fixed nav (About / What I Do / Skills / Certifications / Contact)
  with an active-section indicator
- Horizontal scroll-snap navigation instead of long vertical scrolling —
  scroll, swipe, use the on-screen arrows, the side dots, or the arrow keys
- A new **Skills** section with a two-row running marquee of tool logos
- A new **Certifications** section

## File structure

```
index.html
css/style.css
js/main.js
assets/          ← all images, gifs, and videos
```

Everything is plain HTML/CSS/JS — no build step, no dependencies.

## Deploying to GitHub Pages

1. Create a new repository on GitHub (e.g. `anukriti-portfolio`).
2. Upload/push these files to the repo root (keep the folder structure as-is).
   From the command line, inside this folder:
   ```bash
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. On GitHub: go to the repo → **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`,
   branch `main`, folder `/ (root)`. Save.
5. GitHub will publish the site at:
   `https://<your-username>.github.io/<repo-name>/`
   (takes 1–2 minutes to go live after the first push).

## Editing content later

- **Text** — edit directly inside `index.html`; each section is clearly
  commented (`<!-- HERO -->`, `<!-- ABOUT -->`, etc).
- **Skills marquee logos** — edit the `SKILLS` array at the top of
  `js/main.js`. Real logos use `path` (SVG path data); anything without a
  vector mark on hand falls back to a two-letter `mono` badge.
- **Certifications** — duplicate a `<article class="cert-card">` block in the
  Certifications section of `index.html`.
- **Colors** — all tokens (background, accent purple, text colors) are CSS
  variables at the top of `css/style.css` under `:root`.
