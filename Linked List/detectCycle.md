1. BFS
- Using a map to store visited nodes and finding if an already visited node is encountered or not
- TC: O(N*1) best and avg case, (N*N) worst case for unordered map and O(N*logN) if ordered map used
- we traverse the entire linked list once so N TC and store and retrieve nodes from the hash map. Map operations since unordered map used hence 1 or N, if ordered map used them TC: O(logN) for all best, avg and worst. 
- SC: O(N)

2. OS
- Fast and Slow Pointer
- We traverse the entire linked list once. The fast pointer either reaches the end of the list or meets the slow pointer in linear time.
- loop while fast != null && fast->next != null
- move fast and slow, checek if fast and slow same, if yes return true
- TC: O(n), SC: O(1)
  ##### Remember: in case of dining mid of linkedlist => os: just return slow pointer => TC: O(N/2)
  - and for BFS: just count total nodes - c by traversing the list, calc mid = c/2 + 1, again traverse list till mid = 0 by decrementing mid inside loop, just return the pointer temp uptil that bcs break done when mid == 0 => TC: O(N + N/2)
