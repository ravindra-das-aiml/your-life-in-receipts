# Your Life, In Receipts 🧾

A frontend-only interactive story built from a fictional person's digital-life receipts
(music, movies, places, purchases, photos, messages, searches, events, notes).

## What it does
- **Explore** — search + filter all receipts by type
- **Chapters** — receipts auto-clustered by time proximity into named "chapters",
  each with a short auto-generated insight line explaining the pattern in that cluster
- **Connections** — a graph view where nodes are receipts and edges are shared
  date/location/tags; click any node to see what it's connected to and why
- **Insights** — computed stats (recurring theme, total spend, most common moment type)

## Run it
No build step. Just open `index.html` in a browser, or deploy the single file directly.

## Deploy (pick one, ~2 min)
- **Netlify**: drag `index.html` into netlify.com/drop
- **Vercel**: `vercel --prod` in this folder (or drag-drop on vercel.com/new)
- **GitHub Pages**: push to a repo, enable Pages on `main` branch root

## Swap in the real dataset
Replace the `RECEIPTS` array near the top of the `<script>` tag in `index.html`.
Keep the same field shape:
```js
{id, type, date, title, sub, tags:[], loc, amt}
```
Everything else (clustering, graph edges, insights, search) recomputes automatically.
