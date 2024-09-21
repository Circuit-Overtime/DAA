# Analysis of Dijkstra’s Algorithm for Single Source Shortest Path Problem

## Overview
Dijkstra's algorithm finds the shortest paths from a source vertex to all other vertices in a graph with non-negative edge weights. It operates by maintaining a set of visited (or "burnt") vertices and progressively updating the shortest distances.

### Initial Setup
1. **Vertices State:** All vertices start as unvisited, with distances set to infinity.
2. **Source Vertex:** Set the distance of the source vertex (e.g., vertex 1) to 0.

## Algorithm Process
1. **Select Minimum Distance Vertex:** Repeatedly pick the unvisited vertex with the smallest known distance.
2. **Visit Neighbors:** Update the distances to neighboring vertices based on the selected vertex's distance.

## Correctness
Dijkstra's algorithm is a greedy algorithm, and its correctness relies on maintaining an invariant:
- **Invariant:** The distances assigned to burnt vertices are the shortest distances from the source.
- **Inductive Step:** When a new vertex \(v\) is added to the burnt set, the distance to \(v\) is the shortest possible, as shown through reasoning about potential alternative paths.

## Complexity Analysis
1. **Initialization:** \(O(n)\) to initialize distances.
2. **Outer Loop:** Runs \(n\) times (one for each vertex).
   - **Finding Minimum Vertex:** Requires \(O(n)\) to scan unvisited vertices.
   - **Updating Neighbors:** Involves scanning outgoing edges, also \(O(n)\) in an adjacency matrix.

Overall, with adjacency matrix representation, the complexity is \(O(n^2)\).

### Optimization with Adjacency Lists
Switching to an adjacency list allows for more efficient neighbor updates, reducing the complexity to \(O(m + n \log n)\) using a min-heap to maintain and update distances:
- Finding the minimum vertex takes \(O(\log n)\).
- Updating distances for edges takes \(O(m \log n)\) in total.

## Handling Negative Weights
- Dijkstra's algorithm assumes non-negative edge weights. If negative edges are present, the algorithm may yield incorrect results.
- **Negative Cycles:** If present, the shortest path problem becomes undefined. 

## Alternative Algorithms
1. **Bellman-Ford Algorithm:** Can handle graphs with negative edge weights (as long as there are no negative cycles).
2. **Floyd-Warshall Algorithm:** Solves all-pairs shortest path problems, applicable to graphs with negative edges but no negative cycles.

## Conclusion
Dijkstra’s algorithm efficiently finds shortest paths in graphs with non-negative weights, but care must be taken when negative weights are involved. Alternative algorithms exist for handling those cases.
