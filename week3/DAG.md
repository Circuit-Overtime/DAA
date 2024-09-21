# Directed Acyclic Graphs (DAGs)

## Introduction to DAGs
Directed Acyclic Graphs (DAGs) are important in modeling tasks with constraints. For example, when preparing for a foreign trip, several tasks (like getting a passport, buying a ticket, etc.) depend on each other. 

### Task Dependencies
- **Tasks:** Passport, Ticket, Insurance, Visa, Foreign Exchange, Gifts
- **Dependencies:**
  - Passport → Ticket
  - Passport → Insurance
  - Ticket + Insurance → Visa
  - Visa → Foreign Exchange
  - Visa → Gifts (only after confirming the trip)

## Characteristics of DAGs
1. **Directed:** The dependencies point from one task to another.
2. **Acyclic:** There are no cycles, ensuring that tasks can be sequenced.

## Topological Sorting
The goal is to sequence tasks such that all dependencies are satisfied. This is known as topological sorting.

### Key Observations
- **No Cycle:** If the graph had a cycle, no topological ordering is possible.
- **At least One Vertex with Indegree 0:** Every DAG has at least one vertex with no incoming edges.

## Algorithm for Topological Sorting
1. **Identify Vertices with Indegree 0:** Start with vertices that have no dependencies.
2. **Enumerate and Remove:** Remove the chosen vertex and reduce the indegrees of its neighbors. Repeat until all vertices are processed.

### Example Process
1. Start with vertices with indegree 0 (e.g., Passport).
2. Remove a vertex and update neighbors' indegrees.
3. Continue until all tasks are enumerated.

## Pseudocode Outline
```plaintext
1. Compute indegree of all vertices.
2. While there are vertices with indegree 0:
   a. Select a vertex with indegree 0.
   b. Remove it and update the indegrees of its neighbors.
