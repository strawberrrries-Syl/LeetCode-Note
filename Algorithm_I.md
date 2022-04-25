## binary search

Using high pointer and low pointer

**important**
```cpp
low = low + 1;    // do not stuck into loop plz
high = high - 1;

curr = low + (high - low) / 2; // always remember to add this one
```
## Two Sum

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

**Important:**
When the array is not sorted, we can put them in hash map.
not map<int, int>, but map<int, vector<int>>
! can store multiple position.

**Important**
  INT_MAX INT_MIN
