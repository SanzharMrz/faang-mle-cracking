# 26. remove-duplicates-from-sorted-array

* link: https://leetcode.com/problems/remove-duplicates-from-sorted-array/description/
* main idea:
  * create two pointers
    * l for left one
    * r for right one
  * start comparing pairwise elements
  * if they are not equal (i.e., a new unique element is found):
    * move forward left pointer and put right element to the left one
    * move forward right pointer
  * if they equal, do nothing, move right pointer to the next element
    
* Solution
  * ```python class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        l = 1
        for r in range(1, len(nums)):
            if nums[r] != nums[r - 1]:
                nums[l] = nums[r]
                l += 1
        return l

* Time Complexity: ```O(n)```, where n is the length of the input array. We scan through the array once.
* Space Complexity: ```O(1)```, since we are modifying the array in place and not using any extra space.
