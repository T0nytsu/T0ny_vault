---
course: [CAL1]
chapter: ["1.8"]
tags: [calculus, homework, questions, continuity]
source:
  - "Stewart, Calculus, §1.8 Exercises, pp. 92-94, scanned PDF"
  - "The graph of Exercise 3 is redrawn from the scan"
created: 2026-10-04
solutions: "[[CAL1 HW 1.8 Solutions]]"
---
> [!info] Coverage
> ST §1.8: 3, 13, 19, 21, 23, 25, 27, 29, 31, 35, 41, 45, 47, 49, 55. These are the exercises assigned for Section 1.8. ST is Stewart, *Calculus*.
>
> Additional exercises, not assigned: 17, 48, 50, 54, 64, 72, 73, 74, 76. They are at the bottom of this note and cover types of problems that the assigned exercises leave out.

## ST §1.8 Continuity

### ST 1.8.3
- (a) From the given graph of $f$, state the numbers at which $f$ is discontinuous and explain why.
- (b) For each of the numbers stated in part (a), determine whether $f$ is continuous from the right, or from the left, or neither.

![[CAL1 HW 1.8 Questions fig 3.png|480]]

### ST 1.8.13
**13–16** Use the definition of continuity and the properties of limits to show that the function is continuous at the given number $a$.
$$
f(x) = 3x^2 + (x + 2)^5, \qquad a = -1
$$

### ST 1.8.19
**19–24** Explain why the function is discontinuous at the given number $a$. Sketch the graph of the function.
$$
f(x) = \frac{1}{x + 2}, \qquad a = -2
$$

### ST 1.8.21
**19–24** Explain why the function is discontinuous at the given number $a$. Sketch the graph of the function.
$$
f(x) = \begin{cases} 1 - x^2 & \text{if } x < 1 \\ 1/x & \text{if } x \ge 1 \end{cases} \qquad a = 1
$$

### ST 1.8.23
**19–24** Explain why the function is discontinuous at the given number $a$. Sketch the graph of the function.
$$
f(x) = \begin{cases} \cos x & \text{if } x < 0 \\ 0 & \text{if } x = 0 \\ 1 - x^2 & \text{if } x > 0 \end{cases} \qquad a = 0
$$

### ST 1.8.25
**25–26**
- (a) Show that $f$ has a removable discontinuity at $x = 3$.
- (b) Redefine $f(3)$ so that $f$ is continuous at $x = 3$ (and thus the discontinuity is "removed").

$$
f(x) = \frac{x - 3}{x^2 - 9}
$$

### ST 1.8.27
**27–34** Explain, using Theorems 4, 5, 7, and 9, why the function is continuous at every number in its domain. State the domain.
$$
f(x) = \frac{x^2}{\sqrt{x^4 + 2}}
$$

### ST 1.8.29
**27–34** Explain, using Theorems 4, 5, 7, and 9, why the function is continuous at every number in its domain. State the domain.
$$
h(t) = \frac{\cos(t^2)}{1 - t^2}
$$

### ST 1.8.31
**27–34** Explain, using Theorems 4, 5, 7, and 9, why the function is continuous at every number in its domain. State the domain.
$$
L(v) = v\sqrt{9 - v^2}
$$

### ST 1.8.35
**35–38** Use continuity to evaluate the limit.
$$
\lim_{x \to 2} x\sqrt{20 - x^2}
$$

### ST 1.8.41
**41–42** Show that $f$ is continuous on $(-\infty, \infty)$.
$$
f(x) = \begin{cases} 1 - x^2 & \text{if } x \le 1 \\ \sqrt{x - 1} & \text{if } x > 1 \end{cases}
$$

### ST 1.8.45
**43–45** Find the numbers at which $f$ is discontinuous. At which of these numbers is $f$ continuous from the right, from the left, or neither? Sketch the graph of $f$.
$$
f(x) = \begin{cases} x + 2 & \text{if } x < 0 \\ 2x^2 & \text{if } 0 \le x \le 1 \\ 2 - x & \text{if } x > 1 \end{cases}
$$

### ST 1.8.47
For what value of the constant $c$ is the function $f$ continuous on $(-\infty, \infty)$?
$$
f(x) = \begin{cases} cx^2 + 2x & \text{if } x < 2 \\ x^3 - cx & \text{if } x \ge 2 \end{cases}
$$

### ST 1.8.49
Suppose $f$ and $g$ are continuous functions such that $g(2) = 6$ and $\lim_{x \to 2} \, [3f(x) + f(x)g(x)] = 36$. Find $f(2)$.

### ST 1.8.55
**55–58** Use the Intermediate Value Theorem to show that there is a solution of the given equation in the specified interval.
$$
-x^3 + 4x + 1 = 0, \qquad (-1, 0)
$$

## ST §1.8 Additional Exercises

### ST 1.8.17
**17–18** Use the definition of continuity and the properties of limits to show that the function is continuous on the given interval.
$$
f(x) = x + \sqrt{x - 4}, \qquad [4, \infty)
$$

### ST 1.8.48
Find the values of $a$ and $b$ that make $f$ continuous everywhere.
$$
f(x) = \begin{cases} \dfrac{x^2 - 4}{x - 2} & \text{if } x < 2 \\[6pt] ax^2 - bx + 3 & \text{if } 2 \le x < 3 \\ 2x - a + b & \text{if } x \ge 3 \end{cases}
$$

### ST 1.8.50
Let $f(x) = 1/x$ and $g(x) = 1/x^2$.
- (a) Find $(f \circ g)(x)$.
- (b) Is $f \circ g$ continuous everywhere? Explain.

### ST 1.8.54
Suppose $f$ is continuous on $[1, 5]$ and the only solutions of the equation $f(x) = 6$ are $x = 1$ and $x = 4$. If $f(2) = 8$, explain why $f(3) > 6$.

### ST 1.8.64
**63–64** Prove, without graphing, that the graph of the function has at least two $x$-intercepts in the specified interval.
$$
y = x^2 - 3 + 1/x, \qquad (0, 2)
$$

### ST 1.8.72
For what values of $x$ is $g$ continuous?
$$
g(x) = \begin{cases} 0 & \text{if } x \text{ is rational} \\ x & \text{if } x \text{ is irrational} \end{cases}
$$

### ST 1.8.73
Show that the function
$$
f(x) = \begin{cases} x^4 \sin(1/x) & \text{if } x \ne 0 \\ 0 & \text{if } x = 0 \end{cases}
$$
is continuous on $(-\infty, \infty)$.

### ST 1.8.74
If $a$ and $b$ are positive numbers, prove that the equation
$$
\frac{a}{x^3 + 2x^2 - 1} + \frac{b}{x^3 + x - 2} = 0
$$
has at least one solution in the interval $(-1, 1)$.

### ST 1.8.76
**Absolute Value and Continuity**
- (a) Show that the absolute value function $F(x) = \lvert x \rvert$ is continuous everywhere.
- (b) Prove that if $f$ is a continuous function on an interval, then so is $\lvert f \rvert$.
- (c) Is the converse of the statement in part (b) also true? In other words, if $\lvert f \rvert$ is continuous, does it follow that $f$ is continuous? If so, prove it. If not, find a counterexample.
