1. Determine Optimal Substructure 
2. Find overlapping subproblems
3. Find recurrence relationship 

### Knapsack Problems
- at it's core, the knapsack problem is a subset problem in that you have to enumerate all subsets and make some sort of determination about them. you might need to count the number of subsets that add to a specific number for example.  
- the most basic version of the knapsack problem is where you have a list of weights and you need to determine all the sums you can make with the weights.
- A more complex version of the knapsack problem is [Coin Change 2](https://leetcode.com/problems/coin-change-ii/description/) where you are given a list of coins and an amount and you need to return the number of ways you can add up to that amount with the given coins. you can use the same coin more than once. This is a knapsack problem because you need to enumerate all the subsets from the list of coins however in this case you can have duplicates meaning you can include a coin in a subset multiple times. the number of subsets is infinite but is bounded by the `amount`.
		- 
