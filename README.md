# 🌊 hydrate

Smart water intake tracker with weather-aware daily targets. A PWA companion to [vitd](https://github.com/nd28/vitd).

**Live app:** https://nd28.github.io/hydrate/

## Features

- ☀️ **Weather-aware targets** — Automatically adjusts your daily goal based on temperature and humidity (via Open-Meteo, no API key needed)
- 💧 **Quick tracking** — One-tap logging with 3 preset sizes (200ml, 350ml, 500ml)
- 📊 **Visual progress** — Animated ring fills up as you drink
- 📈 **Statistics** — 7-day chart, streak counter, daily averages
- 🔔 **Smart reminders** — Choose your schedule (fixed times, every 2h, every 3h)
- ☁️ **GitHub Gist sync** — Backup and sync across devices
- 📱 **PWA** — Install as standalone app, works offline

## Quick Start

1. Visit https://nd28.github.io/hydrate/
2. Enter your weight and city (for weather adjustments)
3. Tap to log water throughout the day
4. Install to home screen for easy access

## Weather Adjustments

- 🔥 **Hot day (>25°C)** → +400ml to target
- 💧 **Humid day (>70% humidity)** → +300ml to target

## Ecosystem

hydrate works standalone but links seamlessly with vitd:

- ☀️ [vitd](https://nd28.github.io/vitd/) — Vitamin D tracker
- 🌊 **hydrate** — Water tracker

Tap "Open Vitamin D Tracker" in Settings to switch between apps.

## Tech Stack

- Single-file HTML/CSS/JS (no build step)
- Open-Meteo API (free weather, no key)
- GitHub Gist for optional sync
- Service Worker for offline support

## Privacy

- All data stored in browser localStorage
- Optional sync uses your own GitHub Gist (private by default)
- No tracking, no analytics, no server

---

MIT License — Build your health stack, one PWA at a time.
