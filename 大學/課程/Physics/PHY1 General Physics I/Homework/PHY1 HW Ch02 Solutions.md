---
course: [PHY1]
chapter: ["2.1", "2.2", "2.3", "2.4", "2.5", "2.6"]
tags: [physics, homework, solutions, kinematics]
source:
  - "Own solutions; every number recomputed with Python, symbolic results with sympy"
  - "EUP Ch. 2 (pp. 32-49), scanned PDF: worked examples and answers to GOT IT? questions"
  - "[[PHY1 Ch02 Fig 2.16.png]]"
created: 2026-10-05
questions: "[[PHY1 HW Ch02 Questions]]"
---
> [!note] Notation
> - Equation numbers are the book's, for constant acceleration only: $v = v_{0} + at$ (2.7), $x = x_{0} + \tfrac{1}{2}(v_{0} + v)t$ (2.9), $x = x_{0} + v_{0}t + \tfrac{1}{2}at^{2}$ (2.10), $v^{2} = v_{0}^{2} + 2a(x - x_{0})$ (2.11).
> - In free fall $y$ points upward unless the solution says otherwise, so $a = -g$ with $g = 9.8\ \mathrm{m/s^2}$.
> - Intermediate values keep one extra figure.

## Answer Key

| Problem | Answer |
| --- | --- |
| [[PHY1 HW Ch02 Questions#EUP Example 2.1\|EUP Example 2.1]] | $\bar{v} = 250\ \mathrm{km/h}$ north; average speed $600\ \mathrm{km/h}$ |
| [[PHY1 HW Ch02 Questions#EUP Example 2.2\|EUP Example 2.2]] | $v = 2bt = 116\ \mathrm{m/s}$; $\bar{v} = bt = \tfrac{1}{2}v$ |
| [[PHY1 HW Ch02 Questions#EUP Conceptual Example 2.1\|EUP Conceptual Example 2.1]] | Yes; $\bar{a} = -9.8\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch02 Questions#EUP Example 2.3\|EUP Example 2.3]] | $625\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#EUP Example 2.4\|EUP Example 2.4]] | $350\ \mathrm{m}$; $150\ \mathrm{km/h}$ |
| [[PHY1 HW Ch02 Questions#EUP Example 2.5\|EUP Example 2.5]] | $14\ \mathrm{m/s}$; $1.4\ \mathrm{s}$ |
| [[PHY1 HW Ch02 Questions#EUP Example 2.6\|EUP Example 2.6]] | $1.7\ \mathrm{s}$; $4.2\ \mathrm{m}$; $7.3\ \mathrm{m/s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.13\|EUP 2.13]] | (a) $24\ \mathrm{km}$ north; (b) $9.6\ \mathrm{km/h}$ north; (c) $16\ \mathrm{km/h}$ south; (d) $0$; (e) $0$ |
| [[PHY1 HW Ch02 Questions#EUP 2.52\|EUP 2.52]] | after $6.03\ \mathrm{h}$, $6.27 \times 10^{3}\ \mathrm{km}$ from London |
| [[PHY1 HW Ch02 Questions#EUP 2.83\|EUP 2.83]] | (a) $\tfrac{1}{2}(v_{1} + v_{2})$; (b) $\dfrac{2v_{1}v_{2}}{v_{1} + v_{2}}$; (c) case (a) |
| [[PHY1 HW Ch02 Questions#EUP 2.53\|EUP 2.53]] | (a) $9.82\ \mathrm{m/s}$; (b) $9.34\ \mathrm{m/s}$; (c) $9.18\ \mathrm{m/s}$; (d) $v = b + 3ct^{2}$, $9.18\ \mathrm{m/s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.84\|EUP 2.84]] | (a) $0.282\ \mathrm{m/s^4}$; (b) $9.25\ \mathrm{m/s}$; (c) $-18.2\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.21\|EUP 2.21]] | $0.38\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.29\|EUP 2.29]] | (a) $\dfrac{v^{2}}{2h}$; (b) $\dfrac{2h}{v}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.62\|EUP 2.62]] | (a) $\dfrac{2v_{0}}{a}$; (b) $v_{0}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.66\|EUP 2.66]] | (a) $21\ \mathrm{m/s}$ ($77\ \mathrm{km/h}$); (b) $2.6\ \mathrm{s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.67\|EUP 2.67]] | (a) $25\ \mathrm{m/s}$; (b) $1.8 \times 10^{2}\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.55\|EUP 2.55]] | $14.1\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.68\|EUP 2.68]] | No collision; about $10\ \mathrm{m}$ apart |
| [[PHY1 HW Ch02 Questions#EUP 2.70\|EUP 2.70]] | No collision; closest approach $4.3\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.37\|EUP 2.37]] | (a) $\dfrac{v^{2}}{2g}$; (b) $\dfrac{v}{\sqrt{2}}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.59\|EUP 2.59]] | from $3.38\ \mathrm{s}$ to $6.14\ \mathrm{s}$ after the explosion |
| [[PHY1 HW Ch02 Questions#EUP 2.73\|EUP 2.73]] | $2.7 \times 10^{2}\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.85\|EUP 2.85]] | $\dfrac{1}{\sqrt{2}} \approx 71\%$ |
| [[PHY1 HW Ch02 Questions#EUP 2.86\|EUP 2.86]] | $1.2\ \mathrm{m}$ above the top of the window |
| [[PHY1 HW Ch02 Questions#EUP 2.90\|EUP 2.90]] | (a) $-9.1\ \mathrm{m/s}$; (b) $-9.1\ \mathrm{m/s}$; (c) $0.18\ \mathrm{s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.91\|EUP 2.91]] | $15$ drops per second |
| [[PHY1 HW Ch02 Questions#EUP 2.77\|EUP 2.77]] | (a) $7.88\ \mathrm{m/s}$ and $7.67\ \mathrm{m/s}$; (b) the first diver, by $0.16\ \mathrm{s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.78\|EUP 2.78]] | $2.4\ \mathrm{s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.97\|EUP 2.97]] | (a) $v_{0} > \sqrt{\dfrac{gh_{0}}{2}}$; (b) $h_{0} - \dfrac{gh_{0}^{2}}{2v_{0}^{2}}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.88\|EUP 2.88]] | (a) $v_{0} + a_{0}t + \tfrac{1}{2}bt^{2}$; (b) $x_{0} + v_{0}t + \tfrac{1}{2}a_{0}t^{2} + \tfrac{1}{6}bt^{3}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.94\|EUP 2.94]] | $5.4\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.95\|EUP 2.95]] | (a) $\sqrt{\dfrac{2b}{c}}$; (b) $-5b$ |
| [[PHY1 HW Ch02 Questions#EUP 2.96\|EUP 2.96]] | (a) $\dfrac{a_{0}}{b}\left(1 - e^{-bt}\right)$; (b) no; (c) yes |
| [[PHY1 HW Ch02 Questions#EUP 2.98 to 2.102\|EUP 2.98 to 2.102]] | b, c, b, c, b |
| [[PHY1 HW Ch02 Questions#EUP 2.58\|EUP 2.58]] | $x$ versus $t^{2}$; slope $\approx 1.6\ \mathrm{m/s^2}$; $a \approx 3.2\ \mathrm{m/s^2}$ |

## Textbook Examples

### EUP Example 2.1
Question: [[PHY1 HW Ch02 Questions#EUP Example 2.1|EUP Example 2.1]]

> [!solution] Solution
> Take north as positive. $\Delta x = 1000\ \mathrm{km}$ and $\Delta t = 2.2\ \mathrm{h} + 0.50\ \mathrm{h} + 1.3\ \mathrm{h} = 4.0\ \mathrm{h}$:
> $$
> \bar{v} = \frac{\Delta x}{\Delta t} = \frac{1000\ \mathrm{km}}{4.0\ \mathrm{h}} = 250\ \mathrm{km/h}.
> $$
> Distance traveled: $1000\ \mathrm{km} + 2(700\ \mathrm{km}) = 2400\ \mathrm{km}$:
> $$
> \text{average speed} = \frac{2400\ \mathrm{km}}{4.0\ \mathrm{h}} = 600\ \mathrm{km/h}.
> $$

### EUP Example 2.2
Question: [[PHY1 HW Ch02 Questions#EUP Example 2.2|EUP Example 2.2]]

> [!solution] Solution
> $$
> v = \frac{dx}{dt} = \frac{d(bt^{2})}{dt} = 2bt, \qquad v(20\ \mathrm{s}) = 2(2.90\ \mathrm{m/s^2})(20\ \mathrm{s}) = 116\ \mathrm{m/s}.
> $$
> From liftoff ($x = 0$ at $t = 0$) to time $t$:
> $$
> \bar{v} = \frac{\Delta x}{\Delta t} = \frac{bt^{2}}{t} = bt = \tfrac{1}{2}v.
> $$

### EUP Conceptual Example 2.1
Question: [[PHY1 HW Ch02 Questions#EUP Conceptual Example 2.1|EUP Conceptual Example 2.1]]

> [!solution] Solution
> Yes. Acceleration is the rate of change of velocity and does not depend on the value of the velocity. At the peak of its flight a ball has $v = 0$, but $v$ is changing from positive to negative, so $a \ne 0$.
>
> Making the connection, with upward positive:
> $$
> \bar{a} = \frac{\Delta v}{\Delta t} = \frac{-0.098\ \mathrm{m/s} - 0.098\ \mathrm{m/s}}{0.020\ \mathrm{s}} = -9.8\ \mathrm{m/s^2}.
> $$

### EUP Example 2.3
Question: [[PHY1 HW Ch02 Questions#EUP Example 2.3|EUP Example 2.3]]

> [!solution] Solution
> Take $+x$ in the direction of motion: $v_{0} = 270\ \mathrm{km/h} = 75\ \mathrm{m/s}$, $v = 0$, $a = -4.5\ \mathrm{m/s^2}$. By (2.11) with $v = 0$,
> $$
> \Delta x = \frac{-v_{0}^{2}}{2a} = \frac{-(75\ \mathrm{m/s})^{2}}{2(-4.5\ \mathrm{m/s^2})} = 625\ \mathrm{m}.
> $$

### EUP Example 2.4
Question: [[PHY1 HW Ch02 Questions#EUP Example 2.4|EUP Example 2.4]]

> [!solution] Solution
> Take $x = 0$ and $t = 0$ where the speeder passes the police car. By (2.10),
> $$
> x_{\mathrm{s}} = v_{\mathrm{s0}}t, \qquad x_{\mathrm{p}} = \tfrac{1}{2}a_{\mathrm{p}}t^{2}.
> $$
> $x_{\mathrm{s}} = x_{\mathrm{p}}$ gives $t = 0$ (the start) or $t = \dfrac{2v_{\mathrm{s0}}}{a_{\mathrm{p}}}$. With $v_{\mathrm{s0}} = 21\ \mathrm{m/s}$,
> $$
> x_{\mathrm{s}} = v_{\mathrm{s0}}t = \frac{2v_{\mathrm{s0}}^{2}}{a_{\mathrm{p}}} = \frac{2(21\ \mathrm{m/s})^{2}}{2.5\ \mathrm{m/s^2}} = 350\ \mathrm{m}, \qquad v_{\mathrm{p}} = a_{\mathrm{p}}t = 2v_{\mathrm{s0}} = 150\ \mathrm{km/h}.
> $$

### EUP Example 2.5
Question: [[PHY1 HW Ch02 Questions#EUP Example 2.5|EUP Example 2.5]]

> [!solution] Solution
> $y = 0$ at the water: $y_{0} = 10\ \mathrm{m}$, $v_{0} = 0$. By (2.11),
> $$
> \lvert v \rvert = \sqrt{-2g(y - y_{0})} = \sqrt{(-2)(9.8\ \mathrm{m/s^2})(0\ \mathrm{m} - 10\ \mathrm{m})} = 14\ \mathrm{m/s},
> $$
> and $v = -14\ \mathrm{m/s}$ (downward). By (2.7),
> $$
> t = \frac{v_{0} - v}{g} = \frac{0 - (-14\ \mathrm{m/s})}{9.8\ \mathrm{m/s^2}} = 1.4\ \mathrm{s}.
> $$

### EUP Example 2.6
Question: [[PHY1 HW Ch02 Questions#EUP Example 2.6|EUP Example 2.6]]

> [!solution] Solution
> $y = 0$ at the floor: $y_{0} = 1.5\ \mathrm{m}$, $v_{0} = +7.3\ \mathrm{m/s}$. At the floor, (2.10) gives $0 = y_{0} + v_{0}t - \tfrac{1}{2}gt^{2}$:
> $$
> t = \frac{v_{0} \pm \sqrt{v_{0}^{2} + 2y_{0}g}}{g} = 1.7\ \mathrm{s} \ \text{ or } \ -0.18\ \mathrm{s}.
> $$
> The ball hits the floor at $1.7\ \mathrm{s}$ (the negative root is before the toss). At the peak $v = 0$, so by (2.11)
> $$
> y = y_{0} + \frac{v_{0}^{2}}{2g} = 1.5\ \mathrm{m} + \frac{(7.3\ \mathrm{m/s})^{2}}{2(9.8\ \mathrm{m/s^2})} = 4.2\ \mathrm{m}.
> $$
> At $y = y_{0}$, (2.11) gives $v^{2} = v_{0}^{2}$: the speed on the way down is $7.3\ \mathrm{m/s}$.

## Average Velocity and Average Speed

### EUP 2.13
Question: [[PHY1 HW Ch02 Questions#EUP 2.13|EUP 2.13]]

> [!solution] Solution
> Take north as positive, origin at home.
> - (a) $\Delta x = +24\ \mathrm{km}$ ($24\ \mathrm{km}$ north)
> - (b) $\bar{v} = \dfrac{+24\ \mathrm{km}}{2.5\ \mathrm{h}} = +9.6\ \mathrm{km/h}$ (north)
> - (c) $\bar{v} = \dfrac{-24\ \mathrm{km}}{1.5\ \mathrm{h}} = -16\ \mathrm{km/h}$ (south)
> - (d) $\Delta x = 0$
> - (e) $\bar{v} = \dfrac{0}{4.0\ \mathrm{h}} = 0$

### EUP 2.52
Question: [[PHY1 HW Ch02 Questions#EUP 2.52|EUP 2.52]]

> [!solution] Solution
> Origin at London, $+x$ toward Singapore, $L = 10{,}886\ \mathrm{km}$: $x_{1} = v_{1}t$ and $x_{2} = L - v_{2}t$. Setting $x_{1} = x_{2}$,
> $$
> \begin{aligned}
> t &= \frac{L}{v_{1} + v_{2}} = \frac{10{,}886\ \mathrm{km}}{1040\ \mathrm{km/h} + 765\ \mathrm{km/h}} = 6.03\ \mathrm{h}, \\
> x_{1} &= v_{1}t = (1040\ \mathrm{km/h})(6.031\ \mathrm{h}) = 6.27 \times 10^{3}\ \mathrm{km}.
> \end{aligned}
> $$
> They pass $6.03\ \mathrm{h}$ after departure, $6.27 \times 10^{3}\ \mathrm{km}$ from London.

### EUP 2.83
Question: [[PHY1 HW Ch02 Questions#EUP 2.83|EUP 2.83]]

> [!solution] Solution
> Let $T$ be the total time; the average speed is $L/T$.
>
> **(a)** $L = v_{1}\dfrac{T}{2} + v_{2}\dfrac{T}{2}$, so $\dfrac{L}{T} = \tfrac{1}{2}(v_{1} + v_{2})$.
>
> **(b)** $T = \dfrac{L/2}{v_{1}} + \dfrac{L/2}{v_{2}} = \dfrac{L(v_{1} + v_{2})}{2v_{1}v_{2}}$, so $\dfrac{L}{T} = \dfrac{2v_{1}v_{2}}{v_{1} + v_{2}}$.
>
> **(c)** Case (a), since
> $$
> \tfrac{1}{2}(v_{1} + v_{2}) - \frac{2v_{1}v_{2}}{v_{1} + v_{2}} = \frac{(v_{1} - v_{2})^{2}}{2(v_{1} + v_{2})} \ge 0.
> $$

## Velocity from Position

### EUP 2.53
Question: [[PHY1 HW Ch02 Questions#EUP 2.53|EUP 2.53]]

> [!solution] Solution
> | $t$ ($\mathrm{s}$) | 1.00 | 1.50 | 1.95 | 2.05 | 2.50 | 3.00 |
> | --- | --- | --- | --- | --- | --- | --- |
> | $x = bt + ct^{3}$ ($\mathrm{m}$) | 2.140 | 4.410 | 7.6705 | 8.5887 | 13.750 | 21.780 |
>
> - (a) $\bar{v} = \dfrac{21.780\ \mathrm{m} - 2.140\ \mathrm{m}}{2.00\ \mathrm{s}} = 9.82\ \mathrm{m/s}$
> - (b) $\bar{v} = \dfrac{13.750\ \mathrm{m} - 4.410\ \mathrm{m}}{1.00\ \mathrm{s}} = 9.34\ \mathrm{m/s}$
> - (c) $\bar{v} = \dfrac{8.5887\ \mathrm{m} - 7.6705\ \mathrm{m}}{0.10\ \mathrm{s}} = 9.18\ \mathrm{m/s}$
> - (d) $v = \dfrac{dx}{dt} = b + 3ct^{2}$; $v(2\ \mathrm{s}) = 1.50\ \mathrm{m/s} + 3(0.640\ \mathrm{m/s^3})(2\ \mathrm{s})^{2} = 9.18\ \mathrm{m/s}$. The average velocities approach this value as the interval shrinks.

### EUP 2.84
Question: [[PHY1 HW Ch02 Questions#EUP 2.84|EUP 2.84]]

> [!solution] Solution
> Let $t_{1} = 2.54\ \mathrm{s}$.
>
> **(a)** $x = t^{2}(b - ct^{2}) = 0$ at $t_{1}$ requires $ct_{1}^{2} = b$:
> $$
> c = \frac{b}{t_{1}^{2}} = \frac{1.82\ \mathrm{m/s^2}}{(2.54\ \mathrm{s})^{2}} = 0.282\ \mathrm{m/s^4}.
> $$
>
> **(b)** $v = \dfrac{dx}{dt} = 2bt - 4ct^{3}$; at $t_{1}$, $v = 2bt_{1} - 4bt_{1} = -2bt_{1} = -9.25\ \mathrm{m/s}$. The speed is $9.25\ \mathrm{m/s}$.
>
> **(c)** $a = \dfrac{dv}{dt} = 2b - 12ct^{2}$; at $t_{1}$, $a = 2b - 12b = -10b = -18.2\ \mathrm{m/s^2}$.

## Average Acceleration

### EUP 2.21
Question: [[PHY1 HW Ch02 Questions#EUP 2.21|EUP 2.21]]

> [!solution] Solution
> Only the initial and final velocities matter:
> $$
> \bar{a} = \frac{\Delta v}{\Delta t} = \frac{18\ \mathrm{m/s} - 0}{48\ \mathrm{s}} = 0.38\ \mathrm{m/s^2}.
> $$

## Constant Acceleration with One Object

### EUP 2.29
Question: [[PHY1 HW Ch02 Questions#EUP 2.29|EUP 2.29]]

> [!solution] Solution
> $v_{0} = 0$ and $x - x_{0} = h$.
>
> **(a)** By (2.11), $v^{2} = 2ah$, so $a = \dfrac{v^{2}}{2h}$.
>
> **(b)** By (2.9), $h = \tfrac{1}{2}(0 + v)t$, so $t = \dfrac{2h}{v}$.

### EUP 2.62
Question: [[PHY1 HW Ch02 Questions#EUP 2.62|EUP 2.62]]

> [!solution] Solution
> The acceleration is $-a$.
>
> **(a)** By (2.10), $x = x_{0} + v_{0}t - \tfrac{1}{2}at^{2}$. Setting $x = x_{0}$: $t = 0$ (the start) or $t = \dfrac{2v_{0}}{a}$.
>
> **(b)** By (2.7), $v = v_{0} - a\dfrac{2v_{0}}{a} = -v_{0}$: the speed is $v_{0}$.

### EUP 2.66
Question: [[PHY1 HW Ch02 Questions#EUP 2.66|EUP 2.66]]

> [!solution] Solution
> Take $+x$ in the direction of motion: $a = -6.3\ \mathrm{m/s^2}$, $\Delta x = 34\ \mathrm{m}$, $v = 18\ \mathrm{km/h} = 5.0\ \mathrm{m/s}$.
>
> **(a)** By (2.11),
> $$
> \begin{aligned}
> v_{0} = \sqrt{v^{2} - 2a\,\Delta x} &= \sqrt{(5.0\ \mathrm{m/s})^{2} - 2(-6.3\ \mathrm{m/s^2})(34\ \mathrm{m})} \\
> &= 21.3\ \mathrm{m/s} \approx 21\ \mathrm{m/s} \quad (77\ \mathrm{km/h}).
> \end{aligned}
> $$
>
> **(b)** By (2.7),
> $$
> t = \frac{v - v_{0}}{a} = \frac{5.0\ \mathrm{m/s} - 21.3\ \mathrm{m/s}}{-6.3\ \mathrm{m/s^2}} = 2.6\ \mathrm{s}.
> $$

### EUP 2.67
Question: [[PHY1 HW Ch02 Questions#EUP 2.67|EUP 2.67]]

> [!solution] Solution
> **(a)** By (2.9), $\Delta x = \tfrac{1}{2}(v_{0} + v)t$:
> $$
> v_{0} = \frac{2\,\Delta x}{t} - v = \frac{2(140\ \mathrm{m})}{3.6\ \mathrm{s}} - 53\ \mathrm{m/s} = 24.8\ \mathrm{m/s} \approx 25\ \mathrm{m/s}.
> $$
>
> **(b)** By (2.7), $a = \dfrac{v - v_{0}}{t} = \dfrac{53\ \mathrm{m/s} - 24.8\ \mathrm{m/s}}{3.6\ \mathrm{s}} = 7.84\ \mathrm{m/s^2}$. From rest to $v = 53\ \mathrm{m/s}$, (2.11) gives
> $$
> d = \frac{v^{2}}{2a} = \frac{(53\ \mathrm{m/s})^{2}}{2(7.84\ \mathrm{m/s^2})} = 1.8 \times 10^{2}\ \mathrm{m}.
> $$

## Constant Acceleration with Two Objects

### EUP 2.55
Question: [[PHY1 HW Ch02 Questions#EUP 2.55|EUP 2.55]]

> [!solution] Solution
> Both start from rest at $x = 0$, so $x = \tfrac{1}{2}at^{2}$, and a car with acceleration $a$ finishes $L = 400\ \mathrm{m}$ at $t = \sqrt{2L/a}$.
> $$
> \begin{aligned}
> t_{\mathrm{w}} &= \sqrt{\frac{2(400\ \mathrm{m})}{4.25\ \mathrm{m/s^2}}} = 13.720\ \mathrm{s}, \\
> t_{\ell} &= t_{\mathrm{w}} + 0.248\ \mathrm{s} = 13.968\ \mathrm{s}, \qquad a_{\ell} = \frac{2L}{t_{\ell}^{2}}.
> \end{aligned}
> $$
> At $t_{\mathrm{w}}$ the loser is at
> $$
> x_{\ell} = \tfrac{1}{2}a_{\ell}t_{\mathrm{w}}^{2} = L\left(\frac{t_{\mathrm{w}}}{t_{\ell}}\right)^{2} = (400\ \mathrm{m})\left(\frac{13.720\ \mathrm{s}}{13.968\ \mathrm{s}}\right)^{2} = 385.9\ \mathrm{m},
> $$
> which is $400\ \mathrm{m} - 385.9\ \mathrm{m} = 14.1\ \mathrm{m}$ behind.

### EUP 2.68
Question: [[PHY1 HW Ch02 Questions#EUP 2.68|EUP 2.68]]

> [!solution] Solution
> Each car: $v_{0} = 88\ \mathrm{km/h} = 24.4\ \mathrm{m/s}$, $v = 0$, $a = -8\ \mathrm{m/s^2}$ along its own direction of motion. By (2.11), each needs
> $$
> d = \frac{-v_{0}^{2}}{2a} = \frac{-(24.4\ \mathrm{m/s})^{2}}{2(-8\ \mathrm{m/s^2})} = 37.3\ \mathrm{m}.
> $$
> $2d = 74.7\ \mathrm{m} < 85\ \mathrm{m}$: they do not collide, and they stop $85\ \mathrm{m} - 74.7\ \mathrm{m} \approx 10\ \mathrm{m}$ apart.
>
> Graph: with $x = 0$ at car 1 and car 2 at $85\ \mathrm{m}$ when they brake, $x_{1} = v_{0}t - \tfrac{1}{2}\lvert a \rvert t^{2}$ and $x_{2} = 85\ \mathrm{m} - v_{0}t + \tfrac{1}{2}\lvert a \rvert t^{2}$ until both stop at $t = v_{0}/\lvert a \rvert = 3.1\ \mathrm{s}$.
>
> ![[PHY1 Ch02 Problem 2.68 graph.png]]

### EUP 2.70
Question: [[PHY1 HW Ch02 Questions#EUP 2.70|EUP 2.70]]

> [!solution] Solution
> Take $x = 0$ at your car and $t = 0$ when you brake: $v_{1} = 85\ \mathrm{km/h}$, $v_{2} = 60\ \mathrm{km/h}$, $v_{1} - v_{2} = 25\ \mathrm{km/h} = 6.94\ \mathrm{m/s}$, $a = 4.2\ \mathrm{m/s^2}$ (magnitude), $d = 10\ \mathrm{m}$. The gap is
> $$
> s(t) = x_{2} - x_{1} = (d + v_{2}t) - \left(v_{1}t - \tfrac{1}{2}at^{2}\right) = d - (v_{1} - v_{2})t + \tfrac{1}{2}at^{2}.
> $$
> It is smallest when $\dfrac{ds}{dt} = -(v_{1} - v_{2}) + at = 0$, at $t = \dfrac{v_{1} - v_{2}}{a} = 1.65\ \mathrm{s}$:
> $$
> s_{\min} = d - \frac{(v_{1} - v_{2})^{2}}{2a} = 10\ \mathrm{m} - \frac{(6.94\ \mathrm{m/s})^{2}}{2(4.2\ \mathrm{m/s^2})} = 4.3\ \mathrm{m} > 0.
> $$
> No collision; the closest approach is $4.3\ \mathrm{m}$.

> [!warning] Closest approach
> It comes when the two velocities are equal, not when your car stops.

## Free Fall with One Object

### EUP 2.37
Question: [[PHY1 HW Ch02 Questions#EUP 2.37|EUP 2.37]]

> [!solution] Solution
> By (2.11), the velocity $v_{y}$ at height $y$ satisfies $v_{y}^{2} = v^{2} - 2gy$.
>
> **(a)** At the top $v_{y} = 0$: $h = \dfrac{v^{2}}{2g}$.
>
> **(b)** At $y = \tfrac{1}{2}h = \dfrac{v^{2}}{4g}$: $v_{y}^{2} = v^{2} - \tfrac{1}{2}v^{2}$, so $\lvert v_{y} \rvert = \dfrac{v}{\sqrt{2}}$.

### EUP 2.59
Question: [[PHY1 HW Ch02 Questions#EUP 2.59|EUP 2.59]]

> [!solution] Solution
> $y = 0$ at the ground, $y_{0} = 82.0\ \mathrm{m}$. By (2.10), $0 = y_{0} + v_{0}t - \tfrac{1}{2}gt^{2}$, whose positive root is
> $$
> t = \frac{v_{0} + \sqrt{v_{0}^{2} + 2gy_{0}}}{g}, \qquad 2gy_{0} = 1607\ \mathrm{m^2/s^2}.
> $$
> $$
> \begin{aligned}
> v_{0} = -7.68\ \mathrm{m/s}: \quad t &= \frac{-7.68\ \mathrm{m/s} + \sqrt{(7.68\ \mathrm{m/s})^{2} + 1607\ \mathrm{m^2/s^2}}}{9.8\ \mathrm{m/s^2}} = 3.38\ \mathrm{s}, \\
> v_{0} = +16.7\ \mathrm{m/s}: \quad t &= \frac{16.7\ \mathrm{m/s} + \sqrt{(16.7\ \mathrm{m/s})^{2} + 1607\ \mathrm{m^2/s^2}}}{9.8\ \mathrm{m/s^2}} = 6.14\ \mathrm{s}.
> \end{aligned}
> $$
> Fragments hit the ground from $3.38\ \mathrm{s}$ to $6.14\ \mathrm{s}$ after the explosion.

### EUP 2.73
Question: [[PHY1 HW Ch02 Questions#EUP 2.73|EUP 2.73]]

> [!solution] Solution
> Let $T$ be the total time of fall from height $h$. From rest, $h = \tfrac{1}{2}gT^{2}$, and the first $\tfrac{3}{4}h$ takes $T - 1\ \mathrm{s}$: $\tfrac{3}{4}h = \tfrac{1}{2}g(T - 1\ \mathrm{s})^{2}$. Dividing,
> $$
> \frac{T - 1\ \mathrm{s}}{T} = \frac{\sqrt{3}}{2} \implies T = \frac{1\ \mathrm{s}}{1 - \sqrt{3}/2} = 7.46\ \mathrm{s},
> $$
> $$
> h = \tfrac{1}{2}gT^{2} = \tfrac{1}{2}(9.8\ \mathrm{m/s^2})(7.46\ \mathrm{s})^{2} = 2.7 \times 10^{2}\ \mathrm{m}.
> $$
> (The root $-\tfrac{\sqrt{3}}{2}$ gives $T = 0.54\ \mathrm{s} < 1\ \mathrm{s}$ and is rejected.)

### EUP 2.85
Question: [[PHY1 HW Ch02 Questions#EUP 2.85|EUP 2.85]]

> [!solution] Solution
> The motion is symmetric about the peak. Falling from rest at the peak through a distance $d$ takes $t = \sqrt{2d/g}$:
> $$
> \frac{t_{\text{upper half}}}{t_{\text{total}}} = \frac{\sqrt{2(h/2)/g}}{\sqrt{2h/g}} = \frac{1}{\sqrt{2}} \approx 0.71.
> $$

### EUP 2.86
Question: [[PHY1 HW Ch02 Questions#EUP 2.86|EUP 2.86]]

> [!solution] Solution
> Take $y$ **downward**, so $a = +g$. Let $v_{\mathrm{t}}$ be the velocity at the top of the window. Across the window, by (2.10),
> $$
> \Delta y = v_{\mathrm{t}}t + \tfrac{1}{2}gt^{2} \implies v_{\mathrm{t}} = \frac{1.3\ \mathrm{m} - \tfrac{1}{2}(9.8\ \mathrm{m/s^2})(0.22\ \mathrm{s})^{2}}{0.22\ \mathrm{s}} = 4.83\ \mathrm{m/s}.
> $$
> From rest down to the top of the window, by (2.11),
> $$
> H = \frac{v_{\mathrm{t}}^{2}}{2g} = \frac{(4.83\ \mathrm{m/s})^{2}}{2(9.8\ \mathrm{m/s^2})} = 1.2\ \mathrm{m}.
> $$

> [!warning] Not from rest
> $1.3\ \mathrm{m} = \tfrac{1}{2}gt^{2}$ is wrong for the window: the balloon is already moving at its top.

### EUP 2.90
Question: [[PHY1 HW Ch02 Questions#EUP 2.90|EUP 2.90]]

> [!solution] Solution
> $y = 0$ at the floor, $y_{0} = 1.5\ \mathrm{m}$.
>
> **(a)** By (2.11) with $v_{0} = +7.3\ \mathrm{m/s}$, moving downward at the floor:
> $$
> v = -\sqrt{v_{0}^{2} + 2gy_{0}} = -\sqrt{(7.3\ \mathrm{m/s})^{2} + 2(9.8\ \mathrm{m/s^2})(1.5\ \mathrm{m})} = -9.1\ \mathrm{m/s}.
> $$
>
> **(b)** With $v_{0} = -7.3\ \mathrm{m/s}$, $v_{0}^{2}$ is the same: $v = -9.1\ \mathrm{m/s}$.
>
> **(c)** By (2.10), $0 = y_{0} + v_{0}t - \tfrac{1}{2}gt^{2}$ with $v_{0} = -7.3\ \mathrm{m/s}$:
> $$
> t = \frac{v_{0} \pm \sqrt{v_{0}^{2} + 2y_{0}g}}{g} = \frac{-7.3\ \mathrm{m/s} \pm 9.09\ \mathrm{m/s}}{9.8\ \mathrm{m/s^2}} = 0.18\ \mathrm{s} \ \text{ or } \ -1.7\ \mathrm{s}.
> $$
> It hits the floor after $0.18\ \mathrm{s}$. The root $-1.7\ \mathrm{s}$ is when a ball always in free fall would have left the floor moving upward.

### EUP 2.91
Question: [[PHY1 HW Ch02 Questions#EUP 2.91|EUP 2.91]]

> [!solution] Solution
> A drop falls $h = 0.196\ \mathrm{m}$ from rest in
> $$
> t = \sqrt{\frac{2h}{g}} = \sqrt{\frac{2(0.196\ \mathrm{m})}{9.8\ \mathrm{m/s^2}}} = 0.200\ \mathrm{s}.
> $$
> Four drops (one leaving, two in between, one landing) span three equal time intervals $\Delta t$: $\Delta t = \dfrac{0.200\ \mathrm{s}}{3} = 0.0667\ \mathrm{s}$, so there are $\dfrac{1}{\Delta t} = 15$ drops per second.

## Free Fall with Two Objects

### EUP 2.77
Question: [[PHY1 HW Ch02 Questions#EUP 2.77|EUP 2.77]]

> [!solution] Solution
> $y = 0$ at the water, $y_{0} = 3.00\ \mathrm{m}$.
>
> **(a)** By (2.11), $v^{2} = v_{0}^{2} + 2gy_{0}$:
> $$
> \begin{aligned}
> v_{1} &= \sqrt{(1.80\ \mathrm{m/s})^{2} + 2(9.8\ \mathrm{m/s^2})(3.00\ \mathrm{m})} = 7.88\ \mathrm{m/s}, \\
> v_{2} &= \sqrt{2(9.8\ \mathrm{m/s^2})(3.00\ \mathrm{m})} = 7.67\ \mathrm{m/s}.
> \end{aligned}
> $$
>
> **(b)** The first diver passes the platform going down at $1.80\ \mathrm{m/s}$, at the instant the second steps off. From then on, by (2.7),
> $$
> t_{1} = \frac{7.877\ \mathrm{m/s} - 1.80\ \mathrm{m/s}}{9.8\ \mathrm{m/s^2}} = 0.620\ \mathrm{s}, \qquad t_{2} = \frac{7.668\ \mathrm{m/s}}{9.8\ \mathrm{m/s^2}} = 0.782\ \mathrm{s}.
> $$
> The first diver hits the water first, by $0.16\ \mathrm{s}$.

### EUP 2.78
Question: [[PHY1 HW Ch02 Questions#EUP 2.78|EUP 2.78]]

> [!solution] Solution
> Take $y$ upward from the point of release, with $u = 10\ \mathrm{m/s}$ for the balloon and $w = 12\ \mathrm{m/s}$ for the ball relative to it:
> $$
> y_{\text{ball}} = (u + w)t - \tfrac{1}{2}gt^{2}, \qquad y_{\text{hand}} = ut.
> $$
> Equal when $wt - \tfrac{1}{2}gt^{2} = 0$: $t = 0$ (the throw) or
> $$
> t = \frac{2w}{g} = \frac{2(12\ \mathrm{m/s})}{9.8\ \mathrm{m/s^2}} = 2.4\ \mathrm{s}.
> $$

### EUP 2.97
Question: [[PHY1 HW Ch02 Questions#EUP 2.97|EUP 2.97]]

> [!solution] Solution
> $y = 0$ at the ground:
> $$
> y_{1} = h_{0} - \tfrac{1}{2}gt^{2}, \qquad y_{2} = v_{0}t - \tfrac{1}{2}gt^{2}.
> $$
> $y_{1} = y_{2}$ gives $t = \dfrac{h_{0}}{v_{0}}$.
>
> **(b)** The height is $y = h_{0} - \tfrac{1}{2}g\left(\dfrac{h_{0}}{v_{0}}\right)^{2} = h_{0} - \dfrac{gh_{0}^{2}}{2v_{0}^{2}}$.
>
> **(a)** Mid-air means $y > 0$: $v_{0} > \sqrt{\dfrac{gh_{0}}{2}}$.

## Nonconstant Acceleration

### EUP 2.88
Question: [[PHY1 HW Ch02 Questions#EUP 2.88|EUP 2.88]]

> [!solution] Solution
> **(a)** $v(t) = \displaystyle\int (a_{0} + bt)\,dt = a_{0}t + \tfrac{1}{2}bt^{2} + C_{1}$, and $v(0) = v_{0}$ gives $C_{1} = v_{0}$:
> $$
> v(t) = v_{0} + a_{0}t + \tfrac{1}{2}bt^{2}.
> $$
>
> **(b)** $x(t) = \displaystyle\int v\,dt = v_{0}t + \tfrac{1}{2}a_{0}t^{2} + \tfrac{1}{6}bt^{3} + C_{2}$, and $x(0) = x_{0}$ gives $C_{2} = x_{0}$:
> $$
> x(t) = x_{0} + v_{0}t + \tfrac{1}{2}a_{0}t^{2} + \tfrac{1}{6}bt^{3}.
> $$

### EUP 2.94
Question: [[PHY1 HW Ch02 Questions#EUP 2.94|EUP 2.94]]

> [!solution] Solution
> With $v(0) = 0$ and $x(0) = 0$,
> $$
> v(t) = \int_{0}^{t} bt'^{2}\,dt' = \tfrac{1}{3}bt^{3}, \qquad x(t) = \int_{0}^{t} \tfrac{1}{3}bt'^{3}\,dt' = \tfrac{1}{12}bt^{4},
> $$
> $$
> x(6.3\ \mathrm{s}) = \tfrac{1}{12}(0.041\ \mathrm{m/s^4})(6.3\ \mathrm{s})^{4} = 5.4\ \mathrm{m}.
> $$

### EUP 2.95
Question: [[PHY1 HW Ch02 Questions#EUP 2.95|EUP 2.95]]

> [!solution] Solution
> **(a)** With $x(0) = 0$,
> $$
> x(t) = \int_{0}^{t} \left(bt' - ct'^{3}\right)dt' = \tfrac{1}{2}bt^{2} - \tfrac{1}{4}ct^{4} = \tfrac{1}{4}t^{2}\left(2b - ct^{2}\right),
> $$
> so $x = 0$ again at $t = \sqrt{\dfrac{2b}{c}}$.
>
> **(b)** $a = \dfrac{dv}{dt} = b - 3ct^{2}$; with $ct^{2} = 2b$, $a = b - 6b = -5b$.

### EUP 2.96
Question: [[PHY1 HW Ch02 Questions#EUP 2.96|EUP 2.96]]

> [!solution] Solution
> **(a)** With $v(0) = 0$,
> $$
> v(t) = \int_{0}^{t} a_{0}e^{-bt'}\,dt' = \frac{a_{0}}{b}\left(1 - e^{-bt}\right).
> $$
>
> **(b)** No: as $t \to \infty$, $v \to \dfrac{a_{0}}{b}$.
>
> **(c)** Yes:
> $$
> x(t) = \int_{0}^{t} v\,dt' = \frac{a_{0}}{b}\left[t - \frac{1}{b}\left(1 - e^{-bt}\right)\right] \to \infty \quad \text{as } t \to \infty.
> $$

## Reading Graphs

### EUP 2.98 to 2.102
Question: [[PHY1 HW Ch02 Questions#EUP 2.98 to 2.102|EUP 2.98 to 2.102]]

![[PHY1 Ch02 Fig 2.16.png]]

> [!solution] Solution
> On a $v$–$t$ graph the height of the curve is $v$ and its slope is $a$.
> - **98.** b. $v = 0$ where the curve meets the time axis: A, E, and H.
> - **99.** c. $a = 0$ where the slope is zero: C and F.
> - **100.** b. $\lvert v \rvert$ is largest at C (F is closer to the axis).
> - **101.** c. The curve is steepest at D.
> - **102.** b. $v > 0$ from A to E and $v < 0$ after E, so the tiger is farthest from its start at E.

## Data and Straight-Line Fits

### EUP 2.58
Question: [[PHY1 HW Ch02 Questions#EUP 2.58|EUP 2.58]]

> [!solution] Solution
> From rest at $x = 0$, (2.10) gives $x = \tfrac{1}{2}at^{2}$: plot $x$ versus $t^{2}$; the slope is $\tfrac{1}{2}a$.
>
> | $t^{2}$ ($\mathrm{s^2}$) | 0 | 1 | 4 | 9 | 16 | 25 |
> | --- | --- | --- | --- | --- | --- | --- |
> | $x$ ($\mathrm{m}$) | 0 | 1.7 | 6.2 | 17 | 24 | 40 |
>
> The best-fit line has slope $\approx 1.6\ \mathrm{m/s^2}$, so $a = 2 \times \text{slope} \approx 3.2\ \mathrm{m/s^2}$.
>
> ![[PHY1 Ch02 Problem 2.58 fit.png]]
