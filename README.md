# TURBO BOUNTY

A single-file 3D arcade racing + combat game built with [Three.js](https://threejs.org/) — **no build step, no asset files, one `index.html`.**

> Lead the race, become the target. The car in 1st grows a bounty and everyone hunts it. Get wrecked and your **ghost** gets 5 seconds of revenge.

## Play

- **WASD / Arrows** — drive
- **Space** — shoot (twin guns, watch the overheat bar)
- **Shift** — use pickup (homing rocket · mine · shield)
- **C** — handbrake drift
- **T** — trailer mode (extra pickups + aggression, for recording clips)
- **Esc** pause · **M** mute

Pick a location on the **track-select** screen: Lagos (Third Mainland Bridge), Tokyo neon streets, Dubai desert, Iceland volcano road, Swiss Alps, or Random.

## Run locally

Any static server works (ES-module importmaps need `http://`, not `file://`):

```bash
npx serve
# or
python -m http.server
```

Then open the printed URL.

## Deploy

It's a static site — deploy the folder as-is to Vercel, Netlify, or GitHub Pages. On Vercel: import the repo, no framework preset, no build command, output = project root.

## Tech / performance

- Three.js `0.160.0` via importmap (unpkg). Optional post-processing (bloom, FXAA), reflections (PMREM) and rounded-box car geometry load with graceful fallbacks.
- All visuals are **procedural** (canvas textures, instanced props) — no external/CC0 assets, so nothing to license or attribute.
- A `QUALITY` block at the top of the script controls shadows, bloom, resolution, etc. The renderer **adapts resolution automatically** to keep the framerate smooth.

## Licence

MIT — do whatever you like.
