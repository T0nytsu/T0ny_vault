---
course: [CAL1]
semester: "115-1"
chapter: ["4.3"]
tags: [calculus, homework, questions, integrals, derivatives]
source:
  - "Stewart, Calculus, §4.3 Exercises, pp. 335-338, scanned PDF"
  - "The figures of Exercises 3 and 5 are redrawn from the scan"
created: 2026-11-18
solutions: "[[CAL1 HW 4.3 Solutions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> ST §4.3: 3, 5, 9, 11, 13, 15, 17, 19, 21, 27, 31, 37, 41, 43, 45, 47, 49, 59–63, 65, 67, 68, 73, 74, 81. These are the exercises assigned for Section 4.3. ST is Stewart, *Calculus*. Solutions: [[CAL1 HW 4.3 Solutions]].

## ST §4.3 The Fundamental Theorem of Calculus

### ST 4.3.3
Let $g(x) = \int_0^x f(t)\,dt$, where $f$ is the function whose graph is shown.
- (a) Evaluate $g(0)$, $g(1)$, $g(2)$, $g(3)$, and $g(6)$.
- (b) On what interval is $g$ increasing?
- (c) Where does $g$ have a maximum value?
- (d) Sketch a rough graph of $g$.

![ST 4.3.3 figure|440](../Attachments/CAL1%20HW%204.3%20Questions%20fig%203.png)

### ST 4.3.5
**5–6** The graph of a function $f$ is shown. Let $g$ be the function that represents the area under the graph of $f$ between 0 and $x$.
- (a) Use geometry to find a formula for $g(x)$.
- (b) Verify that $g$ is an antiderivative of $f$ and explain how this confirms Part 1 of the Fundamental Theorem of Calculus for the function $f$.

![ST 4.3.5 figure|400](../Attachments/CAL1%20HW%204.3%20Questions%20fig%205.png)

### ST 4.3.9
**9–20** Use Part 1 of the Fundamental Theorem of Calculus to find the derivative of the function.
$$
g(x) = \int_0^x \sqrt{t + t^3}\,dt
$$

### ST 4.3.11
**9–20** Use Part 1 of the Fundamental Theorem of Calculus to find the derivative of the function.
$$
g(w) = \int_0^w \sin(1 + t^3)\,dt
$$

### ST 4.3.13
**9–20** Use Part 1 of the Fundamental Theorem of Calculus to find the derivative of the function.
$$
F(x) = \int_x^0 \sqrt{1 + \sec t}\,dt
$$
[*Hint:* $\int_x^0 \sqrt{1 + \sec t}\,dt = -\int_0^x \sqrt{1 + \sec t}\,dt$]

### ST 4.3.15
**9–20** Use Part 1 of the Fundamental Theorem of Calculus to find the derivative of the function.
$$
h(x) = \int_2^{1/x} \sin^4 t\,dt
$$

### ST 4.3.17
**9–20** Use Part 1 of the Fundamental Theorem of Calculus to find the derivative of the function.
$$
y = \int_1^{3x+2} \frac{t}{1 + t^3}\,dt
$$

### ST 4.3.19
**9–20** Use Part 1 of the Fundamental Theorem of Calculus to find the derivative of the function.
$$
y = \int_{\sqrt{x}}^{\pi/4} \theta\tan\theta\,d\theta
$$

### ST 4.3.21
**21–24** Use Part 2 of the Fundamental Theorem of Calculus to evaluate the integral and interpret the result as an area or a difference of areas. Illustrate with a sketch.
$$
\int_{-1}^{2} x^3\,dx
$$

### ST 4.3.27
**25–46** Evaluate the integral.
$$
\int_0^2 \left(\tfrac{4}{5}t^3 - \tfrac{3}{4}t^2 + \tfrac{2}{5}t\right) dt
$$

### ST 4.3.31
**25–46** Evaluate the integral.
$$
\int_0^4 (t^2 + t^{3/2})\,dt
$$

### ST 4.3.37
**25–46** Evaluate the integral.
$$
\int_1^4 \frac{2 + x^2}{\sqrt{x}}\,dx
$$

### ST 4.3.41
**25–46** Evaluate the integral.
$$
\int_0^{\pi/3} \sec\theta\tan\theta\,d\theta
$$

### ST 4.3.43
**25–46** Evaluate the integral.
$$
\int_0^1 (1 + r)^3\,dr
$$

### ST 4.3.45
**25–46** Evaluate the integral.
$$
\int_0^\pi f(x)\,dx \quad \text{where } f(x) = \begin{cases} \sin x & \text{if } 0 \le x < \pi/2 \\ \cos x & \text{if } \pi/2 \le x \le \pi \end{cases}
$$

### ST 4.3.47
**47–50** Sketch the region enclosed by the given curves and calculate its area.
$$
y = \sqrt{x}, \quad y = 0, \quad x = 4
$$

### ST 4.3.49
**47–50** Sketch the region enclosed by the given curves and calculate its area.
$$
y = 4 - x^2, \quad y = 0
$$

### ST 4.3.59
**59–62** Find the derivative of the function.
$$
g(x) = \int_{2x}^{3x} \frac{u^2 - 1}{u^2 + 1}\,du
$$
[*Hint:* $\int_{2x}^{3x} f(u)\,du = \int_{2x}^{0} f(u)\,du + \int_0^{3x} f(u)\,du$]

### ST 4.3.60
**59–62** Find the derivative of the function.
$$
g(x) = \int_{1-2x}^{1+2x} t\sin t\,dt
$$

### ST 4.3.61
**59–62** Find the derivative of the function.
$$
h(x) = \int_{\sqrt{x}}^{x^3} \cos(t^2)\,dt
$$

### ST 4.3.62
**59–62** Find the derivative of the function.
$$
g(x) = \int_{\tan x}^{x^2} \frac{1}{\sqrt{2 + t^4}}\,dt
$$

### ST 4.3.63
Let $F(x) = \int_\pi^x \dfrac{\cos t}{t}\,dt$. Find an equation of the tangent line to the curve $y = F(x)$ at the point with $x$-coordinate $\pi$.

### ST 4.3.65
On what interval is the curve
$$
y = \int_0^x \frac{t^2}{t^2 + t + 2}\,dt
$$
concave downward?

### ST 4.3.67
If $f(1) = 12$, $f'$ is continuous, and $\int_1^4 f'(x)\,dx = 17$, what is the value of $f(4)$?

### ST 4.3.68
If $f(x) = \int_0^{\sin x} \sqrt{1 + t^2}\,dt$ and $g(y) = \int_3^y f(x)\,dx$, find $g''(\pi/6)$.

### ST 4.3.73
**73–74** Evaluate the limit by first recognizing the sum as a Riemann sum for a function defined on $[0, 1]$.
$$
\lim_{n \to \infty} \sum_{i=1}^{n} \left(\frac{i^4}{n^5} + \frac{i}{n^2}\right)
$$

### ST 4.3.74
**73–74** Evaluate the limit by first recognizing the sum as a Riemann sum for a function defined on $[0, 1]$.
$$
\lim_{n \to \infty} \frac{1}{n}\left(\sqrt{\frac{1}{n}} + \sqrt{\frac{2}{n}} + \sqrt{\frac{3}{n}} + \cdots + \sqrt{\frac{n}{n}}\right)
$$

### ST 4.3.81
Find a function $f$ and a number $a$ such that
$$
6 + \int_a^x \frac{f(t)}{t^2}\,dt = 2\sqrt{x} \qquad \text{for all } x > 0
$$
