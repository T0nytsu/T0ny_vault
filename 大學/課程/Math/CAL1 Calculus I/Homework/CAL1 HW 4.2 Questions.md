---
course: [CAL1]
semester: "115-1"
chapter: ["4.2"]
tags: [calculus, homework, questions, integrals]
source:
  - "Stewart, Calculus, §4.2 Exercises, pp. 324-327, scanned PDF"
  - "The figures of Exercises 35, 61 and 63 are redrawn from the scan"
created: 2026-11-18
solutions: "[[CAL1 HW 4.2 Solutions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> ST §4.2: 1, 9, 19–22, 23, 25, 33, 35, 51, 52, 57–61, 63, 65–68, 75, 83, 84. These are the exercises assigned for Section 4.2. ST is Stewart, *Calculus*. Solutions: [[CAL1 HW 4.2 Solutions]].

## ST §4.2 The Definite Integral

### ST 4.2.1
Evaluate the Riemann sum for $f(x) = x - 1$, $-6 \le x \le 4$, with five subintervals, taking the sample points to be right endpoints. Explain, with the aid of a diagram, what the Riemann sum represents.

### ST 4.2.9
**9–10** Use the Midpoint Rule with $n = 4$ to approximate the integral.
$$
\int_0^8 x^2\,dx
$$

### ST 4.2.19
**19–22** Express the limit as a definite integral on the given interval.
$$
\lim_{n \to \infty} \sum_{i=1}^{n} \frac{\sin x_i}{1 + x_i}\,\Delta x, \quad [0, \pi]
$$

### ST 4.2.20
**19–22** Express the limit as a definite integral on the given interval.
$$
\lim_{n \to \infty} \sum_{i=1}^{n} x_i\sqrt{1 + x_i^3}\,\Delta x, \quad [2, 5]
$$

### ST 4.2.21
**19–22** Express the limit as a definite integral on the given interval.
$$
\lim_{n \to \infty} \sum_{i=1}^{n} \left[5(x_i^*)^3 - 4x_i^*\right]\Delta x, \quad [2, 7]
$$

### ST 4.2.22
**19–22** Express the limit as a definite integral on the given interval.
$$
\lim_{n \to \infty} \sum_{i=1}^{n} \frac{x_i^*}{(x_i^*)^2 + 4}\,\Delta x, \quad [1, 3]
$$

### ST 4.2.23
**23–24** Show that the definite integral is equal to $\lim_{n \to \infty} R_n$ and then evaluate the limit.
$$
\int_0^4 (x - x^2)\,dx, \quad R_n = \frac{4}{n}\sum_{i=1}^{n}\left[\frac{4i}{n} - \frac{16i^2}{n^2}\right]
$$

### ST 4.2.25
**25–26** Express the integral as a limit of Riemann sums using right endpoints. Do not evaluate the limit.
$$
\int_1^3 \sqrt{4 + x^2}\,dx
$$

### ST 4.2.33
**27–34** Use the form of the definition of the integral given in Theorem 4 to evaluate the integral.
$$
\int_0^1 (x^3 - 3x^2)\,dx
$$

### ST 4.2.35
The graph of $f$ is shown. Evaluate each integral by interpreting it in terms of areas.
- (a) $\int_0^2 f(x)\,dx$
- (b) $\int_0^5 f(x)\,dx$
- (c) $\int_5^7 f(x)\,dx$
- (d) $\int_3^7 f(x)\,dx$
- (e) $\int_3^7 \lvert f(x) \rvert\,dx$
- (f) $\int_2^0 f(x)\,dx$

![ST 4.2.35 figure|460](../Attachments/CAL1%20HW%204.2%20Questions%20fig%2035.png)

### ST 4.2.51
Evaluate $\int_1^1 \sqrt{1 + x^4}\,dx$.

### ST 4.2.52
Given that $\int_0^\pi \sin^4 x\,dx = \tfrac{3}{8}\pi$, what is $\int_\pi^0 \sin^4\theta\,d\theta$?

### ST 4.2.57
Write as a single integral in the form $\int_a^b f(x)\,dx$:
$$
\int_{-2}^{2} f(x)\,dx + \int_2^5 f(x)\,dx - \int_{-2}^{-1} f(x)\,dx
$$

### ST 4.2.58
If $\int_2^8 f(x)\,dx = 7.3$ and $\int_2^4 f(x)\,dx = 5.9$, find $\int_4^8 f(x)\,dx$.

### ST 4.2.59
If $\int_0^9 f(x)\,dx = 37$ and $\int_0^9 g(x)\,dx = 16$, find
$$
\int_0^9 [2f(x) + 3g(x)]\,dx
$$

### ST 4.2.60
Find $\int_0^5 f(x)\,dx$ if
$$
f(x) = \begin{cases} 3 & \text{for } x < 3 \\ x & \text{for } x \ge 3 \end{cases}
$$

### ST 4.2.61
For the function $f$ whose graph is shown, list the following quantities in increasing order, from smallest to largest, and explain your reasoning.
- (A) $\int_0^8 f(x)\,dx$
- (B) $\int_0^3 f(x)\,dx$
- (C) $\int_3^8 f(x)\,dx$
- (D) $\int_4^8 f(x)\,dx$
- (E) $f'(1)$

![ST 4.2.61 figure|440](../Attachments/CAL1%20HW%204.2%20Questions%20fig%2061.png)

### ST 4.2.63
Each of the regions $A$, $B$, and $C$ bounded by the graph of $f$ and the $x$-axis has area 3. Find the value of
$$
\int_{-4}^{2} [f(x) + 2x + 5]\,dx
$$

![ST 4.2.63 figure|460](../Attachments/CAL1%20HW%204.2%20Questions%20fig%2063.png)

### ST 4.2.65
**65–68** Use the properties of integrals to verify the inequality without evaluating the integrals.
$$
\int_0^4 (x^2 - 4x + 4)\,dx \ge 0
$$

### ST 4.2.66
**65–68** Use the properties of integrals to verify the inequality without evaluating the integrals.
$$
\int_0^1 \sqrt{1 + x^2}\,dx \le \int_0^1 \sqrt{1 + x}\,dx
$$

### ST 4.2.67
**65–68** Use the properties of integrals to verify the inequality without evaluating the integrals.
$$
2 \le \int_{-1}^{1} \sqrt{1 + x^2}\,dx \le 2\sqrt{2}
$$

### ST 4.2.68
**65–68** Use the properties of integrals to verify the inequality without evaluating the integrals.
$$
\frac{\pi}{12} \le \int_{\pi/6}^{\pi/3} \sin x\,dx \le \frac{\sqrt{3}\,\pi}{12}
$$

### ST 4.2.75
**75–76** Use properties of integrals, together with Exercises 47 and 48, to prove the inequality.
$$
\int_1^3 \sqrt{x^4 + 1}\,dx \ge \frac{26}{3}
$$

### ST 4.2.83
**83–84** Express the limit as a definite integral.
$$
\lim_{n \to \infty} \sum_{i=1}^{n} \frac{i^4}{n^5}
$$
[*Hint:* Consider $f(x) = x^4$.]

### ST 4.2.84
**83–84** Express the limit as a definite integral.
$$
\lim_{n \to \infty} \frac{1}{n} \sum_{i=1}^{n} \frac{1}{1 + (i/n)^2}
$$
