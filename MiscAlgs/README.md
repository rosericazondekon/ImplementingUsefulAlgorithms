# MiscAlgs

This folder contains a collection of **miscellaneous algorithms and data structures** that are widely useful but don't fit neatly into a single category.

## Algorithms and Data Structures Included

### Fenwick Tree / Binary Indexed Tree (`FenwickTree.h`)
A space-efficient data structure that supports prefix sum queries and point updates in O(log n) time. It is used for range sum queries, order statistics, and counting inversions. Despite its simplicity, it is significantly faster in practice than a segment tree for 1D prefix sum problems.

### Prime Sieve (`PrimeTable.h`)
Generates all prime numbers up to a given limit using the **Sieve of Eratosthenes** or a segmented sieve. Used in number theory, cryptography, and factorization.

### Combinatorial Generation (`CombinatorialGeneration.h`)
Generates all permutations, combinations, subsets, and other combinatorial structures. Useful for exhaustive search, testing, and counting problems.

### K-Bit Word Vector (`KBitWordVector.h`)
A compact array that stores integers using exactly *k* bits each (where k < 64). Saves memory when elements have a known bounded range.

### Interval Set Union (`IntervalSetUnion.h`)
Maintains a dynamic set of non-overlapping intervals, supporting merging overlapping intervals and querying membership. Used in calendar scheduling, range compression, and string matching.

### LRU Cache (`LRUCache.h`)
A **Least Recently Used** cache with O(1) get and put operations. The LRU policy evicts the least recently accessed item when the cache is full. Used in web browsers, database buffer pools, and operating system page caches.

## Files

| File | Description |
|------|-------------|
| `CombinatorialGeneration.h` | Permutation, combination, and subset generators |
| `FenwickTree.h` | Fenwick tree for efficient prefix sum queries |
| `PrimeTable.h` | Prime sieve for generating prime numbers |
| `KBitWordVector.h` | Compact k-bit integer array |
| `IntervalSetUnion.h` | Dynamic interval set with union operations |
| `LRUCache.h` | Least Recently Used cache |
| `MiscAlgsTestAuto.h` | Automated test helpers |
| `test.cpp` | Test driver |
| `testIntervalSetUnion.cpp` | Test driver for interval set union |

## Usage

Compile and run the test files:

```bash
g++ -O2 -o test test.cpp && ./test
g++ -O2 -o testIntervalSetUnion testIntervalSetUnion.cpp && ./testIntervalSetUnion
```
