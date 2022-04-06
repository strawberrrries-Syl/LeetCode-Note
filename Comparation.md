# How to sort vectors as your way?
Want to sort vectors by the first thing in them:

``` cpp

 auto compare = [](vector<int> &intervalA, vector<int> &intervalB){
            return intervalA.at(1) < intervalB.at(1);
        };
        
        sort(intervals.begin(), intervals.end(),compare);
```
