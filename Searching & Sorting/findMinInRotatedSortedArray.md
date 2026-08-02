1. BFS:
- Linear search
- TC: O(n) SC: O(1)

2. OS: 
- Binary search
- If arr[low] < arr[high], the current range is already sorted, return arr[low].
- Loop while(low < high) not <= since when low == high, min found
- Compute mid.
- If arr[mid] > arr[high], the minimum lies to the right of mid, set low = mid + 1.
- Otherwise, the minimum lies at mid or to its left, set high = mid.
- When low == high, that index stores the minimum element.
- TC: O(logN) SC: O(1)
