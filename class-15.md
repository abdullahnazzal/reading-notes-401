
# Trees

# Common Terminology
**Node** - A Tree node is a component which may contain it’s own values, and references to other nodes.

**Root** - The root is the node at the beginning of the tree
K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.

**Left** - A reference to one child node, in a binary tree.

**Right** - A reference to the other child node, in a binary tree.

**Edge** - The edge in a tree is the link between a parent and child node.

**Leaf** - A leaf is a node that does not have any children.

**Height** - The height of a tree is the number of edges from the root to the furthest leaf.

## **Traversals**
An important aspect of trees is how to traverse them. Traversing a tree allows us to search for a node, print out the contents of a tree, and much more! There are two categories of traversals when it comes to trees:

-   Depth First
-   Breadth First

**Depth First**
Depth first traversal is where we prioritize going through the depth (height) of the tree first. There are multiple ways to carry out depth first traversal, and each method changes the order in which we search/print the root. Here are three methods for depth first traversal:



```py
Pre-order: root >> left >> right
In-order: left >> root >> right
Post-order: left >> right >> root
```

**Breadth First**

Breadth first traversal iterates through the tree by going through each level of the tree node-by-node. So, given our starting tree one more time:


Our output using breadth first traversal is now:
```py
Output: A, B, C, D, E, F
```


```py
Pseudocode
Here is the pseudocode, utilizing a built-in queue to implement a breadth first traversal.

ALGORITHM breadthFirst(root)
// INPUT  <-- root node
// OUTPUT <-- front node of queue to console

  Queue breadth <-- new Queue()
  breadth.enqueue(root)

  while breadth.peek()
    node front = breadth.dequeue()
    OUTPUT <-- front.value

    if front.left is not NULL
      breadth.enqueue(front.left)

    if front.right is not NULL
      breadth.enqueue(front.right)

```

***
**To know more please [visit this page](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)**
***

