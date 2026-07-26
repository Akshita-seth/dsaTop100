1. BFS:
- Nested loop
- Find new area for every i with every j
- area = (j-i) * min(height[i], height[j])
- Update max area in inner loop only, DND -> not in outer loop
- TC: O(n^2)  SC:O(1)

2. OS:
- Two pointers approach
- left and right pointers set, loop while(l<r)
- calc area similar to above, then 
- Always move the pointer that points to the lower line.
- TC: O(n) SC: O(1)
