---
course: [CAL1]
semester: "115-1"
chapter: ["2.6"]
tags: [calculus, homework, solutions, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §2.6, pp. 164-169, scanned PDF (implicit differentiation)"
created: 2026-11-08
questions: "[[CAL1 HW 2.6 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 2.6 Questions#ST 2.6.3\|ST 2.6.3]] | (a) $y' = -\sqrt{y}/\sqrt{x}$; (b) $y' = 1 - 1/\sqrt{x}$; (c) they agree |
| [[CAL1 HW 2.6 Questions#ST 2.6.5\|ST 2.6.5]] | $y' = \frac{2y - x}{y - 2x}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.7\|ST 2.6.7]] | $y' = -\frac{4x^{3} + 2xy^{2}}{2x^{2}y + 3y^{2}}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.9\|ST 2.6.9]] | $y' = \frac{2x - y^{2} - 1}{2xy + 3y^{2} + 1}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.15\|ST 2.6.15]] | $y' = \frac{y\sec^{2}(x/y) - y^{2}}{y^{2} + x\sec^{2}(x/y)}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.17\|ST 2.6.17]] | $y' = \frac{8x^{3}\sqrt{x + y} - 1}{1 - 8y^{3}\sqrt{x + y}}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.19\|ST 2.6.19]] | $y' = \frac{4xy\sqrt{xy} - y}{x - 2x^{2}\sqrt{xy}}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.21\|ST 2.6.21]] | $f'(1) = -\tfrac{16}{13}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.24\|ST 2.6.24]] | $\frac{dx}{dy} = \frac{x\sec^{2}y - \sec x}{y\sec x\tan x - \tan y}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.25\|ST 2.6.25]] | $y = \tfrac{1}{2}x$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.29\|ST 2.6.29]] | $y = \tfrac{3}{4}x - \tfrac{1}{2}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.31\|ST 2.6.31]] | $y = x + \tfrac{1}{2}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.33\|ST 2.6.33]] | $y = -\tfrac{9}{13}x + \tfrac{40}{13}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.37\|ST 2.6.37]] | $y'' = -\frac{1}{4y^{3}}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.39\|ST 2.6.39]] | $y'' = \frac{\cos x\cos^{2}y + \sin^{2}x\sin y}{\cos^{3}y}$ |
| [[CAL1 HW 2.6 Questions#ST 2.6.46\|ST 2.6.46]] | Proof |
| [[CAL1 HW 2.6 Questions#ST 2.6.48\|ST 2.6.48]] | Proof |
| [[CAL1 HW 2.6 Questions#ST 2.6.61\|ST 2.6.61]] | $(1, 1)$ and $(-1, -1)$ |

## ST §2.6 Implicit Differentiation

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Implicit Differentiation]]**: regard $y$ as a function of $x$, differentiate both sides of the equation with respect to $x$, and apply the [[Chain Rule]] to every term that contains $y$: $\dfrac{d}{dx}\,g(y) = g'(y)\,y'$. For example $\dfrac{d}{dx}(y^{3}) = 3y^{2}y'$ and $\dfrac{d}{dx}(\cos y) = -\sin y \cdot y'$. Then collect the terms with $y'$ on one side and solve for $y'$.
> - **Products and quotients that contain $y$**: $\dfrac{d}{dx}(xy) = y + xy'$ ([[Product Rule]]) and $\dfrac{d}{dx}\dfrac{x}{y} = \dfrac{y - xy'}{y^{2}}$ ([[Quotient Rule]]).
> - **[[Tangent Line]] at $(a, b)$**: substitute the point right after differentiating, solve for the slope $m = y'$, then $y - b = m(x - a)$.
> - **$y''$** ([[Higher Derivatives]]): differentiate the formula for $y'$ again, remembering that $y$ still depends on $x$; replace $y'$ by its formula, and simplify with the original equation.
> - Each answer is written as on an exam paper: differentiate both sides, collect the $y'$ terms, solve, then a Hence line. The formula for $y'$ may contain both $x$ and $y$; it holds at the points of the curve where its denominator is not $0$. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 2.6.3
Question: [[CAL1 HW 2.6 Questions#ST 2.6.3|ST 2.6.3]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> &\frac{d}{dx}\left(\sqrt{x} + \sqrt{y}\right) = \frac{d}{dx}(1) \\
> &\frac{1}{2\sqrt{x}} + \frac{1}{2\sqrt{y}}\,y' = 0 \\
> &\implies y' = -\frac{\sqrt{y}}{\sqrt{x}}
> \end{aligned}
> $$
>
> **(b)**
> $$
> \begin{aligned}
> &\sqrt{y} = 1 - \sqrt{x} \implies y = (1 - \sqrt{x})^{2} = 1 - 2\sqrt{x} + x \qquad (0 \le x \le 1) \\
> &\implies y' = -\frac{1}{\sqrt{x}} + 1
> \end{aligned}
> $$
>
> **(c)**
> $$
> -\frac{\sqrt{y}}{\sqrt{x}} = -\frac{1 - \sqrt{x}}{\sqrt{x}} = -\frac{1}{\sqrt{x}} + 1 \qquad (\sqrt{y} = 1 - \sqrt{x})
> $$
> Hence $y' = -\dfrac{\sqrt{y}}{\sqrt{x}} = 1 - \dfrac{1}{\sqrt{x}}$ for $0 < x < 1$, and (a) and (b) agree.
>
> \# In (a), $\dfrac{d}{dx}\sqrt{y} = \dfrac{1}{2\sqrt{y}} \cdot y'$ by the Chain Rule: the outer function is $\sqrt{\ }$, the inner function is $y$. In (b), $\sqrt{y} = 1 - \sqrt{x}$ needs $1 - \sqrt{x} \ge 0$, so the curve lives only on $0 \le x \le 1$. In (c), the two answers look different because (a) still contains $y$; replacing $\sqrt{y}$ by $1 - \sqrt{x}$ (read off the original equation) turns one into the other.

### ST 2.6.5
Question: [[CAL1 HW 2.6 Questions#ST 2.6.5|ST 2.6.5]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dx}\left(x^{2} - 4xy + y^{2}\right) = \frac{d}{dx}(4) \\
> &2x - 4(y + xy') + 2yy' = 0 \\
> &\implies (2y - 4x)\,y' = 4y - 2x \\
> &\implies y' = \frac{4y - 2x}{2y - 4x} = \frac{2y - x}{y - 2x}
> \end{aligned}
> $$
> Hence $\dfrac{dy}{dx} = \dfrac{2y - x}{y - 2x}$.
>
> \# The middle term needs the Product Rule: $\dfrac{d}{dx}(4xy) = 4(1 \cdot y + x \cdot y')$. Writing only $4xy'$ (forgetting the term $4y$) is the most common mistake.

### ST 2.6.7
Question: [[CAL1 HW 2.6 Questions#ST 2.6.7|ST 2.6.7]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dx}\left(x^{4} + x^{2}y^{2} + y^{3}\right) = \frac{d}{dx}(5) \\
> &4x^{3} + \left(2xy^{2} + x^{2} \cdot 2yy'\right) + 3y^{2}y' = 0 \\
> &\implies (2x^{2}y + 3y^{2})\,y' = -4x^{3} - 2xy^{2} \\
> &\implies y' = -\frac{4x^{3} + 2xy^{2}}{2x^{2}y + 3y^{2}}
> \end{aligned}
> $$
> Hence $\dfrac{dy}{dx} = -\dfrac{4x^{3} + 2xy^{2}}{2x^{2}y + 3y^{2}}$.
>
> \# $\dfrac{d}{dx}(x^{2}y^{2})$: the Product Rule gives $(x^{2})' \cdot y^{2} + x^{2} \cdot (y^{2})'$, and $(y^{2})' = 2y\,y'$ by the Chain Rule. Factored, the answer is $y' = -\dfrac{2x(2x^{2} + y^{2})}{y(2x^{2} + 3y)}$.

### ST 2.6.9
Question: [[CAL1 HW 2.6 Questions#ST 2.6.9|ST 2.6.9]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{x^{2}}{x + y} = y^{2} + 1 \implies x^{2} = (y^{2} + 1)(x + y) = xy^{2} + y^{3} + x + y && (x + y \ne 0) \\
> &\frac{d}{dx}: \ 2x = \left(y^{2} + x \cdot 2yy'\right) + 3y^{2}y' + 1 + y' \\
> &\implies (2xy + 3y^{2} + 1)\,y' = 2x - y^{2} - 1 \\
> &\implies y' = \frac{2x - y^{2} - 1}{2xy + 3y^{2} + 1}
> \end{aligned}
> $$
> Hence $\dfrac{dy}{dx} = \dfrac{2x - y^{2} - 1}{2xy + 3y^{2} + 1}$.
>
> \# Clearing the denominator first avoids the Quotient Rule; it is allowed because $x + y \ne 0$ wherever the equation makes sense. With the Quotient Rule directly one gets $y' = \dfrac{x^{2} + 2xy}{x^{2} + 2y(x + y)^{2}}$. The two formulas differ, but they give the same value at every point of the curve, because each can be turned into the other with the equation of the curve (checked numerically at several points of the curve).

### ST 2.6.15
Question: [[CAL1 HW 2.6 Questions#ST 2.6.15|ST 2.6.15]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dx}\tan\frac{x}{y} = \frac{d}{dx}(x + y) \\
> &\sec^{2}\frac{x}{y} \cdot \frac{y - xy'}{y^{2}} = 1 + y' && \text{(Chain Rule, Quotient Rule)} \\
> &\implies y\sec^{2}\frac{x}{y} - xy'\sec^{2}\frac{x}{y} = y^{2} + y^{2}y' && (\times\, y^{2}) \\
> &\implies \left(y^{2} + x\sec^{2}\frac{x}{y}\right) y' = y\sec^{2}\frac{x}{y} - y^{2} \\
> &\implies y' = \frac{y\sec^{2}(x/y) - y^{2}}{y^{2} + x\sec^{2}(x/y)}
> \end{aligned}
> $$
> Hence $\dfrac{dy}{dx} = \dfrac{y\sec^{2}(x/y) - y^{2}}{y^{2} + x\sec^{2}(x/y)}$.
>
> \# The inner function is $x/y$, a quotient in which $y$ depends on $x$: $\dfrac{d}{dx}\dfrac{x}{y} = \dfrac{1 \cdot y - x \cdot y'}{y^{2}}$. Multiplying by $y^{2}$ removes the fraction before collecting the $y'$ terms.

### ST 2.6.17
Question: [[CAL1 HW 2.6 Questions#ST 2.6.17|ST 2.6.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dx}\sqrt{x + y} = \frac{d}{dx}\left(x^{4} + y^{4}\right) \\
> &\frac{1 + y'}{2\sqrt{x + y}} = 4x^{3} + 4y^{3}y' \\
> &\implies 1 + y' = 8x^{3}\sqrt{x + y} + 8y^{3}\sqrt{x + y}\;y' && (\times\, 2\sqrt{x + y}) \\
> &\implies \left(1 - 8y^{3}\sqrt{x + y}\right) y' = 8x^{3}\sqrt{x + y} - 1 \\
> &\implies y' = \frac{8x^{3}\sqrt{x + y} - 1}{1 - 8y^{3}\sqrt{x + y}}
> \end{aligned}
> $$
> Hence $\dfrac{dy}{dx} = \dfrac{8x^{3}\sqrt{x + y} - 1}{1 - 8y^{3}\sqrt{x + y}}$.
>
> \# $\dfrac{d}{dx}\sqrt{x + y} = \dfrac{1}{2\sqrt{x + y}} \cdot (x + y)' = \dfrac{1 + y'}{2\sqrt{x + y}}$.

### ST 2.6.19
Question: [[CAL1 HW 2.6 Questions#ST 2.6.19|ST 2.6.19]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dx}\sqrt{xy} = \frac{d}{dx}\left(1 + x^{2}y\right) \\
> &\frac{y + xy'}{2\sqrt{xy}} = 2xy + x^{2}y' \\
> &\implies y + xy' = 4xy\sqrt{xy} + 2x^{2}\sqrt{xy}\;y' && (\times\, 2\sqrt{xy}) \\
> &\implies \left(x - 2x^{2}\sqrt{xy}\right) y' = 4xy\sqrt{xy} - y \\
> &\implies y' = \frac{4xy\sqrt{xy} - y}{x - 2x^{2}\sqrt{xy}}
> \end{aligned}
> $$
> Hence $\dfrac{dy}{dx} = \dfrac{4xy\sqrt{xy} - y}{x - 2x^{2}\sqrt{xy}}$.
>
> \# Inside the root, $(xy)' = y + xy'$ by the Product Rule; on the right, $(x^{2}y)' = 2xy + x^{2}y'$.

### ST 2.6.21
Question: [[CAL1 HW 2.6 Questions#ST 2.6.21|ST 2.6.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dx}: \ f'(x) + 2x[f(x)]^{3} + x^{2} \cdot 3[f(x)]^{2}f'(x) = 0 \\
> &x = 1,\ f(1) = 2: \ f'(1) + 2 \cdot 8 + 3 \cdot 4\,f'(1) = 0 \\
> &\implies 13f'(1) = -16 \implies f'(1) = -\frac{16}{13}
> \end{aligned}
> $$
> Hence $f'(1) = -\dfrac{16}{13}$.
>
> \# Here $f(x)$ plays the role of $y$: $\dfrac{d}{dx}[f(x)]^{3} = 3[f(x)]^{2}f'(x)$. Substitute $x = 1$ and $f(1) = 2$ right after differentiating; there is no need to find a formula for $f'(x)$.

### ST 2.6.24
Question: [[CAL1 HW 2.6 Questions#ST 2.6.24|ST 2.6.24]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dy}(y\sec x) = \frac{d}{dy}(x\tan y) && (x' = dx/dy) \\
> &1 \cdot \sec x + y \cdot \sec x\tan x \cdot x' = x'\tan y + x\sec^{2}y \\
> &\implies (y\sec x\tan x - \tan y)\,x' = x\sec^{2}y - \sec x \\
> &\implies \frac{dx}{dy} = \frac{x\sec^{2}y - \sec x}{y\sec x\tan x - \tan y}
> \end{aligned}
> $$
> Hence $\dfrac{dx}{dy} = \dfrac{x\sec^{2}y - \sec x}{y\sec x\tan x - \tan y}$.
>
> \# The roles are swapped: now $x$ is the function (of $y$), so the factor $x' = dx/dy$ appears on every term that contains $x$, while $\dfrac{d}{dy}(y) = 1$ and $\dfrac{d}{dy}(\tan y) = \sec^{2}y$ need no extra factor. As a check, $\dfrac{dx}{dy} = 1 \Big/ \dfrac{dy}{dx}$ wherever both are nonzero.

### ST 2.6.25
Question: [[CAL1 HW 2.6 Questions#ST 2.6.25|ST 2.6.25]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dx}(y\sin 2x) = \frac{d}{dx}(x\cos 2y) \\
> &y'\sin 2x + y \cdot 2\cos 2x = \cos 2y + x \cdot (-2\sin 2y)\,y' \\
> &\left(\tfrac{\pi}{2}, \tfrac{\pi}{4}\right): \ \sin\pi = 0,\ \cos\pi = -1,\ \cos\tfrac{\pi}{2} = 0,\ \sin\tfrac{\pi}{2} = 1 \\
> &\implies 0 + \tfrac{\pi}{4} \cdot 2 \cdot (-1) = 0 - \tfrac{\pi}{2} \cdot 2 \cdot 1 \cdot y' \\
> &\implies -\tfrac{\pi}{2} = -\pi y' \implies y' = \tfrac{1}{2} \\[4pt]
> &y - \tfrac{\pi}{4} = \tfrac{1}{2}\left(x - \tfrac{\pi}{2}\right) \implies y = \tfrac{1}{2}x
> \end{aligned}
> $$
> Hence the tangent line is $y = \tfrac{1}{2}x$.
>
> \# The point lies on the curve: $\tfrac{\pi}{4}\sin\pi = 0 = \tfrac{\pi}{2}\cos\tfrac{\pi}{2}$. Substituting before solving for $y'$ turns the trigonometric equation into a linear one in $y'$.

### ST 2.6.29
Question: [[CAL1 HW 2.6 Questions#ST 2.6.29|ST 2.6.29]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dx}\left(x^{2} - xy - y^{2}\right) = \frac{d}{dx}(1) \\
> &2x - (y + xy') - 2yy' = 0 \\
> &(2, 1): \ 4 - 1 - 2y' - 2y' = 0 \implies y' = \tfrac{3}{4} \\[4pt]
> &y - 1 = \tfrac{3}{4}(x - 2) \implies y = \tfrac{3}{4}x - \tfrac{1}{2}
> \end{aligned}
> $$
> Hence the tangent line is $y = \tfrac{3}{4}x - \tfrac{1}{2}$.
>
> \# In general $y' = \dfrac{2x - y}{x + 2y}$; at $(2, 1)$ this is $\tfrac{3}{4}$.

### ST 2.6.31
Question: [[CAL1 HW 2.6 Questions#ST 2.6.31|ST 2.6.31]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dx}\left(x^{2} + y^{2}\right) = \frac{d}{dx}(2x^{2} + 2y^{2} - x)^{2} \\
> &2x + 2yy' = 2(2x^{2} + 2y^{2} - x)(4x + 4yy' - 1) && \text{(Chain Rule)} \\
> &\left(0, \tfrac{1}{2}\right): \ 2x^{2} + 2y^{2} - x = \tfrac{1}{2},\quad 4x + 4yy' - 1 = 2y' - 1 \\
> &\implies 0 + y' = 2 \cdot \tfrac{1}{2}\,(2y' - 1) = 2y' - 1 \implies y' = 1 \\[4pt]
> &y - \tfrac{1}{2} = 1 \cdot (x - 0) \implies y = x + \tfrac{1}{2}
> \end{aligned}
> $$
> Hence the tangent line is $y = x + \tfrac{1}{2}$.
>
> ![ST 2.6.31 figure|320](../Attachments/CAL1%20HW%202.6%20Solutions%20fig%2031.png)
>
> \# Differentiate the right side with the Chain Rule (outer function $u^{2}$, inner function $u = 2x^{2} + 2y^{2} - x$) and do not expand it; substituting the point first keeps the numbers small.

### ST 2.6.33
Question: [[CAL1 HW 2.6 Questions#ST 2.6.33|ST 2.6.33]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dx}\,2(x^{2} + y^{2})^{2} = \frac{d}{dx}\,25(x^{2} - y^{2}) \\
> &4(x^{2} + y^{2})(2x + 2yy') = 25(2x - 2yy') \\
> &(3, 1): \ x^{2} + y^{2} = 10 \implies 40(6 + 2y') = 25(6 - 2y') \\
> &\implies 240 + 80y' = 150 - 50y' \implies 130y' = -90 \implies y' = -\tfrac{9}{13} \\[4pt]
> &y - 1 = -\tfrac{9}{13}(x - 3) \implies y = -\tfrac{9}{13}x + \tfrac{40}{13}
> \end{aligned}
> $$
> Hence the tangent line is $y = -\tfrac{9}{13}x + \tfrac{40}{13}$.
>
> ![ST 2.6.33 figure|440](../Attachments/CAL1%20HW%202.6%20Solutions%20fig%2033.png)
>
> \# The point lies on the curve: $2 \cdot 10^{2} = 200 = 25 \cdot 8$. The slope is negative because $(3, 1)$ is on the upper right arc of the loop, past its highest point.

### ST 2.6.37
Question: [[CAL1 HW 2.6 Questions#ST 2.6.37|ST 2.6.37]]

> [!solution] Solution
> $$
> \begin{aligned}
> &2x + 8yy' = 0 \implies y' = -\frac{x}{4y} \\[4pt]
> y'' &= -\frac{1 \cdot 4y - x \cdot 4y'}{(4y)^{2}} = -\frac{y - xy'}{4y^{2}} && \text{(Quotient Rule)} \\
> &= -\frac{y + \frac{x^{2}}{4y}}{4y^{2}} = -\frac{4y^{2} + x^{2}}{16y^{3}} && (y' = -\tfrac{x}{4y}) \\
> &= -\frac{4}{16y^{3}} = -\frac{1}{4y^{3}} && (x^{2} + 4y^{2} = 4)
> \end{aligned}
> $$
> Hence $y'' = -\dfrac{1}{4y^{3}}$.
>
> \# In the last step the original equation simplifies the numerator: always look for $x^{2} + 4y^{2}$ (or whatever the equation gives) after substituting $y'$.

### ST 2.6.39
Question: [[CAL1 HW 2.6 Questions#ST 2.6.39|ST 2.6.39]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\cos y \cdot y' - \sin x = 0 \implies y' = \frac{\sin x}{\cos y} \\[4pt]
> y'' &= \frac{\cos x \cdot \cos y - \sin x \cdot (-\sin y)\,y'}{\cos^{2}y} && \text{(Quotient Rule)} \\
> &= \frac{\cos x\cos y + \sin x\sin y \cdot \frac{\sin x}{\cos y}}{\cos^{2}y} && (y' = \tfrac{\sin x}{\cos y}) \\
> &= \frac{\cos x\cos^{2}y + \sin^{2}x\sin y}{\cos^{3}y} && (\times\, \tfrac{\cos y}{\cos y})
> \end{aligned}
> $$
> Hence $y'' = \dfrac{\cos x\cos^{2}y + \sin^{2}x\sin y}{\cos^{3}y}$.
>
> \# $\dfrac{d}{dx}(\cos y) = -\sin y \cdot y'$: the factor $y'$ is easy to forget. Then replace $y'$ by $\dfrac{\sin x}{\cos y}$ and clear the small fraction.

### ST 2.6.46
Question: [[CAL1 HW 2.6 Questions#ST 2.6.46|ST 2.6.46]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{pf: } \frac{d}{dx}\left(\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}}\right) = 0 \implies \frac{2x}{a^{2}} + \frac{2yy'}{b^{2}} = 0 \implies y' = -\frac{b^{2}x}{a^{2}y} \qquad (y \ne 0) \\[6pt]
> &\text{Case } y_{0} \ne 0: \text{ the tangent at } (x_{0}, y_{0}) \text{ is} \\
> &\qquad y - y_{0} = -\frac{b^{2}x_{0}}{a^{2}y_{0}}(x - x_{0}) \\
> &\implies \frac{y_{0}y}{b^{2}} - \frac{y_{0}^{2}}{b^{2}} = -\frac{x_{0}x}{a^{2}} + \frac{x_{0}^{2}}{a^{2}} && (\times\, \tfrac{y_{0}}{b^{2}}) \\
> &\implies \frac{x_{0}x}{a^{2}} + \frac{y_{0}y}{b^{2}} = \frac{x_{0}^{2}}{a^{2}} + \frac{y_{0}^{2}}{b^{2}} = 1 && ((x_{0}, y_{0}) \text{ is on the ellipse}) \\[6pt]
> &\text{Case } y_{0} = 0: \ x_{0} = \pm a, \text{ and the tangent is the vertical line } x = \pm a; \\
> &\qquad \frac{x_{0}x}{a^{2}} + \frac{0 \cdot y}{b^{2}} = 1 \iff x = \frac{a^{2}}{x_{0}} = \pm a, \text{ the same line.} \\[6pt]
> &\text{Hence the tangent at } (x_{0}, y_{0}) \text{ has equation } \frac{x_{0}x}{a^{2}} + \frac{y_{0}y}{b^{2}} = 1. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The slope formula divides by $y$, so the two points $(\pm a, 0)$, where the tangent is vertical, are checked separately; grading deducts points for a missing case. The result is easy to remember: in the equation of the ellipse, replace $x^{2}$ by $x_{0}x$ and $y^{2}$ by $y_{0}y$.

### ST 2.6.48
Question: [[CAL1 HW 2.6 Questions#ST 2.6.48|ST 2.6.48]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{pf: Let } (x_{0}, y_{0}) \text{ be a point of the curve with } x_{0} > 0,\ y_{0} > 0. \\
> &\frac{1}{2\sqrt{x}} + \frac{y'}{2\sqrt{y}} = 0 \implies y' = -\frac{\sqrt{y}}{\sqrt{x}} \\
> &\text{tangent: } y - y_{0} = -\frac{\sqrt{y_{0}}}{\sqrt{x_{0}}}(x - x_{0}) \\
> &x\text{-intercept } (y = 0): \ x - x_{0} = \frac{\sqrt{x_{0}}}{\sqrt{y_{0}}}\,y_{0} \implies x = x_{0} + \sqrt{x_{0}}\sqrt{y_{0}} \\
> &y\text{-intercept } (x = 0): \ y - y_{0} = \frac{\sqrt{y_{0}}}{\sqrt{x_{0}}}\,x_{0} \implies y = y_{0} + \sqrt{x_{0}}\sqrt{y_{0}} \\
> &\text{sum} = x_{0} + 2\sqrt{x_{0}}\sqrt{y_{0}} + y_{0} = \left(\sqrt{x_{0}} + \sqrt{y_{0}}\right)^{2} = \left(\sqrt{c}\right)^{2} = c && ((x_{0}, y_{0}) \text{ is on the curve}) \\[6pt]
> &\text{Hence the intercepts of every tangent line add up to } c. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# At the endpoints $(c, 0)$ and $(0, c)$ the tangent is a coordinate axis itself ($y' = 0$ at $(c, 0)$, a vertical tangent at $(0, c)$), so it has no pair of intercepts; that is why the proof takes $x_{0}, y_{0} > 0$. Exercise 3 is the case $c = 1$.

### ST 2.6.61
Question: [[CAL1 HW 2.6 Questions#ST 2.6.61|ST 2.6.61]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\frac{d}{dx}\left(x^{2}y^{2} + xy\right) = \frac{d}{dx}(2) \\
> &\left(2xy^{2} + 2x^{2}yy'\right) + (y + xy') = 0 \\
> &\implies (2x^{2}y + x)\,y' = -(2xy^{2} + y) \implies y' = -\frac{y(2xy + 1)}{x(2xy + 1)} = -\frac{y}{x} \\
> &\text{on the curve: } (xy)^{2} + xy - 2 = 0 \implies (xy - 1)(xy + 2) = 0 \implies xy = 1 \text{ or } xy = -2 \\
> &\qquad \implies 2xy + 1 = 3 \text{ or } -3,\ \text{never } 0 \quad \text{(so the cancellation is allowed)} \\[4pt]
> &y' = -1 \iff -\frac{y}{x} = -1 \iff y = x \\
> &\implies x^{4} + x^{2} = 2 \implies (x^{2} + 2)(x^{2} - 1) = 0 \implies x^{2} = 1 \implies x = \pm 1
> \end{aligned}
> $$
> Hence the points are $(1, 1)$ and $(-1, -1)$.
>
> \# Check: $1 \cdot 1 + 1 = 2$ and $(-1)^{2}(-1)^{2} + (-1)(-1) = 2$. The curve is the two hyperbolas $xy = 1$ and $xy = -2$; on $xy = 1$, $y = 1/x$ gives $y' = -1/x^{2} = -y/x$ directly. The line $y = x$ meets only $xy = 1$, since $x^{2} = -2$ has no solution.
