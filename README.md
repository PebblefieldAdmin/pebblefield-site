# Pebblefield website

The public pages for the Pebblefield app: home and support (`index.html`) and the privacy policy (`privacy.html`).
Published with GitHub Pages. The game itself lives in a separate, private repository.

The site matches the launch version, **1.0.1 (iPhone build 28, game commit `b03b3b4`; Android the same code)**, updated
2026-10-12: five ways to play (with Scene of the Day and Photo Puzzle), support for iPhone and Android, and a privacy
policy covering Photo Puzzle, Android and the Android Blitz leaderboard (`privacy.html#delete` is the data-deletion
link for Google Play).

Images: `shots/` holds eight real game screens (WebP, 600 x 1300): 1 painting, 2 the five ways to play, 3 rescue,
4 Pebble Dash, 5 Blitz, 6 style sets (from the game's `store/raw` captures for v1.0), 7 Scene of the Day and 8 Photo
Puzzle (captured from build 28's code on 2026-10-12; the photo is a drawn stand-in, not a real one), and
`scenes/` the 25 painting scenes as 48 x 48 pixel art, exported from the game; both are shown on the home page.

## Launch week (`launch.json`)

The game reads `launch.json` from this site to know when Launch week runs: `{ "start":"YYYY-MM-DD" }` (the release
date, Singapore time). It runs to the last day of that month (or an optional `"end"`); players who start late still
get 7 days, and from the 1st of the next month nobody new can start it. It is **not published yet**: add it on (or before) release day with the release date. Without the
file, or before its start date, the game shows nothing.
