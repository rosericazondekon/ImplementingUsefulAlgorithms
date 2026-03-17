# HashTable

This folder contains implementations of **hash table** data structures and related probabilistic data structures.

## What is a Hash Table?

A hash table stores key-value pairs for near-instant lookup, insertion, and deletion (on average O(1) time). It works by applying a hash function to a key to compute an index into an array. When two keys map to the same index (a "collision"), the table uses a collision resolution strategy.

## Data Structures Included

### Chaining Hash Table (`ChainingHashTable.h`)
Resolves collisions by storing all keys that map to the same slot in a linked list. Simple and robust — performance degrades gracefully even at high load.

### Linear Probing Hash Table (`LinearProbingHashTable.h`)
An open-addressing strategy where collisions are resolved by scanning forward through the array until an empty slot is found. More cache-friendly than chaining due to better memory locality.

### Bloom Filter (`BloomFilter.h`)
A probabilistic data structure that answers "is this element in the set?" in O(1) time and space, with a small false-positive rate but zero false negatives. Bloom filters are used in databases, caches, and network routers to avoid expensive lookups for items that definitely aren't present.

### Hash Functions (`HashFunction.h`)
A collection of good general-purpose hash functions for strings, integers, and other data types.

## Files

| File | Description |
|------|-------------|
| `HashFunction.h` | General-purpose hash functions |
| `ChainingHashTable.h` | Hash table with chaining collision resolution |
| `LinearProbingHashTable.h` | Hash table with linear probing collision resolution |
| `BloomFilter.h` | Probabilistic Bloom filter |
| `HashTableTestAuto.h` | Automated test helpers |
| `MapTestAutoHelper.h` | Map interface test helpers |
| `test.cpp` | Test driver |

## Usage

Compile and run `test.cpp` to exercise the hash table tests:

```bash
g++ -O2 -o test test.cpp && ./test
```
