# Rajesh_Agarwal_Sample

Portfolio site for Rajesh Kumar Agrawal (Structural Integrity & Architectural Engineering).

## Deploy on Vercel

- Push to `main`; then in [Vercel](https://vercel.com) import this repo and deploy (no env or build settings needed).
- Or: install [Vercel CLI](https://vercel.com/cli) and run `vercel` in the project root.

## Run locally

```bash
# From project root
python3 -m http.server 8080
```

Then open [http://localhost:8080](http://localhost:8080).

Or with Node (if you have `npx`):

```bash
npx serve -l 8080
```

## Stack

- Single HTML file with Tailwind CSS (CDN), Google Fonts (Space Grotesk, DM Mono, Material Symbols).
- No build step; open `index.html` in a browser or serve via any static server.

## Optimizations and fixes

- Hero ref/subtitle/block/scroll visibility driven by CSS (`.js-enabled` / `.loaded`) instead of invalid Tailwind classes.
- Responsive grid: single column on small screens, 12-column on large; sections use `col-span-12` with `lg:` overrides for alignment.
- SVG map pins use `<text>` instead of `<foreignObject>` for better cross-browser support.
- Timeline reveal items start with `opacity: 0` and are shown via JS when the career section is visible.
- Count-up animation: suffix `+` only applied when target is reached (12+, 50+).
- Nav rail active state updates when hero is in view (IntersectionObserver).
- Reduced motion respected via `@media (prefers-reduced-motion: reduce)`.
- Footer and contact section layout adjusted for small screens; table scrolls horizontally on narrow viewports.
- Minor accessibility: `aria-label` on nav, `aria-hidden` where appropriate, semantic button type.
