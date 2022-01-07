Longest Substring Without Repeating Characters
====
map operations
--
1. init: map<type1, type2>

2. map.find(), if exist, return loc, if not return map.end().  Usually using map.find(x) == map.end() express map does not have certain key.

3. map.insert(pair<type1, type2> (key, value))  

4. find key's value: map[key] * not map(key) *

5. iteration: 

for (auto j = map.begin(); j != map.end(); j++)  // remember not using j < map.end()

Ascii
---
  0 ~ 9 -> 48 ~ 57

  A ~ Z ->   65 ~ 90

  a ~ z ->   97 ~ 122

  ' '  ->  32

slide window
---
![image](https://user-images.githubusercontent.com/57583420/148501579-ebbe2096-04d6-4df1-9638-b12dc7bfb25d.png)
fix end, find begining.
```cpp
int lengthOfLongestSubstring(string s) {
        int ans = 0;
        int curr = 0;
        map<char, int> location;
        map<char, int> location2;
        for(int i = 0; i < s.size(); i++)
        {
            
            if(location.find(s[i]) == location.end())   // not exist before
            {
                location.insert(pair<char, int>(s[i], i));
                curr ++;
            } else {
                int start1 = location2.find(s[i]) == location2.end()? location[s[i]] : location2[s[i]];
                int start2 = 0;
                for(auto j = location2.begin(); j != location2.end(); j++)
                {
                    int num = location[j->first];
                    start2 = start2 > num? start2:num;
                }
                int loc = start1>start2? start1:start2;
                curr = i - loc;
                ans = ans > (i - loc)? ans:(i - loc);
                if(location2.find(s[i]) == location2.end()) // never repeat
                {
                    location2.insert(pair<char, int>(s[i], i));
                } else {
                    location[s[i]] = location2[s[i]];
                    location2[s[i]] = i;
                }
            }
            ans = ans > curr ? ans : curr;
        }
        return ans;
    }
```
