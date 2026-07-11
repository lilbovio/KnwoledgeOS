---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["algorithms", "dsa", "topological-sort"]
domain: "Knowledge/Algorithms"
---

# Summary
Ordering vertices in Directed Acyclic Graphs (DAG) such that for edge $u \to v$, $u$ appears before $v$.

# Key Concepts
- **Optimal Time Complexity**: Evaluated per input constraint.
- **Space Allocation**: Memory utilization patterns.
- **Edge Cases**: Empty structures, single elements, overflow limits.

# Practical Applications
Used in optimizing nested iteration blocks down to linear or logarithmic execution times.

# Examples
```python
# Kahn's algorithm using In-degree array and Queue
from collections import deque
def findOrder(numCourses, prerequisites):
    indegree = [0] * numCourses
    # ... build graph and update indegrees
    queue = deque([i for i, val in enumerate(indegree) if val == 0])
    # ... process queue to find topological order

```

# Related Notes
- [[Algorithms MOC]]
- [[Algorithms Dashboard]]

# Action Items
- [ ] Solve standard LeetCode problems: LeetCode 210.

# References
- LeetCode Patterns (Blind 75)
- Introduction to Algorithms (CLRS)
