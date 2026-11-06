$$
a_n = c_1 a_{n-1} + \dots + c_r a_{n-r} + f(n)
$$
where $f(n) \neq 0$ is the **inhomogeneous part** ([[Recurrence Relations]])

# Method
1. Solve the homogeneous part (drop $f(n)$) to get the general solution $g(n)$ ([[Homogeneous Linear Recurrences]]). **Don't** fix the constants yet
2. Find a **particular solution** $p(n)$ of the full recurrence (table below)
3. General solution: $a_n = g(n) + p(n)$
4. Apply the initial conditions to fix the constants in $g(n)$

# Particular solution table
| $f(n)$ | try $p(n)$ |
| --- | --- |
| $A$ | $B_0$ |
| $An$ | $B_0 + B_1 n$ |
| $An^2$ | $B_0 + B_1n + B_2n^2$ |
| $Aq^n$ | $B_0 q^n$ |
| $Anq^n$ | $(B_0 + B_1n)q^n$ |

Substitute $p(n)$ into the recurrence and compare coefficients. If $f(n)$ is a sum of these types, find a $p(n)$ for each and add them

**Exceptions:**
- $q$ is a root of the characteristic equation (repeated $k$ times): $q^n$ is already in $g(n)$, so use $nq^n$ (or $n^kq^n$)
- $1$ is a root: treat $An^k$ as $An^k \cdot 1^n$, so the first rule applies and you multiply $p(n)$ by $n$

# Example
$a_n = a_{n-1} + 2a_{n-2} - 2n$, $a_0 = a_1 = 0$
$$
\begin{aligned}
x^2 - x - 2 = 0 &\implies x = 2, -1 \implies g(n) = d_1(-1)^n + d_2 2^n \\
\text{try } p(n) &= B_0 + B_1 n \\
B_0 + B_1 n &= B_0 + B_1(n-1) + 2B_0 + 2B_1(n-2) - 2n \\
n: \; B_1 &= 3B_1 - 2 \implies B_1 = 1 \\
1: \; B_0 &= 3B_0 - 5B_1 \implies B_0 = \tfrac{5}{2} \\
a_n &= d_1(-1)^n + d_2 2^n + n + \tfrac{5}{2} \\
a_0: \; 0 &= d_1 + d_2 + \tfrac52 \\
a_1: \; 0 &= -d_1 + 2d_2 + \tfrac72 \\
\implies d_2 = -2, \; d_1 &= -\tfrac12 \\
\therefore a_n &= \tfrac12(-1)^{n+1} - 2^{n+1} + n + \tfrac52
\end{aligned}
$$
Check: $a_2 = 0 + 0 - 4 = -4$ ✓ (the coefficient line in the lecture PDF has a typo; this working is corrected)

# Lines in the plane
$r_n = r_{n-1} + n$, $r_0 = 1$ (see [[Recurrence Relations#Lines in the plane]])
$x - 1 = 0$ has root 1, so $g(n) = d_1$
$f(n) = n = n \cdot 1^n$ and 1 is a root, so $B_0 + B_1 n$ fails (its constant is already in $g$). Try $p(n) = B_0n + B_1n^2$:
$$
\begin{aligned}
B_0n + B_1n^2 &= B_0(n-1) + B_1(n-1)^2 + n \\
&= (B_0 - 2B_1 + 1)n + B_1n^2 + (B_1 - B_0) \\
\implies B_0 = B_1 &= \tfrac12 \\
r_n &= d_1 + \tfrac12 n(n+1) \\
r_0 = 1 &\implies d_1 = 1 \\
\therefore r_n &= 1 + \tfrac12 n(n+1)
\end{aligned}
$$
Easier one: [[Tower of Hanoi]]
