# Sorting

This folder contains implementations of **sorting algorithms** — methods for arranging a sequence of elements in order.

## What is Sorting?

Sorting is one of the most fundamental operations in computer science. Efficient sorting enables fast searching, data deduplication, and is a building block for many other algorithms (merge sort, quicksort, and heapsort underlie much of the standard library). Algorithms differ in their worst-case time complexity, memory usage, stability (whether equal elements keep their original order), and performance on already-sorted or nearly-sorted data.

## Algorithms Included (`Sort.h`)

### Comparison-Based Sorting
- **Quicksort**: Average O(n log n), in-place. Fast in practice; used in many standard library implementations.
- **Mergesort**: Worst-case O(n log n), stable. Requires O(n) extra memory.
- **Heapsort**: Worst-case O(n log n), in-place but not stable.
- **Insertion Sort**: O(n²) but very fast for nearly-sorted data or small arrays.

### Non-Comparison Sorting
- **Radix Sort**: O(nk) where k is the number of digits/passes. Faster than comparison sorts for integers with bounded values.
- **Counting Sort**: O(n + k) for small integer ranges.

## Files

| File | Description |
|------|-------------|
| `Sort.h` | All sorting algorithm implementations |
| `SortTestAuto.h` | Automated test helpers |
| `testSort.cpp` | Test driver |

## Usage

Compile and run `testSort.cpp` to exercise the sorting tests:

```bash
g++ -O2 -o testSort testSort.cpp && ./testSort
```
