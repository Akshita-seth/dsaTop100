1. BFS:
- Nested loop, i starts with 0, j with i+1
- Find max of prices[j] - prices[i]
-  TC(N^2) SC:O(1)

2. OS:
- One scan solution
- Keep track of min price, initially prices[0]
- Compute profit if sold today, update max profit
- Update min price if today's price lower
- TC: O(N) SC: O(1)
