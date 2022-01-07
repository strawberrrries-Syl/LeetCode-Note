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

345 Reverse Vowels of a String
===

low, high pointers.
---

when two pointer both point to vowels, change values.

```cpp
string reverseVowels(string s) {
        // my thought
        // 1. get location of vowels
        // 2. reverse them by location (odd / even) 
        string vowels = "aeiouAEIOU";
        string ans = s;
        int low = 0;
        int high = s.size() - 1;
        while(low<= high)
        {
            int num1 = vowels.find(s[low]);
            int num2 = vowels.find(s[high]);
            if(num1 >=0 && num1 < vowels.size() && num2 < vowels.size() && num1 >= 0)
            {
                ans[low] = s[high];
                ans[high] = s[low];
                low++;
                high--;
            } else {
                if(num1 < 0){
                    low++;
                }
                if(num2 < 0) {
                    high --;
                }
            }
        }
        return ans;
    }
```

680 Valid Palindrome II
===

*important*

have a one time chance to delete a character.
recursion
try both left and right then decide.


524 Longest Word in Dictionary through Deleting
===
Substrings
---
problem can be thought as finding whether verbe in dictionary is a substring of s.
``` cpp
public:
    bool isSubstr (string s1, string s2) {
    
        int low = s1.find(s2[0]);
        int high = 0;
        
        if(low >= 0 && low < s1.size())
        {
            while(low < s1.size())
            {
                if(s1[low] == s2[high])
                {
                    high++;
                }
                low ++;
            }
            if(high == s2.size())
            {
                return true;
            }
            else {
                return false;
            }
        }else {
            return false;
        }
        
    }
public:
    string findLongestWord(string s, vector<string>& dictionary) {
        string ans;
        for(int i = 0; i < dictionary.size(); i++)
        {
            if(isSubstr(s, dictionary[i])){
                if(dictionary[i].size() > ans.size())
                {
                    ans = dictionary[i];
                } else if(dictionary[i].size() == ans.size())
                {
                    ans = dictionary[i] < ans? dictionary[i]: ans;
                }
            }
        }
        return ans;
    }
                                              ```
                                        
