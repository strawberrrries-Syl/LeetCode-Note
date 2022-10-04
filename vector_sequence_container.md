# 1.  Definition & Init
```cpp

#include <vector>
// 通用
vector<type> name(number, init_elem);
// e.g.
vector<int> vec(10,1);  // 初始化一个int vector，10个1
vector<int> newvec(vec);    // 用已有vec初始化新vec
// 也可以vector套vector
vector<vector<int>> vec2;   // 二维数组

// 大小
vec.size();
```

# 2. Oprations
```cpp
// 加入
vec.push_back(int i);
// 仅删除末尾，无返回值
vec.pop_back();
// 插入
vec.insert(* position, Elem elem);
// pos 可以是vec.begin() + 偏移；
vec.erase(* pos);   // 这里的pos也必须是迭代器，也可以加偏移
// 两vec内容交换
vec.swap(another_vec); //  swap every element in two 

vec.begin(); vec.end(); // 返回迭代器

vec.back(); vec.front(); // 头，尾

bool vec.empty();

vec.clear();    // 清除所有元素
```

# 3. 迭代
```cpp
// 可以直接索引访问：
vec[int i];

// or 迭代器

for(auto x : vec)
{
    x;
}
// 或者这样
for (auto i = v.begin(); i != v.end(); i++)
    {
        cout << *i << endl;
    }

// 迭代器是指针，可以通过取值符号得到
```
