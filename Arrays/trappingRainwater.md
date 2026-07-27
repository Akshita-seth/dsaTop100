1. BFS:
- Nested loop: i traverses the entire height array
- maxLeft and maxRight are initialised to 0 for every new i
- j loop from 0 to <=i for maxLeft  [Remember the limits, DND]
- j loop from i to <n for maxRight
- Total trapped water formula: at end of i loop calc -> total += min(maxLeft, maxRight) - height[i]
- TC: O(n^2) SC: O(1)

2. OS:
- Two Pointer approach: One pass soln
- The key insight is that the amount of water trapped at any position depends on the tallest bars to the left and right of that position
- Initialise two pointers: left & right, maxLeft, maxRight initialsed to 0 and total = 0
- while(left <= right)
- If the height at the left pointer is less than or equal to the height at the right pointer:
- If the height at left is greater than or equal to maxLeft, update maxLeft.
- Else, add the difference between maxLeft and the current height at left to totalWater.
- Move the left pointer one step right. [REMEMBER: left++ can be inside this above else or outside, both correct, explained below]
-  If left++ / right-- are placed inside the water‑calculation else, the pointer moves only when water is added.
-  If they’re placed outside, the pointer moves every iteration — but it’s still correct because when boundaries are updated, water at that index is zero, so skipping forward is safe.
- Similar for maxRight in else i.e. height[right] > height[left]
- TC: O(n) SC: O(1)
