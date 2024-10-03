# Static Arrays

Static arrays is data structure for statically typed languages like c++, java etc, you cant change their size when its declard

Some dynamically typed languages such as Python and JavaScript do not have static arrays to begin with.

### Time Complexity for operations in array
![image](https://github.com/user-attachments/assets/a47a5223-cc4d-493c-bcf8-2bbc406a90f4)


- For reading: Accessing an element by its index is an ```O(1)``` operation because it's mapped directly to memory.
- For traversing: Iterating through an array takes ```O(n)``` time, where n is the size of the array.
- For deleting: Removing an element from the end of the array is ```O(1)```, but deleting from the middle requires shifting elements, making it ```O(n)```.
- For inserting: Adding an element at the end is ```O(1)```, while inserting in the middle requires shifting elements, resulting in ```O(n)``` time complexity.

### STOP and Think
> Array structures (e.g. the array, or the Java ArrayList, or the C++ array and vector, etc.) require that all elements be the same size. However, array structures can contain strings, which can be different lengths (and thus different sizes in memory). How is this possible?

Because every string is stored as a pointer to a piece of memory where the actual "string" is stored. This is why each array, despite the size of the strings, homogenously. Therefore, each element has the same amount of memory allowing it to be accessed directly and efficiently (random access). What gets stored inside the array of strings is effectively just a pointer (or in C, it literally is just a pointer!) which points to some array of characters somewhere that store the actual symbols in the string
