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

// 重点api
l.splice(iter pos, list l, iter element);
//在list l 的 迭代器 pos处，插入迭代器为element 的元素，并交换
void splice (iterator position, list& x);
// 将整个list x的元素，transfer到container中
void splice (iterator position, list& x, iterator i);
// 将x中的元素itransfer到容器的位置pos处
void splice (iterator position, list& x, iterator 
first, iterator last);
// 将x中从first到las的元素transfer到容器位置pos处

```