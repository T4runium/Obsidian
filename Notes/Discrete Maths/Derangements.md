A **derangement** of $\{1, \dots, n\}$ is a [[Permutation]] where no number is in its own place (no **fixed points**)
e.g. 2341 and 4123 are derangements of 1234; 4132 isn't (3 is fixed)
$n$ people each get the wrong hat back

$d(n)$ = number of derangements: $d(1) = 0,\; d(2) = 1,\; d(3) = 2,\; d(4) = 9$

# Formula
$$
d(n) = n! \sum_{k=0}^{n} \frac{(-1)^k}{k!}
$$
Proof ([[Inclusion-Exclusion Principle]]):
Let $A_i$ = permutations with $i$ fixed. Fixing $k$ chosen points leaves $(n-k)!$ arrangements, and there are ${}^nC_{k}$ ways to choose the points
$$
\begin{aligned}
S_k &= {}^nC_{k}\,(n - k)! = \frac{n!}{k!} \\
|A_1 \cup \dots \cup A_n| &= \sum_{k=1}^{n} (-1)^{k+1} \frac{n!}{k!} \quad \text{(non-derangements)} \\
d(n) &= n! - \sum_{k=1}^{n} (-1)^{k+1} \frac{n!}{k!} \\
&= n! \sum_{k=0}^{n} \frac{(-1)^k}{k!}
\end{aligned}
$$

# Limit
$\sum_{k=0}^\infty \frac{(-1)^k}{k!} = e^{-1}$, so
$$
\lim_{n \to \infty} \frac{d(n)}{n!} = \frac{1}{e}
$$
so about 37% of random permutations are derangements
