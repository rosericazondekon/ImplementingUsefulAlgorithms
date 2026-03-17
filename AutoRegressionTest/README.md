# AutoRegressionTest

This folder contains an implementation and tests for **autoregressive (AR) models** used in time series analysis and forecasting.

## What is an Autoregressive Model?

An autoregressive model predicts future values in a sequence by assuming that each value is a linear combination of its previous values plus some random noise. For example, an AR(p) model of order *p* uses the last *p* observations to predict the next one. This is commonly used for financial time series, signal processing, and other sequential data.

## Files

| File | Description |
|------|-------------|
| `test.cpp` | Test driver that exercises the autoregressive model implementation |

## Usage

Compile and run `test.cpp` to exercise the autoregressive model tests:

```bash
g++ -O2 -o test test.cpp && ./test
```
