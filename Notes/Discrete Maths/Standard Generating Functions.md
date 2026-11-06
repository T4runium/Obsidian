| sequence | generating function |
| --- | --- |
| $1, 1, \dots, 1$ ($n+1$ ones), then $0, 0, \dots$ | $\sum_{k=0}^{n} x^k = \frac{1 - x^{n+1}}{1 - x}$ |
| $1, 1, 1, \dots$ | $\frac{1}{1 - x}$ |
| $1, 2, 3, \dots$ | $\frac{1}{(1 - x)^2}$ |
| ${}^{n+k-1}C_{k}$ | $\frac{1}{(1 - x)^n}$ |
| ${}^nC_{k}$ | $(1 + x)^n$ |
| $n$ | $\frac{x}{(1-x)^2}$ |
| $n^2$ | $\frac{x(1+x)}{(1-x)^3}$ |

($n$ and $n^2$ come from [[Calculus of Generating Functions]])

# Proofs
**Finite geometric series:** the sum telescopes
$$
(1 - x)\sum_{k=0}^{n} x^k = \sum_{k=0}^{n} (x^k - x^{k+1}) = 1 - x^{n+1}
$$
**Infinite geometric series:** let $S = 1 + x + x^2 + \dots$, then $S = 1 + xS \implies S = \frac{1}{1-x}$
**$(1-x)^{-n}$:** [[Extended Binomial Coefficients#^neg-binomial|upper negation]], or see $(1 + x + x^2 + \dots)^n$ as counting [[Arrangements and Combinations with Repetitions#Combinations with repetitions|SP5]]

# Product rule
If $f(x) = \sum a_kx^k$ and $g(x) = \sum b_kx^k$ then $f(x)g(x) = \sum c_kx^k$ where
$$
c_k = \sum_{\ell = 0}^{k} a_\ell\, b_{k - \ell}
$$
i.e. collect every way of making the power $k$
e.g. the $x^2$ coefficient of $(1 + 2x + 4x^2 + \dots)(1 + 5x + 7x^2 + \dots)$ is $1 \cdot 7 + 2 \cdot 5 + 4 \cdot 1 = 21$
