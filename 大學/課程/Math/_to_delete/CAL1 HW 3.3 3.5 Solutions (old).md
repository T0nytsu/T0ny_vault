---
course: [CAL1]
semester: "115-1"
chapter: ["3.3", "3.5"]
tags: [calculus, homework, solutions, derivatives, limits]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §3.3, pp. 226-233, scanned PDF (I/D Test, First Derivative Test, Concavity Test, Second Derivative Test, Examples 1-7)"
  - "Stewart, Calculus, §3.5, pp. 250-256, scanned PDF (Guidelines for Sketching a Curve, Slant Asymptotes, Example 4)"
  - "Exercise 3.3.5: the graph of f' is digitized from the scan"
created: 2026-11-09
questions: "[[CAL1 HW 3.3 3.5 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.5\|ST 3.3.5]] | (a) inc. on $(0, 1)$, $(3, 5)$; dec. on $(1, 3)$, $(5, 6)$; (b) local max at $x = 1$, $x = 5$; local min at $x = 3$ |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.11\|ST 3.3.11]] | Inc. on $(2, \infty)$, dec. on $(-\infty, 2)$; local min $f(2) = -31$, no local max |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.13\|ST 3.3.13]] | Inc. on $(-\infty, 4)$, $(6, \infty)$; dec. on $(4, 5)$, $(5, 6)$; local max $f(4) = 8$, local min $f(6) = 12$ |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.17\|ST 3.3.17]] | CU on $(0, \tfrac{\pi}{4})$, $(\tfrac{3\pi}{4}, \pi)$; CD on $(\tfrac{\pi}{4}, \tfrac{3\pi}{4})$; IP $(\tfrac{\pi}{4}, \tfrac{1}{2})$, $(\tfrac{3\pi}{4}, \tfrac{1}{2})$ |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.19\|ST 3.3.19]] | (a) inc. on $(-1, 0)$, $(1, \infty)$; dec. on $(-\infty, -1)$, $(0, 1)$; (b) local max $f(0) = 3$, local min $f(\pm 1) = 2$; (c) CU on $(-\infty, -\tfrac{\sqrt{3}}{3})$, $(\tfrac{\sqrt{3}}{3}, \infty)$, CD on $(-\tfrac{\sqrt{3}}{3}, \tfrac{\sqrt{3}}{3})$, IP $(\pm\tfrac{\sqrt{3}}{3}, \tfrac{22}{9})$ |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.21\|ST 3.3.21]] | (a) inc. on $(0, \tfrac{\pi}{4})$, $(\tfrac{5\pi}{4}, 2\pi)$; dec. on $(\tfrac{\pi}{4}, \tfrac{5\pi}{4})$; (b) local max $f(\tfrac{\pi}{4}) = \sqrt{2}$, local min $f(\tfrac{5\pi}{4}) = -\sqrt{2}$; (c) CU on $(\tfrac{3\pi}{4}, \tfrac{7\pi}{4})$, CD on $(0, \tfrac{3\pi}{4})$, $(\tfrac{7\pi}{4}, 2\pi)$, IP $(\tfrac{3\pi}{4}, 0)$, $(\tfrac{7\pi}{4}, 0)$ |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.23\|ST 3.3.23]] | Local min $f(0) = 1$, local max $f(1) = 2$ (both tests agree) |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.29\|ST 3.3.29]] | Sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.31\|ST 3.3.31]] | Sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.33\|ST 3.3.33]] | Sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.35\|ST 3.3.35]] | Sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.39\|ST 3.3.39]] | (a) inc. on $(-\infty, 0)$, $(2, \infty)$, dec. on $(0, 2)$; (b) local max $f(0) = 4$, local min $f(2) = 0$; (c) CU on $(1, \infty)$, CD on $(-\infty, 1)$, IP $(1, 2)$; (d) sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.41\|ST 3.3.41]] | (a) inc. on $(-2, 0)$, $(2, \infty)$, dec. on $(-\infty, -2)$, $(0, 2)$; (b) local max $f(0) = 3$, local min $f(\pm 2) = -5$; (c) CU on $(-\infty, -\tfrac{2\sqrt{3}}{3})$, $(\tfrac{2\sqrt{3}}{3}, \infty)$, CD on $(-\tfrac{2\sqrt{3}}{3}, \tfrac{2\sqrt{3}}{3})$, IP $(\pm\tfrac{2\sqrt{3}}{3}, -\tfrac{13}{9})$; (d) sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.43\|ST 3.3.43]] | (a) inc. on $(2, \infty)$, dec. on $(-\infty, 2)$; (b) local min $g(2) = -4$, no local max; (c) CU on $(-\infty, 0)$, $(\tfrac{4}{3}, \infty)$, CD on $(0, \tfrac{4}{3})$, IP $(0, 12)$, $(\tfrac{4}{3}, \tfrac{68}{27})$; (d) sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.49\|ST 3.3.49]] | (a) inc. on $(-1, \infty)$, dec. on $(-\infty, -1)$; (b) local min $C(-1) = -3$, no local max; (c) CU on $(-\infty, 0)$, $(2, \infty)$, CD on $(0, 2)$, IP $(0, 0)$, $(2, 6\sqrt[3]{2})$; (d) sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.67\|ST 3.3.67]] | $f(x) = \tfrac{2}{9}x^{3} + \tfrac{1}{3}x^{2} - \tfrac{4}{3}x + \tfrac{7}{9}$ |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.3.73\|ST 3.3.73]] | Proof; the inflection point is at $x = -\tfrac{b}{3a}$ |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.5.5\|ST 3.5.5]] | Local min $y(1) = -27$; IP $(2, -16)$, $(4, 0)$; sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.5.9\|ST 3.5.9]] | H.A. $y = 2$, V.A. $x = -2$; inc. on $(-\infty, -2)$, $(-2, \infty)$; sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.5.23\|ST 3.5.23]] | Domain $(-\infty, -2] \cup [1, \infty)$; slant asymptotes $y = x + \tfrac{1}{2}$, $y = -x - \tfrac{1}{2}$; sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.5.29\|ST 3.5.29]] | Local max $y(-1) = 2$, local min $y(1) = -2$; IP $(0, 0)$; sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.5.35\|ST 3.5.35]] | V.A. $x = \pm\tfrac{\pi}{2}$; local min $y(0) = 0$; CU on the whole domain; sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.5.51\|ST 3.5.51]] | $y = 2x - 3$ |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.5.53\|ST 3.5.53]] | Slant asymptote $y = x + 1$; local max $y(0) = 0$, local min $y(2) = 4$; sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.5.55\|ST 3.5.55]] | Slant asymptote $y = x$; local min $y(2) = 3$; sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.5.57\|ST 3.5.57]] | Slant asymptote $y = 2x + 1$; IP $(0, 1)$, $(\pm\sqrt{3}, 1 \pm \tfrac{3\sqrt{3}}{2})$; sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.5.59\|ST 3.5.59]] | Proof; sketch |
| [[CAL1 HW 3.3 3.5 Questions#ST 3.5.61\|ST 3.5.61]] | Proof |

## ST §3.3 What Derivatives Tell Us about the Shape of a Graph

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Increasing and Decreasing Test|I/D Test]]**: if $f'(x) > 0$ on an interval, then $f$ is increasing on that interval; if $f'(x) < 0$, decreasing.
> - **[[Critical Number]]**: a number $c$ in the domain of $f$ with $f'(c) = 0$ or $f'(c)$ does not exist.
> - **[[First Derivative Test]]**: let $c$ be a critical number of a continuous $f$. If $f'$ changes from $+$ to $-$ at $c$, then $f$ has a [[Local Extreme Value|local maximum]] at $c$; from $-$ to $+$, a local minimum; no change of sign, neither. An endpoint of the domain is never a local extreme point: $f(c) \ge f(x)$ must hold for all $x$ near $c$ on **both** sides.
> - **[[Concavity|Concavity Test]]**: if $f''(x) > 0$ on an interval $I$, then the graph of $f$ is concave upward (CU) on $I$; if $f''(x) < 0$, concave downward (CD).
> - **[[Inflection Point]]** (IP): a point $P$ on the curve where $f$ is continuous and the curve changes from CU to CD or from CD to CU. So check that $f''$ **changes sign** and that the number is **in the domain**; $f''$ may be $0$ or may not exist there.
> - **[[Second Derivative Test]]**: suppose $f''$ is continuous near $c$. If $f'(c) = 0$ and $f''(c) > 0$, then $f$ has a local minimum at $c$; if $f'(c) = 0$ and $f''(c) < 0$, a local maximum. If $f''(c) = 0$ the test says nothing; use the First Derivative Test.
> - **Sign chart**: list every number where $f'$ (or $f''$) is $0$ or does not exist; between two consecutive ones the sign is constant, so one factor-by-factor check (or one test value) per interval decides it.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 3.3.5
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.5|ST 3.3.5]]

