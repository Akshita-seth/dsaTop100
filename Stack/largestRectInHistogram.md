1. BFS:
- Nested loop i and within it expanding left and right (two separate loops)
- expand towards the left and right while the bars are at least as tall as the current bar.
- Fix bar i as the limiting height.
- Expand left and right while bars are ≥ arr[i].
- For each expansion, add that fixed height again.
- So effectively, curr = arr[i] * width.
- TC: O(N^2), SC: O(1)

2. OS 1: Using two stack traversals
- Keep in mind: 1: In NSE assign default value n(size of array)
                2: In PSE assign default value -1
- area at every idx i = arr[i] * (nse[i] - pse[i] - 1)
- calc maxi everytime in i loop 
- Two helper fns for SNSE and PSE -> both storing indexes of same and not values so slight modification do
- Key difference
   Left → right NSE: assign to the popped index (nse[st.top()] = i).
   Right → left NSE: assign to the current index (nse[i] = st.top()). [Prefer for NSE]

   left→right PSE: updates(assigns to) current index (pse[i] = st.top();) [Prefre for PSE]
   right→left PSE: updates popped indices. (pse[st.top()] = i)
- TC: O(2N) + O(2N) + O(N)
- SC: O(2N) + O(2N)

3. OS 2: Obe stack soln
-
