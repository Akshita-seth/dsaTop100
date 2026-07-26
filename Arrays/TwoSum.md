1. BFS:
- Nested Loop
- Do not use the same element twice; hence, j starts from i+1
- TC: O(n^2) SC: O(1)

2. BS for Sorted and OS for Unsorted Arrays:
- HashMap technique, store {value -> index}
- Do not build the HashMap separately in another loop
- Build along with complement calculation bcz, if {3,4,2} and target 6 then returns {0,0}
- TC: O(n) SC: O(n)
- TC Paradox: if ordered map: O(N*logN) [no collision], if unordered map: O(N*1) [mostly i.e. best and avg TC] but if collision happens [happens once in a blue moon] then O(N*N)

3. OS for Sorted:
- Two Pointer Greedily
- But if indices asked in unsorted then don't sort bcz sorting changes the original index
- TC: O(n) & O(nlogn) [if sorting also done], SC: O(1)

4. If Count the number of pairs asked in Unsorted:
- Build hashmap separately, {val -> freq}
- Then traverse the hashmap x as curr val and y as complement
- if complement exists in map then 2 cases for counting:
- Case 1: if x=y => Choose 2 out of freq[x] nC2 formula c += freq[x] * freq[x]-1 / 2
- Cade 2: else if(x<y) =? c+= freq[x]*freq[y], else if(x<y) is done for skiping to count same pair (x,y) as (y,x) in future iterations
- TC: O(2n) building map, iterating map. Hashmap operations are O(1), SC: O(n)
  
5. If Count the number of pairs asked in Sorted:
- Two pointer greedily
- if sum found then for counting 2 cases:
- Case 1: if nums[i]=nums[j] => cnt = j-i+1 and c+= cnt*(cnt-1)/2 and break (IMP) since for case 2 calc has no condition, thus break is imp here if this condition works
- Case 2: lC = rC = 1, calc duplicates on left and on right, then multiply along with i++ and j-- again. 
- TC: 𝑂(nlogn) if sorting is needed, otherwise O(n), SC: O(1)
