# Sector Rotation

**Live page: https://ducatipartiv4.github.io/sector-rotation/**

An interactive Relative Rotation Graph of the 11 S&P 500 sector ETFs (XLK, XLF, XLC, XLY, XLV, XLI, XLP, XLE, XLU, XLRE, XLB)
against a benchmark (SPY by default; RSP and QQQ selectable). Every sector is a dot that rotates clockwise through four quadrants:

| Quadrant | Color | Meaning |
|---|---|---|
| **Leading** | green | outperforming the benchmark and accelerating |
| **Weakening** | red | still outperforming, momentum rolling over |
| **Lagging** | blue | underperforming and still losing |
| **Improving** | yellow | underperforming, momentum turning up |

Rotation runs Improving → Leading → Weakening → Lagging → Improving.

## Using the page
- **Period:** daily closes or weekly closes. **Range:** 1M / 3M / 6M / YTD / All. **Smoothing:** fast / standard / slow.
- **Play** animates the year one close at a time; the slider scrubs any date; ← → step, space plays, Home/End jump.
- **Tail** = how many past periods each sector drags behind it (dot spacing = speed).
- The **quadrant board** shows how long each sector has sat in its quadrant and which way it moved last.
- The **quadrant changes** log lists every crossing by date (click one to jump there; *brief* = reversed within two periods).
- The **rotation ribbon** paints each sector's quadrant per period across the whole range — the fastest way to see *when* a sector changed. Click it to scrub.
- Hover any dot or ribbon cell for the readings; click a dot to focus one sector; **Patterns** adds hatching for colour-blind viewing.

## Method
RS = 100 × sector ÷ benchmark on dividend-adjusted closes, EMA-smoothed. **RS-Ratio** (x) = 100 + the z-score of RS against its
lookback window (the relative trend). **RS-Momentum** (y) = 100 + the z-score of RS-Ratio against its own lookback (the ratio's
momentum). Daily standard windows 63 / 21 days with a 5-day EMA; weekly 14 / 14 weeks with a 3-week EMA. This is the public
approximation of the JdK RRG; StockCharts' exact series is proprietary.

## Data and updates
Daily closes from a moomoo OpenD feed, 750 sessions of history. The page is regenerated and pushed automatically every weekday:
premarket at 08:05 ET, every 30 minutes during the session (today's point is live), and after the close at 16:25 ET.
The timestamp in the header says when it was last updated.

*Not investment advice. Market data can be delayed or wrong; verify before acting.*
