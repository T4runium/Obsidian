The run of any [[Recursion|recursive]] function can be drawn as a **tree of function calls**
- the first call is the **root**
- the recursive calls a call makes are its **children**

The computer explores it **depth first**: it finishes the whole first subtree before starting the next one
- e.g. [[Fibonacci]]: $F(5)$ has children $F(4)$ and $F(3)$, and so on, which shows the repeated calls
- in [[Backtracking]], each node is a partial solution and each child is one extension. A node can have many children, e.g. 9 in sudoku (digits $1$–$9$)

# Example
Fill a $2 \times 2$ grid with $1$s and $2$s so no row or column repeats a number, with the top-left already given as $1$:
- the root tries the top-right cell with $1$ (✗, the top row repeats) and then $2$ (✓)
- from $\begin{bmatrix} 1 & 2 \\ \_ & \_ \end{bmatrix}$, try bottom-left $= 1$ (✗, the column repeats), then $2$ (✓)
- from $\begin{bmatrix} 1 & 2 \\ 2 & \_ \end{bmatrix}$, try bottom-right $= 1$ (✓ and complete) $\therefore$ solution $\begin{bmatrix} 1 & 2 \\ 2 & 1 \end{bmatrix}$

Invalid nodes are dead ends: they make no further calls
