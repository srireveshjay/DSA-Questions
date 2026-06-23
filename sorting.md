# Sorting & Searching

## 1. Merge Sort
* **Difficulty:** Medium
* **Platform:** [LeetCode 912](https://leetcode.com/problems/sort-an-array/)
* **Time Complexity:** $O(n \log n)$
* **Space Complexity:** $O(n)$

### Core Concept
Divide the array into halves, recursively sort them, and merge the sorted halves.

### Implementation
```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    mid = len(arr) // 2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    return merge(left, right)
