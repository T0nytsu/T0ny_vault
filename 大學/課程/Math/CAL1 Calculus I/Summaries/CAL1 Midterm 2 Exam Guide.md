---
course: [CAL1]
semester: "115-1"
chapter: ["2.3", "2.4", "2.5", "2.6", "2.7", "2.8", "2.9", "3.1", "3.2", "3.3", "3.4", "3.5", "3.7"]
tags: [calculus, concept, exam-prep]
aliases: [期中考二考試指南, 期中考二考點與預測題, Midterm 2 考點]
source:
  - "Stewart, Calculus 9e, §2.3–§2.9, Chapter 2 Review, §3.1–§3.5 and §3.7, pp. 133–276 (scans 2-3_Scan.pdf to 3-7_Scan.pdf)"
  - "CAL1 Mid-term Exam 1 (115-1), graded: the style, the question types, and the grading"
  - "CAL1 Index, Assigned Exercises"
  - "Answers checked with sympy"
created: 2026-11-10
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Exam Focus

> [!abstract] Midterm 2 covers §2.3–§3.7 in the three parts of Midterm 1
> **Format to expect, as in [[CAL1 Midterm 1]]:** Part I True/False ($5 \times 2$ points), Part II single or multiple choice ($8 \times 5$ points, exactly the correct set of letters), Part III computational and proof questions ($5 \times 10$ points, show all work).
>
> **Where Midterm 1 took its questions**
> - Q1 (a) is item 1 of the True-False Quiz of the Chapter 2 Review (p. 200), word for word.
> - Q2 (b) is Exercise 5 of the Chapter 2 Review (p. 200): the graphs of $f$, $f'$, and $f''$.
> - Q6 and Q7 are proofs of theorems of the text (differentiable implies continuous, the Squeeze Theorem), and Q5 is the standard example $x^2 \sin\frac{1}{x}$.
> - Q3 and Q4 are limits of the kind in the exercises, written out with the Limit Laws.
>
> **What that means for Midterm 2**
> - **[T/F] and [MC]** come from the True-False Quizzes of the Chapter Reviews and from "which statements are true" versions of examples and exercises. Items 2–16 of the Chapter 2 quiz are in the sections below, word for word. The Chapter 3 Review comes after §3.9 and is not in the scans: its quiz items are written from memory of the book and marked ‡, so check their wording against the book.
> - **[Proof 10]** are proofs of the formulas and theorems of the text, and the short "Show that" exercises.
> - **[Calc 10]** are exercises of the sections; the assigned ones come first.
>
> Stars run from ★ to ★★★★: how likely the exam asks it. They are estimates from Midterm 1, not information from the teacher.
>
> **Drill first:** write by hand the proofs marked ★★★★ (the Product Rule, $\frac{d}{dx}(\sin x) = \cos x$, Fermat's Theorem, Rolle's Theorem, the Mean Value Theorem, the Increasing/Decreasing Test); then one related-rates problem and one optimization problem; then every True or False list.

| Part III question | Most likely choices | Sections |
| --- | --- | --- |
| Proof of a differentiation formula | the Product Rule; $\frac{d}{dx}(\sin x) = \cos x$; the Power Rule | §2.3, §2.4 |
| Proof of a theorem of Chapter 3 | Rolle's Theorem; the Mean Value Theorem; Fermat's Theorem; the Increasing/Decreasing Test | §3.1–§3.3 |
| Word problem | one related-rates problem or one optimization problem | §2.8, §3.7 |
| Derivative computation | implicit differentiation (a tangent line or $y''$); a Chain Rule value such as $F'(0)$ | §2.5, §2.6 |
| Limit or shape of a graph | a limit at infinity, possibly with an $\varepsilon$, $N$ proof; intervals of increase and concavity | §3.3–§3.5 |

