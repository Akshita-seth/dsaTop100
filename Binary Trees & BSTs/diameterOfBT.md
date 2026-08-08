Diameter: 1: Longest path between two leave nodes 2. May or may not pass through the root node

Brute force = “keep asking every subtree its height again and again.”
Optimized = “ask once, and while you’re at it, also update the diameter.”

1. BFS:
- Heights are recalculated at each node separately.
- To compute height, you recursively traverse the subtree.
- If you do this for every node separately, you end up recalculating heights again and again.
- Global variable maxi
- Helper fn for finding ht (exactly same fn of height/depth calc), Bse case if root ==  null return 0
- In diameter fn also base case, then leftHt and rightHt calac using helper fn
- Then updating maxi with max(maxi, lh+rh)
- Then doing it for every node, i.e.diameter recursive fn for left and right
- TC: O(N^2) in worst case of Slewed trees, N - no. of nodes
- SC: O(H) → where H is the height of the tree. In worst case (skewed tree)=> H = N

2. Optimized:
- Here we don't recompute the heights for subtrees that we have already visited
-  Each node’s height is computed once and returned upward.
-  While backtracking: you use the returned left and right heights to update the diam = max(diam, leftHeight + rightHeight)
-  diam can be global or reference variable
-  helper fn findHeight with same baseCase
-  Calc lh and rh
-  Then updating diam
-  Then returning ht calc 1+max(lh,rh)
-  TC: O(N)
-  SC: O(H) → where H is the height of the tree. In worst case (skewed tree)=> H = N
