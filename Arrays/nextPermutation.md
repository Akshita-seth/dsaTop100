1. BFS
- For n numbers there n! ways i.e. permutations
- Lexicographical => if [1,2,3] then 1,2,3 ; 1,3,2 ; 2,1,3 ; 2,3,1 ; 3,1,2 ; 3,2,1 =? 123 < 132 < 213 < 231 < 312 < 321
- generate all permutatioms for a given set of numbers => using recursion
- Do a linear search and find the index of the given permutation then return the next
- If last given then return first
- TC: O(n! * n) , SC: O(n! * n) since n! permutations to be generated and each is of length n
- Time is of very high order

2. Alternate Optimized soln if C++ is used => an STL exists [InBuilt Fn]
- next_permutation(arr.begin (), arr.end());
- return arr;
- This STL automatically changes the array to its next permuted array
- TC: O(n), SC: O(1)


3. OS
- 1st Obervation is: i) Longer prefix match find so where's the break point? move from right to left -> if (arr[i] < arr[i+1]) 
