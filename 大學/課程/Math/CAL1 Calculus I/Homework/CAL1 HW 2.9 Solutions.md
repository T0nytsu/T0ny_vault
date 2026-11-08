---
course: [CAL1]
semester: "115-1"
chapter: ["2.9"]
tags: [calculus, homework, solutions, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §2.9, pp. 192-196, scanned PDF (linearization, differentials, Figure 5)"
created: 2026-11-08
questions: "[[CAL1 HW 2.9 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 2.9 Questions#ST 2.9.3\|ST 2.9.3]] | $L(x) = \tfrac{1}{12}x + \tfrac{4}{3}$ |
| [[CAL1 HW 2.9 Questions#ST 2.9.13\|ST 2.9.13]] | $dy = -\frac{1}{(1 + 3u)^{2}}\,du$ |
| [[CAL1 HW 2.9 Questions#ST 2.9.17\|ST 2.9.17]] | $dy = \frac{1 + \sin t}{2\sqrt{t - \cos t}}\,dt$ |
| [[CAL1 HW 2.9 Questions#ST 2.9.21\|ST 2.9.21]] | (a) $dy = \frac{x}{\sqrt{3 + x^{2}}}\,dx$; (b) $-0.05$ |
| [[CAL1 HW 2.9 Questions#ST 2.9.23\|ST 2.9.23]] | $\Delta y = 1.25$, $dy = 1$ |
| [[CAL1 HW 2.9 Questions#ST 2.9.29\|ST 2.9.29]] | $\Delta y \approx -0.012539$, $dy = -0.0125$; $\Delta y \approx -0.0025016$, $dy = -0.0025$; yes |
| [[CAL1 HW 2.9 Questions#ST 2.9.31\|ST 2.9.31]] | $15.968$ |
| [[CAL1 HW 2.9 Questions#ST 2.9.33\|ST 2.9.33]] | $10.00\overline{3}$ |
| [[CAL1 HW 2.9 Questions#ST 2.9.38\|ST 2.9.38]] | $L(4.02) = 2.005$ for $\sqrt{x}$ at $a = 4$ |
| [[CAL1 HW 2.9 Questions#ST 2.9.39\|ST 2.9.39]] | (a) 270 cm³, 0.01, 1 %; (b) 36 cm², $\tfrac{1}{150} \approx 0.0067$, about 0.67 % |
| [[CAL1 HW 2.9 Questions#ST 2.9.41\|ST 2.9.41]] | (a) $\frac{84}{\pi} \approx 27$ cm², $\tfrac{1}{84} \approx 0.012$; (b) $\frac{1764}{\pi^{2}} \approx 179$ cm³, $\tfrac{1}{56} \approx 0.018$ |
| [[CAL1 HW 2.9 Questions#ST 2.9.43\|ST 2.9.43]] | (a) $\Delta V \approx 2\pi rh\,\Delta r$; (b) $\pi h(\Delta r)^{2}$ |
| [[CAL1 HW 2.9 Questions#ST 2.9.45\|ST 2.9.45]] | Proof |

## ST §2.9 Linear Approximations and Differentials

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Linearization]]** of $f$ at $a$: $L(x) = f(a) + f'(a)(x - a)$, the [[Tangent Line]] at $(a, f(a))$. The **[[Linear Approximation]]** is $f(x) \approx L(x)$ for $x$ near $a$; choose $a$ close to $x$ with $f(a)$ and $f'(a)$ easy to compute.
> - **[[Differential]]**: for $y = f(x)$, $dy = f'(x)\,dx$. The actual change is $\Delta y = f(x + \Delta x) - f(x)$; with $dx = \Delta x$, $\Delta y \approx dy$. In a picture, $dy$ is the rise of the tangent line and $\Delta y$ the rise of the curve.
> - **Errors**: if $x$ is measured with error $dx$, the error in $V = f(x)$ is about $dV = f'(x)\,dx$; the relative error is $\dfrac{\Delta V}{V} \approx \dfrac{dV}{V}$, and the percentage error is the relative error times 100 %.
> - Each answer is written as on an exam paper: $f$, $a$, $f(a)$, $f'(a)$, then $L$ or $dy$, then a Hence line. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 2.9.3
Question: [[CAL1 HW 2.9 Questions#ST 2.9.3|ST 2.9.3]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(x) = x^{1/3} \implies f(8) = 2 \\
> &f'(x) = \tfrac{1}{3}x^{-2/3} \implies f'(8) = \frac{1}{3 \cdot 8^{2/3}} = \frac{1}{3 \cdot 4} = \frac{1}{12} \\
> &L(x) = f(8) + f'(8)(x - 8) = 2 + \tfrac{1}{12}(x - 8) = \tfrac{1}{12}x + \tfrac{4}{3}
> \end{aligned}
> $$
> Hence $L(x) = \tfrac{1}{12}x + \tfrac{4}{3}$.
>
> \# $8^{2/3} = (\sqrt[3]{8})^{2} = 4$. For example, $\sqrt[3]{8.6} \approx L(8.6) = 2 + \tfrac{0.6}{12} = 2.05$ (actual value $2.0488\ldots$).

### ST 2.9.13
Question: [[CAL1 HW 2.9 Questions#ST 2.9.13|ST 2.9.13]]

> [!solution] Solution
> $$
> dy = \frac{2(1 + 3u) - (1 + 2u) \cdot 3}{(1 + 3u)^{2}}\,du = \frac{2 + 6u - 3 - 6u}{(1 + 3u)^{2}}\,du = -\frac{1}{(1 + 3u)^{2}}\,du \qquad \text{(Quotient Rule)}
> $$
> Hence $dy = -\dfrac{1}{(1 + 3u)^{2}}\,du$.
>
> \# The variable is $u$, so the differential is written with $du$, not $dx$.

### ST 2.9.17
Question: [[CAL1 HW 2.9 Questions#ST 2.9.17|ST 2.9.17]]

> [!solution] Solution
> $$
> dy = \frac{1}{2\sqrt{t - \cos t}} \cdot (1 + \sin t)\,dt = \frac{1 + \sin t}{2\sqrt{t - \cos t}}\,dt \qquad \text{(Chain Rule)}
> $$
> Hence $dy = \dfrac{1 + \sin t}{2\sqrt{t - \cos t}}\,dt$.
>
> \# The inner function is $t - \cos t$, whose derivative is $1 - (-\sin t) = 1 + \sin t$.

### ST 2.9.21
Question: [[CAL1 HW 2.9 Questions#ST 2.9.21|ST 2.9.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{(a) } dy = \frac{1}{2\sqrt{3 + x^{2}}} \cdot 2x\,dx = \frac{x}{\sqrt{3 + x^{2}}}\,dx \\
> &\text{(b) } x = 1,\ dx = -0.1: \ dy = \frac{1}{\sqrt{4}} \cdot (-0.1) = -0.05
> \end{aligned}
> $$
> Hence (a) $dy = \dfrac{x}{\sqrt{3 + x^{2}}}\,dx$; (b) $dy = -0.05$.
>
> \# A negative $dx$ means $x$ decreases from 1 to 0.9, and $y$ decreases by about 0.05 (actual $\Delta y = \sqrt{3.81} - 2 \approx -0.0481$).

### ST 2.9.23
Question: [[CAL1 HW 2.9 Questions#ST 2.9.23|ST 2.9.23]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(x) = x^{2} - 4x,\quad f'(x) = 2x - 4 \\
> &\Delta y = f(3.5) - f(3) = (12.25 - 14) - (9 - 12) = -1.75 + 3 = 1.25 \\
> &dy = f'(3)\,dx = (2 \cdot 3 - 4)(0.5) = 1
> \end{aligned}
> $$
> Hence $\Delta y = 1.25$ and $dy = 1$.
>
> ![ST 2.9.23 figure|420](../Attachments/CAL1%20HW%202.9%20Solutions%20fig%2023.png)
>
> \# In the diagram, $dx = \Delta x$ runs along the horizontal from $x = 3$ to $3.5$; $dy$ is the rise of the tangent line at $(3, -3)$, and $\Delta y$ the rise of the curve. The parabola is concave upward, so it lies above its tangent and $\Delta y > dy$.

### ST 2.9.29
Question: [[CAL1 HW 2.9 Questions#ST 2.9.29|ST 2.9.29]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f'(x) = -\frac{1}{2\sqrt{5 - x}} \implies f'(1) = -\frac{1}{4},\quad dy = -\frac{1}{4}\,dx \\[4pt]
> &1 \to 1.05: \ \Delta y = \sqrt{3.95} - 2 \approx -0.012539,\quad dy = -\tfrac{1}{4}(0.05) = -0.0125 \\
> &\qquad \lvert \Delta y - dy \rvert \approx 0.000039 \\
> &1 \to 1.01: \ \Delta y = \sqrt{3.99} - 2 \approx -0.0025016,\quad dy = -\tfrac{1}{4}(0.01) = -0.0025 \\
> &\qquad \lvert \Delta y - dy \rvert \approx 0.0000016
> \end{aligned}
> $$
> Hence yes: $\Delta y \approx dy$ becomes better as $\Delta x$ gets smaller.
>
> \# When $\Delta x$ is divided by 5, the error $\lvert \Delta y - dy \rvert$ is divided by about 25: the error behaves like $(\Delta x)^{2}$, while $\Delta y$ itself is only divided by 5. That is why the linear approximation is good near $a$.

### ST 2.9.31
Question: [[CAL1 HW 2.9 Questions#ST 2.9.31|ST 2.9.31]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(x) = x^{4},\ a = 2: \ f(2) = 16,\ f'(x) = 4x^{3} \implies f'(2) = 32 \\
> &(1.999)^{4} = f(1.999) \approx L(1.999) = 16 + 32(1.999 - 2) = 16 - 0.032 = 15.968
> \end{aligned}
> $$
> Hence $(1.999)^{4} \approx 15.968$.
>
> \# The actual value is $15.96802\ldots$; the error is about $0.000024$.

### ST 2.9.33
Question: [[CAL1 HW 2.9 Questions#ST 2.9.33|ST 2.9.33]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(x) = \sqrt[3]{x},\ a = 1000: \ f(1000) = 10,\ f'(x) = \tfrac{1}{3}x^{-2/3} \implies f'(1000) = \frac{1}{3 \cdot 100} = \frac{1}{300} \\
> &\sqrt[3]{1001} \approx L(1001) = 10 + \tfrac{1}{300}(1001 - 1000) = 10 + 0.00\overline{3} = 10.00\overline{3}
> \end{aligned}
> $$
> Hence $\sqrt[3]{1001} \approx 10.0033$.
>
> \# $1000^{2/3} = (\sqrt[3]{1000})^{2} = 100$. The actual value is $10.003332\ldots$.

### ST 2.9.38
Question: [[CAL1 HW 2.9 Questions#ST 2.9.38|ST 2.9.38]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(x) = \sqrt{x},\ a = 4: \ f(4) = 2,\ f'(x) = \frac{1}{2\sqrt{x}} \implies f'(4) = \frac{1}{4} \\
> &L(x) = 2 + \tfrac{1}{4}(x - 4) \implies L(4.02) = 2 + \tfrac{1}{4}(0.02) = 2.005
> \end{aligned}
> $$
> Hence $2.005$ is the linear approximation $\sqrt{4.02} \approx L(4.02)$ of $\sqrt{x}$ at $a = 4$, and it is reasonable because $4.02$ is very close to $4$, where the curve $y = \sqrt{x}$ and its tangent line almost coincide.
>
> \# The same in differentials: $dy = \tfrac{1}{4}\,dx$ with $dx = 0.02$ gives $dy = 0.005$, so $\sqrt{4.02} \approx 2 + 0.005$. The actual value is $2.0049938\ldots$.

### ST 2.9.39
Question: [[CAL1 HW 2.9 Questions#ST 2.9.39|ST 2.9.39]]

> [!solution] Solution
> $$
> \begin{aligned}
> &x = 30,\ dx = 0.1 \\[4pt]
> &\text{(a) } V = x^{3}: \ dV = 3x^{2}\,dx = 3 \cdot 900 \cdot 0.1 = 270 \\
> &\qquad \frac{dV}{V} = \frac{3x^{2}\,dx}{x^{3}} = 3\,\frac{dx}{x} = 3 \cdot \frac{0.1}{30} = 0.01 \\[4pt]
> &\text{(b) } S = 6x^{2}: \ dS = 12x\,dx = 12 \cdot 30 \cdot 0.1 = 36 \\
> &\qquad \frac{dS}{S} = \frac{12x\,dx}{6x^{2}} = 2\,\frac{dx}{x} = 2 \cdot \frac{0.1}{30} = \frac{1}{150} \approx 0.0067
> \end{aligned}
> $$
> Hence (a) the maximum error is about 270 cm³, the relative error 0.01, and the percentage error 1 %; (b) the maximum error is about 36 cm², the relative error $\tfrac{1}{150} \approx 0.0067$, and the percentage error about 0.67 %.
>
> \# A power multiplies the relative error by its exponent: $\dfrac{d(x^{n})}{x^{n}} = n\,\dfrac{dx}{x}$. The edge has relative error $\tfrac{1}{300}$, so the volume has 3 times and the area 2 times that.

### ST 2.9.41
Question: [[CAL1 HW 2.9 Questions#ST 2.9.41|ST 2.9.41]]

> [!solution] Solution
> $$
> \begin{aligned}
> &C = 2\pi r \implies r = \frac{C}{2\pi};\quad C = 84,\ dC = 0.5 \\[4pt]
> &\text{(a) } S = 4\pi r^{2} = \frac{C^{2}}{\pi}: \ dS = \frac{2C}{\pi}\,dC = \frac{2 \cdot 84 \cdot 0.5}{\pi} = \frac{84}{\pi} \approx 26.7 \\
> &\qquad \frac{dS}{S} = 2\,\frac{dC}{C} = \frac{2 \cdot 0.5}{84} = \frac{1}{84} \approx 0.012 \\[4pt]
> &\text{(b) } V = \frac{4}{3}\pi r^{3} = \frac{C^{3}}{6\pi^{2}}: \ dV = \frac{C^{2}}{2\pi^{2}}\,dC = \frac{84^{2} \cdot 0.5}{2\pi^{2}} = \frac{1764}{\pi^{2}} \approx 178.7 \\
> &\qquad \frac{dV}{V} = 3\,\frac{dC}{C} = \frac{3 \cdot 0.5}{84} = \frac{1}{56} \approx 0.018
> \end{aligned}
> $$
> Hence (a) the maximum error in the surface area is about $\dfrac{84}{\pi} \approx 27$ cm², relative error $\dfrac{1}{84} \approx 0.012$; (b) the maximum error in the volume is about $\dfrac{1764}{\pi^{2}} \approx 179$ cm³, relative error $\dfrac{1}{56} \approx 0.018$.
>
> \# Write $S$ and $V$ in terms of the measured quantity $C$, so that $dC = 0.5$ can be used directly: $4\pi\left(\tfrac{C}{2\pi}\right)^{2} = \tfrac{C^{2}}{\pi}$ and $\tfrac{4}{3}\pi\left(\tfrac{C}{2\pi}\right)^{3} = \tfrac{C^{3}}{6\pi^{2}}$.

### ST 2.9.43
Question: [[CAL1 HW 2.9 Questions#ST 2.9.43|ST 2.9.43]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{(a) } V = \pi r^{2}h \ (h \text{ fixed}): \ \Delta V \approx dV = 2\pi rh\,dr = 2\pi rh\,\Delta r \\[4pt]
> &\text{(b) } \Delta V = \pi(r + \Delta r)^{2}h - \pi r^{2}h = 2\pi rh\,\Delta r + \pi h(\Delta r)^{2} \\
> &\qquad \text{error} = \Delta V - dV = \pi h(\Delta r)^{2}
> \end{aligned}
> $$
> Hence (a) the shell has volume $\Delta V \approx 2\pi rh\,\Delta r$; (b) the error of this formula is $\pi h(\Delta r)^{2}$.
>
> \# The shell is the region between the cylinders of radius $r$ and $r + \Delta r$, so its volume is $\Delta V$. Unrolled, it is almost a thin slab: circumference $2\pi r$ times height $h$ times thickness $\Delta r$. The error divided by the approximation is $\tfrac{\Delta r}{2r}$, small for a thin shell.

### ST 2.9.45
Question: [[CAL1 HW 2.9 Questions#ST 2.9.45|ST 2.9.45]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{pf: } V \text{ is constant and } I = \frac{V}{R} = VR^{-1}. \\
> &dI = -VR^{-2}\,dR = -\frac{V}{R^{2}}\,dR \\
> &\frac{dI}{I} = \frac{-\frac{V}{R^{2}}\,dR}{\frac{V}{R}} = -\frac{dR}{R} \\
> &\implies \left\lvert \frac{\Delta I}{I} \right\rvert \approx \left\lvert \frac{dI}{I} \right\rvert = \left\lvert \frac{dR}{R} \right\rvert \\[4pt]
> &\text{Hence the relative error in } I \text{ is about the same in magnitude as the relative error in } R. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The minus sign says the errors go in opposite directions: if $R$ is measured too large, $I$ comes out too small, by about the same fraction. This is the rule of Exercise 39 with exponent $n = -1$.
