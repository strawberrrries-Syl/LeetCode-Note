# 15. 3Sum
## About max:
```cpp
max({int1, in2, in3});  //get max value from a set of number.
```
## Thinking
1. ALWAYS remember to sort a vector first. This can help you to prevent a lot of work when you try to keep no duplication.
2. Hashmap is faster than lots of method. Try to use this no matter what you are doing.
3. Remember to `clear` containers
4. Calm down.

# 160 Intersection of Two Linked Lists
## when meet the linked list problem, think about two pointers.
For finding the intersection
`a+c+b = b+c+a`
this can help us solve it.

# 94. Binary Tree Inorder Traversal
## Traversal term:
`Inorder Traversal` -- 中序遍历
`Preorder Traversal` -- 前序遍历
`Postorder Traversal` -- 后序遍历

## Combine vectors
```cpp
vector1, vector2;
vector1+vector2 = vector1.insert(vector1.end(), vector2.begin(), vector2.end());
```

# 116. Populating Next Right Pointers in Each Node *
*Tree -> recursion*

For preorder traversal, top part has been dealed. 



# 17. Letter Combinations of a Phone Number
Searching problem. `dfs` deep first search. `bfs` broad first search.
## push multiple value in vector:
```cpp
vec = {a,b,c,d,e};
```

## push multiple key+value in map:
```cpp
map = {{key1, value1}, {key2, value2}};
```

# 34. Find First and Last Position of Element in Sorted Array
## Think of hashmap
too complicated.
## binary search
1. find the start
2. find the end

start position has characters:  left number is smaller than it or itself is at the 0 position.


# 49. Group Anagrams

**REMEMBER**
`string` can be sorted too.
