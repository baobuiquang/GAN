---
title: Asymptotic Notations
parent: Algorithms
# has_children: true
nav_order: 2
---

# Asymptotic Notations
The efficiency of an algorithm depends on the amount of time, storage and other resources required to execute the algorithm. The efficiency is measured with the help of asymptotic notations.

Asymptotic notations are the mathematical notations used to describe the running time of an algorithm when the input tends towards a particular value or a limiting value. 

An algorithm may not have the same performance for different types of inputs. With the increase in the input size, the performance will change.

For example: In bubble sort, when the input array is already sorted, the time taken by the algorithm is linear i.e. the best case. But, when the input array is in reverse condition, the algorithm takes the maximum time (quadratic) to sort the elements i.e. the worst case. When the input array is neither sorted nor in reverse order, then it takes average time. These durations are denoted using asymptotic notations.

There are mainly three asymptotic notations: Theta notation, Omega notation and Big-O notation. However, we will concern more about the Big-O notation.

### Big-O Notation (O-notation)
Big-O notation represents the upper bound of the running time of an algorithm. Thus, it gives the **worst case** complexity of an algorithm.

Since it gives the worst case running time of an algorithm, it is widely used to analyze an algorithm as we are always interested in the worst case scenario.

You can read more about Big-O Notation here: https://wikipedia.org/wiki/Big_O_notation (It may be hard to understand. If you are a beginner, you just need to know that Big-O Notation is used to represent an algorithm in the worst input case.)

### Theta Notation (Θ-notation)
Theta notation encloses the function from above and below. Since it represents the upper and the lower bound of the running time of an algorithm, it is used for analyzing the **average case** complexity of an algorithm.

### Omega Notation (Ω-notation)
Omega notation represents the lower bound of the running time of an algorithm. Thus, it provides **best case** complexity of an algorithm.