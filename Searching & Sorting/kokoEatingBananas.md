1. BFS:
- Linear scan on all speeds(k) possible 1 to max(piles[])
- Find maxi in the array
- Loop i from 1 to maxi
- Calc req time using helper fn by sending piles and i (as k)
- In helper fn time += (piles[i] - k - 1) / k;
- If calc reqTime <= h, return i
- Outside, return maxi
- TC: O(maxi * n) n = number of piles, O(maxi) is taken by linear search and o(n) isntaken by helper fn; SC: O(1)

2. OS: Binary Search on Answers
- https://www.youtube.com/watch?v=qyfekrNni90
- Same helper fn used
- Binary search on the possibilities of k is done: low = 1 and high = maxi
- Calc mid and send to helper fn along with array
-  if reqTime <= h search the left half => high = mid-1
-  else search the right half => low = mid + 1
-  TC: O(N logN) => O(N) Helper fn, O(logN) binary search; SC: O(1)
