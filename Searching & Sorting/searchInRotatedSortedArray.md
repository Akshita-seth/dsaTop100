1. BFS:
- Linear search
- TC: O(n) SC: O(1)

2. OS 1: two Binary search
- Pivot finding (O(log n)):
- Use binary search to find the smallest element (rotation point).
- If nums[mid] > nums[high], pivot lies to the right.
- Else pivot lies to the left.
- Binary search with pivot (O(log n)):
- Once pivot is found, treat the array as “virtually rotated back.”
- Adjust mid index with (mid + pivot) % n to map to the real index.
- TC: O(logn) SC:O(1)

But since this Sorted property is present, i think it cam be solved using Binary Search too [BinaryS => eliminate one half and find target in the other]

3. OS 2: Single Binary search
- This approach applies a modified version of binary search directly to the entire rotated array. At every iteration, the middle element is checked against the key.
- If it’s not the key, we determine whether the left half or right half is sorted by comparing values at arr[lo] and arr[mid].
- If the left half is sorted and the key lies within its range, we adjust hi = mid - 1; otherwise,
-  we shift lo = mid + 1. If the right half is sorted and the key lies within its range, we move lo = mid + 1; else, hi = mid - 1.
- So even with unique elements, you need <= to handle the edge case when the search window shrinks to size 1 or 2.
- Otherwise, the algorithm can go down the wrong branch and miss the target.
- TC: O(logN) SC: O(1)

