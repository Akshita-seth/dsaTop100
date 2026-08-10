1. BFS (Level Order Traversal)
- Traverse level by level using a queue.
- At each level, record the last node’s value.
- Add that to your answer.
- TC: O(N) SC: O(N)

2. DFS (Recursive Preorder with Right Priority)
- Traverse root → right → left.
- Keep track of the current depth.
- If it’s the first time you’re visiting that depth, record the node’s value.
- This ensures the rightmost node at each level is captured.
-  Depth tracking: Each recursive call carries the current depth.
- First visit rule: If depth == ans.size(), it means we haven’t recorded a node at this level yet → push the current node’s value.
- Right-first traversal: Ensures the rightmost node is seen before any left nodes at the same depth.
- TC: O(N) SC: O(H)

3. Morris Traversal
- TC: O(N) SC: O(1)
