---
title: Invert Binary Tree
language: JavaScript
tags: tree, recursion
difficulty: Easy
---

# Description

This snippet demonstrates how to invert a binary tree, swapping the left and right children of every node.

# Code

```javascript
function invertBinaryTree(root) {
  if (root === null) return null;

  const temp = root.left;
  root.left = invertBinaryTree(root.right);
  root.right = invertBinaryTree(temp);

  return root;
}
```
