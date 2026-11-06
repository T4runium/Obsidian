**Memoization**: store the result of a computation so it can be looked up later instead of recomputed

- e.g. recursive [[Fibonacci]] recomputes the same $F(k)$ many times
- works because the result for an argument never changes
- [[Hash Tables]] are a good structure for it (key = argument, value = result)
