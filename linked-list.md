# linked list
+[Reverse Linked List](#reverse-linked-list)


## Reverse Linked List
https://leetcode.com/problems/reverse-linked-list/

def reverseList(self, head: ListNode) -> ListNode:
        prev = None
        curr = head
        if curr is None:
            return None
        if curr.next is None:
            return curr
        while curr:
            nxt = curr.next
            curr.next = prev
            prev = curr
            curr = nxt
        return prev

