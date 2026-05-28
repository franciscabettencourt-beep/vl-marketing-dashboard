# Vilalara Pulse

An editorial marketing intelligence dashboard for **Vilalara Thalassa Resort**.

> Inspired by Monocle, Cereal, Aman.
> Built as a single HTML file. Zero build step. Zero server.

## What this is

Phase I (MVP) of a multi-phase product. The dashboard opens with a **Today's Story** — an editorial paragraph automatically composed from the day's data — and then unfolds into chapters (KPIs, revenue trajectory, channel mix, pickup vs. forecast, markets in motion).

Every KPI is clickable and opens a drill-down panel with three-year history, channel breakdown, and a suggested action.

## How to run

Open `index.html` in any modern browser. No build, no server, nothing to install.

```bash
open index.html
```

Or — to share with the team — host on GitHub Pages:

```bash
cd vtrl-marketing-dashboard
git init
git add .
git commit -m "Vilalara Pulse — Phase I"
git branch -M main
gh repo create vtrl-marketing-dashboard --public --source=. --push
# Then: Settings → Pages → Source: main / root
```

## Stack

- Vanilla HTML, CSS, JS — no framework, no build.
- [Chart.js](https://www.chartjs.org/) via CDN for trend & history charts.
- [Day.js](https://day.js.org/) via CDN for date helpers.
- Inline SVG for sparklines (no library overhead).
- LocalStorage for preferences (language, theme, view, YoY toggle).

## Features (Phase I)

- **Today's Story** — auto-generated editorial paragraph that surfaces the day's most salient facts (occupancy vs. STLY, top market, channel mix shift, on-the-books delta).
- **Six hero KPIs** — Occupancy, ADR, RevPAR, Today's Revenue, Pickup 7d, On-the-books 30d. Each has a sparkline, a YoY delta, and on hover, contextual prose.
- **Revenue trajectory** chart — 30 days, with 2025 dashed overlay.
- **Channel mix** — bars, shares, deltas in pp.
- **Pickup vs. forecast** — daily bars with forecast line, last 30 days.
- **Markets in motion** — top 6 markets over the last 7 days with YoY deltas.
- **Drill-down panel** — slide-in from right with 3-year monthly history, channel breakdown for the day, and a suggested action tailored to the KPI's state.
- **PT/EN toggle** — full bilingual UI.
- **Light/Dark editorial themes** — warm off-white & warm charcoal palettes.
- **Synthetic data** — three years of deterministic, Algarve-seasonal data so the experience is fully explorable without uploads.

## Coming next

- **Phase II** — The Week, The Month, Origins (channels + markets + interactive world map), Pace & Forecast (port the `vtrl-room-forecast` logic), Sources upload panel for Opera/SiteMinder/GA4. Drag & drop layout.
- **Phase III** — Digital Pulse: GA4 + Google Ads + Meta Ads integration, funnel chart.
- **Phase IV** — Polish: GSAP animations, presentation mode (fullscreen), Cmd+K command palette, annotated timeline, weekly snapshots, PDF export.

## Conventions (carried from `vtrl-room-forecast`)

- Room types **ELETC, ELEDC, STOC, SDOC** → labelled "Comunicante".
- 5th numeric column on Opera occupancy exports = **Reserved**.

## License

Internal use, Vilalara Thalassa Resort.
