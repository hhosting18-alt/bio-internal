# Biomechanix landing page

Open `index.html` over http(s) (Vercel, GitHub Pages, or `python -m http.server` locally).
Opened straight from disk, the 3D character will not load.

## Structure
- `index.html` — the MoveMentor page: one engine, three apps (MoveMentor Fitness, MoveMentor Physio, Sameeksha).
  HTML, CSS and JS in one file. Each app section has a live pose-engine animation.
- `movementor-journey.html` — clickable app prototype (Personal area, Clinic area, Sameeksha hand-off),
  opened from the "Open the interactive journey" buttons. Sign-offs are saved in the visitor's browser
  and can be downloaded as CSV.
- `assets/models/diva_fluo.glb` — Diva character in the hero phone, rendered with Google's `<model-viewer>`
  (loaded from jsDelivr, pinned to 3.5.0). Drag to rotate.
- `assets/img/`, `assets/js/`, other `.glb` files — used by the previous page version; safe to keep or delete.

## Deploy to Vercel
No build step. Framework preset **Other**, Build command **empty**, Output directory **`.`**.
`vercel.json` sets the correct type for `.glb` models and light caching on `assets/`.
File names are case-sensitive on Vercel.

## Still to fill in before launch
1. **Google Play links** — the "Get it on Google Play" buttons have no link yet.
2. **Support and privacy policy pages** — footer "Support" and "Read the full privacy policy" use `href="#"`.

## Fonts
Archivo, Hanken Grotesk and Space Mono (main page); Bricolage Grotesque, Geist and Geist Mono (prototype), from Google Fonts.
