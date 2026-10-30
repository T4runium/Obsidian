**Hash tables** stores pairs of data - the **key** and the **value**
**Keys** are unique and **values** are looked up using the **keys**

A hash table contains a **bucket array** and a **hash function**

a **bucket array** is an array $A$ of size $N$  (the capacity) where each call is a bucket storing a collection of pairs

the **hash function** $h$ maps each key $k$ to an integer $[0, N - 1]$ 
The key value pair $(k, v)$ is stored at $A[h(k)]$

2 keys pointing towards the same address causes a **collision**

# Hash Function

has 2 parts:
- **hash code** - keys to int
- **compression** - int to $[0, N - 1]$

**hash code** is applied first then the **compression **

the goal of the **hash function** is to disperse the keys in apparent random way aka scramble the keys uniformly. It should also be:
- efficiently computable
- each position should be equally likely

Examples of compression functions:
 - integer mod N
 - Multiple add and divide (MAD): $y$ maps to $ay + b$ mod $N$ where $a, b \in \mathbb{N}$
# Collision Handing
Many ways to handle collision. Includes:
- [[Hash Tables#Separate Chaining|Separate Chaining]]
- Linear Probing
- Quadratic Probing
- Double hashing

# Separate Chaining
Each bucket $A[i]$ stores  a list holding the entries $(k, v)$ such that $h(k) = i$
**Performance**:
- Cost $\propto$ length
- Average Length $= M/N$  | $M$ is amount of data
- Worst case: all keys hash to the same list

