1. BFS:
 - The brute force way is to dump both lists into an array, sort, and rebuild.
 - Collect all values into a vector, by traversing on each loop i.e. two passes
 - Then just sort
 - Then build a new linked list using dummy node from the sorted vector, and return dummy->next
 - TC: O((m+n)log(m+n) => Traversion both lists is O(m+n). Sorting is O((m+n)log(m+n)). Rebuilding is O(m+n)
 - SC: O(m+n) due to the vector.

2. OS:
- Using dummy node
-  TC: O(M+N) since both lists traversed once
Sc: O(1)
