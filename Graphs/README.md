# Graphs

This folder contains implementations of **graph algorithms** for representing, traversing, and analyzing networks.

## What is a Graph?

A graph is a set of nodes (vertices) connected by edges. Graphs model a huge variety of real-world structures: road networks, social networks, web pages, computer networks, and more. Graph algorithms answer questions like "what is the shortest path between two cities?" or "what is the maximum amount of water that can flow through a pipe network?"

## Algorithms Included

### General Graph (`Graph.h`)
Core graph data structure supporting both directed and undirected graphs, along with fundamental algorithms:
- **Depth-First Search (DFS)** and **Breadth-First Search (BFS)** for traversal
- **Shortest paths** (Dijkstra's algorithm, Bellman-Ford)
- **Minimum spanning tree** (Prim's / Kruskal's)
- **Topological sort** for directed acyclic graphs

### Network Flow (`NetworkFlow.h`)
Algorithms for finding the maximum flow through a network (e.g., maximum water through pipes, or maximum bandwidth through a network):
- **Ford-Fulkerson / Edmonds-Karp** maximum flow
- **Minimum cut** (by the max-flow min-cut theorem)
- Applications to bipartite matching and circulation problems

## Files

| File | Description |
|------|-------------|
| `Graph.h` | Core graph data structure and algorithms |
| `NetworkFlow.h` | Maximum flow and minimum cut algorithms |
| `GraphsTestAuto.h` | Automated test helpers for graph algorithms |
| `NetworkFlowTestAuto.h` | Automated test helpers for network flow |
| `test.cpp` | Test driver for graph algorithms |
| `testNetworkFlow.cpp` | Test driver for network flow |

## Usage

Compile and run the test files:

```bash
g++ -O2 -o test test.cpp && ./test
g++ -O2 -o testNetworkFlow testNetworkFlow.cpp && ./testNetworkFlow
```
