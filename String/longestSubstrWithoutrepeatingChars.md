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

2. OS 1:
- Initialize two pointers left and right with 0, which define the current window being considered.
- The right pointer moves from left to right, extending the current window.
- If the character at right pointer is not visited, it's marked as visited.
- If the character at right pointer is visited, it means there is a repeating character. The left pointer moves to the right while marking visited characters as false until the repeating character is no longer part of the current window.
- The length of the current window (right - left + 1) is calculated and answer is updated accordingly
- TC: O(n) SC: O(1)

3. OS 2:
- The approach stores the last indexes of already visited characters.
- The idea is to maintain a window of distinct characters. Start from the first character, and keep extending the window on the right side till we see distinct characters.
- When we see a repeating character, we check for the last index of the repeated character:
- If last index of repeated character >= starting index of the current window, then we update the starting index of the current window to last index of repeated character + 1 to remove the repeated character.
- If last index of repeated character < starting index of the current window, then it means that the repeated character is already outside the current window so the window size remains unchanged.
- - TC: O(n) SC: O(1)
