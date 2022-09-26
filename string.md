# 1. type
# 1.1 c风格字符串
 等同于char[]；
```cpp
char ccc[] = "ashfdsajk";
string ccca = "ashfdsajk";
cout << " " << endl;
cout << sizeof(ccc) << endl;    // = 10 加了末尾的换行符
cout << strlen(ccc) << endl;    // = 9
cout << " " << endl;
```
# 1.2 `string`类

```cpp
// init

#include <string>

string s;

char c[] = "sfasdfs";
string s(c);    // 从字符串init
string s(c, len);   // 前len个

string str;
string s(str, startidx);    // substring

string s(str, startidx, len); 

string s(num, c);
```




# 2. Operation

# 2.1 for char[]
```cpp
strcpy(s1, s2); // 复制
strcat(s1, s2); // 连接

strlen(s1);     // 字符长度
strcmp(s1, s2);
strchr(s1, ch); // 返回一个指针，指向ch在s1中第一次出现的位置
// 相当于直接可以得到从此开始的子序列
// 没有匹配项时，返回NULL
strstr(s1, s2); // 返回s1中s2第一次出现的位置
```

# 2.2 for string only
```cpp
str.size();
str[idx];   // 访问


str.find(char c, int pos);  // 向后找   // 如果没有相同值，返回-1；
// if not found, return std::string::npos
str.rfind(char c, int pos); // 向前找
string.find("");  // find first one
string.rfind("");  // find last one
string.substr(start_pos, len); // get sub-string

// int to string
to_string(int);
// string to numbers
stoi(string);
stof();
stol();
stod();
```
## stringstream:
### 1. turn int to string
```cpp
int 12345678;
string sa;
stringstream s;
s << sa;
s >> sa;
s.clear();  // need
```

### 2. trun string to int
```cpp
class Solution {
public:
    int myAtoi(string s) {
       stringstream abc(s);
        int x=0;
        abc>>x;
        return x;
    }
};

```
