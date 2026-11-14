# Stockwatch — site

The marketing page for **Stockwatch**: a self-hosted inventory dashboard for one warehouse —
FastAPI, SQLite, one machine, the database never leaves the customer's hardware.

Plain HTML/CSS/JS in one file. No build step, no fonts to fetch, no dependencies. Open
`index.html` in a browser, or drag the folder into any static host: it is deployed at
**https://nxgenwidgeter.github.io/stockwatch-site/** from this public repo, which holds nothing
but the page.

```
index.html    the whole site (CSS + JS embedded, no assets)
```

## The build is not here

The application lives in a private repo (`NxGenWidgeter/stockwatch`) and is shared on request:
the three cards in the download section open a pre-filled email. That is deliberate — the page
is public so it can be linked to a prospect, the build is not published so a copy cannot be
scraped off it. If that ever changes (public releases, a mirror, an S3 bucket), the download
block is the only thing on the page to edit.

## Editing it

- **Version stamps are the trap.** The page names a version in several places (header, setup
  block, health sample, close paragraph, download note, footer). Bump them together and check
  with `grep -c '<old version>' index.html` — 0 is the only pass.
- Push to `main`; GitHub Pages rebuilds in about a minute. Prove it on the live URL, not on the
  file you just wrote.
