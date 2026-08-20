# Prodigy Racing Association

Official website for the Prodigy Racing Association (PRA) — a sim racing community hosting competitive leagues across iRacing, Wreckfest, Gran Turismo 7, and Automobilista 2.

## Live Site

<https://aosjay13.github.io/pra/>

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Landing page — league intro, platforms, community, and links out |
| `announcements.html` | League announcements |
| `calendar.html` | Embedded race calendar |
| `grid-finder.html` | Grid Finder sign-up splash |
| `discord-link.html` | Discord invite splash |

Schedules, standings, results, records, series details, and driver profiles all
live in the [Phoenix Racing League Manager](https://phoenix-racing-league-manager.vercel.app/),
which this site links out to. This repo holds the public-facing site only —
five embed pages that duplicated the app (league stats, points standings,
league records, the records document, and the spreadsheet viewer) were removed
in favour of linking to it.

## Theme

All pages share the Phoenix Racing League Manager's design tokens, so the site
and the stats hub read as one product:

| Token | Value | Use |
| --- | --- | --- |
| `bg-0` | `#0d0d14` | Page background |
| `bg-1` | `#13131e` | Headers, raised bars |
| `bg-surface` | `#1a1a28` | Cards |
| `bg-elevated` | `#20202f` | Nested surfaces |
| `ink-0` / `ink-1` / `ink-2` | `#eeeef5` / `#bfbfd4` / `#9a9ab4` | Text scale |
| `accent-red` | `#e63946` | Primary brand accent |
| `accent-cyan` | `#00b4d8` | Interactive / links |
| `accent-gold` | `#f4a228` | Highlights |

Type is **Plus Jakarta Sans** (loaded from Google Fonts, falling back to
`Segoe UI` / `system-ui`). Cards use a 16px radius, controls 10px. A 2px
red-to-cyan hairline marks primary headers, matching the stats hub's hero.

Grid Finder orange (`#ff3d00`) and Discord blurple (`#5865f2`) are kept as-is
on their own splash pages.

## Deployment

The site is static HTML deployed via GitHub Pages. Every push to `master`
triggers automatic deployment through the workflow in `.github/workflows/pages.yml`.

### Setup

1. Open repository **Settings > Pages**.
2. Under Build and deployment, set Source to **GitHub Actions**.
3. Save.

### Updating the Site

1. Edit the HTML files in this repository.
2. Commit and push to `master`.
3. The Pages workflow deploys automatically.
4. Verify at the live URL.
