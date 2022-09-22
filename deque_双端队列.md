# 1. 特点介绍
* 支持高效的插入和删除容器的头部元素。 -> 双端队列
* 但访问元素时，因为多了一个中间步骤，所以会比`vector`慢一点

# 2. init
```cpp
#include <deque>

deque<T> name;
deque<T> name(n, elem);
deque<T> name(n);

```

# 3. operations
```cpp
d.begin(); d.cend();
d.rbegin(); d.rend();
d.front(); d.end();

d.push_back(); d.pop_back();
d.push_front(); d.pop_front();

d.insert(iter pos, Elem elem);
```