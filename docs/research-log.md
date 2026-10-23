# Research Log

A dated record of every idea tried, including the ones that did not work.

| Date | Idea | Outcome | Notes |
|------|------|---------|-------|
| 2026-10-23 | [Lead-Lag Centrality](strategies/lead-lag-centrality.md) | Negative: does not beat holding the stocks, in or out of sample | Neighbours move with the hub on day 0 (+380 bps) but not after (day 1: -46 bps), so no catch-up to trade |
| 2026-10-23 | Lead-Lag Centrality, correlation threshold 0.4 and 0.6 | Unstable: out-of-sample Sharpe -0.318 at 0.4, 0.453 at 0.5, 0.249 at 0.6 | Only the threshold was varied; 0.5 was fixed in advance, so the positive result should be treated with caution |
