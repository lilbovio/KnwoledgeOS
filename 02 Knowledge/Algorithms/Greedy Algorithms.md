---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["algorithms", "dsa", "greedy-algorithms"]
domain: "Knowledge/Algorithms"
---

# Summary
Making locally optimal choices at each step, hoping it resolves to a globally optimal solution.

# Key Concepts
- **Optimal Time Complexity**: Evaluated per input constraint.
- **Space Allocation**: Memory utilization patterns.
- **Edge Cases**: Empty structures, single elements, overflow limits.

# Practical Applications
Used in optimizing nested iteration blocks down to linear or logarithmic execution times.

# Examples
```python
def canJump(nums):
    max_reach = 0
    for i, n in enumerate(nums):
        if i > max_reach: return False
        max_reach = max(max_reach, i + n)
    return True
```

# Related Notes
- [[Algorithms MOC]]
- [[Algorithms Dashboard]]

# Action Items
- [ ] Solve standard LeetCode problems: LeetCode 55, LeetCode 45.

# References
- LeetCode Patterns (Blind 75)
- Introduction to Algorithms (CLRS)
