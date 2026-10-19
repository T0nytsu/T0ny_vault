---
course: [CAL1]
semester: "115-1"
chapter: ["1.7", "1.8", "2.1"]
tags: [calculus, quiz, limits, continuity, derivatives]
source:
  - "CAL1 G-Quiz 2 (2026-10-05, sections 1.7-1.8, 2.1), graded scan"
  - "[[CAL1 Quiz 02 p1.jpg]]"
created: 2026-10-19
score: "12/12"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
> [!abstract] Result: 12/12
> - Q1 Proof by the [[Precise Definition of a Limit|ε, δ definition of a limit]]: 6/6.
> - Q2 [[Continuity]] with a constant: 3/3. The grader added "If" and "at $x=3$" to the line that states the condition for continuity.
> - Q3 Short-Answer Questions: 3/3. The value of the limit in (b) is $2$, not $1$, but the [[Derivatives of Trigonometric Functions|derivatives of trigonometric functions]] had not been taught yet, so that blank was given free.

## Q1 Epsilon-Delta Proof

> [!question]
> 1. (6 points) Prove the statement using the $\varepsilon$, $\delta$ definition of a limit.
> $$
> \lim_{x \to 3} (x^2 + 2x - 13) = 2
> $$

> [!attempt] My answer: 6/6
> $$
> \begin{aligned}
> &\text{Given any } \varepsilon > 0, \text{ we chouse } \delta = \min\left\{1, \frac{\varepsilon}{9}\right\} > 0 \implies \delta \le 1,\ \delta \le \frac{\varepsilon}{9} \\
> &\text{If } 0 < \lvert x-3 \rvert < \delta \implies \lvert x-3 \rvert < 1 \implies -1 < x-3 < 1 \implies 7 < x+5 < 9 \implies 7 < \lvert x+5 \rvert < 9 \\
> &\qquad \lvert x^2+2x-13-2 \rvert = \lvert x^2+2x-15 \rvert = \lvert x+5 \rvert \lvert x-3 \rvert < \lvert x+5 \rvert \cdot \delta < 9 \cdot \delta \le 9 \cdot \frac{\varepsilon}{9} = \varepsilon \\
> &\text{Hence } \lim_{x \to 3} (x^2+2x-13) = 2 \text{ by the definition of limit.}
> \end{aligned}
> $$
> The grader wrote −0 beside the third line and drew a large ✓ across the last line.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{Given any } \varepsilon > 0, \text{ we choose } \delta = \min\left\{1, \frac{\varepsilon}{9}\right\} > 0 \implies \delta \le 1,\ \delta \le \frac{\varepsilon}{9}. \\[6pt]
> &\text{If } 0 < \lvert x-3 \rvert < \delta, \text{ then} \\
> &\qquad \lvert x-3 \rvert < 1 \implies -1 < x-3 < 1 \implies 7 < x+5 < 9 \implies \lvert x+5 \rvert < 9, \\
> &\qquad \lvert (x^2+2x-13) - 2 \rvert = \lvert x^2+2x-15 \rvert = \lvert x+5 \rvert \lvert x-3 \rvert < 9\delta \le 9 \cdot \frac{\varepsilon}{9} = \varepsilon. \\[6pt]
> &\text{Hence } \lim_{x \to 3} (x^2+2x-13) = 2 \text{ by the definition of limit.} \qquad \blacksquare
> \end{aligned}
> $$
> \# How $\delta$ is found on scratch paper: $\lvert f(x) - 2 \rvert = \lvert x+5 \rvert \lvert x-3 \rvert$, and $\delta$ controls only $\lvert x-3 \rvert$. First $\delta \le 1$ keeps $x$ in $(2, 4)$, so $\lvert x+5 \rvert < 9$; then $9\lvert x-3 \rvert < \varepsilon$ needs $\lvert x-3 \rvert < \frac{\varepsilon}{9}$. The minimum makes both hold at once. This is the proof written in the quiz; only the bound $7 < \lvert x+5 \rvert$, which is not needed, is left out.

## Q2 Continuity

