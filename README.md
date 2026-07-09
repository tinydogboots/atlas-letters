# Atlas Letters

Typography spliced from imagery of a real place — Google Street View and satellite tiles get thresholded, cut into a grid, and rearranged into letterforms. Live-tweakable in the browser.

Live: https://tinydogboots.github.io/atlas-letters/

## Use

1. Get a Google Maps API key at [console.cloud.google.com/google/maps-apis](https://console.cloud.google.com/google/maps-apis)
2. Enable **Maps Static**, **Street View Static**, and **Geocoding** APIs
3. Paste the key into the Imagery panel (kept in your browser's localStorage only)
4. Type a city or `lat,lng` in the Location panel and hit **Fetch imagery**
5. Play with Typography, Tiling, and Threshold — everything updates live
6. **Save PNG** when it looks right

No API key? Drop any image onto the canvas or use **Upload files** — the whole splice pipeline runs on your own imagery too.

## Splice modes

- **Slice** — one primary image gets cut along the letter grid; the composition preserves the image's own geometry
- **Mosaic** — each tile is a fragment of a random photo from the pool; the place is experienced through disjoint pieces

## Tech

Single self-contained HTML file. No build step. Vanilla JS, canvas 2D, no dependencies. Threshold is a CSS filter chain baked into the canvas via `ctx.filter`.
