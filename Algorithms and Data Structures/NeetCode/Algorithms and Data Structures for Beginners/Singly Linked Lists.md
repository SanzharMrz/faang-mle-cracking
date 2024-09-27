# Singly Linked Lists

A **singly linked list** is a data structure that stores elements in a sequential order, but unlike arrays, its elements (called **nodes**) are not stored contiguously in memory. Each node contains two components:
- **Value**: The data the node holds (e.g., an integer or a string).
- **Next**: A reference (or pointer) to the next node in the list.

![image](https://github.com/user-attachments/assets/3bd66209-f9a4-4597-b430-3c0b726c9716)


### Key Concepts:

1. **ListNode**:
   - A node in a singly linked list is represented by a `ListNode` class that stores a value and a pointer to the next node. The last node points to `null` (or `None` in Python) to signify the end of the list.

2. **Traversal**:
   - To traverse a singly linked list, you start at the **head** (the first node) and follow the `next` pointers from one node to the next until you reach the end (when `next` is `null`).
   - Traversal takes **O(n)** time, where **n** is the number of nodes in the list.
![image](https://github.com/user-attachments/assets/2bba03cc-c741-42f1-a250-9da1add3c182)

3. **Circular Linked List**:
   - If a node's `next` pointer refers back to a previous node (e.g., if the last node points back to the first node), it forms a **circular linked list**. This could cause infinite loops during traversal.
![image](https://github.com/user-attachments/assets/db79ba16-335b-4500-9001-ab9d870571df)

### Operations:

1. **Appending (Insertion)**:
   - Adding a new node to the end of the list can be done in **O(1)** time if you have a reference to the **tail** (the last node). You simply update the tail’s `next` pointer to point to the new node, then update the tail reference itself.
   - However, if you need to traverse the list to find the position (e.g., to append in the middle), the operation takes **O(n)** time because you must traverse the list to find the insertion point.

2. **Deleting**:
   - Deleting a node from a singly linked list is also an **O(1)** operation if you have a reference to the node you want to delete. For example, if you want to delete a node from the middle of the list, you can skip the node by updating the previous node's `next` pointer to point to the node after the one being deleted.
   - As with insertion, if you need to search for the node to delete, the time complexity becomes **O(n)** due to the traversal.
![image](https://github.com/user-attachments/assets/4749ebe3-2003-4eb4-b8b1-92cf6f55e493)

3. **Access and Search**:
   - Both accessing an element by index and searching for a particular value in a singly linked list take **O(n)** time because you must traverse the list node by node.

### Example:

Here's a simple Python class for a singly linked list node:

```python
class ListNode:
    def __init__(self, val):
        self.val = val
        self.next = None
```

### Traversing a Linked List:

```python
# Assume head is the first node of the linked list
cur = head
while cur:
    print(cur.val)  # Process the current node
    cur = cur.next  # Move to the next node
```

### Appending a New Node:

```python
# Appending ListNode4 to the end of the list
tail.next = ListNode4  # The current tail points to the new node
tail = ListNode4  # Update tail to the new last node
```

### Deleting a Node:

```python
# Deleting ListNode2, assuming head is ListNode1
head.next = head.next.next  # ListNode1's next now points to ListNode3
```

### Time Complexity Summary:

| Operation | Time Complexity | Notes |
| --------- | --------------- | ----- |
| Access    | O(n)            | Must traverse the list |
| Search    | O(n)            | Linear search through nodes |
| Insertion | O(1)            | If you have a reference to the node |
| Deletion  | O(1)            | If you have a reference to the node |

In summary, linked lists offer flexible memory management and efficient insertions/deletions, but accessing or searching for nodes requires linear time due to the need to traverse the list node by node.
