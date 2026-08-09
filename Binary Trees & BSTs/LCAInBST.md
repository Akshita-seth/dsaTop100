1. BFS: Generic Binary Tree LCA Soln
- Recursive soln
- TC: O(N) SC:O(H)

2. BS:
- Using BST properties but recursively
- This approach takes advantage of the Binary Search Tree (BST) property to avoid searching the entire tree.
- Starting from the root, if both n1 and n2 have values smaller than the current node, then the LCA must be present in the left subtree.
- Similarly, if both values are greater than the current node, then the LCA must be present in the right subtree.
- Otherwise, the current node is the first node where the paths to n1 and n2 split, making it their Lowest Common Ancestor.
- here 4 returns: 1st Base Case, 2nd if both nodes in left subtree, 3rd if both in right, 4th if they got split by current node
- TC: O(H) SC:O(H)

3. OS:
- using BST properties iteratively
- The recursive approach can be optimized by eliminating the recursion stack.
- Instead of making recursive calls, we iteratively traverse the BST from the root, i.e.e while(root)
- At each node, if both n1 and n2 are smaller than the current node, we move to the left child.
- If both are greater, we move to the right child.
- Else the current node is the first node where the paths to n1 and n2 diverge, making it their Lowest Common Ancestor, just return the current node i.e. root
- TC: O(H) SC: O(1)
