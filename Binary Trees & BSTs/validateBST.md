1. BFS:
- Do an inorder traversal, store all values in a list, then check if the list is strictly increasing 
- TC: O(N) SC: O(N)

2. OS:
- Helper fn used, that accepts Root, minVal nd maxVal
- Three returns: 1st if root is null -> true
- 2nd if the root val lie beyond the range -> false
- 3rd recursive fn root->left && recursive fn root->right
- In validate fn just return statement with recursive fn calling (root, LONG_MIN, LONG_MAX)
- Each node is checked against its global bounds, not just its parent.
- TC: O(N) SC: O(H)
