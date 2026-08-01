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
- 
2. OS Recursive:
