# AGENTS.md

## Project

PWA water tracker with weather-aware daily targets. Companion to vitd. Zero build tools, pure HTML/CSS/JS.

## Architecture

- `docs/index.html` — Single-file app (~40KB), all CSS/JS inline
- `docs/manifest.json` — PWA manifest (standalone display)
- `docs/sw.js` — Service worker for offline + background sync
- `docs/icons/` — 192x192 and 512x512 PNGs (generated via Python script, not in repo)

## Deployment

- GitHub Pages serves from `docs/` folder on main branch
- URL: https://nd28.github.io/hydrate/
- No build step — push to main deploys immediately

## Key Features

- **Open-Meteo API** — Free weather, no API key (uses geocoding-api + forecast endpoints)
- **Weather logic** — Hot (>25°C) → +400ml, Humid (>70%) → +300ml
- **Gist sync** — Same pattern as vitd, separate data file
- **Ecosystem link** — Settings has "Open Vitamin D Tracker" → vitd

## Gotchas

- Single-file architecture — all CSS in `<style>`, all JS in `<script>`
- Icons generated via Python/Pillow script (not committed, can regenerate)
- Uses localStorage, data stays in browser only unless Gist sync enabled
- Quiet hours hardcoded: 22:00-07:00 (no notifications)
- Reminder schedules: 'fixed' (9/13/17/21h), '2h', '3h' — smart skip if goal reached
- No tests — verify by opening in browser and testing manually
- Mobile-first design — test on actual device or mobile viewport
