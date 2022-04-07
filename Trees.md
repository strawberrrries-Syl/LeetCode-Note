Tree is a non-linear structure. A recursive data structure.

* Root, children, parent, sibling(from the same parent)
* Leaf nodes(no child nodes)
* each nodes only have 1 incoming node (except the root).

## Binary Tree
struct TreeNode
{
  int val;
  TreeNode* left;
  TreeNode* right;
  
}



## Application:
1. files
2. searching
3. trie ->dictionary


## Binary Tree
*Each node can have at most 2 children*

* **Strict binary tree/ proper binary tree: **

each node have 2 or 0 childre

* **Complete binary tree**

按顺序存数据，没有跳过某个空位插入（从上到下，从左到右，不留空位）

-------------- [1] ------------------

----------- / --------\ -------------

------- [2] ---------- [3] ----------

----- / - \ -------- / ---- \ -------

-- [4] -- [5] ---- [6] ---- [7] -----

-- / --------------------------------

[8] ---------------------------------




