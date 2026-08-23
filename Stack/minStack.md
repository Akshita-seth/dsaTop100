1. BFS:
- A stack of pairs is used, where each pair contains the element itself and the minimum element at the time the element was pushed onto the stack.
- The MinStack class is initialized with an empty stack.
- Push Operation:
  When a new element is pushed, it is compared with the current minimum.
  The new element and the updated minimum are stored as a pair and pushed onto the stack.
- Pop Operation:
  The top element (which is a pair) is removed from the stack.
- Top Operation:
  The top element of the stack is accessed to get the actual value (first component) stored in the pair.
- GetMin Operation:
  The second value of the pair at the top of the stack, which represents the minimum element at that point, is accessed.
- TC: O(1) SC: O(2N)

2. OS:
- Use a stack to store elements and maintain a variable to keep track of the current minimum value.
- Push Operation:
  If the stack is empty, push the value and set it as the current minimum.
  If the value is greater than or equal to the current minimum, simply push the value onto the stack.
  If the value is less than the current minimum, push a modified value calculated using the new value and update the current minimum.
- Pop Operation:
  If the stack is empty, do nothing.
  Otherwise, retrieve and pop the top value from the stack.
  If the popped value indicates it was used to store a new minimum, update the current minimum using the retrieved value.
- Top Operation:
  If the stack is empty, return -1 indicating the stack is empty.
  Retrieve the top value. If it is greater than or equal to the current minimum, return it.
 If the top value indicates it was used to store a new minimum, return the current minimum.
- GetMin Operation:
  Simply return the current minimum.
- TC: O(1) SC: O(N) onluy basic already used stack, no extra
  
