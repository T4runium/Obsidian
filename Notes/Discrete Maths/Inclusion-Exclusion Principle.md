Size of a union of sets that are **not** disjoint (if they are, use the [[Addition Principle]])

**Two sets:**
$$
|A_1 \cup A_2| = |A_1| + |A_2| - |A_1 \cap A_2|
$$
**Three sets:**
$$
|A_1 \cup A_2 \cup A_3| = \sum|A_i| - \sum_{i<j}|A_i \cap A_j| + |A_1 \cap A_2 \cap A_3|
$$
Proof: an element in all 3 sets is counted $1 + 1 + 1 - 1 - 1 - 1 + 1 = 1$ time. Check elements in exactly 1 or 2 sets the same way

# General formula
Let $S_k$ = sum of the sizes of all $k$-fold intersections
$$
S_k = \sum_{i_1 < i_2 < \dots < i_k} |A_{i_1} \cap \dots \cap A_{i_k}|
$$
$$
|A_1 \cup \dots \cup A_n| = \sum_{k=1}^{n} (-1)^{k+1} S_k = S_1 - S_2 + S_3 - \dots
$$
Proof: each element is counted once on both sides, or by [[Mathematical Induction]] on $n$

**Method:** let $A_i$ = the "bad" cases, count the union, subtract it from the total

# Examples
**5-letter words from PQR missing at least one letter:** $A_1$ = no P, $A_2$ = no Q, $A_3$ = no R
$|A_i| = 2^5$, $|A_i \cap A_j| = 1$ (e.g. RRRRR), $|A_1 \cap A_2 \cap A_3| = 0$
$$
3 \cdot 2^5 - 3 \cdot 1 + 0 = 93
$$

**Arrangements of 11223344 with no two equal digits adjacent:**
total $= \frac{8!}{2!\,2!\,2!\,2!} = 2520$ ([[Arrangements#Standard Problem 4|SP4]])
$A_i$ = arrangements with $ii$ together (treat it as one block)
$|A_i| = \frac{7!}{2!\,2!\,2!} = 630$, $|A_i \cap A_j| = \frac{6!}{2!\,2!} = 180$, $|A_i \cap A_j \cap A_k| = \frac{5!}{2!} = 60$, all four $= 4! = 24$
$$
\begin{aligned}
|A_1 \cup \dots \cup A_4| &= {}^4C_1(630) - {}^4C_2(180) + {}^4C_3(60) - {}^4C_4(24) \\
&= 1656 \\
\therefore \text{answer} &= 2520 - 1656 = 864
\end{aligned}
$$

# Try
- integers in $\{1, \dots, 210\}$ divisible by none of 2, 3, 5, 7 (answer: 48)
- ways to put 5 distinct objects into 4 boxes with at least 2 boxes empty

Big application: [[Derangements]]
