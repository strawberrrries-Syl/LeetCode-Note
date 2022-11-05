# 1. 特点
二叉树构成。每个元素都唯一。也是用红黑树构成。

# 2. init
```cpp
#include <set>

set<int> s;
// 排好序
s.insert(int i);
s.erase();

```

# 3. 常用方法
```cpp
s.find();
s.count();  // 都可以查找元素，一个返回指针，一个返回1、0

s.begin();
s.end();

s.size();

s.lower_bound(x); /* 返回第一个大于等于x的迭代器 */
s.upper_bound(x); /* 返回第一个大于x的迭代器 */

```

# 4. multiset
可以允许多个相同值出现.
用法和set相似
```cpp
multiset<int> ms;
```
