# AGENTS.md

Single static page. The whole app is `index.html`. No package manager, bundler, tests, lint, or CI.

Tailwind via Play CDN in `index.html` (`cdn.tailwindcss.com`). No npm, PostCSS, or build. Do not add React or TypeScript unless asked. Trust `index.html` over README.

Preview by opening `index.html` in a browser. No install or build step. CDN is for local/dev; do not add a Tailwind CLI pipeline unless asked.

All wedding-specific content lives in the `INVITATION` object in `index.html`. Change copy, venue, and image paths there only — do not hardcode names, dates, or addresses in markup.

Images: files under `images/` only (`hero.jpg`, `gallery-1.jpg`, …), never the repo root. List them in `INVITATION.images`. Missing files show a fallback.

Music: files under `music/` (mp3, wav, ogg — browsers play mp3 fine). Path in `INVITATION.music.src` must match the real filename/extension. Empty `src` hides the player. Browsers start playback on the floating button, not on load.
