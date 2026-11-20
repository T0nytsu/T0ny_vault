---
course: [CAL1]
semester: "115-1"
chapter: ["4.2"]
tags: [calculus, homework, solutions, integrals]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §4.2, pp. 314-327, scanned PDF (Definition 2, Theorems 3 and 4, the Midpoint Rule, sums of powers, properties of the integral)"
created: 2026-11-18
questions: "[[CAL1 HW 4.2 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 4.2 Questions#ST 4.2.1\|ST 4.2.1]] | $R_5 = -10$: areas of the rectangles above the $x$-axis minus those below |
| [[CAL1 HW 4.2 Questions#ST 4.2.9\|ST 4.2.9]] | $M_4 = 168$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.19\|ST 4.2.19]] | $\int_0^\pi \dfrac{\sin x}{1 + x}\,dx$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.20\|ST 4.2.20]] | $\int_2^5 x\sqrt{1 + x^3}\,dx$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.21\|ST 4.2.21]] | $\int_2^7 (5x^3 - 4x)\,dx$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.22\|ST 4.2.22]] | $\int_1^3 \dfrac{x}{x^2 + 4}\,dx$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.23\|ST 4.2.23]] | $-\tfrac{40}{3}$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.25\|ST 4.2.25]] | $\lim_{n \to \infty} \sum_{i=1}^{n} \sqrt{4 + \left(1 + \tfrac{2i}{n}\right)^2}\cdot\tfrac{2}{n}$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.33\|ST 4.2.33]] | $-\tfrac{3}{4}$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.35\|ST 4.2.35]] | (a) $4$; (b) $10$; (c) $-3$; (d) $0$; (e) $6$; (f) $-4$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.51\|ST 4.2.51]] | $0$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.52\|ST 4.2.52]] | $-\tfrac{3}{8}\pi$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.57\|ST 4.2.57]] | $\int_{-1}^{5} f(x)\,dx$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.58\|ST 4.2.58]] | $1.4$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.59\|ST 4.2.59]] | $122$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.60\|ST 4.2.60]] | $17$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.61\|ST 4.2.61]] | $B < E < A < D < C$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.63\|ST 4.2.63]] | $15$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.65\|ST 4.2.65]] | Shown: $(x - 2)^2 \ge 0$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.66\|ST 4.2.66]] | Shown: $\sqrt{1 + x^2} \le \sqrt{1 + x}$ on $[0, 1]$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.67\|ST 4.2.67]] | Shown: $1 \le \sqrt{1 + x^2} \le \sqrt{2}$ on $[-1, 1]$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.68\|ST 4.2.68]] | Shown: $\tfrac{1}{2} \le \sin x \le \tfrac{\sqrt{3}}{2}$ on $[\tfrac{\pi}{6}, \tfrac{\pi}{3}]$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.75\|ST 4.2.75]] | Proof: $\sqrt{x^4 + 1} \ge x^2$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.83\|ST 4.2.83]] | $\int_0^1 x^4\,dx$ |
| [[CAL1 HW 4.2 Questions#ST 4.2.84\|ST 4.2.84]] | $\int_0^1 \dfrac{1}{1 + x^2}\,dx$ |

## ST §4.2 The Definite Integral

> [!note] Note
> The facts that the answers use, each under its name. An answer writes the fact itself; the numbers are those of ST §4.2 and matter only where a question names them.
> - **Riemann sum**: divide $[a, b]$ into $n$ subintervals of width $\Delta x = \dfrac{b - a}{n}$, with endpoints $x_i = a + i\,\Delta x$, and pick a sample point $x_i^*$ in $[x_{i-1}, x_i]$. Then $\sum_{i=1}^{n} f(x_i^*)\,\Delta x$ is a Riemann sum.
> - **Definite integral** (Definition 2): $\int_a^b f(x)\,dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*)\,\Delta x$, if the limit exists and is the same for every choice of sample points; then $f$ is *integrable* on $[a, b]$.
> - **Integrable functions** (Theorem 3): if $f$ is continuous on $[a, b]$, or has only finitely many jump discontinuities there, then $f$ is integrable on $[a, b]$.
> - **Right endpoints** (Theorem 4): if $f$ is integrable on $[a, b]$, then $\int_a^b f(x)\,dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i)\,\Delta x$, where $\Delta x = \dfrac{b - a}{n}$ and $x_i = a + i\,\Delta x$.
> - **Midpoint Rule**: $\int_a^b f(x)\,dx \approx \Delta x\,[f(\bar{x}_1) + \cdots + f(\bar{x}_n)]$, where $\bar{x}_i = \tfrac{1}{2}(x_{i-1} + x_i)$ is the midpoint of $[x_{i-1}, x_i]$.
> - **Net area**: $\int_a^b f(x)\,dx = A_1 - A_2$, where $A_1$ is the area above the $x$-axis and below $y = f(x)$, and $A_2$ the area below the $x$-axis and above $y = f(x)$.
> - **Sums of powers**: $\sum_{i=1}^{n} 1 = n$, $\sum_{i=1}^{n} i = \dfrac{n(n + 1)}{2}$, $\sum_{i=1}^{n} i^2 = \dfrac{n(n + 1)(2n + 1)}{6}$, $\sum_{i=1}^{n} i^3 = \left[\dfrac{n(n + 1)}{2}\right]^2$; constants come out of a sum, and a sum splits over $+$ and $-$.
> - **Properties of the integral**: $\int_b^a f\,dx = -\int_a^b f\,dx$; $\int_a^a f\,dx = 0$; $\int_a^b c\,dx = c(b - a)$; $\int_a^b [f \pm g]\,dx = \int_a^b f\,dx \pm \int_a^b g\,dx$; $\int_a^b cf\,dx = c\int_a^b f\,dx$; $\int_a^c f\,dx + \int_c^b f\,dx = \int_a^b f\,dx$.
> - **Comparison properties** (Properties 6–8, for $a \le b$): $f(x) \ge 0$ on $[a, b] \implies \int_a^b f\,dx \ge 0$; $f(x) \ge g(x)$ on $[a, b] \implies \int_a^b f\,dx \ge \int_a^b g\,dx$; $m \le f(x) \le M$ on $[a, b] \implies m(b - a) \le \int_a^b f\,dx \le M(b - a)$.
> - **Exercises 47 and 48**: $\int_a^b x\,dx = \dfrac{b^2 - a^2}{2}$ and $\int_a^b x^2\,dx = \dfrac{b^3 - a^3}{3}$.
> - Each answer is written as on an exam paper: the computation first, then the conclusion on a Hence line. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 4.2.1
Question: [[CAL1 HW 4.2 Questions#ST 4.2.1|ST 4.2.1]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\Delta x = \frac{4 - (-6)}{5} = 2, \quad x_i = -6 + 2i\text{: } -4,\ -2,\ 0,\ 2,\ 4 \\
> &R_5 = \sum_{i=1}^{5} f(x_i)\,\Delta x = 2\,[f(-4) + f(-2) + f(0) + f(2) + f(4)] \\
> &\hphantom{R_5} = 2\,[(-5) + (-3) + (-1) + 1 + 3] = 2(-5) = -10
> \end{aligned}
> $$
> Hence $R_5 = -10$.
>
> ![ST 4.2.1 figure|400](../Attachments/CAL1%20HW%204.2%20Solutions%20fig%201.png)
>
> The Riemann sum is the sum of the areas of the two rectangles above the $x$-axis minus the sum of the areas of the three rectangles below it:
> $$
> R_5 = (2 + 6) - (10 + 6 + 2) = -10.
> $$
>
> \# The numbers in the figure are the areas of the rectangles: width $2$ times height $\lvert f(x_i) \rvert$. A rectangle below the axis comes from $f(x_i) < 0$, so it enters the sum with a minus sign. $R_5$ only estimates the net area $\int_{-6}^{4} (x - 1)\,dx = \tfrac{16 - 36}{2} - 10 = -20$: $f$ is increasing, so every right endpoint gives the largest value on its subinterval and $R_5$ is too large.

### ST 4.2.9
Question: [[CAL1 HW 4.2 Questions#ST 4.2.9|ST 4.2.9]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\Delta x = \frac{8 - 0}{4} = 2, \quad \text{midpoints } \bar{x}_i\text{: } 1,\ 3,\ 5,\ 7 \\
> &M_4 = 2\,(1^2 + 3^2 + 5^2 + 7^2) = 2\,(1 + 9 + 25 + 49) = 2 \cdot 84 = 168
> \end{aligned}
> $$
> Hence $\int_0^8 x^2\,dx \approx 168$.
>
> \# The subintervals are $[0, 2]$, $[2, 4]$, $[4, 6]$, $[6, 8]$; take the middle of each, not an endpoint. By Exercise 48 the exact value is $\tfrac{8^3}{3} = \tfrac{512}{3} \approx 170.67$, so $M_4$ is already close.

### ST 4.2.19
Question: [[CAL1 HW 4.2 Questions#ST 4.2.19|ST 4.2.19]]

> [!solution] Solution
> $f(x) = \dfrac{\sin x}{1 + x}$ is continuous on $[0, \pi]$ ($1 + x \ge 1 > 0$), so it is integrable there, and
> $$
> \lim_{n \to \infty} \sum_{i=1}^{n} \frac{\sin x_i}{1 + x_i}\,\Delta x = \int_0^\pi \frac{\sin x}{1 + x}\,dx.
> $$
>
> \# Read the sum as $\sum f(x_i)\,\Delta x$: whatever is done to $x_i$ is $f$, and the interval gives the limits $a = 0$, $b = \pi$. Continuity is what makes $f$ integrable, so that the limit exists and equals the integral. Exercises 20–22 work the same way.

### ST 4.2.20
Question: [[CAL1 HW 4.2 Questions#ST 4.2.20|ST 4.2.20]]

> [!solution] Solution
> $f(x) = x\sqrt{1 + x^3}$ is continuous on $[2, 5]$ ($1 + x^3 > 0$ there), so
> $$
> \lim_{n \to \infty} \sum_{i=1}^{n} x_i\sqrt{1 + x_i^3}\,\Delta x = \int_2^5 x\sqrt{1 + x^3}\,dx.
> $$

### ST 4.2.21
Question: [[CAL1 HW 4.2 Questions#ST 4.2.21|ST 4.2.21]]

> [!solution] Solution
> $f(x) = 5x^3 - 4x$ is a polynomial, continuous on $[2, 7]$, so
> $$
> \lim_{n \to \infty} \sum_{i=1}^{n} \left[5(x_i^*)^3 - 4x_i^*\right]\Delta x = \int_2^7 (5x^3 - 4x)\,dx.
> $$
>
> \# Here the sample points are any $x_i^*$ in $[x_{i-1}, x_i]$, not only right endpoints; for an integrable $f$ every choice gives the same limit (Definition 2).

### ST 4.2.22
Question: [[CAL1 HW 4.2 Questions#ST 4.2.22|ST 4.2.22]]

> [!solution] Solution
> $f(x) = \dfrac{x}{x^2 + 4}$ is continuous on $[1, 3]$ ($x^2 + 4 > 0$), so
> $$
> \lim_{n \to \infty} \sum_{i=1}^{n} \frac{x_i^*}{(x_i^*)^2 + 4}\,\Delta x = \int_1^3 \frac{x}{x^2 + 4}\,dx.
> $$

### ST 4.2.23
Question: [[CAL1 HW 4.2 Questions#ST 4.2.23|ST 4.2.23]]

> [!solution] Solution
> $f(x) = x - x^2$ is continuous on $[0, 4]$, so it is integrable and the right-endpoint form applies:
> $$
> \begin{aligned}
> &\Delta x = \frac{4 - 0}{n} = \frac{4}{n}, \quad x_i = 0 + i\,\Delta x = \frac{4i}{n} \\
> &f(x_i) = \frac{4i}{n} - \Big(\frac{4i}{n}\Big)^2 = \frac{4i}{n} - \frac{16i^2}{n^2} \\
> &\int_0^4 (x - x^2)\,dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i)\,\Delta x = \lim_{n \to \infty} \frac{4}{n}\sum_{i=1}^{n}\left[\frac{4i}{n} - \frac{16i^2}{n^2}\right] = \lim_{n \to \infty} R_n
> \end{aligned}
> $$
> Evaluate:
> $$
> \begin{aligned}
> R_n &= \frac{16}{n^2}\sum_{i=1}^{n} i - \frac{64}{n^3}\sum_{i=1}^{n} i^2 \\
> &= \frac{16}{n^2} \cdot \frac{n(n + 1)}{2} - \frac{64}{n^3} \cdot \frac{n(n + 1)(2n + 1)}{6} \\
> &= 8\Big(1 + \frac{1}{n}\Big) - \frac{32}{3}\Big(1 + \frac{1}{n}\Big)\Big(2 + \frac{1}{n}\Big) \\
> \lim_{n \to \infty} R_n &= 8 - \frac{32}{3} \cdot 2 = 8 - \frac{64}{3} = -\frac{40}{3}
> \end{aligned}
> $$
> Hence $\int_0^4 (x - x^2)\,dx = \lim_{n \to \infty} R_n = -\tfrac{40}{3}$.
>
> \# Third line: $\tfrac{16}{n^2} \cdot \tfrac{n(n + 1)}{2} = \tfrac{8(n + 1)}{n}$ and $\tfrac{64}{n^3} \cdot \tfrac{n(n + 1)(2n + 1)}{6} = \tfrac{32}{3} \cdot \tfrac{n + 1}{n} \cdot \tfrac{2n + 1}{n}$; dividing each factor by $n$ shows the limit. The answer is negative because $x - x^2 = x(1 - x) < 0$ on $(1, 4]$, and that part of the region lies below the $x$-axis and is larger than the part above it on $(0, 1)$.

### ST 4.2.25
Question: [[CAL1 HW 4.2 Questions#ST 4.2.25|ST 4.2.25]]

> [!solution] Solution
> $f(x) = \sqrt{4 + x^2}$ is continuous on $[1, 3]$.
> $$
> \begin{aligned}
> &\Delta x = \frac{3 - 1}{n} = \frac{2}{n}, \quad x_i = 1 + i\,\Delta x = 1 + \frac{2i}{n} \\
> &\int_1^3 \sqrt{4 + x^2}\,dx = \lim_{n \to \infty} \sum_{i=1}^{n} \sqrt{4 + \Big(1 + \frac{2i}{n}\Big)^2} \cdot \frac{2}{n}
> \end{aligned}
> $$
>
> \# The right endpoints start from $a = 1$, so $x_i = 1 + \tfrac{2i}{n}$, not $\tfrac{2i}{n}$: check $x_n = 1 + 2 = 3 = b$.

### ST 4.2.33
Question: [[CAL1 HW 4.2 Questions#ST 4.2.33|ST 4.2.33]]

> [!solution] Solution
> $f(x) = x^3 - 3x^2$ is continuous on $[0, 1]$, so by Theorem 4, with $\Delta x = \tfrac{1}{n}$ and $x_i = \tfrac{i}{n}$,
> $$
> \begin{aligned}
> \int_0^1 (x^3 - 3x^2)\,dx &= \lim_{n \to \infty} \sum_{i=1}^{n}\left[\Big(\frac{i}{n}\Big)^3 - 3\Big(\frac{i}{n}\Big)^2\right]\frac{1}{n} \\
> &= \lim_{n \to \infty}\left[\frac{1}{n^4}\sum_{i=1}^{n} i^3 - \frac{3}{n^3}\sum_{i=1}^{n} i^2\right] \\
> &= \lim_{n \to \infty}\left[\frac{1}{n^4}\Big(\frac{n(n + 1)}{2}\Big)^2 - \frac{3}{n^3} \cdot \frac{n(n + 1)(2n + 1)}{6}\right] \\
> &= \lim_{n \to \infty}\left[\frac{1}{4}\Big(1 + \frac{1}{n}\Big)^2 - \frac{1}{2}\Big(1 + \frac{1}{n}\Big)\Big(2 + \frac{1}{n}\Big)\right] \\
> &= \frac{1}{4} - 1 = -\frac{3}{4}
> \end{aligned}
> $$
> Hence $\int_0^1 (x^3 - 3x^2)\,dx = -\tfrac{3}{4}$.
>
> \# $\tfrac{1}{n^4} \cdot \tfrac{n^2(n + 1)^2}{4} = \tfrac{(n + 1)^2}{4n^2}$ and $\tfrac{3}{n^3} \cdot \tfrac{n(n + 1)(2n + 1)}{6} = \tfrac{(n + 1)(2n + 1)}{2n^2}$. The value is negative because $x^3 - 3x^2 = x^2(x - 3) \le 0$ on $[0, 1]$: the whole region lies below the $x$-axis.

### ST 4.2.35
Question: [[CAL1 HW 4.2 Questions#ST 4.2.35|ST 4.2.35]]

> [!solution] Solution
> ![ST 4.2.35 figure|460](../Attachments/CAL1%20HW%204.2%20Solutions%20fig%2035.png)
>
> From the graph: $f(0) = 1$, $f(2) = f(3) = 3$, $f(5) = 0$, $f(7) = -3$.
> - (a) $\int_0^2 f(x)\,dx = \dfrac{1 + 3}{2} \cdot 2 = 4$ (trapezoid)
> - (b) $\int_0^5 f(x)\,dx = 4 + 3 \cdot 1 + \tfrac{1}{2} \cdot 2 \cdot 3 = 4 + 3 + 3 = 10$
> - (c) $\int_5^7 f(x)\,dx = -\tfrac{1}{2} \cdot 2 \cdot 3 = -3$ (below the axis)
> - (d) $\int_3^7 f(x)\,dx = \int_3^5 f(x)\,dx + \int_5^7 f(x)\,dx = 3 + (-3) = 0$
> - (e) $\int_3^7 \lvert f(x) \rvert\,dx = 3 + 3 = 6$
> - (f) $\int_2^0 f(x)\,dx = -\int_0^2 f(x)\,dx = -4$
>
> \# An integral is the area above the axis minus the area below. $\lvert f \rvert$ reflects the part below the axis upward, so in (e) both triangles count as $+3$; compare (d), where they cancel. In (f) the limits are reversed, which changes the sign.

### ST 4.2.51
Question: [[CAL1 HW 4.2 Questions#ST 4.2.51|ST 4.2.51]]

> [!solution] Solution
> $$
> \int_1^1 \sqrt{1 + x^4}\,dx = 0
> $$
> since the lower and upper limits are equal.
>
> \# $\int_a^a f(x)\,dx = 0$ for every $f$: there is no width, so there is no area. Nothing about $\sqrt{1 + x^4}$ needs to be computed.

### ST 4.2.52
Question: [[CAL1 HW 4.2 Questions#ST 4.2.52|ST 4.2.52]]

> [!solution] Solution
> $$
> \int_\pi^0 \sin^4\theta\,d\theta = -\int_0^\pi \sin^4\theta\,d\theta = -\int_0^\pi \sin^4 x\,dx = -\frac{3}{8}\pi
> $$
>
> \# Two facts: reversing the limits changes the sign, and the name of the variable does not matter ($\theta$ and $x$ are both dummy variables), so $\int_0^\pi \sin^4\theta\,d\theta$ is the given $\tfrac{3}{8}\pi$.

### ST 4.2.57
Question: [[CAL1 HW 4.2 Questions#ST 4.2.57|ST 4.2.57]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\int_{-2}^{2} f(x)\,dx + \int_2^5 f(x)\,dx = \int_{-2}^{5} f(x)\,dx \\
> &\int_{-2}^{5} f(x)\,dx = \int_{-2}^{-1} f(x)\,dx + \int_{-1}^{5} f(x)\,dx \\
> &\implies \int_{-2}^{5} f(x)\,dx - \int_{-2}^{-1} f(x)\,dx = \int_{-1}^{5} f(x)\,dx
> \end{aligned}
> $$
> Hence the expression equals $\int_{-1}^{5} f(x)\,dx$.
>
> \# Think in intervals: $[-2, 2]$ and $[2, 5]$ join into $[-2, 5]$, and taking away $[-2, -1]$ leaves $[-1, 5]$.

### ST 4.2.58
Question: [[CAL1 HW 4.2 Questions#ST 4.2.58|ST 4.2.58]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\int_2^8 f(x)\,dx = \int_2^4 f(x)\,dx + \int_4^8 f(x)\,dx \\
> &\implies \int_4^8 f(x)\,dx = 7.3 - 5.9 = 1.4
> \end{aligned}
> $$
> Hence $\int_4^8 f(x)\,dx = 1.4$.

### ST 4.2.59
Question: [[CAL1 HW 4.2 Questions#ST 4.2.59|ST 4.2.59]]

> [!solution] Solution
> $$
> \int_0^9 [2f(x) + 3g(x)]\,dx = 2\int_0^9 f(x)\,dx + 3\int_0^9 g(x)\,dx = 2 \cdot 37 + 3 \cdot 16 = 74 + 48 = 122
> $$
> Hence the integral is $122$.

### ST 4.2.60
Question: [[CAL1 HW 4.2 Questions#ST 4.2.60|ST 4.2.60]]

> [!solution] Solution
> $$
> \begin{aligned}
> \int_0^5 f(x)\,dx &= \int_0^3 3\,dx + \int_3^5 x\,dx \\
> &= 3(3 - 0) + \frac{5^2 - 3^2}{2} = 9 + 8 = 17
> \end{aligned}
> $$
> Hence $\int_0^5 f(x)\,dx = 17$.
>
> \# Split at $3$, where the formula for $f$ changes. $\int_3^5 x\,dx$ is Exercise 47, or the area of a trapezoid with parallel sides $3$ and $5$ and width $2$: $\tfrac{3 + 5}{2} \cdot 2 = 8$.

### ST 4.2.61
Question: [[CAL1 HW 4.2 Questions#ST 4.2.61|ST 4.2.61]]

> [!solution] Solution
> ![ST 4.2.61 figure|440](../Attachments/CAL1%20HW%204.2%20Solutions%20fig%2061.png)
>
> $f < 0$ on $(0, 3)$ and $f > 0$ on $(3, 8)$. Counting squares (each of area $1$):
> $$
> \begin{aligned}
> &B = \int_0^3 f(x)\,dx \approx -3.6 \\
> &E = f'(1) \approx -0.6 \quad (\text{the tangent at } x = 1 \text{ slopes slightly down, less steeply than slope } -1) \\
> &C = \int_3^4 f(x)\,dx + D, \quad \int_3^4 f(x)\,dx \approx 1 > 0 \implies D < C \\
> &A = B + C = \Big(B + \int_3^4 f(x)\,dx\Big) + D, \quad B + \int_3^4 f(x)\,dx \approx -3.6 + 1 < 0 \implies A < D \\
> &A = B + C \approx -3.6 + 14.2 > 0 > E, \qquad E > -1 > B
> \end{aligned}
> $$
> Hence $B < E < A < D < C$.
>
> \# Only the order matters, so rough counts are enough: the region below the axis on $[0, 3]$ is a little less than $4$ squares, the region on $[3, 4]$ about $1$ square, and the region on $[4, 8]$ about $13$ squares. The two negatives are $B$ and $E$; the lowest point of the graph is just to the right of $x = 1$, so $f'(1)$ is negative but small. The other three all contain the big positive piece $D$: $C$ is $D$ plus the small positive piece on $[3, 4]$, and $A$ is $C$ plus the negative $B$, which outweighs that small piece.

### ST 4.2.63
Question: [[CAL1 HW 4.2 Questions#ST 4.2.63|ST 4.2.63]]

> [!solution] Solution
> ![ST 4.2.63 figure|460](../Attachments/CAL1%20HW%204.2%20Solutions%20fig%2063.png)
>
> $$
> \begin{aligned}
> &\int_{-4}^{2} f(x)\,dx = -3 + 3 - 3 = -3 \quad (A, C \text{ below the axis, } B \text{ above}) \\
> &\int_{-4}^{2} (2x + 5)\,dx = 2 \cdot \frac{2^2 - (-4)^2}{2} + 5\,(2 - (-4)) = -12 + 30 = 18 \\
> &\int_{-4}^{2} [f(x) + 2x + 5]\,dx = -3 + 18 = 15
> \end{aligned}
> $$
> Hence the value is $15$.
>
> \# "Area 3" is always positive; the integral gives a region below the axis the sign $-$. The second line uses Exercise 47 for $\int x\,dx$ and $\int_a^b c\,dx = c(b - a)$.

### ST 4.2.65
Question: [[CAL1 HW 4.2 Questions#ST 4.2.65|ST 4.2.65]]

> [!solution] Solution
> $$
> x^2 - 4x + 4 = (x - 2)^2 \ge 0 \quad \text{for } 0 \le x \le 4 \implies \int_0^4 (x^2 - 4x + 4)\,dx \ge 0
> $$
>
> \# Comparison property: $f(x) \ge 0$ on $[a, b]$ gives $\int_a^b f(x)\,dx \ge 0$. Factoring is the step that shows the sign.

### ST 4.2.66
Question: [[CAL1 HW 4.2 Questions#ST 4.2.66|ST 4.2.66]]

> [!solution] Solution
> $$
> \begin{aligned}
> &0 \le x \le 1 \implies x^2 \le x \implies 1 + x^2 \le 1 + x \implies \sqrt{1 + x^2} \le \sqrt{1 + x} \\
> &\implies \int_0^1 \sqrt{1 + x^2}\,dx \le \int_0^1 \sqrt{1 + x}\,dx
> \end{aligned}
> $$
>
> \# $x^2 \le x$ because $x^2 - x = x(x - 1) \le 0$ when $0 \le x \le 1$ (this fails for $x > 1$). $\sqrt{\phantom{x}}$ is increasing, so it keeps $\le$. Last step: $f \le g$ on $[a, b]$ gives $\int_a^b f \le \int_a^b g$.

### ST 4.2.67
Question: [[CAL1 HW 4.2 Questions#ST 4.2.67|ST 4.2.67]]

> [!solution] Solution
> $$
> \begin{aligned}
> &-1 \le x \le 1 \implies 0 \le x^2 \le 1 \implies 1 \le 1 + x^2 \le 2 \implies 1 \le \sqrt{1 + x^2} \le \sqrt{2} \\
> &\implies 1 \cdot (1 - (-1)) \le \int_{-1}^{1} \sqrt{1 + x^2}\,dx \le \sqrt{2} \cdot (1 - (-1)) \\
> &\implies 2 \le \int_{-1}^{1} \sqrt{1 + x^2}\,dx \le 2\sqrt{2}
> \end{aligned}
> $$
>
> \# Comparison property with $m = 1$ (at $x = 0$) and $M = \sqrt{2}$ (at $x = \pm 1$): $m(b - a) \le \int_a^b f \le M(b - a)$, and $b - a = 2$.

### ST 4.2.68
Question: [[CAL1 HW 4.2 Questions#ST 4.2.68|ST 4.2.68]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{\pi}{6} \le x \le \frac{\pi}{3} \implies \sin\frac{\pi}{6} \le \sin x \le \sin\frac{\pi}{3} \implies \frac{1}{2} \le \sin x \le \frac{\sqrt{3}}{2} \\
> &\implies \frac{1}{2}\Big(\frac{\pi}{3} - \frac{\pi}{6}\Big) \le \int_{\pi/6}^{\pi/3} \sin x\,dx \le \frac{\sqrt{3}}{2}\Big(\frac{\pi}{3} - \frac{\pi}{6}\Big) \\
> &\implies \frac{\pi}{12} \le \int_{\pi/6}^{\pi/3} \sin x\,dx \le \frac{\sqrt{3}\,\pi}{12}
> \end{aligned}
> $$
>
> \# The first step uses that $\sin$ is increasing on $[0, \tfrac{\pi}{2}]$, so on $[\tfrac{\pi}{6}, \tfrac{\pi}{3}]$ its smallest value is at the left end and its largest at the right end. The length of the interval is $\tfrac{\pi}{3} - \tfrac{\pi}{6} = \tfrac{\pi}{6}$.

### ST 4.2.75
Question: [[CAL1 HW 4.2 Questions#ST 4.2.75|ST 4.2.75]]

> [!proof] Proof
> For $1 \le x \le 3$,
> $$
> x^4 + 1 > x^4 \implies \sqrt{x^4 + 1} > \sqrt{x^4} = x^2.
> $$
> Hence, by the comparison property and Exercise 48,
> $$
> \int_1^3 \sqrt{x^4 + 1}\,dx \ge \int_1^3 x^2\,dx = \frac{3^3 - 1^3}{3} = \frac{26}{3}. \qquad \blacksquare
> $$
>
> \# The idea: drop the $+1$ to get a function you can integrate (Exercise 48), and dropping a positive term makes the integrand smaller, so the inequality goes the right way. $\sqrt{x^4} = x^2$ holds because $x^2 \ge 0$.

### ST 4.2.83
Question: [[CAL1 HW 4.2 Questions#ST 4.2.83|ST 4.2.83]]

> [!solution] Solution
> $$
> \sum_{i=1}^{n} \frac{i^4}{n^5} = \sum_{i=1}^{n} \Big(\frac{i}{n}\Big)^4 \cdot \frac{1}{n}
> $$
> This is $\sum f(x_i)\,\Delta x$ with $f(x) = x^4$ on $[0, 1]$: $\Delta x = \tfrac{1 - 0}{n} = \tfrac{1}{n}$, $x_i = 0 + \tfrac{i}{n}$. Since $f$ is continuous on $[0, 1]$,
> $$
> \lim_{n \to \infty} \sum_{i=1}^{n} \frac{i^4}{n^5} = \int_0^1 x^4\,dx.
> $$
>
> \# Split $n^5 = n^4 \cdot n$: $n^4$ goes with $i^4$ to make $\big(\tfrac{i}{n}\big)^4 = f(x_i)$, and the last $n$ becomes $\Delta x = \tfrac{1}{n}$. $\Delta x = \tfrac{1}{n}$ and $x_i = \tfrac{i}{n}$ together say $a = 0$, $b = 1$.

### ST 4.2.84
Question: [[CAL1 HW 4.2 Questions#ST 4.2.84|ST 4.2.84]]

> [!solution] Solution
> $$
> \frac{1}{n}\sum_{i=1}^{n} \frac{1}{1 + (i/n)^2} = \sum_{i=1}^{n} \frac{1}{1 + (i/n)^2} \cdot \frac{1}{n}
> $$
> This is $\sum f(x_i)\,\Delta x$ with $f(x) = \dfrac{1}{1 + x^2}$ on $[0, 1]$: $\Delta x = \tfrac{1}{n}$, $x_i = \tfrac{i}{n}$. Since $f$ is continuous on $[0, 1]$,
> $$
> \lim_{n \to \infty} \frac{1}{n}\sum_{i=1}^{n} \frac{1}{1 + (i/n)^2} = \int_0^1 \frac{1}{1 + x^2}\,dx.
> $$
>
> \# Same pattern as Exercise 83: the $\tfrac{1}{n}$ in front is $\Delta x$, and $\tfrac{i}{n}$ inside is $x_i$.
