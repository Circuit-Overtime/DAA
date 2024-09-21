# Breadth-First Search (BFS) Algorithm Overview

## Graph Representation
- A graph consists of **vertices** and **edges**.
- **Vertices** are numbered from 1 to n.
- Represent the graph using an **adjacency matrix** or an **adjacency list**:
  - **Adjacency Matrix**: 
    - Entry `a[i][j]` is 1 if there’s an edge from vertex i to j, otherwise 0.
    - Allows constant-time checks for direct connections but can be inefficient for sparse graphs.
  - **Adjacency List**:
    - Each vertex stores a list of its neighbors.
    - More efficient for sparse graphs.

## Problem Statement
- Determine if there exists a path between a **source vertex** \( v_0 \) and a **target vertex** \( v_k \).

## BFS Approach
1. **Initialization**:
   - Use a **visited** array to track visited vertices.
   - Use a **queue** to manage vertices to be explored.

2. **Exploration**:
   - Start from the source vertex, mark it as visited, and add it to the queue.
   - While the queue is not empty:
     - Dequeue a vertex and explore its neighbors.
     - If a neighbor has not been visited:
       - Mark it as visited.
       - Add it to the queue.

3. **Termination**:
   - The algorithm terminates when the queue is empty, indicating all reachable vertices from the source have been explored.

## Complexity Analysis
- **Using Adjacency Matrix**: \( O(n^2) \)
- **Using Adjacency List**: \( O(n + m) \) where m is the number of edges, making it more efficient for sparse graphs.

## Additional Features
- **Path Reconstruction**:
  - Track **parent** of each visited vertex to reconstruct the path from the source to any vertex.
  
- **Level Tracking**:
  - Maintain the **level** of each vertex to determine its distance from the source.

## Pseudocode
```python
def bfs(graph, start):
    visited = [False] * (n + 1)
    parent = [-1] * (n + 1)
    level = [-1] * (n + 1)
    queue = []

    visited[start] = True
    level[start] = 0
    queue.append(start)

    while queue:
        current = queue.pop(0)
        for neighbor in graph[current]:
            if not visited[neighbor]:
                visited[neighbor] = True
                parent[neighbor] = current
                level[neighbor] = level[current] + 1
                queue.append(neighbor)

    return parent, level
