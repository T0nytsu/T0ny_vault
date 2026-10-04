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
| [[CAL1 HW 1.8 Questions#ST 1.8.3\|ST 1.8.3]] | (a) $-4$: $f(-4)$ is not defined; $-2$, $2$, $4$: the limit does not exist. (b) $-4$: neither; $-2$: left; $2$, $4$: right |
| [[CAL1 HW 1.8 Questions#ST 1.8.13\|ST 1.8.13]] | Proof: $\lim_{x \to -1} f(x) = 4 = f(-1)$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.19\|ST 1.8.19]] | $\lim_{x \to -2} f(x)$ does not exist; graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.21\|ST 1.8.21]] | $\lim_{x \to 1^{-}} f(x) = 0 \ne 1 = \lim_{x \to 1^{+}} f(x)$; graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.23\|ST 1.8.23]] | $\lim_{x \to 0} f(x) = 1 \ne 0 = f(0)$; graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.25\|ST 1.8.25]] | (a) $\lim_{x \to 3} f(x) = \tfrac{1}{6}$, $f(3)$ is not defined; (b) $f(3) = \tfrac{1}{6}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.27\|ST 1.8.27]] | Domain $\mathbb{R}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.29\|ST 1.8.29]] | Domain $\mathbb{R} \setminus \{1, -1\}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.31\|ST 1.8.31]] | Domain $[-3, 3]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.35\|ST 1.8.35]] | $8$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.41\|ST 1.8.41]] | Proof: $\lim_{x \to 1^{-}} f(x) = \lim_{x \to 1^{+}} f(x) = 0 = f(1)$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.45\|ST 1.8.45]] | Discontinuous at $0$ (continuous from the right) and at $1$ (continuous from the left); graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.47\|ST 1.8.47]] | $c = \tfrac{2}{3}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.49\|ST 1.8.49]] | $f(2) = 4$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.55\|ST 1.8.55]] | Proof: Intermediate Value Theorem on $[-1, 0]$, $f(-1) = -2 < 0 < 1 = f(0)$ |

Additional exercises, not assigned:

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 1.8 Questions#ST 1.8.17\|ST 1.8.17]] | Proof: $\lim_{x \to a} f(x) = f(a)$ for $a > 4$; $\lim_{x \to 4^{+}} f(x) = f(4)$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.48\|ST 1.8.48]] | $a = b = \tfrac{1}{2}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.50\|ST 1.8.50]] | (a) $x^2$, $x \ne 0$; (b) No |
| [[CAL1 HW 1.8 Questions#ST 1.8.54\|ST 1.8.54]] | Proof by contradiction: Intermediate Value Theorem on $[2, 3]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.64\|ST 1.8.64]] | Proof: Intermediate Value Theorem on $\left[\tfrac{1}{4}, 1\right]$ and on $[1, 2]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.72\|ST 1.8.72]] | Only at $x = 0$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.73\|ST 1.8.73]] | Proof: product and composite of continuous functions for $x \ne 0$; Squeeze Theorem at $0$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.74\|ST 1.8.74]] | Proof: Intermediate Value Theorem for $p(x) = a(x^3 + x - 2) + b(x^3 + 2x^2 - 1)$ on $[-1, 1]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.76\|ST 1.8.76]] | (a), (b) Proofs; (c) No: $f(x) = 1$ ($x \ge 0$), $-1$ ($x < 0$) |

## ST §1.8 Continuity

> [!note] Note
> The facts that the answers use, each under its name. An answer gives the fact in words. The number of a theorem appears in an answer only when the question asks for it (Exercises 27–34); those numbers are from the standard text of ST §1.8, because the scan holds only the exercise pages. Compare them with the book.
> - **Definition of continuity** ([[Continuity|continuous]] at $a$): $\lim_{x \to a} f(x) = f(a)$. It needs: $f(a)$ is defined, $\lim_{x \to a} f(x)$ exists, and both are equal.
> - **Continuous from the right** at $a$: $\lim_{x \to a^{+}} f(x) = f(a)$. **From the left**: $\lim_{x \to a^{-}} f(x) = f(a)$.
> - **Continuous on an interval**: continuous at every number in it, and from one side at an endpoint.
> - **Sums, differences, products, quotients** (Theorem 4): $f$, $g$ continuous at $a$ $\implies$ $f + g$, $f - g$, $cf$, $fg$, and $\tfrac{f}{g}$ if $g(a) \ne 0$, are continuous at $a$.
> - **Polynomials and rational functions** (Theorem 5): a polynomial is continuous $\forall x \in \mathbb{R}$; a rational function is continuous on its domain.
> - **Root and trigonometric functions** (Theorem 7): continuous on their domains.
> - **Limit of a composite** (Theorem 8): $f$ continuous at $b$, $\lim_{x \to a} g(x) = b$ $\implies$ $\lim_{x \to a} f(g(x)) = f(b)$.
> - **Composite of continuous functions** (Theorem 9): $g$ continuous at $a$, $f$ continuous at $g(a)$ $\implies$ $f \circ g$ continuous at $a$.
> - **[[Intermediate Value Theorem]]**: $f$ continuous on $[a, b]$, $N$ between $f(a)$ and $f(b)$, $f(a) \ne f(b)$ $\implies$ $\exists\, c \in (a, b)$ s.t. $f(c) = N$.
> - **[[Discontinuity]]** at $a$: *removable* ($\lim_{x \to a} f(x)$ exists), *jump* (the one-sided limits exist and differ), *infinite* (a one-sided limit is $\pm\infty$, see [[Infinite Limit]]).
> - **Limit Laws** (ST §1.6): Sum, Difference, Constant Multiple, Product, Quotient, Power and Root Laws; Constant Law: $\lim_{x \to a} c = c$; Identity Law: $\lim_{x \to a} x = a$; Direct Substitution Property: $f$ a polynomial or a rational function, $a$ in its domain $\implies$ $\lim_{x \to a} f(x) = f(a)$.
> - **One-sided limits** ([[One-Sided Limit]]): $\lim_{x \to a} f(x) = L$ $\iff$ $\lim_{x \to a^{-}} f(x) = L = \lim_{x \to a^{+}} f(x)$.
> - **[[Squeeze Theorem]]** (ST §1.6): $f(x) \le g(x) \le h(x)$ near $a$, $\lim_{x \to a} f(x) = \lim_{x \to a} h(x) = L$ $\implies$ $\lim_{x \to a} g(x) = L$.
> - Each answer is written as on an exam paper: the computation first, then one short line per thought, joined by Since, $\because$, $\therefore$ and Hence. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 1.8.3
Question: [[CAL1 HW 1.8 Questions#ST 1.8.3|ST 1.8.3]]

> [!solution] Solution
> **(a)** $f$ is discontinuous at
> $$
> \begin{aligned}
> -4\ \ &\text{because } f(-4) \text{ is not defined.} \\
> -2\ \ &\text{because } \lim_{x \to -2^{-}} f(x) \ne \lim_{x \to -2^{+}} f(x) \implies \lim_{x \to -2} f(x) \text{ does not exist.} \\
> 2\ \ &\text{because } \lim_{x \to 2^{-}} f(x) \ne \lim_{x \to 2^{+}} f(x) \implies \lim_{x \to 2} f(x) \text{ does not exist.} \\
> 4\ \ &\text{because } \lim_{x \to 4^{-}} f(x) = -\infty \implies \lim_{x \to 4} f(x) \text{ does not exist.}
> \end{aligned}
> $$
> **(b)**
> $$
> \begin{aligned}
> \text{At } {-4}:\ \ &\text{neither, because } f(-4) \text{ is not defined.} \\
> \text{At } {-2}:\ \ &\text{from the left. } \lim_{x \to -2^{-}} f(x) = f(-2), \text{ while } \lim_{x \to -2^{+}} f(x) \ne f(-2). \\
> \text{At } 2:\ \ &\text{from the right. } \lim_{x \to 2^{+}} f(x) = f(2), \text{ while } \lim_{x \to 2^{-}} f(x) \ne f(2). \\
> \text{At } 4:\ \ &\text{from the right. } \lim_{x \to 4^{+}} f(x) = f(4), \text{ while } \lim_{x \to 4^{-}} f(x) = -\infty \ne f(4).
> \end{aligned}
> $$
>
> \# $-4$: removable. $\pm 2$: jump. $4$: infinite. At $0$ the graph has a corner but no break, so $f$ is continuous at $0$.
>
> ![[CAL1 HW 1.8 Solutions fig 3.png|480]]

### ST 1.8.13
Question: [[CAL1 HW 1.8 Questions#ST 1.8.13|ST 1.8.13]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\because \lim_{x \to -1} f(x) = \lim_{x \to -1} \left[3x^2 + (x + 2)^5\right] \\
> &\qquad = \lim_{x \to -1} 3x^2 + \lim_{x \to -1} (x + 2)^5 && \text{(Sum Law)} \\
> &\qquad = 3\lim_{x \to -1} x^2 + \lim_{x \to -1} (x + 2)^5 && \text{(Constant Multiple Law)} \\
> &\qquad = 3\left(\lim_{x \to -1} x\right)^2 + \left(\lim_{x \to -1} (x + 2)\right)^5 && \text{(Power Law)} \\
> &\qquad = 3\left(\lim_{x \to -1} x\right)^2 + \left(\lim_{x \to -1} x + \lim_{x \to -1} 2\right)^5 && \text{(Sum Law)} \\
> &\qquad = 3(-1)^2 + (-1 + 2)^5 && \text{(Identity, Constant Laws)} \\
> &\qquad = f(-1)
> \end{aligned}
> $$
> $\therefore$ $f$ is continuous at $a = -1$ by the definition of continuity. $\blacksquare$
>
> \# The chain may stop at $f(-1)$: the definition asks only for $\lim_{x \to -1} f(x) = f(-1)$, so the value $3 + 1 = 4$ is extra. Read from the bottom up, each law needs the limits on its right side to exist.

### ST 1.8.19
Question: [[CAL1 HW 1.8 Questions#ST 1.8.19|ST 1.8.19]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Since } \lim_{x \to -2^{-}} f(x) = -\infty \text{ and } \lim_{x \to -2^{+}} f(x) = \infty,\ \lim_{x \to -2} f(x) \text{ does not exist.} \\
> &\text{Hence } f \text{ is discontinuous at } a = -2.
> \end{aligned}
> $$
> ![[CAL1 HW 1.8 Solutions fig 19.png|380]]
>
> \# Infinite discontinuity. A second reason, even shorter: $f(-2)$ is not defined. The graph is $y = \tfrac{1}{x}$ shifted $2$ units to the left: asymptotes $x = -2$ and $y = 0$, $y$-intercept $\tfrac{1}{2}$.

### ST 1.8.21
Question: [[CAL1 HW 1.8 Questions#ST 1.8.21|ST 1.8.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\lim_{x \to 1^{-}} f(x) = \lim_{x \to 1^{-}} (1 - x^2) = 0, \qquad \lim_{x \to 1^{+}} f(x) = \lim_{x \to 1^{+}} \frac{1}{x} = 1 \\
> &\text{Since } \lim_{x \to 1^{-}} f(x) = 0 \ne 1 = \lim_{x \to 1^{+}} f(x),\ \lim_{x \to 1} f(x) \text{ does not exist.} \\
> &\text{Hence } f \text{ is discontinuous at } a = 1.
> \end{aligned}
> $$
> ![[CAL1 HW 1.8 Solutions fig 21.png|420]]
>
> \# Jump discontinuity. The first line shows where $0$ and $1$ come from: each side uses its own formula. $\lim_{x \to 1^{+}} f(x) = 1 = f(1)$, so $f$ is continuous from the right at $1$: the solid dot is on the right branch.

### ST 1.8.23
Question: [[CAL1 HW 1.8 Questions#ST 1.8.23|ST 1.8.23]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\lim_{x \to 0^{-}} f(x) = \lim_{x \to 0^{-}} \cos x = 1, \qquad \lim_{x \to 0^{+}} f(x) = \lim_{x \to 0^{+}} (1 - x^2) = 1 \\
> &\lim_{x \to 0^{-}} f(x) = 1 = \lim_{x \to 0^{+}} f(x) \implies \lim_{x \to 0} f(x) = 1 \\
> &\text{Since } \lim_{x \to 0} f(x) = 1 \ne 0 = f(0),\ f \text{ is discontinuous at } a = 0.
> \end{aligned}
> $$
> ![[CAL1 HW 1.8 Solutions fig 23.png|420]]
>
> \# Removable discontinuity: $f(0) = 1$ would make $f$ continuous at $0$. Exercises 19, 21 and 23 show three ways the definition of continuity fails: $f(a)$ is not defined and the limit is infinite; the one-sided limits differ; the limit exists but is not $f(a)$.

### ST 1.8.25
Question: [[CAL1 HW 1.8 Questions#ST 1.8.25|ST 1.8.25]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> \lim_{x \to 3} f(x) &= \lim_{x \to 3} \frac{x - 3}{x^2 - 9} \\
> &= \lim_{x \to 3} \frac{x - 3}{(x - 3)(x + 3)} && (x - 3 \ne 0) \\
> &= \lim_{x \to 3} \frac{1}{x + 3} \\
> &= \frac{1}{6} && \text{(Direct Substitution Property)}
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\text{Since Domain} = \mathbb{R} \setminus \{3, -3\},\ f(3) \text{ is not defined.} \\
> &\because \lim_{x \to 3} f(x) = \tfrac{1}{6},\ f(3) \text{ is not defined} \\
> &\therefore f \text{ has a removable discontinuity at } x = 3.
> \end{aligned}
> $$
> **(b)**
> $$
> \begin{aligned}
> &\text{Redefine } f(3) = \tfrac{1}{6}. \\
> &\text{Since } \lim_{x \to 3} f(x) = \tfrac{1}{6} = f(3),\ f \text{ is continuous at } x = 3.
> \end{aligned}
> $$
>
> \# Order: the limit first, then the domain, then both facts together. The last step of the limit is the Direct Substitution Property ($\tfrac{1}{x + 3}$ is rational and defined at $3$), not the Identity Law, which is only $\lim_{x \to a} x = a$. For $f(3)$ the exact wording is "is not defined". Removable means: the limit exists, and only the value $f(3)$ is missing.

### ST 1.8.27
Question: [[CAL1 HW 1.8 Questions#ST 1.8.27|ST 1.8.27]]

> [!solution] Solution
> **(1)** Domain
> $$
> \begin{aligned}
> &\because \forall x \in \mathbb{R},\ x^4 \ge 0 \implies x^4 + 2 \ge 2 > 0 \\
> &\therefore \sqrt{x^4 + 2} > 0 \text{ and is defined.} \\
> &\text{Hence the Domain of } f \text{ is } \mathbb{R}.
> \end{aligned}
> $$
> **(2)** Continuity
> $$
> \begin{aligned}
> &x^2 \text{ is a polynomial, so it is continuous } \forall x \in \mathbb{R}. && \text{(Theorem 5)} \\
> &x^4 + 2 \text{ is a polynomial, so it is continuous } \forall x \in \mathbb{R}. && \text{(Theorem 5)} \\
> &\sqrt{x} \text{ is continuous } \forall x \in [0, \infty). && \text{(Theorem 7)} \\
> &\because x^4 + 2 > 0\ \ \forall x \in \mathbb{R} \\
> &\therefore \sqrt{x^4 + 2} \text{ is continuous } \forall x \in \mathbb{R} \text{ and } \sqrt{x^4 + 2} > 0. && \text{(Theorem 9)} \\
> &\text{Hence } f \text{ is continuous } \forall x \in \mathbb{R}. && \text{(Theorem 4)}
> \end{aligned}
> $$
>
> \# The theorem numbers are in the right column only because this question asks for them; the words on the left are the reason. Theorem 9 is the composite $\sqrt{\ \cdot\ } \circ (x^4 + 2)$, and Theorem 4 is the quotient, which needs the denominator $\sqrt{x^4 + 2} \ne 0$.

### ST 1.8.29
Question: [[CAL1 HW 1.8 Questions#ST 1.8.29|ST 1.8.29]]

> [!solution] Solution
> **(1)** Domain
> $$
> \begin{aligned}
> &\because 1 - t^2 = 0 \iff t = 1 \text{ or } t = -1 \\
> &\therefore h(t) \text{ is defined} \iff t \ne 1, -1. \\
> &\text{Hence the Domain of } h \text{ is } \mathbb{R} \setminus \{1, -1\}.
> \end{aligned}
> $$
> **(2)** Continuity
> $$
> \begin{aligned}
> &t^2 \text{ is a polynomial, so it is continuous } \forall t \in \mathbb{R}. && \text{(Theorem 5)} \\
> &\cos x \text{ is continuous } \forall x \in \mathbb{R}. && \text{(Theorem 7)} \\
> &\therefore \cos(t^2) \text{ is continuous } \forall t \in \mathbb{R}. && \text{(Theorem 9)} \\
> &1 - t^2 \text{ is a polynomial, so it is continuous } \forall t \in \mathbb{R}. && \text{(Theorem 5)} \\
> &\because 1 - t^2 \ne 0\ \ \forall t \in \mathbb{R} \setminus \{1, -1\} \\
> &\therefore h \text{ is continuous } \forall t \in \mathbb{R} \setminus \{1, -1\}. && \text{(Theorem 4)}
> \end{aligned}
> $$
>
> \# The same plan as Exercise 27: the inside functions, then the composite, then the quotient with its denominator $\ne 0$.

### ST 1.8.31
Question: [[CAL1 HW 1.8 Questions#ST 1.8.31|ST 1.8.31]]

> [!solution] Solution
> **(1)** Domain
> $$
> \begin{aligned}
> &\because \sqrt{9 - v^2} \text{ is defined} \iff 9 - v^2 \ge 0 \iff v^2 \le 9 \iff -3 \le v \le 3 \\
> &\therefore \text{the Domain of } L \text{ is } [-3, 3].
> \end{aligned}
> $$
> **(2)** Continuity
> $$
> \begin{aligned}
> &v \text{ is a polynomial, so it is continuous } \forall v \in \mathbb{R}. && \text{(Theorem 5)} \\
> &9 - v^2 \text{ is a polynomial, so it is continuous } \forall v \in \mathbb{R}. && \text{(Theorem 5)} \\
> &\sqrt{x} \text{ is continuous } \forall x \in [0, \infty). && \text{(Theorem 7)} \\
> &\because 9 - v^2 \ge 0\ \ \forall v \in [-3, 3] \\
> &\therefore \sqrt{9 - v^2} \text{ is continuous } \forall v \in [-3, 3]. && \text{(Theorem 9)} \\
> &\text{Hence } L \text{ is continuous } \forall v \in [-3, 3]. && \text{(Theorem 4)}
> \end{aligned}
> $$
>
> \# Here Theorem 4 is the product $v \cdot \sqrt{9 - v^2}$. At the endpoints $\pm 3$, continuous means from one side: $\lim_{v \to -3^{+}} L(v) = 0 = L(-3)$ and $\lim_{v \to 3^{-}} L(v) = 0 = L(3)$.

### ST 1.8.35
Question: [[CAL1 HW 1.8 Questions#ST 1.8.35|ST 1.8.35]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Let } f(x) = x\sqrt{20 - x^2}. \\
> &x \text{ and } 20 - x^2 \text{ are polynomials, so they are continuous } \forall x \in \mathbb{R}. \\
> &\sqrt{x} \text{ is continuous } \forall x \in [0, \infty). \\
> &\because 20 - 2^2 = 16 > 0 \\
> &\therefore \sqrt{20 - x^2} \text{ is continuous at } x = 2, \text{ and so is } f. \\
> &\text{Hence } \lim_{x \to 2} x\sqrt{20 - x^2} = f(2) = 2\sqrt{16} = 8.
> \end{aligned}
> $$
>
> \# "Use continuity" means: show first that $f$ is continuous at $2$; then the limit is the value $f(2)$. Without the first four lines the substitution has no reason.

### ST 1.8.41
Question: [[CAL1 HW 1.8 Questions#ST 1.8.41|ST 1.8.41]]

> [!proof] Proof
> $$
> \begin{aligned}
> &1 - x^2 \text{ is a polynomial, so } f \text{ is continuous } \forall x < 1. \\
> &\because x - 1 \text{ is a polynomial},\ x - 1 > 0\ \ \forall x > 1,\ \sqrt{x} \text{ is continuous } \forall x \in [0, \infty) \\
> &\therefore f(x) = \sqrt{x - 1} \text{ is continuous } \forall x > 1. \\
> &\lim_{x \to 1^{-}} f(x) = \lim_{x \to 1^{-}} (1 - x^2) = 0, \qquad \lim_{x \to 1^{+}} f(x) = \lim_{x \to 1^{+}} \sqrt{x - 1} = 0 \\
> &\lim_{x \to 1^{-}} f(x) = 0 = \lim_{x \to 1^{+}} f(x) \implies \lim_{x \to 1} f(x) = 0 \\
> &\text{Since } \lim_{x \to 1} f(x) = 0 = f(1),\ f \text{ is continuous at } x = 1. \\
> &\text{Hence } f \text{ is continuous on } (-\infty, \infty). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Three places to check: left of $1$, right of $1$, and $1$ itself, where the formula changes. $\lim_{x \to 1^{+}} \sqrt{x - 1} = 0$ because the root function is continuous from the right at $0$.

### ST 1.8.45
Question: [[CAL1 HW 1.8 Questions#ST 1.8.45|ST 1.8.45]]

> [!solution] Solution
> $$
> \begin{aligned}
> &x + 2,\ 2x^2,\ 2 - x \text{ are polynomials, so } f \text{ is continuous } \forall x \ne 0, 1. \\[4pt]
> \text{At } 0:\ \ &\lim_{x \to 0^{-}} f(x) = \lim_{x \to 0^{-}} (x + 2) = 2, \qquad \lim_{x \to 0^{+}} f(x) = \lim_{x \to 0^{+}} 2x^2 = 0 \\
> &\text{Since } 2 \ne 0,\ \lim_{x \to 0} f(x) \text{ does not exist. Hence } f \text{ is discontinuous at } 0. \\
> &\lim_{x \to 0^{+}} f(x) = 0 = f(0), \text{ while } \lim_{x \to 0^{-}} f(x) = 2 \ne f(0) \\
> &\implies f \text{ is continuous from the right at } 0. \\[4pt]
> \text{At } 1:\ \ &\lim_{x \to 1^{-}} f(x) = \lim_{x \to 1^{-}} 2x^2 = 2, \qquad \lim_{x \to 1^{+}} f(x) = \lim_{x \to 1^{+}} (2 - x) = 1 \\
> &\text{Since } 2 \ne 1,\ \lim_{x \to 1} f(x) \text{ does not exist. Hence } f \text{ is discontinuous at } 1. \\
> &\lim_{x \to 1^{-}} f(x) = 2 = f(1), \text{ while } \lim_{x \to 1^{+}} f(x) = 1 \ne f(1) \\
> &\implies f \text{ is continuous from the left at } 1.
> \end{aligned}
> $$
> ![[CAL1 HW 1.8 Solutions fig 45.png|420]]
>
> \# Both are jump discontinuities. On the graph, the solid dot at each jump is on the side from which $f$ is continuous.

### ST 1.8.47
Question: [[CAL1 HW 1.8 Questions#ST 1.8.47|ST 1.8.47]]

> [!solution] Solution
> $$
> \begin{aligned}
> &cx^2 + 2x,\ x^3 - cx \text{ are polynomials, so } f \text{ is continuous } \forall x \ne 2. \\
> &\lim_{x \to 2^{-}} f(x) = \lim_{x \to 2^{-}} (cx^2 + 2x) = 4c + 4 \\
> &\lim_{x \to 2^{+}} f(x) = \lim_{x \to 2^{+}} (x^3 - cx) = 8 - 2c = f(2) \\
> &f \text{ is continuous at } 2 \iff \lim_{x \to 2^{-}} f(x) = \lim_{x \to 2^{+}} f(x) = f(2) \\
> &\phantom{f \text{ is continuous at } 2} \iff 4c + 4 = 8 - 2c \iff c = \tfrac{2}{3} \\
> &\text{Hence } c = \tfrac{2}{3}.
> \end{aligned}
> $$
>
> \# The only place that can go wrong is $2$, where the formula changes. Check: $c = \tfrac{2}{3}$ gives $4c + 4 = 8 - 2c = \tfrac{20}{3}$.

### ST 1.8.49
Question: [[CAL1 HW 1.8 Questions#ST 1.8.49|ST 1.8.49]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\because f,\ g \text{ are continuous at } 2 \\
> &\therefore 3f + fg \text{ is continuous at } 2 \quad \text{(sums and products of continuous functions)} \\
> &\implies \lim_{x \to 2} \left[3f(x) + f(x)g(x)\right] = 3f(2) + f(2)g(2) \\
> &\text{Since the limit is } 36 \text{ and } g(2) = 6:\quad 3f(2) + 6f(2) = 36 \implies 9f(2) = 36 \\
> &\text{Hence } f(2) = 4.
> \end{aligned}
> $$
>
> \# Continuity is what turns the limit into the values at $2$; after that it is one equation in $f(2)$.

### ST 1.8.55
Question: [[CAL1 HW 1.8 Questions#ST 1.8.55|ST 1.8.55]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } f(x) = -x^3 + 4x + 1. \\
> &f \text{ is a polynomial, so it is continuous on } [-1, 0]. \\
> &f(-1) = 1 - 4 + 1 = -2 < 0, \qquad f(0) = 1 > 0 \\
> &\because f \text{ is continuous on } [-1, 0],\ f(-1) < 0 < f(0) \\
> &\therefore \exists\, c \in (-1, 0) \text{ s.t. } f(c) = 0 \quad \text{(Intermediate Value Theorem)} \\
> &\text{Hence } -x^3 + 4x + 1 = 0 \text{ has a solution in } (-1, 0). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The Intermediate Value Theorem needs two things, and the $\because$ line holds both: $f$ continuous on the closed interval, and $0$ between the values at the endpoints. It gives existence only; here $c \approx -0.254$.

## ST §1.8 Additional Exercises

> [!note] Note
> These exercises are not assigned. Each one adds a type of problem that the assigned exercises do not cover.
> - 17: continuity on an interval with an endpoint (continuity from one side).
> - 48: two unknown constants and two numbers where the formula changes.
> - 50: the domain of a composite function; a formula that simplifies can hide a discontinuity.
> - 54: the Intermediate Value Theorem in a proof by contradiction, with no formula for $f$.
> - 64: the Intermediate Value Theorem used twice, with test numbers that we choose ourselves.
> - 72: a function that is continuous at exactly one number.
> - 73: the Squeeze Theorem at a number where the product and composite rules do not apply.
> - 74: the Intermediate Value Theorem for an equation with fractions; the denominators are checked afterwards.
> - 76: the continuity of $\lvert f \rvert$, and a converse that is false.

### ST 1.8.17
Question: [[CAL1 HW 1.8 Questions#ST 1.8.17|ST 1.8.17]]

> [!proof] Proof
> For $a > 4$:
> $$
> \begin{aligned}
> &\because \lim_{x \to a} f(x) = \lim_{x \to a} \left(x + \sqrt{x - 4}\right) \\
> &\qquad = \lim_{x \to a} x + \lim_{x \to a} \sqrt{x - 4} && \text{(Sum Law)} \\
> &\qquad = \lim_{x \to a} x + \sqrt{\lim_{x \to a} (x - 4)} && \text{(Root Law, } a - 4 > 0 \text{)} \\
> &\qquad = a + \sqrt{a - 4} && \text{(Identity, Difference, Constant Laws)} \\
> &\qquad = f(a)
> \end{aligned}
> $$
> $\therefore$ $f$ is continuous at $a$ by the definition of continuity.
>
> At $4$:
> $$
> \begin{aligned}
> &\lim_{x \to 4^{+}} f(x) = \lim_{x \to 4^{+}} x + \lim_{x \to 4^{+}} \sqrt{x - 4} = 4 + 0 = f(4) && \text{(Sum Law)} \\
> &\therefore f \text{ is continuous from the right at } 4. \\
> &\text{Hence } f \text{ is continuous on } [4, \infty). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The same chain as Exercise 13, with a letter $a$ in place of the number. An interval with an endpoint needs the endpoint separately, from one side. $\lim_{x \to 4^{+}} \sqrt{x - 4} = 0$ because the root function is continuous from the right at $0$.

### ST 1.8.48
Question: [[CAL1 HW 1.8 Questions#ST 1.8.48|ST 1.8.48]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\forall x < 2:\ \frac{x^2 - 4}{x - 2} = x + 2 \quad (x - 2 \ne 0) \\
> &x + 2,\ ax^2 - bx + 3,\ 2x - a + b \text{ are polynomials,} \\
> &\text{so } f \text{ is continuous } \forall x \ne 2, 3.
> \end{aligned}
> $$
> $$
> \begin{aligned}
> \text{At } 2:\ \ &\lim_{x \to 2^{-}} f(x) = \lim_{x \to 2^{-}} (x + 2) = 4 \\
> &\lim_{x \to 2^{+}} f(x) = 4a - 2b + 3 = f(2) \\
> &f \text{ is continuous at } 2 \iff 4 = 4a - 2b + 3 \\
> &\phantom{f \text{ is continuous at } 2} \iff 4a - 2b = 1 \quad (1) \\[4pt]
> \text{At } 3:\ \ &\lim_{x \to 3^{-}} f(x) = 9a - 3b + 3 \\
> &\lim_{x \to 3^{+}} f(x) = 6 - a + b = f(3) \\
> &f \text{ is continuous at } 3 \iff 9a - 3b + 3 = 6 - a + b \\
> &\phantom{f \text{ is continuous at } 3} \iff 10a - 4b = 3 \quad (2) \\[4pt]
> &(2) - 2 \cdot (1):\ 2a = 1 \implies a = \tfrac{1}{2} \implies b = \tfrac{1}{2} \\
> &\text{Hence } a = b = \tfrac{1}{2}.
> \end{aligned}
> $$
>
> \# The plan of Exercise 47, done twice: each number where the formula changes gives one equation. Check: the middle formula $\tfrac{1}{2}x^2 - \tfrac{1}{2}x + 3$ is $4$ at $x = 2$ and $6$ at $x = 3$; the last formula is $6$ at $x = 3$.

### ST 1.8.50
Question: [[CAL1 HW 1.8 Questions#ST 1.8.50|ST 1.8.50]]

> [!solution] Solution
> **(a)**
> $$
> (f \circ g)(x) = f\left(\frac{1}{x^2}\right) = \frac{1}{1/x^2} = x^2 \qquad (x \ne 0)
> $$
> **(b)** No.
> $$
> \begin{aligned}
> &\text{Since } g(0) \text{ is not defined},\ (f \circ g)(0) = f(g(0)) \text{ is not defined.} \\
> &\text{Hence } f \circ g \text{ is discontinuous at } 0.
> \end{aligned}
> $$
>
> \# The formula $x^2$ looks continuous everywhere, but $f \circ g$ keeps the restriction $x \ne 0$ of $g$. At every $a \ne 0$, $f \circ g$ is continuous. The discontinuity at $0$ is removable.

### ST 1.8.54
Question: [[CAL1 HW 1.8 Questions#ST 1.8.54|ST 1.8.54]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Since the only solutions of } f(x) = 6 \text{ are } x = 1, 4:\ f(3) \ne 6. \\
> &\text{Suppose } f(3) < 6. \\
> &\because f \text{ is continuous on } [2, 3],\ f(3) < 6 < 8 = f(2) \\
> &\therefore \exists\, c \in (2, 3) \text{ s.t. } f(c) = 6 \quad \text{(Intermediate Value Theorem)} \\
> &\text{But } c \ne 1, 4, \text{ which contradicts the first line.} \\
> &\text{Hence } f(3) > 6. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Graph view: on $(1, 4)$ the graph never meets the line $y = 6$, and at $x = 2$ it is above the line, so it stays above.

### ST 1.8.64
Question: [[CAL1 HW 1.8 Questions#ST 1.8.64|ST 1.8.64]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } f(x) = x^2 - 3 + \tfrac{1}{x}. \\
> &f \text{ is a rational function, so it is continuous } \forall x \ne 0. \\
> &f\left(\tfrac{1}{4}\right) = \tfrac{17}{16} > 0, \qquad f(1) = -1 < 0, \qquad f(2) = \tfrac{3}{2} > 0 \\
> &\because f \text{ is continuous on } \left[\tfrac{1}{4}, 1\right],\ f(1) < 0 < f\left(\tfrac{1}{4}\right) \\
> &\therefore \exists\, c_1 \in \left(\tfrac{1}{4}, 1\right) \text{ s.t. } f(c_1) = 0 \quad \text{(Intermediate Value Theorem)} \\
> &\because f \text{ is continuous on } [1, 2],\ f(1) < 0 < f(2) \\
> &\therefore \exists\, c_2 \in (1, 2) \text{ s.t. } f(c_2) = 0 \quad \text{(Intermediate Value Theorem)} \\
> &\text{Since } c_1 < 1 < c_2,\ c_1 \ne c_2. \\
> &\text{Hence the graph has at least two } x\text{-intercepts in } (0, 2). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $0$ cannot be an endpoint, because $f(0)$ is not defined. $f\left(\tfrac{1}{2}\right) = -\tfrac{3}{4} < 0$, so the first test number must be smaller than $\tfrac{1}{2}$. Here $c_1 \approx 0.347$ and $c_2 \approx 1.532$.

### ST 1.8.72
Question: [[CAL1 HW 1.8 Questions#ST 1.8.72|ST 1.8.72]]

> [!solution] Solution
> $g$ is continuous only at $x = 0$.

> [!proof] Proof
> At $0$:
> $$
> \begin{aligned}
> &\because {-\lvert x \rvert} \le g(x) \le \lvert x \rvert\ \ \forall x \in \mathbb{R},\ \lim_{x \to 0} \left(-\lvert x \rvert\right) = 0 = \lim_{x \to 0} \lvert x \rvert \\
> &\therefore \lim_{x \to 0} g(x) = 0 \quad \text{(Squeeze Theorem)} \\
> &\text{Since } \lim_{x \to 0} g(x) = 0 = g(0),\ g \text{ is continuous at } 0.
> \end{aligned}
> $$
> At $a \ne 0$: let $\varepsilon = \tfrac{\lvert a \rvert}{2}$. $\forall \delta > 0$:
> $$
> \begin{aligned}
> a \in \mathbb{Q}:\ \ &\exists\, s \notin \mathbb{Q} \text{ s.t. } 0 < \lvert s - a \rvert < \min\left\{\delta, \tfrac{\lvert a \rvert}{2}\right\} \\
> &\implies \lvert g(s) - g(a) \rvert = \lvert s \rvert > \tfrac{\lvert a \rvert}{2} = \varepsilon \\
> a \notin \mathbb{Q}:\ \ &\exists\, r \in \mathbb{Q} \text{ s.t. } 0 < \lvert r - a \rvert < \delta \\
> &\implies \lvert g(r) - g(a) \rvert = \lvert a \rvert > \varepsilon \\
> &\therefore \lim_{x \to a} g(x) = g(a) \text{ is false.} \\
> &\text{Hence } g \text{ is discontinuous at } a. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Every open interval contains a rational and an irrational number. For $a \in \mathbb{Q}$: $\lvert s \rvert \ge \lvert a \rvert - \lvert a - s \rvert > \tfrac{\lvert a \rvert}{2}$ (Triangle Inequality). The second part negates the [[Precise Definition of a Limit|precise definition of a limit]]: for this $\varepsilon$ no $\delta$ works. $\lim_{x \to 0} \lvert x \rvert = 0$ is [[CAL1 HW 1.7 Solutions#ST 1.7.27|ST 1.7.27]].

### ST 1.8.73
Question: [[CAL1 HW 1.8 Questions#ST 1.8.73|ST 1.8.73]]

> [!proof] Proof
> For $x \ne 0$:
> $$
> \begin{aligned}
> &\tfrac{1}{x} \text{ is a rational function, so it is continuous } \forall x \ne 0. \\
> &\sin x \text{ is continuous } \forall x \in \mathbb{R}. \\
> &\therefore \sin\tfrac{1}{x} \text{ is continuous } \forall x \ne 0. \\
> &x^4 \text{ is a polynomial, so it is continuous } \forall x \in \mathbb{R}. \\
> &\therefore f(x) = x^4\sin\tfrac{1}{x} \text{ is continuous } \forall x \ne 0.
> \end{aligned}
> $$
> At $0$:
> $$
> \begin{aligned}
> &\because {-1} \le \sin\tfrac{1}{x} \le 1 \implies {-x^4} \le x^4\sin\tfrac{1}{x} \le x^4 \quad (x \ne 0) \\
> &\phantom{\because}\ \lim_{x \to 0} \left(-x^4\right) = 0 = \lim_{x \to 0} x^4 \\
> &\therefore \lim_{x \to 0} f(x) = 0 \quad \text{(Squeeze Theorem)} \\
> &\text{Since } \lim_{x \to 0} f(x) = 0 = f(0),\ f \text{ is continuous at } 0. \\
> &\text{Hence } f \text{ is continuous on } (-\infty, \infty). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The first part cannot reach $0$, because $\tfrac{1}{x}$ is not defined there and $\lim_{x \to 0} \sin\tfrac{1}{x}$ does not exist. The Squeeze Theorem needs no limit of $\sin\tfrac{1}{x}$, only its bounds.

### ST 1.8.74
Question: [[CAL1 HW 1.8 Questions#ST 1.8.74|ST 1.8.74]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } D_1 = x^3 + 2x^2 - 1,\ D_2 = x^3 + x - 2,\ p = aD_2 + bD_1. \\
> &p \text{ is a polynomial, so it is continuous on } [-1, 1]. \\
> &p(-1) = -4a < 0, \qquad p(1) = 2b > 0 \\
> &\because p \text{ is continuous on } [-1, 1],\ p(-1) < 0 < p(1) \\
> &\therefore \exists\, c \in (-1, 1) \text{ s.t. } p(c) = 0 \quad \text{(Intermediate Value Theorem)} \\[4pt]
> &D_1 = (x + 1)(x^2 + x - 1), \qquad D_2 = (x - 1)(x^2 + x + 2) \\
> &\implies \text{in } (-1, 1):\ D_1D_2 = 0 \text{ only at } r = \tfrac{-1 + \sqrt{5}}{2} \\
> &\because r^2 = 1 - r,\ r^3 = 2r - 1 \implies p(r) = aD_2(r) = 3a(r - 1) < 0 \\
> &\therefore c \ne r \implies D_1(c)D_2(c) \ne 0 \\
> &\text{Hence } \frac{a}{D_1(c)} + \frac{b}{D_2(c)} = \frac{p(c)}{D_1(c)D_2(c)} = 0. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Multiplying the equation by $D_1D_2$ gives the polynomial $p$, and the first half is Exercise 55 again. $p(c) = 0$ solves the equation only if no denominator is $0$ at $c$; that is why $r$ is checked. $x^2 + x + 2$ has no real zero (discriminant $-7$), and the other zero of $x^2 + x - 1$ is $\tfrac{-1 - \sqrt{5}}{2} < -1$.

### ST 1.8.76
Question: [[CAL1 HW 1.8 Questions#ST 1.8.76|ST 1.8.76]]

> [!proof] Proof of (a)
> $$
> \begin{aligned}
> a > 0:\ \ &\lvert x \rvert = x \text{ near } a \implies \lim_{x \to a} \lvert x \rvert = \lim_{x \to a} x = a = \lvert a \rvert \\
> a < 0:\ \ &\lvert x \rvert = -x \text{ near } a \implies \lim_{x \to a} \lvert x \rvert = \lim_{x \to a} (-x) = -a = \lvert a \rvert \\
> a = 0:\ \ &\lim_{x \to 0} \lvert x \rvert = 0 = \lvert 0 \rvert && \text{(ST 1.7.27)} \\
> &\therefore \lim_{x \to a} F(x) = F(a)\ \ \forall a \in \mathbb{R}. \\
> &\text{Hence } F \text{ is continuous } \forall x \in \mathbb{R}. \qquad \blacksquare
> \end{aligned}
> $$

> [!proof] Proof of (b)
> $$
> \begin{aligned}
> &\text{Let } a \text{ be in the interval.} \\
> &\because f \text{ is continuous at } a,\ F(x) = \lvert x \rvert \text{ is continuous at } f(a) \quad \text{(by (a))} \\
> &\therefore \lvert f \rvert = F \circ f \text{ is continuous at } a \quad \text{(composite of continuous functions)} \\
> &\text{Hence } \lvert f \rvert \text{ is continuous on the interval.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# At an endpoint of the interval, use the one-sided limit.

> [!solution] Solution
> **(c)** No.
> $$
> \begin{aligned}
> &\text{Let } f(x) = \begin{cases} 1 & x \ge 0 \\ -1 & x < 0 \end{cases} \\
> &\lvert f(x) \rvert = 1\ \ \forall x \in \mathbb{R} \implies \lvert f \rvert \text{ is continuous } \forall x \in \mathbb{R}. \\
> &\text{Since } \lim_{x \to 0^{-}} f(x) = -1 \ne 1 = \lim_{x \to 0^{+}} f(x),\ \lim_{x \to 0} f(x) \text{ does not exist.} \\
> &\text{Hence } f \text{ is discontinuous at } 0.
> \end{aligned}
> $$
>
> \# A counterexample has to show both halves: $\lvert f \rvert$ is continuous, and $f$ is not.
