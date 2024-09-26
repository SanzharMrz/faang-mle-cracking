# Stacks

A **stack** is a data structure that allows adding and removing elements from only one end, known as the top, following a LIFO (Last In, First Out) principle. Similar to a stack of plates, you can only push (add) or pop (remove) items from the top, not from the middle or bottom. Stacks support three main operations: push, pop, and peek.

# Operations:
## Push:
- Adds an element to the top of the stack.
- In dynamic arrays, this is equivalent to appending an element to the end of the array.
- The time complexity is O(1) because no shifting is required; the new element is added directly to the next available position.

## Pop:
- Removes the last element (top of the stack).
- This is an O(1) operation since it involves removing the last item in the dynamic array.
- It is important to check if the stack is empty before performing this operation to avoid errors.

## Peek:
- Returns the top element without removing it.
- This is also an O(1) operation since you are simply accessing the last element.


## Time Complexity:
- Push: O(1)
- Pop: O(1)
- Peek: O(1)

Stacks are commonly implemented using dynamic arrays and can be used in scenarios like reversing sequences (e.g., reversing a string).


