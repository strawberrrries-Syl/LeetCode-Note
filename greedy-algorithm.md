455 Assign Cookies
===

Sorting child and cookie. Giving minimum value.

*Remember:

  Any value not smaller than aim is useful.
  Do not need another vector to store whether each value was used.
  If some kid (in the sorted sequence) can not be satisfied, which means others after him are not able to be satisfied either. ==> This makes the program much more easier.
  ```cpp
  int findContentChildren(vector<int>& g, vector<int>& s) {
        sort(g.begin(), g.end());
        sort(s.begin(), s.end());
        int i = 0, j = 0;
        while(j < s.size() && i < g.size())
        {
            if(g[i] <= s[j])
            {
                i++;
            } j++;
            
        }
        return i;
    }
  ```
  
  
  435 Non-overlapping Intervals
  ===
  
  *First thought:
  
  Since we are doing the greeding algorithm problem. My thought is like this:
  
  * First dealing with short one then bigger one, see overlaping area.

  *Method:
  
  find number of intervals which do not overlaping with each others. Subtracted from sum interval size.
  
  How to sort ``` vector<vector<int>> ```
  ---
  
  rewrite a compare function of sort third parameter. As code below:
  ```cpp
  int eraseOverlapIntervals(vector<vector<int>>& intervals) {
        
        auto compare = [](vector<int> &intervalA, vector<int> &intervalB){
            return intervalA.at(1) < intervalB.at(1);
        };
        
        sort(intervals.begin(), intervals.end(),compare);
        
        int num = 0, end = intervals[0][0];;
        for(int i = 0; i < intervals.size(); i++)
        {
            if(intervals[i][0] >= end)
            {
                end = intervals[i][1];
                num++;
            }
        }
        return intervals.size() - num;
    }
  ```


452 Minimum Number of Arrows to Burst Balloons
===

Same as above. Small changes.

406 Queue Reconstruction by Height   -- rewrite the cmp rule
===

The trick is descending ordered by height and ascending ordered by people before.

If some person are not at their aim position, just insert him.

```cpp
public:
    void insertIn(vector<vector<int>> &vec, int loc, int ist) {
        vector<int> target = vec[ist];
        for(int i = ist; i > loc; i-- )
        {
            vec[i] = vec[i - 1];
        }
        vec[loc] = target;
    }
    
public:
    vector<vector<int>> reconstructQueue(vector<vector<int>>& people) {
        auto cmp = [](vector<int> &a, vector<int> &b) {
            if(a.at(0) > b.at(0))
            {
                return true;
            } else if (a.at(0) == b.at(0) && a.at(1) < b.at(1)) {
                return true;
            } else {
                return false;
            }
        };
        
        sort(people.begin(), people.end(), cmp);
        for(int i = 0; i < people.size(); i++)
        {
            if(people[i][1] != i)
            {
                insertIn(people, people[i][1], i);
            }
        }
        return people;
    }
```

122 Best Time to Buy and Sell Stock II
===

At first I thought need to keep two value.

* The biggest interval of stock price.
* Added up profit.

Then compare them.

Actually, second can do both.

```cpp
int maxProfit(vector<int>& prices) {
        int low = prices[0];
        int prof = 0;
        for (int i = 1; i < prices.size(); i++)
        {
            
            if(prices[i] < low)
            {
                low = prices[i];
            } else if (prices[i] > low) {
                prof = prof +prices[i] - low;
                low = prices[i];
            }
        }
        return prof;
    }
```


