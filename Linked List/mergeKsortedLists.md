1. BFS
- Sequential merge
- Use helper fn merge2Lists()
- Edge case: if lists.empty() true, return NULL
- Create newhead node, initialise with lists[0]
- Loop from i = 1 till lisis.size()
- For every i get newhead = merge2lists(newHead, lists[i])
- TC: O(N.K) => N is total number of nodes acrosss all lists, K is number of lists, SC: O(1)
- The problem: each time, the merged list grows larger, so later merges are more expensive.
- Worst case (all lists of equal size, about N/k nodes each):
- Merge 1: O(2N/k)
- Merge 2: O(3N/k)
- Merge 3: O(4N/k)
- …
- Merge (k-1): O(N)

Total cost ≈

(N/k) * (2 + 3 + 4 + … + k)  
= (N/k) * (k(k+1)/2)  
≈ O(Nk)

  2. OS 1:
  - Pairwise Merge => Divide & Conquer: Merge lists in pairs recursively (like merge sort)
  - Use helper fn merge2lists in the same way
  - Just recursion in mergeKLists()
  - 2 edge cases => lists.empty -> return null, and lists.size = 1 return list[0]
  - calc mid = lists.size / 2
  - Create two vectors of lists -> left and right using begin, begin + mid, and end
  - Remember the First iterator is INCLUSIVE and second is EXCLUSIVE
  - Then create two new Nodes right and left by recursive fn [ListNode* right = mergeKLists(rightList);]
  - Atlast return merge2lists(left, right)
  ### Complexity of Pairwise Merge (Divide & Conquer)

- **Time Complexity:** O(N log k)  
  - Each merge operation (`merge2Lists`) costs O(n), where n is the total number of nodes across the lists being merged.  
  - The recursion splits the vector of lists in half each time → recursion depth is O(log k).  
  - At each level of recursion, all nodes are merged once.  
  - Therefore, total time = O(N log k).

- **Space Complexity:**  
  - Recursion stack depth = O(log k).  
  - Temporary vectors when splitting (`leftList`, `rightList`) → each copy costs O(k), but overall bounded by O(k) at each level.  
  - So space = O(k) with vector slicing, or O(log k) if you avoid slicing and recurse with indices.

### Layman’s Explanation
Think of it like a **tournament bracket**:
- You start with k players (lists).
- In round 1, they play matches in pairs → k/2 winners.
- In round 2, those winners play again → k/4 winners.
- This continues until one champion (the final merged list) remains.

At each round, **every player participates once**, so all N nodes are touched.  
The number of rounds is about **log₂(k)** (because the group halves each time).  
So each node gets processed log k times → total work = N × log k.

### Summary
- **TC:** O(N log k)  
- **SC:** O(k) with slicing, optimized to O(log k) if using indices.

3. OS 2:
- Using heaps
- Do whiledoing heaps
