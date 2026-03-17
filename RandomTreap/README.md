# RandomTreap

This folder contains implementations of **randomized search data structures** that provide efficient sorted-order operations with high probability.

## Data Structures Included

### Treap (`Treap.h`)
A **treap** is a combination of a binary search tree (BST) and a heap. Each node has a key (used for BST ordering) and a random priority (used for heap ordering). Randomly assigned priorities keep the tree balanced with high probability, giving O(log n) expected time for insert, delete, and search — without the complex rebalancing logic of AVL or red-black trees.

### LCP Treap (`LCPTreap.h`)
An extension of the treap that also maintains **Longest Common Prefix (LCP)** information. Useful for string processing tasks such as suffix array construction and substring queries.

### Skip List (`SkipList.h`)
A **skip list** is a probabilistic alternative to balanced binary search trees. It uses multiple linked lists of increasing "express lane" speed to skip over elements. Insert, delete, and search all run in O(log n) expected time. Skip lists are simpler to implement than balanced trees and are used in Redis and LevelDB.

### Trie (`Trie.h`)
A **trie** (prefix tree) stores a dynamic set of strings where each node represents a character prefix. It enables:
- O(m) lookup, insertion, and deletion where m is the string length
- Efficient prefix-based queries (e.g., autocomplete)
- Lexicographic ordering of strings

## Files

| File | Description |
|------|-------------|
| `Treap.h` | Randomized treap (BST + heap) |
| `LCPTreap.h` | Treap with longest-common-prefix support |
| `SkipList.h` | Probabilistic skip list |
| `Trie.h` | Prefix trie for string sets |
| `DynamicSortedSequenceTestAuto.h` | Automated test helpers |
| `test.cpp` | Test driver |

## Usage

Compile and run `test.cpp` to exercise the randomized structure tests:

```bash
g++ -O2 -o test test.cpp && ./test
```
