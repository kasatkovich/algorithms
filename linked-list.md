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
#second solution
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
    
#third solution
def getIntersectionNode(self, headA, headB):
    if not headA or not headB:
        return None
    cur1 = headA
    cur2 = headB
    count1 = count2 = 0
    while cur1:
        count1 += 1
        cur1 = cur1.next
    while cur2:
        count2 += 1
        cur2 = cur2.next
    cur1 = headA
    cur2 = headB
    if count1 > count2:
        i = 0
        while cur1 and i < count1 - count2:
            cur1 = cur1.next
            i += 1
    else:
        i = 0
        while cur2 and i < count2 - count1:
            cur2 = cur2.next
            i += 1
    while cur1 and cur2  and cur1 != cur2:
        cur1 = cur1.next
        cur2 = cur2.next
    return cur1

#fourth solution
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












