# 27. remove-element

* link: [https://leetcode.com/problems/remove-duplicates-from-sorted-array/description/](https://leetcode.com/problems/remove-element/description/)
* main idea:
  * create two pointers
    * l for left one
    * r for right one
  * start comparing elements with ```val```
  * if they are not equal (i.e., a new unique element is found):
    * move forward left pointer and copy right element to the left element
    * move forward right pointer
  * if they equal, do nothing, move right pointer to the next element
    
* Solution
  * ```python class Solution:
    class Solution:
        def removeElement(self, nums: List[int], val: int) -> int:
            l = 0
            for r in range(len(nums)):
                if nums[r] != val:
                    nums[l] = nums[r]
                    l += 1
            return l

* Time Complexity: ```O(n)```, where n is the length of the input array. We scan through the array once.
* Space Complexity: ```O(1)```, since we are modifying the array in place and not using any extra space.
