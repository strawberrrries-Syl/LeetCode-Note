Linked List Method
==

Fast and slow pointer method.
---
1. For list which need to decide whether it has a loop.
2. Finding half point.

Sometimes, find the intersection of two lists, without loop inside. Can also make it like looping. If one iter to end, make it be any header agian.

For delete exact value nodes:
---
1. strat from a none value node
2. delete next node which same as in title
3. remember only next one not the aim number can move pointer to next.

Palindrome Linked List
---
two ways
1. (mine) find half point, check
2. reverse = original

Stacks & Queue
==
Infix expression & Postfix expression
--
1. numbers out directly.
2. symbols push in stack. Until exists ) or }, pop out. Or next symbol has lower level than before.

Using 2 queues realizing stack
----
Remember not using queue's size() as iter. It's changing and easy to make mistakes.

Special calculation
---
string to int: stoi().

First unrepeated character:
---
my thought: delet repeat one.
simple algorithms:
1. hashmap.
2. record the frequency of 26 letters.

my answer
```cpp
class Solution {
public:
    int firstUniqChar(string s) {
        int sizestring = s.size();
        vector<bool> flag;
        for (int k = 0; k < sizestring; k++)
        {
            flag.push_back(true);
        }

        int i = 0;
        while (i < s.size())
        {
            bool same = false;
            if (flag[i] == true)
            {
                for (int j = (i + 1); j < s.size(); j++)
                {
                    if (flag[j] == true)
                    {
                        if (s[i] == s[j])
                        {
                            same = true;
                            flag[j] = false;
                        }
                    }
                }

                if (same == true)
                {
                    flag[i] = false;
                }
                else
                {
                    return i;
                }
            }
            else
            {
                i++;
            }
        }
        return -1;
    }
};
```
refer others:
```cpp
    int flag[26] = { 0 };
    for (int j = 0; j < s.size(); j++)
    {
        int add = s[j] - 'a';
        flag[add] = flag[add] + 1;
    }
    for (int i = 0; i < s.size(); i++)
    {
        int add = s[i] - 'a';
        if (flag[add] == 1)
        {
            return i;
        }
    }
    return -1;
```


Tree 
====

Sorted arry to BST
----
1. find mid
2. left and right child use function.

```cpp
TreeNode* sortedArrayToBST(vector<int>& nums) {
        if(nums.size() == 0)
        {
            return nullptr;
        }
        int mid = (nums.size() + 1)/2 - 1;
        TreeNode *root = new TreeNode;
        root->val = nums[mid];
        
        if(nums.size() <2)
        {
            return root;
        }
        
        vector<int> l;
        vector<int> r;
        for(int i = 0; i < mid;i++)
        {
            l.push_back(nums[i]);
        }
        for(int i = mid+1; i < nums.size();i++)
        {
            r.push_back(nums[i]);
        }
        root->left = sortedArrayToBST(l);
        root->right = sortedArrayToBST(r);
        
        return root;
    }
```



Finding some path
--
#112

```cpp
bool hasPathSum(TreeNode* root, int targetSum) {
        int sum = targetSum;
        if(root != nullptr)
        {
            sum = sum - root->val;
            if(root->left == nullptr && root->right == nullptr && sum == 0)
            {
                return true;
            } else if (root->left == nullptr && root->right == nullptr) {
                return false;
            }
            
            bool l = hasPathSum(root->left, sum);
            bool r = hasPathSum(root->right,sum);
            
            if(l||r)
            {
                return true;
            }
            else 
            {
                return false;
            }
            
        }
        return false;
    }
```
