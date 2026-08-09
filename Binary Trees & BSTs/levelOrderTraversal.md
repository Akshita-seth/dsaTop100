Soln:
- Edge case of root == NULL
- Use a queue
- Push the root before the loop
- Loop till q not empty
- Calc size beforehand
- i loop for size
- Store front, add in temp vector and pop q
- If left and right exist, push temp in result vector 
- TC: O(N) SC:(N)