> [!question]
> 2. (3 points) For what value of the constant $c$ is **the function $f$ continuous on** $(-\infty, \infty)$?
> $$
> f(x) = \begin{cases} cx^2 + 2x & \text{if } x < 3 \\ x^3 - cx & \text{if } x \ge 3 \end{cases}
> $$

> [!attempt] My answer: 3/3
> $$
> \begin{aligned}
> &cx^2 + 2x \text{ is polynominal, so it is continuous } \forall\, x \in \mathbb{R} \\
> &x^3 - cx \text{ is polynominal, so it is continuous } \forall\, x \in \mathbb{R} \\
> &f \text{ is continuous} \iff \lim_{x \to 3^{-}} f(x) = \lim_{x \to 3^{+}} f(x) = f(3) \\
> &\therefore \lim_{x \to 3^{-}} (cx^2 + 2x) = \lim_{x \to 3^{+}} (x^3 - cx) = 3^3 - c \cdot 3 \\
> &\implies c \cdot 3^2 + 2 \cdot 3 = 3^3 - c \cdot 3 = 27 - 3c \\
> &\implies 9c + 6 = 27 - 3c = 27 - 3c \\
> &\implies 12c = 21 \\
> &\implies c = \frac{7}{4} \\
> &\text{Hence } c = \frac{7}{4}.
> \end{aligned}
> $$
> The last three lines are written in a column on the right. The grader wrote "If" in front of the third line and "at $x=3$" after "continuous", wrote −0 beside the fourth line, and drew a ✓ at $27 - 3c$.

> [!failure] Mistake: the limit condition is continuity at x = 3
> The equalities $\lim_{x \to 3^{-}} f(x) = \lim_{x \to 3^{+}} f(x) = f(3)$ say that $f$ is continuous at the single number $3$; they are not what "$f$ is continuous" means. Continuity on $(-\infty, \infty)$ comes in three parts: on $(-\infty, 3)$ and on $(3, \infty)$, $f$ equals a polynomial, so it is continuous there; at $3$, the two [[One-Sided Limit|one-sided limits]] must both equal $f(3)$. No points were taken off; the grader's "If … at $x=3$" makes the line say exactly this.

> [!solution]- Solution
> $$
> \begin{aligned}
> &x < 3:\ f(x) = cx^2 + 2x \text{ is a polynomial, so } f \text{ is continuous on } (-\infty, 3) \\
> &x > 3:\ f(x) = x^3 - cx \text{ is a polynomial, so } f \text{ is continuous on } (3, \infty) \\
> &x = 3:\ f \text{ is continuous at } 3 \iff \lim_{x \to 3^{-}} f(x) = \lim_{x \to 3^{+}} f(x) = f(3) \\[6pt]
> &\lim_{x \to 3^{-}} f(x) = \lim_{x \to 3^{-}} (cx^2 + 2x) = 9c + 6 \\
> &\lim_{x \to 3^{+}} f(x) = \lim_{x \to 3^{+}} (x^3 - cx) = 27 - 3c = f(3) \\[6pt]
> &\implies 9c + 6 = 27 - 3c \implies 12c = 21 \implies c = \frac{7}{4} \\[6pt]
> &\text{Hence } f \text{ is continuous on } (-\infty, \infty) \text{ exactly when } c = \frac{7}{4}.
> \end{aligned}
> $$
> \# $f(3)$ comes from the piece for $x \ge 3$, the same piece as the right-hand limit, so the right-hand limit always equals $f(3)$; the real condition is that the left-hand limit matches it. Each polynomial is continuous on all of $\mathbb{R}$, but it is $f$ only on its own side of $3$, which is why the number $3$ is checked separately.

## Q3 Short-Answer Questions

> [!question]
> 3. (3 points) <u>Short-Answer Questions</u>: Each limit represents the derivative of some function $f$ at some number $a$. State such an $f$ and $a$ in each case.
> - (a) $\displaystyle\lim_{h \to 0} \frac{\sqrt{9+h}-3}{h} = \underline{\qquad\qquad}$ where $f = \underline{\qquad\qquad}$ and $a = \underline{\qquad\qquad}$.
> - (a) $\displaystyle\lim_{h \to 0} \frac{\tan\left(\frac{\pi}{4}+h\right)-1}{h} = \underline{\qquad\qquad}$ where $f = \underline{\qquad\qquad}$ and $a = \underline{\qquad\qquad}$.

