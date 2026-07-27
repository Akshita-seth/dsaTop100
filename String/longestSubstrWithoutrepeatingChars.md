1. BFS:
- Generate all substring by nested loop
- Check for uniqueness by initialising a visited array for every new i
- If constraint mentions: s consists of English letters, digits, symbols and spaces.
- Take freq array of size 256
- If only English lowercase alphabets then a 26-size array and use visited[s[j]-'a']
- j loop starts from i
- If an already visited char is encountered in the j loop, break
- else update the length of substr by ans=max(ans, j-i+1) and marking that char as visited
- TC: O(n^2) SC: O(1)
- If Asked for the Substring Itself:
- ans = max(ans, j - i + 1);
if(ans == j - i + 1) longest = s.substr(i, ans);

2. BS:
- 
