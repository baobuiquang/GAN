# Developer Handbook

## Table of Contents

### DSA - Data Structures and Algorithms

<details>
  <summary><b>
     1. Introduction
  </b></summary>
   
   - What is an algorithm?
   - Asymptotic Notations
   - Master Theorem
   - Divide and Conquer Algorithm
</details>
<details>
  <summary><b>
     2. Data Structures
  </b></summary>
   
   - Stack
   - Queue
     - Types of Queue
     - Circular Queue
     - Priority Queue
     - Deque
   - Linked List
     - Linked List Operations
     - Types of Linked List
   - Hash Table
   - Heap Data Structure
     - Fibonacci Heap
     - Decrease key and delete node from Fibonacci Heap
</details>

## What is an algorithm?
An algorithm is a set of well-defined instructions in sequence to solve a problem.

### Qualities of a good algorithm

1. Input and output should be defined precisely.
2. Each step in the algorithm should be clear and unambiguous.
3. Algorithms should be most effective among many different ways to solve a problem.
4. An algorithm shouldn't include computer code. Instead, the algorithm should be written in such a way that it can be used in different programming languages.

### Examples Of Algorithms In Programming

Write an algorithm to add two numbers entered by the user.
```
Step 1: Start
Step 2: Declare variables num1, num2 and sum. 
Step 3: Read values num1 and num2. 
Step 4: Add num1 and num2 and assign the result to sum.
        sum←num1+num2 
Step 5: Display sum 
Step 6: Stop
```

Write an algorithm to find all roots of a quadratic equation ax^2+bx+c=0
```
Step 1: Start
Step 2: Declare variables a, b, c, D, x1, x2, rp and ip;
Step 3: Calculate discriminant
         D ← b2-4ac
Step 4: If D ≥ 0
              r1 ← (-b+√D)/2a
              r2 ← (-b-√D)/2a 
              Display r1 and r2 as roots.
        Else     
              Calculate real part and imaginary part
              rp ← -b/2a
              ip ← √(-D)/2a
              Display rp+j(ip) and rp-j(ip) as roots
Step 5: Stop             
```