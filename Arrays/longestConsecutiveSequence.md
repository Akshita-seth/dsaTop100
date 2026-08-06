1. BFS:
- Using sorting
- Edge case imp bcz otherwise empty vector gets output as 1 since longest = 1 initialised
- Sort the array in ascending order.
- Initialise current count and longest as 1 since it includes the starting element
- Also longest 1 imp since if nums.size = 1 then that's only the longest
- Traverse the sorted array and skip duplicate elements.
- If the current element is one greater than the previous element, increment the current consecutive count and update the maximum count.
- Otherwise, reset the current consecutive count to 1.
- Return the maximum consecutive count.
- TC: O(n * log n), SC: O(1)



2. OS:
- The idea is to use Hashing.
- Edge case: if(nums.empty()) 
        return 0;
- We first insert all elements in a Hash Set.
- Iterate over the set, not the vector  This removes duplicates automatically and ensures each number is considered once.[]Also avoids TLE if 0<n<10^5]
- Check if the current element can be a starting element of a consecutive subsequence.
- How do we check? by checking of X-1 exists in set or not, if not then can be starting point so
- Start from X and keep checking furtehr elements X + 1, X + 2 .... to find a consecutive subsequence.
- Don't modify the original X hence store int curr = X and a cnt for current cnt = 0
- Calc longest = max(longest, cnt) within that if only (if possible to be starting pt for X)
- TC: O(n) Each number visited at most twice -> Once in the outer loop, once in the inner expansion. That’s why it’s truly O(N) average.
- SC: O(n)
