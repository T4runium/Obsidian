f is differentiable at ${}x = x_{0}{}$ if $$\lim_{ x \to x_{0}} \frac{f(x) - f(x_{0})}{x - x_{0}}$$ exists

the formula for a derivative for a function $f(x)$ at point $x_{0}$is

$$
f'(x) = \lim_{ h \to 0 } \frac{f(x_{0} + h) - f(x_{0})}{h}  
$$
if $f(x)  = c$ then $f'(x) = 0 \forall x$
proof:

$$
\begin{aligned}
f'(x) &= \lim_{ h \to 0 } \frac{f(x_{0} + h) - f(x_{0})}{h}  \\
&= \lim_{ h \to 0 } \frac{c - c}{h} \\
&= \lim_{ h \to 0 } 0 \\
&= 0
\end{aligned}
$$

if $f(x) = x$ then $f'(x) = 1 \forall x$
proof:
$$
\begin{aligned}
f'(x) &= \lim_{ h \to 0 } \frac{f(x_{0} + h) - f(x_{0})}{h}  \\
&= \lim_{ h \to 0 }  \frac{(x_{0} + h) - (x_{0})}{h} \\
&= \lim_{ h \to 0 } 1 \\
&= 1
\end{aligned}
$$
if $f(x) = x^n$ then $f'(x) = nx^{n - 1} \forall x$

# Continuity
for $f: \mathbb{R}\to \mathbb{R}$,
$x$ is continuous at $a$ if 
$$
\lim_{ x \to a^- }  f(x) =  \lim_{ x \to a^+ f(x) = L } 
$$
and
$$
f(a) = L 
$$
If we can keep differentiating and function and still get
 a result, its a smooth function

# Product Rule

if $f(x)$ and $g(x)$ are differentiable at $x_0$, then
$$
\frac{d}{dx} f(x)g(x) = f'(x)g(x) + g'(x)f(x) \text{ at } x_{0}
$$

# Quotient Rule

if $f(x)$ and $g(x)$ are differentiable at $x_0$, then
$$
\frac{d}{dx} \frac{f(x)}{g(x)} = \frac{f'(x)g(x) - g'(x)f(x)}{(g(x))^2} \text{ at } x_0
$$


# Chain Rule
iif $f(x)$ and $g(x)$ are differentiable at $x_0$ and $g(x_{0})$ respectevily, then 

$$
\frac{d}{dx} f(g(x)) = \frac{df}{dg} \frac{dg}{dx} or f'(g(x))g'(x) \text{ at } x_{0}
$$