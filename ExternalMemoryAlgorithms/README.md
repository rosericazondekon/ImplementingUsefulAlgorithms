# ExternalMemoryAlgorithms

This folder contains implementations of **algorithms and data structures designed to work efficiently when data is too large to fit in main memory (RAM)**.

## What are External Memory Algorithms?

When data sets are larger than available RAM, algorithms must read and write data from disk. The bottleneck shifts from CPU speed to disk I/O. External memory algorithms minimize the number of disk accesses by reading and writing large blocks of data at a time, making them essential for databases, big data processing, and file systems.

## Data Structures Included

### External Memory B-Tree (`EMBTree.h`)
A B-tree optimized for disk storage. Unlike in-memory trees, a B-tree stores many keys per node to match the size of a disk block, reducing the number of disk reads needed to find a value. B-trees are the foundation of most database indexes.

### External Memory Vector (`EMVector.h`)
A dynamic array that transparently spills to disk when the data no longer fits in RAM.

### External Memory Freelist (`EMFreelist.h`)
A memory management structure that tracks free blocks in an on-disk data store, enabling efficient reuse of space.

### File and CSV Utilities (`File.h`, `CSV.h`)
Low-level file I/O helpers and a CSV reader/writer for loading and saving structured data from disk.

## Files

| File | Description |
|------|-------------|
| `File.h` | Low-level file I/O utilities |
| `CSV.h` | CSV reader and writer |
| `EMVector.h` | External memory dynamic array |
| `EMFreelist.h` | External memory freelist allocator |
| `EMBTree.h` | External memory B-tree |
| `ExternalMemoryAlgorithmsTestAuto.h` | Automated test helpers |
| `Test.cpp` | Test driver |

## Usage

Compile and run `Test.cpp` to exercise the external memory algorithm tests:

```bash
g++ -O2 -o Test Test.cpp && ./Test
```
