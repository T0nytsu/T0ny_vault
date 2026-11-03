---
course: [PHY1]
semester: "115-1"
chapter: ["9.1", "9.2", "9.3", "9.4", "9.5", "9.6"]
tags: [physics, homework, solutions, momentum]
source:
  - "Own solutions; every number recomputed with Python, symbolic results with sympy"
  - "EUP Ch. 9 (pp. 166-190), scanned PDF: equations and answers to GOT IT? questions"
  - "[[PHY1 Ch09 Fig 9.6.png]]"
  - "[[PHY1 Ch09 Fig 9.24.png]]"
  - "[[PHY1 Ch09 Fig 9.26.png]]"
  - "[[PHY1 Ch09 Fig 9.27.png]]"
  - "[[PHY1 Ch09 Fig 9.28.png]]"
  - "[[PHY1 Ch09 Fig 9.30.png]]"
  - "[[PHY1 Ch09 Problem 9.92 fit.png]]"
created: 2026-10-21
questions: "[[PHY1 HW Ch09 Questions]]"
up: "[[PHY1 Index]]"
format: "physics-notes 1.1"
---
> [!note] Notation
> - Equation numbers are the book's: center of mass $\vec{r}_{\mathrm{cm}} = \sum m_{i}\vec{r}_{i}/M$ (9.2) and $\vec{r}_{\mathrm{cm}} = \int \vec{r}\,dm/M$ (9.4); $\vec{P} = M\vec{v}_{\mathrm{cm}}$ (9.5), for constant $M$; $\vec{F}_{\mathrm{net\,ext}} = d\vec{P}/dt$ (9.6); $\vec{P}$ constant (9.7), **only when the net external force is zero** (or negligible during a brief collision); $K = K_{\mathrm{cm}} + K_{\mathrm{int}}$ (9.9).
> - Impulse: $\Delta\vec{p} = \bar{\vec{F}}\Delta t$ (9.10a), $\Delta\vec{p} = \vec{J} = \int \vec{F}\,dt$ (9.10b), for the net force.
> - Totally inelastic: $m_{1}\vec{v}_{1} + m_{2}\vec{v}_{2} = (m_{1} + m_{2})\vec{v}_{\mathrm{f}}$ (9.11). Elastic: momentum (9.12) and kinetic energy (9.13); in one dimension $m_{1}(v_{\mathrm{1i}} - v_{\mathrm{1f}}) = m_{2}(v_{\mathrm{2f}} - v_{\mathrm{2i}})$ (9.12b), $v_{\mathrm{1i}} - v_{\mathrm{2i}} = v_{\mathrm{2f}} - v_{\mathrm{1f}}$ (9.14), the final velocities (9.15a) and (9.15b), and $K_{2}/K_{1} = 4m_{1}m_{2}/(m_{1} + m_{2})^{2}$ (9.16), **for $m_{2}$ initially at rest**.
> - In one-dimensional collisions $v$ is a velocity component along the stated positive direction. $g = 9.8\ \mathrm{m/s^2}$; $9.80\ \mathrm{m/s^2}$ in the KSU and SIU problems. Intermediate values keep one extra figure.

## Answer Key

