# Binary Search（二分法）
## 1. 应用场景
在一组数中寻找目标数。$O(nlogn)$时间复杂度。若不是sorted的数组，需要经过快速排序，$O(nlogn)$时间复杂度。
## 2. 算法
一般需要low, high两指针指向头和尾。
```java
int l = 0, h = nums.length-1;
while(l<=h)
{
    int mid = l + (h-l) / 2;
    // 判断语句
}
```
