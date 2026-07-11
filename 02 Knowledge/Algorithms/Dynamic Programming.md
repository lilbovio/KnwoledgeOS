---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["algorithms", "dsa", "dynamic-programming"]
domain: "Knowledge/Algorithms"
---

# Summary
Solving complex problems by breaking them into overlapping subproblems, saving subproblem results (memoization/tabulation).

# Key Concepts
- **Optimal Time Complexity**: Evaluated per input constraint.
- **Space Allocation**: Memory utilization patterns.
- **Edge Cases**: Empty structures, single elements, overflow limits.

# Practical Applications
Used in optimizing nested iteration blocks down to linear or logarithmic execution times.

# Examples
```python
def coinChange(coins, amount):
    dp = [amount + 1] * (amount + 1)
    dp[0] = 0
    for i in range(1, amount + 1):
        for c in coins:
            if i - c >= 0:
                dp[i] = min(dp[i], dp[i-c] + 1)
    return dp[amount] if dp[amount] != amount + 1 else -1
```

# Related Notes
- [[Algorithms MOC]]
- [[Algorithms Dashboard]]

# Action Items
- [ ] Solve standard LeetCode problems: LeetCode 70, LeetCode 322.

# References
- LeetCode Patterns (Blind 75)
- Introduction to Algorithms (CLRS)
