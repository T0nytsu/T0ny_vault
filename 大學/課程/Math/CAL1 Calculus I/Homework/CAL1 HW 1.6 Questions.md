---
course: [CAL1]
semester: "115-1"
chapter: ["1.6"]
tags: [calculus, homework, questions, limits]
source:
  - "Stewart, Calculus, §1.6 Exercises, pp. 70-72, scanned PDF"
created: 2026-11-16
solutions: "[[CAL1 HW 1.6 Solutions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> ST §1.6: 1, 5, 7, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 39, 41, 43, 45, 47, 49, 51, 53, 55, 59, 65, 67. Solutions: [[CAL1 HW 1.6 Solutions]].

## ST §1.6 Calculating Limits Using the Limit Laws

### ST 1.6.1
Given that
$$
\lim_{x \to 2} f(x) = 4 \qquad \lim_{x \to 2} g(x) = -2 \qquad \lim_{x \to 2} h(x) = 0
$$
find the limits that exist. If the limit does not exist, explain why.
- (a) $\displaystyle\lim_{x \to 2} [f(x) + 5g(x)]$
- (b) $\displaystyle\lim_{x \to 2} [g(x)]^3$
- (c) $\displaystyle\lim_{x \to 2} \sqrt{f(x)}$
- (d) $\displaystyle\lim_{x \to 2} \frac{3f(x)}{g(x)}$
- (e) $\displaystyle\lim_{x \to 2} \frac{g(x)}{h(x)}$
- (f) $\displaystyle\lim_{x \to 2} \frac{g(x)h(x)}{f(x)}$

### ST 1.6.5
**3–9** Evaluate the limit and justify each step by indicating the appropriate Limit Law(s).
$$
\lim_{v \to 2} (v^2 + 2v)(2v^3 - 5)
$$

### ST 1.6.7
**3–9** Evaluate the limit and justify each step by indicating the appropriate Limit Law(s).
$$
\lim_{u \to -2} \sqrt{9 - u^3 + 2u^2}
$$

### ST 1.6.11
**11–34** Evaluate the limit, if it exists.
$$
\lim_{x \to -2} (3x - 7)
$$

### ST 1.6.13
**11–34** Evaluate the limit, if it exists.
$$
\lim_{t \to 4} \frac{t^2 - 2t - 8}{t - 4}
$$

### ST 1.6.15
**11–34** Evaluate the limit, if it exists.
$$
\lim_{x \to 2} \frac{x^2 + 5x + 4}{x - 2}
$$

### ST 1.6.17
**11–34** Evaluate the limit, if it exists.
$$
\lim_{x \to -2} \frac{x^2 - x - 6}{3x^2 + 5x - 2}
$$

### ST 1.6.19
**11–34** Evaluate the limit, if it exists.
$$
\lim_{t \to 3} \frac{t^3 - 27}{t^2 - 9}
$$

### ST 1.6.21
**11–34** Evaluate the limit, if it exists.
$$
\lim_{h \to 0} \frac{(h - 3)^2 - 9}{h}
$$

### ST 1.6.23
**11–34** Evaluate the limit, if it exists.
$$
\lim_{h \to 0} \frac{\sqrt{9 + h} - 3}{h}
$$

### ST 1.6.25
**11–34** Evaluate the limit, if it exists.
$$
\lim_{x \to 3} \frac{\dfrac{1}{x} - \dfrac{1}{3}}{x - 3}
$$

### ST 1.6.27
**11–34** Evaluate the limit, if it exists.
$$
\lim_{t \to 0} \frac{\sqrt{1 + t} - \sqrt{1 - t}}{t}
$$

### ST 1.6.29
**11–34** Evaluate the limit, if it exists.
$$
\lim_{x \to 16} \frac{4 - \sqrt{x}}{16x - x^2}
$$

### ST 1.6.31
**11–34** Evaluate the limit, if it exists.
$$
\lim_{t \to 0} \left(\frac{1}{t\sqrt{1 + t}} - \frac{1}{t}\right)
$$

