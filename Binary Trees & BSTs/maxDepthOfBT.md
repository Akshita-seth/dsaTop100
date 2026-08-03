1. Recursive soln:
- “At each node, depth = 1 + max(depth of left, depth of right).”
- Edge case root == NULL return 0 [here base case of recursion]
-  TC: O(N)
-  SC: O(height of tree), i.e. O(N) worst case, O(log N) best case for balanced trees.

2. Iterative: Level Order Traversal
- Traversing level by level with depth++ wil give the depth of BT
- Edge case root == NULL return 0
- Initialiose q and push root
- Loop while q not empty
- Calc size before hand bcz it will during the course of for loop
- Loop from i to q size
- Store front of q in node
- Check if left of node exists, if yes push into q
- Same for right
- After for loop increment depth
- TC: O(N) Every node is enqueued and dequeued once → O(2N).
- SC: O(N) Worst Case if complete BTand O(width of tree), (width is less than N) if balanced tree
