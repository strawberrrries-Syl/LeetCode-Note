# 1. 特点
first in, largest out.

堆的实现，可以实现堆排序

# 2. init
```cpp
#include <queue>

priority_queue<int> pq; // 默认是大顶堆

// or
priority_queue<template, container, cmp> pq;
// 可以通过lambda函数实现小顶堆
priority_queue<T, vector<int>, less<int>> pql;  // 小顶堆

```

# 3. operations
```cpp
pq.top();
pq.pop();
pq.push();
pq.size();
```

