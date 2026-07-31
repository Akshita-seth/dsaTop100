## Max Consecutive Ones I
1. BFS [No need to say in interview waste soln]
- Nested Loop, i = 0, j = i
- If nums[j] = 1 then increment count nad update max1
- else break
- TC: O(n^2) SC: O(1)

2. OS:
- Just i loop
- Check if 1 increment count and update max1
- Else just make count 0
- TC: O(n), SC: O(1)

## Max Consecutive bits 1 or 0
- Take 0s and 1s counter, initially 0 and a max bit counter
- Traverse with i loop
- If 1 is encountered, increment 1s counter and make 0s counter zero
- Vice Versa if 0 is encountered
- Just take max of both counters every time at end of loop
- TC: O(n), SC: O(1)

## Max Consecutive Ones II
1. BFS [Just mention this in interview, no need to code]
- Checking all subarrays
- Naively, I brute force by flipping each zero and checking the streak
- Initialise maxi with 0
- In the i loop, initialise flip and len as 0
- Then in j loop, j starts from i, if 0 is encountered flip++; if flips becomes > 1, break the j loop
- In outer loop update maxi with max of maxi and len
- TC: O(n^2), SC: O(1)

2. OS: GREEDY approach
- The key observation is that we are allowed to flip at most one 0, which means every valid segment of consecutive 1’s can include at most one zero inside it.
- To track this efficiently, we move through the array while maintaining two counts:
- ones: the length of the current stretch of consecutive 1’s without any zero flipped.
- ones_with_flip: the length of the current stretch if we allow ourselves to flip one 0.
- When we see a 1, both counts extend normally.
- When we see a 0, the stretch without flipping resets, but the stretch with one flip becomes the number of previous consecutive 1’s plus 1 (because we can flip this zero).
- At every step, the maximum of ones_with_flip represents the best possible streak ending at that position
- TC: O(n), SC: O(1)

3. OS: Sliding Window [Expected in Interviewa]
- Maintain a window [left, right] that contains at most one zero.
- Expand right as you traverse. using for loop
- If the window has more than one zero, shrink left until only one zero remains. using while loop
- Track the maximum window length
- TC: O(n), SC: O(1)

## Max Consecutive Ones III
1. BFS [Just mention this in interview, no need to code]
- Checking all subarrays
- Naively, I brute force by flipping each zero and checking the streak
- Initialise maxi with 0
- In the i loop, initialise flip and len as 0
- Then in j loop, j starts from i, if 0 is encountered flip++; if flips becomes > 1, break the j loop
- In outer loop update maxi with max of maxi and len
- TC: O(n^2), SC: O(1)

2. BS: Sliding Window [Expected in Interviewa]
- Maintain a window [left, right] that contains at most one zero.
- Expand right as you traverse. using for loop
- If the window has more than k zeros, shrink left until only one zero remains. using while loop
- Track the maximum window length
- O(N^2)>TC>O(N) bcz  0<k<n, CS: O(1)

3. OS: Two pointer Approach
- In prev, SW approach -> right pointer waits until left shrinks, here right won't wait
- Just change the "while" in shrinking part to "if"
- One more thing, with or without maxi both are correct.
- If updating maxi is not done at every step at the end of loop, we can simply return n-left;