> [!attempt] My answer: 3/3
> - (a) $\frac{1}{6}$, $f = \sqrt{x}$ ✓, $a = 9$ ✓
> - (b) $1$, $f = \tan x$ ✓, $a = \frac{\pi}{4}$ ✓
>
> Work under the question:
> $$
> \begin{aligned}
> &\text{(a)}\quad f(x) = \sqrt{x} \\
> &\qquad \lim_{h \to 0} \frac{9+h-9}{h} \cdot \frac{1}{\sqrt{9+h}+3} = \frac{1}{6} \\[6pt]
> &\text{(b)}\quad \frac{\frac{\sin}{\cos} - 1}{h} \qquad f'\left(\tan\frac{\pi}{4}\right) <
> \end{aligned}
> $$
> In (a), $9+h-9$ and $h$ are crossed out. The work for (b) stops there; faint scratch in the right margin is not transcribed. The second item is printed as a second "(a)"; the work calls it (b), and so does this note. The grader wrote −0 beside (b). The value blank of (b) was given free, because the derivatives of trigonometric functions had not been taught yet.

> [!failure] Mistake: (b) the limit is f′(π/4), not f(π/4)
> The $-1$ in the numerator is $f(a) = \tan\frac{\pi}{4} = 1$; the limit itself is the [[Derivative|derivative]] $f'\left(\frac{\pi}{4}\right)$, the slope of $y = \tan x$ at $x = \frac{\pi}{4}$. With $(\tan x)' = \sec^2 x$, it equals $\sec^2\frac{\pi}{4} = 2$. In the scratch, $f'$ is evaluated at $\tan\frac{\pi}{4}$; it is evaluated at $a = \frac{\pi}{4}$ itself.

> [!solution]- Solution
> **(a)** $f(x) = \sqrt{x}$, $a = 9$
> $$
> \begin{aligned}
> f'(9) &= \lim_{h \to 0} \frac{\sqrt{9+h} - \sqrt{9}}{h} = \lim_{h \to 0} \frac{\sqrt{9+h} - 3}{h} \\
> &= \lim_{h \to 0} \frac{(9+h) - 9}{h\left(\sqrt{9+h} + 3\right)} = \lim_{h \to 0} \frac{1}{\sqrt{9+h} + 3} = \frac{1}{3+3} = \frac{1}{6}
> \end{aligned}
> $$
>
> **(b)** $f(x) = \tan x$, $a = \frac{\pi}{4}$
> $$
> \begin{aligned}
> &\tan\frac{\pi}{4} = 1 \implies \lim_{h \to 0} \frac{\tan\left(\frac{\pi}{4}+h\right) - 1}{h} = \lim_{h \to 0} \frac{\tan\left(\frac{\pi}{4}+h\right) - \tan\frac{\pi}{4}}{h} = f'\left(\frac{\pi}{4}\right) \\
> &f'(x) = \sec^2 x \implies f'\left(\frac{\pi}{4}\right) = \frac{1}{\cos^2\frac{\pi}{4}} = \frac{1}{\left(\frac{\sqrt{2}}{2}\right)^2} = 2
> \end{aligned}
> $$
> \# Read each limit as $\lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$: what is added to $h$ is $a$, and what is subtracted is $f(a)$. Other pairs also work, such as $f(x) = \sqrt{9+x}$, $a = 0$ in (a). Without $(\tan x)' = \sec^2 x$, which came after this quiz, the addition formula gives the same value: $\tan\left(\frac{\pi}{4}+h\right) - 1 = \frac{1+\tan h}{1-\tan h} - 1 = \frac{2\tan h}{1-\tan h}$, so the quotient is $\frac{\tan h}{h} \cdot \frac{2}{1-\tan h} \to 1 \cdot 2 = 2$.
