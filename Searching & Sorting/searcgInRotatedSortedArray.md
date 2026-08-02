1. BFS:
- Linear search
- TC: O(n) SC: O(1)

But since this Sorted property is present, i think it ca be solved using Binary Search too [BinaryS => eliminate one half and find target in the other]

2. OS :
- Here one half is sorted and the other is not
- Hence, identify the sorted half => HOW? sorted Property -> check if arr[low] < arr[mid]
- Start with initialising low, high. Calc mid
- if mid is target return; otherwise check which half is sorted left/right [Guaranteed either of the halves is sorted]
- when sorted hald found -> check if target exists in that half, update low and high accordingly
- Repeat until target found
- So even with unique elements, you need <= to handle the edge case when the search window shrinks to size 1 or 2.
- Otherwise, the algorithm can go down the wrong branch and miss the target.
- TC: O(logN) SC: O(1)

