# FlowState Signal Engine

> **Institutional Bitcoin flow intelligence. Data receipts, not vibes.**

A live, browser-based dashboard that aggregates real-time BTC derivatives data, ETF flow signals, market structure, and on-chain sentiment into a single composite read — built for the institutional crypto analyst workflow.

🔴 **[Live Dashboard →](https://Oxsimba.github.io/flow-state-dashboard)**

---

## What It Does

Every morning the crypto analyst's workflow involves pulling data from six different sources, cross-referencing them, and forming a directional view before writing. This dashboard compresses that into 60 seconds.

It auto-fetches live data across five signal categories, generates a composite bull/bear score from the **FlowState 5-Signal Framework**, and produces a **data receipt** — a one-paragraph summary of exactly what the data says, ready to inform institutional-grade analysis.

---

## Live Data Sources

| Signal | Source | Refresh |
|---|---|---|
| BTC Price, High, Low, Market Cap | CoinGecko API | 30s |
| Funding Rate | Binance Futures API | 30s |
| Open Interest | Binance Futures API | 30s |
| Long/Short Ratio | Binance Futures API | 30s |
| Fear & Greed Index + 7-day trend | Alternative.me API | 30s |
| Market Dominance (BTC/ETH/SOL) | CoinGecko Global API | 30s |
| Spot Volume vs OI Divergence | Binance Spot API | 30s |
| ETF Daily Net Flow | Manual — Farside Investors | Daily |

> All live data sources are **keyless and free** — no API keys required, no backend infrastructure, runs entirely in the browser.

---

## The 5-Signal Framework

The core analytical engine. Each signal is scored independently, then combined into a composite read:

```
Signal 01 — ETF Net Flow Direction     (institutional demand)
Signal 02 — Open Interest              (leverage expansion vs contraction)
Signal 03 — Funding Rate               (market sentiment, overextension)
Signal 04 — Fear & Greed Index         (extremes as contrarian signals)
Signal 05 — Long/Short Ratio           (positioning imbalance)
```

**Output:** `STRONG BULL / BULLISH LEAN / MIXED / BEARISH LEAN / STRONG BEAR`

Composite score displayed as `X/5 bull signals` with a visual bar chart and a full **Data Receipt** — a structured summary of all active signals including ETF flows, whale positioning (Nansen), and analyst notes.

---

## Tech Stack

```
HTML5 / CSS3 / Vanilla JavaScript
REST APIs — CoinGecko, Binance Futures, Alternative.me
Deployed via GitHub Pages (zero infrastructure cost)
Auto-refresh every 30 seconds via setInterval
SVG — custom gauge, sparklines, bar charts (no charting library)
```

No frameworks. No build pipeline. No dependencies. Pure browser-native code — intentionally lean for maximum portability and zero maintenance overhead.

---

## Screenshots

> Dashboard running live — BTC price hero, signal cards, 7-day Fear & Greed sparkline, Spot/OI divergence ratio, 5-signal composite framework, and data receipt.

![FlowState Signal Engine](https://Oxsimba.github.io/flow-state-dashboard)

---

## Context & Background

This tool was built to support **[Flow State Weekly](https://flowstatweekly.substack.com)** — an institutional Bitcoin flow intelligence newsletter tracking ETF flows, on-chain whale movements, and derivatives positioning.

The analytical framework powering this dashboard is the same one used to produce weekly intelligence for professional crypto traders and institutional allocators.

> *"Data receipts, not vibes."*

---

## Running Locally

No installation required. Clone and open:

```bash
git clone https://github.com/Oxsimba/flow-state-dashboard.git
cd flow-state-dashboard
open index.html
```

Or just visit the **[live deployment](https://Oxsimba.github.io/flow-state-dashboard)** directly.

---

## Roadmap

- [ ] 30-day ETF flow trend chart
- [ ] Nansen wallet cluster live feed (requires Nansen API key)
- [ ] Macro overlay — oil, gold, DXY (server proxy required)
- [ ] Alert system — signal threshold notifications
- [ ] FlowState Pro tier integration

---

## About

Built by **Simba** ([@0xbrel](https://twitter.com/0xbrel)) — crypto analyst and author of Flow State Weekly. Based in Tanzania. Tracking institutional Bitcoin flows since 2025.

**Newsletter:** [flowstatweekly.substack.com](https://flowstatweekly.substack.com)
**Twitter/X:** [@0xbrel](https://twitter.com/0xbrel)

---

*This dashboard is a personal analytical tool. Nothing here is financial advice.*
