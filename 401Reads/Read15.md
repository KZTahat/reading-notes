# Read 15

## Trees

- `Common Terminology`

  - Node - A Tree node is a component which may contain it’s own values, and references to other nodes
  - Root - The root is the node at the beginning of the tree
  - K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
  - Left - A reference to one child node, in a binary tree
  - Right - A reference to the other child node, in a binary tree
  - Edge - The edge in a tree is the link between a parent and child node
  - Leaf - A leaf is a node that does not have any children
  - Height - The height of a tree is the number of edges from the root to the furthest leaf

- `Sample Tree :`

<img src="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG"
     alt="code-challenge-2 whiteBoard"
     style="float: left; margin-right: 10px;" />

- Traversals
  An important aspect of trees is how to traverse them. Traversing a tree allows us to search for a node, print out the contents of a tree, and much more! There are two categories of traversals when it comes to trees:

  - Depth First.

    - Pre-order: root >> left >> right
    - In-order: left >> root >> right
    - Post-order: left >> right >> root

  - Breadth First.

- `Binary Tree Vs K-ary Trees`

In all of our examples, we’ve been using a Binary Tree. Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).<br />

There is no specific sorting order for a binary tree. Nodes can be added into a binary tree wherever space allows. Here is what a binary tree looks like:

<img src="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree2.PNG"
     alt="code-challenge-2 whiteBoard"
     style="float: left; margin-right: 10px;" />

If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree. In this type of tree we use K to refer to the maximum number of children that each Node is able to have.

<img src="https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/KaryTree1.png"
     alt="code-challenge-2 whiteBoard"
     style="float: left; margin-right: 10px;" />

- `Adding a node`

Because there are no structural rules for where nodes are “supposed to go” in a binary tree, it really doesn’t matter where a new node gets placed.

One strategy for adding a new node to a binary tree is to fill all “child” spots from the top down. To do so, we would leverage the use of breadth first traversal. During the traversal, we find the first node that does not have all it’s children filled, and insert the new node as a child. We fill the child slots from left to right.

In the event you would like to have a node placed in a specific location, you need to reference both the new node to create, and the parent node upon which the child is attached to.

- `Searching a BST`
  Searching a BST can be done quickly, because all you do is compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.

- `Big O`

The Big O time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n). Because of the lack of organizational structure in a Binary Tree, the worst case for most operations will involve traversing the entire tree. If we assume that a tree has n nodes, then in the worst case we will have to look at n items, hence the O(n) complexity.

The Big O space complexity for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree. For example, in the above tree, w is 4.

A “perfect” binary tree is one where every non-leaf node has exactly two children. The maximum width for a perfect binary tree, is 2^(h-1), where h is the height of the tree. Height can be calculated as log n, where n is the number of nodes.

The Big O time complexity of a `Binary Search` Tree’s insertion and search operations is O(h), or O(height). In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced (or “perfect”) tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.

The Big O space complexity of a BST search would be O(1). During a search, we are not allocating any additional space.

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)
