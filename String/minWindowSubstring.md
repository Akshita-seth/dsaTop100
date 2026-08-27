1. BFS:
-  TC: O(M^3 + M*N) SC: O(256) contant space
- Generate all substrings and compare if substring hasAllChars by comparing the frequency using fixed arrayof 256 size
- helper fn hasAllChars(): Build frequency counts of t once/first.
                           Compare counts of substr against counts of t +> if count[ch] > 0 +> count[ch]--

2. BS:
- Binary search on answers but not expected
- TC: O(N*logN) SC: O(1)

3. OS: SLiding Window
- Build frequency array for all chars in t.
- Initialize pointers l = 0, r = 0, count = 0, stratIdx = -1, minLen = INT_MAX.
- Expand right pointer till s.size
- Decrement freq[s[r]] alwsys (since will increment when l traverses it, now decrement, update count if neede i.e. preinserted i.e. freq[s[r]] > 0)
- Check validity: [use while istead of if nbcz shjrinking doen inside] count == n (t.size), window has all chars hence net point 
- Update answer: record minLen= r-l+1, and startIdx = left.
- Shrink left pointer: increment freq[s[l]] (since decreased when r traversed it, now increment), increment count if needed i.e. freq[s[l]] > 0, then at end left++
- Repeat expansion: move r++ until end of string.
-  return startIdx == -1 ? "" : s.substr(startIdx, minLen);
-  TC: O(2M + N) -> N storing freq of T, M while loop r<m, M while checking valididty and shrinking(worst case can be M i.e. traversing entire string with l)
-  SC: O(256) const space
