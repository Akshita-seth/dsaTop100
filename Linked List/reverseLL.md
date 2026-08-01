1. BFS
- Use Stack
- Edge case:
  if(head == NULL || head->next == NULL)
        return head;
- Two pass solution, just values reversed, links stay the same
- We traverse the linked list twice once to push all node values into the stack, and once to reassign values. Each traversal takes O(N) time, where N is the number of nodes.
- TC: O(2N), SC: O(N)

2. OS Iterative:
- Links are also reversed.
- Edge case resolve
- The idea is to reverse the linked list by changing the direction of links using three pointers: prev, curr, and next. At each step, point the current node to its previous node and then      move all three pointers forward until the list is fully reversed.
- Initially: prev null, curr head
- while(curr != NULL) {}
- return prev;
- TC: O(n), SC:O(1)
  
2. OS Recursive:
