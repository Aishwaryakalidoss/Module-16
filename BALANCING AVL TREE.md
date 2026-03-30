# Experiment 10(b): Balancing AVL Tree

## Aim
To write a Python program to construct an AVL tree, balance it, and print the nodes of the tree before and after balancing using the appropriate packages and built-in functions.

---

## Algorithm

1. Start the program.
2. Define `getDictTree(self)` to return the dictionary representation of the AVL tree.
3. Define `Construct_AVL(L)` to:
   - Create the AVL tree from the list `L`.
   - Print the tree before balancing.
   - Balance the tree using the `BalanceTree()` method.
   - Print the tree after balancing.
4. Create a list `L` of integers.
5. Call `Construct_AVL(L)` to build and balance the tree.
6. End the program.

---

## Program

```
class TreeNode(object):
	def __init__(self, val):
		self.val = val
		self.left = None
		self.right = None
		self.height = 1
class AVL_Tree(object):
	def insert(self, root, key):
		if not root:
			return TreeNode(key)
		elif key < root.val:
			root.left = self.insert(root.left, key)
		else:
			root.right = self.insert(root.right, key)
		root.height = 1 + max(self.getHeight(root.left),
						self.getHeight(root.right))
		balance = self.getBalance(root)
		if balance > 1 and key < root.left.val:
			return self.rightRotate(root)
		if balance < -1 and key > root.right.val:
			return self.leftRotate(root)
		if balance > 1 and key > root.left.val:
			root.left = self.leftRotate(root.left)
			return self.rightRotate(root)
		if balance < -1 and key < root.right.val:
			root.right = self.rightRotate(root.right)
			return self.leftRotate(root)
		return root
	def leftRotate(self, z):
		y = z.right
		T2 = y.left
		y.left = z
		z.right = T2
		z.height = 1 + max(self.getHeight(z.left),
						self.getHeight(z.right))
		y.height = 1 + max(self.getHeight(y.left),
						self.getHeight(y.right))
		return y
	def getHeight(self, root):
		if not root:
			return 0
		return root.height
	def getBalance(self, root):
		if not root:
			return 0
		return self.getHeight(root.left) - self.getHeight(root.right)
	def preOrder(self, root):
		if not root:
			return
		print("{0} ".format(root.val), end="")
		self.preOrder(root.left)
		self.preOrder(root.right)
myTree = AVL_Tree()
root = None
n=int(input())
root = myTree.insert(root, 13)
root = myTree.insert(root, 10)
root = myTree.insert(root, 15)
root = myTree.insert(root, 5)
root = myTree.insert(root, 11)
root = myTree.insert(root, 16)
root = myTree.insert(root, n)
print("Preorder traversal of the constructed AVL tree is")
myTree.preOrder(root)
print()
```
## OUTPUT
<img width="1187" height="279" alt="image" src="https://github.com/user-attachments/assets/14206faf-b38e-478b-8906-4935f8b6438f" />

## RESULT
Therefore, the output is the example to write a Python function def leftRotate(self, z): to perform the left rotation operation in an AVL Tree and insert the element '7' into it.
