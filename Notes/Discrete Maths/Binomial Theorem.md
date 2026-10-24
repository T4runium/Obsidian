let $n \in \mathbb{N}$ and $a, b \in \mathbb{R}$ then,
$$
(a + b)^n = \sum_{k = 0}^{n} {}^nC_{k} \times a^k b^{n - k}
$$
Any term in this expansion is a list of length $n$ consisting of $a$ and $b$.
the number of times $a$ appears for a given term is $a^nb^{n - k}$
Then, the number of times $a^kb^{n - k}$ is the number of ways $k$ number of $a$'s can be chosen $\therefore ^{n}C_{k}$ possible ways.

# Identities
**1.**
$$
\begin{aligned}
\sum_{k = 0}^n {}^{n}C_{k} &= 2^n \\
\end{aligned}
$$
Proof:
consider the expansion of $(x + 1)^n$

$$
(x + 1)^n = \sum_{k = 0}^{n} {}^nC_{k} \times x^k
$$
let $x = 1$
$$
\begin{aligned}
&2^n = \sum_{k = 0}^{n} {}^nC_{k} \times \\
&\therefore True
\end{aligned}
$$

**2.**
$$
\sum_{k = 0}^n {}^nC_{k} (-1)^k = 0
$$
Proof:
consider the expansion of $(x + 1)^n$

$$
(x + 1)^n = \sum_{k = 0}^{n} {}^nC_{k} \times x^k
$$
let $x = -1$
$$
\begin{aligned}
&0 = \sum_{k = 0}^n {}^nC_{k} (-1)^k \\
&\therefore True
\end{aligned}
$$

**3.**

$$
\sum_{k = 0}^n {}^nC_{k} 2^k = 3^n
$$
Proof:
consider the expansion of $(x + 1)^n$

$$
(x + 1)^n = \sum_{k = 0}^{n} {}^nC_{k} \times x^k
$$
let x = 2
$$
\begin{aligned}
&3^n = \sum_{k = 0}^n {}^nC_{k} 2^k \\
&\therefore True
\end{aligned}
$$


**4.**
$$
\sum_{k = 0}^n {}^nC_{k} (k) = n{2}^{n - 1}
$$
Proof:
consider the expansion of $(x + 1)^n$

$$
\begin{aligned}
(x + 1)^n &= \sum_{k = 0}^{n} {}^nC_{k} \times x^k \\
\frac{d}{dx} (1 + x)^n &= \frac{d}{dx}\sum_{k = 0}^n {}^nC_{k} x^k \\
n(1 + x)^{n - 1} &= \sum_{k = 0}^n {}^nC_{k} kx^{k - 1} \\
let \text{ }x &= 1\\
n{2}^{n - 1} &= \sum_{k = 0}^n {}^nC_{k}(k) \\
\therefore True
\end{aligned}
$$
