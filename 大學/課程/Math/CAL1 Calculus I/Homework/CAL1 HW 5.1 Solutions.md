---
course: [CAL1]
semester: "115-1"
chapter: ["5.1"]
tags: [calculus, homework, solutions, integrals]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §5.1, pp. 364-370, scanned PDF (areas between curves, integrating with respect to x and to y)"
created: 2026-11-25
questions: "[[CAL1 HW 5.1 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 5.1 Questions#ST 5.1.1\|ST 5.1.1]] | (a) $\int_0^2 (2x - x^2)\,dx$; (b) $\tfrac{4}{3}$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.3\|ST 5.1.3]] | (a) $\int_0^1 \big[\sqrt{y} - (y^2 - 1)\big]\,dy$; (b) $\tfrac{4}{3}$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.5\|ST 5.1.5]] | $8$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.7\|ST 5.1.7]] | $\int_1^2 \left(\tfrac{1}{x} - \tfrac{1}{x^2}\right)dx$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.8\|ST 5.1.8]] | $\int_0^1 (\tan x - \sin x)\,dx$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.9\|ST 5.1.9]] | $\int_1^2 \big[(2x - x^2) - (2 - x)\big]\,dx$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.19\|ST 5.1.19]] | $72$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.21\|ST 5.1.21]] | $\tfrac{32}{3}$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.25\|ST 5.1.25]] | $9$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.27\|ST 5.1.27]] | $\tfrac{1}{2}$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.29\|ST 5.1.29]] | $6\sqrt{3} \approx 10.39$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.31\|ST 5.1.31]] | $\tfrac{13}{5}$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.33\|ST 5.1.33]] | $\tfrac{4}{\pi} - \tfrac{1}{2} \approx 0.773$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.35\|ST 5.1.35]] | (a) $39$; (b) $15$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.41\|ST 5.1.41]] | $\tfrac{3\sqrt{3}}{2} - 1 \approx 1.598$, the area between $y = \sin x$ and $y = \cos 2x$ on $[0, \tfrac{\pi}{2}]$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.52\|ST 5.1.52]] | $\tfrac{7}{12}$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.63\|ST 5.1.63]] | $b = 4^{2/3} = 2\sqrt[3]{2} \approx 2.52$ |
| [[CAL1 HW 5.1 Questions#ST 5.1.67\|ST 5.1.67]] | $c = \tfrac{32}{27}$ |

## ST §5.1 Areas Between Curves

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Area Between Curves]], with respect to $x$** (textbook p. 364): if $f$ and $g$ are continuous and $f(x) \ge g(x)$ on $[a, b]$, the region bounded by $y = f(x)$, $y = g(x)$, $x = a$, $x = b$ has area $A = \int_a^b [f(x) - g(x)]\,dx = \int_a^b (y_T - y_B)\,dx$: top minus bottom, summed over vertical rectangles of width $dx$.
> - **When the curves cross** (p. 366): $A = \int_a^b \lvert f(x) - g(x) \rvert\,dx$. In practice: find where $f = g$, split $[a, b]$ there, and on each piece integrate (top) $-$ (bottom).
> - **With respect to $y$** (p. 367): if the region is bounded by $x = f(y)$, $x = g(y)$, $y = c$, $y = d$ with $f(y) \ge g(y)$, then $A = \int_c^d [f(y) - g(y)]\,dy = \int_c^d (x_R - x_L)\,dy$: right minus left, over horizontal rectangles of height $dy$. It is the better choice when the left and right boundaries are each a single curve, typically when the curves are given as $x = \dots$
> - **The steps**: set the curves equal to find the intersections (the limits); a test point between them shows which curve is on top (or on the right); integrate top $-$ bottom with the [[Fundamental Theorem of Calculus]].
> - **Symmetry** ([[Integrals of Symmetric Functions]]): if the integrand is even, $\int_{-a}^{a} = 2\int_0^a$.
> - **Antiderivatives**: $x^n \to \dfrac{x^{n+1}}{n+1}$ ($n \ne -1$), $\sin kx \to -\tfrac{1}{k}\cos kx$, $\cos kx \to \tfrac{1}{k}\sin kx$, $\sec^2 x \to \tan x$.
> - **Identities**: $\sin 2x = 2\sin x\cos x$, $\cos 2x = 1 - 2\sin^2 x$.
> - Each answer is written as on an exam paper: the intersections, which curve is on top, the integral, then the conclusion on a Hence line. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 5.1.1
Question: [[CAL1 HW 5.1 Questions#ST 5.1.1|ST 5.1.1]]

> [!solution] Solution
> ![ST 5.1.1 figure|400](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%201.png)
>
> Intersections: $3x - x^2 = x \iff x^2 - 2x = 0 \iff x(x - 2) = 0 \iff x = 0, 2$.
> On $[0, 2]$: $3x - x^2 \ge x$ ($x = 1$: $2 > 1$).
>
> **(a)**
> $$
> A = \int_0^2 \big[(3x - x^2) - x\big]\,dx = \int_0^2 (2x - x^2)\,dx
> $$
>
> **(b)**
> $$
> A = \Big[x^2 - \frac{x^3}{3}\Big]_0^2 = 4 - \frac{8}{3} = \frac{4}{3}
> $$
> Hence the area is $\tfrac{4}{3}$.
>
> \# A vertical rectangle has height $y_T - y_B = (3x - x^2) - x$ and width $dx$. The figure shows $(2, 2)$, but on an exam the limits come from solving $3x - x^2 = x$.

### ST 5.1.3
Question: [[CAL1 HW 5.1 Questions#ST 5.1.3|ST 5.1.3]]

> [!solution] Solution
> ![ST 5.1.3 figure|400](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%203.png)
>
> Integrate with respect to $y$: for $0 \le y \le 1$, the left boundary is $x_L = y^2 - 1$ and the right boundary is $x_R = \sqrt{y}$.
>
> **(a)**
> $$
> A = \int_0^1 \big[\sqrt{y} - (y^2 - 1)\big]\,dy
> $$
>
> **(b)**
> $$
> A = \int_0^1 \big(y^{1/2} - y^2 + 1\big)\,dy = \Big[\frac{2}{3}y^{3/2} - \frac{y^3}{3} + y\Big]_0^1 = \frac{2}{3} - \frac{1}{3} + 1 = \frac{4}{3}
> $$
> Hence the area is $\tfrac{4}{3}$.
>
> \# With respect to $x$ the bottom and top change at $x = 0$ (for $-1 \le x \le 0$ the region is $0 \le y \le \sqrt{x + 1}$, for $0 \le x \le 1$ it is $x^2 \le y \le 1$), so it takes two integrals: $\int_{-1}^{0} \sqrt{x + 1}\,dx + \int_0^1 (1 - x^2)\,dx = \tfrac{2}{3} + \tfrac{2}{3} = \tfrac{4}{3}$. With respect to $y$, left and right are each a single curve, so one integral suffices.

### ST 5.1.5
Question: [[CAL1 HW 5.1 Questions#ST 5.1.5|ST 5.1.5]]

> [!solution] Solution
> ![ST 5.1.5 figure|380](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%205.png)
>
> Intersections: $x^3 - 3x = x \iff x^3 - 4x = 0 \iff x(x - 2)(x + 2) = 0 \iff x = -2, 0, 2$.
> On $[-2, 0]$: $x^3 - 3x \ge x$ ($x = -1$: $2 > -1$). On $[0, 2]$: $x \ge x^3 - 3x$ ($x = 1$: $1 > -2$).
> $$
> \begin{aligned}
> A &= \int_{-2}^{0} \big[(x^3 - 3x) - x\big]\,dx + \int_0^2 \big[x - (x^3 - 3x)\big]\,dx \\
> &= \int_{-2}^{0} (x^3 - 4x)\,dx + \int_0^2 (4x - x^3)\,dx \\
> &= \Big[\frac{x^4}{4} - 2x^2\Big]_{-2}^{0} + \Big[2x^2 - \frac{x^4}{4}\Big]_0^2 \\
> &= \big(0 - (4 - 8)\big) + (8 - 4) = 4 + 4 = 8
> \end{aligned}
> $$
> Hence the area is $8$.
>
> \# The curves cross at $x = 0$, so the integral is split there. Writing $\int_{-2}^{2} (x^3 - 4x)\,dx$ would give $0$, because it subtracts $A_2$ from $A_1$. Both functions are odd, so $A_1 = A_2$ and $A = 2A_2$.

### ST 5.1.7
Question: [[CAL1 HW 5.1 Questions#ST 5.1.7|ST 5.1.7]]

> [!solution] Solution
> Intersection: $\dfrac{1}{x} = \dfrac{1}{x^2} \iff x = 1$ ($x \ne 0$).
> On $[1, 2]$: $\dfrac{1}{x} - \dfrac{1}{x^2} = \dfrac{x - 1}{x^2} \ge 0$, so $y = \tfrac{1}{x}$ is on top.
> $$
> A = \int_1^2 \Big(\frac{1}{x} - \frac{1}{x^2}\Big)\,dx
> $$
>
> \# The region is closed on the left by the crossing point $(1, 1)$ and on the right by $x = 2$. Its value, $\ln 2 - \tfrac{1}{2}$, needs $\int \tfrac{1}{x}\,dx = \ln\lvert x \rvert$ from Chapter 6.

### ST 5.1.8
Question: [[CAL1 HW 5.1 Questions#ST 5.1.8|ST 5.1.8]]

> [!solution] Solution
> Intersection: $\tan x = \sin x \iff \sin x\Big(\dfrac{1}{\cos x} - 1\Big) = 0 \iff \sin x = 0$ or $\cos x = 1$; on $[0, 1]$ both give only $x = 0$.
> On $[0, 1]$: $0 < \cos x \le 1$ and $\sin x \ge 0$, so $\tan x = \dfrac{\sin x}{\cos x} \ge \sin x$.
> $$
> A = \int_0^1 (\tan x - \sin x)\,dx
> $$
>
> \# The region runs from $x = 0$, where the curves meet, to $x = 1$; since $1 < \tfrac{\pi}{2}$, $\tan x$ is continuous there.

### ST 5.1.9
Question: [[CAL1 HW 5.1 Questions#ST 5.1.9|ST 5.1.9]]

> [!solution] Solution
> Intersections: $2 - x = 2x - x^2 \iff x^2 - 3x + 2 = 0 \iff (x - 1)(x - 2) = 0 \iff x = 1, 2$.
> On $[1, 2]$: $2x - x^2 \ge 2 - x$ ($x = \tfrac{3}{2}$: $\tfrac{3}{4} > \tfrac{1}{2}$).
> $$
> A = \int_1^2 \big[(2x - x^2) - (2 - x)\big]\,dx
> $$
>
> \# The integrand simplifies to $-x^2 + 3x - 2 = -(x - 1)(x - 2)$, which is $\ge 0$ between its roots: another way to see that the parabola is on top.

### ST 5.1.19
Question: [[CAL1 HW 5.1 Questions#ST 5.1.19|ST 5.1.19]]

> [!solution] Solution
> ![ST 5.1.19 figure|340](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2019.png)
>
> Intersections: $12 - x^2 = x^2 - 6 \iff 2x^2 = 18 \iff x = \pm 3$.
> On $[-3, 3]$: $12 - x^2 \ge x^2 - 6$ ($x = 0$: $12 > -6$).
> $$
> \begin{aligned}
> A &= \int_{-3}^{3} \big[(12 - x^2) - (x^2 - 6)\big]\,dx = \int_{-3}^{3} (18 - 2x^2)\,dx \\
> &= 2\int_0^3 (18 - 2x^2)\,dx = 2\Big[18x - \frac{2x^3}{3}\Big]_0^3 = 2(54 - 18) = 72
> \end{aligned}
> $$
> Hence the area is $72$.
>
> \# $18 - 2x^2$ is even, so $\int_{-3}^{3} = 2\int_0^3$.

### ST 5.1.21
Question: [[CAL1 HW 5.1 Questions#ST 5.1.21|ST 5.1.21]]

> [!solution] Solution
> ![ST 5.1.21 figure|420](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2021.png)
>
> Both curves are given as $x = \dots$: integrate with respect to $y$.
> Intersections: $2y^2 = 4 + y^2 \iff y^2 = 4 \iff y = \pm 2$.
> On $[-2, 2]$: $x_R = 4 + y^2$, $x_L = 2y^2$ ($y = 0$: $4 > 0$).
> $$
> \begin{aligned}
> A &= \int_{-2}^{2} \big[(4 + y^2) - 2y^2\big]\,dy = \int_{-2}^{2} (4 - y^2)\,dy \\
> &= 2\int_0^2 (4 - y^2)\,dy = 2\Big[4y - \frac{y^3}{3}\Big]_0^2 = 2\Big(8 - \frac{8}{3}\Big) = \frac{32}{3}
> \end{aligned}
> $$
> Hence the area is $\tfrac{32}{3}$.
>
> \# Right minus left, with horizontal rectangles of height $dy$. With respect to $x$ the boundaries would change at $x = 4$ and need square roots ($y = \pm\sqrt{x/2}$, $y = \pm\sqrt{x - 4}$).

### ST 5.1.25
Question: [[CAL1 HW 5.1 Questions#ST 5.1.25|ST 5.1.25]]

> [!solution] Solution
> ![ST 5.1.25 figure|440](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2025.png)
>
> Intersections ($x \ge 0$, square both sides): $\sqrt{x} = \tfrac{1}{3}x \iff 9x = x^2 \iff x(x - 9) = 0 \iff x = 0, 9$.
> On $[0, 9]$: $\sqrt{x} \ge \tfrac{1}{3}x$ ($x = 1$: $1 > \tfrac{1}{3}$). On $[9, 16]$: $\tfrac{1}{3}x \ge \sqrt{x}$ ($x = 16$: $\tfrac{16}{3} > 4$).
> $$
> \begin{aligned}
> A &= \int_0^9 \Big(\sqrt{x} - \frac{x}{3}\Big)\,dx + \int_9^{16} \Big(\frac{x}{3} - \sqrt{x}\Big)\,dx \\
> &= \Big[\frac{2}{3}x^{3/2} - \frac{x^2}{6}\Big]_0^9 + \Big[\frac{x^2}{6} - \frac{2}{3}x^{3/2}\Big]_9^{16} \\
> &= \Big(18 - \frac{27}{2}\Big) + \Big[\Big(\frac{128}{3} - \frac{128}{3}\Big) - \Big(\frac{27}{2} - 18\Big)\Big] = \frac{9}{2} + \frac{9}{2} = 9
> \end{aligned}
> $$
> Hence the area is $9$.
>
> \# The curves cross at $x = 9$, inside $[0, 16]$, so the integral is split there. Values: $9^{3/2} = 27$, $16^{3/2} = 64$, so $\tfrac{2}{3} \cdot 27 = 18$, $\tfrac{81}{6} = \tfrac{27}{2}$, and $\tfrac{256}{6} = \tfrac{128}{3} = \tfrac{2}{3} \cdot 64$.

### ST 5.1.27
Question: [[CAL1 HW 5.1 Questions#ST 5.1.27|ST 5.1.27]]

> [!solution] Solution
> ![ST 5.1.27 figure|420](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2027.png)
>
> Intersections: $\cos x = \sin 2x = 2\sin x\cos x \iff \cos x\,(1 - 2\sin x) = 0 \iff \cos x = 0$ or $\sin x = \tfrac{1}{2}$; in $[0, \tfrac{\pi}{2}]$: $x = \tfrac{\pi}{6}, \tfrac{\pi}{2}$.
> On $[0, \tfrac{\pi}{6}]$: $\cos x \ge \sin 2x$ ($x = 0$: $1 > 0$). On $[\tfrac{\pi}{6}, \tfrac{\pi}{2}]$: $\sin 2x \ge \cos x$ ($x = \tfrac{\pi}{4}$: $1 > \tfrac{\sqrt{2}}{2}$).
> $$
> \begin{aligned}
> A &= \int_0^{\pi/6} (\cos x - \sin 2x)\,dx + \int_{\pi/6}^{\pi/2} (\sin 2x - \cos x)\,dx \\
> &= \Big[\sin x + \frac{1}{2}\cos 2x\Big]_0^{\pi/6} + \Big[-\frac{1}{2}\cos 2x - \sin x\Big]_{\pi/6}^{\pi/2} \\
> &= \Big(\frac{1}{2} + \frac{1}{4} - \frac{1}{2}\Big) + \Big[\Big(\frac{1}{2} - 1\Big) - \Big(-\frac{1}{4} - \frac{1}{2}\Big)\Big] = \frac{1}{4} + \frac{1}{4} = \frac{1}{2}
> \end{aligned}
> $$
> Hence the area is $\tfrac{1}{2}$.
>
> \# Do not divide by $\cos x$ when solving: that loses the root $x = \tfrac{\pi}{2}$. $\int \sin 2x\,dx = -\tfrac{1}{2}\cos 2x$ (substitute $u = 2x$); values used: $\cos\tfrac{\pi}{3} = \tfrac{1}{2}$, $\cos\pi = -1$.

### ST 5.1.29
Question: [[CAL1 HW 5.1 Questions#ST 5.1.29|ST 5.1.29]]

> [!solution] Solution
> ![ST 5.1.29 figure|360](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2029.png)
>
> Intersections: $\sec^2 x = 8\cos x \iff 1 = 8\cos^3 x \iff \cos x = \tfrac{1}{2} \iff x = \pm\tfrac{\pi}{3}$ (in $[-\tfrac{\pi}{3}, \tfrac{\pi}{3}]$).
> On $[-\tfrac{\pi}{3}, \tfrac{\pi}{3}]$: $8\cos x \ge \sec^2 x$ ($x = 0$: $8 > 1$).
> $$
> \begin{aligned}
> A &= \int_{-\pi/3}^{\pi/3} (8\cos x - \sec^2 x)\,dx = 2\int_0^{\pi/3} (8\cos x - \sec^2 x)\,dx \\
> &= 2\Big[8\sin x - \tan x\Big]_0^{\pi/3} = 2\Big(8 \cdot \frac{\sqrt{3}}{2} - \sqrt{3}\Big) = 2 \cdot 3\sqrt{3} = 6\sqrt{3}
> \end{aligned}
> $$
> Hence the area is $6\sqrt{3} \approx 10.39$.
>
> \# To solve, multiply both sides by $\cos^2 x$ (not $0$ on this interval). The integrand is even ($\cos(-x) = \cos x$), so $\int_{-\pi/3}^{\pi/3} = 2\int_0^{\pi/3}$.

### ST 5.1.31
Question: [[CAL1 HW 5.1 Questions#ST 5.1.31|ST 5.1.31]]

> [!solution] Solution
> ![ST 5.1.31 figure|420](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2031.png)
>
> Both curves are symmetric about the $y$-axis; for $x \ge 0$, $2 - \lvert x \rvert = 2 - x$.
> Intersection ($x \ge 0$): $x^4 = 2 - x \iff x^4 + x - 2 = 0 \iff (x - 1)(x^3 + x^2 + x + 2) = 0 \iff x = 1$, because $x^3 + x^2 + x + 2 > 0$ for $x \ge 0$. By symmetry also $x = -1$.
> On $[0, 1]$: $2 - x \ge x^4$ ($x = 0$: $2 > 0$).
> $$
> A = 2\int_0^1 (2 - x - x^4)\,dx = 2\Big[2x - \frac{x^2}{2} - \frac{x^5}{5}\Big]_0^1 = 2\Big(2 - \frac{1}{2} - \frac{1}{5}\Big) = 2 \cdot \frac{13}{10} = \frac{13}{5}
> $$
> Hence the area is $\tfrac{13}{5}$.
>
> \# $x = 1$ is found by trying ($1 + 1 - 2 = 0$); dividing by $x - 1$ gives the cubic. Working on $x \ge 0$ and doubling removes the absolute value.

### ST 5.1.33
Question: [[CAL1 HW 5.1 Questions#ST 5.1.33|ST 5.1.33]]

> [!solution] Solution
> ![ST 5.1.33 figure|400](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2033.png)
>
> Intersections: $\sin(\tfrac{\pi x}{2}) = x^3$ at $x = 0, \pm 1$ (by inspection: $\sin 0 = 0$, $\sin(\pm\tfrac{\pi}{2}) = \pm 1$).
> On $[0, 1]$: $\sin(\tfrac{\pi x}{2}) \ge x^3$ ($x = \tfrac{1}{2}$: $\tfrac{\sqrt{2}}{2} > \tfrac{1}{8}$). Both functions are odd, so the region on $[-1, 0]$ is the reflection of the one on $[0, 1]$ through the origin.
> $$
> \begin{aligned}
> A &= 2\int_0^1 \Big[\sin\Big(\frac{\pi x}{2}\Big) - x^3\Big]\,dx = 2\Big[-\frac{2}{\pi}\cos\Big(\frac{\pi x}{2}\Big) - \frac{x^4}{4}\Big]_0^1 \\
> &= 2\Big[\Big(0 - \frac{1}{4}\Big) - \Big(-\frac{2}{\pi} - 0\Big)\Big] = 2\Big(\frac{2}{\pi} - \frac{1}{4}\Big) = \frac{4}{\pi} - \frac{1}{2}
> \end{aligned}
> $$
> Hence the area is $\tfrac{4}{\pi} - \tfrac{1}{2} \approx 0.773$.
>
> \# Why there are no other crossings: for $\lvert x \rvert > 1$, $\lvert x^3 \rvert > 1 \ge \lvert \sin(\tfrac{\pi x}{2}) \rvert$; on $(0, 1)$, $\sin(\tfrac{\pi x}{2})$ is concave downward, so it lies above its chord $y = x$ from $(0, 0)$ to $(1, 1)$, and $x > x^3$ there. $\int \sin(\tfrac{\pi x}{2})\,dx = -\tfrac{2}{\pi}\cos(\tfrac{\pi x}{2})$ (substitute $u = \tfrac{\pi x}{2}$).

### ST 5.1.35
Question: [[CAL1 HW 5.1 Questions#ST 5.1.35|ST 5.1.35]]

> [!solution] Solution
> ![ST 5.1.35 figure|420](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2035.png)
>
> **(a)** The total area is the sum of the two areas:
> $$
> A = 12 + 27 = 39
> $$
>
> **(b)** On $[0, 2]$, $g \ge f$, so $f(x) - g(x) \le 0$; on $[2, 5]$, $f \ge g$.
> $$
> \int_0^5 [f(x) - g(x)]\,dx = \int_0^2 [f(x) - g(x)]\,dx + \int_2^5 [f(x) - g(x)]\,dx = -12 + 27 = 15
> $$
>
> \# (a) is $\int_0^5 \lvert f(x) - g(x) \rvert\,dx$, an area, never negative; (b) is a net value, in which the region where $g$ is on top counts with a minus sign.

### ST 5.1.41
Question: [[CAL1 HW 5.1 Questions#ST 5.1.41|ST 5.1.41]]

> [!solution] Solution
> ![ST 5.1.41 figure|420](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2041.png)
>
> $\sin x - \cos 2x = \sin x - (1 - 2\sin^2 x) = 2\sin^2 x + \sin x - 1 = (2\sin x - 1)(\sin x + 1)$.
> On $[0, \tfrac{\pi}{2}]$: $\sin x + 1 > 0$, so the sign is that of $2\sin x - 1$: negative on $[0, \tfrac{\pi}{6})$, $\ge 0$ on $[\tfrac{\pi}{6}, \tfrac{\pi}{2}]$.
> $$
> \begin{aligned}
> \int_0^{\pi/2} \lvert \sin x - \cos 2x \rvert\,dx &= \int_0^{\pi/6} (\cos 2x - \sin x)\,dx + \int_{\pi/6}^{\pi/2} (\sin x - \cos 2x)\,dx \\
> &= \Big[\frac{1}{2}\sin 2x + \cos x\Big]_0^{\pi/6} + \Big[-\cos x - \frac{1}{2}\sin 2x\Big]_{\pi/6}^{\pi/2} \\
> &= \Big(\frac{\sqrt{3}}{4} + \frac{\sqrt{3}}{2} - 1\Big) + \Big[0 - \Big(-\frac{\sqrt{3}}{2} - \frac{\sqrt{3}}{4}\Big)\Big] \\
> &= \Big(\frac{3\sqrt{3}}{4} - 1\Big) + \frac{3\sqrt{3}}{4} = \frac{3\sqrt{3}}{2} - 1
> \end{aligned}
> $$
> Hence the integral equals $\tfrac{3\sqrt{3}}{2} - 1 \approx 1.598$. It is the area of the region between the curves $y = \sin x$ and $y = \cos 2x$ for $0 \le x \le \tfrac{\pi}{2}$: $\cos 2x$ is on top on $[0, \tfrac{\pi}{6}]$, $\sin x$ on $[\tfrac{\pi}{6}, \tfrac{\pi}{2}]$.
>
> \# $\lvert f - g \rvert$ means top minus bottom on each piece; the pieces meet where $f = g$, here at $(\tfrac{\pi}{6}, \tfrac{1}{2})$. At $x = \tfrac{\pi}{2}$: $\cos\tfrac{\pi}{2} = 0$ and $\sin\pi = 0$.

### ST 5.1.52
Question: [[CAL1 HW 5.1 Questions#ST 5.1.52|ST 5.1.52]]

> [!solution] Solution
> ![ST 5.1.52 figure|360](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2052.png)
>
> $x - 2y^2 \ge 0 \iff x \ge 2y^2$: on or to the right of the parabola $x = 2y^2$.
> $1 - x - \lvert y \rvert \ge 0 \iff x \le 1 - \lvert y \rvert$: on or to the left of the lines $x = 1 - y$ ($y \ge 0$) and $x = 1 + y$ ($y \le 0$).
> So the region is $2y^2 \le x \le 1 - \lvert y \rvert$; integrate with respect to $y$.
> Intersection ($y \ge 0$): $2y^2 = 1 - y \iff 2y^2 + y - 1 = 0 \iff (2y - 1)(y + 1) = 0 \iff y = \tfrac{1}{2}$. By symmetry about the $x$-axis also $y = -\tfrac{1}{2}$.
> $$
> A = 2\int_0^{1/2} \big[(1 - y) - 2y^2\big]\,dy = 2\Big[y - \frac{y^2}{2} - \frac{2y^3}{3}\Big]_0^{1/2} = 2\Big(\frac{1}{2} - \frac{1}{8} - \frac{1}{12}\Big) = 2 \cdot \frac{7}{24} = \frac{7}{12}
> $$
> Hence the area is $\tfrac{7}{12}$.
>
> \# Replacing $y$ by $-y$ changes neither inequality, so the region is symmetric about the $x$-axis, and on $y \ge 0$, $\lvert y \rvert = y$. Right minus left: $x_R = 1 - y$, $x_L = 2y^2$.

### ST 5.1.63
Question: [[CAL1 HW 5.1 Questions#ST 5.1.63|ST 5.1.63]]

> [!solution] Solution
> ![ST 5.1.63 figure|400](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2063.png)
>
> The region is $x^2 \le y \le 4$. Integrate with respect to $y$: at height $y$ the width is $x_R - x_L = \sqrt{y} - (-\sqrt{y}) = 2\sqrt{y}$.
> $$
> \begin{aligned}
> \text{total area} &= \int_0^4 2\sqrt{y}\,dy = \Big[\frac{4}{3}y^{3/2}\Big]_0^4 = \frac{4}{3} \cdot 8 = \frac{32}{3} \\
> \text{area below } y = b &= \int_0^b 2\sqrt{y}\,dy = \frac{4}{3}b^{3/2} \qquad (0 < b < 4)
> \end{aligned}
> $$
> Equal areas $\iff$ the part below $y = b$ is half of the total:
> $$
> \frac{4}{3}b^{3/2} = \frac{1}{2} \cdot \frac{32}{3} = \frac{16}{3} \iff b^{3/2} = 4 \iff b = 4^{2/3} = 2^{4/3} = 2\sqrt[3]{2}
> $$
> Hence $b = 4^{2/3} = 2\sqrt[3]{2} \approx 2.52$.
>
> \# Horizontal rectangles make this easy: every horizontal slice is one segment from $-\sqrt{y}$ to $\sqrt{y}$. With respect to $x$, the part above $y = b$ would have to be split at $x = \pm\sqrt{b}$. Check: $b^{3/2} = 4$ gives $\tfrac{4}{3} \cdot 4 = \tfrac{16}{3}$ below and $\tfrac{32}{3} - \tfrac{16}{3} = \tfrac{16}{3}$ above.

### ST 5.1.67
Question: [[CAL1 HW 5.1 Questions#ST 5.1.67|ST 5.1.67]]

> [!solution] Solution
> ![ST 5.1.67 figure|400](../Attachments/CAL1%20HW%205.1%20Solutions%20fig%2067.png)
>
> Let $f(x) = 8x - 27x^3$, and let $0 < a < b$ be the $x$-coordinates where $y = c$ meets the curve. On $[0, a]$ the line is on top ($A_1$); on $[a, b]$ the curve is on top ($A_2$).
> $$
> \begin{aligned}
> A_1 = A_2 &\iff \int_0^a [c - f(x)]\,dx = \int_a^b [f(x) - c]\,dx \\
> &\iff \int_0^a [f(x) - c]\,dx + \int_a^b [f(x) - c]\,dx = 0 \iff \int_0^b [f(x) - c]\,dx = 0
> \end{aligned}
> $$
> $$
> \int_0^b (8x - 27x^3 - c)\,dx = 4b^2 - \frac{27}{4}b^4 - cb = 0 \implies c = 4b - \frac{27}{4}b^3 \quad (b > 0)
> $$
> $b$ is on the curve: $c = f(b) = 8b - 27b^3$. So
> $$
> 8b - 27b^3 = 4b - \frac{27}{4}b^3 \iff 4b = \frac{81}{4}b^3 \iff b^2 = \frac{16}{81} \iff b = \frac{4}{9} \quad (b > 0)
> $$
> $$
> c = 8 \cdot \frac{4}{9} - 27 \cdot \frac{64}{729} = \frac{32}{9} - \frac{64}{27} = \frac{96 - 64}{27} = \frac{32}{27}
> $$
> Hence $c = \tfrac{32}{27} \approx 1.185$.
>
> \# The idea: $\int_0^b (f - c)\,dx$ counts $A_2$ with $+$ and $A_1$ with $-$, so equal areas means this net value is $0$, and $a$ is never needed. Check: $f'(x) = 8 - 81x^2 = 0$ at $x = \tfrac{2\sqrt{2}}{9} \approx 0.314 < b$, so $b = \tfrac{4}{9}$ is the right-hand crossing; the left one is $a = \tfrac{2\sqrt{3} - 2}{9} \approx 0.163$, and both areas equal $\tfrac{32\sqrt{3}}{81} - \tfrac{16}{27} \approx 0.092$ (checked by computer).
