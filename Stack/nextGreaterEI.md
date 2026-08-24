1. BFS:
- Nested loop i=0 and j=i+1
- Imp to initialize size of ans vector filled with -1.
- Imp to break after nge found for every index; otherwise, -
- TC: O(N^2)  SC: O(1)

2. OS:
- Monotonic stack => A decreasing stack intuition
- Initialize an empty stack and a result array of the same length as input.
- Traverse the array from the last element to the first (right to left).
- For each element, pop elements from the stack while the stack top is less than or equal to the current element.
- If the stack becomes empty, no greater element exists, assign -1 in the result.
- Otherwise, the top of the stack is the next greater element for the current element.
- Push the current element onto the stack for use in future comparisons.
- TC: O(N) SC: O(N)

3. LeetCode-type array and subarray version
- SImilar monotonic stack 
- Just nge map instaed of array  Store this mapping in a hashmap: {element → nextGreater}
- For each element in nums1 i.e. traverse over n1 (subset of n2), just look up the precomputed hashmap and store in anotehr ans vector that will be returned
