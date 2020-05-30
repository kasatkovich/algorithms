# linked list
+[Reverse Linked List](#reverse-linked-list)
+[Middle of the Linked List](#middle-of-the-linked-list)
+[Palindrome Linked List](#palindrome-linked-list)
+[Merge Two Sorted Lists](#merge-two-sorted-lists)


## Reverse Linked List
https://leetcode.com/problems/reverse-linked-list/

## Middle of the Linked List
https://leetcode.com/problems/middle-of-the-linked-list/

## Palindrome Linked List
https://leetcode.com/problems/palindrome-linked-list/
```python
#first solution
def isPalindrome(self, head):
    slow = head
    fast = head
    stack = []
    while fast and fast.next:
        stack.append(slow.val)
        slow = slow.next
        fast = fast.next.next
    if fast:
        slow = slow.next
    while slow:
        if slow.val != stack.pop():
            return False
        slow = slow.next
    return True
 #second solution
 def getListLength(self, head):
    cnt = 0
    while head:
        head = head.next
        cnt += 1
    return cnt


def inverseHalfList(self, head, n):
    pre_idx = (n - 1) / 2
    pre = head
    for i in range(pre_idx):
        pre = pre.next
    p = pre.next
    for i in range(n - pre_idx - 2):
        tmp = pre.next
        pre.next = p.next
        p.next = p.next.next
        pre.next.next = tmp
    return pre_idx, pre.next


def isPalindrome(self, head):
    n = self.getListLength(head)
    if n < 2:
        return True
    p = head
    j, q = self.inverseHalfList(head, n)
    for t in range(n - j - 1):
        if p.val != q.val:
            return False
        p, q = p.next, q.next
    return True

 ```


## Merge Two Sorted Lists
https://leetcode.com/problems/merge-two-sorted-lists/



