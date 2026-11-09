---
course: [CAL1]
semester: "115-1"
chapter: ["2.8"]
tags: [calculus, homework, solutions, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §2.8, pp. 185-188, scanned PDF (related rates, problem-solving strategy)"
created: 2026-11-08
questions: "[[CAL1 HW 2.8 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 2.8 Questions#ST 2.8.1\|ST 2.8.1]] | (a) $\frac{dV}{dt} = 3x^{2}\frac{dx}{dt}$; (b) 2700 cm³/s |
| [[CAL1 HW 2.8 Questions#ST 2.8.3\|ST 2.8.3]] | 48 cm²/s |
| [[CAL1 HW 2.8 Questions#ST 2.8.5\|ST 2.8.5]] | $128\pi \approx 402$ cm²/min |
| [[CAL1 HW 2.8 Questions#ST 2.8.7\|ST 2.8.7]] | $\frac{3}{25\pi} \approx 0.038$ m/min |
| [[CAL1 HW 2.8 Questions#ST 2.8.9\|ST 2.8.9]] | (a) $-\tfrac{3}{8}$; (b) $\tfrac{8}{3}$ |
| [[CAL1 HW 2.8 Questions#ST 2.8.15\|ST 2.8.15]] | 2.25 m/s |
| [[CAL1 HW 2.8 Questions#ST 2.8.17\|ST 2.8.17]] | 78 km/h |
| [[CAL1 HW 2.8 Questions#ST 2.8.19\|ST 2.8.19]] | $\approx 2.79$ m/s |
| [[CAL1 HW 2.8 Questions#ST 2.8.20\|ST 2.8.20]] | (a) decreasing at $\tfrac{3\sqrt{5}}{2} \approx 3.35$ m/s; (b) increasing at $\tfrac{3\sqrt{5}}{2} \approx 3.35$ m/s |
| [[CAL1 HW 2.8 Questions#ST 2.8.21\|ST 2.8.21]] | $-1.6$ cm/min (the base decreases) |
| [[CAL1 HW 2.8 Questions#ST 2.8.27\|ST 2.8.27]] | $\tfrac{1}{30}$ m/min $\approx 3.3$ cm/min |
| [[CAL1 HW 2.8 Questions#ST 2.8.29\|ST 2.8.29]] | $\frac{4}{3\pi} \approx 0.42$ m/min |
| [[CAL1 HW 2.8 Questions#ST 2.8.31\|ST 2.8.31]] | $150\sqrt{3} \approx 260$ cm²/min |
| [[CAL1 HW 2.8 Questions#ST 2.8.37\|ST 2.8.37]] | 80 cm³/min |
| [[CAL1 HW 2.8 Questions#ST 2.8.39\|ST 2.8.39]] | $\frac{107}{810} \approx 0.132\ \Omega/\text{s}$ |
| [[CAL1 HW 2.8 Questions#ST 2.8.41\|ST 2.8.41]] | $20\sqrt{19} \approx 87.2$ km/h |
| [[CAL1 HW 2.8 Questions#ST 2.8.43\|ST 2.8.43]] | $\frac{\pi}{3\sqrt{7}} \approx 0.396$ m/min |
| [[CAL1 HW 2.8 Questions#ST 2.8.47\|ST 2.8.47]] | $\frac{10\pi}{9} \approx 3.49$ km/min $\approx 209$ km/h |
| [[CAL1 HW 2.8 Questions#ST 2.8.49\|ST 2.8.49]] | $\frac{1650}{\sqrt{31}} \approx 296$ km/h |

## ST §2.8 Related Rates

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Related Rates]]**, Stewart's strategy: (1) name every quantity that changes with time $t$ and draw a picture; (2) write the given rates and the unknown rate as derivatives; (3) write an equation that relates the quantities and holds at *every* time $t$; (4) differentiate both sides with respect to $t$ ([[Chain Rule]]); (5) only then substitute the values at the instant asked.
> - **Never substitute a changing quantity before differentiating**: it would become a constant with derivative $0$. Only quantities that stay fixed (the radius of the tank in Exercise 7, the angle $60^{\circ}$ in Exercise 41) may be substituted early.
> - **Signs**: a quantity that decreases has a negative derivative. "Decreasing at a rate of 80" means the derivative is $-80$; the answer then names the positive number 80.
> - **Geometry used**: the Pythagorean Theorem, similar triangles, $V = \tfrac{4}{3}\pi r^{3}$ and $S = 4\pi r^{2}$ for a sphere, $V = \tfrac{1}{3}\pi r^{2}h$ for a cone, and the Law of Cosines $c^{2} = a^{2} + b^{2} - 2ab\cos\theta$. Angles go in radians before differentiating $\sin$ or $\cos$.
> - Each answer is written as on an exam paper: the variables, the equation, its derivative, the values at the instant, then a Hence line with units. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 2.8.1
Question: [[CAL1 HW 2.8 Questions#ST 2.8.1|ST 2.8.1]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{(a) } V = x^{3} \implies \frac{dV}{dt} = 3x^{2}\frac{dx}{dt} && \text{(Chain Rule)} \\
> &\text{(b) } \frac{dx}{dt} = 4,\ x = 15: \ \frac{dV}{dt} = 3 \cdot 15^{2} \cdot 4 = 2700
> \end{aligned}
> $$
> Hence (a) $\dfrac{dV}{dt} = 3x^{2}\dfrac{dx}{dt}$; (b) the volume increases at 2700 cm³/s.
>
> \# $V$ depends on $x$ and $x$ depends on $t$, so $\dfrac{dV}{dt} = \dfrac{dV}{dx} \cdot \dfrac{dx}{dt}$.

### ST 2.8.3
Question: [[CAL1 HW 2.8 Questions#ST 2.8.3|ST 2.8.3]]

> [!solution] Solution
> $$
> \begin{aligned}
> &s = \text{side},\ A = s^{2},\ \frac{ds}{dt} = 6 \\
> &\frac{dA}{dt} = 2s\frac{ds}{dt} \\
> &A = 16 \implies s = 4: \ \frac{dA}{dt} = 2 \cdot 4 \cdot 6 = 48
> \end{aligned}
> $$
> Hence the area increases at 48 cm²/s.
>
> \# The data give the area, not the side: turn $A = 16$ into $s = 4$ before substituting.

### ST 2.8.5
Question: [[CAL1 HW 2.8 Questions#ST 2.8.5|ST 2.8.5]]

> [!solution] Solution
> $$
> \begin{aligned}
> &S = 4\pi r^{2} \implies \frac{dS}{dt} = 8\pi r\frac{dr}{dt} \\
> &r = 8,\ \frac{dr}{dt} = 2: \ \frac{dS}{dt} = 8\pi \cdot 8 \cdot 2 = 128\pi \approx 402
> \end{aligned}
> $$
> Hence the surface area increases at $128\pi \approx 402$ cm²/min.

### ST 2.8.7
Question: [[CAL1 HW 2.8 Questions#ST 2.8.7|ST 2.8.7]]

> [!solution] Solution
> $$
> \begin{aligned}
> &V = \pi r^{2}h = 25\pi h && (r = 5 \text{ is fixed}) \\
> &\frac{dV}{dt} = 25\pi\frac{dh}{dt} \implies 3 = 25\pi\frac{dh}{dt} \implies \frac{dh}{dt} = \frac{3}{25\pi} \approx 0.038
> \end{aligned}
> $$
> Hence the water level rises at $\dfrac{3}{25\pi} \approx 0.038$ m/min.
>
> \# The radius of the tank never changes, so it may be substituted before differentiating; the height does change. Because the walls are vertical, the rate is the same at every moment.

### ST 2.8.9
Question: [[CAL1 HW 2.8 Questions#ST 2.8.9|ST 2.8.9]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dt}\left(4x^{2} + 9y^{2}\right) = \frac{d}{dt}(25) \implies 8x\frac{dx}{dt} + 18y\frac{dy}{dt} = 0 \\[4pt]
> &\text{(a) } x = 2,\ y = 1,\ \frac{dy}{dt} = \frac{1}{3}: \ 16\frac{dx}{dt} + 18 \cdot \frac{1}{3} = 0 \implies \frac{dx}{dt} = -\frac{6}{16} = -\frac{3}{8} \\
> &\text{(b) } x = -2,\ y = 1,\ \frac{dx}{dt} = 3: \ -16 \cdot 3 + 18\frac{dy}{dt} = 0 \implies \frac{dy}{dt} = \frac{48}{18} = \frac{8}{3}
> \end{aligned}
> $$
> Hence (a) $\dfrac{dx}{dt} = -\dfrac{3}{8}$; (b) $\dfrac{dy}{dt} = \dfrac{8}{3}$.
>
> \# Both points lie on the ellipse: $4 \cdot 4 + 9 \cdot 1 = 25$. This is implicit differentiation with respect to $t$: both $x$ and $y$ get a Chain Rule factor.

### ST 2.8.15
Question: [[CAL1 HW 2.8 Questions#ST 2.8.15|ST 2.8.15]]

> [!solution] Solution
> - (a) Given: the pole is 6 m tall, the man is 2 m tall, and he walks away from the pole at $\dfrac{dx}{dt} = 1.5$ m/s, where $x$ is his distance from the pole.
> - (b) Unknown: $\dfrac{ds}{dt}$ when $x = 10$, where $s$ is the distance from the pole to the tip of his shadow.
> - (c) The picture:
>
> ![ST 2.8.15 figure|440](../Attachments/CAL1%20HW%202.8%20Solutions%20fig%2015.png)
>
> - (d) The ray from the light through the top of his head reaches the ground at the tip, so the two right triangles with the vertex at the tip are similar:
>
> $$
> \frac{6}{s} = \frac{2}{s - x} \implies 6s - 6x = 2s \implies s = \frac{3}{2}x
> $$
> - (e)
>
> $$
> \frac{ds}{dt} = \frac{3}{2}\frac{dx}{dt} = \frac{3}{2} \cdot 1.5 = 2.25
> $$
> Hence the tip of the shadow moves at 2.25 m/s.
>
> \# Since $s$ is proportional to $x$, the rate is the same at every moment, and $x = 10$ is not needed. The tip moves faster than the man; the shadow itself, $s - x = \tfrac{1}{2}x$, grows at 0.75 m/s.

### ST 2.8.17
Question: [[CAL1 HW 2.8 Questions#ST 2.8.17|ST 2.8.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> &x = \text{distance of the westbound car},\ y = \text{of the southbound car},\ z = \text{between them} \\
> &z^{2} = x^{2} + y^{2} \implies 2z\frac{dz}{dt} = 2x\frac{dx}{dt} + 2y\frac{dy}{dt} && \text{(west} \perp \text{south)} \\
> &t = 2: \ x = 72 \cdot 2 = 144,\ y = 30 \cdot 2 = 60,\ z = \sqrt{144^{2} + 60^{2}} = 156 \\
> &\frac{dz}{dt} = \frac{144 \cdot 72 + 60 \cdot 30}{156} = \frac{12168}{156} = 78
> \end{aligned}
> $$
> Hence the distance increases at 78 km/h.
>
> \# $144 : 60 : 156 = 12 : 5 : 13$. In fact $z = \sqrt{(72t)^{2} + (30t)^{2}} = 78t$ for every $t$, so the distance always grows at 78 km/h.

### ST 2.8.19
Question: [[CAL1 HW 2.8 Questions#ST 2.8.19|ST 2.8.19]]

> [!solution] Solution
> $$
> \begin{aligned}
> &y_{1} = \text{distance of the man north of } P,\ y_{2} = \text{distance of the woman south of her start} \\
> &y = y_{1} + y_{2} = \text{north–south gap},\ z = \text{distance between them} \\
> &z^{2} = 200^{2} + y^{2} \implies 2z\frac{dz}{dt} = 2y\frac{dy}{dt},\quad \frac{dy}{dt} = 1.2 + 1.6 = 2.8 \\[4pt]
> &\text{15 min after the woman starts (the man has walked 20 min):} \\
> &y_{1} = 1.2 \cdot 1200 = 1440,\quad y_{2} = 1.6 \cdot 900 = 1440,\quad y = 2880 \\
> &z = \sqrt{200^{2} + 2880^{2}} = \sqrt{8\,334\,400} \approx 2886.9 \\
> &\frac{dz}{dt} = \frac{y}{z}\frac{dy}{dt} = \frac{2880 \cdot 2.8}{2886.9} \approx 2.79
> \end{aligned}
> $$
> Hence the people move apart at about 2.79 m/s.
>
> \# The speeds are in m/s, so the times go into seconds: 20 min = 1200 s, 15 min = 900 s. The east–west distance stays 200 m. At the moment asked both are walking, so the gap grows at $1.2 + 1.6$ m/s. Exactly, $z = 40\sqrt{5209}$ and $\dfrac{dz}{dt} = \dfrac{8064}{40\sqrt{5209}}$.

### ST 2.8.20
Question: [[CAL1 HW 2.8 Questions#ST 2.8.20|ST 2.8.20]]

> [!solution] Solution
> $$
> \begin{aligned}
> &x = \text{distance of the runner from home plate},\ \frac{dx}{dt} = 7.5 \\[4pt]
> &\text{(a) } D = \text{distance to second base: } D^{2} = (18 - x)^{2} + 18^{2} && \text{(right angle at first base)} \\
> &\qquad 2D\frac{dD}{dt} = -2(18 - x)\frac{dx}{dt} \\
> &\qquad x = 9 \implies D = \sqrt{81 + 324} = 9\sqrt{5},\quad \frac{dD}{dt} = -\frac{9 \cdot 7.5}{9\sqrt{5}} = -\frac{7.5}{\sqrt{5}} \approx -3.35 \\[4pt]
> &\text{(b) } E = \text{distance to third base: } E^{2} = x^{2} + 18^{2} && \text{(right angle at home plate)} \\
> &\qquad 2E\frac{dE}{dt} = 2x\frac{dx}{dt} \implies \frac{dE}{dt} = \frac{9 \cdot 7.5}{9\sqrt{5}} = \frac{7.5}{\sqrt{5}} \approx 3.35 && (E = 9\sqrt{5})
> \end{aligned}
> $$
> Hence (a) his distance from second base decreases at $\dfrac{7.5}{\sqrt{5}} = \dfrac{3\sqrt{5}}{2} \approx 3.35$ m/s; (b) his distance from third base increases at $\dfrac{3\sqrt{5}}{2} \approx 3.35$ m/s.
>
> ![ST 2.8.20 figure|380](../Attachments/CAL1%20HW%202.8%20Solutions%20fig%2020.png)
>
> \# The minus sign in (a) says that $D$ is getting smaller; the question asks how fast it decreases, so the answer is the positive number. At the halfway point he is equally far from second and third base ($D = E = 9\sqrt{5}$), so the two rates have the same size.

### ST 2.8.21
Question: [[CAL1 HW 2.8 Questions#ST 2.8.21|ST 2.8.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &A = \tfrac{1}{2}bh \implies \frac{dA}{dt} = \frac{1}{2}\left(\frac{db}{dt}\,h + b\,\frac{dh}{dt}\right) && \text{(Product Rule)} \\
> &h = 10,\ A = 100 \implies b = \frac{2A}{h} = 20 \\
> &2 = \frac{1}{2}\left(10\frac{db}{dt} + 20 \cdot 1\right) \implies 10\frac{db}{dt} = -16 \implies \frac{db}{dt} = -1.6
> \end{aligned}
> $$
> Hence the base is decreasing at 1.6 cm/min.
>
> \# Both $b$ and $h$ change, so $A = \tfrac{1}{2}bh$ needs the Product Rule. The base must be computed from the given area before substituting.

### ST 2.8.27
Question: [[CAL1 HW 2.8 Questions#ST 2.8.27|ST 2.8.27]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{in meters: } h = \text{water depth},\ w = \text{width of the water surface} = 0.3 + h \\
> &V = 10 \cdot \frac{(0.3 + w)\,h}{2} = 10 \cdot \frac{(0.6 + h)\,h}{2} = 3h + 5h^{2} && \text{(trapezoid area} \times \text{length)} \\
> &\frac{dV}{dt} = (3 + 10h)\frac{dh}{dt} \\
> &h = 0.3,\ \frac{dV}{dt} = 0.2: \ 0.2 = 6\frac{dh}{dt} \implies \frac{dh}{dt} = \frac{1}{30} \approx 0.033
> \end{aligned}
> $$
> Hence the water level rises at $\tfrac{1}{30}$ m/min $\approx$ 3.3 cm/min.
>
> \# Work in one unit (meters), because the rate is given in m³/min. The water's cross-section is a smaller trapezoid with bottom 0.3 and top $w$. Each slanted side moves out $\tfrac{0.8 - 0.3}{2} = 0.25$ over the full height $0.5$, that is, $0.5h$ over the depth $h$ (similar triangles), so $w = 0.3 + 2 \cdot 0.5h = 0.3 + h$.

### ST 2.8.29
Question: [[CAL1 HW 2.8 Questions#ST 2.8.29|ST 2.8.29]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{diameter} = \text{height} \implies r = \frac{h}{2} \\
> &V = \frac{1}{3}\pi r^{2}h = \frac{1}{3}\pi\left(\frac{h}{2}\right)^{2}h = \frac{\pi h^{3}}{12} \\
> &\frac{dV}{dt} = \frac{\pi h^{2}}{4}\frac{dh}{dt} \\
> &h = 3,\ \frac{dV}{dt} = 3: \ 3 = \frac{9\pi}{4}\frac{dh}{dt} \implies \frac{dh}{dt} = \frac{4}{3\pi} \approx 0.42
> \end{aligned}
> $$
> Hence the height increases at $\dfrac{4}{3\pi} \approx 0.42$ m/min.
>
> \# Eliminate $r$ first, as in Example 3, so that $V$ depends on $h$ alone; then one differentiation gives $dh/dt$.

### ST 2.8.31
Question: [[CAL1 HW 2.8 Questions#ST 2.8.31|ST 2.8.31]]

> [!solution] Solution
> $$
> \begin{aligned}
> &A = \frac{\sqrt{3}}{4}s^{2} \implies \frac{dA}{dt} = \frac{\sqrt{3}}{2}s\frac{ds}{dt} \\
> &s = 30,\ \frac{ds}{dt} = 10: \ \frac{dA}{dt} = \frac{\sqrt{3}}{2} \cdot 30 \cdot 10 = 150\sqrt{3} \approx 260
> \end{aligned}
> $$
> Hence the area increases at $150\sqrt{3} \approx 260$ cm²/min.
>
> \# The height of an equilateral triangle is $\tfrac{\sqrt{3}}{2}s$, so $A = \tfrac{1}{2} \cdot s \cdot \tfrac{\sqrt{3}}{2}s = \tfrac{\sqrt{3}}{4}s^{2}$.

### ST 2.8.37
Question: [[CAL1 HW 2.8 Questions#ST 2.8.37|ST 2.8.37]]

> [!solution] Solution
> $$
> \begin{aligned}
> &PV = C \implies \frac{dP}{dt}\,V + P\,\frac{dV}{dt} = 0 && \text{(Product Rule)} \\
> &V = 600,\ P = 150,\ \frac{dP}{dt} = 20: \ 20 \cdot 600 + 150\frac{dV}{dt} = 0 \implies \frac{dV}{dt} = -80
> \end{aligned}
> $$
> Hence the volume is decreasing at 80 cm³/min.

### ST 2.8.39
Question: [[CAL1 HW 2.8 Questions#ST 2.8.39|ST 2.8.39]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{1}{R} = \frac{1}{R_{1}} + \frac{1}{R_{2}} \implies -\frac{1}{R^{2}}\frac{dR}{dt} = -\frac{1}{R_{1}^{2}}\frac{dR_{1}}{dt} - \frac{1}{R_{2}^{2}}\frac{dR_{2}}{dt} \\
> &R_{1} = 80,\ R_{2} = 100: \ \frac{1}{R} = \frac{1}{80} + \frac{1}{100} = \frac{9}{400} \implies R = \frac{400}{9} \\
> &\frac{dR}{dt} = R^{2}\left(\frac{0.3}{80^{2}} + \frac{0.2}{100^{2}}\right) = \frac{160000}{81} \cdot \frac{107}{1600000} = \frac{107}{810} \approx 0.132
> \end{aligned}
> $$
> Hence $R$ is increasing at $\dfrac{107}{810} \approx 0.132\ \Omega/\text{s}$.
>
> \# Differentiate $\tfrac{1}{R} = R^{-1}$ by the Chain Rule: $-R^{-2}\,\tfrac{dR}{dt}$; then multiply both sides by $-R^{2}$. Compute $R$ itself before substituting.

### ST 2.8.41
Question: [[CAL1 HW 2.8 Questions#ST 2.8.41|ST 2.8.41]]

> [!solution] Solution
> $$
> \begin{aligned}
> &a, b = \text{distances of the cars from the intersection},\ c = \text{distance between them} \\
> &c^{2} = a^{2} + b^{2} - 2ab\cos 60^{\circ} = a^{2} + b^{2} - ab && \text{(Law of Cosines)} \\
> &2c\frac{dc}{dt} = 2a\frac{da}{dt} + 2b\frac{db}{dt} - \left(\frac{da}{dt}\,b + a\,\frac{db}{dt}\right) \\
> &t = \tfrac{1}{2}: \ a = 30,\ b = 50,\ c = \sqrt{900 + 2500 - 1500} = \sqrt{1900} = 10\sqrt{19} \\
> &\frac{dc}{dt} = \frac{2 \cdot 30 \cdot 60 + 2 \cdot 50 \cdot 100 - (60 \cdot 50 + 30 \cdot 100)}{2 \cdot 10\sqrt{19}} = \frac{7600}{20\sqrt{19}} = 20\sqrt{19} \approx 87.2
> \end{aligned}
> $$
> Hence the distance between the cars increases at $20\sqrt{19} \approx 87.2$ km/h.
>
> \# The angle between the roads stays $60^{\circ}$, so $\cos 60^{\circ} = \tfrac{1}{2}$ may be put in before differentiating; $ab$ needs the Product Rule. As in Exercise 17, the distance is proportional to $t$: $c = \sqrt{3600 + 10000 - 6000}\;t = 20\sqrt{19}\,t$.

### ST 2.8.43
Question: [[CAL1 HW 2.8 Questions#ST 2.8.43|ST 2.8.43]]

> [!solution] Solution
> $$
> \begin{aligned}
> &c^{2} = 12^{2} + 15^{2} - 2 \cdot 12 \cdot 15\cos\theta = 369 - 360\cos\theta && \text{(Law of Cosines)} \\
> &2c\frac{dc}{dt} = 360\sin\theta\,\frac{d\theta}{dt} \\
> &\frac{d\theta}{dt} = 2^{\circ}/\text{min} = \frac{2\pi}{180} = \frac{\pi}{90} \text{ rad/min} \\
> &\theta = 60^{\circ}: \ c^{2} = 369 - 180 = 189 \implies c = 3\sqrt{21} \\
> &\frac{dc}{dt} = \frac{180\sin\theta}{c}\,\frac{d\theta}{dt} = \frac{180 \cdot \frac{\sqrt{3}}{2} \cdot \frac{\pi}{90}}{3\sqrt{21}} = \frac{\sqrt{3}\,\pi}{3\sqrt{21}} = \frac{\pi}{3\sqrt{7}} \approx 0.396
> \end{aligned}
> $$
> Hence the third side increases at $\dfrac{\pi}{3\sqrt{7}} \approx 0.396$ m/min.
>
> \# Change degrees to radians before using $\dfrac{d}{d\theta}\cos\theta = -\sin\theta$: that formula holds only for $\theta$ in radians.

### ST 2.8.47
Question: [[CAL1 HW 2.8 Questions#ST 2.8.47|ST 2.8.47]]

> [!solution] Solution
> $$
> \begin{aligned}
> &x = \text{horizontal distance from the telescope to the plane},\ \theta = \text{angle of elevation} \\
> &\tan\theta = \frac{5}{x} \implies \sec^{2}\theta\,\frac{d\theta}{dt} = -\frac{5}{x^{2}}\frac{dx}{dt} \\
> &\theta = \frac{\pi}{3}: \ x = \frac{5}{\tan(\pi/3)} = \frac{5}{\sqrt{3}},\quad \sec^{2}\frac{\pi}{3} = 4,\quad \frac{d\theta}{dt} = -\frac{\pi}{6} \\
> &4\left(-\frac{\pi}{6}\right) = -\frac{5}{25/3}\,\frac{dx}{dt} \implies -\frac{2\pi}{3} = -\frac{3}{5}\,\frac{dx}{dt} \implies \frac{dx}{dt} = \frac{10\pi}{9} \approx 3.49
> \end{aligned}
> $$
> Hence the plane flies at $\dfrac{10\pi}{9} \approx 3.49$ km/min $= \dfrac{200\pi}{3} \approx 209$ km/h.
>
> \# The plane has passed over the telescope and moves away, so the angle decreases ($d\theta/dt < 0$) while $x$ increases ($dx/dt > 0$); the signs agree with the equation.

### ST 2.8.49
Question: [[CAL1 HW 2.8 Questions#ST 2.8.49|ST 2.8.49]]

> [!solution] Solution
> At $t = 0$ the plane is 1 km directly above the station and starts to climb. Let $s$ be the distance flown along its path, so $\dfrac{ds}{dt} = 300$, and $D$ its distance from the station. The path makes the angle $90^{\circ} + 30^{\circ} = 120^{\circ}$ with the vertical segment from the station.
> $$
> \begin{aligned}
> &D^{2} = 1^{2} + s^{2} - 2 \cdot 1 \cdot s\cos 120^{\circ} = 1 + s^{2} + s && \text{(Law of Cosines)} \\
> &2D\frac{dD}{dt} = (2s + 1)\frac{ds}{dt} \\
> &t = \tfrac{1}{60} \text{ h}: \ s = 300 \cdot \tfrac{1}{60} = 5,\quad D = \sqrt{1 + 25 + 5} = \sqrt{31} \\
> &\frac{dD}{dt} = \frac{(2 \cdot 5 + 1) \cdot 300}{2\sqrt{31}} = \frac{1650}{\sqrt{31}} \approx 296
> \end{aligned}
> $$
> Hence the distance increases at about 296 km/h.
>
> ![ST 2.8.49 figure|420](../Attachments/CAL1%20HW%202.8%20Solutions%20fig%2049.png)
>
> \# $\cos 120^{\circ} = -\tfrac{1}{2}$, so $-2s\cos 120^{\circ} = +s$. The answer is a little below 300 km/h because the plane does not fly straight away from the station.
