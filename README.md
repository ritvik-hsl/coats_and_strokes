# Coats & Strokes — Link Page

A tiny static site meant to be deployed on Vercel and printed as a QR code.
The QR code points at this site's home page (`/`) and never has to change —
when you want to add, remove, or update a link (YouTube, Instagram, anything
else), you edit this project and redeploy. The QR stays valid forever.

## How it works

- `index.html` — the page people land on after scanning the QR. It renders a
  list of buttons from a small `LINKS` array at the bottom of the file.
- `qr.html` — visit `/qr` on your deployed site to get the actual QR code
  image (generated in the browser, pointing at your site's own URL). Click
  "Download PNG" to save it for printing.

## Updating the links later

Open `index.html` and edit the `LINKS` array:

```js
const LINKS = [
  { name: "YouTube", url: "https://www.youtube.com/YOUR_CHANNEL", icon: `...` },
  { name: "Instagram", url: "https://www.instagram.com/YOUR_HANDLE", icon: `...` },
  // add more entries here later, e.g.:
  // { name: "Website", url: "https://example.com", icon: `<svg>...</svg>` },
];
```

Commit and push (or redeploy on Vercel) — the live page updates immediately.
The QR code does **not** need to be regenerated or reprinted, since it only
points at the page URL, not at any individual link.

## Deploying to Vercel

1. Push this repo to GitHub (already done if you're reading this on your repo).
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. No build step is needed — it's a static site, so leave the framework
   preset as "Other" and deploy.
4. Once deployed, open `https://<your-project>.vercel.app/qr` to get your
   QR code (or use your custom domain if you attach one).

## Recommended: attach a custom domain

Vercel's default `*.vercel.app` URL works fine, but if you ever move hosting
providers, a custom domain (e.g. `coatsandstrokes.com`) means your QR code
stays valid even if you change where the site is hosted. You can add one
for free under the project's Settings → Domains in Vercel.