| Problem | Answer |
| --- | --- |
| [[PHY1 HW Ch09 Questions#EUP 9.11\|EUP 9.11]] | $2m$ |
| [[PHY1 HW Ch09 Questions#EUP 9.41\|EUP 9.41]] | On the symmetry axis, $\dfrac{a}{12\tan 36^{\circ}} \approx 0.115a$ from the pentagon's center, away from the missing triangle |
| [[PHY1 HW Ch09 Questions#EUP 9.86\|EUP 9.86]] | $\dfrac{2R}{\pi} \approx 0.64R$ |
| [[PHY1 HW Ch09 Questions#EUP 9.91\|EUP 9.91]] | (a) $\dfrac{M}{1 + a}$; (b) $\dfrac{1 + a}{2 + a}L$; (c) yes: $M$ and $\tfrac{1}{2}L$ |
| [[PHY1 HW Ch09 Questions#EUP 9.45\|EUP 9.45]] | The mouse has $\tfrac{1}{4}$ the bowl's mass |
| [[PHY1 HW Ch09 Questions#EUP 9.59\|EUP 9.59]] | $9.0\ \mathrm{m/s}$ to the right, relative to the cart |
| [[PHY1 HW Ch09 Questions#EUP 9.63\|EUP 9.63]] | (a) $37.7^{\circ}$ or $52.3^{\circ}$; (b) $0.657\ \mathrm{m/s}$ or $0.508\ \mathrm{m/s}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.65\|EUP 9.65]] | $6.1\ \mathrm{s}$ after the explosion |
| [[PHY1 HW Ch09 Questions#EUP 9.54\|EUP 9.54]] | $(2.1\hat{\imath} - 1.5\hat{\jmath}) \times 10^{5}\ \mathrm{m/s}$: $2.6 \times 10^{5}\ \mathrm{m/s}$ at $36^{\circ}$ below the $x$-axis |
| [[PHY1 HW Ch09 Questions#EUP 9.57\|EUP 9.57]] | $(4.0\hat{\imath} + 2.8\hat{\jmath})\ \mathrm{m/s}$: $4.9\ \mathrm{m/s}$ at $35^{\circ}$ counterclockwise from the $x$-axis |
| [[PHY1 HW Ch09 Questions#EUP 9.20\|EUP 9.20]] | $3$ |
| [[PHY1 HW Ch09 Questions#EUP 9.43\|EUP 9.43]] | $K_{\mathrm{cm}} = 1.74\ \mathrm{J}$; $K_{\mathrm{int}} = 32.8\ \mathrm{J}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.22\|EUP 9.22]] | (a) $2.2 \times 10^{-4}\ \mathrm{N}$; (b) $2.6 \times 10^{-7}\ \mathrm{N \cdot s}$; (c) $2.6 \times 10^{-7}\ \mathrm{kg \cdot m/s}$; all upward |
| [[PHY1 HW Ch09 Questions#EUP 9.60\|EUP 9.60]] | $2.9 \times 10^{-3}\ \mathrm{N}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.68\|EUP 9.68]] | $J = 17\ \mathrm{N \cdot s}$: yes |
| [[PHY1 HW Ch09 Questions#EUP 9.92\|EUP 9.92]] | $h$ versus $(J/m)^{2}$; slope $0.0443\ \mathrm{s^2/m}$; $g \approx 11\ \mathrm{m/s^2}$, too large because of air resistance |
| [[PHY1 HW Ch09 Questions#EUP 9.24\|EUP 9.24]] | (a) $5.4\ \mathrm{mi/h}$; (b) $13\%$ |
| [[PHY1 HW Ch09 Questions#EUP 9.26\|EUP 9.26]] | $(10.9\hat{\imath} + 26.7\hat{\jmath})\ \mathrm{Mm/s}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.71\|EUP 9.71]] | $120^{\circ}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.49\|EUP 9.49]] | (a) $0.99\ \mathrm{m}$; (b) $3.9\ \mathrm{m/s}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.69\|EUP 9.69]] | Leaf at the limit: SUV $76\ \mathrm{km/h}$; SUV at the limit: Leaf $92\ \mathrm{km/h}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.88\|EUP 9.88]] | $0.30\ \mathrm{J}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.29\|EUP 9.29]] | $48\ \mathrm{m/s}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.72\|EUP 9.72]] | $4.00\ \mathrm{u}$; $1.08\ \mathrm{Mm/s}$ in the proton's initial direction |
| [[PHY1 HW Ch09 Questions#EUP 9.81\|EUP 9.81]] | $\tfrac{1}{8}v$ and $\tfrac{7}{8}v$, both forward |
| [[PHY1 HW Ch09 Questions#EUP 9.74\|EUP 9.74]] | $A$: $\tfrac{1}{3}v$ to the left; $B$: $\tfrac{2}{9}v$ and $C$: $\tfrac{8}{9}v$ to the right |
| [[PHY1 HW Ch09 Questions#EUP 9.80\|EUP 9.80]] | $9h$ |
| [[PHY1 HW Ch09 Questions#EUP 9.82\|EUP 9.82]] | $8.0\ \mathrm{s}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.76\|EUP 9.76]] | Proof |
| [[PHY1 HW Ch09 Questions#EUP 9.78\|EUP 9.78]] | $-\tfrac{1}{5}v_{0}\hat{\imath}$; $\tfrac{3}{5}v_{0}\hat{\imath} \pm \tfrac{\sqrt{3}}{5}v_{0}\hat{\jmath}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.94 to 9.97\|EUP 9.94 to 9.97]] | c, b, b, a |
| [[PHY1 HW Ch09 Questions#KSU 3.6 to 3.8\|KSU 3.6 to 3.8]] | T, T, F |
| [[PHY1 HW Ch09 Questions#KSU 3.9\|KSU 3.9]] | a) $12.0\ \mathrm{m/s}$ east; b) $1.1 \times 10^{3}\ \mathrm{N}$ east |
| [[PHY1 HW Ch09 Questions#KSU 3.10\|KSU 3.10]] | a) $17\ \mathrm{m/s}$; b) $18\ \mathrm{m}$ |
| [[PHY1 HW Ch09 Questions#KSU 4.1\|KSU 4.1]] | c |
| [[PHY1 HW Ch09 Questions#KSU 4.4 to 4.6\|KSU 4.4 to 4.6]] | F, F, F |
| [[PHY1 HW Ch09 Questions#KSU 4.7\|KSU 4.7]] | a) $28\ \mathrm{m/s}$; b) $4.6 \times 10^{2}\ \mathrm{N}$ |
| [[PHY1 HW Ch09 Questions#SIU 3.6\|SIU 3.6]] | $245\ \mathrm{m/s}$ |
| [[PHY1 HW Ch09 Questions#SIU 3.7\|SIU 3.7]] | $0.67\ \mathrm{m}$ |

## Center of Mass of Discrete Particles

### EUP 9.11
Question: [[PHY1 HW Ch09 Questions#EUP 9.11|EUP 9.11]]

> [!solution] Solution
> Take $y = 0$ on the base, the third vertex at height $h$ with mass $m_{3}$. By (9.2),
> $$
> y_{\mathrm{cm}} = \frac{m(0) + m(0) + m_{3}h}{2m + m_{3}} = \frac{h}{2} \implies 2m_{3} = 2m + m_{3} \implies m_{3} = 2m.
> $$

### EUP 9.41
Question: [[PHY1 HW Ch09 Questions#EUP 9.41|EUP 9.41]]

![EUP Figure 9.24|300](../Attachments/PHY1%20Ch09%20Fig%209.24.png)

> [!solution] Solution
> Split the whole pentagon into five equal triangles with apexes at its center $O$. Each has height $r = \dfrac{a}{2\tan 36^{\circ}}$ (from $O$ to the middle of a side), and by Example 9.3 its center of mass lies $\tfrac{2}{3}r$ from $O$. Take $y$ along the symmetry axis, away from the missing triangle; let $m$ be the mass of one triangle. The whole pentagon has its center of mass at $O$, so by (9.2)
> $$
> 5m(0) = 4m\,y_{\mathrm{cm}} + m\left(-\tfrac{2}{3}r\right) \implies y_{\mathrm{cm}} = \frac{r}{6} = \frac{a}{12\tan 36^{\circ}} = 0.115a.
> $$
> The center of mass is on the symmetry axis, $0.115a$ from the pentagon's center, on the side away from the missing triangle.

## Center of Mass by Integration

### EUP 9.86
Question: [[PHY1 HW Ch09 Questions#EUP 9.86|EUP 9.86]]

![EUP Figure 9.6|400](../Attachments/PHY1%20Ch09%20Fig%209.6.png)

> [!solution] Solution
> Origin at the center of the semicircle, $y$ upward. The wire between $\theta$ and $\theta + d\theta$ has $y = R\sin\theta$ and $dm = \dfrac{M}{\pi R}R\,d\theta = \dfrac{M}{\pi}d\theta$. By (9.4),
> $$
> y_{\mathrm{cm}} = \frac{1}{M}\int y\,dm = \frac{1}{\pi}\int_{0}^{\pi} R\sin\theta\,d\theta = \frac{2R}{\pi} = 0.64R.
> $$
> By symmetry $x_{\mathrm{cm}} = 0$: the center of mass is $2R/\pi$ above the center (point A).

### EUP 9.91
Question: [[PHY1 HW Ch09 Questions#EUP 9.91|EUP 9.91]]

> [!solution] Solution
> **(a)**
> $$
> m = \int_{0}^{L} \mu\,dx = \frac{M}{L^{1+a}}\int_{0}^{L} x^{a}\,dx = \frac{M}{L^{1+a}} \cdot \frac{L^{1+a}}{1 + a} = \frac{M}{1 + a}.
> $$
> **(b)** By (9.4),
> $$
> x_{\mathrm{cm}} = \frac{1}{m}\int_{0}^{L} x\mu\,dx = \frac{1 + a}{M} \cdot \frac{M}{L^{1+a}} \cdot \frac{L^{2+a}}{2 + a} = \frac{1 + a}{2 + a}L.
> $$
> **(c)** For $a = 0$: $m = M$ and $x_{\mathrm{cm}} = \tfrac{1}{2}L$, as expected for a uniform rod.

## Center of Mass That Stays Put

### EUP 9.45
Question: [[PHY1 HW Ch09 Questions#EUP 9.45|EUP 9.45]]

> [!solution] Solution
> The counter exerts no horizontal force and the mouse lands with no horizontal velocity, so the horizontal position of the center of mass of mouse and bowl stays fixed. Relative to the bowl the mouse moves $\tfrac{1}{2}D$ (rim to bottom); the bowl moves $\tfrac{1}{10}D$ the other way, so relative to the counter the mouse moves $\tfrac{1}{2}D - \tfrac{1}{10}D = \tfrac{2}{5}D$. By (9.2), $\Delta x_{\mathrm{cm}} = 0$:
> $$
> m\left(\tfrac{2}{5}D\right) - M\left(\tfrac{1}{10}D\right) = 0 \implies \frac{m}{M} = \frac{1}{4}.
> $$

> [!warning] Ground displacements
> The mouse's $\tfrac{1}{2}D$ is relative to the bowl; the center of mass equation needs displacements relative to the counter.

## Momentum Conservation in One Dimension

### EUP 9.59
Question: [[PHY1 HW Ch09 Questions#EUP 9.59|EUP 9.59]]

> [!solution] Solution
> Take $+x$ to the right. No horizontal external force acts on sprinter and cart, so by (9.7), with her final velocity $0$ relative to the ground,
> $$
> (55\ \mathrm{kg} + 180\ \mathrm{kg})(-6.9\ \mathrm{m/s}) = (180\ \mathrm{kg})v_{\mathrm{c}} \implies v_{\mathrm{c}} = -9.01\ \mathrm{m/s}.
> $$
> Her velocity relative to the cart: $0 - (-9.01\ \mathrm{m/s}) = 9.0\ \mathrm{m/s}$, to the right.

> [!warning] Relative velocity
> Momentum conservation takes velocities relative to the ground; the speed relative to the cart comes only at the end.

### EUP 9.63
Question: [[PHY1 HW Ch09 Questions#EUP 9.63|EUP 9.63]]

> [!solution] Solution
> Take $+x$ along the toss; the rock ($m = 4.50\ \mathrm{kg}$) leaves at $v_{0} = 12.0\ \mathrm{m/s}$ at angle $\theta$ and lands at the height it was thrown from. The ice exerts no horizontal force, so by (9.7) you ($M = 65.0\ \mathrm{kg}$) recoil at $V = \dfrac{m}{M}v_{0}\cos\theta$. The rock is in the air for $t = \dfrac{2v_{0}\sin\theta}{g}$, and the separation grows at $v_{0}\cos\theta + V$:
> $$
> d = \left(1 + \frac{m}{M}\right)v_{0}\cos\theta \cdot \frac{2v_{0}\sin\theta}{g} = \left(1 + \frac{m}{M}\right)\frac{v_{0}^{2}\sin 2\theta}{g}
> $$
> $$
> \sin 2\theta = \frac{gd}{(1 + m/M)v_{0}^{2}} = \frac{(9.8\ \mathrm{m/s^2})(15.2\ \mathrm{m})}{(1.0692)(12.0\ \mathrm{m/s})^{2}} = 0.9675.
> $$
> **(a)** $2\theta = 75.35^{\circ}$ or $104.65^{\circ}$: $\theta = 37.7^{\circ}$ or $52.3^{\circ}$.
>
> **(b)** $V = \dfrac{4.50\ \mathrm{kg}}{65.0\ \mathrm{kg}}(12.0\ \mathrm{m/s})\cos\theta = 0.657\ \mathrm{m/s}$ for $37.7^{\circ}$, or $0.508\ \mathrm{m/s}$ for $52.3^{\circ}$.

> [!warning] Separation from a moving thrower
> The $15.2\ \mathrm{m}$ is measured from you, and you slide backward while the rock flies; both angles are answers.

### EUP 9.65
Question: [[PHY1 HW Ch09 Questions#EUP 9.65|EUP 9.65]]

> [!solution] Solution
> Take $y$ upward from the ground. The peak is at $H = \dfrac{v_{0}^{2}}{2g} = \dfrac{(40\ \mathrm{m/s})^{2}}{2(9.8\ \mathrm{m/s^2})} = 81.6\ \mathrm{m}$, where the rocket is momentarily at rest; by (9.7) the equal-mass fragments leave with opposite vertical velocities. For the first fragment, $0 = H + u_{1}t_{1} - \tfrac{1}{2}gt_{1}^{2}$ with $t_{1} = 2.75\ \mathrm{s}$:
> $$
> u_{1} = \frac{\tfrac{1}{2}gt_{1}^{2} - H}{t_{1}} = \frac{37.06\ \mathrm{m} - 81.63\ \mathrm{m}}{2.75\ \mathrm{s}} = -16.21\ \mathrm{m/s}.
> $$
> The second leaves upward at $u_{2} = +16.21\ \mathrm{m/s}$, returns to the explosion point after $2u_{2}/g$ moving down at $16.21\ \mathrm{m/s}$, and then falls exactly like the first:
> $$
> t_{2} = t_{1} + \frac{2u_{2}}{g} = 2.75\ \mathrm{s} + \frac{2(16.21\ \mathrm{m/s})}{9.8\ \mathrm{m/s^2}} = 6.1\ \mathrm{s} \text{ after the explosion.}
> $$

> [!warning] Not the same fall time
> Opposite velocities do not mean equal times: the upward fragment first rises and comes back.

## Momentum Conservation in Two Dimensions

### EUP 9.54
Question: [[PHY1 HW Ch09 Questions#EUP 9.54|EUP 9.54]]

> [!solution] Solution
> Masses in $\mathrm{u}$ (only ratios matter): $238$, $4$, $234$. By (9.7), $238\,\vec{v}_{\mathrm{U}} = 4\,\vec{v}_{\alpha} + 234\,\vec{v}_{\mathrm{Th}}$:
> $$
> \begin{aligned}
> v_{\mathrm{Th},x} &= \frac{238(4.1 \times 10^{5}\ \mathrm{m/s}) - 4(1.5 \times 10^{7}\ \mathrm{m/s})\cos 36^{\circ}}{234} = 2.1 \times 10^{5}\ \mathrm{m/s}, \\
> v_{\mathrm{Th},y} &= -\frac{4(1.5 \times 10^{7}\ \mathrm{m/s})\sin 36^{\circ}}{234} = -1.5 \times 10^{5}\ \mathrm{m/s}.
> \end{aligned}
> $$
> $\vec{v}_{\mathrm{Th}} = (2.1\hat{\imath} - 1.5\hat{\jmath}) \times 10^{5}\ \mathrm{m/s}$: $2.6 \times 10^{5}\ \mathrm{m/s}$ at $36^{\circ}$ below the $x$-axis.

> [!warning] Moving parent
> The uranium is moving, so the momenta after the decay add up to $238\,\vec{v}_{\mathrm{U}}$, not to $\vec{0}$.

### EUP 9.57
Question: [[PHY1 HW Ch09 Questions#EUP 9.57|EUP 9.57]]

> [!solution] Solution
> Everything starts at rest, so by (9.7) the camera's momentum is $\vec{p}_{\mathrm{c}} = -(\vec{p}_{\mathrm{t}} + \vec{p}_{\mathrm{a}})$, with
> $$
> \begin{aligned}
> \vec{p}_{\mathrm{t}} &= (18\ \mathrm{kg})(1.1\ \mathrm{m/s})\hat{\imath} = 19.8\hat{\imath}\ \mathrm{kg \cdot m/s}, \\
> \vec{p}_{\mathrm{a}} &= (67\ \mathrm{kg})(0.66\ \mathrm{m/s})(\cos 200^{\circ}\hat{\imath} + \sin 200^{\circ}\hat{\jmath}) = (-41.55\hat{\imath} - 15.12\hat{\jmath})\ \mathrm{kg \cdot m/s}.
> \end{aligned}
> $$
> $$
> \vec{v}_{\mathrm{c}} = \frac{(21.75\hat{\imath} + 15.12\hat{\jmath})\ \mathrm{kg \cdot m/s}}{5.4\ \mathrm{kg}} = (4.0\hat{\imath} + 2.8\hat{\jmath})\ \mathrm{m/s},
> $$
> that is, $4.9\ \mathrm{m/s}$ at $35^{\circ}$ counterclockwise from the $x$-axis.

## Kinetic Energy of a System

### EUP 9.20
Question: [[PHY1 HW Ch09 Questions#EUP 9.20|EUP 9.20]]

> [!solution] Solution
> Let the object have mass $M$ and speed $v$, so $K = \tfrac{1}{2}Mv^{2}$. No external force acts in the explosion, so $\vec{v}_{\mathrm{cm}}$ is unchanged and $K_{\mathrm{cm}} = \tfrac{1}{2}Mv^{2} = K$. Afterward every piece moves at $2v$:
> $$
> K_{\mathrm{after}} = \tfrac{1}{2}m_{1}(2v)^{2} + \tfrac{1}{2}m_{2}(2v)^{2} = 4\left(\tfrac{1}{2}Mv^{2}\right) = 4K.
> $$
> By (9.9), $K_{\mathrm{int}} = 4K - K = 3K$, so $\dfrac{K_{\mathrm{int}}}{K_{\mathrm{cm}}} = 3$.

### EUP 9.43
Question: [[PHY1 HW Ch09 Questions#EUP 9.43|EUP 9.43]]

> [!solution] Solution
> Each mass is $m = 0.200\ \mathrm{kg}$; $M = 0.600\ \mathrm{kg}$. By (9.5),
> $$
> \vec{v}_{\mathrm{cm}} = \frac{\vec{v}_{1} + \vec{v}_{2} + \vec{v}_{3}}{3} = \frac{(15.0 - 3.45 - 4.32)\hat{\jmath}\ \mathrm{m/s}}{3} = 2.41\hat{\jmath}\ \mathrm{m/s},
> $$
> so $K_{\mathrm{cm}} = \tfrac{1}{2}Mv_{\mathrm{cm}}^{2} = \tfrac{1}{2}(0.600\ \mathrm{kg})(2.41\ \mathrm{m/s})^{2} = 1.74\ \mathrm{J}$.
> $$
> \begin{aligned}
> K &= \tfrac{1}{2}m\left(v_{1}^{2} + v_{2}^{2} + v_{3}^{2}\right) \\
> &= \tfrac{1}{2}(0.200\ \mathrm{kg})(225 + 56.79 + 63.55)\ \mathrm{m^2/s^2} = 34.53\ \mathrm{J}.
> \end{aligned}
> $$
> By (9.9), $K_{\mathrm{int}} = K - K_{\mathrm{cm}} = 34.53\ \mathrm{J} - 1.74\ \mathrm{J} = 32.8\ \mathrm{J}$.

## Impulse and Average Force

### EUP 9.22
Question: [[PHY1 HW Ch09 Questions#EUP 9.22|EUP 9.22]]

> [!solution] Solution
> Take $y$ upward; $m = 220\ \mathrm{\mu g} = 2.20 \times 10^{-7}\ \mathrm{kg}$, $\bar{a} = 100g$, $\Delta t = 1.2 \times 10^{-3}\ \mathrm{s}$. Newton's second law for the flea: $\bar{F} - mg = m\bar{a}$.
> - (a) $\bar{F} = m(\bar{a} + g) = 101mg = 101(2.20 \times 10^{-7}\ \mathrm{kg})(9.8\ \mathrm{m/s^2}) = 2.2 \times 10^{-4}\ \mathrm{N}$, upward.
> - (b) $J = \bar{F}\Delta t = (2.18 \times 10^{-4}\ \mathrm{N})(1.2 \times 10^{-3}\ \mathrm{s}) = 2.6 \times 10^{-7}\ \mathrm{N \cdot s}$, upward.
> - (c) By (9.10a) with the net force, $\Delta p = m\bar{a}\Delta t = 100mg\,\Delta t = 2.6 \times 10^{-7}\ \mathrm{kg \cdot m/s}$, upward.

> [!warning] Ground force versus net force
> The momentum change comes from the net force $\bar{F} - mg$; the ground's impulse is $1\%$ larger, which disappears in rounding only because $\bar{a} \gg g$.

### EUP 9.60
Question: [[PHY1 HW Ch09 Questions#EUP 9.60|EUP 9.60]]

> [!solution] Solution
> Each mound lands with no horizontal velocity and must be brought to the belt's speed $v = 0.52\ \mathrm{m/s}$. By (9.6), the force is the rate at which horizontal momentum is given to the dough:
> $$
> \bar{F} = \frac{\Delta m}{\Delta t}v = \frac{0.011\ \mathrm{kg}}{2\ \mathrm{s}}(0.52\ \mathrm{m/s}) = 2.9 \times 10^{-3}\ \mathrm{N}.
> $$

### EUP 9.68
Question: [[PHY1 HW Ch09 Questions#EUP 9.68|EUP 9.68]]

> [!solution] Solution
> By (9.10b),
> $$
> \begin{aligned}
> J &= \int_{0}^{\Delta t} at(t - \Delta t)\,dt = a\left(\frac{\Delta t^{3}}{3} - \frac{\Delta t^{3}}{2}\right) = -\frac{a\,\Delta t^{3}}{6} \\
> &= -\frac{(-4.6\ \mathrm{N/s^2})(2.8\ \mathrm{s})^{3}}{6} = 17\ \mathrm{N \cdot s}.
> \end{aligned}
> $$
> $10\ \mathrm{N \cdot s} < J < 20\ \mathrm{N \cdot s}$: the rocket meets its specs.

### EUP 9.92
Question: [[PHY1 HW Ch09 Questions#EUP 9.92|EUP 9.92]]

> [!solution] Solution
> The motor's impulse gives the rocket its momentum, $J = mv_{0}$ (9.10b), and the rocket then rises freely, so by (2.11) $h = \dfrac{v_{0}^{2}}{2g} = \dfrac{1}{2g}\left(\dfrac{J}{m}\right)^{2}$. Plot $h$ versus $(J/m)^{2}$: a straight line through the origin with slope $\dfrac{1}{2g}$.
>
> | $(J/m)^{2}$ ($\mathrm{m^2/s^2}$) | 625 | 259 | 370 | 1111 | 514 |
> | --- | --- | --- | --- | --- | --- |
> | $h$ ($\mathrm{m}$) | 22 | 13 | 19 | 51 | 23 |
>
> The best-fit line through the origin has slope $0.0443\ \mathrm{s^2/m}$, so $g = \dfrac{1}{2(0.0443\ \mathrm{s^2/m})} = 11\ \mathrm{m/s^2}$.
>
> Air resistance lowers every maximum height, so the slope comes out too small and $g$ too large (here by about $15\%$).
>
> ![EUP 9.92 fit|480](../Attachments/PHY1%20Ch09%20Problem%209.92%20fit.png)

## Totally Inelastic Collisions

### EUP 9.24
Question: [[PHY1 HW Ch09 Questions#EUP 9.24|EUP 9.24]]

> [!solution] Solution
> Take $+x$ along the motion. Tons and $\mathrm{mi/h}$ appear only in ratios, so no conversion is needed.
>
> **(a)** By (9.11),
> $$
> v_{\mathrm{f}} = \frac{m_{1}v_{1} + m_{2}v_{2}}{m_{1} + m_{2}} = \frac{(56\ \mathrm{ton})(7.0\ \mathrm{mi/h}) + (31\ \mathrm{ton})(2.6\ \mathrm{mi/h})}{87\ \mathrm{ton}} = 5.4\ \mathrm{mi/h}.
> $$
> **(b)**
> $$
> \frac{K_{\mathrm{i}} - K_{\mathrm{f}}}{K_{\mathrm{i}}} = 1 - \frac{(m_{1} + m_{2})v_{\mathrm{f}}^{2}}{m_{1}v_{1}^{2} + m_{2}v_{2}^{2}} = 1 - \frac{(87)(5.43)^{2}}{(56)(7.0)^{2} + (31)(2.6)^{2}} = 0.13
> $$
> $13\%$ of the kinetic energy was lost.

### EUP 9.26
Question: [[PHY1 HW Ch09 Questions#EUP 9.26|EUP 9.26]]

> [!solution] Solution
> By (9.11), $m_{\mathrm{n}}\vec{v}_{\mathrm{n}} + m_{\mathrm{d}}\vec{v}_{\mathrm{d}} = m_{\mathrm{t}}\vec{v}_{\mathrm{t}}$, masses in $\mathrm{u}$:
> $$
> \begin{aligned}
> \vec{v}_{\mathrm{d}} &= \frac{m_{\mathrm{t}}\vec{v}_{\mathrm{t}} - m_{\mathrm{n}}\vec{v}_{\mathrm{n}}}{m_{\mathrm{d}}} = \frac{3.02(15.1\hat{\imath} + 22.6\hat{\jmath}) - 1.01(23.5\hat{\imath} + 14.4\hat{\jmath})}{2.01}\ \mathrm{Mm/s} \\
> &= (10.9\hat{\imath} + 26.7\hat{\jmath})\ \mathrm{Mm/s}.
> \end{aligned}
> $$

### EUP 9.71
Question: [[PHY1 HW Ch09 Questions#EUP 9.71|EUP 9.71]]

> [!solution] Solution
> Each object has mass $m$ and speed $v$; let $\varphi$ be the angle between the velocities. By (9.11), $m\vec{v}_{1} + m\vec{v}_{2} = 2m\vec{v}_{\mathrm{f}}$ with $v_{\mathrm{f}} = \tfrac{1}{2}v$, so $\lvert \vec{v}_{1} + \vec{v}_{2} \rvert = v$:
> $$
> \lvert \vec{v}_{1} + \vec{v}_{2} \rvert^{2} = v^{2} + v^{2} + 2v^{2}\cos\varphi = v^{2} \implies \cos\varphi = -\tfrac{1}{2} \implies \varphi = 120^{\circ}.
> $$

## Collision Followed by Another Process

### EUP 9.49
Question: [[PHY1 HW Ch09 Questions#EUP 9.49|EUP 9.49]]

> [!solution] Solution
> **Coupling** (brief, so the spring does not act yet), by (9.11):
> $$
> V = \frac{m_{2}v_{2}}{m_{1} + m_{2}} = \frac{(9400\ \mathrm{kg})(8.5\ \mathrm{m/s})}{20{,}400\ \mathrm{kg}} = 3.92\ \mathrm{m/s}.
> $$
> **Compression** (mechanical energy conserved): $\tfrac{1}{2}(m_{1} + m_{2})V^{2} = \tfrac{1}{2}kx^{2}$.
>
> **(a)**
> $$
> x = V\sqrt{\frac{m_{1} + m_{2}}{k}} = (3.92\ \mathrm{m/s})\sqrt{\frac{20{,}400\ \mathrm{kg}}{0.32 \times 10^{6}\ \mathrm{N/m}}} = 0.99\ \mathrm{m}.
> $$
> **(b)** The spring gives all the energy back: $3.9\ \mathrm{m/s}$, away from the bumper.

> [!warning] Two stages
> Kinetic energy is not conserved in the coupling: use momentum for the collision and energy only for the spring.

### EUP 9.69
Question: [[PHY1 HW Ch09 Questions#EUP 9.69|EUP 9.69]]

> [!solution] Solution
> **Skid**: the wreckage ($M = 4860\ \mathrm{kg}$) stops when friction has removed its kinetic energy, $\mu_{\mathrm{k}}Mgd = \tfrac{1}{2}MV^{2}$:
> $$
> V = \sqrt{2\mu_{\mathrm{k}}gd} = \sqrt{2(0.697)(9.8\ \mathrm{m/s^2})(17.6\ \mathrm{m})} = 15.51\ \mathrm{m/s},
> $$
> so $P = MV = 7.536 \times 10^{4}\ \mathrm{kg \cdot m/s}$.
> **Collision**, by (9.11): the two momenta are perpendicular, so $p_{\mathrm{L}}^{2} + p_{\mathrm{S}}^{2} = P^{2}$. The limit is $70\ \mathrm{km/h} = 19.44\ \mathrm{m/s}$.
> - Leaf at the limit: $p_{\mathrm{L}} = 3.189 \times 10^{4}\ \mathrm{kg \cdot m/s}$, so $p_{\mathrm{S}} = \sqrt{P^{2} - p_{\mathrm{L}}^{2}} = 6.828 \times 10^{4}\ \mathrm{kg \cdot m/s}$ and $v_{\mathrm{S}} = 21.2\ \mathrm{m/s} = 76\ \mathrm{km/h}$.
> - SUV at the limit: $p_{\mathrm{S}} = 6.261 \times 10^{4}\ \mathrm{kg \cdot m/s}$, so $p_{\mathrm{L}} = 4.194 \times 10^{4}\ \mathrm{kg \cdot m/s}$ and $v_{\mathrm{L}} = 25.6\ \mathrm{m/s} = 92\ \mathrm{km/h}$.
>
> Either way the other car was above $70\ \mathrm{km/h}$, so at least one car exceeded the limit.

### EUP 9.88
Question: [[PHY1 HW Ch09 Questions#EUP 9.88|EUP 9.88]]

> [!solution] Solution
> Pellet $m = 0.52 \times 10^{-3}\ \mathrm{kg}$, block $M = 0.400\ \mathrm{kg}$. **Swing** (mechanical energy): the block leaves at $V = \sqrt{2gh} = \sqrt{2(9.8\ \mathrm{m/s^2})(0.52 \times 10^{-3}\ \mathrm{m})} = 0.1010\ \mathrm{m/s}$. **Passage** (momentum, (9.7)), with $v_{0} = \sqrt{2K_{0}/m} = 111.8\ \mathrm{m/s}$: $mv_{0} = mv + MV$, so
> $$
> \begin{aligned}
> v &= v_{0} - \frac{M}{m}V \\
> &= 111.8\ \mathrm{m/s} - \frac{0.400\ \mathrm{kg}}{0.52 \times 10^{-3}\ \mathrm{kg}}(0.1010\ \mathrm{m/s}) = 34.1\ \mathrm{m/s}.
> \end{aligned}
> $$
> $$
> K = \tfrac{1}{2}mv^{2} = \tfrac{1}{2}(0.52 \times 10^{-3}\ \mathrm{kg})(34.1\ \mathrm{m/s})^{2} = 0.30\ \mathrm{J}.
> $$

> [!warning] Not totally inelastic
> The pellet keeps going, so Example 9.9's $mv = (m + M)V$ does not apply: pellet and block end with different velocities.

## One-Dimensional Elastic Collisions

### EUP 9.29
Question: [[PHY1 HW Ch09 Questions#EUP 9.29|EUP 9.29]]

> [!solution] Solution
> Take $+x$ toward the car. The car is so much more massive that its velocity $v_{2} = -15\ \mathrm{m/s}$ does not change. By (9.14), $v_{\mathrm{1i}} - v_{2} = v_{2} - v_{\mathrm{1f}}$:
> $$
> v_{\mathrm{1f}} = 2v_{2} - v_{\mathrm{1i}} = 2(-15\ \mathrm{m/s}) - 18\ \mathrm{m/s} = -48\ \mathrm{m/s}.
> $$
> The ball comes back at $48\ \mathrm{m/s}$.

> [!warning] Moving wall
> The ball does not just reverse its $18\ \mathrm{m/s}$: relative to the car it arrives at $33\ \mathrm{m/s}$ and leaves at $33\ \mathrm{m/s}$.

### EUP 9.72
Question: [[PHY1 HW Ch09 Questions#EUP 9.72|EUP 9.72]]

> [!solution] Solution
> Take $+x$ along the proton's initial velocity: $v_{\mathrm{1i}} = 6.90\ \mathrm{Mm/s}$, $v_{\mathrm{2i}} = -2.80\ \mathrm{Mm/s}$, $v_{\mathrm{1f}} = -8.62\ \mathrm{Mm/s}$. By (9.14),
> $$
> v_{\mathrm{2f}} = v_{\mathrm{1i}} - v_{\mathrm{2i}} + v_{\mathrm{1f}} = (6.90 + 2.80 - 8.62)\ \mathrm{Mm/s} = 1.08\ \mathrm{Mm/s}.
> $$
> By (9.12b),
> $$
> m_{2} = m_{1}\frac{v_{\mathrm{1i}} - v_{\mathrm{1f}}}{v_{\mathrm{2f}} - v_{\mathrm{2i}}} = (1\ \mathrm{u})\frac{(6.90 + 8.62)\ \mathrm{Mm/s}}{(1.08 + 2.80)\ \mathrm{Mm/s}} = 4.00\ \mathrm{u}.
> $$
> The second particle has mass $4.00\ \mathrm{u}$ and moves at $1.08\ \mathrm{Mm/s}$ in the proton's initial direction.

### EUP 9.81
Question: [[PHY1 HW Ch09 Questions#EUP 9.81|EUP 9.81]]

> [!solution] Solution
> Equal masses; take $+x$ along $v$. Momentum (9.7) and the energy that is left give
> $$
> v_{1} + v_{2} = v, \qquad v_{1}^{2} + v_{2}^{2} = \left(1 - \tfrac{7}{32}\right)v^{2} = \tfrac{25}{32}v^{2}.
> $$
> Squaring the first, $2v_{1}v_{2} = v^{2} - \tfrac{25}{32}v^{2} = \tfrac{7}{32}v^{2}$, so $v_{1}$ and $v_{2}$ are the roots of $u^{2} - vu + \tfrac{7}{64}v^{2} = 0$: $u = \tfrac{1}{8}v$ or $\tfrac{7}{8}v$. The struck car must end up in front, moving faster:
> $$
> v_{1} = \tfrac{1}{8}v, \qquad v_{2} = \tfrac{7}{8}v \quad \text{(both in the original direction).}
> $$

> [!warning] Two roots
> $v_{1} = \tfrac{7}{8}v$, $v_{2} = \tfrac{1}{8}v$ would put the first car through the second.

## Successive Collisions

### EUP 9.74
Question: [[PHY1 HW Ch09 Questions#EUP 9.74|EUP 9.74]]

![EUP Figure 9.26|400](../Attachments/PHY1%20Ch09%20Fig%209.26.png)

> [!solution] Solution
> Take $+x$ to the right. Each collision is elastic with the struck block at rest, so (9.15) with $v_{\mathrm{2i}} = 0$ applies.
> - $A$ ($m$) hits $B$ ($2m$): $v_{A} = \dfrac{m - 2m}{3m}v = -\tfrac{1}{3}v$, $v_{B} = \dfrac{2m}{3m}v = \tfrac{2}{3}v$.
> - $B$ ($2m$) hits $C$ ($m$): $v_{B}' = \dfrac{2m - m}{3m}\left(\tfrac{2}{3}v\right) = \tfrac{2}{9}v$, $v_{C} = \dfrac{2(2m)}{3m}\left(\tfrac{2}{3}v\right) = \tfrac{8}{9}v$.
>
> $A$ moves left and $v_{B}' < v_{C}$, so there are no more collisions: $A$ at $\tfrac{1}{3}v$ to the left, $B$ at $\tfrac{2}{9}v$ and $C$ at $\tfrac{8}{9}v$ to the right.

> [!warning] Check for more collisions
> After each collision compare the velocities: the blocks stop colliding only when no block is catching up with another.

### EUP 9.80
Question: [[PHY1 HW Ch09 Questions#EUP 9.80|EUP 9.80]]

> [!solution] Solution
> Take $y$ upward. Both balls reach the floor at speed $v = \sqrt{2gh}$. The large ball rebounds elastically from the floor with $+v$ and then meets the small ball, still moving at $-v$. By (9.15a), with the small ball as object 1 and $M \gg m$,
> $$
> v_{\mathrm{1f}} = \frac{m - M}{m + M}(-v) + \frac{2M}{m + M}(+v) \approx v + 2v = 3v.
> $$
> The small ball rises to $\dfrac{(3v)^{2}}{2g} = 9\dfrac{v^{2}}{2g} = 9h$.

### EUP 9.82
Question: [[PHY1 HW Ch09 Questions#EUP 9.82|EUP 9.82]]

![EUP Figure 9.28|420](../Attachments/PHY1%20Ch09%20Fig%209.28.png)

> [!solution] Solution
> At the bottom of the incline the $200$-g block has $v_{0} = \sqrt{2gh} = \sqrt{2(9.8\ \mathrm{m/s^2})(0.25\ \mathrm{m})} = 2.214\ \mathrm{m/s}$. By (9.15) with $m_{1} = 0.2\ \mathrm{kg}$, $m_{2} = 0.8\ \mathrm{kg}$:
> $$
> \begin{aligned}
> v_{1} &= \frac{m_{1} - m_{2}}{m_{1} + m_{2}}v_{0} = -\tfrac{3}{5}v_{0} = -1.328\ \mathrm{m/s}, \\
> v_{2} &= \frac{2m_{1}}{m_{1} + m_{2}}v_{0} = \tfrac{2}{5}v_{0} = 0.885\ \mathrm{m/s}.
> \end{aligned}
> $$
> Block 1 goes back $d = 1.4\ \mathrm{m}$ in $t_{a} = d/\lvert v_{1} \rvert = 1.054\ \mathrm{s}$, goes up the incline and back with acceleration $g\sin 30^{\circ}$ in $t_{b} = \dfrac{2\lvert v_{1} \rvert}{g\sin 30^{\circ}} = 0.542\ \mathrm{s}$, and leaves the bottom at $T_{0} = 1.596\ \mathrm{s}$ with speed $1.328\ \mathrm{m/s}$. Block 2 is then $d + v_{2}T_{0} = 2.813\ \mathrm{m}$ from the bottom, and block 1 gains on it at $\lvert v_{1} \rvert - v_{2} = 0.443\ \mathrm{m/s}$:
> $$
> T = T_{0} + \frac{2.813\ \mathrm{m}}{0.443\ \mathrm{m/s}} = 1.596\ \mathrm{s} + 6.35\ \mathrm{s} = 8.0\ \mathrm{s}.
> $$

## Two-Dimensional Elastic Collisions

### EUP 9.76
Question: [[PHY1 HW Ch09 Questions#EUP 9.76|EUP 9.76]]

> [!solution] Solution
> The equal masses cancel from (9.12) and (9.13), and $\vec{v}_{\mathrm{2i}} = \vec{0}$:
> $$
> \vec{v}_{\mathrm{1i}} = \vec{v}_{\mathrm{1f}} + \vec{v}_{\mathrm{2f}}, \qquad v_{\mathrm{1i}}^{2} = v_{\mathrm{1f}}^{2} + v_{\mathrm{2f}}^{2}.
> $$
> The dot product of the first equation with itself gives $v_{\mathrm{1i}}^{2} = v_{\mathrm{1f}}^{2} + v_{\mathrm{2f}}^{2} + 2\vec{v}_{\mathrm{1f}} \cdot \vec{v}_{\mathrm{2f}}$, so $\vec{v}_{\mathrm{1f}} \cdot \vec{v}_{\mathrm{2f}} = 0$. The collision isn't head-on, so neither final velocity is zero: they are perpendicular.

### EUP 9.78
Question: [[PHY1 HW Ch09 Questions#EUP 9.78|EUP 9.78]]

![EUP Figure 9.27|330](../Attachments/PHY1%20Ch09%20Fig%209.27.png)

> [!solution] Solution
> At contact the three centers form an equilateral triangle, so the contact forces, along the lines of centers, push ball 2 at $+30^{\circ}$ and ball 11 at $-30^{\circ}$ from the $x$-axis. By symmetry both leave with the same speed $u$, and the incident ball stays on the $x$-axis with velocity $v_{1}$. By (9.12) and (9.13), with the equal masses canceled:
> $$
> v_{0} = v_{1} + 2u\cos 30^{\circ} = v_{1} + \sqrt{3}u, \qquad v_{0}^{2} = v_{1}^{2} + 2u^{2}.
> $$
> With $u = (v_{0} - v_{1})/\sqrt{3}$: $v_{0}^{2} - v_{1}^{2} = \tfrac{2}{3}(v_{0} - v_{1})^{2}$, so $v_{0} + v_{1} = \tfrac{2}{3}(v_{0} - v_{1})$, $v_{1} = -\tfrac{1}{5}v_{0}$, and $u = \dfrac{2\sqrt{3}}{5}v_{0}$ (the other root, $v_{1} = v_{0}$, is no collision).
> $$
> \vec{v}_{1} = -\tfrac{1}{5}v_{0}\hat{\imath}, \qquad \vec{v}_{2} = \tfrac{3}{5}v_{0}\hat{\imath} + \tfrac{\sqrt{3}}{5}v_{0}\hat{\jmath}, \qquad \vec{v}_{11} = \tfrac{3}{5}v_{0}\hat{\imath} - \tfrac{\sqrt{3}}{5}v_{0}\hat{\jmath}.
> $$

## Passage Problems

### EUP 9.94 to 9.97
Question: [[PHY1 HW Ch09 Questions#EUP 9.94 to 9.97|EUP 9.94 to 9.97]]

![EUP Figure 9.30|480](../Attachments/PHY1%20Ch09%20Fig%209.30.png)

> [!solution] Solution
> - **94.** c. The ball bounces back up, but lower each time.
> - **95.** b. At a peak the mechanical energy is almost all $mgh$, since the horizontal speed hardly changes. The peak after the second collision is about $0.6$ of the height of the one before it, so roughly $40\%$ is lost.
> - **96.** b. The images keep about the same horizontal spacing; the vertical velocity reverses and shrinks.
> - **97.** a. The ball is at the floor only briefly compared with its long arcs.

## Problems from Other Universities' Exams

### KSU 3.6 to 3.8
Question: [[PHY1 HW Ch09 Questions#KSU 3.6 to 3.8|KSU 3.6 to 3.8]]

> [!solution] Solution
> - **6.** T. The impulse of the net force equals the change in momentum (9.10b).
> - **7.** T. For a given impulse, $\bar{F} = J/\Delta t$ (9.10a): the longer the time, the smaller the average force.
> - **8.** F. Momentum is conserved in every collision; an inelastic collision loses kinetic energy.

### KSU 3.9
Question: [[PHY1 HW Ch09 Questions#KSU 3.9|KSU 3.9]]

> [!solution] Solution
> Take $+x$ east; $m = 0.160\ \mathrm{kg}$. In a one-dimensional elastic collision of equal masses the velocities are exchanged ((9.15) with $m_{1} = m_{2}$).
>
> **(a)** The 2-ball moves at $12.0\ \mathrm{m/s}$, east.
>
> **(b)** By (9.10a), on the 2-ball:
> $$
> \bar{F} = \frac{m\,\Delta v}{\Delta t} = \frac{(0.160\ \mathrm{kg})[12.0\ \mathrm{m/s} - (-4.5\ \mathrm{m/s})]}{2.5 \times 10^{-3}\ \mathrm{s}} = 1.1 \times 10^{3}\ \mathrm{N}, \text{ east.}
> $$

### KSU 3.10
Question: [[PHY1 HW Ch09 Questions#KSU 3.10|KSU 3.10]]

> [!solution] Solution
> Take $x$ east, $y$ north. By (9.11),
> $$
> \begin{aligned}
> \vec{P} &= (1800\ \mathrm{kg})(18.0\ \mathrm{m/s})\hat{\imath} + (3200\ \mathrm{kg})(24\ \mathrm{m/s})\hat{\jmath} \\
> &= (3.24\hat{\imath} + 7.68\hat{\jmath}) \times 10^{4}\ \mathrm{kg \cdot m/s}.
> \end{aligned}
> $$
> **(a)** $V = \dfrac{P}{M} = \dfrac{8.34 \times 10^{4}\ \mathrm{kg \cdot m/s}}{5000\ \mathrm{kg}} = 16.7\ \mathrm{m/s} \approx 17\ \mathrm{m/s}$, at $67^{\circ}$ north of east.
>
> **(b)** Friction removes the kinetic energy, $\mu_{\mathrm{k}}Mgd = \tfrac{1}{2}MV^{2}$:
> $$
> d = \frac{V^{2}}{2\mu_{\mathrm{k}}g} = \frac{(16.67\ \mathrm{m/s})^{2}}{2(0.80)(9.80\ \mathrm{m/s^2})} = 18\ \mathrm{m}.
> $$

### KSU 4.1
Question: [[PHY1 HW Ch09 Questions#KSU 4.1|KSU 4.1]]

> [!solution] Solution
> c. No external force acts on rocket and gas, so by (9.7) their momentum changes are equal in magnitude and opposite in direction.

### KSU 4.4 to 4.6
Question: [[PHY1 HW Ch09 Questions#KSU 4.4 to 4.6|KSU 4.4 to 4.6]]

> [!solution] Solution
> - **4.** F. Impulse is the average force times the time interval, $\vec{J} = \bar{\vec{F}}\Delta t$ (9.10a), a vector.
> - **5.** F. By the work–energy theorem $\bar{F}d = \tfrac{1}{2}mv^{2}$: a shorter stopping distance needs a larger average force.
> - **6.** F. A completely inelastic collision conserves momentum (9.11); only kinetic energy is lost.

### KSU 4.7
Question: [[PHY1 HW Ch09 Questions#KSU 4.7|KSU 4.7]]

> [!solution] Solution
> Take $+x$ along the medicine ball's velocity; $m_{1} = 5.0\ \mathrm{kg}$, $m_{2} = 0.62\ \mathrm{kg}$, $v_{\mathrm{2i}} = 0$.
>
> **(a)** By (9.15b),
> $$
> v_{\mathrm{2f}} = \frac{2m_{1}}{m_{1} + m_{2}}v_{\mathrm{1i}} = \frac{2(5.0\ \mathrm{kg})}{5.62\ \mathrm{kg}}(16.0\ \mathrm{m/s}) = 28\ \mathrm{m/s}.
> $$
> **(b)** By (9.10a),
> $$
> \bar{F} = \frac{m_{2}\,\Delta v_{2}}{\Delta t} = \frac{(0.62\ \mathrm{kg})(28.47\ \mathrm{m/s})}{38 \times 10^{-3}\ \mathrm{s}} = 4.6 \times 10^{2}\ \mathrm{N}.
> $$

### SIU 3.6
Question: [[PHY1 HW Ch09 Questions#SIU 3.6|SIU 3.6]]

> [!solution] Solution
> **Collision** (momentum, (9.11)): $m_{1}v = (m_{1} + m_{2})V$. **Rise** (mechanical energy): $\tfrac{1}{2}(m_{1} + m_{2})V^{2} = (m_{1} + m_{2})gh$, so $V = \sqrt{2gh}$.
> $$
> v = \frac{m_{1} + m_{2}}{m_{1}}\sqrt{2gh} = \frac{3.030\ \mathrm{kg}}{0.03000\ \mathrm{kg}}\sqrt{2(9.80\ \mathrm{m/s^2})(0.300\ \mathrm{m})} = 245\ \mathrm{m/s}.
> $$

### SIU 3.7
Question: [[PHY1 HW Ch09 Questions#SIU 3.7|SIU 3.7]]

> [!solution] Solution
> Here $\rho(x) = bx$ is the mass per unit length, so $dm = bx\,dx$. By (9.4),
> $$
> x_{\mathrm{cm}} = \frac{\int_{0}^{L} x(bx)\,dx}{\int_{0}^{L} bx\,dx} = \frac{bL^{3}/3}{bL^{2}/2} = \frac{2}{3}L = 0.67\ \mathrm{m}.
> $$
> This is EUP 9.91 with $a = 1$.
