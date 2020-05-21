# linked list
+[Reverse Linked List](#reverse-linked-list)
+[Middle of the Linked List](#middle-of-the-linked-list)
+[Palindrome Linked List](#palindrome-linked-list)


## Reverse Linked List
https://leetcode.com/problems/reverse-linked-list/

## Middle of the Linked List
https://leetcode.com/problems/middle-of-the-linked-list/

## Palindrome Linked List
https://leetcode.com/problems/palindrome-linked-list/

'''python
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
 
 '''




