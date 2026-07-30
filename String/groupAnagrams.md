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
- Frequency arrays are faster when word length is large.
- The delimiter ('#','$',',') is purely to avoid collisions when serializing the frequency array into a string key for the hash map:
Word = "abb", Frequency: a=1, b=2, Key (no separator): "12"
Now imagine a slightly different case:
Word = "aaaaaaaaaaa b" (11 a’s, 1 b), Frequency: a=11, b=1, Key (no separator): "111"
"111" could also mean "a=1, b=11" if you just read digits in sequence.
So "a=11, b=1" and "a=1, b=11" both collapse into "111" — collision.
- So use helper fn to create the hash of every string, then in groupAnagram fn similar to BS:
- Use map {string -> index}, check if not present in map, add in map with index as result.size() and pushing empty vector in res so as to reserve place for string.
- Outside, add result[mpp[key]].push_back(arr[i])
- TC: O(n*k), where n is the number of words and k is the maximum length of a word. SC: O(n*k).

