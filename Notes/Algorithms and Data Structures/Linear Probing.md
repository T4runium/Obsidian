**Open addressing** [[Collision Handling]] method

If $A[i]$ is taken (where $i = h(k)$), try $A[(i+1) \bmod N]$, then $A[(i+2) \bmod N]$, ... until an empty bucket is found
- each bucket we look at is a **probe**

**Performance**:
- insert/search cost depends on the length of the **cluster** (run of full buckets)
- if a $(1 - 1/x)$ fraction of the table is full ($x \ge 2$), average cluster length $\propto x^2$
- Worst case: all keys hash into the same cluster

# Example
$N = 7$, $h(k) = k \bmod 7$, insert $10, 17, 24$ (all hash to $3$)
$$
\begin{aligned}
10 &\to 3 \\
17 &\to 3 \text{ (taken)} \to 4 \\
24 &\to 3, 4 \text{ (taken)} \to 5
\end{aligned}
$$
Keys pile up next to each other, which is **primary clustering**

Compare: [[Quadratic Probing#Example|quadratic]], [[Double Hashing#Example|double hashing]]
