# Bubble Sort

A simple comparison-based sorting algorithm in Go.

## Code

```go
package main

import "fmt"

func bubbleSort(arr []int) []int {
	n := len(arr)
	
	for i := 0; i < n; i++ {
		swapped := false
		
		for j := 0; j < n-i-1; j++ {
			if arr[j] > arr[j+1] {
				arr[j], arr[j+1] = arr[j+1], arr[j]
				swapped = true
			}
		}
		
		// If no swapping occurred, array is already sorted
		if !swapped {
			break
		}
	}
	
	return arr
}

func main() {
	nums := []int{64, 34, 25, 12, 22, 11, 90}
	fmt.Println("Original:", nums)
	fmt.Println("Sorted:", bubbleSort(nums))
}
```

## Output

```
Original: [64 34 25 12 22 11 90]
Sorted: [11 12 22 25 34 64 90]
```

## Complexity

- **Time:** O(n²) worst/average, O(n) best (already sorted)
- **Space:** O(1)