> [!solution] Solution
> From the graph: $f'(x) = 0$ at $x = 1, 3, 5$; $f'(x) > 0$ on $(0, 1)$ and $(3, 5)$; $f'(x) < 0$ on $(1, 3)$ and $(5, 6)$.
> - (a) $f$ is increasing on $(0, 1)$ and $(3, 5)$, decreasing on $(1, 3)$ and $(5, 6)$.
> - (b) Local maximum at $x = 1$ and $x = 5$ ($f'$ changes from $+$ to $-$); local minimum at $x = 3$ ($f'$ changes from $-$ to $+$).
>
> ![ST 3.3.5 figure|440](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.3.5.png)
>
> \# The graph is the graph of $f'$, not of $f$: read only on which side of the $x$-axis it lies (the green signs), not whether it rises or falls. The peak of $f'$ at $x = 4$ is where $f$ increases fastest, not a maximum of $f$. The endpoints $0$ and $6$ are not local extreme points, because the graph stops there.

### ST 3.3.11
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.11|ST 3.3.11]]

> [!solution] Solution
> $$
> f'(x) = 24x^{3} - 48x^{2} = 24x^{2}(x - 2) = 0 \iff x = 0,\ 2
> $$
>
> | $x$ | $(-\infty, 0)$ | $(0, 2)$ | $(2, \infty)$ |
> | --- | --- | --- | --- |
> | $24x^{2}$ | $+$ | $+$ | $+$ |
> | $x - 2$ | $-$ | $-$ | $+$ |
> | $f'(x)$ | $-$ | $-$ | $+$ |
> | $f$ | dec. | dec. | inc. |
>
> Hence $f$ is decreasing on $(-\infty, 2)$ and increasing on $(2, \infty)$. Local minimum $f(2) = 96 - 128 + 1 = -31$; no local maximum.
>
> \# At $x = 0$ we have $f'(0) = 0$, but $f'$ does not change sign there ($24x^{2} \ge 0$ on both sides), so by the First Derivative Test $f(0)$ is not an extreme value: the graph has a horizontal tangent at $(0, 1)$ and keeps falling. Since $f$ is continuous at $0$, the two intervals of decrease join into $(-\infty, 2)$; writing $(-\infty, 0)$ and $(0, 2)$ separately is also true.

### ST 3.3.13
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.13|ST 3.3.13]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(x) = \frac{x^{2} - 24}{x - 5}, \quad x \ne 5 \\
> &f'(x) = \frac{2x(x - 5) - (x^{2} - 24)}{(x - 5)^{2}} = \frac{x^{2} - 10x + 24}{(x - 5)^{2}} = \frac{(x - 4)(x - 6)}{(x - 5)^{2}} = 0 \iff x = 4,\ 6
> \end{aligned}
> $$
>
> | $x$ | $(-\infty, 4)$ | $(4, 5)$ | $(5, 6)$ | $(6, \infty)$ |
> | --- | --- | --- | --- | --- |
> | $x - 4$ | $-$ | $+$ | $+$ | $+$ |
> | $x - 6$ | $-$ | $-$ | $-$ | $+$ |
> | $f'(x)$ | $+$ | $-$ | $-$ | $+$ |
> | $f$ | inc. | dec. | dec. | inc. |
>
> Hence $f$ is increasing on $(-\infty, 4)$ and $(6, \infty)$, decreasing on $(4, 5)$ and $(5, 6)$. Local maximum $f(4) = \frac{16 - 24}{-1} = 8$; local minimum $f(6) = \frac{36 - 24}{1} = 12$.
>
> \# The [[Quotient Rule]] gives $f'$; its denominator $(x - 5)^{2}$ is positive, so the sign comes from $(x - 4)(x - 6)$. The number $5$ is not a critical number (it is not in the domain), but it still splits the sign chart, and $(4, 5)$ and $(5, 6)$ cannot be joined: $x = 5$ is a vertical asymptote. That is also why the local maximum value $8$ is smaller than the local minimum value $12$: they lie on the two branches of the graph, on either side of the asymptote.

### ST 3.3.17
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.17|ST 3.3.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f'(x) = 2\sin x\cos x + 2\sin 2x = \sin 2x + 2\sin 2x = 3\sin 2x \\
> &f''(x) = 6\cos 2x = 0 \iff 2x = \tfrac{\pi}{2},\ \tfrac{3\pi}{2} \iff x = \tfrac{\pi}{4},\ \tfrac{3\pi}{4} && (0 \le 2x \le 2\pi)
> \end{aligned}
> $$
>
> | $x$ | $(0, \tfrac{\pi}{4})$ | $(\tfrac{\pi}{4}, \tfrac{3\pi}{4})$ | $(\tfrac{3\pi}{4}, \pi)$ |
> | --- | --- | --- | --- |
> | $f''(x)$ | $+$ | $-$ | $+$ |
> | $f$ | CU | CD | CU |
>
> Hence $f$ is CU on $(0, \tfrac{\pi}{4})$ and $(\tfrac{3\pi}{4}, \pi)$, CD on $(\tfrac{\pi}{4}, \tfrac{3\pi}{4})$.
> $$
> f\!\left(\tfrac{\pi}{4}\right) = \tfrac{1}{2} - \cos\tfrac{\pi}{2} = \tfrac{1}{2}, \qquad f\!\left(\tfrac{3\pi}{4}\right) = \tfrac{1}{2} - \cos\tfrac{3\pi}{2} = \tfrac{1}{2}
> $$
> Inflection points: $\left(\tfrac{\pi}{4}, \tfrac{1}{2}\right)$ and $\left(\tfrac{3\pi}{4}, \tfrac{1}{2}\right)$.
>
> \# $(\sin^{2}x)' = 2\sin x \cdot \cos x$ and $(\cos 2x)' = -2\sin 2x$ by the [[Chain Rule]]; then $2\sin x\cos x = \sin 2x$. Signs of $\cos 2x$: for $0 < x < \frac{\pi}{4}$ the angle $2x$ lies in $(0, \frac{\pi}{2})$, where cosine is positive; for $\frac{\pi}{4} < x < \frac{3\pi}{4}$ it lies in $(\frac{\pi}{2}, \frac{3\pi}{2})$, where cosine is negative. Turn $0 \le x \le \pi$ into $0 \le 2x \le 2\pi$ before solving $\cos 2x = 0$, or a solution is lost.

### ST 3.3.19
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.19|ST 3.3.19]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f'(x) = 4x^{3} - 4x = 4x(x + 1)(x - 1) = 0 \iff x = -1,\ 0,\ 1 \\
> &f''(x) = 12x^{2} - 4 = 4(3x^{2} - 1) = 0 \iff x = \pm\tfrac{1}{\sqrt{3}} = \pm\tfrac{\sqrt{3}}{3}
> \end{aligned}
> $$
>
> | $x$ | $(-\infty, -1)$ | $(-1, 0)$ | $(0, 1)$ | $(1, \infty)$ |
> | --- | --- | --- | --- | --- |
> | $f'(x)$ | $-$ | $+$ | $-$ | $+$ |
> | $f$ | dec. | inc. | dec. | inc. |
>
> - (a) Increasing on $(-1, 0)$ and $(1, \infty)$; decreasing on $(-\infty, -1)$ and $(0, 1)$.
> - (b) Local maximum $f(0) = 3$; local minimum $f(\pm 1) = 1 - 2 + 3 = 2$.
> - (c) $f''(x) > 0 \iff x^{2} > \tfrac{1}{3}$: CU on $\left(-\infty, -\tfrac{\sqrt{3}}{3}\right)$ and $\left(\tfrac{\sqrt{3}}{3}, \infty\right)$, CD on $\left(-\tfrac{\sqrt{3}}{3}, \tfrac{\sqrt{3}}{3}\right)$. $f\!\left(\pm\tfrac{\sqrt{3}}{3}\right) = \tfrac{1}{9} - \tfrac{2}{3} + 3 = \tfrac{22}{9}$, so the inflection points are $\left(\pm\tfrac{\sqrt{3}}{3}, \tfrac{22}{9}\right)$.
>
> \# $f(-x) = f(x)$, so $f$ is even and its graph is symmetric about the $y$-axis: the results for $x < 0$ mirror those for $x > 0$. The sign of $f''$ needs no chart: $3x^{2} - 1$ is an upward parabola, positive outside its two roots and negative between them.

