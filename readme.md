# Data Structures and Algorithms Overview

This repository contains concise summaries of key data structures and algorithms commonly used in computer science. Each section provides an overview, properties, and relevant details to aid understanding and implementation.

## Contents

- [Prim's Algorithm](#prims-algorithm)
- [Kruskal's Algorithm](#kruskals-algorithm)
- [Binary Tree](#binary-tree)
- [Binary Search Tree](#binary-search-tree)

## Prim's Algorithm
- **Definition**: A greedy algorithm that finds the minimum spanning tree (MST) for a weighted undirected graph.
- **Properties**:
  - Starts with a single vertex and grows the MST by adding the smallest edge from the tree to a vertex outside the tree.
  - Efficiently implemented using priority queues.
- **Complexity**: 
  - Using adjacency matrix: \(O(V^2)\)
  - Using adjacency list with a priority queue: \(O(E \log V)\)

## Kruskal's Algorithm
- **Definition**: A greedy algorithm that finds the minimum spanning tree for a weighted undirected graph by sorting edges.
- **Properties**:
  - Sorts all edges in non-decreasing order of their weights.
  - Adds edges one by one to the MST while avoiding cycles using the union-find data structure.
- **Complexity**: \(O(E \log E)\), primarily due to sorting the edges.

## Binary Tree
- **Definition**: A tree data structure where each node has at most two children.
- **Properties**:
  - Can be complete, full, or perfect.
  - Used for various applications like expression trees and representing hierarchical data.
- **Traversal Methods**:
  - Pre-order, In-order, Post-order.

## Binary Search Tree (BST)
- **Definition**: A specialized form of a binary tree that maintains a specific order property.
- **Properties**:
  - Left subtree values are less, right subtree values are greater than the node's value.
  - Supports efficient searching, insertion, and deletion.
- **Complexity**:
  - Average case: \(O(\log n)\)
  - Worst case: \(O(n)\) when unbalanced.

## Usage

You can clone this repository and explore the summaries for a quick reference or use it as a basis for deeper study into these fundamental concepts.

