1. BFS
- For n numbers there n! ways i.e. permutations
- Lexicographical => if [1,2,3] then 1,2,3 ; 1,3,2 ; 2,1,3 ; 2,3,1 ; 3,1,2 ; 3,2,1 =? 123 < 132 < 213 < 231 < 312 < 321
- generate all permutatioms for a given set of numbers => using recursion
- Do a linear search and find the index of the given permutation then return the next
- If last given then return first // edge case
- TC: O(n! * n) , SC: O(n! * n) since n! permutations to be generated and each is of length n
- Time is of very high order

2. Alternate Optimized soln if C++ is used => an STL exists [InBuilt Fn]
- next_permutation(arr.begin (), arr.end());
- return arr;
- This STL automatically changes the array to its next permuted array
- TC: O(n), SC: O(1)


3. OS
- 1st Observation is: Longer prefix match find so where's the break point? move from right to left -> if (arr[i] < arr[i+1])
- 2nd: To replace arr[i], move from right and find num just greater than arr[i], i.e. next greater
- 3rd: Now place the remaining places with the remaining numbers in ascending sorted order, so that it's nearest to the given array
- Find the break point; the least place of finding a dip is n-2, hence start loop from n-2 till >=0, if break condition satisfies store idx and break.
- Keep idx = -1 before loop, so if no break found i.e. the last permutation given, just reverse the array and return i.e. the first permutation
- Now loop from right end to idx and find number next greater to idx value and swap with the first value u get greater
  The suffix (to the right of idx) is guaranteed to be descending (because idx was the first drop).
So:

If we scan from the right, the first element we encounter that’s greater than nums[idx] is automatically the smallest possible greater element.
- For last, we just reverse the suffix from arr.egin() + idx+1 to arr.end() for array
- TC: O(n) SC: O(1)
