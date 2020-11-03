---
title: Insertion Sort
parent: Sorting Algorithms
grand_parent: Algorithms
# has_children: true
nav_order: 3
---

# Insertion Sort

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