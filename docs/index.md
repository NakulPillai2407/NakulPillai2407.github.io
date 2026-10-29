# Holdout Research

An independent systematic strategy research lab: each idea starts with an economic hypothesis, is tested on data it was never designed on (the holdout), and is written up honestly, including when it doesn't work.

!!! note "What this is"
    A personal project by [Nakul Pillai](about.md), built alongside an MSc in Financial Technology at Imperial College London. It is not a company or a live trading operation.

## Strategies

| # | Strategy | Asset class | Hypothesis | Out-of-sample result | Status |
|---|----------|-------------|------------|----------------------|--------|
| 01 | [Lead-Lag Centrality](strategies/lead-lag-centrality.md) | US tech / semiconductor equities | Highly connected hub stocks lead their neighbours | Sharpe 0.45 vs 1.58 for equal-weight; no multi-day lag found | Negative result |
| 02 | [News Sentiment](strategies/news-sentiment.md) | US large-cap equities | Clearly positive (negative) news keeps moving a stock's abnormal return after the headline | Daily Sharpe -0.34 vs 0.94 for equal-weight; intraday -3.74 vs 1.18 | Negative result |
| 03 | [Sector Residual Reversion](strategies/sector-residual-reversion.md) | US large-cap equities | The part of a stock's move that its sector ETF does not explain reverses the next day | Sharpe -4.02 after costs, -0.24 before; reversal coefficient t = -0.66 | Negative result |

More strategies will be added as they are built. See the [Research Log](research-log.md) for every idea tried, including the ones that failed.

## How it works

Every strategy goes through the same process, described in the [Methodology](methodology.md): out-of-sample testing, transaction costs, robustness checks, and a section on where it breaks.

## Tools

Interactive playgrounds let you change parameters and see how fragile a result is. See [Tools](tools.md).
