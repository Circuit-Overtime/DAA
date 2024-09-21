# Depth-First Search (DFS) Algorithm Overview

## Concept
- DFS explores a graph by going as deep as possible down one path before backing up and exploring others.
- Instead of level-by-level exploration, it visits the first unexplored neighbor of the current vertex and suspends the exploration of the current vertex.

## Process
1. **Start at Vertex \( i \)**:
   - Mark \( i \) as visited.
   - Explore its first neighbor \( j \) that is not visited.

2. **Suspension**:
   - Suspend exploration of \( i \) and proceed to explore \( j \).

3. **Backtracking**:
   - If no unexplored neighbors are found, backtrack to the nearest suspended vertex with unexplored neighbors.

4. **Stack Utilization**:
   - The suspended vertices are conceptually managed using a stack.

## Example Execution (Starting from Vertex 4)
- Mark 4 as visited and explore its neighbors in order (1, 3, 5, 6):
  - Visit 1 (mark as visited), suspend 4.
  - Visit 2 (mark as visited), suspend 1.
  - Visit 3 (already visited); backtrack to 2.
  - All neighbors of 2 visited; backtrack to 1.
  - All neighbors of 1 visited; backtrack to 4.
  - Continue with unexplored neighbors: visit 5, then 6, and subsequently 7 and 8.
  - Explore further until no unexplored neighbors are left, then backtrack completely.

## Recursive Implementation
- Implementing DFS recursively eliminates the need for an explicit stack:
  - Each recursive call handles the suspension and exploration.
  
### Pseudocode
```python
def dfs(vertex):
    mark_as_visited(vertex)
    for neighbor in get_neighbors(vertex):
        if not is_visited(neighbor):
            mark_parent(neighbor, vertex)
            dfs(neighbor)
