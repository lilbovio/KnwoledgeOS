---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["algorithms", "dsa", "dfs"]
domain: "Knowledge/Algorithms"
---

# Summary
Depth-First Search explores path branches exhaustively before backtracking. Relies on system stack or manual stack.

# Key Concepts
- **Optimal Time Complexity**: Evaluated per input constraint.
- **Space Allocation**: Memory utilization patterns.
- **Edge Cases**: Empty structures, single elements, overflow limits.

# Practical Applications
Used in optimizing nested iteration blocks down to linear or logarithmic execution times.

# Examples
```python
def dfs(node, visited):
    if node in visited: return
    visited.add(node)
    for neighbor in node.neighbors:
        dfs(neighbor, visited)
```

# Related Notes
- [[Algorithms MOC]]
- [[Algorithms Dashboard]]

# Action Items
- [ ] Solve standard LeetCode problems: LeetCode 200, LeetCode 133.

# References
- LeetCode Patterns (Blind 75)
- Introduction to Algorithms (CLRS)
