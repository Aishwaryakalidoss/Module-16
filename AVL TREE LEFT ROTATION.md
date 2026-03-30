# Experiment 10(e): AVL Tree - Left Rotation

## Aim
To write a Python function `def leftRotate(self, z)` to perform the left rotation operation in an AVL Tree. Additionally, insert '7' into the existing AVL Tree and perform the necessary rotations to balance it.

---

## Algorithm

1. Define the `TreeNode` class to represent each node in the AVL Tree with:
   - Key value
   - Left and right child pointers
   - Height of the node
2. Define the `AVL_Tree` class to manage AVL Tree operations.
3. In the `insert()` method:
   - Insert the key using Binary Search Tree (BST) logic.
   - Update the height of the current node.
   - Calculate the balance factor to check if the node is unbalanced.
   - Based on balance factor and key position, perform the necessary rotations (left or right).
4. Define the `leftRotate(z)` method:
   - Let `y = z.right` and `T2 = y.left`.
   - Make `z` the left child of `y`.
   - Assign `T2` as the right child of `z`.
   - Update the heights of `z` and `y`.
   - Return `y` as the new root of the subtree.
5. Insert the key '7' using the `insert()` method. If it causes an imbalance, perform the appropriate rotation.
6. Display the AVL Tree structure after insertion and rotations using preOrder traversal.

---

## Program

```
from TreeAVL.AVL import AVL
def Construct_AVL(L):
    t=AVL(L)
    print("Length of an AVL Tree is",t.length_tree)
```

## OUTPUT
<img width="1185" height="195" alt="image" src="https://github.com/user-attachments/assets/956c337f-3f3c-4797-8c00-ab4bee7719b4" />

## RESULT
Therefore, the output is the example to write a Python program to construct an AVL tree, balance it, and print the nodes before and after balancing using the appropriate packages and built-in function.
