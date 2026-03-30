# Experiment 10(a): AVL Tree

## Aim
To write a Python program to construct an AVL tree and print the nodes of it using the appropriate packages and built-in functions.

---

## Algorithm

1. Start the program.
2. Define a function `getDictTree(tree)` to return the dictionary representation of an AVL tree.
3. Define a function `Construct_AVL(L)` to:
   - Create an AVL tree from the list `L`.
   - Get and print the dictionary tree using `getDictTree(tree)`.
4. Define a list `L` with integer values.
5. Call `Construct_AVL(L)` to build the tree and print the result.
6. End the program.

---

## Program

```
from TreeAVL.AVL import AVL
def getDictTree(self):
    return self.dict_tree
def Construct_AVL(L,n):
    t=AVL(L)
    for i in n:
        t.insertNode(i)
    print(getDictTree(t))
```

## OUTPUT
<img width="1190" height="215" alt="image" src="https://github.com/user-attachments/assets/a2f31e15-8668-42d3-9155-85aea7abace6" />

## RESULT
Therefore, the output is the example to write a Python program to construct an AVL tree and print the nodes of it using the appropriate packages and built-in function
