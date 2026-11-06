$$
a_n = c_1 a_{n-1} + c_2 a_{n-2} + \dots + c_r a_{n-r} \quad (n \geq r)
$$
with constants $c_i$ and initial conditions $a_0, \dots, a_{r-1}$ ([[Recurrence Relations]])

# Method
1. Try $a_n = x^n$ and divide by $x^{n-r}$ to get the **characteristic equation**
$$
x^r - c_1 x^{r-1} - \dots - c_r = 0
$$
2. Find its roots $\alpha_1, \dots, \alpha_r$
3. **General solution** (distinct roots): $a_n = d_1\alpha_1^n + \dots + d_r\alpha_r^n$. This works because the recurrence is linear, so any [[Linear Combinations|linear combination]] of solutions is a solution
4. Put in the initial conditions to get $r$ simultaneous equations for the $d_i$ ([[Linear Systems]])

**Repeated roots:** if $\alpha$ is repeated $k$ times, use $(e_1 + e_2 n + \dots + e_k n^{k-1})\alpha^n$ in place of the $\alpha$ terms
Very similar to solving linear ODEs

# Example
$a_n = 3a_{n-1} + 4a_{n-2}$, $a_0 = 1$, $a_1 = 0$
$$
\begin{aligned}
x^2 - 3x - 4 = 0 &\implies (x - 4)(x + 1) = 0 \implies x = 4, -1 \\
a_n &= d_1(-1)^n + d_2 4^n \\
a_0: \; 1 &= d_1 + d_2 \\
a_1: \; 0 &= -d_1 + 4d_2 \\
\implies d_2 = \tfrac{1}{5}, \; d_1 &= \tfrac{4}{5} \\
\therefore a_n &= \tfrac{1}{5}4^n + \tfrac{4}{5}(-1)^n
\end{aligned}
$$

# Fibonacci
$f_n = f_{n-1} + f_{n-2}$, $f_0 = f_1 = 1$
$$
\begin{aligned}
x^2 - x - 1 = 0 &\implies \alpha = \tfrac{1 + \sqrt5}{2}, \; \beta = \tfrac{1 - \sqrt5}{2} \\
f_n &= c_1\alpha^n + c_2\beta^n \\
f_0: \; 1 &= c_1 + c_2 \\
f_1: \; 1 &= c_1\alpha + c_2\beta \\
\implies c_1 = \tfrac{\alpha}{\sqrt5}, \; c_2 &= -\tfrac{\beta}{\sqrt5} \\
\therefore f_n &= \frac{1}{\sqrt5}\left(\left(\frac{1+\sqrt5}{2}\right)^{n+1} - \left(\frac{1-\sqrt5}{2}\right)^{n+1}\right)
\end{aligned}
$$
The solution is unique: $f_0, f_1$ fix $f_2$, then $f_1, f_2$ fix $f_3$, and so on
See also [[Fibonacci]] (ADS)
