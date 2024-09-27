# 20. Valid Parentheses

* link: https://leetcode.com/problems/valid-parentheses/description/
* main idea:
  * create mapping of brances from close to open
  * create empty stack (dynamic array)
  * start iterating through sequence
  * if element is not closing one, so we could add it to the stack and continue iteration
  * if element is closing and not equal to his opening pair, or stack is already empty
    * so return false, sequence if broken
  * else just pop element
  * if stack is empty so everything is perfect return True
    
* Solution
  * ```python
    braces = {')':'(', ']':'[', '}':'{'}
    
    class Solution:
      def isValid(self, s: str) -> bool:
          stack = []
  
          for char in s:
              if char not in braces:
                  stack.append(char)
                  continue
              
              if not stack or stack[-1] != braces[char]:
                  return False
  
              stack.pop()
          return not stack


        

* Time complexity: ```O(n)```, regardless of whether it's ```nums * 2```, ```nums * 3```, or ```nums * 4```.
* Space complexity: ```O(n)```, with the same rationale.
