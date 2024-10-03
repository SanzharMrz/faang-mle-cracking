# merge-two-sorted-lists

* link: https://leetcode.com/problems/merge-two-sorted-lists/description/
* main idea:
  * create new node
  * copy it to traverse
  * while lists are not finished
    * if val1>val
      * create a new node from val and put it to new head
      * move list1 forward
    * opposite case is same
    * if they equal, create two new nodes and populate the main one
      * move two lists forward
    * move clone forward
    * if list1 or list2 are not ended, put one of them in the end
    
* Solution
  * ```python
    # Definition for singly-linked list.
    # class ListNode:
    #     def __init__(self, val=0, next=None):
    #         self.val = val
    #         self.next = next
    
    class Solution:
        def mergeTwoLists(self, list1: Optional[ListNode], list2: Optional[ListNode]) -> Optional[ListNode]:
            new_head = ListNode(None)
            head_clone = new_head
            while list1 and list2:
                if list1.val < list2.val:
                    head_clone.next = ListNode(list1.val, None)
                    list1 = list1.next
                elif list1.val > list2.val:
                    head_clone.next = ListNode(list2.val, None)
                    list2 = list2.next
                    print(head_clone.val)
                else:
                    head_clone.next = ListNode(list1.val, None)
                    head_clone = head_clone.next
                    head_clone.next = ListNode(list2.val, None)
                    list1 = list1.next
                    list2 = list2.next
                head_clone = head_clone.next
            if list1:
                head_clone.next = list1
            else:
                head_clone.next = list2
            return new_head.next
        

* Time Complexity: ```O(n+m)```, where n is the length of the input list1. m input of list2
* Space Complexity: ```O(n+m)```, storing n+m list
