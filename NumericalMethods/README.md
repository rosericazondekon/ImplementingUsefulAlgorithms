# NumericalMethods

This folder contains implementations of **numerical analysis** algorithms for solving mathematical problems that have no closed-form solution, or where exact computation is impractical.

## Algorithms Included

### Matrix Operations (`Matrix.h`, `SparseMatrix.h`)
Dense and sparse matrix data structures with:
- Matrix multiplication, transposition, inversion
- LU decomposition and Gaussian elimination for solving systems of linear equations Ax = b
- Sparse representation for large, mostly-zero matrices (common in physical simulations and graph problems)

### Fast Fourier Transform (`FFT.h`)
The FFT computes the Discrete Fourier Transform (DFT) in O(n log n) instead of O(n²). It decomposes a signal into its constituent frequencies, used in audio processing, image compression (JPEG), polynomial multiplication, and signal analysis.

### Numerical Integration (`Integration.h`)
Approximates definite integrals (areas under curves) when no analytical formula exists:
- Trapezoidal rule, Simpson's rule
- Gaussian quadrature for high accuracy

### Numerical Differentiation (`Differentiation.h`)
Approximates derivatives of functions using finite differences. Used when the analytical derivative is unavailable or difficult to compute.

### Interpolation and Splines (`Interpolation.h`, `CubicSpline.h`)
Constructs smooth curves passing through or near a set of data points:
- **Polynomial interpolation** (Lagrange, Newton)
- **Cubic splines** for smooth piecewise interpolation, used in computer graphics and data smoothing

### Equation and Root Solving (`EquationSolving.h`, `AllRootsFinder.h`)
Finds values of x where f(x) = 0:
- Bisection, Newton-Raphson, secant methods
- Finds all real roots of a function in an interval

### ODE Solving (`ODESolving.h`)
Numerically integrates ordinary differential equations (ODEs) of the form dy/dx = f(x, y):
- Euler, Runge-Kutta methods
- Used in physics simulations, population models, and engineering

### Interval Arithmetic (`IntervalNumber.h`)
Represents numbers as intervals [lo, hi] and propagates bounds through calculations, providing guaranteed error bounds on numerical results.

## Files

| File | Description |
|------|-------------|
| `Matrix.h` | Dense matrix with linear algebra operations |
| `SparseMatrix.h` | Sparse matrix for large, mostly-zero matrices |
| `FFT.h` | Fast Fourier Transform |
| `Integration.h` | Numerical integration (quadrature) |
| `Differentiation.h` | Numerical differentiation (finite differences) |
| `Interpolation.h` | Polynomial interpolation |
| `CubicSpline.h` | Cubic spline interpolation |
| `EquationSolving.h` | Root-finding algorithms |
| `AllRootsFinder.h` | Finds all roots in an interval |
| `ODESolving.h` | ODE numerical integrators |
| `IntervalNumber.h` | Interval arithmetic for error bounds |
| `*TestAuto.h` | Automated test helpers |
| `test*.cpp` | Test drivers for each component |

## Usage

Compile and run individual test files:

```bash
g++ -O2 -o testMatrix testMatrix.cpp && ./testMatrix
g++ -O2 -o testFFT testFFT.cpp && ./testFFT
# ...and so on for other test files
```
