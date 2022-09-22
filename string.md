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





# Operation
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
## find substr:
```cpp
string.find("");  // find first one
string.rfind("");  // find last one

string.substr(start_pos, end_pos); // get sub-string from start_position, to end_position.
```
## int to string:
```cpp
to_string(int);
```

## string to int

```cpp
stoi(string);
stof();
stol();
stod();
//...
```
## stringstream:
### 1. turn int to string
```cpp
int 12345678;
string sa;
stringstream s;
s << a;
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
