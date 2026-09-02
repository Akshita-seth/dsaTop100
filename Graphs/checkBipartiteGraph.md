Soln:
- Use color[] array, init all -1 (uncolored).
- For each uncolored node, start DFS with color 0.
- In DFS: assign current node its color.
- For each neighbor:
- If uncolored → assign opposite color (1 - color[node]) and recurse.
- If already colored and same as current → conflict → return false.
- If all DFS calls succeed → graph is bipartite.
- TC:  O(V + 2E), Where V = Vertices, 2E is for total degrees as we traverse all adjacent nodes.
- SC: O(3V) ~ O(V), Space for DFS stack space, colour array and an adjacency list.
