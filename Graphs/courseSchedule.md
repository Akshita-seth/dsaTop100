### Course Schedule 1
1. Using BFS:
- Kahn's algo
- No topo vector, just a counter every time after q.pop()
- return count == numCourses

2. Using DFS:
- Exactly like cycle detection (not like topo)
- No stack, only visited and pathVisited arrays
- Just return true/false in courseSchedule() will be reversed since if cycle yes then return false and vice versa (course completion requirement)


### Course Schedule 2
1. BFS:
- Kahn's algo
- Instead of counter, topo vector

2. DFS:
- Combo of topo and cycle detection
- Both stack and pathVis along with visited
- Return type of dfs still bool
- If true in course schedule fn return {} => cycle exists
- Otherwise, create topo vector (reverse of stack) and return
