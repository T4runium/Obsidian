Selections from a set $S$ where $|S| = n$ and each element can be picked more than once

# Arrangements with repetitions
Order matters, repetitions allowed. This is [[Arrangements#Standard Problem 1|SP1]]. Arranging a given list with repeated items is [[Arrangements#Standard Problem 4|SP4]]
$$
\text{Arrangements} = n^k
$$
Each of the $k$ slots has $n$ choices ([[Multiplication Principle]])

# Combinations with repetitions
(**Standard Problem 5**) Order doesn't matter, repetitions allowed
A [[Combinations|combination]] is fixed by its multiplicities $m_{1}, \dots, m_{n}$ where $m_{i} \in \{0, 1, \dots\}$ and
$$
m_{1} + m_{2} + \dots + m_{n} = k
$$

$$
\text{Combinations} = {}^{n + k - 1}C_{k}
$$

Proof (**stars and bars**):
Write the combination as $k$ stars ($\star$) split into $n$ groups by $n - 1$ bars ($|$)
group $i$ has $m_{i}$ stars
e.g. $n = 3, k = 4$: $\star\star|\,|\star\star$ means $m_{1} = 2, m_{2} = 0, m_{3} = 2$

Every combination gives exactly one string and every string gives exactly one combination (a bijection, see [[Functions]])
$$
\begin{aligned}
\text{length of string} &= k + (n - 1) \\
\text{Combinations} &= \text{ways to choose positions of the } k \text{ stars} \\
&= {}^{n + k - 1}C_{k} \\
&= {}^{n + k - 1}C_{n - 1} \text{ (by } {}^nC_{k} = {}^nC_{n-k} \text{)}
\end{aligned}
$$

In balls and bins terms ([[Configurations]]): $k$ **indistinguishable** balls into $n$ **distinguishable** bins

# Standard Problem 6
Combinations with repetitions where **every** object is chosen at least once ($k \geq n$)
$$
{}^{k-1}C_{n-1}
$$
Proof: sort the combination, e.g. $1\,1\,1\,|\,2\,|\,3$. There are $k - 1$ gaps between the $k$ items; choose $n - 1$ of them for the bars

SP5 from SP6: add one extra of each type ($m_i \to m_i + 1$), so $k$ items from $n$ types ↔ $k + n$ items with at least one of each: ${}^{k+n-1}C_{n-1}$ ✓

# Integer solutions
Number of solutions of $x_1 + \dots + x_n = k$:
- $x_i \geq 0$: SP5, ${}^{n+k-1}C_{n-1}$
- $x_i \geq 1$: SP6, ${}^{k-1}C_{n-1}$
- other lower bounds: **change of variables** so every bound becomes $\geq 1$

e.g. $x_1 + x_2 + x_3 + x_4 = 7$ with $x_1, x_3 \geq 0$ and $x_2, x_4 \geq 1$
let $y_1 = x_1 + 1,\; y_3 = x_3 + 1,\; y_2 = x_2,\; y_4 = x_4$
$$
y_1 + y_2 + y_3 + y_4 = 9, \; y_i \geq 1 \implies {}^{8}C_{3}
$$
Upper bounds as well? Use [[Generating Functions]]

# Examples
- 6-letter words in weak alphabetical order (ACCESS, ALMOST): SP5 with $n = 26, k = 6$: ${}^{31}C_{6}$
- 7 meal orders from 4 types: ${}^{10}C_{3}$; omitting at least one type: ${}^{10}C_{3} - {}^6C_{3}$; omitting exactly one: $4 \cdot {}^6C_{2}$

# Summary

|  | no repetitions | repetitions |
| --- | --- | --- |
| order matters | $\frac{n!}{(n - k)!}$ ([[Arrangements#^0a665c\|SP2]]) | $n^k$ ([[Arrangements#Standard Problem 1\|SP1]]) |
| order doesn't matter | ${}^nC_{k}$ ([[Combinations#^28b8fd\|SP3]]) | ${}^{n + k - 1}C_{k}$ |
