The **(ordinary) generating function** of a sequence $a_0, a_1, a_2, \dots$ is the formal sum
$$
f(x) = \sum_{k=0}^{\infty} a_k x^k
$$
**Formal** means we ignore convergence and just add, multiply and differentiate as normal
The coefficients carry the counting information, e.g. $(1 + x)^n$ encodes ${}^nC_{0}, \dots, {}^nC_{n}$ ([[Binomial Theorem]]). It links discrete and continuous maths

# Counting with generating functions
To count solutions of $e_1 + \dots + e_n = k$ with restrictions on each $e_i$:
1. For each $e_i$, write $\sum x^p$ over the values $p$ that $e_i$ can take
2. Multiply these together
3. The answer is the coefficient of $x^k$

Picking one term from each bracket gives $x^{e_1}\cdots x^{e_n} = x^{e_1 + \dots + e_n}$, so each way to reach $x^k$ is exactly one solution

**Example:** 7 bars shared between Alice (≤ 4), Brian (≤ 3), Claire (≤ 2), Derek (≤ 1)
$$
f(x) = (1 + x + \dots + x^4)(1 + x + x^2 + x^3)(1 + x + x^2)(1 + x)
$$
coefficient of $x^7$ = 15

Special cases:
- $e_i \in \{0, 1\}$: $(1 + x)^n$ gives ${}^nC_{k}$ (the binomial theorem again)
- $e_i \geq 0$: $(1 + x + x^2 + \dots)^n = (1 - x)^{-n}$ gives ${}^{n+k-1}C_{k}$ ([[Arrangements and Combinations with Repetitions#Combinations with repetitions|SP5]])

# Finding coefficients
1. Write the product form from the problem
2. Make it compact with [[Standard Generating Functions]], e.g. $1 + x + \dots + x^m = \frac{1 - x^{m+1}}{1 - x}$
3. Expand each factor ([[Binomial Theorem]], [[Extended Binomial Coefficients#^neg-binomial|(1 - x)^(-n)]])
4. Collect all pairs of terms whose powers add up to $k$

**Example:** coefficient of $x^4$ in $(1 + x + x^2)^3$ (solutions with $e_i \in \{0, 1, 2\}$)
$$
\begin{aligned}
f(x) &= (1 - x^3)^3(1 - x)^{-3} \\
&= \left(\sum_{i=0}^{3} {}^3C_{i}(-1)^i x^{3i}\right)\left(\sum_{j=0}^{\infty} {}^{2+j}C_{j}\, x^j\right) \\
3i + j = 4 &: (i, j) = (0, 4), (1, 1) \\
\text{coefficient} &= {}^3C_{0}\,{}^6C_{4} - {}^3C_{1}\,{}^3C_{1} = 15 - 9 = 6
\end{aligned}
$$

**Example:** coefficient of $x^{17}$ in $(1 + x + \dots + x^{10})^5$
$$
\begin{aligned}
f(x) &= (1 - x^{11})^5 (1 - x)^{-5} \\
&= \left(\sum_{i=0}^{5} {}^5C_{i}(-1)^i x^{11i}\right)\left(\sum_{j=0}^{\infty} {}^{4+j}C_{4}\, x^j\right) \\
11i + j = 17 &: (i, j) = (0, 17), (1, 6) \\
\text{coefficient} &= {}^5C_{0}\,{}^{21}C_{4} - {}^5C_{1}\,{}^{10}C_{4} = 5985 - 1050 = 4935
\end{aligned}
$$

Next: [[Generating Functions for Recurrences]], [[Partitions]], [[Calculus of Generating Functions]]
