A **heuristic** for the [[Knight's Tour]]: always move to the square that has the **fewest onward moves**

- squares with few exits get cut off quickly if you don't visit them now
	- e.g. a corner has only 2 exits. If one gets used up, the knight can enter the corner but never leave
- trying these squares first makes [[Backtracking]] much faster

The opposite intuition (most onward moves first, to keep options open) also sounds reasonable. Often you can't tell which ordering is better in theory, so **implement both and test**: for the knight's tour, fewest onward moves wins
