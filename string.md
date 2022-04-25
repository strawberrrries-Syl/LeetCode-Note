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
