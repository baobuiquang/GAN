---
title: Bubble Sort
parent: Sorting Algorithms
grand_parent: Algorithms
# has_children: true
nav_order: 1
---

# Bubble Sort

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

![](/Algorithms/SortingAlgorithms/assets/Bubble1.gif)

Reversed Sorted - Worst Case - `O(n^2)`

![](/assets/Sorting/Bubble1.gif)

Sorted - Best Case - `O(n)`

![](/assets/Sorting/Bubble2.gif)