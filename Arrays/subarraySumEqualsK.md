1. BFS:
- Nested loop -> generate all subarrays
- Check with target and count
- TC: O(n^2) SC: O(1)

3. OS:
- Prefix Sum technique
- For best explanation: https://takeuforward.org/arrays/count-subarray-sum-equals-k
- Approach: V.Imp 1. Storing key as prefix sum and value as freq{prefixSum -> freq}
                  2. prefixSum[0] =1; first entry in map
- First, we will declare a map to store the prefix sums and their counts.
- Then, we will set the value of 0 as 1 on the map.
- Then we will run a loop(say i) from index 0 to n-1(n = size of the array).
-For each index i, we will do the following:
- We will add the current element i.e. arr[i] to the prefix sum.
- We will calculate the prefix sum i.e. x-k, for which we need the occurrence.
- We will add the occurrence of the prefix sum x-k i.e. mpp[x-k] to our answer.
- Then we will store the current prefix sum in the map increasing its occurrence by 1.
- TC: O(n) SC: O(n)
