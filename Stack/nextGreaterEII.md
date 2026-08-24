1. BFS:
- Nested Loop: TC: O(N^2) SC: O(N) just for ans
- 1st Version : Hypothetically double the array:
               for(int i=0; i<n; i++)
        {
            // Double the array hypothetically
            for(int j=i+1; j< i+n; j++)
            {
                int idx = j%n;
                if(nums[idx] > nums[i])
                {
                    nge[i] = nums[idx];
                    break;
                }
            }
        }
- 2nd Version : Get the hypothetical double index
               for(int i=0; i<n; i++)
        {
            
            for(int j=1; j< n; j++)
            {
                // Getting the hypothetical index
                int idx = (i+j)%n;
                if(nums[idx] > nums[i])
                {
                    nge[i] = nums[idx];
                    break;
                }
            }
        }

2. OS:
- Monotonic Stack, doubled the array hypothetically
- Initialize an answer array with default values of -1
- Initialize an empty stack to keep track of elements
- Traverse from 2n - 1 down to 0 using modulus to simulate circular indexing
- While stack is not empty and top of stack is less than or equal to current element, pop from stack
- If index is in the original array range, assign top of stack to answer if stack is not empty, else keep -1
- Push the current element onto the stack
- After traversal ends, return the answer array
- TC: O(N^2) SC: O(1) just O(N) for ans vector

2. OS:
- 
