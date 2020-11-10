---
title: Merge Sort
parent: Sorting Algorithms
grand_parent: Algorithms
# has_children: true
nav_order: 4
---

# Merge Sort

```
void merge(int arr[], int left, int mid, int right) {
	// Create 2 temporary subarray
	int n1 = mid - left + 1;
	int n2 = right - mid;
	int* L = new int[n1];
	int* R = new int[n2];
	for (int i = 0; i < n1; i++)
		L[i] = arr[left + i];
	for (int j = 0; j < n2; j++)
		R[j] = arr[mid + 1 + j];

	// Maintain indexes: L, R and merged subarray (in main array)
	int i = 0;
	int j = 0;
	int k = left;

	// Until reaching the end of either L or R, pick the smaller element
	while (i < n1 && j < n2) {
		if (L[i] <= R[j]) {
			arr[k] = L[i];
			i++;
		}
		else {
			arr[k] = R[j];
			j++;
		}
		k++;
	}

	// When run out of elements in either L or M, pick up the remaining elements
	while (i < n1) {
		arr[k] = L[i];
		i++;
		k++;
	}
	while (j < n2) {
		arr[k] = R[j];
		j++;
		k++;
	}

	// Delete dynamic memories
	delete[] L;
	delete[] R;
}

void mergeSort(int arr[], int left, int right) {
	// Recursion Condition
	if (left < right) {
		// Find mid position
		int mid = left + (right - left) / 2;

		// Sort 2 subarray 
		mergeSort(arr, left, mid);
		mergeSort(arr, mid + 1, right);

		// Merge 2 subarray
		merge(arr, left, mid, right);
	}
}

// Print the array 
void printArray(int A[], int size)
{
	for (int i = 0; i < size; i++)
		cout << A[i] << " ";
}

// Main
int main()
{
	int arr[] = { 10, 5, 20, 1, 4, 54 };
	int arr_size = sizeof(arr) / sizeof(arr[0]);

	cout << "Array:\n";
	printArray(arr, arr_size);

	mergeSort(arr, 0, arr_size - 1);

	cout << "\nSorted array:\n";
	printArray(arr, arr_size);
	return 0;
}
```

![](assets/Merge.gif)

Reversed Sorted

![](assets/Merge1.gif)

Sorted

![](assets/Merge2.gif)

### Implementation

#### Step 1
```
// Merge 2 subarrays
void merge(int arr[], int left, int mid, int right) {
}

// Divide array into 2 subarrays -> call mergeSort -> call merge
void mergeSort(int arr[], int left, int right) {
}
```

#### Step 2
```
void mergeSort(int arr[], int left, int right) {

  // Recursion Condition
	if (left < right) {

    // Find mid position
		int mid = left + (right - left) / 2;

    // Sort 2 subarray 
		mergeSort(arr, left, mid);
		mergeSort(arr, mid + 1, right);

    // Merge 2 subarray
		merge(arr, left, mid, right);

	}
}
```

#### Step 3
```
void merge(int arr[], int left, int mid, int right) {

  // Create 2 temporary subarray
	int n1 = mid - left + 1;
	int n2 = right - mid;
	int* L = new int[n1];
	int* R = new int[n2];
	for (int i = 0; i < n1; i++)
		L[i] = arr[left + i];
	for (int j = 0; j < n2; j++)
		R[j] = arr[mid + 1 + j];

  // ...

  // Delete dynamic memories
	delete[] L;
	delete[] R;

}
```

#### Step 4
```
void merge(int arr[], int left, int mid, int right) {

  // Create 2 temporary subarray
	// ...

  // Maintain indexes: L, R and merged subarray (in main array)
	int i = 0;
	int j = 0;
	int k = left;

  // Until reaching the end of either L or R, pick the smaller element
	while (i < n1 && j < n2) {
		if (L[i] <= R[j]) {
			arr[k] = L[i];
			i++;
		}
		else {
			arr[k] = R[j];
			j++;
		}
		k++;
	}

	// When run out of elements in either L or M, pick up the remaining elements
	while (i < n1) {
		arr[k] = L[i];
		i++;
		k++;
	}
	while (j < n2) {
		arr[k] = R[j];
		j++;
		k++;
	}

  // Delete dynamic memories
	// ...

}
```