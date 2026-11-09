---
course: [CAL1]
semester: "115-1"
chapter: ["3.7"]
tags: [calculus, homework, solutions, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §3.7, pp. 265-270, scanned PDF (steps in solving optimization problems, First Derivative Test for Absolute Extreme Values)"
created: 2026-11-08
questions: "[[CAL1 HW 3.7 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 3.7 Questions#ST 3.7.5\|ST 3.7.5]] | $\tfrac{9}{4}$, at $x = \tfrac{1}{2}$ |
| [[CAL1 HW 3.7 Questions#ST 3.7.11\|ST 3.7.11]] | 2250 m² (pens 30 m deep, rectangle 75 m long) |
| [[CAL1 HW 3.7 Questions#ST 3.7.15\|ST 3.7.15]] | 30 m along the barn, 20 m out from the barn |
| [[CAL1 HW 3.7 Questions#ST 3.7.21\|ST 3.7.21]] | $90\sqrt[3]{6} \approx$ \$163.54 |
| [[CAL1 HW 3.7 Questions#ST 3.7.23\|ST 3.7.23]] | $\tfrac{137}{3} \times \tfrac{137}{3} \times \tfrac{274}{3}$ cm $\approx 45.7 \times 45.7 \times 91.3$ cm |
| [[CAL1 HW 3.7 Questions#ST 3.7.26\|ST 3.7.26]] | $\left(\tfrac{5}{2}, \tfrac{\sqrt{10}}{2}\right)$ |
| [[CAL1 HW 3.7 Questions#ST 3.7.31\|ST 3.7.31]] | width $\tfrac{L}{2}$, height $\tfrac{\sqrt{3}}{4}L$ |
| [[CAL1 HW 3.7 Questions#ST 3.7.37\|ST 3.7.37]] | $\frac{4\pi r^{3}}{3\sqrt{3}}$ |
| [[CAL1 HW 3.7 Questions#ST 3.7.47\|ST 3.7.47]] | $\frac{2\pi R^{3}}{9\sqrt{3}}$ |
| [[CAL1 HW 3.7 Questions#ST 3.7.63\|ST 3.7.63]] | $2\sqrt{6}$ |
| [[CAL1 HW 3.7 Questions#ST 3.7.67\|ST 3.7.67]] | (a) $p(x) = 19 - \frac{x}{3000}$; (b) \$9.50 |
| [[CAL1 HW 3.7 Questions#ST 3.7.71\|ST 3.7.71]] | Proof |
| [[CAL1 HW 3.7 Questions#ST 3.7.79\|ST 3.7.79]] | $x = 15$ cm (fold length $15\sqrt{3} \approx 26$ cm) |
| [[CAL1 HW 3.7 Questions#ST 3.7.81\|ST 3.7.81]] | $\tfrac{\pi}{6}$ |

## ST §3.7 Optimization Problems

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Optimization Problems]]**, Stewart's steps: understand the problem, draw a diagram, introduce notation, write the quantity $Q$ to be maximized or minimized, use the given information to write $Q$ as a function of **one** variable, find its domain, then find the absolute maximum or minimum.
> - **[[Closed Interval Method]]**: for $f$ continuous on a closed interval $[a, b]$, compare the values of $f$ at the critical numbers in $(a, b)$ and at the endpoints $a$, $b$; the largest is the absolute maximum, the smallest the absolute minimum.
> - **[[First Derivative Test for Absolute Extreme Values]]**: let $c$ be a critical number of a continuous $f$ on an interval. If $f'(x) > 0$ for all $x < c$ and $f'(x) < 0$ for all $x > c$ (in the interval), then $f(c)$ is the absolute maximum; with the signs reversed, the absolute minimum. Use it when the domain is not a closed interval.
> - **Distances and areas with roots**: $d \ge 0$, so $d$ and $d^{2}$ are smallest at the same point; minimize $d^{2}$ and avoid the root (Exercises 26, 63, 71).
> - **Business**: the demand (price) function $p(x)$ is the price at which $x$ units sell; revenue $R(x) = x\,p(x)$.
> - Each answer is written as on an exam paper: variables, the function and its **domain**, the critical number, a **reason** why it gives the maximum or minimum, then a Hence line. Grading deducts points when the domain or that reason is missing. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 3.7.5
Question: [[CAL1 HW 3.7 Questions#ST 3.7.5|ST 3.7.5]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{for } -1 \le x \le 2: \ x^{2} - x - 2 = (x - 2)(x + 1) \le 0 \implies x + 2 \ge x^{2} \\
> &d(x) = (x + 2) - x^{2},\quad -1 \le x \le 2 \\
> &d'(x) = 1 - 2x = 0 \implies x = \tfrac{1}{2} \\
> &d(-1) = 0,\quad d\left(\tfrac{1}{2}\right) = \tfrac{1}{2} + 2 - \tfrac{1}{4} = \tfrac{9}{4},\quad d(2) = 0 && \text{(Closed Interval Method)}
> \end{aligned}
> $$
> Hence the maximum vertical distance is $\tfrac{9}{4}$, at $x = \tfrac{1}{2}$.
>
> \# The line and the parabola meet exactly at the endpoints $x = -1$ and $x = 2$, and between them the line is on top; so the distance is $(x + 2) - x^{2}$ without absolute value signs.

### ST 3.7.11
Question: [[CAL1 HW 3.7 Questions#ST 3.7.11|ST 3.7.11]]

> [!solution] Solution
> Let $x$ be the length of the five fences parallel to the dividers (the depth of the pens) and $y$ the length of the rectangle, all in meters.
>
> **(a)** Three configurations (top and lower left) and the general diagram (lower right):
>
> ![ST 3.7.11 figure|480](../Attachments/CAL1%20HW%203.7%20Solutions%20fig%2011.png)
>
> | depth $x$ | length $y$ | total area |
> | --- | --- | --- |
> | 10 | 125 | 1250 |
> | 20 | 100 | 2000 |
> | 30 | 75 | 2250 |
> | 40 | 50 | 2000 |
> | 50 | 25 | 1250 |
>
> There appears to be a maximum area, about 2250 m².
>
> **(b)** See the general diagram: five segments of length $x$, two of length $y$.
>
> **(c)** $A = xy$.
>
> **(d)** $5x + 2y = 300$.
>
> **(e)**
> $$
> y = 150 - \tfrac{5}{2}x \implies A(x) = 150x - \tfrac{5}{2}x^{2},\quad 0 < x < 60
> $$
>
> **(f)**
> $$
> \begin{aligned}
> &A'(x) = 150 - 5x = 0 \implies x = 30 \\
> &A'(x) > 0 \text{ for } 0 < x < 30,\ A'(x) < 0 \text{ for } 30 < x < 60 && \text{(First Derivative Test)} \\
> &x = 30 \implies y = 150 - 75 = 75,\quad A = 30 \cdot 75 = 2250
> \end{aligned}
> $$
> Hence the largest total area is 2250 m² (pens 30 m deep, rectangle 75 m long), which agrees with the estimate in (a).
>
> \# The domain comes from $x > 0$ and $y > 0$: $y = 150 - \tfrac{5}{2}x > 0 \iff x < 60$. At the optimum, half of the fence (150 m) goes into the five segments of length $x$ and half into the two of length $y$.

### ST 3.7.15
Question: [[CAL1 HW 3.7 Questions#ST 3.7.15|ST 3.7.15]]

> [!solution] Solution
> $$
> \begin{aligned}
> &x = \text{length of the west and east sides},\ y = \text{length of the north side (parallel to the barn)} \\
> &\text{cost: } 30y + 30x + \tfrac{1}{2} \cdot 30x = 1800 && \text{(the neighbor pays half of the west side)} \\
> &\implies y = 60 - \tfrac{3}{2}x,\quad 0 < x < 40 \\
> &A(x) = xy = 60x - \tfrac{3}{2}x^{2} \\
> &A'(x) = 60 - 3x = 0 \implies x = 20 \\
> &A'(x) > 0 \text{ for } 0 < x < 20,\ A'(x) < 0 \text{ for } 20 < x < 40 && \text{(First Derivative Test)} \\
> &x = 20 \implies y = 60 - 30 = 30,\quad A = 600
> \end{aligned}
> $$
> Hence the plot should be 30 m along the barn (north side) and 20 m out from the barn (west and east sides), enclosing 600 m².
>
> ![ST 3.7.15 figure|400](../Attachments/CAL1%20HW%203.7%20Solutions%20fig%2015.png)
>
> \# The farmer should spend the whole \$1800: money left over could lengthen the north side and enlarge the plot, so the cost equation uses "$= 1800$". The south side runs along the barn and costs nothing. The domain is $x > 0$, $y > 0$.

### ST 3.7.21
Question: [[CAL1 HW 3.7 Questions#ST 3.7.21|ST 3.7.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{width } w,\ \text{length } 2w,\ \text{height } h \ \ (\text{m}) \\
> &V = 2w^{2}h = 10 \implies h = \frac{5}{w^{2}} \\
> &\text{cost} = 10 \cdot 2w^{2} + 6\left(2 \cdot wh + 2 \cdot 2wh\right) = 20w^{2} + 36wh && \text{(base; four sides, no lid)} \\
> &C(w) = 20w^{2} + \frac{180}{w},\quad w > 0 \\
> &C'(w) = 40w - \frac{180}{w^{2}} = \frac{40w^{3} - 180}{w^{2}} = 0 \implies w^{3} = \frac{9}{2} \implies w = \sqrt[3]{4.5} \approx 1.651 \\
> &C'(w) < 0 \text{ for } w < \sqrt[3]{4.5},\ C'(w) > 0 \text{ for } w > \sqrt[3]{4.5} && \text{(First Derivative Test)} \\
> &C_{\min} = \frac{20w^{3} + 180}{w} = \frac{90 + 180}{w} = \frac{270}{\sqrt[3]{4.5}} \approx 163.54 && (w^{3} = 4.5)
> \end{aligned}
> $$
> Hence the least expensive container costs about \$163.54.
>
> \# Writing $C = \dfrac{20w^{3} + 180}{w}$ and using $w^{3} = 4.5$ avoids computing $w^{2}$ from a cube root; exactly, $C_{\min} = 90\sqrt[3]{6}$. The container is about $1.65$ m wide, $3.30$ m long and $h = \tfrac{5}{w^{2}} \approx 1.83$ m high.

### ST 3.7.23
Question: [[CAL1 HW 3.7 Questions#ST 3.7.23|ST 3.7.23]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{square base } x \times x,\ \text{length } l \ (\text{the longest side}),\ \text{girth} = 4x \\
> &l + 4x = 274 \implies l = 274 - 4x && \text{(use the full 274 cm)} \\
> &V(x) = x^{2}l = 274x^{2} - 4x^{3},\quad 0 \le x \le 54.8 && (x \le l \iff x \le 274 - 4x) \\
> &V'(x) = 548x - 12x^{2} = 4x(137 - 3x) = 0 \implies x = 0 \text{ or } x = \tfrac{137}{3} \approx 45.7 \\
> &V(0) = 0,\quad V\left(\tfrac{137}{3}\right) \approx 190\,471,\quad V(54.8) \approx 164\,567 && \text{(Closed Interval Method)} \\
> &x = \tfrac{137}{3} \implies l = 274 - \tfrac{548}{3} = \tfrac{274}{3} \approx 91.3
> \end{aligned}
> $$
> Hence the box measures $\tfrac{137}{3} \times \tfrac{137}{3} \times \tfrac{274}{3}$ cm, about $45.7 \times 45.7 \times 91.3$ cm.
>
> \# For a fixed base, a longer box holds more, so length plus girth should be exactly 274. The girth goes around the box perpendicular to the length, that is, around the square base: $4x$. The bound $x \le 54.8$ keeps $l$ the longest side. If instead the square's sides were the longest, the length would be $x$ and the girth $2x + 2l$; that case gives at most about 169 300 cm³, which is less.

### ST 3.7.26
Question: [[CAL1 HW 3.7 Questions#ST 3.7.26|ST 3.7.26]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{point } (x, \sqrt{x}),\ x \ge 0 \\
> &f(x) := d^{2} = (x - 3)^{2} + (\sqrt{x} - 0)^{2} = x^{2} - 5x + 9 \\
> &f'(x) = 2x - 5 = 0 \implies x = \tfrac{5}{2} \\
> &f'(x) < 0 \text{ for } 0 \le x < \tfrac{5}{2},\ f'(x) > 0 \text{ for } x > \tfrac{5}{2} && \text{(First Derivative Test)}
> \end{aligned}
> $$
> Hence the closest point is $\left(\tfrac{5}{2}, \sqrt{\tfrac{5}{2}}\right) = \left(\tfrac{5}{2}, \tfrac{\sqrt{10}}{2}\right)$, at distance $\sqrt{f(5/2)} = \tfrac{\sqrt{11}}{2}$.
>
> \# Minimize $d^{2}$ instead of $d$: since $d \ge 0$, both are smallest at the same $x$, and $d^{2}$ has no square root. Note that $(\sqrt{x})^{2} = x$, which makes $f$ a quadratic.

### ST 3.7.31
Question: [[CAL1 HW 3.7 Questions#ST 3.7.31|ST 3.7.31]]

> [!solution] Solution
> Put the base on the $x$-axis with its midpoint at the origin; the top vertex is $\left(0, \tfrac{\sqrt{3}}{2}L\right)$. Let $(x, y)$ be the upper right corner of the rectangle.
> $$
> \begin{aligned}
> &\text{right side of the triangle: } y = \sqrt{3}\left(\tfrac{L}{2} - x\right) && (\text{slope } -\sqrt{3} = -\tan 60^{\circ}) \\
> &A(x) = 2x \cdot \sqrt{3}\left(\tfrac{L}{2} - x\right) = \sqrt{3}\,(Lx - 2x^{2}),\quad 0 \le x \le \tfrac{L}{2} \\
> &A'(x) = \sqrt{3}\,(L - 4x) = 0 \implies x = \tfrac{L}{4} \\
> &A(0) = A\left(\tfrac{L}{2}\right) = 0,\quad A\left(\tfrac{L}{4}\right) = \tfrac{\sqrt{3}}{8}L^{2} && \text{(Closed Interval Method)} \\
> &x = \tfrac{L}{4} \implies \text{width } 2x = \tfrac{L}{2},\ \text{height } y = \sqrt{3} \cdot \tfrac{L}{4} = \tfrac{\sqrt{3}}{4}L
> \end{aligned}
> $$
> Hence the rectangle has width $\tfrac{L}{2}$ and height $\tfrac{\sqrt{3}}{4}L$.
>
> ![ST 3.7.31 figure|320](../Attachments/CAL1%20HW%203.7%20Solutions%20fig%2031.png)
>
> \# Both upper corners lie on the slanted sides, so the rectangle is symmetric about the height of the triangle and has width $2x$. Its height is half the triangle's height, and its area $\tfrac{\sqrt{3}}{8}L^{2}$ is half the triangle's area $\tfrac{\sqrt{3}}{4}L^{2}$.

### ST 3.7.37
Question: [[CAL1 HW 3.7 Questions#ST 3.7.37|ST 3.7.37]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{cylinder: radius } \rho,\ \text{height } 2h \\
> &\rho^{2} + h^{2} = r^{2} && \text{(Pythagoras in the cross-section)} \\
> &V = \pi\rho^{2} \cdot 2h = 2\pi(r^{2} - h^{2})h = 2\pi(r^{2}h - h^{3}),\quad 0 \le h \le r \\
> &V'(h) = 2\pi(r^{2} - 3h^{2}) = 0 \implies h = \frac{r}{\sqrt{3}} \\
> &V(0) = V(r) = 0,\quad V\left(\tfrac{r}{\sqrt{3}}\right) = 2\pi\left(r^{2} - \tfrac{r^{2}}{3}\right)\frac{r}{\sqrt{3}} = \frac{4\pi r^{3}}{3\sqrt{3}} && \text{(Closed Interval Method)}
> \end{aligned}
> $$
> Hence the largest volume is $\dfrac{4\pi r^{3}}{3\sqrt{3}} = \dfrac{4\sqrt{3}}{9}\pi r^{3}$.
>
> ![ST 3.7.37 figure|300](../Attachments/CAL1%20HW%203.7%20Solutions%20fig%2037.png)
>
> \# Taking half the height as the variable gives the right triangle center–middle of a side–corner with legs $\rho$ and $h$ and hypotenuse $r$. The best cylinder has radius $\sqrt{\tfrac{2}{3}}\,r$ and height $\tfrac{2r}{\sqrt{3}}$, and fills $\tfrac{1}{\sqrt{3}} \approx 58$ % of the sphere.

### ST 3.7.47
Question: [[CAL1 HW 3.7 Questions#ST 3.7.47|ST 3.7.47]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{the radius } R \text{ of the paper becomes the slant height of the cone} \\
> &\text{cone: radius } r,\ \text{height } h,\quad r^{2} + h^{2} = R^{2} \\
> &V = \tfrac{1}{3}\pi r^{2}h = \tfrac{\pi}{3}(R^{2} - h^{2})h = \tfrac{\pi}{3}(R^{2}h - h^{3}),\quad 0 \le h \le R \\
> &V'(h) = \tfrac{\pi}{3}(R^{2} - 3h^{2}) = 0 \implies h = \frac{R}{\sqrt{3}} \\
> &V(0) = V(R) = 0,\quad V\left(\tfrac{R}{\sqrt{3}}\right) = \frac{\pi}{3} \cdot \frac{2R^{2}}{3} \cdot \frac{R}{\sqrt{3}} = \frac{2\pi R^{3}}{9\sqrt{3}} && \text{(Closed Interval Method)}
> \end{aligned}
> $$
> Hence the maximum capacity is $\dfrac{2\pi R^{3}}{9\sqrt{3}} = \dfrac{2\sqrt{3}}{27}\pi R^{3}$.
>
> ![ST 3.7.47 figure|300](../Attachments/CAL1%20HW%203.7%20Solutions%20fig%2047.png)
>
> \# When $CA$ is joined to $CB$, the center $C$ becomes the tip of the cone and the remaining arc becomes the rim. With $h$ as the variable there is no square root (with $r$ one would get $V = \tfrac{\pi}{3}r^{2}\sqrt{R^{2} - r^{2}}$). Same computation as Exercise 37. At the optimum $r = \sqrt{\tfrac{2}{3}}\,R$, so the sector cut out has angle $2\pi\left(1 - \sqrt{\tfrac{2}{3}}\right) \approx 66^{\circ}$.

### ST 3.7.63
Question: [[CAL1 HW 3.7 Questions#ST 3.7.63|ST 3.7.63]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{tangent at } \left(a, \tfrac{3}{a}\right),\ a > 0: \ y' = -\frac{3}{x^{2}} \implies \text{slope } -\frac{3}{a^{2}} \\
> &y - \frac{3}{a} = -\frac{3}{a^{2}}(x - a) \\
> &x\text{-intercept } (y = 0): \ x = 2a,\qquad y\text{-intercept } (x = 0): \ y = \frac{6}{a} \\
> &f(a) := L^{2} = (2a)^{2} + \left(\frac{6}{a}\right)^{2} = 4a^{2} + \frac{36}{a^{2}},\quad a > 0 \\
> &f'(a) = 8a - \frac{72}{a^{3}} = \frac{8(a^{4} - 9)}{a^{3}} = 0 \implies a^{4} = 9 \implies a = \sqrt{3} \\
> &f'(a) < 0 \text{ for } 0 < a < \sqrt{3},\ f'(a) > 0 \text{ for } a > \sqrt{3} && \text{(First Derivative Test)} \\
> &f(\sqrt{3}) = 12 + 12 = 24 \implies L = \sqrt{24} = 2\sqrt{6}
> \end{aligned}
> $$
> Hence the shortest length is $2\sqrt{6} \approx 4.90$.
>
> \# The segment's length is $L = \sqrt{(2a)^{2} + (6/a)^{2}}$ (Pythagoras between the intercepts); minimize $L^{2}$. The point of tangency $(\sqrt{3}, \sqrt{3})$ is the midpoint of the segment, as it is for every tangent to $y = 3/x$.

### ST 3.7.67
Question: [[CAL1 HW 3.7 Questions#ST 3.7.67|ST 3.7.67]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> &x = \text{attendance},\ p(x) = \text{ticket price, linear in } x \\
> &\text{slope} = \frac{8 - 10}{33000 - 27000} = -\frac{1}{3000} \\
> &p(x) = 10 - \frac{1}{3000}(x - 27000) = 19 - \frac{x}{3000}
> \end{aligned}
> $$
>
> **(b)**
> $$
> \begin{aligned}
> &R(x) = x\,p(x) = 19x - \frac{x^{2}}{3000},\quad 0 \le x \le 55000 \\
> &R'(x) = 19 - \frac{x}{1500} = 0 \implies x = 28500 \\
> &R'(x) > 0 \text{ for } x < 28500,\ R'(x) < 0 \text{ for } x > 28500 && \text{(First Derivative Test)} \\
> &p(28500) = 19 - 9.5 = 9.5
> \end{aligned}
> $$
> Hence (a) $p(x) = 19 - \dfrac{x}{3000}$; (b) tickets should cost \$9.50 (attendance 28,500, revenue \$270,750).
>
> \# The demand function gives the price as a function of the number of tickets sold. The optimal attendance 28,500 is below the 55,000 seats, so the capacity of the stadium does not restrict the answer.

### ST 3.7.71
Question: [[CAL1 HW 3.7 Questions#ST 3.7.71|ST 3.7.71]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{pf: Let the perimeter be } P,\ \text{the two equal sides } a,\ \text{the base } b: \ 2a + b = P. \\
> &\text{height to the base: } h = \sqrt{a^{2} - \tfrac{b^{2}}{4}},\quad a = \frac{P - b}{2} \implies h^{2} = \frac{(P - b)^{2} - b^{2}}{4} = \frac{P^{2} - 2Pb}{4} \\
> &A = \tfrac{1}{2}bh \implies A^{2} = \frac{b^{2}}{4} \cdot \frac{P^{2} - 2Pb}{4} = \frac{P^{2}b^{2} - 2Pb^{3}}{16},\quad 0 < b < \tfrac{P}{2} \\
> &\text{Let } g(b) := P^{2}b^{2} - 2Pb^{3}. \text{ Since } A \ge 0, \ A \text{ is largest where } g \text{ is largest.} \\
> &g'(b) = 2P^{2}b - 6Pb^{2} = 2Pb\,(P - 3b) \\
> &g'(b) > 0 \text{ for } 0 < b < \tfrac{P}{3},\quad g'(b) < 0 \text{ for } \tfrac{P}{3} < b < \tfrac{P}{2} \\
> &\implies g, \text{ and hence } A, \text{ has its absolute maximum at } b = \tfrac{P}{3} && \text{(First Derivative Test)} \\
> &b = \tfrac{P}{3} \implies a = \frac{P - P/3}{2} = \frac{P}{3} = b \\[4pt]
> &\text{Hence the isosceles triangle of greatest area has all three sides } \tfrac{P}{3}: \text{ it is equilateral.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The bound $b < \tfrac{P}{2}$ is the triangle inequality $b < a + a = P - b$; at $b = \tfrac{P}{2}$ the triangle is flat ($h = 0$). Working with $A^{2}$ instead of $A$ avoids differentiating a square root.

### ST 3.7.79
Question: [[CAL1 HW 3.7 Questions#ST 3.7.79|ST 3.7.79]]

> [!solution] Solution
> Let the fold run from $E$ on the right edge ($x$ below the corner) to $F$ on the top edge ($t$ from the corner); the corner lands at $Q$ on the bottom edge, $u$ from the lower right corner.
>
> ![ST 3.7.79 figure|400](../Attachments/CAL1%20HW%203.7%20Solutions%20fig%2079.png)
>
> $$
> \begin{aligned}
> &\text{folding keeps lengths and angles: } EQ = x,\ FQ = t,\ \angle FQE = 90^{\circ} \\
> &u^{2} + (20 - x)^{2} = x^{2} \implies u^{2} = 40x - 400 && \text{(right triangle at the lower right corner)} \\
> &(t - u)^{2} + 20^{2} = t^{2} \implies t = \frac{u^{2} + 400}{2u} = \frac{20x}{u} && \text{(right triangle below } F) \\
> &y^{2} = x^{2} + t^{2} = x^{2} + \frac{400x^{2}}{40x - 400} = x^{2} + \frac{10x^{2}}{x - 10} = \frac{x^{3}}{x - 10} && \text{(right angle at the corner)} \\[4pt]
> &f(x) := y^{2} = \frac{x^{3}}{x - 10},\quad 45 - 15\sqrt{5} \le x \le 20 && (t \le 30,\ x \le 20) \\
> &f'(x) = \frac{3x^{2}(x - 10) - x^{3}}{(x - 10)^{2}} = \frac{2x^{2}(x - 15)}{(x - 10)^{2}} = 0 \implies x = 15 \\
> &f(45 - 15\sqrt{5}) \approx 1031,\quad f(15) = \frac{3375}{5} = 675,\quad f(20) = 800 && \text{(Closed Interval Method)}
> \end{aligned}
> $$
> Hence fold so that $x = 15$ cm; the shortest fold is $y = \sqrt{675} = 15\sqrt{3} \approx 26$ cm.
>
> \# The domain: $F$ must stay on the top edge, $t \le 30$, that is, $20x \le 30\sqrt{40x - 400} \iff x^{2} - 90x + 900 \le 0 \iff x \ge 45 - 15\sqrt{5} \approx 11.5$; and $E$ must stay on the right edge, $x \le 20$. At $x = 15$: $u = 10\sqrt{2}$ and $t = 15\sqrt{2} \approx 21.2 \le 30$. The reflected corner $Q$ is where the corner $C$ lands, so $EQ = EC$ and $FQ = FC$.

### ST 3.7.81
Question: [[CAL1 HW 3.7 Questions#ST 3.7.81|ST 3.7.81]]

> [!solution] Solution
> When the slower runner is $x$ from $S$, the faster is $3x$ from $S$. Let $\alpha$ and $\beta$ be the angles at $P$ between $PS$ and the lines to the slower and the faster runner, so $\theta = \beta - \alpha$.
> $$
> \begin{aligned}
> &\tan\alpha = \frac{x}{1} = x,\quad \tan\beta = 3x \\
> &\tan\theta = \tan(\beta - \alpha) = \frac{\tan\beta - \tan\alpha}{1 + \tan\beta\tan\alpha} = \frac{2x}{1 + 3x^{2}} =: g(x),\quad x \ge 0 \\
> &g'(x) = \frac{2(1 + 3x^{2}) - 2x \cdot 6x}{(1 + 3x^{2})^{2}} = \frac{2(1 - 3x^{2})}{(1 + 3x^{2})^{2}} = 0 \implies x = \frac{1}{\sqrt{3}} \\
> &g'(x) > 0 \text{ for } 0 \le x < \tfrac{1}{\sqrt{3}},\ g'(x) < 0 \text{ for } x > \tfrac{1}{\sqrt{3}} && \text{(First Derivative Test)} \\
> &g\left(\tfrac{1}{\sqrt{3}}\right) = \frac{2/\sqrt{3}}{1 + 1} = \frac{1}{\sqrt{3}} \implies \theta = \frac{\pi}{6}
> \end{aligned}
> $$
> Hence the maximum angle of sight is $\dfrac{\pi}{6}$ (30°).
>
> ![ST 3.7.81 figure|360](../Attachments/CAL1%20HW%203.7%20Solutions%20fig%2081.png)
>
> \# Why the Hint works: $0 \le \theta < \tfrac{\pi}{2}$, and $\tan$ is increasing there, so $\theta$ is largest exactly when $\tan\theta$ is largest. The subtraction formula for $\tan$ is in Appendix D. At the best moment the runners are at $\tfrac{1}{\sqrt{3}}$ and $\sqrt{3}$, seen from $P$ at $30^{\circ}$ and $60^{\circ}$ from $PS$.
