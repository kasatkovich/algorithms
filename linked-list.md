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
def isPalindrome(self, head: ListNode) -> bool:
    reverse = None
    middle = bottom = head
    while bottom and bottom.next:
        bottom = bottom.next.next
        reverse, reverse.next, middle = middle, reverse, middle.next
    if bottom:
        middle = middle.next
    while reverse and reverse.val == middle.val:
        middle = middle.next
        reverse = reverse.next
    return not reverse

 ```


## Merge Two Sorted Lists
https://leetcode.com/problems/merge-two-sorted-lists/



