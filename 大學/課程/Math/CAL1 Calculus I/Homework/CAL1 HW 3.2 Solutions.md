---
course: [CAL1]
semester: "115-1"
chapter: ["3.2"]
tags: [calculus, homework, solutions, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §3.2, pp. 220-224, scanned PDF (Rolle's Theorem and the Mean Value Theorem)"
  - "Exercise 7: the value of c is read from the graph, digitized from the scan"
created: 2026-11-08
questions: "[[CAL1 HW 3.2 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 3.2 Questions#ST 3.2.7\|ST 3.2.7]] | Yes; $c \approx 3.8$ |
| [[CAL1 HW 3.2 Questions#ST 3.2.9\|ST 3.2.9]] | $c = 1$ |
| [[CAL1 HW 3.2 Questions#ST 3.2.11\|ST 3.2.11]] | $c = \pi$ |
| [[CAL1 HW 3.2 Questions#ST 3.2.13\|ST 3.2.13]] | $f'(0)$ does not exist, so $f$ is not differentiable on $(-1, 1)$ |
| [[CAL1 HW 3.2 Questions#ST 3.2.15\|ST 3.2.15]] | $c = 1$ |
| [[CAL1 HW 3.2 Questions#ST 3.2.17\|ST 3.2.17]] | $c = \tfrac{\sqrt{3}}{9} \approx 0.192$ |
| [[CAL1 HW 3.2 Questions#ST 3.2.21\|ST 3.2.21]] | The only solution is $c = 1 \notin (1, 4)$; $f$ is not continuous on $[1, 4]$ |
| [[CAL1 HW 3.2 Questions#ST 3.2.25\|ST 3.2.25]] | Proof |
| [[CAL1 HW 3.2 Questions#ST 3.2.29\|ST 3.2.29]] | $16$ |
| [[CAL1 HW 3.2 Questions#ST 3.2.31\|ST 3.2.31]] | No |
| [[CAL1 HW 3.2 Questions#ST 3.2.33\|ST 3.2.33]] | Proof |
| [[CAL1 HW 3.2 Questions#ST 3.2.35\|ST 3.2.35]] | Proof |

## ST §3.2 The Mean Value Theorem

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Rolle's Theorem]]**: if 1. $f$ is continuous on $[a, b]$, 2. $f$ is differentiable on $(a, b)$, and 3. $f(a) = f(b)$, then there is a number $c$ in $(a, b)$ such that $f'(c) = 0$.
> - **[[Mean Value Theorem]]** (MVT): if 1. $f$ is continuous on $[a, b]$ and 2. $f$ is differentiable on $(a, b)$, then there is a number $c$ in $(a, b)$ such that $f'(c) = \dfrac{f(b) - f(a)}{b - a}$, or equivalently $f(b) - f(a) = f'(c)(b - a)$. The tangent at $(c, f(c))$ is parallel to the secant line through $(a, f(a))$ and $(b, f(b))$.
> - **Checking the hypotheses**: polynomials, $\sin$, $\cos$ and $\sqrt[3]{x}$ are continuous everywhere, and a function whose derivative exists at a number is continuous there ([[Differentiable Function]]). A hypothesis fails at a break (Exercise 21) or at a cusp, corner or vertical tangent inside the open interval (Exercise 13); a vertical tangent at an endpoint does no harm (Exercise 17).
> - **Rolle's Theorem against a second root**: if $f(x) = 0$ had two solutions $a < b$, Rolle's Theorem would give $f'(r) = 0$ for some $r$ between them (Example 2, Exercise 25).
> - **The MVT turns a bound on $f'$ into a bound on $f$**: $f(b) - f(a) = f'(c)(b - a)$ (Example 5, Exercises 29, 31, 33, 35).
> - Each answer is written as on an exam paper: the hypotheses first, one per line with its reason, then the computation or the proof, then a Hence line. Grading deducts points for missing conditions, so write both intervals ($[a, b]$ for continuity, $(a, b)$ for differentiability) and check that $c$ lies in the open interval. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 3.2.7
Question: [[CAL1 HW 3.2 Questions#ST 3.2.7|ST 3.2.7]]

> [!solution] Solution
> $$
> \begin{aligned}
> &1.\ f \text{ is continuous on } [0, 5] && \text{(no break)} \\
> &2.\ f \text{ is differentiable on } (0, 5) && \text{(no corner, no vertical tangent)} \\
> &\implies \text{yes, } f \text{ satisfies the hypotheses of the MVT on } [0, 5] \\[6pt]
> &\frac{f(5) - f(0)}{5 - 0} = \frac{3 - 1}{5} = \frac{2}{5} \\[4pt]
> &f'(x) = 0 \ne \tfrac{2}{5} \text{ on } (0, 3) \implies c \in (3, 5) \\
> &\text{the tangent parallel to the secant through } (0, 1),\ (5, 3) \\
> &\text{touches the curve at } x \approx 3.8
> \end{aligned}
> $$
> Hence yes, and $c \approx 3.8$.
>
> ![ST 3.2.7 figure|440](../Attachments/CAL1%20HW%203.2%20Solutions%20fig%207.png)
>
> \# Read $f(0) = 1$ and $f(5) = 3$ from the grid. The MVT asks for a point where the tangent has the slope of the secant, $\tfrac{2}{5}$: slide a ruler parallel to the secant until it just touches the curve. On $(0, 3)$ the graph is flat (slope $0$), and on $(3, 5)$ the slope grows from $0$ to very steep, so it passes $\tfrac{2}{5}$ once, near $3.8$; any estimate between $3.7$ and $3.9$ is a fair reading. At $x = 3$ the flat part joins the curve without a corner. The steep tangent at $x = 5$ does not matter: $5$ is an endpoint, and the MVT asks for differentiability only on the open interval $(0, 5)$.

### ST 3.2.9
Question: [[CAL1 HW 3.2 Questions#ST 3.2.9|ST 3.2.9]]

> [!solution] Solution
> $$
> \begin{aligned}
> &1.\ f \text{ is a polynomial} \implies f \text{ is continuous on } [-1, 3] \\
> &2.\ f'(x) = 4x - 4 \text{ exists for all } x \implies f \text{ is differentiable on } (-1, 3) \\
> &3.\ f(-1) = 2 + 4 + 5 = 11,\quad f(3) = 18 - 12 + 5 = 11 \implies f(-1) = f(3) \\[6pt]
> &f'(c) = 4c - 4 = 0 \implies c = 1 \in (-1, 3)
> \end{aligned}
> $$
> Hence $c = 1$.
>
> \# Write all three hypotheses, each with its reason; the third, $f(a) = f(b)$, is the one Rolle's Theorem adds to the MVT. Then check that $c$ lies in the open interval $(-1, 3)$. The point $(1, f(1)) = (1, 3)$ is the vertex of the parabola, where the tangent is horizontal.

### ST 3.2.11
Question: [[CAL1 HW 3.2 Questions#ST 3.2.11|ST 3.2.11]]

> [!solution] Solution
> $$
> \begin{aligned}
> &1.\ \sin \text{ is continuous everywhere} \implies f(x) = \sin(x/2) \text{ is continuous on } [\pi/2, 3\pi/2] \\
> &2.\ f'(x) = \tfrac{1}{2}\cos(x/2) \text{ exists for all } x \implies f \text{ is differentiable on } (\pi/2, 3\pi/2) \\
> &3.\ f(\pi/2) = \sin\tfrac{\pi}{4} = \tfrac{\sqrt{2}}{2},\quad f(3\pi/2) = \sin\tfrac{3\pi}{4} = \tfrac{\sqrt{2}}{2} \implies f(\pi/2) = f(3\pi/2) \\[6pt]
> &f'(c) = \tfrac{1}{2}\cos\tfrac{c}{2} = 0 \implies \cos\tfrac{c}{2} = 0 \\
> &\tfrac{\pi}{2} < c < \tfrac{3\pi}{2} \implies \tfrac{\pi}{4} < \tfrac{c}{2} < \tfrac{3\pi}{4} \implies \tfrac{c}{2} = \tfrac{\pi}{2} \implies c = \pi
> \end{aligned}
> $$
> Hence $c = \pi$.
>
> \# The factor $\tfrac{1}{2}$ comes from the Chain Rule (inner function $x/2$). Restrict $c/2$ to $\left(\tfrac{\pi}{4}, \tfrac{3\pi}{4}\right)$ before solving: the zeros of $\cos$ are $\tfrac{\pi}{2} + n\pi$, and only $\tfrac{\pi}{2}$ lies in that interval.

### ST 3.2.13
Question: [[CAL1 HW 3.2 Questions#ST 3.2.13|ST 3.2.13]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(-1) = 1 - \left(\sqrt[3]{-1}\right)^2 = 1 - 1 = 0,\quad f(1) = 1 - 1 = 0 \implies f(-1) = f(1) \\[6pt]
> &x \ne 0:\ \ f'(x) = -\tfrac{2}{3}x^{-1/3} = -\frac{2}{3\sqrt[3]{x}} \ne 0 \quad \text{(the numerator is } -2\text{)} \\
> &x = 0:\ \ \frac{f(0 + h) - f(0)}{h} = \frac{-h^{2/3}}{h} = -\frac{1}{\sqrt[3]{h}} \quad (h \ne 0) \\
> &\qquad \lim_{h \to 0^{+}} \left(-\frac{1}{\sqrt[3]{h}}\right) = -\infty,\quad \lim_{h \to 0^{-}} \left(-\frac{1}{\sqrt[3]{h}}\right) = \infty \\
> &\qquad \implies f'(0) \text{ does not exist} \\[6pt]
> &\implies \text{there is no } c \in (-1, 1) \text{ with } f'(c) = 0
> \end{aligned}
> $$
> This does not contradict Rolle's Theorem: $f$ is not differentiable at $0$, and $0 \in (-1, 1)$, so hypothesis 2 ($f$ is differentiable on $(-1, 1)$) fails. Rolle's Theorem then says nothing about $f$.
>
> ![ST 3.2.13 figure|440](../Attachments/CAL1%20HW%203.2%20Solutions%20fig%2013.png)
>
> \# Rolle's Theorem has the form "if 1, 2 and 3, then $c$ exists". When a hypothesis fails, the conclusion may fail too, and that is no contradiction. Here hypotheses 1 and 3 hold ($x^{2/3} = (\sqrt[3]{x})^2$ is continuous everywhere, and $f(-1) = f(1)$); only 2 fails, at the cusp $(0, 1)$. The cusp is the highest point of the graph, but there is no tangent line there, so no horizontal one. The formula $-\tfrac{2}{3}x^{-1/3}$ is undefined at $0$, but that alone does not prove that $f'(0)$ does not exist; the difference quotient does.

### ST 3.2.15
Question: [[CAL1 HW 3.2 Questions#ST 3.2.15|ST 3.2.15]]

> [!solution] Solution
> $$
> \begin{aligned}
> &1.\ f \text{ is a polynomial} \implies f \text{ is continuous on } [0, 2] \\
> &2.\ f'(x) = 4x - 3 \text{ exists for all } x \implies f \text{ is differentiable on } (0, 2) \\[6pt]
> &\frac{f(2) - f(0)}{2 - 0} = \frac{3 - 1}{2} = 1 \\
> &f'(c) = 4c - 3 = 1 \implies c = 1 \in (0, 2)
> \end{aligned}
> $$
> Hence $c = 1$.
>
> \# The MVT has two hypotheses; $f(a) = f(b)$ is not needed (here $f(0) = 1 \ne 3 = f(2)$). For every quadratic $f(x) = px^2 + qx + r$ the number $c$ is the midpoint of the interval, because $\dfrac{f(b) - f(a)}{b - a} = p(a + b) + q = f'\!\left(\tfrac{a + b}{2}\right)$. Here $\tfrac{0 + 2}{2} = 1$, and in Exercise 9, $\tfrac{-1 + 3}{2} = 1$.

### ST 3.2.17
Question: [[CAL1 HW 3.2 Questions#ST 3.2.17|ST 3.2.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> &1.\ \sqrt[3]{x} \text{ is continuous for all } x \implies f \text{ is continuous on } [0, 1] \\
> &2.\ f'(x) = \tfrac{1}{3}x^{-2/3} = \frac{1}{3\sqrt[3]{x^2}} \text{ exists for } x \ne 0 \implies f \text{ is differentiable on } (0, 1) \\[6pt]
> &\frac{f(1) - f(0)}{1 - 0} = \frac{1 - 0}{1} = 1 \\
> &f'(c) = \frac{1}{3c^{2/3}} = 1 \implies c^{2/3} = \tfrac{1}{3} \implies c^2 = \tfrac{1}{27} \\
> &\implies c = \pm\frac{1}{3\sqrt{3}} = \pm\frac{\sqrt{3}}{9} \\
> &c \in (0, 1) \implies c = \frac{\sqrt{3}}{9} \approx 0.192
> \end{aligned}
> $$
> Hence $c = \dfrac{\sqrt{3}}{9}$.
>
> \# $f'(0)$ does not exist (the graph of $\sqrt[3]{x}$ has a vertical tangent at the origin), but $0$ is an endpoint: the MVT needs differentiability only on the open interval $(0, 1)$. Compare Exercise 13, where the bad point $0$ lies inside the interval. To solve $c^{2/3} = \tfrac{1}{3}$, cube both sides, then take square roots and keep the root in $(0, 1)$.

### ST 3.2.21
Question: [[CAL1 HW 3.2 Questions#ST 3.2.21|ST 3.2.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(4) - f(1) = \frac{1}{1^2} - \frac{1}{(-2)^2} = 1 - \frac{1}{4} = \frac{3}{4} \\
> &f'(x) = -2(x - 3)^{-3} = -\frac{2}{(x - 3)^3} \quad (x \ne 3) \\[6pt]
> &f(4) - f(1) = f'(c)(4 - 1) \iff \frac{3}{4} = -\frac{6}{(c - 3)^3} \\
> &\phantom{f(4) - f(1) = f'(c)(4 - 1)} \iff (c - 3)^3 = -8 \iff c - 3 = -2 \iff c = 1 \\
> &1 \notin (1, 4) \implies \text{there is no such } c \text{ in } (1, 4)
> \end{aligned}
> $$
> This does not contradict the Mean Value Theorem: $f(3)$ is not defined ($\lim_{x \to 3} (x - 3)^{-2} = \infty$), so $f$ is not continuous on $[1, 4]$ and hypothesis 1 fails (hypothesis 2 fails at $3$ too). The MVT does not apply to $f$ on $[1, 4]$.
>
> ![ST 3.2.21 figure|420](../Attachments/CAL1%20HW%203.2%20Solutions%20fig%2021.png)
>
> \# Another way to see it: on $(1, 3)$, $0 < 3 - x < 2$, so $f'(x) = \dfrac{2}{(3 - x)^3} > \dfrac{2}{8} = \dfrac{1}{4}$; on $(3, 4)$, $f'(x) < 0$. So no tangent over $(1, 4)$ has the slope $\tfrac{1}{4}$ of the secant. The only solution of the equation, $c = 1$, is an endpoint, and the MVT always gives a $c$ strictly inside. A real number has exactly one real cube root, so $(c - 3)^3 = -8$ gives only $c - 3 = -2$.

### ST 3.2.25
Question: [[CAL1 HW 3.2 Questions#ST 3.2.25|ST 3.2.25]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{pf: Let } f(x) = x^3 - 15x + c. \\
> &\text{Suppose there are two solutions } a < b \text{ in } [-2, 2]. \\
> &\implies f(a) = f(b) = 0 \\
> &\because f \text{ is a polynomial,} \\
> &\therefore f \text{ is continuous on } [a, b] \text{ and differentiable on } (a, b) \\
> &\implies \exists\, r \in (a, b) \text{ s.t. } f'(r) = 0 && \text{(Rolle's Theorem)} \\[6pt]
> &\text{But } -2 \le a < r < b \le 2 \implies r^2 < 4 \\
> &\implies f'(r) = 3r^2 - 15 < 3 \cdot 4 - 15 = -3 < 0, \text{ a contradiction.} \\[6pt]
> &\text{Hence the equation has at most one solution in } [-2, 2]. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The letter $c$ is already taken by the equation, so the number that Rolle's Theorem gives is called $r$. This is the method of Example 2 ($x^3 + x - 1 = 0$): two solutions $\implies$ by Rolle's Theorem $f'$ has a zero between them; then show that $f'$ has no zero there. The interval is what makes it work: $f'(x) = 3(x^2 - 5) = 0$ only at $x = \pm\sqrt{5} \approx \pm 2.24$, both outside $[-2, 2]$. On all of $\mathbb{R}$ the equation can have three solutions (for $c = 0$: $x = 0, \pm\sqrt{15}$). "At most one" does not claim that a solution exists: for $c = 100$, $x^3 - 15x + 100 \ge 100 - (8 + 30) = 62 > 0$ on $[-2, 2]$, so there is none.

### ST 3.2.29
Question: [[CAL1 HW 3.2 Questions#ST 3.2.29|ST 3.2.29]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f'(x) \text{ exists for } 1 \le x \le 4 \implies f \text{ is continuous on } [1, 4] \text{ and differentiable on } (1, 4) \\
> &\implies \exists\, c \in (1, 4) \text{ s.t. } f(4) - f(1) = f'(c)(4 - 1) && \text{(MVT)} \\
> &\implies f(4) = 10 + 3f'(c) \ge 10 + 3 \cdot 2 = 16 && (f'(c) \ge 2) \\[6pt]
> &f(x) = 2x + 8:\ \ f(1) = 10,\quad f'(x) = 2 \ge 2,\quad f(4) = 16
> \end{aligned}
> $$
> Hence $f(4) \ge 16$, and $16$ is attained: the smallest possible value of $f(4)$ is $16$.
>
> \# Example 5 with $\ge$ in place of $\le$. "Differentiable implies continuous" gives hypothesis 1 without extra work. The line $f(x) = 2x + 8$ through $(1, 10)$ with slope exactly $2$ shows that $16$ is not only a lower bound but the actual minimum; without such an example, "how small can $f(4)$ be" is only half answered.

### ST 3.2.31
Question: [[CAL1 HW 3.2 Questions#ST 3.2.31|ST 3.2.31]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Suppose such an } f \text{ exists.} \\
> &f'(x) \text{ exists for all } x \implies f \text{ is continuous on } [0, 2] \text{ and differentiable on } (0, 2) \\
> &\implies \exists\, c \in (0, 2) \text{ s.t. } f'(c) = \frac{f(2) - f(0)}{2 - 0} = \frac{4 - (-1)}{2} = \frac{5}{2} && \text{(MVT)} \\
> &\text{But } f'(c) \le 2 < \tfrac{5}{2}, \text{ a contradiction.}
> \end{aligned}
> $$
> Hence no such function exists.
>
> \# The secant from $(0, -1)$ to $(2, 4)$ has slope $\tfrac{5}{2}$, and the MVT puts a tangent with that slope somewhere in between; but every tangent has slope at most $2$. Equivalently, as in Example 5: $f(2) = f(0) + 2f'(c) \le -1 + 4 = 3 < 4$.

### ST 3.2.33
Question: [[CAL1 HW 3.2 Questions#ST 3.2.33|ST 3.2.33]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{pf: Let } 0 < x < 2\pi. \\
> &\because \sin \text{ is differentiable everywhere,} \\
> &\therefore \sin \text{ is continuous on } [0, x] \text{ and differentiable on } (0, x) \\
> &\implies \exists\, c \in (0, x) \text{ s.t. } \sin x - \sin 0 = \cos c\,(x - 0) && \text{(MVT)} \\
> &\implies \sin x = x\cos c \\[6pt]
> &0 < c < x < 2\pi \implies \cos c < 1 && (\cos c = 1 \iff c = 2n\pi) \\
> &x > 0 \implies \sin x = x\cos c < x \cdot 1 = x \\[6pt]
> &\text{Hence } \sin x < x \text{ for } 0 < x < 2\pi. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Two conditions carry the proof. First, $c$ lies strictly between $0$ and $2\pi$, so $\cos c \ne 1$; this is where the bound $2\pi$ is used (at $c = 0$ or $c = 2\pi$, $\cos c = 1$, and only $\le$ would follow). Second, $x > 0$, so multiplying $\cos c < 1$ by $x$ keeps the direction of the inequality. Another way: apply the MVT to $g(t) = t - \sin t$ on $[0, x]$, which gives $g(x) = g(x) - g(0) = (1 - \cos c)\,x > 0$. In fact $\sin x < x$ for every $x > 0$: for $x \ge 2\pi$, $\sin x \le 1 < 2\pi \le x$.

### ST 3.2.35
Question: [[CAL1 HW 3.2 Questions#ST 3.2.35|ST 3.2.35]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{pf: If } a = b, \text{ then } \lvert \sin a - \sin b \rvert = 0 = \lvert a - b \rvert. \\[4pt]
> &\text{If } a \ne b, \text{ let } I \text{ be the closed interval with endpoints } a \text{ and } b. \\
> &\because \sin \text{ is differentiable everywhere,} \\
> &\therefore \sin \text{ is continuous on } I \text{ and differentiable inside } I \\
> &\implies \exists\, c \text{ between } a \text{ and } b \text{ s.t. } \sin a - \sin b = \cos c\,(a - b) && \text{(MVT)} \\
> &\implies \lvert \sin a - \sin b \rvert = \lvert \cos c \rvert\,\lvert a - b \rvert \le \lvert a - b \rvert && (\lvert \cos c \rvert \le 1) \\[6pt]
> &\text{Hence } \lvert \sin a - \sin b \rvert \le \lvert a - b \rvert \text{ for all } a \text{ and } b. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The MVT is stated on $[a, b]$ with $a < b$, so the case $a = b$ is separate. If $a > b$, the MVT on $[b, a]$ gives $\sin a - \sin b = \cos c\,(a - b)$, the same equation, so the order of $a$ and $b$ does not matter. Meaning: $\sin$ never changes faster than $x$ does, because its slope $\cos c$ stays between $-1$ and $1$. With $b = 0$ it says $\lvert \sin a \rvert \le \lvert a \rvert$; compare Exercise 33.
