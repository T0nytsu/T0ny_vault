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
| [[CAL1 HW 1.8 Questions#ST 1.8.19\|ST 1.8.19]] | $f(-2)$ is not defined; graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.21\|ST 1.8.21]] | $\lim_{x \to 1^{-}} f(x) = 0 \ne 1 = \lim_{x \to 1^{+}} f(x)$; graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.23\|ST 1.8.23]] | $\lim_{x \to 0} f(x) = 1 \ne 0 = f(0)$; graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.25\|ST 1.8.25]] | (a) $\lim_{x \to 3} f(x) = \tfrac{1}{6}$, $f(3)$ is not defined; (b) $f(3) = \tfrac{1}{6}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.27\|ST 1.8.27]] | Domain $\mathbb{R}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.29\|ST 1.8.29]] | Domain $\mathbb{R} \setminus \{\pm 1\}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.31\|ST 1.8.31]] | Domain $[-3, 3]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.35\|ST 1.8.35]] | $8$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.41\|ST 1.8.41]] | Proof: $\lim_{x \to 1^{-}} f(x) = \lim_{x \to 1^{+}} f(x) = 0 = f(1)$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.45\|ST 1.8.45]] | Discontinuous at $0$ (continuous from the right) and at $1$ (continuous from the left); graph |
| [[CAL1 HW 1.8 Questions#ST 1.8.47\|ST 1.8.47]] | $c = \tfrac{2}{3}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.49\|ST 1.8.49]] | $f(2) = 4$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.55\|ST 1.8.55]] | Proof: IVT on $[-1, 0]$, $f(-1) = -2 < 0 < 1 = f(0)$ |

Additional exercises, not assigned:

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 1.8 Questions#ST 1.8.17\|ST 1.8.17]] | Proof: $\lim_{x \to a} f(x) = f(a)$ for $a > 4$; $\lim_{x \to 4^{+}} f(x) = f(4)$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.48\|ST 1.8.48]] | $a = b = \tfrac{1}{2}$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.50\|ST 1.8.50]] | (a) $x^2$, $x \ne 0$; (b) No |
| [[CAL1 HW 1.8 Questions#ST 1.8.54\|ST 1.8.54]] | Proof by contradiction: IVT on $[2, 3]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.64\|ST 1.8.64]] | Proof: IVT on $\left[\tfrac{1}{4}, 1\right]$ and on $[1, 2]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.72\|ST 1.8.72]] | Only at $x = 0$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.73\|ST 1.8.73]] | Proof: Thm 4, 5, 7, 9 for $a \ne 0$; Squeeze Thm at $0$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.74\|ST 1.8.74]] | Proof: IVT for $p(x) = a(x^3 + x - 2) + b(x^3 + 2x^2 - 1)$ on $[-1, 1]$ |
| [[CAL1 HW 1.8 Questions#ST 1.8.76\|ST 1.8.76]] | (a), (b) Proofs; (c) No: $f(x) = 1$ ($x \ge 0$), $-1$ ($x < 0$) |

## ST §1.8 Continuity

> [!note] Note
> Results cited in the reason column. A number without a section refers to ST §1.8. The scan holds only the exercise pages, so these statements are written from the standard text of ST §1.8, not copied from the scan; compare the numbers with the book.
> - **Def 1** ([[Continuity|continuous]] at $a$): $\lim_{x \to a} f(x) = f(a)$. It needs: $f(a)$ is defined, $\lim_{x \to a} f(x)$ exists, and both are equal.
> - **Def 2**: continuous from the right at $a$: $\lim_{x \to a^{+}} f(x) = f(a)$; from the left: $\lim_{x \to a^{-}} f(x) = f(a)$.
> - **Def 3**: continuous on an interval: continuous at every number in it, and from one side at an endpoint.
> - **Thm 4**: $f$, $g$ continuous at $a$ $\implies$ $f + g$, $f - g$, $cf$, $fg$, and $\tfrac{f}{g}$ if $g(a) \ne 0$, are continuous at $a$.
> - **Thm 5**: polynomials are continuous on $\mathbb{R}$; rational functions are continuous on their domains.
> - **Thm 7**: polynomials, rational functions, root functions and trigonometric functions are continuous on their domains.
> - **Thm 8**: $f$ continuous at $b$, $\lim_{x \to a} g(x) = b$ $\implies$ $\lim_{x \to a} f(g(x)) = f(b)$.
> - **Thm 9**: $g$ continuous at $a$, $f$ continuous at $g(a)$ $\implies$ $f \circ g$ continuous at $a$.
> - **IVT** (Thm 10, [[Intermediate Value Theorem]]): $f$ continuous on $[a, b]$, $N$ between $f(a)$ and $f(b)$, $f(a) \ne f(b)$ $\implies$ $\exists\, c \in (a, b)$ s.t. $f(c) = N$.
> - **[[Discontinuity]]** at $a$: *removable* ($\lim_{x \to a} f(x)$ exists), *jump* (the one-sided limits exist and differ), *infinite* (a one-sided limit is $\pm\infty$, see [[Infinite Limit]]).
> - **Limit Laws** (ST §1.6): Sum, Difference, Constant Multiple, Product, Quotient, Power and Root Laws; Constant Law: $\lim_{x \to a} c = c$; Identity Law: $\lim_{x \to a} x = a$.
> - **Thm 1.6.1** ([[One-Sided Limit]]): $\lim_{x \to a} f(x) = L$ $\iff$ $\lim_{x \to a^{-}} f(x) = L = \lim_{x \to a^{+}} f(x)$.
> - **Squeeze Thm** ([[Squeeze Theorem]], ST §1.6): $f(x) \le g(x) \le h(x)$ near $a$, $\lim_{x \to a} f(x) = \lim_{x \to a} h(x) = L$ $\implies$ $\lim_{x \to a} g(x) = L$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 1.8.3
Question: [[CAL1 HW 1.8 Questions#ST 1.8.3|ST 1.8.3]]

> [!solution] Solution
> **(a)** $f$ is discontinuous at
> $$
> \begin{aligned}
> -4 &:\ f(-4) \text{ is not defined} \\
> -2 &:\ \lim_{x \to -2^{-}} f(x) \ne \lim_{x \to -2^{+}} f(x) \implies \lim_{x \to -2} f(x) \text{ does not exist} \\
> 2 &:\ \lim_{x \to 2^{-}} f(x) \ne \lim_{x \to 2^{+}} f(x) \implies \lim_{x \to 2} f(x) \text{ does not exist} \\
> 4 &:\ \lim_{x \to 4^{-}} f(x) = -\infty \implies \lim_{x \to 4} f(x) \text{ does not exist}
> \end{aligned}
> $$
> **(b)**
> $$
> \begin{aligned}
> -4 &:\ \text{neither} && f(-4) \text{ is not defined} \\
> -2 &:\ \text{from the left} && \lim_{x \to -2^{-}} f(x) = f(-2) \ne \lim_{x \to -2^{+}} f(x) \\
> 2 &:\ \text{from the right} && \lim_{x \to 2^{+}} f(x) = f(2) \ne \lim_{x \to 2^{-}} f(x) \\
> 4 &:\ \text{from the right} && \lim_{x \to 4^{+}} f(x) = f(4),\ \lim_{x \to 4^{-}} f(x) = -\infty
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
> &\lim_{x \to -1} f(x) = \lim_{x \to -1} \left[3x^2 + (x + 2)^5\right] \\
> &\quad = \lim_{x \to -1} 3x^2 + \lim_{x \to -1} (x + 2)^5 && \text{(Sum Law)} \\
> &\quad = 3\lim_{x \to -1} x^2 + \lim_{x \to -1} (x + 2)^5 && \text{(Constant Multiple Law)} \\
> &\quad = 3\left(\lim_{x \to -1} x\right)^2 + \left(\lim_{x \to -1} (x + 2)\right)^5 && \text{(Power Law)} \\
> &\quad = 3\left(\lim_{x \to -1} x\right)^2 + \left(\lim_{x \to -1} x + \lim_{x \to -1} 2\right)^5 && \text{(Sum Law)} \\
> &\quad = 3(-1)^2 + (-1 + 2)^5 && \text{(Identity, Constant Laws)} \\
> &\quad = f(-1)
> \end{aligned}
> $$
> $\therefore$ $f$ is continuous at $-1$ (Def 1). $\blacksquare$
>
> \# The chain ends at $f(-1)$, which is all Def 1 asks for; the value $3 + 1 = 4$ is not needed. Each law is used from the bottom up: it needs the limits on its right side to exist.

### ST 1.8.19
Question: [[CAL1 HW 1.8 Questions#ST 1.8.19|ST 1.8.19]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(-2) \text{ is not defined} \implies f \text{ is discontinuous at } {-2} \\
> &\lim_{x \to -2^{-}} f(x) = -\infty, \qquad \lim_{x \to -2^{+}} f(x) = \infty
> \end{aligned}
> $$
> ![[CAL1 HW 1.8 Solutions fig 19.png|380]]
>
> \# Infinite discontinuity. The graph is $y = \tfrac{1}{x}$ shifted $2$ units to the left: asymptotes $x = -2$ and $y = 0$, $y$-intercept $\tfrac{1}{2}$.

### ST 1.8.21
Question: [[CAL1 HW 1.8 Questions#ST 1.8.21|ST 1.8.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\lim_{x \to 1^{-}} f(x) = \lim_{x \to 1^{-}} (1 - x^2) = 0 \\
> &\lim_{x \to 1^{+}} f(x) = \lim_{x \to 1^{+}} \frac{1}{x} = 1 \\
> &\because 0 \ne 1 \quad \therefore \lim_{x \to 1} f(x) \text{ does not exist} \implies f \text{ is discontinuous at } 1
> \end{aligned}
> $$
> ![[CAL1 HW 1.8 Solutions fig 21.png|420]]
>
> \# Jump discontinuity. $\lim_{x \to 1^{+}} f(x) = 1 = f(1)$, so $f$ is continuous from the right at $1$: the solid dot is on the right branch.

### ST 1.8.23
Question: [[CAL1 HW 1.8 Questions#ST 1.8.23|ST 1.8.23]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\lim_{x \to 0^{-}} f(x) = \lim_{x \to 0^{-}} \cos x = 1 \\
> &\lim_{x \to 0^{+}} f(x) = \lim_{x \to 0^{+}} (1 - x^2) = 1 \\
> &\implies \lim_{x \to 0} f(x) = 1 \ne 0 = f(0) \implies f \text{ is discontinuous at } 0
> \end{aligned}
> $$
> ![[CAL1 HW 1.8 Solutions fig 23.png|420]]
>
> \# Removable discontinuity: $f(0) = 1$ would make $f$ continuous at $0$. Exercises 19, 21 and 23 show the three ways Def 1 fails: $f(a)$ is not defined; the limit does not exist; the limit is not $f(a)$.

### ST 1.8.25
Question: [[CAL1 HW 1.8 Questions#ST 1.8.25|ST 1.8.25]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> &3^2 - 9 = 0 \implies f(3) \text{ is not defined} \implies f \text{ is discontinuous at } 3 \\
> &\lim_{x \to 3} f(x) = \lim_{x \to 3} \frac{x - 3}{(x - 3)(x + 3)} = \lim_{x \to 3} \frac{1}{x + 3} = \frac{1}{6} \qquad (x \ne 3) \\
> &\therefore \text{the discontinuity at } 3 \text{ is removable}
> \end{aligned}
> $$
> **(b)**
> $$
> f(3) := \tfrac{1}{6} \implies \lim_{x \to 3} f(x) = \tfrac{1}{6} = f(3) \implies f \text{ is continuous at } 3
> $$
>
> \# Removable means: the limit exists and only the value $f(3)$ is missing or wrong. The last limit is by direct substitution ($\tfrac{1}{x + 3}$ is rational and defined at $3$, Thm 5). At $-3$ the discontinuity is infinite and cannot be removed.

### ST 1.8.27
Question: [[CAL1 HW 1.8 Questions#ST 1.8.27|ST 1.8.27]]

> [!solution] Solution
> **Domain.**
> $$
> \forall x \in \mathbb{R}:\ x^4 \ge 0 \implies x^4 + 2 \ge 2 > 0 \qquad \therefore \text{Domain} = \mathbb{R}
> $$
> **Continuity.**
> $$
> \begin{aligned}
> &x^2,\ x^4 + 2 \text{: polynomials} \implies \text{continuous on } \mathbb{R} && \text{(Thm 5)} \\
> &\sqrt{u} \text{ continuous on } [0, \infty) && \text{(Thm 7)} \\
> &x^4 + 2 > 0 \implies \sqrt{x^4 + 2} \text{ continuous on } \mathbb{R} && \text{(Thm 9)} \\
> &\sqrt{x^4 + 2} \ne 0 \implies f \text{ continuous on } \mathbb{R} && \text{(Thm 4)}
> \end{aligned}
> $$

### ST 1.8.29
Question: [[CAL1 HW 1.8 Questions#ST 1.8.29|ST 1.8.29]]

> [!solution] Solution
> **Domain.**
> $$
> 1 - t^2 = 0 \iff t = \pm 1 \qquad \therefore \text{Domain} = \mathbb{R} \setminus \{\pm 1\}
> $$
> **Continuity.**
> $$
> \begin{aligned}
> &t^2,\ 1 - t^2 \text{: polynomials} \implies \text{continuous on } \mathbb{R} && \text{(Thm 5)} \\
> &\cos u \text{ continuous on } \mathbb{R} && \text{(Thm 7)} \\
> &\implies \cos(t^2) \text{ continuous on } \mathbb{R} && \text{(Thm 9)} \\
> &1 - t^2 \ne 0 \text{ on the domain} \implies h \text{ continuous on it} && \text{(Thm 4)}
> \end{aligned}
> $$
>
> \# In interval notation the domain is $(-\infty, -1) \cup (-1, 1) \cup (1, \infty)$.

### ST 1.8.31
Question: [[CAL1 HW 1.8 Questions#ST 1.8.31|ST 1.8.31]]

> [!solution] Solution
> **Domain.**
> $$
> 9 - v^2 \ge 0 \iff -3 \le v \le 3 \qquad \therefore \text{Domain} = [-3, 3]
> $$
> **Continuity.**
> $$
> \begin{aligned}
> &v,\ 9 - v^2 \text{: polynomials} \implies \text{continuous on } \mathbb{R} && \text{(Thm 5)} \\
> &\sqrt{u} \text{ continuous on } [0, \infty) && \text{(Thm 7)} \\
> &\implies \sqrt{9 - v^2} \text{ continuous on } [-3, 3] && \text{(Thm 9)} \\
> &\implies L(v) = v\sqrt{9 - v^2} \text{ continuous on } [-3, 3] && \text{(Thm 4)}
> \end{aligned}
> $$
>
> \# At the endpoints $\pm 3$, continuous means from one side (Def 3): $\lim_{v \to -3^{+}} L(v) = 0 = L(-3)$ and $\lim_{v \to 3^{-}} L(v) = 0 = L(3)$.

### ST 1.8.35
Question: [[CAL1 HW 1.8 Questions#ST 1.8.35|ST 1.8.35]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(x) = x\sqrt{20 - x^2} \text{ is continuous on its domain} && \text{(Thm 4, 5, 7, 9)} \\
> &20 - 2^2 = 16 > 0 \implies f \text{ continuous at } 2 \\
> &\therefore \lim_{x \to 2} x\sqrt{20 - x^2} = f(2) = 2\sqrt{16} = 8
> \end{aligned}
> $$

### ST 1.8.41
Question: [[CAL1 HW 1.8 Questions#ST 1.8.41|ST 1.8.41]]

> [!proof] Proof
> $$
> \begin{aligned}
> &x < 1:\ f(x) = 1 - x^2 \implies f \text{ continuous} \quad \text{(Thm 5)} \\
> &x > 1:\ f(x) = \sqrt{x - 1} \implies f \text{ continuous} \quad \text{(Thm 5, 7, 9)} \\
> &x = 1:\ \lim_{x \to 1^{-}} f(x) = \lim_{x \to 1^{-}} (1 - x^2) = 0 \\
> &\phantom{x = 1:\ } \lim_{x \to 1^{+}} f(x) = \lim_{x \to 1^{+}} \sqrt{x - 1} = 0 \\
> &\phantom{x = 1:\ } \implies \lim_{x \to 1} f(x) = 0 = f(1) \implies f \text{ continuous} \\
> &\therefore f \text{ is continuous on } (-\infty, \infty) \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $\lim_{x \to 1^{+}} \sqrt{x - 1} = 0$ because the root function is continuous from the right at $0$ (Definition 4 of ST §1.7 with $\delta = \varepsilon^2$).

### ST 1.8.45
Question: [[CAL1 HW 1.8 Questions#ST 1.8.45|ST 1.8.45]]

> [!solution] Solution
> $$
> \begin{aligned}
> &x \ne 0, 1:\ f \text{ is a polynomial near } x \implies f \text{ continuous} \quad \text{(Thm 5)} \\
> &x = 0:\ \lim_{x \to 0^{-}} f(x) = \lim_{x \to 0^{-}} (x + 2) = 2 \\
> &\phantom{x = 0:\ } \lim_{x \to 0^{+}} f(x) = \lim_{x \to 0^{+}} 2x^2 = 0 = f(0) \\
> &\phantom{x = 0:\ } \implies \text{discontinuous at } 0,\ \text{continuous from the right} \\
> &x = 1:\ \lim_{x \to 1^{-}} f(x) = \lim_{x \to 1^{-}} 2x^2 = 2 = f(1) \\
> &\phantom{x = 1:\ } \lim_{x \to 1^{+}} f(x) = \lim_{x \to 1^{+}} (2 - x) = 1 \\
> &\phantom{x = 1:\ } \implies \text{discontinuous at } 1,\ \text{continuous from the left}
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
> &x \ne 2:\ f \text{ is a polynomial near } x \implies f \text{ continuous} && \text{(Thm 5)} \\
> &x = 2:\ \lim_{x \to 2^{-}} f(x) = \lim_{x \to 2^{-}} (cx^2 + 2x) = 4c + 4 \\
> &\phantom{x = 2:\ } \lim_{x \to 2^{+}} f(x) = \lim_{x \to 2^{+}} (x^3 - cx) = 8 - 2c = f(2) \\
> &f \text{ continuous at } 2 \iff 4c + 4 = 8 - 2c \iff c = \tfrac{2}{3}
> \end{aligned}
> $$
>
> \# Check: $c = \tfrac{2}{3}$ gives $4c + 4 = 8 - 2c = \tfrac{20}{3}$.

### ST 1.8.49
Question: [[CAL1 HW 1.8 Questions#ST 1.8.49|ST 1.8.49]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f,\ g \text{ continuous at } 2 \implies 3f + fg \text{ continuous at } 2 \quad \text{(Thm 4)} \\
> &\implies 36 = \lim_{x \to 2} \left[3f(x) + f(x)g(x)\right] = 3f(2) + f(2)g(2) \\
> &\phantom{\implies 36} = 9f(2) \quad (g(2) = 6) \\
> &\therefore f(2) = 4
> \end{aligned}
> $$

### ST 1.8.55
Question: [[CAL1 HW 1.8 Questions#ST 1.8.55|ST 1.8.55]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } f(x) = -x^3 + 4x + 1. \\
> &f \text{: polynomial} \implies f \text{ continuous on } [-1, 0] && \text{(Thm 5)} \\
> &f(-1) = -2 < 0 < 1 = f(0) \\
> &\implies \exists\, c \in (-1, 0) \text{ s.t. } f(c) = 0 && \text{(IVT)} \\
> &\therefore -x^3 + 4x + 1 = 0 \text{ has a solution in } (-1, 0) \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The IVT takes three steps: move all terms to one side to get $f$; $f$ continuous on the closed interval; opposite signs at the endpoints. It gives existence only; here $c \approx -0.254$.

## ST §1.8 Additional Exercises

> [!note] Note
> These exercises are not assigned. Each one adds a type of problem that the assigned exercises do not cover.
> - 17: continuity on an interval with an endpoint (continuity from one side, Def 3).
> - 48: two unknown constants and two numbers where the formula changes.
> - 50: the domain of a composite function; a formula that simplifies can hide a discontinuity.
> - 54: the IVT in a proof by contradiction, with no formula for $f$.
> - 64: the IVT used twice, with test numbers that we choose ourselves.
> - 72: a function that is continuous at exactly one number.
> - 73: the Squeeze Thm at a number where Thm 4 and Thm 9 do not apply.
> - 74: the IVT for an equation with fractions; the denominators are checked afterwards.
> - 76: the continuity of $\lvert f \rvert$, and a converse that is false.

### ST 1.8.17
Question: [[CAL1 HW 1.8 Questions#ST 1.8.17|ST 1.8.17]]

> [!proof] Proof
> $$
> \begin{aligned}
> a > 4:\ \lim_{x \to a} f(x) &= \lim_{x \to a} x + \lim_{x \to a} \sqrt{x - 4} && \text{(Sum Law)} \\
> &= \lim_{x \to a} x + \sqrt{\lim_{x \to a} (x - 4)} && \text{(Root Law)} \\
> &= a + \sqrt{a - 4} = f(a) \\
> a = 4:\ \lim_{x \to 4^{+}} f(x) &= \lim_{x \to 4^{+}} x + \lim_{x \to 4^{+}} \sqrt{x - 4} && \text{(Sum Law)} \\
> &= 4 + 0 = f(4)
> \end{aligned}
> $$
> $\therefore$ $f$ is continuous at every $a > 4$ and from the right at $4$ $\implies$ $f$ is continuous on $[4, \infty)$ (Def 3). $\blacksquare$
>
> \# The Root Law needs $\lim_{x \to a} (x - 4) = a - 4 > 0$. At the endpoint, $\lim_{x \to 4^{+}} \sqrt{x - 4} = 0$ (Definition 4 of ST §1.7 with $\delta = \varepsilon^2$).

### ST 1.8.48
Question: [[CAL1 HW 1.8 Questions#ST 1.8.48|ST 1.8.48]]

> [!solution] Solution
> $$
> \begin{aligned}
> &x < 2:\ \frac{x^2 - 4}{x - 2} = x + 2 \\
> &x \ne 2, 3:\ f \text{ is a polynomial near } x \implies f \text{ continuous} && \text{(Thm 5)} \\
> &x = 2:\ \lim_{x \to 2^{-}} f(x) = \lim_{x \to 2^{-}} (x + 2) = 4 \\
> &\phantom{x = 2:\ } \lim_{x \to 2^{+}} f(x) = 4a - 2b + 3 = f(2) \\
> &\phantom{x = 2:\ } \implies 4a - 2b = 1 && (1) \\
> &x = 3:\ \lim_{x \to 3^{-}} f(x) = 9a - 3b + 3 \\
> &\phantom{x = 3:\ } \lim_{x \to 3^{+}} f(x) = 6 - a + b = f(3) \\
> &\phantom{x = 3:\ } \implies 10a - 4b = 3 && (2) \\
> &(2) - 2 \cdot (1):\ 2a = 1 \implies a = \tfrac{1}{2},\ b = \tfrac{1}{2}
> \end{aligned}
> $$
>
> \# Check: the middle formula $\tfrac{1}{2}x^2 - \tfrac{1}{2}x + 3$ is $4$ at $x = 2$ and $6$ at $x = 3$; the last formula is $6$ at $x = 3$.

### ST 1.8.50
Question: [[CAL1 HW 1.8 Questions#ST 1.8.50|ST 1.8.50]]

> [!solution] Solution
> **(a)**
> $$
> (f \circ g)(x) = f\left(\frac{1}{x^2}\right) = \frac{1}{1/x^2} = x^2, \qquad x \ne 0
> $$
> **(b)** No.
> $$
> \begin{aligned}
> &g(0) \text{ is not defined} \implies (f \circ g)(0) \text{ is not defined} \\
> &\implies f \circ g \text{ is discontinuous at } 0
> \end{aligned}
> $$
>
> \# The formula $x^2$ looks continuous everywhere, but $f \circ g$ keeps the restriction $x \ne 0$ of $g$. At every $a \ne 0$, $f \circ g$ is continuous (Thm 5, 9). The discontinuity at $0$ is removable.

### ST 1.8.54
Question: [[CAL1 HW 1.8 Questions#ST 1.8.54|ST 1.8.54]]

> [!proof] Proof
> $$
> \begin{aligned}
> &3 \ne 1, 4 \implies f(3) \ne 6 \\
> &\text{Suppose } f(3) < 6. \\
> &f \text{ continuous on } [2, 3],\quad f(3) < 6 < 8 = f(2) \\
> &\implies \exists\, c \in (2, 3) \text{ s.t. } f(c) = 6 && \text{(IVT)} \\
> &\implies \text{contradiction: } c \ne 1, 4 \\
> &\therefore f(3) > 6 \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Graph view: on $(1, 4)$ the graph never meets the line $y = 6$, and at $x = 2$ it is above the line, so it stays above.

### ST 1.8.64
Question: [[CAL1 HW 1.8 Questions#ST 1.8.64|ST 1.8.64]]

> [!proof] Proof
> $$
> \begin{aligned}
> &f(x) = x^2 - 3 + \tfrac{1}{x} \text{: rational} \implies f \text{ continuous on } (0, \infty) && \text{(Thm 5)} \\
> &f\left(\tfrac{1}{4}\right) = \tfrac{17}{16} > 0,\quad f(1) = -1 < 0,\quad f(2) = \tfrac{3}{2} > 0 \\
> &\implies \exists\, c_1 \in \left(\tfrac{1}{4}, 1\right),\ c_2 \in (1, 2) \text{ s.t. } f(c_1) = f(c_2) = 0 && \text{(IVT)} \\
> &c_1 < 1 < c_2 \quad \therefore \text{at least two } x\text{-intercepts in } (0, 2) \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $0$ cannot be an endpoint, because $f(0)$ is not defined. $f\left(\tfrac{1}{2}\right) = -\tfrac{3}{4} < 0$, so the first test number must be smaller than $\tfrac{1}{2}$. Here $c_1 \approx 0.347$ and $c_2 \approx 1.532$.

### ST 1.8.72
Question: [[CAL1 HW 1.8 Questions#ST 1.8.72|ST 1.8.72]]

> [!solution] Solution
> $g$ is continuous only at $x = 0$.

> [!proof] Proof
> $$
> \begin{aligned}
> &a = 0:\ {-\lvert x \rvert} \le g(x) \le \lvert x \rvert,\quad \lim_{x \to 0} \left(\pm\lvert x \rvert\right) = 0 \\
> &\phantom{a = 0:\ } \implies \lim_{x \to 0} g(x) = 0 = g(0) \quad \text{(Squeeze Thm)} \\
> &a \ne 0:\ \text{let } \varepsilon = \tfrac{\lvert a \rvert}{2}.\ \ \forall \delta > 0: \\
> &a \in \mathbb{Q}:\ \exists\, s \notin \mathbb{Q} \text{ s.t. } 0 < \lvert s - a \rvert < \min\left\{\delta, \tfrac{\lvert a \rvert}{2}\right\} \\
> &\phantom{a \in \mathbb{Q}:\ } \implies \lvert g(s) - g(a) \rvert = \lvert s \rvert > \tfrac{\lvert a \rvert}{2} = \varepsilon \\
> &a \notin \mathbb{Q}:\ \exists\, r \in \mathbb{Q} \text{ s.t. } 0 < \lvert r - a \rvert < \delta \\
> &\phantom{a \notin \mathbb{Q}:\ } \implies \lvert g(r) - g(a) \rvert = \lvert a \rvert > \varepsilon \\
> &\therefore \lim_{x \to a} g(x) = g(a) \text{ is false} \implies g \text{ is discontinuous at } a \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Every open interval contains a rational and an irrational number. For $a \in \mathbb{Q}$: $\lvert s \rvert \ge \lvert a \rvert - \lvert a - s \rvert > \tfrac{\lvert a \rvert}{2}$ (Triangle Inequality). The second part negates the [[Precise Definition of a Limit|precise definition of a limit]]: for this $\varepsilon$ no $\delta$ works. $\lim_{x \to 0} \lvert x \rvert = 0$ is [[CAL1 HW 1.7 Solutions#ST 1.7.27|ST 1.7.27]].

### ST 1.8.73
Question: [[CAL1 HW 1.8 Questions#ST 1.8.73|ST 1.8.73]]

> [!proof] Proof
> $$
> \begin{aligned}
> &a \ne 0:\ \tfrac{1}{x} \text{ rational},\ \sin \text{ continuous},\ x^4 \text{ polynomial} \\
> &\phantom{a \ne 0:\ } \implies f \text{ continuous at } a \quad \text{(Thm 4, 5, 7, 9)} \\
> &a = 0:\ {-1} \le \sin\tfrac{1}{x} \le 1 \implies {-x^4} \le x^4\sin\tfrac{1}{x} \le x^4 \quad (x \ne 0) \\
> &\phantom{a = 0:\ } \lim_{x \to 0} \left(\pm x^4\right) = 0 \implies \lim_{x \to 0} f(x) = 0 = f(0) \quad \text{(Squeeze Thm)} \\
> &\therefore f \text{ is continuous on } (-\infty, \infty) \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Thm 4 and Thm 9 fail at $0$, because $\tfrac{1}{x}$ is not defined there and $\lim_{x \to 0} \sin\tfrac{1}{x}$ does not exist. The Squeeze Thm needs no limit of $\sin\tfrac{1}{x}$, only its bounds.

### ST 1.8.74
Question: [[CAL1 HW 1.8 Questions#ST 1.8.74|ST 1.8.74]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } D_1 = x^3 + 2x^2 - 1,\ D_2 = x^3 + x - 2,\ p = aD_2 + bD_1. \\
> &p \text{: polynomial} \implies p \text{ continuous on } [-1, 1] \quad \text{(Thm 5)} \\
> &p(-1) = -4a < 0 < 2b = p(1) \\
> &\implies \exists\, c \in (-1, 1) \text{ s.t. } p(c) = 0 \quad \text{(IVT)} \\
> &D_1 = (x + 1)(x^2 + x - 1),\quad D_2 = (x - 1)(x^2 + x + 2) \\
> &\implies \text{in } (-1, 1):\ D_1D_2 = 0 \text{ only at } r = \tfrac{-1 + \sqrt{5}}{2} \\
> &r^2 = 1 - r,\ r^3 = 2r - 1 \implies p(r) = aD_2(r) = 3a(r - 1) < 0 \\
> &\implies c \ne r \implies D_1(c)D_2(c) \ne 0 \\
> &\therefore \frac{a}{D_1(c)} + \frac{b}{D_2(c)} = \frac{p(c)}{D_1(c)D_2(c)} = 0 \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $p(c) = 0$ solves the equation only if no denominator is $0$ at $c$; that is why $r$ is checked. $x^2 + x + 2$ has no real zero (discriminant $-7$), and the other zero of $x^2 + x - 1$ is $\tfrac{-1 - \sqrt{5}}{2} < -1$.

### ST 1.8.76
Question: [[CAL1 HW 1.8 Questions#ST 1.8.76|ST 1.8.76]]

> [!proof] Proof of (a)
> $$
> \begin{aligned}
> &a > 0:\ \lvert x \rvert = x \text{ near } a \implies \lim_{x \to a} \lvert x \rvert = a = \lvert a \rvert \\
> &a < 0:\ \lvert x \rvert = -x \text{ near } a \implies \lim_{x \to a} \lvert x \rvert = -a = \lvert a \rvert \\
> &a = 0:\ \lim_{x \to 0} \lvert x \rvert = 0 = \lvert 0 \rvert && \text{(ST 1.7.27)} \\
> &\therefore F \text{ is continuous on } \mathbb{R} \qquad \blacksquare
> \end{aligned}
> $$

> [!proof] Proof of (b)
> $$
> \begin{aligned}
> &a \in I:\ f \text{ continuous at } a,\ F(u) = \lvert u \rvert \text{ continuous at } f(a) && \text{(by (a))} \\
> &\implies \lim_{x \to a} \lvert f(x) \rvert = F\left(\lim_{x \to a} f(x)\right) = \lvert f(a) \rvert && \text{(Thm 8)} \\
> &\therefore \lvert f \rvert \text{ is continuous on } I \qquad \blacksquare
> \end{aligned}
> $$
>
> \# At an endpoint of $I$, use the one-sided limit.

> [!solution] Solution
> **(c)** No.
> $$
> \begin{aligned}
> &f(x) = \begin{cases} 1 & x \ge 0 \\ -1 & x < 0 \end{cases} \implies \lvert f(x) \rvert = 1\ \ \forall x \implies \lvert f \rvert \text{ continuous on } \mathbb{R} \\
> &\lim_{x \to 0^{-}} f(x) = -1 \ne 1 = \lim_{x \to 0^{+}} f(x) \implies f \text{ is discontinuous at } 0
> \end{aligned}
> $$
