---
course: [CAL1]
semester: "115-1"
chapter: ["1.7"]
tags: [calculus, homework, questions, limits]
source:
  - "Stewart, Calculus, §1.7 Exercises, pp. 81-82, scanned PDF with the assigned exercise numbers highlighted"
  - "The graph of Exercise 3 is redrawn from the scan"
created: 2026-10-02
solutions: "[[CAL1 HW 1.7 Solutions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> ST §1.7: 3, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 41, 43. These are the exercises whose numbers are highlighted in the scan. ST is Stewart, *Calculus*.
>
> Additional exercises, not assigned: 11, 24, 28, 32, 36, 37, 38, 39, 40, 42. They are at the bottom of this note and cover types of problems that the assigned exercises leave out.

## ST §1.7 The Precise Definition of a Limit

### ST 1.7.3
Use the given graph of $f(x) = \sqrt{x}$ to find a number $\delta$ such that
$$
\text{if} \quad \lvert x - 4 \rvert < \delta \quad \text{then} \quad \lvert \sqrt{x} - 2 \rvert < 0.4
$$

![ST 1.7.3 figure|380](../Attachments/CAL1%20HW%201.7%20Questions%20fig%203.svg)

### ST 1.7.13
- (a) Find a number $\delta$ such that if $\lvert x - 2 \rvert < \delta$, then $\lvert 4x - 8 \rvert < \varepsilon$, where $\varepsilon = 0.1$.
- (b) Repeat part (a) with $\varepsilon = 0.01$.

### ST 1.7.15
**15–18** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit and illustrate with a diagram like Figure 9.
$$
\lim_{x \to 4} \left(\tfrac{1}{2}x - 1\right) = 1
$$

### ST 1.7.17
**15–18** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit and illustrate with a diagram like Figure 9.
$$
\lim_{x \to -2} \, (-2x + 1) = 5
$$

### ST 1.7.19
**19–32** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit.
$$
\lim_{x \to 9} \left(1 - \tfrac{1}{3}x\right) = -2
$$

### ST 1.7.21
**19–32** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit.
$$
\lim_{x \to 4} \frac{x^2 - 2x - 8}{x - 4} = 6
$$

### ST 1.7.23
**19–32** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit.
$$
\lim_{x \to a} x = a
$$

### ST 1.7.25
**19–32** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit.
$$
\lim_{x \to 0} x^2 = 0
$$

### ST 1.7.27
**19–32** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit.
$$
\lim_{x \to 0} \, \lvert x \rvert = 0
$$

### ST 1.7.29
**19–32** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit.
$$
\lim_{x \to 2} \, (x^2 - 4x + 5) = 1
$$

### ST 1.7.31
**19–32** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit.
$$
\lim_{x \to -2} \, (x^2 - 1) = 3
$$

### ST 1.7.41
How close to $-3$ do we have to take $x$ so that
$$
\frac{1}{(x + 3)^4} > 10{,}000
$$

### ST 1.7.43
Prove that $\displaystyle \lim_{x \to -1^{-}} \frac{5}{(x + 1)^3} = -\infty$.

## ST §1.7 Additional Exercises

### ST 1.7.11
A machinist is required to manufacture a circular metal disk with area $1000 \text{ cm}^2$.
- (a) What radius produces such a disk?
- (b) If the machinist is allowed an error tolerance of $\pm 5 \text{ cm}^2$ in the area of the disk, how close to the ideal radius in part (a) must the machinist control the radius?
- (c) In terms of the $\varepsilon$, $\delta$ definition of $\lim_{x \to a} f(x) = L$, what is $x$? What is $f(x)$? What is $a$? What is $L$? What value of $\varepsilon$ is given? What is the corresponding value of $\delta$?

### ST 1.7.24
**19–32** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit.
$$
\lim_{x \to a} c = c
$$

### ST 1.7.28
**19–32** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit.
$$
\lim_{x \to -6^{+}} \sqrt[8]{6 + x} = 0
$$

### ST 1.7.32
**19–32** Prove the statement using the $\varepsilon$, $\delta$ definition of a limit.
$$
\lim_{x \to 2} x^3 = 8
$$

### ST 1.7.36
Prove that $\displaystyle \lim_{x \to 2} \frac{1}{x} = \frac{1}{2}$.

### ST 1.7.37
Prove that $\displaystyle \lim_{x \to a} \sqrt{x} = \sqrt{a}$ if $a > 0$.
$$
\left[\textit{Hint: } \text{Use } \left\lvert \sqrt{x} - \sqrt{a} \right\rvert = \frac{\lvert x - a \rvert}{\sqrt{x} + \sqrt{a}}.\right]
$$

### ST 1.7.38
If $H$ is the Heaviside function defined in Section 1.5, prove, using Definition 2, that $\lim_{t \to 0} H(t)$ does not exist. [*Hint:* Use an indirect proof as follows. Suppose that the limit is $L$. Take $\varepsilon = \tfrac{1}{2}$ in the definition of a limit and try to arrive at a contradiction.]

### ST 1.7.39
If the function $f$ is defined by
$$
f(x) = \begin{cases} 0 & \text{if } x \text{ is rational} \\ 1 & \text{if } x \text{ is irrational} \end{cases}
$$
prove that $\lim_{x \to 0} f(x)$ does not exist.

### ST 1.7.40
By comparing Definitions 2, 3, and 4, prove Theorem 1.6.1:
$$
\lim_{x \to a} f(x) = L \qquad \text{if and only if} \qquad \lim_{x \to a^{-}} f(x) = L = \lim_{x \to a^{+}} f(x)
$$

### ST 1.7.42
Prove, using Definition 6, that $\displaystyle \lim_{x \to -3} \frac{1}{(x + 3)^4} = \infty$.
