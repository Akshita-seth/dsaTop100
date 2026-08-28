1. DFS:
- No need of counting componenets type loops, just durecty call dfs(sr,sc,m,n,orgColor, color, image)
- Before this do this:  if(orgColor == color) 
                         return image; // to avoid unnecessary recursion
- In dfs helper fn: similar assigns color -> Creates dx, dy ->mK loop 0 to <4 -> Cgeckinh boundaries, id it has orgColor or not -> dfs with neighbour indices
- TC: O(M*N) each cell visited at most once
- SC: O(M*N) due to recursion in worst case i.e. all cells connected

2. BFS:
- On similar lines, no componenets loop
- Just q not empty loop -> k loop
- q with pairs initialised
- TC: O(M*N) each cell visited at most once
- SC: O(M*N)  queue can hold all cells in worst cas
