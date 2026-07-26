1. BFS:
- Nested loop
- Calc each element’s frequency in j loop (inner) by scanning entire array and calc freq of arr[i] at a time
- Check for > n/2
- TC: O(n^2) SC: O(1)

  2. BS:
  - Using unordered map
  - One pass to build frequency map
  - One pass to check majority
  - TC: O(n) SC: O(n)

  3. OS:
  - Boyer-Moore / Majority vote Algorithm
  - Intuition: Pair off different elements until one survives — the survivor must be the majority
  - Keep a candidate and a counter.
  - Traverse the array:
  - If counter is 0 → set candidate = current element.
  - If current element == candidate → increment counter.
  - Else → decrement counter.
  - At the end, candidate is the majority element.
  - Calculating majority element in linear time and constant space
  - TC: O(n), SC: O(1)
