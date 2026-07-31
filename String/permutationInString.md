#### Remember to understand both solutions:
A permutation means the arrangement can change, but the multiset of characters must be identical. So if two strings have the same length and the same frequency of each character, they are permutations

1. BFS:
- Sort every substring of s2 of length s1.size() and compare with sorted s1.
- Sort s1 initially
- Loop for i starting as 0
-  DND: limit for i is <= len1-len2 otherwise problem: 
   1st: if not len2 not subtracted then i goes out of bounds
   2nd: if just < then i misses last pssbl substring hence <=
- sot substrings for evry new i, compare with s1, if matched return true
- TC: O(n. mlogm) where Sorting each substring costs O(len1.loglen1),i.e. m=len1 and
- Doing this for all windows i.e. multiply (len2-len1) i.e. n [heavier than necessary], SC: O(1)

2. OS:
- Use character frequency arrays + sliding window:
- Build s1 freq array
- initialise a len1 size window on s2 and build freq array
- Initial window comparison: freq1 == freq2
- Slide window across s2: loop from i=len1 to i<len2 
  adding new char: freq2[s2[i]-'a']++;  and removing leftmost char: freq2[s2[i - len1] - 'a']--;
- again compare at end of loop 
- TC: O(len2), each slide is constant work + 26‑char comparison, SC: O(1) since we use two arrays of length 26.
- 1. build freq -> O(len1), 2. Initialize first window of len1 in s2 -> O(len1), Slide the window across s2for len2-len1 windows -> len2-len1
  Hence overall: len1 + len1 + len2-len1 => len2 
