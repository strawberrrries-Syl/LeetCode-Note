# 1. 特点
不能通过位置直接访问元素

# 2. init
```cpp
list<T> l;

// 3种方式
list<int> l1 = {1,2,3}; // 用数组初始化
list<int> l2(3,11);     //  三个11
lsit<int> l3(l2);       // copyl2
```

# 3. operations
```cpp
// 返回的引用
l.front();
l.back();

// 其余与deque相同，有双向pop，push操作

// 这两个操作map没有
l.reverse();    // reverse
l.sort();

l.push_front();
l.pop_front();

l.push_back();
l.pop_back();

l.insert(iter pos, T value);
l.erase(iter pos);
l.remove(T value);
```