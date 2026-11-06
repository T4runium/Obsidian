A permutation on set $S$ is a list of elements of $S$ where each element of $S$ is only used once

if $|S| = n$ then there are $n!$ permutations of $S$
Proof:
[[Arrangements#^0a665c|SP2]] but k = n
$$
\begin{aligned}
SP2 = \frac{n!}{(n - k)!} \\
= \frac{n!}{(n - (n))!}\\
= n!
\end{aligned}

$$

General Idea: If $r$ is a non-negative number, an r permutation on $S$ is an arrangement of $r$ distinct elements of $S$
P(n, r) denotes the number of $r$ permutations on set of size $n$
$$
P(n, r) = \frac{n!}{(n - r)!}
$$

$P(n, 0) = 1$ (the empty list) and $P(n, r) = 0$ for $r > n$
