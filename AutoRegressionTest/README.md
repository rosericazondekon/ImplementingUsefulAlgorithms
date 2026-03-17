# AutoRegressionTest

This folder contains the **automated regression test runner** for the entire library. It compiles and runs all of the automated test suites from every other module in a single pass to verify that nothing is broken.

## What is Regression Testing?

Regression testing checks that existing functionality still works correctly after changes are made to the codebase. Running all tests together makes it easy to catch any unintended side effects when modifying shared utilities or algorithms.

## How it Works

`test.cpp` includes the `*TestAuto.h` header from each module and calls the corresponding `testAllAuto*()` function. Each function runs a battery of assertions on the algorithms in that module. If any assertion fails the program prints an error and stops; if all pass, it prints `"All Tests Auto passed"`.

The following modules are exercised:

| Module | Test Function Called |
|--------|---------------------|
| Utils | `testAllAutoUtils()` |
| Sorting | `testAllAutoSort()` |
| RandomTreap | `testAllAutoDynamicSortedSequence()` |
| HashTable | `testAllAutoHashTable()` |
| Heaps | `testAllAutoHeaps()` |
| Graphs | `testAllAutoGraphs()` |
| ExternalMemoryAlgorithms | `testAllAutoExternalMemoryAlgorithms()` |
| StringAlgorithms | `testAllAutoStringAlgorithms()` |
| Compression | `testAllAutoCompression()` |
| MiscAlgs | `testAllAutoMiscAlgorithms()` |
| Optimization | `testAllAutoOpt()` |
| LargeNumbers | `testAllAutoLargeNumbers()` |
| ComputationalGeometry | `testAllAutoComputationalGeometry()` |
| ErrorCorrectingCodes | `testAllAutoErrorCorrectingCodes()` |
| Cryptography | `testAllAutoCryptography()` |
| NumericalMethods | `testAllAutoNumericalMethods()` |
| FinancialCalculations | `testAllAutoFinancialCalculations()` |

## Files

| File | Description |
|------|-------------|
| `test.cpp` | Automated regression test runner that exercises all library modules |

## Usage

Compile and run `test.cpp` from the `AutoRegressionTest/` directory:

```bash
g++ -O2 -o test test.cpp && ./test
```

A successful run prints `"All Tests Auto passed"` at the end. Any failure prints the failing test name and stops execution.
