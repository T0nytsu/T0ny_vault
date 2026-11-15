---
course: [CAL1]
semester: "115-1"
chapter: ["1.6"]
tags: [calculus, homework, solutions, limits]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-11-16
questions: "[[CAL1 HW 1.6 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 1.6 Questions#ST 1.6.1\|ST 1.6.1]] | (a) $-6$; (b) $-8$; (c) $2$; (d) $-6$; (e) does not exist; (f) $0$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.5\|ST 1.6.5]] | $88$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.7\|ST 1.6.7]] | $5$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.11\|ST 1.6.11]] | $-13$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.13\|ST 1.6.13]] | $6$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.15\|ST 1.6.15]] | Does not exist ($\infty$ from the right, $-\infty$ from the left) |
| [[CAL1 HW 1.6 Questions#ST 1.6.17\|ST 1.6.17]] | $\tfrac{5}{7}$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.19\|ST 1.6.19]] | $\tfrac{9}{2}$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.21\|ST 1.6.21]] | $-6$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.23\|ST 1.6.23]] | $\tfrac{1}{6}$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.25\|ST 1.6.25]] | $-\tfrac{1}{9}$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.27\|ST 1.6.27]] | $1$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.29\|ST 1.6.29]] | $\tfrac{1}{128}$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.31\|ST 1.6.31]] | $-\tfrac{1}{2}$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.33\|ST 1.6.33]] | $3x^2$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.39\|ST 1.6.39]] | $7$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.41\|ST 1.6.41]] | Proof (Squeeze Theorem) |
| [[CAL1 HW 1.6 Questions#ST 1.6.43\|ST 1.6.43]] | $8$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.45\|ST 1.6.45]] | $-4$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.47\|ST 1.6.47]] | Does not exist ($-\infty$) |
| [[CAL1 HW 1.6 Questions#ST 1.6.49\|ST 1.6.49]] | (b) $1$; $-1$; does not exist; $1$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.51\|ST 1.6.51]] | (a) $5$; $-5$; (b) No |
| [[CAL1 HW 1.6 Questions#ST 1.6.53\|ST 1.6.53]] | $c = 7$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.55\|ST 1.6.55]] | (a) $-2$; does not exist; $-3$; (b) $n - 1$; $n$; (c) $a \notin \mathbb{Z}$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.59\|ST 1.6.59]] | Proof |
| [[CAL1 HW 1.6 Questions#ST 1.6.65\|ST 1.6.65]] | $f = g = \operatorname{sgn}$, $a = 0$ |
| [[CAL1 HW 1.6 Questions#ST 1.6.67\|ST 1.6.67]] | $a = 15$, limit $-1$ |

## ST §1.6 Calculating Limits Using the Limit Laws

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Limit Laws]]**: if $\lim f$ and $\lim g$ exist, then the limit of $f \pm g$, $cf$, $fg$, $f/g$ (if $\lim g \ne 0$), $f^n$, $\sqrt[n]{f}$ is the same operation on the limits; also $\lim_{x \to a} c = c$ and $\lim_{x \to a} x = a$.
> - **Direct substitution**: for a polynomial or rational function $f$ with $a$ in its domain, $\lim_{x \to a} f(x) = f(a)$.
> - If $f(x) = g(x)$ for $x \ne a$, then $\lim_{x \to a} f(x) = \lim_{x \to a} g(x)$. This is why we may cancel a common factor $x - a$.
> - $\lim_{x \to a} f(x) = L$ $\iff$ $\lim_{x \to a^{-}} f(x) = L = \lim_{x \to a^{+}} f(x)$.
> - **[[Squeeze Theorem]]**: if $f(x) \le g(x) \le h(x)$ near $a$ (except possibly at $a$) and $\lim f = \lim h = L$, then $\lim g = L$.

### ST 1.6.1
Question: [[CAL1 HW 1.6 Questions#ST 1.6.1|ST 1.6.1]]

> [!solution] Solution
> All limits are as $x \to 2$.
> - (a) $\lim f + 5\lim g = 4 + 5(-2) = -6$
> - (b) $(\lim g)^3 = (-2)^3 = -8$
> - (c) $\sqrt{\lim f} = \sqrt{4} = 2$
> - (d) $\dfrac{3\lim f}{\lim g} = \dfrac{12}{-2} = -6$
> - (e) Does not exist. If $\lim \dfrac{g}{h} = L$, then $\lim g = \lim\left(\dfrac{g}{h} \cdot h\right) = L \cdot 0 = 0 \ne -2$, a contradiction.
> - (f) $\dfrac{\lim g \cdot \lim h}{\lim f} = \dfrac{(-2) \cdot 0}{4} = 0$
>
> \# In (e) the Quotient Law cannot be used, because $\lim h = 0$.

### ST 1.6.5
Question: [[CAL1 HW 1.6 Questions#ST 1.6.5|ST 1.6.5]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{v \to 2} (v^2 + 2v)(2v^3 - 5) &= \lim_{v \to 2} (v^2 + 2v) \cdot \lim_{v \to 2} (2v^3 - 5) && \text{(Product Law)} \\
> &= \Big(\lim_{v \to 2} v^2 + 2\lim_{v \to 2} v\Big)\Big(2\lim_{v \to 2} v^3 - \lim_{v \to 2} 5\Big) && \text{(Sum, Difference, Constant Multiple)} \\
> &= (2^2 + 2 \cdot 2)(2 \cdot 2^3 - 5) && \text{(Power, } \lim x = a, \lim c = c\text{)} \\
> &= 8 \cdot 11 = 88
> \end{aligned}
> $$

### ST 1.6.7
Question: [[CAL1 HW 1.6 Questions#ST 1.6.7|ST 1.6.7]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{u \to -2} \sqrt{9 - u^3 + 2u^2} &= \sqrt{\lim_{u \to -2} (9 - u^3 + 2u^2)} && \text{(Root Law)} \\
> &= \sqrt{\lim_{u \to -2} 9 - \lim_{u \to -2} u^3 + 2\lim_{u \to -2} u^2} && \text{(Sum, Difference, Constant Multiple)} \\
> &= \sqrt{9 - (-2)^3 + 2(-2)^2} && \text{(}\lim c = c\text{, Power)} \\
> &= \sqrt{25} = 5
> \end{aligned}
> $$

### ST 1.6.11
Question: [[CAL1 HW 1.6 Questions#ST 1.6.11|ST 1.6.11]]

> [!solution] Solution
> $\displaystyle\lim_{x \to -2} (3x - 7) = 3(-2) - 7 = -13$ (direct substitution).

### ST 1.6.13
Question: [[CAL1 HW 1.6 Questions#ST 1.6.13|ST 1.6.13]]

> [!solution] Solution
> $$
> \lim_{t \to 4} \frac{t^2 - 2t - 8}{t - 4} = \lim_{t \to 4} \frac{(t - 4)(t + 2)}{t - 4} = \lim_{t \to 4} (t + 2) = 6
> $$

### ST 1.6.15
Question: [[CAL1 HW 1.6 Questions#ST 1.6.15|ST 1.6.15]]

> [!solution] Solution
> As $x \to 2$: $x^2 + 5x + 4 \to 18 > 0$ and $x - 2 \to 0$.
> $$
> \lim_{x \to 2^{+}} \frac{x^2 + 5x + 4}{x - 2} = \infty \quad (x - 2 > 0), \qquad \lim_{x \to 2^{-}} \frac{x^2 + 5x + 4}{x - 2} = -\infty \quad (x - 2 < 0)
> $$
> Hence the limit does not exist.

### ST 1.6.17
Question: [[CAL1 HW 1.6 Questions#ST 1.6.17|ST 1.6.17]]

> [!solution] Solution
> $$
> \lim_{x \to -2} \frac{x^2 - x - 6}{3x^2 + 5x - 2} = \lim_{x \to -2} \frac{(x - 3)(x + 2)}{(3x - 1)(x + 2)} = \lim_{x \to -2} \frac{x - 3}{3x - 1} = \frac{-5}{-7} = \frac{5}{7}
> $$

### ST 1.6.19
Question: [[CAL1 HW 1.6 Questions#ST 1.6.19|ST 1.6.19]]

> [!solution] Solution
> $$
> \lim_{t \to 3} \frac{t^3 - 27}{t^2 - 9} = \lim_{t \to 3} \frac{(t - 3)(t^2 + 3t + 9)}{(t - 3)(t + 3)} = \lim_{t \to 3} \frac{t^2 + 3t + 9}{t + 3} = \frac{27}{6} = \frac{9}{2}
> $$

### ST 1.6.21
Question: [[CAL1 HW 1.6 Questions#ST 1.6.21|ST 1.6.21]]

> [!solution] Solution
> $$
> \lim_{h \to 0} \frac{(h - 3)^2 - 9}{h} = \lim_{h \to 0} \frac{h^2 - 6h}{h} = \lim_{h \to 0} (h - 6) = -6
> $$

### ST 1.6.23
Question: [[CAL1 HW 1.6 Questions#ST 1.6.23|ST 1.6.23]]

> [!solution] Solution
> $$
> \lim_{h \to 0} \frac{\sqrt{9 + h} - 3}{h} \cdot \frac{\sqrt{9 + h} + 3}{\sqrt{9 + h} + 3} = \lim_{h \to 0} \frac{h}{h(\sqrt{9 + h} + 3)} = \lim_{h \to 0} \frac{1}{\sqrt{9 + h} + 3} = \frac{1}{6}
> $$

### ST 1.6.25
Question: [[CAL1 HW 1.6 Questions#ST 1.6.25|ST 1.6.25]]

> [!solution] Solution
> $$
> \lim_{x \to 3} \frac{\dfrac{1}{x} - \dfrac{1}{3}}{x - 3} = \lim_{x \to 3} \frac{3 - x}{3x(x - 3)} = \lim_{x \to 3} \frac{-1}{3x} = -\frac{1}{9}
> $$

### ST 1.6.27
Question: [[CAL1 HW 1.6 Questions#ST 1.6.27|ST 1.6.27]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{t \to 0} \frac{\sqrt{1 + t} - \sqrt{1 - t}}{t} \cdot \frac{\sqrt{1 + t} + \sqrt{1 - t}}{\sqrt{1 + t} + \sqrt{1 - t}} &= \lim_{t \to 0} \frac{(1 + t) - (1 - t)}{t(\sqrt{1 + t} + \sqrt{1 - t})} \\
> &= \lim_{t \to 0} \frac{2}{\sqrt{1 + t} + \sqrt{1 - t}} = \frac{2}{2} = 1
> \end{aligned}
> $$

### ST 1.6.29
Question: [[CAL1 HW 1.6 Questions#ST 1.6.29|ST 1.6.29]]

> [!solution] Solution
> $16x - x^2 = x(16 - x) = x(4 - \sqrt{x})(4 + \sqrt{x})$, so
> $$
> \lim_{x \to 16} \frac{4 - \sqrt{x}}{x(4 - \sqrt{x})(4 + \sqrt{x})} = \lim_{x \to 16} \frac{1}{x(4 + \sqrt{x})} = \frac{1}{16 \cdot 8} = \frac{1}{128}
> $$

### ST 1.6.31
Question: [[CAL1 HW 1.6 Questions#ST 1.6.31|ST 1.6.31]]

> [!solution] Solution
> $$
> \begin{aligned}
> \frac{1}{t\sqrt{1 + t}} - \frac{1}{t} &= \frac{1 - \sqrt{1 + t}}{t\sqrt{1 + t}} \cdot \frac{1 + \sqrt{1 + t}}{1 + \sqrt{1 + t}} = \frac{-t}{t\sqrt{1 + t}\,(1 + \sqrt{1 + t})} = \frac{-1}{\sqrt{1 + t}\,(1 + \sqrt{1 + t})} \\
> \implies \lim_{t \to 0} \left(\frac{1}{t\sqrt{1 + t}} - \frac{1}{t}\right) &= \frac{-1}{1 \cdot 2} = -\frac{1}{2}
> \end{aligned}
> $$

### ST 1.6.33
Question: [[CAL1 HW 1.6 Questions#ST 1.6.33|ST 1.6.33]]

> [!solution] Solution
> $$
> \lim_{h \to 0} \frac{(x + h)^3 - x^3}{h} = \lim_{h \to 0} \frac{3x^2h + 3xh^2 + h^3}{h} = \lim_{h \to 0} (3x^2 + 3xh + h^2) = 3x^2
> $$

### ST 1.6.39
Question: [[CAL1 HW 1.6 Questions#ST 1.6.39|ST 1.6.39]]

> [!solution] Solution
> $$
> \lim_{x \to 4} (4x - 9) = 7, \qquad \lim_{x \to 4} (x^2 - 4x + 7) = 16 - 16 + 7 = 7
> $$
> The inequality holds for $x \ge 0$, so near $4$. By the Squeeze Theorem, $\lim_{x \to 4} f(x) = 7$.

### ST 1.6.41
Question: [[CAL1 HW 1.6 Questions#ST 1.6.41|ST 1.6.41]]

> [!proof] Proof
> For $x \ne 0$: $-1 \le \cos\dfrac{2}{x} \le 1$ and $x^4 \ge 0$, so
> $$
> -x^4 \le x^4\cos\frac{2}{x} \le x^4.
> $$
> Since $\lim_{x \to 0} (-x^4) = 0 = \lim_{x \to 0} x^4$, the Squeeze Theorem gives $\displaystyle\lim_{x \to 0} x^4\cos\frac{2}{x} = 0$. $\blacksquare$
>
> \# The Product Law cannot be used: $\lim_{x \to 0} \cos\tfrac{2}{x}$ does not exist.

### ST 1.6.43
Question: [[CAL1 HW 1.6 Questions#ST 1.6.43|ST 1.6.43]]

> [!solution] Solution
> $$
> \begin{aligned}
> x > -4:&\quad \lvert x + 4 \rvert - 2x = (x + 4) - 2x = 4 - x \implies \lim_{x \to -4^{+}} = 8 \\
> x < -4:&\quad \lvert x + 4 \rvert - 2x = -(x + 4) - 2x = -3x - 4 \implies \lim_{x \to -4^{-}} = 8
> \end{aligned}
> $$
> Both one-sided limits are $8$, so $\displaystyle\lim_{x \to -4} (\lvert x + 4 \rvert - 2x) = 8$.

### ST 1.6.45
Question: [[CAL1 HW 1.6 Questions#ST 1.6.45|ST 1.6.45]]

> [!solution] Solution
> $2x^3 - x^2 = x^2(2x - 1)$. For $x < 0.5$, $2x - 1 < 0$, so $\lvert 2x^3 - x^2 \rvert = -x^2(2x - 1)$.
> $$
> \lim_{x \to 0.5^{-}} \frac{2x - 1}{-x^2(2x - 1)} = \lim_{x \to 0.5^{-}} \frac{-1}{x^2} = \frac{-1}{0.25} = -4
> $$

### ST 1.6.47
Question: [[CAL1 HW 1.6 Questions#ST 1.6.47|ST 1.6.47]]

> [!solution] Solution
> For $x < 0$, $\lvert x \rvert = -x$:
> $$
> \frac{1}{x} - \frac{1}{\lvert x \rvert} = \frac{1}{x} + \frac{1}{x} = \frac{2}{x} \to -\infty \quad \text{as } x \to 0^{-}
> $$
> The limit does not exist ($-\infty$).

### ST 1.6.49
Question: [[CAL1 HW 1.6 Questions#ST 1.6.49|ST 1.6.49]]

> [!solution] Solution
> **(a)**
>
> ![ST 1.6.49 figure|440](../Attachments/CAL1%20HW%201.6%20Solutions%20fig%2049.png)
>
> **(b)**
> - (i) $\operatorname{sgn} x = 1$ for $x > 0$ $\implies$ $\lim_{x \to 0^{+}} \operatorname{sgn} x = 1$
> - (ii) $\operatorname{sgn} x = -1$ for $x < 0$ $\implies$ $\lim_{x \to 0^{-}} \operatorname{sgn} x = -1$
> - (iii) Does not exist, since $1 \ne -1$ in (i) and (ii).
> - (iv) $\lvert \operatorname{sgn} x \rvert = 1$ for $x \ne 0$ $\implies$ $\lim_{x \to 0} \lvert \operatorname{sgn} x \rvert = 1$

### ST 1.6.51
Question: [[CAL1 HW 1.6 Questions#ST 1.6.51|ST 1.6.51]]

> [!solution] Solution
> $x^2 + x - 6 = (x + 3)(x - 2)$, so
> $$
> g(x) = \begin{cases} x + 3 & x > 2 \\ -(x + 3) & x < 2 \end{cases}
> $$
> **(a)**
> - (i) $\lim_{x \to 2^{+}} (x + 3) = 5$
> - (ii) $\lim_{x \to 2^{-}} -(x + 3) = -5$
>
> **(b)** No, since $5 \ne -5$.
>
> **(c)**
>
> ![ST 1.6.51 figure|380](../Attachments/CAL1%20HW%201.6%20Solutions%20fig%2051.png)

### ST 1.6.53
Question: [[CAL1 HW 1.6 Questions#ST 1.6.53|ST 1.6.53]]

> [!solution] Solution
> $$
> \lim_{t \to 2^{-}} B(t) = 4 - \tfrac{1}{2} \cdot 2 = 3, \qquad \lim_{t \to 2^{+}} B(t) = \sqrt{2 + c}
> $$
> The limit exists $\iff$ $\sqrt{2 + c} = 3$ $\iff$ $c = 7$.

### ST 1.6.55
Question: [[CAL1 HW 1.6 Questions#ST 1.6.55|ST 1.6.55]]

> [!solution] Solution
> **(a)**
> - (i) $-2 \le x < -1$ $\implies$ $[\![ x ]\!] = -2$, so $\lim_{x \to -2^{+}} [\![ x ]\!] = -2$
> - (ii) $-3 \le x < -2$ $\implies$ $[\![ x ]\!] = -3$, so the left-hand limit is $-3 \ne -2$: does not exist.
> - (iii) $-3 \le x < -2$ near $-2.4$ $\implies$ $\lim_{x \to -2.4} [\![ x ]\!] = -3$
>
> **(b)**
> - (i) $n - 1 \le x < n$ $\implies$ $\lim_{x \to n^{-}} [\![ x ]\!] = n - 1$
> - (ii) $n \le x < n + 1$ $\implies$ $\lim_{x \to n^{+}} [\![ x ]\!] = n$
>
> **(c)** For every $a$ that is not an integer: then $[\![ x ]\!] = [\![ a ]\!]$ near $a$. At an integer, the one-sided limits are $n - 1 \ne n$ by (b).

### ST 1.6.59
Question: [[CAL1 HW 1.6 Questions#ST 1.6.59|ST 1.6.59]]

> [!proof] Proof
> Let $p(x) = c_nx^n + c_{n-1}x^{n-1} + \cdots + c_1x + c_0$. Then
> $$
> \begin{aligned}
> \lim_{x \to a} p(x) &= c_n\lim_{x \to a} x^n + \cdots + c_1\lim_{x \to a} x + \lim_{x \to a} c_0 && \text{(Sum, Constant Multiple)} \\
> &= c_na^n + \cdots + c_1a + c_0 && \text{(Power, } \lim x = a, \lim c = c\text{)} \\
> &= p(a). \qquad \blacksquare
> \end{aligned}
> $$

### ST 1.6.65
Question: [[CAL1 HW 1.6 Questions#ST 1.6.65|ST 1.6.65]]

> [!solution] Solution
> Take $f(x) = g(x) = \operatorname{sgn} x$ and $a = 0$. By ST 1.6.49, $\lim_{x \to 0} \operatorname{sgn} x$ does not exist. But
> $$
> f(x)g(x) = (\operatorname{sgn} x)^2 = 1 \quad (x \ne 0) \implies \lim_{x \to 0} [f(x)g(x)] = 1.
> $$

### ST 1.6.67
Question: [[CAL1 HW 1.6 Questions#ST 1.6.67|ST 1.6.67]]

> [!solution] Solution
> The denominator $x^2 + x - 2 = (x + 2)(x - 1) \to 0$ as $x \to -2$. If the limit $L$ exists, the numerator must also $\to 0$:
> $$
> \lim_{x \to -2} (3x^2 + ax + a + 3) = \lim_{x \to -2} \left(\frac{3x^2 + ax + a + 3}{x^2 + x - 2} \cdot (x^2 + x - 2)\right) = L \cdot 0 = 0.
> $$
> So $12 - 2a + a + 3 = 0$, that is, $a = 15$. Then
> $$
> \lim_{x \to -2} \frac{3x^2 + 15x + 18}{(x + 2)(x - 1)} = \lim_{x \to -2} \frac{3(x + 2)(x + 3)}{(x + 2)(x - 1)} = \lim_{x \to -2} \frac{3(x + 3)}{x - 1} = \frac{3}{-3} = -1
> $$
> **Answer.** Yes: $a = 15$, and the limit is $-1$.
