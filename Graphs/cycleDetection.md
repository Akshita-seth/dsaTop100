1. In undirected graph: Loop component wise, return type - bool fro helepr fns
- Track both node and parent
- In dfs using recursion send a parent parameter in helper fn dfs
- In bfs make the queue store pairs {node, parent}
- TC: O(V+E) each node and edge visited once
- SC: O(V+E) adjacency list, recursion stack/queue and visited array

2. In directed graph: Loop component wise
- For DFS approach: Use visited and pathVisited array, recursive DFS helper fn
- TC: O(V+E)+O(V) , visit each vertex once and traverse each edge once. There can be at most V components. So, another O(V) time complexity.
- SC: O(2V + O(V) ~ O(2V): O(2V) for two visited arrays and O(V) for recursive stack space.

- For BFS approach - Kahn's algo, Use of indegree array instead of visited
-  TC: O(V + E) because we visit each vertex exactly once and process all outgoing edges from each vertex exactly once. 
- The in-degree calculation takes O(E), and each vertex is enqueued and dequeued exactly once in O(V). Thus, total time is linear in the sum of vertices and edges.
- SC: O(V + E) because we store the adjacency list which takes O(E) space, the in-degree array which takes O(V), the queue which can store up to O(V) vertices at a time, 
- and the topological order array which takes O(V). Overall, the space requirement is proportional to the size of the graph.
