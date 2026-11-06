If $n$ envelopes go into $m$ pigeon-holes and $n > m$, then some pigeon-hole has **more than one** envelope

The trick is choosing what the envelopes and the holes are
Same reason a [[Hash Tables|hash table]] with more keys than slots must have a [[Collision Handling|collision]]

# Examples
**Hairs:** ~280,000 people in Newcastle, at most 200,000 hairs each
holes: 0 to 200,000 hairs, so 200,001 holes < 280,000 people $\therefore$ two people have the same number of hairs

**League:** $n$ teams each play each other once, every team wins at least once
wins $\in \{1, \dots, n-1\}$: $n - 1$ holes for $n$ teams $\therefore$ two teams have the same number of wins

**Subset sums:** any 9 distinct numbers from $\{1, \dots, 60\}$ have two disjoint non-empty subsets with equal sums
- envelopes: $2^9 = 512$ subsets ([[Set Theory]])
- holes: sums from $0$ to $52 + 53 + \dots + 60 = 504$, i.e. 505 holes
- $512 > 505$ $\therefore$ two subsets have the same sum. Neither is $\emptyset$ (only $\emptyset$ sums to 0)
- remove their common elements: now disjoint, sums still equal
