---
hide:
  - navigation
  - toc
---

# Research Log

A dated record of every idea tried, including the ones that did not work. Newest first.

<div class="nowrap-first" markdown>

| Date | Idea | Outcome | Notes |
|------|------|---------|-------|
| 2026-10-29 | [HR-003 Sector Residual Reversion](strategies/sector-residual-reversion.md), pre-registered one-shot holdout | Negative: NOT SUPPORTED. Reversal coefficient -0.0040 (t = -0.66), gross Sharpe -0.24, net Sharpe at 5 bp -4.02 | No detectable effect before costs, and the book turns over about 1.77 times a day, so costs alone take about 22% a year. Thresholds, holds and sectors were exploratory: every gross interval includes zero and no variant has a positive net Sharpe |
| 2026-10-29 | [HR-002 News Sentiment](strategies/news-sentiment.md), intraday test (exact release times, 1-minute bars) | Negative: in-sample 60-minute coefficient +3.95 bps per unit (p = 0.56), holdout Sharpe -3.74 vs 1.18 | Seven other horizons from 5 to 300 minutes were exploratory: 2 of 16 estimates had p < 0.05, about what chance gives; none beats the cost |
| 2026-10-27 | [HR-002 News Sentiment](strategies/news-sentiment.md), daily test | Negative: holdout Sharpe -0.34 vs 0.94 for equal-weight | The news-direction effect is +110 bps on the article's own day but +9.7 bps the next day (p = 0.30), about the size of the 10 bps cost |
| 2026-10-27 | HR-002 News Sentiment, delayed three-day hold (first design) | Replaced after the first results were seen | The hypothesis was always to trade straight after the news, so the delayed hold was swapped for an entry at the close of the article's date. Logged as a post-hoc deviation, so the holdout result of the replacement is exploratory |
| 2026-10-23 | HR-001 Lead-Lag Centrality, correlation threshold 0.4 and 0.6 | Unstable: holdout Sharpe -0.318 at 0.4, 0.453 at 0.5, 0.249 at 0.6 | Only the threshold was varied; 0.5 was fixed in advance, so the positive result should be treated with caution |
| 2026-10-23 | [HR-001 Lead-Lag Centrality](strategies/lead-lag-centrality.md) | Negative: does not beat holding the stocks, in sample or in the holdout | Neighbours move with the hub on day 0 (+380 bps) but not after (day 1: -46 bps), so no catch-up to trade |

</div>
