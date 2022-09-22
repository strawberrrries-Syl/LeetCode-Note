# Difference between `map` & `unordered_map`
*`unordered_map`在用迭代器输出时是按key有序的*

# 1. init  `map`是红黑树构成的
```cpp
map<key, value> name;
```
# 2.  insert
```cpp
map[key] = value; // 1. 
map.insert(pair<key, value>); //2. 

map.size();   // 获取大小

```
# 3. Operations
```cpp
map.find(key);  // return iter，相当于指针，用iter->first or iter->second操作
// 如果没找到，返回map.end()
map.count(key); // 找到返回1，没找到返回0
map.empty();

map.erase(iter);  // 可以按照迭代器删除
map.erase(key);   // 也可以按照key的值删除

map.lower_bound(key);  // 返回键值大于给定元素的第一个位置

map.upper_bound(key); // 返回键值小于给定元素的第一个位置

// 正向迭代器
map.begin();
map.end();
// 反向迭代器
map.rbegin();
map.rend();

```
# 4. 迭代
```cpp
// method 1
for(auto p : map)
{
  p.first;  // key
  p.second; // value
}
// method 2 
for(auto iter = map.begin(); iter != map.end(); iter++)
{
  iter->first;  // key
  iter->second; // value
}
```

# 4. hash map  `unordered_map` 以bucket实现:
# 4.1 init

```cpp
#include <unoredered_map>
unordered_map<key, value> map;

map.size();

map.clear();

```

# 4.2 operations
```cpp
map.insert();
// or
map[key];

map.find(key);

map.erase(iter);

map.begin();
map.end();

map.count(key);  // 找到返回1，没找到返回0

bool map.empty();
```
