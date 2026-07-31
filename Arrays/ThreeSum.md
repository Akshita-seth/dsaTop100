1. BFS:
- Nested Loop i,j,k => generate all triplets
- Use a set to store vector of triplets initially; At last, before return, convert to vector of vectors by vector<vector<int>> ans(st.begin(), st.end())
- Start i with 0, j with i+1, k with j+1 since no value used twice
- If sum matches, create temp vector -> sort it -> insert in set => All these done in k loop
- TC: O(n^3) * O(log(no. of triplets)) since insertion in set is logN as it is unique   
- SC: O(2*(no. of triplets)) for set and result

2. BS:
- Use HashSet to find the third element.
- Use a set to store vector of triplets initially; At last, before return, convert to vector of vectors by vector<vector<int>> ans(st.begin(), st.end())
- Start i loop, then initialise a hashSet, Set to store elements seen in this iteration: set <int> hashset;
- Start j loop with i+1 since not using same val twice
- Calc third as complement and check in hashSet
- If yes, create temp vector -> sort it -> insert in set ans , also insert nums[j] in hashSet => All these done in j loop
- DND: Do not insert the complement in hashSet (third). Otherwise, you’re storing the complement instead of the actual number you’ve seen, which breaks the logic.
- TC: O(n^3) * O(log(no. of triplets)) sice insertion in set is logN as it is unique   
- SC: O(2*(no. of triplets)) for set and result

3. OS:
- Two pointer approach
- Duplicates check is done for each i, j, k as a substitute set data structure 
- Keep in mind for i duplicates check, check i AFTER incrementing i hence => if(i>0 && nums[i] == nums[i-1]) continue;
- Initialise j and k, loop while(j<k)
- Check for target sum greedily
- If found, push triplet into ans, update j&k and check duplicates for j and k similarly, these checks are also AFTER incrementing {Keep in mind}
- TC: O(NlogN)+O(N^2) sorting + TwoPointer * i loop, SC: O(1)
