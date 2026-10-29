# Research Log

A dated record of every idea tried, including the ones that did not work.

| Date | Idea | Outcome | Notes |
|------|------|---------|-------|
| 2026-10-23 | [Lead-Lag Centrality](strategies/lead-lag-centrality.md) | Negative: does not beat holding the stocks, in or out of sample | Neighbours move with the hub on day 0 (+380 bps) but not after (day 1: -46 bps), so no catch-up to trade |
| 2026-10-23 | Lead-Lag Centrality, correlation threshold 0.4 and 0.6 | Unstable: out-of-sample Sharpe -0.318 at 0.4, 0.453 at 0.5, 0.249 at 0.6 | Only the threshold was varied; 0.5 was fixed in advance, so the positive result should be treated with caution |
| 2026-10-27 | News Sentiment, delayed three-day hold (first design) | Replaced after the first results were seen | The hypothesis was always to trade straight after the news, so the delayed hold was swapped for an entry at the close of the article's date. Logged as a post-hoc deviation, so the held-out result of the replacement is exploratory |
| 2026-10-27 | [News Sentiment](strategies/news-sentiment.md), daily test | Negative: held-out Sharpe -0.34 vs 0.94 for equal-weight | The news-direction effect is +110 bps on the article's own day but +9.7 bps the next day (p = 0.30), about the size of the 10 bps cost |
| 2026-10-29 | [News Sentiment](strategies/news-sentiment.md), intraday test (exact release times, 1-minute bars) | Negative: 60-minute coefficient +3.95 bps per unit (p = 0.56), held-out Sharpe -3.74 vs 1.18 | Seven other horizons from 5 to 300 minutes were exploratory: 2 of 16 estimates had p < 0.05, about what chance gives; none beats the cost |
