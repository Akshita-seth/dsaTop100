1. BFS:
- Sort and Check
- First basic size check
- Sort both strings
- return (s1 == s2)
- TC: O(nlogn) SC: O(1) even if space taken then depends on sorting algorithm
- O(1) for in‑place sort (like heapsort), O(n) for mergesort.

2. BS:
- HashMap approach
- Basic check: if size not same, then false
- First, count the occurrences of each character in the first string using a HashMap.
- Then, iterate through the second string and decrement the corresponding count for each character in the same HashMap.
- After processing both strings, check the HashMap: if all character counts are zero, the strings are anagrams
- Any non-zero count indicates a mismatch in character frequency, meaning the strings are not anagrams.
- TC: O(n) or O(n+m) SC: O(n) or O(m) if size not same for both i.e. not anagrams

3. OS:
- Using a Fixed Frequency Array of size 26
- Two ways: Plain C-style int freq[26] = {0}; static behaviour
- st::vector style: vector<int> freq(26,0);  dynamic behaviour
- Same approach of counting for one string, then decrementing for other, then checking if all 0
- Use freq[ch-'a'] here since not a map; a's freq stored at index 0, b's at 1 etc
- TC: O(n) or O(n+m) SC: O(1) since fixed array of 26 size declared
