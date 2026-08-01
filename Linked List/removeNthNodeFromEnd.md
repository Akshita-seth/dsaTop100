1. BFS:
- To remove the Nth node from the end, first determine the length of the linked list.
- Then, delete the (length - N + 1)th node from the front.
- Traverse the linked list to calculate its length.
- Compute the position to delete from the front : nodeToDelete = (length - n + 1).
- If nodeToDelete is 1 i.e. length == c => return head->next simply
- Use prev to keep track of previous node while changing links, use temp too
- Traverse to the node by keeping a tracker which when reaches length - n + 1, update its next pointer to skip the target node.
- TC: O(2n) SC: O(1)

2. OS:
- The idea is to first move the fast pointer N steps ahead, then move both fast and slow pointers together until fast reaches the end.
- The slow pointer will then be just before the node to be removed, allowing to update the next pointer to skip the target node.
- Initialize three pointers, dummy and slow & fast, both will be equal to dummy. dummy will be new Node(0, head) since dummy->next = head
- fast moves ahead by n (i=0 -> i<=n  => fast = fast->next)
- Then both pointers will move simultaneously until (fast != NULL).
- Finally, free up the space occupied by this to delete it.
- dummy->next initially equals the original head.  IMPORTANCE of dummy:
    - If you remove a node in the middle or end, the head doesn’t change. Returning dummy->next just gives back the original head.
    - If you remove the first node (head itself), then slow->next gets updated to skip that node
- TC: O(N), SC: O(1)
