This is the Connected Components in Undirected Graph pattern. You can solve it using:
1. DFS/BFS traversal:
- Counting Componenets version
- Create an adjacency list bcz the neighbours are not explicit in form of grids(as in acse of number of islands)
- Mark visited nodes, increment count when you start a new traversal (DFS or BFS helper fn)
- TC: O(V+2E), we visit every node and for every node we visit all of its neighbours in the DFS traversal.
- SC: O(V), for storing visited array and auxiliary stack space.

 
2. Union-Find (Disjoint Set Union):
- Impleemnt the DijointSet class with union and parent functions
- No need to create any adj list
- Create dijoint set by calling its classname and sneing n (num of nodes)
- Just nested i, j loop, whenevr isConnecetd[i][j] is 1, call unionBySize pr Rank
- Traverse i for n times and then if(findUPar(i) == i) do provinces++
- TC: O(N^2), SC: O(N)
