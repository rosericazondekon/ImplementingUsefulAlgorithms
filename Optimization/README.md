# Optimization

This folder contains implementations of **combinatorial optimization algorithms** — methods for finding the best solution from a finite (but potentially enormous) set of discrete possibilities.

## What is Combinatorial Optimization?

Unlike continuous optimization, combinatorial optimization deals with problems where the solution is chosen from a discrete set (e.g., which items to pack, how to assign workers to tasks). Many of these problems are NP-hard, meaning no known algorithm solves all instances efficiently. Practical approaches use exact methods for small instances and approximation or heuristic methods for large ones.

## Algorithms Included

### Knapsack Problem (`Knapsack.h`)
Given items with weights and values, and a knapsack with a maximum weight capacity, select the subset of items that maximizes total value without exceeding the capacity. Solved exactly with dynamic programming, or approximately with greedy/heuristic methods.

### Bin Packing (`BinPacking.h`)
Given items of various sizes and bins of fixed capacity, pack all items into the fewest bins possible. This is NP-hard; the implementation provides practical approximation algorithms (first-fit decreasing, etc.).

### 3-SAT Satisfiability (`Satisfiability3.h`)
Determines whether a Boolean formula in 3-CNF (conjunctive normal form with 3 literals per clause) can be satisfied. SAT is the canonical NP-complete problem; heuristic and local search methods are used for large instances.

### Constraint Processing (`ContraintProcessing.h`)
Constraint propagation and satisfaction for constraint satisfaction problems (CSPs). Applies arc consistency and backtracking search to prune the solution space.

### Meta-Heuristics (`MetaHeuristics.h`)
General-purpose optimization strategies that guide a search process without problem-specific knowledge:
- **Simulated Annealing**: Accepts worse solutions occasionally (with decreasing probability) to escape local optima.
- **Genetic Algorithms**: Evolves a population of solutions by selection, crossover, and mutation.
- **Tabu Search**: Keeps a short-term memory of recent moves to avoid cycling.

### Search Algorithms (`SearchAlgorithms.h`)
General search strategies including branch-and-bound and beam search.

## Files

| File | Description |
|------|-------------|
| `Knapsack.h` | Knapsack problem (dynamic programming + heuristics) |
| `BinPacking.h` | Bin packing approximation algorithms |
| `MetaHeuristics.h` | Simulated annealing, genetic algorithms, tabu search |
| `SearchAlgorithms.h` | Branch-and-bound and beam search |
| `Satisfiability3.h` | 3-SAT solver |
| `ContraintProcessing.h` | Constraint satisfaction / propagation |
| `OptTestAuto.h` | Automated test helpers |
| `test.cpp` | Test driver for knapsack, bin packing, and meta-heuristics |
| `TestConstraint.cpp` | Test driver for constraint processing |

## Usage

Compile and run the test files:

```bash
g++ -O2 -o test test.cpp && ./test
g++ -O2 -o TestConstraint TestConstraint.cpp && ./TestConstraint
```
