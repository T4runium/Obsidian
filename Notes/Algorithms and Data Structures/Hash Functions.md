A **hash function** $h$ maps each key $k$ to an integer in $[0, N - 1]$, used as the index into the bucket array of a [[Hash Tables|hash table]]

has 2 parts:
- **hash code** - keys to int
- **compression** - int to $[0, N - 1]$

**hash code** is applied first then the **compression**

the goal of the **hash function** is to disperse the keys in apparent random way aka scramble the keys uniformly. It should also be:
- efficiently computable
- each position should be equally likely

Examples of compression functions:
 - integer mod N
 - Multiply add and divide (MAD): $y$ maps to $ay + b$ mod $N$ where $a, b \in \mathbb{N}$
