# Strategies

All strategies are tested with the same process (see [Methodology](../methodology.md)), so results are comparable.

| # | Strategy | Asset class | Hypothesis | Sample | Out-of-sample Sharpe (after costs) | Status |
|---|----------|-------------|------------|--------|-------------------------------------|--------|
| 01 | [Lead-Lag Centrality](lead-lag-centrality.md) | US tech / semiconductor equities | Hub stocks in a rolling-correlation network lead their neighbours | 2019 to 2026, 56 stocks; last 12 months held out | 0.45 (equal-weight 1.58, S&P 500 1.21) | Negative result |
| 02 | [News Sentiment](news-sentiment.md) | US large-cap equities | Clearly positive (negative) news keeps moving a stock's abnormal return after the headline | Daily test 2021 to 2023 and intraday test 2024 to 2026, 50 stocks each; last 12 months held out | Daily -0.34 (equal-weight 0.94); intraday -3.74 (equal-weight 1.18) | Negative result |
| 03 | [Sector Residual Reversion](sector-residual-reversion.md) | US large-cap equities | The part of a stock's move that its sector ETF does not explain reverses the next day | 2018 to 2026, S&P 500 members point in time; last 2.75 years (2024-01 to 2026-09) held out | -4.02 (SPY buy-and-hold 0.98, equal-weight sector ETFs 0.79); gross -0.24 | Negative result |

## Adding a strategy

Copy [the strategy template](template.md) and fill in each section.
