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
 
 ```python
 def isSymmetric(self, root: TreeNode) -> bool:
    if not root:
        return True
    level = [root]
    while level:
        nextlevel = []
        val = []
        for node in level:
            if node.right:
                nextlevel.append(node.right)
                val.append(node.right.val)
            else:
                val.append("Empty")
            if node.left:
                nextlevel.append(node.left)
                val.append(node.left.val)
            else:
                val.append("Empty")
        if val != val[::-1]:
            return False
        level = nextlevel
    return True

```



## Same Tree

https://leetcode.com/problems/same-tree/



## Invert Binary Tree
https://leetcode.com/problems/invert-binary-tree/



## Path Sum

https://leetcode.com/problems/path-sum/



## Binary Tree Level Order Traversal

https://leetcode.com/problems/binary-tree-level-order-traversal/



## Subtree of Another Tree

https://leetcode.com/problems/subtree-of-another-tree/



## Kth Smallest Element in a BST

https://leetcode.com/problems/kth-smallest-element-in-a-bst/



## Validate Binary Search Tree

https://leetcode.com/problems/validate-binary-search-tree/


## Binary Search Tree Iterator

https://leetcode.com/problems/binary-search-tree-iterator/

