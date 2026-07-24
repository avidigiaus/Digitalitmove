# NovaTech — Multi-Page Site with 3D Scroll

A modern, dark-themed marketing site for a tech services company offering five practices: Data & Cloud, AI Agents, Digital Marketing, Training, and Cybersecurity.

## Quick start

```bash
cd site
python3 -m http.server 8000
# open http://localhost:8000
```

Or open `site/index.html` directly in a browser (the scripts are loaded from CDN, so the file:// protocol works for a quick preview).

## File structure

```
site/
├── index.html              ← Home
├── data-cloud.html         ← Data & Cloud Solutions
├── ai-agents.html          ← AI Agents & Workflows
├── digital-marketing.html  ← Digital Marketing
├── training.html           ← Training Services
├── cybersecurity.html      ← Cybersecurity
├── css/style.css           ← All styles (CSS variables, 3D transforms, responsive)
└── js/main.js              ← Lenis + GSAP ScrollTrigger engine
```

## What's in the 3D scroll engine

- **Lenis** — buttery-smooth scroll
- **GSAP + ScrollTrigger** — orchestrated entrance + parallax animations
- **CSS perspective + transforms** — 3D card tilts, depth-parallax, hero content tilts on scroll
- **Custom cursor follower** (desktop only) with hover states
- **Animated number counters** on scroll
- **Mouse-driven 3D tilt** on every service card
- **Rotating 3D showcase cube** that follows scroll position
- **Floating particles** around hero orbs and the cube
- **Word-by-word hero title reveal** on load
- **Scroll progress bar** at top

## Customizing

All design tokens live at the top of `css/style.css` as CSS variables — colors, gradients, easing curves. Change the brand by editing `--accent`, `--accent-2`, `--accent-3`, and the `--grad-1`/`--grad-2` definitions.

Service page content is hand-edited in each HTML file. Cards, sections, and CTAs follow consistent patterns — copy and remix as needed.

## Tech notes

- No build step. Drop the `site/` folder on any static host (Netlify, Vercel, S3, Cloudflare Pages, GitHub Pages).
- External libs loaded via CDN: GSAP 3.12, ScrollTrigger, Lenis 1.1.
- All assets are inline SVG / CSS — no image dependencies.
- Tested in modern Chrome / Firefox / Safari. Mobile responsive down to ~360px.
