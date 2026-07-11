---
created: 2026-06-23
updated: 2026-06-23
status: "Seed"
tags: ["algorithms", "dsa", "fast-&-slow-pointers"]
domain: "Knowledge/Algorithms"
---

# Summary
Also known as Floyd's cycle detection. Pointers move at different speeds (usually 1 step and 2 steps).

# Key Concepts
- **Optimal Time Complexity**: Evaluated per input constraint.
- **Space Allocation**: Memory utilization patterns.
- **Edge Cases**: Empty structures, single elements, overflow limits.

# Practical Applications
Used in optimizing nested iteration blocks down to linear or logarithmic execution times.

# Examples
```java
public boolean hasCycle(ListNode head) {
    ListNode slow = head, fast = head;
    while (fast != null && fast.next != null) {
        slow = slow.next;
        fast = fast.next.next;
        if (slow == fast) return true;
    }
    return false;
}
```

# Related Notes
- [[Algorithms MOC]]
- [[Algorithms Dashboard]]

# Action Items
- [ ] Solve standard LeetCode problems: LeetCode 141, LeetCode 287.

# References
- LeetCode Patterns (Blind 75)
- Introduction to Algorithms (CLRS)
