- Used to find maximum contiguous sum sub-array
- keep track of `max_so_far` and `max_ending_here` 
- set `max_ending_here` to zero if it's negative

### Steps 
```python
def kadanes(nums):
	maxSum = nums[0]
	currSum = 0

	for n in nums:
		currSum = max(curSum, 0)
		currSum += n
		maxSum = max(maxSum, curSum)
	return maxSum
```
