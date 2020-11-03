---
title: Master Theorem
parent: Algorithms
# has_children: true
nav_order: 3
---

# Master Theorem
The master method is a formula for solving recurrence relations of the form:
```
T(n) = aT(n/b) + f(n),
where,
n = size of input
a = number of subproblems in the recursion
n/b = size of each subproblem. All subproblems are assumed 
     to have the same size.
f(n) = cost of the work done outside the recursive call, 
      which includes the cost of dividing the problem and
      cost of merging the solutions

Here, a ≥ 1 and b > 1 are constants, and f(n) is an asymptotically positive function.
```
Master theorem is used in calculating the time complexity of recurrence relations (divide and conquer algorithms) in a simple and quick way.

If `f(n)` is polynomially smaller than `n^log(a,b)` then `T(n) = Θ(n^log(a,b))`

If `f(n)` is asymptotically the same as `n^log(a,b)` then `T(n) = Θ(n^log(a,b) * log(n))`

If `f(n)` is polynomially larger than `n^log(a,b)` then `T(n) = Θ(f(n))` 

Example

```
Consider the recurrence
T(n) = 9*T(n/3) + n

In this case, n^log(a,b) = n^2 and f(n) = n. 
Since f(n) is polynomially smaller than n^log(a,b), master theorem implies that T(n) = Θ(n^2).
```

```
Consider the recurrence
T(n) = 27*T(n/3) + n^3

In this case, n^log(a,b) = n^3 and f(n) = n^3. 
Since f(n) is asymptotically the same as n^log(a,b), master theorem implies that T(n) = Θ(n^3 * log(n)).
```

```
Consider the recurrence
T(n) = 2*T(n/2) + n^2

In this case, n^log(a,b) = n and f(n) = n^2. 
Since f(n) is polynomially larger than n^log(a,b), master theorem implies that T(n) = Θ(f(n)) = Θ(n^2).
```

```
Consider the recurrence
T(n) = 8*T(n/2) + (n^3)/log(n)

In this case, n^log(a,b) = n^3 and f(n) = (n^3)/log(n). 
The master theorem makes no claim about the solution to the recurrence.
```