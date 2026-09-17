# Surface

Surface is a standalone static HTML experience. It does not use npm, a
JavaScript framework, a server, or a build step. The complete application is
in [`index.html`](./index.html), including its CSS, inline SVG artwork, and
browser-side interactions.

## Deploying on Render

The repository includes [`render.yaml`](./render.yaml), which configures the
application as a Render Static Site:

- **Service type:** Static Site
- **Root Directory:** repository root (`.`)
- **Build Command:** `mkdir -p dist && cp index.html dist/index.html`
- **Publish Directory:** `dist`
- **Environment variables:** none required

If configuring the service manually, remove the old `npm install && npm run
build` command. This repository intentionally has no `package.json`; the
static build command above creates the publish directory without npm.

The site does not use client-side URL routing, so no SPA rewrite rule is
required. All visual assets are inline, and the only external resources are
the Google Fonts requested by `index.html`.