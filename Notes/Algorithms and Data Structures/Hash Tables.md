**Hash tables** stores pairs of data - the **key** and the **value**
**Keys** are unique and **values** are looked up using the **keys**

A hash table contains a **bucket array** and a **[[Hash Functions|hash function]]**

a **bucket array** is an array $A$ of size $N$  (the capacity) where each cell is a bucket storing a collection of pairs

the **hash function** $h$ maps each key $k$ to an integer $[0, N - 1]$ 
The key value pair $(k, v)$ is stored at $A[h(k)]$

2 keys pointing towards the same address causes a **collision** (so $h$ is not [[Functions|injective]]), see [[Collision Handling]]
