# Dynamic Arrays

**Dynamic arrays**, unlike **static arrays**, can grow in size as needed, making them more flexible. They are the default array types in languages like Python and JavaScript and do not require specifying a size upon initialization. Dynamic arrays expand by automatically resizing at runtime when their capacity is exceeded.

## Key Operations:
- **Insertion:** When an element is inserted and there’s enough space, it’s placed at the next available index in O(1) time. However, when the array is full, it resizes by doubling its capacity. This resizing involves copying the old array into a new larger one, making the resize operation O(n), but since resizing occurs infrequently, the amortized time complexity for insertion is O(1).

- **Resizing:** Resizing occurs when the array's capacity is exceeded. The array doubles in size and its elements are copied over to the new larger array. Although resizing takes O(n) time, it is infrequent enough that the average time per insertion remains O(1).

- **Doubling Capacity:** Dynamic arrays typically double their size to minimize the frequency of resizing. For example, an array of size 1 doubles to 2, then 4, 8, and so on. Creating a large array requires a sequence of operations that grows linearly with the size, leading to O(n) overall time complexity for n insertions.

- **Other Operations:** Inserting or deleting in the middle of the array requires shifting elements to maintain order, resulting in O(n) time complexity for these operations.

## Time Complexity Summary:
- Access: O(1)
- Insertion: O(n) if in the middle or any arbitrary place, O(1) amortized in the end or array if it is not full
- Deletion: O(n) if in the middle or any arbitrary place, O(1) amortized in the end or array if it is not full
