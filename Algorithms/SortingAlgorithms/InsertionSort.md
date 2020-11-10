---
title: Insertion Sort
parent: Sorting Algorithms
grand_parent: Algorithms
# has_children: true
nav_order: 2
---

# Insertion Sort

``` cpp
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

![](assets/Insertion.gif)

Reversed Sorted - Worst Case - `O(n^2)`

![](assets/Insertion1.gif)

Sorted - Best Case - `O(n)`

![](assets/Insertion2.gif)