### ST 3.3.21
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.21|ST 3.3.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f'(x) = \cos x - \sin x = 0 \iff \tan x = 1 \iff x = \tfrac{\pi}{4},\ \tfrac{5\pi}{4} \\
> &f''(x) = -\sin x - \cos x = 0 \iff \tan x = -1 \iff x = \tfrac{3\pi}{4},\ \tfrac{7\pi}{4} && (0 \le x \le 2\pi)
> \end{aligned}
> $$
>
> | $x$ | $(0, \tfrac{\pi}{4})$ | $(\tfrac{\pi}{4}, \tfrac{3\pi}{4})$ | $(\tfrac{3\pi}{4}, \tfrac{5\pi}{4})$ | $(\tfrac{5\pi}{4}, \tfrac{7\pi}{4})$ | $(\tfrac{7\pi}{4}, 2\pi)$ |
> | --- | --- | --- | --- | --- | --- |
> | $f'(x)$ | $+$ | $-$ | $-$ | $+$ | $+$ |
> | $f''(x)$ | $-$ | $-$ | $+$ | $+$ | $-$ |
> | $f$ | inc., CD | dec., CD | dec., CU | inc., CU | inc., CD |
>
> - (a) Increasing on $(0, \tfrac{\pi}{4})$ and $(\tfrac{5\pi}{4}, 2\pi)$; decreasing on $(\tfrac{\pi}{4}, \tfrac{5\pi}{4})$.
> - (b) Local maximum $f(\tfrac{\pi}{4}) = \tfrac{\sqrt{2}}{2} + \tfrac{\sqrt{2}}{2} = \sqrt{2}$; local minimum $f(\tfrac{5\pi}{4}) = -\sqrt{2}$.
> - (c) CU on $(\tfrac{3\pi}{4}, \tfrac{7\pi}{4})$; CD on $(0, \tfrac{3\pi}{4})$ and $(\tfrac{7\pi}{4}, 2\pi)$. Inflection points $(\tfrac{3\pi}{4}, 0)$ and $(\tfrac{7\pi}{4}, 0)$.
>
> \# Dividing by $\cos x$ loses nothing: if $\cos x = 0$, then $\sin x = \pm 1$, so neither $\cos x = \sin x$ nor $\cos x = -\sin x$ can hold. Test values for the chart: $f'(\pi) = -1 < 0$, $f'(\tfrac{3\pi}{2}) = 1 > 0$; $f''(\tfrac{\pi}{2}) = -1 < 0$, $f''(\pi) = 1 > 0$. Here $f''(x) = -f(x)$, so the inflection points are exactly where the graph crosses the $x$-axis. The endpoint values $f(0) = f(2\pi) = 1$ are not local extreme values.

### ST 3.3.23
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.23|ST 3.3.23]]

> [!solution] Solution
> $$
> f'(x) = 6x - 6x^{2} = 6x(1 - x) = 0 \iff x = 0,\ 1
> $$
>
> **First Derivative Test**
>
> | $x$ | $(-\infty, 0)$ | $(0, 1)$ | $(1, \infty)$ |
> | --- | --- | --- | --- |
> | $f'(x)$ | $-$ | $+$ | $-$ |
>
> $f'$: $- \to +$ at $0$, so $f(0) = 1$ is a local minimum; $+ \to -$ at $1$, so $f(1) = 1 + 3 - 2 = 2$ is a local maximum.
>
> **Second Derivative Test**
> $$
> \begin{aligned}
> &f''(x) = 6 - 12x \\
> &f''(0) = 6 > 0 \implies \text{local min } f(0) = 1 \\
> &f''(1) = -6 < 0 \implies \text{local max } f(1) = 2
> \end{aligned}
> $$
>
> Preferred here: the Second Derivative Test, because $f''$ is quick to find and is not $0$ at either critical number.
>
> \# Either preference is acceptable if it is justified. The First Derivative Test always decides and also gives the intervals of increase and decrease; the Second Derivative Test gives no answer when $f''(c) = 0$ or $f''(c)$ does not exist (as at $x = 0$ in Exercise 11 and Exercise 43), and then you are back to the First Derivative Test.

### ST 3.3.29
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.29|ST 3.3.29]]

> [!solution] Solution
> **(a)** $f' > 0$: increasing everywhere; $f'' < 0$: concave downward everywhere. One possible graph:
>
> ![ST 3.3.29 (a) figure|400](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.3.29a.png)
>
> **(b)** $f' < 0$: decreasing everywhere; $f'' > 0$: concave upward everywhere. One possible graph:
>
> ![ST 3.3.29 (b) figure|400](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.3.29b.png)
>
> \# In (a) the curve rises more and more slowly; in (b) it falls more and more slowly. It never has a horizontal tangent, since $f' \ne 0$. The figures use (a) $f(x) = x - \sqrt{x^{2} + 1}$, with $f'(x) = 1 - \frac{x}{\sqrt{x^{2} + 1}} > 0$ (because $\lvert x \rvert < \sqrt{x^{2} + 1}$) and $f''(x) = -\frac{1}{(x^{2} + 1)^{3/2}} < 0$, and (b) $f(x) = \sqrt{x^{2} + 1} - x$; a sketch needs no formula.

### ST 3.3.31
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.31|ST 3.3.31]]

> [!solution] Solution
> - $f'(0) = f'(2) = f'(4) = 0$: horizontal tangents at $x = 0, 2, 4$.
> - $f'$: $+$ on $(-\infty, 0)$, $-$ on $(0, 2)$, $+$ on $(2, 4)$, $-$ on $(4, \infty)$: local maximum at $x = 0$ and $x = 4$, local minimum at $x = 2$.
> - $f''$: $-$ on $(-\infty, 1)$, $+$ on $(1, 3)$, $-$ on $(3, \infty)$: CD, CU, CD, so inflection points at $x = 1$ and $x = 3$.
>
> One possible graph:
>
> ![ST 3.3.31 figure|440](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.3.31.png)
>
> \# The shape is an M: peaks at $0$ and $4$, a valley at $2$, and the bending changes at $1$ and $3$, between each peak and the valley. No heights are given, so any heights with this shape work.

### ST 3.3.33
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.33|ST 3.3.33]]

> [!solution] Solution
> - $f'(5) = 0$, $f' < 0$ for $x < 5$, $f' > 0$ for $x > 5$: decreasing, then increasing, so a local minimum at $x = 5$.
> - $f''$: $-$ on $(-\infty, 2)$, $+$ on $(2, 8)$, $-$ on $(8, \infty)$: CD, CU, CD, so inflection points at $x = 2$ and $x = 8$.
>
> One possible graph:
>
> ![ST 3.3.33 figure|440](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.3.33.png)
>
> \# Left of $2$ the graph falls while bending downward; between $2$ and $8$ it is a cup with its bottom at $5$; right of $8$ it rises while bending downward, so it flattens out. The two inflection points are where the graph is steepest.

### ST 3.3.35
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.35|ST 3.3.35]]

