---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["algorithms", "dsa", "backtracking"]
domain: "Knowledge/Algorithms"
---

# Summary
Systematic generation of all search candidates. Prunes bad search paths immediately.

# Key Concepts
- **Optimal Time Complexity**: Evaluated per input constraint.
- **Space Allocation**: Memory utilization patterns.
- **Edge Cases**: Empty structures, single elements, overflow limits.

# Practical Applications
Used in optimizing nested iteration blocks down to linear or logarithmic execution times.

# Examples
```python
def backtrack(start, curr_path, res):
    res.append(list(curr_path))
    for i in range(start, len(nums)):
        curr_path.append(nums[i])
        backtrack(i + 1, curr_path, res)
        curr_path.pop()
```

# Related Notes
- [[Algorithms MOC]]
- [[Algorithms Dashboard]]

# Action Items
- [ ] Solve standard LeetCode problems: LeetCode 46, LeetCode 78.

# References
- LeetCode Patterns (Blind 75)
- Introduction to Algorithms (CLRS)
