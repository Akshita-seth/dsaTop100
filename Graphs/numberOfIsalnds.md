1. Using DFS:
- Matrix qs should be preferred to solved via dfs
- No. of islands is equivalent to no. of components
- visited array should be in grid (m x n) -> vector<vector<int>> visited(m, vector<int>(n,0));  
- Hence i j loop for matrix in islands fn where if land found && not visited found -> dfs exploration sent
- dfs(i,j,m,n,grid,visited)
- initialise dx and dy
- Loop k=0 -> <4
- Calc neighbours ni and nj
- Check if within boundaries (both from left and right), land and not visited -> dfs of ni and nj
- TC: O(m·n) since each cell is visited once.
- SC: O(m·n) for the visited matrix plus recursion stack in worst case.


2. Using BFS:
- Eveyrthing similar till i j loop for matrix in islands fn
- Remember to make dx and dy before i j loop
- Start BFS
- queue initialised to take pairs as in {i,j}, mark visited
- Loop until q not empty
- use auto or first second as r and c taken as front
- then popped
- k loop
- then calculate neighbours i.e. nr and nc
- checked condition if true => mark visited, q.push({nr,nc})
- TC: O(m.n) SC: O(m.n)


3. BFS Without visited array [Since modifies given input so don'tuse, just know]
- BFS without visited array, not advised in interviews but u should know how flipping 1's in grid to 0 when visited saves the memory of extra visisted matrix. 
- The grid values with 0 i.e. water are not traversed by the loop; similarly, the grid values with 0 i.e. already visited ones will also not be traversed again.
