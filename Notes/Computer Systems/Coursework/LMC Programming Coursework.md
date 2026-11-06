**Summative** coursework for Computer Systems (COMP1071): *Two sequences using decimal digits*

# Key info
- **Due:** Tue 1 Dec 2026, 14:00 (GMT), on Ultra (*LMC Programming Submission Point*)
- 5 credits, about 10 hours of work. Setter: Dr Carlton Shepherd
- **Submit:** one plain text file named exactly `lmcCOMP1071.txt` containing **commented** LMC assembly
- It must open, compile and run in the LMC Assembly Editor **with no changes**, because marking is mostly automatic
- Supplied files: `test1.txt` to `test4.txt` (one test each) and `testAll.txt` (10 tests run back to back), in *Coursework Additional Files.zip*
- **Unlimited attempts**, and the last marked attempt counts
- **Late:** capped at 40% for up to 5 working days, then 0%. Doesn't apply if you have an approved extension
- **AI:** allowed for research and preparation, but cite it, and the work must be substantially your own

# Task
- Read two integers $a, b \in [0, 999]$. **Read both before outputting anything**
- Each one starts a sequence: next term $=$ current term $-$ (sum of its decimal digits)
	- e.g. $57 \to 57 - 12 = 45 \to 36 \to 27 \to 18 \to 9 \to 0$
- Each round, output sequence A's term and then sequence B's term, starting with the inputs themselves
- Once a sequence hits $0$, keep outputting $0$ for it
- **Halt** straight after the first round where both are $0$. No extra outputs

| Input | Output |
| --- | --- |
| 0, 0 | 0, 0 |
| 0, 7 | 0, 7, 0, 0 |
| 12, 30 | 12, 30, 9, 27, 0, 18, 0, 9, 0, 0 |

# Gotchas
- **Re-runnable:** after HLT the PC is reset to 0 and the next pair is fed in **without recompiling**. Every variable must be re-initialised at the start, because the mailboxes aren't cleared
- The whole program must fit in **100 mailboxes**
- The supplied tests cover only a few cases, so write your own: $0$, $a = b$, 1/2/3-digit numbers, either sequence finishing first, and consecutive runs with different pairs
- Speed is measured on an **unseen** script (not `testAll.txt`), so don't optimise just for the examples

# Marking

| Criterion | Marks |
| --- | --- |
| Correctness and robustness (unseen tests, re-run without recompiling) | 64 |
| Speed efficiency (fewer cycles is better) | 25 |
| Comments (what each part does, plus key details) | 10 |

- The parts add up to 99 but the stated total is 100. The speed bands are also listed as 0–10, 11–20 and 21–30, which doesn't match 25. **Ask the setter**
- Speed marks normally go only to programs that pass the unseen tests
- If a program fails, it may still get partial marks from reading the code and comments, but nobody will fix it for you
- Week 6 lecture material has examples of well-commented code

# Related
[[Introductions to Number Systems]], [[Adding and Subtraction]]

# Checklist
- [ ] Digit-sum routine (no DIV in LMC, so repeatedly subtract 100s and then 10s)
- [ ] Main loop with alternating output and the halt condition
- [ ] Re-initialise every variable at the start
- [ ] Pass test1–4 and testAll, plus my own edge cases
- [ ] Optimise the cycle count
- [ ] Comment it properly
- [ ] Submit `lmcCOMP1071.txt` before 1 Dec, 14:00
