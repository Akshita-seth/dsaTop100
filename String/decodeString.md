Optimized Solution:
- Direction summary: Use a stack (or recursion) to manage nested brackets, build numbers for repeat counts, and expand strings when you hit ]
- The stack keeps track of nested contexts.
- Each [ starts a new context, each ] closes it.
- Digits tell you how many times to repeat.
- 
- Identify the pattern: The string has nested encodings like "3[a2[c]]". This screams stack-based parsing (or recursion).
- Traverse the string
- Go character by character.
- You’ll encounter digits, [, ], and letters.
- Maintain a stack of (previousString, repeatCount).
- initialise currString = "" and int num = 0
- Traverse the input string:
   - If digit → build the number.
   - If [ → push (currentString, repeatCount) and reset for new context i.e. currString="" and num=0.
   - If letter → append to currentString, use push_back since one char added only or use currString.appedn(1,ch)
   - If ] → pop, expand, and merge. currString = prevString (from st.top.first) + expanded(from looping st.top.second times of currString added in expanded)
- Return currentString at the end.

- SC: O(1)
- TC: O(n.k) where n is length of string, k is max repeat count in string.
- But when you expand, you may repeat substrings up to k times. If k is large, expansion dominates.
  Example: "100[a]" → output length = 100, so expansion cost is proportional to k.

In an interview, you can say:
“I’ll solve this using a stack of (string, repeatCount) pairs. Each [ pushes the current context, each ] pops and expands. 
- This runs in O(n) time and O(1) extra space. It’s the optimized solution for this problem.”
- That’s crisp, correct, and sufficient. If they probe further, you can add:
- “There’s also a recursive way to parse, but the stack solution is clearer and easier to implement.”
