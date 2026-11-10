---
course: [CAL1]
semester: "115-1"
chapter: ["2.7"]
tags: [calculus, homework, solutions, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §2.7, pp. 172-181, scanned PDF (rates of change, Examples 1 and 3)"
created: 2026-11-10
questions: "[[CAL1 HW 2.7 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 2.7 Questions#ST 2.7.3\|ST 2.7.3]] | (a) $v(t) = \tfrac{\pi}{2}\cos\tfrac{\pi t}{2}$; (b) 0 m/s; (c) $t = 1, 3, 5, \dots$; (d) $0 \le t < 1$, $3 < t < 5$, $7 < t < 9$, …; (e) 6 m; (g) $a(t) = -\tfrac{\pi^{2}}{4}\sin\tfrac{\pi t}{2}$, $a(1) = -\tfrac{\pi^{2}}{4} \approx -2.47$ m/s²; (i) speeding up when $1 < t < 2$, $3 < t < 4$, $5 < t < 6$, …; slowing down when $0 < t < 1$, $2 < t < 3$, $4 < t < 5$, … |
| [[CAL1 HW 2.7 Questions#ST 2.7.7\|ST 2.7.7]] | forward when $0 < t < 5$; backward when $7 < t < 8$; at rest when $5 < t < 7$ |
| [[CAL1 HW 2.7 Questions#ST 2.7.17\|ST 2.7.17]] | $\frac{dS}{dr} = 8\pi r$: (a) $160\pi \approx 503$; (b) $320\pi \approx 1005$; (c) $480\pi \approx 1508$ cm²/cm; the rate is proportional to $r$ |
| [[CAL1 HW 2.7 Questions#ST 2.7.21\|ST 2.7.21]] | (a) 4.75 A; (b) 5 A; lowest at $t = \tfrac{2}{3}$ s |
| [[CAL1 HW 2.7 Questions#ST 2.7.23\|ST 2.7.23]] | Proof |
| [[CAL1 HW 2.7 Questions#ST 2.7.33\|ST 2.7.33]] | (a) $A'(x) = \frac{xp'(x) - p(x)}{x^{2}}$; (b) Proof |

## ST §2.7 Rates of Change in the Natural and Social Sciences

> [!note] Note
> The facts that the answers use, each under its name.
> - **Rate of change**: if $y = f(x)$, the [[Derivative|derivative]] $\dfrac{dy}{dx}$ is the instantaneous rate of change of $y$ with respect to $x$. Its units are the units of $y$ divided by the units of $x$.
> - **Motion on a line**, position $s = f(t)$: velocity $v(t) = f'(t)$, acceleration $a(t) = v'(t) = f''(t)$ ([[Higher Derivatives]]). The particle is at rest when $v = 0$, moves forward (in the positive direction) when $v > 0$, and moves backward when $v < 0$.
> - **Total distance**: the particle can turn around only where $v = 0$. Split the time interval at those times and add the distances $\lvert f(t_{2}) - f(t_{1}) \rvert$ of the pieces.
> - **Speeding up** means that the speed $\lvert v \rvert$ increases: $v$ and $a$ have the same sign. **Slowing down**: $v$ and $a$ have opposite signs.
> - **Current**: $I = \dfrac{dQ}{dt}$, the rate at which charge passes the point; 1 A = 1 C/s.
> - Each answer is written as on an exam paper: the derivative, the values or the inequality, then a Hence line with units. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 2.7.3
Question: [[CAL1 HW 2.7 Questions#ST 2.7.3|ST 2.7.3]]

> [!solution] Solution
> **(a)**
> $$
> v(t) = f'(t) = \cos\left(\frac{\pi t}{2}\right) \cdot \frac{\pi}{2} = \frac{\pi}{2}\cos\frac{\pi t}{2} \qquad \text{(Chain Rule)}
> $$
>
> **(b)**
> $$
> v(1) = \frac{\pi}{2}\cos\frac{\pi}{2} = \frac{\pi}{2} \cdot 0 = 0
> $$
> Hence the velocity after 1 second is 0 m/s.
>
> **(c)**
> $$
> \begin{aligned}
> &\text{at rest} \iff v(t) = 0 \iff \cos\frac{\pi t}{2} = 0 \\
> &\iff \frac{\pi t}{2} = \frac{\pi}{2} + n\pi && (n = 0, 1, 2, \dots, \text{ since } t \ge 0) \\
> &\iff t = 2n + 1
> \end{aligned}
> $$
> Hence the particle is at rest when $t = 1, 3, 5, \dots$ (every odd number of seconds).
>
> **(d)**
> $$
> \begin{aligned}
> &\text{positive direction} \iff v(t) > 0 \iff \cos\frac{\pi t}{2} > 0 \\
> &\iff \frac{\pi t}{2} \in \left[0, \frac{\pi}{2}\right) \cup \left(\frac{3\pi}{2}, \frac{5\pi}{2}\right) \cup \left(\frac{7\pi}{2}, \frac{9\pi}{2}\right) \cup \cdots && (t \ge 0) \\
> &\iff 0 \le t < 1 \ \text{ or } \ 3 < t < 5 \ \text{ or } \ 7 < t < 9 \ \text{ or } \dots
> \end{aligned}
> $$
> Hence the particle moves in the positive direction when $0 \le t < 1$, $3 < t < 5$, $7 < t < 9$, and so on.
>
> **(e)** On $[0, 6]$ the velocity is $0$ at $t = 1, 3, 5$, so we split there:
> $$
> \begin{aligned}
> &f(0) = 0,\quad f(1) = 1,\quad f(3) = -1,\quad f(5) = 1,\quad f(6) = 0 \\
> &\lvert f(1) - f(0) \rvert + \lvert f(3) - f(1) \rvert + \lvert f(5) - f(3) \rvert + \lvert f(6) - f(5) \rvert = 1 + 2 + 2 + 1 = 6
> \end{aligned}
> $$
> Hence the total distance traveled during the first 6 seconds is 6 m.
>
> **(f)** The particle starts at $s = 0$, moves forward to $s = 1$ ($t = 1$), backward to $s = -1$ ($t = 3$), forward to $s = 1$ ($t = 5$), and backward to $s = 0$ ($t = 6$):
>
> ![ST 2.7.3 (f) figure|440](../Attachments/CAL1%20HW%202.7%20Solutions%20fig%203f.png)
>
> **(g)**
> $$
> \begin{aligned}
> &a(t) = v'(t) = \frac{\pi}{2}\left(-\sin\frac{\pi t}{2}\right) \cdot \frac{\pi}{2} = -\frac{\pi^{2}}{4}\sin\frac{\pi t}{2} && \text{(Chain Rule)} \\
> &a(1) = -\frac{\pi^{2}}{4}\sin\frac{\pi}{2} = -\frac{\pi^{2}}{4} \approx -2.47
> \end{aligned}
> $$
> Hence $a(t) = -\dfrac{\pi^{2}}{4}\sin\dfrac{\pi t}{2}$, and the acceleration after 1 second is $-\dfrac{\pi^{2}}{4} \approx -2.47$ m/s².
>
> **(h)** $s$ is the solid curve, $v$ the dashed curve, and $a$ the dotted curve, for $0 \le t \le 6$. The two bars below the graph record (d) and (i).
>
> ![ST 2.7.3 (h) figure|460](../Attachments/CAL1%20HW%202.7%20Solutions%20fig%203h.png)
>
> **(i)** Speeding up $\iff$ $v$ and $a$ have the same sign. The signs of $v = \tfrac{\pi}{2}\cos\tfrac{\pi t}{2}$ and $a = -\tfrac{\pi^{2}}{4}\sin\tfrac{\pi t}{2}$:
> $$
> \begin{array}{c|cccccc}
> t & (0, 1) & (1, 2) & (2, 3) & (3, 4) & (4, 5) & (5, 6) \\ \hline
> v & + & - & - & + & + & - \\
> a & - & - & + & + & - & - \\ \hline
>  & \text{slows} & \text{speeds} & \text{slows} & \text{speeds} & \text{slows} & \text{speeds}
> \end{array}
> $$
> Hence the particle is speeding up when $1 < t < 2$, $3 < t < 4$, $5 < t < 6$, and so on, and slowing down when $0 < t < 1$, $2 < t < 3$, $4 < t < 5$, and so on.
>
> \# $v$ and $a$ both repeat every 4 seconds, so the table repeats: speeding up on $(2n + 1, 2n + 2)$ and slowing down on $(2n, 2n + 1)$, $n = 0, 1, 2, \dots$ A one-line check: $v(t)\,a(t) = -\tfrac{\pi^{3}}{8}\sin\tfrac{\pi t}{2}\cos\tfrac{\pi t}{2} = -\tfrac{\pi^{3}}{16}\sin \pi t$, which is positive exactly when $\sin \pi t < 0$.
>
> \# In (e), $f(6) - f(0) = 0$ is the displacement, not the distance: the particle is back where it started but has traveled 6 m. That is why the interval is split at the turning points.

### ST 2.7.7
Question: [[CAL1 HW 2.7 Questions#ST 2.7.7|ST 2.7.7]]

> [!solution] Solution
> The graph gives the velocity $v$ at time $t$, so we read the sign of $v$:
> $$
> \begin{aligned}
> &\text{forward} \iff v > 0 \ \text{(graph above the } t\text{-axis)} \iff 0 < t < 5 \\
> &\text{backward} \iff v < 0 \ \text{(graph below the } t\text{-axis)} \iff 7 < t < 8 \\
> &5 < t < 7: \ v = 0 \ \text{(graph on the } t\text{-axis)}
> \end{aligned}
> $$
> Hence the particle travels forward when $0 < t < 5$ and backward when $7 < t < 8$. When $5 < t < 7$ its velocity is 0: the particle is at rest (it does not move).
>
> ![ST 2.7.7 figure|420](../Attachments/CAL1%20HW%202.7%20Solutions%20fig%207.png)
>
> \# This is a graph of velocity, not of position. Read whether the graph is above or below the axis, not whether it goes up or down: for $3 < t < 5$ the graph falls, but $v > 0$, so the particle still travels forward, only more and more slowly.

### ST 2.7.17
Question: [[CAL1 HW 2.7 Questions#ST 2.7.17|ST 2.7.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> &S = 4\pi r^{2} \implies \frac{dS}{dr} = 8\pi r \\
> &\text{(a) } r = 20: \ \frac{dS}{dr} = 8\pi \cdot 20 = 160\pi \approx 503 \\
> &\text{(b) } r = 40: \ \frac{dS}{dr} = 8\pi \cdot 40 = 320\pi \approx 1005 \\
> &\text{(c) } r = 60: \ \frac{dS}{dr} = 8\pi \cdot 60 = 480\pi \approx 1508
> \end{aligned}
> $$
> Hence the surface area increases at (a) $160\pi \approx 503$, (b) $320\pi \approx 1005$, (c) $480\pi \approx 1508$ cm²/cm.
>
> Conclusion: $\dfrac{dS}{dr} = 8\pi r$ is proportional to $r$. As the radius increases, the surface area grows at an increasing rate: when $r$ doubles, the rate doubles.
>
> \# The unit cm²/cm is the unit of $S$ divided by the unit of $r$: at $r = 20$ cm, each extra centimeter of radius adds about 503 cm² of surface.

### ST 2.7.21
Question: [[CAL1 HW 2.7 Questions#ST 2.7.21|ST 2.7.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &I(t) = Q'(t) = 3t^{2} - 4t + 6 \\
> &\text{(a) } I(0.5) = 3(0.5)^{2} - 4(0.5) + 6 = 0.75 - 2 + 6 = 4.75 \\
> &\text{(b) } I(1) = 3 - 4 + 6 = 5
> \end{aligned}
> $$
> Hence the current is (a) 4.75 A and (b) 5 A.
>
> Lowest current:
> $$
> \begin{aligned}
> &I'(t) = 6t - 4 = 0 \implies t = \tfrac{2}{3} \\
> &I'(t) < 0 \text{ for } 0 \le t < \tfrac{2}{3} && (I \text{ decreases}) \\
> &I'(t) > 0 \text{ for } t > \tfrac{2}{3} && (I \text{ increases})
> \end{aligned}
> $$
> Hence the current is lowest at $t = \tfrac{2}{3}$ s, where $I\left(\tfrac{2}{3}\right) = \tfrac{4}{3} - \tfrac{8}{3} + 6 = \tfrac{14}{3} \approx 4.67$ A.
>
> \# The question asks for the lowest current $I = Q'$, not the lowest charge $Q$, so we differentiate once more and look at the sign of $I' = Q''$. Check without calculus: $I(t) = 3\left(t - \tfrac{2}{3}\right)^{2} + \tfrac{14}{3} \ge \tfrac{14}{3}$.

### ST 2.7.23
Question: [[CAL1 HW 2.7 Questions#ST 2.7.23|ST 2.7.23]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{pf: } m = m_{0}\left(1 - \frac{v^{2}}{c^{2}}\right)^{-1/2}, \text{ where } v = v(t) \text{ and } m_{0},\ c \text{ are constants.} \\[6pt]
> &\frac{dm}{dt} = m_{0}\left(-\frac{1}{2}\right)\left(1 - \frac{v^{2}}{c^{2}}\right)^{-3/2}\left(-\frac{2v}{c^{2}}\right)\frac{dv}{dt} \quad \text{(Chain Rule)} \\
> &\phantom{\frac{dm}{dt}} = \frac{m_{0}va}{c^{2}}\left(1 - \frac{v^{2}}{c^{2}}\right)^{-3/2} \quad \left(a = \tfrac{dv}{dt}\right) \\[6pt]
> &F = \frac{d}{dt}(mv) = \frac{dm}{dt}\,v + m\,\frac{dv}{dt} \quad \text{(Product Rule)} \\
> &\phantom{F} = \frac{m_{0}v^{2}a}{c^{2}}\left(1 - \frac{v^{2}}{c^{2}}\right)^{-3/2} + m_{0}a\left(1 - \frac{v^{2}}{c^{2}}\right)^{-1/2} \\
> &\phantom{F} = m_{0}a\left(1 - \frac{v^{2}}{c^{2}}\right)^{-3/2}\left[\frac{v^{2}}{c^{2}} + \left(1 - \frac{v^{2}}{c^{2}}\right)\right] \\
> &\phantom{F} = \frac{m_{0}a}{(1 - v^{2}/c^{2})^{3/2}} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The mass $m$ changes with $t$ because $v$ does, so $\dfrac{d}{dt}(mv)$ needs the Product Rule; treating $m$ as a constant would give only $F = ma$. In the factoring step, $\left(1 - \tfrac{v^{2}}{c^{2}}\right)^{-1/2} = \left(1 - \tfrac{v^{2}}{c^{2}}\right)^{-3/2}\left(1 - \tfrac{v^{2}}{c^{2}}\right)$, and the bracket adds up to 1.

### ST 2.7.33
Question: [[CAL1 HW 2.7 Questions#ST 2.7.33|ST 2.7.33]]

> [!solution] Solution
> **(a)**
> $$
> A'(x) = \frac{x\,p'(x) - p(x) \cdot 1}{x^{2}} = \frac{xp'(x) - p(x)}{x^{2}} \qquad \text{(Quotient Rule)}
> $$
> If $A'(x) > 0$, then $A$ is increasing at $x$: the average productivity rises when more workers are added. Hence the company wants to hire more workers.

> [!proof] Proof of (b)
> $$
> \begin{aligned}
> &\text{pf: Here } x > 0 \ \text{(the number of workers). Suppose } p'(x) > A(x) = \frac{p(x)}{x}. \\
> &\implies xp'(x) > p(x) \quad \text{(multiply by } x > 0\text{)} \\
> &\implies xp'(x) - p(x) > 0 \\
> &\implies A'(x) = \frac{xp'(x) - p(x)}{x^{2}} > 0 \quad (x^{2} > 0) \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $p'(x)$ is the marginal productivity: about the value that one more worker adds. If the next worker adds more than the present average, the average goes up, like a test score above your average raising your average. The condition $x > 0$ is needed: multiplying an inequality by a negative number would reverse it.
