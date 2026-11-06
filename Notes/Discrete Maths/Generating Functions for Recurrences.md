Solve a [[Recurrence Relations|recurrence relation]] by turning it into an equation for $f(x) = \sum a_n x^n$ ([[Generating Functions]])

# Method
1. Split off the initial terms: $f(x) = a_0 + a_1x + \sum_{n \geq 2} a_nx^n$
2. Substitute the recurrence into the sum
3. Take out powers of $x$ so the index matches the power ($a_{n-1}x^n = x \cdot a_{n-1}x^{n-1}$), then re-index
4. Write each sum in terms of $f(x)$, e.g. $\sum_{n \geq 1} a_nx^n = f(x) - a_0$
5. Solve for $f(x)$, expand it ([[Standard Generating Functions]]) and read off $a_n$

# Example
$a_n = a_{n-1} + 2a_{n-2}$, $a_0 = 1$, $a_1 = -1$
$$
\begin{aligned}
f(x) &= 1 - x + \sum_{n=2}^{\infty}(a_{n-1} + 2a_{n-2})x^n \\
&= 1 - x + x\sum_{n=1}^{\infty}a_nx^n + 2x^2\sum_{n=0}^{\infty}a_nx^n \\
&= 1 - x + x(f(x) - 1) + 2x^2f(x) \\
f(x)(2x^2 + x - 1) &= 2x - 1 \\
f(x)(2x - 1)(x + 1) &= 2x - 1 \\
f(x) &= \frac{1}{1 + x} = 1 - x + x^2 - x^3 + \dots \\
\therefore a_n &= (-1)^n
\end{aligned}
$$
Check: $a_2 = -1 + 2 = 1$, $a_3 = 1 - 2 = -1$ ✓ (the PDF says "1 if even, 0 if odd", which is wrong)

# Example: lines in the plane
$a_n = a_{n-1} + n$, $a_0 = 1$ ([[Recurrence Relations#Lines in the plane]])
$$
\begin{aligned}
f(x) &= 1 + \sum_{n=1}^{\infty}(a_{n-1} + n)x^n \\
&= 1 + x\sum_{n=1}^{\infty}a_{n-1}x^{n-1} + x\sum_{n=1}^{\infty}nx^{n-1} \\
&= 1 + x\sum_{n=0}^{\infty}a_nx^n + x\sum_{n=0}^{\infty}(n+1)x^n \\
&= 1 + xf(x) + x(1-x)^{-2} \\
f(x) &= (1-x)^{-1} + x(1-x)^{-3} \\
&= \sum_{n=0}^{\infty}x^n + \sum_{n=0}^{\infty}{}^{n+2}C_{2}\, x^{n+1} \\
&= \sum_{n=0}^{\infty}x^n + \sum_{n=1}^{\infty}{}^{n+1}C_{2}\, x^{n} \\
&= \sum_{n=0}^{\infty}\left(1 + {}^{n+1}C_{2}\right)x^n \\
\therefore a_n &= 1 + {}^{n+1}C_{2}
\end{aligned}
$$
