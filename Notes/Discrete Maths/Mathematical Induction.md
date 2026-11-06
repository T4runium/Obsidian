Proves a statement $P(n)$ for every integer $n \geq n_0$

**Principle:** if
1. **Base case:** $P(n_0)$ is true
2. **Inductive step:** for any $n \geq n_0$, $P(n) \implies P(n + 1)$

then $P(n)$ is true for all $n \geq n_0$, since $P(n_0) \to P(n_0+1) \to P(n_0+2) \to \dots$

Assuming $P(n)$ in the step is the **inductive hypothesis**
Used to prove closed forms guessed from [[Recurrence Relations]]; same shape as [[Recursion]] (base case + smaller case)

# Example 1
$2^n > 2n$ for $n \geq 3$
Base: $2^3 = 8 > 6$ ✓
Step: assume $2^n > 2n$
$$
\begin{aligned}
2^{n+1} &= 2 \cdot 2^n \\
&> 2 \cdot 2n && \text{(hypothesis)} \\
&> 2(n + 1) && \text{(since } 2n > n + 1 \text{ for } n \geq 3) \\
&\therefore P(n+1)
\end{aligned}
$$

# Example 2
For integers $n, m \geq 0$:
$$
\sum_{k=0}^{n} {}^{m+k}C_{k} = {}^{m+n+1}C_{n}
$$
Fix $m$, induct on $n$
Base $n = 0$: ${}^{m}C_{0} = 1 = {}^{m+1}C_{0}$ ✓
Step: assume true for $n$
$$
\begin{aligned}
\sum_{k=0}^{n+1} {}^{m+k}C_{k} &= \sum_{k=0}^{n} {}^{m+k}C_{k} + {}^{m+n+1}C_{n+1} \\
&= {}^{m+n+1}C_{n} + {}^{m+n+1}C_{n+1} && \text{(hypothesis)} \\
&= {}^{m+n+2}C_{n+1} && \text{(Pascal's formula)} \\
&\therefore P(n+1)
\end{aligned}
$$

using [[Combinations#Pascal's formula|Pascal's formula]]

# Try
$\sum_{k=0}^{n} {}^{k}C_{m} = {}^{n+1}C_{m+1}$ for $n, m \geq 0$
