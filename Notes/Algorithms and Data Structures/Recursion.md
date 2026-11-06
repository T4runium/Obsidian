A **recursive algorithm** calls itself to do part of its work. It must:
- have a **base case**
- **change state** and move towards the base case
- **call itself**

Idea: split the problem into a smaller copy of itself plus a bit of extra work

Examples: [[Factorial]], [[Sum of a List]], [[Fibonacci]], [[Flood Fill]]
Techniques built on it: [[Memoization]], [[Backtracking]]
Visualise a run with a [[Recursion Tree]]

# Exam
Past exam question (May): given a recursive formula like [[Fibonacci]],
- compute a value by hand (e.g. $P(10)$)
- write **recursive** pseudocode for it
- write **iterative** pseudocode using only a **queue**
