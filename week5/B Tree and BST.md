## Summary of Binary Trees and Binary Search Trees

### Binary Tree
- **Definition**: A tree data structure where each node has at most two children, referred to as the left and right child.
- **Properties**:
  - Can be complete, full, or perfect, depending on the structure and node arrangement.
  - Used for various applications like expression trees, Huffman coding, and representing hierarchical data.
- **Traversal Methods**:
  - Pre-order: Visit the root, then left subtree, followed by the right subtree.
  - In-order: Visit the left subtree, the root, and then the right subtree.
  - Post-order: Visit the left subtree, right subtree, and then the root.

### Binary Search Tree (BST)
- **Definition**: A specialized form of a binary tree that maintains a specific order property.
- **Properties**:
  - For each node, all values in the left subtree are less, and all values in the right subtree are greater than the node's value.
  - Supports efficient searching, insertion, and deletion operations.
- **Complexity**:
  - Average case: \(O(\log n)\) for search, insertion, and deletion.
  - Worst case: \(O(n)\) when the tree becomes unbalanced (like a linked list).
