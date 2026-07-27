1. BFS:
- helper fn for validAnagram check via sort + check (brute force), receiving two strings and returning a boolean
- visited bool vector (n, false)
- i loop runs over entire strings vector, check if visited, continue
- Treat each unvisited string as the start of a new group and compare it with every remaining unvisited string in j loop, j= i+1 starts.
- If new string (visited[j]) is unvisited && two strings (i and j) are anagrams, place them in the same group and mark the matching string(j) as visited.
- Push group in result vector
- Repeat this process until all strings are grouped.
- TC: O(n^2 * klogk), Sorting each comparison: O(klogk) in helper fn and Comparing all pairs: O(n^2)
- SC: O(n.k), Sorting O(1) or O(k) depending on sorting algo, here assumed O(1), Group stored O(n.k)

2. BS:
- The idea is that if we sort two strings which are anagrams of each other, then the sorted strings will always be the same.
- So, we can maintain a hash map with the sorted strings as keys and the index of the anagram group in the result array as the value.
- 
