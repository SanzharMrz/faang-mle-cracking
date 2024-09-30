# 206. Reverse a Linked List

* link: [[https://leetcode.com/problems/remove-duplicates-from-sorted-array/description/](https://leetcode.com/problems/remove-element/description/)(https://leetcode.com/problems/reverse-linked-list/description/)
* main idea:
  * create two pointers
    * ```current``` which is copy of head
    * ```previous``` which in initialized as none
  * start while loop while ```current``` is not None
    * create ```temp``` variable which is copy of next item of ```current```
    * replace next pointer of ```current``` with previous
    * make ```previous``` to ```current```
    * make current as ```temp```
  * return ```previous```
* Solution:
  
  * ```python
    class Solution:
      def reverseList(self, head: Optional[ListNode]) -> Optional[ListNode]:
        current = head
        previous = None
        while current:
            temp = current.next
            current.next = previous
            previous = current
            current = temp
        return previous

* Time Complexity: ```O(n)```, where n is the length of the input array. We scan through the array once.
* Space Complexity: ```O(1)```, since we are modifying the array in place and not using any extra space.
