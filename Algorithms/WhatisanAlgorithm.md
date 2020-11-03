---
title: What is an algorithm?
parent: Algorithms
# has_children: true
nav_order: 1
---

# What is an algorithm?
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

## Why Learn Data Structures and Algorithms?
Programming is all about data structures and algorithms. Data structures are used to hold data while algorithms are used to solve the problem using that data.

Data structures and algorithms (DSA) goes through solutions to standard problems in detail and gives you an insight into how efficient it is to use each one of them. It also teaches you the science of evaluating the efficiency of an algorithm. This enables you to choose the best of various choices.

### Time is precious
Suppose, `A` and `B` are trying to solve a simple problem of finding the sum of the first 10^10 natural numbers.

Algorithm by `A`
```
N = 10^10
Initialize sum = 0
for every natural number i in range 1 to N:
    add i to sum
sum is your answer
```
Algorithm by `B`
```
N = 10^10
sum = N * (N + 1) / 2
sum is your answer
```
`A` ran his code a few minutes back but it's still not showing the output.

`B` ran his code and immediately got the result.

Two of the most valuable resources for a computer program are time and memory. The time taken by the computer to run code is:
```
Time to run code = number of instructions * time to execute each instruction
```
The number of instructions depends on the algorithm you used, and the time taken to execute each code depends on your machine and compiler.

The total number of instructions executed in `A`'s algorithm is much more than in `B`'s algorithm. `A`'s algorithm has a loop that add every natural number in range 1 to 10^10, while `B`'s algorithm just uses 1 formula to calculate the sum of first N natural numbers.

Both algorithm are true to solve the problem, but `B`'s is better than `A`'s. We cannot use `A`'s algorithm in reality.

Learn algorithm is to learn how to analyze and optimize algorithms, learn how to code like `B`, not `A`.

### Scalability
Scalability is scale plus ability, which means the quality of an algorithm/system to handle the problem of larger size.

Consider the problem of setting up a classroom of 50 students. One of the simplest solutions is to book a room, get a blackboard, a few chalks, and the problem is solved.

But what if the size of the problem increases? What if the number of students increased to 200? The solution still holds but it needs more resources. In this case, you will probably need a much larger room (probably a theater), a projector screen and a digital pen.

What if the number of students increased to 1000? The solution fails or uses a lot of resources when the size of the problem increases. This means, your solution wasn't scalable.

**What is a scalable solution then?**

Consider a site like Khanacademy, millions of students can see videos, read answers at the same time and no more resources are required. So, the solution can solve the problems of larger size under resource crunch.

If you see `A`'s solution to find the sum of first N natural numbers, it wasn't scalable. It's because it required linear growth in time with the linear growth in the size of the problem. Such algorithms are also known as **linearly scalable algorithms**.

`B`'s solution was very **scalable** and didn't require the use of any more time to solve a problem of larger size. These are known as **constant-time algorithms**.