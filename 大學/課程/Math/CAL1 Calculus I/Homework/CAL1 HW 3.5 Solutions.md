---
course: [CAL1]
semester: "115-1"
chapter: ["3.5"]
tags: [calculus, homework, solutions, derivatives, limits]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §3.5, pp. 250-256, scanned PDF (Guidelines for Sketching a Curve, Slant Asymptotes, Example 4)"
created: 2026-11-09
questions: "[[CAL1 HW 3.5 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 3.5 Questions#ST 3.5.5\|ST 3.5.5]] | Local min $y(1) = -27$; IP $(2, -16)$, $(4, 0)$; sketch |
| [[CAL1 HW 3.5 Questions#ST 3.5.9\|ST 3.5.9]] | H.A. $y = 2$, V.A. $x = -2$; inc. on $(-\infty, -2)$, $(-2, \infty)$; sketch |
| [[CAL1 HW 3.5 Questions#ST 3.5.23\|ST 3.5.23]] | Domain $(-\infty, -2] \cup [1, \infty)$; slant asymptotes $y = x + \tfrac{1}{2}$, $y = -x - \tfrac{1}{2}$; sketch |
| [[CAL1 HW 3.5 Questions#ST 3.5.29\|ST 3.5.29]] | Local max $y(-1) = 2$, local min $y(1) = -2$; IP $(0, 0)$; sketch |
| [[CAL1 HW 3.5 Questions#ST 3.5.35\|ST 3.5.35]] | V.A. $x = \pm\tfrac{\pi}{2}$; local min $y(0) = 0$; CU on the whole domain; sketch |
| [[CAL1 HW 3.5 Questions#ST 3.5.51\|ST 3.5.51]] | $y = 2x - 3$ |
| [[CAL1 HW 3.5 Questions#ST 3.5.53\|ST 3.5.53]] | Slant asymptote $y = x + 1$; local max $y(0) = 0$, local min $y(2) = 4$; sketch |
| [[CAL1 HW 3.5 Questions#ST 3.5.55\|ST 3.5.55]] | Slant asymptote $y = x$; local min $y(2) = 3$; sketch |
| [[CAL1 HW 3.5 Questions#ST 3.5.57\|ST 3.5.57]] | Slant asymptote $y = 2x + 1$; IP $(0, 1)$, $(\pm\sqrt{3}, 1 \pm \tfrac{3\sqrt{3}}{2})$; sketch |
| [[CAL1 HW 3.5 Questions#ST 3.5.59\|ST 3.5.59]] | Proof; sketch |
| [[CAL1 HW 3.5 Questions#ST 3.5.61\|ST 3.5.61]] | Proof |

## ST §3.5 Summary of Curve Sketching

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Curve Sketching|Guidelines for sketching a curve]]**: A. Domain; B. Intercepts; C. Symmetry (even, $f(-x) = f(x)$: symmetric about the $y$-axis; odd, $f(-x) = -f(x)$: symmetric about the origin; periodic); D. Asymptotes (horizontal, vertical, slant); E. Intervals of increase or decrease ($f'$); F. Local maximum or minimum values (critical numbers, First Derivative Test); G. Concavity and points of inflection ($f''$); H. Sketch the curve: asymptotes as dashed lines, then the points from B, F and G.
> - **[[Horizontal Asymptote]]** (H.A.) $y = L$: $\lim_{x \to \infty} f(x) = L$ or $\lim_{x \to -\infty} f(x) = L$. **[[Vertical Asymptote]]** (V.A.) $x = a$: at least one one-sided limit of $f$ at $a$ is $\infty$ or $-\infty$.
> - **[[Slant Asymptote]]**: the line $y = mx + b$ with $m \ne 0$ is a slant asymptote if $\lim_{x \to \infty} [f(x) - (mx + b)] = 0$ (or the same for $x \to -\infty$). For a rational function whose numerator has degree one more than the denominator, long division gives $f(x) = mx + b + \frac{R(x)}{Q(x)}$ with $\frac{R(x)}{Q(x)} \to 0$.
> - **Roots**: $\sqrt{x^{2}} = \lvert x \rvert$; for the form $\infty - \infty$ with a root, multiply by the conjugate.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 3.5.5
Question: [[CAL1 HW 3.5 Questions#ST 3.5.5|ST 3.5.5]]

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
> ![ST 3.5.5 figure|400](../Attachments/CAL1%20HW%203.5%20Solutions%20fig%205.png)
>
> \# $y'$ by the [[Product Rule]] and the Chain Rule, then factor out $(x - 4)^{2}$. At $x = 4$, $y'(4) = 0$ but $(x - 4)^{2} \ge 0$ keeps $y'$ positive on both sides: no extreme value, but an inflection point with a horizontal tangent, as at $t = 0$ in [[CAL1 HW 3.3 Solutions#ST 3.3.43|Exercise 3.3.43]]. $y(2) = 2 \cdot (-2)^{3} = -16$.

### ST 3.5.9
Question: [[CAL1 HW 3.5 Questions#ST 3.5.9|ST 3.5.9]]

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
> ![ST 3.5.9 figure|440](../Attachments/CAL1%20HW%203.5%20Solutions%20fig%209.png)
>
> \# Long division gives $y = 2 - \frac{1}{x + 2}$: the hyperbola $y = -\frac{1}{x}$ moved 2 left and 2 up, which explains both asymptotes and the shape at once. $y''$ comes from $y' = (x + 2)^{-2}$ by the Chain Rule.

### ST 3.5.23
Question: [[CAL1 HW 3.5 Questions#ST 3.5.23|ST 3.5.23]]

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
> ![ST 3.5.23 figure|440](../Attachments/CAL1%20HW%203.5%20Solutions%20fig%2023.png)
>
> \# Where $x + \tfrac{1}{2}$ comes from: complete the square, $x^{2} + x - 2 = \left(x + \tfrac{1}{2}\right)^{2} - \tfrac{9}{4}$, so for large $\lvert x \rvert$ the root is close to $\left\lvert x + \tfrac{1}{2} \right\rvert$. For $y''$, write $y' = \frac{2x + 1}{2y}$: then $y'' = \frac{2 \cdot 2y - (2x + 1) \cdot 2y'}{4y^{2}} = \frac{4y^{2} - (2x + 1)^{2}}{4y^{3}} = \frac{-9}{4y^{3}}$. At $x = -2$ and $x = 1$ the tangent is vertical ($\lvert y' \rvert \to \infty$); the value $0$ there is the absolute minimum, but endpoints are not local extreme points.

### ST 3.5.29
Question: [[CAL1 HW 3.5 Questions#ST 3.5.29|ST 3.5.29]]

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
> ![ST 3.5.29 figure|440](../Attachments/CAL1%20HW%203.5%20Solutions%20fig%2029.png)
>
> \# $x^{2/3} = (\sqrt[3]{x})^{2} > 0$ for $x \ne 0$, so $y'$ has the sign of $x^{2/3} - 1$, which is positive exactly when $\lvert x \rvert > 1$; $x^{5/3}$ has the sign of $x$. At $0$, $y'(x) \to -\infty$: the inflection point $(0, 0)$ has a vertical tangent. $x^{2/3} = 3 \iff \lvert x \rvert = 3^{3/2} = 3\sqrt{3}$. Because $y$ is odd, the maximum at $-1$ and the minimum at $1$ mirror each other.

### ST 3.5.35
Question: [[CAL1 HW 3.5 Questions#ST 3.5.35|ST 3.5.35]]

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
> ![ST 3.5.35 figure|360](../Attachments/CAL1%20HW%203.5%20Solutions%20fig%2035.png)
>
> \# $(\sec^{2}x)' = 2\sec x \cdot (\sec x)' = 2\sec x \cdot \sec x\tan x$ by the Chain Rule. On the domain, $x$ and $\tan x$ always have the same sign, which gives both E and G without a sign chart.

### ST 3.5.51
Question: [[CAL1 HW 3.5 Questions#ST 3.5.51|ST 3.5.51]]

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
Question: [[CAL1 HW 3.5 Questions#ST 3.5.53|ST 3.5.53]]

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
> ![ST 3.5.53 figure|440](../Attachments/CAL1%20HW%203.5%20Solutions%20fig%2053.png)
>
> \# Long division: $x^{2} = (x - 1)(x + 1) + 1$. Differentiating the divided form $x + 1 + (x - 1)^{-1}$ is quicker than the Quotient Rule and gives $y''$ at once. Right of $1$ the curve lies above its asymptote ($\frac{1}{x - 1} > 0$), left of $1$ below it.

### ST 3.5.55
Question: [[CAL1 HW 3.5 Questions#ST 3.5.55|ST 3.5.55]]

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
> ![ST 3.5.55 figure|440](../Attachments/CAL1%20HW%203.5%20Solutions%20fig%2055.png)
>
> \# Here no long division is needed: dividing each term by $x^{2}$ gives $x + \frac{4}{x^{2}}$. Since $\frac{4}{x^{2}} > 0$, the whole curve lies above its slant asymptote $y = x$. The vertical asymptote is the $y$-axis itself.

### ST 3.5.57
Question: [[CAL1 HW 3.5 Questions#ST 3.5.57|ST 3.5.57]]

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
> ![ST 3.5.57 figure|440](../Attachments/CAL1%20HW%203.5%20Solutions%20fig%2057.png)
>
> \# Long division: $2x^{3} + x^{2} + 1 = (x^{2} + 1)(2x + 1) - 2x$. For $y''$, use $\left(\frac{x}{x^{2} + 1}\right)'' = \frac{2x(x^{2} - 3)}{(x^{2} + 1)^{3}}$ from [[CAL1 HW 3.4 Solutions#ST 3.4.51|Exercise 3.4.51]], so $y'' = -2 \cdot \frac{2x(x^{2} - 3)}{(x^{2} + 1)^{3}}$. $y(\sqrt{3}) = 2\sqrt{3} + 1 - \frac{2\sqrt{3}}{4} = 1 + \frac{3\sqrt{3}}{2}$. The factor $2x^{2} - x + 1$ has discriminant $1 - 8 < 0$, so $-1$ is the only $x$-intercept. The curve crosses its asymptote at $x = 0$: left of $0$ it lies above the line ($-\frac{2x}{x^{2} + 1} > 0$), right of $0$ below it.

### ST 3.5.59
Question: [[CAL1 HW 3.5 Questions#ST 3.5.59|ST 3.5.59]]

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
> ![ST 3.5.59 figure|400](../Attachments/CAL1%20HW%203.5%20Solutions%20fig%2059.png)
>
> \# For $x \to -\infty$ the asymptote is $y = -2x$, not $y = 2x$: there $\sqrt{4x^{2}} = 2\lvert x \rvert = -2x$. The curve lies above both asymptotes, because $\sqrt{4x^{2} + 9} > \sqrt{4x^{2}} = 2\lvert x \rvert$. It is the upper half of the hyperbola $y^{2} - 4x^{2} = 9$ (compare Exercise 61).

### ST 3.5.61
Question: [[CAL1 HW 3.5 Questions#ST 3.5.61|ST 3.5.61]]

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
