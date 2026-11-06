For any $\alpha \in \mathbb{R}$, ${}^{\alpha}C_{k}$ is the coefficient of $x^k$ in the power series of $(1 + x)^\alpha$:
$$
(1 + x)^\alpha = \sum_{k = 0}^{\infty} {}^{\alpha}C_{k}\, x^k
$$
**Maclaurin's theorem** (used without proof):
$$
{}^{\alpha}C_{k} = \frac{\alpha(\alpha - 1)\cdots(\alpha - k + 1)}{k!}
$$
- $\alpha$ a positive integer, $k \leq \alpha$: the normal [[Combinations|n choose k]]
- $\alpha$ a positive integer, $k > \alpha$: the numerator has a factor 0 so ${}^{\alpha}C_{k} = 0$ and the series stops ([[Binomial Theorem]])
- $\alpha$ not an integer: never 0, so the series is infinite

# Upper negation
For positive integers $n, k$:
$$
{}^{-n}C_{k} = (-1)^k\, {}^{k+n-1}C_{k} = (-1)^k\, {}^{k+n-1}C_{n-1}
$$
Proof:
$$
\begin{aligned}
{}^{-n}C_{k} &= \frac{(-n)(-n-1)\cdots(-n-k+1)}{k!} \\
&= (-1)^k \frac{n(n+1)\cdots(n+k-1)}{k!} \\
&= (-1)^k \frac{(n+k-1)!}{(n-1)!\,k!} \\
&= (-1)^k\, {}^{k+n-1}C_{k}
\end{aligned}
$$
${}^{k+n-1}C_{k}$ is the answer to [[Arrangements and Combinations with Repetitions#Combinations with repetitions|SP5]], which is not a coincidence (see [[Generating Functions]])

# Key expansion
Upper negation with $x \to -x$:
$$
(1 - x)^{-n} = \sum_{k=0}^{\infty} {}^{k+n-1}C_{k}\, x^k
$$ ^neg-binomial

- $(1-x)^{-1} = 1 + x + x^2 + \dots$
- $(1-x)^{-2} = \sum (k+1)x^k = 1 + 2x + 3x^2 + \dots$

# Example
Evaluate $\sum_{k=0}^\infty k 2^{-k}$. Work backwards to a closed form:
$$
\begin{aligned}
\sum_{k=0}^\infty k x^k &= \sum_{k=0}^\infty (k+1) x^{k+1} \\
&= x \sum_{k=0}^\infty (k+1) x^k \\
&= x(1-x)^{-2} \\
\text{let } x &= \tfrac12 \\
\sum_{k=0}^\infty k 2^{-k} &= \frac{1/2}{1/4} = 2
\end{aligned}
$$
