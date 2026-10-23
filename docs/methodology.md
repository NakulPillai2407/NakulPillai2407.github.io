# Methodology

Every strategy on this site is tested the same way, so results can be compared and the weaknesses are visible.

## Principles

1. **Start with a hypothesis.** Each strategy must have an economic reason to work before any backtest is run.
2. **Test out of sample.** A held-out period is never used to choose parameters.
3. **Include costs.** Results are reported after transaction costs, with sensitivity to the cost assumption.
4. **Check robustness.** Parameters are varied to see whether the result survives, not just one tuned setting.
5. **Report failures.** Ideas that do not work are written up, not hidden.

## Standard testing process

| Step | What is done |
|------|--------------|
| Data | Source, period, universe; look-ahead and survivorship bias handled |
| Splits | In-sample for design, held-out period for evaluation (walk-forward where possible) |
| Costs | Proportional transaction cost per trade, plus a sensitivity sweep |
| Metrics | Annualised return, volatility, Sharpe ratio, max drawdown, turnover |
| Benchmarks | Equal-weight and a relevant market index |
| Robustness | Parameter sweeps and sub-period analysis |

## Multiple testing

The more variants that are tried, the more likely one looks good by chance. Every variant tried is recorded in the [Research Log](research-log.md), and results are interpreted with that in mind. Adjustments such as the deflated Sharpe ratio will be added as the number of trials grows.

## Shared engine

TODO: describe the shared backtesting engine (link to the `multi-strategy-backtester` repo) once strategies are ported onto it.
