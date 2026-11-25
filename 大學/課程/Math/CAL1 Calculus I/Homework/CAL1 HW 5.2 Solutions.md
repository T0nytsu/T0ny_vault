---
course: [CAL1]
semester: "115-1"
chapter: ["5.2"]
tags: [calculus, homework, solutions, integrals, volumes]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §5.2, pp. 374-383, scanned PDF (Definition of Volume, disks and washers, Examples 1-9)"
  - "Sketches drawn with matplotlib"
created: 2026-11-25
questions: "[[CAL1 HW 5.2 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 5.2 Questions#ST 5.2.1\|ST 5.2.1]] | (a) sketch; (b) $\int_0^3 \pi(x^2 + 5)^2\,dx$; (c) $\tfrac{1068\pi}{5}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.2\|ST 5.2.2]] | (a) sketch; (b) $\int_0^4 \pi\left(x - \tfrac{1}{4}x^2\right)dx$; (c) $\tfrac{8\pi}{3}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.3\|ST 5.2.3]] | (a) sketch; (b) $\int_1^9 \pi(y - 1)^{2/3}\,dy$; (c) $\tfrac{96\pi}{5}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.4\|ST 5.2.4]] | (a) sketch; (b) $\int_1^2 \pi\left(4y^2 - \tfrac{4}{y^2}\right)dy$; (c) $\tfrac{22\pi}{3}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.5\|ST 5.2.5]] | $\int_1^3 \pi\left(1 - \tfrac{1}{x}\right)^2 dx$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.6\|ST 5.2.6]] | $\int_0^5 \pi(5 - y)\,dy$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.7\|ST 5.2.7]] | $\int_0^2 \pi(8y - y^4)\,dy$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.8\|ST 5.2.8]] | $\int_{-1}^{6} \pi\left[(x + 10)^2 - (x - 2)^4\right]dx$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.9\|ST 5.2.9]] | $\int_0^{\pi} \pi\left[(2 + \sin x)^2 - 4\right]dx$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.10\|ST 5.2.10]] | $\int_0^2 \pi\left[(6 - y^2)^2 - 4\right]dy$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.13\|ST 5.2.13]] | $8\pi$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.15\|ST 5.2.15]] | $162\pi$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.21\|ST 5.2.21]] | $\tfrac{11\pi}{30}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.23\|ST 5.2.23]] | $\tfrac{8\pi^2}{3} - 2\sqrt{3}\,\pi \approx 15.44$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.25\|ST 5.2.25]] | $\tfrac{3\pi}{5}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.27\|ST 5.2.27]] | $\tfrac{10\sqrt{2}\,\pi}{3}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.29\|ST 5.2.29]] | $\tfrac{\pi}{3}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.30\|ST 5.2.30]] | $\tfrac{2\pi}{3}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.31\|ST 5.2.31]] | $\tfrac{\pi}{3}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.32\|ST 5.2.32]] | $\tfrac{2\pi}{3}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.33\|ST 5.2.33]] | $\tfrac{\pi}{3}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.34\|ST 5.2.34]] | $\tfrac{\pi}{9}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.35\|ST 5.2.35]] | $\tfrac{13\pi}{45}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.36\|ST 5.2.36]] | $\tfrac{\pi}{15}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.37\|ST 5.2.37]] | $\tfrac{\pi}{3}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.38\|ST 5.2.38]] | $\tfrac{2\pi}{9}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.39\|ST 5.2.39]] | $\tfrac{17\pi}{45}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.40\|ST 5.2.40]] | $\tfrac{4\pi}{15}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.49\|ST 5.2.49]] | The region under $y = \sin x$, $0 \le x \le \tfrac{\pi}{2}$, rotated about the $x$-axis |
| [[CAL1 HW 5.2 Questions#ST 5.2.51\|ST 5.2.51]] | The region between $y = x^3$ and $y = x^2$, $0 \le x \le 1$, rotated about the $x$-axis |
| [[CAL1 HW 5.2 Questions#ST 5.2.53\|ST 5.2.53]] | The region between $x = \sqrt{y}$ and the $y$-axis, $0 \le y \le 4$, rotated about the $y$-axis |
| [[CAL1 HW 5.2 Questions#ST 5.2.59\|ST 5.2.59]] | $\tfrac{1}{3}\pi r^2 h$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.61\|ST 5.2.61]] | $\pi h^2\left(r - \tfrac{h}{3}\right)$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.63\|ST 5.2.63]] | $\tfrac{2}{3}b^2 h$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.65\|ST 5.2.65]] | $10\ \text{cm}^3$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.67\|ST 5.2.67]] | $24$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.73\|ST 5.2.73]] | $\tfrac{4\pi}{15}$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.75\|ST 5.2.75]] | (a) $\int_{-r}^{r} 4\pi R\sqrt{r^2 - y^2}\,dy$; (b) $2\pi^2 r^2 R$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.79\|ST 5.2.79]] | Proof: both cross-sectional areas at height $y$ equal $\pi(r^2 - y^2)$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.80\|ST 5.2.80]] | $\tfrac{16}{3}r^3$ |
| [[CAL1 HW 5.2 Questions#ST 5.2.81\|ST 5.2.81]] | $\tfrac{5}{12}\pi r^3$ |

## ST §5.2 Volumes

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Volume|Definition of volume]]** (textbook p. 376): if $S$ lies between $x = a$ and $x = b$ and the cross-section of $S$ in the plane through $x$ perpendicular to the $x$-axis has area $A(x)$, with $A$ continuous, then $V = \int_a^b A(x)\,dx$. With slices perpendicular to the $y$-axis, $V = \int_c^d A(y)\,dy$.
> - **[[Solid of Revolution|Solids of revolution]]**: slice perpendicular to the axis of rotation. Rotation about a horizontal line → slices at $x$, integrate in $x$; about a vertical line → slices at $y$, integrate in $y$, so the curves must be written as $x = \dots$
> - **[[Disk Method|Disk]]**: the region reaches the axis; $A = \pi(\text{radius})^2$. **[[Washer Method|Washer]]**: there is a gap between the region and the axis; $A = \pi(\text{outer radius})^2 - \pi(\text{inner radius})^2$. A radius is a distance to the axis: about $y = c$ it is $\lvert y - c \rvert$, about $x = c$ it is $\lvert x - c \rvert$.
> - **Areas of cross-sections**: square with side $s$: $s^2$; right triangle with legs $p$, $q$: $\tfrac{1}{2}pq$; isosceles right triangle with hypotenuse $c$: $\tfrac{c^2}{4}$; similar figures: lengths scale by $k$, areas by $k^2$.
> - **Integrals**: $\int_{-a}^{a} f = 2\int_0^a f$ for even $f$ ([[Integrals of Symmetric Functions]]); $\int \sec^2 x\,dx = \tan x + C$; $\int_{-r}^{r} \sqrt{r^2 - y^2}\,dy = \tfrac{1}{2}\pi r^2$ (half a disk).
> - Each answer is written as on an exam paper: the slice (variable, disk or washer, radii), the integral, the computation, then the conclusion on a Hence line. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 5.2.1
Question: [[CAL1 HW 5.2 Questions#ST 5.2.1|ST 5.2.1]]

> [!solution] Solution
> **(a)**
>
> ![ST 5.2.1 figure|300](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%201.png)
>
> **(b)** Slice at $x$, $0 \le x \le 3$: disk, radius $x^2 + 5$.
> $$
> V = \int_0^3 \pi(x^2 + 5)^2\,dx
> $$
>
> **(c)**
> $$
> \begin{aligned}
> V &= \pi\int_0^3 (x^4 + 10x^2 + 25)\,dx = \pi\Big[\tfrac{1}{5}x^5 + \tfrac{10}{3}x^3 + 25x\Big]_0^3 \\
> &= \pi\Big(\frac{243}{5} + 90 + 75\Big) = \frac{1068\pi}{5}
> \end{aligned}
> $$
> Hence $V = \tfrac{1068\pi}{5} \approx 671.0$.
>
> \# Rotating about the $x$-axis, we cut perpendicular to the $x$-axis. The shaded region reaches the axis, so every slice is a full disk, and its radius is the height of the region at $x$, which is $x^2 + 5$.

### ST 5.2.2
Question: [[CAL1 HW 5.2 Questions#ST 5.2.2|ST 5.2.2]]

> [!solution] Solution
> **(a)**
>
> ![ST 5.2.2 figure|340](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%202.png)
>
> **(b)** Slice at $x$, $0 \le x \le 4$: washer, outer radius $\sqrt{x}$, inner radius $\tfrac{1}{2}x$ ($\sqrt{x} \ge \tfrac{1}{2}x$ on $[0, 4]$).
> $$
> A(x) = \pi(\sqrt{x})^2 - \pi\left(\tfrac{1}{2}x\right)^2 = \pi\left(x - \tfrac{1}{4}x^2\right), \qquad V = \int_0^4 \pi\left(x - \tfrac{1}{4}x^2\right)dx
> $$
>
> **(c)**
> $$
> V = \pi\Big[\tfrac{1}{2}x^2 - \tfrac{1}{12}x^3\Big]_0^4 = \pi\Big(8 - \frac{16}{3}\Big) = \frac{8\pi}{3}
> $$
> Hence $V = \tfrac{8\pi}{3}$.
>
> \# Between the axis and the line $y = \tfrac{1}{2}x$ there is no region, so the slice has a hole: a washer. The outer radius goes to the farther curve, the inner radius to the nearer one. $\sqrt{x} \ge \tfrac{1}{2}x \iff x \ge \tfrac{1}{4}x^2 \iff x(4 - x) \ge 0$, true on $[0, 4]$. Note $A = \pi(R^2 - r^2)$, not $\pi(R - r)^2$.

### ST 5.2.3
Question: [[CAL1 HW 5.2 Questions#ST 5.2.3|ST 5.2.3]]

> [!solution] Solution
> **(a)**
>
> ![ST 5.2.3 figure|340](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%203.png)
>
> **(b)** $y = x^3 + 1 \iff x = \sqrt[3]{y - 1}$. Slice at $y$, $1 \le y \le 9$: disk, radius $\sqrt[3]{y - 1}$.
> $$
> V = \int_1^9 \pi\left(\sqrt[3]{y - 1}\right)^2 dy = \int_1^9 \pi(y - 1)^{2/3}\,dy
> $$
>
> **(c)**
> $$
> V = \pi\Big[\tfrac{3}{5}(y - 1)^{5/3}\Big]_1^9 = \frac{3\pi}{5} \cdot 8^{5/3} = \frac{3\pi}{5} \cdot 32 = \frac{96\pi}{5}
> $$
> Hence $V = \tfrac{96\pi}{5}$.
>
> \# About the $y$-axis the slices are horizontal, so everything is written in $y$: solve the curve for $x$. The region starts at $y = 1$, where the curve meets the $y$-axis, and ends at $y = 9$. $8^{5/3} = (8^{1/3})^5 = 2^5$.

### ST 5.2.4
Question: [[CAL1 HW 5.2 Questions#ST 5.2.4|ST 5.2.4]]

> [!solution] Solution
> **(a)**
>
> ![ST 5.2.4 figure|440](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%204.png)
>
> **(b)** $y = \tfrac{2}{x} \iff x = \tfrac{2}{y}$, $\ y = \tfrac{x}{2} \iff x = 2y$. Slice at $y$, $1 \le y \le 2$: washer, outer radius $2y$, inner radius $\tfrac{2}{y}$ ($2y \ge \tfrac{2}{y}$ for $y \ge 1$).
> $$
> V = \int_1^2 \pi\left[(2y)^2 - \left(\tfrac{2}{y}\right)^2\right]dy = \int_1^2 \pi\left(4y^2 - \frac{4}{y^2}\right)dy
> $$
>
> **(c)**
> $$
> V = \pi\Big[\tfrac{4}{3}y^3 + \tfrac{4}{y}\Big]_1^2 = \pi\Big[\Big(\frac{32}{3} + 2\Big) - \Big(\frac{4}{3} + 4\Big)\Big] = \frac{22\pi}{3}
> $$
> Hence $V = \tfrac{22\pi}{3}$.
>
> \# The region lies between the heights $y = 1$, the point $(2, 1)$, and $y = 2$. At height $y$ it runs from the hyperbola $x = \tfrac{2}{y}$ to the line $x = 2y$, so a horizontal slice sweeps out a washer. $\int y^{-2}\,dy = -y^{-1}$, which gives the $+\tfrac{4}{y}$.

### ST 5.2.5
Question: [[CAL1 HW 5.2 Questions#ST 5.2.5|ST 5.2.5]]

> [!solution] Solution
> ![ST 5.2.5 figure|340](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%205.png)
>
> $1 - \tfrac{1}{x} = 0 \iff x = 1$. Slice at $x$, $1 \le x \le 3$: disk, radius $1 - \tfrac{1}{x}$.
> $$
> V = \int_1^3 \pi\left(1 - \frac{1}{x}\right)^2 dx
> $$
>
> \# The left end of the region is where the curve meets $y = 0$; for $1 \le x \le 3$, $1 - \tfrac{1}{x} \ge 0$, so the region lies on the axis side and the slices are disks.

### ST 5.2.6
Question: [[CAL1 HW 5.2 Questions#ST 5.2.6|ST 5.2.6]]

> [!solution] Solution
> ![ST 5.2.6 figure|340](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%206.png)
>
> $\sqrt{5 - y} = 0 \iff y = 5$. Slice at $y$, $0 \le y \le 5$: disk, radius $\sqrt{5 - y}$.
> $$
> V = \int_0^5 \pi\left(\sqrt{5 - y}\right)^2 dy = \int_0^5 \pi(5 - y)\,dy
> $$
>
> \# The curve is already written as $x = \dots$, which is what slices perpendicular to the $y$-axis need. It meets the $y$-axis $x = 0$ at $y = 5$ and the line $y = 0$ at $x = \sqrt{5}$.

### ST 5.2.7
Question: [[CAL1 HW 5.2 Questions#ST 5.2.7|ST 5.2.7]]

> [!solution] Solution
> ![ST 5.2.7 figure|440](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%207.png)
>
> $\tfrac{1}{8}x^2 = \sqrt{x} \implies x^4 = 64x \implies x = 0$ or $x = 4$: the curves meet at $(0, 0)$ and $(4, 2)$.
> In $y$: $y = \sqrt{x} \iff x = y^2$, $\ 8y = x^2 \iff x = \sqrt{8y}$ $(x, y \ge 0)$; for $0 \le y \le 2$, $\sqrt{8y} \ge y^2$.
> Slice at $y$: washer, outer radius $\sqrt{8y}$, inner radius $y^2$.
> $$
> V = \int_0^2 \pi\left[\left(\sqrt{8y}\right)^2 - (y^2)^2\right]dy = \int_0^2 \pi(8y - y^4)\,dy
> $$
>
> \# $\sqrt{8y} \ge y^2 \iff 8y \ge y^4 \iff y^3 \le 8$ for $y \ge 0$. (The value, not asked, is $\tfrac{48\pi}{5}$.)

### ST 5.2.8
Question: [[CAL1 HW 5.2 Questions#ST 5.2.8|ST 5.2.8]]

> [!solution] Solution
> ![ST 5.2.8 figure|340](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%208.png)
>
> $(x - 2)^2 = x + 10 \iff x^2 - 5x - 6 = 0 \iff (x - 6)(x + 1) = 0 \iff x = -1$ or $x = 6$.
> For $-1 \le x \le 6$: $x + 10 \ge (x - 2)^2 \ge 0$.
> Slice at $x$: washer, outer radius $x + 10$, inner radius $(x - 2)^2$.
> $$
> V = \int_{-1}^{6} \pi\left[(x + 10)^2 - (x - 2)^4\right]dx
> $$
>
> \# Both curves stay on or above the $x$-axis on $[-1, 6]$, so the radii are just their $y$-values. The inner radius $(x - 2)^2$ is $0$ at $x = 2$, where the hole closes to a point; the washer formula still holds there.

### ST 5.2.9
Question: [[CAL1 HW 5.2 Questions#ST 5.2.9|ST 5.2.9]]

> [!solution] Solution
> ![ST 5.2.9 figure|340](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%209.png)
>
> Slice at $x$, $0 \le x \le \pi$: washer about $y = -2$,
> outer radius $\sin x - (-2) = 2 + \sin x$, inner radius $0 - (-2) = 2$.
> $$
> V = \int_0^{\pi} \pi\left[(2 + \sin x)^2 - 2^2\right]dx
> $$
>
> \# A radius is a distance to the axis $y = -2$: the $y$-value minus $(-2)$. The region sits $2$ units above the axis, which leaves the hole of radius $2$.

### ST 5.2.10
Question: [[CAL1 HW 5.2 Questions#ST 5.2.10|ST 5.2.10]]

> [!solution] Solution
> ![ST 5.2.10 figure|460](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2010.png)
>
> $y = \sqrt{x} \iff x = y^2$; the region is $0 \le y \le 2$, $y^2 \le x \le 4$.
> Slice at $y$: washer about $x = 6$, outer radius $6 - y^2$, inner radius $6 - 4 = 2$.
> $$
> V = \int_0^2 \pi\left[(6 - y^2)^2 - 2^2\right]dy
> $$
>
> \# The axis $x = 6$ is vertical, so the slices are horizontal and the integral is in $y$, from $y = 0$ to $y = \sqrt{4} = 2$. The region lies to the left of the axis, so the distance from a point $x$ to the axis is $6 - x$.

### ST 5.2.13
Question: [[CAL1 HW 5.2 Questions#ST 5.2.13|ST 5.2.13]]

> [!solution] Solution
> ![ST 5.2.13 figure|360](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2013.png)
>
> $\sqrt{x - 1} = 0 \iff x = 1$. Slice at $x$, $1 \le x \le 5$: disk, radius $\sqrt{x - 1}$.
> $$
> V = \int_1^5 \pi(x - 1)\,dx = \pi\Big[\tfrac{1}{2}(x - 1)^2\Big]_1^5 = \pi \cdot \frac{16}{2} = 8\pi
> $$
> Hence $V = 8\pi$.

### ST 5.2.15
Question: [[CAL1 HW 5.2 Questions#ST 5.2.15|ST 5.2.15]]

> [!solution] Solution
> ![ST 5.2.15 figure|360](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2015.png)
>
> Slice at $y$, $0 \le y \le 9$: disk, radius $2\sqrt{y}$.
> $$
> V = \int_0^9 \pi(2\sqrt{y})^2\,dy = \int_0^9 4\pi y\,dy = \Big[2\pi y^2\Big]_0^9 = 162\pi
> $$
> Hence $V = 162\pi$.
>
> \# The region lies between the $y$-axis and the curve $x = 2\sqrt{y}$, from $y = 0$ (where $x = 0$) to the line $y = 9$.

### ST 5.2.21
Question: [[CAL1 HW 5.2 Questions#ST 5.2.21|ST 5.2.21]]

> [!solution] Solution
> ![ST 5.2.21 figure|320](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2021.png)
>
> $x = y^2 \iff y = \sqrt{x}$ $(y \ge 0)$; $x^2 = \sqrt{x} \iff x = 0$ or $1$; for $0 \le x \le 1$: $x^2 \le \sqrt{x} \le 1$.
> Slice at $x$: washer about $y = 1$, outer radius $1 - x^2$, inner radius $1 - \sqrt{x}$.
> $$
> \begin{aligned}
> V &= \int_0^1 \pi\left[(1 - x^2)^2 - (1 - \sqrt{x})^2\right]dx \\
> &= \pi\int_0^1 \left(2x^{1/2} - x - 2x^2 + x^4\right)dx \\
> &= \pi\Big[\tfrac{4}{3}x^{3/2} - \tfrac{1}{2}x^2 - \tfrac{2}{3}x^3 + \tfrac{1}{5}x^5\Big]_0^1 = \pi\Big(\frac{4}{3} - \frac{1}{2} - \frac{2}{3} + \frac{1}{5}\Big) = \frac{11\pi}{30}
> \end{aligned}
> $$
> Hence $V = \tfrac{11\pi}{30}$.
>
> \# The axis $y = 1$ is above the region, so a distance to it is $1 - y$. The lower curve $y = x^2$ is farther from the axis, so it gives the outer radius. Expanded: $(1 - x^2)^2 = 1 - 2x^2 + x^4$ and $(1 - \sqrt{x})^2 = 1 - 2\sqrt{x} + x$.

### ST 5.2.23
Question: [[CAL1 HW 5.2 Questions#ST 5.2.23|ST 5.2.23]]

> [!solution] Solution
> ![ST 5.2.23 figure|320](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2023.png)
>
> For $\lvert x \rvert \le \tfrac{\pi}{3}$: $1 \le \sec x \le 2$, so $1 + \sec x \le 3$.
> Slice at $x$: washer about $y = 1$, outer radius $3 - 1 = 2$, inner radius $(1 + \sec x) - 1 = \sec x$.
> $$
> \begin{aligned}
> V &= \int_{-\pi/3}^{\pi/3} \pi\left(2^2 - \sec^2 x\right)dx = 2\pi\int_0^{\pi/3} (4 - \sec^2 x)\,dx \\
> &= 2\pi\Big[4x - \tan x\Big]_0^{\pi/3} = 2\pi\Big(\frac{4\pi}{3} - \sqrt{3}\Big) = \frac{8\pi^2}{3} - 2\sqrt{3}\,\pi
> \end{aligned}
> $$
> Hence $V = \tfrac{8\pi^2}{3} - 2\sqrt{3}\,\pi \approx 15.44$.
>
> \# The integrand $4 - \sec^2 x$ is even, so the integral over $[-\tfrac{\pi}{3}, \tfrac{\pi}{3}]$ is twice the integral over $[0, \tfrac{\pi}{3}]$. $\sec\tfrac{\pi}{3} = 2$ is where $y = 1 + \sec x$ reaches $y = 3$.

### ST 5.2.25
Question: [[CAL1 HW 5.2 Questions#ST 5.2.25|ST 5.2.25]]

> [!solution] Solution
> ![ST 5.2.25 figure|440](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2025.png)
>
> $y = x^3 \iff x = \sqrt[3]{y}$; the region is $0 \le y \le 1$, $\sqrt[3]{y} \le x \le 1$.
> Slice at $y$: washer about $x = 2$, outer radius $2 - \sqrt[3]{y}$, inner radius $2 - 1 = 1$.
> $$
> \begin{aligned}
> V &= \int_0^1 \pi\left[\left(2 - y^{1/3}\right)^2 - 1^2\right]dy = \pi\int_0^1 \left(3 - 4y^{1/3} + y^{2/3}\right)dy \\
> &= \pi\Big[3y - 3y^{4/3} + \tfrac{3}{5}y^{5/3}\Big]_0^1 = \pi\Big(3 - 3 + \frac{3}{5}\Big) = \frac{3\pi}{5}
> \end{aligned}
> $$
> Hence $V = \tfrac{3\pi}{5}$.
>
> \# The axis $x = 2$ is vertical, so slice horizontally. The region lies to the left of the axis: the curve $x = \sqrt[3]{y}$ is farther away (outer), the line $x = 1$ is nearer (inner).

### ST 5.2.27
Question: [[CAL1 HW 5.2 Questions#ST 5.2.27|ST 5.2.27]]

> [!solution] Solution
> ![ST 5.2.27 figure|460](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2027.png)
>
> $y^2 = 1 - y^2 \iff y = \pm\tfrac{1}{\sqrt{2}}$; for $\lvert y \rvert \le \tfrac{1}{\sqrt{2}}$: $y^2 \le x \le 1 - y^2$.
> Slice at $y$: washer about $x = 3$, outer radius $3 - y^2$, inner radius $3 - (1 - y^2) = 2 + y^2$.
> $$
> \begin{aligned}
> (3 - y^2)^2 - (2 + y^2)^2 &= (3 - y^2 - 2 - y^2)(3 - y^2 + 2 + y^2) = 5(1 - 2y^2) \\
> V = \int_{-1/\sqrt{2}}^{1/\sqrt{2}} 5\pi(1 - 2y^2)\,dy &= 10\pi\Big[y - \tfrac{2}{3}y^3\Big]_0^{1/\sqrt{2}} = 10\pi\Big(\frac{1}{\sqrt{2}} - \frac{1}{3\sqrt{2}}\Big) = \frac{20\pi}{3\sqrt{2}} = \frac{10\sqrt{2}\,\pi}{3}
> \end{aligned}
> $$
> Hence $V = \tfrac{10\sqrt{2}\,\pi}{3}$.
>
> \# The difference of squares $a^2 - b^2 = (a - b)(a + b)$ saves the expansion. The integrand is even, so the integral is twice the one over $[0, \tfrac{1}{\sqrt{2}}]$. $\tfrac{2}{3}\big(\tfrac{1}{\sqrt{2}}\big)^3 = \tfrac{2}{3} \cdot \tfrac{1}{2\sqrt{2}} = \tfrac{1}{3\sqrt{2}}$.

### ST 5.2.29
Question: [[CAL1 HW 5.2 Questions#ST 5.2.29|ST 5.2.29]]

> [!solution] Solution
> ![ST 5.2.29 figure|280](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2029.png)
>
> $\mathcal{R}_1$: $0 \le x \le 1$, $0 \le y \le x$. $OA$ is the $x$-axis. Slice at $x$: disk, radius $x$.
> $$
> V = \int_0^1 \pi x^2\,dx = \frac{\pi}{3}
> $$
> Hence $V = \tfrac{\pi}{3}$.
>
> \# For Exercises 29–40, with $y = \sqrt[4]{x} \iff x = y^4$ $(x, y \ge 0)$ and $x \le \sqrt[4]{x}$ on $[0, 1]$:
> $\mathcal{R}_1$: $0 \le y \le x$, or $y \le x \le 1$; $\ \mathcal{R}_2$: $\sqrt[4]{x} \le y \le 1$, or $0 \le x \le y^4$; $\ \mathcal{R}_3$: $x \le y \le \sqrt[4]{x}$, or $y^4 \le x \le y$, each for $0 \le x \le 1$ or $0 \le y \le 1$.
> $OA$ ($x$-axis) and $BC$ ($y = 1$) are horizontal: slice at $x$. $OC$ ($y$-axis) and $AB$ ($x = 1$) are vertical: slice at $y$. Here $\mathcal{R}_1$ is a triangle and the solid is a cone with radius $1$ and height $1$: $\tfrac{1}{3}\pi \cdot 1^2 \cdot 1$.

### ST 5.2.30
Question: [[CAL1 HW 5.2 Questions#ST 5.2.30|ST 5.2.30]]

> [!solution] Solution
> ![ST 5.2.30 figure|300](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2030.png)
>
> $\mathcal{R}_1$: $0 \le y \le 1$, $y \le x \le 1$. $OC$ is the $y$-axis. Slice at $y$: washer, outer radius $1$, inner radius $y$.
> $$
> V = \int_0^1 \pi(1 - y^2)\,dy = \pi\Big(1 - \frac{1}{3}\Big) = \frac{2\pi}{3}
> $$
> Hence $V = \tfrac{2\pi}{3}$.
>
> \# The solid is a cylinder with radius $1$ and height $1$ with a cone removed: $\pi - \tfrac{\pi}{3}$.

### ST 5.2.31
Question: [[CAL1 HW 5.2 Questions#ST 5.2.31|ST 5.2.31]]

> [!solution] Solution
> ![ST 5.2.31 figure|320](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2031.png)
>
> $\mathcal{R}_1$: $0 \le y \le 1$, $y \le x \le 1$. $AB$ is the line $x = 1$. Slice at $y$: disk, radius $1 - y$.
> $$
> V = \int_0^1 \pi(1 - y)^2\,dy = \pi\Big[-\tfrac{1}{3}(1 - y)^3\Big]_0^1 = \frac{\pi}{3}
> $$
> Hence $V = \tfrac{\pi}{3}$.
>
> \# The region touches the axis $x = 1$, so the slices are disks; the radius is the distance from $x = y$ to $x = 1$.

### ST 5.2.32
Question: [[CAL1 HW 5.2 Questions#ST 5.2.32|ST 5.2.32]]

> [!solution] Solution
> ![ST 5.2.32 figure|300](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2032.png)
>
> $\mathcal{R}_1$: $0 \le x \le 1$, $0 \le y \le x$. $BC$ is the line $y = 1$. Slice at $x$: washer, outer radius $1 - 0 = 1$, inner radius $1 - x$.
> $$
> V = \int_0^1 \pi\left[1 - (1 - x)^2\right]dx = \pi\Big(1 - \frac{1}{3}\Big) = \frac{2\pi}{3}
> $$
> Hence $V = \tfrac{2\pi}{3}$.
>
> \# The axis $y = 1$ is above the region: the farthest part is the bottom side $OA$ ($y = 0$), the nearest part is the line $y = x$. $\int_0^1 (1 - x)^2\,dx = \tfrac{1}{3}$ as in [[#ST 5.2.31|ST 5.2.31]].

### ST 5.2.33
Question: [[CAL1 HW 5.2 Questions#ST 5.2.33|ST 5.2.33]]

> [!solution] Solution
> ![ST 5.2.33 figure|280](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2033.png)
>
> $\mathcal{R}_2$: $0 \le x \le 1$, $\sqrt[4]{x} \le y \le 1$. Slice at $x$: washer about $OA$, outer radius $1$, inner radius $\sqrt[4]{x}$.
> $$
> V = \int_0^1 \pi\left(1 - x^{1/2}\right)dx = \pi\Big(1 - \frac{2}{3}\Big) = \frac{\pi}{3}
> $$
> Hence $V = \tfrac{\pi}{3}$.
>
> \# $\big(\sqrt[4]{x}\big)^2 = x^{1/2}$.

### ST 5.2.34
Question: [[CAL1 HW 5.2 Questions#ST 5.2.34|ST 5.2.34]]

> [!solution] Solution
> ![ST 5.2.34 figure|300](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2034.png)
>
> $\mathcal{R}_2$: $0 \le y \le 1$, $0 \le x \le y^4$. Slice at $y$: disk about $OC$, radius $y^4$.
> $$
> V = \int_0^1 \pi y^8\,dy = \frac{\pi}{9}
> $$
> Hence $V = \tfrac{\pi}{9}$.
>
> \# $\mathcal{R}_2$ touches the $y$-axis along $OC$, so horizontal slices give disks; the curve must be written as $x = y^4$.

### ST 5.2.35
Question: [[CAL1 HW 5.2 Questions#ST 5.2.35|ST 5.2.35]]

> [!solution] Solution
> ![ST 5.2.35 figure|320](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2035.png)
>
> $\mathcal{R}_2$: $0 \le y \le 1$, $0 \le x \le y^4$. Slice at $y$: washer about $AB$ ($x = 1$), outer radius $1 - 0 = 1$, inner radius $1 - y^4$.
> $$
> V = \int_0^1 \pi\left[1 - (1 - y^4)^2\right]dy = \pi\int_0^1 (2y^4 - y^8)\,dy = \pi\Big(\frac{2}{5} - \frac{1}{9}\Big) = \frac{13\pi}{45}
> $$
> Hence $V = \tfrac{13\pi}{45}$.

### ST 5.2.36
Question: [[CAL1 HW 5.2 Questions#ST 5.2.36|ST 5.2.36]]

> [!solution] Solution
> ![ST 5.2.36 figure|300](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2036.png)
>
> $\mathcal{R}_2$: $0 \le x \le 1$, $\sqrt[4]{x} \le y \le 1$. Slice at $x$: disk about $BC$ ($y = 1$), radius $1 - \sqrt[4]{x}$.
> $$
> V = \int_0^1 \pi\left(1 - x^{1/4}\right)^2 dx = \pi\int_0^1 \left(1 - 2x^{1/4} + x^{1/2}\right)dx = \pi\Big(1 - \frac{8}{5} + \frac{2}{3}\Big) = \frac{\pi}{15}
> $$
> Hence $V = \tfrac{\pi}{15}$.
>
> \# $\int_0^1 x^{1/4}\,dx = \tfrac{4}{5}$ and $\int_0^1 x^{1/2}\,dx = \tfrac{2}{3}$.

### ST 5.2.37
Question: [[CAL1 HW 5.2 Questions#ST 5.2.37|ST 5.2.37]]

> [!solution] Solution
> ![ST 5.2.37 figure|280](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2037.png)
>
> $\mathcal{R}_3$: $0 \le x \le 1$, $x \le y \le \sqrt[4]{x}$. Slice at $x$: washer about $OA$, outer radius $\sqrt[4]{x}$, inner radius $x$.
> $$
> V = \int_0^1 \pi\left(x^{1/2} - x^2\right)dx = \pi\Big(\frac{2}{3} - \frac{1}{3}\Big) = \frac{\pi}{3}
> $$
> Hence $V = \tfrac{\pi}{3}$.

### ST 5.2.38
Question: [[CAL1 HW 5.2 Questions#ST 5.2.38|ST 5.2.38]]

> [!solution] Solution
> ![ST 5.2.38 figure|300](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2038.png)
>
> $\mathcal{R}_3$: $0 \le y \le 1$, $y^4 \le x \le y$. Slice at $y$: washer about $OC$, outer radius $y$, inner radius $y^4$.
> $$
> V = \int_0^1 \pi\left(y^2 - y^8\right)dy = \pi\Big(\frac{1}{3} - \frac{1}{9}\Big) = \frac{2\pi}{9}
> $$
> Hence $V = \tfrac{2\pi}{9}$.

### ST 5.2.39
Question: [[CAL1 HW 5.2 Questions#ST 5.2.39|ST 5.2.39]]

> [!solution] Solution
> ![ST 5.2.39 figure|320](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2039.png)
>
> $\mathcal{R}_3$: $0 \le y \le 1$, $y^4 \le x \le y$. Slice at $y$: washer about $AB$ ($x = 1$), outer radius $1 - y^4$, inner radius $1 - y$.
> $$
> \begin{aligned}
> V &= \int_0^1 \pi\left[(1 - y^4)^2 - (1 - y)^2\right]dy = \pi\int_0^1 \left(2y - y^2 - 2y^4 + y^8\right)dy \\
> &= \pi\Big(1 - \frac{1}{3} - \frac{2}{5} + \frac{1}{9}\Big) = \frac{17\pi}{45}
> \end{aligned}
> $$
> Hence $V = \tfrac{17\pi}{45}$.
>
> \# The axis $x = 1$ is to the right of $\mathcal{R}_3$: the curve $x = y^4$ is farther (outer), the line $x = y$ is nearer (inner).

### ST 5.2.40
Question: [[CAL1 HW 5.2 Questions#ST 5.2.40|ST 5.2.40]]

> [!solution] Solution
> ![ST 5.2.40 figure|300](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2040.png)
>
> $\mathcal{R}_3$: $0 \le x \le 1$, $x \le y \le \sqrt[4]{x}$. Slice at $x$: washer about $BC$ ($y = 1$), outer radius $1 - x$, inner radius $1 - \sqrt[4]{x}$.
> $$
> \begin{aligned}
> V &= \int_0^1 \pi\left[(1 - x)^2 - \left(1 - x^{1/4}\right)^2\right]dx = \pi\int_0^1 \left(2x^{1/4} - x^{1/2} - 2x + x^2\right)dx \\
> &= \pi\Big(\frac{8}{5} - \frac{2}{3} - 1 + \frac{1}{3}\Big) = \frac{4\pi}{15}
> \end{aligned}
> $$
> Hence $V = \tfrac{4\pi}{15}$.
>
> \# A check of Exercises 29–40: $\mathcal{R}_1$, $\mathcal{R}_2$, $\mathcal{R}_3$ fill the square, which sweeps out a cylinder of radius $1$ and height $1$ about each side, so for each axis the three volumes add up to $\pi$.
> About $OA$: $\tfrac{\pi}{3} + \tfrac{\pi}{3} + \tfrac{\pi}{3}$; about $OC$: $\tfrac{2\pi}{3} + \tfrac{\pi}{9} + \tfrac{2\pi}{9}$; about $AB$: $\tfrac{\pi}{3} + \tfrac{13\pi}{45} + \tfrac{17\pi}{45}$; about $BC$: $\tfrac{2\pi}{3} + \tfrac{\pi}{15} + \tfrac{4\pi}{15}$. Each sum is $\pi$.

### ST 5.2.49
Question: [[CAL1 HW 5.2 Questions#ST 5.2.49|ST 5.2.49]]

> [!solution] Solution
> ![ST 5.2.49 figure|300](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2049.png)
>
> $\pi\int_0^{\pi/2} \sin^2 x\,dx = \int_0^{\pi/2} \pi(\sin x)^2\,dx$: disks of radius $\sin x$, slices at $x$.
>
> The solid obtained by rotating the region under $y = \sin x$ and above the $x$-axis, $0 \le x \le \tfrac{\pi}{2}$, about the $x$-axis.
>
> \# Read the integral backwards: $\pi(\text{radius})^2$ with one square means disks, $dx$ means slices perpendicular to the $x$-axis, so the axis is horizontal, and the limits give the ends of the region.

### ST 5.2.51
Question: [[CAL1 HW 5.2 Questions#ST 5.2.51|ST 5.2.51]]

> [!solution] Solution
> ![ST 5.2.51 figure|300](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2051.png)
>
> $\pi\int_0^1 (x^4 - x^6)\,dx = \int_0^1 \pi\left[(x^2)^2 - (x^3)^2\right]dx$: washers, outer radius $x^2$, inner radius $x^3$ ($x^3 \le x^2$ on $[0, 1]$), slices at $x$.
>
> The solid obtained by rotating the region between $y = x^3$ and $y = x^2$, $0 \le x \le 1$, about the $x$-axis.
>
> \# A difference of two squares means washers: $x^4 = (x^2)^2$ is the outer radius squared, $x^6 = (x^3)^2$ the inner one. The two curves meet at $x = 0$ and $x = 1$.

### ST 5.2.53
Question: [[CAL1 HW 5.2 Questions#ST 5.2.53|ST 5.2.53]]

> [!solution] Solution
> ![ST 5.2.53 figure|300](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2053.png)
>
> $\pi\int_0^4 y\,dy = \int_0^4 \pi(\sqrt{y})^2\,dy$: disks of radius $\sqrt{y}$, slices at $y$.
>
> The solid obtained by rotating the region between the curve $x = \sqrt{y}$ (that is, $y = x^2$, $x \ge 0$) and the $y$-axis, $0 \le y \le 4$, about the $y$-axis.
>
> \# $dy$ means horizontal slices, so the axis is vertical. The solid is the inside of the paraboloid $y = x^2 + z^2$ cut off at height $4$, like a filled bowl.

### ST 5.2.59
Question: [[CAL1 HW 5.2 Questions#ST 5.2.59|ST 5.2.59]]

> [!solution] Solution
> ![ST 5.2.59 figure|340](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2059.png)
>
> Vertex at $O$, axis along the $x$-axis: the cone is the region under $y = \tfrac{r}{h}x$, $0 \le x \le h$, rotated about the $x$-axis.
> Slice at $x$: disk, radius $\tfrac{r}{h}x$.
> $$
> V = \int_0^h \pi\Big(\frac{r}{h}x\Big)^2 dx = \frac{\pi r^2}{h^2}\Big[\tfrac{1}{3}x^3\Big]_0^h = \frac{\pi r^2}{h^2} \cdot \frac{h^3}{3} = \frac{1}{3}\pi r^2 h
> $$
> Hence $V = \tfrac{1}{3}\pi r^2 h$.
>
> \# The line through $(0, 0)$ and $(h, r)$ has slope $\tfrac{r}{h}$; it is the slant side of the cone.

### ST 5.2.61
Question: [[CAL1 HW 5.2 Questions#ST 5.2.61|ST 5.2.61]]

> [!solution] Solution
> ![ST 5.2.61 figure|340](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2061.png)
>
> The sphere is $x^2 + y^2 = r^2$ rotated about the $y$-axis; the cap is the part with $r - h \le y \le r$.
> Slice at $y$: disk, radius $\sqrt{r^2 - y^2}$.
> $$
> \begin{aligned}
> V &= \int_{r - h}^{r} \pi(r^2 - y^2)\,dy = \pi\Big[r^2 y - \tfrac{1}{3}y^3\Big]_{r - h}^{r} \\
> &= \pi\Big[\frac{2}{3}r^3 - \Big(r^2(r - h) - \frac{1}{3}(r - h)^3\Big)\Big] \\
> &= \pi\Big[\frac{2}{3}r^3 - \Big(\frac{2}{3}r^3 - rh^2 + \frac{1}{3}h^3\Big)\Big] = \pi\Big(rh^2 - \frac{1}{3}h^3\Big) = \pi h^2\Big(r - \frac{h}{3}\Big)
> \end{aligned}
> $$
> Hence $V = \pi h^2\left(r - \tfrac{h}{3}\right)$.
>
> \# $r^2(r - h) - \tfrac{1}{3}(r - h)^3 = r^3 - r^2h - \tfrac{1}{3}(r^3 - 3r^2h + 3rh^2 - h^3) = \tfrac{2}{3}r^3 - rh^2 + \tfrac{1}{3}h^3$. Check: $h = r$ gives a half ball, $\tfrac{2}{3}\pi r^3$; $h = 2r$ gives the whole ball, $\tfrac{4}{3}\pi r^3$.

### ST 5.2.63
Question: [[CAL1 HW 5.2 Questions#ST 5.2.63|ST 5.2.63]]

> [!solution] Solution
> ![ST 5.2.63 figure|340](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2063.png)
>
> Vertex at $O$, $x$-axis perpendicular to the base, base at $x = h$.
> Slice at $x$, $0 \le x \le h$: a rectangle similar to the base with ratio $\tfrac{x}{h}$, sides $\tfrac{b}{h}x$ and $\tfrac{2b}{h}x$.
> $$
> A(x) = \frac{b}{h}x \cdot \frac{2b}{h}x = \frac{2b^2}{h^2}x^2, \qquad V = \int_0^h \frac{2b^2}{h^2}x^2\,dx = \frac{2b^2}{h^2} \cdot \frac{h^3}{3} = \frac{2}{3}b^2 h
> $$
> Hence $V = \tfrac{2}{3}b^2 h$.
>
> \# By similar triangles every length in the slice at distance $x$ from the vertex is $\tfrac{x}{h}$ times the length in the base. Check: $\tfrac{1}{3}(\text{base area})(\text{height}) = \tfrac{1}{3}(2b^2)h$.

### ST 5.2.65
Question: [[CAL1 HW 5.2 Questions#ST 5.2.65|ST 5.2.65]]

> [!solution] Solution
> ![ST 5.2.65 figure|320](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2065.png)
>
> Put the corner where the three perpendicular edges meet at $O$, the $5$ cm edge on the $x$-axis.
> Slice at $x$, $0 \le x \le 5$: a right triangle similar to the face with legs $3$ and $4$, ratio $1 - \tfrac{x}{5}$.
> $$
> \begin{aligned}
> A(x) &= \frac{1}{2} \cdot 3\Big(1 - \frac{x}{5}\Big) \cdot 4\Big(1 - \frac{x}{5}\Big) = 6\Big(1 - \frac{x}{5}\Big)^2 \\
> V &= \int_0^5 6\Big(1 - \frac{x}{5}\Big)^2 dx = 6\Big[-\frac{5}{3}\Big(1 - \frac{x}{5}\Big)^3\Big]_0^5 = 6 \cdot \frac{5}{3} = 10
> \end{aligned}
> $$
> Hence $V = 10\ \text{cm}^3$.
>
> \# At $x = 0$ the slice is the face with legs $3$ and $4$; at $x = 5$ it shrinks to a point, and in between its sides shrink linearly. Check: $\tfrac{1}{3}\big(\tfrac{1}{2} \cdot 3 \cdot 4\big) \cdot 5 = 10$.

### ST 5.2.67
Question: [[CAL1 HW 5.2 Questions#ST 5.2.67|ST 5.2.67]]

> [!solution] Solution
> ![ST 5.2.67 figure|420](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2067.png)
>
> $9x^2 + 4y^2 = 36 \iff \tfrac{x^2}{4} + \tfrac{y^2}{9} = 1$, $-2 \le x \le 2$; upper half $y = \tfrac{3}{2}\sqrt{4 - x^2}$.
> Slice at $x$: isosceles right triangle with hypotenuse $2y$, height $y$ (half the hypotenuse).
> $$
> \begin{aligned}
> A(x) &= \frac{1}{2} \cdot 2y \cdot y = y^2 = \frac{9}{4}(4 - x^2) \\
> V &= \int_{-2}^{2} \frac{9}{4}(4 - x^2)\,dx = \frac{9}{2}\Big[4x - \tfrac{1}{3}x^3\Big]_0^2 = \frac{9}{2} \cdot \frac{16}{3} = 24
> \end{aligned}
> $$
> Hence $V = 24$.
>
> \# The hypotenuse lies in the base and runs across the ellipse from $-y$ to $y$. In an isosceles right triangle the height to the hypotenuse is half of it: the right angle sits over the midpoint and the two half-triangles are again isosceles right triangles.

### ST 5.2.73
Question: [[CAL1 HW 5.2 Questions#ST 5.2.73|ST 5.2.73]]

> [!solution] Solution
> ![ST 5.2.73 figure|380](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2073.png)
>
> Slice at $x$, $-1 \le x \le 1$: the disk bounded by the circle with center $\big(x, \tfrac{1}{2}(1 - x^2)\big)$ through the point $(x, 0)$ of the $x$-axis, so its radius is $\tfrac{1}{2}(1 - x^2)$.
> $$
> \begin{aligned}
> A(x) &= \pi\Big[\frac{1}{2}(1 - x^2)\Big]^2 = \frac{\pi}{4}(1 - x^2)^2 \\
> V &= \int_{-1}^{1} \frac{\pi}{4}(1 - x^2)^2\,dx = \frac{\pi}{2}\int_0^1 (1 - 2x^2 + x^4)\,dx = \frac{\pi}{2}\Big(1 - \frac{2}{3} + \frac{1}{5}\Big) = \frac{4\pi}{15}
> \end{aligned}
> $$
> Hence $V = \tfrac{4\pi}{15}$.
>
> \# Each circle lies in the plane through $x$ perpendicular to the $x$-axis, and that plane meets the $x$-axis only at the point $(x, 0)$. So "intersects the $x$-axis" means the circle passes through $(x, 0)$, and the radius is the distance from there to the center, $\tfrac{1}{2}(1 - x^2)$.

### ST 5.2.75
Question: [[CAL1 HW 5.2 Questions#ST 5.2.75|ST 5.2.75]]

> [!solution] Solution
> ![ST 5.2.75 figure|460](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2075.png)
>
> **(a)** The torus is the disk $(x - R)^2 + y^2 \le r^2$ $(R > r)$ rotated about the $y$-axis.
> Slice at $y$, $-r \le y \le r$: washer, outer radius $R + \sqrt{r^2 - y^2}$, inner radius $R - \sqrt{r^2 - y^2}$.
> $$
> \begin{aligned}
> A(y) &= \pi\Big[\Big(R + \sqrt{r^2 - y^2}\Big)^2 - \Big(R - \sqrt{r^2 - y^2}\Big)^2\Big] = 4\pi R\sqrt{r^2 - y^2} \\
> V &= \int_{-r}^{r} 4\pi R\sqrt{r^2 - y^2}\,dy
> \end{aligned}
> $$
>
> **(b)** $\int_{-r}^{r} \sqrt{r^2 - y^2}\,dy$ is the area between the half circle $x = \sqrt{r^2 - y^2}$ and the $y$-axis, half of a disk of radius $r$: $\tfrac{1}{2}\pi r^2$.
> $$
> V = 4\pi R \cdot \frac{1}{2}\pi r^2 = 2\pi^2 r^2 R
> $$
> Hence $V = 2\pi^2 r^2 R$.
>
> \# $(a + b)^2 - (a - b)^2 = 4ab$. At height $y$ the circle $(x - R)^2 + y^2 = r^2$ has $x = R \pm \sqrt{r^2 - y^2}$: the right point gives the outer radius, the left point the inner one. The answer is $(\pi r^2)(2\pi R)$: the area of the small disk times the length of the circle traced by its center.

### ST 5.2.79
Question: [[CAL1 HW 5.2 Questions#ST 5.2.79|ST 5.2.79]]

> [!proof] Proof
> ![ST 5.2.79 figure|460](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2079.png)
>
> Put both solids on one plane and cut them with the plane at height $y$, $0 \le y \le r$, parallel to it.
>
> Hemisphere (center of the base at height $0$): the cut is a disk of radius $\sqrt{r^2 - y^2}$,
> $$
> A_1(y) = \pi(r^2 - y^2).
> $$
> Cylinder with the cone removed (vertex at the center of the bottom, base the top of the cylinder): the cone's radius at height $y$ is $y$ (it grows linearly from $0$ at $y = 0$ to $r$ at $y = r$), so the cut is a ring with outer radius $r$ and inner radius $y$,
> $$
> A_2(y) = \pi r^2 - \pi y^2 = \pi(r^2 - y^2).
> $$
> $A_1(y) = A_2(y)$ for every $0 \le y \le r$, so by [[Cavalieri's Principle]] the two volumes are equal. $\blacksquare$
>
> \# Then the hemisphere has volume $\pi r^2 \cdot r - \tfrac{1}{3}\pi r^2 \cdot r = \tfrac{2}{3}\pi r^3$. The principle itself comes from the definition of volume: equal $A(y)$ give equal $\int_0^r A(y)\,dy$.

### ST 5.2.80
Question: [[CAL1 HW 5.2 Questions#ST 5.2.80|ST 5.2.80]]

> [!solution] Solution
> ![ST 5.2.80 figure|440](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2080.png)
>
> Axes: the cylinders are $x^2 + y^2 \le r^2$ (axis the $z$-axis) and $x^2 + z^2 \le r^2$ (axis the $y$-axis); the axes meet at $O$ at a right angle.
> Slice at $x$, $-r \le x \le r$: $\lvert y \rvert \le \sqrt{r^2 - x^2}$ and $\lvert z \rvert \le \sqrt{r^2 - x^2}$, a square with side $2\sqrt{r^2 - x^2}$.
> $$
> V = \int_{-r}^{r} 4(r^2 - x^2)\,dx = 8\Big[r^2 x - \tfrac{1}{3}x^3\Big]_0^r = 8 \cdot \frac{2}{3}r^3 = \frac{16}{3}r^3
> $$
> Hence $V = \tfrac{16}{3}r^3$.
>
> \# Slice perpendicular to the $x$-axis, which is perpendicular to both cylinder axes. The plane through $x$ cuts each cylinder in a band of width $2\sqrt{r^2 - x^2}$, one along $z$ and one along $y$; the part common to both is the square. (A slice along one of the axes would give a more complicated shape.)

### ST 5.2.81
Question: [[CAL1 HW 5.2 Questions#ST 5.2.81|ST 5.2.81]]

> [!solution] Solution
> ![ST 5.2.81 figure|440](../Attachments/CAL1%20HW%205.2%20Solutions%20fig%2081.png)
>
> Centers $O$ and $(r, 0, 0)$; the common part is the region inside both circles $x^2 + y^2 = r^2$ and $(x - r)^2 + y^2 = r^2$ rotated about the $x$-axis.
> $x^2 = (x - r)^2 \iff x = \tfrac{r}{2}$, and the solid is symmetric about the plane $x = \tfrac{r}{2}$. For $\tfrac{r}{2} \le x \le r$, slice at $x$: disk, radius $\sqrt{r^2 - x^2}$.
> $$
> \begin{aligned}
> V &= 2\int_{r/2}^{r} \pi(r^2 - x^2)\,dx = 2\pi\Big[r^2 x - \tfrac{1}{3}x^3\Big]_{r/2}^{r} \\
> &= 2\pi\Big[\frac{2}{3}r^3 - \Big(\frac{1}{2}r^3 - \frac{1}{24}r^3\Big)\Big] = 2\pi \cdot \frac{5}{24}r^3 = \frac{5}{12}\pi r^3
> \end{aligned}
> $$
> Hence $V = \tfrac{5}{12}\pi r^3$.
>
> \# The common part is two caps of height $\tfrac{r}{2}$ glued along the plane $x = \tfrac{r}{2}$. With the cap volume $\pi h^2\left(r - \tfrac{h}{3}\right)$ of [[#ST 5.2.61|ST 5.2.61]] and $h = \tfrac{r}{2}$: $2 \cdot \pi\big(\tfrac{r}{2}\big)^2\big(r - \tfrac{r}{6}\big) = \tfrac{5}{12}\pi r^3$.
