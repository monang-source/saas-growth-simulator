# SaaS Growth Simulator

Model your SaaS growth trajectory from a small set of assumptions. A self-contained, single-page interactive simulator covering MRR, ARR, CAC, and churn over a 12-month projection.

## Pages

| Page | Purpose |
|------|---------|
| `index.html` | Home launcher and overview of the 5 key assumptions |
| `dashboard.html` | Interactive 12-month simulator (Chart.js) — MRR/ARR/CAC/churn, sliders, A/B comparison, CSV export |
| `scenarios.html` | Save, load, and compare model presets |
| `churn.html` | Retention curves, customer lifetime, and LTV analysis |
| `unit-economics.html` | CAC payback, LTV:CAC ratio, and gross margin analysis |
| `customers.html` | Acquisition funnel from leads to paid customers |

## How it works

The model projects growth from five assumptions:

1. **Starting MRR** — current monthly recurring revenue
2. **Net Monthly Growth** — new + recovered MRR each month
3. **Monthly Churn** — % of existing MRR lost each month
4. **ARPU** — average revenue per user per month
5. **CAC** — customer acquisition cost

For each of the 12 months it computes end-of-month MRR, annualized run-rate (ARR), new/recovered MRR, CAC payback, and LTV — feeding KPI cards, a chart, and plain-language insights.

## Design system

Visual language lives in `design-system/saas-growth-simulator/MASTER.md`: navy data (`#1E40AF`) with amber accents (`#D97706`), **Fira Code** for figures and **Fira Sans** for UI, data-dense dashboard style.

All pages share:
- Consistent app navigation linking all 6 pages
- Dark mode via `prefers-color-scheme` + persistent toggle (`sgs-theme` in localStorage)
- Accessibility: ARIA labels, visible focus states, `prefers-reduced-motion`
- SVG icons (no emojis) and responsive nav

## Tech

- Plain HTML + CSS + vanilla JS — no build step
- [Chart.js](https://www.chartjs.org/) (loaded from cdnjs) for revenue projection
- Google Fonts (Fira Sans / Fira Code)

## Run it

Open `index.html` in any browser — no server or dependencies needed.

## Stack planned (roadmap)

Interactive per-page modules for Scenarios (save/compare presets), Churn & Retention, Unit Economics, and the Customers funnel are stubbed and ready to be built out.
