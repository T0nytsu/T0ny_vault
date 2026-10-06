---
course: [CAL1]
chapter: ["2.2"]
tags: [calculus, homework, questions, derivatives]
source:
  - "Stewart, Calculus, §2.2 Exercises, pp. 128-133, scanned PDF"
  - "The graphs of Exercises 3, 39, 41, 45 and 47 are redrawn from the scan"
created: 2026-10-05
solutions: "[[CAL1 HW 2.2 Solutions]]"
---
> [!info] Coverage
> ST §2.2: 3, 19, 23, 27, 39, 41, 45, 47, 55, 57, 59, 63. These are the exercises assigned for Section 2.2. ST is Stewart, *Calculus*.
>
> Additional exercises, not assigned: 29, 37, 53, 58, 61, 62. They are at the bottom of this note and cover types of problems that the assigned exercises leave out.

## ST §2.2 The Derivative as a Function

### ST 2.2.3
Match the graph of each function in (a)–(d) with the graph of its derivative in I–IV. Give reasons for your choices.

![[CAL1 HW 2.2 Questions fig 3.png|440]]

### ST 2.2.19
**19–30** Find the derivative of the function using the definition of derivative. State the domain of the function and the domain of its derivative.
$$
f(x) = 3x - 8
$$

### ST 2.2.23
**19–30** Find the derivative of the function using the definition of derivative. State the domain of the function and the domain of its derivative.
$$
A(p) = 4p^3 + 3p
$$

### ST 2.2.27
**19–30** Find the derivative of the function using the definition of derivative. State the domain of the function and the domain of its derivative.
$$
g(u) = \frac{u + 1}{4u - 1}
$$

### ST 2.2.39
**39–42** The graph of $f$ is given. State, with reasons, the numbers at which $f$ is *not* differentiable.

![[CAL1 HW 2.2 Questions fig 39.png|440]]

### ST 2.2.41
**39–42** The graph of $f$ is given. State, with reasons, the numbers at which $f$ is *not* differentiable.

![[CAL1 HW 2.2 Questions fig 41.png|440]]

### ST 2.2.45
**45–46** The graphs of a function $f$ and its derivative $f'$ are shown. Which is bigger, $f'(-1)$ or $f''(1)$?

![[CAL1 HW 2.2 Questions fig 45.png|400]]

### ST 2.2.47
The figure shows the graphs of $f$, $f'$, and $f''$. Identify each curve, and explain your choices.

![[CAL1 HW 2.2 Questions fig 47.png|440]]

### ST 2.2.55
Let $f(x) = \sqrt[3]{x}$.
- (a) If $a \ne 0$, use Equation 2.1.5 to find $f'(a)$.
- (b) Show that $f'(0)$ does not exist.
- (c) Show that $y = \sqrt[3]{x}$ has a vertical tangent line at $(0, 0)$. (Recall the shape of the graph of $f$. See Figure 1.2.13.)

### ST 2.2.57
Show that the function $f(x) = \lvert x - 6 \rvert$ is not differentiable at $6$. Find a formula for $f'$ and sketch its graph.

### ST 2.2.59
- (a) Sketch the graph of the function $f(x) = x\lvert x \rvert$.
- (b) For what values of $x$ is $f$ differentiable?
- (c) Find a formula for $f'$.

### ST 2.2.63
**62–63 Left- and Right-Hand Derivatives** The *left-hand* and *right-hand derivatives* of $f$ at $a$ are defined by
$$
f'_{-}(a) = \lim_{h \to 0^{-}} \frac{f(a + h) - f(a)}{h}
$$
and
$$
f'_{+}(a) = \lim_{h \to 0^{+}} \frac{f(a + h) - f(a)}{h}
$$
if these limits exist. Then $f'(a)$ exists if and only if these one-sided derivatives exist and are equal.

Let
$$
f(x) = \begin{cases} 0 & \text{if } x \le 0 \\[4pt] 5 - x & \text{if } 0 < x < 4 \\[4pt] \dfrac{1}{5 - x} & \text{if } x \ge 4 \end{cases}
$$
- (a) Find $f'_{-}(4)$ and $f'_{+}(4)$.
- (b) Sketch the graph of $f$.
- (c) Where is $f$ discontinuous?
- (d) Where is $f$ not differentiable?

## ST §2.2 Additional Exercises

### ST 2.2.29
**19–30** Find the derivative of the function using the definition of derivative. State the domain of the function and the domain of its derivative.
$$
f(x) = \frac{1}{\sqrt{1 + x}}
$$

### ST 2.2.37
Let $P$ represent the percentage of a city's electrical power that is produced by solar panels $t$ years after January 1, 2020.
- (a) What does $dP/dt$ represent in this context?
- (b) Interpret the statement
$$
\left.\frac{dP}{dt}\right\rvert_{t = 2} = 3.5
$$

### ST 2.2.53
If $f(x) = 2x^2 - x^3$, find $f'(x)$, $f''(x)$, $f'''(x)$, and $f^{(4)}(x)$. Graph $f$, $f'$, $f''$, and $f'''$ on a common screen. Are the graphs consistent with the geometric interpretations of these derivatives?

### ST 2.2.58
Where is the greatest integer function $f(x) = [\![ x ]\!]$ not differentiable? Find a formula for $f'$ and sketch its graph.

### ST 2.2.61
**Derivatives of Even and Odd Functions** Recall that a function $f$ is called *even* if $f(-x) = f(x)$ for all $x$ in its domain and *odd* if $f(-x) = -f(x)$ for all such $x$. Prove each of the following.
- (a) The derivative of an even function is an odd function.
- (b) The derivative of an odd function is an even function.

### ST 2.2.62
**62–63 Left- and Right-Hand Derivatives** (The definitions of $f'_{-}(a)$ and $f'_{+}(a)$ are stated in [[#ST 2.2.63]].)

Find $f'_{-}(0)$ and $f'_{+}(0)$ for the given function $f$. Is $f$ differentiable at $0$?
- (a) $f(x) = \begin{cases} 0 & \text{if } x \le 0 \\ x & \text{if } x > 0 \end{cases}$
- (b) $f(x) = \begin{cases} 0 & \text{if } x \le 0 \\ x^2 & \text{if } x > 0 \end{cases}$
