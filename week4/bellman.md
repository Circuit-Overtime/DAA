## Bellman-Ford Algorithm Overview

The Bellman-Ford algorithm is used to find the shortest paths from a source vertex to all other vertices in a graph, even when negative edge weights are allowed (but without negative cycles).

### Key Properties
1. **No Loops in Shortest Paths**: A shortest path will never go through a loop. If a path goes through the same vertex multiple times, the loop can be removed without increasing the cost of the path.
2. **Shortest Path Prefix**: Every prefix of a shortest path is itself a shortest path. If a path from \( s \) to \( t \) goes through vertices \( v_1, v_2, \ldots, v_m \), then the path from \( s \) to \( v_m \) is the shortest path from \( s \) to \( v_m \).

### Algorithm Steps
1. **Initialization**: 
   - Set the distance to the source vertex \( s \) to 0 and all other vertices to infinity.
  
2. **Relaxation**: 
   - For \( n-1 \) iterations (where \( n \) is the number of vertices), update the distance for each edge \( (u, v) \) in the graph:
     \[
     \text{distance}[v] = \min(\text{distance}[v], \text{distance}[u] + \text{weight}(u, v))
     \]
  
3. **Result**: 
   - After \( n-1 \) iterations, the distances reflect the shortest paths from the source vertex to all other vertices.

### Complexity
- The time complexity of the Bellman-Ford algorithm is \( O(n \cdot m) \) when using an adjacency list, where \( m \) is the number of edges and \( n \) is the number of vertices.
- If an adjacency matrix is used, the time complexity increases to \( O(n^3) \).

### Example
Consider a graph with negative edge weights but no negative cycles. By applying the Bellman-Ford algorithm iteratively, we can compute the shortest paths from the source vertex to all other vertices effectively.

### Conclusion
The Bellman-Ford algorithm is a robust method for calculating shortest paths in graphs with negative weights, provided that negative cycles are not present.
