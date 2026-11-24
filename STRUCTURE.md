# STRUCTURE — tollplazanearme

## DOM-id contract — do not rename

| id / selector | Used by |
| --- | --- |
| `#map` | `js/app.js` (Leaflet mount) |
| `#ncontent` | `js/content.js` |
| `#nblocks` | `js/blocks.js` |
| `.controls` | `js/app.js` |

## File roles

| File | Role |
| --- | --- |
| `index.html` | the only page |
| `css/style.css` | all styling |
| `js/app.js` | Leaflet map, geolocation, search |
| `js/blocks.js` | near-me blocks + Read more expansion |
| `js/content.js` | intro, query headings, how-to, FAQ |
| `js/analytics.js` | first-party pageview beacon |
| `sitemap.xml` | urlset, own host only |
| `robots.txt` | allow all, Sitemap line last |

## Improvement protocol

1. Read this file and `index.html` before editing.
2. Never remove a DOM id the JS depends on.
3. Add a `<loc>` to `sitemap.xml` whenever a real page is added.
4. Verify live after deploy: home 200, title, h1, sitemap locs > 0.
