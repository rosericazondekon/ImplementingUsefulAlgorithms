# Utils

This folder contains **core utility data structures and helper functions** used throughout the library.

## What's Included

### Dynamic Array / Vector (`Vector.h`)
A resizable array similar to `std::vector`. Supports O(1) amortized append, O(1) random access, and O(n) insertion/removal. The foundation of most other data structures in this library.

### Stack (`Stack.h`)
A last-in, first-out (LIFO) container. Supports push, pop, and peek in O(1). Used in DFS, expression evaluation, and backtracking algorithms.

### Queue (`Queue.h`)
A first-in, first-out (FIFO) container. Supports enqueue and dequeue in O(1). Used in BFS and producer-consumer patterns.

### Union-Find / Disjoint Set (`UnionFind.h`)
Maintains a collection of disjoint sets, supporting:
- **Union**: Merge two sets
- **Find**: Identify which set an element belongs to (with path compression and union by rank, both operations are nearly O(1) amortized)

Used in Kruskal's minimum spanning tree, connected components, and network connectivity queries.

### Bit Manipulation (`Bits.h`)
Utilities for common bit-level operations: counting set bits (popcount), finding the lowest/highest set bit, bit reversal, and more. Often maps to single CPU instructions.

### Bitset (`Bitset.h`)
A compact fixed-size array of bits where each element uses exactly 1 bit of storage. Supports fast bitwise AND, OR, XOR operations. Useful for set operations, filters, and dynamic programming over subsets.

### GC-Free Freelist (`GCFreeList.h`)
A memory allocator that reuses freed objects from a pool without relying on the garbage collector. Reduces allocation overhead in performance-critical code.

### General Utilities (`Utils.h`)
Miscellaneous helper functions used across the library (min/max, swap, random utilities, etc.).

### Debugging Helpers (`Debug.h`)
Utilities for printing data structures, assertions, and runtime diagnostics during development.

## Files

| File | Description |
|------|-------------|
| `Utils.h` | General-purpose helper functions |
| `Vector.h` | Dynamic resizable array |
| `Stack.h` | LIFO stack |
| `Queue.h` | FIFO queue |
| `UnionFind.h` | Disjoint set (union-find) structure |
| `Bits.h` | Bit manipulation utilities |
| `Bitset.h` | Compact bitset |
| `Debug.h` | Debugging helpers |
| `GCFreeList.h` | GC-free memory pool allocator |
| `UtilsTestAuto.h` | Automated test helpers |
| `testBasics.cpp` | Test driver for basic data structures |
| `testBits.cpp` | Test driver for bit utilities |
| `testUF.cpp` | Test driver for union-find |

## Usage

Compile and run the test files:

```bash
g++ -O2 -o testBasics testBasics.cpp && ./testBasics
g++ -O2 -o testBits testBits.cpp && ./testBits
g++ -O2 -o testUF testUF.cpp && ./testUF
```
