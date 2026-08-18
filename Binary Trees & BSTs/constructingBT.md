1. Constructing BT from Pre and In Order
- Helper fn for building(pre, start, end, in, start, end, map)
- Map used to map {value->index} for inorder
- base case check: start > end for either pre || in then return
- initialise root as pre[start]
- find inRootIdx = map[root->val]
- find left size = inRootIdx - inStart
- root->left = building(preorder, preStart+1, preStart+leftSize, inorder, inStart, inRootIdx-1, mpp);
- root->right = building(preorder, preStart+leftSize+1, preEnd, inorder, inRootIdx+1, inEnd, mpp);
- returns root
- TC: O(N) SC: O(N)


2. Constructing BT from Post and In Order
- Helper fn for building(post, start, end, in, start, end, map)
- Map used to map {value->index} for inorder
- base case check: start > end for either post || in then return
- initialise root as post[end]
- find inRootIdx = map[root->val]
- find left size = inRootIdx - inStart
- root->left = building(inorder, inStart, inRootIdx-1, postorder, postStart, postStart+leftSize-1, inMap);
- root->right = building(inorder, inRootIdx+1, inEnd, postorder, postStart+leftSize, postEnd-1, inMap);
- returns root
- TC: O(N) SC: O(N)
