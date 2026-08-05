1. Soln:
- Not in lexicographical order
- Sent to helper function (nums,0,n-1,all)
- Base case left == right, push nums in alla nd return
- i loops from l to r
- Swapping nums of l and i
- Recursive fn calling with l+1
- Swapping again to get back original <- Backtracking Step
- - TC: O(n!.n) SC: O(n!.n) [output storage] + O(n) [recursion depth]



2. Soln with STL:
- Sort given array to get all permuattaions, along with in lexicographic order
- do push nums while next_permutation(nums.begin(), nums.end())
- TC: O(n!.n) SC: O(n!.n) [output storage] 