> [!solution] Solution
> For $x \ge 0$:
> - $f(0) = 0$, $f'(0) = 0$: the graph starts at the origin with a horizontal tangent.
> - $f'$: $+$ on $(0, 2)$, $-$ on $(2, 4)$, $+$ on $(4, 6)$, $-$ on $(6, \infty)$: local maximum at $x = 2$ and $x = 6$, local minimum at $x = 4$.
> - $f''$: $+$ on $(0, 1)$, $-$ on $(1, 3)$, $+$ on $(3, 5)$, $-$ on $(5, \infty)$: inflection points at $x = 1, 3, 5$.
>
> $f(-x) = f(x)$: the graph is symmetric about the $y$-axis, so reflect the part for $x \ge 0$. Then $f$ has a local minimum at $0$ as well. One possible graph:
>
> ![ST 3.3.35 figure|480](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.3.35.png)
>
> \# Blue dots are local extreme points and green dots inflection points. For $x < 0$ the conditions follow from symmetry: for an even $f$, $f'$ is odd and $f''$ is even, so for example $f' < 0$ on $(-2, 0)$ and $f'' > 0$ on $(-1, 0)$; that is why $0$ is a local minimum. The heights of the peaks are not given.

### ST 3.3.39
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.39|ST 3.3.39]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f'(x) = 3x^{2} - 6x = 3x(x - 2) = 0 \iff x = 0,\ 2 \\
> &f''(x) = 6x - 6 = 6(x - 1) = 0 \iff x = 1
> \end{aligned}
> $$
>
> | $x$ | $(-\infty, 0)$ | $(0, 1)$ | $(1, 2)$ | $(2, \infty)$ |
> | --- | --- | --- | --- | --- |
> | $f'(x)$ | $+$ | $-$ | $-$ | $+$ |
> | $f''(x)$ | $-$ | $-$ | $+$ | $+$ |
> | $f$ | inc., CD | dec., CD | dec., CU | inc., CU |
>
> - (a) Increasing on $(-\infty, 0)$ and $(2, \infty)$; decreasing on $(0, 2)$.
> - (b) Local maximum $f(0) = 4$; local minimum $f(2) = 8 - 12 + 4 = 0$.
> - (c) CU on $(1, \infty)$, CD on $(-\infty, 1)$; inflection point $(1, f(1)) = (1, 2)$.
> - (d) $f(x) = (x + 1)(x - 2)^{2}$: intercepts $(-1, 0)$, $(2, 0)$, $(0, 4)$.
>
> ![ST 3.3.39 figure|400](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.3.39.png)
>
> \# Factoring: $f(2) = 0$, so $x - 2$ divides $f$, and $x^{3} - 3x^{2} + 4 = (x - 2)(x^{2} - x - 2) = (x - 2)^{2}(x + 1)$. The double root $2$ is where the graph touches the $x$-axis at its local minimum. The inflection point of a cubic lies midway between its critical numbers, here $1$ (see Exercise 73).

### ST 3.3.41
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.41|ST 3.3.41]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f'(x) = 2x^{3} - 8x = 2x(x + 2)(x - 2) = 0 \iff x = -2,\ 0,\ 2 \\
> &f''(x) = 6x^{2} - 8 = 0 \iff x^{2} = \tfrac{4}{3} \iff x = \pm\tfrac{2}{\sqrt{3}} = \pm\tfrac{2\sqrt{3}}{3}
> \end{aligned}
> $$
>
> | $x$ | $(-\infty, -2)$ | $(-2, 0)$ | $(0, 2)$ | $(2, \infty)$ |
> | --- | --- | --- | --- | --- |
> | $f'(x)$ | $-$ | $+$ | $-$ | $+$ |
> | $f$ | dec. | inc. | dec. | inc. |
>
> - (a) Increasing on $(-2, 0)$ and $(2, \infty)$; decreasing on $(-\infty, -2)$ and $(0, 2)$.
> - (b) Local maximum $f(0) = 3$; local minimum $f(\pm 2) = 8 - 16 + 3 = -5$.
> - (c) $f''(x) > 0 \iff x^{2} > \tfrac{4}{3}$: CU on $\left(-\infty, -\tfrac{2\sqrt{3}}{3}\right)$ and $\left(\tfrac{2\sqrt{3}}{3}, \infty\right)$, CD on $\left(-\tfrac{2\sqrt{3}}{3}, \tfrac{2\sqrt{3}}{3}\right)$. $f\!\left(\pm\tfrac{2\sqrt{3}}{3}\right) = \tfrac{1}{2} \cdot \tfrac{16}{9} - 4 \cdot \tfrac{4}{3} + 3 = -\tfrac{13}{9}$, so the inflection points are $\left(\pm\tfrac{2\sqrt{3}}{3}, -\tfrac{13}{9}\right)$.
> - (d) $f$ is even: symmetric about the $y$-axis; $y$-intercept $3$.
>
> ![ST 3.3.41 figure|440](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.3.41.png)
>
> \# The $x$-intercepts are not needed for the sketch: $x^{4} - 8x^{2} + 6 = 0$ gives $x^{2} = 4 \pm \sqrt{10}$, so $x \approx \pm 0.92$ and $x \approx \pm 2.68$. The figure stretches the horizontal scale.

### ST 3.3.43
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.43|ST 3.3.43]]

> [!solution] Solution
> $$
> \begin{aligned}
> &g'(t) = 12t^{3} - 24t^{2} = 12t^{2}(t - 2) = 0 \iff t = 0,\ 2 \\
> &g''(t) = 36t^{2} - 48t = 12t(3t - 4) = 0 \iff t = 0,\ \tfrac{4}{3}
> \end{aligned}
> $$
>
> | $t$ | $(-\infty, 0)$ | $(0, \tfrac{4}{3})$ | $(\tfrac{4}{3}, 2)$ | $(2, \infty)$ |
> | --- | --- | --- | --- | --- |
> | $g'(t)$ | $-$ | $-$ | $-$ | $+$ |
> | $g''(t)$ | $+$ | $-$ | $+$ | $+$ |
> | $g$ | dec., CU | dec., CD | dec., CU | inc., CU |
>
> - (a) Increasing on $(2, \infty)$; decreasing on $(-\infty, 2)$.
> - (b) Local minimum $g(2) = 48 - 64 + 12 = -4$; no local maximum.
> - (c) CU on $(-\infty, 0)$ and $(\tfrac{4}{3}, \infty)$, CD on $(0, \tfrac{4}{3})$; inflection points $(0, 12)$ and $\left(\tfrac{4}{3}, \tfrac{68}{27}\right)$.
> - (d)
>
> ![ST 3.3.43 figure|400](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.3.43.png)
>
> \# At $t = 0$: $g'(0) = 0$ but $g'$ does not change sign ($12t^{2} \ge 0$), so there is no extreme value; the concavity changes instead, which gives an inflection point with a horizontal tangent. $g\!\left(\tfrac{4}{3}\right) = 3 \cdot \tfrac{256}{81} - 8 \cdot \tfrac{64}{27} + 12 = \tfrac{256 - 512 + 324}{27} = \tfrac{68}{27}$.

### ST 3.3.49
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.49|ST 3.3.49]]

> [!solution] Solution
> $$
> \begin{aligned}
> &C(x) = x^{1/3}(x + 4) = x^{4/3} + 4x^{1/3} \\
> &C'(x) = \tfrac{4}{3}x^{1/3} + \tfrac{4}{3}x^{-2/3} = \tfrac{4}{3}x^{-2/3}(x + 1) = \frac{4(x + 1)}{3x^{2/3}} \\
> &\qquad C'(-1) = 0, \quad C'(0) \text{ does not exist} \\
> &C''(x) = \tfrac{4}{9}x^{-2/3} - \tfrac{8}{9}x^{-5/3} = \tfrac{4}{9}x^{-5/3}(x - 2) = \frac{4(x - 2)}{9x^{5/3}} \\
> &\qquad C''(2) = 0, \quad C''(0) \text{ does not exist}
> \end{aligned}
> $$
>
> | $x$ | $(-\infty, -1)$ | $(-1, 0)$ | $(0, 2)$ | $(2, \infty)$ |
> | --- | --- | --- | --- | --- |
> | $C'(x)$ | $-$ | $+$ | $+$ | $+$ |
> | $C''(x)$ | $+$ | $+$ | $-$ | $+$ |
> | $C$ | dec., CU | inc., CU | inc., CD | inc., CU |
>
> - (a) Increasing on $(-1, \infty)$; decreasing on $(-\infty, -1)$.
> - (b) Local minimum $C(-1) = (-1)(3) = -3$; no local maximum.
> - (c) CU on $(-\infty, 0)$ and $(2, \infty)$, CD on $(0, 2)$; inflection points $(0, 0)$ and $(2, 6\sqrt[3]{2})$.
> - (d) Intercepts $(-4, 0)$, $(0, 0)$.
>
> ![ST 3.3.49 figure|400](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.3.49.png)
>
> \# Signs: $x^{2/3} = (\sqrt[3]{x})^{2} > 0$ for $x \ne 0$, so $C'$ has the sign of $x + 1$; $x^{5/3}$ has the sign of $x$, so $C''$ has the sign of $\frac{x - 2}{x}$. At $0$ the derivative does not exist ($C'(x) \to \infty$: a [[Vertical Tangent Line|vertical tangent]]), yet $C$ is continuous there and the concavity changes, so $(0, 0)$ is still an inflection point; $C''(0) = 0$ is not needed. $C(2) = \sqrt[3]{2} \cdot 6$.

