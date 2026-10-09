# Biomechanix landing page

Open `index.html` in a browser (or upload the whole folder to any static host).

## Structure
- `index.html` — the full page (HTML, CSS and JS in one file)
- `assets/img/` — PLACEHOLDER photos, to be replaced before launch

## 3D athlete
The hero and the "how it works" tabs use a rigged 3D character: `assets/models/athlete.glb`
(a free three.js sample character, PLACEHOLDER). Swap in your own Mixamo character by
replacing that file with a `.glb` using the standard Mixamo skeleton (bone names `mixamorig:*`).
The 3D only loads over http(s) (Vercel, GitHub Pages, or `python3 -m http.server` locally).
Opened straight from disk, the page falls back to the flat 2D figure.

The character behaves like a companion that travels with the visitor. It sits in the places it works
(the hero and the "how it works" panel) and does its squat demo there. When you scroll away it gets up
and walks alongside you on screen, resting only in empty space (it measures every heading, paragraph,
button, image and card on the page and avoids them). If content scrolls under it, it moves to the nearest
free spot: walking if the way is clear, otherwise a quick fade-hop. If there's no free space on screen it
waits out of sight and comes back as soon as there is. No markup is needed: change the layout and it adapts.

## Deploy to Vercel
No build step. Either drag this folder into vercel.com/new, or run `vercel` inside it.
If asked: Framework preset **Other**, Build command **empty**, Output directory **`.`** (this folder).
`vercel.json` sets the correct type for the `.glb` model and light caching on `assets/`.
File names are case-sensitive on Vercel, so keep replacement images lowercase with the same names.

## Replace before going live
1. **3D character** — `assets/models/athlete.glb` (see above).
2. **Photos** — every file in `assets/img/` is a temporary placeholder.
   Keep the same file names and they drop straight in:
   hero-runner, path-training, path-rehab, path-self-assessment, path-enterprise,
   fitness-banner, physio-banner, sameeksha-banner, team-gaurav, team-raghunandan,
   partners-banner, footer-photo (.webp).
3. **App store links** — "Get it on Google Play" buttons currently use `href="#"`.
4. **Support / Privacy Policy links** — currently `#support` and `#privacy-policy`.

## Colours (from biomechanix.github.io)
Black #000000, near-black #0A0A0A, card #111111, lime #CCFF00, cyan #22D3EE,
text #F5F5F5, muted #A3A3A3. All defined as CSS variables at the top of index.html.

## Fonts
Inter Tight + JetBrains Mono, loaded from Google Fonts.
