**Open addressing** [[Collision Handling]] method

Try $A[(i + j^2) \bmod N]$ for $j = 0, 1, 2, \dots$ (where $i = h(k)$) until an empty bucket is found
- avoids the clustering of [[Linear Probing]], but keys with the same $h(k)$ still follow the same probe sequence, giving **secondary clustering**
- may **not find an empty bucket even if one exists**

# Example
$N = 7$, $h(k) = k \bmod 7$, insert $10, 17, 24$ (all hash to $3$)
$$
\begin{aligned}
10 &\to 3 \\
17 &\to 3 \text{ (taken)} \to 3 + 1 = 4 \\
24 &\to 3, 4 \text{ (taken)} \to (3 + 4) \bmod 7 = 0
\end{aligned}
$$
