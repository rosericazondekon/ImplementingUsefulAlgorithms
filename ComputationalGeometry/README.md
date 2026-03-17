# ComputationalGeometry

This folder contains implementations of fundamental **computational geometry** algorithms and data structures.

## Algorithms Included

### Convex Hull (`ConvexHull.h`)
Given a set of points in 2D space, the convex hull is the smallest convex polygon that encloses all of them — think of stretching a rubber band around a set of nails. This is useful in collision detection, pattern recognition, and geographic analysis.

### K-D Tree (`KDTree.h`)
A K-Dimensional tree is a space-partitioning data structure that organizes points in k-dimensional space. It allows efficient nearest-neighbor search and range queries, used in machine learning (e.g., k-NN), computer graphics, and spatial databases.

### Building Area (`BuildingArea.h`)
Computes the area of polygons, useful for geographic information systems (GIS) and urban planning applications.

### Point Utilities (`Point.h`)
Basic 2D/3D point class with geometric operations such as distance, dot product, and cross product.

## Files

| File | Description |
|------|-------------|
| `Point.h` | 2D/3D point class and basic geometric operations |
| `ConvexHull.h` | Convex hull algorithm |
| `KDTree.h` | K-D tree for spatial indexing and nearest-neighbor search |
| `BuildingArea.h` | Polygon area calculation |
| `ComputationalGeometryTestAuto.h` | Automated test helpers |
| `testConvexHull.cpp` | Test driver for convex hull |
| `testBuildingArea.cpp` | Test driver for building area |
| `testTrees.cpp` | Test driver for K-D tree |

## Usage

Compile and run individual test files:

```bash
g++ -O2 -o testConvexHull testConvexHull.cpp && ./testConvexHull
g++ -O2 -o testTrees testTrees.cpp && ./testTrees
g++ -O2 -o testBuildingArea testBuildingArea.cpp && ./testBuildingArea
```
