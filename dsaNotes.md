
---

## Dutch Flag Algorithm

The Dutch Flag Algorithm is named after the flag of the Netherlands, which has three horizontal stripes in three different colors: red, white, and blue. Similarly, in this algorithm, we need to arrange an array containing three distinct elements, such that they are grouped in order.

### Problem Statement

Given an array with elements having three distinct values (e.g., 0, 1, 2), the task is to sort the array in a way that all 0s come first, followed by 1s, and then 2s.

### Approach

1. Initialize three pointers: `low`, `mid`, and `high`.
   - `low` points to the beginning of the array (initially 0).
   - `mid` points to the beginning of the array (initially 0).
   - `high` points to the end of the array (initially `arr.length - 1`).

2. Traverse the array until `mid` is less than `high`.
   - If `arr[mid]` is 0, swap `arr[mid]` with `arr[low]` and increment both `low` and `mid`.
   - If `arr[mid]` is 1, move to the next element by incrementing `mid`.
   - If `arr[mid]` is 2, swap `arr[mid]` with `arr[high]` and decrement `high`.

3. Repeat step 2 until `mid` is less than or equal to `high`.

### JavaScript Implementation

```javascript
function dutchFlagSort(arr) {
  let low = 0;
  let mid = 0;
  let high = arr.length - 1;

  while (mid <= high) {
    if (arr[mid] === 0) {
      // Swap arr[mid] with arr[low]
      [arr[low], arr[mid]] = [arr[mid], arr[low]];
      low++;
      mid++;
    } else if (arr[mid] === 1) {
      // Move to the next element
      mid++;
    } else {
      // Swap arr[mid] with arr[high]
      [arr[mid], arr[high]] = [arr[high], arr[mid]];
      high--;
    }
  }

  return arr;
}

// Example usage
const arr = [2, 0, 1, 1, 0, 2, 1];
console.log("Original Array:", arr);
dutchFlagSort(arr);
console.log("Sorted Array:", arr); // Output: [0, 0, 1, 1, 1, 2, 2]
```

### Example

Let's demonstrate the algorithm with an example array `[2, 0, 1, 1, 0, 2, 1]`:

1. Initial Array: `[2, 0, 1, 1, 0, 2, 1]`
2. After applying the Dutch Flag Algorithm: `[0, 0, 1, 1, 1, 2, 2]`

---

Excellent! Let's organize the information about the Kadane's Algorithm in a structured and comprehensive manner for your markdown file.

---

## Kadane's Algorithm

Kadane's Algorithm is a widely known algorithm used to efficiently find the maximum sum of a contiguous subarray within a given array.

### Problem Statement

Given an array of integers, the task is to find the maximum sum of a subarray (contiguous elements) within the array.

### Brute Force Approach

The brute force approach involves calculating the sum of all possible subarrays and finding the maximum among them. However, this approach has a time complexity of O(n^2), which can be inefficient for large arrays.

### Kadane's Algorithm Approach

Kadane's Algorithm provides an optimized solution to find the maximum sum of a subarray with a time complexity of O(n). The algorithm follows these steps:

1. Initialize a variable `currentSum`,  set to 0 initially. Also, initialize `maxSumSoFar` to negative infinity.

2. Traverse the array, and for each element:
   - Update `currentSum` by adding the current element to it.
   - If `currentSum` is greater than `maxSumSoFar`, update `maxSumSoFar` to `currentSum`.
   - If `currentSum` becomes negative, reset it to 0.

3. After traversing the array, the maximum sum of the subarray is stored in `maxSumSoFar`.

### JavaScript Implementation

```javascript
function kadanesAlgorithm(arr) {
  let maxSumSoFar = Number.NEGATIVE_INFINITY;
  let currentSum = 0;

  for (let i = 0; i < arr.length; i++) {
    currentSum += arr[i];

    if (currentSum > maxSumSoFar) {
      maxSumSoFar = currentSum;
    }

    if (currentSum < 0) {
      currentSum = 0;
    }
  }

  return maxSumSoFar;
}

// Example usage
const arr = [-2, -3, 4, -1, -2, 1, 5, -3];
const maxSum = kadanesAlgorithm(arr);
console.log("Maximum Sum of a Contiguous Subarray:", maxSum); // Output: 7
```

### Example

Let's demonstrate the algorithm with an example array `[-2, -3, 4, -1, -2, 1, 5, -3]`:

1. Initial Array: `[-2, -3, 4, -1, -2, 1, 5, -3]`
2. Maximum Sum of a Contiguous Subarray: `7` (corresponding to subarray `[4, -1, -2, 1, 5]`)

---

Feel free to modify and enhance this markdown template according to your preferences and any additional information you want to include.