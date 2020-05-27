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

```python
#first solution
def inorderTraversal(self, root: TreeNode) -> List[int]:
    res = []
    stack = deque([])
    while stack or root:
        while root:
            stack.append(root)
            root = root.left
        top = stack.pop()
        res.append(top.val)
        root = top.right
    return res
    
#second solution
def inorderTraversal(self, root):
    def helper(nodeIn, res):
        if nodeIn:
            helper(nodeIn.left, res)
            res.append(nodeIn.val)
            helper(nodeIn.right, res)
    res = []
    if not root:
        return res
    helper(root, res)
    return res

```


## Symmetric Tree

https://leetcode.com/problems/symmetric-tree/
 
 ```python
 #first solution
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

#second solution
def isSymmetric(self, root: TreeNode) -> bool:
    if not root:
        return True

    def isIdentical(left, right):
        if not left and not right:
            return True
        if not left or not right:
            return False
        if left.val != right.val:
            return False
        else:
            return isIdentical(left.left, right.right) and isIdentical(left.right, right.left)
    return isIdentical(root.left, root.right)


```

## Maximum Depth of Binary Tree
https://leetcode.com/problems/maximum-depth-of-binary-tree/




## Same Tree

https://leetcode.com/problems/same-tree/
```python
def isSameTree(self, p: TreeNode, q: TreeNode) -> bool:
    if not p or not q :
        return p == q
    if p.val != q.val:
        return False
    return self.isSameTree(p.left, q.left) and self.isSameTree(p.right, q.right)


```



## Invert Binary Tree
https://leetcode.com/problems/invert-binary-tree/

```python
def invertTree(self, root: TreeNode) -> TreeNode:
    if root:
        root.left, root.right = self.invertTree(root.right), self.invertTree(root.left)
        return root
```

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

