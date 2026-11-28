---
course: [CAL1]
semester: "115-1"
chapter: ["5.3"]
tags: [calculus, homework, solutions, integrals, volumes]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §5.3, pp. 388-392, scanned PDF (the method of cylindrical shells, Examples 1-5)"
created: 2026-11-25
questions: "[[CAL1 HW 5.3 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 5.3 Questions#ST 5.3.3\|ST 5.3.3]] | (a) $\int_0^{\sqrt{\pi/2}} 2\pi x\cos(x^2)\,dx$; (b) $\pi$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.5\|ST 5.3.5]] | $\int_0^2 2\pi x\sqrt[4]{x}\,dx$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.6\|ST 5.3.6]] | $\int_0^8 2\pi y\sqrt[3]{y}\,dy$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.7\|ST 5.3.7]] | $\int_0^2 2\pi(3 - y)(4 - y^2)\,dy$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.8\|ST 5.3.8]] | $\int_0^3 2\pi(7 - x)(3x - x^2)\,dx$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.9\|ST 5.3.9]] | $\tfrac{128\pi}{5}$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.11\|ST 5.3.11]] | $6\pi$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.13\|ST 5.3.13]] | $\tfrac{2\pi}{3}(27 - 5\sqrt{5}) \approx 33.13$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.15\|ST 5.3.15]] | $4\pi$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.17\|ST 5.3.17]] | $192\pi$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.19\|ST 5.3.19]] | $\tfrac{16\pi}{3}$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.21\|ST 5.3.21]] | (a) and (b) $\tfrac{384\pi}{5}$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.22\|ST 5.3.22]] | (a) and (b) $\tfrac{32768\pi}{35} \approx 2941.25$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.23\|ST 5.3.23]] | (b) $\int_0^4 2\pi(x + 2)(4x - x^2)\,dx$; (c) $\tfrac{256\pi}{3}$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.24\|ST 5.3.24]] | (b) $\int_0^1 2\pi(y + 1)(\sqrt[3]{y} - y^2)\,dy$; (c) $\tfrac{25\pi}{21}$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.25\|ST 5.3.25]] | $\tfrac{264\pi}{5}$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.29\|ST 5.3.29]] | $\tfrac{13\pi}{3}$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.39\|ST 5.3.39]] | The region under $y = x^4$, $0 \le x \le 3$, rotated about the $y$-axis |
| [[CAL1 HW 5.3 Questions#ST 5.3.41\|ST 5.3.41]] | The region bounded by $x = 1/y^2$, $x = 0$, $y = 1$, $y = 4$, rotated about $y = -2$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.47\|ST 5.3.47]] | (a) $\int_0^1 2\pi x(2 - x - \sqrt[3]{x})\,dx$; (b) $\tfrac{10\pi}{21}$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.49\|ST 5.3.49]] | (a) $\int_0^\pi \pi\sin x\,dx$; (b) $2\pi$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.51\|ST 5.3.51]] | (a) $\int_0^{1/2} 2\pi(x + 2)(x^2 - x^3)\,dx$; (b) $\tfrac{59\pi}{480}$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.53\|ST 5.3.53]] | $8\pi$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.57\|ST 5.3.57]] | $\tfrac{4\pi}{3}$ |
| [[CAL1 HW 5.3 Questions#ST 5.3.59\|ST 5.3.59]] | $\tfrac{117\pi}{5}$ |

## ST §5.3 Volumes by Cylindrical Shells

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Method of Cylindrical Shells]]**: a shell with radius $r$, height $h$ and thickness $\Delta r$ has volume $2\pi rh\,\Delta r$, that is, [circumference][height][thickness]. Rotating the region under $y = f(x)$, $a \le x \le b$ ($0 \le a < b$), about the $y$-axis gives $V = \int_a^b 2\pi x f(x)\,dx$.
> - **Shells about any line**: $V = \int 2\pi\,r\,h$, integrated over the strips. Cut the region into strips parallel to the axis of rotation: vertical strips ($dx$) for a vertical axis, horizontal strips ($dy$) for a horizontal axis. $r$ is the distance from the strip to the axis ($x - c$ or $c - x$ for the axis $x = c$, $y - c$ or $c - y$ for $y = c$), and $h$ is the length of the strip (top minus bottom, or right minus left).
> - **[[Disk Method]] and [[Washer Method]]** (§5.2): strips perpendicular to the axis. A disk of radius $R$ gives $V = \int \pi R^2$; a washer gives $V = \int \pi\left(r_{\mathrm{out}}^2 - r_{\mathrm{in}}^2\right)$, where $r_{\mathrm{out}}$ and $r_{\mathrm{in}}$ are the distances from the axis to the far and the near end of the strip.
> - **Which method** ("any method"): the variable of integration is the direction of the strip's thickness. Choose the strip that gives one integral with easy limits and an integrand you can integrate.
> - **[[Substitution Rule]]**, for Exercises 3, 13 and 57.
> - Each answer is written as on an exam paper: the strip ($r$, $h$ and the limits), the integral, the computation, then the conclusion on a Hence line. In each figure the red strip is the typical strip. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 5.3.3
Question: [[CAL1 HW 5.3 Questions#ST 5.3.3|ST 5.3.3]]

> [!solution] Solution
> ![ST 5.3.3 figure|400](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%203.png)
>
> Shell at $x$: $r = x$, $h = \cos(x^2)$, $0 \le x \le \sqrt{\pi/2}$.
>
> **(a)**
> $$
> V = \int_0^{\sqrt{\pi/2}} 2\pi x\cos(x^2)\,dx
> $$
> **(b)** Let $u = x^2$. Then $du = 2x\,dx$. When $x = 0$, $u = 0$; when $x = \sqrt{\pi/2}$, $u = \tfrac{\pi}{2}$.
> $$
> V = \pi\int_0^{\pi/2} \cos u\,du = \pi\Big[\sin u\Big]_0^{\pi/2} = \pi(1 - 0) = \pi
> $$
> Hence $V = \pi$.
>
> \# The axis is vertical, so the strips are vertical and the variable is $x$. The shell radius $x$ is exactly what the substitution needs: $2\pi x\,dx = \pi\,du$. Washers would need $x$ in terms of $y$ from $y = \cos(x^2)$.

### ST 5.3.5
Question: [[CAL1 HW 5.3 Questions#ST 5.3.5|ST 5.3.5]]

> [!solution] Solution
> ![ST 5.3.5 figure|400](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%205.png)
>
> Shell at $x$: $r = x$, $h = \sqrt[4]{x}$, $0 \le x \le 2$. Hence
> $$
> V = \int_0^2 2\pi x\sqrt[4]{x}\,dx
> $$
>
> \# The region lies under $y = \sqrt[4]{x}$ between $x = 0$ and $x = 2$. The integrand can also be written $2\pi x^{5/4}$.

### ST 5.3.6
Question: [[CAL1 HW 5.3 Questions#ST 5.3.6|ST 5.3.6]]

> [!solution] Solution
> ![ST 5.3.6 figure|360](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%206.png)
>
> $y = x^3 \iff x = \sqrt[3]{y}$; the curves meet at $(2, 8)$.
>
> Shell at $y$: $r = y$, $h = \sqrt[3]{y} - 0 = \sqrt[3]{y}$, $0 \le y \le 8$. Hence
> $$
> V = \int_0^8 2\pi y\sqrt[3]{y}\,dy
> $$
>
> \# The axis is horizontal, so the shells come from horizontal strips and the variable is $y$; each strip runs from $x = 0$ to $x = \sqrt[3]{y}$. Washers would give $\int_0^2 \pi(64 - x^6)\,dx$, the same number $\tfrac{768\pi}{7}$.

### ST 5.3.7
Question: [[CAL1 HW 5.3 Questions#ST 5.3.7|ST 5.3.7]]

> [!solution] Solution
> ![ST 5.3.7 figure|420](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%207.png)
>
> Region: $-4 \le x \le 0$, $0 \le y \le \sqrt{x + 4}$; at $x = 0$, $y = 2$. Also $y = \sqrt{x + 4} \iff x = y^2 - 4$ $(y \ge 0)$.
>
> Shell at $y$: $r = 3 - y$, $h = 0 - (y^2 - 4) = 4 - y^2$, $0 \le y \le 2$. Hence
> $$
> V = \int_0^2 2\pi(3 - y)(4 - y^2)\,dy
> $$
>
> \# The axis $y = 3$ is horizontal, so the strips are horizontal. It lies above the region ($y \le 2$), so the distance is $3 - y$, not $y - 3$. The strip runs from the curve $x = y^2 - 4$ on the left to the $y$-axis $x = 0$ on the right. (The value is $24\pi$.)

### ST 5.3.8
Question: [[CAL1 HW 5.3 Questions#ST 5.3.8|ST 5.3.8]]

> [!solution] Solution
> ![ST 5.3.8 figure|440](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%208.png)
>
> $4x - x^2 = x \iff x(3 - x) = 0 \iff x = 0, 3$. For $0 \le x \le 3$, $4x - x^2 \ge x$.
>
> Shell at $x$: $r = 7 - x$, $h = (4x - x^2) - x = 3x - x^2$, $0 \le x \le 3$. Hence
> $$
> V = \int_0^3 2\pi(7 - x)(3x - x^2)\,dx
> $$
>
> \# The axis $x = 7$ is vertical and lies to the right of the region, so $r = 7 - x$. (The value is $\tfrac{99\pi}{2}$.)

### ST 5.3.9
Question: [[CAL1 HW 5.3 Questions#ST 5.3.9|ST 5.3.9]]

> [!solution] Solution
> ![ST 5.3.9 figure|400](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%209.png)
>
> Shell at $x$: $r = x$, $h = \sqrt{x}$, $0 \le x \le 4$.
> $$
> V = \int_0^4 2\pi x\sqrt{x}\,dx = 2\pi\int_0^4 x^{3/2}\,dx = 2\pi\Big[\tfrac{2}{5}x^{5/2}\Big]_0^4 = 2\pi \cdot \tfrac{2}{5} \cdot 32 = \tfrac{128\pi}{5}
> $$
> Hence $V = \tfrac{128\pi}{5}$.
>
> \# $4^{5/2} = (\sqrt{4})^5 = 32$.

### ST 5.3.11
Question: [[CAL1 HW 5.3 Questions#ST 5.3.11|ST 5.3.11]]

> [!solution] Solution
> ![ST 5.3.11 figure|400](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2011.png)
>
> Shell at $x$: $r = x$, $h = \tfrac{1}{x}$, $1 \le x \le 4$.
> $$
> V = \int_1^4 2\pi x \cdot \frac{1}{x}\,dx = \int_1^4 2\pi\,dx = 2\pi(4 - 1) = 6\pi
> $$
> Hence $V = 6\pi$.
>
> \# Every shell has $rh = 1$, so the volume is $2\pi$ times the length of $[1, 4]$.

### ST 5.3.13
Question: [[CAL1 HW 5.3 Questions#ST 5.3.13|ST 5.3.13]]

> [!solution] Solution
> ![ST 5.3.13 figure|400](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2013.png)
>
> Shell at $x$: $r = x$, $h = \sqrt{5 + x^2}$, $0 \le x \le 2$.
>
> Let $u = 5 + x^2$. Then $du = 2x\,dx$. When $x = 0$, $u = 5$; when $x = 2$, $u = 9$.
> $$
> V = \int_0^2 2\pi x\sqrt{5 + x^2}\,dx = \pi\int_5^9 u^{1/2}\,du = \pi\Big[\tfrac{2}{3}u^{3/2}\Big]_5^9 = \tfrac{2\pi}{3}\left(27 - 5\sqrt{5}\right)
> $$
> Hence $V = \tfrac{2\pi}{3}(27 - 5\sqrt{5}) \approx 33.13$.
>
> \# $2\pi x\,dx = \pi\,du$, $9^{3/2} = 27$ and $5^{3/2} = 5\sqrt{5}$.

### ST 5.3.15
Question: [[CAL1 HW 5.3 Questions#ST 5.3.15|ST 5.3.15]]

> [!solution] Solution
> ![ST 5.3.15 figure|360](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2015.png)
>
> $xy = 1 \iff x = \tfrac{1}{y}$. Region: $1 \le y \le 3$, $0 \le x \le \tfrac{1}{y}$.
>
> Shell at $y$: $r = y$, $h = \tfrac{1}{y}$, $1 \le y \le 3$.
> $$
> V = \int_1^3 2\pi y \cdot \frac{1}{y}\,dy = \int_1^3 2\pi\,dy = 2\pi(3 - 1) = 4\pi
> $$
> Hence $V = 4\pi$.
>
> \# The axis is horizontal, so the strips are horizontal and the variable is $y$; each strip runs from the $y$-axis to the curve $x = 1/y$.

### ST 5.3.17
Question: [[CAL1 HW 5.3 Questions#ST 5.3.17|ST 5.3.17]]

> [!solution] Solution
> ![ST 5.3.17 figure|400](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2017.png)
>
> $y = x^{3/2} \iff x = y^{2/3}$ $(x \ge 0)$; the curves meet at $(4, 8)$. Region: $0 \le y \le 8$, $0 \le x \le y^{2/3}$.
>
> Shell at $y$: $r = y$, $h = y^{2/3}$, $0 \le y \le 8$.
> $$
> V = \int_0^8 2\pi y \cdot y^{2/3}\,dy = 2\pi\int_0^8 y^{5/3}\,dy = 2\pi\Big[\tfrac{3}{8}y^{8/3}\Big]_0^8 = 2\pi \cdot \tfrac{3}{8} \cdot 256 = 192\pi
> $$
> Hence $V = 192\pi$.
>
> \# $8^{8/3} = (\sqrt[3]{8})^8 = 2^8 = 256$. Check with washers: $\int_0^4 \pi\left(8^2 - (x^{3/2})^2\right)dx = \pi(256 - 64) = 192\pi$.

### ST 5.3.19
Question: [[CAL1 HW 5.3 Questions#ST 5.3.19|ST 5.3.19]]

> [!solution] Solution
> ![ST 5.3.19 figure|380](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2019.png)
>
> $1 + (y - 2)^2 = 2 \iff (y - 2)^2 = 1 \iff y = 1, 3$. For $1 \le y \le 3$, $1 + (y - 2)^2 \le 2$.
>
> Shell at $y$: $r = y$, $h = 2 - \left[1 + (y - 2)^2\right] = -y^2 + 4y - 3$, $1 \le y \le 3$.
> $$
> \begin{aligned}
> V &= \int_1^3 2\pi y(-y^2 + 4y - 3)\,dy = 2\pi\int_1^3 (-y^3 + 4y^2 - 3y)\,dy \\
> &= 2\pi\Big[-\tfrac{y^4}{4} + \tfrac{4y^3}{3} - \tfrac{3y^2}{2}\Big]_1^3 = 2\pi\left(\tfrac{9}{4} + \tfrac{5}{12}\right) = 2\pi \cdot \tfrac{8}{3} = \tfrac{16\pi}{3}
> \end{aligned}
> $$
> Hence $V = \tfrac{16\pi}{3}$.
>
> \# The parabola has vertex $(1, 2)$ and opens to the right; the line $x = 2$ cuts it at $y = 1$ and $y = 3$. At $y = 3$ the bracket is $-\tfrac{81}{4} + 36 - \tfrac{27}{2} = \tfrac{9}{4}$; at $y = 1$ it is $-\tfrac{1}{4} + \tfrac{4}{3} - \tfrac{3}{2} = -\tfrac{5}{12}$.

### ST 5.3.21
Question: [[CAL1 HW 5.3 Questions#ST 5.3.21|ST 5.3.21]]

> [!solution] Solution
> ![ST 5.3.21 figure|640](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2021.png)
>
> $x^2 = 8\sqrt{x} \iff x^4 = 64x \iff x(x^3 - 64) = 0 \iff x = 0, 4$; the curves meet at $(0, 0)$ and $(4, 16)$. For $0 \le x \le 4$, $8\sqrt{x} \ge x^2$.
>
> **(a)** Shell at $x$: $r = x$, $h = 8\sqrt{x} - x^2$, $0 \le x \le 4$.
> $$
> \begin{aligned}
> V &= \int_0^4 2\pi x(8\sqrt{x} - x^2)\,dx = 2\pi\int_0^4 (8x^{3/2} - x^3)\,dx \\
> &= 2\pi\Big[\tfrac{16}{5}x^{5/2} - \tfrac{x^4}{4}\Big]_0^4 = 2\pi\left(\tfrac{512}{5} - 64\right) = \tfrac{384\pi}{5}
> \end{aligned}
> $$
> **(b)** $y = x^2 \iff x = \sqrt{y}$ and $y = 8\sqrt{x} \iff x = \tfrac{y^2}{64}$. Washer at $y$: $r_{\mathrm{out}} = \sqrt{y}$, $r_{\mathrm{in}} = \tfrac{y^2}{64}$, $0 \le y \le 16$.
> $$
> \begin{aligned}
> V &= \int_0^{16} \pi\left[(\sqrt{y})^2 - \left(\tfrac{y^2}{64}\right)^2\right]dy = \pi\int_0^{16} \left(y - \tfrac{y^4}{4096}\right)dy \\
> &= \pi\Big[\tfrac{y^2}{2} - \tfrac{y^5}{20480}\Big]_0^{16} = \pi\left(128 - \tfrac{256}{5}\right) = \tfrac{384\pi}{5}
> \end{aligned}
> $$
> Hence $V = \tfrac{384\pi}{5}$, both ways.
>
> \# In (b) the strip is horizontal, perpendicular to the axis, so it sweeps a washer, not a shell. Its far end is on $y = x^2$: $\sqrt{y} \ge \tfrac{y^2}{64} \iff y^{3/2} \le 64 \iff y \le 16$. $4^{5/2} = 32$; $16^5 = 1048576 = 20480 \cdot \tfrac{256}{5}$.

### ST 5.3.22
Question: [[CAL1 HW 5.3 Questions#ST 5.3.22|ST 5.3.22]]

> [!solution] Solution
> ![ST 5.3.22 figure|640](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2022.png)
>
> $x^3 = 4x^2 \iff x^2(x - 4) = 0 \iff x = 0, 4$; the curves meet at $(0, 0)$ and $(4, 64)$. For $0 \le x \le 4$, $4x^2 - x^3 = x^2(4 - x) \ge 0$.
>
> **(a)** Washer at $x$: $r_{\mathrm{out}} = 4x^2$, $r_{\mathrm{in}} = x^3$, $0 \le x \le 4$.
> $$
> \begin{aligned}
> V &= \int_0^4 \pi\left[(4x^2)^2 - (x^3)^2\right]dx = \pi\int_0^4 (16x^4 - x^6)\,dx \\
> &= \pi\Big[\tfrac{16x^5}{5} - \tfrac{x^7}{7}\Big]_0^4 = \pi\left(\tfrac{16384}{5} - \tfrac{16384}{7}\right) = \tfrac{32768\pi}{35}
> \end{aligned}
> $$
> **(b)** $y = 4x^2 \iff x = \tfrac{\sqrt{y}}{2}$ and $y = x^3 \iff x = \sqrt[3]{y}$. Shell at $y$: $r = y$, $h = \sqrt[3]{y} - \tfrac{\sqrt{y}}{2}$, $0 \le y \le 64$.
> $$
> \begin{aligned}
> V &= \int_0^{64} 2\pi y\left(y^{1/3} - \tfrac{1}{2}y^{1/2}\right)dy = 2\pi\int_0^{64} \left(y^{4/3} - \tfrac{1}{2}y^{3/2}\right)dy \\
> &= 2\pi\Big[\tfrac{3}{7}y^{7/3} - \tfrac{1}{5}y^{5/2}\Big]_0^{64} = 2\pi\left(\tfrac{3}{7} \cdot 16384 - \tfrac{1}{5} \cdot 32768\right) = \tfrac{32768\pi}{35}
> \end{aligned}
> $$
> Hence $V = \tfrac{32768\pi}{35} \approx 2941.25$, both ways.
>
> \# In (a) the strip is vertical, perpendicular to the $x$-axis, so it sweeps a washer. In (b) the right end of the strip is on $y = x^3$: $\sqrt[3]{y} \ge \tfrac{\sqrt{y}}{2} \iff y^{1/6} \le 2 \iff y \le 64$. $4^7 = 16384$, $64^{7/3} = 4^7$, $64^{5/2} = 8^5 = 32768$, and $2\pi \cdot 16384\left(\tfrac{3}{7} - \tfrac{2}{5}\right) = \tfrac{32768\pi}{35}$.

### ST 5.3.23
Question: [[CAL1 HW 5.3 Questions#ST 5.3.23|ST 5.3.23]]

> [!solution] Solution
> **(a)**
>
> ![ST 5.3.23 figure|560](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2023.png)
>
> The solid is a ring around the line $x = -2$, with a hole of radius $2$, outer radius $6$ and greatest height $4$. A typical shell is the vertical strip at $x$ swept around $x = -2$ (red).
>
> **(b)** Shell at $x$: $r = x - (-2) = x + 2$, $h = 4x - x^2$, $0 \le x \le 4$.
> $$
> V = \int_0^4 2\pi(x + 2)(4x - x^2)\,dx
> $$
> **(c)**
> $$
> \begin{aligned}
> V &= 2\pi\int_0^4 (-x^3 + 2x^2 + 8x)\,dx = 2\pi\Big[-\tfrac{x^4}{4} + \tfrac{2x^3}{3} + 4x^2\Big]_0^4 \\
> &= 2\pi\left(-64 + \tfrac{128}{3} + 64\right) = \tfrac{256\pi}{3}
> \end{aligned}
> $$
> Hence $V = \tfrac{256\pi}{3}$.
>
> \# The axis lies $2$ units to the left of the $y$-axis, so every radius is $2$ more than $x$. $(x + 2)(4x - x^2) = 4x^2 - x^3 + 8x - 2x^2 = -x^3 + 2x^2 + 8x$.

### ST 5.3.24
Question: [[CAL1 HW 5.3 Questions#ST 5.3.24|ST 5.3.24]]

> [!solution] Solution
> **(a)**
>
> ![ST 5.3.24 figure|420](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2024.png)
>
> The solid is a hollow horn around the line $y = -1$: its outer surface comes from $y = \sqrt{x}$ and its inner surface from $y = x^3$. A typical shell is the horizontal strip at height $y$ swept around $y = -1$, a horizontal tube (red).
>
> **(b)** $y = \sqrt{x} \iff x = y^2$ and $y = x^3 \iff x = \sqrt[3]{y}$. For $0 \le y \le 1$, $y^2 \le \sqrt[3]{y}$.
>
> Shell at $y$: $r = y - (-1) = y + 1$, $h = \sqrt[3]{y} - y^2$, $0 \le y \le 1$.
> $$
> V = \int_0^1 2\pi(y + 1)\left(\sqrt[3]{y} - y^2\right)dy
> $$
> **(c)**
> $$
> \begin{aligned}
> V &= 2\pi\int_0^1 \left(y^{4/3} + y^{1/3} - y^3 - y^2\right)dy = 2\pi\Big[\tfrac{3}{7}y^{7/3} + \tfrac{3}{4}y^{4/3} - \tfrac{y^4}{4} - \tfrac{y^3}{3}\Big]_0^1 \\
> &= 2\pi\left(\tfrac{3}{7} + \tfrac{3}{4} - \tfrac{1}{4} - \tfrac{1}{3}\right) = 2\pi \cdot \tfrac{25}{42} = \tfrac{25\pi}{21}
> \end{aligned}
> $$
> Hence $V = \tfrac{25\pi}{21}$.
>
> \# The strip at height $y$ runs from $y = \sqrt{x}$ on the left ($x = y^2$) to $y = x^3$ on the right ($x = \sqrt[3]{y}$). Check with washers: $\int_0^1 \pi\left[(\sqrt{x} + 1)^2 - (x^3 + 1)^2\right]dx = \tfrac{25\pi}{21}$.

### ST 5.3.25
Question: [[CAL1 HW 5.3 Questions#ST 5.3.25|ST 5.3.25]]

> [!solution] Solution
> ![ST 5.3.25 figure|400](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2025.png)
>
> $x^3 = 8 \iff x = 2$. Region: $0 \le x \le 2$, $x^3 \le y \le 8$.
>
> Shell at $x$: $r = 3 - x$, $h = 8 - x^3$, $0 \le x \le 2$.
> $$
> \begin{aligned}
> V &= \int_0^2 2\pi(3 - x)(8 - x^3)\,dx = 2\pi\int_0^2 (x^4 - 3x^3 - 8x + 24)\,dx \\
> &= 2\pi\Big[\tfrac{x^5}{5} - \tfrac{3x^4}{4} - 4x^2 + 24x\Big]_0^2 = 2\pi\left(\tfrac{32}{5} - 12 - 16 + 48\right) = \tfrac{264\pi}{5}
> \end{aligned}
> $$
> Hence $V = \tfrac{264\pi}{5}$.
>
> \# The axis $x = 3$ lies to the right of the region ($x \le 2$), so $r = 3 - x$. $(3 - x)(8 - x^3) = 24 - 3x^3 - 8x + x^4$.

### ST 5.3.29
Question: [[CAL1 HW 5.3 Questions#ST 5.3.29|ST 5.3.29]]

> [!solution] Solution
> ![ST 5.3.29 figure|400](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2029.png)
>
> $2y^2 = 2 \iff y = 1$ $(y \ge 0)$. Region: $0 \le y \le 1$, $2y^2 \le x \le 2$.
>
> Shell at $y$: $r = 2 - y$, $h = 2 - 2y^2$, $0 \le y \le 1$.
> $$
> \begin{aligned}
> V &= \int_0^1 2\pi(2 - y)(2 - 2y^2)\,dy = 4\pi\int_0^1 (y^3 - 2y^2 - y + 2)\,dy \\
> &= 4\pi\Big[\tfrac{y^4}{4} - \tfrac{2y^3}{3} - \tfrac{y^2}{2} + 2y\Big]_0^1 = 4\pi\left(\tfrac{1}{4} - \tfrac{2}{3} - \tfrac{1}{2} + 2\right) = 4\pi \cdot \tfrac{13}{12} = \tfrac{13\pi}{3}
> \end{aligned}
> $$
> Hence $V = \tfrac{13\pi}{3}$.
>
> \# The condition $y \ge 0$ keeps only the upper half of the parabola, so the $x$-axis also bounds the region. The axis $y = 2$ is horizontal and lies above the region, so the strips are horizontal and $r = 2 - y$. $(2 - y)(1 - y^2) = y^3 - 2y^2 - y + 2$.

### ST 5.3.39
Question: [[CAL1 HW 5.3 Questions#ST 5.3.39|ST 5.3.39]]

> [!solution] Solution
> ![ST 5.3.39 figure|380](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2039.png)
>
> $\int_0^3 2\pi x^5\,dx = \int_0^3 2\pi \cdot x \cdot x^4\,dx$: shells with $r = x$, $h = x^4$, $0 \le x \le 3$.
>
> Hence the solid is obtained by rotating the region under $y = x^4$ (above $y = 0$), $0 \le x \le 3$, about the $y$-axis.
>
> \# Read the integrand as $2\pi \cdot r \cdot h$. The variable is $x$, so the strips are vertical and the axis is vertical; $r = x$ is the distance to $x = 0$, the $y$-axis. (The volume is $\tfrac{2\pi \cdot 3^6}{6} = 243\pi$.)

### ST 5.3.41
Question: [[CAL1 HW 5.3 Questions#ST 5.3.41|ST 5.3.41]]

> [!solution] Solution
> ![ST 5.3.41 figure|360](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2041.png)
>
> $2\pi\int_1^4 \dfrac{y + 2}{y^2}\,dy = \int_1^4 2\pi(y + 2) \cdot \dfrac{1}{y^2}\,dy$: shells with $r = y + 2 = y - (-2)$, $h = \tfrac{1}{y^2}$, $1 \le y \le 4$.
>
> Hence the solid is obtained by rotating the region bounded by $x = \tfrac{1}{y^2}$, $x = 0$, $y = 1$ and $y = 4$ about the line $y = -2$.
>
> \# The variable is $y$, so the strips are horizontal and the axis is a horizontal line; $r = y + 2$ is the distance from height $y$ down to $y = -2$. Each strip runs from $x = 0$ to $x = 1/y^2$.

### ST 5.3.47
Question: [[CAL1 HW 5.3 Questions#ST 5.3.47|ST 5.3.47]]

> [!solution] Solution
> ![ST 5.3.47 figure|380](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2047.png)
>
> The curves meet at $(1, 0)$. Region: $0 \le x \le 1$, $x - 1 \le y \le 1 - \sqrt[3]{x}$.
>
> **(a)** Shell at $x$: $r = x$, $h = (1 - \sqrt[3]{x}) - (x - 1) = 2 - x - \sqrt[3]{x}$, $0 \le x \le 1$.
> $$
> V = \int_0^1 2\pi x\left(2 - x - \sqrt[3]{x}\right)dx
> $$
> **(b)**
> $$
> V = 2\pi\int_0^1 \left(2x - x^2 - x^{4/3}\right)dx = 2\pi\Big[x^2 - \tfrac{x^3}{3} - \tfrac{3}{7}x^{7/3}\Big]_0^1 = 2\pi\left(1 - \tfrac{1}{3} - \tfrac{3}{7}\right) = \tfrac{10\pi}{21}
> $$
> Hence $V = \tfrac{10\pi}{21}$.
>
> \# Shells, because the region is described by a top and a bottom curve over one interval $[0, 1]$. Washers would need two integrals: below the $x$-axis the right end of the strip is on $y = x - 1$, above it on $y = 1 - \sqrt[3]{x}$. $1 - \tfrac{1}{3} - \tfrac{3}{7} = \tfrac{21 - 7 - 9}{21} = \tfrac{5}{21}$.

### ST 5.3.49
Question: [[CAL1 HW 5.3 Questions#ST 5.3.49|ST 5.3.49]]

> [!solution] Solution
> ![ST 5.3.49 figure|400](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2049.png)
>
> **(a)** Disk at $x$: $R = \sqrt{\sin x}$, $0 \le x \le \pi$.
> $$
> V = \int_0^\pi \pi\left(\sqrt{\sin x}\right)^2 dx = \int_0^\pi \pi\sin x\,dx
> $$
> **(b)**
> $$
> V = \pi\Big[-\cos x\Big]_0^\pi = \pi\big(1 - (-1)\big) = 2\pi
> $$
> Hence $V = 2\pi$.
>
> \# Disks, because the region touches the axis and squaring $R$ removes the root. Shells would need $x$ in terms of $y$ from $y = \sqrt{\sin x}$, on two branches.

### ST 5.3.51
Question: [[CAL1 HW 5.3 Questions#ST 5.3.51|ST 5.3.51]]

> [!solution] Solution
> ![ST 5.3.51 figure|440](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2051.png)
>
> Region: $0 \le x \le \tfrac{1}{2}$, $x^3 \le y \le x^2$ (since $x^2 - x^3 = x^2(1 - x) \ge 0$).
>
> **(a)** Shell at $x$: $r = x - (-2) = x + 2$, $h = x^2 - x^3$, $0 \le x \le \tfrac{1}{2}$.
> $$
> V = \int_0^{1/2} 2\pi(x + 2)(x^2 - x^3)\,dx
> $$
> **(b)**
> $$
> \begin{aligned}
> V &= 2\pi\int_0^{1/2} (-x^4 - x^3 + 2x^2)\,dx = 2\pi\Big[-\tfrac{x^5}{5} - \tfrac{x^4}{4} + \tfrac{2x^3}{3}\Big]_0^{1/2} \\
> &= 2\pi\left(-\tfrac{1}{160} - \tfrac{1}{64} + \tfrac{1}{12}\right) = 2\pi \cdot \tfrac{59}{960} = \tfrac{59\pi}{480}
> \end{aligned}
> $$
> Hence $V = \tfrac{59\pi}{480}$.
>
> \# Shells, because the axis is vertical and the region has one top curve and one bottom curve. $(x + 2)(x^2 - x^3) = -x^4 - x^3 + 2x^2$; with the common denominator $960$: $-6 - 15 + 80 = 59$.

### ST 5.3.53
Question: [[CAL1 HW 5.3 Questions#ST 5.3.53|ST 5.3.53]]

> [!solution] Solution
> ![ST 5.3.53 figure|420](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2053.png)
>
> $-x^2 + 6x - 8 = -(x - 2)(x - 4) = 0 \iff x = 2, 4$. Region: $2 \le x \le 4$, $0 \le y \le -x^2 + 6x - 8$.
>
> Shell at $x$: $r = x$, $h = -x^2 + 6x - 8$, $2 \le x \le 4$.
> $$
> \begin{aligned}
> V &= \int_2^4 2\pi x(-x^2 + 6x - 8)\,dx = 2\pi\int_2^4 (-x^3 + 6x^2 - 8x)\,dx \\
> &= 2\pi\Big[-\tfrac{x^4}{4} + 2x^3 - 4x^2\Big]_2^4 = 2\pi\big(0 - (-4)\big) = 8\pi
> \end{aligned}
> $$
> Hence $V = 8\pi$.
>
> \# Shells, because washers would need $x$ in terms of $y$ on both sides of the parabola, $x = 3 \pm \sqrt{1 - y}$. At $x = 4$ the bracket is $-64 + 128 - 64 = 0$; at $x = 2$ it is $-4 + 16 - 16 = -4$.

### ST 5.3.57
Question: [[CAL1 HW 5.3 Questions#ST 5.3.57|ST 5.3.57]]

> [!solution] Solution
> ![ST 5.3.57 figure|380](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2057.png)
>
> The region is the disk with center $(0, 1)$ and radius $1$. The $y$-axis passes through the center, so the left half and the right half sweep the same solid; use the right half, $0 \le x \le 1$.
>
> Shell at $x$: $r = x$, $h = \left(1 + \sqrt{1 - x^2}\right) - \left(1 - \sqrt{1 - x^2}\right) = 2\sqrt{1 - x^2}$, $0 \le x \le 1$.
>
> Let $u = 1 - x^2$. Then $du = -2x\,dx$. When $x = 0$, $u = 1$; when $x = 1$, $u = 0$.
> $$
> V = \int_0^1 2\pi x \cdot 2\sqrt{1 - x^2}\,dx = 2\pi\int_1^0 u^{1/2}\,(-du) = 2\pi\int_0^1 u^{1/2}\,du = 2\pi \cdot \tfrac{2}{3} = \tfrac{4\pi}{3}
> $$
> Hence $V = \tfrac{4\pi}{3}$.
>
> \# The solid is a ball of radius $1$, and $\tfrac{4}{3}\pi \cdot 1^3 = \tfrac{4\pi}{3}$ agrees. Integrating from $-1$ to $1$ would count the ball twice. Solving the circle for $y$: $(y - 1)^2 = 1 - x^2 \iff y = 1 \pm \sqrt{1 - x^2}$.

### ST 5.3.59
Question: [[CAL1 HW 5.3 Questions#ST 5.3.59|ST 5.3.59]]

> [!solution] Solution
> ![ST 5.3.59 figure|440](../Attachments/CAL1%20HW%205.3%20Solutions%20fig%2059.png)
>
> $x - y = 1 \iff x = y + 1$. Then $y + 1 = (y - 1)^2 \iff y^2 - 3y = 0 \iff y = 0, 3$; the curves meet at $(1, 0)$ and $(4, 3)$. For $0 \le y \le 3$, $(y - 1)^2 \le y + 1$.
>
> Washer at $y$: $r_{\mathrm{in}} = (y - 1)^2 - (-1) = (y - 1)^2 + 1$, $r_{\mathrm{out}} = (y + 1) - (-1) = y + 2$, $0 \le y \le 3$.
> $$
> \begin{aligned}
> V &= \int_0^3 \pi\left[(y + 2)^2 - \big((y - 1)^2 + 1\big)^2\right]dy = \pi\int_0^3 (-y^4 + 4y^3 - 7y^2 + 12y)\,dy \\
> &= \pi\Big[-\tfrac{y^5}{5} + y^4 - \tfrac{7y^3}{3} + 6y^2\Big]_0^3 = \pi\left(-\tfrac{243}{5} + 81 - 63 + 54\right) = \tfrac{117\pi}{5}
> \end{aligned}
> $$
> Hence $V = \tfrac{117\pi}{5}$.
>
> \# Washers, because the horizontal strip runs from the parabola to the line for every $y$, so one integral does it. Shells (vertical strips) would need two integrals: the bottom of the region is $y = 1 - \sqrt{x}$ for $0 \le x \le 1$ and $y = x - 1$ for $1 \le x \le 4$; they give the same $\tfrac{117\pi}{5}$. Expansion: $(y + 2)^2 = y^2 + 4y + 4$ and $\big((y - 1)^2 + 1\big)^2 = (y^2 - 2y + 2)^2 = y^4 - 4y^3 + 8y^2 - 8y + 4$.
