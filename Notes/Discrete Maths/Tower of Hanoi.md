3 pegs, $n$ rings stacked largest at the bottom. Move one ring at a time and never put a ring on a smaller one. Move the whole tower to another peg in as few moves as possible

$t_n$ = minimum number of moves: $1, 3, 7, 15, 31, \dots$

**Optimal strategy:**
1. Move the top $n - 1$ rings to the spare peg: $t_{n-1}$ moves
2. Move the largest ring: 1 move
3. Move the $n - 1$ rings back on top of it: $t_{n-1}$ moves

The largest ring has to move at some point, which needs the other $n - 1$ rings off it and an empty peg, so this is optimal
$$
t_n = 2t_{n-1} + 1 \quad (n \geq 2), \qquad t_1 = 1
$$

# Solution
$$
t_n = 2^n - 1
$$
Using [[Inhomogeneous Linear Recurrences]]:
$$
\begin{aligned}
x - 2 = 0 &\implies g(n) = d_1 2^n \\
f(n) = 1 \text{, try } p(n) = B_0 &\implies B_0 = 2B_0 + 1 \implies B_0 = -1 \\
t_n &= d_1 2^n - 1 \\
t_1 = 1 &\implies 2d_1 - 1 = 1 \implies d_1 = 1 \\
\therefore t_n &= 2^n - 1
\end{aligned}
$$
Or guess it from the table and prove it by [[Mathematical Induction]]. Also a classic [[Recursion]] example
