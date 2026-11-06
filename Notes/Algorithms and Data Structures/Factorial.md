$n! = n \times (n-1)!$, e.g. $5! = 5 \times 4!$, so it can be written as a [[Recursion|recursive]] algorithm
$$
n! =
\begin{cases}
1 & n = 1 \\
n \times (n-1)! & n > 1
\end{cases}
$$
```
factorial(n):
    if n = 1 then return 1
    else return n × factorial(n-1)
```
Iterative version: `total = 1`, multiply by `i` for `i = 1..n`
