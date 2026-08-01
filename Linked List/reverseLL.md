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
- The idea is to reverse the linked list by changing the direction of links using three pointers: prev, curr, and front.
- At each step, point the current node to its previous node and then move all three pointers forward until the list is fully reversed.
- Initially: prev null, curr head
- while(curr != NULL) {
            front=curr->next;
            curr->next=prev;
            prev=curr;
            curr=front;}
- return prev;
- TC: O(n), SC:O(1)
  
2. OS Recursive:
- edge case resolve/ here basr case for ending recursion
- The idea is to use recursion to reach the last node of the list, which becomes the new head after reversal.
- As the recursion starts returning, each node makes its next node point back to itself, effectively reversing the links one by one until the entire list is reversed.
- newHead takes the return of recusrive fn, and t last it is returned
- Use front = head->next -> front->next = head -> head->next = NULL
- TC: O(N)Each node is visited exactly once during the recursive call, and we do constant-time work for each node (like flipping pointers).
- SC:  O(n),The recursion stack goes up to n levels deep (one for each node), which uses extra space on the call stack.
