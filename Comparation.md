# How to sort vectors as your way?
Want to sort vectors by the first thing in them:

``` cpp

 auto compare = [](vector<int> &intervalA, vector<int> &intervalB){
            return intervalA.at(1) < intervalB.at(1);
        };
        
        sort(intervals.begin(), intervals.end(),compare);
        // sort as small to big
```
**important**
the ```cmp``` function must return a bool ans.

You can use this sort function in struct. As below:
```cpp
struct someThing {
        string name;
        int age;
        int height;
        string birthday;

        someThing()
        {
            name = "";
            age = 0;
            height = 0;
            birthday = "";
        };
    };
    
  auto cmp2 = [](someThing& a, someThing& b) {
        return a.age > b.age;
    };

```
