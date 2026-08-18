1. Preorder Traversal
   i. Using recursion:
    - Helper fn + recursion + ans vector in parater
    - Process (push in ans) -> traverse left -> Traverse right
    - TC: O(N) SC: O(H)
  ii. Using Stack:  process the root immediately when you see it ->Then explore left, then right.
    - A stack helps you remember which nodes to return to.
    - Push root
    - loop till stack not empty
    - Pop, process it
    - Push right child first, then left child (so left is processed before right).
    - TC: O(N) SC: O(N)

2. Inorder Traversal
   i. Using recursion:
    - Helper fn + recursion + ans vector in parater
    - Traverse left -> Process (push in ans) -> Traverse right
    - TC: O(N) SC: O(H)
  ii. Using Stack: go all the way left before processing root.
    - Stack helps you remember the path back up
    - Don't push root in stack, just initialise node = root then while(true)
    - Start at root, keep pushing left children until null.
    - If null, check is stack empty and brrak, otehrwise
    - Pop → process node.
    - Then move to right child.
    - TC: O(N) SC: O(N)
3. Postorder Traversal
   i. Using recursion:
    - Helper fn + recursion + ans vector in parater
    - Process (push in ans) -> traverse left -> Traverse right
    - TC: O(N) SC: O(H)
  ii. Using 2 Stacks: must process children before root.
    - Push root into stack1.
    - Pop from stack1 → push into stack2.
    - Push its children into stack1.
    - At the end, stack2 has nodes in reverse postorder → pop them out.
    - TC: O(N) SC: O(2N)
 iii. Using 1 Stack: must process children before root.
    - Push left path → simulate recursion.
    - Check right child → decide whether to descend or process.
    - Process when no right → children done, now root.
    - Backtrack → climb up and finish ancestors.
    - TC: O(2N) SC: O(N)


### Big Picture Intuition
- Preorder (Root first): Push root, process immediately, then children.

- Inorder (Root middle): Keep going left, stack remembers path back, process root only after left done.

- Postorder (Root last): Delay root until children are processed — either by using a second stack (easy) or by tracking visited children with one stack (tricky).
