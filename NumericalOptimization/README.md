# NumericalOptimization

This folder contains implementations of **continuous optimization algorithms** — methods for finding the minimum or maximum of a function over a continuous domain.

## What is Numerical Optimization?

Many real-world problems require minimizing a cost function (e.g., fitting a model to data, minimizing energy, or maximizing profit). When the function has no analytical solution, numerical optimization algorithms iteratively improve an estimate of the optimal solution.

## Algorithms Included

### Local Optimization (finds a nearby local minimum)

- **L-BFGS** (`LBFGS.h`): Limited-memory Broyden–Fletcher–Goldfarb–Shanno. A quasi-Newton method that uses gradient information to converge rapidly. Widely used for training machine learning models.
- **Nelder-Mead** (`NelderMead.h`): A derivative-free simplex method. Works even when the gradient is unavailable or noisy. Robust but slower than gradient-based methods.
- **Coordinate Descent** (`CoordinateDescent.h`): Minimizes by repeatedly optimizing one variable at a time while holding all others fixed. Simple and effective for Lasso and other separable problems.
- **SPSA** (`SPSA.h`): Simultaneous Perturbation Stochastic Approximation. Estimates the gradient using only two function evaluations regardless of the number of parameters. Useful for noisy or black-box functions.
- **Golden Section Search** (`GoldenSection.h`): Efficiently finds the minimum of a unimodal function on a 1D interval.

### Global Optimization (searches for the global best)

- **Differential Evolution** (`DifferentialEvolution.h`): A population-based evolutionary algorithm that evolves a set of candidate solutions. Effective for high-dimensional, non-convex problems.
- **Discrete Global Optimization** (`DiscreteGlobalOptimization.h`): Optimization over discrete (integer or categorical) variables.
- **Global Numerical Optimization** (`GlobalNumericalOptimization.h`): Additional global search strategies.
- **Metaheuristic Wrappers** (`MetaheuristicWrappers.h`): Common interface to plug in various metaheuristics.

### Linear Programming (`LinearProgramming.h`)
Finds the optimum of a linear objective subject to linear constraints (e.g., maximize profit given resource constraints). Uses the simplex method or interior-point methods.

### Combined Interface (`NumericalOptimization.h`)
Unified interface for selecting and calling the above optimization methods.

## Files

| File | Description |
|------|-------------|
| `NumericalOptimization.h` | Unified optimization interface |
| `LBFGS.h` | L-BFGS quasi-Newton optimizer |
| `NelderMead.h` | Nelder-Mead simplex optimizer |
| `CoordinateDescent.h` | Coordinate descent optimizer |
| `SPSA.h` | SPSA stochastic gradient estimator |
| `GoldenSection.h` | Golden section 1D line search |
| `GlobalNumericalOptimization.h` | Global optimization strategies |
| `DifferentialEvolution.h` | Differential evolution (population-based) |
| `DiscreteGlobalOptimization.h` | Discrete/integer global optimization |
| `LinearProgramming.h` | Linear programming (simplex method) |
| `MetaheuristicWrappers.h` | Metaheuristic algorithm wrappers |
| `testOpt.cpp` | Test driver for general optimization |
| `testOpt1D.cpp` | Test driver for 1D optimization |
| `testOptGlobal.cpp` | Test driver for global optimization |
| `testLinearProgramming.cpp` | Test driver for linear programming |
| `testOptCommon.h` | Shared test utilities |

## Usage

Compile and run the test files:

```bash
g++ -O2 -o testOpt testOpt.cpp && ./testOpt
g++ -O2 -o testLinearProgramming testLinearProgramming.cpp && ./testLinearProgramming
```
