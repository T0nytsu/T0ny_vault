---
course: [CAL1]
semester: "115-1"
chapter: ["4.3"]
tags: [calculus, homework, solutions, integrals, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §4.3, pp. 329-338, scanned PDF (the Fundamental Theorem of Calculus, Parts 1 and 2)"
created: 2026-11-18
questions: "[[CAL1 HW 4.3 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 4.3 Questions#ST 4.3.3\|ST 4.3.3]] | (a) $0, 2, 5, 7, 3$; (b) $(0, 3)$; (c) at $x = 3$; (d) sketch |
| [[CAL1 HW 4.3 Questions#ST 4.3.5\|ST 4.3.5]] | (a) $g(x) = 3x$; (b) $g'(x) = 3 = f(x)$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.9\|ST 4.3.9]] | $g'(x) = \sqrt{x + x^3}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.11\|ST 4.3.11]] | $g'(w) = \sin(1 + w^3)$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.13\|ST 4.3.13]] | $F'(x) = -\sqrt{1 + \sec x}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.15\|ST 4.3.15]] | $h'(x) = -\dfrac{\sin^4(1/x)}{x^2}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.17\|ST 4.3.17]] | $y' = \dfrac{3(3x + 2)}{1 + (3x + 2)^3}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.19\|ST 4.3.19]] | $y' = -\tfrac{1}{2}\tan\sqrt{x}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.21\|ST 4.3.21]] | $\tfrac{15}{4} = 4 - \tfrac{1}{4}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.27\|ST 4.3.27]] | $2$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.31\|ST 4.3.31]] | $\tfrac{512}{15}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.37\|ST 4.3.37]] | $\tfrac{82}{5}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.41\|ST 4.3.41]] | $1$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.43\|ST 4.3.43]] | $\tfrac{15}{4}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.45\|ST 4.3.45]] | $0$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.47\|ST 4.3.47]] | $\tfrac{16}{3}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.49\|ST 4.3.49]] | $\tfrac{32}{3}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.59\|ST 4.3.59]] | $g'(x) = \dfrac{3(9x^2 - 1)}{9x^2 + 1} - \dfrac{2(4x^2 - 1)}{4x^2 + 1}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.60\|ST 4.3.60]] | $g'(x) = 2(1 + 2x)\sin(1 + 2x) + 2(1 - 2x)\sin(1 - 2x)$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.61\|ST 4.3.61]] | $h'(x) = 3x^2\cos(x^6) - \dfrac{\cos x}{2\sqrt{x}}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.62\|ST 4.3.62]] | $g'(x) = \dfrac{2x}{\sqrt{2 + x^8}} - \dfrac{\sec^2 x}{\sqrt{2 + \tan^4 x}}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.63\|ST 4.3.63]] | $y = -\dfrac{x}{\pi} + 1$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.65\|ST 4.3.65]] | $(-4, 0)$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.67\|ST 4.3.67]] | $f(4) = 29$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.68\|ST 4.3.68]] | $\dfrac{\sqrt{15}}{4}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.73\|ST 4.3.73]] | $\int_0^1 (x^4 + x)\,dx = \tfrac{7}{10}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.74\|ST 4.3.74]] | $\int_0^1 \sqrt{x}\,dx = \tfrac{2}{3}$ |
| [[CAL1 HW 4.3 Questions#ST 4.3.81\|ST 4.3.81]] | $f(x) = x^{3/2}$, $a = 9$ |

## ST §4.3 The Fundamental Theorem of Calculus

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Fundamental Theorem of Calculus]], Part 1 (FTC1)**: if $f$ is continuous on $[a, b]$, then $g(x) = \int_a^x f(t)\,dt$ is continuous on $[a, b]$ and differentiable on $(a, b)$, and $g'(x) = f(x)$.
> - **FTC1 with the [[Chain Rule]]**: if $f$ is continuous and $u$ is differentiable, then $\dfrac{d}{dx}\int_a^{u(x)} f(t)\,dt = f(u(x))\,u'(x)$.
> - **Variable in the lower limit**: $\int_{v(x)}^{a} f(t)\,dt = -\int_a^{v(x)} f(t)\,dt$. With both limits variable, split at a constant $a$: $\int_{v(x)}^{u(x)} f(t)\,dt = \int_a^{u(x)} f(t)\,dt - \int_a^{v(x)} f(t)\,dt$, so its derivative is $f(u(x))\,u'(x) - f(v(x))\,v'(x)$.
> - **Fundamental Theorem of Calculus, Part 2 (FTC2)**: if $f$ is continuous on $[a, b]$ and $F' = f$ (an [[Antiderivative]]), then $\int_a^b f(x)\,dx = F(b) - F(a)$, written $F(x)\Big]_a^b$.
> - **Antiderivatives**: $x^n \to \dfrac{x^{n+1}}{n+1}$ ($n \ne -1$), $\sin x \to -\cos x$, $\cos x \to \sin x$, $\sec x\tan x \to \sec x$; constants come out, and sums go term by term.
> - **Net area**: $\int_a^b f(x)\,dx = A_1 - A_2$, the area above the $x$-axis minus the area below it.
> - **[[Riemann Sum]] on $[0, 1]$ with right endpoints**: $\Delta x = \tfrac{1}{n}$, $x_i = \tfrac{i}{n}$, and $\lim_{n \to \infty} \sum_{i=1}^{n} f\big(\tfrac{i}{n}\big)\tfrac{1}{n} = \int_0^1 f(x)\,dx$ for continuous $f$.
> - **Shape of $g$ from $g' = f$**: $g$ increases where $f > 0$ ([[Increasing and Decreasing Test]]), has a local maximum where $f$ changes from $+$ to $-$ ([[First Derivative Test]]), and is concave downward where $g'' < 0$ ([[Concavity]]).
> - Each answer is written as on an exam paper: the computation first, then the conclusion on a Hence line. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 4.3.3
Question: [[CAL1 HW 4.3 Questions#ST 4.3.3|ST 4.3.3]]

> [!solution] Solution
> ![ST 4.3.3 figure|440](../Attachments/CAL1%20HW%204.3%20Solutions%20fig%203.png)
>
> $g(x)$ is the net area under $f$ from $0$ to $x$.
>
> **(a)**
> $$
> \begin{aligned}
> g(0) &= \int_0^0 f(t)\,dt = 0 \\
> g(1) &= 1 \cdot 2 = 2 && \text{(rectangle)} \\
> g(2) &= g(1) + \frac{2 + 4}{2} \cdot 1 = 2 + 3 = 5 && \text{(trapezoid)} \\
> g(3) &= g(2) + \frac{1}{2} \cdot 1 \cdot 4 = 5 + 2 = 7 && \text{(triangle)} \\
> g(6) &= g(3) - \frac{1}{2} \cdot 2 \cdot 2 - 1 \cdot 2 = 7 - 2 - 2 = 3 && \text{(below the axis)}
> \end{aligned}
> $$
>
> **(b)** $f$ is continuous, so $g'(x) = f(x)$ by FTC1.
> $$
> g'(x) = f(x) > 0 \quad \text{for } 0 < x < 3
> $$
> Hence $g$ is increasing on $(0, 3)$.
>
> **(c)** $g' = f > 0$ on $(0, 3)$ and $g' = f < 0$ on $(3, 7)$: $g$ increases up to $x = 3$ and decreases after it. Hence $g$ has its maximum value at $x = 3$, namely $g(3) = 7$.
>
> **(d)**
>
> ![ST 4.3.3 (d) figure|400](../Attachments/CAL1%20HW%204.3%20Solutions%20fig%203d.png)
>
> \# For the sketch, two more values help: $g(5) = 7 - 2 = 5$ and $g(7) = 3 - \tfrac{1}{2} \cdot 1 \cdot 2 = 2$. The shape comes from $g' = f$: where $f$ is constant ($0 < x < 1$ and $5 < x < 6$) $g$ is a straight line of slope $2$ or $-2$; where $f$ increases, $g'' = f' > 0$ and $g$ is concave upward ($1 < x < 2$ and $6 < x < 7$); where $f$ decreases ($2 < x < 5$), $g$ is concave downward. The top of $g$ is where $f$ crosses the axis, not where $f$ is highest: at $x = 2$ the area is still growing fastest.

### ST 4.3.5
Question: [[CAL1 HW 4.3 Questions#ST 4.3.5|ST 4.3.5]]

> [!solution] Solution
> ![ST 4.3.5 figure|400](../Attachments/CAL1%20HW%204.3%20Solutions%20fig%205.png)
>
> **(a)** The region is a rectangle of width $x$ and height $3$:
> $$
> g(x) = 3 \cdot x = 3x
> $$
>
> **(b)**
> $$
> g'(x) = \frac{d}{dx}(3x) = 3 = f(x)
> $$
> Hence $g$ is an antiderivative of $f$. This is what FTC1 says: $f(t) = 3$ is continuous, so $\dfrac{d}{dx}\int_0^x f(t)\,dt = f(x) = 3$.
>
> \# The idea of FTC1 in this picture: moving the right edge from $x$ to $x + h$ adds a strip of width $h$ and height $f(x) = 3$, so the area grows at the rate $3$, the height of $f$ at the moving edge.

### ST 4.3.9
Question: [[CAL1 HW 4.3 Questions#ST 4.3.9|ST 4.3.9]]

> [!solution] Solution
> $f(t) = \sqrt{t + t^3}$ is continuous on $[0, \infty)$ ($t + t^3 \ge 0$ there), so by FTC1
> $$
> g'(x) = \sqrt{x + x^3}.
> $$
>
> \# The lower limit is the constant $0$ and the upper limit is just $x$: replace $t$ by $x$ in the integrand. Nothing has to be integrated.

### ST 4.3.11
Question: [[CAL1 HW 4.3 Questions#ST 4.3.11|ST 4.3.11]]

> [!solution] Solution
> $f(t) = \sin(1 + t^3)$ is continuous on $\mathbb{R}$, so by FTC1
> $$
> g'(w) = \sin(1 + w^3).
> $$

### ST 4.3.13
Question: [[CAL1 HW 4.3 Questions#ST 4.3.13|ST 4.3.13]]

> [!solution] Solution
> $$
> F(x) = \int_x^0 \sqrt{1 + \sec t}\,dt = -\int_0^x \sqrt{1 + \sec t}\,dt
> $$
> $f(t) = \sqrt{1 + \sec t}$ is continuous on $(-\tfrac{\pi}{2}, \tfrac{\pi}{2})$ ($\sec t \ge 1$ there), so for $x$ in this interval FTC1 gives
> $$
> F'(x) = -\sqrt{1 + \sec x}.
> $$
>
> \# FTC1 is about $\int_a^x$, with $x$ on top. Here $x$ is the lower limit, so swap the limits first; that is where the minus sign comes from.

### ST 4.3.15
Question: [[CAL1 HW 4.3 Questions#ST 4.3.15|ST 4.3.15]]

> [!solution] Solution
> Let $u = \dfrac{1}{x}$, so $h(x) = \int_2^u \sin^4 t\,dt$ and $\dfrac{du}{dx} = -\dfrac{1}{x^2}$. $\sin^4 t$ is continuous on $\mathbb{R}$, so by FTC1 and the Chain Rule
> $$
> h'(x) = \frac{d}{du}\left[\int_2^u \sin^4 t\,dt\right]\frac{du}{dx} = \sin^4 u \cdot \Big(-\frac{1}{x^2}\Big) = -\frac{\sin^4(1/x)}{x^2}.
> $$
>
> \# FTC1 differentiates with respect to the upper limit $u$; since $u$ is a function of $x$, the Chain Rule multiplies by $u'(x)$. Forgetting the factor $-\tfrac{1}{x^2}$ is the usual mistake.

### ST 4.3.17
Question: [[CAL1 HW 4.3 Questions#ST 4.3.17|ST 4.3.17]]

> [!solution] Solution
> Let $u = 3x + 2$, so $\dfrac{du}{dx} = 3$. $\dfrac{t}{1 + t^3}$ is continuous on $(-1, \infty)$ ($1 + t^3 > 0$ there), which contains $1$ and $3x + 2$ when $x > -1$. By FTC1 and the Chain Rule,
> $$
> y' = \frac{u}{1 + u^3} \cdot \frac{du}{dx} = \frac{3x + 2}{1 + (3x + 2)^3} \cdot 3 = \frac{3(3x + 2)}{1 + (3x + 2)^3}.
> $$
>
> \# The condition $x > -1$ keeps the whole interval of integration away from $t = -1$, where $1 + t^3 = 0$.

### ST 4.3.19
Question: [[CAL1 HW 4.3 Questions#ST 4.3.19|ST 4.3.19]]

> [!solution] Solution
> $$
> y = \int_{\sqrt{x}}^{\pi/4} \theta\tan\theta\,d\theta = -\int_{\pi/4}^{\sqrt{x}} \theta\tan\theta\,d\theta
> $$
> Let $u = \sqrt{x}$, so $\dfrac{du}{dx} = \dfrac{1}{2\sqrt{x}}$. $\theta\tan\theta$ is continuous on $(-\tfrac{\pi}{2}, \tfrac{\pi}{2})$, which contains $\tfrac{\pi}{4}$ and $\sqrt{x}$ when $0 < x < \tfrac{\pi^2}{4}$. By FTC1 and the Chain Rule,
> $$
> y' = -u\tan u \cdot \frac{du}{dx} = -\sqrt{x}\tan\sqrt{x} \cdot \frac{1}{2\sqrt{x}} = -\frac{1}{2}\tan\sqrt{x}.
> $$
>
> \# Two steps from the Note in a row: swap the limits (minus sign), then the Chain Rule for $u = \sqrt{x}$. The $\sqrt{x}$ from the integrand cancels the $\sqrt{x}$ from $u'$.

### ST 4.3.21
Question: [[CAL1 HW 4.3 Questions#ST 4.3.21|ST 4.3.21]]

> [!solution] Solution
> $x^3$ is continuous and $\big(\tfrac{x^4}{4}\big)' = x^3$, so by FTC2
> $$
> \int_{-1}^{2} x^3\,dx = \frac{x^4}{4}\Big]_{-1}^{2} = \frac{16}{4} - \frac{1}{4} = \frac{15}{4}.
> $$
>
> ![ST 4.3.21 figure|300](../Attachments/CAL1%20HW%204.3%20Solutions%20fig%2021.png)
>
> $x^3 \ge 0$ on $[0, 2]$ and $x^3 \le 0$ on $[-1, 0]$:
> $$
> A_1 = \int_0^2 x^3\,dx = \frac{16}{4} - 0 = 4, \qquad A_2 = -\int_{-1}^{0} x^3\,dx = -\Big(0 - \frac{1}{4}\Big) = \frac{1}{4}
> $$
> Hence $\int_{-1}^{2} x^3\,dx = A_1 - A_2 = 4 - \tfrac{1}{4} = \tfrac{15}{4}$: the area above the $x$-axis minus the area below it.

### ST 4.3.27
Question: [[CAL1 HW 4.3 Questions#ST 4.3.27|ST 4.3.27]]

> [!solution] Solution
> $$
> \begin{aligned}
> \int_0^2 \left(\tfrac{4}{5}t^3 - \tfrac{3}{4}t^2 + \tfrac{2}{5}t\right) dt &= \left[\frac{t^4}{5} - \frac{t^3}{4} + \frac{t^2}{5}\right]_0^2 \\
> &= \Big(\frac{16}{5} - \frac{8}{4} + \frac{4}{5}\Big) - 0 = 4 - 2 = 2
> \end{aligned}
> $$
> Hence the integral is $2$.
>
> \# Term by term: $\tfrac{4}{5} \cdot \tfrac{t^4}{4} = \tfrac{t^4}{5}$, $\tfrac{3}{4} \cdot \tfrac{t^3}{3} = \tfrac{t^3}{4}$, $\tfrac{2}{5} \cdot \tfrac{t^2}{2} = \tfrac{t^2}{5}$. A polynomial is continuous everywhere, so FTC2 applies.

### ST 4.3.31
Question: [[CAL1 HW 4.3 Questions#ST 4.3.31|ST 4.3.31]]

> [!solution] Solution
> $$
> \begin{aligned}
> \int_0^4 (t^2 + t^{3/2})\,dt &= \left[\frac{t^3}{3} + \frac{2}{5}t^{5/2}\right]_0^4 \\
> &= \frac{64}{3} + \frac{2}{5} \cdot 32 = \frac{64}{3} + \frac{64}{5} = \frac{320 + 192}{15} = \frac{512}{15}
> \end{aligned}
> $$
> Hence the integral is $\tfrac{512}{15}$.
>
> \# $t^{3/2} \to \dfrac{t^{5/2}}{5/2} = \tfrac{2}{5}t^{5/2}$, and $4^{5/2} = (\sqrt{4})^5 = 32$.

### ST 4.3.37
Question: [[CAL1 HW 4.3 Questions#ST 4.3.37|ST 4.3.37]]

> [!solution] Solution
> $$
> \begin{aligned}
> \int_1^4 \frac{2 + x^2}{\sqrt{x}}\,dx &= \int_1^4 (2x^{-1/2} + x^{3/2})\,dx = \left[4x^{1/2} + \frac{2}{5}x^{5/2}\right]_1^4 \\
> &= \Big(8 + \frac{64}{5}\Big) - \Big(4 + \frac{2}{5}\Big) = 4 + \frac{62}{5} = \frac{82}{5}
> \end{aligned}
> $$
> Hence the integral is $\tfrac{82}{5}$.
>
> \# There is no quotient rule for integrals: divide each term by $\sqrt{x} = x^{1/2}$ first, then use the power rule. $\tfrac{2 + x^2}{\sqrt{x}}$ is continuous on $[1, 4]$ because $x > 0$ there.

### ST 4.3.41
Question: [[CAL1 HW 4.3 Questions#ST 4.3.41|ST 4.3.41]]

> [!solution] Solution
> $(\sec\theta)' = \sec\theta\tan\theta$, which is continuous on $[0, \tfrac{\pi}{3}]$. By FTC2
> $$
> \int_0^{\pi/3} \sec\theta\tan\theta\,d\theta = \sec\theta\Big]_0^{\pi/3} = \sec\frac{\pi}{3} - \sec 0 = 2 - 1 = 1.
> $$
>
> \# $\sec\tfrac{\pi}{3} = \dfrac{1}{\cos(\pi/3)} = \dfrac{1}{1/2} = 2$.

### ST 4.3.43
Question: [[CAL1 HW 4.3 Questions#ST 4.3.43|ST 4.3.43]]

> [!solution] Solution
> $$
> \begin{aligned}
> \int_0^1 (1 + r)^3\,dr &= \int_0^1 (1 + 3r + 3r^2 + r^3)\,dr = \left[r + \frac{3r^2}{2} + r^3 + \frac{r^4}{4}\right]_0^1 \\
> &= 1 + \frac{3}{2} + 1 + \frac{1}{4} = \frac{15}{4}
> \end{aligned}
> $$
> Hence the integral is $\tfrac{15}{4}$.
>
> \# A shorter way: $\Big(\dfrac{(1 + r)^4}{4}\Big)' = (1 + r)^3$ by the Chain Rule (the inside $1 + r$ has derivative $1$), so the integral is $\dfrac{(1 + r)^4}{4}\Big]_0^1 = \dfrac{16}{4} - \dfrac{1}{4} = \dfrac{15}{4}$. Differentiating the answer is always a quick check of an antiderivative.

### ST 4.3.45
Question: [[CAL1 HW 4.3 Questions#ST 4.3.45|ST 4.3.45]]

> [!solution] Solution
> Split at $\tfrac{\pi}{2}$, where the formula for $f$ changes:
> $$
> \begin{aligned}
> \int_0^\pi f(x)\,dx &= \int_0^{\pi/2} \sin x\,dx + \int_{\pi/2}^{\pi} \cos x\,dx = \Big[-\cos x\Big]_0^{\pi/2} + \Big[\sin x\Big]_{\pi/2}^{\pi} \\
> &= (0 + 1) + (0 - 1) = 0
> \end{aligned}
> $$
> Hence $\int_0^\pi f(x)\,dx = 0$.
>
> \# On $[0, \tfrac{\pi}{2}]$, $f$ equals $\sin x$ except at the single point $\tfrac{\pi}{2}$, and changing one value does not change an integral, so FTC2 can be used on each piece. The answer $0$ means the area under $\sin x$ on $[0, \tfrac{\pi}{2}]$ (which is $1$) equals the area between $\cos x$ and the axis on $[\tfrac{\pi}{2}, \pi]$, which lies below the axis.

### ST 4.3.47
Question: [[CAL1 HW 4.3 Questions#ST 4.3.47|ST 4.3.47]]

> [!solution] Solution
> ![ST 4.3.47 figure|400](../Attachments/CAL1%20HW%204.3%20Solutions%20fig%2047.png)
>
> $\sqrt{x} \ge 0$ on $[0, 4]$ and meets $y = 0$ at $x = 0$, so the region lies under $y = \sqrt{x}$ for $0 \le x \le 4$:
> $$
> A = \int_0^4 \sqrt{x}\,dx = \frac{2}{3}x^{3/2}\Big]_0^4 = \frac{2}{3} \cdot 8 - 0 = \frac{16}{3}
> $$
> Hence the area is $\tfrac{16}{3}$.

### ST 4.3.49
Question: [[CAL1 HW 4.3 Questions#ST 4.3.49|ST 4.3.49]]

> [!solution] Solution
> ![ST 4.3.49 figure|360](../Attachments/CAL1%20HW%204.3%20Solutions%20fig%2049.png)
>
> $4 - x^2 = 0 \iff x = \pm 2$, and $4 - x^2 \ge 0$ on $[-2, 2]$:
> $$
> \begin{aligned}
> A &= \int_{-2}^{2} (4 - x^2)\,dx = \left[4x - \frac{x^3}{3}\right]_{-2}^{2} \\
> &= \Big(8 - \frac{8}{3}\Big) - \Big(-8 + \frac{8}{3}\Big) = 16 - \frac{16}{3} = \frac{32}{3}
> \end{aligned}
> $$
> Hence the area is $\tfrac{32}{3}$.
>
> \# The curves give no $x$-interval, so first find where they meet: those $x$ are the limits of integration.

### ST 4.3.59
Question: [[CAL1 HW 4.3 Questions#ST 4.3.59|ST 4.3.59]]

> [!solution] Solution
> $f(u) = \dfrac{u^2 - 1}{u^2 + 1}$ is continuous on $\mathbb{R}$ ($u^2 + 1 > 0$). Split at $0$:
> $$
> g(x) = \int_{2x}^{0} f(u)\,du + \int_0^{3x} f(u)\,du = -\int_0^{2x} f(u)\,du + \int_0^{3x} f(u)\,du
> $$
> By FTC1 and the Chain Rule,
> $$
> g'(x) = -f(2x) \cdot 2 + f(3x) \cdot 3 = \frac{3(9x^2 - 1)}{9x^2 + 1} - \frac{2(4x^2 - 1)}{4x^2 + 1}.
> $$
>
> \# Splitting at a constant puts $x$ only in upper limits, where FTC1 works. $f(2x) = \dfrac{(2x)^2 - 1}{(2x)^2 + 1} = \dfrac{4x^2 - 1}{4x^2 + 1}$, and the factor $2$ is the derivative of $2x$. Pattern to remember: $f(\text{top}) \cdot (\text{top})' - f(\text{bottom}) \cdot (\text{bottom})'$. Exercises 60–62 use the same pattern.

### ST 4.3.60
Question: [[CAL1 HW 4.3 Questions#ST 4.3.60|ST 4.3.60]]

> [!solution] Solution
> $t\sin t$ is continuous on $\mathbb{R}$, so
> $$
> \begin{aligned}
> &g(x) = -\int_0^{1-2x} t\sin t\,dt + \int_0^{1+2x} t\sin t\,dt \\
> &g'(x) = -(1 - 2x)\sin(1 - 2x) \cdot (-2) + (1 + 2x)\sin(1 + 2x) \cdot 2 \\
> &\hphantom{g'(x)} = 2(1 + 2x)\sin(1 + 2x) + 2(1 - 2x)\sin(1 - 2x)
> \end{aligned}
> $$
>
> \# The derivative of the lower limit $1 - 2x$ is $-2$; together with the minus sign in front, the second term is added.

### ST 4.3.61
Question: [[CAL1 HW 4.3 Questions#ST 4.3.61|ST 4.3.61]]

> [!solution] Solution
> $\cos(t^2)$ is continuous on $\mathbb{R}$. For $x > 0$,
> $$
> \begin{aligned}
> &h(x) = -\int_0^{\sqrt{x}} \cos(t^2)\,dt + \int_0^{x^3} \cos(t^2)\,dt \\
> &h'(x) = -\cos\big((\sqrt{x})^2\big) \cdot \frac{1}{2\sqrt{x}} + \cos\big((x^3)^2\big) \cdot 3x^2 = 3x^2\cos(x^6) - \frac{\cos x}{2\sqrt{x}}
> \end{aligned}
> $$
>
> \# $x > 0$ because $\sqrt{x}$ is differentiable only there. Put the whole limit into $t^2$: $(\sqrt{x})^2 = x$ and $(x^3)^2 = x^6$.

### ST 4.3.62
Question: [[CAL1 HW 4.3 Questions#ST 4.3.62|ST 4.3.62]]

> [!solution] Solution
> $\dfrac{1}{\sqrt{2 + t^4}}$ is continuous on $\mathbb{R}$ ($2 + t^4 > 0$), so
> $$
> \begin{aligned}
> &g(x) = -\int_0^{\tan x} \frac{dt}{\sqrt{2 + t^4}} + \int_0^{x^2} \frac{dt}{\sqrt{2 + t^4}} \\
> &g'(x) = -\frac{1}{\sqrt{2 + \tan^4 x}} \cdot \sec^2 x + \frac{1}{\sqrt{2 + (x^2)^4}} \cdot 2x = \frac{2x}{\sqrt{2 + x^8}} - \frac{\sec^2 x}{\sqrt{2 + \tan^4 x}}
> \end{aligned}
> $$
> where $x \ne \tfrac{\pi}{2} + k\pi$, so that $\tan x$ is defined.

### ST 4.3.63
Question: [[CAL1 HW 4.3 Questions#ST 4.3.63|ST 4.3.63]]

> [!solution] Solution
> $\dfrac{\cos t}{t}$ is continuous on $(0, \infty)$, which contains $\pi$, so for $x > 0$ FTC1 gives $F'(x) = \dfrac{\cos x}{x}$.
> $$
> \begin{aligned}
> &F(\pi) = \int_\pi^\pi \frac{\cos t}{t}\,dt = 0, \qquad F'(\pi) = \frac{\cos\pi}{\pi} = -\frac{1}{\pi} \\
> &y - 0 = -\frac{1}{\pi}(x - \pi) \implies y = -\frac{x}{\pi} + 1
> \end{aligned}
> $$
> Hence the tangent line is $y = -\dfrac{x}{\pi} + 1$.
>
> \# A tangent line needs a point and a slope. The point is free because the limits are equal at $x = \pi$; the slope comes from FTC1. $\int \tfrac{\cos t}{t}\,dt$ has no elementary formula, and none is needed.

### ST 4.3.65
Question: [[CAL1 HW 4.3 Questions#ST 4.3.65|ST 4.3.65]]

> [!solution] Solution
> $t^2 + t + 2 = \big(t + \tfrac{1}{2}\big)^2 + \tfrac{7}{4} > 0$, so $\dfrac{t^2}{t^2 + t + 2}$ is continuous on $\mathbb{R}$, and by FTC1
> $$
> \begin{aligned}
> y' &= \frac{x^2}{x^2 + x + 2} \\
> y'' &= \frac{2x(x^2 + x + 2) - x^2(2x + 1)}{(x^2 + x + 2)^2} = \frac{x^2 + 4x}{(x^2 + x + 2)^2} = \frac{x(x + 4)}{(x^2 + x + 2)^2}
> \end{aligned}
> $$
> The denominator is positive, so $y'' < 0 \iff x(x + 4) < 0 \iff -4 < x < 0$.
>
> Hence the curve is concave downward on $(-4, 0)$.
>
> \# FTC1 turns the integral into $y'$ for free; concavity then needs one more derivative, by the Quotient Rule. Numerator: $2x^3 + 2x^2 + 4x - 2x^3 - x^2 = x^2 + 4x$. Sign of $x(x + 4)$: negative only between its roots $-4$ and $0$.

### ST 4.3.67
Question: [[CAL1 HW 4.3 Questions#ST 4.3.67|ST 4.3.67]]

> [!solution] Solution
> $f'$ is continuous and $f$ is an antiderivative of $f'$, so by FTC2
> $$
> \int_1^4 f'(x)\,dx = f(4) - f(1) \implies 17 = f(4) - 12 \implies f(4) = 29.
> $$
> Hence $f(4) = 29$.
>
> \# Integrating a rate of change gives the total change: $f$ goes up by $17$ from $x = 1$ to $x = 4$, starting at $12$. The hypothesis "$f'$ is continuous" is exactly what FTC2 needs.

### ST 4.3.68
Question: [[CAL1 HW 4.3 Questions#ST 4.3.68|ST 4.3.68]]

> [!solution] Solution
> $\sqrt{1 + t^2}$ is continuous on $\mathbb{R}$, so by FTC1 and the Chain Rule
> $$
> f'(x) = \sqrt{1 + \sin^2 x}\,\cos x.
> $$
> $f$ is differentiable, hence continuous, so by FTC1 $g'(y) = f(y)$ and $g''(y) = f'(y)$:
> $$
> g''\Big(\frac{\pi}{6}\Big) = f'\Big(\frac{\pi}{6}\Big) = \sqrt{1 + \frac{1}{4}} \cdot \frac{\sqrt{3}}{2} = \frac{\sqrt{5}}{2} \cdot \frac{\sqrt{3}}{2} = \frac{\sqrt{15}}{4}
> $$
> Hence $g''(\pi/6) = \dfrac{\sqrt{15}}{4}$.
>
> \# Two layers. $g$ is the area function of $f$, so $g' = f$ and $g'' = f'$. Then $f$ is itself an area function with upper limit $\sin x$, so $f'$ needs the Chain Rule factor $\cos x$. Values: $\sin\tfrac{\pi}{6} = \tfrac{1}{2}$, $\cos\tfrac{\pi}{6} = \tfrac{\sqrt{3}}{2}$.

### ST 4.3.73
Question: [[CAL1 HW 4.3 Questions#ST 4.3.73|ST 4.3.73]]

> [!solution] Solution
> $$
> \sum_{i=1}^{n} \left(\frac{i^4}{n^5} + \frac{i}{n^2}\right) = \sum_{i=1}^{n} \left[\Big(\frac{i}{n}\Big)^4 + \frac{i}{n}\right]\frac{1}{n}
> $$
> This is $\sum f(x_i)\,\Delta x$ with $f(x) = x^4 + x$ on $[0, 1]$, $\Delta x = \tfrac{1}{n}$, $x_i = \tfrac{i}{n}$. $f$ is continuous, so
> $$
> \lim_{n \to \infty} \sum_{i=1}^{n} \left(\frac{i^4}{n^5} + \frac{i}{n^2}\right) = \int_0^1 (x^4 + x)\,dx = \left[\frac{x^5}{5} + \frac{x^2}{2}\right]_0^1 = \frac{1}{5} + \frac{1}{2} = \frac{7}{10}.
> $$
>
> \# Pull one $\tfrac{1}{n}$ out of each term: $\tfrac{i^4}{n^5} = \big(\tfrac{i}{n}\big)^4 \cdot \tfrac{1}{n}$ and $\tfrac{i}{n^2} = \tfrac{i}{n} \cdot \tfrac{1}{n}$. What is left is $f$ at $x_i = \tfrac{i}{n}$. The integral replaces the long limit computation of §4.2.

### ST 4.3.74
Question: [[CAL1 HW 4.3 Questions#ST 4.3.74|ST 4.3.74]]

> [!solution] Solution
> $$
> \frac{1}{n}\left(\sqrt{\frac{1}{n}} + \sqrt{\frac{2}{n}} + \cdots + \sqrt{\frac{n}{n}}\right) = \sum_{i=1}^{n} \sqrt{\frac{i}{n}} \cdot \frac{1}{n}
> $$
> This is $\sum f(x_i)\,\Delta x$ with $f(x) = \sqrt{x}$ on $[0, 1]$, $\Delta x = \tfrac{1}{n}$, $x_i = \tfrac{i}{n}$. $f$ is continuous on $[0, 1]$, so
> $$
> \lim_{n \to \infty} \frac{1}{n}\left(\sqrt{\frac{1}{n}} + \cdots + \sqrt{\frac{n}{n}}\right) = \int_0^1 \sqrt{x}\,dx = \frac{2}{3}x^{3/2}\Big]_0^1 = \frac{2}{3}.
> $$

### ST 4.3.81
Question: [[CAL1 HW 4.3 Questions#ST 4.3.81|ST 4.3.81]]

> [!solution] Solution
> Differentiate both sides (FTC1, with $\tfrac{f(t)}{t^2}$ continuous):
> $$
> \frac{f(x)}{x^2} = \frac{1}{\sqrt{x}} \implies f(x) = \frac{x^2}{\sqrt{x}} = x^{3/2}
> $$
> Put $x = a$: the integral $\int_a^a$ is $0$, so
> $$
> 6 + 0 = 2\sqrt{a} \implies \sqrt{a} = 3 \implies a = 9
> $$
> Check, by FTC2 ($t^{-1/2}$ is continuous on $(0, \infty)$):
> $$
> 6 + \int_9^x \frac{t^{3/2}}{t^2}\,dt = 6 + \int_9^x t^{-1/2}\,dt = 6 + 2\sqrt{t}\Big]_9^x = 6 + 2\sqrt{x} - 6 = 2\sqrt{x}
> $$
> Hence $f(x) = x^{3/2}$ and $a = 9$.
>
> \# Two unknowns, two tools: the derivative removes the integral and gives $f$; the choice $x = a$ makes the integral $0$ and gives $a$. The check is needed because differentiating an equation can lose a constant.
