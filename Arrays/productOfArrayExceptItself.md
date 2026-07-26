1. BFS:
- Nested loop, generate all values
- Calc new product for every i, in inner loop if(j!=i) prod *= nums[j]
- Push in result array ouytside inner loop
- TC: O(n^2) SC: (1)

2. OS:
- Prefix Sum technique for optimization
- DND: don't forget to declare size of ans array since we use ans[0] = 1 for leftProd of index 0 other wise null refrence error
- 1st: calculate leftProduct, store in ans vector only
- First index as 1 only since nothing on the left of it so leftProduct 1 => ans[0] = 1
- Traverse left to right, use: ans[l] = ans[l-1] * nums[l-1]
- 2nd- Find final result using rightProd variable
- From the last index, rightProd as 1 only since nothing on the right of it => rightProd = 1; 
- Traverse right to left, update the ans with ans[r] *= rightProd
- Update rightProd next, rightProd *= nums[r]
- TC: O(n+n) SC: O(n)
