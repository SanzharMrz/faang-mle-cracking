# Big-{something} notations

There are three main notations to describe time complexity: Big-O ("Big-Oh"), Big-Ω ("Big-Omega"), and Big-ϴ ("Big-Theta"). 

- Big-O notation provides an upper-bound on the number of operations performed,
- Big-Ω provides a lower-bound, and Big-ϴ provides both an upper-bound and a lower-bound. In other words, 
- Big-ϴ implies both Big-O and Big-Ω.

For our purposes, we will only consider Big-O notation because, in general, we only care about upper-bounds on our algorithms.

![image](https://github.com/user-attachments/assets/69480617-7814-4dec-bec4-c6af8289d003)

* "Constant Time" = O(1)
* "Logarithmic Time" = "Scales/Increases Logarithmically" = O(log n)
* "Polynomial Time" = "Scales/Increases Polynomially" = O(nk) (for any constant k)
* "Exponential Time" = "Scales/Increases Exponentially" = O(kⁿ) (for any constant k)
* "Factorial Time" = O(n!)
  
![image](https://github.com/user-attachments/assets/41c4bb9c-a5f4-4c7c-9bd6-082296784475)

# Problem Complexity
![image](https://github.com/user-attachments/assets/663e6d80-c538-4463-83dc-fc5ecb1b3753)

### 1. **P (Polynomial Time)**:  
Problems that can be solved quickly by a computer (in a reasonable amount of time as the input gets bigger).  
- **Example**: Sorting a list of numbers.

### 2. **NP (Nondeterministic Polynomial Time)**:  
Problems where, if someone gives you a solution, you can check if it’s right quickly, but you might not know how to find the solution quickly yourself.  
- **Example**: Solving a puzzle — hard to solve, but easy to check if someone hands you the answer.

### 3. **NP-hard**:  
Problems that are at least as hard as the hardest problems in NP. Solving these would mean solving all NP problems, but they might be even tougher.  
- **Example**: Finding the best route between cities (traveling salesman problem).

### 4. **NP-complete**:  
The hardest problems in NP. If you could solve any one of these quickly, you could solve every problem in NP quickly.  
- **Example**: Figuring out if a puzzle has a solution (satisfiability problem).

### 5. **P vs NP**:  
The big question: Can every problem that can be **checked quickly** also be **solved quickly**? We don’t know yet!

In simple terms:
- **P**: Problems you can solve fast.
- **NP**: Problems you can check fast but may be slow to solve.
- **NP-hard**: Even harder problems.
- **NP-complete**: The hardest problems in NP.

