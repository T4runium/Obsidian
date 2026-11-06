$$
F(n) =
\begin{cases}
0 & n = 0 \\
1 & n = 1 \\
F(n-1) + F(n-2) & n \ge 2
\end{cases}
$$
[[Recursion|Recursive]] version:
```
fibonacci(n):
    if n = 0 or n = 1 then return n
    return fibonacci(n-1) + fibonacci(n-2)
```
Iterative version: start with `fibs = [0, 1]` and keep appending the sum of the last two, then return `fibs[n]`

Problem: the recursive version calls itself with the **same argument many times**, e.g. $F(5)$ computes $F(3)$ twice and $F(2)$ three times. Fix: [[Memoization]]
