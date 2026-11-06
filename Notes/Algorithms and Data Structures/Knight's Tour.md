A **knight** moves 1 square in one direction and 2 in the perpendicular direction, so it has up to 8 moves
**Knight's tour**: move a knight round the board visiting every square **exactly once** (usually starting top left)
**Closed tour**: the last square is one knight move from the start, so it could jump back

Solved with [[Backtracking]] by answering the 4 questions:
- **solution**: list of squares visited, in order
- **valid**: the newest move stays **on the board** and lands on an **unvisited** square
- **complete**: number of squares visited $=$ number of squares ($64$ on $8 \times 8$)
- **extend**: from the last square, try each of the 8 possible moves

```
extend_solution(current solution):
    if new move is to an unvisited square on the board then
        if every square has been visited then
            return current solution
        else
            for each of 8 possible moves do
                extend_solution(with move added)
```

# Implementation
- board array: $0$ = unvisited, $1$ = start, $2$ = 2nd square, ... (stores the order instead of a list of moves)
- pass a **count** of moves made, so you don't recount the board each time
- the 8 moves are stored as $(dx, dy)$ pairs
- helpers: `on_board(loc)`, `apply_move(loc, move)`, `unvisited(loc)`

```python
def extend_solution(loc, count):
    if not (on_board(loc) and unvisited(loc)):
        return False
    row, col = loc
    board[row][col] = count          # make the move
    if count == BOARD_SIZE ** 2:
        return True                  # complete tour
    for move in KNIGHT_MOVES:
        if extend_solution(apply_move(loc, move), count + 1):
            return True
    board[row][col] = 0              # BACKTRACK: undo the move
    return False

extend_solution((0, 0), 1)
```
- returns `True`/`False` and prints the board, instead of returning the solution
- forgetting `board[row][col] = 0` is the classic bug: the square stays "visited" after backtracking
- **closed tour**: only count it as complete if the last square is a knight move from $(0, 0)$

**Speed**: found a $6 \times 6$ tour in about 4s in the lecture. $8 \times 8$ is slow and $100 \times 100$ is hopeless, because the running time grows very fast with board size
- fix: try moves in a smarter order, see [[Warnsdorff's Rule]]
