a set S is defined by the elements that belong to it

Notations:
$x \in S$              $x$ belongs to S
$x \not\in S$              $x$ doesn't belong to S
$X \subseteq S$            $X$ is a subset of S
$S \setminus R$               $\text{elements of }R \text{are removed from }S$
$R\cup S$              Union - combines the elements of both
$R \cap S$              Intersection - Returns elements common in both
$\emptyset$                        Empty set



If a set S is finite, its size or **cardinality** is  $|S|$

For sets X and Y, their **Cartesian product** (x) is
for i in X:
	for j in Y:
		product += (i, j) ^888b0e
$S \times S = S^2$
$|X \times Y| = |X||Y|$ ([[Multiplication Principle]])
If $|S| =n$ then the number of subsets of S is $2^n$



Proof: In a subset of S, a given element in S is either present or not present (boolean). Therefore, for any subset, a boolean string of $|S|$ bits can be used to represent all possible subsets of S. Since Boolean is being used, the number of combinations is $2^n$ which is also the number of subsets (includes $\emptyset$)
Same as [[Binomial Theorem#Identities|binomial identity 1]] and the number of values of [[Introductions to Number Systems|n bits]]

**Disjoint sets:** when the sets given have no elements in common 
if $A$ and $B$ are disjoint sets then $A \cap B = \emptyset$ ^019723

# More notation
**Set-builder notation:** $S = \{n : n \in \mathbb{Z}, 0 \leq n \leq 9\}$ ("all $n$ such that ...")
$\mathbb{Z}$ = integers, $\mathbb{N} = \{1, 2, \dots\}$ (0 not included in this course)
Listing order doesn't matter: $\{0, 1, 2\} = \{2, 0, 1\}$

$R \subset S$: **strict subset** ($R \subseteq S$ and $R \neq S$)
$\emptyset \subseteq A$ for every $A$ (vacuously)
$R = S \iff R \subseteq S$ and $S \subseteq R$ (how to prove two sets are equal)
$A \setminus B = \{x : x \in A \text{ and } x \notin B\}$
$$
\bigcup_{i=1}^n A_i = \{x : x \in A_i \text{ for at least one } i\} \qquad \bigcap_{i=1}^n A_i = \{x : x \in A_i \text{ for every } i\}
$$
Unions of sets that overlap: [[Inclusion-Exclusion Principle]]

$X^n = \{(x_1, \dots, x_n) : x_i \in X\}$ ($n$-tuples) and $|X^n| = |X|^n$
Order inside a pair matters, $(1, a) \neq (a, 1)$, so in general $X \times Y \neq Y \times X$

**Combinatorial proof:** count a set by putting it in one-to-one correspondence (a bijection, see [[Functions]]) with a set you can already count, e.g. subsets of $\{1, \dots, 6\}$ ↔ $\{0, 1\}^6$ with $\{1, 4, 5\} \leftrightarrow (1, 0, 0, 1, 1, 0)$
