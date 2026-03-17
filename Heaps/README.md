# Heaps

This folder contains implementations of **heap** data structures, which are the foundation of efficient priority queues.

## What is a Heap?

A heap is a tree-based data structure that satisfies the heap property: the key of each node is greater than (max-heap) or less than (min-heap) the keys of its children. This allows the minimum or maximum element to be found in O(1) time, and inserted or removed in O(log n) time.

## Data Structures Included

### Binary Heap (`Heap.h`)
A classic array-based binary heap supporting:
- **Insert** a new element
- **Find-min/max** in O(1)
- **Delete-min/max** in O(log n)
- **Build heap** from an unsorted array in O(n)

Used as the basis for heapsort and Dijkstra's shortest-path algorithm.

### Indexed Heap (`IndexedHeap.h`)
An extension of the binary heap that keeps track of element positions, enabling efficient **decrease-key** and **increase-key** operations in O(log n). This is essential for algorithms like Dijkstra's and Prim's where edge weights are updated dynamically.

## Files

| File | Description |
|------|-------------|
| `Heap.h` | Binary heap (min/max priority queue) |
| `IndexedHeap.h` | Indexed heap with decrease/increase-key |
| `HeapTestAuto.h` | Automated test helpers |
| `test.cpp` | Test driver |

## Usage

Compile and run `test.cpp` to exercise the heap tests:

```bash
g++ -O2 -o test test.cpp && ./test
```