> [!warning] Conditions the grader looks for
> - A quotient by $h$ or by $x - a$: write "$h \ne 0$" ([[CAL1 Midterm 1#Q5 Does the Derivative Exist at 0|Midterm 1 Q5]], −1).
> - An inequality that holds only near a number: say where it holds, and keep $x$ there ([[CAL1 Midterm 1#Q7 The Squeeze Theorem|Midterm 1 Q7]], −2).
> - A theorem with hypotheses (Rolle, Mean Value, Extreme Value, the Closed Interval Method): write "continuous on $[a, b]$" and "differentiable on $(a, b)$" before using it.
> - Name the law or theorem of each step in a right-hand column, as in Q3 and Q4.
> - A word problem: define every symbol, state the domain, and say why the value found is the absolute maximum or minimum.

> [!info] Coverage
> Stewart, *Calculus*, §2.3–§2.9, §3.1–§3.5 and §3.7 (pp. 133–276), and the Chapter 2 Review (pp. 199–203). Each section below lists its exam points and then predicted questions in the three forms of the exam, with collapsed answers. "Assigned" marks a homework exercise; its full solution is in the HW Solutions note linked beside it. Longer treatments of two sections: [[CAL1 2.6 Exam Notes]] and [[CAL1 3.1 Exam Notes]].

## §2.3 Differentiation Formulas

### 2.3 Exam Points

- **[Proof 10] ★★★★** the [[Product Rule]] (p. 138): subtract and add $f(x+h)g(x)$; $\lim_{h \to 0} f(x+h) = f(x)$ because a differentiable function is continuous ([[CAL1 Midterm 1#Q6 Differentiable Implies Continuous|Midterm 1 Q6]]). The [[Quotient Rule]] (p. 139) uses the same trick with $f(x)g(x)$.
- **[Proof 10] ★★★** the [[Power Rule]] for a positive integer $n$ (pp. 134–135): first proof by $x^n - a^n = (x - a)(x^{n-1} + x^{n-2}a + \cdots + a^{n-1})$, second proof by the Binomial Theorem. Short proofs: the constant function, the Constant Multiple Rule, the Sum Rule (pp. 133–136), and $\frac{d}{dx}(x^{-n}) = -nx^{-n-1}$ by the Quotient Rule (p. 140).
- **[Proof 10] ★★** exercises that prove a rule: $(fgh)' = f'gh + fg'h + fgh'$ (107, assigned); the Reciprocal Rule $\left(\frac{1}{g}\right)' = -\frac{g'}{g^2}$ (108); the Quotient Rule from the Product Rule with $f = Fg$ (109); $(fg)'' = f''g + 2f'g' + fg''$ (110).
- **[T/F] [MC] ★★★★** $(fg)' \ne f'g'$ (p. 137: $f = x$, $g = x^2$); the derivative of a polynomial is a polynomial, and of a rational function a rational function; a polynomial of degree $n$ has $(n+1)$-st derivative $0$ (Midterm 1 Q2 (c)); the Power Rule holds for every real exponent (p. 141); the slope of a tangent line is the number $f'(a)$.
- **[Calc 10] ★★★** piecewise functions: is $f$ differentiable where the pieces meet (111, assigned), find $m$ and $b$ (115, assigned), $\lvert x^2 - 9 \rvert$ (113). Check continuity, then compare the one-sided derivatives $f'_{-}(a)$ and $f'_{+}(a)$.
- **[Calc] ★★★** derivatives by the Product and Quotient Rules, rewriting first when that is simpler (NOTE, p. 140); [[Tangent Line|tangent]] and [[Normal Line|normal lines]] (Example 12; 61, 63 assigned); horizontal tangents (Example 4; 87 assigned); tangents parallel to a line (Example 13; 91, 93 assigned); values from $f(5)$, $f'(5)$, $g(5)$, $g'(5)$ (79–82 assigned) or from graphs (83 assigned); a limit read as a derivative (119, assigned).

### 2.3 True or False

> [!question]
> Respond with true (T) or false (F). Items (a)–(i) are items 2, 3, 8, 9, 10, 11, 13, 14, 16 of the True-False Quiz of the Chapter 2 Review (p. 200), word for word.
> - (a) If $f$ and $g$ are differentiable, then $\dfrac{d}{dx}[f(x) + g(x)] = f'(x) + g'(x)$.
> - (b) If $f$ and $g$ are differentiable, then $\dfrac{d}{dx}[f(x)g(x)] = f'(x)g'(x)$.
> - (c) If $f'(r)$ exists, then $\lim_{x \to r} f(x) = f(r)$.
> - (d) If $g(x) = x^5$, then $\displaystyle\lim_{x \to 2} \frac{g(x) - g(2)}{x - 2} = 80$.
> - (e) $\dfrac{d^2y}{dx^2} = \left(\dfrac{dy}{dx}\right)^2$
> - ==(f)== An equation of the tangent line to the parabola $y = x^2$ at $(-2, 4)$ is $y - 4 = 2x(x + 2)$.
> - ==(g)== The derivative of a polynomial is a polynomial.
> - (h) The derivative of a rational function is a rational function.
> - (i) If $f(x) = (x^6 - x^4)^5$, then $f^{(31)}(x) = 0$.

> [!solution]- Answers
> - (a) **T.** The Sum Rule.
> - (b) **F.** $f(x) = x$, $g(x) = x^2$: $(fg)'(x) = (x^3)' = 3x^2$, but $f'(x)g'(x) = 1 \cdot 2x = 2x$.
> - (c) **T.** $f$ is differentiable at $r$, so $f$ is continuous at $r$.
> - (d) **T.** The limit is $g'(2)$, and $g'(x) = 5x^4$ gives $g'(2) = 80$.
> - (e) **F.** $y = x^2$: $\frac{d^2y}{dx^2} = 2$, but $\left(\frac{dy}{dx}\right)^2 = 4x^2$.
> - (f) **F.** The slope is the number $y'(-2) = -4$, so the tangent line is $y - 4 = -4(x + 2)$. The given equation is not the equation of a line.
> - (g) **T.** Differentiate term by term with the Power Rule.
> - (h) **T.** $\left(\frac{P}{Q}\right)' = \frac{QP' - PQ'}{Q^2}$, where $P'$ and $Q'$ are polynomials.
> - (i) **T.** $f$ is a polynomial of degree $30$. Each derivative lowers the degree by one, so $f^{(30)}$ is a constant and $f^{(31)}(x) = 0$.

### 2.3 Multiple Choice

> [!question]
> **MC 1.** (5 points) Suppose that $f(5) = 1$, $f'(5) = 6$, $g(5) = -3$, and $g'(5) = 2$. Which of the following statements are true?
> - A. $(fg)'(5) = -16$
> - B. $(f/g)'(5) = -\frac{20}{9}$
> - C. $(g/f)'(5) = 20$
> - D. $(fg)'(5) = f'(5)g'(5) = 12$

> [!solution]- Answer to MC 1
> **A, B, C.** (Exercise 79, assigned: [[CAL1 HW 2.3 Solutions#ST 2.3.79|ST 2.3.79]].)
> - A. $(fg)'(5) = f(5)g'(5) + g(5)f'(5) = 1 \cdot 2 + (-3) \cdot 6 = -16$; so D fails.
> - B. $(f/g)'(5) = \frac{g(5)f'(5) - f(5)g'(5)}{[g(5)]^2} = \frac{-18 - 2}{9} = -\frac{20}{9}$.
> - C. $(g/f)'(5) = \frac{f(5)g'(5) - g(5)f'(5)}{[f(5)]^2} = \frac{2 + 18}{1} = 20$.

> [!question]
> **MC 2.** (5 points) Let
> $$
> f(x) = \begin{cases} x^2 + 1 & \text{if } x < 1 \\ x + 1 & \text{if } x \ge 1. \end{cases}
> $$
> Which of the following statements are true?
> - A. $f$ is continuous at $1$.
> - B. $f'_{-}(1) = 2$.
> - C. $f'_{+}(1) = 1$.
> - D. $f$ is differentiable at $1$.

> [!solution]- Answer to MC 2
> **A, B, C.** (Exercise 111, assigned: [[CAL1 HW 2.3 Solutions#ST 2.3.111|ST 2.3.111]].)
> - A. $\lim_{x \to 1^-}(x^2 + 1) = 2 = \lim_{x \to 1^+}(x + 1) = f(1)$.
> - B. $f'_{-}(1) = \lim_{x \to 1^-} \frac{(x^2 + 1) - 2}{x - 1} = \lim_{x \to 1^-}(x + 1) = 2$.
> - C. $f'_{+}(1) = \lim_{x \to 1^+} \frac{(x + 1) - 2}{x - 1} = 1$.
> - D fails: $f'_{-}(1) = 2 \ne 1 = f'_{+}(1)$, so $f'(1)$ does not exist.

### 2.3 Computation and Proof

> [!question]
> **P1.** ★★★★ (10 points) Prove the Product Rule: if $f$ and $g$ are both differentiable, then
> $$
> \frac{d}{dx}[f(x)g(x)] = f(x)g'(x) + g(x)f'(x).
> $$

> [!proof]- Proof of P1
> Let $F(x) = f(x)g(x)$.
> $$
> \begin{aligned}
> F'(x) &= \lim_{h \to 0} \frac{F(x+h) - F(x)}{h} = \lim_{h \to 0} \frac{f(x+h)g(x+h) - f(x)g(x)}{h} \\
> &= \lim_{h \to 0} \frac{f(x+h)g(x+h) - f(x+h)g(x) + f(x+h)g(x) - f(x)g(x)}{h} \\
> &= \lim_{h \to 0} \left[ f(x+h) \cdot \frac{g(x+h) - g(x)}{h} + g(x) \cdot \frac{f(x+h) - f(x)}{h} \right] && (h \ne 0) \\
> &= \lim_{h \to 0} f(x+h) \cdot \lim_{h \to 0} \frac{g(x+h) - g(x)}{h} + \lim_{h \to 0} g(x) \cdot \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} && \text{(by Sum and Product Laws)} \\
> &= f(x)g'(x) + g(x)f'(x) \qquad \blacksquare
> \end{aligned}
> $$
> \# Two reasons to write beside the last step: $\lim_{h \to 0} g(x) = g(x)$ because $g(x)$ does not depend on $h$; $\lim_{h \to 0} f(x+h) = f(x)$ because $f$ is differentiable at $x$, hence continuous at $x$.

> [!question]
> ==**P2.**== ★★★ (10 points) Prove the Power Rule: if $n$ is a positive integer, then $\dfrac{d}{dx}(x^n) = nx^{n-1}$.

> [!proof]- Proof of P2
> Let $f(x) = x^n$ and let $a$ be any number.
> $$
> \begin{aligned}
> f'(a) &= \lim_{x \to a} \frac{f(x) - f(a)}{x - a} = \lim_{x \to a} \frac{x^n - a^n}{x - a} \\
> &= \lim_{x \to a} \frac{(x - a)(x^{n-1} + x^{n-2}a + \cdots + xa^{n-2} + a^{n-1})}{x - a} \\
> &= \lim_{x \to a} (x^{n-1} + x^{n-2}a + \cdots + xa^{n-2} + a^{n-1}) && (x \ne a) \\
> &= a^{n-1} + a^{n-2}a + \cdots + aa^{n-2} + a^{n-1} && \text{(a polynomial in \(x\))} \\
> &= na^{n-1} && \text{(\(n\) terms)}
> \end{aligned}
> $$
> Hence $f'(x) = nx^{n-1}$ for every $x$. $\blacksquare$
>
> \# Second proof (p. 135): $(x+h)^n = x^n + nx^{n-1}h + \frac{n(n-1)}{2}x^{n-2}h^2 + \cdots + h^n$ by the Binomial Theorem, so $\frac{(x+h)^n - x^n}{h} = nx^{n-1} + \frac{n(n-1)}{2}x^{n-2}h + \cdots + h^{n-1} \to nx^{n-1}$: every term except the first has $h$ as a factor.

> [!question]
> **P3.** ★★★ (10 points) Let
> $$
> f(x) = \begin{cases} x^2 & \text{if } x \le 2 \\ mx + b & \text{if } x > 2. \end{cases}
> $$
> Find the values of $m$ and $b$ that make $f$ differentiable everywhere.

> [!solution]- Solution of P3
> Exercise 115, assigned: [[CAL1 HW 2.3 Solutions#ST 2.3.115|ST 2.3.115]].
> $$
> \begin{aligned}
> &x \ne 2:\ f \text{ is a polynomial on each side of } 2, \text{ so } f \text{ is differentiable there.} \\
> &f \text{ differentiable at } 2 \implies f \text{ continuous at } 2 \implies \lim_{x \to 2^+}(mx + b) = f(2) \implies 2m + b = 4 \\
> &f'_{-}(2) = \lim_{x \to 2^-} \frac{x^2 - 4}{x - 2} = \lim_{x \to 2^-}(x + 2) = 4 \\
> &f'_{+}(2) = \lim_{x \to 2^+} \frac{(mx + b) - 4}{x - 2} = \lim_{x \to 2^+} \frac{mx + b - (2m + b)}{x - 2} = m \\
> &f'(2) \text{ exists} \iff f'_{-}(2) = f'_{+}(2) \implies m = 4,\ b = 4 - 2m = -4
> \end{aligned}
> $$
> Hence $m = 4$ and $b = -4$.

> [!question]
> **P4.** ★★★ (10 points) Evaluate $\displaystyle\lim_{x \to 1} \frac{x^{1000} - 1}{x - 1}$.

> [!solution]- Solution of P4
> Exercise 119, assigned: [[CAL1 HW 2.3 Solutions#ST 2.3.119|ST 2.3.119]]. Let $f(x) = x^{1000}$, so $f(1) = 1$.
> $$
> \lim_{x \to 1} \frac{x^{1000} - 1}{x - 1} = \lim_{x \to 1} \frac{f(x) - f(1)}{x - 1} = f'(1) = 1000 \cdot 1^{999} = 1000
> $$

> [!question]
> **P5.** ★★ (10 points) Find equations for two lines that are both tangent to the curve $y = x^3 - 3x^2 + 3x - 3$ and parallel to the line $3x - y = 15$.

> [!solution]- Solution of P5
> Exercise 91, assigned: [[CAL1 HW 2.3 Solutions#ST 2.3.91|ST 2.3.91]]. The line $y = 3x - 15$ has slope $3$.
> $$
> \begin{aligned}
> &y' = 3x^2 - 6x + 3 = 3 \implies 3x(x - 2) = 0 \implies x = 0 \text{ or } x = 2 \\
> &x = 0:\ y = -3,\quad y + 3 = 3(x - 0) \implies y = 3x - 3 \\
> &x = 2:\ y = -1,\quad y + 1 = 3(x - 2) \implies y = 3x - 7
> \end{aligned}
> $$

> [!question]
> **P6.** ★★ (10 points) Prove the Quotient Rule: if $f$ and $g$ are differentiable, then $\dfrac{d}{dx}\left[\dfrac{f(x)}{g(x)}\right] = \dfrac{g(x)f'(x) - f(x)g'(x)}{[g(x)]^2}$.

> [!solution]- Key steps of P6
> 1. $F = \frac{f}{g}$: $\frac{F(x+h) - F(x)}{h} = \frac{f(x+h)g(x) - f(x)g(x+h)}{h\,g(x+h)g(x)}$ $(h \ne 0)$.
> 2. Subtract and add $f(x)g(x)$ in the numerator:
> $$
> \frac{g(x) \cdot \dfrac{f(x+h) - f(x)}{h} - f(x) \cdot \dfrac{g(x+h) - g(x)}{h}}{g(x+h)g(x)}
> $$
> 3. Take $h \to 0$ with the Quotient, Difference and Product Laws. $\lim_{h \to 0} g(x+h) = g(x)$ because $g$ is differentiable, hence continuous, and $g(x) \ne 0$.
> 4. The limit is $\frac{g(x)f'(x) - f(x)g'(x)}{[g(x)]^2}$.

## §2.4 Derivatives of Trigonometric Functions

### 2.4 Exam Points

- **[Proof 10] ★★★★** $\frac{d}{dx}(\sin x) = \cos x$ from the definition (pp. 148–149): the addition formula for sine, then the two [[Special Trigonometric Limits|special limits]]. Its twin is Exercise 26: $\frac{d}{dx}(\cos x) = -\sin x$ with $\cos(x+h) = \cos x\cos h - \sin x\sin h$.
- **[Proof 10] ★★★** $\lim_{\theta \to 0} \frac{\cos\theta - 1}{\theta} = 0$ (p. 152): multiply by $\cos\theta + 1$. $\lim_{\theta \to 0} \frac{\sin\theta}{\theta} = 1$ (pp. 151–152): $\sin\theta < \theta < \tan\theta$ for $0 < \theta < \frac{\pi}{2}$, then the [[Squeeze Theorem]] ([[CAL1 Midterm 1#Q7 The Squeeze Theorem|Midterm 1 Q7]]; $\frac{\sin h}{h}$ was Q2 (g)).
- **[Proof 10] ★★★** the derivatives of $\tan$, $\csc$, $\sec$, $\cot$ by the Quotient Rule (p. 149; Exercises 23–25, of which 23 and 25 are assigned).
- **[T/F] [MC] ★★★** the table of the six [[Derivatives of Trigonometric Functions|derivatives]] (p. 150): the minus signs go with the cofunctions $\cos$, $\csc$, $\cot$; the formulas hold only when $x$ is in radians; $\sin 7x \ne 7\sin x$.
- **[Calc] ★★★★** limits by $\frac{\sin\theta}{\theta} \to 1$ (Examples 5–7; Exercises 45–60, of which 47, 49, 51, 53, 55, 57, 59 are assigned): make the angle and the denominator match, as in $\frac{\sin 7x}{4x} = \frac{7}{4} \cdot \frac{\sin 7x}{7x}$.
- **[Calc] ★★★** a high derivative by the cycle of length 4 (Example 4; 61 assigned; 62); horizontal tangents (Example 2: $\tan x = 1$); simple harmonic motion $s = 4\cos t$ (Example 3; 41 assigned).

### 2.4 True or False

> [!question]
> Respond with true (T) or false (F). Item (a) is item 12 of the True-False Quiz of the Chapter 2 Review (p. 200).
> - ==(a)== $\dfrac{d}{dx}(\tan^2 x) = \dfrac{d}{dx}(\sec^2 x)$
> - (b) Since $\displaystyle\lim_{\theta \to 0} \frac{\cos\theta - 1}{\theta} = 0$, also $\displaystyle\lim_{\theta \to 0} \frac{\cos\theta - 1}{\theta^2} = 0$.
> - (c) If $f(x) = \cos x$, then $f^{(27)}(x) = \sin x$.
> - ==(d)== If $\theta$ is measured in degrees, then $\dfrac{d}{d\theta}(\sin\theta) = \cos\theta$.
> - (e) The graph of $f(x) = \dfrac{\sec x}{1 + \tan x}$ has a horizontal tangent wherever $\tan x = 1$.
> - ==(f)== $\displaystyle\lim_{x \to 0} x\cot x = 0$

> [!solution]- Answers
> - (a) **T.** $\sec^2 x = \tan^2 x + 1$, so the two functions differ by a constant; both derivatives are $2\tan x\sec^2 x$.
> - (b) **F.** $\frac{\cos\theta - 1}{\theta^2} = \frac{-\sin^2\theta}{\theta^2(\cos\theta + 1)} = -\left(\frac{\sin\theta}{\theta}\right)^2 \cdot \frac{1}{\cos\theta + 1} \to -\frac{1}{2}$.
> - (c) **T.** The derivatives of $\cos x$ are $-\sin x$, $-\cos x$, $\sin x$, $\cos x$, and then repeat; $27 = 4 \cdot 6 + 3$, so $f^{(27)}(x) = \sin x$ (Example 4).
> - (d) **F.** In degrees $\frac{d}{d\theta}(\sin\theta) = \frac{\pi}{180}\cos\theta$ (Exercise 2.5.85); the formulas of the table need radians.
> - (e) **T.** $f'(x) = \frac{\sec x(\tan x - 1)}{(1 + \tan x)^2}$ and $\sec x$ is never $0$ (Example 2).
> - (f) **F.** $x\cot x = \frac{\cos x}{\frac{\sin x}{x}} \to \frac{1}{1} = 1$ (Example 6).

### 2.4 Multiple Choice

> [!question]
> **MC 1.** (5 points) Which of the following statements are true?
> - ==A.== $\displaystyle\lim_{x \to 0} \frac{\tan 2x}{x} = 2$
> - B. $\displaystyle\lim_{t \to 0} \frac{\sin 3t}{\sin t} = \frac{1}{3}$
> - C. $\displaystyle\lim_{\theta \to 0} \frac{\sin\theta}{\theta + \tan\theta} = \frac{1}{2}$
> - D. $\displaystyle\lim_{x \to 0} \frac{\sin x - \sin x\cos x}{x^2} = 0$

> [!solution]- Answer to MC 1
> **A, C, D.** (Exercises 51, 47, 55, 49, all assigned: [[CAL1 HW 2.4 Solutions]].)
> - A. $\frac{\tan 2x}{x} = \frac{\sin 2x}{2x} \cdot \frac{2}{\cos 2x} \to 1 \cdot 2 = 2$.
> - B fails: $\frac{\sin 3t}{\sin t} = \frac{\sin 3t}{3t} \cdot 3 \cdot \frac{t}{\sin t} \to 3$.
> - C. Divide by $\theta$: $\frac{\frac{\sin\theta}{\theta}}{1 + \frac{\sin\theta}{\theta} \cdot \frac{1}{\cos\theta}} \to \frac{1}{1 + 1} = \frac{1}{2}$.
> - D. $\frac{\sin x}{x} \cdot \frac{1 - \cos x}{x} \to 1 \cdot 0 = 0$.

> [!question]
> **MC 2.** (5 points) Which of the following statements are true?
> - A. $\dfrac{d}{dx}(\sec x) = \sec x\tan x$
> - B. $\dfrac{d}{dx}(\cot x) = -\csc^2 x$
> - C. $\dfrac{d}{dx}(\csc x) = \csc x\cot x$
> - D. $\dfrac{d^{99}}{dx^{99}}(\sin x) = -\cos x$

> [!solution]- Answer to MC 2
> **A, B, D.**
> - C fails: $\frac{d}{dx}(\csc x) = -\csc x\cot x$.
> - D. The derivatives of $\sin x$ are $\cos x$, $-\sin x$, $-\cos x$, $\sin x$, and then repeat; $99 = 4 \cdot 24 + 3$ (Exercise 61, assigned).

### 2.4 Computation and Proof

> [!question]
> **P1.** ★★★★ (10 points) Prove, using the definition of a derivative, that $\dfrac{d}{dx}(\sin x) = \cos x$. You may use $\lim_{h \to 0} \frac{\sin h}{h} = 1$ and $\lim_{h \to 0} \frac{\cos h - 1}{h} = 0$.

> [!proof]- Proof of P1
> Let $f(x) = \sin x$.
> $$
> \begin{aligned}
> f'(x) &= \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} = \lim_{h \to 0} \frac{\sin(x+h) - \sin x}{h} \\
> &= \lim_{h \to 0} \frac{\sin x\cos h + \cos x\sin h - \sin x}{h} && \text{(addition formula for sine)} \\
> &= \lim_{h \to 0} \left[ \sin x \cdot \frac{\cos h - 1}{h} + \cos x \cdot \frac{\sin h}{h} \right] && (h \ne 0) \\
> &= \lim_{h \to 0} \sin x \cdot \lim_{h \to 0} \frac{\cos h - 1}{h} + \lim_{h \to 0} \cos x \cdot \lim_{h \to 0} \frac{\sin h}{h} && \text{(by Sum and Product Laws)} \\
> &= \sin x \cdot 0 + \cos x \cdot 1 = \cos x \qquad \blacksquare
> \end{aligned}
> $$
> \# $\sin x$ and $\cos x$ do not depend on $h$, so $\lim_{h \to 0} \sin x = \sin x$ and $\lim_{h \to 0} \cos x = \cos x$. For $\cos x$ (Exercise 26) the same steps with $\cos(x+h) = \cos x\cos h - \sin x\sin h$ give $\cos x \cdot 0 - \sin x \cdot 1 = -\sin x$.

> [!question]
> **P2.** ★★★ (10 points) Prove that $\displaystyle\lim_{\theta \to 0} \frac{\cos\theta - 1}{\theta} = 0$. You may use $\lim_{\theta \to 0} \frac{\sin\theta}{\theta} = 1$.

> [!proof]- Proof of P2
> $$
> \begin{aligned}
> \lim_{\theta \to 0} \frac{\cos\theta - 1}{\theta} &= \lim_{\theta \to 0} \left( \frac{\cos\theta - 1}{\theta} \cdot \frac{\cos\theta + 1}{\cos\theta + 1} \right) = \lim_{\theta \to 0} \frac{\cos^2\theta - 1}{\theta(\cos\theta + 1)} \\
> &= \lim_{\theta \to 0} \frac{-\sin^2\theta}{\theta(\cos\theta + 1)} && (\sin^2\theta + \cos^2\theta = 1) \\
> &= -\lim_{\theta \to 0} \frac{\sin\theta}{\theta} \cdot \lim_{\theta \to 0} \frac{\sin\theta}{\cos\theta + 1} && \text{(by Product Law)} \\
> &= -1 \cdot \frac{0}{1 + 1} = 0 \qquad \blacksquare
> \end{aligned}
> $$
> \# $\cos\theta + 1 \ne 0$ for $\theta$ near $0$, and $\frac{\sin\theta}{\cos\theta + 1}$ is continuous at $0$, so its limit is found by direct substitution.

> [!question]
> ==**P3.**== ★★ (10 points) Prove that $\displaystyle\lim_{\theta \to 0} \frac{\sin\theta}{\theta} = 1$.

> [!solution]- Key steps of P3
> 1. Let $0 < \theta < \frac{\pi}{2}$, in a circle of radius $1$ with center $O$ and central angle $\theta$ (Figure 6, p. 151). $\lvert BC \rvert < \lvert AB \rvert < \text{arc } AB$ gives $\sin\theta < \theta$, so $\frac{\sin\theta}{\theta} < 1$.
> 2. $\theta = \text{arc } AB < \lvert AE \rvert + \lvert EB \rvert < \lvert AE \rvert + \lvert ED \rvert = \lvert AD \rvert = \tan\theta$ gives $\theta < \frac{\sin\theta}{\cos\theta}$, so $\cos\theta < \frac{\sin\theta}{\theta}$.
> 3. $\cos\theta < \frac{\sin\theta}{\theta} < 1$ for $0 < \theta < \frac{\pi}{2}$, and $\lim_{\theta \to 0} \cos\theta = 1 = \lim_{\theta \to 0} 1$, so $\lim_{\theta \to 0^+} \frac{\sin\theta}{\theta} = 1$ by the Squeeze Theorem.
> 4. $\frac{\sin\theta}{\theta}$ is an even function, so the left-hand limit is also $1$. Hence the limit is $1$.

> [!question]
> **P4.** ★★★ (10 points) Show that $\dfrac{d}{dx}(\tan x) = \sec^2 x$ and $\dfrac{d}{dx}(\csc x) = -\csc x\cot x$.

> [!solution]- Solution of P4
> $$
> \begin{aligned}
> \frac{d}{dx}(\tan x) &= \frac{d}{dx}\left(\frac{\sin x}{\cos x}\right) = \frac{\cos x \cdot \cos x - \sin x \cdot (-\sin x)}{\cos^2 x} && \text{(by Quotient Rule)} \\
> &= \frac{\cos^2 x + \sin^2 x}{\cos^2 x} = \frac{1}{\cos^2 x} = \sec^2 x \\
> \frac{d}{dx}(\csc x) &= \frac{d}{dx}\left(\frac{1}{\sin x}\right) = \frac{\sin x \cdot 0 - 1 \cdot \cos x}{\sin^2 x} && \text{(by Quotient Rule)} \\
> &= -\frac{1}{\sin x} \cdot \frac{\cos x}{\sin x} = -\csc x\cot x
> \end{aligned}
> $$
> The second part is Exercise 23, assigned: [[CAL1 HW 2.4 Solutions#ST 2.4.23|ST 2.4.23]].

> [!question]
> **P5.** ★★★ (10 points) Find the limits.
> - ==(a)== $\displaystyle\lim_{x \to \pi/4} \frac{1 - \tan x}{\sin x - \cos x}$
> - ==(b)== $\displaystyle\lim_{x \to 1} \frac{\sin(x - 1)}{x^2 + x - 2}$

> [!solution]- Solution of P5
> **(a)** Exercise 59, assigned: [[CAL1 HW 2.4 Solutions#ST 2.4.59|ST 2.4.59]].
> $$
> \lim_{x \to \pi/4} \frac{1 - \tan x}{\sin x - \cos x} = \lim_{x \to \pi/4} \frac{\dfrac{\cos x - \sin x}{\cos x}}{\sin x - \cos x} = \lim_{x \to \pi/4} \frac{-1}{\cos x} = -\frac{1}{\cos\frac{\pi}{4}} = -\sqrt{2}
> $$
> since $\sin x - \cos x \ne 0$ for $x \ne \frac{\pi}{4}$ near $\frac{\pi}{4}$.
>
> **(b)** Exercise 60. Let $\theta = x - 1$; then $\theta \to 0$ as $x \to 1$.
> $$
> \lim_{x \to 1} \frac{\sin(x - 1)}{(x - 1)(x + 2)} = \lim_{\theta \to 0} \frac{\sin\theta}{\theta} \cdot \lim_{x \to 1} \frac{1}{x + 2} = 1 \cdot \frac{1}{3} = \frac{1}{3}
> $$

> [!question]
> ==**P6.**== ★★ (10 points) Find $\dfrac{d^{35}}{dx^{35}}(x\sin x)$.

> [!solution]- Solution of P6
> Exercise 62.
> $$
> \begin{aligned}
> &y = x\sin x,\quad y' = \sin x + x\cos x,\quad y'' = 2\cos x - x\sin x, \\
> &y''' = -3\sin x - x\cos x,\quad y^{(4)} = -4\cos x + x\sin x,\ \dots \\
> &\text{Pattern: } y^{(n)} = x \cdot \frac{d^n}{dx^n}(\sin x) + n \cdot \frac{d^{n-1}}{dx^{n-1}}(\sin x) \\
> &35 = 4 \cdot 8 + 3 \implies \frac{d^{35}}{dx^{35}}(\sin x) = -\cos x,\qquad 34 = 4 \cdot 8 + 2 \implies \frac{d^{34}}{dx^{34}}(\sin x) = -\sin x \\
> &y^{(35)} = -x\cos x - 35\sin x
> \end{aligned}
> $$

## §2.5 The Chain Rule

### 2.5 Exam Points

- **Statement with its hypotheses (p. 156):** if $g$ is differentiable at $x$ and $f$ is differentiable at $g(x)$, then $F = f \circ g$ is differentiable at $x$ and $F'(x) = f'(g(x)) \cdot g'(x)$; in Leibniz notation $\frac{dy}{dx} = \frac{dy}{du}\frac{du}{dx}$.
- **[Proof 10] ★★★** the proof of the [[Chain Rule]] (p. 161): a differentiable function satisfies $\Delta y = f'(a)\,\Delta x + \varepsilon\,\Delta x$ with $\varepsilon \to 0$ as $\Delta x \to 0$. **[T/F]** the flaw of the short argument (p. 157): $\Delta u$ may be $0$ even when $\Delta x \ne 0$, and we cannot divide by $0$.
- **[Proof 10] ★★★** exercises proved with the Chain Rule: the derivative of an even function is odd, and of an odd function even (83, assigned); the Quotient Rule from $f(x)[g(x)]^{-1}$ (84); $\frac{d}{dx}\lvert x \rvert = \frac{x}{\lvert x \rvert}$ from $\lvert x \rvert = \sqrt{x^2}$ (86); $(f \circ g \circ h)'(x) = f'(g(h(x))) \cdot g'(h(x)) \cdot h'(x)$ (87); $F''(x) = f''(g(x)) \cdot [g'(x)]^2 + f'(g(x)) \cdot g''(x)$ (88).
- **[T/F] ★★★★** items 4, 5, 6, 7, 15 of the True-False Quiz of the Chapter 2 Review: where the inner function goes, and absolute values.
- **[Calc] ★★★★** the Power Rule combined with the Chain Rule (p. 159); a chain of three functions (Examples 7 and 8; 43, 47 assigned); the Product Rule first, then the Chain Rule (Example 6; 19, 21 assigned); values from a table or from given numbers (63, 65, 73 assigned; 71, 74); tangent lines (53, 55 assigned); horizontal tangents (61, assigned); a high derivative such as $D^{103}\cos 2x$ (75, assigned).

### 2.5 True or False

> [!question]
> Respond with true (T) or false (F). Items (a)–(e) are items 4, 5, 6, 7, 15 of the True-False Quiz of the Chapter 2 Review (p. 200), word for word.
> - (a) If $f$ and $g$ are differentiable, then $\dfrac{d}{dx}\left[f(g(x))\right] = f'(g(x))g'(x)$.
> - (b) If $f$ is differentiable, then $\dfrac{d}{dx}\sqrt{f(x)} = \dfrac{f'(x)}{2\sqrt{f(x)}}$.
> - (c) If $f$ is differentiable, then $\dfrac{d}{dx}f(\sqrt{x}) = \dfrac{f'(x)}{2\sqrt{x}}$.
> - ==(d)== $\dfrac{d}{dx}\lvert x^2 + x \rvert = \lvert 2x + 1 \rvert$
> - (e) If $f$ is differentiable at $a$, so is $\lvert f \rvert$.
> - ==(f)== The derivative of an even function is an even function.
> - ==(g)== The computation $\dfrac{dy}{dx} = \displaystyle\lim_{\Delta x \to 0} \frac{\Delta y}{\Delta u} \cdot \frac{\Delta u}{\Delta x} = \frac{dy}{du}\frac{du}{dx}$ is a complete proof of the Chain Rule.

> [!solution]- Answers
> - (a) **T.** The Chain Rule.
> - (b) **T.** The outer function is $\sqrt{u}$: $\frac{1}{2\sqrt{f(x)}} \cdot f'(x)$, where $f(x) > 0$.
> - (c) **F.** $\frac{d}{dx}f(\sqrt{x}) = f'(\sqrt{x}) \cdot \frac{1}{2\sqrt{x}}$: the derivative of the outer function is evaluated at the inner function. For $f(u) = u^2$: $f(\sqrt{x}) = x$ has derivative $1$, but $\frac{f'(x)}{2\sqrt{x}} = \frac{2x}{2\sqrt{x}} = \sqrt{x}$.
> - (d) **F.** For $-1 < x < 0$, $x^2 + x < 0$, so $\lvert x^2 + x \rvert = -x^2 - x$ with derivative $-2x - 1$. At $x = -\frac{1}{4}$ this is $-\frac{1}{2}$, but $\lvert 2x + 1 \rvert = \frac{1}{2}$.
> - (e) **F.** $f(x) = x$, $a = 0$: $\lvert f(x) \rvert = \lvert x \rvert$ is not differentiable at $0$.
> - (f) **F.** It is odd: $f(-x) = f(x)$ gives $-f'(-x) = f'(x)$ (Exercise 83). Example: $x^2$ has derivative $2x$.
> - (g) **F.** $\Delta u$ may be $0$ when $\Delta x \ne 0$, and then $\frac{\Delta y}{\Delta u}$ is not defined (p. 157).

### 2.5 Multiple Choice

> [!question]
> **MC 1.** (5 points) A table of values for $f$, $g$, $f'$, and $g'$ is given.
>
> | $x$ | $f(x)$ | $g(x)$ | $f'(x)$ | $g'(x)$ |
> | :---: | :---: | :---: | :---: | :---: |
> | $1$ | $3$ | $2$ | $4$ | $6$ |
> | $2$ | $1$ | $8$ | $5$ | $7$ |
> | $3$ | $7$ | $2$ | $7$ | $9$ |
>
> Which of the following statements are true?
> - A. If $h(x) = f(g(x))$, then $h'(1) = 30$.
> - B. If $H(x) = g(f(x))$, then $H'(1) = 36$.
> - C. If $F(x) = f(f(x))$, then $F'(2) = 25$.
> - D. If $G(x) = g(g(x))$, then $G'(3) = 63$.

> [!solution]- Answer to MC 1
> **A, B, D.** (Exercise 65, assigned: [[CAL1 HW 2.5 Solutions#ST 2.5.65|ST 2.5.65]]; Exercise 66.)
> - A. $h'(1) = f'(g(1))g'(1) = f'(2) \cdot 6 = 5 \cdot 6 = 30$.
> - B. $H'(1) = g'(f(1))f'(1) = g'(3) \cdot 4 = 9 \cdot 4 = 36$.
> - C fails: $F'(2) = f'(f(2))f'(2) = f'(1) \cdot 5 = 4 \cdot 5 = 20$.
> - D. $G'(3) = g'(g(3))g'(3) = g'(2) \cdot 9 = 7 \cdot 9 = 63$.

> [!question]
> **MC 2.** (5 points) Suppose that $f$ is differentiable on $\mathbb{R}$. Which of the following statements are true?
> - A. $\dfrac{d}{dx}f(x^2) = 2xf'(x^2)$
> - B. $\dfrac{d}{dx}[f(x)]^2 = 2f(x)f'(x)$
> - C. $\dfrac{d}{dx}f(f(x)) = [f'(x)]^2$
> - D. $\dfrac{d}{dx}\sin(f(x)) = \cos(f'(x))$

> [!solution]- Answer to MC 2
> **A, B.** (Exercise 70 with $\alpha = 2$, assigned.)
> - C fails: $\frac{d}{dx}f(f(x)) = f'(f(x)) \cdot f'(x)$.
> - D fails: $\frac{d}{dx}\sin(f(x)) = \cos(f(x)) \cdot f'(x)$.

### 2.5 Computation and Proof

> [!question]
> ==**P1.**== ★★★ (10 points) Use the Chain Rule to prove the following.
> - (a) The derivative of an even function is an odd function.
> - (b) The derivative of an odd function is an even function.

> [!proof]- Proof of P1
> Exercise 83, assigned: [[CAL1 HW 2.5 Solutions#ST 2.5.83|ST 2.5.83]]. Let $f$ be differentiable.
> $$
> \begin{aligned}
> &\text{(a)}\ f \text{ is even} \implies f(-x) = f(x) \text{ for all } x \\
> &\qquad \implies f'(-x) \cdot (-1) = f'(x) && \text{(differentiate both sides; Chain Rule)} \\
> &\qquad \implies f'(-x) = -f'(x) \text{ for all } x \implies f' \text{ is odd.} \\[6pt]
> &\text{(b)}\ f \text{ is odd} \implies f(-x) = -f(x) \text{ for all } x \\
> &\qquad \implies f'(-x) \cdot (-1) = -f'(x) && \text{(differentiate both sides; Chain Rule)} \\
> &\qquad \implies f'(-x) = f'(x) \text{ for all } x \implies f' \text{ is even.} \qquad \blacksquare
> \end{aligned}
> $$

> [!question]
> ==**P2.**== ★★★ (10 points) State and prove the Chain Rule.

> [!solution]- Key steps of P2
> **Statement.** If $g$ is differentiable at $x$ and $f$ is differentiable at $g(x)$, then $F = f \circ g$ is differentiable at $x$ and $F'(x) = f'(g(x)) \cdot g'(x)$.
> 1. If $y = f(x)$ is differentiable at $a$, put $\varepsilon = \frac{\Delta y}{\Delta x} - f'(a)$ for $\Delta x \ne 0$ and $\varepsilon = 0$ for $\Delta x = 0$. Then $\Delta y = f'(a)\,\Delta x + \varepsilon\,\Delta x$ and $\varepsilon \to 0$ as $\Delta x \to 0$.
> 2. $u = g(x)$ is differentiable at $a$: $\Delta u = [g'(a) + \varepsilon_1]\,\Delta x$, where $\varepsilon_1 \to 0$ as $\Delta x \to 0$.
> 3. $y = f(u)$ is differentiable at $b = g(a)$: $\Delta y = [f'(b) + \varepsilon_2]\,\Delta u$, where $\varepsilon_2 \to 0$ as $\Delta u \to 0$.
> 4. Substitute: $\Delta y = [f'(b) + \varepsilon_2][g'(a) + \varepsilon_1]\,\Delta x$, so $\frac{\Delta y}{\Delta x} = [f'(b) + \varepsilon_2][g'(a) + \varepsilon_1]$ for $\Delta x \ne 0$.
> 5. As $\Delta x \to 0$, step 2 shows $\Delta u \to 0$, so $\varepsilon_1 \to 0$ and $\varepsilon_2 \to 0$:
> $$
> \frac{dy}{dx} = \lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x} = f'(b)g'(a) = f'(g(a))g'(a)
> $$
>
> \# The proof never divides by $\Delta u$; that is what the short argument of p. 157 gets wrong.

> [!question]
> **P3.** ★★★★ (10 points) Find the derivative of the function.
> - (a) $y = \cos\sqrt{\sin(\tan \pi x)}$
> - (b) $F(x) = (4x + 5)^3(x^2 - 2x + 5)^4$

> [!solution]- Solution of P3
> **(a)** Exercise 47, assigned: [[CAL1 HW 2.5 Solutions#ST 2.5.47|ST 2.5.47]]. Four functions, from the outside in:
> $$
> \begin{aligned}
> y' &= -\sin\sqrt{\sin(\tan \pi x)} \cdot \frac{d}{dx}\sqrt{\sin(\tan \pi x)} \\
> &= -\sin\sqrt{\sin(\tan \pi x)} \cdot \frac{1}{2\sqrt{\sin(\tan \pi x)}} \cdot \cos(\tan \pi x) \cdot \sec^2(\pi x) \cdot \pi \\
> &= -\frac{\pi\cos(\tan \pi x)\sec^2(\pi x)\sin\sqrt{\sin(\tan \pi x)}}{2\sqrt{\sin(\tan \pi x)}}
> \end{aligned}
> $$
>
> **(b)** Exercise 19, assigned: [[CAL1 HW 2.5 Solutions#ST 2.5.19|ST 2.5.19]]. Product Rule first, then the Chain Rule in each term:
> $$
> \begin{aligned}
> F'(x) &= 3(4x + 5)^2 \cdot 4 \cdot (x^2 - 2x + 5)^4 + (4x + 5)^3 \cdot 4(x^2 - 2x + 5)^3(2x - 2) \\
> &= 4(4x + 5)^2(x^2 - 2x + 5)^3\left[3(x^2 - 2x + 5) + (4x + 5)(2x - 2)\right] \\
> &= 4(4x + 5)^2(x^2 - 2x + 5)^3(11x^2 - 4x + 5)
> \end{aligned}
> $$

> [!question]
> **P4.** ★★★ (10 points) If $F(x) = f(3f(4f(x)))$, where $f(0) = 0$ and $f'(0) = 2$, find $F'(0)$.

> [!solution]- Solution of P4
> Exercise 73, assigned: [[CAL1 HW 2.5 Solutions#ST 2.5.73|ST 2.5.73]].
> $$
> \begin{aligned}
> F'(x) &= f'(3f(4f(x))) \cdot 3f'(4f(x)) \cdot 4f'(x) && \text{(Chain Rule twice)} \\
> F'(0) &= f'(3f(4f(0))) \cdot 3f'(4f(0)) \cdot 4f'(0) \\
> &= f'(3f(0)) \cdot 3f'(0) \cdot 4f'(0) && (f(0) = 0) \\
> &= f'(0) \cdot 3f'(0) \cdot 4f'(0) = 2 \cdot 6 \cdot 8 = 96
> \end{aligned}
> $$

> [!question]
> ==**P5.**== ★★ (10 points)
> - (a) Write $\lvert x \rvert = \sqrt{x^2}$ and use the Chain Rule to show that $\dfrac{d}{dx}\lvert x \rvert = \dfrac{x}{\lvert x \rvert}$.
> - (b) If $f(x) = \lvert \sin x \rvert$, find $f'(x)$. Where is $f$ not differentiable?

> [!solution]- Solution of P5
> Exercise 86.
> $$
> \begin{aligned}
> &\text{(a)}\ \frac{d}{dx}\lvert x \rvert = \frac{d}{dx}(x^2)^{1/2} = \frac{1}{2}(x^2)^{-1/2} \cdot 2x = \frac{x}{\sqrt{x^2}} = \frac{x}{\lvert x \rvert} && (x \ne 0) \\
> &\text{(b)}\ f'(x) = \frac{\sin x}{\lvert \sin x \rvert} \cdot \cos x && (\sin x \ne 0)
> \end{aligned}
> $$
> $f$ is not differentiable where $\sin x = 0$, that is, at $x = n\pi$ for every integer $n$. At $0$, for example, $\lim_{h \to 0^+} \frac{\lvert \sin h \rvert}{h} = 1$ and $\lim_{h \to 0^-} \frac{\lvert \sin h \rvert}{h} = -1$.

> [!question]
> **P6.** ★★ (10 points) Find $D^{103}\cos 2x$.

> [!solution]- Solution of P6
> Exercise 75, assigned: [[CAL1 HW 2.5 Solutions#ST 2.5.75|ST 2.5.75]].
> $$
> \begin{aligned}
> &D\cos 2x = -2\sin 2x,\quad D^2\cos 2x = -2^2\cos 2x,\quad D^3\cos 2x = 2^3\sin 2x,\quad D^4\cos 2x = 2^4\cos 2x \\
> &\text{Each derivative multiplies by } 2, \text{ and the functions repeat with period } 4. \\
> &103 = 4 \cdot 25 + 3 \implies D^{103}\cos 2x = 2^{103}\sin 2x
> \end{aligned}
> $$

## §2.6 Implicit Differentiation

### 2.6 Exam Points

The full note for this section is [[CAL1 2.6 Exam Notes]].

- **Method (p. 165):** differentiate both sides with respect to $x$, treating $y$ as a differentiable function of $x$, and solve for $y'$. Every term in $y$ needs the Chain Rule, $\frac{d}{dx}(y^3) = 3y^2y'$, and a term such as $6xy$ needs the Product Rule. See [[Implicit Differentiation]].
- **[Calc 10] ★★★★** $\frac{dy}{dx}$ (Examples 1–3; 5–20, of which 5, 7, 9, 15, 17, 19 are assigned); the tangent line at a given point (25–34; 25, 29, 31, 33 assigned); $y''$, simplified with the equation of the curve (Example 4; 37, 39 assigned); a value such as $f'(1)$ (21, assigned); points where the tangent has a given slope (61, assigned); $\frac{dx}{dy}$ (24, assigned).
- **[Proof 10] ★★★** "Show that" exercises: the tangent line to the ellipse at $(x_0, y_0)$ is $\frac{x_0x}{a^2} + \frac{y_0y}{b^2} = 1$ (46, assigned); the intercepts of any tangent line to $\sqrt{x} + \sqrt{y} = \sqrt{c}$ add up to $c$ (48, assigned); a tangent to a circle is perpendicular to the radius (49); the Power Rule for rational exponents (50), which the text cites on p. 141; orthogonal trajectories (51–54).
- **[T/F] [MC] ★★★** $y' = -\frac{x}{y}$ holds on every branch of the circle (NOTE 1, p. 166); the tangent is horizontal where the numerator of $y'$ is $0$ and the denominator is not (Example 2 (c)).

### 2.6 True or False

> [!question]
> Respond with true (T) or false (F).
> - ==(a)== If $x^2 + y^2 = 25$, then $\dfrac{dy}{dx} = -\dfrac{x}{y}$ on the upper semicircle and on the lower semicircle.
> - (b) If $y$ is a differentiable function of $x$, then $\dfrac{d}{dx}(y^3) = 3y^2$.
> - (c) The tangent line to the folium of Descartes $x^3 + y^3 = 6xy$ at the point $(3, 3)$ has slope $1$.
> - (d) If $x^4 + y^4 = 16$, then $y'' = -\dfrac{48x^2}{y^7}$.
> - (e) If $x^2 + y^2 = 25$, then $\dfrac{d^2y}{d^2x} = -\dfrac{25}{y^3}$.

> [!solution]- Answers
> - (a) **T.** For $y = \sqrt{25 - x^2}$, $y' = -\frac{x}{\sqrt{25 - x^2}} = -\frac{x}{y}$; for $y = -\sqrt{25 - x^2}$, $y' = \frac{x}{\sqrt{25 - x^2}} = -\frac{x}{y}$ (NOTE 1, p. 166).
> - (b) **F.** $\frac{d}{dx}(y^3) = 3y^2\,\frac{dy}{dx}$ by the Chain Rule.
> - (c) **F.** $y' = \frac{2y - x^2}{y^2 - 2x} = \frac{6 - 9}{9 - 6} = -1$ (Example 2).
> - (d) **T.** $y' = -\frac{x^3}{y^3}$ and $y'' = -\frac{3x^2(y^4 + x^4)}{y^7} = -\frac{3x^2 \cdot 16}{y^7}$ (Example 4).
> - (e) **T.** $y' = -\frac{x}{y}$, so $y'' = -\frac{y - xy'}{y^2} = -\frac{y + \frac{x^2}{y}}{y^2} = -\frac{x^2 + y^2}{y^3} = -\frac{25}{y^3}$.

### 2.6 Multiple Choice

> [!question]
> **MC 1.** (5 points) Let $y$ be defined implicitly as a function of $x$ by $x^2 + xy + y^2 = 3$. Which of the following statements are true?
> - A. $y' = -\dfrac{2x + y}{x + 2y}$
> - B. The tangent line at the point $(1, 1)$ has slope $-1$.
> - C. The tangent line is horizontal at the points of the curve where $x = -2y$.
> - D. $y'' = -\dfrac{18}{(x + 2y)^3}$

> [!solution]- Answer to MC 1
> **A, B, D.** (Exercise 38.)
> - A. $2x + y + xy' + 2yy' = 0 \implies y' = -\frac{2x + y}{x + 2y}$.
> - B. At $(1, 1)$: $y' = -\frac{3}{3} = -1$.
> - C fails: $y' = 0$ where $2x + y = 0$, that is, where $y = -2x$: the points $(1, -2)$ and $(-1, 2)$. Where $x = -2y$ the denominator is $0$ and the tangent is vertical.
> - D. $y'' = -\frac{(2 + y')(x + 2y) - (2x + y)(1 + 2y')}{(x + 2y)^2} = -\frac{3(y - xy')}{(x + 2y)^2}$, and $y - xy' = \frac{2(x^2 + xy + y^2)}{x + 2y} = \frac{6}{x + 2y}$.

> [!question]
> **MC 2.** (5 points) If $f(x) + x^2[f(x)]^3 = 10$ and $f(1) = 2$, then $f'(1) =$
> - A. $-\frac{16}{13}$
> - B. $-16$
> - C. $\frac{16}{13}$
> - D. $-\frac{8}{13}$

> [!solution]- Answer to MC 2
> **A.** (Exercise 21, assigned: [[CAL1 HW 2.6 Solutions#ST 2.6.21|ST 2.6.21]].) Differentiate both sides: $f'(x) + 2x[f(x)]^3 + 3x^2[f(x)]^2f'(x) = 0$. At $x = 1$: $f'(1) + 16 + 12f'(1) = 0 \implies f'(1) = -\frac{16}{13}$.

### 2.6 Computation and Proof

> [!question]
> **P1.** ★★★★ (10 points) Find $y''$ by implicit differentiation, and simplify: $x^2 + 4y^2 = 4$.

> [!solution]- Solution of P1
> Exercise 37, assigned: [[CAL1 HW 2.6 Solutions#ST 2.6.37|ST 2.6.37]].
> $$
> \begin{aligned}
> &2x + 8yy' = 0 \implies y' = -\frac{x}{4y} && (y \ne 0) \\
> &y'' = -\frac{1 \cdot 4y - x \cdot 4y'}{(4y)^2} = -\frac{y - xy'}{4y^2} && \text{(by Quotient Rule)} \\
> &\phantom{y''} = -\frac{y + \dfrac{x^2}{4y}}{4y^2} = -\frac{4y^2 + x^2}{16y^3} && \left(y' = -\tfrac{x}{4y}\right) \\
> &\phantom{y''} = -\frac{4}{16y^3} = -\frac{1}{4y^3} && (x^2 + 4y^2 = 4)
> \end{aligned}
> $$

> [!question]
> **P2.** ★★★ (10 points) Show by implicit differentiation that the tangent line to the ellipse
> $$
> \frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
> $$
> at the point $(x_0, y_0)$ has equation $\dfrac{x_0x}{a^2} + \dfrac{y_0y}{b^2} = 1$.

> [!proof]- Proof of P2
> Exercise 46, assigned: [[CAL1 HW 2.6 Solutions#ST 2.6.46|ST 2.6.46]].
> $$
> \begin{aligned}
> &\frac{2x}{a^2} + \frac{2yy'}{b^2} = 0 \implies y' = -\frac{b^2x}{a^2y} && (y \ne 0) \\
> &\text{If } y_0 \ne 0, \text{ the tangent line at } (x_0, y_0) \text{ is } y - y_0 = -\frac{b^2x_0}{a^2y_0}(x - x_0) \\
> &\implies \frac{y_0y}{b^2} - \frac{y_0^2}{b^2} = -\frac{x_0x}{a^2} + \frac{x_0^2}{a^2} && \left(\text{multiply by } \tfrac{y_0}{b^2}\right) \\
> &\implies \frac{x_0x}{a^2} + \frac{y_0y}{b^2} = \frac{x_0^2}{a^2} + \frac{y_0^2}{b^2} = 1 && ((x_0, y_0) \text{ is on the ellipse}) \\
> &\text{If } y_0 = 0, \text{ then } x_0 = \pm a \text{ and the tangent line is the vertical line } x = x_0, \\
> &\text{which is } \frac{x_0x}{a^2} = 1, \text{ because } x_0^2 = a^2. \qquad \blacksquare
> \end{aligned}
> $$

> [!question]
> **P3.** ★★★ (10 points) Let $y = x^{p/q}$, where $p$ and $q$ are integers with $q > 0$, and assume that $y$ is a differentiable function of $x$. Use implicit differentiation to show that $y' = \dfrac{p}{q}x^{(p/q) - 1}$.

> [!proof]- Proof of P3
> Exercise 50: the Power Rule for rational exponents.
> $$
> \begin{aligned}
> &y = x^{p/q} \implies y^q = x^p \\
> &\implies qy^{q-1}y' = px^{p-1} && \text{(differentiate both sides; Chain Rule on the left)} \\
> &\implies y' = \frac{px^{p-1}}{qy^{q-1}} = \frac{p}{q} \cdot \frac{x^{p-1}}{(x^{p/q})^{q-1}} = \frac{p}{q} \cdot \frac{x^{p-1}}{x^{p - p/q}} = \frac{p}{q}x^{(p/q) - 1} && (y \ne 0) \qquad \blacksquare
> \end{aligned}
> $$

> [!question]
> **P4.** ★★★ (10 points) Use implicit differentiation to find an equation of the tangent line to the curve $x^2 - xy - y^2 = 1$ at the point $(2, 1)$.

> [!solution]- Solution of P4
> Exercise 29, assigned: [[CAL1 HW 2.6 Solutions#ST 2.6.29|ST 2.6.29]].
> $$
> \begin{aligned}
> &2x - (y + xy') - 2yy' = 0 \implies y' = \frac{2x - y}{x + 2y} \\
> &\text{At } (2, 1):\ y' = \frac{4 - 1}{2 + 2} = \frac{3}{4} \implies y - 1 = \frac{3}{4}(x - 2), \text{ that is, } y = \frac{3}{4}x - \frac{1}{2}
> \end{aligned}
> $$

> [!question]
> **P5.** ★★★ (10 points) Find all points on the curve $x^2y^2 + xy = 2$ where the slope of the tangent line is $-1$.

> [!solution]- Solution of P5
> Exercise 61, assigned: [[CAL1 HW 2.6 Solutions#ST 2.6.61|ST 2.6.61]].
> $$
> \begin{aligned}
> &(xy)^2 + xy - 2 = 0 \implies (xy + 2)(xy - 1) = 0 \implies xy = -2 \text{ or } xy = 1 \\
> &2xy^2 + 2x^2yy' + y + xy' = 0 \implies x(2xy + 1)y' = -y(2xy + 1) \\
> &\implies y' = -\frac{y}{x} && (2xy + 1 \ne 0 \text{ and } x \ne 0 \text{ on the curve}) \\
> &y' = -1 \implies y = x \implies x^2 = xy = 1 \implies x = \pm 1 && (x^2 = -2 \text{ is impossible})
> \end{aligned}
> $$
> The points are $(1, 1)$ and $(-1, -1)$.

## §2.7 Rates of Change in the Natural and Social Sciences

### 2.7 Exam Points

- **Rates (p. 172):** the average rate of change $\frac{\Delta y}{\Delta x}$ over an interval and the instantaneous rate $\frac{dy}{dx}$; the units of $\frac{dy}{dx}$ are the units of $y$ per unit of $x$.
- **[Calc 10] ★★★ motion on a line (Example 1):** $v = s'$ and $a = v'$; at rest when $v = 0$; moving in the positive direction when $v > 0$; total distance: split the time at the zeros of $v$ and add $\lvert f(t_2) - f(t_1) \rvert$; speeding up when $v$ and $a$ have the same sign, slowing down when the signs are opposite. Assigned: 3, 7.
- **[T/F] [MC] ★★★** speeding up or slowing down read from a graph of $v$ (5, 7): "$v$ is decreasing" is not "slowing down".
- **Named rates ★★:** linear density $\rho = \frac{dm}{dx}$; current $I = \frac{dQ}{dt}$ (21, assigned); rate of reaction; compressibility $\beta = -\frac{1}{V}\frac{dV}{dP}$; growth rate $\frac{dn}{dt}$; marginal cost $C'(n) \approx C(n+1) - C(n)$ (Example 8).
- **[Proof 10] ★★** "Show that" exercises: $F = \frac{m_0a}{(1 - v^2/c^2)^{3/2}}$ (23, assigned); $A'(x) > 0$ if $p'(x)$ is greater than the average productivity $A(x) = \frac{p(x)}{x}$ (33, assigned); the rate of change of the area of a circle with respect to its radius is its circumference (15); $\beta = \frac{1}{P}$ for $PV = C$ (25).

### 2.7 True or False

> [!question]
> Respond with true (T) or false (F). A particle moves on a line with position $s = f(t)$, velocity $v$, and acceleration $a$.
> - (a) The particle is speeding up whenever $a > 0$.
> - (b) The particle is at rest when $f'(t) = 0$.
> - (c) The total distance traveled during $0 \le t \le 5$ is $\lvert f(5) - f(0) \rvert$.
> - (d) If $C(x)$ is the cost of producing $x$ units, then the marginal cost $C'(n)$ is approximately the cost of producing the $(n+1)$-st unit.

> [!solution]- Answers
> - (a) **F.** It speeds up when $v$ and $a$ have the same sign. In Example 1, for $2 < t < 3$, $a > 0$ and $v < 0$: the particle slows down.
> - (b) **T.** At rest means $v(t) = f'(t) = 0$.
> - (c) **F.** That is the displacement. In Example 1 the distance is $4 + 4 + 20 = 28$ m, but $\lvert f(5) - f(0) \rvert = 20$ m.
> - (d) **T.** $C'(n) \approx C(n+1) - C(n)$ (Example 8).

### 2.7 Multiple Choice

> [!question]
> **MC 1.** (5 points) The position of a particle is $s = f(t) = t^3 - 6t^2 + 9t$, where $t \ge 0$ is measured in seconds and $s$ in meters. Which of the following statements are true?
> - A. The particle is at rest when $t = 1$ and when $t = 3$.
> - B. The particle moves in the negative direction when $1 < t < 3$.
> - C. The total distance traveled during the first five seconds is $20$ m.
> - D. The particle is speeding up when $1 < t < 2$ and when $t > 3$.

> [!solution]- Answer to MC 1
> **A, B, D.** (Example 1, pp. 173–174.) $v = 3t^2 - 12t + 9 = 3(t - 1)(t - 3)$ and $a = 6t - 12$.
> - A. $v = 0$ at $t = 1$ and $t = 3$.
> - B. $v < 0$ for $1 < t < 3$.
> - C fails: $\lvert f(1) - f(0) \rvert + \lvert f(3) - f(1) \rvert + \lvert f(5) - f(3) \rvert = 4 + 4 + 20 = 28$ m.
> - D. For $1 < t < 2$, $v < 0$ and $a < 0$; for $t > 3$, $v > 0$ and $a > 0$.

### 2.7 Computation and Proof

> [!question]
> **P1.** ★★★ (10 points) A particle moves according to the law of motion $s = f(t) = \sin(\pi t/2)$, $t \ge 0$, where $t$ is measured in seconds and $s$ in meters.
> - (a) Find the velocity at time $t$.
> - (b) When is the particle at rest?
> - (c) When is the particle moving in the positive direction?
> - (d) Find the total distance traveled during the first 6 seconds.
> - (e) During $0 < t < 6$, when is the particle speeding up? When is it slowing down?

> [!solution]- Solution of P1
> Exercise 3, assigned.
> $$
> \begin{aligned}
> &\text{(a)}\ v(t) = f'(t) = \frac{\pi}{2}\cos\frac{\pi t}{2} \\
> &\text{(b)}\ v(t) = 0 \iff \cos\frac{\pi t}{2} = 0 \iff t = 1, 3, 5, \dots \\
> &\text{(c)}\ v(t) > 0 \iff 0 \le t < 1,\ 3 < t < 5,\ 7 < t < 9, \dots \\
> &\text{(d)}\ f(0) = 0,\ f(1) = 1,\ f(3) = -1,\ f(5) = 1,\ f(6) = 0 \\
> &\qquad \lvert 1 - 0 \rvert + \lvert -1 - 1 \rvert + \lvert 1 - (-1) \rvert + \lvert 0 - 1 \rvert = 1 + 2 + 2 + 1 = 6 \text{ m} \\
> &\text{(e)}\ a(t) = v'(t) = -\frac{\pi^2}{4}\sin\frac{\pi t}{2}:\ a < 0 \text{ on } (0, 2) \text{ and } (4, 6),\ a > 0 \text{ on } (2, 4) \\
> &\qquad \text{speeding up } (v, a \text{ same sign}):\ 1 < t < 2,\ 3 < t < 4,\ 5 < t < 6 \\
> &\qquad \text{slowing down } (v, a \text{ opposite signs}):\ 0 < t < 1,\ 2 < t < 3,\ 4 < t < 5
> \end{aligned}
> $$

> [!question]
> **P2.** ★★ (10 points) The force $F$ acting on a body with mass $m$ and velocity $v$ is the rate of change of momentum: $F = \dfrac{d}{dt}(mv)$. In the theory of relativity the mass of a particle varies with $v$ as $m = \dfrac{m_0}{\sqrt{1 - v^2/c^2}}$, where $m_0$ is the mass of the particle at rest and $c$ is the speed of light. Show that
> $$
> F = \frac{m_0a}{(1 - v^2/c^2)^{3/2}}, \qquad \text{where } a = \frac{dv}{dt}.
> $$

> [!proof]- Proof of P2
> Exercise 23, assigned.
> $$
> \begin{aligned}
> \frac{dm}{dt} &= m_0 \cdot \left(-\frac{1}{2}\right)\left(1 - \frac{v^2}{c^2}\right)^{-3/2} \cdot \left(-\frac{2v}{c^2}\right) \cdot \frac{dv}{dt} = \frac{m_0va}{c^2(1 - v^2/c^2)^{3/2}} && \text{(Chain Rule)} \\
> F &= \frac{d}{dt}(mv) = \frac{dm}{dt} \cdot v + m \cdot \frac{dv}{dt} && \text{(Product Rule)} \\
> &= \frac{m_0a \cdot \dfrac{v^2}{c^2}}{(1 - v^2/c^2)^{3/2}} + \frac{m_0a\left(1 - \dfrac{v^2}{c^2}\right)}{(1 - v^2/c^2)^{3/2}} = \frac{m_0a}{(1 - v^2/c^2)^{3/2}} \qquad \blacksquare
> \end{aligned}
> $$

> [!question]
> **P3.** ★★ (10 points) If $p(x)$ is the total value of the production when there are $x$ workers in a plant, then the average productivity of the workforce is $A(x) = \dfrac{p(x)}{x}$.
> - (a) Find $A'(x)$.
> - (b) Show that $A'(x) > 0$ if $p'(x)$ is greater than the average productivity.

> [!solution]- Solution of P3
> Exercise 33, assigned.
> $$
> \begin{aligned}
> &\text{(a)}\ A'(x) = \frac{xp'(x) - p(x) \cdot 1}{x^2} && \text{(by Quotient Rule)} \\
> &\text{(b)}\ p'(x) > A(x) = \frac{p(x)}{x} \implies xp'(x) > p(x) && (x > 0) \\
> &\qquad \implies xp'(x) - p(x) > 0 \implies A'(x) = \frac{xp'(x) - p(x)}{x^2} > 0 && (x^2 > 0)
> \end{aligned}
> $$

## §2.8 Related Rates

### 2.8 Exam Points

- **Strategy (p. 187):** draw a diagram; give symbols to the quantities that are functions of $t$; write the given rate and the required rate as derivatives; write an equation that relates the quantities, using geometry to eliminate a variable if necessary; differentiate both sides with respect to $t$ by the Chain Rule; then substitute and solve. See [[Related Rates]].
- **WARNING (p. 187) [T/F] ★★★:** substitute the numerical values only after differentiating. The rate of a decreasing quantity is negative.
- **[Calc 10] ★★★★** the five models of the examples: the sphere $V = \frac{4}{3}\pi r^3$ (Example 1); the ladder $x^2 + y^2 = 25$ (Example 2); the conical tank with similar triangles, $V = \frac{\pi}{12}h^3$ (Example 3); two cars, $z^2 = x^2 + y^2$ (Example 4); the rotating spotlight, $x = 6\tan\theta$ (Example 5).
- **Assigned types:** areas and volumes (1, 3, 5, 7); a curve $4x^2 + 9y^2 = 25$ (9); a shadow by similar triangles (15); distances by the Pythagorean Theorem (17, 19, 20); the area of a triangle (21, 31); a trough and a cone (27, 29); Boyle's Law and resistors (37, 39); the Law of Cosines (41, 43); angles (47, 49).
- **Angles in degrees** are changed to radians before differentiating: $2^{\circ}$ per minute is $\frac{\pi}{90}$ rad/min (43).

### 2.8 True or False

> [!question]
> Respond with true (T) or false (F).
> - (a) In a related rates problem, the numerical values of the quantities that vary with time should be substituted before differentiating.
> - (b) If the volume of a spherical balloon increases at a constant rate, then its radius increases at a constant rate.
> - (c) If each side of a square is increasing at a rate of $6$ cm/s, then the area of the square is increasing at a rate of $48$ cm²/s when the area is $16$ cm².
> - (d) A ladder $5$ m long rests against a vertical wall. If the bottom of the ladder slides away from the wall at $1$ m/s, then the top slides down the wall at $1$ m/s.

> [!solution]- Answers
> - (a) **F.** Substitute after differentiating (WARNING, p. 187). With $r = 25$ put in first, $V$ would be a constant and $\frac{dV}{dt} = 0$.
> - (b) **F.** $\frac{dr}{dt} = \frac{1}{4\pi r^2}\frac{dV}{dt}$, which gets smaller as $r$ grows (p. 186).
> - (c) **T.** $A = x^2$, so $\frac{dA}{dt} = 2x\frac{dx}{dt} = 2 \cdot 4 \cdot 6 = 48$ (Exercise 3, assigned).
> - (d) **F.** $\frac{dy}{dt} = -\frac{x}{y}\frac{dx}{dt}$ depends on the position; when $x = 3$ it is $-0.75$ m/s (Example 2).

### 2.8 Multiple Choice

> [!question]
> **MC 1.** (5 points) Suppose $4x^2 + 9y^2 = 25$, where $x$ and $y$ are functions of $t$. Which of the following statements are true?
> - A. $8x\dfrac{dx}{dt} + 18y\dfrac{dy}{dt} = 0$
> - B. If $\dfrac{dy}{dt} = \dfrac{1}{3}$, then $\dfrac{dx}{dt} = -\dfrac{3}{8}$ when $x = 2$ and $y = 1$.
> - C. If $\dfrac{dx}{dt} = 3$, then $\dfrac{dy}{dt} = \dfrac{8}{3}$ when $x = -2$ and $y = 1$.
> - D. $\dfrac{dx}{dt}$ and $\dfrac{dy}{dt}$ always have opposite signs.

> [!solution]- Answer to MC 1
> **A, B, C.** (Exercise 9, assigned: [[CAL1 HW 2.8 Solutions#ST 2.8.9|ST 2.8.9]].)
> - A. Differentiate both sides with respect to $t$.
> - B. $8 \cdot 2 \cdot \frac{dx}{dt} + 18 \cdot 1 \cdot \frac{1}{3} = 0 \implies \frac{dx}{dt} = -\frac{3}{8}$.
> - C. $8 \cdot (-2) \cdot 3 + 18 \cdot 1 \cdot \frac{dy}{dt} = 0 \implies \frac{dy}{dt} = \frac{8}{3}$.
> - D fails: in C both rates are positive.

### 2.8 Computation and Proof

> [!question]
> **P1.** ★★★★ (10 points) A street light is mounted at the top of a 6-meter-tall pole. A man 2 m tall walks away from the pole with a speed of 1.5 m/s along a straight path. How fast is the tip of his shadow moving when he is 10 m from the pole?

> [!solution]- Solution of P1
> Exercise 15, assigned: [[CAL1 HW 2.8 Solutions#ST 2.8.15|ST 2.8.15]]. Let $x$ be the distance from the pole to the man and $y$ the distance from the pole to the tip of his shadow, in meters.
> $$
> \begin{aligned}
> &\text{Given: } \frac{dx}{dt} = 1.5 \text{ m/s}. \qquad \text{Unknown: } \frac{dy}{dt} \text{ when } x = 10. \\
> &\text{Similar triangles: } \frac{y - x}{y} = \frac{2}{6} \implies 6y - 6x = 2y \implies y = \frac{3}{2}x \\
> &\frac{dy}{dt} = \frac{3}{2}\frac{dx}{dt} = \frac{3}{2}(1.5) = 2.25 \text{ m/s}
> \end{aligned}
> $$
> The tip of the shadow moves at $2.25$ m/s, at every distance from the pole.

> [!question]
> **P2.** ★★★ (10 points) Gravel is being dumped from a conveyor belt at a rate of 3 m³/min, and its coarseness is such that it forms a pile in the shape of a cone whose base diameter and height are always equal. How fast is the height of the pile increasing when the pile is 3 m high?

> [!solution]- Solution of P2
> Exercise 29, assigned: [[CAL1 HW 2.8 Solutions#ST 2.8.29|ST 2.8.29]]. Let $V$ be the volume, $r$ the base radius, and $h$ the height of the pile.
> $$
> \begin{aligned}
> &\text{Given: } \frac{dV}{dt} = 3 \text{ m}^3\text{/min}. \qquad \text{Unknown: } \frac{dh}{dt} \text{ when } h = 3. \\
> &2r = h \implies r = \frac{h}{2} \implies V = \frac{1}{3}\pi r^2h = \frac{\pi}{12}h^3 \\
> &\frac{dV}{dt} = \frac{\pi}{4}h^2\frac{dh}{dt} \implies 3 = \frac{\pi}{4}(3)^2\frac{dh}{dt} \implies \frac{dh}{dt} = \frac{4}{3\pi} \approx 0.42 \text{ m/min}
> \end{aligned}
> $$

> [!question]
> **P3.** ★★★ (10 points) A plane flies horizontally at an altitude of 5 km and passes directly over a tracking telescope on the ground. When the angle of elevation is $\pi/3$, this angle is decreasing at a rate of $\pi/6$ rad/min. How fast is the plane traveling at that time?

> [!solution]- Solution of P3
> Exercise 47, assigned: [[CAL1 HW 2.8 Solutions#ST 2.8.47|ST 2.8.47]]. Let $x$ be the horizontal distance from the telescope to the plane, in km, and $\theta$ the angle of elevation.
> $$
> \begin{aligned}
> &\text{Given: } \frac{d\theta}{dt} = -\frac{\pi}{6} \text{ rad/min when } \theta = \frac{\pi}{3}. \qquad \text{Unknown: } \frac{dx}{dt}. \\
> &\tan\theta = \frac{5}{x} \implies x = 5\cot\theta \implies \frac{dx}{dt} = -5\csc^2\theta\,\frac{d\theta}{dt} \\
> &\frac{dx}{dt} = -5 \cdot \frac{4}{3} \cdot \left(-\frac{\pi}{6}\right) = \frac{10\pi}{9} \approx 3.49 \text{ km/min} && \left(\csc^2\tfrac{\pi}{3} = \tfrac{4}{3}\right)
> \end{aligned}
> $$

> [!question]
> **P4.** ★★★ (10 points) Two straight roads diverge from an intersection at an angle of $60^{\circ}$. Two cars leave the intersection at the same time, the first traveling down one road at 60 km/h and the second traveling down the other road at 100 km/h. How fast is the distance between the cars changing after half an hour?

> [!solution]- Solution of P4
> Exercise 41, assigned: [[CAL1 HW 2.8 Solutions#ST 2.8.41|ST 2.8.41]]. Let $a$ and $b$ be the distances of the cars from the intersection and $z$ the distance between the cars, in km, with $t$ in hours.
> $$
> \begin{aligned}
> &\text{Given: } \frac{da}{dt} = 60,\ \frac{db}{dt} = 100. \qquad \text{Unknown: } \frac{dz}{dt} \text{ when } t = \frac{1}{2}. \\
> &z^2 = a^2 + b^2 - 2ab\cos 60^{\circ} = a^2 + b^2 - ab && \text{(Law of Cosines)} \\
> &2z\frac{dz}{dt} = 2a\frac{da}{dt} + 2b\frac{db}{dt} - a\frac{db}{dt} - b\frac{da}{dt} \\
> &t = \frac{1}{2}:\ a = 30,\ b = 50,\ z = \sqrt{900 + 2500 - 1500} = 10\sqrt{19} \\
> &20\sqrt{19}\,\frac{dz}{dt} = 3600 + 10000 - 3000 - 3000 = 7600 \implies \frac{dz}{dt} = \frac{380}{\sqrt{19}} = 20\sqrt{19} \approx 87.2 \text{ km/h}
> \end{aligned}
> $$

## §2.9 Linear Approximations and Differentials

### 2.9 Exam Points

- **[[Linearization]] (p. 192):** $L(x) = f(a) + f'(a)(x - a)$, the function whose graph is the tangent line at $(a, f(a))$. The [[Linear Approximation|linear approximation]] is $f(x) \approx L(x)$ for $x$ near $a$.
- **[[Differential|Differentials]] (p. 194):** $dy = f'(x)\,dx$, where $dx$ is an independent variable. $\Delta y = f(x + \Delta x) - f(x)$ is the rise of the curve and $dy$ is the rise of the tangent line (Figure 5); $f(a + dx) \approx f(a) + dy$.
- **[Calc] ★★★** estimate a number (31–36; 31, 33 assigned): choose $f$ and a nearby $a$ at which $f(a)$ is easy. $\sqrt{4.05} \approx 2.0125$ (Example 1).
- **[Calc] ★★★** errors (Example 4; 39, 41 assigned): the maximum error is about $\lvert dV \rvert$, the relative error is $\frac{dV}{V}$, and the percentage error is the relative error as a percentage. For a sphere $\frac{dV}{V} = 3\frac{dr}{r}$.
- **[T/F] [MC] ★★★** $\sin x \approx x$ and $\cos x \approx 1$ near $0$ (p. 194); the approximation is an overestimate where the tangent line lies above the curve (Example 1); $dy \ne \Delta y$ in general (Example 3; 23, 29 assigned).
- **[Proof 10] ★** "Show that" exercises: the volume of a thin cylindrical shell is about $2\pi rh\,\Delta r$ (43, assigned); in Ohm's Law the relative errors of $I$ and $R$ are about equal in magnitude (45, assigned); the rules for differentials (47).

### 2.9 True or False

> [!question]
> Respond with true (T) or false (F).
> - (a) The linearization of $f(x) = \sin x$ at $a = 0$ is $L(x) = x$.
> - (b) If $y = f(x)$ and $dx = \Delta x$, then $dy = \Delta y$.
> - (c) The linear approximation of $\sqrt{x + 3}$ at $a = 1$ gives an overestimate of $\sqrt{4.05}$.
> - (d) If the radius $r$ of a sphere is measured with relative error $\dfrac{dr}{r}$, then the relative error in the computed volume is about $3\dfrac{dr}{r}$.
> - (e) A linear approximation gives $(1.999)^4 \approx 15.968$.

> [!solution]- Answers
> - (a) **T.** $f(0) = 0$ and $f'(0) = \cos 0 = 1$, so $L(x) = 0 + 1 \cdot (x - 0) = x$.
> - (b) **F.** In Example 3, $y = x^3 + x^2 - 2x + 1$, $x = 2$, $\Delta x = 0.05$: $\Delta y = 0.717625$ but $dy = 0.7$. $dy$ is the change along the tangent line.
> - (c) **T.** $L(1.05) = 2.0125 > \sqrt{4.05} = 2.01246\dots$; the tangent line lies above the curve (Example 1).
> - (d) **T.** $V = \frac{4}{3}\pi r^3$, $dV = 4\pi r^2\,dr$, so $\frac{dV}{V} = 3\frac{dr}{r}$ (NOTE, p. 196).
> - (e) **T.** $f(x) = x^4$, $a = 2$: $f(1.999) \approx 16 + 32(-0.001) = 15.968$ (Exercise 31, assigned).

### 2.9 Multiple Choice

> [!question]
> **MC 1.** (5 points) Let $f(x) = \sqrt[3]{x}$ and let $L$ be the linearization of $f$ at $a = 8$. Which of the following statements are true?
> - A. $L(x) = 2 + \frac{1}{12}(x - 8)$
> - B. $\sqrt[3]{8.06} \approx 2.005$
> - C. The differential of $y = \sqrt[3]{x}$ is $dy = \frac{1}{3}x^{-2/3}\,dx$.
> - D. $L(x) \le f(x)$ for all $x$ near $8$.

> [!solution]- Answer to MC 1
> **A, B, C.** (Exercise 3, assigned: [[CAL1 HW 2.9 Solutions#ST 2.9.3|ST 2.9.3]].)
> - A, C. $f'(x) = \frac{1}{3}x^{-2/3}$, so $f'(8) = \frac{1}{12}$ and $f(8) = 2$.
> - B. $L(8.06) = 2 + \frac{0.06}{12} = 2.005$.
> - D fails: $f''(x) = -\frac{2}{9}x^{-5/3} < 0$ for $x > 0$, so the curve is concave downward and lies below its tangent line: $L(x) \ge f(x)$ near $8$.

### 2.9 Computation and Proof

> [!question]
> **P1.** ★★★ (10 points) Use a linear approximation (or differentials) to estimate $\sqrt[3]{1001}$.

> [!solution]- Solution of P1
> Exercise 33, assigned: [[CAL1 HW 2.9 Solutions#ST 2.9.33|ST 2.9.33]]. Let $f(x) = \sqrt[3]{x}$ and $a = 1000$.
> $$
> \begin{aligned}
> &f(1000) = 10,\qquad f'(x) = \frac{1}{3}x^{-2/3} \implies f'(1000) = \frac{1}{300} \\
> &L(x) = 10 + \frac{1}{300}(x - 1000) \implies \sqrt[3]{1001} \approx L(1001) = 10 + \frac{1}{300} \approx 10.0033
> \end{aligned}
> $$

> [!question]
> **P2.** ★★★ (10 points) The edge of a cube was found to be 30 cm with a possible error in measurement of 0.1 cm. Use differentials to estimate the maximum possible error, relative error, and percentage error in computing (a) the volume of the cube and (b) the surface area of the cube.

> [!solution]- Solution of P2
> Exercise 39, assigned: [[CAL1 HW 2.9 Solutions#ST 2.9.39|ST 2.9.39]]. Let $x$ be the edge, with $x = 30$ and $dx = 0.1$.
> $$
> \begin{aligned}
> &\text{(a)}\ V = x^3 \implies dV = 3x^2\,dx = 3(30)^2(0.1) = 270 \text{ cm}^3 \\
> &\qquad \frac{dV}{V} = \frac{270}{27000} = 0.01 = 1\% \\
> &\text{(b)}\ S = 6x^2 \implies dS = 12x\,dx = 12(30)(0.1) = 36 \text{ cm}^2 \\
> &\qquad \frac{dS}{S} = \frac{36}{5400} \approx 0.0067 = 0.67\%
> \end{aligned}
> $$

> [!question]
> **P3.** ★★ (10 points) Compute $\Delta y$ and $dy$ for $y = x^2 - 4x$, $x = 3$, and $dx = \Delta x = 0.5$.

> [!solution]- Solution of P3
> Exercise 23, assigned: [[CAL1 HW 2.9 Solutions#ST 2.9.23|ST 2.9.23]]. Let $f(x) = x^2 - 4x$.
> $$
> \begin{aligned}
> &\Delta y = f(3.5) - f(3) = (12.25 - 14) - (9 - 12) = -1.75 + 3 = 1.25 \\
> &dy = f'(x)\,dx = (2x - 4)\,dx = (2 \cdot 3 - 4)(0.5) = 1
> \end{aligned}
> $$

> [!question]
> **P4.** ★ (10 points) If a current $I$ passes through a resistor with resistance $R$, Ohm's Law states that the voltage drop is $V = RI$. If $V$ is constant and $R$ is measured with a certain error, use differentials to show that the relative error in calculating $I$ is approximately the same (in magnitude) as the relative error in $R$.

> [!proof]- Proof of P4
> Exercise 45, assigned: [[CAL1 HW 2.9 Solutions#ST 2.9.45|ST 2.9.45]].
> $$
> \begin{aligned}
> &I = \frac{V}{R} = VR^{-1} \implies dI = -\frac{V}{R^2}\,dR && (V \text{ is constant}) \\
> &\frac{\Delta I}{I} \approx \frac{dI}{I} = \frac{-\dfrac{V}{R^2}\,dR}{\dfrac{V}{R}} = -\frac{dR}{R} \implies \left\lvert \frac{dI}{I} \right\rvert = \left\lvert \frac{dR}{R} \right\rvert \qquad \blacksquare
> \end{aligned}
> $$

## §3.1 Maximum and Minimum Values

### 3.1 Exam Points

The full note for this section is [[CAL1 3.1 Exam Notes]].

- **Definitions (p. 210):** $f(c)$ is an [[Absolute Extreme Value|absolute]] maximum value if $f(c) \ge f(x)$ for all $x$ in the domain, and a [[Local Extreme Value|local]] maximum value if $f(c) \ge f(x)$ when $x$ is near $c$, that is, on an open interval containing $c$. So a local extreme value never occurs at an endpoint.
- **[T/F] [MC] ★★★ the Extreme Value Theorem (p. 211):** a function continuous on a closed interval $[a, b]$ attains an absolute maximum value and an absolute minimum value. Both hypotheses are needed (Figures 9 and 10, p. 212).
- **[Proof 10] ★★★★ [[Fermat's Theorem]] (p. 212):** if $f$ has a local maximum or minimum at $c$, and if $f'(c)$ exists, then $f'(c) = 0$. **[T/F]** the converse is false ($x^3$ at $0$), and an extreme value can occur where $f'$ does not exist ($\lvert x \rvert$ at $0$).
- **[[Critical Number]] (p. 214):** a number $c$ in the domain of $f$ such that $f'(c) = 0$ or $f'(c)$ does not exist. A local maximum or minimum occurs only at a critical number.
- **[Calc 10] ★★★ the [[Closed Interval Method]] (p. 214):** for $f$ continuous on $[a, b]$, compare the values of $f$ at the critical numbers in $(a, b)$ and at the endpoints (Example 8; 49–60, of which 53, 55, 57, 59 are assigned). Critical numbers with fractional powers: Example 7; 39, 41 (assigned).
- **[Proof 10] ★★** $x^{101} + x^{51} + x + 1$ has no local extreme value (72, assigned); Fermat's Theorem for a local minimum through $-f$ (73); a cubic has two, one, or no critical numbers (74).

### 3.1 True or False

> [!question]
> Respond with true (T) or false (F). Items (a)–(c) are from the True-False Quiz of the Chapter 3 Review ‡.
> - (a) ‡ If $f'(c) = 0$, then $f$ has a local maximum or minimum at $c$.
> - (b) ‡ If $f$ has an absolute minimum value at $c$, then $f'(c) = 0$.
> - (c) ‡ If $f$ is continuous on $(a, b)$, then $f$ attains an absolute maximum value $f(c)$ and an absolute minimum value $f(d)$ at some numbers $c$ and $d$ in $(a, b)$.
> - (d) If $f$ has a local maximum or minimum at $c$, then $c$ is a critical number of $f$.
> - ==(e)== If $f'(c)$ does not exist, then $c$ is a critical number of $f$.
> - ==(f)== If $f$ is continuous on $[a, b]$, then the absolute maximum value of $f$ on $[a, b]$ is also a local maximum value of $f$.

> [!solution]- Answers
> - (a) **F.** $f(x) = x^3$, $c = 0$: $f'(0) = 0$, but $f$ has no maximum or minimum at $0$ (Example 5).
> - (b) **F.** $f(x) = \lvert x \rvert$ has its absolute minimum at $0$, where $f'(0)$ does not exist (Example 6). Also $f(x) = x$ on $[0, 1]$: the minimum is at the endpoint $0$, where the slope is $1$.
> - (c) **F.** $f(x) = x$ on $(0, 1)$ has no maximum and no minimum value. The Extreme Value Theorem needs a closed interval.
> - (d) **T.** $c$ is in the domain; if $f'(c)$ exists, then $f'(c) = 0$ by Fermat's Theorem, and otherwise $f'(c)$ does not exist (p. 214).
> - (e) **F.** A critical number must be in the domain of $f$: for $f(x) = \frac{1}{x}$, $f'(0)$ does not exist, but $0$ is not a critical number.
> - (f) **F.** It can occur at an endpoint, which is never a local maximum: in Example 1, $f(-1) = 37$ is the absolute maximum on $[-1, 4]$.

### 3.1 Multiple Choice

> [!question]
> **MC 1.** (5 points) Let $f(x) = x^{3/5}(4 - x)$. Which of the following statements are true?
> - A. $f'(x) = \dfrac{12 - 8x}{5x^{2/5}}$
> - B. $\frac{3}{2}$ is a critical number of $f$.
> - C. $0$ is a critical number of $f$.
> - D. $f$ has a local maximum or minimum at each of its critical numbers.

> [!solution]- Answer to MC 1
> **A, B, C.** (Example 7, p. 214.)
> - A. $f'(x) = \frac{3}{5}x^{-2/5}(4 - x) - x^{3/5} = \frac{3(4 - x) - 5x}{5x^{2/5}} = \frac{12 - 8x}{5x^{2/5}}$.
> - B. $f'\left(\frac{3}{2}\right) = 0$.
> - C. $f'(0)$ does not exist and $0$ is in the domain.
> - D fails: $x^{2/5} > 0$ for $x \ne 0$, so $f'(x) > 0$ on both sides of $0$; $f$ has no maximum or minimum at $0$.

> [!question]
> **MC 2.** (5 points) Which of the following statements is true?
> - A. If $f$ is continuous on $[a, b]$, then $f$ attains an absolute maximum value and an absolute minimum value on $[a, b]$.
> - B. If $f$ is defined on $[a, b]$, then $f$ attains an absolute maximum value on $[a, b]$.
> - C. If $f$ is continuous on $(a, b)$, then $f$ attains an absolute maximum value on $(a, b)$.
> - D. If $f$ attains an absolute maximum value and an absolute minimum value on $[a, b]$, then $f$ is continuous on $[a, b]$.

> [!solution]- Answer to MC 2
> **A.** The Extreme Value Theorem.
> - B fails: $f(x) = x$ for $0 \le x < 1$ and $f(1) = 0$ on $[0, 1]$: the values come as close to $1$ as we like, but $1$ is never attained (compare Figure 9).
> - C fails: $f(x) = x$ on $(0, 1)$ (compare Figure 10).
> - D fails: $f(x) = 0$ for $x \ne \frac{1}{2}$ and $f\left(\frac{1}{2}\right) = 1$ on $[0, 1]$ attains its maximum value $1$ and its minimum value $0$, but it is not continuous at $\frac{1}{2}$.

### 3.1 Computation and Proof

> [!question]
> ==**P1.**== ★★★★ (10 points) State and prove Fermat's Theorem.

> [!proof]- Proof of P1
> **Fermat's Theorem.** If $f$ has a local maximum or minimum at $c$, and if $f'(c)$ exists, then $f'(c) = 0$.
> $$
> \begin{aligned}
> &\text{Suppose } f \text{ has a local maximum at } c. \\
> &\implies \exists\, \delta > 0 \text{ s.t. } f(c) \ge f(x) \text{ for all } x \text{ in } (c - \delta, c + \delta) \\
> &\implies f(c + h) - f(c) \le 0 \text{ if } \lvert h \rvert < \delta \qquad (\ast) \\[6pt]
> &\text{Since } f'(c) \text{ exists, } f'(c) = \lim_{h \to 0^+} \frac{f(c+h) - f(c)}{h} = \lim_{h \to 0^-} \frac{f(c+h) - f(c)}{h}. \\[6pt]
> &\text{If } 0 < h < \delta:\ \frac{f(c+h) - f(c)}{h} \le 0 && \text{(divide } (\ast) \text{ by } h > 0) \\
> &\qquad \implies f'(c) = \lim_{h \to 0^+} \frac{f(c+h) - f(c)}{h} \le 0 && \text{(limits preserve } \le) \\
> &\text{If } -\delta < h < 0:\ \frac{f(c+h) - f(c)}{h} \ge 0 && \text{(dividing by } h < 0 \text{ reverses } \le) \\
> &\qquad \implies f'(c) = \lim_{h \to 0^-} \frac{f(c+h) - f(c)}{h} \ge 0 \\[6pt]
> &\text{Hence } 0 \le f'(c) \le 0, \text{ so } f'(c) = 0. \\[6pt]
> &\text{If } f \text{ has a local minimum at } c, \text{ then } g = -f \text{ has a local maximum at } c, \\
> &\text{and } g'(c) = -f'(c) \text{ exists, so } g'(c) = 0 \text{ and } f'(c) = 0. \qquad \blacksquare
> \end{aligned}
> $$
> \# The version with every reason is [[CAL1 3.1 Exam Notes#Proof of Fermat's Theorem|Proof of Fermat's Theorem]]. The two lines that lose points: $(\ast)$ holds only for $\lvert h \rvert < \delta$, and "$f'(c)$ exists" is what makes both one-sided limits equal to $f'(c)$.

> [!question]
> **P2.** ★★★ (10 points) Find the absolute maximum and absolute minimum values of $f(t) = t - \sqrt[3]{t}$ on the interval $[-1, 4]$.

> [!solution]- Solution of P2
> Exercise 57, assigned: [[CAL1 HW 3.1 Solutions#ST 3.1.57|ST 3.1.57]]. $f$ is continuous on $[-1, 4]$, so the Closed Interval Method applies.
> $$
> \begin{aligned}
> &f'(t) = 1 - \frac{1}{3}t^{-2/3} = 1 - \frac{1}{3t^{2/3}} \\
> &f'(t) = 0 \iff t^{2/3} = \frac{1}{3} \iff t = \pm\left(\frac{1}{3}\right)^{3/2} = \pm\frac{\sqrt{3}}{9}; \qquad f'(t) \text{ does not exist} \iff t = 0 \\
> &\text{Critical numbers in } (-1, 4):\ -\frac{\sqrt{3}}{9},\ 0,\ \frac{\sqrt{3}}{9} \\
> &f\left(\frac{\sqrt{3}}{9}\right) = \frac{\sqrt{3}}{9} - \frac{\sqrt{3}}{3} = -\frac{2\sqrt{3}}{9} \approx -0.38,\qquad f\left(-\frac{\sqrt{3}}{9}\right) = \frac{2\sqrt{3}}{9} \approx 0.38 \\
> &f(0) = 0,\qquad f(-1) = -1 + 1 = 0,\qquad f(4) = 4 - \sqrt[3]{4} \approx 2.41
> \end{aligned}
> $$
> The absolute maximum value is $f(4) = 4 - \sqrt[3]{4}$ and the absolute minimum value is $f\left(\frac{\sqrt{3}}{9}\right) = -\frac{2\sqrt{3}}{9}$.
>
> \# $\sqrt[3]{\frac{\sqrt{3}}{9}} = \left(3^{-3/2}\right)^{1/3} = 3^{-1/2} = \frac{\sqrt{3}}{3}$.

> [!question]
> **P3.** ★★★ (10 points) Find the absolute maximum and absolute minimum values of $f(t) = 2\cos t + \sin 2t$ on the interval $[0, \pi/2]$.

> [!solution]- Solution of P3
> Exercise 59, assigned: [[CAL1 HW 3.1 Solutions#ST 3.1.59|ST 3.1.59]]. $f$ is continuous on $\left[0, \frac{\pi}{2}\right]$ and differentiable everywhere.
> $$
> \begin{aligned}
> &f'(t) = -2\sin t + 2\cos 2t = -2\sin t + 2(1 - 2\sin^2 t) = -2(2\sin t - 1)(\sin t + 1) \\
> &f'(t) = 0 \text{ in } \left(0, \tfrac{\pi}{2}\right) \iff \sin t = \frac{1}{2} \iff t = \frac{\pi}{6} \\
> &f\left(\frac{\pi}{6}\right) = \sqrt{3} + \frac{\sqrt{3}}{2} = \frac{3\sqrt{3}}{2} \approx 2.60,\qquad f(0) = 2,\qquad f\left(\frac{\pi}{2}\right) = 0
> \end{aligned}
> $$
> The absolute maximum value is $f\left(\frac{\pi}{6}\right) = \frac{3\sqrt{3}}{2}$ and the absolute minimum value is $f\left(\frac{\pi}{2}\right) = 0$.

> [!question]
> **P4.** ★★ (10 points) Prove that the function $f(x) = x^{101} + x^{51} + x + 1$ has neither a local maximum nor a local minimum.

> [!proof]- Proof of P4
> Exercise 72, assigned: [[CAL1 HW 3.1 Solutions#ST 3.1.72|ST 3.1.72]].
> $$
> \begin{aligned}
> &f \text{ is a polynomial} \implies f'(x) \text{ exists for all } x \\
> &f'(x) = 101x^{100} + 51x^{50} + 1 \ge 1 > 0 \text{ for all } x && (x^{100} \ge 0,\ x^{50} \ge 0) \\
> &\implies f \text{ has no critical number} \\
> &\implies f \text{ has neither a local maximum nor a local minimum,} \\
> &\qquad \text{because a local maximum or minimum occurs only at a critical number.} \qquad \blacksquare
> \end{aligned}
> $$

## §3.2 The Mean Value Theorem

### 3.2 Exam Points

- **[Proof 10] ★★★★ [[Rolle's Theorem]] (p. 220):** hypotheses 1. $f$ is continuous on the closed interval $[a, b]$; 2. $f$ is differentiable on the open interval $(a, b)$; 3. $f(a) = f(b)$. Conclusion: there is a number $c$ in $(a, b)$ such that $f'(c) = 0$. The proof has three cases and uses the Extreme Value Theorem and Fermat's Theorem.
- **[Proof 10] ★★★★ the [[Mean Value Theorem]] (p. 221):** hypotheses 1 and 2. Conclusion: there is a number $c$ in $(a, b)$ such that $f'(c) = \frac{f(b) - f(a)}{b - a}$, or $f(b) - f(a) = f'(c)(b - a)$. The proof applies Rolle's Theorem to $h(x) = f(x) - f(a) - \frac{f(b) - f(a)}{b - a}(x - a)$.
- **[Proof 10] ★★★** if $f'(x) = 0$ for all $x$ in an interval $(a, b)$, then $f$ is constant on $(a, b)$; if $f'(x) = g'(x)$ on $(a, b)$, then $f - g$ is constant (p. 224). **[T/F]** the domain must be an interval: $\frac{x}{\lvert x \rvert}$ (NOTE, p. 224; Exercise 37).
- **[Proof 10] ★★★** the number of solutions of an equation: exactly one (Example 2: the [[Intermediate Value Theorem]] gives one, Rolle's Theorem forbids two; 23, 24); at most one or two (25 assigned; 26, 27).
- **[Calc] [Proof] ★★★** bounds from the Mean Value Theorem (Example 5; 29, 31 assigned; 30, 32); inequalities such as $\sin x < x$ and $\lvert \sin a - \sin b \rvert \le \lvert a - b \rvert$ (33, 35 assigned).
- **[Calc] [MC] ★★★** verify the hypotheses and find every $c$ (9, 11, 15, 17 assigned); explain why a failure does not contradict the theorem: $1 - x^{2/3}$ is not differentiable at $0$ (13, assigned), and $(x - 3)^{-2}$ is not continuous at $3$ (21, assigned).

### 3.2 True or False

> [!question]
> Respond with true (T) or false (F). Items (a)–(d) are from the True-False Quiz of the Chapter 3 Review ‡.
> - (a) ‡ If $f$ is differentiable and $f(-1) = f(1)$, then there is a number $c$ such that $\lvert c \rvert < 1$ and $f'(c) = 0$.
> - (b) ‡ If $f'(x) = g'(x)$ for $0 < x < 1$, then $f(x) = g(x)$ for $0 < x < 1$.
> - (c) ‡ There exists a function $f$ such that $f(1) = -2$, $f(3) = 0$, and $f'(x) > 1$ for all $x$.
> - ==(d)== ‡ If $f'(x)$ exists and is nonzero for all $x$, then $f(1) \ne f(0)$.
> - ==(e)== If $f'(x) = 0$ for all $x$ in the domain of $f$, then $f$ is a constant function.
> - (f) If $f$ is continuous on $[a, b]$ and $f(a) = f(b)$, then there is a number $c$ in $(a, b)$ such that $f'(c) = 0$.

> [!solution]- Answers
> - (a) **T.** $f$ is continuous on $[-1, 1]$ and differentiable on $(-1, 1)$, and $f(-1) = f(1)$: Rolle's Theorem.
> - (b) **F.** Only $f - g$ is constant: $f(x) = x + 1$ and $g(x) = x$.
> - (c) **F.** By the Mean Value Theorem on $[1, 3]$ there is a $c$ with $f'(c) = \frac{0 - (-2)}{3 - 1} = 1$, which contradicts $f'(c) > 1$.
> - (d) **T.** If $f(1) = f(0)$, Rolle's Theorem on $[0, 1]$ would give a $c$ with $f'(c) = 0$.
> - (e) **F.** $f(x) = \frac{x}{\lvert x \rvert}$ has $f'(x) = 0$ on its domain, which is not an interval, and $f$ is not constant (NOTE, p. 224).
> - (f) **F.** Differentiability on $(a, b)$ is missing: $f(x) = \lvert x \rvert$ on $[-1, 1]$.

### 3.2 Multiple Choice

> [!question]
> **MC 1.** (5 points) Let $f(x) = 1 - x^{2/3}$ on the interval $[-1, 1]$. Which of the following statements are true?
> - A. $f$ is continuous on $[-1, 1]$.
> - B. $f(-1) = f(1)$.
> - C. $f$ is differentiable on $(-1, 1)$.
> - D. There is no number $c$ in $(-1, 1)$ such that $f'(c) = 0$.

> [!solution]- Answer to MC 1
> **A, B, D.** (Exercise 13, assigned: [[CAL1 HW 3.2 Solutions#ST 3.2.13|ST 3.2.13]].)
> - B. $f(-1) = 1 - 1 = 0 = f(1)$.
> - C fails: $f'(x) = -\frac{2}{3}x^{-1/3}$ does not exist at $x = 0$.
> - D. $f'(x) = -\frac{2}{3x^{1/3}} \ne 0$ for every $x \ne 0$. This does not contradict Rolle's Theorem, because hypothesis 2 fails.

> [!question]
> **MC 2.** (5 points) Suppose that $f$ is continuous on $[1, 4]$ and differentiable on $(1, 4)$, that $f(1) = 10$, and that $f'(x) \ge 2$ for $1 < x < 4$. Which of the following statements are true?
> - A. $f(4) - f(1) = 3f'(c)$ for some number $c$ in $(1, 4)$.
> - B. $f(4) \ge 16$.
> - C. $f(4) = 15$ is possible.
> - D. $f(4) = 20$ is possible.

> [!solution]- Answer to MC 2
> **A, B, D.** (Exercise 29, assigned: [[CAL1 HW 3.2 Solutions#ST 3.2.29|ST 3.2.29]].)
> - A. The Mean Value Theorem on $[1, 4]$.
> - B. $f(4) = f(1) + 3f'(c) \ge 10 + 3 \cdot 2 = 16$; so C fails.
> - D. $f(x) = 10 + \frac{10}{3}(x - 1)$ has $f'(x) = \frac{10}{3} \ge 2$ and $f(4) = 20$.

### 3.2 Computation and Proof

> [!question]
> ==**P1.**== ★★★★ (10 points) State and prove Rolle's Theorem.

> [!proof]- Proof of P1
> **Rolle's Theorem.** Let $f$ be a function that satisfies the following three hypotheses: 1. $f$ is continuous on the closed interval $[a, b]$; 2. $f$ is differentiable on the open interval $(a, b)$; 3. $f(a) = f(b)$. Then there is a number $c$ in $(a, b)$ such that $f'(c) = 0$.
> $$
> \begin{aligned}
> &\textbf{Case I: } f(x) = k, \text{ a constant, on } [a, b]. \\
> &\qquad f'(x) = 0, \text{ so } c \text{ can be any number in } (a, b). \\[6pt]
> &\textbf{Case II: } f(x) > f(a) \text{ for some } x \text{ in } (a, b). \\
> &\qquad f \text{ is continuous on } [a, b], \text{ so by the Extreme Value Theorem} \\
> &\qquad f \text{ has a maximum value } f(c) \text{ for some } c \text{ in } [a, b]. \\
> &\qquad f(c) \ge f(x) > f(a) = f(b) \implies c \ne a,\ c \ne b \implies c \text{ is in } (a, b) \\
> &\qquad \implies f \text{ has a local maximum at } c, \text{ and } f'(c) \text{ exists} && \text{(hypothesis 2)} \\
> &\qquad \implies f'(c) = 0 && \text{(Fermat's Theorem)} \\[6pt]
> &\textbf{Case III: } f(x) < f(a) \text{ for some } x \text{ in } (a, b). \\
> &\qquad \text{By the Extreme Value Theorem, } f \text{ has a minimum value } f(c) \text{ for some } c \text{ in } [a, b]. \\
> &\qquad f(c) \le f(x) < f(a) = f(b) \implies c \text{ is in } (a, b) \\
> &\qquad \implies f \text{ has a local minimum at } c \implies f'(c) = 0 && \text{(Fermat's Theorem)} \qquad \blacksquare
> \end{aligned}
> $$

> [!question]
> ==**P2.**== ★★★★ (10 points) State and prove the Mean Value Theorem.

> [!proof]- Proof of P2
> **The Mean Value Theorem.** Let $f$ be a function that satisfies the following hypotheses: 1. $f$ is continuous on the closed interval $[a, b]$; 2. $f$ is differentiable on the open interval $(a, b)$. Then there is a number $c$ in $(a, b)$ such that $f'(c) = \dfrac{f(b) - f(a)}{b - a}$.
> $$
> \begin{aligned}
> &\text{Let } h(x) = f(x) - f(a) - \frac{f(b) - f(a)}{b - a}(x - a) \text{ for } x \text{ in } [a, b]. \\[6pt]
> &1.\ h \text{ is continuous on } [a, b]: \text{ it is the sum of } f \text{ and a first-degree polynomial.} \\
> &2.\ h \text{ is differentiable on } (a, b), \text{ and } h'(x) = f'(x) - \frac{f(b) - f(a)}{b - a}. \\
> &3.\ h(a) = f(a) - f(a) - 0 = 0, \qquad h(b) = f(b) - f(a) - [f(b) - f(a)] = 0 \implies h(a) = h(b). \\[6pt]
> &\text{By Rolle's Theorem, } \exists\, c \text{ in } (a, b) \text{ s.t. } h'(c) = 0 \\
> &\implies 0 = f'(c) - \frac{f(b) - f(a)}{b - a} \implies f'(c) = \frac{f(b) - f(a)}{b - a}. \qquad \blacksquare
> \end{aligned}
> $$
> \# $h(x)$ is the vertical distance between the graph of $f$ and the secant line through $(a, f(a))$ and $(b, f(b))$. All three hypotheses of Rolle's Theorem must be checked in writing.

> [!question]
> ==**P3.**== ★★★ (10 points) Prove: if $f'(x) = 0$ for all $x$ in an interval $(a, b)$, then $f$ is constant on $(a, b)$.

> [!proof]- Proof of P3
> $$
> \begin{aligned}
> &\text{Let } x_1 \text{ and } x_2 \text{ be any two numbers in } (a, b) \text{ with } x_1 < x_2. \\
> &f \text{ is differentiable on } (a, b) \implies f \text{ is differentiable on } (x_1, x_2) \text{ and continuous on } [x_1, x_2] \\
> &\text{By the Mean Value Theorem, } \exists\, c \text{ in } (x_1, x_2) \text{ s.t. } f(x_2) - f(x_1) = f'(c)(x_2 - x_1). \\
> &f'(c) = 0 \implies f(x_2) - f(x_1) = 0 \cdot (x_2 - x_1) = 0 \\
> &\implies f(x_2) = f(x_1) \\
> &\text{Hence } f \text{ has the same value at any two numbers in } (a, b): \\
> &f \text{ is constant on } (a, b). \qquad \blacksquare
> \end{aligned}
> $$
> \# Corollary (p. 224): if $f'(x) = g'(x)$ on $(a, b)$, let $F = f - g$; then $F' = f' - g' = 0$, so $F$ is constant, that is, $f(x) = g(x) + c$.

> [!question]
> ==**P4.**== ★★★ (10 points) Show that the equation $x^3 - 15x + c = 0$ has at most one solution in the interval $[-2, 2]$.

> [!proof]- Proof of P4
> Exercise 25, assigned: [[CAL1 HW 3.2 Solutions#ST 3.2.25|ST 3.2.25]]. Let $f(x) = x^3 - 15x + c$.
> $$
> \begin{aligned}
> &\text{Suppose the equation has two solutions } a < b \text{ in } [-2, 2]: f(a) = f(b) = 0. \\
> &f \text{ is a polynomial} \implies f \text{ is continuous on } [a, b] \text{ and differentiable on } (a, b) \\
> &\implies \exists\, r \text{ in } (a, b) \text{ s.t. } f'(r) = 0 && \text{(Rolle's Theorem)} \\
> &\text{But } -2 \le a < r < b \le 2 \implies r^2 < 4 \implies f'(r) = 3r^2 - 15 = 3(r^2 - 5) < 0. \text{ Contradiction.} \\
> &\text{Hence the equation has at most one solution in } [-2, 2]. \qquad \blacksquare
> \end{aligned}
> $$

> [!question]
> ==**P5.**== ★★★ (10 points) Use the Mean Value Theorem to prove the inequality $\lvert \sin a - \sin b \rvert \le \lvert a - b \rvert$ for all $a$ and $b$.

> [!proof]- Proof of P5
> Exercise 35, assigned: [[CAL1 HW 3.2 Solutions#ST 3.2.35|ST 3.2.35]].
> $$  
> \begin{aligned}  
> &\text{If } a = b, \text{ both sides are } 0. \\  
> &\text{Suppose } b < a. \; f(x) = \sin x \text{ is continuous on } [b, a] \text{ and differentiable on } (b, a) \\  
> &\implies \exists\, c \text{ in } (b, a) \text{ s.t. } \sin a - \sin b = \cos c \cdot (a - b) && \text{(Mean Value Theorem)} \\  
> &\implies \lvert \sin a - \sin b \rvert = \lvert \cos c \rvert \lvert a - b \rvert \le \lvert a - b \rvert && (\lvert \cos c \rvert \le 1) \\  
> &\text{If } a < b, \text{ then } \lvert \sin a - \sin b \rvert = \lvert \sin b - \sin a \rvert \le \lvert b - a \rvert = \lvert a - b \rvert && \text{(by the case above)} \qquad \blacksquare  
> \end{aligned}  
> $$

> [!question]
> ==**P6.**== ★★★ (10 points) Show that the equation $2x + \cos x = 0$ has exactly one real solution.

> [!proof]- Proof of P6
> Exercise 23; the method of Example 2. Let $f(x) = 2x + \cos x$, which is continuous and differentiable for all $x$.
> $$
> \begin{aligned}
> &\textbf{At least one: } f(-\pi) = -2\pi - 1 < 0 < 1 = f(0) \\
> &\qquad \implies f(r) = 0 \text{ for some } r \text{ in } (-\pi, 0) && \text{(Intermediate Value Theorem)} \\
> &\textbf{At most one: } \text{suppose } f(a) = f(b) = 0 \text{ with } a < b. \\
> &\qquad \implies \exists\, c \text{ in } (a, b) \text{ s.t. } f'(c) = 0 && \text{(Rolle's Theorem)} \\
> &\qquad \text{But } f'(x) = 2 - \sin x \ge 1 > 0 \text{ for all } x. \text{ Contradiction.} \\
> &\text{Hence the equation has exactly one real solution.} \qquad \blacksquare
> \end{aligned}
> $$

## §3.3 What Derivatives Tell Us about the Shape of a Graph

### 3.3 Exam Points

- **[Proof 10] ★★★★ the [[Increasing and Decreasing Test|Increasing/Decreasing Test]] (p. 226):** (a) if $f'(x) > 0$ on an interval, then $f$ is increasing on that interval; (b) if $f'(x) < 0$ on an interval, then $f$ is decreasing on that interval. The proof applies the Mean Value Theorem on $[x_1, x_2]$ (p. 227).
- **The [[First Derivative Test]] (p. 228):** for a critical number $c$ of a continuous function $f$: if $f'$ changes from positive to negative at $c$, a local maximum; from negative to positive, a local minimum; no change of sign, neither.
- **[[Concavity]] (p. 230):** $f$ is concave upward on $I$ if its graph lies above all of its tangents on $I$. Concavity Test: $f''(x) > 0$ on $I$ gives concave upward, $f''(x) < 0$ gives concave downward. An [[Inflection Point|inflection point]] is a point where $f$ is continuous and the curve changes its direction of concavity (p. 231).
- **The [[Second Derivative Test]] (p. 231):** suppose $f''$ is continuous near $c$. If $f'(c) = 0$ and $f''(c) > 0$, a local minimum; if $f'(c) = 0$ and $f''(c) < 0$, a local maximum. It is inconclusive when $f''(c) = 0$, and it fails when $f''(c)$ does not exist (NOTE, p. 232).
- **[T/F] ★★★★** $f''(c) = 0$ does not give an inflection point ($x^4$, Exercise 76); an inflection point can occur where $f''$ does not exist ($x\lvert x \rvert$, Exercise 77); an increasing function need not have $f' > 0$ everywhere ($x^3$); sums, products and reciprocals of increasing functions (Chapter 3 Review ‡).
- **[MC] ★★★★** read the graph of $f'$ (5–8, 37, 38; 5 assigned): $f$ increases where $f' > 0$; a local maximum where $f'$ changes from positive to negative; concave upward where $f'$ increases; inflection points where $f'$ has a local maximum or minimum. Sketch a graph from conditions on $f'$ and $f''$ (Example 5; 29, 31, 33, 35 assigned).
- **[Calc 10] ★★★★** the full analysis: intervals of increase and decrease, local maximum and minimum values, intervals of concavity, inflection points, and a sketch (Examples 1, 6, 7; 9–22 and 39–52, of which 11, 13, 17, 19, 21, 23, 39, 41, 43, 49 are assigned). Critical numbers where $f'$ does not exist count too (Example 7).
- **[Proof 10] ★★** a cubic has exactly one inflection point, at $x = \frac{x_1 + x_2 + x_3}{3}$ (73, assigned); find the cubic with given local extreme values (67, assigned); at an inflection point with $f''$ continuous, $f''(c) = 0$ (75); $f'(x) > 0$ except at a single number still gives increasing (79).

### 3.3 True or False

> [!question]
> Respond with true (T) or false (F). Items (a)–(k) are from the True-False Quiz of the Chapter 3 Review ‡.
> - (a) ‡ If $f'(x) < 0$ for $1 < x < 6$, then $f$ is decreasing on $(1, 6)$.
> - (b) ‡ If $f''(2) = 0$, then $(2, f(2))$ is an inflection point of the curve $y = f(x)$.
> - (c) ‡ There exists a function $f$ such that $f(x) > 0$, $f'(x) < 0$, and $f''(x) > 0$ for all $x$.
> - (d) ‡ There exists a function $f$ such that $f(x) < 0$, $f'(x) < 0$, and $f''(x) > 0$ for all $x$.
> - (e) ‡ If $f$ and $g$ are increasing on an interval $I$, then $f + g$ is increasing on $I$.
> - (f) ‡ If $f$ and $g$ are increasing on an interval $I$, then $f - g$ is increasing on $I$.
> - (g) ‡ If $f$ and $g$ are increasing on an interval $I$, then $fg$ is increasing on $I$.
> - (h) ‡ If $f$ and $g$ are positive increasing functions on an interval $I$, then $fg$ is increasing on $I$.
> - (i) ‡ If $f$ is increasing and $f(x) > 0$ on $I$, then $g(x) = 1/f(x)$ is decreasing on $I$.
> - (j) ‡ If $f$ is even, then $f'$ is even.
> - (k) ‡ If $f$ is periodic, then $f'$ is periodic.
> - (l) If $f'(c) = 0$ and $f''(c) = 0$, then $f$ has neither a local maximum nor a local minimum at $c$.

> [!solution]- Answers
> - (a) **T.** The Increasing/Decreasing Test.
> - (b) **F.** $f(x) = (x - 2)^4$: $f''(2) = 0$, but $f''(x) = 12(x - 2)^2 \ge 0$ does not change sign, so the concavity does not change.
> - (c) **T.** $f(x) = \sqrt{x^2 + 1} - x$: $f(x) > 0$ because $\sqrt{x^2 + 1} > \lvert x \rvert \ge x$; $f'(x) = \frac{x}{\sqrt{x^2 + 1}} - 1 < 0$; $f''(x) = \frac{1}{(x^2 + 1)^{3/2}} > 0$.
> - (d) **F.** $f'' > 0$ makes the graph lie above its tangent line at $0$: $f(x) \ge f(0) + f'(0)x$. Since $f'(0) < 0$, the right side tends to $\infty$ as $x \to -\infty$, so $f(x) > 0$ for some $x$.
> - (e) **T.** $x_1 < x_2 \implies f(x_1) < f(x_2)$ and $g(x_1) < g(x_2) \implies f(x_1) + g(x_1) < f(x_2) + g(x_2)$.
> - (f) **F.** $f(x) = x$, $g(x) = 2x$: $f(x) - g(x) = -x$ is decreasing.
> - (g) **F.** $f(x) = g(x) = x$ on $(-\infty, 0)$: $f(x)g(x) = x^2$ is decreasing there.
> - (h) **T.** $0 < f(x_1) < f(x_2)$ and $0 < g(x_1) < g(x_2) \implies f(x_1)g(x_1) < f(x_2)g(x_2)$.
> - (i) **T.** $0 < f(x_1) < f(x_2) \implies \frac{1}{f(x_1)} > \frac{1}{f(x_2)}$.
> - (j) **F.** $f'$ is odd (Exercise 2.5.83): $x^2$ has derivative $2x$.
> - (k) **T.** $f(x + p) = f(x)$ for all $x$ gives $f'(x + p) = f'(x)$ by the Chain Rule.
> - (l) **F.** $f(x) = x^4$, $c = 0$: $f'(0) = f''(0) = 0$, and $f(0) = 0$ is a local minimum. The Second Derivative Test is inconclusive here.

### 3.3 Multiple Choice

> [!question]
> **MC 1.** (5 points) Suppose the derivative of a function $f$ is $f'(x) = (x - 4)^2(x + 3)^7(x - 5)^8$. Which of the following statements are true?
> - A. $f$ has a local minimum at $x = -3$.
> - B. $f$ has a local maximum at $x = 4$.
> - C. $f$ has neither a local maximum nor a local minimum at $x = 5$.
> - D. $f$ is decreasing on $(-\infty, -3)$.

> [!solution]- Answer to MC 1
> **A, C, D.** (Exercise 25.) $(x - 4)^2 \ge 0$ and $(x - 5)^8 \ge 0$, so $f'(x)$ has the sign of $(x + 3)^7$: negative for $x < -3$, positive for $x > -3$ with $x \ne 4, 5$.
> - A. $f'$ changes from negative to positive at $-3$.
> - B fails, and C holds: $f'$ does not change sign at $4$ or at $5$.
> - D. $f'(x) < 0$ on $(-\infty, -3)$.

> [!question]
> **MC 2.** (5 points) Suppose $f''$ is continuous on $(-\infty, \infty)$. Which of the following statements are true?
> - A. If $f'(2) = 0$ and $f''(2) = -5$, then $f$ has a local maximum at $2$.
> - B. If $f'(6) = 0$ and $f''(6) = 0$, then $f$ has an inflection point at $6$.
> - C. If $f'(6) = 0$ and $f''(6) = 0$, then $f$ may have a local maximum, a local minimum, or neither at $6$.
> - D. If $f''(x) > 0$ for all $x$, then $f$ has a local minimum.

> [!solution]- Answer to MC 2
> **A, C.** (Exercise 27.)
> - A. The Second Derivative Test.
> - B fails, and C holds: $-(x - 6)^4$ has a local maximum at $6$, $(x - 6)^4$ a local minimum, and $(x - 6)^3$ neither; only the last has an inflection point there.
> - D fails: $f(x) = \sqrt{x^2 + 1} - x$ has $f'' > 0$ and $f' < 0$ for all $x$, so it has no local minimum.

> [!question]
> **MC 3.** (5 points) Let $f(x) = x^4 - 4x^3$. Which of the following statements are true?
> - A. The critical numbers of $f$ are $0$ and $3$.
> - B. $f(3) = -27$ is a local minimum value.
> - C. $f(0) = 0$ is a local maximum value.
> - D. The inflection points are $(0, 0)$ and $(2, -16)$.

> [!solution]- Answer to MC 3
> **A, B, D.** (Example 6, p. 232.) $f'(x) = 4x^2(x - 3)$ and $f''(x) = 12x(x - 2)$.
> - B. $f'(3) = 0$ and $f''(3) = 36 > 0$.
> - C fails: $f'(x) < 0$ for $x < 0$ and for $0 < x < 3$, so $f$ has no local maximum or minimum at $0$.
> - D. $f'' > 0$ on $(-\infty, 0)$, $f'' < 0$ on $(0, 2)$, $f'' > 0$ on $(2, \infty)$.

### 3.3 Computation and Proof

> [!question]
> **P1.** ★★★★ (10 points) Prove the Increasing/Decreasing Test: if $f'(x) > 0$ on an interval, then $f$ is increasing on that interval.

> [!proof]- Proof of P1
> $$
> \begin{aligned}
> &\text{Let } x_1 \text{ and } x_2 \text{ be any two numbers in the interval with } x_1 < x_2. \\
> &f'(x) > 0 \text{ on the interval} \implies f \text{ is differentiable on } [x_1, x_2] \\
> &\implies f \text{ is continuous on } [x_1, x_2] \text{ and differentiable on } (x_1, x_2) \\
> &\text{By the Mean Value Theorem, } \exists\, c \text{ in } (x_1, x_2) \text{ s.t. } f(x_2) - f(x_1) = f'(c)(x_2 - x_1). \\
> &f'(c) > 0 \text{ and } x_2 - x_1 > 0 \implies f(x_2) - f(x_1) > 0 \implies f(x_1) < f(x_2) \\
> &\text{Hence } f \text{ is increasing on the interval.} \qquad \blacksquare
> \end{aligned}
> $$
> \# The last line is the definition of an increasing function: $f(x_1) < f(x_2)$ whenever $x_1 < x_2$. Part (b) is the same with $f'(c) < 0$, which gives $f(x_1) > f(x_2)$.

> [!question]
> **P2.** ★★★★ (10 points) Let $f(x) = x^4 - 2x^2 + 3$.
> - (a) Find the intervals on which $f$ is increasing or decreasing.
> - (b) Find the local maximum and minimum values of $f$.
> - (c) Find the intervals of concavity and the inflection points.

> [!solution]- Solution of P2
> Exercise 19, assigned: [[CAL1 HW 3.3 Solutions#ST 3.3.19|ST 3.3.19]].
> $$
> \begin{aligned}
> &f'(x) = 4x^3 - 4x = 4x(x + 1)(x - 1), \qquad \text{critical numbers } -1,\ 0,\ 1 \\
> &x < -1:\ f' < 0; \qquad -1 < x < 0:\ f' > 0; \qquad 0 < x < 1:\ f' < 0; \qquad x > 1:\ f' > 0 \\
> &\text{(a) increasing on } (-1, 0) \text{ and } (1, \infty); \text{ decreasing on } (-\infty, -1) \text{ and } (0, 1) \\
> &\text{(b) by the First Derivative Test: local minimum values } f(-1) = 2 \text{ and } f(1) = 2; \\
> &\qquad \text{local maximum value } f(0) = 3 \\
> &\text{(c)}\ f''(x) = 12x^2 - 4 = 4(3x^2 - 1): \quad f'' > 0 \iff \lvert x \rvert > \tfrac{\sqrt{3}}{3} \\
> &\qquad \text{concave upward on } \left(-\infty, -\tfrac{\sqrt{3}}{3}\right) \text{ and } \left(\tfrac{\sqrt{3}}{3}, \infty\right) \\
> &\qquad \text{concave downward on } \left(-\tfrac{\sqrt{3}}{3}, \tfrac{\sqrt{3}}{3}\right) \\
> &\qquad \text{inflection points } \left(\pm\tfrac{\sqrt{3}}{3}, \tfrac{22}{9}\right), \text{ since } f\left(\pm\tfrac{\sqrt{3}}{3}\right) = \tfrac{1}{9} - \tfrac{2}{3} + 3 = \tfrac{22}{9}
> \end{aligned}
> $$

> [!question]
> **P3.** ★★★ (10 points) Let $C(x) = x^{1/3}(x + 4)$.
> - (a) Find the intervals of increase or decrease.
> - (b) Find the local maximum and minimum values.
> - (c) Find the intervals of concavity and the inflection points.

> [!solution]- Solution of P3
> Exercise 49, assigned: [[CAL1 HW 3.3 Solutions#ST 3.3.49|ST 3.3.49]]. $C(x) = x^{4/3} + 4x^{1/3}$ is continuous for all $x$.
> $$
> \begin{aligned}
> &C'(x) = \frac{4}{3}x^{1/3} + \frac{4}{3}x^{-2/3} = \frac{4(x + 1)}{3x^{2/3}} \\
> &\text{critical numbers: } -1 \ (C' = 0) \text{ and } 0 \ (C' \text{ does not exist}) \\
> &x^{2/3} > 0 \text{ for } x \ne 0:\quad C' < 0 \text{ for } x < -1; \quad C' > 0 \text{ for } -1 < x < 0 \text{ and for } x > 0 \\
> &\text{(a) decreasing on } (-\infty, -1); \text{ increasing on } (-1, \infty) \\
> &\text{(b) local minimum value } C(-1) = -3; \text{ no local maximum } (C' \text{ does not change sign at } 0) \\
> &\text{(c)}\ C''(x) = \frac{4}{9}x^{-2/3} - \frac{8}{9}x^{-5/3} = \frac{4(x - 2)}{9x^{5/3}} \\
> &\qquad C'' > 0 \text{ for } x < 0 \text{ and for } x > 2; \quad C'' < 0 \text{ for } 0 < x < 2 \\
> &\qquad \text{concave upward on } (-\infty, 0) \text{ and } (2, \infty); \text{ concave downward on } (0, 2) \\
> &\qquad \text{inflection points } (0, 0) \text{ and } \left(2, 6\sqrt[3]{2}\right)
> \end{aligned}
> $$
> \# $(0, 0)$ is an inflection point although $C''(0)$ does not exist: $C$ is continuous there and the concavity changes. The tangent at $(0, 0)$ is vertical.

> [!question]
> **P4.** ★★★ (10 points) Show that a cubic function (a third-degree polynomial) always has exactly one point of inflection. If its graph has three $x$-intercepts $x_1$, $x_2$, and $x_3$, show that the $x$-coordinate of the inflection point is $(x_1 + x_2 + x_3)/3$.

> [!proof]- Proof of P4
> Exercise 73, assigned: [[CAL1 HW 3.3 Solutions#ST 3.3.73|ST 3.3.73]]. Let $f(x) = ax^3 + bx^2 + cx + d$ with $a \ne 0$.
> $$
> \begin{aligned}
> &f''(x) = 6ax + 2b = 6a\left(x + \frac{b}{3a}\right) \\
> &6a \ne 0 \implies f'' \text{ changes sign at } x = -\frac{b}{3a} \text{ and nowhere else, and } f \text{ is continuous} \\
> &\implies \text{exactly one inflection point, at } x = -\frac{b}{3a}. \\[6pt]
> &\text{If the } x\text{-intercepts are } x_1, x_2, x_3: \\
> &f(x) = a(x - x_1)(x - x_2)(x - x_3) = a\left[x^3 - (x_1 + x_2 + x_3)x^2 + \cdots\right] \\
> &\implies b = -a(x_1 + x_2 + x_3) \implies -\frac{b}{3a} = \frac{x_1 + x_2 + x_3}{3} \qquad \blacksquare
> \end{aligned}
> $$

> [!question]
> **P5.** ★★ (10 points) Find a cubic function $f(x) = ax^3 + bx^2 + cx + d$ that has a local maximum value of $3$ at $x = -2$ and a local minimum value of $0$ at $x = 1$.

> [!solution]- Solution of P5
> Exercise 67, assigned: [[CAL1 HW 3.3 Solutions#ST 3.3.67|ST 3.3.67]].
> $$
> \begin{aligned}
> &f'(x) = 3ax^2 + 2bx + c; \quad f \text{ is differentiable, so } f'(-2) = 0 \text{ and } f'(1) = 0 && \text{(Fermat's Theorem)} \\
> &12a - 4b + c = 0,\quad 3a + 2b + c = 0 \implies 9a - 6b = 0 \implies b = \frac{3}{2}a,\quad c = -3a - 2b = -6a \\
> &f(1) = 0:\ a + b + c + d = 0 \implies d = \frac{7}{2}a \\
> &f(-2) = 3:\ -8a + 4b - 2c + d = \frac{27}{2}a = 3 \implies a = \frac{2}{9},\ b = \frac{1}{3},\ c = -\frac{4}{3},\ d = \frac{7}{9} \\
> &f(x) = \frac{1}{9}(2x^3 + 3x^2 - 12x + 7)
> \end{aligned}
> $$
> Check: $f'(x) = \frac{2}{3}(x + 2)(x - 1)$ changes from positive to negative at $-2$ and from negative to positive at $1$.

## §3.4 Limits at Infinity; Horizontal Asymptotes

### 3.4 Exam Points

- **Definitions:** $\lim_{x \to \infty} f(x) = L$ (p. 238) and $\lim_{x \to -\infty} f(x) = L$; the line $y = L$ is a [[Horizontal Asymptote|horizontal asymptote]] if either limit is $L$ (p. 239). A curve can have two horizontal asymptotes, and it can cross one. See [[Limit at Infinity]].
- **The basic limit (p. 240):** if $r > 0$ is a rational number, then $\lim_{x \to \infty} \frac{1}{x^r} = 0$, and $\lim_{x \to -\infty} \frac{1}{x^r} = 0$ when $x^r$ is defined for all $x$. The Limit Laws of §1.6 also hold for $x \to \pm\infty$, except the two for $\lim_{x \to a} x^n$ and $\lim_{x \to a} \sqrt[n]{x}$.
- **[Calc 10] ★★★★ techniques:** divide numerator and denominator by the highest power of $x$ in the denominator (Example 3); with a square root, $\sqrt{x^2} = \lvert x \rvert = -x$ for $x < 0$ (Example 4: the two asymptotes $y = \pm\frac{\sqrt{2}}{3}$); multiply by the conjugate (Example 5; 25, 27 assigned); substitute $t = \frac{1}{x}$ (Example 6; 31 assigned); $\lim_{x \to \infty} \sin x$ does not exist (Example 7).
- **Infinite limits at infinity (p. 243):** the Limit Laws cannot be applied to infinite limits. $\lim_{x \to \infty}(x^2 - x) = \lim_{x \to \infty} x(x - 1) = \infty$ (Example 9; 21, 29 assigned).
- **[Proof 10] ★★★ precise definitions (pp. 244–247):** $\lim_{x \to \infty} f(x) = L$ means that for every $\varepsilon > 0$ there is a number $N$ such that if $x > N$ then $\lvert f(x) - L \rvert < \varepsilon$; for $x \to -\infty$ the condition is "if $x < N$"; $\lim_{x \to \infty} f(x) = \infty$ means that for every $M > 0$ there is $N > 0$ such that if $x > N$ then $f(x) > M$. Proofs: $\lim_{x \to \infty} \frac{1}{x} = 0$ (Example 13); $\lim_{x \to \infty} \frac{1}{x^2} = 0$ (71, assigned); $\lim_{x \to -\infty} \frac{1}{x} = 0$ (73, assigned); $\lim_{x \to \infty} x^3 = \infty$ (74). [[CAL1 Quiz 02]] and Midterm 1 each had a proof by the precise definition.
- **[Calc] [MC] ★★★** horizontal and vertical asymptotes of a rational function (35–40; 37 assigned); limits read from a graph (3, 4 assigned); the Squeeze Theorem at infinity (63; 65 assigned); a sketch from given limits (57, 58 assigned) or from asymptotes and derivatives (49, 51 assigned).

### 3.4 True or False

> [!question]
> Respond with true (T) or false (F).
> - (a) A curve $y = f(x)$ can have at most one horizontal asymptote.
> - (b) The graph of a function can intersect its horizontal asymptote.
> - (c) $\displaystyle\lim_{x \to \infty}(x^2 - x) = \lim_{x \to \infty} x^2 - \lim_{x \to \infty} x = \infty - \infty = 0$
> - (d) $\displaystyle\lim_{x \to -\infty} \frac{\sqrt{2x^2 + 1}}{3x - 5} = \frac{\sqrt{2}}{3}$
> - (e) ‡ If $f$ has domain $[0, \infty)$ and has no horizontal asymptote, then $\lim_{x \to \infty} f(x) = \infty$ or $\lim_{x \to \infty} f(x) = -\infty$.
> - (f) $\displaystyle\lim_{x \to \infty} x\sin\frac{1}{x} = 1$

> [!solution]- Answers
> - (a) **F.** $y = \frac{\sqrt{2x^2 + 1}}{3x - 5}$ has the two horizontal asymptotes $y = \frac{\sqrt{2}}{3}$ and $y = -\frac{\sqrt{2}}{3}$ (Example 4).
> - (b) **T.** $y = \frac{\sin x}{x}$ crosses its asymptote $y = 0$ infinitely often (Exercise 63).
> - (c) **F.** The Limit Laws do not apply to infinite limits; $x^2 - x = x(x - 1) \to \infty$ (Example 9).
> - (d) **F.** For $x < 0$, $\sqrt{x^2} = -x$, so the limit is $-\frac{\sqrt{2}}{3}$ (Example 4).
> - (e) **F.** $f(x) = \sin x$ on $[0, \infty)$ has no horizontal asymptote, and $\lim_{x \to \infty} \sin x$ does not exist.
> - (f) **T.** Let $t = \frac{1}{x}$; then $t \to 0^+$ and $x\sin\frac{1}{x} = \frac{\sin t}{t} \to 1$ (Exercise 31, assigned).

### 3.4 Multiple Choice

> [!question]
> **MC 1.** (5 points) Let $f(x) = \dfrac{\sqrt{2x^2 + 1}}{3x - 5}$. Which of the following statements are true?
> - A. $y = \frac{\sqrt{2}}{3}$ is a horizontal asymptote of the curve $y = f(x)$.
> - B. $y = -\frac{\sqrt{2}}{3}$ is a horizontal asymptote of the curve $y = f(x)$.
> - C. $x = \frac{5}{3}$ is a vertical asymptote of the curve $y = f(x)$.
> - D. $\displaystyle\lim_{x \to -\infty} f(x) = \frac{\sqrt{2}}{3}$

> [!solution]- Answer to MC 1
> **A, B, C.** (Example 4, pp. 241–242.)
> - A. For $x > 0$: $\frac{\sqrt{2x^2 + 1}}{3x - 5} = \frac{\sqrt{2 + \frac{1}{x^2}}}{3 - \frac{5}{x}} \to \frac{\sqrt{2}}{3}$ as $x \to \infty$.
> - B. For $x < 0$, $\frac{\sqrt{2x^2 + 1}}{x} = -\sqrt{2 + \frac{1}{x^2}}$, so the limit as $x \to -\infty$ is $-\frac{\sqrt{2}}{3}$; so D fails.
> - C. As $x$ approaches $\frac{5}{3}$ from the right, the numerator tends to $\sqrt{\frac{59}{9}} > 0$ and $3x - 5 \to 0^+$, so $f(x) \to \infty$.

> [!question]
> **MC 2.** (5 points) Which of the following statements are true?
> - A. $\displaystyle\lim_{t \to \infty}\left(\sqrt{25t^2 + 2} - 5t\right) = 0$
> - B. $\displaystyle\lim_{x \to \infty}\left(\sqrt{x^2 + ax} - \sqrt{x^2 + bx}\right) = \frac{a - b}{2}$
> - C. $\displaystyle\lim_{x \to -\infty}(x^2 + 2x^7) = \infty$
> - D. $\displaystyle\lim_{r \to \infty} \frac{r - r^3}{2 - r^2 + 3r^3} = -\frac{1}{3}$

> [!solution]- Answer to MC 2
> **A, B, D.** (Exercises 25, 27, 29, 13, all assigned: [[CAL1 HW 3.4 Solutions]].)
> - A. Multiply by the conjugate: $\frac{2}{\sqrt{25t^2 + 2} + 5t} \to 0$.
> - B. Multiply by the conjugate: $\frac{(a - b)x}{\sqrt{x^2 + ax} + \sqrt{x^2 + bx}} = \frac{a - b}{\sqrt{1 + \frac{a}{x}} + \sqrt{1 + \frac{b}{x}}} \to \frac{a - b}{2}$.
> - C fails: $x^2 + 2x^7 = x^7\left(\frac{1}{x^5} + 2\right) \to -\infty$, because $x^7 \to -\infty$ and the other factor tends to $2$.
> - D. Divide by $r^3$: $\frac{\frac{1}{r^2} - 1}{\frac{2}{r^3} - \frac{1}{r} + 3} \to -\frac{1}{3}$.

### 3.4 Computation and Proof

> [!question]
> **P1.** ★★★ (10 points) Prove, using the precise definition of a limit at infinity, that $\displaystyle\lim_{x \to \infty} \frac{1}{x^2} = 0$.

> [!proof]- Proof of P1
> Exercise 71 (b), assigned: [[CAL1 HW 3.4 Solutions#ST 3.4.71|ST 3.4.71]].
> $$
> \begin{aligned}
> &\text{Given any } \varepsilon > 0, \text{ we take } N = \frac{1}{\sqrt{\varepsilon}} > 0. \\
> &\text{If } x > N, \text{ then } x > \frac{1}{\sqrt{\varepsilon}} > 0 \implies x^2 > \frac{1}{\varepsilon} \implies \frac{1}{x^2} < \varepsilon. \\
> &\text{Then } \left\lvert \frac{1}{x^2} - 0 \right\rvert = \frac{1}{x^2} < \varepsilon. \\
> &\text{Hence } \lim_{x \to \infty} \frac{1}{x^2} = 0 \text{ by the definition of a limit at infinity.} \qquad \blacksquare
> \end{aligned}
> $$
> \# How $N$ is found on scratch paper: $\frac{1}{x^2} < \varepsilon \iff x^2 > \frac{1}{\varepsilon} \iff x > \frac{1}{\sqrt{\varepsilon}}$ for $x > 0$.

> [!question]
> **P2.** ★★★ (10 points) Prove, using the precise definition of a limit at negative infinity, that $\displaystyle\lim_{x \to -\infty} \frac{1}{x} = 0$.

> [!proof]- Proof of P2
> Exercise 73, assigned: [[CAL1 HW 3.4 Solutions#ST 3.4.73|ST 3.4.73]].
> $$
> \begin{aligned}
> &\text{Given any } \varepsilon > 0, \text{ we take } N = -\frac{1}{\varepsilon} < 0. \\
> &\text{If } x < N, \text{ then } x < -\frac{1}{\varepsilon} < 0 \implies \lvert x \rvert = -x > \frac{1}{\varepsilon} \implies \frac{1}{\lvert x \rvert} < \varepsilon. \\
> &\text{Then } \left\lvert \frac{1}{x} - 0 \right\rvert = \frac{1}{\lvert x \rvert} < \varepsilon. \\
> &\text{Hence } \lim_{x \to -\infty} \frac{1}{x} = 0 \text{ by the definition of a limit at negative infinity.} \qquad \blacksquare
> \end{aligned}
> $$
> \# The same pattern proves $\lim_{x \to \infty} x^3 = \infty$ (Exercise 74): given any $M > 0$, take $N = \sqrt[3]{M} > 0$; if $x > N$, then $x^3 > N^3 = M$.

> [!question]
> **P3.** ★★★★ (10 points) Find the limit: $\displaystyle\lim_{x \to -\infty}\left(\sqrt{4x^2 + 3x} + 2x\right)$.

> [!solution]- Solution of P3
> Exercise 26.
> $$
> \begin{aligned}
> \lim_{x \to -\infty}\left(\sqrt{4x^2 + 3x} + 2x\right) &= \lim_{x \to -\infty}\left(\sqrt{4x^2 + 3x} + 2x\right) \cdot \frac{\sqrt{4x^2 + 3x} - 2x}{\sqrt{4x^2 + 3x} - 2x} \\
> &= \lim_{x \to -\infty} \frac{(4x^2 + 3x) - 4x^2}{\sqrt{4x^2 + 3x} - 2x} = \lim_{x \to -\infty} \frac{3x}{\sqrt{4x^2 + 3x} - 2x} \\
> &= \lim_{x \to -\infty} \frac{3}{-\sqrt{4 + \frac{3}{x}} - 2} && \left(\text{divide by } x;\ \sqrt{x^2} = -x \text{ for } x < 0\right) \\
> &= \frac{3}{-\sqrt{4 + 0} - 2} = -\frac{3}{4}
> \end{aligned}
> $$

> [!question]
> **P4.** ★★★ (10 points) Evaluate the limit and justify each step by indicating the appropriate properties of limits: $\displaystyle\lim_{x \to \infty} \frac{2x^2 - 7}{5x^2 + x - 3}$.

> [!solution]- Solution of P4
> Exercise 7. This is the format of Midterm 1 Q3 and Q4.
> $$
> \begin{aligned}
> \lim_{x \to \infty} \frac{2x^2 - 7}{5x^2 + x - 3} &= \lim_{x \to \infty} \frac{2 - \dfrac{7}{x^2}}{5 + \dfrac{1}{x} - \dfrac{3}{x^2}} && (\text{divide by } x^2,\ x \ne 0) \\
> &= \frac{\lim\limits_{x \to \infty}\left(2 - \dfrac{7}{x^2}\right)}{\lim\limits_{x \to \infty}\left(5 + \dfrac{1}{x} - \dfrac{3}{x^2}\right)} && \text{(by Quotient Law)} \\
> &= \frac{\lim\limits_{x \to \infty} 2 - 7\lim\limits_{x \to \infty} \dfrac{1}{x^2}}{\lim\limits_{x \to \infty} 5 + \lim\limits_{x \to \infty} \dfrac{1}{x} - 3\lim\limits_{x \to \infty} \dfrac{1}{x^2}} && \text{(by Sum, Difference and Constant Multiple Laws)} \\
> &= \frac{2 - 7 \cdot 0}{5 + 0 - 3 \cdot 0} = \frac{2}{5} && \left(\lim\limits_{x \to \infty} c = c,\ \lim\limits_{x \to \infty} \tfrac{1}{x^r} = 0\right)
> \end{aligned}
> $$

> [!question]
> **P5.** ★★ (10 points) Find $\lim_{x \to \infty} f(x)$ if
> $$
> \frac{4x - 1}{x} < f(x) < \frac{4x^2 + 3x}{x^2}
> $$
> for all $x > 5$.

> [!solution]- Solution of P5
> Exercise 65, assigned: [[CAL1 HW 3.4 Solutions#ST 3.4.65|ST 3.4.65]].
> $$
> \begin{aligned}
> &\lim_{x \to \infty} \frac{4x - 1}{x} = \lim_{x \to \infty}\left(4 - \frac{1}{x}\right) = 4, \qquad \lim_{x \to \infty} \frac{4x^2 + 3x}{x^2} = \lim_{x \to \infty}\left(4 + \frac{3}{x}\right) = 4 \\
> &\because \frac{4x - 1}{x} < f(x) < \frac{4x^2 + 3x}{x^2} \text{ for all } x > 5 \text{ and both limits are } 4 \\
> &\therefore \lim_{x \to \infty} f(x) = 4 \text{ by the Squeeze Theorem.}
> \end{aligned}
> $$

> [!question]
> **P6.** ★★★ (10 points) Find the horizontal and vertical asymptotes of the curve $y = \dfrac{2x^2 + x - 1}{x^2 + x - 2}$.

> [!solution]- Solution of P6
> Exercise 37, assigned: [[CAL1 HW 3.4 Solutions#ST 3.4.37|ST 3.4.37]].
> $$
> \begin{aligned}
> &\lim_{x \to \pm\infty} \frac{2x^2 + x - 1}{x^2 + x - 2} = \lim_{x \to \pm\infty} \frac{2 + \frac{1}{x} - \frac{1}{x^2}}{1 + \frac{1}{x} - \frac{2}{x^2}} = 2 \implies \text{horizontal asymptote } y = 2 \\
> &y = \frac{(2x - 1)(x + 1)}{(x + 2)(x - 1)}: \text{ the denominator is } 0 \text{ at } x = -2 \text{ and } x = 1, \text{ where the numerator is } 5 \text{ and } 2 \\
> &\lim_{x \to 1^+} y = \infty,\quad \lim_{x \to -2^+} y = -\infty \implies \text{vertical asymptotes } x = 1 \text{ and } x = -2
> \end{aligned}
> $$

## §3.5 Summary of Curve Sketching

### 3.5 Exam Points

- **Guidelines A–H (pp. 251–252):** A. Domain; B. Intercepts; C. Symmetry (even, $f(-x) = f(x)$: about the $y$-axis; odd, $f(-x) = -f(x)$: about the origin; periodic); D. Asymptotes (horizontal, vertical, slant); E. Intervals of increase or decrease; F. Local maximum or minimum values; G. Concavity and points of inflection; H. Sketch the curve. See [[Curve Sketching]].
- **[[Slant Asymptote]] (p. 255):** the line $y = mx + b$ with $m \ne 0$ is a slant asymptote if $\lim_{x \to \infty}[f(x) - (mx + b)] = 0$, or the same as $x \to -\infty$. A rational function has one when the degree of the numerator is one more than the degree of the denominator; find it by long division (Example 4).
- **[Calc 10] ★★★** sketch a curve with the guidelines: a rational function with asymptotes (Example 1; 9, 53, 55, 57 assigned); a root and a restricted domain (Example 2; 23, 29 assigned); a periodic function (Example 3; 35 assigned); a polynomial (5 assigned).
- **[Calc] [MC] ★★★** the equation of a slant asymptote (49–52; 51 assigned).
- **[Proof 10] ★★** $y = \sqrt{4x^2 + 9}$ has the slant asymptotes $y = 2x$ and $y = -2x$ (59, assigned); the lines $y = \pm\frac{b}{a}x$ are slant asymptotes of the hyperbola $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$ (61, assigned).
- **[T/F] ★★** a number outside the domain gives no inflection point and no local extreme value (Example 1: $x = \pm 1$; Example 2: $-\frac{4}{3}$ is not a critical number).

### 3.5 True or False

> [!question]
> Respond with true (T) or false (F).
> - (a) The curve $y = \dfrac{x^3}{x^2 + 1}$ has the slant asymptote $y = x$.
> - (b) The curve $y = \dfrac{2x^2}{x^2 - 1}$ has inflection points at $x = \pm 1$, because $y''$ changes sign there.
> - (c) If $f(-x) = -f(x)$ for all $x$ in the domain of $f$, then the graph of $f$ is symmetric about the $y$-axis.
> - (d) Every rational function whose numerator has a higher degree than its denominator has a slant asymptote.
> - (e) The curve $y = \sqrt{4x^2 + 9}$ has two slant asymptotes.

> [!solution]- Answers
> - (a) **T.** $\frac{x^3}{x^2 + 1} = x - \frac{x}{x^2 + 1}$ and $\frac{x}{x^2 + 1} \to 0$ as $x \to \pm\infty$ (Example 4).
> - (b) **F.** $1$ and $-1$ are not in the domain; the lines $x = \pm 1$ are vertical asymptotes (Example 1).
> - (c) **F.** $f$ is odd, and its graph is symmetric about the origin.
> - (d) **F.** The degree must be exactly one more: $\frac{x^3 + 1}{x} = x^2 + \frac{1}{x}$ approaches the parabola $y = x^2$ (Exercise 62).
> - (e) **T.** $y = 2x$ as $x \to \infty$ and $y = -2x$ as $x \to -\infty$ (Exercise 59, assigned).

### 3.5 Multiple Choice

> [!question]
> **MC 1.** (5 points) Let $f(x) = \dfrac{x^2}{x - 1}$. Which of the following statements are true?
> - A. $x = 1$ is a vertical asymptote.
> - B. $y = x + 1$ is a slant asymptote.
> - C. $f(0) = 0$ is a local maximum value and $f(2) = 4$ is a local minimum value.
> - D. $f$ is concave upward on $(-\infty, 1)$.

> [!solution]- Answer to MC 1
> **A, B, C.** (Exercise 53, assigned: [[CAL1 HW 3.5 Solutions#ST 3.5.53|ST 3.5.53]].)
> - A, B. $f(x) = x + 1 + \frac{1}{x - 1}$ by long division; $\frac{1}{x - 1} \to 0$ as $x \to \pm\infty$ and $\lim_{x \to 1^+} f(x) = \infty$.
> - C. $f'(x) = 1 - \frac{1}{(x - 1)^2} = \frac{x(x - 2)}{(x - 1)^2}$ changes from positive to negative at $0$ and from negative to positive at $2$.
> - D fails: $f''(x) = \frac{2}{(x - 1)^3} < 0$ for $x < 1$, so $f$ is concave downward on $(-\infty, 1)$.

> [!question]
> **MC 2.** (5 points) Let $f(x) = \dfrac{2x^2}{x^2 - 1}$. Which of the following statements are true?
> - A. $f$ is an even function.
> - B. $y = 2$ is a horizontal asymptote.
> - C. $f(0) = 0$ is a local minimum value.
> - D. $f$ is concave upward on $(-1, 1)$.

> [!solution]- Answer to MC 2
> **A, B.** (Example 1, pp. 252–253.)
> - C fails: $f'(x) = \frac{-4x}{(x^2 - 1)^2}$ changes from positive to negative at $0$, so $f(0) = 0$ is a local maximum value.
> - D fails: $f''(x) = \frac{12x^2 + 4}{(x^2 - 1)^3} < 0$ for $\lvert x \rvert < 1$, so $f$ is concave downward on $(-1, 1)$.

### 3.5 Computation and Proof

> [!question]
> **P1.** ★★★ (10 points) Use the guidelines of curve sketching to sketch the curve $y = \dfrac{x^3 + 4}{x^2}$. In guideline D, find an equation of the slant asymptote.

> [!solution]- Solution of P1
> Exercise 55, assigned: [[CAL1 HW 3.5 Solutions#ST 3.5.55|ST 3.5.55]]. $f(x) = x + \dfrac{4}{x^2}$.
> $$
> \begin{aligned}
> &\textbf{A. } \text{Domain: } x \ne 0. \qquad \textbf{B. } x\text{-intercept: } x^3 = -4,\ x = -\sqrt[3]{4}; \text{ no } y\text{-intercept.} \qquad \textbf{C. } \text{No symmetry.} \\
> &\textbf{D. } \lim_{x \to 0} \left(x + \frac{4}{x^2}\right) = \infty \implies \text{vertical asymptote } x = 0 \\
> &\qquad f(x) - x = \frac{4}{x^2} \to 0 \text{ as } x \to \pm\infty \implies \text{slant asymptote } y = x \\
> &\textbf{E. } f'(x) = 1 - \frac{8}{x^3} = \frac{x^3 - 8}{x^3}: \text{ increasing on } (-\infty, 0) \text{ and } (2, \infty); \text{ decreasing on } (0, 2) \\
> &\textbf{F. } \text{local minimum value } f(2) = 3; \text{ no local maximum} \\
> &\textbf{G. } f''(x) = \frac{24}{x^4} > 0: \text{ concave upward on } (-\infty, 0) \text{ and } (0, \infty); \text{ no inflection point}
> \end{aligned}
> $$
> **H.** The curve lies above the line $y = x$ because $\frac{4}{x^2} > 0$. For $x < 0$ it rises along $y = x$, crosses the $x$-axis at $-\sqrt[3]{4}$, and goes to $\infty$ as $x \to 0^-$. For $x > 0$ it comes down from $\infty$, reaches the minimum point $(2, 3)$, and then rises toward $y = x$.

> [!question]
> **P2.** ★★★ (10 points) Show that the curve $y = \sqrt{4x^2 + 9}$ has two slant asymptotes: $y = 2x$ and $y = -2x$.

> [!proof]- Proof of P2
> Exercise 59, assigned: [[CAL1 HW 3.5 Solutions#ST 3.5.59|ST 3.5.59]].
> $$
> \begin{aligned}
> \lim_{x \to \infty}\left[\sqrt{4x^2 + 9} - 2x\right] &= \lim_{x \to \infty} \frac{(4x^2 + 9) - 4x^2}{\sqrt{4x^2 + 9} + 2x} = \lim_{x \to \infty} \frac{9}{\sqrt{4x^2 + 9} + 2x} = 0 \\
> \lim_{x \to -\infty}\left[\sqrt{4x^2 + 9} - (-2x)\right] &= \lim_{x \to -\infty} \frac{(4x^2 + 9) - 4x^2}{\sqrt{4x^2 + 9} - 2x} = \lim_{x \to -\infty} \frac{9}{\sqrt{4x^2 + 9} - 2x} = 0
> \end{aligned}
> $$
> In the first limit $\sqrt{4x^2 + 9} + 2x \to \infty$ as $x \to \infty$; in the second $-2x \to \infty$ as $x \to -\infty$, so $\sqrt{4x^2 + 9} - 2x \to \infty$. Hence $y = 2x$ and $y = -2x$ are slant asymptotes, by the definition of a slant asymptote. $\blacksquare$

> [!question]
> **P3.** ★★ (10 points) Find an equation of the slant asymptote of the curve $y = \dfrac{2x^3 - 5x^2 + 3x}{x^2 - x - 2}$.

> [!solution]- Solution of P3
> Exercise 51, assigned: [[CAL1 HW 3.5 Solutions#ST 3.5.51|ST 3.5.51]]. Long division:
> $$
> \begin{aligned}
> &2x^3 - 5x^2 + 3x = (2x - 3)(x^2 - x - 2) + (4x - 6) \implies y = 2x - 3 + \frac{4x - 6}{x^2 - x - 2} \\
> &y - (2x - 3) = \frac{4x - 6}{x^2 - x - 2} = \frac{\frac{4}{x} - \frac{6}{x^2}}{1 - \frac{1}{x} - \frac{2}{x^2}} \to 0 \text{ as } x \to \pm\infty
> \end{aligned}
> $$
> The slant asymptote is $y = 2x - 3$.

## §3.7 Optimization Problems

### 3.7 Exam Points

- **Steps (p. 265):** understand the problem; draw a diagram; introduce notation, with $Q$ the quantity to be maximized or minimized; express $Q$ in terms of the other symbols; use the given information to write $Q$ as a function of one variable, and state its domain; find the absolute maximum or minimum of that function. See [[Optimization Problems]].
- **Justify the absolute extreme value ★★★★:** on a closed interval use the Closed Interval Method (Examples 1, 4, 5). Otherwise use the [[First Derivative Test for Absolute Extreme Values]] (p. 267): if $c$ is a critical number of a continuous function $f$ defined on an interval, and $f'(x) > 0$ for all $x < c$ and $f'(x) < 0$ for all $x > c$, then $f(c)$ is the absolute maximum value of $f$; with the two signs exchanged, the absolute minimum value.
- **[Calc 10] ★★★★ the models of the examples:** fencing a field, $A = x(1200 - 2x)$ (Example 1); a can that holds 1 L, $A = 2\pi r^2 + \frac{2000}{r}$, which gives $h = 2r$ (Example 2); the point of $y^2 = 2x$ closest to $(1, 4)$, by minimizing $d^2$ (Example 3); rowing and running, $T(x) = \frac{\sqrt{x^2 + 9}}{6} + \frac{8 - x}{8}$ on $[0, 8]$ (Example 4); the largest rectangle in a semicircle, area $r^2$ (Example 5); revenue $R(x) = xp(x)$ with a linear demand function (Example 6).
- **Assigned types:** a distance between curves or to a point (5, 26); fencing and its cost (11, 15); boxes and containers (21, 23); inscribed figures (31, 37, 47); a tangent segment (63); revenue (67); a "Show that" (71); a folded paper and an angle of sight (79, 81).
- **[Proof 10] ★★** of all rectangles with a given area the square has the smallest perimeter, and of all rectangles with a given perimeter the square has the greatest area (17); of all isosceles triangles with a given perimeter the equilateral one has the greatest area (71, assigned).

### 3.7 True or False

> [!question]
> Respond with true (T) or false (F).
> - (a) Suppose that $c$ is a critical number of a continuous function $f$ defined on an interval. If $f'(x) < 0$ for all $x < c$ and $f'(x) > 0$ for all $x > c$, then $f(c)$ is the absolute minimum value of $f$.
> - (b) The point of a curve that is closest to a given point can be found by minimizing the square of the distance.
> - (c) If a function has exactly one critical number $c$ in $(a, b)$, then its absolute maximum value on $[a, b]$ is $f(c)$.
> - (d) Of all the rectangles with a given perimeter, the one with the greatest area is a square.

> [!solution]- Answers
> - (a) **T.** The First Derivative Test for Absolute Extreme Values (p. 267).
> - (b) **T.** $d \ge 0$, so $d$ and $d^2$ are smallest at the same point (Example 3).
> - (c) **F.** The endpoints must be compared: $f(x) = x^2$ on $[-1, 2]$ has the single critical number $0$, where it has its minimum; its maximum is $f(2) = 4$.
> - (d) **T.** With perimeter $p$ and sides $x$ and $\frac{p}{2} - x$: $A = x\left(\frac{p}{2} - x\right)$, $A'(x) = \frac{p}{2} - 2x = 0$ at $x = \frac{p}{4}$, and $A(0) = A\left(\frac{p}{2}\right) = 0$ (Exercise 17).

### 3.7 Multiple Choice

> [!question]
> **MC 1.** (5 points) A farmer has 1200 m of fencing and wants to fence off a rectangular field that borders a straight river. He needs no fence along the river. Let $x$ be the length of each of the two sides perpendicular to the river and $A$ the area of the field. Which of the following statements are true?
> - A. $A(x) = 1200x - 2x^2$ for $0 \le x \le 600$.
> - B. The only critical number of $A$ is $x = 300$.
> - C. The largest area is $180{,}000$ m².
> - D. The field of largest area is a square.

> [!solution]- Answer to MC 1
> **A, B, C.** (Example 1, pp. 265–266.)
> - A. The side along the river is $1200 - 2x$.
> - B. $A'(x) = 1200 - 4x = 0 \iff x = 300$.
> - C. $A(0) = 0$, $A(300) = 180{,}000$, $A(600) = 0$: the Closed Interval Method.
> - D fails: the field is 300 m deep and 600 m wide.

> [!question]
> **MC 2.** (5 points) The point on the curve $y = \sqrt{x}$ that is closest to the point $(3, 0)$ is
> - A. $\left(\frac{5}{2}, \frac{\sqrt{10}}{2}\right)$
> - B. $(3, \sqrt{3})$
> - C. $(2, \sqrt{2})$
> - D. $\left(\frac{7}{2}, \frac{\sqrt{14}}{2}\right)$

> [!solution]- Answer to MC 2
> **A.** (Exercise 26, assigned: [[CAL1 HW 3.7 Solutions#ST 3.7.26|ST 3.7.26]].) Minimize $S(x) = d^2 = (x - 3)^2 + (\sqrt{x})^2 = (x - 3)^2 + x$ for $x \ge 0$. $S'(x) = 2x - 5$ is negative for $x < \frac{5}{2}$ and positive for $x > \frac{5}{2}$, so the absolute minimum is at $x = \frac{5}{2}$, where $y = \sqrt{\frac{5}{2}} = \frac{\sqrt{10}}{2}$.

### 3.7 Computation and Proof

> [!question]
> **P1.** ★★★★ (10 points) A rectangular storage container without a lid is to have a volume of 10 m³. The length of its base is twice the width. Material for the base costs \$10 per square meter. Material for the sides costs \$6 per square meter. Find the cost of materials for the least expensive such container.

> [!solution]- Solution of P1
> Exercise 21, assigned: [[CAL1 HW 3.7 Solutions#ST 3.7.21|ST 3.7.21]]. Let $w$ be the width of the base, $2w$ its length, and $h$ the height, in meters.
> $$
> \begin{aligned}
> &2w^2h = 10 \implies h = \frac{5}{w^2} \\
> &C = 10(2w^2) + 6\left[2(2wh) + 2(wh)\right] = 20w^2 + 36wh = 20w^2 + \frac{180}{w}, \qquad w > 0 \\
> &C'(w) = 40w - \frac{180}{w^2} = \frac{40\left(w^3 - \frac{9}{2}\right)}{w^2} = 0 \iff w = \sqrt[3]{\tfrac{9}{2}} \\
> &C'(w) < 0 \text{ for } 0 < w < \sqrt[3]{\tfrac{9}{2}} \text{ and } C'(w) > 0 \text{ for } w > \sqrt[3]{\tfrac{9}{2}} \\
> &\implies C \text{ has its absolute minimum at } w = \sqrt[3]{\tfrac{9}{2}} \approx 1.65 \\
> &C = \frac{20w^3 + 180}{w} = \frac{270}{w} = \frac{270}{\sqrt[3]{9/2}} = 90\sqrt[3]{6} \approx 163.54
> \end{aligned}
> $$
> The least expensive container costs about \$163.54. The minimum is absolute by the First Derivative Test for Absolute Extreme Values: $C' < 0$ everywhere to the left of the critical number and $C' > 0$ everywhere to the right.

> [!question]
> **P2.** ★★★★ (10 points) A right circular cylinder is inscribed in a sphere of radius $r$. Find the largest possible volume of such a cylinder.

> [!solution]- Solution of P2
> Exercise 37, assigned: [[CAL1 HW 3.7 Solutions#ST 3.7.37|ST 3.7.37]]. Let the cylinder have radius $x$ and height $2y$; its axis passes through the center of the sphere, so $x^2 + y^2 = r^2$.
> $$
> \begin{aligned}
> &V = \pi x^2(2y) = 2\pi(r^2 - y^2)y = 2\pi(r^2y - y^3), \qquad 0 \le y \le r \\
> &V'(y) = 2\pi(r^2 - 3y^2) = 0 \iff y = \frac{r}{\sqrt{3}} \\
> &V(0) = 0,\qquad V(r) = 0,\qquad V\left(\frac{r}{\sqrt{3}}\right) = 2\pi\left(r^2 - \frac{r^2}{3}\right)\frac{r}{\sqrt{3}} = \frac{4\pi r^3}{3\sqrt{3}}
> \end{aligned}
> $$
> By the Closed Interval Method the largest possible volume is $\dfrac{4\pi r^3}{3\sqrt{3}}$.

> [!question]
> **P3.** ★★★ (10 points) What is the shortest possible length of the line segment that is cut off by the first quadrant and is tangent to the curve $y = 3/x$ at some point?

> [!solution]- Solution of P3
> Exercise 63, assigned: [[CAL1 HW 3.7 Solutions#ST 3.7.63|ST 3.7.63]]. Let the point of tangency be $\left(a, \frac{3}{a}\right)$ with $a > 0$.
> $$
> \begin{aligned}
> &y' = -\frac{3}{x^2} \implies \text{tangent line: } y - \frac{3}{a} = -\frac{3}{a^2}(x - a) \\
> &y = 0 \implies x = 2a; \qquad x = 0 \implies y = \frac{6}{a} \\
> &L^2 = S(a) = (2a)^2 + \left(\frac{6}{a}\right)^2 = 4a^2 + \frac{36}{a^2}, \qquad a > 0 \\
> &S'(a) = 8a - \frac{72}{a^3} = \frac{8(a^4 - 9)}{a^3} = 0 \iff a = \sqrt{3} \\
> &S'(a) < 0 \text{ for } 0 < a < \sqrt{3},\quad S'(a) > 0 \text{ for } a > \sqrt{3} \implies \text{absolute minimum at } a = \sqrt{3} \\
> &S(\sqrt{3}) = 12 + 12 = 24 \implies L = \sqrt{24} = 2\sqrt{6}
> \end{aligned}
> $$

> [!question]
> **P4.** ★★★ (10 points) Show that of all the isosceles triangles with a given perimeter, the one with the greatest area is equilateral.

> [!proof]- Proof of P4
> Exercise 71, assigned: [[CAL1 HW 3.7 Solutions#ST 3.7.71|ST 3.7.71]]. Let the perimeter be $p$, the base $2b$, and each of the equal sides $s$.
> $$
> \begin{aligned}
> &2s + 2b = p \implies s = \frac{p}{2} - b; \qquad \text{height } h = \sqrt{s^2 - b^2} = \sqrt{\frac{p^2}{4} - pb} \\
> &A = \frac{1}{2}(2b)h = b\sqrt{\frac{p^2}{4} - pb}, \qquad 0 < b < \frac{p}{4} \\
> &A > 0, \text{ so we maximize } S(b) = A^2 = \frac{p^2}{4}b^2 - pb^3 \\
> &S'(b) = \frac{p^2}{2}b - 3pb^2 = pb\left(\frac{p}{2} - 3b\right) = 0 \iff b = \frac{p}{6} && (b > 0) \\
> &S'(b) > 0 \text{ for } 0 < b < \frac{p}{6},\quad S'(b) < 0 \text{ for } \frac{p}{6} < b < \frac{p}{4} \implies \text{absolute maximum at } b = \frac{p}{6} \\
> &\text{Then the base is } 2b = \frac{p}{3} \text{ and } s = \frac{p}{2} - \frac{p}{6} = \frac{p}{3}: \text{ the triangle is equilateral.} \qquad \blacksquare
> \end{aligned}
> $$

> [!question]
> **P5.** ★★★ (10 points) A baseball team plays in a stadium that seats 55,000 spectators. With ticket prices at \$10, the average attendance had been 27,000. When ticket prices were lowered to \$8, the average attendance rose to 33,000.
> - (a) Find the demand function, assuming that it is linear.
> - (b) How should ticket prices be set to maximize revenue?

> [!solution]- Solution of P5
> Exercise 67, assigned: [[CAL1 HW 3.7 Solutions#ST 3.7.67|ST 3.7.67]]. Let $x$ be the attendance and $p(x)$ the ticket price.
> $$
> \begin{aligned}
> &\text{(a) slope} = \frac{8 - 10}{33000 - 27000} = -\frac{1}{3000} \implies p(x) = 10 - \frac{1}{3000}(x - 27000) = 19 - \frac{x}{3000} \\
> &\text{(b)}\ R(x) = xp(x) = 19x - \frac{x^2}{3000}, \qquad 0 \le x \le 55000 \\
> &\qquad R'(x) = 19 - \frac{x}{1500} = 0 \iff x = 28500 \\
> &\qquad R'(x) > 0 \text{ for } x < 28500,\quad R'(x) < 0 \text{ for } x > 28500 \implies \text{absolute maximum at } x = 28500 \\
> &\qquad p(28500) = 19 - 9.5 = 9.5
> \end{aligned}
> $$
> The price should be set at \$9.50.

> [!question]
> **P6.** ★★ (10 points) What is the maximum vertical distance between the line $y = x + 2$ and the parabola $y = x^2$ for $-1 \le x \le 2$?

> [!solution]- Solution of P6
> Exercise 5, assigned: [[CAL1 HW 3.7 Solutions#ST 3.7.5|ST 3.7.5]].
> $$
> \begin{aligned}
> &d(x) = (x + 2) - x^2 = -(x - 2)(x + 1) \ge 0 \text{ on } [-1, 2], \text{ and } d \text{ is continuous on } [-1, 2] \\
> &d'(x) = 1 - 2x = 0 \iff x = \frac{1}{2} \\
> &d\left(\frac{1}{2}\right) = \frac{9}{4},\qquad d(-1) = 0,\qquad d(2) = 0
> \end{aligned}
> $$
> By the Closed Interval Method the maximum vertical distance is $\dfrac{9}{4}$.
