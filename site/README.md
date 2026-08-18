# Next Plumbing & Heating — nextplumbingandheating.com

Static marketing site. No build step: `index.html` is served as-is.

## Layout

| File | Purpose |
| --- | --- |
| `index.html` | The whole site — markup, CSS and JS are inlined. |
| `vercel.json` | Clean URLs and security headers. |
| `favicon.svg`, `apple-touch-icon.png` | Icons. |
| `robots.txt`, `sitemap.xml` | Crawler hints, pointed at the production domain. |

## Deploying

Vercel project root directory is `site/`. Pushes to the production branch
deploy automatically; there is nothing to install or compile.

## Still to fill in

Three spots ship with bracketed placeholder copy that must be replaced with
real content before the site is advertised:

1. **Diagnostic fee** — `#process`, the paragraph starting "What it costs to find out".
2. **Google reviews** — `#reviews`, three cards. Paste real reviews only.
3. **Form backend** — the callback form validates input and shows a
   confirmation, but does not send anything anywhere. Wire the submit handler
   in `index.html` to a real endpoint (Vercel serverless function, Formspree,
   or similar) before relying on it for leads.
