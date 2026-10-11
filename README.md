# Harum Mandiri — Website

Static site. One HTML, two runtime scripts, a JSON image sidecar.

## Files

- `index.html` — v4 design (navy + orange)
- `support.js`, `image-slot.js` — Claude Design Canvas runtime (templating + image slots)
- `image-slots.state.json` — persisted image data read at page load
- `assets/`, `uploads/` — images and company profile PDF
- `drafts/` — earlier versions (v1 / v2 / v3), kept for reference, not deployed by default
- `vercel.json` — cache + security headers

## Preview locally

```bash
python3 -m http.server 8000
```

Open http://localhost:8000. Editing is disabled off-host; images come from `image-slots.state.json`.

## Deploy (Vercel)

```bash
npx vercel --prod
```

Framework: Other / None. Build command: none. Output dir: `.`

## Switching versions

To ship a different version, overwrite `index.html` from `drafts/`.
