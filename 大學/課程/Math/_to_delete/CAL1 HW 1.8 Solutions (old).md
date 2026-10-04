---
course: [CAL1]
chapter: ["1.8"]
tags: [calculus, homework, solutions, continuity]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-10-04
questions: "[[CAL1 HW 1.8 Questions]]"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 1.8 Questions#ST 1.8.3\|ST 1.8.3]] | (a) $-4$ ($f(-4)$ is not defined); $-2$, $2$ and $4$ (the limit does not exist). (b) $-4$: neither; $-2$: from the left; $2$ and $4$: from the right |
| [[CAL1 HW 1.8 Questions#ST 1.8.13\|ST 1.8.13]] | Proof: $\lim_{x \to -1} f(x) = 4 = f(-1)$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.19\|ST 1.8.19]] | $f(-2)$ is not defined (infinite discontinuity); graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.21\|ST 1.8.21]] | $\lim_{x \to 1^{-}} f(x) = 0 \ne 1 = \lim_{x \to 1^{+}} f(x)$, so $\lim_{x \to 1} f(x)$ does not exist (jump discontinuity); graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.23\|ST 1.8.23]] | $\lim_{x \to 0} f(x) = 1 \ne 0 = f(0)$ (removable discontinuity); graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.25\|ST 1.8.25]] | (a) $\lim_{x \to 3} f(x) = \tfrac{1}{6}$ exists, but $f(3)$ is not defined; (b) $f(3) = \tfrac{1}{6}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.27\|ST 1.8.27]] | Domain $\mathbb{R} = (-\infty, \infty)$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.29\|ST 1.8.29]] | Domain $(-\infty, -1) \cup (-1, 1) \cup (1, \infty)$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.31\|ST 1.8.31]] | Domain $[-3, 3]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.35\|ST 1.8.35]] | $8$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.41\|ST 1.8.41]] | Proof: $\lim_{x \to 1^{-}} f(x) = \lim_{x \to 1^{+}} f(x) = 0 = f(1)$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.45\|ST 1.8.45]] | Discontinuous at $0$ and $1$; continuous from the right at $0$ and from the left at $1$; graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.47\|ST 1.8.47]] | $c = \tfrac{2}{3}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.49\|ST 1.8.49]] | $f(2) = 4$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.55\|ST 1.8.55]] | Proof: Intermediate Value Theorem on $[-1, 0]$, where $f(-1) = -2 < 0 < 1 = f(0)$ |

Additional exercises, not assigned:

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 1.8 Questions#ST 1.8.17\|ST 1.8.17]] | Proof: $\lim_{x \to a} f(x) = f(a)$ for $a > 4$, and $\lim_{x \to 4^{+}} f(x) = 4 = f(4)$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.48\|ST 1.8.48]] | $a = b = \tfrac{1}{2}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.50\|ST 1.8.50]] | (a) $(f \circ g)(x) = x^2$ for $x \ne 0$; (b) No: $f \circ g$ is not defined at $0$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.54\|ST 1.8.54]] | Indirect proof with the Intermediate Value Theorem on $[2, 3]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.64\|ST 1.8.64]] | Proof: $f\left(\tfrac{1}{4}\right) > 0$, $f(1) < 0$, $f(2) > 0$; Intermediate Value Theorem on $\left[\tfrac{1}{4}, 1\right]$ and on $[1, 2]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.72\|ST 1.8.72]] | Only at $x = 0$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.73\|ST 1.8.73]] | Proof: Theorems 4, 5, 7 and 9 for $a \ne 0$, Squeeze Theorem at $0$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.74\|ST 1.8.74]] | Proof: Intermediate Value Theorem for $p(x) = a(x^3 + x - 2) + b(x^3 + 2x^2 - 1)$ on $[-1, 1]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.76\|ST 1.8.76]] | (a), (b) Proofs; (c) No: $f(x) = 1$ for $x \ge 0$ and $f(x) = -1$ for $x < 0$ |

## ST §1.8 Continuity

> [!note] Note
> Definitions and theorems of ST §1.8, and facts about limits from ST §1.6, used below. A number without a section, such as Definition 1 or Theorem 4, refers to ST §1.8. The scan holds only the exercise pages, so these statements are written from the standard text of ST §1.8 and not copied from the scan; compare the numbers with the book.
> - **Definition 1** ([[Continuity|continuity]] at a number): $f$ is *continuous at a number* $a$ if $\lim_{x \to a} f(x) = f(a)$. This asks for three things: $f(a)$ is defined, $\lim_{x \to a} f(x)$ exists, and the two numbers are equal. If $f$ is defined near $a$ but is not continuous at $a$, then $f$ is *discontinuous at* $a$.
> - **Kinds of [[Discontinuity|discontinuity]]**: *removable* ($\lim_{x \to a} f(x)$ exists, but $f(a)$ is not defined or is a different number, so redefining $f$ at the single number $a$ removes it), *infinite* (a one-sided limit at $a$ is $\infty$ or $-\infty$, see [[Infinite Limit]]), and *jump* (both one-sided limits exist but are different).
> - **Definition 2**: $f$ is *continuous from the right* at $a$ if $\lim_{x \to a^{+}} f(x) = f(a)$, and *continuous from the left* at $a$ if $\lim_{x \to a^{-}} f(x) = f(a)$.
> - **Definition 3**: $f$ is *continuous on an interval* if it is continuous at every number in the interval. At an endpoint where $f$ is defined on one side only, continuous means continuous from the right or continuous from the left.
> - **Theorem 4**: If $f$ and $g$ are continuous at $a$ and $c$ is a constant, then these functions are also continuous at $a$: (1) $f + g$, (2) $f - g$, (3) $cf$, (4) $fg$, (5) $\tfrac{f}{g}$ if $g(a) \ne 0$.
> - **Theorem 5**: (a) Every polynomial is continuous on $\mathbb{R} = (-\infty, \infty)$. (b) Every rational function is continuous at every number in its domain.
> - **Theorem 7**: Polynomials, rational functions, root functions and trigonometric functions are continuous at every number in their domains.
> - **Theorem 8**: If $f$ is continuous at $b$ and $\lim_{x \to a} g(x) = b$, then $\lim_{x \to a} f(g(x)) = f(b)$.
> - **Theorem 9**: If $g$ is continuous at $a$ and $f$ is continuous at $g(a)$, then the composite function $f \circ g$ is continuous at $a$.
> - **Theorem 10** (the [[Intermediate Value Theorem]]): Suppose that $f$ is continuous on the closed interval $[a, b]$ and that $N$ is a number between $f(a)$ and $f(b)$, where $f(a) \ne f(b)$. Then there is a number $c$ in $(a, b)$ such that $f(c) = N$.
> - **Limit Laws** (ST §1.6): the Sum, Difference, Constant Multiple, Product, Quotient, Power and Root Laws, together with $\lim_{x \to a} c = c$ and $\lim_{x \to a} x = a$. They also hold for one-sided limits.
> - **Theorem 1.6.1**: $\lim_{x \to a} f(x) = L$ if and only if $\lim_{x \to a^{-}} f(x) = L = \lim_{x \to a^{+}} f(x)$ (see [[One-Sided Limit]]).
> - **The [[Squeeze Theorem]]** (ST §1.6): If $f(x) \le g(x) \le h(x)$ when $x$ is near $a$ (except possibly at $a$) and $\lim_{x \to a} f(x) = \lim_{x \to a} h(x) = L$, then $\lim_{x \to a} g(x) = L$.
> - **Limits depend only on nearby values**: $\lim_{x \to a} f(x)$ depends only on the values $f(x)$ for $x$ near $a$ with $x \ne a$. So if $f(x) = p(x)$ for all $x$ in an open interval that contains $a$ and $p$ is continuous at $a$, then $f$ is continuous at $a$. For a function defined by cases, the limit from the left is computed with the formula valid to the left of $a$, and the limit from the right with the formula valid to the right of $a$.

### ST 1.8.3
Question: [[CAL1 HW 1.8 Questions#ST 1.8.3|ST 1.8.3]]

> [!solution] Solution
> **(a)** $f$ is discontinuous at $-4$, $-2$, $2$ and $4$. At each of these numbers the graph has a break, and one of the three requirements of Definition 1 fails.
>
> | Number $a$ | What the graph shows at $a$ | Why $f$ is discontinuous at $a$ |
> | --- | --- | --- |
> | $-4$ | an open circle on the curve, and no solid dot above or below it | $f(-4)$ is not defined |
> | $-2$ | one branch ends at a solid dot, the next one starts lower, at an open circle | $\lim_{x \to -2^{-}} f(x) \ne \lim_{x \to -2^{+}} f(x)$, so $\lim_{x \to -2} f(x)$ does not exist |
> | $2$ | one branch ends at an open circle, the next one starts higher, at a solid dot | $\lim_{x \to 2^{-}} f(x) \ne \lim_{x \to 2^{+}} f(x)$, so $\lim_{x \to 2} f(x)$ does not exist |
> | $4$ | the curve falls without bound as $x$ approaches $4$ from the left | $\lim_{x \to 4^{-}} f(x) = -\infty$, so $\lim_{x \to 4} f(x)$ does not exist |
>
> The discontinuity at $-4$ is removable: the curve approaches the open circle from both sides, so $\lim_{x \to -4} f(x)$ exists. The discontinuities at $-2$ and $2$ are jump discontinuities, and the one at $4$ is an infinite discontinuity.
>
> At every other number the graph has no break. In particular $f$ is continuous at $0$: the graph has a corner there, but $\lim_{x \to 0} f(x) = f(0)$.
>
> **(b)** By Definition 2 we compare $f(a)$ with each one-sided limit. On the graph, $f(a)$ is the height of the solid dot.
> - At $-4$: neither, because $f(-4)$ is not defined.
> - At $-2$: from the left. The solid dot is the end of the branch on the left, so $\lim_{x \to -2^{-}} f(x) = f(-2)$. The limit from the right is the height of the open circle, which is different from $f(-2)$.
> - At $2$: from the right. The solid dot is the start of the branch on the right, so $\lim_{x \to 2^{+}} f(x) = f(2)$. The limit from the left is the height of the open circle.
> - At $4$: from the right. The solid dot is the start of the last branch, so $\lim_{x \to 4^{+}} f(x) = f(4)$, while $\lim_{x \to 4^{-}} f(x) = -\infty$.
>
> ![[CAL1 HW 1.8 Solutions fig 3.png|480]]

### ST 1.8.13
Question: [[CAL1 HW 1.8 Questions#ST 1.8.13|ST 1.8.13]]

> [!proof] Proof
> By Definition 1 we must show that $\lim_{x \to -1} f(x) = f(-1)$. First, by the Sum Law,
> $$
> \lim_{x \to -1} (x + 2) = \lim_{x \to -1} x + \lim_{x \to -1} 2 = -1 + 2 = 1.
> $$
> Then
> $$
> \begin{aligned}
> \lim_{x \to -1} f(x) &= \lim_{x \to -1} \left[3x^2 + (x + 2)^5\right] \\
> &= \lim_{x \to -1} 3x^2 + \lim_{x \to -1} (x + 2)^5 && \text{(Sum Law)} \\
> &= 3\lim_{x \to -1} x^2 + \lim_{x \to -1} (x + 2)^5 && \text{(Constant Multiple Law)} \\
> &= 3\left(\lim_{x \to -1} x\right)^2 + \left(\lim_{x \to -1} (x + 2)\right)^5 && \text{(Power Law)} \\
> &= 3(-1)^2 + 1^5 && \text{(\(\lim_{x \to -1} x = -1\))} \\
> &= 4.
> \end{aligned}
> $$
> Each law may be used because the limits on its right-hand side exist, as the following lines show. On the other hand,
> $$
> f(-1) = 3(-1)^2 + (-1 + 2)^5 = 3 + 1 = 4.
> $$
> Thus $\lim_{x \to -1} f(x) = 4 = f(-1)$, and $f$ is continuous at $a = -1$ by Definition 1. $\blacksquare$

### ST 1.8.19
Question: [[CAL1 HW 1.8 Questions#ST 1.8.19|ST 1.8.19]]

> [!solution] Solution
> The denominator $x + 2$ is $0$ at $x = -2$, so $f(-2)$ is not defined, while $f$ is defined at every other number. The first requirement of Definition 1 fails, so $f$ is discontinuous at $-2$.
>
> The discontinuity is infinite. As $x \to -2^{+}$, the denominator $x + 2$ is positive and approaches $0$; as $x \to -2^{-}$, it is negative and approaches $0$. Hence
> $$
> \lim_{x \to -2^{+}} \frac{1}{x + 2} = \infty \qquad \text{and} \qquad \lim_{x \to -2^{-}} \frac{1}{x + 2} = -\infty.
> $$
>
> **Graph.** The graph is the hyperbola $y = \tfrac{1}{x}$ shifted $2$ units to the left. The line $x = -2$ is a vertical asymptote, the $x$-axis is a horizontal asymptote, and the $y$-intercept is $f(0) = \tfrac{1}{2}$. The graph breaks into two branches at $x = -2$.
>
> ![[CAL1 HW 1.8 Solutions fig 19.png|380]]

### ST 1.8.21
Question: [[CAL1 HW 1.8 Questions#ST 1.8.21|ST 1.8.21]]

> [!solution] Solution
> Here $f(1) = \tfrac{1}{1} = 1$ is defined, so we examine the limit. For $x < 1$ we have $f(x) = 1 - x^2$, and for $x > 1$ we have $f(x) = \tfrac{1}{x}$. The polynomial $1 - x^2$ and the rational function $\tfrac{1}{x}$ are continuous at $1$ (Theorem 5), so their limits at $1$ are their values at $1$:
> $$
> \begin{aligned}
> \lim_{x \to 1^{-}} f(x) &= \lim_{x \to 1^{-}} (1 - x^2) = 1 - 1^2 = 0, \\
> \lim_{x \to 1^{+}} f(x) &= \lim_{x \to 1^{+}} \frac{1}{x} = \frac{1}{1} = 1.
> \end{aligned}
> $$
> The one-sided limits are different, so $\lim_{x \to 1} f(x)$ does not exist (Theorem 1.6.1). The second requirement of Definition 1 fails, and $f$ is discontinuous at $1$. This is a jump discontinuity. Since $\lim_{x \to 1^{+}} f(x) = 1 = f(1)$, $f$ is continuous from the right at $1$.
>
> **Graph.** For $x < 1$ the graph is the parabola $y = 1 - x^2$, which ends at the open circle $(1, 0)$. For $x \ge 1$ it is the hyperbola $y = \tfrac{1}{x}$, which starts at the solid dot $(1, 1)$. At $x = 1$ the graph jumps from height $0$ to height $1$.
>
> ![[CAL1 HW 1.8 Solutions fig 21.png|420]]

### ST 1.8.23
Question: [[CAL1 HW 1.8 Questions#ST 1.8.23|ST 1.8.23]]

> [!solution] Solution
> Here $f(0) = 0$. For $x < 0$ we have $f(x) = \cos x$, and for $x > 0$ we have $f(x) = 1 - x^2$. The cosine function and the polynomial $1 - x^2$ are continuous at $0$ (Theorem 7), so
> $$
> \begin{aligned}
> \lim_{x \to 0^{-}} f(x) &= \lim_{x \to 0^{-}} \cos x = \cos 0 = 1, \\
> \lim_{x \to 0^{+}} f(x) &= \lim_{x \to 0^{+}} (1 - x^2) = 1 - 0^2 = 1.
> \end{aligned}
> $$
> Both one-sided limits are $1$, so $\lim_{x \to 0} f(x) = 1$ (Theorem 1.6.1). But $f(0) = 0$, hence
> $$
> \lim_{x \to 0} f(x) = 1 \ne 0 = f(0).
> $$
> The limit exists and $f(0)$ is defined, but they are not equal. The third requirement of Definition 1 fails, so $f$ is discontinuous at $0$. The discontinuity is removable: with $f(0) = 1$ in place of $f(0) = 0$, the function would be continuous at $0$.
>
> **Graph.** For $x < 0$ the graph is the cosine curve, and for $x > 0$ it is the parabola $y = 1 - x^2$. Both approach the open circle $(0, 1)$. The value at $0$ is the solid dot at the origin.
>
> ![[CAL1 HW 1.8 Solutions fig 23.png|420]]

> [!tip] Intuition
> Exercises 19, 21 and 23 show the three ways in which Definition 1 can fail, in order. In Exercise 19, $f(a)$ is not defined. In Exercise 21, $f(a)$ is defined but $\lim_{x \to a} f(x)$ does not exist. In Exercise 23, both exist but they are different. To test continuity at a number, check the three requirements in this order.

### ST 1.8.25
Question: [[CAL1 HW 1.8 Questions#ST 1.8.25|ST 1.8.25]]

> [!solution] Solution
> **(a)** Since $x^2 - 9 = (x - 3)(x + 3)$, the function $f$ is defined exactly for $x \ne 3$ and $x \ne -3$. In particular $f(3)$ is not defined, so $f$ is discontinuous at $3$. For $x \ne 3$ and $x \ne -3$ we may cancel the factor $x - 3 \ne 0$:
> $$
> f(x) = \frac{x - 3}{(x - 3)(x + 3)} = \frac{1}{x + 3}.
> $$
> A limit at $3$ does not depend on the value at $3$, and the rational function $\tfrac{1}{x + 3}$ is continuous at $3$ (Theorem 5(b)). Therefore
> $$
> \lim_{x \to 3} f(x) = \lim_{x \to 3} \frac{1}{x + 3} = \frac{1}{3 + 3} = \frac{1}{6}.
> $$
> The limit exists, and $f$ is discontinuous at $3$ only because $f(3)$ is missing. Hence the discontinuity at $3$ is removable.
>
> **(b)** Define $f(3) = \tfrac{1}{6}$. Then
> $$
> \lim_{x \to 3} f(x) = \frac{1}{6} = f(3),
> $$
> so $f$ is continuous at $3$ by Definition 1. The new function is
> $$
> f(x) = \begin{cases} \dfrac{x - 3}{x^2 - 9} & \text{if } x \ne 3 \\[6pt] \dfrac{1}{6} & \text{if } x = 3, \end{cases}
> $$
> and it equals $\tfrac{1}{x + 3}$ for every $x \ne -3$.
>
> By contrast, the discontinuity at $-3$ cannot be removed: $\lim_{x \to -3^{+}} \tfrac{1}{x + 3} = \infty$, so it is an infinite discontinuity.

### ST 1.8.27
Question: [[CAL1 HW 1.8 Questions#ST 1.8.27|ST 1.8.27]]

> [!solution] Solution
> **Domain.** For every real number $x$ we have $x^4 \ge 0$, so $x^4 + 2 \ge 2 > 0$. The square root is therefore defined and is not $0$, and the domain of $f$ is $\mathbb{R} = (-\infty, \infty)$.
>
> **Continuity.**
> 1. The numerator $x^2$ is a polynomial, so it is continuous everywhere (Theorem 5(a)).
> 2. The polynomial $x^4 + 2$ is continuous everywhere (Theorem 5(a)), and the root function $\sqrt{u}$ is continuous at every $u > 0$ (Theorem 7). Since $x^4 + 2 > 0$ for all $x$, the composite function $\sqrt{x^4 + 2}$ is continuous everywhere (Theorem 9).
> 3. The denominator $\sqrt{x^4 + 2}$ is never $0$, so the quotient $f$ is continuous at every real number (Theorem 4, part 5).

### ST 1.8.29
Question: [[CAL1 HW 1.8 Questions#ST 1.8.29|ST 1.8.29]]

> [!solution] Solution
> **Domain.** The numerator $\cos(t^2)$ is defined for every $t$. The denominator is $0$ exactly when $1 - t^2 = 0$, that is, when $t = 1$ or $t = -1$. The domain of $h$ is
> $$
> \{t \mid t \ne -1 \text{ and } t \ne 1\} = (-\infty, -1) \cup (-1, 1) \cup (1, \infty).
> $$
>
> **Continuity.**
> 1. The polynomial $t^2$ is continuous everywhere (Theorem 5(a)), and the cosine function is continuous everywhere (Theorem 7). Hence the composite function $\cos(t^2)$ is continuous everywhere (Theorem 9).
> 2. The denominator $1 - t^2$ is a polynomial, so it is continuous everywhere (Theorem 5(a)).
> 3. The quotient $h$ is continuous at every number where the denominator is not $0$ (Theorem 4, part 5), that is, at every number in its domain.

### ST 1.8.31
Question: [[CAL1 HW 1.8 Questions#ST 1.8.31|ST 1.8.31]]

> [!solution] Solution
> **Domain.** The square root $\sqrt{9 - v^2}$ is defined exactly when $9 - v^2 \ge 0$, that is, $v^2 \le 9$, that is, $-3 \le v \le 3$. The domain of $L$ is $[-3, 3]$.
>
> **Continuity.**
> 1. The factor $v$ is a polynomial, so it is continuous everywhere (Theorem 5(a)).
> 2. The polynomial $9 - v^2$ is continuous everywhere (Theorem 5(a)), and the root function $\sqrt{u}$ is continuous at every number in its domain $[0, \infty)$ (Theorem 7). Hence the composite function $\sqrt{9 - v^2}$ is continuous at every number in its domain $[-3, 3]$ (Theorem 9).
> 3. The product $L$ of these two functions is continuous at every number in $[-3, 3]$ (Theorem 4, part 4).
>
> At the endpoints $-3$ and $3$ the function is defined on one side only. There, continuous means continuous from the right at $-3$ and continuous from the left at $3$ (Definition 3):
> $$
> \lim_{v \to -3^{+}} L(v) = 0 = L(-3) \qquad \text{and} \qquad \lim_{v \to 3^{-}} L(v) = 0 = L(3).
> $$

### ST 1.8.35
Question: [[CAL1 HW 1.8 Questions#ST 1.8.35|ST 1.8.35]]

> [!solution] Solution
> Let $f(x) = x\sqrt{20 - x^2}$. As in Exercise 31, $f$ is the product of the polynomial $x$ and the composite of the root function with the polynomial $20 - x^2$, so $f$ is continuous at every number in its domain (Theorems 4, 5, 7 and 9). The domain is given by $20 - x^2 \ge 0$, so it is the interval $\left[-\sqrt{20}, \sqrt{20}\right]$. The number $2$ lies inside this interval, because $20 - 2^2 = 16 > 0$. Hence $f$ is continuous at $2$, and by Definition 1 the limit is the value of $f$ at $2$:
> $$
> \lim_{x \to 2} x\sqrt{20 - x^2} = f(2) = 2\sqrt{20 - 2^2} = 2\sqrt{16} = 2 \cdot 4 = 8.
> $$
>
> **Answer.** $8$.

### ST 1.8.41
Question: [[CAL1 HW 1.8 Questions#ST 1.8.41|ST 1.8.41]]

> [!proof] Proof
> We show that $f$ is continuous at every real number $a$, in three cases.
>
> **Case $a < 1$.** On the open interval $(-\infty, 1)$, which contains $a$, we have $f(x) = 1 - x^2$. This polynomial is continuous at $a$ (Theorem 5(a)), so $f$ is continuous at $a$.
>
> **Case $a > 1$.** On the open interval $(1, \infty)$, which contains $a$, we have $f(x) = \sqrt{x - 1}$. The polynomial $x - 1$ is continuous at $a$ (Theorem 5(a)), and the root function is continuous at $a - 1 > 0$ (Theorem 7). Hence the composite function $\sqrt{x - 1}$ is continuous at $a$ (Theorem 9), and so is $f$.
>
> **Case $a = 1$.** Here the formula changes, so we compute both one-sided limits. First, $f(1) = 1 - 1^2 = 0$. From the left $f(x) = 1 - x^2$, so
> $$
> \lim_{x \to 1^{-}} f(x) = \lim_{x \to 1^{-}} (1 - x^2) = 1 - 1^2 = 0.
> $$
> From the right $f(x) = \sqrt{x - 1}$, and $\lim_{x \to 1^{+}} \sqrt{x - 1} = 0$ by Definition 4 of ST §1.7: given $\varepsilon > 0$, choose $\delta = \varepsilon^2$. If $1 < x < 1 + \delta$, then $0 < x - 1 < \varepsilon^2$, so $\left\lvert \sqrt{x - 1} - 0 \right\rvert = \sqrt{x - 1} < \varepsilon$. Hence
> $$
> \lim_{x \to 1^{+}} f(x) = \lim_{x \to 1^{+}} \sqrt{x - 1} = 0.
> $$
> Both one-sided limits are $0$, so $\lim_{x \to 1} f(x) = 0 = f(1)$ (Theorem 1.6.1), and $f$ is continuous at $1$ by Definition 1.
>
> Therefore $f$ is continuous at every real number, that is, on $(-\infty, \infty)$. $\blacksquare$

### ST 1.8.45
Question: [[CAL1 HW 1.8 Questions#ST 1.8.45|ST 1.8.45]]

> [!solution] Solution
> On each of the open intervals $(-\infty, 0)$, $(0, 1)$ and $(1, \infty)$, $f$ agrees with a polynomial ($x + 2$, $2x^2$ and $2 - x$), so $f$ is continuous there (Theorem 5(a)). Only the numbers $0$ and $1$, where the formula changes, remain.
>
> **At $0$.** We have $f(0) = 2 \cdot 0^2 = 0$, and
> $$
> \begin{aligned}
> \lim_{x \to 0^{-}} f(x) &= \lim_{x \to 0^{-}} (x + 2) = 2, \\
> \lim_{x \to 0^{+}} f(x) &= \lim_{x \to 0^{+}} 2x^2 = 0.
> \end{aligned}
> $$
> The one-sided limits are different, so $\lim_{x \to 0} f(x)$ does not exist and $f$ is discontinuous at $0$. Since $\lim_{x \to 0^{+}} f(x) = 0 = f(0)$ but $\lim_{x \to 0^{-}} f(x) = 2 \ne f(0)$, $f$ is continuous from the right at $0$, and not from the left.
>
> **At $1$.** We have $f(1) = 2 \cdot 1^2 = 2$, and
> $$
> \begin{aligned}
> \lim_{x \to 1^{-}} f(x) &= \lim_{x \to 1^{-}} 2x^2 = 2, \\
> \lim_{x \to 1^{+}} f(x) &= \lim_{x \to 1^{+}} (2 - x) = 1.
> \end{aligned}
> $$
> The one-sided limits are different, so $\lim_{x \to 1} f(x)$ does not exist and $f$ is discontinuous at $1$. Since $\lim_{x \to 1^{-}} f(x) = 2 = f(1)$ but $\lim_{x \to 1^{+}} f(x) = 1 \ne f(1)$, $f$ is continuous from the left at $1$, and not from the right.
>
> **Answer.** $f$ is discontinuous at $0$ and at $1$; both are jump discontinuities. $f$ is continuous from the right at $0$ and continuous from the left at $1$.
>
> **Graph.** The line $y = x + 2$ for $x < 0$ ends at the open circle $(0, 2)$. The parabola $y = 2x^2$ runs from the solid dot $(0, 0)$ to the solid dot $(1, 2)$. The line $y = 2 - x$ for $x > 1$ starts at the open circle $(1, 1)$. At each jump the solid dot lies on the side from which $f$ is continuous.
>
> ![[CAL1 HW 1.8 Solutions fig 45.png|420]]

> [!tip] Intuition
> For a function defined by cases, the only candidates for a discontinuity are the numbers where the formula changes, and the numbers where one of the formulas is itself not defined. At a number where the formula changes, compute the limit from the left with the left formula and the limit from the right with the right formula, and compare both with the value of $f$ there. Exercises 41, 45, 47 and 48 all follow this plan.

### ST 1.8.47
Question: [[CAL1 HW 1.8 Questions#ST 1.8.47|ST 1.8.47]]

> [!solution] Solution
> For every value of $c$, $f$ agrees with the polynomial $cx^2 + 2x$ on $(-\infty, 2)$ and with the polynomial $x^3 - cx$ on $(2, \infty)$, so $f$ is continuous on these two intervals (Theorem 5(a)). Hence $f$ is continuous on $(-\infty, \infty)$ if and only if it is continuous at $2$.
>
> At $2$ we have $f(2) = 2^3 - 2c = 8 - 2c$, and
> $$
> \begin{aligned}
> \lim_{x \to 2^{-}} f(x) &= \lim_{x \to 2^{-}} (cx^2 + 2x) = 4c + 4, \\
> \lim_{x \to 2^{+}} f(x) &= \lim_{x \to 2^{+}} (x^3 - cx) = 8 - 2c.
> \end{aligned}
> $$
> By Theorem 1.6.1, $\lim_{x \to 2} f(x)$ exists exactly when these two numbers are equal, and then the limit is $8 - 2c = f(2)$. So $f$ is continuous at $2$ if and only if
> $$
> 4c + 4 = 8 - 2c \iff 6c = 4 \iff c = \tfrac{2}{3}.
> $$
>
> **Answer.** $c = \tfrac{2}{3}$.
>
> **Check.** For $c = \tfrac{2}{3}$ we get $4c + 4 = \tfrac{20}{3}$ and $8 - 2c = \tfrac{20}{3}$, so the two pieces meet at the point $\left(2, \tfrac{20}{3}\right)$.

### ST 1.8.49
Question: [[CAL1 HW 1.8 Questions#ST 1.8.49|ST 1.8.49]]

> [!solution] Solution
> Since $f$ and $g$ are continuous at $2$, so is the function $3f + fg$: the function $3f$ by part 3, the function $fg$ by part 4, and their sum by part 1 of Theorem 4. By Definition 1 the limit of $3f + fg$ at $2$ is its value at $2$:
> $$
> \begin{aligned}
> 36 = \lim_{x \to 2} \left[3f(x) + f(x)g(x)\right] &= 3f(2) + f(2)g(2) && \text{(continuity at \(2\))} \\
> &= 3f(2) + 6f(2) && \text{(\(g(2) = 6\))} \\
> &= 9f(2).
> \end{aligned}
> $$
> Hence $f(2) = \tfrac{36}{9} = 4$.
>
> **Answer.** $f(2) = 4$.

### ST 1.8.55
Question: [[CAL1 HW 1.8 Questions#ST 1.8.55|ST 1.8.55]]

> [!proof] Proof
> Let $f(x) = -x^3 + 4x + 1$. A number $c$ is a solution of the given equation exactly when $f(c) = 0$.
>
> The function $f$ is a polynomial, so it is continuous on the closed interval $[-1, 0]$ (Theorem 5(a)). At the endpoints,
> $$
> \begin{aligned}
> f(-1) &= -(-1)^3 + 4(-1) + 1 = 1 - 4 + 1 = -2, \\
> f(0) &= -0^3 + 4 \cdot 0 + 1 = 1.
> \end{aligned}
> $$
> Thus $f(-1) < 0 < f(0)$: the number $N = 0$ lies between $f(-1)$ and $f(0)$, and $f(-1) \ne f(0)$. By the Intermediate Value Theorem (Theorem 10), there is a number $c$ in $(-1, 0)$ such that $f(c) = 0$. This $c$ is a solution of $-x^3 + 4x + 1 = 0$ in the interval $(-1, 0)$. $\blacksquare$

> [!tip] Intuition
> The Intermediate Value Theorem is used in three steps. First, move all terms to one side, so that the solutions are the zeros of a function $f$. Second, check that $f$ is continuous on the closed interval. Third, evaluate $f$ at the two endpoints and find values of opposite sign. The theorem says that a solution exists; it does not say where it is. Here the solution is $c \approx -0.254$.

## ST §1.8 Additional Exercises

> [!note] Note
> These exercises are not assigned. Each one adds a type of problem that the assigned exercises do not cover.
> - 17: continuity on an interval with an endpoint, where continuity from one side is needed (Definition 3).
> - 48: two unknown constants and two numbers where the formula changes. Exercise 47 has one of each.
> - 50: the domain of a composite function. A formula that simplifies can hide a discontinuity.
> - 54: the Intermediate Value Theorem in an indirect proof, with no formula for $f$.
> - 64: the Intermediate Value Theorem used twice, with test numbers that we choose ourselves.
> - 72: a function that is continuous at exactly one number.
> - 73: the Squeeze Theorem at a number where Theorems 4 and 9 do not apply.
> - 74: the Intermediate Value Theorem for an equation with fractions, where the denominators must be checked afterwards.
> - 76: the continuity of $\lvert f \rvert$, and a converse that is false.

### ST 1.8.17
Question: [[CAL1 HW 1.8 Questions#ST 1.8.17|ST 1.8.17]]

> [!proof] Proof
> By Definition 3 we must show that $f$ is continuous at every number $a > 4$ and continuous from the right at the endpoint $4$, where $f$ is defined on one side only.
>
> **Case $a > 4$.** By the Limit Laws,
> $$
> \begin{aligned}
> \lim_{x \to a} f(x) &= \lim_{x \to a} \left(x + \sqrt{x - 4}\right) \\
> &= \lim_{x \to a} x + \lim_{x \to a} \sqrt{x - 4} && \text{(Sum Law)} \\
> &= \lim_{x \to a} x + \sqrt{\lim_{x \to a} (x - 4)} && \text{(Root Law)} \\
> &= a + \sqrt{a - 4} && \text{(Difference Law)} \\
> &= f(a).
> \end{aligned}
> $$
> The Root Law may be used because $\lim_{x \to a} (x - 4) = a - 4 > 0$. So $f$ is continuous at $a$ by Definition 1.
>
> **Case $a = 4$.** First, $\lim_{x \to 4^{+}} \sqrt{x - 4} = 0$ by Definition 4 of ST §1.7: given $\varepsilon > 0$, choose $\delta = \varepsilon^2$. If $4 < x < 4 + \delta$, then $0 < x - 4 < \varepsilon^2$, so $\left\lvert \sqrt{x - 4} - 0 \right\rvert = \sqrt{x - 4} < \varepsilon$. Hence, by the Sum Law for one-sided limits,
> $$
> \lim_{x \to 4^{+}} f(x) = \lim_{x \to 4^{+}} x + \lim_{x \to 4^{+}} \sqrt{x - 4} = 4 + 0 = 4 = f(4).
> $$
> So $f$ is continuous from the right at $4$ by Definition 2.
>
> Therefore $f$ is continuous on $[4, \infty)$. $\blacksquare$

### ST 1.8.48
Question: [[CAL1 HW 1.8 Questions#ST 1.8.48|ST 1.8.48]]

> [!solution] Solution
> For $x < 2$ we have $x - 2 \ne 0$, so
> $$
> \frac{x^2 - 4}{x - 2} = \frac{(x - 2)(x + 2)}{x - 2} = x + 2.
> $$
> Thus $f$ agrees with a polynomial on each of the open intervals $(-\infty, 2)$, $(2, 3)$ and $(3, \infty)$, and it is continuous there for all $a$ and $b$ (Theorem 5(a)). It remains to make $f$ continuous at $2$ and at $3$.
>
> **At $2$.** We have $f(2) = 4a - 2b + 3$, and
> $$
> \begin{aligned}
> \lim_{x \to 2^{-}} f(x) &= \lim_{x \to 2^{-}} (x + 2) = 4, \\
> \lim_{x \to 2^{+}} f(x) &= \lim_{x \to 2^{+}} (ax^2 - bx + 3) = 4a - 2b + 3.
> \end{aligned}
> $$
> So $f$ is continuous at $2$ if and only if $4a - 2b + 3 = 4$, that is,
> $$
> 4a - 2b = 1. \qquad (1)
> $$
>
> **At $3$.** We have $f(3) = 2 \cdot 3 - a + b = 6 - a + b$, and
> $$
> \begin{aligned}
> \lim_{x \to 3^{-}} f(x) &= \lim_{x \to 3^{-}} (ax^2 - bx + 3) = 9a - 3b + 3, \\
> \lim_{x \to 3^{+}} f(x) &= \lim_{x \to 3^{+}} (2x - a + b) = 6 - a + b.
> \end{aligned}
> $$
> So $f$ is continuous at $3$ if and only if $9a - 3b + 3 = 6 - a + b$, that is,
> $$
> 10a - 4b = 3. \qquad (2)
> $$
>
> **Solving.** Subtracting twice equation (1) from equation (2) gives $(10a - 4b) - 2(4a - 2b) = 3 - 2$, that is, $2a = 1$, so $a = \tfrac{1}{2}$. Then equation (1) gives $2 - 2b = 1$, so $b = \tfrac{1}{2}$.
>
> **Answer.** $a = b = \tfrac{1}{2}$.
>
> **Check.** With these values the middle formula is $\tfrac{1}{2}x^2 - \tfrac{1}{2}x + 3$. At $x = 2$ it gives $2 - 1 + 3 = 4$, the limit from the left. At $x = 3$ it gives $\tfrac{9}{2} - \tfrac{3}{2} + 3 = 6$, and the last formula gives $6 - \tfrac{1}{2} + \tfrac{1}{2} = 6$.

### ST 1.8.50
Question: [[CAL1 HW 1.8 Questions#ST 1.8.50|ST 1.8.50]]

> [!solution] Solution
> **(a)** For $x \ne 0$,
> $$
> (f \circ g)(x) = f(g(x)) = f\left(\frac{1}{x^2}\right) = \frac{1}{1/x^2} = x^2.
> $$
> The domain of $f \circ g$ consists of the numbers $x$ in the domain of $g$ for which $g(x)$ is in the domain of $f$. The first condition is $x \ne 0$. The second condition is $\tfrac{1}{x^2} \ne 0$, which holds for every $x \ne 0$. Hence
> $$
> (f \circ g)(x) = x^2, \qquad x \ne 0.
> $$
>
> **(b)** No. The function $f \circ g$ is not defined at $0$, because $g(0)$ is not defined, so $f \circ g$ is discontinuous at $0$. The formula $x^2$ alone suggests a function that is continuous everywhere, but the composite function keeps the restriction $x \ne 0$ of the inner function $g$.
>
> At every number $a \ne 0$ the function $f \circ g$ is continuous: $g$ is a rational function defined at $a$, and $f$ is a rational function defined at $g(a) = \tfrac{1}{a^2} \ne 0$, so both are continuous there (Theorem 5(b)) and Theorem 9 applies. The discontinuity at $0$ is removable, since $\lim_{x \to 0} (f \circ g)(x) = \lim_{x \to 0} x^2 = 0$ exists.

### ST 1.8.54
Question: [[CAL1 HW 1.8 Questions#ST 1.8.54|ST 1.8.54]]

> [!proof] Proof
> The only solutions of $f(x) = 6$ are $x = 1$ and $x = 4$, and $3$ is neither of them, so $f(3) \ne 6$. Hence either $f(3) < 6$ or $f(3) > 6$.
>
> Suppose, to the contrary, that $f(3) < 6$. The function $f$ is continuous on $[1, 5]$, so it is continuous on the closed interval $[2, 3]$. The number $N = 6$ lies between $f(3)$ and $f(2)$, because
> $$
> f(3) < 6 < 8 = f(2).
> $$
> By the Intermediate Value Theorem (Theorem 10), there is a number $c$ in $(2, 3)$ such that $f(c) = 6$. Then $c$ is a solution of $f(x) = 6$ with $2 < c < 3$, so $c \ne 1$ and $c \ne 4$. This contradicts the hypothesis that $1$ and $4$ are the only solutions. Therefore $f(3) > 6$. $\blacksquare$

> [!tip] Intuition
> The graph of a continuous function cannot pass from one side of the horizontal line $y = 6$ to the other side without meeting the line. Between $x = 1$ and $x = 4$ the graph never meets this line, and at $x = 2$ it is above the line, since $f(2) = 8$. So the graph stays above the line on the whole interval $(1, 4)$, and in particular $f(3) > 6$.

### ST 1.8.64
Question: [[CAL1 HW 1.8 Questions#ST 1.8.64|ST 1.8.64]]

> [!proof] Proof
> Let $f(x) = x^2 - 3 + \tfrac{1}{x}$. An $x$-intercept of the graph is a number $x$ with $f(x) = 0$. Since
> $$
> f(x) = \frac{x^3 - 3x + 1}{x},
> $$
> $f$ is a rational function that is defined for $x \ne 0$. Hence $f$ is continuous on $(0, \infty)$ (Theorem 5(b)), and in particular on every closed interval inside $(0, \infty)$.
>
> We cannot use the endpoint $0$, where $f$ is not defined. Instead we evaluate $f$ at three numbers of $(0, 2]$:
> $$
> \begin{aligned}
> f\left(\tfrac{1}{4}\right) &= \tfrac{1}{16} - 3 + 4 = \tfrac{17}{16} > 0, \\
> f(1) &= 1 - 3 + 1 = -1 < 0, \\
> f(2) &= 4 - 3 + \tfrac{1}{2} = \tfrac{3}{2} > 0.
> \end{aligned}
> $$
> On $\left[\tfrac{1}{4}, 1\right]$ the function $f$ is continuous and $f(1) < 0 < f\left(\tfrac{1}{4}\right)$. By the Intermediate Value Theorem (Theorem 10), there is a number $c_1$ in $\left(\tfrac{1}{4}, 1\right)$ such that $f(c_1) = 0$.
>
> On $[1, 2]$ the function $f$ is continuous and $f(1) < 0 < f(2)$. By the same theorem, there is a number $c_2$ in $(1, 2)$ such that $f(c_2) = 0$.
>
> Since $c_1 < 1 < c_2$, the numbers $c_1$ and $c_2$ are different, and both lie in $(0, 2)$. Therefore the graph has at least two $x$-intercepts in $(0, 2)$. $\blacksquare$

> [!tip] Intuition
> To find the test numbers, look at the signs. For small positive $x$ the term $\tfrac{1}{x}$ is large, so $f(x) > 0$ near $0$. At $x = 1$ the value is negative, and at $x = 2$ it is positive again. Two changes of sign give two zeros, here $c_1 \approx 0.347$ and $c_2 \approx 1.532$. A number that is not small enough fails: $f\left(\tfrac{1}{2}\right) = -\tfrac{3}{4} < 0$.

### ST 1.8.72
Question: [[CAL1 HW 1.8 Questions#ST 1.8.72|ST 1.8.72]]

> [!solution] Solution
> **Answer.** $g$ is continuous at $x = 0$ and at no other number.
>
> **Plan.** Near $0$ both formulas, $0$ and $x$, give small values, so $g(x)$ is squeezed towards $g(0) = 0$. Near a number $a \ne 0$ the rational numbers give the value $0$ and the irrational numbers give values close to $a$, so the values of $g$ do not settle near the single number $g(a)$. We use the fact that every open interval contains a rational number and an irrational number.

> [!proof] Proof
> **Continuity at $0$.** For every real number $x$, $g(x)$ is $0$ or $x$, so $\lvert g(x) \rvert \le \lvert x \rvert$, that is,
> $$
> -\lvert x \rvert \le g(x) \le \lvert x \rvert.
> $$
> We have $\lim_{x \to 0} \lvert x \rvert = 0$ ([[CAL1 HW 1.7 Solutions#ST 1.7.27|ST 1.7.27]]), and so $\lim_{x \to 0} \left(-\lvert x \rvert\right) = 0$ by the Constant Multiple Law. By the Squeeze Theorem, $\lim_{x \to 0} g(x) = 0$. Since $0$ is rational, $g(0) = 0$. Hence $\lim_{x \to 0} g(x) = g(0)$, and $g$ is continuous at $0$.
>
> **Discontinuity at $a \ne 0$.** Let $a \ne 0$. We show that the statement $\lim_{x \to a} g(x) = g(a)$ is false. By the [[Precise Definition of a Limit|precise definition of a limit]] (Definition 2 of ST §1.7), it suffices to find one number $\varepsilon > 0$ for which no $\delta > 0$ works. Take $\varepsilon = \tfrac{\lvert a \rvert}{2}$, and let $\delta > 0$ be arbitrary.
>
> *Case 1: $a$ is rational.* Then $g(a) = 0$. Let $\delta' = \min\left\{\delta, \tfrac{\lvert a \rvert}{2}\right\}$. The interval $(a, a + \delta')$ contains an irrational number $s$. Then $0 < \lvert s - a \rvert < \delta$ and $\lvert s - a \rvert < \tfrac{\lvert a \rvert}{2}$. By the Triangle Inequality, $\lvert a \rvert \le \lvert a - s \rvert + \lvert s \rvert$, so
> $$
> \lvert g(s) - g(a) \rvert = \lvert s \rvert \ge \lvert a \rvert - \lvert a - s \rvert > \lvert a \rvert - \tfrac{\lvert a \rvert}{2} = \varepsilon.
> $$
>
> *Case 2: $a$ is irrational.* Then $g(a) = a$. The interval $(a, a + \delta)$ contains a rational number $r$. Then $0 < \lvert r - a \rvert < \delta$ and
> $$
> \lvert g(r) - g(a) \rvert = \lvert 0 - a \rvert = \lvert a \rvert > \tfrac{\lvert a \rvert}{2} = \varepsilon.
> $$
>
> In both cases, for every $\delta > 0$ there is a number $x$ with $0 < \lvert x - a \rvert < \delta$ and $\lvert g(x) - g(a) \rvert > \varepsilon$. So no $\delta$ works for this $\varepsilon$, and $\lim_{x \to a} g(x) = g(a)$ does not hold. Hence $g$ is discontinuous at every number $a \ne 0$. $\blacksquare$

### ST 1.8.73
Question: [[CAL1 HW 1.8 Questions#ST 1.8.73|ST 1.8.73]]

> [!proof] Proof
> **Continuity at $a \ne 0$.** Let $a \ne 0$. On an open interval that contains $a$ but not $0$, we have $f(x) = x^4\sin(1/x)$. The rational function $\tfrac{1}{x}$ is continuous at $a$ (Theorem 5(b)), and the sine function is continuous everywhere (Theorem 7), so the composite function $\sin(1/x)$ is continuous at $a$ (Theorem 9). The polynomial $x^4$ is continuous at $a$ (Theorem 5(a)). Hence the product $x^4\sin(1/x)$ is continuous at $a$ (Theorem 4, part 4), and so is $f$.
>
> **Continuity at $0$.** The argument above fails at $0$: there $\tfrac{1}{x}$ is not defined, and the Product Law cannot be used because $\lim_{x \to 0} \sin(1/x)$ does not exist. Instead, for every $x \ne 0$,
> $$
> -1 \le \sin\frac{1}{x} \le 1.
> $$
> Multiplying by $x^4 > 0$ keeps the directions of the inequalities:
> $$
> -x^4 \le x^4\sin\frac{1}{x} \le x^4.
> $$
> The polynomials $-x^4$ and $x^4$ are continuous at $0$ (Theorem 5(a)), so $\lim_{x \to 0} \left(-x^4\right) = 0$ and $\lim_{x \to 0} x^4 = 0$. By the Squeeze Theorem,
> $$
> \lim_{x \to 0} f(x) = \lim_{x \to 0} x^4\sin\frac{1}{x} = 0 = f(0).
> $$
> So $f$ is continuous at $0$ by Definition 1.
>
> Therefore $f$ is continuous at every real number, that is, on $(-\infty, \infty)$. $\blacksquare$

### ST 1.8.74
Question: [[CAL1 HW 1.8 Questions#ST 1.8.74|ST 1.8.74]]

> [!solution] Solution
> **Plan.** The left side of the equation is not defined where a denominator is $0$, so the Intermediate Value Theorem cannot be applied to it on $[-1, 1]$ directly. We clear the denominators, apply the theorem to the resulting polynomial, and then check that the number we find is not a zero of a denominator.
>
> **The denominators.** Both denominators factor:
> $$
> \begin{aligned}
> x^3 + 2x^2 - 1 &= (x + 1)(x^2 + x - 1), \\
> x^3 + x - 2 &= (x - 1)(x^2 + x + 2).
> \end{aligned}
> $$
> The quadratic $x^2 + x - 1$ has the zeros $\tfrac{-1 + \sqrt{5}}{2} \approx 0.618$ and $\tfrac{-1 - \sqrt{5}}{2} \approx -1.618$. The quadratic $x^2 + x + 2$ has no real zero, because its discriminant is $1 - 8 = -7 < 0$. So in the open interval $(-1, 1)$ a denominator is $0$ at only one number,
> $$
> r = \frac{-1 + \sqrt{5}}{2},
> $$
> which is a zero of the first denominator.

> [!proof] Proof
> Let
> $$
> p(x) = a(x^3 + x - 2) + b(x^3 + 2x^2 - 1).
> $$
> The function $p$ is a polynomial, so it is continuous on $[-1, 1]$ (Theorem 5(a)). Since $a > 0$ and $b > 0$,
> $$
> \begin{aligned}
> p(-1) &= a(-1 - 1 - 2) + b(-1 + 2 - 1) = -4a < 0, \\
> p(1) &= a(1 + 1 - 2) + b(1 + 2 - 1) = 2b > 0.
> \end{aligned}
> $$
> Thus $p(-1) < 0 < p(1)$, and by the Intermediate Value Theorem (Theorem 10) there is a number $c$ in $(-1, 1)$ such that $p(c) = 0$.
>
> We check that no denominator is $0$ at $c$. In $(-1, 1)$ this can happen only at $r = \tfrac{-1 + \sqrt{5}}{2}$, where $r^2 + r - 1 = 0$. Then $r^2 = 1 - r$ and $r^3 = r \cdot r^2 = r - r^2 = 2r - 1$, so
> $$
> p(r) = a(r^3 + r - 2) + b \cdot 0 = a\big((2r - 1) + r - 2\big) = 3a(r - 1) < 0,
> $$
> because $a > 0$ and $r < 1$. Hence $p(r) \ne 0$, so $c \ne r$, and both denominators are different from $0$ at $c$.
>
> Dividing $p(c) = 0$ by the nonzero number $(c^3 + 2c^2 - 1)(c^3 + c - 2)$ gives
> $$
> \frac{a}{c^3 + 2c^2 - 1} + \frac{b}{c^3 + c - 2} = 0.
> $$
> Therefore $c$ is a solution of the given equation in the interval $(-1, 1)$. $\blacksquare$

### ST 1.8.76
Question: [[CAL1 HW 1.8 Questions#ST 1.8.76|ST 1.8.76]]

> [!proof] Proof of (a)
> Let $a$ be a real number. We show that $\lim_{x \to a} \lvert x \rvert = \lvert a \rvert$.
> - If $a > 0$, then $\lvert x \rvert = x$ on the open interval $(0, \infty)$, which contains $a$. Hence $\lim_{x \to a} \lvert x \rvert = \lim_{x \to a} x = a = \lvert a \rvert$.
> - If $a < 0$, then $\lvert x \rvert = -x$ on the open interval $(-\infty, 0)$, which contains $a$. Hence $\lim_{x \to a} \lvert x \rvert = \lim_{x \to a} (-x) = -a = \lvert a \rvert$.
> - If $a = 0$, then $\lim_{x \to 0} \lvert x \rvert = 0 = \lvert 0 \rvert$, as proved in [[CAL1 HW 1.7 Solutions#ST 1.7.27|ST 1.7.27]].
>
> In every case $\lim_{x \to a} F(x) = F(a)$, so $F$ is continuous at every real number. $\blacksquare$

> [!proof] Proof of (b)
> Let $f$ be continuous on an interval $I$, and let $a$ be a number in $I$. Then $\lim_{x \to a} f(x) = f(a)$, and by part (a) the function $F(u) = \lvert u \rvert$ is continuous at the number $f(a)$. By Theorem 8,
> $$
> \lim_{x \to a} \lvert f(x) \rvert = \lim_{x \to a} F(f(x)) = F(f(a)) = \lvert f(a) \rvert.
> $$
> So $\lvert f \rvert$ is continuous at $a$. If $a$ is an endpoint of $I$, the same computation holds with the one-sided limit in place of $\lim_{x \to a}$. Therefore $\lvert f \rvert$ is continuous on $I$. $\blacksquare$

> [!solution] Solution
> **(c)** No, the converse is false. A counterexample is
> $$
> f(x) = \begin{cases} 1 & \text{if } x \ge 0 \\ -1 & \text{if } x < 0. \end{cases}
> $$
> Here $\lvert f(x) \rvert = 1$ for every $x$. The constant function $1$ is continuous everywhere, so $\lvert f \rvert$ is continuous on $\mathbb{R}$. But $f$ is not continuous at $0$, because
> $$
> \lim_{x \to 0^{-}} f(x) = -1 \ne 1 = \lim_{x \to 0^{+}} f(x),
> $$
> so $\lim_{x \to 0} f(x)$ does not exist. Thus $\lvert f \rvert$ is continuous, while $f$ is not.