### ST 3.3.67
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.67|ST 3.3.67]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f'(x) = 3ax^{2} + 2bx + c \\
> &\text{local max } 3 \text{ at } -2: \quad f(-2) = -8a + 4b - 2c + d = 3, \quad f'(-2) = 12a - 4b + c = 0 \\
> &\text{local min } 0 \text{ at } 1: \quad f(1) = a + b + c + d = 0, \quad f'(1) = 3a + 2b + c = 0 \\[6pt]
> &f'(-2) - f'(1): \ 9a - 6b = 0 \implies b = \tfrac{3}{2}a, \quad c = -3a - 2b = -6a \\
> &f(-2) - f(1): \ -9a + 3b - 3c = 3 \\
> &\implies -9a + \tfrac{9}{2}a + 18a = \tfrac{27}{2}a = 3 \implies a = \tfrac{2}{9} \\
> &b = \tfrac{1}{3}, \quad c = -\tfrac{4}{3}, \quad d = -(a + b + c) = \tfrac{7}{9}
> \end{aligned}
> $$
> $$
> f(x) = \tfrac{2}{9}x^{3} + \tfrac{1}{3}x^{2} - \tfrac{4}{3}x + \tfrac{7}{9}
> $$
> Check: $f''(x) = \tfrac{4}{3}x + \tfrac{2}{3}$; $f''(-2) = -2 < 0$ (local max), $f''(1) = 2 > 0$ (local min).
>
> \# $f'(-2) = 0$ and $f'(1) = 0$ come from [[Fermat's Theorem]]: a local extremum of a differentiable function is at a critical number. The four equations only make $-2$ and $1$ critical numbers with the right values; the Second Derivative Test then confirms that $-2$ gives a maximum and $1$ a minimum. Factored, $f(x) = \tfrac{1}{9}(x - 1)^{2}(2x + 7)$: the local minimum value $0$ at $1$ makes $1$ a double root.

### ST 3.3.73
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.3.73|ST 3.3.73]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{pf: Let } f(x) = ax^{3} + bx^{2} + cx + d, \ a \ne 0. \\
> &f'(x) = 3ax^{2} + 2bx + c, \quad f''(x) = 6ax + 2b = 0 \iff x = -\frac{b}{3a} \\
> &f'' \text{ is linear with slope } 6a \ne 0 \\
> &\implies f'' \text{ changes sign at } -\tfrac{b}{3a} \text{ and has one sign on each side of it} \\
> &f \text{ is continuous (a polynomial)} \\
> &\implies \left(-\tfrac{b}{3a},\ f\!\left(-\tfrac{b}{3a}\right)\right) \text{ is an inflection point, and there is no other.} \\[6pt]
> &\text{If the } x\text{-intercepts are } x_{1}, x_{2}, x_{3}, \text{ then} \\
> &f(x) = a(x - x_{1})(x - x_{2})(x - x_{3}) = a\left[x^{3} - (x_{1} + x_{2} + x_{3})x^{2} + \cdots\right] \\
> &\implies b = -a(x_{1} + x_{2} + x_{3}) && (x^{2}\text{-coefficients}) \\
> &\implies -\frac{b}{3a} = \frac{x_{1} + x_{2} + x_{3}}{3}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# If $a > 0$, then $f'' < 0$ left of $-\tfrac{b}{3a}$ and $f'' > 0$ right of it (CD, then CU); if $a < 0$, the other way. Either way the concavity changes exactly once. The factorization holds because each $x$-intercept $x_{i}$ gives a factor $x - x_{i}$ (Factor Theorem), and the leading coefficient must stay $a$; only the $x^{2}$-coefficient is needed. Exercise 39 checks it: $f(x) = (x + 1)(x - 2)^{2}$ has roots $-1, 2, 2$ (the double root counted twice), and $\tfrac{-1 + 2 + 2}{3} = 1$ is its inflection point.

## ST §3.5 Summary of Curve Sketching

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Curve Sketching|Guidelines for sketching a curve]]**: A. Domain; B. Intercepts; C. Symmetry (even, $f(-x) = f(x)$: symmetric about the $y$-axis; odd, $f(-x) = -f(x)$: symmetric about the origin; periodic); D. Asymptotes (horizontal, vertical, slant); E. Intervals of increase or decrease ($f'$); F. Local maximum or minimum values (critical numbers, First Derivative Test); G. Concavity and points of inflection ($f''$); H. Sketch the curve: asymptotes as dashed lines, then the points from B, F and G.
> - **[[Horizontal Asymptote]]** (H.A.) $y = L$: $\lim_{x \to \infty} f(x) = L$ or $\lim_{x \to -\infty} f(x) = L$. **[[Vertical Asymptote]]** (V.A.) $x = a$: at least one one-sided limit of $f$ at $a$ is $\infty$ or $-\infty$.
> - **[[Slant Asymptote]]**: the line $y = mx + b$ with $m \ne 0$ is a slant asymptote if $\lim_{x \to \infty} [f(x) - (mx + b)] = 0$ (or the same for $x \to -\infty$). For a rational function whose numerator has degree one more than the denominator, long division gives $f(x) = mx + b + \frac{R(x)}{Q(x)}$ with $\frac{R(x)}{Q(x)} \to 0$.
> - **Roots**: $\sqrt{x^{2}} = \lvert x \rvert$; for the form $\infty - \infty$ with a root, multiply by the conjugate.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 3.5.5
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.5.5|ST 3.5.5]]

> [!solution] Solution
> - **A.** Domain $\mathbb{R}$.
> - **B.** $y$-intercept $0$; $x$-intercepts $0$, $4$.
> - **C.** No symmetry.
> - **D.** No asymptote (a polynomial; $y \to \infty$ as $x \to \pm\infty$).
>
> $$
> \begin{aligned}
> &y' = (x - 4)^{3} + 3x(x - 4)^{2} = (x - 4)^{2}(4x - 4) = 4(x - 1)(x - 4)^{2} \\
> &y'' = 4\left[(x - 4)^{2} + 2(x - 1)(x - 4)\right] = 4(x - 4)(3x - 6) = 12(x - 2)(x - 4)
> \end{aligned}
> $$
>
> | $x$ | $(-\infty, 1)$ | $(1, 2)$ | $(2, 4)$ | $(4, \infty)$ |
> | --- | --- | --- | --- | --- |
> | $y'$ | $-$ | $+$ | $+$ | $+$ |
> | $y''$ | $+$ | $+$ | $-$ | $+$ |
> | $y$ | dec., CU | inc., CU | inc., CD | inc., CU |
>
> - **E.** Decreasing on $(-\infty, 1)$; increasing on $(1, \infty)$.
> - **F.** Local minimum $y(1) = 1 \cdot (-3)^{3} = -27$; no local maximum.
> - **G.** CU on $(-\infty, 2)$ and $(4, \infty)$, CD on $(2, 4)$; inflection points $(2, -16)$ and $(4, 0)$.
> - **H.**
>
> ![ST 3.5.5 figure|400](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.5.5.png)
>
> \# $y'$ by the [[Product Rule]] and the Chain Rule, then factor out $(x - 4)^{2}$. At $x = 4$, $y'(4) = 0$ but $(x - 4)^{2} \ge 0$ keeps $y'$ positive on both sides: no extreme value, but an inflection point with a horizontal tangent, as at $t = 0$ in Exercise 3.3.43. $y(2) = 2 \cdot (-2)^{3} = -16$.

