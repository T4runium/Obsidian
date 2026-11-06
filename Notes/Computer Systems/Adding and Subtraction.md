# Half Adder
For bits A, B and output C (carry) and sum S

$S = A \oplus B\\ C = A.B$

This only works for the first bit. Therefore, we have full adders

# Full Adder

For inputs A, B and $C_{in}$ (from the previous adder) and outputs sum S and $C_{out}$

$$
S = A \oplus B \oplus C_{in} \\
C_{out} = (A.B) + (B.C_{in}) + (A.C_{in})
$$

For k boolean inputs there are $2^{2^k}$  possible logic functions ($2^k$ rows in the truth table, each output 0 or 1: [[Arrangements#Standard Problem 1|SP1]] twice)

# Ripple Carry Adder

Ripple carry adders are just full adders stacked on top of each other to accommodate more bits.

n bits = n full adders

gate delay $\approx 2n$

# Subtraction

$A$ subtract $B$ = $A$ add $\overline B$ + 1 (2's complement)



