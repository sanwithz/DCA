# Drawdown DCA Simulator

A Bitcoin DCA (Dollar Cost Averaging) simulator and backtester featuring Heikin Ashi candlestick generation, peak-to-trough drawdown detection, RSI-weighted dynamic position sizing, trend moving averages (21 EMA, 50 EMA, 200 MA), and persistent LocalStorage/URL state synchronization.

## 🚀 Features

- **Heikin Ashi Price Smoothing**: Filters short-term noise for swing high/low identification.
- **Peak-to-Trough Drawdown Mapping**: Automatically detects peak highs and tracks drawdown percentages (`-10.5%`, `-14.8%`, `-24.7%`, `-29.9%`, etc.).
- **RSI-Weighted DCA Allocation**:
  - `RSI <= 30` (Oversold): **2.0x Multiplier**
  - `RSI >= 70` (Overbought): **0.0x Multiplier (Pauses DCA)**
  - Normal: **1.0x Base Allocation**
- **Trend Indicators**: 🟢 21 EMA, 🔴 50 EMA, 🟣 200 MA, and 🟠 Step-down Average Cost Line.
- **Interactive Timeframes & Filters**: Switch between `1D`, `3D`, and `1W` charts with custom date filtering (`01/01/2026` → `31/12/2099`).
- **State & URL Synchronization**: All backtest parameters and date ranges automatically sync to `localStorage` and URL query parameters for seamless sharing and reloading.
- **Live Binance Data Feed**: Real-time ticker updates via WebSocket + REST API fallback.

## 🛠️ Tech Stack

- **Vanilla HTML5 / CSS3 / JavaScript**
- **Lightweight Charts v4.2.1**
- **Tailwind CSS (CDN)**
- **Binance WebSocket API**

## 📦 Getting Started

Open `index.html` directly in any modern browser, or serve it using any static file server:

```bash
npx serve .
```
