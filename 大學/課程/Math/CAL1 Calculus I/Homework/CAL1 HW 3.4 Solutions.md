---
course: [CAL1]
semester: "115-1"
chapter: ["3.4"]
tags: [calculus, homework, solutions, limits, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §3.4, pp. 237-247, scanned PDF (Theorem 4, Definitions 3, 5, 6, Examples 3-13)"
created: 2026-11-09
questions: "[[CAL1 HW 3.4 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 3.4 Questions#ST 3.4.3\|ST 3.4.3]] | (a) $-2$; (b) $2$; (c) $\infty$; (d) $-\infty$; (e) $x = 1$, $x = 3$, $y = 2$, $y = -2$ |
| [[CAL1 HW 3.4 Questions#ST 3.4.4\|ST 3.4.4]] | (a) $2$; (b) $-1$; (c) $-\infty$; (d) $-\infty$; (e) $\infty$; (f) $x = 0$, $x = 2$, $y = -1$, $y = 2$ |
| [[CAL1 HW 3.4 Questions#ST 3.4.11\|ST 3.4.11]] | $0$ |
| [[CAL1 HW 3.4 Questions#ST 3.4.13\|ST 3.4.13]] | $-\tfrac{1}{3}$ |
| [[CAL1 HW 3.4 Questions#ST 3.4.17\|ST 3.4.17]] | $\tfrac{\sqrt{3}}{4}$ |
| [[CAL1 HW 3.4 Questions#ST 3.4.21\|ST 3.4.21]] | $-\infty$ (does not exist) |
| [[CAL1 HW 3.4 Questions#ST 3.4.25\|ST 3.4.25]] | $0$ |
| [[CAL1 HW 3.4 Questions#ST 3.4.27\|ST 3.4.27]] | $\tfrac{a - b}{2}$ |
| [[CAL1 HW 3.4 Questions#ST 3.4.29\|ST 3.4.29]] | $-\infty$ (does not exist) |
| [[CAL1 HW 3.4 Questions#ST 3.4.31\|ST 3.4.31]] | $1$ |
| [[CAL1 HW 3.4 Questions#ST 3.4.37\|ST 3.4.37]] | H.A. $y = 2$; V.A. $x = 1$, $x = -2$ |
| [[CAL1 HW 3.4 Questions#ST 3.4.49\|ST 3.4.49]] | H.A. $y = -1$ (V.A. $x = -1$); decreasing on $(-\infty, -1)$ and $(-1, \infty)$; CD on $(-\infty, -1)$, CU on $(-1, \infty)$; sketch |
| [[CAL1 HW 3.4 Questions#ST 3.4.51\|ST 3.4.51]] | H.A. $y = 0$; increasing on $(-1, 1)$, decreasing on $(-\infty, -1)$ and $(1, \infty)$; CU on $(-\sqrt{3}, 0)$ and $(\sqrt{3}, \infty)$, CD on $(-\infty, -\sqrt{3})$ and $(0, \sqrt{3})$; sketch |
| [[CAL1 HW 3.4 Questions#ST 3.4.57\|ST 3.4.57]] | Sketch |
| [[CAL1 HW 3.4 Questions#ST 3.4.58\|ST 3.4.58]] | Sketch |
| [[CAL1 HW 3.4 Questions#ST 3.4.65\|ST 3.4.65]] | $4$ |
| [[CAL1 HW 3.4 Questions#ST 3.4.71\|ST 3.4.71]] | (a) $x > 100$; (b) proof with $N = \tfrac{1}{\sqrt{\varepsilon}}$ |
| [[CAL1 HW 3.4 Questions#ST 3.4.73\|ST 3.4.73]] | Proof with $N = -\tfrac{1}{\varepsilon}$ |

## ST §3.4 Limits at Infinity; Horizontal Asymptotes

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Horizontal Asymptote]]** (H.A.): the line $y = L$ is a horizontal asymptote of $y = f(x)$ if $\lim_{x \to \infty} f(x) = L$ or $\lim_{x \to -\infty} f(x) = L$. **[[Vertical Asymptote]]** (V.A.): the line $x = a$ is one if at least one one-sided limit of $f$ at $a$ is $\infty$ or $-\infty$.
> - **Powers of $\tfrac{1}{x}$**: $\lim_{x \to \infty} \frac{1}{x^{r}} = 0$ for every rational $r > 0$, and $\lim_{x \to -\infty} \frac{1}{x^{r}} = 0$ when $x^{r}$ is defined for all $x$ (Theorem 4). The [[Limit Laws]] also hold for $x \to \pm\infty$.
> - **Rational functions**: divide the numerator and the denominator by the highest power of $x$ in the **denominator**.
> - **Roots**: $\sqrt{x^{2}} = \lvert x \rvert$, so $\sqrt{x^{2}} = x$ for $x > 0$ and $\sqrt{x^{2}} = -x$ for $x < 0$. For the form $\infty - \infty$ with a root, multiply by the conjugate.
> - **Infinite limits at infinity**: if $g(x) \to \pm\infty$ and $h(x) \to c > 0$, then $g(x)h(x) \to \pm\infty$ (the same sign). For a polynomial, factor out the highest power of $x$.
> - **[[Squeeze Theorem]]** for $x \to \infty$: if $g(x) \le f(x) \le h(x)$ for all large $x$ and $g$, $h$ both tend to $L$, then $f$ tends to $L$.
> - **[[Limit at Infinity|Precise definitions]]**. Definition 5: $\lim_{x \to \infty} f(x) = L$ means that for every $\varepsilon > 0$ there is a corresponding number $N$ such that if $x > N$ then $\lvert f(x) - L \rvert < \varepsilon$. Definition 6: $\lim_{x \to -\infty} f(x) = L$ means the same with "if $x < N$".
> - **Curve sketching**: $f' > 0$ on an interval $\implies$ increasing there, $f' < 0 \implies$ decreasing; $f'' > 0 \implies$ concave upward (CU), $f'' < 0 \implies$ concave downward (CD); an inflection point is a point **of the graph** where the concavity changes.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 3.4.3
Question: [[CAL1 HW 3.4 Questions#ST 3.4.3|ST 3.4.3]]

> [!solution] Solution
> - (a) $\lim_{x \to \infty} f(x) = -2$
> - (b) $\lim_{x \to -\infty} f(x) = 2$
> - (c) $\lim_{x \to 1} f(x) = \infty$
> - (d) $\lim_{x \to 3} f(x) = -\infty$
> - (e) Vertical asymptotes $x = 1$, $x = 3$; horizontal asymptotes $y = 2$, $y = -2$.
>
> ![ST 3.4.3 figure|480](../Attachments/CAL1%20HW%203.4%20Solutions%20fig%203.png)
>
> \# Read (a) and (b) at the far right and the far left of the graph: the curve levels off at height $-2$ on the right and at height $2$ on the left. In (c) both one-sided limits at $1$ are $\infty$, and in (d) both one-sided limits at $3$ are $-\infty$, so the two-sided limits are $\infty$ and $-\infty$. Each infinite limit gives a vertical asymptote and each limit at $\pm\infty$ a horizontal one (the dashed lines).

### ST 3.4.4
Question: [[CAL1 HW 3.4 Questions#ST 3.4.4|ST 3.4.4]]

> [!solution] Solution
> - (a) $\lim_{x \to \infty} g(x) = 2$
> - (b) $\lim_{x \to -\infty} g(x) = -1$
> - (c) $\lim_{x \to 0} g(x) = -\infty$
> - (d) $\lim_{x \to 2^{-}} g(x) = -\infty$
> - (e) $\lim_{x \to 2^{+}} g(x) = \infty$
> - (f) Vertical asymptotes $x = 0$, $x = 2$; horizontal asymptotes $y = -1$, $y = 2$.
>
> ![ST 3.4.4 figure|480](../Attachments/CAL1%20HW%203.4%20Solutions%20fig%204.png)
>
> \# The graph crosses both horizontal asymptotes several times while it oscillates around them. That is allowed: a horizontal asymptote describes only the behavior far to the right or far to the left, unlike a vertical asymptote, which the graph never crosses. At $2$ the one-sided limits differ, so $\lim_{x \to 2} g(x)$ does not exist, but $x = 2$ is still a vertical asymptote.

### ST 3.4.11
Question: [[CAL1 HW 3.4 Questions#ST 3.4.11|ST 3.4.11]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{t \to -\infty} \frac{3t^{2} + t}{t^{3} - 4t + 1}
> &= \lim_{t \to -\infty} \frac{\dfrac{3}{t} + \dfrac{1}{t^{2}}}{1 - \dfrac{4}{t^{2}} + \dfrac{1}{t^{3}}} && (\div\, t^{3}) \\
> &= \frac{0 + 0}{1 - 0 + 0} = 0 && \left(\lim_{t \to -\infty} \tfrac{1}{t^{n}} = 0\right)
> \end{aligned}
> $$
>
> \# $t^{3}$ is the highest power in the denominator. The degree of the numerator (2) is less than that of the denominator (3), so the limit is $0$, at $\infty$ and at $-\infty$ alike.

### ST 3.4.13
Question: [[CAL1 HW 3.4 Questions#ST 3.4.13|ST 3.4.13]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{r \to \infty} \frac{r - r^{3}}{2 - r^{2} + 3r^{3}}
> &= \lim_{r \to \infty} \frac{\dfrac{1}{r^{2}} - 1}{\dfrac{2}{r^{3}} - \dfrac{1}{r} + 3} && (\div\, r^{3}) \\
> &= \frac{0 - 1}{0 - 0 + 3} = -\frac{1}{3}
> \end{aligned}
> $$
>
> \# Equal degrees (3 and 3): the limit is the ratio of the leading coefficients, $\tfrac{-1}{3}$. Mind the order: the leading term of the denominator is $3r^{3}$, written last.

### ST 3.4.17
Question: [[CAL1 HW 3.4 Questions#ST 3.4.17|ST 3.4.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{x \to \infty} \frac{\sqrt{x + 3x^{2}}}{4x - 1}
> &= \lim_{x \to \infty} \frac{\sqrt{x + 3x^{2}} \big/ \sqrt{x^{2}}}{(4x - 1)/x} && (x > 0 \implies x = \sqrt{x^{2}}) \\
> &= \lim_{x \to \infty} \frac{\sqrt{\dfrac{1}{x} + 3}}{4 - \dfrac{1}{x}} = \frac{\sqrt{0 + 3}}{4 - 0} = \frac{\sqrt{3}}{4}
> \end{aligned}
> $$
>
> \# The highest power in the denominator is $x$. To bring $x$ inside the root, write it as $\sqrt{x^{2}}$; this needs $x > 0$, which holds because $x \to \infty$. For $x \to -\infty$ we would have $x = -\sqrt{x^{2}}$ and the answer $-\tfrac{\sqrt{3}}{4}$.

### ST 3.4.21
Question: [[CAL1 HW 3.4 Questions#ST 3.4.21|ST 3.4.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{x \to -\infty} \frac{2x^{5} - x}{x^{4} + 3}
> &= \lim_{x \to -\infty} \frac{2x - \dfrac{1}{x^{3}}}{1 + \dfrac{3}{x^{4}}} && (\div\, x^{4}) \\
> &= -\infty && \left(2x - \tfrac{1}{x^{3}} \to -\infty,\ 1 + \tfrac{3}{x^{4}} \to 1\right)
> \end{aligned}
> $$
> Hence the limit does not exist; it is $-\infty$.
>
> \# The degree of the numerator (5) is greater than that of the denominator (4), so the quotient grows without bound. The sign: for large negative $x$, the numerator behaves like $2x^{5} < 0$ and the denominator is positive.

### ST 3.4.25
Question: [[CAL1 HW 3.4 Questions#ST 3.4.25|ST 3.4.25]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{t \to \infty} \left(\sqrt{25t^{2} + 2} - 5t\right)
> &= \lim_{t \to \infty} \frac{\left(\sqrt{25t^{2} + 2} - 5t\right)\left(\sqrt{25t^{2} + 2} + 5t\right)}{\sqrt{25t^{2} + 2} + 5t} && \text{(conjugate)} \\
> &= \lim_{t \to \infty} \frac{(25t^{2} + 2) - 25t^{2}}{\sqrt{25t^{2} + 2} + 5t} = \lim_{t \to \infty} \frac{2}{\sqrt{25t^{2} + 2} + 5t} \\
> &= 0 && (\text{denominator} \to \infty)
> \end{aligned}
> $$
>
> \# Both terms tend to $\infty$, so this is the form $\infty - \infty$, and the Limit Laws cannot be applied term by term. The conjugate turns the difference into a quotient. Dividing by $t$ instead gives the same: $\frac{2/t}{\sqrt{25 + 2/t^{2}} + 5} \to \frac{0}{10} = 0$.

### ST 3.4.27
Question: [[CAL1 HW 3.4 Questions#ST 3.4.27|ST 3.4.27]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\lim_{x \to \infty} \left(\sqrt{x^{2} + ax} - \sqrt{x^{2} + bx}\right) \\
> &= \lim_{x \to \infty} \frac{(x^{2} + ax) - (x^{2} + bx)}{\sqrt{x^{2} + ax} + \sqrt{x^{2} + bx}} && \text{(conjugate)} \\
> &= \lim_{x \to \infty} \frac{(a - b)x}{\sqrt{x^{2} + ax} + \sqrt{x^{2} + bx}} \\
> &= \lim_{x \to \infty} \frac{a - b}{\sqrt{1 + \dfrac{a}{x}} + \sqrt{1 + \dfrac{b}{x}}} && (\div\, x = \sqrt{x^{2}},\ x > 0) \\
> &= \frac{a - b}{\sqrt{1} + \sqrt{1}} = \frac{a - b}{2}
> \end{aligned}
> $$
>
> \# Same method as Exercise 25: the conjugate, then divide by $x = \sqrt{x^{2}}$. For large $x$ both radicands are positive, so the expression is defined. If $a = b$ the limit is $0$, as it should be.

### ST 3.4.29
Question: [[CAL1 HW 3.4 Questions#ST 3.4.29|ST 3.4.29]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{x \to -\infty} (x^{2} + 2x^{7}) &= \lim_{x \to -\infty} x^{7}\left(\frac{1}{x^{5}} + 2\right) \\
> &= -\infty && \left(x^{7} \to -\infty,\ \tfrac{1}{x^{5}} + 2 \to 2 > 0\right)
> \end{aligned}
> $$
> Hence the limit does not exist; it is $-\infty$.
>
> \# Here $x^{2} \to \infty$ and $2x^{7} \to -\infty$, the form $\infty - \infty$ again. Factoring out the highest power shows that $2x^{7}$ wins: an odd power of a large negative number is large negative.

### ST 3.4.31
Question: [[CAL1 HW 3.4 Questions#ST 3.4.31|ST 3.4.31]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Let } t = \tfrac{1}{x}. \quad x \to \infty \implies t \to 0^{+} \\
> &\lim_{x \to \infty} x \sin \frac{1}{x} = \lim_{t \to 0^{+}} \frac{1}{t} \sin t = \lim_{t \to 0^{+}} \frac{\sin t}{t} = 1 && \left(\lim_{t \to 0} \tfrac{\sin t}{t} = 1\right)
> \end{aligned}
> $$
>
> \# As $x \to \infty$, the factor $x$ tends to $\infty$ while $\sin \frac{1}{x} \to 0$: the form $\infty \cdot 0$, which has no fixed value. The substitution $t = \frac{1}{x}$ moves the limit from infinity to $0^{+}$, where it is one of the [[Special Trigonometric Limits]].

### ST 3.4.37
Question: [[CAL1 HW 3.4 Questions#ST 3.4.37|ST 3.4.37]]

> [!solution] Solution
> $$
> \begin{aligned}
> &y = \frac{2x^{2} + x - 1}{x^{2} + x - 2} = \frac{(2x - 1)(x + 1)}{(x + 2)(x - 1)} \\[6pt]
> &\lim_{x \to \pm\infty} \frac{2x^{2} + x - 1}{x^{2} + x - 2} = \lim_{x \to \pm\infty} \frac{2 + \dfrac{1}{x} - \dfrac{1}{x^{2}}}{1 + \dfrac{1}{x} - \dfrac{2}{x^{2}}} = \frac{2}{1} = 2 && (\div\, x^{2}) \\[6pt]
> &\text{denominator} = 0 \iff x = -2 \text{ or } x = 1; \quad \text{numerator: } 5 \text{ at } x = -2,\ 2 \text{ at } x = 1 \\
> &\lim_{x \to 1^{+}} y = \infty,\quad \lim_{x \to 1^{-}} y = -\infty && (\text{numerator} \to 2,\ \text{denominator} \to 0^{\pm}) \\
> &\lim_{x \to -2^{+}} y = -\infty,\quad \lim_{x \to -2^{-}} y = \infty && (\text{numerator} \to 5,\ \text{denominator} \to 0^{\mp})
> \end{aligned}
> $$
> Hence the horizontal asymptote is $y = 2$, and the vertical asymptotes are $x = 1$ and $x = -2$.
>
> \# The numerator is checked at the zeros of the denominator because a common zero could cancel and give a hole instead of an asymptote. Signs of the denominator $(x + 2)(x - 1)$: near $1$ the factor $x + 2 \approx 3 > 0$, so it has the sign of $x - 1$; near $-2$ the factor $x - 1 \approx -3 < 0$, so it has the opposite sign of $x + 2$. One infinite one-sided limit already makes a vertical asymptote.

### ST 3.4.49
Question: [[CAL1 HW 3.4 Questions#ST 3.4.49|ST 3.4.49]]

> [!solution] Solution
> $$
> \begin{aligned}
> &y = \frac{1 - x}{1 + x}, \quad x \ne -1 \\[6pt]
> &\lim_{x \to \pm\infty} \frac{1 - x}{1 + x} = \lim_{x \to \pm\infty} \frac{\dfrac{1}{x} - 1}{\dfrac{1}{x} + 1} = \frac{0 - 1}{0 + 1} = -1 && (\div\, x) \\
> &\implies \text{H.A. } y = -1 \\[6pt]
> &\lim_{x \to -1^{+}} y = \infty,\quad \lim_{x \to -1^{-}} y = -\infty \implies \text{V.A. } x = -1 && (1 - x \to 2,\ 1 + x \to 0^{\pm}) \\[6pt]
> &y' = \frac{(-1)(1 + x) - (1 - x)(1)}{(1 + x)^{2}} = \frac{-2}{(1 + x)^{2}} < 0 \text{ for all } x \ne -1 \\
> &\implies \text{decreasing on } (-\infty, -1) \text{ and on } (-1, \infty) \\[6pt]
> &y'' = \frac{4}{(1 + x)^{3}}: \quad y'' > 0 \text{ for } x > -1,\quad y'' < 0 \text{ for } x < -1 \\
> &\implies \text{CU on } (-1, \infty),\ \text{CD on } (-\infty, -1);\ \text{no inflection point} && (-1 \notin \text{domain}) \\[6pt]
> &\text{intercepts: } (0, 1),\ (1, 0)
> \end{aligned}
> $$
>
> ![ST 3.4.49 figure|400](../Attachments/CAL1%20HW%203.4%20Solutions%20fig%2049.png)
>
> \# $y''$ comes from $y' = -2(1 + x)^{-2}$ by the [[Chain Rule]]: $y'' = (-2)(-2)(1 + x)^{-3} = \frac{4}{(1 + x)^{3}}$. "Decreasing on $(-\infty, -1)$ and on $(-1, \infty)$" is not the same as decreasing on the whole domain: $y(-2) = -3 < 1 = y(0)$. The concavity changes at $x = -1$, but there is no point of the graph there. Long division gives $y = -1 + \frac{2}{1 + x}$: the hyperbola $y = \frac{2}{x}$ moved 1 left and 1 down, which explains both asymptotes at once.

### ST 3.4.51
Question: [[CAL1 HW 3.4 Questions#ST 3.4.51|ST 3.4.51]]

> [!solution] Solution
> $$
> \begin{aligned}
> &y = \frac{x}{x^{2} + 1}, \quad \text{domain } \mathbb{R} \ (x^{2} + 1 > 0),\quad y(-x) = -y(x) \\[6pt]
> &\lim_{x \to \pm\infty} \frac{x}{x^{2} + 1} = \lim_{x \to \pm\infty} \frac{\dfrac{1}{x}}{1 + \dfrac{1}{x^{2}}} = \frac{0}{1 + 0} = 0 \implies \text{H.A. } y = 0 && (\div\, x^{2}) \\[6pt]
> &y' = \frac{(x^{2} + 1) - x \cdot 2x}{(x^{2} + 1)^{2}} = \frac{(1 - x)(1 + x)}{(x^{2} + 1)^{2}} = 0 \iff x = \pm 1 \\[6pt]
> &y'' = \frac{-2x(x^{2} + 1)^{2} - (1 - x^{2}) \cdot 2(x^{2} + 1) \cdot 2x}{(x^{2} + 1)^{4}} = \frac{2x(x^{2} - 3)}{(x^{2} + 1)^{3}} = 0 \iff x = 0,\ \pm\sqrt{3}
> \end{aligned}
> $$
>
> | $x$ | $(-\infty, -\sqrt{3})$ | $(-\sqrt{3}, -1)$ | $(-1, 0)$ | $(0, 1)$ | $(1, \sqrt{3})$ | $(\sqrt{3}, \infty)$ |
> | --- | --- | --- | --- | --- | --- | --- |
> | $y'$ | $-$ | $-$ | $+$ | $+$ | $-$ | $-$ |
> | $y''$ | $-$ | $+$ | $+$ | $-$ | $-$ | $+$ |
> | $y$ | dec., CD | dec., CU | inc., CU | inc., CD | dec., CD | dec., CU |
>
> Hence: H.A. $y = 0$; increasing on $(-1, 1)$, decreasing on $(-\infty, -1)$ and $(1, \infty)$, local minimum $y(-1) = -\tfrac{1}{2}$, local maximum $y(1) = \tfrac{1}{2}$; CU on $(-\sqrt{3}, 0)$ and $(\sqrt{3}, \infty)$, CD on $(-\infty, -\sqrt{3})$ and $(0, \sqrt{3})$; inflection points $\left(-\sqrt{3}, -\tfrac{\sqrt{3}}{4}\right)$, $(0, 0)$, $\left(\sqrt{3}, \tfrac{\sqrt{3}}{4}\right)$.
>
> ![ST 3.4.51 figure|480](../Attachments/CAL1%20HW%203.4%20Solutions%20fig%2051.png)
>
> \# Simplifying $y''$: factor $2(x^{2} + 1)$ out of the numerator, $-2x(x^{2} + 1) - 4x(1 - x^{2}) = 2x^{3} - 6x = 2x(x^{2} - 3)$, and cancel one $x^{2} + 1$. The function is odd, so the graph is symmetric about the origin and the left half follows from the right half. The graph crosses its asymptote $y = 0$ at the origin. In the figure the vertical scale is stretched four times.

### ST 3.4.57
Question: [[CAL1 HW 3.4 Questions#ST 3.4.57|ST 3.4.57]]

> [!solution] Solution
> - $f(2) = 4$, $f(-2) = -4$: the graph passes through $(2, 4)$ and $(-2, -4)$.
> - $\lim_{x \to -\infty} f(x) = 0$: far to the left the graph approaches the $x$-axis (H.A. $y = 0$).
> - $\lim_{x \to \infty} f(x) = 2$: far to the right the graph approaches the line $y = 2$ (H.A. $y = 2$).
>
> One possible graph:
>
> ![ST 3.4.57 figure|480](../Attachments/CAL1%20HW%203.4%20Solutions%20fig%2057.png)
>
> \# Many graphs work. This one has a local minimum at $(-2, -4)$ and a local maximum at $(2, 4)$, which the conditions do not require; it approaches $y = 0$ from below and $y = 2$ from above, which is also a free choice.

### ST 3.4.58
Question: [[CAL1 HW 3.4 Questions#ST 3.4.58|ST 3.4.58]]

> [!solution] Solution
> - $\lim_{x \to -\infty} f(x) = -\infty$, $\lim_{x \to \infty} f(x) = \infty$: the graph falls without bound far to the left and rises without bound far to the right; there is no horizontal asymptote.
> - $\lim_{x \to -2^{-}} f(x) = \infty$, $\lim_{x \to -2^{+}} f(x) = -\infty$: V.A. $x = -2$, the graph goes up on the left of it and down on the right.
> - $\lim_{x \to 2} f(x) = \infty$: V.A. $x = 2$, the graph goes up on both sides.
>
> One possible graph:
>
> ![ST 3.4.58 figure|440](../Attachments/CAL1%20HW%203.4%20Solutions%20fig%2058.png)
>
> \# Draw the asymptotes first, then the three pieces: left of $-2$ from $-\infty$ up to $\infty$, between $-2$ and $2$ from $-\infty$ up to $\infty$, right of $2$ from $\infty$ down and back up to $\infty$. A formula with these limits is $f(x) = \dfrac{x^{4} + 10x}{(x + 2)(x - 2)^{2}}$ (checked with sympy); a sketch needs no formula.

### ST 3.4.65
Question: [[CAL1 HW 3.4 Questions#ST 3.4.65|ST 3.4.65]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\lim_{x \to \infty} \frac{4x - 1}{x} = \lim_{x \to \infty} \left(4 - \frac{1}{x}\right) = 4 \\
> &\lim_{x \to \infty} \frac{4x^{2} + 3x}{x^{2}} = \lim_{x \to \infty} \left(4 + \frac{3}{x}\right) = 4 \\
> &\frac{4x - 1}{x} < f(x) < \frac{4x^{2} + 3x}{x^{2}} \text{ for all } x > 5 \\
> &\implies \lim_{x \to \infty} f(x) = 4 && \text{(Squeeze Theorem)}
> \end{aligned}
> $$
>
> \# The Squeeze Theorem also holds for $x \to \infty$, and the inequality only has to hold for all large $x$; here it holds for $x > 5$. Both bounds must have the **same** limit; that is the condition to check.

### ST 3.4.71
Question: [[CAL1 HW 3.4 Questions#ST 3.4.71|ST 3.4.71]]

> [!solution] Solution
> **(a)**
> $$
> x > 0: \quad \frac{1}{x^{2}} < 0.0001 \iff x^{2} > \frac{1}{0.0001} = 10\,000 \iff x > 100
> $$
> Hence we have to take $x > 100$.

> [!proof] Proof
> **(b)**
> $$
> \begin{aligned}
> &\text{pf: Given any } \varepsilon > 0, \text{ we take } N = \frac{1}{\sqrt{\varepsilon}}. \\
> &\text{If } x > N, \text{ then } x > \frac{1}{\sqrt{\varepsilon}} > 0 \\
> &\implies x^{2} > \frac{1}{\varepsilon} && (u > v > 0 \implies u^{2} > v^{2}) \\
> &\implies \left\lvert \frac{1}{x^{2}} - 0 \right\rvert = \frac{1}{x^{2}} < \varepsilon && (p > q > 0 \implies \tfrac{1}{p} < \tfrac{1}{q}) \\
> &\text{Hence } \lim_{x \to \infty} \frac{1}{x^{2}} = 0 \text{ by Definition 5.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Finding $N$ (scratch paper): for $x > 0$, $\frac{1}{x^{2}} < \varepsilon \iff x^{2} > \frac{1}{\varepsilon} \iff x > \frac{1}{\sqrt{\varepsilon}}$. With $\varepsilon = 0.0001$ this gives $N = 100$, the answer of (a). The condition $x > 0$ is what lets us square and take reciprocals without reversing an inequality; it comes for free because $N > 0$, so write it down in the proof.

### ST 3.4.73
Question: [[CAL1 HW 3.4 Questions#ST 3.4.73|ST 3.4.73]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{pf: Given any } \varepsilon > 0, \text{ we take } N = -\frac{1}{\varepsilon}. \\
> &\text{If } x < N, \text{ then } x < -\frac{1}{\varepsilon} < 0 \\
> &\implies -x > \frac{1}{\varepsilon} > 0 \\
> &\implies \left\lvert \frac{1}{x} - 0 \right\rvert = \frac{1}{-x} < \varepsilon && (x < 0 \implies \lvert x \rvert = -x;\ p > q > 0 \implies \tfrac{1}{p} < \tfrac{1}{q}) \\
> &\text{Hence } \lim_{x \to -\infty} \frac{1}{x} = 0 \text{ by Definition 6.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Finding $N$ (scratch paper): for $x < 0$, $\left\lvert \frac{1}{x} \right\rvert = \frac{1}{-x} < \varepsilon \iff -x > \frac{1}{\varepsilon} \iff x < -\frac{1}{\varepsilon}$. In Definition 6 the condition is $x < N$, so $N$ is negative here. This is the mirror image of Example 13, where $\lim_{x \to \infty} \frac{1}{x} = 0$ is proved with $N = \frac{1}{\varepsilon}$.
