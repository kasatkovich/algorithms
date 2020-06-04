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
def getIntersectionNode(self, headA: ListNode, headB: ListNode) -> ListNode:
    i = ListNode()
    i = copy.copy(headA)
    len1 = 0
    while i:
        i = i.next
        len1 += 1
    i = ListNode()
    i = copy.copy(headB)
    len2 = 0
    while i != None:
        i = i.next
        len2 += 1
    if len1 > len2:
        while len1 != len2:
            headA = headA.next
            len1 -= 1;
    else:
        while len1 != len2:
            headB = headB.next
            len2 -= 1
    while headA != headB:
        headA = headA.next
        headB = headB.next
    return headA
 

#second solution
def getIntersectionNode(self, headA: ListNode, headB: ListNode) -> ListNode:
    if not headA or not headB:
        return None
    currA, currB = headA, headB
    is_secondA, is_secondB = 0, 0
    while(currA != currB):
        if is_secondA == 0 and not currA.next:
            is_secondA = 1
            currA = headB
        else:
            currA = currA.next
        if is_secondB == 0 and not currB.next:
            is_secondB = 1
            currB = headA
        else:
            currB = currB.next
    return currA


```

## Sort List
https://leetcode.com/problems/sort-list/












