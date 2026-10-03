# Pebblefield website

The public pages for the Pebblefield app: home and support (`index.html`) and the privacy policy (`privacy.html`).
Published with GitHub Pages. The game itself lives in a separate, private repository.

Images: `shots/` holds six real game screens (WebP, made from the game repository's `store/raw` captures: painting, home screen, rescue, Pebble Dash, Blitz, style sets; updated 2026-10-03 for v1.0) and
`scenes/` the 25 painting scenes as 48 x 48 pixel art, exported from the game; both are shown on the home page.

## Launch week (`launch.json`)

The game reads `launch.json` from this site to know when Launch week runs: `{ "start":"YYYY-MM-DD" }` (the release
date, Singapore time). It runs to the last day of that month (or an optional `"end"`); players who start late still
get 7 days, and from the 1st of the next month nobody new can start it. It is **not published yet**: add it on (or before) release day with the release date. Without the
file, or before its start date, the game shows nothing.
