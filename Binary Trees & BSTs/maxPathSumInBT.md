Soln:
- The idea is to use postorder traversal. At each node, calculate left and right path sums, and update a global maximum with (left + node + right).
- Return the node’s value plus the larger side upward. The global maximum at the end gives the answer.
- Helper fn for finidnga nd updating global maxi: [Remember to take maxi as refrence parameter or global]
- explore int left as max(0, recrusive_fn) similar right
- Update maxi as max(maxi, l + r + root->val)
- Returns root->val + max(l,r);
- TC: O(N) SC: O(H) recursion depth
