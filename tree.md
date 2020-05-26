# Tree

+ [Binary Tree Inorder Traversal](#binary-tree-inorder-traversal)
+ [Symmetric Tree](#symmetric-tree)
+ [Maximum Depth of Binary Tree](#maximum-depth-of-binary-tree)
+ [Same Tree](#same-tree)
+ [Invert Binary Tree](#invert-binary-tree)
+ [Path Sum](#path-sum)
+ [Binary Tree Level Order Traversal](#binary-tree-level-order-traversal)
+ [Subtree of Another Tree](#subtree-of-another-tree)
+ [Kth Smallest Element in a BST](#kth-smallest-element-in-a-bst)
+ [Validate Binary Search Tree](#validate-binary-search-tree)
+ [Binary Search Tree Iterator](#binary-search-tree-iterator)

## Binary Tree Inorder Traversal

https://leetcode.com/problems/binary-tree-inorder-traversal/



## Symmetric Tree

https://leetcode.com/problems/symmetric-tree/

## Maximum Depth of Binary Tree
https://leetcode.com/problems/maximum-depth-of-binary-tree/




## Same Tree

https://leetcode.com/problems/same-tree/



## Invert Binary Tree
https://leetcode.com/problems/invert-binary-tree/



## Path Sum

https://leetcode.com/problems/path-sum/



## Binary Tree Level Order Traversal

https://leetcode.com/problems/binary-tree-level-order-traversal/
```python
#first solution
def levelOrder(self, root: TreeNode) -> List[List[int]]:
    self._levels = []
    self.get_level(root, 0)
    return self._levels


def get_level(self, root, depth):
    if not root:
        return
    if depth == len(self._levels):
        self._levels.append([])
    self._levels[depth].append(root.val)
    self.get_level(root.left, depth + 1)
    self.get_level(root.right, depth + 1)

#second solution
def levelOrder(self, root):
    index = 0
    ans, queue = [], [(root, index)]
    while queue:
        node, level = queue.pop(0)
        if node:
            if len(ans) == level:
                ans.append([])
            ans[level] = ans[level] + [node.val]
            queue.append((node.left, level+1))
            queue.append((node.right, level+1))
    return ans

```


## Subtree of Another Tree

https://leetcode.com/problems/subtree-of-another-tree/



## Kth Smallest Element in a BST

https://leetcode.com/problems/kth-smallest-element-in-a-bst/



## Validate Binary Search Tree

https://leetcode.com/problems/validate-binary-search-tree/


## Binary Search Tree Iterator

https://leetcode.com/problems/binary-search-tree-iterator/

