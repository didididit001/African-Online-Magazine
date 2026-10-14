AFRICAN · The Saint Bill Issue — self-hosted flipbook
=====================================================
Open index.html (needs to be served over http/https for video + hash links to behave on every browser;
any static host works: Netlify, Cloudflare Pages, GitHub Pages, your own server, or `python3 -m http.server`).

Folder layout
  index.html        the whole viewer (no libraries, no accounts)
  pages/            cover-*.jpg (6 sample covers) + model-*.jpg (8 Saint Bill photos)
  media/            4 cover videos (.mp4) + media/posters/ (frame shown on the video pages)

Edit the CONFIG / COVERS / INTERIOR blocks at the top of index.html:
  websiteUrl        link used by the cover QR/badge, footers, back cover and the 🌐 button
  seed              null = covers land in a new random order each visit; a number freezes the order (?seed=7 also works)
  frontCover        "random" or 0-5
  autoFlipSeconds, loop, flipMs, curlRadius, curlLift, curlShadow, hoverPeek, maxZoom
To add pages: add an entry to INTERIOR ({ img, tag, pos }) — video pages add { video: "media/x.mp4" }.
Embed in another site:  <iframe src="https://your-site/flipbook/" allowfullscreen style="width:100%;height:80vh;border:0"></iframe>

Controls
  Turn pages      drag a page from its outer edge, click the edges, ◀ ▶ buttons, ← → keys, or swipe
  Back to front   drag/click the page bar above the toolbar to jump anywhere; ⏮ ⏭ for first/last
  Move magazine   grab it anywhere on a page (away from the outer edges) and drag; two-finger pinch + drag on touch;
                  ✋ (or H) = move tool, then drag works even from the edges
  Zoom            − / + buttons, mouse wheel, pinch, double-click, + - keys (35%-400%); 0 or "Fit to window" resets
  Spread / single 📖 / 📄 button (or V). Spread is the default; it rescales to fit the window as the book opens
