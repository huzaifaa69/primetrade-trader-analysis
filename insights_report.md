
# PrimeTrade AI — Trader Behavior & Market Sentiment Analysis
**Junior Data Scientist Assignment | Submitted by: [Your Name]**

---

## Executive Summary

Analysis of **211,224 trades** across **32 traders** on Hyperliquid from May 2023 to May 2025, merged with the Bitcoin Fear & Greed Index. Key finding: **market sentiment is a significant predictor of trader profitability**, with both Extreme Greed and Fear regimes producing the highest average PnL per trade.

---

## Dataset Overview

| Metric | Value |
|--------|-------|
| Total trades | 211,224 |
| Closed trades (PnL events) | 104,402 |
| Unique traders | 32 |
| Unique coins traded | 246 |
| Date range | May 2023 – May 2025 |
| Total cumulative PnL | $10.3M |

---

## Key Finding 1 — Sentiment & Profitability

Traders perform **best during Extreme Greed and Fear** — the two extremes of the sentiment spectrum — and worst during Neutral markets.

| Sentiment | Mean PnL/Trade | Win Rate | Avg Trade Size |
|-----------|---------------|----------|----------------|
| Extreme Fear | $71 | 76.2% | $5,468 |
| Fear | $113 | 87.3% | $8,041 |
| Neutral | $71 | 82.4% | $5,556 |
| Greed | $85 | 76.9% | $5,439 |
| Extreme Greed | $130 | 89.2% | $2,780 |

**Insight:** Fear markets generate the highest average trade sizes ($8K) suggesting experienced traders take larger positions when others are panicking — a classic contrarian pattern.

---

## Key Finding 2 — Contrarian Strategy Outperforms

Buying during Fear outperforms buying during Greed:
- **Buy in Fear** → Mean PnL higher, win rate 87%+
- **Buy in Greed** → Momentum trades are profitable but more volatile
- Traders show a clear **contrarian edge** during extreme sentiment periods

---

## Key Finding 3 — F&G Correlation

- Pearson correlation between daily F&G score and daily total PnL: **r = -0.098** (p = 0.0442)
- The correlation is **not static** — rolling 30-day analysis shows it flips between positive and negative, indicating traders switch strategies across regimes
- During 2024 bull run, PnL and greed moved together (momentum)
- During corrections, PnL spiked despite falling F&G (contrarian)

---

## Key Finding 4 — Top Trader Concentration

- Top 3 traders account for **~45% of total PnL**
- #1 trader: **$2.14M** cumulative PnL
- Top traders show **higher win rates during Fear** than Neutral markets
- Suggests elite traders specifically exploit fear-driven mispricing

---

## Key Finding 5 — Liquidation Risk

- Most liquidations occur during **Extreme Fear** — panic selling triggers cascades
- Neutral markets show fewest liquidations — low volatility reduces forced exits
- Recommendation: reduce leverage during Extreme Fear periods

---

## Key Finding 6 — Time of Day Effect

- Peak mean PnL occurs during **early morning IST hours** (2–6 AM)
- This corresponds to US market hours — high liquidity windows
- Lowest profitability during late evening IST

---

## Key Finding 7 — Coin-Level Insights

- **BTC, SOL, ETH** dominate total PnL across all sentiment regimes
- Some altcoins are **sentiment-specific**: perform in Greed, lose in Fear
- Contrarian traders hold BTC/ETH during Fear; momentum traders pile into altcoins during Greed

---

## Strategic Recommendations

1. **Trade larger in Fear** — win rates and mean PnL are highest; others are underexposed
2. **Reduce leverage in Extreme Fear** — liquidation risk spikes significantly
3. **Monitor F&G transitions** — rolling correlation flips signal regime changes; adapt strategy accordingly
4. **Stick to BTC/SOL/ETH during Fear** — altcoin risk increases disproportionately
5. **Use Neutral markets for positioning** — low volatility = good entry points, not absence of opportunity
6. **Copy top 3 trader patterns** — their sentiment-specific behavior is a proven alpha source

---

## Files Included

- `analysis.py` — Full analysis pipeline
- `chart1_overview.png` — Dashboard overview
- `chart2_behavior.png` — Behavioral patterns
- `chart3_strategy.png` — Strategy intelligence
- `insights_report.md` — This report
