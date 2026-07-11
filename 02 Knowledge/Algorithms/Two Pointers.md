---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["algorithms", "dsa", "two-pointers"]
domain: "Knowledge/Algorithms"
---

# Summary
Using two references to scan data linearly from opposite ends or different speeds to solve arrays/strings problems.

# Key Concepts
- **Optimal Time Complexity**: Evaluated per input constraint.
- **Space Allocation**: Memory utilization patterns.
- **Edge Cases**: Empty structures, single elements, overflow limits.

# Practical Applications
Used in optimizing nested iteration blocks down to linear or logarithmic execution times.

# Examples
```python
def twoSum(nums, target):
    left, right = 0, len(nums) - 1
    while left < right:
        curr = nums[left] + nums[right]
        if curr == target: return [left, right]
        elif curr < target: left += 1
        else: right -= 1
    return []
```

# Related Notes
- [[Algorithms MOC]]
- [[Algorithms Dashboard]]

# Action Items
- [ ] Solve standard LeetCode problems: LeetCode 125, LeetCode 15.

# References
- LeetCode Patterns (Blind 75)
- Introduction to Algorithms (CLRS)
