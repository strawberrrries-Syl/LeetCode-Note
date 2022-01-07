167 Two Sum II - Input Array Is Sorted
===
premise:
---
sequence are sorted.

*inmportant:*
two pointer, one for small number, one for big number. added up.
```cpp
vector<int> twoSum(vector<int>& numbers, int target) {
        int small = 0; int big = numbers.size() - 1;
        vector<int> ans(2,0);
        while(small <= big)
        {
            int sum = numbers[small] + numbers[big];
            if(sum == target)
            {
                ans[0] = small + 1;
                ans[1] = big + 1;
                return ans;
            }
            else if(sum > target){
                big--;
            } else if(sum < target){
                small ++;
            }
        }
        return ans;
    }
```


633 Sum of Square Numbers
===
*important*
Big pointer set as sqrt(c) instead of c to minus runing time.
Other are same as above.
