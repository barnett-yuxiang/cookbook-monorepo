# Bubble Sort

A simple comparison-based sorting algorithm.

## Code

```python
def bubble_sort(arr):
    """
    Bubble Sort - O(n²) time complexity
    Repeatedly swaps adjacent elements if they are in wrong order.
    """
    n = len(arr)
    
    for i in range(n):
        swapped = False
        
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
                swapped = True
        
        # If no swapping occurred, array is already sorted
        if not swapped:
            break
    
    return arr


# Example
if __name__ == "__main__":
    nums = [64, 34, 25, 12, 22, 11, 90]
    print("Original:", nums)
    print("Sorted:", bubble_sort(nums))
```

## Output

```
Original: [64, 34, 25, 12, 22, 11, 90]
Sorted: [11, 12, 22, 25, 34, 64, 90]
```

## Complexity

- **Time:** O(n²) worst/average, O(n) best (already sorted)
- **Space:** O(1)
