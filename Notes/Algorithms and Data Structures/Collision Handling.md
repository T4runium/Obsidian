A **collision** is when 2 keys hash to the same bucket in a [[Hash Tables|hash table]]

Many ways to handle collision. Includes:
- [[Separate Chaining]]
- [[Linear Probing]]
- [[Quadratic Probing]]
- [[Double Hashing]]

The last 3 are **open addressing** schemes: each bucket holds **at most one** entry, so on a collision we **probe** other buckets until we find an empty one

Deleting from an open addressing table needs [[Tombstones]]

# Comparison
- open addressing is **more memory efficient** than separate chaining
- but has a hard capacity limit: at most $N$ entries
- separate chaining is as fast or faster in practice and in theory
- $\therefore$ if memory isn't a big issue, use **separate chaining**
