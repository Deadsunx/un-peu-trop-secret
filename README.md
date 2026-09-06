# Daily Data Archive 🌍

A small project that builds a **growing dataset** by fetching four free sources
every single day and archiving them — all automatically via a scheduled
[GitHub Actions](https://docs.github.com/actions) workflow.

Because the automation runs on **GitHub's servers**, the daily commit happens
whether my laptop is on or off.

**🌐 Live page → https://deadsunx.github.io/daily-ephemeris/**
_(the "Ephemeris" — a daily record of sky, market, word & road)_

## What it collects each day

| # | Source | Provider |
| - | ------ | -------- |
| 1 | Crypto prices (BTC / ETH / SOL) | CoinGecko |
| 2 | Quote of the day | ZenQuotes |
| 3 | Astronomy Picture of the Day | NASA APOD |
| 4 | Top car-news headline | Car-news RSS feed |

## How it works

1. `.github/workflows/daily.yml` runs [`daily_update.py`](daily_update.py) once a day.
2. The script saves a dated snapshot to [`archive/`](archive), appends crypto
   prices to [`data/crypto.csv`](data/crypto.csv), and refreshes the block below.
3. It commits and pushes **as me**, so it counts toward my contribution graph.

## Run it locally

```bash
python daily_update.py
```

Only the Python standard library is used — nothing to install.

<!-- LATEST:START -->
### 📅 Latest snapshot — 2026-09-06

> *"A man with outward courage dares to die: a man with inner courage dares to live."* — **Lao Tzu**

**Crypto (USD)**

| Coin | Price | 24h |
| --- | --- | --- |
| Bitcoin | $79,862 | +0.24% |
| Ethereum | $2,497.9 | +1.73% |
| Solana | $105.3 | +3.02% |

**🔭 NASA:** [Pluto in Enhanced Color](https://apod.nasa.gov/apod/image/2609/PlutoEnhancedHiRes_NewHorizons_960.jpg)

**🚗 Car news:** [Bentley Used To Outsell Rolls-Royce By 3 To 1. Not Anymore](https://www.motor1.com/news/807183/rolls-royce-vs-bentley-sales-figures/)

**📜 On this day, 394:** Battle of the Frigidus: Roman emperor Theodosius I defeats and kills Eugenius the usurper. His Frankish magister militum Arbogast escapes but commits suicide two days later. — [Battle of the Frigidus](https://en.wikipedia.org/wiki/Battle_of_the_Frigidus)

**🐙 GitHub [@Deadsunx](https://github.com/Deadsunx):** 11 repos · 10 followers

<!-- LATEST:END -->
