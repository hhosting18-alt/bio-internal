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

Below the hero and the engine panel, the same character travels down the page as you scroll.
On load (and on resize) the page scans its own layout for empty space: anything with text,
images, cards or buttons is avoided. The character only rests in those empty spots, and leaps with
a spin to the next one as you scroll. No markup is needed: change the layout and the spots update.

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
