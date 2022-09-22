# 形式
```cpp
[capture] (parameter) {body}

// e.g. x,y都用传值的方式给参
[] (int x, int y) -> ubt {int z = x+y; return z+x; }

// or x传值，y引用
[x, &y] (int x, int y) -> ubt {int z = x+y; return z+x; }
```