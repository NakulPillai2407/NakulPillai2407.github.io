# Methodology

Every strategy here is tested to the same standard, and the standard gets stricter as the project goes on. This page describes the process as it is actually practised, including where earlier strategies fell short of it.

## Principles

1. **Hypothesis first.** Each idea starts with an economic reason it might work and, just as importantly, a written list of results that would prove it wrong. This is done before any backtest is run.
2. **Freeze before testing.** Every parameter is fixed in advance: lookback windows, thresholds, holding periods, cost assumptions and the decision rule. Anything changed afterwards is logged as a deviation, and results that depend on it are labelled exploratory.
3. **A holdout that is used once.** The final stretch of data, usually the last 12 months, is kept out of the whole design process. It is evaluated a single time, after everything is frozen. If a result disappoints, the holdout is not reused to tune the strategy. A new hypothesis needs new data.
4. **Test the code before the data.** Each backtest is first run on simulated data. A planted effect must be recovered, and a world with no effect must produce nothing. Only then is it run on real returns.
5. **Costs and benchmarks decide.** The headline number is the Sharpe ratio after transaction costs, compared with simply holding the same stocks (equal-weight) and with a market index. Before-cost results are shown too, because they separate "no signal" from "a signal that costs eat".
6. **Report uncertainty.** Key results come with confidence intervals (bootstrap) or standard errors that allow for autocorrelation (Newey-West), not bare point estimates.
7. **Publish the failures.** Every idea and every variant goes in the [Research Log](research-log.md), whether it worked or not.

## Standard testing process

| Step | What is done |
|------|--------------|
| Data | Source, period and universe stated; look-ahead traced step by step; survivorship bias flagged where the universe is today's stocks |
| Pre-registration | Hypothesis, parameters and decision rule written down and frozen; "what would prove it wrong" stated |
| Splits | An in-sample period for design and a single-use holdout for evaluation |
| Code validation | Planted-effect and no-effect simulations before any real data |
| Costs | A proportional cost per trade, plus a sweep at higher costs |
| Metrics | Annualised return, volatility, Sharpe ratio, maximum drawdown, turnover |
| Benchmarks | Equal-weight holding of the same stocks, plus a relevant market index |
| Inference | Bootstrap intervals and Newey-West t-statistics on the holdout |
| Robustness | Parameter sweeps and alternative specifications, labelled exploratory unless pre-registered |
| Write-up | Full report with limitations; deviations and failures stated |

## How closely each strategy followed it

The process has been tightened over time, so earlier strategies met less of it. This is stated rather than hidden.

| Step | HR-001 | HR-002 | HR-003 |
|------|:------:|:------:|:------:|
| Parameters frozen before testing | Yes | Mostly (first design replaced after results; logged) | Yes (pre-registered) |
| Single-use holdout | Yes | Yes | Yes |
| Planted-effect and null simulation | No | Yes | Yes |
| Bootstrap intervals / Newey-West | No | Partly | Yes |
| Cost sensitivity | Yes | Yes | Yes |
| Benchmarks compared | Yes | Yes | Yes |

## Multiple testing

The more variants that are tried, the more likely one looks good by chance. Every variant tried is recorded in the [Research Log](research-log.md), and results are interpreted with that in mind. For example, two of 16 horizon estimates in [HR-002](strategies/news-sentiment.md) had p below 0.05, which is about what chance gives. Sweeps that were not pre-registered are labelled exploratory and are never used to claim a result. Adjustments such as the deflated Sharpe ratio will be added as the number of trials grows.
