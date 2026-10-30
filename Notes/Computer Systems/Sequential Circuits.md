Outputs depend on the history of values and the current values. 
the clock has 2 edges, rising edge (0 to 1) and the falling edge (1 to 0)

# Latches

Circuits that store 1 bit
Bi stable: 2 states $Q = 1$ or $0$
level sensitive: responds to the input not the clock
feedback: outputs are fed back into the input

# SR Latch
SR = Set Reset
Set makes $Q = 1 (\overline Q = 0)$
Reset makes $Q = 0 (\overline Q = 1)$

Problem: When $S$ and $R = 1$ both $Q$ and $\overline Q$ will be one which is illegal as either $Q$ or $\overline Q$ need to be $1$
Storage element without a clock is called Asynchronous

# D Latch
$2$ inputs: $D$ (data) and $EN$ (enable)
$EN$ is usually the clock

When $EN$ is $1$ $Q$ and $\overline Q$ get the value shown by $D$ at that instant
when $EN$ is $0$, $Q \overline Q$ don't change

Problem: Any changes to $D$ would go through, even a glitch

# D Flip Flop
Only looks at the rising edge

# Registers 

Row of **D flip flops** (one word long) that share one clock 
Grouped into register files, [[Encoders and Decoders#Multiplexer|multiplexers]] to read and [[Encoders and Decoders|decoders]] to write