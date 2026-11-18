---
course: [CAL1]
semester: "115-1"
chapter: ["4.4"]
tags: [calculus, homework, solutions, integrals]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §4.4, pp. 339-344, scanned PDF (indefinite integrals, Table 1, FTC2, the Net Change Theorem, displacement and distance)"
created: 2026-11-18
questions: "[[CAL1 HW 4.4 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 4.4 Questions#ST 4.4.13\|ST 4.4.13]] | $\tfrac{2}{3}u^3 + \tfrac{9}{2}u^2 + 4u + C$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.14\|ST 4.4.14]] | $\tfrac{2}{7}t^{7/2} + \tfrac{6}{5}t^{5/2} + \tfrac{4}{3}t^{3/2} + C$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.15\|ST 4.4.15]] | $2\sqrt{x} + x + \tfrac{2}{3}x^{3/2} + C$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.16\|ST 4.4.16]] | $\tfrac{1}{3}u^3 + u - \tfrac{1}{u} + C$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.17\|ST 4.4.17]] | $\theta + \tan\theta + C$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.18\|ST 4.4.18]] | $\tan t + \sec t + C$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.19\|ST 4.4.19]] | $-3\cot t + C$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.20\|ST 4.4.20]] | $2\sin x + C$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.27\|ST 4.4.27]] | $-2$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.29\|ST 4.4.29]] | $8$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.31\|ST 4.4.31]] | $36$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.35\|ST 4.4.35]] | $\tfrac{55}{63}$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.39\|ST 4.4.39]] | $1 + \tfrac{\pi}{4}$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.41\|ST 4.4.41]] | $\tfrac{659456}{55} \approx 11990.1$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.43\|ST 4.4.43]] | $\tfrac{5}{2}$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.45\|ST 4.4.45]] | $-\tfrac{7}{2}$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.49\|ST 4.4.49]] | $\tfrac{4}{3}$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.50\|ST 4.4.50]] | $\tfrac{1}{5}$ |
| [[CAL1 HW 4.4 Questions#ST 4.4.61\|ST 4.4.61]] | (a) $-\tfrac{3}{2}$ m; (b) $\tfrac{41}{6}$ m |
| [[CAL1 HW 4.4 Questions#ST 4.4.63\|ST 4.4.63]] | (a) $v(t) = \tfrac{1}{2}t^2 + 4t + 5$ m/s; (b) $\tfrac{1250}{3} \approx 416.7$ m |

## ST §4.4 Indefinite Integrals and the Net Change Theorem

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Indefinite Integral]]**: $\int f(x)\,dx = F(x)$ means $F'(x) = f(x)$. A general indefinite integral $F(x) + C$ is meant on one interval (the convention of the section), so where the integrand is undefined at some points, the answer holds on each interval between them.
> - **Table of indefinite integrals** (the derivative table read backwards):
>
> | Integral | Value |
> | --- | --- |
> | $\int cf(x)\,dx$ | $c\int f(x)\,dx$ |
> | $\int [f(x) + g(x)]\,dx$ | $\int f(x)\,dx + \int g(x)\,dx$ |
> | $\int k\,dx$ | $kx + C$ |
> | $\int x^n\,dx$, $n \ne -1$ | $\dfrac{x^{n+1}}{n+1} + C$ |
> | $\int \sin x\,dx$ | $-\cos x + C$ |
> | $\int \cos x\,dx$ | $\sin x + C$ |
> | $\int \sec^2 x\,dx$ | $\tan x + C$ |
> | $\int \csc^2 x\,dx$ | $-\cot x + C$ |
> | $\int \sec x \tan x\,dx$ | $\sec x + C$ |
> | $\int \csc x \cot x\,dx$ | $-\csc x + C$ |
>
> - **[[Fundamental Theorem of Calculus]], Part 2**: if $f$ is continuous on $[a, b]$ and $F$ is any antiderivative of $f$, then $\int_a^b f(x)\,dx = F(b) - F(a) = \Big[F(x)\Big]_a^b$.
> - **[[Net Change Theorem]]**: $\int_a^b F'(x)\,dx = F(b) - F(a)$. For a particle with velocity $v(t) = s'(t)$: the *displacement* from $t_1$ to $t_2$ is $\int_{t_1}^{t_2} v(t)\,dt = s(t_2) - s(t_1)$, and the *total distance traveled* is $\int_{t_1}^{t_2} \lvert v(t) \rvert\,dt$. Also $v'(t) = a(t)$, so $v$ is an antiderivative of $a$.
> - **Identities**: $1 + \tan^2\theta = \sec^2\theta$, $\sin 2x = 2\sin x\cos x$.
> - **Absolute value**: $\lvert g(x) \rvert = g(x)$ where $g(x) \ge 0$ and $-g(x)$ where $g(x) \le 0$; split the integral at the points where $g$ changes sign.
> - Each answer is written as on an exam paper: rewrite the integrand as a sum of powers or table entries, integrate term by term, then the conclusion on a Hence line. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 4.4.13
Question: [[CAL1 HW 4.4 Questions#ST 4.4.13|ST 4.4.13]]

> [!solution] Solution
> $$
> \begin{aligned}
> \int (u + 4)(2u + 1)\,du &= \int (2u^2 + 9u + 4)\,du \\
> &= 2 \cdot \frac{u^3}{3} + 9 \cdot \frac{u^2}{2} + 4u + C
> \end{aligned}
> $$
> Hence $\int (u + 4)(2u + 1)\,du = \tfrac{2}{3}u^3 + \tfrac{9}{2}u^2 + 4u + C$.
>
> \# Expand first: there is no product rule for integrals, and $\int fg\,du \ne \int f\,du \cdot \int g\,du$. $(u + 4)(2u + 1) = 2u^2 + u + 8u + 4$.

### ST 4.4.14
Question: [[CAL1 HW 4.4 Questions#ST 4.4.14|ST 4.4.14]]

> [!solution] Solution
> $$
> \begin{aligned}
> \int \sqrt{t}\,(t^2 + 3t + 2)\,dt &= \int \left(t^{5/2} + 3t^{3/2} + 2t^{1/2}\right)dt \\
> &= \frac{t^{7/2}}{7/2} + 3 \cdot \frac{t^{5/2}}{5/2} + 2 \cdot \frac{t^{3/2}}{3/2} + C
> \end{aligned}
> $$
> Hence $\int \sqrt{t}\,(t^2 + 3t + 2)\,dt = \tfrac{2}{7}t^{7/2} + \tfrac{6}{5}t^{5/2} + \tfrac{4}{3}t^{3/2} + C$.
>
> \# $\sqrt{t} \cdot t^2 = t^{1/2 + 2} = t^{5/2}$ and $\sqrt{t} \cdot t = t^{3/2}$. Dividing by $\tfrac{7}{2}$ is multiplying by $\tfrac{2}{7}$.

### ST 4.4.15
Question: [[CAL1 HW 4.4 Questions#ST 4.4.15|ST 4.4.15]]

> [!solution] Solution
> $$
> \begin{aligned}
> \int \frac{1 + \sqrt{x} + x}{\sqrt{x}}\,dx &= \int \left(x^{-1/2} + 1 + x^{1/2}\right)dx \\
> &= \frac{x^{1/2}}{1/2} + x + \frac{x^{3/2}}{3/2} + C
> \end{aligned}
> $$
> Hence $\int \dfrac{1 + \sqrt{x} + x}{\sqrt{x}}\,dx = 2\sqrt{x} + x + \tfrac{2}{3}x^{3/2} + C$ $(x > 0)$.
>
> \# Divide each term of the numerator by $\sqrt{x}$: $\tfrac{1}{\sqrt{x}} = x^{-1/2}$, $\tfrac{\sqrt{x}}{\sqrt{x}} = 1$, $\tfrac{x}{\sqrt{x}} = x^{1/2}$. The power formula applies to $x^{-1/2}$ because $n = -\tfrac{1}{2} \ne -1$.

### ST 4.4.16
Question: [[CAL1 HW 4.4 Questions#ST 4.4.16|ST 4.4.16]]

> [!solution] Solution
> $$
> \begin{aligned}
> \int \left(u^2 + 1 + \frac{1}{u^2}\right)du &= \int \left(u^2 + 1 + u^{-2}\right)du \\
> &= \frac{u^3}{3} + u + \frac{u^{-1}}{-1} + C
> \end{aligned}
> $$
> Hence $\int \left(u^2 + 1 + \tfrac{1}{u^2}\right)du = \tfrac{1}{3}u^3 + u - \tfrac{1}{u} + C$.
>
> \# $n = -2 \ne -1$, so the power formula works for $u^{-2}$. The integrand is undefined at $u = 0$, so the answer holds on $(-\infty, 0)$ or on $(0, \infty)$, one interval at a time.

### ST 4.4.17
Question: [[CAL1 HW 4.4 Questions#ST 4.4.17|ST 4.4.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> 2 + \tan^2\theta &= 1 + (1 + \tan^2\theta) = 1 + \sec^2\theta \\
> \int (2 + \tan^2\theta)\,d\theta &= \int (1 + \sec^2\theta)\,d\theta = \theta + \tan\theta + C
> \end{aligned}
> $$
> Hence $\int (2 + \tan^2\theta)\,d\theta = \theta + \tan\theta + C$.
>
> \# $\tan^2\theta$ is not in the table, but $\sec^2\theta$ is, so trade it with $1 + \tan^2\theta = \sec^2\theta$. The answer holds on each interval where $\cos\theta \ne 0$.

### ST 4.4.18
Question: [[CAL1 HW 4.4 Questions#ST 4.4.18|ST 4.4.18]]

> [!solution] Solution
> $$
> \int \sec t\,(\sec t + \tan t)\,dt = \int (\sec^2 t + \sec t\tan t)\,dt = \tan t + \sec t + C
> $$
> Hence $\int \sec t\,(\sec t + \tan t)\,dt = \tan t + \sec t + C$.
>
> \# After distributing, both terms are in the table: $(\tan t)' = \sec^2 t$ and $(\sec t)' = \sec t\tan t$.

### ST 4.4.19
Question: [[CAL1 HW 4.4 Questions#ST 4.4.19|ST 4.4.19]]

> [!solution] Solution
> $$
> \int 3\csc^2 t\,dt = 3(-\cot t) + C = -3\cot t + C
> $$
> Hence $\int 3\csc^2 t\,dt = -3\cot t + C$.
>
> \# The minus sign comes from $(\cot t)' = -\csc^2 t$. The answer holds on each interval where $\sin t \ne 0$.

### ST 4.4.20
Question: [[CAL1 HW 4.4 Questions#ST 4.4.20|ST 4.4.20]]

> [!solution] Solution
> $$
> \begin{aligned}
> \frac{\sin 2x}{\sin x} &= \frac{2\sin x\cos x}{\sin x} = 2\cos x \qquad (\sin x \ne 0) \\
> \int \frac{\sin 2x}{\sin x}\,dx &= \int 2\cos x\,dx = 2\sin x + C
> \end{aligned}
> $$
> Hence $\int \dfrac{\sin 2x}{\sin x}\,dx = 2\sin x + C$.
>
> \# The double-angle formula turns the quotient into a table entry. Cancelling $\sin x$ needs $\sin x \ne 0$, so the answer holds on each interval $(k\pi, (k + 1)\pi)$, $k$ an integer.

### ST 4.4.27
Question: [[CAL1 HW 4.4 Questions#ST 4.4.27|ST 4.4.27]]

> [!solution] Solution
> $(2x - 3)(4x^2 + 1) = 8x^3 - 12x^2 + 2x - 3$ is a polynomial, continuous on $[0, 2]$:
> $$
> \begin{aligned}
> \int_0^2 (2x - 3)(4x^2 + 1)\,dx &= \Big[2x^4 - 4x^3 + x^2 - 3x\Big]_0^2 \\
> &= (32 - 32 + 4 - 6) - 0 = -2
> \end{aligned}
> $$
> Hence $\int_0^2 (2x - 3)(4x^2 + 1)\,dx = -2$.
>
> \# $8 \cdot \tfrac{x^4}{4} = 2x^4$, $12 \cdot \tfrac{x^3}{3} = 4x^3$, $2 \cdot \tfrac{x^2}{2} = x^2$. At $x = 0$ every term is $0$. In a definite integral there is no $+C$: it cancels in $F(b) - F(a)$.

### ST 4.4.29
Question: [[CAL1 HW 4.4 Questions#ST 4.4.29|ST 4.4.29]]

> [!solution] Solution
> $4\sin\theta - 3\cos\theta$ is continuous on $[0, \pi]$:
> $$
> \begin{aligned}
> \int_0^\pi (4\sin\theta - 3\cos\theta)\,d\theta &= \Big[-4\cos\theta - 3\sin\theta\Big]_0^\pi \\
> &= (-4\cos\pi - 3\sin\pi) - (-4\cos 0 - 3\sin 0) \\
> &= (4 - 0) - (-4 - 0) = 8
> \end{aligned}
> $$
> Hence $\int_0^\pi (4\sin\theta - 3\cos\theta)\,d\theta = 8$.
>
> \# $\cos\pi = -1$, $\sin\pi = 0$, $\cos 0 = 1$, $\sin 0 = 0$. Watch the signs: $\int \sin\theta\,d\theta = -\cos\theta$.

### ST 4.4.31
Question: [[CAL1 HW 4.4 Questions#ST 4.4.31|ST 4.4.31]]

> [!solution] Solution
> $\dfrac{4 + 6u}{\sqrt{u}} = 4u^{-1/2} + 6u^{1/2}$ is continuous on $[1, 4]$ ($u > 0$):
> $$
> \begin{aligned}
> \int_1^4 \left(4u^{-1/2} + 6u^{1/2}\right)du &= \Big[8u^{1/2} + 4u^{3/2}\Big]_1^4 \\
> &= (8 \cdot 2 + 4 \cdot 8) - (8 + 4) = 48 - 12 = 36
> \end{aligned}
> $$
> Hence $\int_1^4 \dfrac{4 + 6u}{\sqrt{u}}\,du = 36$.
>
> \# $4 \cdot \tfrac{u^{1/2}}{1/2} = 8u^{1/2}$ and $6 \cdot \tfrac{u^{3/2}}{3/2} = 4u^{3/2}$. At $u = 4$: $4^{1/2} = 2$, $4^{3/2} = 2^3 = 8$.

### ST 4.4.35
Question: [[CAL1 HW 4.4 Questions#ST 4.4.35|ST 4.4.35]]

> [!solution] Solution
> $x\left(\sqrt[3]{x} + \sqrt[4]{x}\right) = x^{4/3} + x^{5/4}$ is continuous on $[0, 1]$:
> $$
> \begin{aligned}
> \int_0^1 \left(x^{4/3} + x^{5/4}\right)dx &= \Big[\tfrac{3}{7}x^{7/3} + \tfrac{4}{9}x^{9/4}\Big]_0^1 \\
> &= \frac{3}{7} + \frac{4}{9} = \frac{27 + 28}{63} = \frac{55}{63}
> \end{aligned}
> $$
> Hence $\int_0^1 x\left(\sqrt[3]{x} + \sqrt[4]{x}\right)dx = \tfrac{55}{63}$.
>
> \# $x \cdot x^{1/3} = x^{1 + 1/3} = x^{4/3}$ and $x \cdot x^{1/4} = x^{5/4}$; then $\tfrac{4}{3} + 1 = \tfrac{7}{3}$ and $\tfrac{5}{4} + 1 = \tfrac{9}{4}$. Every power of $1$ is $1$ and every positive power of $0$ is $0$, so only the fractions remain.

### ST 4.4.39
Question: [[CAL1 HW 4.4 Questions#ST 4.4.39|ST 4.4.39]]

> [!solution] Solution
> $\dfrac{1 + \cos^2\theta}{\cos^2\theta} = \dfrac{1}{\cos^2\theta} + 1 = \sec^2\theta + 1$, continuous on $[0, \tfrac{\pi}{4}]$ ($\cos\theta \ge \tfrac{\sqrt{2}}{2} > 0$):
> $$
> \begin{aligned}
> \int_0^{\pi/4} (\sec^2\theta + 1)\,d\theta &= \Big[\tan\theta + \theta\Big]_0^{\pi/4} \\
> &= \Big(1 + \frac{\pi}{4}\Big) - (0 + 0) = 1 + \frac{\pi}{4}
> \end{aligned}
> $$
> Hence $\int_0^{\pi/4} \dfrac{1 + \cos^2\theta}{\cos^2\theta}\,d\theta = 1 + \tfrac{\pi}{4}$.
>
> \# Split the fraction into two terms, then each is a table entry. $\tan\tfrac{\pi}{4} = 1$, $\tan 0 = 0$.

### ST 4.4.41
Question: [[CAL1 HW 4.4 Questions#ST 4.4.41|ST 4.4.41]]

> [!solution] Solution
> $\sqrt{u}\left(u - \sqrt[3]{u}\right) = u^{3/2} - u^{5/6}$ is continuous on $[0, 64]$:
> $$
> \begin{aligned}
> \int_0^{64} \left(u^{3/2} - u^{5/6}\right)du &= \Big[\tfrac{2}{5}u^{5/2} - \tfrac{6}{11}u^{11/6}\Big]_0^{64} \\
> &= \frac{2}{5} \cdot 8^5 - \frac{6}{11} \cdot 2^{11} = \frac{65536}{5} - \frac{12288}{11} \\
> &= \frac{720896 - 61440}{55} = \frac{659456}{55}
> \end{aligned}
> $$
> Hence $\int_0^{64} \sqrt{u}\left(u - \sqrt[3]{u}\right)du = \tfrac{659456}{55} \approx 11990.1$.
>
> \# $u^{1/2} \cdot u^{1/3} = u^{1/2 + 1/3} = u^{5/6}$. Powers of $64$: take the root first, $64^{5/2} = (\sqrt{64})^5 = 8^5 = 32768$ and $64^{11/6} = (\sqrt[6]{64})^{11} = 2^{11} = 2048$.

### ST 4.4.43
Question: [[CAL1 HW 4.4 Questions#ST 4.4.43|ST 4.4.43]]

> [!solution] Solution
> $$
> \lvert x - 3 \rvert = \begin{cases} 3 - x & 2 \le x \le 3 \\ x - 3 & 3 \le x \le 5 \end{cases}
> $$
> $$
> \begin{aligned}
> \int_2^5 \lvert x - 3 \rvert\,dx &= \int_2^3 (3 - x)\,dx + \int_3^5 (x - 3)\,dx \\
> &= \Big[3x - \tfrac{1}{2}x^2\Big]_2^3 + \Big[\tfrac{1}{2}x^2 - 3x\Big]_3^5 \\
> &= \Big(\frac{9}{2} - 4\Big) + \Big(-\frac{5}{2} - \Big(-\frac{9}{2}\Big)\Big) = \frac{1}{2} + 2 = \frac{5}{2}
> \end{aligned}
> $$
> Hence $\int_2^5 \lvert x - 3 \rvert\,dx = \tfrac{5}{2}$.
>
> \# $\lvert x - 3 \rvert$ has no antiderivative in the table as a whole, so split at $x = 3$, where $x - 3$ changes sign. Check by area: the graph forms two triangles above the axis, $\tfrac{1}{2} \cdot 1 \cdot 1 + \tfrac{1}{2} \cdot 2 \cdot 2 = \tfrac{1}{2} + 2$.

### ST 4.4.45
Question: [[CAL1 HW 4.4 Questions#ST 4.4.45|ST 4.4.45]]

> [!solution] Solution
> $$
> x - 2\lvert x \rvert = \begin{cases} x - 2(-x) = 3x & -1 \le x \le 0 \\ x - 2x = -x & 0 \le x \le 2 \end{cases}
> $$
> $$
> \begin{aligned}
> \int_{-1}^{2} (x - 2\lvert x \rvert)\,dx &= \int_{-1}^{0} 3x\,dx + \int_0^2 (-x)\,dx \\
> &= \Big[\tfrac{3}{2}x^2\Big]_{-1}^{0} + \Big[-\tfrac{1}{2}x^2\Big]_0^2 \\
> &= \Big(0 - \frac{3}{2}\Big) + (-2 - 0) = -\frac{7}{2}
> \end{aligned}
> $$
> Hence $\int_{-1}^{2} (x - 2\lvert x \rvert)\,dx = -\tfrac{7}{2}$.
>
> \# Split at $x = 0$, where $\lvert x \rvert$ changes formula: $\lvert x \rvert = -x$ for $x \le 0$. The answer is negative because the integrand is $\le 0$ on the whole interval ($3x \le 0$ for $x \le 0$, $-x \le 0$ for $x \ge 0$): the region lies below the $x$-axis.

### ST 4.4.49
Question: [[CAL1 HW 4.4 Questions#ST 4.4.49|ST 4.4.49]]

> [!solution] Solution
> ![ST 4.4.49 figure|340](../Attachments/CAL1%20HW%204.4%20Solutions%20fig%2049.png)
>
> $2y - y^2 = y(2 - y) \ge 0$ for $0 \le y \le 2$, so the curve is to the right of the $y$-axis there:
> $$
> \begin{aligned}
> A = \int_0^2 (2y - y^2)\,dy &= \Big[y^2 - \tfrac{1}{3}y^3\Big]_0^2 \\
> &= 4 - \frac{8}{3} = \frac{4}{3}
> \end{aligned}
> $$
> Hence the area is $\tfrac{4}{3}$.
>
> \# With $y$ as the variable, the region is cut into horizontal strips: at height $y$ the strip runs from $x = 0$ to $x = 2y - y^2$, so its length is $2y - y^2$ and its thickness is $dy$. The integral adds the strips from $y = 0$ to $y = 2$, the two points where the parabola meets the $y$-axis.

### ST 4.4.50
Question: [[CAL1 HW 4.4 Questions#ST 4.4.50|ST 4.4.50]]

> [!solution] Solution
> ![ST 4.4.50 figure|340](../Attachments/CAL1%20HW%204.4%20Solutions%20fig%2050.png)
>
> $$
> \begin{aligned}
> &y = \sqrt[4]{x} \ (x \ge 0) \iff x = y^4 \ (y \ge 0) \\
> &\text{region: } 0 \le y \le 1, \quad 0 \le x \le y^4 \\
> &A = \int_0^1 y^4\,dy = \Big[\tfrac{1}{5}y^5\Big]_0^1 = \frac{1}{5}
> \end{aligned}
> $$
> Hence the area is $\tfrac{1}{5}$.
>
> \# At height $y$ the strip runs from the $y$-axis ($x = 0$) to the curve ($x = y^4$), so its length is $y^4$. Check with $x$ as the variable: the region lies between $y = \sqrt[4]{x}$ below and $y = 1$ above, $\int_0^1 (1 - x^{1/4})\,dx = 1 - \tfrac{4}{5} = \tfrac{1}{5}$.

### ST 4.4.61
Question: [[CAL1 HW 4.4 Questions#ST 4.4.61|ST 4.4.61]]

> [!solution] Solution
> **(a)**
> $$
> \int_0^3 (3t - 5)\,dt = \Big[\tfrac{3}{2}t^2 - 5t\Big]_0^3 = \frac{27}{2} - 15 = -\frac{3}{2}
> $$
> Hence the displacement is $-\tfrac{3}{2}$ m.
>
> **(b)** $v(t) = 3t - 5 \le 0$ for $0 \le t \le \tfrac{5}{3}$ and $v(t) \ge 0$ for $\tfrac{5}{3} \le t \le 3$:
> $$
> \begin{aligned}
> \int_0^3 \lvert v(t) \rvert\,dt &= \int_0^{5/3} (5 - 3t)\,dt + \int_{5/3}^{3} (3t - 5)\,dt \\
> &= \Big[5t - \tfrac{3}{2}t^2\Big]_0^{5/3} + \Big[\tfrac{3}{2}t^2 - 5t\Big]_{5/3}^{3} \\
> &= \Big(\frac{25}{3} - \frac{25}{6}\Big) + \Big(-\frac{3}{2} - \Big(-\frac{25}{6}\Big)\Big) = \frac{25}{6} + \frac{8}{3} = \frac{41}{6}
> \end{aligned}
> $$
> Hence the distance traveled is $\tfrac{41}{6} \approx 6.83$ m.
>
> ![ST 4.4.61 figure|340](../Attachments/CAL1%20HW%204.4%20Solutions%20fig%2061.png)
>
> \# Displacement is $\int v\,dt$; distance is $\int \lvert v \rvert\,dt$. The particle moves left ($v < 0$) for $\tfrac{25}{6}$ m, then right for $\tfrac{8}{3}$ m: displacement $-\tfrac{25}{6} + \tfrac{8}{3} = -\tfrac{3}{2}$, distance $\tfrac{25}{6} + \tfrac{8}{3} = \tfrac{41}{6}$. At $t = \tfrac{5}{3}$: $\tfrac{3}{2} \cdot \tfrac{25}{9} - \tfrac{25}{3} = \tfrac{25}{6} - \tfrac{50}{6} = -\tfrac{25}{6}$.

### ST 4.4.63
Question: [[CAL1 HW 4.4 Questions#ST 4.4.63|ST 4.4.63]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> &v(t) = \int (t + 4)\,dt = \tfrac{1}{2}t^2 + 4t + C \\
> &v(0) = C = 5
> \end{aligned}
> $$
> Hence $v(t) = \tfrac{1}{2}t^2 + 4t + 5$ m/s.
>
> **(b)** For $0 \le t \le 10$, $v(t) \ge 5 > 0$, so $\lvert v(t) \rvert = v(t)$:
> $$
> \begin{aligned}
> \int_0^{10} \lvert v(t) \rvert\,dt &= \int_0^{10} \left(\tfrac{1}{2}t^2 + 4t + 5\right)dt = \Big[\tfrac{1}{6}t^3 + 2t^2 + 5t\Big]_0^{10} \\
> &= \frac{1000}{6} + 200 + 50 = \frac{500}{3} + 250 = \frac{1250}{3}
> \end{aligned}
> $$
> Hence the distance traveled is $\tfrac{1250}{3} \approx 416.7$ m.
>
> \# $v' = a$, so $v$ is an antiderivative of $a$, and $v(0) = 5$ picks the constant. Distance always needs $\lvert v \rvert$; here $v$ never changes sign, because each term $\tfrac{1}{2}t^2$, $4t$ is $\ge 0$ for $t \ge 0$, so the distance equals the displacement.
