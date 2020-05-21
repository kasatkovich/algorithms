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

## Merge Two Sorted Lists
https://leetcode.com/problems/merge-two-sorted-lists/

'''python
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

'''



