---
course: [CAL1]
semester: "115-1"
chapter: ["2.7"]
tags: [calculus, homework, questions, derivatives]
source:
  - "Stewart, Calculus, §2.7 Exercises, pp. 181-184, scanned PDF"
  - "The graph of Exercise 7 is redrawn from the scan"
created: 2026-11-10
solutions: "[[CAL1 HW 2.7 Solutions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> ST §2.7: 3, 7, 17, 21, 23, 33. These are the exercises assigned for Section 2.7. ST is Stewart, *Calculus*.

## ST §2.7 Rates of Change in the Natural and Social Sciences

### ST 2.7.3
**1–4** A particle moves according to a law of motion $s = f(t)$, $t \ge 0$, where $t$ is measured in seconds and $s$ in meters.
- (a) Find the velocity at time $t$.
- (b) What is the velocity after 1 second?
- (c) When is the particle at rest?
- (d) When is the particle moving in the positive direction?
- (e) Find the total distance traveled during the first 6 seconds.
- (f) Draw a diagram like Figure 2 to illustrate the motion of the particle.
- (g) Find the acceleration at time $t$ and after 1 second.
- (h) Graph the position, velocity, and acceleration functions for $0 \le t \le 6$.
- (i) When is the particle speeding up? When is it slowing down?

$$
f(t) = \sin(\pi t/2)
$$

> [!note] Note
> Figure 2 of the book (p. 174, Example 1) is a schematic sketch of the motion: the path of the particle drawn back and forth above the $s$-axis, with the time and the position marked at the start and at every turning point. Part (h) carries the book's graphing-device icon.

### ST 2.7.7
Suppose that the graph of the velocity function of a particle is as shown in the figure, where $t$ is measured in seconds. When is the particle traveling forward (in the positive direction)? When is it traveling backward? What is happening when $5 < t < 7$?

![ST 2.7.7 figure|400](../Attachments/CAL1%20HW%202.7%20Questions%20fig%207.png)

> [!note] Note
> The printed figure labels the axes $x$ and $y$. By the statement, the horizontal axis is the time $t$ and the vertical axis is the velocity.

### ST 2.7.17
A spherical balloon is being inflated. Find the rate of increase of the surface area ($S = 4\pi r^2$) with respect to the radius $r$ when $r$ is (a) 20 cm, (b) 40 cm, and (c) 60 cm. What conclusion can you make?

### ST 2.7.21
The quantity of charge $Q$ in coulombs (C) that has passed through a point in a wire up to time $t$ (measured in seconds) is given by $Q(t) = t^3 - 2t^2 + 6t + 2$. Find the current when (a) $t = 0.5$ s and (b) $t = 1$ s. (See Example 3. The unit of current is an ampere [1 A = 1 C/s].) At what time is the current lowest?

### ST 2.7.23
The force $F$ acting on a body with mass $m$ and velocity $v$ is the rate of change of momentum: $F = (d/dt)(mv)$. If $m$ is constant, this becomes $F = ma$, where $a = dv/dt$ is the acceleration. But in the theory of relativity, the mass of a particle varies with $v$ as follows: $m = m_0/\sqrt{1 - v^2/c^2}$ where $m_0$ is the mass of the particle at rest and $c$ is the speed of light. Show that
$$
F = \frac{m_0 a}{(1 - v^2/c^2)^{3/2}}
$$

### ST 2.7.33
If $p(x)$ is the total value of the production when there are $x$ workers in a plant, then the *average productivity* of the workforce at the plant is
$$
A(x) = \frac{p(x)}{x}
$$
- (a) Find $A'(x)$. Why does the company want to hire more workers if $A'(x) > 0$?
- (b) Show that $A'(x) > 0$ if $p'(x)$ is greater than the average productivity.
