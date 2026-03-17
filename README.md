This code is for the readers of the book (see https://www.amazon.com/dp/B08PXHJCXY), and for personal use only. For commercial use please reach out (my email is in the book's preface and back cover).

I ask that you please post an honest review of the book on Amazon.com in return. The feedback I got so far for the previous editions has been limited, and I need it to improve the book further. This is hobby project that is worked on weekends/evenings, so any assistance is greatly appreciated.

All reusable code is in .h files, and test*.cpp files allow testing various parts of it.

The code has been reasonably tested, but no guarantees are made about its quality or behavior. I.e. the code is provided "as is", without any implicit warranty of merchantability. So don't use it in pacemakers, nuclear reactors, etc.

Github seems to have a bug in downloading the slides--the best way to get them is to download the entire repository.

---

## What This Repository Does — In Plain English

This is a **collection of computer algorithms** written in C++, organized as a companion to the book linked above. Think of it as a toolbox: each folder contains tools for solving a specific category of computer-science problem. Here is what each folder does in everyday terms:

### Sorting
Tools for **putting things in order** — numbers, names, data records — as quickly as possible. Includes classic techniques like QuickSort (picks a middle value and divides the work), HeapSort (uses a special tree structure), and MergeSort (splits lists in half, sorts each half, then combines them).

### Heaps
A **heap** is like a to-do list that always keeps the most urgent item at the front. This folder provides both a basic heap and an "indexed heap" that lets you quickly update or remove any specific item — useful for scheduling, pathfinding, and event simulation.

### HashTable
A **hash table** is like a well-organized filing cabinet. Instead of searching through every drawer, it calculates exactly which drawer to open. This folder includes different filing strategies (chaining, linear probing) and a Bloom filter — a fast, memory-efficient way to check "have we seen this item before?"

### Utils (Utilities)
General-purpose building blocks that other modules use: growable arrays (`Vector`), stacks (last-in-first-out piles), queues (first-in-first-out lines), bit manipulation helpers, and a `UnionFind` structure for grouping related items together.

### Graphs
Tools for working with **networks of connected things** — roads and cities, social networks, web links. Includes algorithms for finding shortest paths, detecting communities, and solving maximum-flow problems (e.g., "how much water can flow through a pipe network?").

### RandomTreap
A **treap** is a self-balancing search tree that combines tree properties with random ordering to stay fast even in worst-case scenarios. This folder also includes a **skip list** (a layered linked list for fast searches), a **trie** (a tree for storing strings letter-by-letter), and related text-indexing structures.

### StringAlgorithms
Tools for **searching and analysing text** — finding a pattern inside a long string, computing the longest common substring, running a simple regular-expression engine, and diffing two texts (showing what changed between versions).

### Compression
Algorithms that **make files smaller** by finding and eliminating repetition:
- **Huffman coding** — assigns shorter codes to frequent characters (like Morse code).
- **LZW** — replaces repeated byte sequences with short dictionary entries (used in GIF and ZIP).
- **Arithmetic coding** — encodes whole messages as a single fractional number for maximum compression.

### Cryptography
Algorithms for **keeping data secret** — encrypting and decrypting information so only authorized parties can read it.

### ErrorCorrectingCodes
Tools for **detecting and fixing errors** in transmitted data (e.g., CDs, QR codes, satellite links):
- **CRC** — a quick checksum to detect accidental changes.
- **Reed-Solomon** — the code that lets scratched CDs still play.
- **LDPC** — a modern code used in Wi-Fi and 5G for near-perfect error correction.

### LargeNumbers
Lets a computer work with **numbers bigger than it can normally hold** — arbitrary-precision integers and exact fractions. Useful for cryptography and number-theory experiments.

### ComputationalGeometry
Algorithms about **shapes and space**:
- **KD-Tree** — quickly finds the nearest point in a large set of 2D/3D points.
- **Convex Hull** — finds the smallest polygon that encloses a set of points (like stretching a rubber band around them).
- **BuildingArea** — computes the area of overlapping rectangles.

### NumericalMethods
**Mathematical tools** for calculations that are too hard to solve exactly:
- Matrices and linear algebra (solving systems of equations).
- FFT (Fast Fourier Transform) — breaks a signal into its frequencies (used in audio, images, and physics).
- Integration and differentiation (calculus on sampled data).
- Solving differential equations (e.g., simulating physical systems over time).
- Cubic splines and interpolation (drawing smooth curves through data points).

### NumericalOptimization
Algorithms for **finding the best answer** to a mathematical problem when you cannot check every possibility:
- **LBFGS** — a powerful gradient-based minimiser widely used in machine learning.
- **Nelder-Mead** — a "simplex" search that works without needing derivatives.
- **Golden-Section search** — efficiently narrows down the minimum of a curve.
- **Differential Evolution** — a population-based global optimiser inspired by natural selection.
- **Linear Programming** — finds the best outcome given a set of linear constraints (e.g., maximising profit given resource limits).

### Optimization (Combinatorial)
Tools for **hard real-world scheduling and packing problems**:
- **Travelling Salesman Problem (TSP)** — find the shortest route visiting every city once.
- **Knapsack** — choose items to maximise value without exceeding a weight limit.
- **Bin Packing** — fit objects of various sizes into the fewest containers.
- **3-SAT / Satisfiability** — determine whether a set of logical conditions can all be satisfied at once.
- **Metaheuristics** — general-purpose "good-enough" search strategies (simulated annealing, genetic algorithms).

### FinancialCalculations
Tools for **money and investment maths**:
- Portfolio optimisation (mean-variance / Markowitz model).
- Annuities and cash-flow analysis.
- Option pricing (Black-Scholes and Monte Carlo methods).
- Portfolio simulation and risk analysis.

### RandomNumberGeneration
Tools for **generating random numbers** and doing statistics:
- High-quality pseudo-random number generators.
- Statistical distributions (Normal, Poisson, etc.).
- Bootstrap resampling (estimating uncertainty from data).
- Time-series analysis.
- MCMC (Markov Chain Monte Carlo) — a technique for sampling complex probability distributions.
- Sobol sequences — low-discrepancy quasi-random numbers for numerical integration.
- Hypothesis tests (distribution tests, permutation tests).

### MachineLearning
Implementations of popular **machine learning** algorithms:
- **KNN** (K-Nearest Neighbours) — classifies a new point by looking at its closest neighbours.
- **Neural Network** — layers of interconnected nodes that learn patterns from data.
- **Decision Tree / Random Forest** — tree-based rules learned from examples.
- **SVM** (Support Vector Machine) — finds the best boundary between classes.
- **Naive Bayes** — a fast probabilistic classifier.
- **Lasso** — linear regression with built-in feature selection.
- **Clustering** — groups unlabelled data into natural clusters.
- **A-Priori** — finds frequently co-occurring items (e.g., "customers who buy X also buy Y").
- **Reinforcement Learning** — an agent learns by trial and error in a simulated environment.

### ExternalMemoryAlgorithms
Algorithms designed for datasets **too large to fit in RAM** — they read and write data directly on disk in carefully organised chunks:
- **EMBTree** — a B-tree stored on disk for fast key lookups.
- **EMVector** — a disk-backed growable array.
- **CSV** — utilities for reading and writing comma-separated data files.

### MiscAlgs (Miscellaneous Algorithms)
A grab-bag of useful structures that do not fit neatly elsewhere:
- **Fenwick Tree** — efficiently computes prefix sums and range queries on an array.
- **Combinatorial Generation** — enumerates permutations, combinations, and subsets.
- **LRU Cache** — keeps the most recently used items in a small fast cache, evicting the oldest ones.
- **Prime Table** — pre-computes primes up to a given limit using the Sieve of Eratosthenes.
- **KBitWordVector** — stores integers using a fixed, user-chosen number of bits each to save memory.

### AutoRegressionTest
A **master test runner** that compiles and executes automated tests from every module above, checking that nothing is broken after a code change.

### Scrap
**Experimental or in-progress code** — implementations that are not yet polished or fully tested, including an interval tree, a cuckoo hash table, a left-leaning red-black tree, and a pairing heap, among others.

### Slides
Two educational **PDF slide decks** that accompany the book:
- *Introduction to Machine Learning*
- *Monte Carlo Algorithms*

---

## How the Code Is Organised

| File type | Purpose |
|-----------|---------|
| `*.h` | The reusable algorithm (header-only library — just `#include` it) |
| `test*.cpp` | A small program that exercises the algorithm and prints results |
| `*TestAuto.h` | Automated assertions used by the master test runner |

To try any algorithm, compile the corresponding `test*.cpp` file with a C++11-capable compiler:

```bash
g++ -std=c++11 -I. Sorting/testSort.cpp -o testSort && ./testSort
```

No external libraries are required — only the C++ standard library.
