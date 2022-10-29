# 求一个数有多少个1
```cpp
int res = 0;
while(a > 0)
{
    a & (a-1)
    res++;
}
res;    // res是1的个数
    

```