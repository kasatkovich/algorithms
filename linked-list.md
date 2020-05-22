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
def getIntersectionNode(self, headA: ListNode, headB: ListNode) -> ListNode:
    A_nodes, B_nodes = [], set()
    while headA:
        A_nodes.append(headA)
        headA = headA.next
    while headB:
        B_nodes.add(headB)
        headB = headB.next
    for node in A_nodes:
        if node in B_nodes:
            return node
    return None


def getIntersectionNode(self, headA, headB):
    if not headA or not headB: return None
    lenA, lenB = 0, 0 
    currA, currB = headA, headB
    while currA.next:
        currA = currA.next
        lenA += 1
    while currB.next:
        currB = currB.next
        lenB += 1
    if currA != currB: return None
    diff = 0
    if lenA > lenB:
        tmp1 = headA
        tmp2 = headB
        diff = lenA - lenB
    else:
        tmp1 = headB
        tmp2 = headA
        diff = lenB - lenA
    while diff > 0:
        tmp1 = tmp1.next
        diff -= 1
    while tmp1 != tmp2:
        tmp1 = tmp1.next
        tmp2 = tmp2.next
    return tmp1

```

## Sort List
https://leetcode.com/problems/sort-list/












