Get new [[Generating Functions]] from old ones using calculus

# Multiply by n
If $f(x)$ generates $a_n$, then $xf'(x)$ generates $na_n$
$$
\sum_{n=0}^{\infty} na_nx^n = x\sum_{n=0}^{\infty} a_n nx^{n-1} = x\frac{d}{dx}\sum_{n=0}^{\infty} a_nx^n = xf'(x)
$$
(see [[Differentiation]])
- $a_n = n$: $x\frac{d}{dx}\left(\frac{1}{1-x}\right) = \frac{x}{(1-x)^2}$
- $a_n = n^2$: $x\frac{d}{dx}\left(\frac{x}{(1-x)^2}\right) = x\left((1-x)^{-2} + 2x(1-x)^{-3}\right) = \frac{x(1+x)}{(1-x)^3}$
- $a_n = n^3$: $\frac{x(x^2 + 4x + 1)}{(1-x)^4}$

# Partial sums
If $f(x)$ generates $a_n$, then $\frac{f(x)}{1-x}$ generates $s_n = \sum_{k=0}^{n} a_k$
Proof: [[Standard Generating Functions#Product rule|product rule]] with $b_n = 1$, i.e. $g(x) = \frac{1}{1-x}$, gives $c_k = \sum_{\ell=0}^{k} a_\ell$

# Sum of squares
$a_n = n^2$, so $s_n = \sum_{k=1}^{n} k^2$ has generating function $\frac{x(1+x)}{(1-x)^4} = (x + x^2)\sum_{k=0}^{\infty}{}^{k+3}C_{3}\, x^k$
$s_n$ = coefficient of $x^{n-1}$ plus coefficient of $x^{n-2}$ in $(1-x)^{-4}$:
$$
\begin{aligned}
s_n &= {}^{n+2}C_{3} + {}^{n+1}C_{3} \\
&= \tfrac16\left((n+2)(n+1)n + (n+1)n(n-1)\right) \\
\therefore \sum_{k=1}^{n}k^2 &= \tfrac16 n(n+1)(2n+1)
\end{aligned}
$$

# Sum of cubes
Same method with $\frac{x(x^2 + 4x + 1)}{(1-x)^5}$ and $(1-x)^{-5} = \sum {}^{k+4}C_{4}\, x^k$:
$$
\begin{aligned}
s_n &= {}^{n+1}C_{4} + 4\,{}^{n+2}C_{4} + {}^{n+3}C_{4} \\
&= \tfrac{n(n+1)}{24}\left((n-1)(5n+6) + (n+3)(n+2)\right) \\
&= \tfrac{n(n+1)}{24}\left(6n^2 + 6n\right) \\
\therefore \sum_{k=1}^{n}k^3 &= \tfrac14 n^2(n+1)^2
\end{aligned}
$$
