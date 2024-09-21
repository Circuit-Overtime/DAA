## Summary of Prim's and Kruskal's Algorithms

### Prim's Algorithm
- **Purpose**: Finds the Minimum Spanning Tree (MST) of a connected, weighted graph.
- **Approach**:
  - Starts from an arbitrary vertex and grows the MST by repeatedly adding the smallest edge that connects a vertex in the MST to a vertex outside it.
  - Utilizes a priority queue to efficiently retrieve the minimum weight edge.
- **Complexity**: 
  - \(O(E \log V)\) using a priority queue with an adjacency list.
  - \(O(V^2)\) with an adjacency matrix.

### Kruskal's Algorithm
- **Purpose**: Also finds the MST of a connected, weighted graph.
- **Approach**:
  - Begins by sorting all edges in non-decreasing order of their weights.
  - Uses a disjoint-set data structure to avoid cycles and adds edges to the MST until it includes \(V - 1\) edges.
- **Complexity**:
  - \(O(E \log E)\) or \(O(E \log V)\) when sorting edges is the most time-consuming operation.
  - Efficient with sparse graphs.
