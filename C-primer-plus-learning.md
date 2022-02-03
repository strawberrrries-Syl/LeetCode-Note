# string
## Difference between `cin` and `getline`:

  `cin`: get a word from input stream, seperated by space "\ ", inputsstream will still have LF
  
  `getline`: get a line seperawted by LF.

*If you use getline after cin, cout. There will be a empty line with only LF in it.

## `s.size()`

When using `s.size() > n`, n should better not be minus value.
* size() returns a unsigned value, which makes n turn to unsigned int-> a big positive value.

## string adding:
at least one operand to each + operator must be of string type

Example: 
```cpp 
string s1 = "hello";  
string s6 = s1 + ", " + "world"; // right
string s7 = "hello" + ", " + "s2";  // error
```

## `decltype()`
used for declare some unknown value's type

## `for(declaration : expression)`
when you only want to iterate things in expression and not go to change itself, you can not use reference of it. Instead, you shoud use reference.
*Example:

``` cpp
string s = "some string";
    for (auto &c : s)
    {
        c = toupper(c);
    }
    cout << s << endl;
```
OUTPUT:
`"SOME THING"`
  ```cpp
string s = "some string";
    for (auto c : s)
    {
        c = toupper(c);
    }
    cout << s << endl;
 ```
OUTPUT:
`"some string"`
