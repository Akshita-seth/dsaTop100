1. BFS
- Generate all possible substrings of the given string. For each substring, check if it is a palindrome.
- If it is, update the result if its length is greater than the longest palindrome found so far.
- Helper fn checkPal accepting the original string and two indices start and end
- Nested i and j loop: i = 0, j = i
- Inside the j loop:
  int len = checkPal(i,j,s) ? j-i+1 : 0;
  if(len > palin.size())
     palin = s.substr(i,len);
- Just return palin
- TC: O(n^3), SC: O(1)

https://www.geeksforgeeks.org/dsa/longest-palindromic-substring/
Expand Around Center is the expected optimized solution.
You can mention DP as an alternative, and Manacher’s as the theoretical optimal [TC: O(n) SC: O(n)], but code the center‑expansion method.
Complexity: O(n^2 and O(1) — good balance of clarity and efficiency.

2. BS
- Using Expansion around center
- Iterate through each character in the string, treating it as the center of a potential palindrome.
- For each center, expand in two ways: one for odd-length palindromes (center at index i) and one for even-length palindromes (center between indices i and i+1)
- Use two pointers low and high to track the left and right boundaries of the current palindrome.
- While low and high are in bounds and s[low] == s[high], expand outward.
- If the current palindrome length (high - low + 1) is greater than the previous maximum, update the starting index and max length.
- After checking all centers, return the substring starting at start with length maxLen.
- TC: O(n^2) SC: O(1)




