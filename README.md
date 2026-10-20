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
get 7 days, and from the 1st of the next month nobody new can start it. **Published 2026-10-20** (the iPhone release day): `{ "start":"2026-10-20" }`, so Launch week
runs to 31 October and Scene of the Day counts its Day 1 from that date. Without the file, or before its start date,
the game shows nothing.

## Download (since 2026-10-20)

Live on the App Store (https://apps.apple.com/app/id6817978780) since 2026-10-20; Google Play to follow. The home page
has the download button (and Safari on iPhone shows Apple's App Store banner, from the `apple-itunes-app` meta tag).

`get.html?c=<campaign>` is the one link for ads and bios: iPhone and iPad go straight to the App Store, Android to
Google Play once `PLAY_LIVE` is true (until then, the home page), anything else to the home page. `PT` holds Apple's
provider token (129540917, from App Store Connect > Analytics > Acquisition > Campaigns), so App Store downloads are
counted per campaign (the `c` name, letters, digits, - and _ only). When Google Play goes live: set `PLAY_LIVE = true` and swap "Google Play: coming soon" on the home
page for a Google Play button.

## app-ads.txt

AdMob reads it at the root of the developer website's domain: https://pebblefieldadmin.github.io/app-ads.txt (the
`PebblefieldAdmin.github.io` repository, published 2026-10-01). A copy sits here too (added 2026-10-20, as a
precaution); the root one is the one that counts. Both hold the one line AdMob gives in its setup instructions.
