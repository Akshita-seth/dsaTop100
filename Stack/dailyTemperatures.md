1. BFS:
- nested loop
- 2 imp things: 1. initialise, 2. Break
- TC: O(N^2) SC: O(1)

2. OS;
- Monotonic (decreasing) Stack
- Stack stores indices, not values
- Pop when temp[currentIdx] > temp[st.top() Idx]
- Answer = current index − popped index
- Each element pushed and popped once
- TC: O(N) SC: O(N)
 
