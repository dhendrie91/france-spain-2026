# Our Trip — France & Spain · August 2026

A single-page itinerary site. Everything lives in `index.html` (inline CSS + JS, Leaflet and Google Fonts loaded from CDN). No build step.

## Preview locally

The simplest way:

```sh
open index.html        # macOS
xdg-open index.html    # Linux
```

Or, if you want a real `http://` URL (recommended — some browsers restrict file://):

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

Pick whichever is easiest — all three are free and take under a minute.

### Netlify Drop (easiest, no account needed for one-off)

1. Go to https://app.netlify.com/drop
2. Drag the folder containing `index.html` onto the page
3. Netlify gives you a public URL like `https://something-random.netlify.app`
4. (Optional) sign in to claim the site and pick a custom subdomain

### Vercel

1. Install once: `npm i -g vercel`
2. From this directory: `vercel`
3. Follow the prompts — accept defaults. You'll get a URL like `https://trip-xxx.vercel.app`

### GitHub Pages

1. Create a new repo, push `index.html` to the `main` branch
2. Repo → Settings → Pages → Source: `main`, folder: `/ (root)` → Save
3. Wait ~30 seconds. Your site is at `https://<username>.github.io/<repo>/`

## Generate the QR code

Once you have the deployed URL, generate a QR code pointing at it:

- **https://qrcode.show/** — paste the URL, download the SVG/PNG. No account, no tracking.
- Alternatives: https://qrgo.page or https://www.qr-code-generator.com

Print it on a card, slip it into something — done.

## Editing

Open `index.html` in any editor. All styling is in the `<style>` block in `<head>`, all behaviour in the `<script>` block at the bottom. Colour palette is set as CSS variables on `:root` — change those to retheme everything at once.
