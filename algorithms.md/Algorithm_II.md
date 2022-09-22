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

**Important Thinking**
Remember to use the next domain in the Node. 
You can use next to serch previous level's value!!!

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


# 200. Number of Island
Classic problem of `dfs`, `bfs`.

## DFS (Deep First Search)
test 1, and uniform every neighbor 1 to 0. 

write a dfs function to traverse tge graph. As long as you meet '1', change it to '0';

```cpp
class Solution {
public:
    void dfs(vector<vector<char>>& grid, int r, int c) {
        if(grid[r][c] == '1')
        {
            grid[r][c] = '0';
            if(c+1 < grid[0].size())
            {
               dfs(grid, r, c+1); 
            }
            if(r+1 < grid.size())
            {
                dfs(grid, r+1, c);
            }
            if(r>0)
            {
               dfs(grid, r-1, c); 
            }
            if(c>0)
            {
                dfs(grid, r, c-1);
            }
        }
    }
    
public:
    int numIslands(vector<vector<char>>& grid) {
        int cnt = 0;
        for(int i = 0; i < grid.size(); i++)
        {
            for(int j = 0; j < grid[i].size(); j++)
            {
                if(grid[i][j] == '1')
                {
                    dfs(grid, i, j);
                    cnt ++;
                }
            }
        }
        return cnt;
    }
};
```



## BFS (Broad First Search)
need queue;

push all nodes which has value '1'. Then test its arround area. Until there's nothing in queue.

**IMPORTANT**
key thought is broad first.

maintain a queue ti store all the point need to be dealed with.

Boundary: when there's nothing in the queue, the bfs can stop.

```cpp
class Solution {
    
public: 
    void bfs(vector<vector<char>>& grid, queue<vector<int>> q) {
        vector<int> pos;
        while(q.size() > 0)
        {
            pos = q.front();
            q.pop();
            int r = pos[0];
            int c = pos[1];
            if(grid[r][c] == '1')
            {
                grid[r][c] = '0';
                if(c < grid[0].size() - 1)
                {
                  if(grid[r][c+1] == '1')
                  {
                      pos = {r, c+1};
                      q.push(pos);
                  }
                }
                if(r < grid.size() - 1)
                {
                    if(grid[r+1][c]=='1')
                    {
                        pos = {r+1, c};
                        q.push(pos);
                    }
                }
                if(r>0)
                {
                    if(grid[r-1][c] == '1')
                    {
                        pos = {r-1, c};
                        q.push(pos);
                    }
                }
                if(c>0)
                {
                    if(grid[r][c-1] == '1')
                    {
                        pos = {r,c-1};
                        q.push(pos);
                    }
                }
            }
        }
    }
public:
    int numIslands(vector<vector<char>>& grid) {
        int cnt = 0;
        queue<vector<int>> q;
        for(int i = 0; i < grid.size(); i++)
        {
            for(int j = 0; j < grid[i].size(); j++)
            {
                if(grid[i][j] == '1')
                {
                    cnt ++;
                    vector<int> pos = {i,j};
                    q.push(pos);
                    bfs(grid, q);
                }
            }
        }
        return cnt;
    }
};
```

# 22. Generate Parentheses
A classic `backtracking` problem

*Whe will you use backtracking method?*

when you need to output every result from running.

This problem is a classic one.

*How to use it?*
1. give a changebal vector to store every single answer from your code and pass as a parameter of your helper function. 
2. Everytime when you are in the end of handling, push back it.

# 62. Unique Paths
`Dynamic Programming`
**Memory array/List**


