[[Recursion|Recursive]] sum of a list $L$ of integers:
```
listsum(L):
    if len(L) = 1 then return L[0]
    else return L[0] + listsum(L[1:])
```
Base case is a 1-element list. Each call removes the first element

Iterative version: `sum = 0`, add each `i in L`
