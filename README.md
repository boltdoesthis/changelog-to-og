# Changelog → OG

Free micro-tool from **Indie Agent Kit** (`boltdoesthis`).

Paste changelog or release notes → get a social/OG card preview, downloadable PNG or SVG, and short tweet / LinkedIn blurbs. Everything runs in the browser. No build step, no accounts, no paid APIs.

## Features

- Client-side Markdown/plain-text parsing (version, title, summary, bullets, date)
- Live 1200×630 OG card preview (canvas) with four themes (Ink, Mint, Paper, Violet)
- Download PNG (canvas) or SVG (vector twin)
- Suggested tweet (≤280 chars) and LinkedIn blurb with one-click copy
- Static files only. Works on GitHub Pages, Cloudflare Pages, Netlify, or any static host

## Files

| File | Role |
|------|------|
| `index.html` | App (HTML + CSS + JS in one file) |
| `README.md` | This file |

## Local preview

Open `index.html` in a browser, or serve the folder:

```bash
# Python
python3 -m http.server 8080

# Node (if you have npx)
npx --yes serve -p 8080
```

Then visit `http://localhost:8080`.

## Deploy (free)

### GitHub Pages (boltdoesthis / changelog-to-og)

1. Create a public repo named `changelog-to-og` under [github.com/boltdoesthis](https://github.com/boltdoesthis).
2. Push this folder as the repo root (or put files in `/docs` and set Pages source to `/docs`).
3. Settings → Pages → Deploy from branch → `main` / root (or `/docs`).
4. Site URL: `https://boltdoesthis.github.io/changelog-to-og/`

Example first push:

```bash
cd changelog-to-og
git init
git add index.html README.md
git commit -m "Initial Changelog → OG micro-tool"
git branch -M main
git remote add origin https://github.com/boltdoesthis/changelog-to-og.git
git push -u origin main
```

Then enable Pages on `main` / root.

### Cloudflare Pages

1. Push the same repo to GitHub/GitLab.
2. Cloudflare Dashboard → Workers & Pages → Create → Connect to Git.
3. Framework preset: **None**. Build command: empty. Output directory: `/` (repo root).
4. Deploy. Optional: attach a custom domain later.

## License

MIT. Indie Agent Kit / boltdoesthis.

## Brand

Public brand only: **Indie Agent Kit** / **boltdoesthis**.
