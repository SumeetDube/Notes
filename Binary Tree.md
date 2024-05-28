
Consider the following binary tree representing a family:

```
              (A)
             /   \
           (B)   (C)
          /  \     \
        (D)  (E)   (F)
```

1. **Parent node**: A parent node is a node that has at least one child node connected to it. For example, in the tree above, nodes A, B, and C are all parent nodes. Node A is the parent of nodes B and C, node B is the parent of nodes D and E, and node C is the parent of node F.

2. **Leaf node**: A leaf node, also known as an external node, is a node that does not have any children. In the example tree, nodes D, E, and F are all leaf nodes. They are at the ends of the tree and do not have any further descendants.

3. **Internal and external node**: 
   - An internal node, also known as an interior node, is a node that has at least one child node. In the example tree, nodes A, B, and C are internal nodes.
   - An external node, also known as a leaf node, is a node that does not have any children. In the example tree, nodes D, E, and F are external nodes.

4. **Degree of a node**: The degree of a node in a binary tree is the number of children it has. 
   - The degree of node A is 2 because it has two children (nodes B and C).
   - The degree of node B is 2 because it has two children (nodes D and E).
   - The degree of node C is 1 because it has only one child (node F).
   - The degree of nodes D, E, and F is 0 because they have no children.

------------


The Binary tree means that the node can have maximum two children. Here, binary name itself suggests that 'two'; therefore, each node can have either 0, 1 or 2 children.

**Let's understand the binary tree through an example.**

![Binary Tree](https://static.javatpoint.com/ds/images/binary-tree.png)

The above tree is a binary tree because each node contains the utmost two children. The logical representation of the above tree is given below:

![Binary Tree](https://static.javatpoint.com/ds/images/binary-tree2.png)

In the above tree, node 1 contains two pointers, i.e., left and a right pointer pointing to the left and right node respectively. The node 2 contains both the nodes (left and right node); therefore, it has two pointers (left and right). The nodes 3, 5 and 6 are the leaf nodes, so all these nodes contain **NULL** pointer on both left and right parts.

### Properties of Binary Tree

- At each level of i, the maximum number of nodes is 2i.
- The height of the tree is defined as the longest path from the root node to the leaf node. The tree which is shown above has a height equal to 3. Therefore, the maximum number of nodes at height 3 is equal to (1+2+4+8) = 15. In general, the maximum number of nodes possible at height h is (20 + 21 + 22+….2h) = 2h+1 -1.
- The minimum number of nodes possible at height h is equal to **h+1**.
- If the number of nodes is minimum, then the height of the tree would be maximum. Conversely, if the number of nodes is maximum, then the height of the tree would be minimum.

If there are 'n' number of nodes in the binary tree.

**The minimum height can be computed as:**

As we know that,

n = 2h+1 -1

n+1 = 2h+1

Taking log on both the sides,

log2(n+1) = log2(2h+1)

log2(n+1) = h+1

**h = log2(n+1) - 1**

**The maximum height can be computed as:**

As we know that,

n = h+1

**h= n-1**

### Types of Binary Tree

**There are four types of Binary tree:**

- **Full/ proper/ strict Binary tree**
- **Complete Binary tree**
- **Perfect Binary tree**
- **Degenerate Binary tree**
- **Balanced Binary tree**

**1. Full/ proper/ strict Binary tree**

The full binary tree is also known as a strict binary tree. The tree can only be considered as the full binary tree if each node must contain either 0 or 2 children. The full binary tree can also be defined as the tree in which each node must contain 2 children except the leaf nodes.

**Let's look at the simple example of the Full Binary tree.**

![Types of Binary Tree](https://static.javatpoint.com/ds/images/types-of-binary-tree.png)

In the above tree, we can observe that each node is either containing zero or two children; therefore, it is a Full Binary tree.

**Properties of Full Binary Tree**

- The number of leaf nodes is equal to the number of internal nodes plus 1. In the above example, the number of internal nodes is 5; therefore, the number of leaf nodes is equal to 6.
- The maximum number of nodes is the same as the number of nodes in the binary tree, i.e., 2h+1 -1.
- The minimum number of nodes in the full binary tree is 2*h-1.
- The minimum height of the full binary tree is **log2(n+1) - 1.**
- The maximum height of the full binary tree can be computed as:

n= 2*h - 1

n+1 = 2*h

**h = n+1/2**

**Complete Binary Tree**

The complete binary tree is a tree in which all the nodes are completely filled except the last level. In the last level, all the nodes must be as left as possible. In a complete binary tree, the nodes should be added from the left.

Let's create a complete binary tree.

![Types of Binary Tree](https://static.javatpoint.com/ds/images/types-of-binary-tree2.png)

The above tree is a complete binary tree because all the nodes are completely filled, and all the nodes in the last level are added at the left first.

**Properties of Complete Binary Tree**

- The maximum number of nodes in complete binary tree is 2h+1 - 1.
- The minimum number of nodes in complete binary tree is 2h.
- The minimum height of a complete binary tree is **log2(n+1) - 1.**
- The maximum height of a complete binary tree is

**Perfect Binary Tree**

A tree is a perfect binary tree if all the internal nodes have 2 children, and all the leaf nodes are at the same level.

![Types of Binary Tree](https://static.javatpoint.com/ds/images/types-of-binary-tree3.png)

**Let's look at a simple example of a perfect binary tree.**

The below tree is not a perfect binary tree because all the leaf nodes are not at the same level.

![Types of Binary Tree](https://static.javatpoint.com/ds/images/types-of-binary-tree4.png)

#### Note: All the perfect binary trees are the complete binary trees as well as the full binary tree, but vice versa is not true, i.e., all complete binary trees and full binary trees are the perfect binary trees.

### Degenerate Binary Tree

The degenerate binary tree is a tree in which all the internal nodes have only one children.

**Let's understand the Degenerate binary tree through examples.**

![Types of Binary Tree](https://static.javatpoint.com/ds/images/types-of-binary-tree5.png)

The above tree is a degenerate binary tree because all the nodes have only one child. It is also known as a right-skewed tree as all the nodes have a right child only.

![Types of Binary Tree](https://static.javatpoint.com/ds/images/types-of-binary-tree6.png)

The above tree is also a degenerate binary tree because all the nodes have only one child. It is also known as a left-skewed tree as all the nodes have a left child only.

**Balanced Binary Tree**

The balanced binary tree is a tree in which both the left and right trees differ by atmost 1. For example, **_AVL_** and **_Red-Black trees_** are balanced binary tree.

**Let's understand the balanced binary tree through examples.**

![Types of Binary Tree](https://static.javatpoint.com/ds/images/types-of-binary-tree7.png)

The above tree is a balanced binary tree because the difference between the left subtree and right subtree is zero.

![Types of Binary Tree](https://static.javatpoint.com/ds/images/types-of-binary-tree8.png)

The above tree is not a balanced binary tree because the difference between the left subtree and the right subtree is greater than 1.