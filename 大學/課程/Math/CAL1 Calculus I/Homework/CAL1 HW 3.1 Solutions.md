---
course: [CAL1]
semester: "115-1"
chapter: ["3.1"]
tags: [calculus, homework, solutions, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §3.1, pp. 210-216, scanned PDF (extreme values, Fermat's Theorem, critical numbers, the Closed Interval Method)"
  - "Sketches for Exercises 19-27 drawn with matplotlib"
created: 2026-11-09
questions: "[[CAL1 HW 3.1 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 3.1 Questions#ST 3.1.19\|ST 3.1.19]] | abs min $f(0) = 0$; no abs max; no local max or min |
| [[CAL1 HW 3.1 Questions#ST 3.1.21\|ST 3.1.21]] | abs max $f(\pi/2) = 1$, abs min $f(-\pi/2) = -1$; no local max or min |
| [[CAL1 HW 3.1 Questions#ST 3.1.23\|ST 3.1.23]] | abs and local min $f(-1) = 1$; no abs or local max |
| [[CAL1 HW 3.1 Questions#ST 3.1.25\|ST 3.1.25]] | abs max $f(0) = 1$; no abs min; no local max or min |
| [[CAL1 HW 3.1 Questions#ST 3.1.27\|ST 3.1.27]] | abs min $f(1) = -1$; no abs max; local min $f(0) = 0$; no local max |
| [[CAL1 HW 3.1 Questions#ST 3.1.33\|ST 3.1.33]] | No critical number |
| [[CAL1 HW 3.1 Questions#ST 3.1.35\|ST 3.1.35]] | $0$, $2$ |
| [[CAL1 HW 3.1 Questions#ST 3.1.39\|ST 3.1.39]] | $0$, $\tfrac{4}{9}$ |
| [[CAL1 HW 3.1 Questions#ST 3.1.41\|ST 3.1.41]] | $0$, $\tfrac{8}{7}$, $4$ |
| [[CAL1 HW 3.1 Questions#ST 3.1.45\|ST 3.1.45]] | $n\pi$, $n$ an integer |
| [[CAL1 HW 3.1 Questions#ST 3.1.53\|ST 3.1.53]] | abs max $f(-2) = 33$, abs min $f(2) = -31$ |
| [[CAL1 HW 3.1 Questions#ST 3.1.55\|ST 3.1.55]] | abs max $f(0.2) = 5.2$, abs min $f(1) = 2$ |
| [[CAL1 HW 3.1 Questions#ST 3.1.57\|ST 3.1.57]] | abs max $f(4) = 4 - \sqrt[3]{4}$, abs min $f(\tfrac{\sqrt{3}}{9}) = -\tfrac{2\sqrt{3}}{9}$ |
| [[CAL1 HW 3.1 Questions#ST 3.1.59\|ST 3.1.59]] | abs max $f(\tfrac{\pi}{6}) = \tfrac{3\sqrt{3}}{2}$, abs min $f(\tfrac{\pi}{2}) = 0$ |
| [[CAL1 HW 3.1 Questions#ST 3.1.72\|ST 3.1.72]] | Proof |

## ST §3.1 Maximum and Minimum Values

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Absolute Extreme Value|Absolute maximum and minimum]]**: $f(c)$ is the absolute maximum value of $f$ on its domain $D$ if $f(c) \ge f(x)$ for all $x$ in $D$; the absolute minimum value if $f(c) \le f(x)$ for all $x$ in $D$.
> - **[[Local Extreme Value|Local maximum and minimum]]**: $f(c)$ is a local maximum value if $f(c) \ge f(x)$ when $x$ is near $c$, that is, for all $x$ in some open interval containing $c$; a local minimum value with $\le$. So an endpoint of the domain is never a local extremum.
> - **Reading a sketch**: an open dot is not a value of $f$. A value that $f$ approaches but never takes is neither a maximum nor a minimum (Exercises 19, 23, 27). On an interval where $f$ is increasing (or decreasing), no point inside is a local extremum: every open interval around it holds both larger and smaller values.
> - **[[Critical Number]]**: a number $c$ **in the domain** of $f$ such that $f'(c) = 0$ or $f'(c)$ does not exist. Find the domain first. Where the formula for $f'$ breaks down, decide with the difference quotient (Exercises 39, 41, 57).
> - **[[Fermat's Theorem]]**: if $f$ has a local maximum or minimum at $c$, and if $f'(c)$ exists, then $f'(c) = 0$. Equivalently: if $f$ has a local maximum or minimum at $c$, then $c$ is a critical number of $f$ (Exercises 33, 72).
> - **[[Closed Interval Method]]**: for $f$ continuous on $[a, b]$: 1. the values of $f$ at the critical numbers in $(a, b)$; 2. the values at $a$ and $b$; 3. the largest of them is the absolute maximum value, the smallest the absolute minimum value (Exercises 53–59).
> - Each answer is written as on an exam paper: the domain or the continuity first, then the computation, then a Hence line. Grading deducts points for missing conditions, so say why each endpoint is or is not an extremum, and check that each critical number lies in the domain (or in $(a, b)$). A paragraph that starts with \# is a remark and is not part of the answer.

### ST 3.1.19
Question: [[CAL1 HW 3.1 Questions#ST 3.1.19|ST 3.1.19]]

> [!solution] Solution
> $$
> \begin{aligned}
> &y = \sin x \text{ on } [0, \tfrac{\pi}{2})\text{: the arc of the sine curve from } (0, 0) \text{ up to the open dot } (\tfrac{\pi}{2}, 1) \\
> &f \text{ is increasing on } [0, \tfrac{\pi}{2}) \\[6pt]
> &f(0) = 0 \le f(x) \text{ for all } x \in [0, \tfrac{\pi}{2}) \implies \text{abs min } f(0) = 0 \\
> &f(x) < 1 \text{ for all } x \in [0, \tfrac{\pi}{2}), \text{ but } f(x) \to 1 \text{ as } x \to \tfrac{\pi}{2}^{-} \implies \text{no abs max} \\
> &0 \text{ is an endpoint} \implies f(0) \text{ is not a local min} \\
> &f \text{ is increasing on } (0, \tfrac{\pi}{2}) \implies \text{no local max or min}
> \end{aligned}
> $$
> Hence the absolute minimum value is $f(0) = 0$; there is no absolute maximum and no local maximum or minimum.
>
> ![ST 3.1.19 figure|440](../Attachments/CAL1%20HW%203.1%20Solutions%20fig%2019.png)
>
> \# The value $1$ would need $x = \tfrac{\pi}{2}$, which the domain leaves out (the open dot). For any $x$ in the domain there is an $x'$ between $x$ and $\tfrac{\pi}{2}$ with $\sin x' > \sin x$, so no value is the largest. The point $0$ is the lowest point, so $f(0)$ is the absolute minimum, but no open interval around $0$ lies in the domain, so it is not a local minimum. Compare Exercise 20 ($0 < x \le \tfrac{\pi}{2}$): there the roles swap, with the absolute maximum $f(\tfrac{\pi}{2}) = 1$ and no absolute minimum.

### ST 3.1.21
Question: [[CAL1 HW 3.1 Questions#ST 3.1.21|ST 3.1.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &y = \sin x \text{ on } [-\tfrac{\pi}{2}, \tfrac{\pi}{2}]\text{: the arc from } (-\tfrac{\pi}{2}, -1) \text{ up to } (\tfrac{\pi}{2}, 1) \\
> &f \text{ is increasing on } [-\tfrac{\pi}{2}, \tfrac{\pi}{2}] \\[6pt]
> &f(-\tfrac{\pi}{2}) = -1 \le f(x) \le 1 = f(\tfrac{\pi}{2}) \text{ for all } x \in [-\tfrac{\pi}{2}, \tfrac{\pi}{2}] \\
> &\implies \text{abs max } f(\tfrac{\pi}{2}) = 1, \quad \text{abs min } f(-\tfrac{\pi}{2}) = -1 \\
> &\pm\tfrac{\pi}{2} \text{ are endpoints} \implies \text{not local} \\
> &f \text{ is increasing on } (-\tfrac{\pi}{2}, \tfrac{\pi}{2}) \implies \text{no local max or min}
> \end{aligned}
> $$
> Hence the absolute maximum value is $f(\tfrac{\pi}{2}) = 1$ and the absolute minimum value is $f(-\tfrac{\pi}{2}) = -1$; there is no local maximum or minimum.
>
> ![ST 3.1.21 figure|440](../Attachments/CAL1%20HW%203.1%20Solutions%20fig%2021.png)
>
> \# On all of $\mathbb{R}$, $\sin x$ has a local maximum at $\tfrac{\pi}{2}$; here the domain stops at $\tfrac{\pi}{2}$, so no open interval around $\tfrac{\pi}{2}$ lies in the domain, and the book's definition ("near $c$" means on an open interval containing $c$) rules out a local maximum there. Both extreme values exist because $f$ is continuous on a closed interval (the Extreme Value Theorem).

### ST 3.1.23
Question: [[CAL1 HW 3.1 Questions#ST 3.1.23|ST 3.1.23]]

> [!solution] Solution
> $$
> \begin{aligned}
> &y = 1 + (x + 1)^2\text{: } y = x^2 \text{ shifted 1 unit left and 1 unit up, vertex } (-1, 1) \\
> &f \text{ is decreasing on } [-2, -1] \text{ and increasing on } [-1, 5) \\[6pt]
> &(x + 1)^2 \ge 0 \implies f(x) \ge 1 = f(-1) \text{ for all } x \in [-2, 5) \implies \text{abs min } f(-1) = 1 \\
> &-1 \in (-2, 5), \text{ an open interval} \implies f(-1) = 1 \text{ is also a local min} \\[6pt]
> &-2 \le x < 5 \implies \lvert x + 1 \rvert < 6 \implies f(x) < 37, \text{ but } f(x) \to 37 \text{ as } x \to 5^{-} \implies \text{no abs max} \\
> &-2 \text{ is an endpoint} \implies f(-2) = 2 \text{ is not a local max}
> \end{aligned}
> $$
> Hence the absolute minimum value, which is also a local minimum value, is $f(-1) = 1$; there is no absolute maximum and no local maximum.
>
> ![ST 3.1.23 figure|440](../Attachments/CAL1%20HW%203.1%20Solutions%20fig%2023.png)
>
> \# The vertex lies inside the interval, so the lowest point of the parabola is both the absolute and a local minimum. The top of the graph is at the right end, $x = 5$, which the domain leaves out: the values climb toward $37$ but never reach it. The left end $(-2, 2)$ is higher than its right-hand neighbors, but it is an endpoint, so it is not a local maximum; and $f(-2) = 2 < f(4) = 26$, so it is not the absolute maximum either.

### ST 3.1.25
Question: [[CAL1 HW 3.1 Questions#ST 3.1.25|ST 3.1.25]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{domain: } x \ge 0 \\
> &y = 1 - \sqrt{x}\text{: } y = \sqrt{x} \text{ reflected about the } x\text{-axis, then shifted 1 unit up} \\
> &f \text{ is decreasing on } [0, \infty) \\[6pt]
> &\sqrt{x} \ge 0 \implies f(x) \le 1 = f(0) \text{ for all } x \ge 0 \implies \text{abs max } f(0) = 1 \\
> &f(x) \to -\infty \text{ as } x \to \infty \implies \text{no abs min} \\
> &0 \text{ is an endpoint} \implies f(0) \text{ is not a local max} \\
> &f \text{ is decreasing on } (0, \infty) \implies \text{no local max or min}
> \end{aligned}
> $$
> Hence the absolute maximum value is $f(0) = 1$; there is no absolute minimum and no local maximum or minimum.
>
> ![ST 3.1.25 figure|440](../Attachments/CAL1%20HW%203.1%20Solutions%20fig%2025.png)
>
> \# No interval is given, so the domain of the formula is the domain of $f$: $\sqrt{x}$ needs $x \ge 0$, and that makes $0$ an endpoint. The values go below every number: $f(x) < -M$ once $\sqrt{x} > M + 1$, that is, $x > (M + 1)^2$; so no value is the smallest.

### ST 3.1.27
Question: [[CAL1 HW 3.1 Questions#ST 3.1.27|ST 3.1.27]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{On } [-1, 0]\text{: } y = x^2, \text{ from } (-1, 1) \text{ down to } (0, 0) \\
> &\text{On } (0, 1]\text{: } y = 2 - 3x, \text{ a line of slope } -3 \text{ from the open dot } (0, 2) \text{ down to } (1, -1) \\[6pt]
> &f(x) = x^2 \ge 0 \text{ on } [-1, 0], \quad f(x) = 2 - 3x \ge -1 \text{ on } (0, 1] \implies \text{abs min } f(1) = -1 \\
> &f(x) = x^2 \le 1 \text{ on } [-1, 0], \quad f(x) = 2 - 3x < 2 \text{ on } (0, 1] \\
> &\text{but } f(x) \to 2 \text{ as } x \to 0^{+}, \text{ and } f(0) = 0 \ne 2 \implies \text{no abs max} \\[6pt]
> &\text{On } (-\tfrac{1}{3}, \tfrac{1}{3})\text{: } f(x) = x^2 \ge 0 \ (x \le 0), \quad f(x) = 2 - 3x > 1 > 0 \ (x > 0) \\
> &\implies f(0) = 0 \le f(x) \text{ near } 0 \implies \text{local min } f(0) = 0 \\
> &\pm 1 \text{ are endpoints}; \ f \text{ is decreasing on } (-1, 0) \text{ and on } (0, 1) \implies \text{no other local max or min}
> \end{aligned}
> $$
> Hence the absolute minimum value is $f(1) = -1$ and there is no absolute maximum; the local minimum value is $f(0) = 0$ and there is no local maximum.
>
> ![ST 3.1.27 figure|440](../Attachments/CAL1%20HW%203.1%20Solutions%20fig%2027.png)
>
> \# At $x = 0$ the graph jumps: $f(0) = 0$ comes from the first formula ($-1 \le x \le 0$), while the second formula only approaches $2$. So $(0, 2)$ is an open dot, and $2$ is approached but never taken, which leaves no absolute maximum. The filled dot $(0, 0)$ is lower than everything near it on both sides, so it is a local minimum even though $f$ is not continuous there; the definition asks only for $f(0) \le f(x)$ on an open interval around $0$. The interval $(-\tfrac{1}{3}, \tfrac{1}{3})$ is one choice; any open interval inside $(-1, \tfrac{2}{3})$ around $0$ works.

### ST 3.1.33
Question: [[CAL1 HW 3.1 Questions#ST 3.1.33|ST 3.1.33]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{domain: } \mathbb{R} \ \text{(polynomial)} \\
> &g'(t) = 5t^4 + 15t^2 + 50 \text{ exists for all } t \\
> &t^4 \ge 0,\ t^2 \ge 0 \implies g'(t) \ge 50 > 0 \implies g'(t) \ne 0 \text{ for all } t
> \end{aligned}
> $$
> Hence $g$ has no critical number.
>
> \# A critical number needs $g'(c) = 0$ or $g'(c)$ not existing, and both fail everywhere. By Fermat's Theorem, $g$ then has no local maximum or minimum; Exercise 72 is the same argument written as a proof.

### ST 3.1.35
Question: [[CAL1 HW 3.1 Questions#ST 3.1.35|ST 3.1.35]]

> [!solution] Solution
> $$
> \begin{aligned}
> &y^2 - y + 1 = \left(y - \tfrac{1}{2}\right)^2 + \tfrac{3}{4} > 0 \implies \text{domain: } \mathbb{R} \\[4pt]
> &g'(y) = \frac{(y^2 - y + 1) \cdot 1 - (y - 1)(2y - 1)}{(y^2 - y + 1)^2} && \text{(Quotient Rule)} \\
> &\phantom{g'(y)} = \frac{y^2 - y + 1 - (2y^2 - 3y + 1)}{(y^2 - y + 1)^2} = \frac{-y^2 + 2y}{(y^2 - y + 1)^2} = \frac{y(2 - y)}{(y^2 - y + 1)^2} \\[4pt]
> &g'(y) \text{ exists for all } y && (\text{denominator} > 0) \\
> &g'(y) = 0 \iff y(2 - y) = 0 \iff y = 0 \text{ or } y = 2
> \end{aligned}
> $$
> Hence the critical numbers are $0$ and $2$.
>
> \# Completing the square shows that the denominator is never $0$, so $g'$ exists everywhere and only the numerator decides. Compare Exercise 37, $p(x) = \dfrac{x^2 + 2}{2x - 1}$: there $p'$ does not exist at $\tfrac{1}{2}$, but $\tfrac{1}{2}$ is not in the domain, so it is not a critical number.

### ST 3.1.39
Question: [[CAL1 HW 3.1 Questions#ST 3.1.39|ST 3.1.39]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{domain: } t \ge 0 \\
> &t > 0\text{: } h'(t) = \tfrac{3}{4}t^{-1/4} - \tfrac{1}{2}t^{-3/4} = \frac{3t^{1/2} - 2}{4t^{3/4}} \\
> &h'(t) = 0 \iff 3\sqrt{t} = 2 \iff \sqrt{t} = \tfrac{2}{3} \iff t = \tfrac{4}{9} \\[6pt]
> &t = 0\text{: } \frac{h(0 + s) - h(0)}{s} = \frac{s^{3/4} - 2s^{1/4}}{s} = \frac{s^{1/2} - 2}{s^{3/4}} \to -\infty \text{ as } s \to 0^{+} \\
> &\implies h'(0) \text{ does not exist, and } 0 \text{ is in the domain}
> \end{aligned}
> $$
> Hence the critical numbers are $0$ and $\tfrac{4}{9}$.
>
> \# Factor out the lowest power: $\tfrac{3}{4}t^{-1/4} - \tfrac{1}{2}t^{-3/4} = \tfrac{1}{4}t^{-3/4}\left(3t^{1/2} - 2\right)$. The increment is called $s$ because $h$ is already the name of the function. At the endpoint $0$, $h$ is not defined for $t < 0$, so $h'(0)$ cannot exist as a two-sided limit; even the right-hand quotient tends to $-\infty$ (a vertical tangent). Since $0$ is in the domain, it is a critical number, as in the book's answer.

### ST 3.1.41
Question: [[CAL1 HW 3.1 Questions#ST 3.1.41|ST 3.1.41]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{domain: } \mathbb{R} && \left(x^{4/5} = (\sqrt[5]{x})^4\right) \\
> &x \ne 0\text{: } F'(x) = \tfrac{4}{5}x^{-1/5}(x - 4)^2 + x^{4/5} \cdot 2(x - 4) && \text{(Product Rule)} \\
> &\phantom{x \ne 0\text{: } F'(x)} = \frac{(x - 4)\left[4(x - 4) + 10x\right]}{5x^{1/5}} = \frac{(x - 4)(14x - 16)}{5x^{1/5}} = \frac{2(x - 4)(7x - 8)}{5x^{1/5}} \\
> &F'(x) = 0 \iff x = 4 \text{ or } x = \tfrac{8}{7} \\[6pt]
> &x = 0\text{: } \frac{F(0 + h) - F(0)}{h} = \frac{h^{4/5}(h - 4)^2}{h} = \frac{(h - 4)^2}{h^{1/5}} \to \pm\infty \text{ as } h \to 0^{\pm} \\
> &\implies F'(0) \text{ does not exist, and } 0 \text{ is in the domain}
> \end{aligned}
> $$
> Hence the critical numbers are $0$, $\tfrac{8}{7}$ and $4$.
>
> \# Take out the common factor $\dfrac{(x - 4)x^{-1/5}}{5}$: the first term leaves $4(x - 4)$ and the second $10x$ (because $x^{4/5} = x \cdot x^{-1/5}$). Two kinds of critical numbers appear: $\tfrac{8}{7}$ and $4$ where $F' = 0$, and $0$ where $F'$ does not exist. Near $0$ the graph has a cusp ($F'$ jumps from $-\infty$ to $+\infty$), like $x^{2/3}$ in Exercise 13 of §3.2.

### ST 3.1.45
Question: [[CAL1 HW 3.1 Questions#ST 3.1.45|ST 3.1.45]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{domain: } \mathbb{R} \\
> &f'(\theta) = -2\sin\theta + 2\sin\theta\cos\theta = 2\sin\theta\,(\cos\theta - 1) && \text{(Chain Rule on } \sin^2\theta\text{)} \\
> &f'(\theta) \text{ exists for all } \theta \\
> &f'(\theta) = 0 \iff \sin\theta = 0 \text{ or } \cos\theta = 1 \\
> &\sin\theta = 0 \iff \theta = n\pi; \quad \cos\theta = 1 \iff \theta = 2n\pi \ \ (\text{already among the } n\pi)
> \end{aligned}
> $$
> Hence the critical numbers are $\theta = n\pi$, where $n$ is any integer.
>
> \# $\dfrac{d}{d\theta}\sin^2\theta = 2\sin\theta\cos\theta$ by the Chain Rule (outer $u^2$, inner $\sin\theta$). Factor out $2\sin\theta$ instead of dividing by it: dividing would lose the solutions $\sin\theta = 0$. A periodic function has infinitely many critical numbers, so write them with $n$.

### ST 3.1.53
Question: [[CAL1 HW 3.1 Questions#ST 3.1.53|ST 3.1.53]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f \text{ is a polynomial} \implies f \text{ is continuous on } [-2, 3] \\
> &f'(x) = 12x^3 - 12x^2 - 24x = 12x(x^2 - x - 2) = 12x(x + 1)(x - 2) \\
> &f'(x) = 0 \iff x = -1, 0, 2, \text{ all in } (-2, 3) \\[6pt]
> &f(-1) = 3 + 4 - 12 + 1 = -4, \quad f(0) = 1, \quad f(2) = 48 - 32 - 48 + 1 = -31 \\
> &f(-2) = 48 + 32 - 48 + 1 = 33, \quad f(3) = 243 - 108 - 108 + 1 = 28
> \end{aligned}
> $$
> Hence the absolute maximum value is $f(-2) = 33$ and the absolute minimum value is $f(2) = -31$.
>
> \# Write all five values before choosing. The maximum is at an endpoint, and $f(3) = 28$ is close to it, so compute each value term by term: $f(-2) = 3 \cdot 16 - 4 \cdot (-8) - 12 \cdot 4 + 1$.

### ST 3.1.55
Question: [[CAL1 HW 3.1 Questions#ST 3.1.55|ST 3.1.55]]

> [!solution] Solution
> $$
> \begin{aligned}
> &0 \notin [0.2, 4] \implies f \text{ is continuous on } [0.2, 4] \\
> &f'(x) = 1 - \frac{1}{x^2} = \frac{(x - 1)(x + 1)}{x^2} \text{ exists on } [0.2, 4] \\
> &f'(x) = 0 \iff x = \pm 1; \quad 1 \in (0.2, 4), \ -1 \notin (0.2, 4) \\[6pt]
> &f(1) = 1 + 1 = 2 \\
> &f(0.2) = 0.2 + 5 = 5.2, \quad f(4) = 4 + \tfrac{1}{4} = 4.25
> \end{aligned}
> $$
> Hence the absolute maximum value is $f(0.2) = 5.2$ and the absolute minimum value is $f(1) = 2$.
>
> \# Drop the critical number $-1$: it is outside the interval, and using $f(-1) = -2$ would give a wrong minimum. Check: for $x > 0$, $x + \dfrac{1}{x} - 2 = \dfrac{(x - 1)^2}{x} \ge 0$, so $2$ is indeed the smallest value.

### ST 3.1.57
Question: [[CAL1 HW 3.1 Questions#ST 3.1.57|ST 3.1.57]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\sqrt[3]{t} \text{ is continuous everywhere} \implies f \text{ is continuous on } [-1, 4] \\
> &t \ne 0\text{: } f'(t) = 1 - \tfrac{1}{3}t^{-2/3} = 1 - \frac{1}{3\sqrt[3]{t^2}} \\
> &f'(t) = 0 \iff \sqrt[3]{t^2} = \tfrac{1}{3} \iff t^2 = \tfrac{1}{27} \iff t = \pm\frac{1}{3\sqrt{3}} = \pm\frac{\sqrt{3}}{9} \\
> &t = 0\text{: } \frac{f(0 + h) - f(0)}{h} = \frac{h - \sqrt[3]{h}}{h} = 1 - \frac{1}{\sqrt[3]{h^2}} \to -\infty \implies f'(0) \text{ does not exist} \\
> &\text{critical numbers in } (-1, 4)\text{: } -\tfrac{\sqrt{3}}{9},\ 0,\ \tfrac{\sqrt{3}}{9} \\[6pt]
> &\sqrt[3]{\pm\tfrac{\sqrt{3}}{9}} = \pm\sqrt[3]{3^{-3/2}} = \pm 3^{-1/2} = \pm\tfrac{\sqrt{3}}{3} \\
> &f(-\tfrac{\sqrt{3}}{9}) = -\tfrac{\sqrt{3}}{9} + \tfrac{\sqrt{3}}{3} = \tfrac{2\sqrt{3}}{9} \approx 0.385, \quad f(0) = 0 \\
> &f(\tfrac{\sqrt{3}}{9}) = \tfrac{\sqrt{3}}{9} - \tfrac{\sqrt{3}}{3} = -\tfrac{2\sqrt{3}}{9} \approx -0.385 \\
> &f(-1) = -1 - (-1) = 0, \quad f(4) = 4 - \sqrt[3]{4} \approx 2.413
> \end{aligned}
> $$
> Hence the absolute maximum value is $f(4) = 4 - \sqrt[3]{4}$ and the absolute minimum value is $f(\tfrac{\sqrt{3}}{9}) = -\tfrac{2\sqrt{3}}{9}$.
>
> \# Three critical numbers lie in $(-1, 4)$: two where $f' = 0$ and $0$, where $f'$ does not exist (a vertical tangent: the quotient tends to $-\infty$ from both sides, because $\sqrt[3]{h^2} > 0$). Leaving out $0$ is the usual mistake; here $f(0) = 0$ does not win, but the method needs every candidate. To solve $\sqrt[3]{t^2} = \tfrac{1}{3}$, cube both sides; both signs of $t$ count, since $t$ may be negative in $(-1, 4)$. Write $\tfrac{\sqrt{3}}{9} = 3^{1/2} \cdot 3^{-2} = 3^{-3/2}$ to take its cube root.

### ST 3.1.59
Question: [[CAL1 HW 3.1 Questions#ST 3.1.59|ST 3.1.59]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\cos, \sin \text{ are continuous everywhere} \implies f \text{ is continuous on } [0, \tfrac{\pi}{2}] \\
> &f'(t) = -2\sin t + 2\cos 2t && \text{(Chain Rule)} \\
> &\phantom{f'(t)} = -2\sin t + 2(1 - 2\sin^2 t) = -2(2\sin^2 t + \sin t - 1) = -2(2\sin t - 1)(\sin t + 1) \\
> &f'(t) = 0 \iff \sin t = \tfrac{1}{2} \text{ or } \sin t = -1 \\
> &0 < t < \tfrac{\pi}{2} \implies 0 < \sin t < 1 \implies \sin t = \tfrac{1}{2} \implies t = \tfrac{\pi}{6} \\[6pt]
> &f(\tfrac{\pi}{6}) = 2 \cdot \tfrac{\sqrt{3}}{2} + \sin\tfrac{\pi}{3} = \sqrt{3} + \tfrac{\sqrt{3}}{2} = \tfrac{3\sqrt{3}}{2} \approx 2.60 \\
> &f(0) = 2 + 0 = 2, \quad f(\tfrac{\pi}{2}) = 0 + \sin\pi = 0
> \end{aligned}
> $$
> Hence the absolute maximum value is $f(\tfrac{\pi}{6}) = \tfrac{3\sqrt{3}}{2}$ and the absolute minimum value is $f(\tfrac{\pi}{2}) = 0$.
>
> \# Use $\cos 2t = 1 - 2\sin^2 t$ so that $f'$ contains only $\sin t$; then it factors like the quadratic $2u^2 + u - 1 = (2u - 1)(u + 1)$ with $u = \sin t$. On the open interval $(0, \tfrac{\pi}{2})$, $\sin t$ lies strictly between $0$ and $1$, so $\sin t = -1$ gives nothing.

### ST 3.1.72
Question: [[CAL1 HW 3.1 Questions#ST 3.1.72|ST 3.1.72]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{pf: } f \text{ is a polynomial, so its domain is } \mathbb{R} \text{ and } f'(x) \text{ exists for all } x. \\
> &f'(x) = 101x^{100} + 51x^{50} + 1 && \text{(Power Rule)} \\
> &\because x^{100} = (x^{50})^2 \ge 0 \text{ and } x^{50} = (x^{25})^2 \ge 0 \text{ for all } x, \\
> &\therefore f'(x) \ge 1 > 0, \text{ so } f'(x) \ne 0 \text{ for all } x \\
> &\implies f \text{ has no critical number} && \text{(definition of critical number)} \\[6pt]
> &\text{Suppose } f \text{ has a local maximum or minimum at some } c. \\
> &\implies c \text{ is a critical number of } f && \text{(Fermat's Theorem)} \\
> &\text{This contradicts the fact that } f \text{ has no critical number.} \\[6pt]
> &\text{Hence } f \text{ has neither a local maximum nor a local minimum.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Both ways of being a critical number fail here: $f'(c)$ exists, and $f'(c) \ne 0$. Write both, then let Fermat's Theorem finish: a local extremum can only occur at a critical number. The even powers are $\ge 0$ because they are squares; write that reason, since grading deducts points for a missing condition. Equivalently: if $f$ had a local extremum at $c$, then $f'(c) = 0$ by Fermat's Theorem, but $f'(c) \ge 1$.
