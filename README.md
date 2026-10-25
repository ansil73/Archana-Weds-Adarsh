# Archana & Gokul – wedding invitation (static site)
Open `index.html` through any static host. No build step.

## Replace things
- Photos: swap files in `assets/` (same names). Order/names map is the `IM` object in `index.html`.
- Reel: `assets/prewedding-reel.mp4` + poster `assets/reel-poster.jpg`. Re-compress: `ffmpeg -i in.mp4 -vf "scale='min(1080,iw)':-2" -c:v libx264 -crf 24 -pix_fmt yuv420p -c:a aac -movflags +faststart assets/prewedding-reel.mp4`
- Details (date, phone, map link, place): the `CFG` object at the top of the script. Text lives in the HTML.
- Music: not included (no file supplied).

## Deploy (simplest: Netlify Drop)
1. Go to app.netlify.com/drop and drag the whole folder in. You get an https link.
2. Open it on your phone, then paste it in WhatsApp and check the preview.
3. For the preview image, change `og:image` in `index.html` to the full URL, e.g. `https://YOUR-SITE.netlify.app/assets/og-preview.jpg`, and add `<meta property="og:url" content="YOUR LINK">`. Redeploy.
GitHub Pages / Vercel: upload the folder as a repo / project; no settings needed.

## Still needed from you
Exact venue coordinates (or confirm the map pin), landmark, railway station, airport, parking, and a licensed music file. These were not on the card, so they are not shown.

## Checklist
Open on a phone: seal, Skip, language toggle, reel plays, gallery tap/enlarge, map buttons, Call, Copy, .ics, WhatsApp RSVP, Share, link preview.
