1. BFS:
- Using map for visited
- Whenever the first already visited node is encountered
- Return that node then and there
- TC: O(n), SC: O(n)

2. OS:
- Using fast and slow pointers
- Distance theory using fast and slow pointers: The first node where fast and slow pointers meet;
- From there the distance to the starting node of the loop and the distance from the head to the starting of the loop is same.
- while(fast && fast->next) -> just move fast twice and slow once -> if they meet, assign slow = head -> again loop while(fast != slow)
- then, just return slow outside the just before while, within the if(fast == slow)
- Outside return NULL
- TC: O(N) N = number of nodes in the linked list. In the worst case, we traverse the entire list once with the slow and fast pointers, and then again to find the entry point of the loop.
