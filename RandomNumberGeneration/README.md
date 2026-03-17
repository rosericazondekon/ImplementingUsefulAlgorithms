# RandomNumberGeneration

This folder contains implementations of **random number generation**, **statistical methods**, and **simulation** techniques.

## What's Included

### Random Number Generators (`Generators.h`, `Random.h`)
Pseudo-random number generators (PRNGs) that produce sequences of numbers that appear statistically random:
- Fast generators (Mersenne Twister, Xorshift)
- Generators for common probability distributions (uniform, normal, exponential, Poisson, etc.)

### Quasi-Random (Low-Discrepancy) Sequences (`Sobol.h`)
Sobol sequences fill a space more uniformly than pseudo-random numbers. They are used in numerical integration and Monte Carlo simulations to converge faster.

### Statistics (`Statistics.h`)
Descriptive statistics: mean, variance, standard deviation, quantiles, histograms, and more.

### Bootstrapping and Resampling (`Bootstrap.h`)
Estimates confidence intervals and standard errors by repeatedly resampling from a dataset. No assumptions about the underlying distribution are needed.

### Markov Chain Monte Carlo (`MCMC.h`)
MCMC algorithms (e.g., Metropolis-Hastings) draw samples from complex probability distributions that cannot be sampled directly. Used in Bayesian inference, statistical physics, and machine learning.

### Time Series Generation (`TimeSeries.h`)
Generates synthetic time series data with specified autocorrelation, trends, and seasonality. Useful for testing and simulation.

### Correlation (`Correlation.h`)
Computes Pearson and Spearman correlation coefficients and covariance matrices.

### Statistical Testing
- **Distribution Tests** (`DistributionTests.h`): Tests whether data follows a specified distribution (chi-squared goodness-of-fit, Kolmogorov-Smirnov).
- **Permutation Tests** (`PermutationTests.h`): Non-parametric hypothesis tests based on random permutations of the data.
- **Multiple Comparison** (`MultipleComparison.h`): Controls false discovery rate when performing many simultaneous hypothesis tests (Bonferroni, Benjamini-Hochberg).

### Sensitivity Analysis (`SensitivityAnalysis.h`)
Determines how much each input variable contributes to the variability of a model's output (Sobol indices, Morris method).

### Optimal Computing Budget Allocation (`OCBA.h`)
Efficiently allocates simulation runs across alternatives to find the best one with a given computational budget.

## Files

| File | Description |
|------|-------------|
| `Generators.h` | Pseudo-random number generators |
| `Random.h` | Distribution samplers (normal, exponential, etc.) |
| `Sobol.h` | Quasi-random Sobol sequences |
| `Statistics.h` | Descriptive statistics utilities |
| `Bootstrap.h` | Bootstrap resampling |
| `MCMC.h` | Markov Chain Monte Carlo sampling |
| `TimeSeries.h` | Synthetic time series generation |
| `Correlation.h` | Correlation and covariance computation |
| `DistributionTests.h` | Goodness-of-fit tests |
| `PermutationTests.h` | Non-parametric permutation tests |
| `MultipleComparison.h` | Multiple comparison correction |
| `SensitivityAnalysis.h` | Sensitivity / variance decomposition |
| `OCBA.h` | Optimal computing budget allocation |
| `CircleArea.py` | Python utility for Monte Carlo π estimation |
| `*TestAuto.h` | Automated test helpers |
| `test*.cpp` | Test drivers |

## Usage

Compile and run the test files:

```bash
g++ -O2 -o testRNG test.cpp && ./testRNG
```
