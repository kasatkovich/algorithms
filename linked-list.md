# linked list
+[Reverse Linked List](#reverse-linked-list)
+[Middle of the Linked List](#middle-of-the-linked-list)
+[Palindrome Linked List](#palindrome-linked-list)
+[Merge Two Sorted Lists](#merge-two-sorted-lists)
+[Remove Nth Node From End of List](#remove-nth-node-from-end-of-list)
+[Linked List Cycle II](#linked-list-cycle-ii)
+[Linked List Cycle](#linked-list-cycle)
+[Reorder List](#reorder-list)
+[Intersection of Two Linked Lists](#intersection-of-two-linked-lists)
+[Sort List](#sort-list)
## Reverse Linked List
https://leetcode.com/problems/reverse-linked-list/
```python
def reverseList(self, head: ListNode) -> ListNode:
    prev = None
    curr = head
    while curr:
        next = curr.next
        curr.next = prev
        prev = curr
        curr = next
    return prev

```

## Middle of the Linked List
https://leetcode.com/problems/middle-of-the-linked-list/

```python
def middleNode(self, head: ListNode) -> ListNode:
    slow = head
    fast = head
    while fast and fast.next:
        fast = fast.next.next
        slow = slow.next
    return slow
```

## Palindrome Linked List
https://leetcode.com/problems/palindrome-linked-list/

## Merge Two Sorted Lists
https://leetcode.com/problems/merge-two-sorted-lists/

```python
def mergeTwoLists(self, l1: ListNode, l2: ListNode) -> ListNode:
    merged_list = ListNode()
    current_merged = merged_list
    while l1 and l2:
        if l1.val < l2.val:
            current_merged.next = l1
            l1 = l1.next
        else:
            current_merged.next = l2
            l2 = l2.next
        current_merged = current_merged.next
    if l1:
        current_merged.next = l1
    else:
        current_merged.next = l2
    return merged_list.next

```

## Remove Nth Node From End of List
https://leetcode.com/problems/remove-nth-node-from-end-of-list/

## Linked List Cycle II
https://leetcode.com/problems/linked-list-cycle-ii/

## Linked List Cycle
https://leetcode.com/problems/linked-list-cycle/

## Reorder List
https://leetcode.com/problems/reorder-list/

```python
#first solution
def reorderList(self, head: ListNode) -> None:
    if not head:
        return head
    node = head
    parent = None
    while node.next:
        node.parent = parent
        parent = node
        node = node.next
    node.parent = parent
    end = node
    node = head
    while node:
        n = _next = node.next
        if n == end:
            break
        if n:
            end.parent.next = None
            node.next = end
            end.next = _next
        node = _next
        end = end.parent
    return head

#second solution
def _splitList(head):
    fast = head
    slow = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next
        fast = fast.next
    middle = slow.next
    slow.next = None
    return head, middle
def _reverseList(head):
    last = None
    currentNode = head

    while currentNode:
        nextNode = currentNode.next
        currentNode.next = last
        last = currentNode
        currentNode = nextNode
    return last
def _mergeLists(a, b):
    tail = a
    head = a
    a = a.next
    while b:
        tail.next = b
        tail = tail.next
        b = b.next
        if a:
            a, b = b, a
    return head
class Solution:
    def reorderList(self, head):
        if not head or not head.next:
            return
        a, b = _splitList(head)
        b = _reverseList(b)
        head = _mergeLists(a, b

```

## Intersection of Two Linked Lists
https://leetcode.com/problems/intersection-of-two-linked-lists/

## Sort List
https://leetcode.com/problems/sort-list/