### ST 3.5.9
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.5.9|ST 3.5.9]]

> [!solution] Solution
> - **A.** Domain $\{x \mid x \ne -2\} = (-\infty, -2) \cup (-2, \infty)$.
> - **B.** $y$-intercept $\tfrac{3}{2}$; $x$-intercept $-\tfrac{3}{2}$.
> - **C.** No symmetry.
> - **D.**
>
> $$
> \begin{aligned}
> &\lim_{x \to \pm\infty} \frac{2x + 3}{x + 2} = \lim_{x \to \pm\infty} \frac{2 + \frac{3}{x}}{1 + \frac{2}{x}} = 2 \implies \text{H.A. } y = 2 \\
> &\lim_{x \to -2^{+}} y = -\infty, \quad \lim_{x \to -2^{-}} y = \infty \implies \text{V.A. } x = -2 \\
> &\qquad (2x + 3 \to -1,\ x + 2 \to 0^{\pm}) \\[6pt]
> &y' = \frac{2(x + 2) - (2x + 3)}{(x + 2)^{2}} = \frac{1}{(x + 2)^{2}} > 0 \\
> &y'' = \frac{-2}{(x + 2)^{3}}
> \end{aligned}
> $$
>
> - **E.** Increasing on $(-\infty, -2)$ and $(-2, \infty)$.
> - **F.** No local extreme value.
> - **G.** $y'' > 0$ for $x < -2$, $y'' < 0$ for $x > -2$: CU on $(-\infty, -2)$, CD on $(-2, \infty)$; no inflection point ($-2$ is not in the domain).
> - **H.**
>
> ![ST 3.5.9 figure|440](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.5.9.png)
>
> \# Long division gives $y = 2 - \frac{1}{x + 2}$: the hyperbola $y = -\frac{1}{x}$ moved 2 left and 2 up, which explains both asymptotes and the shape at once. $y''$ comes from $y' = (x + 2)^{-2}$ by the Chain Rule.

### ST 3.5.23
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.5.23|ST 3.5.23]]

> [!solution] Solution
> - **A.** $x^{2} + x - 2 = (x + 2)(x - 1) \ge 0 \iff x \le -2$ or $x \ge 1$: domain $(-\infty, -2] \cup [1, \infty)$.
> - **B.** $x$-intercepts $-2$, $1$; no $y$-intercept ($0$ is not in the domain).
> - **C.** No symmetry.
> - **D.** No H.A. or V.A. ($y \to \infty$ as $x \to \pm\infty$). Slant asymptotes:
>
> $$
> \begin{aligned}
> &\lim_{x \to \infty} \left[\sqrt{x^{2} + x - 2} - \left(x + \tfrac{1}{2}\right)\right] \\
> &= \lim_{x \to \infty} \frac{(x^{2} + x - 2) - (x^{2} + x + \tfrac{1}{4})}{\sqrt{x^{2} + x - 2} + x + \tfrac{1}{2}} = \lim_{x \to \infty} \frac{-\tfrac{9}{4}}{\sqrt{x^{2} + x - 2} + x + \tfrac{1}{2}} = 0 \\[6pt]
> &\lim_{x \to -\infty} \left[\sqrt{x^{2} + x - 2} - \left(-x - \tfrac{1}{2}\right)\right] \\
> &= \lim_{x \to -\infty} \frac{-\tfrac{9}{4}}{\sqrt{x^{2} + x - 2} - x - \tfrac{1}{2}} = 0 && (-x \to \infty) \\[6pt]
> &\implies y = x + \tfrac{1}{2} \ (x \to \infty) \text{ and } y = -x - \tfrac{1}{2} \ (x \to -\infty) \\[6pt]
> &y' = \frac{2x + 1}{2\sqrt{x^{2} + x - 2}}, \qquad y'' = \frac{-9}{4(x^{2} + x - 2)^{3/2}} < 0
> \end{aligned}
> $$
>
> - **E.** $y' < 0$ for $x < -2$, $y' > 0$ for $x > 1$: decreasing on $(-\infty, -2)$, increasing on $(1, \infty)$.
> - **F.** No local extreme value ($y' = 0$ only at $x = -\tfrac{1}{2}$, which is not in the domain).
> - **G.** CD on $(-\infty, -2)$ and $(1, \infty)$; no inflection point.
> - **H.**
>
> ![ST 3.5.23 figure|440](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.5.23.png)
>
> \# Where $x + \tfrac{1}{2}$ comes from: complete the square, $x^{2} + x - 2 = \left(x + \tfrac{1}{2}\right)^{2} - \tfrac{9}{4}$, so for large $\lvert x \rvert$ the root is close to $\left\lvert x + \tfrac{1}{2} \right\rvert$. For $y''$, write $y' = \frac{2x + 1}{2y}$: then $y'' = \frac{2 \cdot 2y - (2x + 1) \cdot 2y'}{4y^{2}} = \frac{4y^{2} - (2x + 1)^{2}}{4y^{3}} = \frac{-9}{4y^{3}}$. At $x = -2$ and $x = 1$ the tangent is vertical ($\lvert y' \rvert \to \infty$); the value $0$ there is the absolute minimum, but endpoints are not local extreme points.

### ST 3.5.29
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.5.29|ST 3.5.29]]

> [!solution] Solution
> - **A.** Domain $\mathbb{R}$.
> - **B.** $y$-intercept $0$; $x - 3x^{1/3} = x^{1/3}(x^{2/3} - 3) = 0 \iff x = 0$ or $x^{2/3} = 3 \iff x = 0, \pm 3\sqrt{3}$.
> - **C.** $y(-x) = -x + 3x^{1/3} = -y(x)$: odd, symmetric about the origin.
> - **D.** No asymptote.
>
> $$
> \begin{aligned}
> &y' = 1 - x^{-2/3} = \frac{x^{2/3} - 1}{x^{2/3}}: \quad y' = 0 \iff x = \pm 1, \quad y'(0) \text{ does not exist} \\
> &y'' = \tfrac{2}{3}x^{-5/3} = \frac{2}{3x^{5/3}}
> \end{aligned}
> $$
>
> | $x$ | $(-\infty, -1)$ | $(-1, 0)$ | $(0, 1)$ | $(1, \infty)$ |
> | --- | --- | --- | --- | --- |
> | $y'$ | $+$ | $-$ | $-$ | $+$ |
> | $y''$ | $-$ | $-$ | $+$ | $+$ |
> | $y$ | inc., CD | dec., CD | dec., CU | inc., CU |
>
> - **E.** Increasing on $(-\infty, -1)$ and $(1, \infty)$; decreasing on $(-1, 1)$.
> - **F.** Local maximum $y(-1) = -1 + 3 = 2$; local minimum $y(1) = 1 - 3 = -2$.
> - **G.** CD on $(-\infty, 0)$, CU on $(0, \infty)$; inflection point $(0, 0)$.
> - **H.**
>
> ![ST 3.5.29 figure|440](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.5.29.png)
>
> \# $x^{2/3} = (\sqrt[3]{x})^{2} > 0$ for $x \ne 0$, so $y'$ has the sign of $x^{2/3} - 1$, which is positive exactly when $\lvert x \rvert > 1$; $x^{5/3}$ has the sign of $x$. At $0$, $y'(x) \to -\infty$: the inflection point $(0, 0)$ has a vertical tangent. $x^{2/3} = 3 \iff \lvert x \rvert = 3^{3/2} = 3\sqrt{3}$. Because $y$ is odd, the maximum at $-1$ and the minimum at $1$ mirror each other.

### ST 3.5.35
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.5.35|ST 3.5.35]]

