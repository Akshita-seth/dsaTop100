1. Using BFS:
- Kahn's algo
- No topo vector, just a counter every time after q.pop()
- return count == numCourses

2. Using DFS:
- Exactly like cycle detection (not like topo)
- No stack, only visited and pathVisited arrays
- Just return true/false in courseSchedule() will be reversed since if cycle yes then return false and vice versa (course completion requirement)
