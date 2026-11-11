# Manuals

Gateway / router layer for the three manuals, deployed at **https://manuals.vercel.app**.

| Route | Redirects to |
| --- | --- |
| `/aws`, `/aws/*` | https://awsmanual.vercel.app |
| `/linux`, `/linux/*` | https://linuxmanual.vercel.app |
| `/sql`, `/sql/*` | https://sqlmanual.vercel.app |

The landing page lives in `public/index.html`; routing is handled by the
`redirects` in `vercel.json` (deep paths are preserved, e.g.
`/sql/joins` → `https://sqlmanual.vercel.app/joins`).

## Deploy

1. Import this repo in Vercel (Framework preset: **Other**, no build command).
2. Name the project `manuals` so it is served at `manuals.vercel.app`.

To add another manual, add a card to `public/index.html` and a pair of
redirects to `vercel.json`.

## Theme

Dark, terminal-style look modelled on [devvm.dev](https://devvm.dev): black
background, lime `#7fff00` accent, teal `#20474b` borders, pixel-mono headings.
Headings use [Departure Mono](https://departuremono.com/) (SIL OFL 1.1,
self-hosted in `public/fonts/` with its licence); body text uses Instrument
Sans and Martian Mono from Google Fonts.
