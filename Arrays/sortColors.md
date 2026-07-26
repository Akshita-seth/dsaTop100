1. BFS:
- Count number of 0s, 1s and 2s in one pass
- Overwrite in the array using 3 while loops, one for each 0, 1 & 2
- TC: O(n) SC:O(1)

2. OS:
- Dutch National Flag Algorithm - the famous three-pointer approach
- We maintain three pointers: low → boundary for 0s, mid → current element being checked, high → boundary for 2s
- DNF partitions the array into three regions dynamically
- Traverse with mid: while(mid <=high)
- If nums[mid] == 0 → swap with low, increment both.
- If nums[mid] == 1 → just increment mid.
- If nums[mid] == 2 → swap with high, decrement high.
- TC: O(n) SC:O(1)
