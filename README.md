# qandeel.app

Qandeel (قنديل): from Alif to Ayah. Served by GitHub Pages at https://qandeel.app.

| Path | What |
|---|---|
| `/` (`index.html`, `img/`) | Company landing page |
| `/garden/` | Letter Garden, the children's Arabic letters game |

`garden/` is **generated**. Letter Garden is still developed in its own checkout
(`miftah/.local-work/letter-garden-next-major`). To publish a new version:

```bash
node scripts/sync-garden.mjs
git add -A && git commit -m "Sync Letter Garden" && git push
```

The script copies only what the game uses, retitles the page for Qandeel, points
the anonymous Plausible counts at `qandeel.app`, and regenerates `garden/sw.js` so
its offline shell matches the copied files exactly.
