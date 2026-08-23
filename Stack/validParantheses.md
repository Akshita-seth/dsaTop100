Solution: Using a stack
- Traverse char by char in the given string
- If its one of the open brackets -> push in stack
- else if closing bracket -> (check if stack empty return false) -> Process the top & Check pair of brackets, if not return false
- st.pop at last of loop
- Just return st.empty()
- TC: O(N) SC: O(N)
