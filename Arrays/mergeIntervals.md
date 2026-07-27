1. BFS:
- Nested loop, i with 0, j with i+1
- For each interval, check against every other interval to see if they overlap.
- If yes, merge and keep repeating until no merge possible 
- TC: O(n^2) because for each interval you may scan all others repeatedly. SC: O(n) for visited.

2. OS:
- Sort based on start time + Single pass merge
- Sorting based on start time is done using lambda function
- Initialise ans vector with first interval (starting interval, since sorted)
- Start loop with i=1
- Take last as ans.back() and curr as intervals[i]
- Check for overlapping condition i.e. (curr[0] < last[1])
- If true, replace last[1] with max(curr[1], last[1])
- else just push curr into ans
- Remember to take the last vector as a reference since the change will be done in original ans vector
- TC: O(nlogn) due to sorting, plus O(n) for the merge pass.
