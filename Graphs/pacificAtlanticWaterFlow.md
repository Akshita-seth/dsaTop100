Soln:
- Two reachability matrices -> pacific and atlantic
- Reverse dfs/bfs since from borders towards the centre traversal
- DFS called from borders only: 1st loop (traversing for row times) -> Left and right of matrix, 2nd loop (traversing for column times) -> top and bottom
- Fill the reachability matirces in the dfs
- In dfs -> same stuff, direction vector -> K loop 0 to <4 -> Checing valididty Within limits && reachability false (not yet visited) && heights[ni][nj] >= heights[i][j]
- This heights[ni][nj] >= heights[i][j] is bcz => We are coming from borders to towrds the centre of island, the condition was water will flow from island to border(then eventually to the ocean) if ht f neighbouring cells is less, so since vsiting in opp dir hence condition alo reversed
- Result matirx is intersection of both pacific and atlantic true cells
- TC: M*N SC: M*N
