A combination from a set is an unordered selection from the set. repetitions are allowed.

Formally, a combination on a set $S$ is identified by the multiplicities $m_{i}, i \in S$ when $m_{i} \in \{0, 1, \dots \}$ where $m_i$ determines the number of times $i$ appears.

Size of a combination is the total number of selections size $k$ as $k$ combinations

# Standard problem 3:

^28b8fd

How many k-element combinations can be made from set $S$ where $|S|$ = n and $k \leq n$

From [[Arrangements#^0a665c|SP2]], number of permutations = $P(n, k) = \frac{n!}{(n - k)!}$

from a given combination, there are $k!$ permutations

$$
\begin{aligned} 
\therefore Combinations \times k! &= \frac{n!}{(n - k)!} \text{   where } k \leq n \\
Combinations &= \frac{n!}{k!(n - k)!} 
\end{aligned}
$$

$^nC_{k} = \frac{n!}{k!(n - k)!}$

Subset of size $k$ chosen from a set of size $n$
With repetitions: [[Arrangements and Combinations with Repetitions#Combinations with repetitions|stars and bars]]

# proposition
$^nC_{k} \equiv ^nC_{n-k}$
$$
\begin{aligned}
LHS &= \frac{n!}{k!(n-k)!} \\
 \\
RHS &= \frac{n!}{(n-k)!(n - (n - k))!} \\
&= \frac{n!}{(n - k)!k!} \\
LHS &= RHS \\
\therefore & \text{ Proven}
\end{aligned}
$$
Logical Proof:
choosing k out of n objects is the same as not choosing n - k  $\therefore$ choosing n objects

e.g. 3-letter words with letters in strict alphabetical order: each set of 3 letters gives $3!$ words and exactly one is in order, so $\frac{P(26, 3)}{3!} = {}^{26}C_{3}$

# Pascal's formula
For $1 \leq k \leq n - 1$:
$$
{}^nC_{k} = {}^{n-1}C_{k-1} + {}^{n-1}C_{k}
$$
Combinatorial proof: fix one element $x$. A $k$-subset either contains $x$ (choose the other $k - 1$ from $n - 1$) or doesn't (choose all $k$ from $n - 1$), so use the [[Addition Principle]]
e.g. 6-subsets of $\{0, \dots, 9\}$: ${}^{10}C_{6} = {}^9C_{5} + {}^9C_{6}$ (with 0, without 0)

**Pascal's triangle:** row $n$ is ${}^nC_{0}, \dots, {}^nC_{n}$, and each interior entry is the sum of the two above it
```
1
1 1
1 2 1
1 3 3 1
1 4 6 4 1
```

# Product of consecutive integers
The product of $k$ consecutive positive integers is divisible by $k!$
$$
N = (a+1)(a+2)\cdots(a+k) = \frac{(a+k)!}{a!} = {}^{a+k}C_{a}\; k!
$$
${}^{a+k}C_{a}$ is an integer $\therefore k! \mid N$
