# OpieTaylor911 Stash Scrapers

Custom scrapers for Stash, published as a source index for in-app installation.

## Source Index URL

Use this in Stash:

https://opietaylor911.github.io/StashScrapers/main/index.yml

## Status

Current scraper set:

- AEBN (`scrapers/AEBN.yml`)

## Enable GitHub Pages (required)

If the source URL returns 404, enable Pages deployment:

1. Open repository **Settings**.
2. Go to **Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. Push any change under `scrapers/**` (already done for AEBN) or run the deploy workflow manually.

## Add More Scrapers

Drop new scraper files under `scrapers/` and push to `main`.
The workflow builds zip artifacts and regenerates the source index automatically.

## License

AGPL-3.0. See [LICENCE](LICENCE).
