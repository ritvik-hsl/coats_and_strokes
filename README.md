# Coats & Strokes — Link Page

A tiny static site meant to be deployed on Vercel and printed as a QR code.
The QR code points at this site's home page (`/`) and never has to change —
when you want to add, remove, or update a link (YouTube, Instagram, anything
else), you edit this project and redeploy. The QR stays valid forever.

## How it works

- `index.html` — the page people land on after scanning the QR: hero,
  photo gallery, Instagram/YouTube link buttons, and a contact section.
- `style.css` — all styling (purple/pink/black brand palette, fonts, cards).
- `images/` — drop your real photos here (see `images/README.md` for exact
  filenames). Until a photo exists, that spot shows a striped placeholder.
- `qr.html` — visit `/qr` on your deployed site to get the actual QR code
  image (generated in the browser, pointing at your site's own URL). Click
  "Download PNG" to save it for printing.

## Things you'll want to fill in

Everything below is currently a placeholder, marked with `TODO` comments in
`index.html` — search for `TODO` to find each spot:

- **Instagram URL** — currently `https://instagram.com/coatsandstrokes`
- **YouTube URL** — currently `https://youtube.com/@coatsandstrokes`
- **Phone number** — currently `+1 (000) 000-0000` (the `tel:` link too)
- **Email address** — currently `hello@coatsandstrokes.example`
- **Photos** — see `images/README.md`

## Updating links/contact info later

Open `index.html` and edit the relevant `href`/text directly — each spot is
marked with a `TODO` comment. Commit and push (or redeploy on Vercel) and the
live page updates immediately. The QR code does **not** need to be
regenerated or reprinted, since it only points at the page URL, never at any
individual link or detail on it.

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
