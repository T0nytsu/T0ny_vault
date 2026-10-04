---
course: [PHY1]
chapter: ["2.1", "2.2", "2.3", "2.4", "2.5", "2.6"]
tags: [physics, problems, solutions, kinematics]
source:
  - "Own solutions in the IDEA format of EUP; every number checked with Python, the symbolic results with sympy"
created: 2026-10-05
questions: "[[PHY1 Ch02 Questions]]"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[PHY1 Ch02 Questions#EUP 2.13\|EUP 2.13]] | (a) $24\ \mathrm{km}$ north; (b) $9.6\ \mathrm{km/h}$ north; (c) $16\ \mathrm{km/h}$ south; (d) $0$; (e) $0$ |
| [[PHY1 Ch02 Questions#EUP 2.21\|EUP 2.21]] | $0.38\ \mathrm{m/s^2}$ |
| [[PHY1 Ch02 Questions#EUP 2.37\|EUP 2.37]] | (a) $\dfrac{v^{2}}{2g}$; (b) $\dfrac{v}{\sqrt{2}}$ |
| [[PHY1 Ch02 Questions#EUP 2.52\|EUP 2.52]] | After $6.03\ \mathrm{h}$, $6.27 \times 10^{3}\ \mathrm{km}$ from London |
| [[PHY1 Ch02 Questions#EUP 2.53\|EUP 2.53]] | (a) $9.82\ \mathrm{m/s}$; (b) $9.34\ \mathrm{m/s}$; (c) $9.18\ \mathrm{m/s}$; (d) $v = b + 3ct^{2}$, $9.18\ \mathrm{m/s}$ |
| [[PHY1 Ch02 Questions#EUP 2.55\|EUP 2.55]] | $14.1\ \mathrm{m}$ |
| [[PHY1 Ch02 Questions#EUP 2.58\|EUP 2.58]] | $x$ against $t^{2}$; $a \approx 3.2\ \mathrm{m/s^2}$ |
| [[PHY1 Ch02 Questions#EUP 2.59\|EUP 2.59]] | From $3.38\ \mathrm{s}$ to $6.14\ \mathrm{s}$ after the explosion |
| [[PHY1 Ch02 Questions#EUP 2.66\|EUP 2.66]] | (a) $21\ \mathrm{m/s}$, or $77\ \mathrm{km/h}$; (b) $2.6\ \mathrm{s}$ |
| [[PHY1 Ch02 Questions#EUP 2.68\|EUP 2.68]] | No collision; about $10\ \mathrm{m}$ apart |
| [[PHY1 Ch02 Questions#EUP 2.70\|EUP 2.70]] | No collision; closest approach $4.3\ \mathrm{m}$ |
| [[PHY1 Ch02 Questions#EUP 2.73\|EUP 2.73]] | About $2.7 \times 10^{2}\ \mathrm{m}$ |
| [[PHY1 Ch02 Questions#EUP 2.77\|EUP 2.77]] | (a) $7.88\ \mathrm{m/s}$ and $7.67\ \mathrm{m/s}$; (b) the first diver, by $0.16\ \mathrm{s}$ |
| [[PHY1 Ch02 Questions#EUP 2.78\|EUP 2.78]] | $2.4\ \mathrm{s}$ |
| [[PHY1 Ch02 Questions#EUP 2.83\|EUP 2.83]] | (a) $\tfrac{1}{2}(v_{1} + v_{2})$; (b) $\dfrac{2v_{1}v_{2}}{v_{1} + v_{2}}$; (c) half the time |
| [[PHY1 Ch02 Questions#EUP 2.85\|EUP 2.85]] | $\dfrac{1}{\sqrt{2}} \approx 71\%$ |
| [[PHY1 Ch02 Questions#EUP 2.86\|EUP 2.86]] | $1.2\ \mathrm{m}$ above the top of the window |
| [[PHY1 Ch02 Questions#EUP 2.88\|EUP 2.88]] | (a) $v = v_{0} + a_{0}t + \tfrac{1}{2}bt^{2}$; (b) $x = x_{0} + v_{0}t + \tfrac{1}{2}a_{0}t^{2} + \tfrac{1}{6}bt^{3}$ |
| [[PHY1 Ch02 Questions#EUP 2.91\|EUP 2.91]] | $15$ drops per second |
| [[PHY1 Ch02 Questions#EUP 2.95\|EUP 2.95]] | (a) $t = \sqrt{2b/c}$; (b) $a = -5b$ |
| [[PHY1 Ch02 Questions#EUP 2.96\|EUP 2.96]] | (a) $v = \dfrac{a_{0}}{b}\left(1 - e^{-bt}\right)$; (b) no, it approaches $a_{0}/b$; (c) yes |
| [[PHY1 Ch02 Questions#EUP 2.97\|EUP 2.97]] | (a) $v_{0} > \sqrt{gh_{0}/2}$; (b) $y = h_{0} - \dfrac{gh_{0}^{2}}{2v_{0}^{2}}$ |
| [[PHY1 Ch02 Questions#EUP 2.98 to 2.102\|EUP 2.98 to 2.102]] | b, c, b, c, b |

> [!note] Notation
> - Free-fall problems take the upward direction as positive unless the solution says otherwise, so $a = -g$ with $g = 9.8\ \mathrm{m/s^2}$.
> - Equation numbers such as (2.10) are those of EUP Table 2.1.
> - Intermediate values keep an extra figure; final answers are rounded to the precision of the data.

## EUP §2.1 Average Motion

### EUP 2.13
Question: [[PHY1 Ch02 Questions#EUP 2.13|EUP 2.13]]

> [!solution] Solution
> **Interpret.** One-dimensional motion in two legs. The quantities are displacement and average velocity, which carry a sign, not distance and speed.
>
> **Develop.** Take home as the origin and north as the positive direction. Then $\Delta x = x_{2} - x_{1}$ and $\bar{v} = \Delta x/\Delta t$ (2.1) for each interval.
>
> **Evaluate.**
> - (a) $\Delta x = 24\ \mathrm{km} - 0 = +24\ \mathrm{km}$, that is, $24\ \mathrm{km}$ north.
> - (b) $\bar{v} = \dfrac{+24\ \mathrm{km}}{2.5\ \mathrm{h}} = +9.6\ \mathrm{km/h}$, north.
> - (c) $\bar{v} = \dfrac{0 - 24\ \mathrm{km}}{1.5\ \mathrm{h}} = -16\ \mathrm{km/h}$, that is, $16\ \mathrm{km/h}$ south.
> - (d) $\Delta x = 0 - 0 = 0$.
> - (e) $\bar{v} = \dfrac{0}{4.0\ \mathrm{h}} = 0$.
>
> **Assess.** The average speed for the whole trip is not zero: it is $\dfrac{48\ \mathrm{km}}{4.0\ \mathrm{h}} = 12\ \mathrm{km/h}$. Average velocity depends only on where the trip starts and ends.

## EUP §2.3 Acceleration

### EUP 2.21
Question: [[PHY1 Ch02 Questions#EUP 2.21|EUP 2.21]]

> [!solution] Solution
> **Interpret.** We want the average acceleration over a $48$-s interval in which the acceleration is not constant.
>
> **Develop.** $\bar{a} = \Delta v/\Delta t$ (2.4) uses only the velocities at the two ends of the interval: $v_{1} = 0$ and $v_{2} = 18\ \mathrm{m/s}$.
>
> **Evaluate.**
> $$
> \bar{a} = \frac{\Delta v}{\Delta t} = \frac{18\ \mathrm{m/s} - 0}{48\ \mathrm{s}} = 0.38\ \mathrm{m/s^2}
> $$
>
> **Assess.** The $25\ \mathrm{m/s}$ reached in between does not enter. An average over an interval depends on the net change, just as average velocity depends only on the displacement.

## EUP §2.5 The Acceleration of Gravity

### EUP 2.37
Question: [[PHY1 Ch02 Questions#EUP 2.37|EUP 2.37]]

> [!solution] Solution
> **Interpret.** After launch the rocket is in free fall: constant acceleration $g$ downward. The answers are expressions in $v$ and $g$.
>
> **Develop.** Take $y = 0$ at the ground and upward positive, so $a = -g$ and $v_{0} = v$. No time is given or asked for, so use (2.11): $v_{y}^{2} = v^{2} - 2gy$, where $v_{y}$ is the velocity at height $y$.
>
> **Evaluate.**
> - (a) At the maximum altitude $v_{y} = 0$:
> $$
> 0 = v^{2} - 2gy_{\max} \implies y_{\max} = \frac{v^{2}}{2g}.
> $$
> - (b) At $y = \tfrac{1}{2}y_{\max} = \dfrac{v^{2}}{4g}$:
> $$
> v_{y}^{2} = v^{2} - 2g\left(\frac{v^{2}}{4g}\right) = \frac{v^{2}}{2} \implies \lvert v_{y} \rvert = \frac{v}{\sqrt{2}} \approx 0.71v.
> $$
>
> **Assess.** $v^{2}/g$ has units $(\mathrm{m/s})^{2}/(\mathrm{m/s^2}) = \mathrm{m}$. At half the height the rocket still has $71\%$ of its speed, not half: $v^{2}$, not $v$, decreases linearly with height. The speed is the same going up and coming down.

## EUP Chapter 2 Problems

### EUP 2.52
Question: [[PHY1 Ch02 Questions#EUP 2.52|EUP 2.52]]

> [!solution] Solution
> **Interpret.** Two objects move toward each other at constant velocity. They pass when their positions are equal.
>
> **Develop.** Take London as the origin, the direction toward Singapore as positive, and $t = 0$ at departure. With $L = 10\,886\ \mathrm{km}$, $v_{1} = 1040\ \mathrm{km/h}$, and $v_{2} = 765\ \mathrm{km/h}$,
> $$
> x_{1} = v_{1}t, \qquad x_{2} = L - v_{2}t.
> $$
>
> **Evaluate.** Setting $x_{1} = x_{2}$,
> $$
> \begin{aligned}
> t &= \frac{L}{v_{1} + v_{2}} = \frac{10\,886\ \mathrm{km}}{1805\ \mathrm{km/h}} = 6.03\ \mathrm{h}, \\
> x_{1} &= v_{1}t = (1040\ \mathrm{km/h})(6.031\ \mathrm{h}) = 6.27 \times 10^{3}\ \mathrm{km}.
> \end{aligned}
> $$
> The planes pass $6.03\ \mathrm{h}$ after departure, $6.27 \times 10^{3}\ \mathrm{km}$ from London and $4.61 \times 10^{3}\ \mathrm{km}$ from Singapore.
>
> **Assess.** The gap closes at the sum of the two speeds. The faster plane covers more than half the distance, in the ratio $1040 : 765$.

### EUP 2.53
Question: [[PHY1 Ch02 Questions#EUP 2.53|EUP 2.53]]

> [!solution] Solution
> **Interpret.** Average velocities over shrinking intervals centered on $t = 2\ \mathrm{s}$ should approach the instantaneous velocity there.
>
> **Develop.** Use $\bar{v} = \dfrac{x(t_{2}) - x(t_{1})}{t_{2} - t_{1}}$ (2.1) with $x = bt + ct^{3}$, and $v = dx/dt$ (2.2) with the rule $d(bt^{n})/dt = nbt^{n-1}$ (2.3).
>
> **Evaluate.**
> - (a) $x(3.00\ \mathrm{s}) = 21.78\ \mathrm{m}$ and $x(1.00\ \mathrm{s}) = 2.14\ \mathrm{m}$, so $\bar{v} = \dfrac{19.64\ \mathrm{m}}{2.00\ \mathrm{s}} = 9.82\ \mathrm{m/s}$.
> - (b) $x(2.50\ \mathrm{s}) = 13.75\ \mathrm{m}$ and $x(1.50\ \mathrm{s}) = 4.41\ \mathrm{m}$, so $\bar{v} = \dfrac{9.34\ \mathrm{m}}{1.00\ \mathrm{s}} = 9.34\ \mathrm{m/s}$.
> - (c) $x(2.05\ \mathrm{s}) = 8.5887\ \mathrm{m}$ and $x(1.95\ \mathrm{s}) = 7.6706\ \mathrm{m}$, so $\bar{v} = \dfrac{0.9182\ \mathrm{m}}{0.10\ \mathrm{s}} = 9.18\ \mathrm{m/s}$.
> - (d) Differentiating,
> $$
> v = \frac{dx}{dt} = b + 3ct^{2}, \qquad v(2\ \mathrm{s}) = 1.50\ \mathrm{m/s} + 3(0.640\ \mathrm{m/s^3})(2\ \mathrm{s})^{2} = 9.18\ \mathrm{m/s}.
> $$
>
> **Assess.** The average velocities $9.82$, $9.34$, $9.18\ \mathrm{m/s}$ approach the instantaneous value $9.18\ \mathrm{m/s}$ as the interval shrinks. In (c) the displacement is a small difference of two nearby positions, so the positions keep five figures.

### EUP 2.55
Question: [[PHY1 Ch02 Questions#EUP 2.55|EUP 2.55]]

> [!solution] Solution
> **Interpret.** Two objects with different constant accelerations start from rest at the same place and time. We want the loser's position at the moment the winner finishes.
>
> **Develop.** With $x_{0} = 0$ and $v_{0} = 0$, (2.10) gives $x = \tfrac{1}{2}at^{2}$ for each car. The plan: the winner's time $t_{\mathrm{w}}$ from $L = 400\ \mathrm{m}$; the loser's time $t_{\ell} = t_{\mathrm{w}} + 0.248\ \mathrm{s}$; the loser's acceleration from $L = \tfrac{1}{2}a_{\ell}t_{\ell}^{2}$; then the loser's position at $t_{\mathrm{w}}$.
>
> **Evaluate.**
> $$
> \begin{aligned}
> t_{\mathrm{w}} &= \sqrt{\frac{2L}{a_{\mathrm{w}}}} = \sqrt{\frac{2(400\ \mathrm{m})}{4.25\ \mathrm{m/s^2}}} = 13.720\ \mathrm{s}, \qquad t_{\ell} = 13.968\ \mathrm{s}, \\
> x_{\ell}(t_{\mathrm{w}}) &= \tfrac{1}{2}a_{\ell}t_{\mathrm{w}}^{2} = L\left(\frac{t_{\mathrm{w}}}{t_{\ell}}\right)^{2} = (400\ \mathrm{m})\left(\frac{13.720}{13.968}\right)^{2} = 385.9\ \mathrm{m}.
> \end{aligned}
> $$
> The loser is $400\ \mathrm{m} - 385.9\ \mathrm{m} = 14.1\ \mathrm{m}$ behind.
>
> **Assess.** Near the finish the loser moves at about $a_{\ell}t_{\ell} = 57\ \mathrm{m/s}$, and $(57\ \mathrm{m/s})(0.248\ \mathrm{s}) \approx 14\ \mathrm{m}$, in agreement. The answer is a small difference of large numbers, so the intermediate times keep extra figures.

### EUP 2.58
Question: [[PHY1 Ch02 Questions#EUP 2.58|EUP 2.58]]

> [!solution] Solution
> **Interpret.** The car starts from rest at $x = 0$. If its acceleration is constant, its position is quadratic in time, and we want a plot that turns that into a straight line.
>
> **Develop.** With $x_{0} = 0$ and $v_{0} = 0$, (2.10) is $x = \tfrac{1}{2}at^{2}$. Plotting $x$ against $t^{2}$ gives a straight line through the origin with slope $\tfrac{1}{2}a$.
>
> **Evaluate.**
>
> | $t^{2}$ ($\mathrm{s^2}$) | 0 | 1 | 4 | 9 | 16 | 25 |
> | --- | --- | --- | --- | --- | --- | --- |
> | $x$ (m) | 0 | 1.7 | 6.2 | 17 | 24 | 40 |
>
> ![[PHY1 EUP 2.58 fit.png]]
>
> The best-fit line through the origin has slope about $1.6\ \mathrm{m/s^2}$, so
> $$
> a = 2(\text{slope}) \approx 3.2\ \mathrm{m/s^2}.
> $$
>
> **Assess.** The points scatter about the line (the point at $t = 3\ \mathrm{s}$ lies above it), so the acceleration is only approximately constant and two figures are the most the data support. The slope is half the acceleration, as in Example 1.4.

### EUP 2.59
Question: [[PHY1 Ch02 Questions#EUP 2.59|EUP 2.59]]

> [!solution] Solution
> **Interpret.** Every fragment is in free fall from the same height with a different initial velocity. The first fragment to land is the one thrown downward fastest, the last the one thrown upward fastest.
>
> **Develop.** Take $y = 0$ at the ground and upward positive, with $y_{0} = 82.0\ \mathrm{m}$. Setting $y = 0$ in (2.10), $0 = y_{0} + v_{0}t - \tfrac{1}{2}gt^{2}$, and solving the quadratic for the positive root,
> $$
> t = \frac{v_{0} + \sqrt{v_{0}^{2} + 2gy_{0}}}{g}.
> $$
>
> **Evaluate.**
> $$
> \begin{aligned}
> v_{0} = -7.68\ \mathrm{m/s}: \quad t &= \frac{-7.68\ \mathrm{m/s} + \sqrt{(7.68\ \mathrm{m/s})^{2} + 2(9.8\ \mathrm{m/s^2})(82.0\ \mathrm{m})}}{9.8\ \mathrm{m/s^2}} = 3.38\ \mathrm{s}, \\
> v_{0} = +16.7\ \mathrm{m/s}: \quad t &= \frac{16.7\ \mathrm{m/s} + \sqrt{(16.7\ \mathrm{m/s})^{2} + 2(9.8\ \mathrm{m/s^2})(82.0\ \mathrm{m})}}{9.8\ \mathrm{m/s^2}} = 6.14\ \mathrm{s}.
> \end{aligned}
> $$
> Fragments hit the ground from $3.38\ \mathrm{s}$ to $6.14\ \mathrm{s}$ after the explosion, an interval of $2.75\ \mathrm{s}$.
>
> **Assess.** One formula covers both fragments; only the sign of $v_{0}$ changes. The other root of the quadratic is negative: it is the time before the explosion at which a fragment on the same path would have been at the ground, and it is not part of this problem. A fragment dropped from rest would take $\sqrt{2y_{0}/g} = 4.09\ \mathrm{s}$, between the two answers.

### EUP 2.66
Question: [[PHY1 Ch02 Questions#EUP 2.66|EUP 2.66]]

> [!solution] Solution
> **Interpret.** One object slows with constant acceleration over a known distance and still has a known speed at the end.
>
> **Develop.** Take the direction of motion as positive, so $a = -6.3\ \mathrm{m/s^2}$, $x - x_{0} = 34\ \mathrm{m}$, and $v = 18\ \mathrm{km/h} = 5.0\ \mathrm{m/s}$. Use (2.11) for $v_{0}$, which involves no time, then (2.7) for $t$.
>
> **Evaluate.**
> - (a) From $v^{2} = v_{0}^{2} + 2a(x - x_{0})$,
> $$
> v_{0} = \sqrt{v^{2} - 2a(x - x_{0})} = \sqrt{(5.0\ \mathrm{m/s})^{2} - 2(-6.3\ \mathrm{m/s^2})(34\ \mathrm{m})} = 21.3\ \mathrm{m/s} \approx 21\ \mathrm{m/s},
> $$
> which is $77\ \mathrm{km/h}$.
> - (b) From $v = v_{0} + at$,
> $$
> t = \frac{v - v_{0}}{a} = \frac{5.0\ \mathrm{m/s} - 21.3\ \mathrm{m/s}}{-6.3\ \mathrm{m/s^2}} = 2.6\ \mathrm{s}.
> $$
>
> **Assess.** Check with (2.9): $\tfrac{1}{2}(v_{0} + v)t = \tfrac{1}{2}(26.3\ \mathrm{m/s})(2.59\ \mathrm{s}) = 34\ \mathrm{m}$. The acceleration is negative because it is opposite to the velocity; with a positive $a$ the square root in (a) would be of a negative number. The speed is converted to $\mathrm{m/s}$ before it meets an acceleration in $\mathrm{m/s^2}$.

### EUP 2.68
Question: [[PHY1 Ch02 Questions#EUP 2.68|EUP 2.68]]

> [!solution] Solution
> **Interpret.** Two cars brake toward each other with the same speed and the same acceleration. They collide only if the two stopping distances add up to more than the initial separation.
>
> **Develop.** For each car, (2.11) with final velocity zero gives the stopping distance $d = \dfrac{v_{0}^{2}}{2\lvert a \rvert}$, with $v_{0} = 88\ \mathrm{km/h} = 24.4\ \mathrm{m/s}$ and $\lvert a \rvert = 8\ \mathrm{m/s^2}$.
>
> **Evaluate.**
> $$
> d = \frac{v_{0}^{2}}{2\lvert a \rvert} = \frac{(24.4\ \mathrm{m/s})^{2}}{2(8\ \mathrm{m/s^2})} = 37\ \mathrm{m}
> $$
> The two cars together need $2d \approx 75\ \mathrm{m}$, less than $85\ \mathrm{m}$. They do not collide, and they stop about $85\ \mathrm{m} - 75\ \mathrm{m} = 10\ \mathrm{m}$ apart, after $t = v_{0}/\lvert a \rvert = 3.1\ \mathrm{s}$.
>
> ![[PHY1 EUP 2.68 plot.png]]
>
> **Assess.** The margin is small: the stopping distance grows as $v_{0}^{2}$, so at $94\ \mathrm{km/h}$ each car would need $43\ \mathrm{m}$ and they would collide. The braking acceleration is given to one figure, so "about $10\ \mathrm{m}$" is all we can claim.

### EUP 2.70
Question: [[PHY1 Ch02 Questions#EUP 2.70|EUP 2.70]]

> [!solution] Solution
> **Interpret.** Two objects: your car slows with constant acceleration and the car ahead moves at constant velocity. You collide if the gap between the cars reaches zero.
>
> **Develop.** Take your position at the moment you brake as the origin and the direction of motion as positive. With $v_{1} = 85\ \mathrm{km/h}$, $v_{2} = 60\ \mathrm{km/h}$, $a = -4.2\ \mathrm{m/s^2}$, and initial gap $d_{0} = 10\ \mathrm{m}$, (2.10) gives
> $$
> x_{1} = v_{1}t + \tfrac{1}{2}at^{2}, \qquad x_{2} = d_{0} + v_{2}t, \qquad \text{gap} = x_{2} - x_{1} = d_{0} - (v_{1} - v_{2})t - \tfrac{1}{2}at^{2}.
> $$
> The gap is smallest when its rate of change is zero, that is, when the two velocities are equal.
>
> **Evaluate.** The relative speed is $v_{1} - v_{2} = 25\ \mathrm{km/h} = 6.94\ \mathrm{m/s}$. The velocities are equal at
> $$
> t = \frac{v_{1} - v_{2}}{\lvert a \rvert} = \frac{6.94\ \mathrm{m/s}}{4.2\ \mathrm{m/s^2}} = 1.65\ \mathrm{s},
> $$
> and by then the gap has closed by
> $$
> \frac{(v_{1} - v_{2})^{2}}{2\lvert a \rvert} = \frac{(6.94\ \mathrm{m/s})^{2}}{2(4.2\ \mathrm{m/s^2})} = 5.7\ \mathrm{m}.
> $$
> Since $5.7\ \mathrm{m} < 10\ \mathrm{m}$, there is no collision. The closest approach is $10\ \mathrm{m} - 5.7\ \mathrm{m} = 4.3\ \mathrm{m}$.
>
> **Assess.** Seen from the car ahead, you approach at $6.94\ \mathrm{m/s}$ and slow at $4.2\ \mathrm{m/s^2}$: this is the stopping-distance formula of (2.11) with relative quantities. The closest approach comes when the speeds are equal, not when you stop; after that the car ahead pulls away.

### EUP 2.73
Question: [[PHY1 Ch02 Questions#EUP 2.73|EUP 2.73]]

> [!solution] Solution
> **Interpret.** An object dropped from rest falls a total height $h$ in a total time $T$. In the last second it covers $\tfrac{1}{4}h$, so in the time $T - 1\ \mathrm{s}$ it covers $\tfrac{3}{4}h$.
>
> **Develop.** Take the release point as the origin and downward positive, so the distance fallen is $\tfrac{1}{2}gt^{2}$. Write this at the two times:
> $$
> h = \tfrac{1}{2}gT^{2}, \qquad \tfrac{3}{4}h = \tfrac{1}{2}g(T - 1\ \mathrm{s})^{2}.
> $$
>
> **Evaluate.** Dividing the second equation by the first,
> $$
> \left(\frac{T - 1\ \mathrm{s}}{T}\right)^{2} = \frac{3}{4} \implies \frac{T - 1\ \mathrm{s}}{T} = \frac{\sqrt{3}}{2} \implies T = \frac{1\ \mathrm{s}}{1 - \sqrt{3}/2} = 7.46\ \mathrm{s}.
> $$
> Then
> $$
> h = \tfrac{1}{2}gT^{2} = \tfrac{1}{2}(9.8\ \mathrm{m/s^2})(7.46\ \mathrm{s})^{2} = 2.7 \times 10^{2}\ \mathrm{m}.
> $$
>
> **Assess.** Taking the negative square root, $-\sqrt{3}/2$, gives $T = 0.54\ \mathrm{s}$, a fall shorter than one second, which contradicts "the last second"; that root is rejected. Check: in $6.46\ \mathrm{s}$ the object falls $205\ \mathrm{m}$, which is $\tfrac{3}{4}$ of $273\ \mathrm{m}$. The mass of the object does not enter: all objects in free fall have the same acceleration.

### EUP 2.77
Question: [[PHY1 Ch02 Questions#EUP 2.77|EUP 2.77]]

> [!solution] Solution
> **Interpret.** Two objects in free fall. The first diver leaves the platform moving upward; the second leaves from rest at the moment the first comes back to the level of the platform.
>
> **Develop.** Take $y = 0$ at the water and upward positive, so the platform is at $y_{0} = 3.00\ \mathrm{m}$. Use (2.11) for the speeds at the water. A diver thrown upward returns to the launch height with the same speed, so the first diver passes the platform moving down at $1.80\ \mathrm{m/s}$. From that instant both divers fall from the same height, and (2.7) gives each time.
>
> **Evaluate.**
> - (a) At the water,
> $$
> \begin{aligned}
> \lvert v_{1} \rvert &= \sqrt{v_{0}^{2} + 2gy_{0}} = \sqrt{(1.80\ \mathrm{m/s})^{2} + 2(9.8\ \mathrm{m/s^2})(3.00\ \mathrm{m})} = 7.88\ \mathrm{m/s}, \\
> \lvert v_{2} \rvert &= \sqrt{2gy_{0}} = \sqrt{2(9.8\ \mathrm{m/s^2})(3.00\ \mathrm{m})} = 7.67\ \mathrm{m/s}.
> \end{aligned}
> $$
> - (b) Measured from the instant the first diver passes the platform on the way down,
> $$
> t_{1} = \frac{7.88\ \mathrm{m/s} - 1.80\ \mathrm{m/s}}{9.8\ \mathrm{m/s^2}} = 0.620\ \mathrm{s}, \qquad t_{2} = \frac{7.67\ \mathrm{m/s}}{9.8\ \mathrm{m/s^2}} = 0.782\ \mathrm{s}.
> $$
> The first diver hits the water first, by $0.782\ \mathrm{s} - 0.620\ \mathrm{s} = 0.16\ \mathrm{s}$.
>
> **Assess.** Both fall the same $3.00\ \mathrm{m}$ from that instant, but the first diver already has a downward velocity, so arrives sooner and faster. The speeds differ by little because $v^{2}$, not $v$, gains the same amount $2gy_{0}$.

### EUP 2.78
Question: [[PHY1 Ch02 Questions#EUP 2.78|EUP 2.78]]

> [!solution] Solution
> **Interpret.** Two objects: the balloon rises at constant velocity, and the ball is in free fall. The passenger catches the ball when the two are at the same height again.
>
> **Develop.** Take the release point as the origin and upward positive. Relative to the ground the ball starts at $10\ \mathrm{m/s} + 12\ \mathrm{m/s} = 22\ \mathrm{m/s}$. With (2.10),
> $$
> y_{\text{ball}} = (22\ \mathrm{m/s})t - \tfrac{1}{2}gt^{2}, \qquad y_{\text{balloon}} = (10\ \mathrm{m/s})t.
> $$
>
> **Evaluate.** Setting the two equal,
> $$
> (12\ \mathrm{m/s})t - \tfrac{1}{2}gt^{2} = 0 \implies t = 0 \quad \text{or} \quad t = \frac{2(12\ \mathrm{m/s})}{9.8\ \mathrm{m/s^2}} = 2.4\ \mathrm{s}.
> $$
> The passenger catches the ball $2.4\ \mathrm{s}$ later.
>
> **Assess.** The balloon's $10\ \mathrm{m/s}$ cancels. Seen from the balloon, which moves at constant velocity, the ball is simply thrown up at $12\ \mathrm{m/s}$ and returns after $2v/g$. The root $t = 0$ is the throw itself.

### EUP 2.83
Question: [[PHY1 Ch02 Questions#EUP 2.83|EUP 2.83]]

> [!solution] Solution
> **Interpret.** Average speed is total distance divided by total time. The two cases differ in what is shared equally between the two speeds.
>
> **Develop.** Let $T$ be the total time. In (a) each speed lasts $\tfrac{1}{2}T$; add the distances. In (b) each speed covers $\tfrac{1}{2}L$; add the times.
>
> **Evaluate.**
> - (a) $L = v_{1}\left(\tfrac{1}{2}T\right) + v_{2}\left(\tfrac{1}{2}T\right)$, so
> $$
> \bar{v}_{\text{(a)}} = \frac{L}{T} = \frac{v_{1} + v_{2}}{2}.
> $$
> - (b) $T = \dfrac{L/2}{v_{1}} + \dfrac{L/2}{v_{2}} = \dfrac{L(v_{1} + v_{2})}{2v_{1}v_{2}}$, so
> $$
> \bar{v}_{\text{(b)}} = \frac{L}{T} = \frac{2v_{1}v_{2}}{v_{1} + v_{2}}.
> $$
> - (c) The difference is
> $$
> \frac{v_{1} + v_{2}}{2} - \frac{2v_{1}v_{2}}{v_{1} + v_{2}} = \frac{(v_{1} + v_{2})^{2} - 4v_{1}v_{2}}{2(v_{1} + v_{2})} = \frac{(v_{1} - v_{2})^{2}}{2(v_{1} + v_{2})} \ge 0,
> $$
> so the average speed is greater in case (a), half the time at each speed, unless $v_{1} = v_{2}$.
>
> **Assess.** With equal distances the object spends more time at the lower speed, which pulls the average down. Numbers: $50\ \mathrm{km/h}$ and $100\ \mathrm{km/h}$ give $75\ \mathrm{km/h}$ in (a) and $67\ \mathrm{km/h}$ in (b). If $v_{2} \to 0$, case (b) gives zero, as it must: the second half takes forever.

### EUP 2.85
Question: [[PHY1 Ch02 Questions#EUP 2.85|EUP 2.85]]

> [!solution] Solution
> **Interpret.** A leap is free fall: up to height $h$ and back down. We compare the time spent above $\tfrac{1}{2}h$ with the total time in the air.
>
> **Develop.** The rise and the fall are symmetric, so it is enough to look at the fall from the peak, which starts from rest. Falling a distance $d$ from rest takes $t = \sqrt{2d/g}$, from $d = \tfrac{1}{2}gt^{2}$.
>
> **Evaluate.** Falling from the peak, the upper half is the first $\tfrac{1}{2}h$ and the whole fall is $h$:
> $$
> t_{\text{upper}} = \sqrt{\frac{2\left(\tfrac{1}{2}h\right)}{g}} = \sqrt{\frac{h}{g}}, \qquad t_{\text{fall}} = \sqrt{\frac{2h}{g}}, \qquad \frac{t_{\text{upper}}}{t_{\text{fall}}} = \frac{1}{\sqrt{2}} \approx 0.71.
> $$
> The same fraction holds on the way up, so $71\%$ of the time in the air is spent in the upper half.
>
> **Assess.** The leaper is slowest near the top, so most of the time goes to the upper half of the height. The answer does not depend on $h$ or on $g$.

### EUP 2.86
Question: [[PHY1 Ch02 Questions#EUP 2.86|EUP 2.86]]

> [!solution] Solution
> **Interpret.** The balloon is dropped from rest at an unknown height $H$ above the top of the window. It is already moving when it reaches the window.
>
> **Develop.** Take downward positive. Across the window, (2.10) with $\Delta y = 1.3\ \mathrm{m}$ and $t = 0.22\ \mathrm{s}$ gives the speed $v_{\mathrm{t}}$ at the top of the window; then (2.11) from the release point, where the speed is zero, gives $H$.
>
> **Evaluate.**
> $$
> \begin{aligned}
> \Delta y = v_{\mathrm{t}}t + \tfrac{1}{2}gt^{2} &\implies v_{\mathrm{t}} = \frac{\Delta y}{t} - \tfrac{1}{2}gt = \frac{1.3\ \mathrm{m}}{0.22\ \mathrm{s}} - \tfrac{1}{2}(9.8\ \mathrm{m/s^2})(0.22\ \mathrm{s}) = 4.83\ \mathrm{m/s}, \\
> v_{\mathrm{t}}^{2} = 2gH &\implies H = \frac{v_{\mathrm{t}}^{2}}{2g} = \frac{(4.83\ \mathrm{m/s})^{2}}{2(9.8\ \mathrm{m/s^2})} = 1.2\ \mathrm{m}.
> \end{aligned}
> $$
>
> **Assess.** The average speed across the window is $1.3\ \mathrm{m}/0.22\ \mathrm{s} = 5.9\ \mathrm{m/s}$, and the speed at the top must be less than that; it is. Using $\Delta y = \tfrac{1}{2}gt^{2}$ across the window would be wrong, because the balloon does not start from rest there.

### EUP 2.88
Question: [[PHY1 Ch02 Questions#EUP 2.88|EUP 2.88]]

> [!solution] Solution
> **Interpret.** The acceleration changes with time, so the equations of Table 2.1 do not apply.
>
> **Develop.** Integrate: $v(t) = \int a(t)\,dt$ (2.12) and $x(t) = \int v(t)\,dt$ (2.13). The initial conditions $v(0) = v_{0}$ and $x(0) = x_{0}$ fix the constants of integration.
>
> **Evaluate.**
> - (a)
> $$
> v(t) = \int (a_{0} + bt)\,dt = a_{0}t + \tfrac{1}{2}bt^{2} + C_{1}, \qquad v(0) = v_{0} \implies C_{1} = v_{0},
> $$
> so $v(t) = v_{0} + a_{0}t + \tfrac{1}{2}bt^{2}$.
> - (b)
> $$
> x(t) = \int \left(v_{0} + a_{0}t + \tfrac{1}{2}bt^{2}\right)dt = v_{0}t + \tfrac{1}{2}a_{0}t^{2} + \tfrac{1}{6}bt^{3} + C_{2}, \qquad x(0) = x_{0} \implies C_{2} = x_{0},
> $$
> so $x(t) = x_{0} + v_{0}t + \tfrac{1}{2}a_{0}t^{2} + \tfrac{1}{6}bt^{3}$.
>
> **Assess.** With $b = 0$ these reduce to (2.7) and (2.10), the constant-acceleration results, which is EUP 2.93. Differentiating $x(t)$ twice returns $a_{0} + bt$. The constant $b$ has units $\mathrm{m/s^3}$.

### EUP 2.91
Question: [[PHY1 Ch02 Questions#EUP 2.91|EUP 2.91]]

> [!solution] Solution
> **Interpret.** Each drop falls from rest through $19.6\ \mathrm{cm}$. Drops leave the faucet at equal time intervals, and we want the number of drops per second.
>
> **Develop.** The fall time follows from $h = \tfrac{1}{2}gt^{2}$. At the instant described there are four drops: one leaving, two on the way, and one landing. Four drops in a row are separated by three time intervals, so the fall time is three intervals.
>
> **Evaluate.**
> $$
> t_{\text{fall}} = \sqrt{\frac{2h}{g}} = \sqrt{\frac{2(0.196\ \mathrm{m})}{9.8\ \mathrm{m/s^2}}} = 0.200\ \mathrm{s}, \qquad \Delta t = \frac{t_{\text{fall}}}{3} = 0.0667\ \mathrm{s}.
> $$
> The rate is $1/\Delta t = 15$ drops per second.
>
> **Assess.** The count is of intervals, not drops: dividing the fall time by four would give $20$ per second. The two drops in the air are not equally spaced in height, since they are $2.2\ \mathrm{cm}$ and $8.7\ \mathrm{cm}$ below the faucet, but they are equally spaced in time.

### EUP 2.95
Question: [[PHY1 Ch02 Questions#EUP 2.95|EUP 2.95]]

> [!solution] Solution
> **Interpret.** The velocity is given as a function of time; the acceleration is not constant. We need the position to find when the object returns, and the acceleration at that time.
>
> **Develop.** Integrate the velocity for the position (2.13), with $x(0) = 0$; differentiate it for the acceleration (2.5).
>
> **Evaluate.**
> - (a)
> $$
> x(t) = \int_{0}^{t} \left(bt' - ct'^{3}\right)dt' = \tfrac{1}{2}bt^{2} - \tfrac{1}{4}ct^{4} = \tfrac{1}{4}t^{2}\left(2b - ct^{2}\right).
> $$
> This is zero at $t = 0$ and again at $t = \sqrt{\dfrac{2b}{c}}$.
> - (b)
> $$
> a = \frac{dv}{dt} = b - 3ct^{2}, \qquad a\left(\sqrt{2b/c}\right) = b - 3c\left(\frac{2b}{c}\right) = -5b.
> $$
>
> **Assess.** With $b$ in $\mathrm{m/s^2}$ and $c$ in $\mathrm{m/s^4}$, $\sqrt{b/c}$ is in seconds and $-5b$ in $\mathrm{m/s^2}$. The velocity at that time is $bt - ct^{3} = t(b - 2b) = -bt$, negative: the object is on its way back through the origin, with a negative acceleration.

### EUP 2.96
Question: [[PHY1 Ch02 Questions#EUP 2.96|EUP 2.96]]

> [!solution] Solution
> **Interpret.** The acceleration is positive and dies away exponentially. Take $a_{0} > 0$ and $b > 0$. The object starts from rest at the origin.
>
> **Develop.** Integrate twice, (2.12) and (2.13), with $v(0) = 0$ and $x(0) = 0$, and look at the limits as $t \to \infty$.
>
> **Evaluate.**
> - (a)
> $$
> v(t) = \int_{0}^{t} a_{0}e^{-bt'}\,dt' = \frac{a_{0}}{b}\left(1 - e^{-bt}\right).
> $$
> - (b) No. The acceleration is always positive, so the speed keeps increasing, but it never exceeds $a_{0}/b$: as $t \to \infty$, $e^{-bt} \to 0$ and $v \to \dfrac{a_{0}}{b}$.
> - (c) Yes.
> $$
> x(t) = \int_{0}^{t} \frac{a_{0}}{b}\left(1 - e^{-bt'}\right)dt' = \frac{a_{0}}{b}\,t - \frac{a_{0}}{b^{2}}\left(1 - e^{-bt}\right),
> $$
> which grows without bound, because the velocity approaches a nonzero constant.
>
> **Assess.** $b$ has units $\mathrm{s^{-1}}$, so $a_{0}/b$ is a velocity. For small $t$, $1 - e^{-bt} \approx bt$ and $v \approx a_{0}t$, the constant-acceleration result. For large $t$ the motion is at constant velocity $a_{0}/b$, a distance $a_{0}/b^{2}$ behind where it would be had it moved at that velocity from the start.

### EUP 2.97
Question: [[PHY1 Ch02 Questions#EUP 2.97|EUP 2.97]]

> [!solution] Solution
> **Interpret.** Two objects in free fall, released at the same instant on the same vertical line. They collide when their heights are equal, and "in mid-air" means that this happens above the ground.
>
> **Develop.** Take $y = 0$ at the ground and upward positive. With (2.10) and $a = -g$ for both,
> $$
> y_{1} = h_{0} - \tfrac{1}{2}gt^{2}, \qquad y_{2} = v_{0}t - \tfrac{1}{2}gt^{2}.
> $$
>
> **Evaluate.** Setting $y_{1} = y_{2}$, the terms $\tfrac{1}{2}gt^{2}$ cancel:
> $$
> h_{0} = v_{0}t \implies t = \frac{h_{0}}{v_{0}}.
> $$
> - (b) The height of the collision is
> $$
> y = h_{0} - \tfrac{1}{2}g\left(\frac{h_{0}}{v_{0}}\right)^{2} = h_{0} - \frac{gh_{0}^{2}}{2v_{0}^{2}}.
> $$
> - (a) The collision is in mid-air if $y > 0$:
> $$
> h_{0} > \frac{gh_{0}^{2}}{2v_{0}^{2}} \implies v_{0} > \sqrt{\frac{gh_{0}}{2}}.
> $$
>
> **Assess.** Both balls have the same acceleration, so relative to each other they move at the constant velocity $v_{0}$ and close the distance $h_{0}$ in the time $h_{0}/v_{0}$, whatever $g$ is. As $v_{0} \to \infty$ the collision is at $h_{0}$, at once. If $v_{0}$ is smaller than the limit, the second ball is back on the ground, after a flight of $2v_{0}/g$, before the first ball can reach it.

## EUP Chapter 2 Passage Problems

### EUP 2.98 to 2.102
Question: [[PHY1 Ch02 Questions#EUP 2.98 to 2.102|EUP 2.98 to 2.102]]

> [!solution] Solution
> **Interpret.** The graph shows velocity against time. The value of the curve is the velocity, and its slope is the acceleration (2.5).
>
> **Develop.** Not moving means $v = 0$: the curve is on the time axis. Not accelerating means zero slope: a peak or a valley of the curve. Speed is $\lvert v \rvert$, the distance of the curve from the axis. The position increases while $v > 0$ and decreases while $v < 0$.
>
> **Evaluate.**
> - **2.98** b. The curve is on the axis at A, E, and H.
> - **2.99** c. The slope is zero at the maximum C and at the minimum F.
> - **2.100** b. The curve is farthest from the axis at C; the minimum at F is smaller in magnitude.
> - **2.101** c. Of the four choices, the curve is steepest at D, where the velocity is falling quickly. At C and F the acceleration is zero.
> - **2.102** b. The velocity is positive from A to E, so the tiger moves to the right all that time and is farthest from its start at E. After E it moves back to the left.
>
> **Assess.** The answers to 2.98 and 2.99 are different sets of points: zero velocity and zero acceleration are different things. In 2.102 the tiger does not get farther away on the left than it was on the right at E, because the area between the curve and the axis from E to H is smaller than the area from A to E. The answers to 2.100 and 2.101 are read off the shape of the curve; check them against Fig. 2.16 in the book.
