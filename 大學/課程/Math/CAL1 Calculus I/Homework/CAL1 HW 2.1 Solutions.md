---
course: [CAL1]
chapter: ["2.1"]
tags: [calculus, homework, solutions, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §2.1, pp. 108-116, scanned PDF (definitions and equation numbers)"
created: 2026-10-05
questions: "[[CAL1 HW 2.1 Questions]]"
---
一## Answer Key

| Exercise                                       | Answer                                                                                                                                    |
| ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| [[CAL1 HW 2.1 Questions#ST 2.1.5\|ST 2.1.5]]   | $m = 7$; $y = 7x - 17$                                                                                                                    |
| [[CAL1 HW 2.1 Questions#ST 2.1.7\|ST 2.1.7]]   | $m = -5$; $y = -5x + 6$                                                                                                                   |
| [[CAL1 HW 2.1 Questions#ST 2.1.17\|ST 2.1.17]] | $g'(0) < 0 < g'(4) < g'(2) < g'(-2)$                                                                                                      |
| [[CAL1 HW 2.1 Questions#ST 2.1.21\|ST 2.1.21]] | $f'(3) = \tfrac{5}{9}$                                                                                                                    |
| [[CAL1 HW 2.1 Questions#ST 2.1.23\|ST 2.1.23]] | $f'(a) = 4a - 5$                                                                                                                          |
| [[CAL1 HW 2.1 Questions#ST 2.1.25\|ST 2.1.25]] | $f'(a) = -\dfrac{2a}{(a^2 + 1)^2}$                                                                                                        |
| [[CAL1 HW 2.1 Questions#ST 2.1.27\|ST 2.1.27]] | $y = -\tfrac{1}{2}x + 3$                                                                                                                  |
| [[CAL1 HW 2.1 Questions#ST 2.1.29\|ST 2.1.29]] | $f'(1) = 3$; $y = 3x - 1$                                                                                                                 |
| [[CAL1 HW 2.1 Questions#ST 2.1.33\|ST 2.1.33]] | $f(2) = 3$, $f'(2) = 4$                                                                                                                   |
| [[CAL1 HW 2.1 Questions#ST 2.1.35\|ST 2.1.35]] | velocity $32$ m/s, speed $32$ m/s                                                                                                         |
| [[CAL1 HW 2.1 Questions#ST 2.1.39\|ST 2.1.39]] | Graph (one possible $f$)                                                                                                                  |
| [[CAL1 HW 2.1 Questions#ST 2.1.41\|ST 2.1.41]] | Graph (one possible $g$)                                                                                                                  |
| [[CAL1 HW 2.1 Questions#ST 2.1.43\|ST 2.1.43]] | $f(x) = \sqrt{x}$, $a = 9$                                                                                                                |
| [[CAL1 HW 2.1 Questions#ST 2.1.45\|ST 2.1.45]] | $f(x) = x^6$, $a = 2$                                                                                                                     |
| [[CAL1 HW 2.1 Questions#ST 2.1.47\|ST 2.1.47]] | $f(x) = \tan x$, $a = \tfrac{\pi}{4}$                                                                                                     |
| [[CAL1 HW 2.1 Questions#ST 2.1.49\|ST 2.1.49]] | (a) (i) $20.25$ dollars/unit, (ii) $20.05$ dollars/unit; (b) $20$ dollars/unit                                                            |
| [[CAL1 HW 2.1 Questions#ST 2.1.53\|ST 2.1.53]] | (a) the rate of change of the oxygen solubility with respect to the water temperature, in (mg/L)/°C; (b) $S'(16) \approx -0.25$ (mg/L)/°C |
| [[CAL1 HW 2.1 Questions#ST 2.1.57\|ST 2.1.57]] | $f'(0)$ does not exist                                                                                                                    |
| [[CAL1 HW 2.1 Questions#ST 2.1.58\|ST 2.1.58]] | $f'(0)$ exists, $f'(0) = 0$                                                                                                               |

Additional exercises, not assigned:

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 2.1 Questions#ST 2.1.8\|ST 2.1.8]] | $m = -\tfrac{3}{4}$; $y = -\tfrac{3}{4}x + \tfrac{5}{4}$ |
| [[CAL1 HW 2.1 Questions#ST 2.1.12\|ST 2.1.12]] | (a) $6.28$ m/s; (b) $10 - 3.72a$ m/s; (c) $t = \tfrac{10}{1.86} \approx 5.4$ s; (d) $-10$ m/s |
| [[CAL1 HW 2.1 Questions#ST 2.1.22\|ST 2.1.22]] | $f'(1) = -\tfrac{1}{8}$ |
| [[CAL1 HW 2.1 Questions#ST 2.1.34\|ST 2.1.34]] | $f(4) = 3$, $f'(4) = \tfrac{1}{4}$ |
| [[CAL1 HW 2.1 Questions#ST 2.1.36\|ST 2.1.36]] | velocity $-\tfrac{9}{5}$ m/s, speed $\tfrac{9}{5}$ m/s |
| [[CAL1 HW 2.1 Questions#ST 2.1.55\|ST 2.1.55]] | (a) $-0.015$, $-0.012$, $-0.012$, $-0.011$ (g/dL)/h; (b) $\approx -0.012$ (g/dL)/h |

## ST §2.1 Derivatives and Rates of Change

> [!note] Note
> The facts that the answers use, each under its name. An answer writes the formula itself; the numbers are those of ST §2.1 and matter only where a question names them ("Use Equation 5").
> - **[[Tangent Line]]** (Definition 1): the tangent line to $y = f(x)$ at $P(a, f(a))$ is the line through $P$ with slope $m = \lim_{x \to a} \dfrac{f(x) - f(a)}{x - a}$, provided that this limit exists.
> - **Slope with $h$** (Equation 2): $m = \lim_{h \to 0} \dfrac{f(a + h) - f(a)}{h}$, where $h = x - a$.
> - **Instantaneous velocity** (Definition 3): position function $s = f(t)$ $\implies$ $v(a) = \lim_{h \to 0} \dfrac{f(a + h) - f(a)}{h}$. **Speed** $= \lvert v(a) \rvert$.
> - **[[Derivative]] at $a$** (Definition 4): $f'(a) = \lim_{h \to 0} \dfrac{f(a + h) - f(a)}{h}$, if this limit exists.
> - **Derivative with $x \to a$** (Equation 5): $f'(a) = \lim_{x \to a} \dfrac{f(x) - f(a)}{x - a}$.
> - **Equation of the tangent line** at $(a, f(a))$: $y - f(a) = f'(a)(x - a)$.
> - **Average rate of change** of $y = f(x)$ over $[x_1, x_2]$: $\dfrac{\Delta y}{\Delta x} = \dfrac{f(x_2) - f(x_1)}{x_2 - x_1}$. **Instantaneous rate of change** at $x = a$: $f'(a)$. Units: units of $y$ per unit of $x$.
> - **[[Squeeze Theorem]]** (ST §1.6): $f(x) \le g(x) \le h(x)$ near $a$, $\lim_{x \to a} f(x) = \lim_{x \to a} h(x) = L$ $\implies$ $\lim_{x \to a} g(x) = L$.
> - Each answer is written as on an exam paper: the computation first, one $=$ per line, then the conclusion on a Hence line. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 2.1.5
Question: [[CAL1 HW 2.1 Questions#ST 2.1.5|ST 2.1.5]]

> [!solution] Solution
> Let $f(x) = 2x^2 - 5x + 1$, $a = 3$, $f(3) = 4$.
> $$
> \begin{aligned}
> m &= \lim_{h \to 0} \frac{f(3 + h) - f(3)}{h} \\
> &= \lim_{h \to 0} \frac{2(3 + h)^2 - 5(3 + h) + 1 - 4}{h} \\
> &= \lim_{h \to 0} \frac{18 + 12h + 2h^2 - 15 - 5h - 3}{h} \\
> &= \lim_{h \to 0} \frac{7h + 2h^2}{h} \\
> &= \lim_{h \to 0} (7 + 2h) && (h \ne 0) \\
> &= 7
> \end{aligned}
> $$
> Hence the tangent line is $y - 4 = 7(x - 3)$, i.e. $y = 7x - 17$.
>
> \# Two steps: the slope $m$ from the limit, then the point-slope form $y - y_1 = m(x - x_1)$ with the given point. The constants in the numerator must cancel ($18 - 15 + 1 - 4 = 0$); if they do not, $f(3)$ is wrong.

### ST 2.1.7
Question: [[CAL1 HW 2.1 Questions#ST 2.1.7|ST 2.1.7]]

> [!solution] Solution
> Let $f(x) = \dfrac{x + 2}{x - 3}$, $a = 2$, $f(2) = -4$.
> $$
> \begin{aligned}
> m &= \lim_{x \to 2} \frac{f(x) - f(2)}{x - 2} \\
> &= \lim_{x \to 2} \frac{\dfrac{x + 2}{x - 3} + 4}{x - 2} \\
> &= \lim_{x \to 2} \frac{(x + 2) + 4(x - 3)}{(x - 3)(x - 2)} \\
> &= \lim_{x \to 2} \frac{5(x - 2)}{(x - 3)(x - 2)} \\
> &= \lim_{x \to 2} \frac{5}{x - 3} && (x - 2 \ne 0) \\
> &= -5 && \text{(Direct Substitution Property)}
> \end{aligned}
> $$
> Hence the tangent line is $y + 4 = -5(x - 2)$, i.e. $y = -5x + 6$.
>
> \# Here the form with $x \to a$ is shorter than the form with $h$: one common denominator, and the factor $x - 2$ appears by itself. With $h$: $m = \lim_{h \to 0} \dfrac{1}{h}\left(\dfrac{4 + h}{h - 1} + 4\right) = \lim_{h \to 0} \dfrac{5}{h - 1} = -5$, the same slope.

### ST 2.1.17
Question: [[CAL1 HW 2.1 Questions#ST 2.1.17|ST 2.1.17]]

> [!solution] Solution
> $$
> g'(0) < 0 < g'(4) < g'(2) < g'(-2)
> $$
> $$
> \begin{aligned}
> &g'(a) = \text{the slope of the tangent line to } y = g(x) \text{ at } x = a. \\
> &\text{At } 0:\ g \text{ is decreasing} \implies g'(0) < 0. \\
> &\text{At } {-2},\ 2,\ 4:\ g \text{ is increasing} \implies g'(-2),\ g'(2),\ g'(4) > 0. \\
> &\text{The tangent line is steepest at } {-2}, \text{ less steep at } 2, \text{ and nearly flat at } 4 \\
> &\implies g'(4) < g'(2) < g'(-2).
> \end{aligned}
> $$
> ![[CAL1 HW 2.1 Solutions fig 17.png|480]]
>
> \# No formula is needed, only the signs and the steepness of the four tangent lines. $g'(0)$ is the only negative number, so it goes to the left of $0$.

### ST 2.1.21
Question: [[CAL1 HW 2.1 Questions#ST 2.1.21|ST 2.1.21]]

> [!solution] Solution
> $f(3) = \dfrac{9}{9} = 1$.
> $$
> \begin{aligned}
> f'(3) &= \lim_{x \to 3} \frac{f(x) - f(3)}{x - 3} \\
> &= \lim_{x \to 3} \frac{\dfrac{x^2}{x + 6} - 1}{x - 3} \\
> &= \lim_{x \to 3} \frac{x^2 - x - 6}{(x + 6)(x - 3)} \\
> &= \lim_{x \to 3} \frac{(x - 3)(x + 2)}{(x + 6)(x - 3)} \\
> &= \lim_{x \to 3} \frac{x + 2}{x + 6} && (x - 3 \ne 0) \\
> &= \frac{5}{9} && \text{(Direct Substitution Property)}
> \end{aligned}
> $$
>
> \# Equation 5 is the form with $x \to a$. The numerator $x^2 - x - 6$ must have the factor $x - 3$, because it is $0$ at $x = 3$; that is how to factor it.

### ST 2.1.23
Question: [[CAL1 HW 2.1 Questions#ST 2.1.23|ST 2.1.23]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(a) &= \lim_{h \to 0} \frac{f(a + h) - f(a)}{h} \\
> &= \lim_{h \to 0} \frac{\left[2(a + h)^2 - 5(a + h) + 3\right] - \left[2a^2 - 5a + 3\right]}{h} \\
> &= \lim_{h \to 0} \frac{2a^2 + 4ah + 2h^2 - 5a - 5h + 3 - 2a^2 + 5a - 3}{h} \\
> &= \lim_{h \to 0} \frac{4ah + 2h^2 - 5h}{h} \\
> &= \lim_{h \to 0} (4a + 2h - 5) && (h \ne 0) \\
> &= 4a - 5
> \end{aligned}
> $$
>
> \# $a$ is a fixed number and only $h$ moves. Every term without $h$ must cancel before the division by $h$.

### ST 2.1.25
Question: [[CAL1 HW 2.1 Questions#ST 2.1.25|ST 2.1.25]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(a) &= \lim_{h \to 0} \frac{f(a + h) - f(a)}{h} \\
> &= \lim_{h \to 0} \frac{1}{h}\left[\frac{1}{(a + h)^2 + 1} - \frac{1}{a^2 + 1}\right] \\
> &= \lim_{h \to 0} \frac{(a^2 + 1) - \left[(a + h)^2 + 1\right]}{h\left[(a + h)^2 + 1\right](a^2 + 1)} \\
> &= \lim_{h \to 0} \frac{-2ah - h^2}{h\left[(a + h)^2 + 1\right](a^2 + 1)} \\
> &= \lim_{h \to 0} \frac{-2a - h}{\left[(a + h)^2 + 1\right](a^2 + 1)} && (h \ne 0) \\
> &= -\frac{2a}{(a^2 + 1)^2}
> \end{aligned}
> $$
>
> \# A difference of two fractions: take the common denominator first and leave it factored; only the numerator is expanded. The last step is direct substitution of $h = 0$, and the denominator is never $0$ because $a^2 + 1 \ge 1$.

### ST 2.1.27
Question: [[CAL1 HW 2.1 Questions#ST 2.1.27|ST 2.1.27]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Point: } (6, B(6)) = (6, 0). \qquad \text{Slope: } B'(6) = -\tfrac{1}{2}. \\
> &\text{Hence } y - 0 = -\tfrac{1}{2}(x - 6), \text{ i.e. } y = -\tfrac{1}{2}x + 3.
> \end{aligned}
> $$
>
> \# The formula $y - f(a) = f'(a)(x - a)$ needs only two numbers: the value $B(6)$ gives the point and the derivative $B'(6)$ gives the slope. No limit is computed.

### ST 2.1.29
Question: [[CAL1 HW 2.1 Questions#ST 2.1.29|ST 2.1.29]]

> [!solution] Solution
> $f(1) = 3 - 1 = 2$.
> $$
> \begin{aligned}
> f'(1) &= \lim_{h \to 0} \frac{f(1 + h) - f(1)}{h} \\
> &= \lim_{h \to 0} \frac{3(1 + h)^2 - (1 + h)^3 - 2}{h} \\
> &= \lim_{h \to 0} \frac{(3 + 6h + 3h^2) - (1 + 3h + 3h^2 + h^3) - 2}{h} \\
> &= \lim_{h \to 0} \frac{3h - h^3}{h} \\
> &= \lim_{h \to 0} (3 - h^2) && (h \ne 0) \\
> &= 3
> \end{aligned}
> $$
> Hence the tangent line is $y - 2 = 3(x - 1)$, i.e. $y = 3x - 1$.
>
> \# $(1 + h)^3 = 1 + 3h + 3h^2 + h^3$. The slope of the tangent line at $(1, 2)$ is the derivative $f'(1)$.

### ST 2.1.33
Question: [[CAL1 HW 2.1 Questions#ST 2.1.33|ST 2.1.33]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\because \text{the tangent line passes through the point of tangency } (2, f(2)) \\
> &\therefore f(2) = 4(2) - 5 = 3. \\
> &\because f'(2) = \text{the slope of the tangent line at } x = 2 \\
> &\therefore f'(2) = 4.
> \end{aligned}
> $$
>
> \# Exercise 27 read backwards: there the point and the slope gave the line; here the line gives the point and the slope. The tangent line and the curve share the point $(2, f(2))$, so $f(2)$ is the $y$-value of the line at $x = 2$.

### ST 2.1.35
Question: [[CAL1 HW 2.1 Questions#ST 2.1.35|ST 2.1.35]]

> [!solution] Solution
> $f(4) = 320 - 96 = 224$.
> $$
> \begin{aligned}
> v(4) &= \lim_{h \to 0} \frac{f(4 + h) - f(4)}{h} \\
> &= \lim_{h \to 0} \frac{80(4 + h) - 6(4 + h)^2 - 224}{h} \\
> &= \lim_{h \to 0} \frac{320 + 80h - 96 - 48h - 6h^2 - 224}{h} \\
> &= \lim_{h \to 0} \frac{32h - 6h^2}{h} \\
> &= \lim_{h \to 0} (32 - 6h) && (h \ne 0) \\
> &= 32
> \end{aligned}
> $$
> Hence the velocity is $32$ m/s and the speed is $\lvert 32 \rvert = 32$ m/s.
>
> \# Velocity is the derivative of the position function, $v(4) = f'(4)$; speed is its absolute value. Here both are $32$ because $v(4) > 0$; in [[#ST 2.1.36]] they differ. Units: meters per second.

### ST 2.1.39
Question: [[CAL1 HW 2.1 Questions#ST 2.1.39|ST 2.1.39]]

> [!solution] Solution
> ![[CAL1 HW 2.1 Solutions fig 39.png|420]]
> $$
> \begin{aligned}
> &f(0) = 0: && \text{the graph passes through the origin.} \\
> &f'(0) = 3: && \text{the tangent line at } x = 0 \text{ has slope } 3 \text{ (steep, rising).} \\
> &f'(1) = 0: && \text{the tangent line at } x = 1 \text{ is horizontal.} \\
> &f'(2) = -1: && \text{the tangent line at } x = 2 \text{ has slope } {-1} \text{ (falling).}
> \end{aligned}
> $$
>
> \# Many graphs are correct. Draw the three short tangent segments first, then one smooth curve through them. The curve drawn is $f(x) = \tfrac{1}{3}x^3 - 2x^2 + 3x$, for which $f'(a) = a^2 - 4a + 3$. Only $f(0)$ is given, so the heights at $x = 1$ and $x = 2$ are free.

### ST 2.1.41
Question: [[CAL1 HW 2.1 Questions#ST 2.1.41|ST 2.1.41]]

> [!solution] Solution
> ![[CAL1 HW 2.1 Solutions fig 41.png|460]]
> $$
> \begin{aligned}
> &\text{continuous on } (-5, 5): && \text{one unbroken curve, drawn only for } {-5} < x < 5. \\
> &\lim_{x \to -5^{+}} g(x) = \infty: && \text{the curve rises along the vertical asymptote } x = -5. \\
> &g'(-2) = 0: && \text{the tangent line at } x = -2 \text{ is horizontal.} \\
> &g(0) = 1,\ g'(0) = 1: && \text{the curve passes through } (0, 1) \text{ with slope } 1. \\
> &\lim_{x \to 5^{-}} g(x) = 3: && \text{the curve approaches } (5, 3), \text{ an open dot.}
> \end{aligned}
> $$
>
> \# Many graphs are correct. $5$ is not in the domain, so the end at $(5, 3)$ is an open dot. Between $x = -2$ and $x = 0$ the slope has to grow from $0$ to $1$.

### ST 2.1.43
Question: [[CAL1 HW 2.1 Questions#ST 2.1.43|ST 2.1.43]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\lim_{h \to 0} \frac{\sqrt{9 + h} - 3}{h} = \lim_{h \to 0} \frac{\sqrt{9 + h} - \sqrt{9}}{h} = \lim_{h \to 0} \frac{f(9 + h) - f(9)}{h} = f'(9) \\
> &\text{Hence } f(x) = \sqrt{x},\ a = 9.
> \end{aligned}
> $$
>
> \# Match the limit with $\lim_{h \to 0} \dfrac{f(a + h) - f(a)}{h}$: the number next to $h$ is $a$, and the number subtracted is $f(a)$; check that it fits, $\sqrt{9} = 3$. Another correct answer: $f(x) = \sqrt{9 + x}$, $a = 0$.

### ST 2.1.45
Question: [[CAL1 HW 2.1 Questions#ST 2.1.45|ST 2.1.45]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\lim_{x \to 2} \frac{x^6 - 64}{x - 2} = \lim_{x \to 2} \frac{x^6 - 2^6}{x - 2} = \lim_{x \to 2} \frac{f(x) - f(2)}{x - 2} = f'(2) \\
> &\text{Hence } f(x) = x^6,\ a = 2.
> \end{aligned}
> $$
>
> \# This one has the form with $x \to a$: $a$ is the number that $x$ approaches, and $64 = 2^6 = f(2)$.

### ST 2.1.47
Question: [[CAL1 HW 2.1 Questions#ST 2.1.47|ST 2.1.47]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\lim_{h \to 0} \frac{\tan\left(\frac{\pi}{4} + h\right) - 1}{h} = \lim_{h \to 0} \frac{\tan\left(\frac{\pi}{4} + h\right) - \tan\frac{\pi}{4}}{h} = \lim_{h \to 0} \frac{f\left(\frac{\pi}{4} + h\right) - f\left(\frac{\pi}{4}\right)}{h} = f'\left(\tfrac{\pi}{4}\right) \\
> &\text{Hence } f(x) = \tan x,\ a = \tfrac{\pi}{4}.
> \end{aligned}
> $$
>
> \# The check is $\tan\tfrac{\pi}{4} = 1$. The question asks only for $f$ and $a$; the value of the limit is not needed.

### ST 2.1.49
Question: [[CAL1 HW 2.1 Questions#ST 2.1.49|ST 2.1.49]]

> [!solution] Solution
> **(a)** $C(100) = 5000 + 1000 + 500 = 6500$.
> $$
> \begin{aligned}
> \text{(i)}\ \ &C(105) = 5000 + 1050 + 551.25 = 6601.25 \\
> &\frac{\Delta C}{\Delta x} = \frac{C(105) - C(100)}{105 - 100} = \frac{101.25}{5} = 20.25 \text{ dollars/unit} \\[4pt]
> \text{(ii)}\ \ &C(101) = 5000 + 1010 + 510.05 = 6520.05 \\
> &\frac{\Delta C}{\Delta x} = \frac{C(101) - C(100)}{101 - 100} = \frac{20.05}{1} = 20.05 \text{ dollars/unit}
> \end{aligned}
> $$
> **(b)**
> $$
> \begin{aligned}
> C'(100) &= \lim_{h \to 0} \frac{C(100 + h) - C(100)}{h} \\
> &= \lim_{h \to 0} \frac{5000 + 10(100 + h) + 0.05(100 + h)^2 - 6500}{h} \\
> &= \lim_{h \to 0} \frac{20h + 0.05h^2}{h} \\
> &= \lim_{h \to 0} (20 + 0.05h) && (h \ne 0) \\
> &= 20 \text{ dollars/unit}
> \end{aligned}
> $$
>
> \# Average rate of change $=$ slope of a secant line; instantaneous rate of change $=$ derivative. The average rates $20.25$, $20.05$ approach $C'(100) = 20$ as the interval shrinks: on $[100, 100 + h]$ the average rate is $20 + 0.05h$. Units: dollars per unit.

### ST 2.1.53
Question: [[CAL1 HW 2.1 Questions#ST 2.1.53|ST 2.1.53]]

> [!solution] Solution
> **(a)** $S'(T)$ is the rate at which the oxygen solubility changes with respect to the water temperature. Its units are (mg/L)/°C.
>
> **(b)** The tangent line at $T = 16$ passes through about $(8, 12.2)$ and $(24, 8.2)$:
> $$
> S'(16) \approx \frac{8.2 - 12.2}{24 - 8} = \frac{-4}{16} = -0.25 \text{ (mg/L)/°C}
> $$
> When the water temperature is $16$ °C, the oxygen solubility is decreasing at a rate of about $0.25$ (mg/L)/°C as the temperature rises.
>
> ![[CAL1 HW 2.1 Solutions fig 53.png|420]]
>
> \# An estimate from a graph: draw the tangent line at $T = 16$, read two points on that line, and compute its slope. Any value near $-0.25$ is fine. A second way: the average of the two secant slopes next to $16$, about $\tfrac{1}{2}(-0.26 - 0.21) \approx -0.23$, with $S(8) \approx 12.3$, $S(16) \approx 10.2$, $S(24) \approx 8.6$ read from the graph. The sign is negative because $S$ decreases.

### ST 2.1.57
Question: [[CAL1 HW 2.1 Questions#ST 2.1.57|ST 2.1.57]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(0) &= \lim_{h \to 0} \frac{f(0 + h) - f(0)}{h} \\
> &= \lim_{h \to 0} \frac{h \sin\frac{1}{h} - 0}{h} \\
> &= \lim_{h \to 0} \sin\frac{1}{h} && (h \ne 0)
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &h = \tfrac{1}{n\pi} \implies \sin\tfrac{1}{h} = \sin n\pi = 0 && (n = 1, 2, 3, \dots) \\
> &h = \tfrac{1}{2n\pi + \pi/2} \implies \sin\tfrac{1}{h} = \sin\left(2n\pi + \tfrac{\pi}{2}\right) = 1 && (n = 1, 2, 3, \dots) \\
> &\because \text{both kinds of } h \text{ are as close to } 0 \text{ as we like, while } \sin\tfrac{1}{h} = 0 \text{ and } 1 \\
> &\therefore \lim_{h \to 0} \sin\tfrac{1}{h} \text{ does not exist.} \\
> &\text{Hence } f'(0) \text{ does not exist.}
> \end{aligned}
> $$
>
> \# $f(0) = 0$ comes from the second line of the definition of $f$, and $f(h) = h \sin\tfrac{1}{h}$ from the first, because $h \ne 0$. $\sin\tfrac{1}{h}$ oscillates between $-1$ and $1$ infinitely often as $h \to 0$, so it approaches no single number. $f$ is continuous at $0$ (Squeeze Theorem, $-\lvert x \rvert \le x \sin\tfrac{1}{x} \le \lvert x \rvert$), so this $f$ is continuous at $0$ and still has no derivative there.

### ST 2.1.58
Question: [[CAL1 HW 2.1 Questions#ST 2.1.58|ST 2.1.58]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(0) &= \lim_{h \to 0} \frac{f(0 + h) - f(0)}{h} \\
> &= \lim_{h \to 0} \frac{h^2 \sin\frac{1}{h} - 0}{h} \\
> &= \lim_{h \to 0} h \sin\frac{1}{h} && (h \ne 0)
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\because {-1} \le \sin\tfrac{1}{h} \le 1 \implies {-\lvert h \rvert} \le h \sin\tfrac{1}{h} \le \lvert h \rvert \quad (h \ne 0) \\
> &\phantom{\because}\ \lim_{h \to 0} \left(-\lvert h \rvert\right) = 0 = \lim_{h \to 0} \lvert h \rvert \\
> &\therefore \lim_{h \to 0} h \sin\tfrac{1}{h} = 0 \quad \text{(Squeeze Theorem)} \\
> &\text{Hence } f'(0) \text{ exists and } f'(0) = 0.
> \end{aligned}
> $$
>
> \# The same first three lines as Exercise 57, with one more factor $h$ left over, and that factor squeezes the oscillation to $0$. The bounds are $\pm\lvert h \rvert$, not $\pm h$, because $h$ can be negative. Exercises 57 and 58 are a pair: $x \sin\tfrac{1}{x}$ has no derivative at $0$, $x^2 \sin\tfrac{1}{x}$ has.

## ST §2.1 Additional Exercises

> [!note] Note
> These exercises are not assigned. Each one adds a type of problem that the assigned exercises do not cover.
> - 8: a tangent line to a square root; the limit needs the conjugate.
> - 12: velocity at a general time $a$, then the time and the velocity of impact (the type of Example 3 in ST §2.1).
> - 22: the form with $x \to a$ for $1/\sqrt{\ \cdot\ }$: a common denominator, then the conjugate (the type of Example 5).
> - 34: $f(a)$ and $f'(a)$ from two points on the tangent line.
> - 36: a negative velocity, so that velocity and speed differ.
> - 55: rates of change from a table of values (the type of Example 8).

### ST 2.1.8
Question: [[CAL1 HW 2.1 Questions#ST 2.1.8|ST 2.1.8]]

> [!solution] Solution
> Let $f(x) = \sqrt{1 - 3x}$, $a = -1$, $f(-1) = \sqrt{4} = 2$.
> $$
> \begin{aligned}
> m &= \lim_{h \to 0} \frac{f(-1 + h) - f(-1)}{h} \\
> &= \lim_{h \to 0} \frac{\sqrt{4 - 3h} - 2}{h} \\
> &= \lim_{h \to 0} \frac{\sqrt{4 - 3h} - 2}{h} \cdot \frac{\sqrt{4 - 3h} + 2}{\sqrt{4 - 3h} + 2} \\
> &= \lim_{h \to 0} \frac{(4 - 3h) - 4}{h\left(\sqrt{4 - 3h} + 2\right)} \\
> &= \lim_{h \to 0} \frac{-3}{\sqrt{4 - 3h} + 2} && (h \ne 0) \\
> &= -\frac{3}{4}
> \end{aligned}
> $$
> Hence the tangent line is $y - 2 = -\tfrac{3}{4}(x + 1)$, i.e. $y = -\tfrac{3}{4}x + \tfrac{5}{4}$.
>
> \# $1 - 3(-1 + h) = 4 - 3h$. A root minus a number: multiply by the conjugate, so that the numerator becomes a difference of squares and $h$ cancels.

### ST 2.1.12
Question: [[CAL1 HW 2.1 Questions#ST 2.1.12|ST 2.1.12]]

> [!solution] Solution
> $$
> \begin{aligned}
> v(a) &= \lim_{h \to 0} \frac{H(a + h) - H(a)}{h} \\
> &= \lim_{h \to 0} \frac{\left[10(a + h) - 1.86(a + h)^2\right] - \left[10a - 1.86a^2\right]}{h} \\
> &= \lim_{h \to 0} \frac{10h - 3.72ah - 1.86h^2}{h} \\
> &= \lim_{h \to 0} (10 - 3.72a - 1.86h) && (h \ne 0) \\
> &= 10 - 3.72a
> \end{aligned}
> $$
> $$
> \begin{aligned}
> \text{(a)}\ \ &v(1) = 10 - 3.72 = 6.28 \text{ m/s} \\
> \text{(b)}\ \ &v(a) = 10 - 3.72a \text{ m/s} \\
> \text{(c)}\ \ &H = 0 \iff t(10 - 1.86t) = 0 \iff t = 0 \text{ or } t = \tfrac{10}{1.86} \approx 5.4 \\
> &\text{Hence the rock hits the surface after about } 5.4 \text{ s.} \\
> \text{(d)}\ \ &v\left(\tfrac{10}{1.86}\right) = 10 - 3.72 \cdot \tfrac{10}{1.86} = 10 - 20 = -10 \text{ m/s}
> \end{aligned}
> $$
>
> \# Several velocities are asked, so compute $v(a)$ once for a general $a$ and substitute. $t = 0$ is the moment of the throw, so the impact is the other solution. The velocity of impact is negative because the rock moves downward; its speed, $10$ m/s, equals the initial speed.

### ST 2.1.22
Question: [[CAL1 HW 2.1 Questions#ST 2.1.22|ST 2.1.22]]

> [!solution] Solution
> $f(1) = \dfrac{1}{\sqrt{4}} = \dfrac{1}{2}$.
> $$
> \begin{aligned}
> f'(1) &= \lim_{x \to 1} \frac{f(x) - f(1)}{x - 1} \\
> &= \lim_{x \to 1} \frac{\dfrac{1}{\sqrt{2x + 2}} - \dfrac{1}{2}}{x - 1} \\
> &= \lim_{x \to 1} \frac{2 - \sqrt{2x + 2}}{2\sqrt{2x + 2}\,(x - 1)} \\
> &= \lim_{x \to 1} \frac{2 - \sqrt{2x + 2}}{2\sqrt{2x + 2}\,(x - 1)} \cdot \frac{2 + \sqrt{2x + 2}}{2 + \sqrt{2x + 2}} \\
> &= \lim_{x \to 1} \frac{4 - (2x + 2)}{2\sqrt{2x + 2}\,(x - 1)\left(2 + \sqrt{2x + 2}\right)} \\
> &= \lim_{x \to 1} \frac{-2(x - 1)}{2\sqrt{2x + 2}\,(x - 1)\left(2 + \sqrt{2x + 2}\right)} \\
> &= \lim_{x \to 1} \frac{-1}{\sqrt{2x + 2}\left(2 + \sqrt{2x + 2}\right)} && (x - 1 \ne 0) \\
> &= \frac{-1}{2 \cdot 4} = -\frac{1}{8}
> \end{aligned}
> $$
>
> \# Two tools in a fixed order: the common denominator first, then the conjugate of the numerator $2 - \sqrt{2x + 2}$. $4 - (2x + 2) = -2(x - 1)$ gives the factor that cancels.

### ST 2.1.34
Question: [[CAL1 HW 2.1 Questions#ST 2.1.34|ST 2.1.34]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\because (4, 3) \text{ is the point of tangency, it is on the curve } y = f(x) \\
> &\therefore f(4) = 3. \\
> &\because \text{the tangent line passes through } (4, 3) \text{ and } (0, 2) \\
> &\therefore f'(4) = \text{the slope of the tangent line} = \frac{3 - 2}{4 - 0} = \frac{1}{4}.
> \end{aligned}
> $$
>
> \# $(0, 2)$ is a point of the tangent line, not of the curve: it says nothing about $f(0)$.

### ST 2.1.36
Question: [[CAL1 HW 2.1 Questions#ST 2.1.36|ST 2.1.36]]

> [!solution] Solution
> $f(4) = 10 + \dfrac{45}{5} = 19$.
> $$
> \begin{aligned}
> v(4) &= \lim_{h \to 0} \frac{f(4 + h) - f(4)}{h} \\
> &= \lim_{h \to 0} \frac{1}{h}\left[10 + \frac{45}{5 + h} - 19\right] \\
> &= \lim_{h \to 0} \frac{1}{h} \cdot \frac{45 - 9(5 + h)}{5 + h} \\
> &= \lim_{h \to 0} \frac{-9h}{h(5 + h)} \\
> &= \lim_{h \to 0} \frac{-9}{5 + h} && (h \ne 0) \\
> &= -\frac{9}{5}
> \end{aligned}
> $$
> Hence the velocity is $-\tfrac{9}{5}$ m/s and the speed is $\left\lvert -\tfrac{9}{5} \right\rvert = \tfrac{9}{5}$ m/s.
>
> \# The velocity is negative: the particle moves in the negative direction at $t = 4$. Speed has no sign.

### ST 2.1.55
Question: [[CAL1 HW 2.1 Questions#ST 2.1.55|ST 2.1.55]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> \text{(i)}\ \ &[1.0, 2.0]: && \frac{C(2.0) - C(1.0)}{2.0 - 1.0} = \frac{0.018 - 0.033}{1} = -0.015 \text{ (g/dL)/h} \\[4pt]
> \text{(ii)}\ \ &[1.5, 2.0]: && \frac{C(2.0) - C(1.5)}{2.0 - 1.5} = \frac{0.018 - 0.024}{0.5} = -0.012 \text{ (g/dL)/h} \\[4pt]
> \text{(iii)}\ \ &[2.0, 2.5]: && \frac{C(2.5) - C(2.0)}{2.5 - 2.0} = \frac{0.012 - 0.018}{0.5} = -0.012 \text{ (g/dL)/h} \\[4pt]
> \text{(iv)}\ \ &[2.0, 3.0]: && \frac{C(3.0) - C(2.0)}{3.0 - 2.0} = \frac{0.007 - 0.018}{1} = -0.011 \text{ (g/dL)/h}
> \end{aligned}
> $$
> **(b)**
> $$
> C'(2) \approx \frac{(-0.012) + (-0.012)}{2} = -0.012 \text{ (g/dL)/h}
> $$
> After $2$ hours, the blood alcohol concentration is decreasing at a rate of about $0.012$ (g/dL)/h.
>
> \# The estimate is the average of the two average rates over the shortest intervals on each side of $t = 2$, (ii) and (iii). Units: units of $C$ per unit of $t$.
