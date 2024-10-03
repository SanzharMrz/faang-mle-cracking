# Linked list frequency

* link: [https://leetcode.com/problems/reverse-linked-list/description/](https://leetcode.com/problems/linked-list-frequency/)
* main idea:
  * create frequency table
  * while linked list is not empty, populate hash table
  * populate linked list with frequencies
* Solution:
  
  * ```python
    # Definition for singly-linked list.
    # class ListNode:
    #     def __init__(self, val=0, next=None):
    #         self.val = val
    #         self.next = next
    class Solution:
        def frequenciesOfElements(self, head: Optional[ListNode]) -> Optional[ListNode]:
            table = dict()
        
            while head:
                if head.val not in table.keys():
                    table[head.val] = 0
                table[head.val] += 1
                head = head.next
    
            freqs = list(table.values())
            freqs_node = final_freqs_node = ListNode(None)
            while freqs:
                freq = freqs.pop()
                freqs_node.next = ListNode(freq, None)
                freqs_node = freqs_node.next
    
            return final_freqs_node.next


* Time Complexity: ```O(n+m)```, where n is the length of the input array. We scan through the array once. iterate through frequencies m
* Space Complexity: ```O(n+m)```, since we are storing linked list of freqs and hash table freq
