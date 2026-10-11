a set S if defined by the elements that belong to it

Notations:
$x \in S$              $x$ belongs to S
$x \not\in S$              $x$ doesn't belong to S
$X \subseteq S$            $x$ is a subset of S
$S / R$                 $\text{elements of }R \text{are removed from }S$
$R\cup S$              Union - combines the elements of both
$R \cap S$              Intersection - Returns elements common in both
$\emptyset$                        Empty set



If a set S is finite, its size of **cardinality** is  $|S|$

For sets X and Y, their **[[Cartesian product]]** is
for i in X:
	for j in Y:
		product += (i, y)

If $|S| =n$ then the number of subsets of S is $2^n$

Proof: In a subset of S, a given element in S is either present or not present (boolean). Therefore, for any subset, a boolean string of $|S|$ bits can be used to represent all possible subsets of S. Since Boolean is being used, the number of combinations is $2^n$ which is also the number of subsets (includes $\emptyset$)

