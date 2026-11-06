If $u$ and $v$ are vectors in $\mathbb{R}^n$ then $||u + v|| \leq ||u|| + ||v||$

# Proof
Take $(||u|| + ||v||)^2$

$$
\begin{aligned} \\
(||u|| + ||v||)^2 &= ||u||^2 + ||v||^2 + 2||u||.||v|| \\
&\geq ||u||^2 + ||v||^2 + 2u.v \text{ (applying Cauchy-Schwarz)}\\
&= ||u + v||^2 \\
||u|| + ||v|| &\geq ||u + v||
\end{aligned}

$$
$2u.v \leq 2||u||.||v||$ according to [[Cauchy-Schwarz Inequality]]