> [!solution] Solution
> - **A.** Domain $\left(-\tfrac{\pi}{2}, \tfrac{\pi}{2}\right)$.
> - **B.** $x \tan x = 0 \iff x = 0$ (in the domain): intercept $(0, 0)$.
> - **C.** $(-x)\tan(-x) = x \tan x$: even, symmetric about the $y$-axis.
> - **D.**
>
> $$
> \begin{aligned}
> &\lim_{x \to \pi/2^{-}} x \tan x = \infty && (x \to \tfrac{\pi}{2} > 0,\ \tan x \to \infty) \\
> &\lim_{x \to -\pi/2^{+}} x \tan x = \infty && (x \to -\tfrac{\pi}{2} < 0,\ \tan x \to -\infty) \\
> &\implies \text{V.A. } x = \tfrac{\pi}{2} \text{ and } x = -\tfrac{\pi}{2} \\[6pt]
> &y' = \tan x + x\sec^{2}x \\
> &y'' = \sec^{2}x + \sec^{2}x + x \cdot 2\sec x \cdot \sec x\tan x \\
> &\hphantom{y''} = 2\sec^{2}x\,(1 + x\tan x)
> \end{aligned}
> $$
>
> - **E.** For $0 < x < \tfrac{\pi}{2}$: $\tan x > 0$ and $x\sec^{2}x > 0$, so $y' > 0$; for $-\tfrac{\pi}{2} < x < 0$ both terms are negative, so $y' < 0$. Decreasing on $\left(-\tfrac{\pi}{2}, 0\right)$, increasing on $\left(0, \tfrac{\pi}{2}\right)$.
> - **F.** Local minimum $y(0) = 0$.
> - **G.** $x\tan x \ge 0$ on the domain, so $y'' = 2\sec^{2}x\,(1 + x\tan x) > 0$: CU on $\left(-\tfrac{\pi}{2}, \tfrac{\pi}{2}\right)$; no inflection point.
> - **H.**
>
> ![ST 3.5.35 figure|360](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.5.35.png)
>
> \# $(\sec^{2}x)' = 2\sec x \cdot (\sec x)' = 2\sec x \cdot \sec x\tan x$ by the Chain Rule. On the domain, $x$ and $\tan x$ always have the same sign, which gives both E and G without a sign chart.

### ST 3.5.51
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.5.51|ST 3.5.51]]

> [!solution] Solution
> $$
> \begin{aligned}
> &2x^{3} - 5x^{2} + 3x = (x^{2} - x - 2)(2x - 3) + (4x - 6) && \text{(long division)} \\
> &\implies y = 2x - 3 + \frac{4x - 6}{x^{2} - x - 2} \\
> &\lim_{x \to \pm\infty} \frac{4x - 6}{x^{2} - x - 2} = \lim_{x \to \pm\infty} \frac{\frac{4}{x} - \frac{6}{x^{2}}}{1 - \frac{1}{x} - \frac{2}{x^{2}}} = 0 \\
> &\implies \lim_{x \to \pm\infty} \left[y - (2x - 3)\right] = 0
> \end{aligned}
> $$
> Hence the slant asymptote is $y = 2x - 3$.
>
> \# Long division: $2x^{3} \div x^{2} = 2x$, and $2x^{3} - 5x^{2} + 3x - 2x(x^{2} - x - 2) = -3x^{2} + 7x$; then $-3x^{2} \div x^{2} = -3$, and $-3x^{2} + 7x + 3(x^{2} - x - 2) = 4x - 6$. Check: $(x^{2} - x - 2)(2x - 3) + 4x - 6 = 2x^{3} - 5x^{2} + 3x$. The slant asymptote is the quotient; the remainder does not matter, as long as its degree is less than that of the denominator.

### ST 3.5.53
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.5.53|ST 3.5.53]]

> [!solution] Solution
> - **A.** Domain $\{x \mid x \ne 1\}$.
> - **B.** Intercept $(0, 0)$.
> - **C.** No symmetry.
> - **D.**
>
> $$
> \begin{aligned}
> &\lim_{x \to 1^{+}} \frac{x^{2}}{x - 1} = \infty, \quad \lim_{x \to 1^{-}} \frac{x^{2}}{x - 1} = -\infty \implies \text{V.A. } x = 1 \\
> &\qquad (x^{2} \to 1,\ x - 1 \to 0^{\pm}) \\
> &y = \frac{x^{2}}{x - 1} = x + 1 + \frac{1}{x - 1}, \quad \frac{1}{x - 1} \to 0 \ (x \to \pm\infty) \\
> &\implies \text{slant asymptote } y = x + 1 \\[6pt]
> &y' = 1 - \frac{1}{(x - 1)^{2}} = \frac{(x - 1)^{2} - 1}{(x - 1)^{2}} = \frac{x(x - 2)}{(x - 1)^{2}}, \qquad y'' = \frac{2}{(x - 1)^{3}}
> \end{aligned}
> $$
>
> | $x$ | $(-\infty, 0)$ | $(0, 1)$ | $(1, 2)$ | $(2, \infty)$ |
> | --- | --- | --- | --- | --- |
> | $y'$ | $+$ | $-$ | $-$ | $+$ |
> | $y''$ | $-$ | $-$ | $+$ | $+$ |
> | $y$ | inc., CD | dec., CD | dec., CU | inc., CU |
>
> - **E.** Increasing on $(-\infty, 0)$ and $(2, \infty)$; decreasing on $(0, 1)$ and $(1, 2)$.
> - **F.** Local maximum $y(0) = 0$; local minimum $y(2) = 4$.
> - **G.** CD on $(-\infty, 1)$, CU on $(1, \infty)$; no inflection point ($1$ is not in the domain).
> - **H.**
>
> ![ST 3.5.53 figure|440](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.5.53.png)
>
> \# Long division: $x^{2} = (x - 1)(x + 1) + 1$. Differentiating the divided form $x + 1 + (x - 1)^{-1}$ is quicker than the Quotient Rule and gives $y''$ at once. Right of $1$ the curve lies above its asymptote ($\frac{1}{x - 1} > 0$), left of $1$ below it.

### ST 3.5.55
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.5.55|ST 3.5.55]]

> [!solution] Solution
> - **A.** Domain $\{x \mid x \ne 0\}$.
> - **B.** No $y$-intercept; $x^{3} + 4 = 0 \iff x = -\sqrt[3]{4}$.
> - **C.** No symmetry.
> - **D.**
>
> $$
> \begin{aligned}
> &y = \frac{x^{3} + 4}{x^{2}} = x + \frac{4}{x^{2}} \\
> &\lim_{x \to 0} y = \infty \implies \text{V.A. } x = 0 && (x \to 0,\ \tfrac{4}{x^{2}} \to \infty) \\
> &\frac{4}{x^{2}} \to 0 \ (x \to \pm\infty) \implies \text{slant asymptote } y = x \\[6pt]
> &y' = 1 - \frac{8}{x^{3}} = \frac{x^{3} - 8}{x^{3}}: \quad y' = 0 \iff x = 2, \qquad y'' = \frac{24}{x^{4}} > 0
> \end{aligned}
> $$
>
> | $x$ | $(-\infty, 0)$ | $(0, 2)$ | $(2, \infty)$ |
> | --- | --- | --- | --- |
> | $x^{3} - 8$ | $-$ | $-$ | $+$ |
> | $x^{3}$ | $-$ | $+$ | $+$ |
> | $y'$ | $+$ | $-$ | $+$ |
>
> - **E.** Increasing on $(-\infty, 0)$ and $(2, \infty)$; decreasing on $(0, 2)$.
> - **F.** Local minimum $y(2) = 2 + 1 = 3$.
> - **G.** CU on $(-\infty, 0)$ and $(0, \infty)$; no inflection point.
> - **H.**
>
> ![ST 3.5.55 figure|440](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.5.55.png)
>
> \# Here no long division is needed: dividing each term by $x^{2}$ gives $x + \frac{4}{x^{2}}$. Since $\frac{4}{x^{2}} > 0$, the whole curve lies above its slant asymptote $y = x$. The vertical asymptote is the $y$-axis itself.

### ST 3.5.57
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.5.57|ST 3.5.57]]

