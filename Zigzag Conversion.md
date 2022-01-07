vector
===
1.init

vector<> vec(number, init value);

2. insert


first coming in mind:
```cpp
string convert(string s, int numRows) {
        if(numRows < 2 || s.size() < numRows)
        {
            return s;
        }
        int circle = numRows + numRows - 2;
        string ans = "";
        vector<string> preans(numRows, "");
        for(int i = 0; i < s.size(); i++)
        {
            int num = i%circle;
            if(num < numRows)
            {
                preans[num] = preans[num] + s[i];
            } else {
                preans[circle - num] = preans[circle - num] + s[i];
            }
        }
        for(int i = 0; i < numRows; i++)
        {
            ans = ans + preans[i];
        }
        return ans;
    }
```

pretty slow method: Runtime: 93 ms, faster than 6.72% of C++ online submissions for Zigzag Conversion.Memory Usage: 51 MB, less than 6.23% of C++ online submissions for Zigzag Conversion.

Awful one.

Try to find another O(n) method.
