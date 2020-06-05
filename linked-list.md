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

## Middle of the Linked List
https://leetcode.com/problems/middle-of-the-linked-list/

## Palindrome Linked List
https://leetcode.com/problems/palindrome-linked-list/

## Merge Two Sorted Lists
https://leetcode.com/problems/merge-two-sorted-lists/

## Remove Nth Node From End of List
https://leetcode.com/problems/remove-nth-node-from-end-of-list/

## Linked List Cycle II
https://leetcode.com/problems/linked-list-cycle-ii/

## Linked List Cycle
https://leetcode.com/problems/linked-list-cycle/

## Reorder List
https://leetcode.com/problems/reorder-list/

## Intersection of Two Linked Lists
https://leetcode.com/problems/intersection-of-two-linked-lists/

```python
#first solution
def getSize(self, head: ListNode) -> int:
    cur = head
    size = 0
    while cur:
        size += 1
        cur = cur.next
    return size


def getIntersectionNode(self, headA: ListNode, headB: ListNode) -> ListNode:
    size_of_a, size_of_b = self.getSize(headA), self.getSize(headB)
    diff = size_of_a - size_of_b
    if diff > 0:
        for i in range(diff):
            headA = headA.next
    elif diff < 0:
        for i in range(abs(diff)):
            headB = headB.next
    while headA and headB:
        if headA is headB:
            break
        headA = headA.next
        headB = headB.next
    return headA

 

#second solution
def getIntersectionNode(self, headA: ListNode, headB: ListNode) -> ListNode:
    curA, curB = headA, headB
    while curA is not curB:
        if curA:
            curA = curA.next
        else:
            curA = headB
        if curB:
            curB = curB.next
        else:
            curB = headA
    return curA

```

## Sort List
https://leetcode.com/problems/sort-list/