### ST 1.6.33
**11–34** Evaluate the limit, if it exists.
$$
\lim_{h \to 0} \frac{(x + h)^3 - x^3}{h}
$$

### ST 1.6.39
If $4x - 9 \le f(x) \le x^2 - 4x + 7$ for $x \ge 0$, find $\lim_{x \to 4} f(x)$.

### ST 1.6.41
Prove that $\displaystyle\lim_{x \to 0} x^4 \cos\frac{2}{x} = 0$.

### ST 1.6.43
**43–48** Find the limit, if it exists. If the limit does not exist, explain why.
$$
\lim_{x \to -4} (\lvert x + 4 \rvert - 2x)
$$

### ST 1.6.45
**43–48** Find the limit, if it exists. If the limit does not exist, explain why.
$$
\lim_{x \to 0.5^{-}} \frac{2x - 1}{\lvert 2x^3 - x^2 \rvert}
$$

### ST 1.6.47
**43–48** Find the limit, if it exists. If the limit does not exist, explain why.
$$
\lim_{x \to 0^{-}} \left(\frac{1}{x} - \frac{1}{\lvert x \rvert}\right)
$$

### ST 1.6.49
**The Signum Function** The *signum* (or sign) *function*, denoted by sgn, is defined by
$$
\operatorname{sgn} x = \begin{cases} -1 & \text{if } x < 0 \\ 0 & \text{if } x = 0 \\ 1 & \text{if } x > 0 \end{cases}
$$
**(a)** Sketch the graph of this function.

**(b)** Find each of the following limits or explain why it does not exist.
- (i) $\displaystyle\lim_{x \to 0^{+}} \operatorname{sgn} x$
- (ii) $\displaystyle\lim_{x \to 0^{-}} \operatorname{sgn} x$
- (iii) $\displaystyle\lim_{x \to 0} \operatorname{sgn} x$
- (iv) $\displaystyle\lim_{x \to 0} \lvert \operatorname{sgn} x \rvert$

### ST 1.6.51
Let
$$
g(x) = \frac{x^2 + x - 6}{\lvert x - 2 \rvert}.
$$
**(a)** Find
- (i) $\displaystyle\lim_{x \to 2^{+}} g(x)$
- (ii) $\displaystyle\lim_{x \to 2^{-}} g(x)$

**(b)** Does $\lim_{x \to 2} g(x)$ exist?

**(c)** Sketch the graph of $g$.

### ST 1.6.53
Let
$$
B(t) = \begin{cases} 4 - \tfrac{1}{2}t & \text{if } t < 2 \\ \sqrt{t + c} & \text{if } t \ge 2 \end{cases}
$$
Find the value of $c$ so that $\lim_{t \to 2} B(t)$ exists.

### ST 1.6.55
**(a)** If the symbol $[\![\ ]\!]$ denotes the greatest integer function defined in Example 10, evaluate
- (i) $\displaystyle\lim_{x \to -2^{+}} [\![ x ]\!]$
- (ii) $\displaystyle\lim_{x \to -2} [\![ x ]\!]$
- (iii) $\displaystyle\lim_{x \to -2.4} [\![ x ]\!]$

**(b)** If $n$ is an integer, evaluate
- (i) $\displaystyle\lim_{x \to n^{-}} [\![ x ]\!]$
- (ii) $\displaystyle\lim_{x \to n^{+}} [\![ x ]\!]$

**(c)** For what values of $a$ does $\lim_{x \to a} [\![ x ]\!]$ exist?

### ST 1.6.59
If $p$ is a polynomial, show that $\lim_{x \to a} p(x) = p(a)$.

### ST 1.6.65
Show by means of an example that $\lim_{x \to a} [f(x)g(x)]$ may exist even though neither $\lim_{x \to a} f(x)$ nor $\lim_{x \to a} g(x)$ exists.

### ST 1.6.67
Is there a number $a$ such that
$$
\lim_{x \to -2} \frac{3x^2 + ax + a + 3}{x^2 + x - 2}
$$
exists? If so, find the value of $a$ and the value of the limit.
