# RedBlackBinarySearchTree
1. what is a tree
2. what is binary tree
3. what is binary search tree
4. where is it used - what are the operations? search,insert, delete.
5. what is the time complexity of a skewed , non-balanced BST
6. what is the impact
7. how can we improve
8. auto balancing techniques for BST
9. what does the red black algorithm mean
10. working demo on white board for non-balanced vs balanced BST
11. code run
12. time complexity of balanced BST
13. questions



what is a tree?

hierarchal abstract data structure to preserve data in form of parents and children.
non-linear

what is a binary tree ?

tree where there can be maximum of two children for each parent.

what is binary search tree
A Binary Search Tree (BST) is a treein which all the nodes follow the below-mentioned properties − 
The left sub-tree of a node has a key less than or equal to its parent node's key. The right sub-tree of a node has a key greater than to its parent node's key.

where is it used? why talk about trees at all?

sorted map use cases
for example: CMS data needs sorting based on indices , however it is a map of module vs data. It needs random access as well.

So basic operations of a BST are:
i. insert, ii. search, iii. delete.

time complexity of the operations in a non-balanced binary tree is :
O(n) 

for example: 
45,54,65,99,100,101,110,300,500,600,1000,1001,5000,7000,9000

Impact is:

When there are millions of data a difference between O(log n) vs O(n) is huge. 

n = 1,000,000, for example, the minimum height is log-2-(1 million) = 19

How can we improve?

What if we created a BST which automatically maintains its balance to make that it is equal on left and right.
A balanced tree = left height - right height < = 1
left subtree and right subtree are balanced too

Now there are 2 primary algorithms which does it for us:

RED BLACK tree
AVL tree

RED BLACK tree:

each node will have an extra element color.
color - red/black

Rules:

1. root node will be black
2. no RED - RED child parent relationship
3. Number of black nodes from X node to a NIL node should be equal for all the paths we can traverse from that node to NIL.


How to balance?

1. empty tree - insert red
2. if parent is black great ! insert
3. if parent is RED - then look at uncle - if he is RED too - change both parent and uncle to black and grandfather to RED. - do a recursive check on grandfather.
4. if parent is RED and uncle is BLACK or NIL then rotate grandfather on the opposite side of the tree.


data to demo:

45 54 65 99 100 101 110 300 500 600 625 650 700 1000 1200 5000 7000 8000 9000
