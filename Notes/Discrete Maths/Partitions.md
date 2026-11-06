A **partition** of a positive integer $n$ writes $n$ as an **unordered** sum of positive integers, called the **parts**. Parts are usually written in non-increasing order
$p(n)$ = number of partitions of $n$

e.g. $p(5) = 7$: $5,\; 4+1,\; 3+2,\; 3+1+1,\; 2+2+1,\; 2+1+1+1,\; 1+1+1+1+1$

Same as $n$ identical balls into $n$ identical boxes ([[Configurations]])

There is no simple formula. The Hardy–Ramanujan asymptotic formula is
$$
p(n) \sim \frac{1}{4n\sqrt3}\exp\left(\pi\sqrt{\frac{2n}{3}}\right)
$$

# Generating function
Let $e_k$ = the total from parts of size $k$, so $e_k \in \{0, k, 2k, \dots\}$, giving the factor $1 + x^k + x^{2k} + \dots = \frac{1}{1 - x^k}$
$$
\sum_{n=0}^{\infty} p(n)x^n = \prod_{k=1}^{\infty} \frac{1}{1 - x^k}
$$

**Distinct parts:** each $k$ is used at most once, so $e_k \in \{0, k\}$:
$$
\prod_{k=1}^{\infty}(1 + x^k) = 1 + x + x^2 + 2x^3 + 2x^4 + 3x^5 + \dots
$$
e.g. 5 has 3 partitions into distinct parts: $5,\; 4+1,\; 3+2$

**Coins:** the number of ways to make $n$p from 1p, 2p and 5p coins is the coefficient of $x^n$ in
$$
\frac{1}{1 - x}\cdot\frac{1}{1 - x^2}\cdot\frac{1}{1 - x^5}
$$
See [[Generating Functions]]
