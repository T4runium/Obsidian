A combination from a set is an unordered selection from the set. repetitions are allowed.

Formally, a combination on a set $S$ is identified by the multiplicities $m_{i}, i \in S$ when $m_{i} \{0, 1, \dots \}$ where $m_i$ determines the number of times $i$ appears.

Size of a combination is the total number of selections size $k$ as $k$ combinations

# Standard problem 3:

^28b8fd

How many k-element combinations can be made from set $S$ where $|S|$ = n and $n > k$

From [[Arrangements#^0a665c|SP2]], number of permutations = $P(n, k) = \frac{n!}{(n - k)!}$

from a given combination, there are $k!$ permutations

$$
\begin{aligned} 
\therefore Combinations \times k! &= \frac{n!}{(n - k)!} \text{   where n > k} \\
Combinations &= \frac{n!}{k!(n - k)!} 
\end{aligned}
$$

$^nC_{k} = \frac{n!}{k!(n - k)!}$

Subset of size $k$ chosen from a set of size $n$

# proposition
$^nC_{k} \equiv ^nC_{n-k}$
$$
\begin{aligned}
LHS &= \frac{n!}{k!(n-k)!} \\
 \\
RHS &= \frac{n!}{(n-k)!(n - (n - k)!)} \\
&= \frac{n!}{(n - k)!k!} \\
LHS &= RHS \\
\therefore & \text{ Proven}
\end{aligned}
$$
Logical Proof:
choosing k out of n objects is the same as not choosing n - k  $\therefore$ choosing n objects


