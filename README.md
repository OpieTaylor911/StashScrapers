# OpieTaylor911 Stash Scrapers

Custom scrapers for [Stash](https://github.com/stashapp/stash), published as a GitHub Pages source index.

## Source Index URL

Add this URL in Stash:

**https://opietaylor911.github.io/StashScrapers/main/index.yml**

## Quick Setup

1. Open Stash.
2. Go to **Settings -> Plugins -> Add Source**.
3. Paste the source index URL above.
4. Refresh sources and install the scraper(s) you want.

## Included Scrapers

- [AEBN](scrapers/AEBN.yml)

## What The AEBN Scraper Covers

- Scene and group scraping from mobile AEBN pages
- Box cover + first scene image logic
- Categories -> tags
- Stars -> performers
- Studio extraction (deepest studio when multiple are listed)

## Repository Layout

- `scrapers/` -> scraper YAML files
- `build_site.sh` -> builds index + zip artifacts for publication
- `.github/workflows/deploy.yml` -> deploys source index to GitHub Pages

## Publishing Flow

On push to `main` for files under `scrapers/**`:

1. `build_site.sh` packages scrapers and generates `index.yml`
2. GitHub Actions deploys output to Pages
3. Stash source URL serves latest index and zips

## Troubleshooting

### Source URL returns 404

1. Open **Repository Settings -> Pages**
2. Set **Build and deployment -> Source** to **GitHub Actions**
3. Check **Actions** tab for the latest deploy job status
4. Re-run deploy workflow or push a small change under `scrapers/**`

### Scraper not showing in Stash

1. Confirm index URL is reachable in browser
2. In Stash, refresh sources
3. Check scraper YAML filename and `name:` field
4. Validate YAML syntax and push again

## Contributing

Add new scraper files to `scrapers/` and push to `main`.

## License

[AGPL-3.0](LICENCE)