> [!solution] Solution
> - **A.** Domain $\mathbb{R}$ ($x^{2} + 1 > 0$).
> - **B.** $y$-intercept $1$; $2x^{3} + x^{2} + 1 = (x + 1)(2x^{2} - x + 1) = 0 \iff x = -1$.
> - **C.** No symmetry.
> - **D.** No V.A. or H.A.
>
> $$
> \begin{aligned}
> &y = 2x + 1 - \frac{2x}{x^{2} + 1}, \quad \frac{2x}{x^{2} + 1} \to 0 \ (x \to \pm\infty) \implies \text{slant asymptote } y = 2x + 1 \\[6pt]
> &y' = 2 - \frac{2(x^{2} + 1) - 2x \cdot 2x}{(x^{2} + 1)^{2}} = 2 - \frac{2(1 - x^{2})}{(x^{2} + 1)^{2}} = \frac{2x^{2}(x^{2} + 3)}{(x^{2} + 1)^{2}} \ge 0 \\
> &y'' = \frac{4x(3 - x^{2})}{(x^{2} + 1)^{3}} = 0 \iff x = 0,\ \pm\sqrt{3}
> \end{aligned}
> $$
>
> | $x$ | $(-\infty, -\sqrt{3})$ | $(-\sqrt{3}, 0)$ | $(0, \sqrt{3})$ | $(\sqrt{3}, \infty)$ |
> | --- | --- | --- | --- | --- |
> | $4x$ | $-$ | $-$ | $+$ | $+$ |
> | $3 - x^{2}$ | $-$ | $+$ | $+$ | $-$ |
> | $y''$ | $+$ | $-$ | $+$ | $-$ |
>
> - **E.** Increasing on $(-\infty, \infty)$.
> - **F.** No local extreme value ($y'(0) = 0$, but $y'$ does not change sign).
> - **G.** CU on $(-\infty, -\sqrt{3})$ and $(0, \sqrt{3})$, CD on $(-\sqrt{3}, 0)$ and $(\sqrt{3}, \infty)$; inflection points $\left(-\sqrt{3}, 1 - \tfrac{3\sqrt{3}}{2}\right)$, $(0, 1)$, $\left(\sqrt{3}, 1 + \tfrac{3\sqrt{3}}{2}\right)$.
> - **H.**
>
> ![ST 3.5.57 figure|440](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.5.57.png)
>
> \# Long division: $2x^{3} + x^{2} + 1 = (x^{2} + 1)(2x + 1) - 2x$. For $y''$, use $\left(\frac{x}{x^{2} + 1}\right)'' = \frac{2x(x^{2} - 3)}{(x^{2} + 1)^{3}}$ from [[CAL1 HW 3.4 Solutions#ST 3.4.51|Exercise 3.4.51]], so $y'' = -2 \cdot \frac{2x(x^{2} - 3)}{(x^{2} + 1)^{3}}$. $y(\sqrt{3}) = 2\sqrt{3} + 1 - \frac{2\sqrt{3}}{4} = 1 + \frac{3\sqrt{3}}{2}$. The factor $2x^{2} - x + 1$ has discriminant $1 - 8 < 0$, so $-1$ is the only $x$-intercept. The curve crosses its asymptote at $x = 0$: left of $0$ it lies above the line ($-\frac{2x}{x^{2} + 1} > 0$), right of $0$ below it.

### ST 3.5.59
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.5.59|ST 3.5.59]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\lim_{x \to \infty} \left(\sqrt{4x^{2} + 9} - 2x\right) = \lim_{x \to \infty} \frac{(4x^{2} + 9) - 4x^{2}}{\sqrt{4x^{2} + 9} + 2x} \\
> &= \lim_{x \to \infty} \frac{9}{\sqrt{4x^{2} + 9} + 2x} = 0 && (\text{denominator} \to \infty) \\[6pt]
> &\lim_{x \to -\infty} \left(\sqrt{4x^{2} + 9} - (-2x)\right) = \lim_{x \to -\infty} \frac{(4x^{2} + 9) - 4x^{2}}{\sqrt{4x^{2} + 9} - 2x} \\
> &= \lim_{x \to -\infty} \frac{9}{\sqrt{4x^{2} + 9} - 2x} = 0 && (-2x \to \infty) \\[6pt]
> &\text{Hence } y = 2x \text{ and } y = -2x \text{ are slant asymptotes.} \qquad \blacksquare
> \end{aligned}
> $$

> [!solution] Solution
> - **A.** Domain $\mathbb{R}$. **B.** $y$-intercept $3$; no $x$-intercept ($y \ge 3$). **C.** Even: symmetric about the $y$-axis. **D.** Slant asymptotes $y = 2x$ ($x \to \infty$) and $y = -2x$ ($x \to -\infty$); no H.A. or V.A.
>
> $$
> \begin{aligned}
> &y' = \frac{4x}{\sqrt{4x^{2} + 9}} \\
> &y'' = \frac{4\sqrt{4x^{2} + 9} - 4x \cdot \frac{4x}{\sqrt{4x^{2} + 9}}}{4x^{2} + 9} = \frac{4(4x^{2} + 9) - 16x^{2}}{(4x^{2} + 9)^{3/2}} = \frac{36}{(4x^{2} + 9)^{3/2}} > 0
> \end{aligned}
> $$
>
> - **E.** Decreasing on $(-\infty, 0)$, increasing on $(0, \infty)$. **F.** Local minimum $y(0) = 3$. **G.** CU on $(-\infty, \infty)$; no inflection point.
> - **H.**
>
> ![ST 3.5.59 figure|400](../Attachments/CAL1%20HW%203.3%203.5%20Solutions%20fig%203.5.59.png)
>
> \# For $x \to -\infty$ the asymptote is $y = -2x$, not $y = 2x$: there $\sqrt{4x^{2}} = 2\lvert x \rvert = -2x$. The curve lies above both asymptotes, because $\sqrt{4x^{2} + 9} > \sqrt{4x^{2}} = 2\lvert x \rvert$. It is the upper half of the hyperbola $y^{2} - 4x^{2} = 9$ (compare Exercise 61).

### ST 3.5.61
Question: [[CAL1 HW 3.3 3.5 Questions#ST 3.5.61|ST 3.5.61]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\frac{x^{2}}{a^{2}} - \frac{y^{2}}{b^{2}} = 1 \iff y = \pm\frac{b}{a}\sqrt{x^{2} - a^{2}}, \quad \lvert x \rvert \ge a && (a, b > 0) \\[6pt]
> &\lim_{x \to \infty} \left(\frac{b}{a}\sqrt{x^{2} - a^{2}} - \frac{b}{a}x\right) = \frac{b}{a}\lim_{x \to \infty} \frac{(x^{2} - a^{2}) - x^{2}}{\sqrt{x^{2} - a^{2}} + x} \\
> &= \frac{b}{a}\lim_{x \to \infty} \frac{-a^{2}}{\sqrt{x^{2} - a^{2}} + x} = 0 \\
> &\implies y = \tfrac{b}{a}x \text{ is a slant asymptote of the upper half } y = \tfrac{b}{a}\sqrt{x^{2} - a^{2}} \\[6pt]
> &\lim_{x \to \infty} \left[-\frac{b}{a}\sqrt{x^{2} - a^{2}} - \left(-\frac{b}{a}x\right)\right] = -\frac{b}{a}\lim_{x \to \infty} \left(\sqrt{x^{2} - a^{2}} - x\right) = -\frac{b}{a} \cdot 0 = 0 \\
> &\implies y = -\tfrac{b}{a}x \text{ is a slant asymptote of the lower half } y = -\tfrac{b}{a}\sqrt{x^{2} - a^{2}} \\[6pt]
> &\text{Hence both lines are slant asymptotes of the hyperbola.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The middle limit was already computed in the first one: $\sqrt{x^{2} - a^{2}} - x \to 0$. As $x \to -\infty$ the roles swap (the hyperbola is symmetric about the $y$-axis): the upper half approaches $y = -\tfrac{b}{a}x$ and the lower half $y = \tfrac{b}{a}x$. Exercise 59 is the case $y^{2}/9 - x^{2}/(9/4) = 1$ with $x$ and $y$ exchanged.
