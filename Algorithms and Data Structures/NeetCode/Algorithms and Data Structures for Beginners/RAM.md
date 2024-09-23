# RAM

**RAM** - stands for Random Access Memory (RAM). RAM is often just referred to as memory in PC. Its a computer component which used for storing data, data structures in context of programming.

Most computers these days have gigabytes (GBs) of RAM. Most of modern computers have 8 GB (10**9 bytes) of RAM. A byte of RAM is made up of exactly 8 bits.

Going back to our integers, each of ```[1, 3, 5]``` has a binary representation, meaning they can be represented as ```0s``` and ```1s```. If we use a single byte to store each, then the integer ```1``` can be represented as ```00000001```, ```3``` as ```00000011```, and ```5``` as ```00000101```.

When we store an array in RAM, each element is stored continously in order.

Integers commonly occupy 4 bytes (32 bits) in memory. An ```address``` and a ```value``` gets associated with an integer upon storing it in RAM. An address is just a distinct location that each one of the values is stored at. Each value is stored contiguously in the RAM, just like an array.

![image](https://github.com/user-attachments/assets/44b54008-8fd4-48d9-9dc1-d84cc3d456ac)

> Each integer occupies 4 bytes of space, hence the addresses are 4 bytes apart.

Instead of integers, we could also store characters in an array.

![image](https://github.com/user-attachments/assets/43ce4839-57a6-41bb-87ac-6d4f69692d8f)

> Each character occupies 1 byte of space, hence the addresses are 1 byte apart.
