1. BFS:
- Nested loop to generate all subarrays
- Since negative nums also allowed, initialize maxSum as nums[0] and not just 0
- Calc new sum for every i in the inner loop
- Update maxS in inner loop
- TC: O(N^2) Sc: (1)

2. OS:
- Kadane's Algo for optimization since negative numbers present
- If extending makes the sum worse, you “slide” the window to start forward to current i.
- So Kadane’s is a greedy sliding window that shrinks instantly when the prefix sum goes negative
- One-pass soln: in each pass -> To decide: extend or restart
- Keep track of current window sum and best seen so far, initialise both as nums[0]
- Start loop with 1 since window already has the 0th index value
- If you start the loop at i = 0, you’d reprocess the first element unnecessarily.
- Worse Situation, you’d compare nums[0] against curr + nums[0], which is like adding it twice.
- Wrong sum (nums[0] twice) gets carried forward
- TC: O(N), SC:O(1)
