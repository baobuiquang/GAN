# Developer Handbook

This handbook has been compiled by me from many different sources, with the purpose of making it convenient and easy to find and look up frequently used programming knowledge. This is only used for learning purposes.

## Table of Contents

### DSA - Data Structures and Algorithms

1. Introduction
   - [What is an algorithm?](#What-is-an-algorithm?)
   - [Why Learn Data Structures and Algorithms?](#Why-Learn-Data-Structures-and-Algorithms?)
   - [Asymptotic Notations](#Asymptotic-Notations)
   - [Master Theorem](#Master-Theorem)
2. Data Structures
   - Stack
3. Sorting Algorithm
   - [Bubble Sort O(n^2)](#bubble-sort)
   - [Selection Sort O(n^2)](#selection-sort)
   - [Insertion Sort O(n^2)](#insertion-sort)
   - [Merge Sort O(n*logn)](#merge-sort)
   - [Quick Sort O(n^2)](#quick-sort)

________________________

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

## Asymptotic Notations
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

## Master Theorem
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

If `f(n)` is polynomially smaller than `n^log(b,a)` then `T(n) = Θ(n^log(b,a))`

If `f(n)` is asymptotically the same as `n^log(b,a)` then `T(n) = Θ(n^log(b,a) * log(n))`

If `f(n)` is polynomially larger than `n^log(b,a)` then `T(n) = Θ(f(n))` 

Example

```
Consider the recurrence
T(n) = 9*T(n/3) + n

In this case, n^log(b,a) = n^2 and f(n) = n. 
Since f(n) is polynomially smaller than n^log(b,a), master theorem implies that T(n) = Θ(n^2).
```

```
Consider the recurrence
T(n) = 27*T(n/3) + n^3

In this case, n^log(b,a) = n^3 and f(n) = n^3. 
Since f(n) is asymptotically the same as n^log(b,a), master theorem implies that T(n) = Θ(n^3 * log(n)).
```

```
Consider the recurrence
T(n) = 2*T(n/2) + n^2

In this case, n^log(b,a) = n and f(n) = n^2. 
Since f(n) is polynomially larger than n^log(b,a), master theorem implies that T(n) = Θ(f(n)) = Θ(n^2).
```

```
Consider the recurrence
T(n) = 8*T(n/2) + (n^3)/log(n)

In this case, n^log(b,a) = n^3 and f(n) = (n^3)/log(n). 
The master theorem makes no claim about the solution to the recurrence.
```

## Bubble Sort

```
for i = N - 1 to 1
  swapped = false
  for j = 0 to (i - 1)
    if a[j] > a[j + 1]
      swap(a[j], a[j + 1])
      swapped = true
  if swapped == false
    break
```

Number of comparisons: `(n - 1) + (n - 2) + (n - 3) +.....+ 1 = n(n - 1) / 2`

Complexity: `O(n^2)`

```
a[j] and a[j + 1] = 2 green bars
```

![](/assets/Sorting/Bubble.gif)

Reversed Sorted - Worst Case - `O(n^2)`

![](/assets/Sorting/Bubble1.gif)

Sorted - Best Case - `O(n)`

![](/assets/Sorting/Bubble2.gif)

## Selection Sort

```
for i = 0 to (N - 2)
  minimum = a[i]
  for j = i + 1 to (N - 1)
    if a[j] < minimum
      minimum = a[j]
  swap(minimum, a[i])
```

Number of comparisons: `(n - 1) + (n - 2) + (n - 3) +.....+ 1 = n(n - 1) / 2`

Complexity: `O(n^2)`

```
a[i] = first unsorted element
minimum = red bar
```

![](/assets/Sorting/Selection.gif)

Reversed Sorted - Worst Case - `O(n^2)`

![](/assets/Sorting/Selection1.gif)

Sorted - Best Case - `O(n^2)`

![](/assets/Sorting/Selection2.gif)

## Insertion Sort

```
for i = 1 to (N-1)
  key = a[i]
  j = i - 1
  while (j >= 0 and key < a[j])
    a[j + 1] = a[j]
    j--
  a[j + 1] = key
```

Complexity: `O(n^2)`

```
key = red bar
a[j] = green bar
a[j+1] = the gap
```

![](/assets/Sorting/Insertion.gif)

Reversed Sorted - Worst Case - `O(n^2)`

![](/assets/Sorting/Insertion1.gif)

Sorted - Best Case - `O(n)`

![](/assets/Sorting/Insertion2.gif)

## Merge Sort

```
void merge(int arr[], int left, int mid, int right) {
  // Create 2 sub-arrays
  int n1 = mid - left + 1;
  int n2 = right - mid;
  int* L = new int[n1];
  int* M = new int[n2];
  for (int i = 0; i < n1; i++)
    L[i] = arr[left + i];
  for (int j = 0; j < n2; j++)
    M[j] = arr[mid + 1 + j];

  // Maintain current index of sub-arrays and main array
  int i, j, k;
  i = 0;
  j = 0;
  k = left;

  // Until we reach either end of either L or M, pick larger among elements L and M
  while (i < n1 && j < n2) {
    if (L[i] <= M[j]) {
      arr[k] = L[i];
      i++;
    } else {
      arr[k] = M[j];
      j++;
    }
    k++;
  }

  // When we run out of elements in either L or M, pick up the remaining elements
  while (i < n1) {
    arr[k] = L[i];
    i++;
    k++;
  }
  while (j < n2) {
    arr[k] = M[j];
    j++;
    k++;
  }

  delete[] L;
  delete[] M;
}

void mergeSort(int arr[], int left, int right) {
  if (left < right) {
    int mid = left + (right - left) / 2;
    mergeSort(arr, left, mid);
    mergeSort(arr, mid + 1, right);
    merge(arr, left, mid, right);
  }
}
```

Complexity: `O(n*logn)`

![](/assets/Sorting/Merge.gif)

Reversed Sorted

![](/assets/Sorting/Merge1.gif)

Sorted

![](/assets/Sorting/Merge2.gif)

## Quick Sort

```
int partition(int array[], int left, int right) {
  // Select the pivot element
  int pivot = array[right];
  int i = (left - 1);

  // Put the elements smaller than pivot on the left 
  // and greater than pivot on the right of pivot
  for (int j = left; j < right; j++) {
    if (array[j] <= pivot) {
      i++;
      swap(&array[i], &array[j]);
    }
  }
  swap(&array[i + 1], &array[right]);
  return (i + 1);
}

void quickSort(int array[], int left, int right) {
  if (left < right) {
    // Select pivot position and put all the elements smaller 
    // than pivot on left and greater than pivot on right
    int pi = partition(array, left, right);

    quickSort(array, left, pi - 1);
    quickSort(array, pi + 1, right);
  }
}
```

Complexity: `O(n^2)`

![](/assets/Sorting/Quick.gif)

Reversed Sorted

![](/assets/Sorting/Quick1.gif)

Sorted

![](/assets/Sorting/Quick2.gif)