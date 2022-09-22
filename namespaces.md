# 1. namespace的有来：
为了避免一些重复的函数名的混乱引用。最熟悉的`namespace`是
```cpp
std::cin >>  ； 
std::cout << xxx << std::endl;
```

# 2. definition
```cpp
namespace xxx {

    // 括号内的内容可以直接引用，不用带域名
    func1();

}

// 括号外需要指定空间名称+内部名称
```

# 3. 引用
```cpp
using namespace xxx

func1();
```