1. BFS:
- Nested loop i and within it expanding left and right (two separate loops)
- Fix bar i as the limiting height.
- Expand left and right while bars are ≥ arr[i].
- For each expansion, add that fixed height again.
- So effectively, curr = arr[i] * width.
- TC: O(N^2), SC: O(1)

2. 
