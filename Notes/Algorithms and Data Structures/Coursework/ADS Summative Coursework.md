**Summative** coursework for Algorithms and Data Structures (COMP1081)

# Key info
- **My code:** `/home/tarun/programming/year1/ADS/coursework1/`
- **Due:** Tue 15 Dec 2026, 14:00 (GMT), on **Gradescope**
- **34% of the module mark**, 6.8 credits, about 14 hours of work. Setter: Prof Thomas Erlebach
- Attempt everything, because incomplete answers get partial credit
- **Late:** capped at 40% for up to 5 working days, then 0%
- **AI:** allowed for research and preparation, but cite it, and the work must be substantially your own. If your IDE auto-suggests code and you keep it or use it, say how in a comment in the `.py` file
- Supplied files are in *Python-Supplementary.zip*: `q1/q2/q3/q7_supplementary.py`. **Don't modify** the `Node`, `LinkedGrid` or `HashTable` classes, and **don't include** them in your submission, because they're added at marking time

# What to submit
- **Two separate submission points**:
	1. **Python files:** `q1.py`, `q2.py`, `q3.py`, `q4.py`, `q7.py`, using the exact file and function names below. If you work in Jupyter, export to `.py`
	2. **Written answers:** one `solution.pdf` for Q5, Q6 and Q7(b). Typed or clearly handwritten. On Gradescope, tag which pages belong to which question
- Python is **autograded on a wider set of inputs than the supplied tests**, and efficiency may count

# Questions

| Q | Topic | File / functions | Marks |
| --- | --- | --- | --- |
| 1 | Coin-flip game (first `HTTH` wins), run-length encoding | `q1.py`: `compute_winner`, `encode`, `decode`, `compute_winner_compressed` | 10 |
| 2 | **Linked grids** (2D [[Types of Linked List\|linked lists]]) | `q2.py`: `fetch`, `equal_values`, `extract_row`, `extract_column`, `transpose`, `element_wise_multiply` | 20 |
| 3 | [[Hash Tables]], $h(k) = 7k + 11 \pmod{23}$, tombstones = `None` | `q3.py`: `hash_linear`, `hash_quadratic` | 10 |
| 4 | Recursion and backtracking: **Miller arrays** (each row and each column a permutation of $1..n$) | `q4.py`: `check_miller`, `all_miller` | 10 |
| 5 | Prove or disprove 5 asymptotic statements ($O, \Theta, o, \omega, \Omega$) | written | 10 |
| 6 | Master Theorem on 5 recurrences | written | 15 |
| 7 | **Merge4Sort**: 4-way, non-increasing MergeSort, plus complexity | `q7.py`: `Merge4Way`, `Merge4Sort` (a), written (b) | 25 |

## Q1: coin-flip game
- Player A and player B each flip a coin $n$ times, giving strings over $\{H, T\}$. Whoever's history contains `HTTH` at the earlier position wins. If neither contains it, or both first contain it at the same position, it's a draw (`'D'`)
- Compressed form: pairs of (character, single-digit count), e.g. `'H3T1'` = `HHHT`
- (a) `compute_winner` returns `'A'`, `'B'` or `'D'`. (b) `encode`. (c) `decode`. 2 marks each
- (d) `compute_winner_compressed` must work **directly on the compressed form**. Decoding and then running the same logic as (a) is banned, even if you copy the code in. Adapting the technique to work on compressed input is fine (2)
- **+2 marks** for a meaningful **recursive** implementation of at least one of the four. It must be in one of those four functions themselves: recursion in a helper doesn't count
- The tests won't hit Python's recursion limit

## Q2: linked grids
- Rows are numbered $1..$`sizeY` (top to bottom) and columns $1..$`sizeX` (left to right). **Indexing starts at 1**
- Only the head is stored, not the other three corners
- (a) `fetch(grid, i, j)` (2). (b) `equal_values` (3). Reusing `fetch` is allowed, but a linear-time solution may earn efficiency marks
- (c) `extract_row` and (d) `extract_column` remove the row or column from the original and return it as a new grid. **Reuse the existing nodes**, don't create new ones (4 each)
- (e) `transpose` modifies the grid in place, with no new nodes (4). (f) `element_wise_multiply` assumes both grids are the same size, and you may modify the inputs (3)

## Q3: hash tables
- $D$ is a list of operations: $+i$ inserts $i$ and $-i$ deletes $i$. It never inserts a duplicate and never deletes a missing key
- (a) **linear probing** (5). (b) **quadratic probing** $(h(k) + i^2) \bmod 23$ (5)
- If there's no free slot, skip that insert. Return the resulting `HashTable`
- You only store keys, not values. You still have to work out *where* each key goes yourself

## Q4: Miller arrays
- (a) `check_miller(A)` returns `True` or `False` (3)
- (b) `all_miller(n)` returns a list of all Miller arrays of size $n$, using **backtracking**. It's tested for $n = 2$ to at least $5$ (7)
- The autograder **times out after 10 minutes**, and slow code loses marks
- `import copy` is allowed (for `copy.deepcopy`)

## Q5 and Q6 (written)
- Q5: 5 statements at 2 marks each, 1 for the correct True/False verdict and 1 for the argument. See [[Fundamental definitions]]
- Q6: 5 recurrences at 3 marks each, 2 for the answer and 1 for the justification. If the Master Theorem doesn't apply, say why. For Case 3, show the regularity condition $af(n/b) \le cf(n)$ with $c < 1$

## Q7: Merge4Sort
- (a) `Merge4Way(L1, L2, L3, L4)` merges 4 lists sorted in **non-increasing** order. The lists can be any length, including empty (7)
- `Merge4Sort(L)`: if $|L| \le 1$, return `L`. If $2 \le |L| \le 4$, make **one** call to `Merge4Way` with sub-lists of length 1 or 0 and no recursion. Otherwise split into 4 parts whose sizes differ by at most 1, recurse on each, then merge (8)
- No sorting except your own functions
- (b)(i) Worst-case time of `Merge4Way` (total length $n$) and of `Merge4Sort`, as the tightest $O(f(n))$ with justification. Assume appending or removing an element is $O(1)$ and $4 \mid n$ (5)
- (b)(ii) **MergeRootSort**: $\sqrt{n}$ recursive calls on sub-lists of size $\sqrt{n}$, where merging costs $O(n \log n)$. Give the tightest bound with justification (5)

# Rules (brief + Q&A)
- **No `import` at all** in Q1–3 and Q7a. Q4 may `import copy` and nothing else
- **Built-in functions and methods are fine** (anything you can call without an import), e.g. string methods
- Helper functions are allowed in every question (explicitly so in Q4)
- Test code with `import random` is fine locally, but remove it or comment it out before submitting
- Plagiarism rules apply until the exam board in June 2027. Don't share your code, and cite any source other than the lecture notes

# Checklist
- [ ] Q1 (a–d) + recursive version
- [ ] Q2 (a–f), checking the 1-indexing and node reuse
- [ ] Q3 (a–b)
- [ ] Q4 (a–b), checking it runs quickly up to $n = 5$
- [ ] Q7a
- [ ] Run all supplementary tests, plus my own edge cases
- [ ] Strip imports and test code, and check file and function names
- [ ] `solution.pdf`: Q5, Q6, Q7b
- [ ] Submit the code **and** the PDF on Gradescope, and tag the PDF pages
- [ ] Recheck the Q&A thread before submitting
