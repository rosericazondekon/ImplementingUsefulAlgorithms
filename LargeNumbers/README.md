# LargeNumbers

This folder contains implementations of **arbitrary-precision (big integer) arithmetic** — calculations on numbers that are too large to fit in a standard 64-bit integer.

## What is Arbitrary-Precision Arithmetic?

Standard integer types (e.g., `int`, `long long`) hold numbers up to about 9.2 × 10¹⁸. Arbitrary-precision arithmetic lifts this limit by representing numbers as arrays of digits, enabling exact computation on numbers of any size. This is used in cryptography (RSA key generation), scientific computing, and financial systems that require exact decimal results.

## Data Structures Included

### Large Integer (`LargeNumber.h`)
Supports exact arithmetic on integers of arbitrary size:
- Addition, subtraction, multiplication, division, modulo
- Comparison operators
- Power and greatest common divisor (GCD)

### Large Rational Number (`LargeRational.h`)
Represents fractions as exact ratios of two large integers (numerator / denominator). Arithmetic on rationals is always exact — no floating-point rounding errors — making it useful for symbolic computation and exact algorithms.

## Files

| File | Description |
|------|-------------|
| `LargeNumber.h` | Arbitrary-precision integer arithmetic |
| `LargeRational.h` | Exact rational arithmetic using large integers |
| `LargeNumberTestAuto.h` | Automated test helpers |
| `test.cpp` | Test driver |

## Usage

Compile and run `test.cpp` to exercise the large number tests:

```bash
g++ -O2 -o test test.cpp && ./test
```
