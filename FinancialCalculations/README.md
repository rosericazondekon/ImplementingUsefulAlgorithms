# FinancialCalculations

This folder contains implementations of **financial mathematics algorithms** for pricing, analysis, and portfolio optimization.

## Algorithms Included

### Annuity Calculations (`Annuity.h`)
Compute the present and future value of annuities — streams of regular cash payments. Used for loan amortization, pension planning, and valuing bonds.

### Cash Flow Analysis (`CashFlows.h`)
Compute Net Present Value (NPV) and Internal Rate of Return (IRR) for a series of cash flows. These are the core tools of capital budgeting and investment appraisal.

### Option Pricing (`OptionPricing.h`)
Price financial derivatives such as European and American options using models like Black-Scholes and binomial trees. Options give the holder the right (but not obligation) to buy or sell an asset at a set price.

### Mean-Variance Portfolio Optimization (`MeanVarianceOptimization.h`)
Implements Harry Markowitz's Modern Portfolio Theory: given a set of assets with expected returns and a covariance matrix, find the portfolio allocation that maximizes return for a given level of risk (or minimizes risk for a given return). This traces out the "efficient frontier."

### Portfolio Simulation (`PortfolioSimulation.h`)
Uses Monte Carlo simulation to model the future value of a portfolio under uncertainty, accounting for randomness in asset returns.

### Miscellaneous Financial Utilities (`Misc.h`)
Additional helper routines for common financial computations.

## Files

| File | Description |
|------|-------------|
| `Annuity.h` | Annuity present/future value calculations |
| `CashFlows.h` | NPV and IRR for cash flow streams |
| `OptionPricing.h` | Black-Scholes and binomial option pricing |
| `MeanVarianceOptimization.h` | Markowitz mean-variance portfolio optimization |
| `PortfolioSimulation.h` | Monte Carlo portfolio simulation |
| `Misc.h` | Miscellaneous financial helper routines |
| `FinancialCalculationsTestAuto.h` | Automated test helpers |
| `test.cpp` | Test driver |

## Usage

Compile and run `test.cpp` to exercise the financial calculation tests:

```bash
g++ -O2 -o test test.cpp && ./test
```
