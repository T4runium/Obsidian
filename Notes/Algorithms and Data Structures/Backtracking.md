**Backtracking**: a [[Recursion|recursive]] technique for problems with too many **candidate** solutions to try them all (e.g. there are about $6.67 \times 10^{21}$ ways to fill a sudoku grid)

**General idea**: build the solution one step at a time, and **back up** a step when you can't continue

Can be used to:
- **find one** solution: stop at the first complete one
- **enumerate all** solutions: when you find one, add it to a list and **keep searching**

Writing it recursively is much easier than iteratively: iterative code has to store all the unfinished partial solutions itself (in a stack or queue), whereas recursion does that for you

# Informal algorithm
1. Do I have a solution yet?
2. If not, can I extend my solution by one step?
3. If yes, do that
4. Do I have a solution now? If yes, done
5. If not, try to extend again
6. If I can't extend, go one step back and try a different way
7. If there are no other options left, give up: **no solution exists**

# Generic algorithm
```
extend_solution(current solution):
    if current solution is valid then
        if current solution is complete then
            return current solution
        else
            for each extension of the current solution do
                extend_solution(extension)
```
- an invalid partial solution is dropped straight away, which is what saves time compared with trying everything
- returning from a call **is** the backtrack: the loop moves on to the next extension
- the calls form a [[Recursion Tree]], explored depth first

To use it, answer 4 questions:
- what is a (partial) **solution**?
- when is it **valid**?
- when is it **complete**?
- how can it be **extended**?

# Sudoku
- **solution**: partially filled grid (start with the given numbers)
- **valid**: no row, column or $3 \times 3$ box repeats a digit
- **complete**: no blanks left
- **extend**: take the first empty cell and try each digit $1$–$9$

# Implementing it
Two ways to store the partial solution:
1. **One shared structure**: add a step, recurse, then **undo the step** when backtracking. Forgetting the undo is the classic bug
2. **Copy per call**: pass a copy (e.g. `copy.deepcopy`) to each recursive call, so nothing needs undoing
	- if you collect **all** solutions, you must append a **copy** of each one, or later changes will overwrite it

**Ordering** the extensions can make it much faster, e.g. [[Warnsdorff's Rule]]

Example: [[Knight's Tour]]
