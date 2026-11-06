A **recurrence relation** gives each term of a sequence from earlier terms. Together with the **initial conditions** it fixes the whole sequence
Same idea as [[Recursion]]

To find one: take one step, then count what's left

# Stairs (Fibonacci)
$f_n$ = ways to climb $n$ stairs taking 1 or 2 at a time
The first stride is 1 (leaving $f_{n-1}$ ways) or 2 (leaving $f_{n-2}$). These are disjoint, so by the [[Addition Principle]]:
$$
f_n = f_{n-1} + f_{n-2} \quad (n \geq 2), \qquad f_0 = f_1 = 1
$$
$1, 1, 2, 3, 5, 8, 13, \dots$ are the [[Fibonacci]] numbers ($f_0 = 1$: the empty staircase has one way, the empty sequence)
Closed form: [[Homogeneous Linear Recurrences#Fibonacci]]

# Lines in the plane
$r_n$ = regions made by $n$ lines, no two parallel and no three through one point
The $n$th line crosses the other $n - 1$, so it passes through $n$ old regions and splits each in two
$$
r_n = r_{n-1} + n \quad (n \geq 1), \qquad r_0 = 1
$$
$1, 2, 4, 7, 11, 16, \dots$ with closed form $r_n = 1 + {}^{n+1}C_{2} = 1 + \frac{1}{2}n(n+1)$

Proof by [[Mathematical Induction]]: base $r_1 = 1 + {}^2C_2 = 2$ ✓, step:
$$
\begin{aligned}
r_{n+1} &= r_n + n + 1 \\
&= 1 + \tfrac{1}{2}n(n+1) + n + 1 \\
&= 1 + (n+1)\left(\tfrac12 n + 1\right) \\
&= 1 + \tfrac{1}{2}(n+1)(n+2) = 1 + {}^{n+2}C_{2}
\end{aligned}
$$
Also solved in [[Inhomogeneous Linear Recurrences#Lines in the plane]] and [[Generating Functions for Recurrences]]

# [[Tower of Hanoi]]
$t_n = 2t_{n-1} + 1$, $t_1 = 1$

# Types
$$
a_n = c_1 a_{n-1} + \dots + c_r a_{n-r} + f(n)
$$
- **linear:** no term multiplies two $a_i$'s together
- **homogeneous:** $f(n) = 0$, so every term has an $a_i$ → [[Homogeneous Linear Recurrences]]
- **inhomogeneous:** $f(n) \neq 0$ → [[Inhomogeneous Linear Recurrences]]
- or use [[Generating Functions for Recurrences]]
