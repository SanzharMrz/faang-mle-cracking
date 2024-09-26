# 1929. Concatenation of Array

* link: [https://leetcode.com/problems/remove-duplicates-from-sorted-array/description/](https://leetcode.com/problems/concatenation-of-array/description/)
* main idea:
  * create another array and put your values into it
  * or just multiply it to given value
  * or just extend
    
* Solution
  * ```python
      def getConcatenation(self, nums: List[int]) -> List[int]:
        return nums * 2
        

* Time complexity: ```O(n)```, regardless of whether it's ```nums * 2```, ```nums * 3```, or ```nums * 4```.
* Space complexity: ```O(n)```, with the same rationale.
