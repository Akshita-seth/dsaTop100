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
- The idea is that if we sort two strings that are anagrams of each other, then the sorted strings will always be the same.
- So, we can maintain a hash map with the sorted strings as keys and the index of the anagram group in the result array as the value.
- Create a map {string -> index} this index will be anagrams i.e. ans vector size everytime
- Start i loop, sort the string at i, if not present in map => mpp[str] = anagram.size() and push an empty vector in ans vector anagram as reserving a space for group if added in future
- No push original string at i into anagram[mpp[str]] i.e. the index of the sorted string
- TC: O(n. klogk) Sorting each word: O(klogk), For n words: O(n. klogk), Hash insertions: O(n)
- SC: O(n.k) Hash map storing groups

3. OS:
- Anagrams have the same frequency of every character. Use the character frequency of each string as a unique key to group all its anagrams together.
- 

