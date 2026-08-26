# TourScale email assets

Static, publicly readable assets referenced by CRM email templates.

Email clients cannot load images from a private host and many (Outlook's Word
rendering engine in particular) will not render WebP, so brand logos are kept
here as PNG and served over GitHub Pages. Referencing them from here rather than
from the brand websites means an email's artwork does not depend on a site
deploy, and does not break if a site reorganises `public/images/`.

## Logos

| File | Brand | Use on |
|---|---|---|
| `logos/pedal-pub.png` | Pedal Pub | dark grounds (white wordmark, gold sprocket) |
| `logos/trolley-pub.png` | Trolley Pub | dark grounds (white/gold) |
| `logos/tiki-pub.png` | Tiki Pub | dark grounds (white wordmark) |
| `logos/paddle-pub.png` | Paddle Pub | **light grounds only** (navy/teal wordmark) |

Exported at 480px wide for a ~220px display width, so they stay sharp on retina.
Transparent PNG32, metadata stripped.

Note: `paddle-pub-logo-white.webp` in the paddlepub.com repo is byte-identical to
`paddle-pub-logo.webp`, so no white Paddle Pub wordmark exists. Until one does,
Paddle Pub email headers use a light ground.

## Adding an asset

Commit it and it is live at
`https://tourscale-repos.github.io/email-assets/<path>` within a minute or so.
Keep filenames stable: they are referenced from templates already sent.

## Photos

`photos/<brand>/<n>-<slot>.jpg` — hero image for each email in that brand's drip.

Exported at 1072px wide (2x a 536px display column) and cropped to a consistent
3:2, so the sequence reads as one set. JPEG q78, progressive, metadata stripped,
around 100-140KB each.

Sources are each brand site's own franchise photography, so the emails show the
same imagery a candidate sees on the website.
