---
course: [CAL1]
semester: "115-1"
chapter: ["3.1"]
tags: [calculus, concept, exam-prep]
aliases: [3.1 考試筆記, 最大值與最小值考試筆記]
source:
  - "Stewart, Calculus 9e, §3.1 Maximum and Minimum Values, pp. 210–220 (scan 3-1_Scan_2.pdf)"
  - "Computations checked with sympy and numpy"
created: 2026-11-07
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Exam Focus

> [!abstract] About 12 points (10–15), ★★★
> **Files:** the map [[CAL1 3.1 Exam Map.excalidraw]]. There is no unit summary and no homework note for §3.1 yet. The proofs follow the style of [[CAL1 Midterm 1]].
>
> **How §3.1 gets asked**
> - **[Proof 10] ★★★★** [[#Proof of Fermat's Theorem]]: the interval on which $f(c+h) \le f(c)$ holds, the step that uses "$f'(c)$ exists" (so both one-sided limits exist and equal $f'(c)$), the two signs of $h$, and the inequality that reverses for $h < 0$. The local-minimum case through $-f$ ([[#Fermat's Theorem for a Local Minimum]]) is the natural variant.
> - **[T/F] [MC] ★★★** an endpoint is never a local extremum; the two hypotheses of [[#The Extreme Value Theorem]] and a counterexample for each; the converse of Fermat's Theorem fails ($x^3$); an extremum can occur where $f'$ does not exist ($\lvert x \rvert$); a critical number must lie in the domain.
> - **[Calc 10] ★★★** [[#Absolute Extreme Values on a Closed Interval]], including critical numbers where $f'$ does not exist ([[#Finding Critical Numbers]]).
> - **[Proof 10] ★★** shorter proofs: [[#No Local Extremum]] ($f' > 0$), [[#Critical Numbers of a Cubic]], [[#Why the Closed Interval Method Works]].
>
> **Midterm 1 lessons that apply here**
> - Write every condition: $h \ne 0$ before dividing by $h$, and the interval $0 < \lvert h \rvert < \delta$ on which $f(c+h) \le f(c)$ holds. Leaving out that interval is the same mistake as the missing $\delta_3$ in Q7.
> - Name each step in words in a right-hand column: "limits preserve $\le$", "$f'(c)$ exists, so it equals each one-sided limit".
> - The Chapter 3 Review (not in this scan) is the likeliest source of T/F items; [[#True or False]] covers the same points.
>
> **Drill first:** write the Fermat proof by hand twice; then one Closed Interval Method problem with a fractional power (Exercise 57); then the T/F list.

## Definitions and Theorems

The section opens with optimization problems (the can that minimizes cost, the maximum acceleration of a spacecraft, the radius of a contracted windpipe, the branching angle of blood vessels): each reduces to finding the maximum or minimum value of a function (p. 210).

### Absolute Extreme Values

> [!definition] Definition: absolute maximum and minimum (p. 210)
> Let $c$ be a number in the domain $D$ of a function $f$. Then $f(c)$ is the
> - **absolute maximum** value of $f$ on $D$ if $f(c) \ge f(x)$ for all $x$ in $D$.
> - **absolute minimum** value of $f$ on $D$ if $f(c) \le f(x)$ for all $x$ in $D$.
>
> An absolute maximum or minimum is sometimes called a **global** maximum or minimum. The maximum and minimum values of $f$ are called **extreme values** of $f$.

> [!note] Figures 1–3 (p. 210)
> - Figure 1: the highest point is $(3, 5)$, so $f(3) = 5$ is the absolute maximum; the absolute minimum is $f(6) = 2$.
> - Figure 2: absolute minimum $f(a)$ and absolute maximum $f(d)$; local minima $f(c)$, $f(e)$; local maxima $f(b)$, $f(d)$. $(d, f(d))$ is the highest point and $(a, f(a))$ the lowest.
> - Figure 3: $f(4) = 5$ is a local minimum (the smallest value on the interval $I$) but not the absolute minimum; $f(12) = 3$ is both a local minimum and the absolute minimum; $f(8) = 7$ is a local maximum but not the absolute maximum, because $f$ takes larger values near $1$.

> [!note] Examples 2–4 (p. 211)
> - $f(x) = \cos x$ takes its (local and absolute) maximum value $1$ infinitely many times, since $\cos 2n\pi = 1$ for any integer $n$ and $-1 \le \cos x \le 1$ for all $x$; likewise $\cos(2n+1)\pi = -1$ is its minimum value (Figure 5).
> - $f(x) = x^2$: $f(x) \ge f(0)$ because $x^2 \ge 0$ for all $x$, so $f(0) = 0$ is the absolute (and local) minimum value; there is no highest point on the parabola, so there is no maximum value (Figure 6).
> - $f(x) = x^3$ has neither an absolute maximum nor an absolute minimum value, and no local extreme values either (Figure 7).

### Local Extreme Values

> [!definition] Definition: local maximum and minimum (p. 210)
> The number $f(c)$ is a
> - **local maximum** value of $f$ if $f(c) \ge f(x)$ when $x$ is near $c$.
> - **local minimum** value of $f$ if $f(c) \le f(x)$ when $x$ is near $c$.
>
> Something is true **near** $c$ if it is true on some open interval containing $c$. Thus a local maximum or minimum can't occur at an endpoint.

> [!note] In symbols
> $f(c)$ is a local maximum value $\iff \exists\, \delta > 0$ such that $f(c) \ge f(x)$ for all $x \in (c - \delta, c + \delta)$, where $(c - \delta, c + \delta)$ lies in the domain. From an open interval $(p, q)$ containing $c$, take $\delta = \min\{c - p,\ q - c\}$.

> [!warning] Endpoints
> An endpoint of the domain is never a local extremum, but it can be an absolute one: in Example 1 (p. 211) the absolute maximum $f(-1) = 37$ is not a local maximum, because it occurs at an endpoint.

### The Extreme Value Theorem

> [!theorem] The Extreme Value Theorem (p. 211)
> If $f$ is continuous on a closed interval $[a, b]$, then $f$ attains an absolute maximum value $f(c)$ and an absolute minimum value $f(d)$ at some numbers $c$ and $d$ in $[a, b]$.

> [!note] Note (pp. 211–212)
> - An extreme value can be taken on more than once (Figure 8; $\cos x$ in Example 2).
> - The book omits the proof ("it is difficult to prove"): expect questions on the hypotheses and counterexamples, not on a proof.
> - The theorem says that the extreme values exist, but not how to find them; [[#The Closed Interval Method]] finds them.

> [!warning] Both hypotheses are needed (Figures 9 and 10, p. 212)
> - **Closed interval, not continuous:** the $f$ of Figure 9 is defined on $[0, 2]$ and has range $[0, 3)$. It takes values arbitrarily close to $3$ but never $3$, so it has the minimum value $f(2) = 0$ and no maximum value. A formula of this kind: $f(x) = x$ for $0 \le x < 1$, $f(1) = 0$, on $[0, 1]$.
> - **Continuous, open interval:** the $g$ of Figure 10 is continuous on $(0, 2)$ with range $(1, \infty)$: it has neither a maximum nor a minimum. A formula of this kind: $g(x) = x$ on $(0, 1)$.
> - **The converse is false:** a discontinuous function can still have both extreme values (Exercise 13 (b)): on $[-1, 2]$, $f(x) = x$ for $x \ne 0$ and $f(0) = 1$ is discontinuous at $0$, but has the maximum $f(2) = 2$ and the minimum $f(-1) = -1$.
> - **The hypotheses give a guarantee; they are not necessary:** $\sin x$ is continuous on the open interval $(0, \pi)$ and still has the maximum $\sin\frac{\pi}{2} = 1$.

### Fermat's Theorem

> [!theorem] Fermat's Theorem (p. 212)
> If $f$ has a local maximum or minimum at $c$, and if $f'(c)$ exists, then $f'(c) = 0$.

> [!note] Figure 11 (p. 212)
> The Extreme Value Theorem does not say how to find extreme values, but in Figure 8 the absolute extreme values strictly between $a$ and $b$ occur at local extreme values. Figure 11 shows a local maximum at $c$ and a local minimum at $d$ where the tangent lines are horizontal, so $f'(c) = 0$ and $f'(d) = 0$; Fermat's Theorem says that this is always true for differentiable functions.

Proof: [[#Proof of Fermat's Theorem]]. (Margin, p. 213: the theorem is named after Pierre Fermat (1601–1665), a French lawyer and amateur mathematician, one of the two inventors of analytic geometry and a forerunner of Newton.)

> [!warning] WARNING (p. 213)
> - $f(x) = x^3$ (Example 5): $f'(x) = 3x^2$, so $f'(0) = 0$, but $f$ has no maximum or minimum at $0$, since $x^3 > 0$ for $x > 0$ and $x^3 < 0$ for $x < 0$. Even when $f'(c) = 0$ there need not be a maximum or minimum at $c$: **the converse of Fermat's Theorem is false in general.** $f'(0) = 0$ only means that $y = x^3$ has a horizontal tangent at $(0, 0)$; the curve crosses its horizontal tangent there.
> - $f(x) = \lvert x \rvert$ (Example 6): the (local and absolute) minimum value is $f(0) = 0$, but $f'(0)$ does not exist (§2.2), so it can't be found by setting $f'(x) = 0$. **There may be an extreme value where $f'(c)$ does not exist.**
> - So start looking for extreme values at the numbers $c$ where $f'(c) = 0$ or where $f'(c)$ does not exist.

### Critical Number

> [!definition] Definition: critical number (p. 214)
> A **critical number** of a function $f$ is a number $c$ in the domain of $f$ such that either $f'(c) = 0$ or $f'(c)$ does not exist.

> [!warning] It must be in the domain
> For $f(x) = \tfrac{1}{x}$, $f'(0)$ does not exist, but $0$ is not a critical number: it is not in the domain. Likewise $\tfrac{1}{2}$ is not a critical number of $p(x) = \tfrac{x^2+2}{2x-1}$ (Exercise 37).

### Local Extremum Implies Critical Number

> [!theorem] Fermat's Theorem in terms of critical numbers (p. 214)
> If $f$ has a local maximum or minimum at $c$, then $c$ is a critical number of $f$.

Proof: [[#Proof That a Local Extremum Occurs at a Critical Number]]. The converse is false: $0$ is a critical number of $x^3$ without an extremum.

### The Closed Interval Method

> [!theorem] The Closed Interval Method (p. 214)
> To find the *absolute* maximum and minimum values of a continuous function $f$ on a closed interval $[a, b]$:
> 1. Find the values of $f$ at the critical numbers of $f$ in $(a, b)$.
> 2. Find the values of $f$ at the endpoints of the interval.
> 3. The largest of the values from Steps 1 and 2 is the absolute maximum value; the smallest of these values is the absolute minimum value.

Why it works: [[#Why the Closed Interval Method Works]]. Template: [[#Absolute Extreme Values on a Closed Interval]].

### Results Used from Other Sections

- **Limits preserve $\le$** (§1.6, the theorem the book cites on p. 213; used in [[#Proof of Fermat's Theorem]]): if $f(x) \le g(x)$ when $x$ is near $a$ (except possibly at $a$) **and the limits of $f$ and $g$ both exist** as $x \to a$, then $\lim_{x \to a} f(x) \le \lim_{x \to a} g(x)$. It holds for one-sided limits too. A strict $<$ only gives $\le$: $0 < x^2$ for $x \ne 0$, but both limits at $0$ equal $0$.
- **A limit exists exactly when both one-sided limits exist and are equal** (§1.6): so if $f'(c)$ exists, $f'(c)$ equals both one-sided limits of the difference quotient.
- **$\lvert x \rvert$ is not differentiable at $0$** (§2.2), as in [[CAL1 Midterm 1]] Q1 (a): the one-sided limits of $\tfrac{\lvert h \rvert}{h}$ are $-1$ and $1$.
- **Rolle's Theorem** (start of §3.2, p. 220) is proved from the Extreme Value Theorem and Fermat's Theorem: [[CAL1 3.2 Exam Notes]].
- **The Increasing/Decreasing Test and the First Derivative Test** (§3.3) are used in [[#Critical Numbers of a Cubic]] (b): [[CAL1 3.3 Exam Notes]].

## Proofs

### Proof of Fermat's Theorem

> [!theorem] Fermat's Theorem (p. 212)
> If $f$ has a local maximum or minimum at $c$, and if $f'(c)$ exists, then $f'(c) = 0$.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: Suppose } f \text{ has a local maximum at } c. \\
> &\because f(c) \text{ is a local maximum value,} \\
> &\therefore \exists\, \delta > 0 \text{ s.t. } f(c) \ge f(x) \text{ for all } x \in (c - \delta, c + \delta) && \text{(definition of local maximum)} \\
> &\implies f(c+h) - f(c) \le 0 \text{ for } 0 < \lvert h \rvert < \delta && (x = c + h) \quad (\ast) \\[6pt]
> &\because f'(c) = \lim_{h \to 0} \frac{f(c+h) - f(c)}{h} \text{ exists,} \\
> &\therefore \lim_{h \to 0^{+}} \frac{f(c+h) - f(c)}{h} \text{ and } \lim_{h \to 0^{-}} \frac{f(c+h) - f(c)}{h} \text{ exist and both equal } f'(c) && \text{(a limit equals each one-sided limit)} \\[6pt]
> &\text{If } 0 < h < \delta, \text{ then} \\
> &\qquad \frac{f(c+h) - f(c)}{h} \le 0 && \text{(divide } (\ast) \text{ by } h > 0\text{)} \\
> &\qquad \implies f'(c) = \lim_{h \to 0^{+}} \frac{f(c+h) - f(c)}{h} \le \lim_{h \to 0^{+}} 0 = 0 && \text{(limits preserve } \le\text{; both limits exist)} \\[6pt]
> &\text{If } -\delta < h < 0, \text{ then} \\
> &\qquad \frac{f(c+h) - f(c)}{h} \ge 0 && \text{(divide } (\ast) \text{ by } h < 0\text{: the inequality reverses)} \\
> &\qquad \implies f'(c) = \lim_{h \to 0^{-}} \frac{f(c+h) - f(c)}{h} \ge \lim_{h \to 0^{-}} 0 = 0 && \text{(limits preserve } \ge\text{; both limits exist)} \\[6pt]
> &\text{Then } 0 \le f'(c) \le 0, \text{ so } f'(c) = 0. \\[6pt]
> &\text{If } f \text{ has a local minimum at } c, \text{ let } g = -f. \text{ Then } g \text{ has a local maximum at } c \\
> &\text{and } g'(c) = -f'(c) \text{ exists, so } g'(c) = 0 \text{ by the case above, and } f'(c) = -g'(c) = 0. \\[6pt]
> &\text{Hence } f'(c) = 0. \qquad \blacksquare
> \end{aligned}
> $$

\# **Points.** Each of these is a line the grader looks for:
- the interval: $\exists\, \delta > 0$ with $f(c) \ge f(x)$ on $(c - \delta, c + \delta)$, so $(\ast)$ holds only for $0 < \lvert h \rvert < \delta$, not for every $h$;
- $h \ne 0$ whenever you divide by $h$, with the cases $h > 0$ and $h < 0$ written separately;
- the inequality reverses when you divide by $h < 0$;
- limits keep $\le$, never $<$, and only for limits that exist: the one-sided limits are $\le 0$ and $\ge 0$;
- the hypothesis "$f'(c)$ exists", used by name **before** taking the one-sided limits: it makes both one-sided limits exist (so "limits preserve $\le$" may be applied) and equal $f'(c)$. For $\lvert x \rvert$ at $0$ the two one-sided limits are $-1$ and $1$, and the proof breaks there;
- the local-minimum case: say how it follows (through $-f$, or "similarly", with every inequality reversed).

\# Intuition: just right of a peak every secant slope is $\le 0$; just left of it every secant slope is $\ge 0$. A tangent slope that exists is the limit of both, so it is $0$.

### Fermat's Theorem for a Local Minimum

> [!theorem] Exercise 73 (p. 218)
> (a) If $f$ has a local minimum value at $c$, show that the function $g(x) = -f(x)$ has a local maximum value at $c$.
> (b) Use part (a) to prove Fermat's Theorem for the case in which $f$ has a local minimum at $c$.

> [!proof]- Proof
> **(a)**
> $$
> \begin{aligned}
> &\because f(c) \text{ is a local minimum value,} \\
> &\therefore \exists\, \delta > 0 \text{ s.t. } f(c) \le f(x) \text{ for all } x \in (c - \delta, c + \delta) && \text{(definition of local minimum)} \\
> &\implies -f(c) \ge -f(x) \text{ for all } x \in (c - \delta, c + \delta) && \text{(multiply by } -1\text{)} \\
> &\implies g(c) \ge g(x) \text{ for all } x \in (c - \delta, c + \delta) \\
> &\text{Hence } g \text{ has a local maximum value at } c. && \text{(definition of local maximum)}
> \end{aligned}
> $$
> **(b)** Suppose $f$ has a local minimum at $c$ and $f'(c)$ exists.
> $$
> \begin{aligned}
> &g = -f \text{ has a local maximum at } c && \text{(part (a))} \\
> &g'(c) = -f'(c) \text{ exists} && \text{(Constant Multiple Rule)} \\
> &\implies g'(c) = 0 && \text{(Fermat's Theorem, local maximum case)} \\
> &\implies f'(c) = -g'(c) = 0. \qquad \blacksquare
> \end{aligned}
> $$

\# **Points.** Multiplying by $-1$ reverses the inequality; the same $\delta$ (the same open interval) works for $g$; state that $g'(c)$ exists before using Fermat's Theorem, because that is its hypothesis.

### Proof That a Local Extremum Occurs at a Critical Number

> [!theorem] Fermat's Theorem in terms of critical numbers (p. 214)
> If $f$ has a local maximum or minimum at $c$, then $c$ is a critical number of $f$.

> [!proof]- Proof
> $$
> \begin{aligned}
> &f(c) \text{ is a local extreme value, so } f(c) \text{ is defined: } c \text{ is in the domain of } f. \\
> &\text{Case 1: } f'(c) \text{ does not exist} \implies c \text{ is a critical number.} && \text{(definition of critical number)} \\
> &\text{Case 2: } f'(c) \text{ exists} \implies f'(c) = 0 && \text{(Fermat's Theorem)} \\
> &\hphantom{\text{Case 2: } f'(c) \text{ exists}} \implies c \text{ is a critical number.} && \text{(definition of critical number)} \\
> &\text{Hence } c \text{ is a critical number of } f. \qquad \blacksquare
> \end{aligned}
> $$

\# **Points.** Say that $c$ is in the domain; cover both cases. The contrapositive is the tool of [[#No Local Extremum]]: no critical numbers $\implies$ no local extrema. The converse is false ($x^3$ at $0$).

### Why the Closed Interval Method Works

> [!theorem] The Closed Interval Method works (p. 214)
> If $f$ is continuous on $[a, b]$, then its absolute maximum and minimum values are among the values of $f$ at the critical numbers in $(a, b)$ and at $a$ and $b$.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\because f \text{ is continuous on the closed interval } [a, b], \\
> &\therefore \exists\, c \in [a, b] \text{ s.t. } f(c) \ge f(x) \text{ for all } x \in [a, b] && \text{(Extreme Value Theorem)} \\[6pt]
> &\text{If } c = a \text{ or } c = b, \text{ then } f(c) \text{ is a value of Step 2.} \\
> &\text{If } a < c < b, \text{ then } (a, b) \text{ is an open interval containing } c \text{ and } f(c) \ge f(x) \text{ on } (a, b) \\
> &\qquad \implies f \text{ has a local maximum at } c && \text{(definition of local maximum)} \\
> &\qquad \implies c \text{ is a critical number of } f \text{ in } (a, b) && \text{(a local extremum is at a critical number)} \\
> &\qquad \implies f(c) \text{ is a value of Step 1.} \\[6pt]
> &\text{So } f(c) \text{ is among the values of Steps 1 and 2, and } f(c) \ge \text{each of them: it is the largest.} \\
> &\text{The minimum is the same with } \le. \\
> &\text{Hence Step 3 gives the absolute maximum and minimum values.} \qquad \blacksquare
> \end{aligned}
> $$

\# **Points.** Continuity on the *closed* interval is what lets the Extreme Value Theorem start the argument; an interior absolute maximum is local because $(a, b)$ is an open interval around it.

### No Local Extremum

> [!theorem] Exercise 72 (p. 218)
> Prove that the function $f(x) = x^{101} + x^{51} + x + 1$ has neither a local maximum nor a local minimum.

> [!proof]- Proof
> $$
> \begin{aligned}
> &f \text{ is a polynomial, so its domain is } \mathbb{R} \text{ and } f \text{ is differentiable everywhere.} \\
> &f'(x) = 101x^{100} + 51x^{50} + 1 && \text{(Power Rule, Sum Rule)} \\
> &\because x^{100} = (x^{50})^2 \ge 0 \text{ and } x^{50} = (x^{25})^2 \ge 0 \text{ for all } x, \\
> &\therefore f'(x) \ge 1 > 0 \text{ for all } x \\
> &\implies f'(x) \text{ exists and } f'(x) \ne 0 \text{ for every } x \\
> &\implies f \text{ has no critical number.} && \text{(definition of critical number)} \\[6pt]
> &\text{Suppose } f \text{ had a local maximum or minimum at some } c. \\
> &\text{Then } c \text{ would be a critical number of } f, \text{ a contradiction.} && \text{(a local extremum is at a critical number)} \\
> &\text{Hence } f \text{ has neither a local maximum nor a local minimum.} \qquad \blacksquare
> \end{aligned}
> $$

\# **Points.** Both halves of "no critical number": $f'$ exists everywhere and is never $0$. Give the reason the even powers are $\ge 0$, and name the theorem used at the end.

### Critical Numbers of a Cubic

> [!theorem] Exercise 74 (p. 218)
> A cubic function is a polynomial of degree 3; that is, it has the form $f(x) = ax^3 + bx^2 + cx + d$, where $a \ne 0$.
> (a) Show that a cubic function can have two, one, or no critical number(s). Give examples and sketches to illustrate the three possibilities.
> (b) How many local extreme values can a cubic function have?

> [!proof]- Proof
> **(a)**
> $$
> \begin{aligned}
> &f'(x) = 3ax^2 + 2bx + c \text{ exists for every } x && \text{(polynomial)} \\
> &\implies \text{the critical numbers are the real roots of } 3ax^2 + 2bx + c = 0 && (3a \ne 0\text{: a quadratic}) \\
> &\text{discriminant } \Delta = (2b)^2 - 4(3a)c = 4(b^2 - 3ac) \\[4pt]
> &\Delta > 0: \text{two critical numbers, e.g. } f(x) = x^3 - 3x,\ f'(x) = 3(x-1)(x+1)\text{: } x = \pm 1 \\
> &\Delta = 0: \text{one critical number, e.g. } f(x) = x^3,\ f'(x) = 3x^2\text{: } x = 0 \\
> &\Delta < 0: \text{no critical number, e.g. } f(x) = x^3 + x,\ f'(x) = 3x^2 + 1 > 0. \qquad \blacksquare
> \end{aligned}
> $$
> Sketches: $x^3 - 3x$ rises to the local maximum $(-1, 2)$, falls to the local minimum $(1, -2)$, then rises; $x^3$ rises with a horizontal tangent at $(0, 0)$; $x^3 + x$ rises everywhere with no horizontal tangent.
>
> **(b)** Two or none.
> - Two critical numbers $r_1 < r_2$: $f'(x) = 3a(x - r_1)(x - r_2)$ changes sign at each, so $f$ has a local maximum at one and a local minimum at the other (First Derivative Test, §3.3).
> - One critical number $r$: $f'(x) = 3a(x - r)^2$ keeps the sign of $a$ on both sides of $r$, so $f$ is increasing (or decreasing) on $\mathbb{R}$ and has no local extreme value, like $x^3$.
> - No critical number: no local extreme value, because a local extremum is at a critical number.

\# **Points.** "Critical number" means $f' = 0$ or $f'$ undefined; for a polynomial only $f' = 0$ remains, so the count is the number of real roots of a quadratic. Part (b) needs §3.3 for the sign change.

### Minimizing the Pulling Force

> [!theorem] Exercise 68 (p. 218)
> An object with weight $W$ is dragged along a horizontal plane by a force acting along a rope attached to the object. If the rope makes an angle $\theta$ with the plane, then the magnitude of the force is
> $$
> F = \frac{\mu W}{\mu \sin\theta + \cos\theta}
> $$
> where $\mu$ is a positive constant called the *coefficient of friction* and where $0 \le \theta \le \pi/2$. Show that $F$ is minimized when $\tan\theta = \mu$.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{On } [0, \tfrac{\pi}{2}]\text{: } \mu \sin\theta + \cos\theta > 0 && (\mu > 0;\ \sin\theta, \cos\theta \ge 0 \text{, not both } 0) \\
> &\implies F \text{ is continuous on } [0, \tfrac{\pi}{2}] \text{ and differentiable on } (0, \tfrac{\pi}{2}) \\
> &F'(\theta) = \frac{-\mu W(\mu\cos\theta - \sin\theta)}{(\mu\sin\theta + \cos\theta)^2} && \text{(Quotient Rule)} \\
> &F'(\theta) = 0 \iff \sin\theta = \mu\cos\theta \iff \tan\theta = \mu && (\cos\theta > 0 \text{ on } (0, \tfrac{\pi}{2})) \\
> &\text{Let } \theta^{*} = \tan^{-1}\mu \in (0, \tfrac{\pi}{2})\text{: } \sin\theta^{*} = \frac{\mu}{\sqrt{1+\mu^2}},\ \cos\theta^{*} = \frac{1}{\sqrt{1+\mu^2}} \\
> &F(\theta^{*}) = \frac{\mu W}{\sqrt{1+\mu^2}}, \qquad F(0) = \mu W, \qquad F(\tfrac{\pi}{2}) = W \\
> &\because \sqrt{1+\mu^2} > 1 \text{ and } \sqrt{1+\mu^2} > \mu, \\
> &\therefore F(\theta^{*}) < \mu W = F(0) \text{ and } F(\theta^{*}) < W = F(\tfrac{\pi}{2}) \\
> &\text{Hence } F \text{ is minimized when } \tan\theta = \mu. && \text{(Closed Interval Method)} \qquad \blacksquare
> \end{aligned}
> $$

\# **Points.** Continuity on the closed interval, then the values at the endpoints: $F'(\theta^{*}) = 0$ alone does not show a minimum.

## True or False

Each statement is marked *book* (with the page it comes from) or *constructed*. Statements 15, 21 and 24 are worded the way the Chapter 3 Review True-False Quiz words them, as far as I know; that Review is not in this scan, so check the wording when you have it.

### True or False on Extreme Values

**1.** An absolute maximum is also called a global maximum. *(book, p. 210)*

> [!solution]- Answer
> **T.** Definition of absolute maximum and minimum (p. 210).

**2.** If $f(c)$ is a local maximum value of $f$, then $f(c) \ge f(x)$ for all $x$ in some open interval containing $c$. *(book, p. 210)*

> [!solution]- Answer
> **T.** "Near $c$" means on some open interval containing $c$.

**3.** A local maximum or minimum can occur at an endpoint of the domain. *(book, p. 210)*

> [!solution]- Answer
> **F.** No open interval around an endpoint lies in the domain, so an endpoint is never a local extremum under the book's definition.

**4.** An absolute maximum can occur at an endpoint of the domain. *(book, p. 211)*

> [!solution]- Answer
> **T.** Example 1: $f(x) = 3x^4 - 16x^3 + 18x^2$ on $[-1, 4]$ has the absolute maximum $f(-1) = 37$. Also Example 8: $f(4) = 17$.

**5.** If $f$ has an absolute maximum at $c$, then $f$ has a local maximum at $c$. *(book, p. 211)*

> [!solution]- Answer
> **F.** Example 1: the absolute maximum $f(-1) = 37$ occurs at an endpoint, so it is not a local maximum.

**6.** If $f$ has an absolute maximum at $c$ and some open interval containing $c$ lies in the domain of $f$, then $f$ has a local maximum at $c$. *(constructed)*

> [!solution]- Answer
> **T.** $f(c) \ge f(x)$ for all $x$ in the domain, in particular on that open interval.

**7.** If $f$ has a local maximum at $c$, then $f(c)$ is the absolute maximum value of $f$. *(book, p. 210)*

> [!solution]- Answer
> **F.** Figure 3: $f(8) = 7$ is a local maximum, but $f$ takes larger values near $1$.

**8.** A function can take its absolute maximum value at more than one number. *(book, p. 211)*

> [!solution]- Answer
> **T.** Example 2: $\cos x$ takes its maximum value $1$ at every $2n\pi$. Also Figure 8.

**9.** Every function has an absolute maximum or an absolute minimum. *(book, p. 211)*

> [!solution]- Answer
> **F.** Example 4: $f(x) = x^3$ has neither, and no local extreme values either.

**10.** $f(x) = x^2$ has an absolute minimum value but no maximum value. *(book, p. 211)*

> [!solution]- Answer
> **T.** Example 3: $x^2 \ge 0 = f(0)$ for all $x$, and there is no highest point on the parabola.

**11.** If $f$ has a local maximum at $c$, then $f$ is continuous at $c$. *(constructed; Exercise 11 (c))*

> [!solution]- Answer
> **F.** $f(x) = 0$ for $x \ne 0$ and $f(0) = 1$: $f(0) \ge f(x)$ for all $x$, so $f$ has a local maximum at $0$, but $f$ is not continuous at $0$.

**12.** $f(x) = \tfrac{1}{x}$, $1 < x < 3$, has an absolute minimum value. *(constructed; Exercise 18)*

> [!solution]- Answer
> **F.** $f$ is decreasing; its values approach $\tfrac{1}{3}$ as $x \to 3^{-}$, but $3$ is not in the domain, so no value is the smallest.

**13.** $f(x) = x^2$, $-1 \le x < 2$, has the absolute maximum value $4$. *(constructed; Exercise 16)*

> [!solution]- Answer
> **F.** $f(x) < 4$ for every $x$ in the domain, though $f(x) \to 4$ as $x \to 2^{-}$: $4$ is never attained, and there is no absolute maximum.

### True or False on the Extreme Value Theorem

**14.** If $f$ is continuous on $[a, b]$, then $f$ attains an absolute maximum value and an absolute minimum value on $[a, b]$. *(book, p. 211)*

> [!solution]- Answer
> **T.** The Extreme Value Theorem.

**15.** If $f$ is continuous on $(a, b)$, then $f$ attains an absolute maximum value $f(c)$ and an absolute minimum value $f(d)$ at some numbers $c$ and $d$ in $(a, b)$. *(book, p. 212; likely Chapter 3 Review wording)*

> [!solution]- Answer
> **F.** Figure 10; for instance $g(x) = x$ on $(0, 1)$ has neither a maximum nor a minimum. The closed interval is needed for the guarantee.

**16.** If $f$ is defined on the closed interval $[a, b]$, then $f$ attains an absolute maximum value on $[a, b]$. *(book, p. 212)*

> [!solution]- Answer
> **F.** Figure 9; for instance $f(x) = x$ for $0 \le x < 1$, $f(1) = 0$: the values approach $1$ but never reach it. Continuity is needed for the guarantee.

**17.** If $f$ has an absolute maximum and an absolute minimum on $[a, b]$, then $f$ is continuous on $[a, b]$. *(book, p. 212)*

> [!solution]- Answer
> **F.** The converse of the Extreme Value Theorem is false (Exercise 13 (b)): on $[-1, 2]$, $f(x) = x$ for $x \ne 0$ and $f(0) = 1$ has the maximum $f(2) = 2$ and the minimum $f(-1) = -1$ but is discontinuous at $0$.

**18.** The Extreme Value Theorem tells us how to find the extreme values of a continuous function on $[a, b]$. *(book, p. 212)*

> [!solution]- Answer
> **F.** It only says that they exist (at some numbers in $[a, b]$); it does not tell us how to find them. The Closed Interval Method finds them.

**18b.** A function that is continuous on an open interval cannot have an absolute maximum there. *(constructed)*

> [!solution]- Answer
> **F.** $\sin x$ on $(0, \pi)$ has the absolute maximum $\sin\frac{\pi}{2} = 1$. The hypotheses of the Extreme Value Theorem guarantee extreme values; they are not necessary for them.

**19.** If $f$ is continuous on $[a, b]$ and its absolute maximum occurs at $c \in (a, b)$, then $c$ is a critical number of $f$. *(constructed; p. 214)*

> [!solution]- Answer
> **T.** $(a, b)$ is an open interval containing $c$ on which $f(c) \ge f(x)$, so $f$ has a local maximum at $c$, and a local extremum is at a critical number.

**20.** If $f$ is continuous on $[a, b]$ and $f(a) = f(b)$, then $f$ has a critical number in $(a, b)$. *(constructed; the first half of Rolle's proof, §3.2)*

> [!solution]- Answer
> **T.** If $f$ is constant, $f'(x) = 0$ for every $x \in (a, b)$. Otherwise some $f(x_0) \ne f(a)$, say $f(x_0) > f(a)$. By the Extreme Value Theorem the maximum $f(c) \ge f(x_0) > f(a) = f(b)$, so $c \ne a, b$; then $c \in (a, b)$ is a local maximum and hence a critical number. The case $f(x_0) < f(a)$ is the same with the minimum.

### True or False on Fermat's Theorem and Critical Numbers

**21.** If $f'(c) = 0$, then $f$ has a local maximum or minimum at $c$. *(book, p. 213; likely Chapter 3 Review wording)*

> [!solution]- Answer
> **F.** Example 5: $f(x) = x^3$, $f'(0) = 0$, but $x^3 < 0$ for $x < 0$ and $x^3 > 0$ for $x > 0$, so $f(0) = 0$ is neither a maximum nor a minimum. The converse of Fermat's Theorem is false in general.

**22.** If $f$ has a local minimum at $c$, then $f'(c) = 0$. *(book, p. 213)*

> [!solution]- Answer
> **F.** Example 6: $f(x) = \lvert x \rvert$ has a minimum at $0$, but $f'(0)$ does not exist. Fermat's Theorem needs "$f'(c)$ exists".

**23.** If $f$ has a local minimum at $c$ and $f$ is differentiable at $c$, then $f'(c) = 0$. *(book, p. 212)*

> [!solution]- Answer
> **T.** Fermat's Theorem.

**24.** If $f$ has an absolute minimum value at $c$, then $f'(c) = 0$. *(constructed from pp. 211–213; likely Chapter 3 Review wording)*

> [!solution]- Answer
> **F.** $\lvert x \rvert$ has its absolute minimum at $0$, where $f'(0)$ does not exist (Example 6). An endpoint also fails: in Exercise 49 the minimum of $12 + 4x - x^2$ on $[0, 5]$ is $f(5) = 7$, and the derivative $4 - 2x$ is $-6 \ne 0$ there (only a one-sided derivative exists at an endpoint).

**25.** If $f$ has a local maximum at $c$, then $c$ is a critical number of $f$. *(book, p. 214)*

> [!solution]- Answer
> **T.** Fermat's Theorem in terms of critical numbers.

**26.** If $c$ is a critical number of $f$, then $f$ has a local maximum or minimum at $c$. *(book, pp. 213–214)*

> [!solution]- Answer
> **F.** $0$ is a critical number of $x^3$ ($f'(0) = 0$) without an extremum.

**27.** If $f'(c)$ does not exist, then $c$ is a critical number of $f$. *(constructed)*

> [!solution]- Answer
> **F.** $c$ must also be in the domain: for $f(x) = \tfrac{1}{x}$, $f'(0)$ does not exist, but $0$ is not a critical number.

**28.** $0$ is a critical number of $f(x) = \lvert x \rvert$. *(book, pp. 213–214)*

> [!solution]- Answer
> **T.** $0$ is in the domain and $f'(0)$ does not exist.

**29.** $\tfrac{1}{2}$ is a critical number of $p(x) = \dfrac{x^2 + 2}{2x - 1}$. *(constructed; Exercise 37)*

> [!solution]- Answer
> **F.** $\tfrac{1}{2}$ is not in the domain. $p'(x) = \dfrac{2(x-2)(x+1)}{(2x-1)^2}$, so the critical numbers are $-1$ and $2$.

**30.** The critical numbers of $f(x) = x^{3/5}(4 - x)$ are $0$ and $\tfrac{3}{2}$. *(book, p. 214)*

> [!solution]- Answer
> **T.** Example 7 (b): $f'(x) = \dfrac{12 - 8x}{5x^{2/5}}$, which is $0$ at $\tfrac{3}{2}$ and does not exist at $0$, and the domain is $\mathbb{R}$.

**31.** If $f'(c) = 0$, then the graph of $f$ has a horizontal tangent at $(c, f(c))$. *(book, p. 213)*

> [!solution]- Answer
> **T.** $f'(c)$ is the slope of the tangent line. This is all that $f'(0) = 0$ says about $x^3$.

**32.** In the proof of Fermat's Theorem for a local maximum at $c$, $\dfrac{f(c+h) - f(c)}{h} \ge 0$ for $h < 0$ close to $0$. *(book, p. 213)*

> [!solution]- Answer
> **T.** $f(c+h) - f(c) \le 0$, and dividing by $h < 0$ reverses the inequality.

**33.** If $f(x) < g(x)$ for all $x \ne a$ near $a$ and both limits exist, then $\lim_{x \to a} f(x) < \lim_{x \to a} g(x)$. *(constructed; the step "limits preserve $\le$" of Fermat's proof)*

> [!solution]- Answer
> **F.** $0 < x^2$ for $x \ne 0$, but both limits at $0$ are $0$. Limits keep only $\le$; that is why Fermat's proof gets $f'(c) \le 0$, not $f'(c) < 0$.

**34.** If $f$ has a local minimum at $c$, then $g(x) = -f(x)$ has a local maximum at $c$. *(book, p. 218; Exercise 73)*

> [!solution]- Answer
> **T.** $f(c) \le f(x)$ near $c$ gives $-f(c) \ge -f(x)$ near $c$.

**35.** $f(x) = x^{101} + x^{51} + x + 1$ has a local minimum. *(book, p. 218; Exercise 72)*

> [!solution]- Answer
> **F.** $f'(x) = 101x^{100} + 51x^{50} + 1 \ge 1$, so $f$ has no critical number and therefore no local extremum.

**36.** A cubic function always has exactly two critical numbers. *(book, p. 218; Exercise 74)*

> [!solution]- Answer
> **F.** $x^3$ has one, $x^3 + x$ has none.

**37.** A cubic function can have exactly one local extreme value. *(book, p. 218; Exercise 74)*

> [!solution]- Answer
> **F.** A cubic has two local extreme values (two critical numbers) or none.

**38.** A function can have three local minima, two local maxima, and seven critical numbers. *(book, p. 217; Exercise 14 (b))*

> [!solution]- Answer
> **T.** A critical number need not be an extremum: two of the seven can be flat points like $0$ for $x^3$ (see [[#Sketching a Graph with Given Properties]]).

### True or False on the Closed Interval Method

**39.** If $f$ is continuous on $[a, b]$, its absolute maximum value occurs either at a critical number in $(a, b)$ or at an endpoint. *(book, p. 214)*

> [!solution]- Answer
> **T.** See [[#Why the Closed Interval Method Works]].

**40.** The Closed Interval Method applies to $f(x) = \tfrac{1}{x}$ on $[-1, 1]$. *(constructed)*

> [!solution]- Answer
> **F.** $f$ is not continuous on $[-1, 1]$ ($0$ is not even in the domain), and it has no maximum or minimum there.

**41.** In the Closed Interval Method, critical numbers outside $[a, b]$ must also be checked. *(book, p. 214)*

> [!solution]- Answer
> **F.** Only critical numbers in $(a, b)$ are used, together with $a$ and $b$. For $x^2$ on $[1, 2]$, the critical number $0$ is outside; using $f(0) = 0$ would give a wrong minimum, while the true minimum is $f(1) = 1$.

**42.** If $f$ is continuous on $[a, b]$ and has no critical number in $(a, b)$, then its absolute extreme values occur at $a$ and $b$. *(constructed)*

> [!solution]- Answer
> **T.** Step 1 gives no values, so both extreme values come from Step 2.

**43.** The absolute maximum value of $f(x) = x^3 - 3x^2 + 1$ on $[-\tfrac{1}{2}, 4]$ is $17$. *(book, p. 215)*

> [!solution]- Answer
> **T.** Example 8: $f(-\tfrac{1}{2}) = \tfrac{1}{8}$, $f(0) = 1$, $f(2) = -3$, $f(4) = 17$.

**44.** The absolute minimum value of $f(x) = x - 2\sin x$ on $[0, 2\pi]$ is $\tfrac{\pi}{3} - \sqrt{3}$. *(book, p. 215)*

> [!solution]- Answer
> **T.** Example 9: the values are $f(0) = 0$, $f(\tfrac{\pi}{3}) = \tfrac{\pi}{3} - \sqrt{3} \approx -0.68$, $f(\tfrac{5\pi}{3}) = \tfrac{5\pi}{3} + \sqrt{3} \approx 6.97$, $f(2\pi) = 2\pi$.

## Problem Types

### Reading Extreme Values from a Graph

> [!example] Example 1 (p. 211, paraphrased as a question)
> The graph of the function $f(x) = 3x^4 - 16x^3 + 18x^2$, $-1 \le x \le 4$, is shown in Figure 4; it passes through $(-1, 37)$, $(0, 0)$, $(1, 5)$, $(3, -27)$ and ends at $(4, 32)$. State the local and absolute extreme values.

> [!solution]- Solution
> - $f(-1) = 37$: the absolute maximum. It is not a local maximum, because it occurs at an endpoint.
> - $f(1) = 5$: a local maximum.
> - $f(0) = 0$: a local minimum.
> - $f(3) = -27$: both a local and the absolute minimum.
> - $x = 4$: neither a local nor an absolute maximum ($f(4) = 32 < 37$, and it is an endpoint).
>
> \# $f'(x) = 12x(x-1)(x-3)$, so the interior extrema are exactly at the critical numbers $0$, $1$, $3$.

**Where the points are:** say "absolute" or "local" for each value, and why an endpoint is never local; an open dot is not a value of $f$.

**Practice:** Exercises 1, 3–6. Answers read from the graphs in the scan:
- **1.** An absolute minimum $f(c)$ is $\le f(x)$ for all $x$ in the domain; a local minimum only for $x$ near $c$ (on an open interval). An absolute minimum at an endpoint is not local; a local minimum need not be absolute.
- **3.** Absolute maximum at $s$, absolute minimum at $r$; local maximum at $c$; local minima at $b$ and $r$; neither at $a$ and $d$.
- **4.** Absolute maximum at $r$, absolute minimum at $a$; local maxima at $b$ and $r$; local minimum at $d$; neither at $c$ and $s$.
- **5.** Absolute maximum $f(4) = 5$; no absolute minimum (the values near the open dot at $x = 7$ approach $1$); local maxima $f(4) = 5$ and $f(6) = 4$; local minima $f(1) = 3$, $f(2) = 2$, $f(5) = 3$.
- **6.** No absolute maximum (the open dot at $x = 0$); absolute minimum $g(4) = 1$; local maxima $g(3) = 4$ and $g(6) = 3$; local minima $g(2) = 2$ and $g(4) = 1$.

### Sketching a Graph with Given Properties

> [!example] Exercise 10 (p. 216)
> Sketch the graph of a function $f$ that is continuous on $[1, 5]$ and has the given properties: absolute maximum at $2$, absolute minimum at $5$, $4$ is a critical number but there is no local maximum or minimum there.

> [!solution]- Solution
> $$
> f(x) = \begin{cases} 12 - 3(x - 2)^2 & \text{if } 1 \le x \le 2 \\ 4 - (x - 4)^3 & \text{if } 2 < x \le 5 \end{cases}
> $$
> - Continuous: both pieces give $12$ at $x = 2$.
> - On $[1, 2]$ $f$ rises from $f(1) = 9$ to $f(2) = 12$; on $(2, 5]$ it falls from $12$ to $f(5) = 3$. So $f(2) = 12$ is the absolute maximum and $f(5) = 3$ the absolute minimum.
> - $f'(4) = -3(4 - 4)^2 = 0$, so $4$ is a critical number, but $f$ is decreasing on both sides of $4$: no extremum there (the $x^3$ shape).

**Where the points are:** endpoints can carry absolute (never local) extrema; a critical number without an extremum is a flat point like $0$ for $x^3$; a local maximum may be a corner or even a jump.

**Practice:** Exercises 7–14. Graphs that work (polygonal graphs through the listed points are continuous on $[1, 5]$):
- **7.** Through $(1, 3)$, $(2, 1)$, $(3, 4)$, $(4, 2)$, $(5, 6)$: absolute maximum $f(5) = 6$, absolute and local minimum $f(2) = 1$, local maximum $f(3) = 4$, local minimum $f(4) = 2$.
- **8.** Through $(1, 2)$, $(2, 4)$, $(3, 3)$, $(4, 6)$, $(5, 0)$: absolute maximum $f(4) = 6$, absolute minimum $f(5) = 0$, local maximum $f(2) = 4$, local minimum $f(3) = 3$.
- **9.** Through $(1, 2)$, $(2, 4)$, $(3, 0)$, $(4, 6)$, $(5, 3)$: absolute minimum $f(3) = 0$, absolute maximum $f(4) = 6$, local maximum $f(2) = 4$.

Formulas for the trickier ones:
- **11.** (a) $f(x) = -(x-2)^2$; (b) $f(x) = -\lvert x - 2 \rvert$; (c) $f(x) = -(x-2)^2$ for $x \ne 2$, $f(2) = 1$.
- **12.** On $[-1, 2]$: (a) $f(x) = x$ (absolute maximum $f(2) = 2$ at an endpoint, no local maximum); (b) $f(x) = -x^2$ for $-1 \le x \le 1$, $f(x) = x - 1$ for $1 < x < 2$, $f(2) = 0$ (local maximum $f(0) = 0$; values approach $1$ but never reach it).
- **13.** On $[-1, 2]$: (a) $f(x) = x$ for $-1 < x \le 2$, $f(-1) = 0$ (maximum $f(2) = 2$; the values approach $-1$ but never reach it); (b) $f(x) = x$ for $x \ne 0$, $f(0) = 1$ (discontinuous at $0$; maximum $f(2) = 2$, minimum $f(-1) = -1$).
- **14.** (a) $f(x) = -x^4 + 2x^2$: local maxima $f(\pm 1) = 1$, local minimum $f(0) = 0$, and $f(x) \to -\infty$, so no absolute minimum. (b) a polynomial with $f'(x) = x(x^2 - 1)(x^2 - 4)(x^2 - 9)^2$: local minima at $-2, 0, 2$, local maxima at $\pm 1$, and $\pm 3$ are critical numbers where $f'$ does not change sign (First Derivative Test, §3.3): seven critical numbers.

### Extreme Values from a Sketch

> [!example] Example 3 (p. 211) and Exercise 16 (p. 217)
> (a) Find the extreme values of $f(x) = x^2$ (Example 3, paraphrased as a question). (b) Sketch $f(x) = x^2$, $-1 \le x < 2$, and use the sketch to find the absolute and local maximum and minimum values of $f$.

> [!solution]- Solution
> **(a)** $f(x) = x^2 \ge 0 = f(0)$ for all $x$, so $f(0) = 0$ is the absolute (and local) minimum value; there is no highest point on the parabola, so there is no maximum value.
>
> **(b)**
> - $x^2 \ge 0 = f(0)$ on $[-1, 2)$, and $0$ lies in the open interval $(-1, 2)$: $f(0) = 0$ is the absolute minimum and a local minimum.
> - $f(x) < 4$ for all $x \in [-1, 2)$, but $f(x) \to 4$ as $x \to 2^{-}$: no absolute maximum.
> - $f(-1) = 1$ is an endpoint, so not a local maximum; there is no local maximum.

**Where the points are:** check whether each endpoint belongs to the domain; a value approached but not attained is not a maximum; endpoints are never local.

**Practice:** Exercises 15–28 (and Examples 2–4). Answers:

| Ex. | Absolute | Local |
| --- | --- | --- |
| 15 | max $f(-1) = 5$; no min | none |
| 16 | min $f(0) = 0$; no max | min $f(0) = 0$ |
| 17 | max $f(1) = 1$; no min | none |
| 18 | none | none |
| 19 | min $f(0) = 0$; no max | none |
| 20 | max $f(\tfrac{\pi}{2}) = 1$; no min | none |
| 21 | max $f(\tfrac{\pi}{2}) = 1$, min $f(-\tfrac{\pi}{2}) = -1$ | none |
| 22 | max $f(0) = 1$, min $f(\pm \pi) = -1$ | max $f(0) = 1$, min $f(\pm\pi) = -1$ |
| 23 | min $f(-1) = 1$; no max | min $f(-1) = 1$ |
| 24 | min $f(0) = 0$; no max | min $f(0) = 0$ |
| 25 | max $f(0) = 1$; no min | none |
| 26 | none | none |
| 27 | min $f(1) = -1$; no max | min $f(0) = 0$ |
| 28 | min $f(3) = -2$; no max | none |

### Finding Critical Numbers

> [!example] Example 7 (p. 214)
> Find the critical numbers of (a) $f(x) = x^3 - 3x^2 + 1$ and (b) $f(x) = x^{3/5}(4 - x)$.

> [!solution]- Solution
> **(a)**
> $$
> \begin{aligned}
> &f'(x) = 3x^2 - 6x = 3x(x - 2) && (f'(x) \text{ exists for all } x) \\
> &f'(x) = 0 \iff x = 0 \text{ or } x = 2 \\
> &\text{Hence the critical numbers are } 0 \text{ and } 2.
> \end{aligned}
> $$
> **(b)**
> $$
> \begin{aligned}
> &\text{The domain of } f \text{ is } \mathbb{R}. \\
> &f'(x) = x^{3/5}(-1) + (4 - x)\left(\tfrac{3}{5}x^{-2/5}\right) && \text{(Product Rule, } x \ne 0\text{)} \\
> &\hphantom{f'(x)} = -x^{3/5} + \frac{3(4 - x)}{5x^{2/5}} = \frac{-5x + 3(4 - x)}{5x^{2/5}} = \frac{12 - 8x}{5x^{2/5}} \\
> &f'(x) = 0 \iff 12 - 8x = 0 \iff x = \tfrac{3}{2} \\
> &\text{At } 0\text{: } \lim_{h \to 0} \frac{f(h) - f(0)}{h} = \lim_{h \to 0} \frac{h^{3/5}(4 - h)}{h} = \lim_{h \to 0} \frac{4 - h}{h^{2/5}} = \infty && (h \ne 0;\ h^{2/5} > 0) \\
> &\implies f'(0) \text{ does not exist, and } 0 \text{ is in the domain.} \\
> &\text{Hence the critical numbers are } \tfrac{3}{2} \text{ and } 0.
> \end{aligned}
> $$
> \# The same result comes from writing $f(x) = 4x^{3/5} - x^{8/5}$ first. Figure 14 (margin, p. 214): a horizontal tangent at $x = 1.5$, where $f'(x) = 0$, and a vertical tangent at $x = 0$, where $f'(x)$ is undefined.

**Where the points are:** the domain first; both kinds of critical numbers ($f' = 0$ and $f'$ undefined); a number outside the domain is never critical.

**Practice:** Exercises 29–46. Answers:

| Ex. | Critical numbers | Ex. | Critical numbers |
| --- | --- | --- | --- |
| 29 | $-\tfrac{1}{6}$ | 38 | $0$ ($\pm 3$ not in the domain) |
| 30 | $\pm 2$ | 39 | $0$, $\tfrac{4}{9}$ |
| 31 | $-4$, $0$, $2$ | 40 | $0$, $\pm 2$ |
| 32 | none | 41 | $0$, $\tfrac{8}{7}$, $4$ |
| 33 | none | 42 | $-1$ ($0$ not in the domain) |
| 34 | $\tfrac{3}{2}$ ($f'$ undefined) | 43 | $0$, $\tfrac{4}{3}$, $4$ |
| 35 | $0$, $2$ | 44 | $\tfrac{\pi}{4} + 2n\pi$, $\tfrac{3\pi}{4} + 2n\pi$ |
| 36 | $1 \pm \sqrt{5}$ | 45 | $n\pi$ |
| 37 | $-1$, $2$ ($\tfrac{1}{2}$ not in the domain) | 46 | $0$, $\pm 1$ |

### Counting Critical Numbers from the Derivative

> [!example] Exercise 47 (p. 217)
> A formula for the *derivative* of a function $f$ is given: $f'(x) = 1 + \dfrac{210\sin x}{x^2 - 6x + 10}$. How many critical numbers does $f$ have?

> [!solution]- Solution
> $x^2 - 6x + 10 = (x - 3)^2 + 1 > 0$, so $f'(x)$ exists for every $x$, and the critical numbers are the solutions of $f'(x) = 0$:
> $$
> \sin x = -\frac{x^2 - 6x + 10}{210}.
> $$
> The right side is $\ge -1$ only when $x^2 - 6x + 10 \le 210$, that is, $3 - \sqrt{209} \le x \le 3 + \sqrt{209}$ (about $-11.5 \le x \le 17.5$). Graphing both sides on that interval shows **10** intersections, so $f$ has 10 critical numbers.
>
> \# Exercise 48, $f'(x) = \dfrac{100\cos^2 x}{10 + x^2} - 1$: solutions only for $x^2 \le 90$; a graph shows **14**. Both counts were checked by computer (sign changes of $f'$).

**Where the points are:** say why $f'$ exists everywhere, so only $f' = 0$ counts; bound the interval before counting.

### Absolute Extreme Values on a Closed Interval

> [!example] Example 8 (pp. 214–215)
> Find the absolute maximum and minimum values of the function
> $$
> f(x) = x^3 - 3x^2 + 1 \qquad -\tfrac{1}{2} \le x \le 4
> $$

> [!solution]- Solution
> $$
> \begin{aligned}
> &\because f \text{ is a polynomial, it is continuous on } [-\tfrac{1}{2}, 4], \\
> &\therefore \text{we can use the Closed Interval Method.} \\[6pt]
> &f'(x) = 3x^2 - 6x = 3x(x - 2) && (f'(x) \text{ exists for all } x) \\
> &f'(x) = 0 \iff x = 0 \text{ or } x = 2, \text{ both in } (-\tfrac{1}{2}, 4) \\[6pt]
> &\text{At the critical numbers: } f(0) = 1, \quad f(2) = -3 \\
> &\text{At the endpoints: } f(-\tfrac{1}{2}) = \tfrac{1}{8}, \quad f(4) = 17 \\[6pt]
> &\text{Hence the absolute maximum value is } f(4) = 17 \text{ and the absolute minimum value is } f(2) = -3.
> \end{aligned}
> $$
> \# The absolute maximum occurs at an endpoint, the absolute minimum at a critical number (Figure 15).

**Where the points are:** continuity on the closed interval, stated; $f'$ and where it is $0$ or undefined; only critical numbers in $(a, b)$; all the values listed; a conclusion that names each value and where it occurs.

**Practice:** Exercise 2 ((a) the Extreme Value Theorem guarantees the extreme values; (b) the three steps of the Closed Interval Method) and Exercises 49–60. Answers:

| Ex. | Absolute maximum | Absolute minimum |
| --- | --- | --- |
| 49 | $f(2) = 16$ | $f(5) = 7$ |
| 50 | $f(3) = 113$ | $f(0) = 5$ |
| 51 | $f(-1) = 8$ | $f(2) = -19$ |
| 52 | $f(0) = 5$ | $f(-3) = -76$ |
| 53 | $f(-2) = 33$ | $f(2) = -31$ |
| 54 | $f(3) = 125$ | $f(0) = -64$ |
| 55 | $f(0.2) = 5.2$ | $f(1) = 2$ |
| 56 | $f(1) = 1$ | $f(0) = 0$ |
| 57 | $f(4) = 4 - \sqrt[3]{4}$ | $f(\tfrac{\sqrt{3}}{9}) = -\tfrac{2\sqrt{3}}{9}$ |
| 58 | $f(\tfrac{1}{\sqrt{3}}) = \tfrac{\sqrt[4]{27}}{4}$ | $f(0) = 0$ |
| 59 | $f(\tfrac{\pi}{6}) = \tfrac{3\sqrt{3}}{2}$ | $f(\tfrac{\pi}{2}) = 0$ |
| 60 | $f(\pi) = 2$ | $f(\tfrac{\pi}{2}) = 1$ |

\# Exercise 57 has three critical numbers in $(-1, 4)$: $\pm\tfrac{\sqrt{3}}{9}$ (where $f' = 0$) and $0$ (where $f'$ does not exist); $f(-1) = f(0) = 0$ and $f(-\tfrac{\sqrt{3}}{9}) = \tfrac{2\sqrt{3}}{9}$.

### Estimating and Then Finding Exact Values

> [!example] Example 9 (p. 215)
> (a) Use a calculator or computer to estimate the absolute minimum and maximum values of the function $f(x) = x - 2\sin x$, $0 \le x \le 2\pi$.
> (b) Use calculus to find the exact minimum and maximum values.

> [!solution]- Solution
> **(a)** From the graph in the viewing rectangle $[0, 2\pi]$ by $[-1, 8]$ (Figure 16): the absolute maximum is about $6.97$, at $x \approx 5.24$; the absolute minimum is about $-0.68$, at $x \approx 1.05$.
>
> **(b)**
> $$
> \begin{aligned}
> &f(x) = x - 2\sin x \text{ is continuous on } [0, 2\pi]. \\
> &f'(x) = 1 - 2\cos x = 0 \iff \cos x = \tfrac{1}{2} \iff x = \tfrac{\pi}{3} \text{ or } \tfrac{5\pi}{3} && (0 < x < 2\pi) \\[6pt]
> &f(\tfrac{\pi}{3}) = \tfrac{\pi}{3} - 2\sin\tfrac{\pi}{3} = \tfrac{\pi}{3} - \sqrt{3} \approx -0.684853 \\
> &f(\tfrac{5\pi}{3}) = \tfrac{5\pi}{3} - 2\sin\tfrac{5\pi}{3} = \tfrac{5\pi}{3} + \sqrt{3} \approx 6.968039 \\
> &f(0) = 0, \quad f(2\pi) = 2\pi \approx 6.28 \\[6pt]
> &\text{Hence the absolute minimum value is } f(\tfrac{\pi}{3}) = \tfrac{\pi}{3} - \sqrt{3} \\
> &\text{and the absolute maximum value is } f(\tfrac{5\pi}{3}) = \tfrac{5\pi}{3} + \sqrt{3}.
> \end{aligned}
> $$
> \# The estimates of part (a) check the exact values; a graph alone never gives exact values.

**Where the points are:** exact values with $\sqrt{3}$ and $\pi$, not decimals; the endpoint values listed even when they lose.

**Practice:** Exercises 63–66. Exact answers:
- **63.** $f(x) = x^5 - x^3 + 2$ on $[-1, 1]$: maximum $f(-\sqrt{3/5}) = 2 + \tfrac{6\sqrt{15}}{125} \approx 2.19$, minimum $f(\sqrt{3/5}) = 2 - \tfrac{6\sqrt{15}}{125} \approx 1.81$.
- **64.** $f(x) = x^4 - 3x^3 + 3x^2 - x$ on $[0, 2]$: $f'(x) = (x-1)^2(4x-1)$; maximum $f(2) = 2$, minimum $f(\tfrac{1}{4}) = -\tfrac{27}{256} \approx -0.11$.
- **65.** $f(x) = x\sqrt{x - x^2}$ on its domain $[0, 1]$: maximum $f(\tfrac{3}{4}) = \tfrac{3\sqrt{3}}{16} \approx 0.32$, minimum $f(0) = f(1) = 0$.
- **66.** $f(x) = x - 2\cos x$ on $[-2, 0]$: maximum $f(-2) = -2 - 2\cos 2 \approx -1.17$, minimum $f(-\tfrac{\pi}{6}) = -\tfrac{\pi}{6} - \sqrt{3} \approx -2.26$.

### Applied Extreme Values

> [!example] Example 10 (pp. 215–216)
> The Hubble Space Telescope was deployed on April 24, 1990, by the space shuttle *Discovery*. A model for the velocity of the shuttle during this mission, from liftoff at $t = 0$ until the solid rocket boosters were jettisoned at $t = 126$ seconds, is given by
> $$
> v(t) = 0.000397t^3 - 0.02752t^2 + 7.196t - 0.9397
> $$
> (in meters per second). Using this model, estimate the absolute maximum and minimum values of the *acceleration* of the shuttle between liftoff and the jettisoning of the boosters.

> [!solution]- Solution
> $$
> \begin{aligned}
> &a(t) = v'(t) = 0.001191t^2 - 0.05504t + 7.196 && \text{(the quantity to optimize is } a\text{, not } v\text{)} \\
> &a \text{ is continuous on } [0, 126]\text{: Closed Interval Method.} \\
> &a'(t) = 0.0023808t - 0.05504 = 0 \iff t_1 = \frac{0.05504}{0.0023808} \approx 23.12 \\[6pt]
> &a(0) = 7.196, \quad a(t_1) = a(23.12) = 6.56, \quad a(126) \approx 19.16 \\[6pt]
> &\text{Hence the maximum acceleration is about } 19.16 \text{ m/s}^2 \text{ and the minimum about } 6.56 \text{ m/s}^2.
> \end{aligned}
> $$
> \# The numbers are the book's. Computing directly from $a(t)$ gives $a'(t) = 0.002382t - 0.05504$, $t_1 \approx 23.11$ and $a(126) \approx 19.17$: the same conclusion.

**Where the points are:** differentiate first when the question asks about a rate (here acceleration); the interval from the problem; endpoint values; units.

**Practice:** Exercises 67–71 (68 is in [[#Minimizing the Pulling Force]]). Answers, computed:
- **67.** $V'(T) = -0.06426 + 0.0170086T - 0.0002037T^2 = 0$ at $T \approx 3.9665$ (the other root, $\approx 79.5$, is outside $[0, 30]$). $V(0) = 999.87$, $V(3.9665) \approx 999.745$, $V(30) \approx 1003.763$, so $V$ is smallest and the density (mass over volume) largest at about $3.9665\,^{\circ}\mathrm{C}$.
- **69.** $L'(t) = 0.01317t^2 - 0.2546t + 0.8239 = 0$ at $t \approx 4.11$ (and $\approx 15.22$, outside $[0, 12]$). $L(0) = 323.1$, $L(4.11) \approx 324.64$, $L(12) \approx 322.24$: the water was highest about 4.1 months after January 1, early May 2012, at about $324.6$ m.
- **70.** (a) A least-squares cubic fit of the table gives $v(t) \approx 0.000445t^3 - 0.0352t^2 + 7.614t - 6.49$. (b) $a(t) = v'(t) \approx 0.001336t^2 - 0.0704t + 7.614$; $a'(t) = 0$ at $t \approx 26.35$; $a(0) \approx 7.61$, $a(26.35) \approx 6.69$, $a(125) \approx 19.69$: maximum about $19.7$ m/s², minimum about $6.7$ m/s². (A different regression tool may give slightly different coefficients.)
- **71.** (a) $v'(r) = k(2r_0 r - 3r^2) = kr(2r_0 - 3r) = 0$ at $r = \tfrac{2}{3}r_0$, inside $[\tfrac{1}{2}r_0, r_0]$. $v(\tfrac{1}{2}r_0) = \tfrac{1}{8}kr_0^3$, $v(\tfrac{2}{3}r_0) = \tfrac{4}{27}kr_0^3$, $v(r_0) = 0$: the absolute maximum is at $r = \tfrac{2}{3}r_0$, which agrees with the X-rays (the trachea contracts to about two-thirds of its normal radius). (b) $\tfrac{4}{27}kr_0^3$. (c) On $[0, r_0]$ the graph starts at $v(0) = 0$, rises to $\tfrac{4}{27}kr_0^3$ at $r = \tfrac{2}{3}r_0$, and falls to $v(r_0) = 0$.

### Maximum with Parameters

> [!example] Exercise 61 (p. 217)
> If $a$ and $b$ are positive numbers, find the maximum value of $f(x) = x^a(1 - x)^b$, $0 \le x \le 1$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &f \text{ is continuous on } [0, 1]. \\
> &f'(x) = ax^{a-1}(1-x)^b - bx^a(1-x)^{b-1} = x^{a-1}(1-x)^{b-1}\big[a(1-x) - bx\big] && \text{(Product Rule, Chain Rule; } 0 < x < 1\text{)} \\
> &f'(x) = 0 \iff a - (a+b)x = 0 \iff x = \frac{a}{a+b} \in (0, 1) \\
> &f(0) = f(1) = 0, \quad f\!\left(\frac{a}{a+b}\right) = \frac{a^a b^b}{(a+b)^{a+b}} > 0 \\
> &\text{Hence the maximum value is } \frac{a^a b^b}{(a+b)^{a+b}}.
> \end{aligned}
> $$

**Where the points are:** factor $f'$ before solving; check that the critical number lies in $(0, 1)$; compare with the endpoints.

### Critical Numbers of an Absolute Value

> [!example] Exercise 62 (p. 217)
> Use a graph to estimate the critical numbers of $f(x) = \lvert 1 + 5x - x^3 \rvert$ correct to one decimal place.

> [!solution]- Solution
> Let $g(x) = 1 + 5x - x^3$, so $f = \lvert g \rvert$.
> - Where $g(x) \ne 0$, $f'(x) = \pm g'(x)$, so $f'(x) = 0 \iff g'(x) = 5 - 3x^2 = 0 \iff x = \pm\sqrt{5/3} \approx \pm 1.3$.
> - Where $g(x) = 0$ and $g'(x) \ne 0$, the graph of $f$ has a corner, so $f'(x)$ does not exist: the roots of $1 + 5x - x^3 = 0$ are $x \approx -2.1$, $-0.2$, $2.3$.
>
> The critical numbers are about $-2.1$, $-1.3$, $-0.2$, $1.3$, $2.3$.

**Where the points are:** both kinds of critical numbers; the corners of $\lvert g \rvert$ are where $g$ crosses $0$.

### Applied Project The Calculus of Rainbows

Optional (pp. 219–220). The deviation of a ray is minimized with the Closed Interval Method idea: $D'(\alpha) = 0$. Why the minimum matters: near $\alpha \approx 59.4^{\circ}$, $D'(\alpha) \approx 0$, so $\Delta D / \Delta\alpha \approx 0$ and many rays are deviated by about the same amount; this concentration of rays makes the primary bow bright, and the rainbow angle is $180^{\circ} - 138^{\circ} = 42^{\circ}$. The index of refraction differs by color (dispersion), so each color has its own bow.

> [!example] Problems 1–4 (pp. 219–220, condensed)
> 1. With Snell's Law $\sin\alpha = k\sin\beta$ ($k \approx \tfrac{4}{3}$), the deviation of the primary rainbow is $D(\alpha) = (\alpha - \beta) + (\pi - 2\beta) + (\alpha - \beta) = \pi + 2\alpha - 4\beta$. Show that the minimum value of the deviation is $D(\alpha) \approx 138^{\circ}$ and occurs when $\alpha \approx 59.4^{\circ}$.
> 2. For red light $k \approx 1.3318$ and for violet light $k \approx 1.3435$. Show that the rainbow angle is about $42.3^{\circ}$ for the red bow and $40.6^{\circ}$ for the violet bow.
> 3. For the secondary rainbow, show that $D(\alpha) = 2\alpha - 6\beta + 2\pi$ and that $D(\alpha)$ has a minimum value when $\cos\alpha = \sqrt{\dfrac{k^2 - 1}{8}}$. Taking $k = \tfrac{4}{3}$, show that the minimum deviation is about $129^{\circ}$ and so the rainbow angle for the secondary rainbow is about $51^{\circ}$.
> 4. Show that the colors in the secondary rainbow appear in the opposite order from those in the primary rainbow.

> [!solution]- Solution
> **1.** $\beta = \sin^{-1}\!\left(\tfrac{\sin\alpha}{k}\right)$, so $\beta'(\alpha) = \dfrac{\cos\alpha}{k\cos\beta}$ (implicit differentiation of $\sin\alpha = k\sin\beta$), and
> $$
> D'(\alpha) = 2 - 4\beta'(\alpha) = 0 \iff k\cos\beta = 2\cos\alpha \iff k^2 - \sin^2\alpha = 4\cos^2\alpha \iff \cos\alpha = \sqrt{\frac{k^2 - 1}{3}}.
> $$
> For $k = \tfrac{4}{3}$: $\alpha \approx 59.4^{\circ}$, $\beta \approx 40.2^{\circ}$, $D \approx 138.0^{\circ}$; the rainbow angle is $180^{\circ} - 138^{\circ} = 42^{\circ}$. At the ends, $D(0) = 180^{\circ}$ and $D(90^{\circ}) \approx 165.6^{\circ}$, so this critical number gives the minimum.
>
> **2.** $k = 1.3318$: $D_{\min} \approx 137.7^{\circ}$, rainbow angle $\approx 42.3^{\circ}$. $k = 1.3435$: $D_{\min} \approx 139.4^{\circ}$, rainbow angle $\approx 40.6^{\circ}$.
>
> **3.** $D'(\alpha) = 2 - 6\beta'(\alpha) = 0 \iff k\cos\beta = 3\cos\alpha \iff k^2 - \sin^2\alpha = 9\cos^2\alpha \iff \cos\alpha = \sqrt{\dfrac{k^2 - 1}{8}}$. For $k = \tfrac{4}{3}$: $\alpha \approx 71.8^{\circ}$, $\beta \approx 45.5^{\circ}$, and $D \approx 231^{\circ}$ of counterclockwise rotation, that is $360^{\circ} - 231^{\circ} \approx 129^{\circ}$ measured the other way, so the rainbow angle is $180^{\circ} - 129^{\circ} \approx 51^{\circ}$.
>
> **4.** With the formula of Problem 3, red ($k = 1.3318$) gives a rainbow angle $\approx 50.6^{\circ}$ and violet ($k = 1.3435$) $\approx 53.6^{\circ}$: violet is now higher than red, the opposite of the primary bow (red $42.3^{\circ}$ above violet $40.6^{\circ}$).
>
> \# Computed numerically. The value $D \approx 231^{\circ}$ in Problem 3 is the minimum of the formula $2\alpha - 6\beta + 2\pi$; the book's "about $129^{\circ}$" is its supplement to $360^{\circ}$.
