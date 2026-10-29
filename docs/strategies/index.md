---
hide:
  - toc
---

# Strategies

All strategies are tested with the same process (see [Methodology](../methodology.md)), so results are comparable.

<div class="nowrap-first nowrap-last strong-first" markdown>

| Ref | Strategy | Hypothesis | Out-of-sample Sharpe (after costs) | Status |
|-----|----------|------------|------------------------------------|--------|
| HR-001 | [Lead-Lag Centrality](lead-lag-centrality.md)<br><small>US tech / semiconductor equities</small> | Hub stocks in a rolling-correlation network lead their neighbours | 0.45<br><small>equal-weight 1.58, S&P 500 1.21</small> | Negative result |
| HR-002 | [News Sentiment](news-sentiment.md)<br><small>US large-cap equities</small> | Clearly positive (negative) news keeps moving a stock's abnormal return after the headline | Daily -0.34<br><small>equal-weight 0.94</small><br>Intraday -3.74<br><small>equal-weight 1.18</small> | Negative result |
| HR-003 | [Sector Residual Reversion](sector-residual-reversion.md)<br><small>US large-cap equities</small> | The part of a stock's move that its sector ETF does not explain reverses the next day | -4.02<br><small>SPY buy-and-hold 0.98, equal-weight sector ETFs 0.79; before costs -0.24</small> | Negative result |

</div>
