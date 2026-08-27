1. BFS:
- Last element after sorting the array
- But since origial modified hence not good
- TC: O(logN) SC: O(1)

2. BS:
- Using Min-Heap
- Create a min Heap with the first K elements
- For the rest of the elements check => if element > heap.top() => heap.pop() => heap.push(element)
- This will result in the heap containing the first K largest elements, and the root of this heap will be the Kth largest element (this is why we took min-heap).
- TC: O(nlogk) => building a heap O(k), Processing the remaining (n-k) elements each push/pop is O(logk)
- SC: O(k)

3. OS:
- Quick Sort derived Quick Select ALgo
- First helepr fn -> randomIdx() so that TC can be avg
- Second
