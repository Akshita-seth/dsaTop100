1. BFS:
- Nested loop
- IMP: 1. Initialise the size of array 2. Break
- TC: O(N^2) SC: O(N) for ans vector

2. OS:
- Monotonically increasing stack (st.top() >= curr element) => pop stack
- Traverse right to left since NEXT is asked
- Initialise ans array (n,-1)
- TC: O(N) SC: O(2N)
