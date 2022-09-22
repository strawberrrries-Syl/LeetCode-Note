 # 1. Define
 ```cpp
 type arrayName [arraySize];

 //e.g.
 int a[10];

 ```

 # 2. 初始化
 ```cpp
 int a[10] = {1,2,3,4,5,6,7,8,9,10};
 // or
 int a[] = {1,2,3,4,5,6,7}; //a的size为7


 ```

 # 3. 遍历
 ```cpp
 for(auto & c : array)
 {

 }
 // or just like in java
 for(int i : array)
 {

 }
 ```

 # 4. 指针数组（存放多个指针的数组）
 ```cpp
 int* ptr[3] = {1,2,3};
 *ptr[0];   // = 1


 ```