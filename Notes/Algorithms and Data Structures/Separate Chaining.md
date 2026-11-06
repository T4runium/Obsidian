[[Collision Handling]] method: each bucket $A[i]$ stores  a list holding the entries $(k, v)$ such that $h(k) = i$

**Performance**:
- Cost $\propto$ length
- Average Length $= M/N$  | $M$ is amount of data
- Worst case: all keys hash to the same list
