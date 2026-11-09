# The Venetian Edge
### ETF Pair Strategy & Weight Optimization

A quantitative research project that searches for ETF pairs offering genuine diversification,
then finds the portfolio weighting that maximizes risk-adjusted return.

## Overview
Using 8 years of daily data (Aug 2018 – Aug 2026, 2,009 trading days) across 24 ETFs spanning
equities, bonds, commodities, currencies, volatility, real estate, and leveraged/inverse products,
this project:

1. **Screens for negatively correlated pairs** and separates real cross-asset relationships from
   trivial ones (e.g., an ETF paired with its own inverse)
2. **Sweeps every weight from 0–100% in 1% steps** with monthly rebalancing and 5 bp transaction costs
3. **Compares weighting methods**: equal weight, risk parity, minimum variance, beta-neutral,
   maximum diversification, and empirical Sharpe optimization
4. **Validates out-of-sample** with a walk-forward test (fit on the first 60%, tested on the unseen final 40%)
5. **Stress-tests** with block-bootstrap Monte Carlo simulation (3,000 runs per horizon)

## Key Findings
- **Inverse pairs are a decay trade, not a hedge.** A 50/50 QQQ/SQQQ blend lost 83% of its value
  over 8 years due to daily-leverage compounding.
- **Gold (GLD) + US Dollar (UUP) is a real diversifier** (correlation −0.435). Five independent
  weighting methods converge on 22–33% GLD.
- **Recommended allocation: 30% GLD / 70% UUP**, which achieved:

| Metric | GLD/UUP (out-of-sample) | SPY (same window) |
|---|---|---|
| Sharpe ratio | **1.71** | 1.43 |
| CAGR | 12.0% | 22.6% |
| Volatility | **6.8%** | 15.1% |
| Max drawdown | **−7.5%** | −18.8% |

## Limitations
This strategy improves **risk-adjusted** returns, not absolute returns: it underperformed SPY in
65–76% of bootstrapped scenarios during a strong equity bull market. The gold/dollar relationship
is historically grounded but has weakened during some past regimes. This is research, not
investment advice.

## Built With
Python · pandas · NumPy · Matplotlib
