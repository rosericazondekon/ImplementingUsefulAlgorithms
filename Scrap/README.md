# Scrap

This folder contains **experimental, auxiliary, and work-in-progress** implementations that are not yet fully integrated into the main library. The code here may be incomplete, less tested, or serve as a research scratchpad.

## Contents

### Alternative Data Structures
- **Cuckoo Hash Table** (`CuckooHashTable.h`): An open-addressing hash table that uses two hash functions and "kicks out" existing items to their alternate position on collision. Guarantees O(1) worst-case lookup.
- **Left-Leaning Red-Black Tree** (`LeftLeaningRedBlackTree.h`): A simplified variant of the red-black tree with fewer cases to handle. Maintains O(log n) balanced BST operations.
- **Pairing Heap** (`PairingHeap.h`): A heap variant with excellent practical performance and simple decrease-key operation.
- **Interval Tree** (`IntervalTree.h`): Stores intervals and efficiently answers "which intervals overlap with this query interval?" — useful for scheduling and computational geometry.

### Advanced Algorithms
- **Arithmetic Coding** (`ArithmeticCoding.h`): A lossless compression method that encodes a message as a single fractional number; achieves entropy-optimal compression unlike Huffman coding.
- **Locality Sensitive Hashing** (`LSH.h`): Hashes similar items into the same bucket with high probability. Used for approximate nearest-neighbor search in high-dimensional spaces.
- **Scrap Clustering** (`ScrapClustering.h`): Experimental clustering algorithms under development.
- **Scrap Trie** (`ScrapTrie.h`): Experimental trie variants.
- **Scrap Heap** (`ScrapHeap.h`): Experimental heap variants.

### Statistical and Other Utilities
Additional experimental statistical methods and utilities awaiting refinement.

## Files

| File | Description |
|------|-------------|
| `ArithmeticCoding.h` | Arithmetic coding compression |
| `CuckooHashTable.h` | Cuckoo hashing |
| `IntervalTree.h` | Interval tree for overlap queries |
| `LeftLeaningRedBlackTree.h` | Left-leaning red-black BST |
| `PairingHeap.h` | Pairing heap |
| `LSH.h` | Locality Sensitive Hashing |
| `ScrapClustering.h` | Experimental clustering code |
| `ScrapTrie.h` | Experimental trie code |
| `ScrapHeap.h` | Experimental heap code |
| `test*.cpp` | Test drivers for various experiments |

> **Note:** Code in this folder is experimental and may not be production-ready. It is provided for educational exploration.
