# Strategy 01: Lead-Lag Centrality

**Status:** To improve  
**Asset class:** US tech / semiconductor equities  
**Code:** [lead-lag-centrality-strategy](https://github.com/NakulPillai2407/lead-lag-centrality-strategy)  
**Report:** TODO: add PDF (`capstone_report.pdf` in the code repo)  
**Playground:** not yet built

!!! warning "Headline result"
    Out of sample, this strategy does not beat the equal-weight or S&P 500 benchmarks. This page documents the idea, the method and why it fell short, as a first entry in the research process.

## 1. Hypothesis

In a network of stocks built from rolling correlations, highly connected "hub" stocks may react to information first, and their less central neighbours may follow with a delay. If so, a large move in a hub could predict the short-term return of its neighbours.

## 2. Data and universe

- US tech and semiconductor stocks.
- Prices downloaded with `yfinance` (cached copies are in the code repo's `data/` folder).
- TODO: state the exact universe, date range, and how survivorship and look-ahead bias were handled.

## 3. Signal construction

- Build a weekly network from rolling correlations (60-day window, 0.5 correlation threshold).
- Rank stocks by degree centrality and take the top 6 as hubs.
- A shock is triggered when a hub's return exceeds 2x its trailing 60-day volatility.
- On a shock, trade the basket of that hub's neighbours and hold for 3 days.
- Transaction costs of 10 bps are applied.

## 4. Backtest results

The last 12 months are held out as the out-of-sample period.

| Metric | In-sample | Out-of-sample | Benchmark |
|--------|-----------|---------------|-----------|
| Annualised return | TODO | TODO | TODO |
| Sharpe ratio | TODO | TODO | TODO |
| Max drawdown | TODO | TODO | TODO |

TODO: add the equity curve and fill in the table from the notebook.

## 5. Robustness

TODO: parameter sensitivity (window, threshold, number of hubs, hold period) and sensitivity to transaction costs.

## 6. What went wrong / limitations

- The strategy does not beat benchmarks out of sample.
- TODO: discuss why (signal decay, crowding, small number of events, cost sensitivity, regime dependence).

## 7. Next steps

TODO: ideas to improve it (for example alternative centrality measures, different shock definitions, other universes).

## 8. Links

- [Code repository](https://github.com/NakulPillai2407/lead-lag-centrality-strategy)
- Report PDF: TODO
