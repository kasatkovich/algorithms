# linked list
+[Reverse Linked List](#reverse-linked-list)
+[Middle of the Linked List](#middle-of-the-linked-list)


## Reverse Linked List
https://leetcode.com/problems/reverse-linked-list/

## Middle of the Linked List
https://leetcode.com/problems/middle-of-the-linked-list/

def middleNode(self, head: ListNode) -> ListNode:
        slow = head
        fast = head
        try:
            while fast.next.next:
                fast = fast.next.next
                slow = slow.next
            slow = slow.next
        except:
            pass
        return slow



