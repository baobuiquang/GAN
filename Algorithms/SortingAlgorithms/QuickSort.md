---
title: Quick Sort
parent: Sorting Algorithms
grand_parent: Algorithms
# has_children: true
nav_order: 5
---

# Quick Sort

``` cpp
int partition(int arr[], int left, int right) {
    
    // 1. Select pivot
    int pivot = arr[left];
    int pos = left;

    // 2. For loop: Put all smaller on the left and greater on the right
    for (int i = left + 1; i <= right; i++) {
        if (arr[i] < pivot) {
            pos++;
            swap(arr[i], arr[pos]);
        }
    }

    // 3. Swap pivot with the "last left"
    swap(arr[left], arr[pos]);
    return pos;
}

void quickSort(int arr[], int left, int right) {
    // Exit Recursion Condition
    if (left < right) {

        // Select pivot (pos is position of pivot)
        // Put all smaller on the left and greater on the right
        int pos = partition(arr, left, right);

        // Recursion
        quickSort(arr, left, pos - 1);
        quickSort(arr, pos + 1, right);
    }
}
```

Complexity: `O(n^2)`

![](assets/Quick.gif)

Reversed Sorted

![](assets/Quick1.gif)

Sorted

![](assets/Quick2.gif)