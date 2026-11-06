**Open addressing** [[Collision Handling]] method

Use a **secondary hash function** $h'$ for the step size: try $A[(i + j \cdot h'(k)) \bmod N]$ for $j = 0, 1, 2, \dots$ (where $i = h(k)$)
- common choice: $h'(k) = q - (k \bmod q)$ for some prime $q < N$
- $h'(k)$ must **never be $0$**, or we'd probe the same bucket forever

# Example
$N = 7$, $h(k) = k \bmod 7$, $q = 5$, insert $10, 17, 24$ (all hash to $3$)
$$
\begin{aligned}
10 &\to 3 \\
17 &: h'(17) = 5 - 2 = 3, \quad 3 \text{ (taken)} \to 3 + 3 = 6 \\
24 &: h'(24) = 5 - 4 = 1, \quad 3 \text{ (taken)} \to 3 + 1 = 4
\end{aligned}
$$
Keys colliding at the same bucket now take **different** paths
