# Half Adder
For bits A, B and output C (carry) and sum S

$S = A \oplus B\\ C = A.B$

This only works for the first bit. Therefore, we have full adders

# Full Adder

For inputs A, B and $C_{in}$ (from the previous adder) and outputs sum S and $C_{out}$

$$
S = A \oplus B \oplus C_{in} \\
C_{out} = (A.B) + (B.C) + (A.C)
$$

For k boolean inputs there are $2^{2^k}$  possible logic functions

# Ripple Carry Adder

Ripple carry adders are just full adders stacked on top of each others to accommodate more bits.

n bits = n full adders

gate delay $\approx 2n$

# Subtraction

$A$ subtract $B$ = $A$ add $\overline B$ + 1 (2's complement)



