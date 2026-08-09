Soln:
- Make the lca fn recursive
- Base case: root is null || root is p || root is q => return root
- Accept TreeNode* in left and right with each recursion going left and right, respectively
- If both left right exist -> return root
- Otherwise just return left? left: right;
- TC: O(N), In the worst case, we may need to traverse all nodes to find the LCA.
- SC: O(H), This is due to the recursive stack space used during the traversal. In the worst case, for a skewed tree, H can be equal to N, but for a balanced tree, H will be log(N).
