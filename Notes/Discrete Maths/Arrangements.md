List or string in which order matters - finite
Length = number of items
Repetitions are allowed

# Standard Problem 1
([[Configurations#^fd7bcd|distinguishable balls and bins]])
How many arrangements of length k can be made from elements of set S size n
all arrangements = $|S|=n$
arrangements are just picking from the set so a [[Set Theory#^888b0e|Cartesian product]] of the set itself
$\therefore \text{Num of arrangements }=|S|^k = n^k$

# Standard Problem 2
([[Configurations#^fd7bcd|distinguishable balls and bins]])
How many arrangements are there of length $k$, from set $S$ where $|S| = n$ and there are no repetitions ($k \leq n$). ^0a665c

$$
Arrangements = \frac{n!}{(n - k)!}
$$
Both SP1 and SP2 lead us to the **[[Multiplication Principle]]**


# [[Combinations#^28b8fd|Standard Problem 3]]
$$
Combinations = \frac{n!}{k!(n - k)!}
$$
notation = $^nC_{k}$

# Standard Problem 4
How many arrangements are there of a list of objects in which some objects are repeating where $n_{i}$ is the number of repetitions of an object and $n$ is the total

$$
P(n; n_{1}, n_{2},\dots,n_{r}) = \frac{n!}{n_{1}!n_{2}!\dots n_{r}!}
$$

e.g. MISSISSIPPI: $\frac{11!}{4!\,4!\,2!\,1!}$
Proof idea: label the identical letters ($I_1, I_2, \dots$) to get $n!$ arrangements, then divide by $n_i!$ for each type, since permuting identical letters gives the same word

**Tricks** (REARRANGE = RRR AA EE G N, total $\frac{9!}{3!\,2!\,2!}$):
- **Block:** R's all together → treat RRR as one object: $\frac{7!}{2!\,2!}$
- **Gaps:** no two R's adjacent → arrange the rest ($\frac{6!}{2!\,2!}$), then choose 3 of the 7 gaps for the R's: ${}^7C_{3}\,\frac{6!}{2!\,2!}$
- at least two R's together = total − no R's together

Combinations version: [[Arrangements and Combinations with Repetitions]]
