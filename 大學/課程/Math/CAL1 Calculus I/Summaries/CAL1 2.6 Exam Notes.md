---
course: [CAL1]
semester: "115-1"
chapter: ["2.6"]
tags: [calculus, concept, derivatives, exam-prep]
aliases: ["2.6 隱函數微分 考試筆記", "隱函數微分"]
source:
  - "Stewart, Calculus, §2.6 Implicit Differentiation, pp. 164-172, scanned PDF"
  - "CAL1 Midterm 1 (115-1): exam format and grading"
  - "Own solutions; computations checked with sympy"
created: 2026-11-07
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Exam Focus

> [!abstract] Exam Focus
> **Weight:** about 6 of the 100 points of Midterm 2 (range 5–8). Likelihood ★★.
>
> **How this section gets asked**
> - **[Calc 10] or part of one.** Find $y'$ by [[Implicit Differentiation|implicit differentiation]], then use it: a [[Tangent Line|tangent line]] at a given point, the points with a horizontal (or vertical) tangent, or $y''$ simplified with the original equation (Examples 1, 2, 4).
> - **[Proof 10] ★★.** The [[Power Rule]] for rational exponents by implicit differentiation (Exercise 50). Less likely: a tangent line at a general point $(x_0, y_0)$ (Exercises 46–49).
> - **[T/F] and [MC].** $\frac{d}{dx}(y^2) = 2y\,y'$, not $2y$; "horizontal where the numerator is $0$" needs the denominator $\ne 0$; $y''$ needs $y'$ and the original equation substituted back; Note 1 ($-x/y$ holds for every function the equation defines); the standing assumption that $y$ is a differentiable function of $x$.
> - **Lost points in Midterm 1 were missing conditions.** Here they are: "assume $y$ is a differentiable function of $x$", "(denominator $\ne 0$)" before dividing by it, and "the point lies on the curve" before substituting it.
>
> **Drill first:** Example 2 (all three parts), Example 4, the Power Rule proof, then the True or False list.
>
> **Links:** the map [[CAL1 2.6 Exam Map.excalidraw]]; the assigned exercises in [[CAL1 Index#Assigned Exercises]] (no 2.6 Summary or HW 2.6 notes yet); the [[Chain Rule]] it rests on in [[CAL1 2.5 Summary]] and [[CAL1 HW 2.5 Solutions]].

## Definitions and Theorems

### Implicitly Defined Functions

> [!definition] Definition: Explicit and implicit functions (pp. 164–165)
> The functions that we have met so far can be described by expressing one variable explicitly in terms of another variable—for example,
> $$
> y = \sqrt{x^3 + 1} \qquad \text{or} \qquad y = x \sin x
> $$
> or, in general, $y = f(x)$. Some functions, however, are defined implicitly by a relation between $x$ and $y$ such as
> $$
> \text{(1)}\quad x^2 + y^2 = 25 \qquad \text{or} \qquad \text{(2)}\quad x^3 + y^3 = 6xy
> $$
> … When we say that $f$ is a function defined implicitly by Equation 2, we mean that the equation
> $$
> x^3 + [f(x)]^3 = 6x f(x)
> $$
> is true for all values of $x$ in the domain of $f$.

> [!note] One relation can define several functions (p. 165)
> - Solving Equation 1 for $y$ gives $y = \pm\sqrt{25 - x^2}$, so two of the functions determined by Equation 1 are $f(x) = \sqrt{25 - x^2}$ and $g(x) = -\sqrt{25 - x^2}$: the upper and lower semicircles of the circle $x^2 + y^2 = 25$ (Figure 1).
> - Equation 2 is the **folium of Descartes** (Figure 2). It is not easy to solve for $y$ by hand, and it implicitly defines $y$ as several functions of $x$ (three are graphed in Figure 3).

### Implicit Differentiation

> [!definition] Definition: Implicit differentiation (p. 165)
> Fortunately, we don't need to solve an equation for $y$ in terms of $x$ in order to find the derivative of $y$. Instead we can use the method of **implicit differentiation**. This consists of differentiating both sides of the equation with respect to $x$ and then solving the resulting equation for $dy/dx$. In the examples and exercises of this section it is always assumed that the given equation determines $y$ implicitly as a differentiable function of $x$ so that the method of implicit differentiation can be applied.

> [!theorem] The Chain Rule on a y-term (p. 166)
> "Remembering that $y$ is a function of $x$ and using the Chain Rule, we have"
> $$
> \frac{d}{dx}\left(y^2\right) = \frac{d}{dy}\left(y^2\right)\frac{dy}{dx} = 2y\,\frac{dy}{dx}
> $$
> In general (the [[Chain Rule]] of §2.5; the general form is not printed in §2.6): if $y$ is a differentiable function of $x$ and $g$ is differentiable, then
> $$
> \frac{d}{dx}\,g(y) = g'(y)\,\frac{dy}{dx}, \qquad \text{e.g.} \quad \frac{d}{dx}\left(y^3\right) = 3y^2\,y', \quad \frac{d}{dx}\sin y = \cos y \cdot y'.
> $$
> A term containing both $x$ and $y$ needs the [[Product Rule]] (or the [[Quotient Rule]]) as well: $\frac{d}{dx}(6xy) = 6xy' + 6y$ (p. 167). We can use either of the notations $dy/dx$ or $y'$ for the derivative of $y$ with respect to $x$ (margin, p. 167).

> [!note] The procedure, read off Examples 1–3
> 1. Assume $y$ is a differentiable function of $x$.
> 2. Differentiate both sides with respect to $x$: every term with $y$ gets a factor $y'$ (Chain Rule); products and quotients of $x$ and $y$ use the Product and Quotient Rules.
> 3. Collect the terms with $y'$ on one side and factor out $y'$.
> 4. Solve for $y'$, stating that the coefficient of $y'$ is $\ne 0$.
> 5. To evaluate $y'$ at a point, the point must lie on the curve; substitute both coordinates.

> [!theorem] Note 1: the formula holds for every function the equation defines (pp. 166–167)
> The expression $dy/dx = -x/y$ in Solution 1 [of Example 1] gives the derivative in terms of both $x$ and $y$. It is correct no matter which function $y$ is determined by the given equation. For instance, for $y = f(x) = \sqrt{25 - x^2}$ we have
> $$
> \frac{dy}{dx} = -\frac{x}{y} = -\frac{x}{\sqrt{25 - x^2}}
> $$
> whereas for $y = g(x) = -\sqrt{25 - x^2}$ we have
> $$
> \frac{dy}{dx} = -\frac{x}{y} = -\frac{x}{-\sqrt{25 - x^2}} = \frac{x}{\sqrt{25 - x^2}}
> $$

> [!note] Remarks in the text (pp. 166–168)
> - Example 1 illustrates that even when it is possible to solve an equation explicitly for $y$ in terms of $x$, it may be easier to use implicit differentiation (margin, p. 166).
> - **Note 2** (pp. 167–168). There is a formula for the three solutions of a cubic equation that is like the quadratic formula but much more complicated. If we use this formula (or a computer) to solve the equation $x^3 + y^3 = 6xy$ for $y$ in terms of $x$, we get three functions determined by the equations
> $$
> y = f(x) = \sqrt[3]{-\tfrac{1}{2}x^3 + \sqrt{\tfrac{1}{4}x^6 - 8x^3}} + \sqrt[3]{-\tfrac{1}{2}x^3 - \sqrt{\tfrac{1}{4}x^6 - 8x^3}}
> $$
> and
> $$
> y = \tfrac{1}{2}\left[-f(x) \pm \sqrt{-3}\left(\sqrt[3]{-\tfrac{1}{2}x^3 + \sqrt{\tfrac{1}{4}x^6 - 8x^3}} - \sqrt[3]{-\tfrac{1}{2}x^3 - \sqrt{\tfrac{1}{4}x^6 - 8x^3}}\right)\right]
> $$
> (These are the three functions whose graphs are shown in Figure 3.) You can see that the method of implicit differentiation saves an enormous amount of work in cases such as this.
> - Implicit differentiation works just as easily for equations such as $y^5 + 3x^2y^2 + 5x^4 = 12$, for which it is *impossible* to find an expression for $y$ in terms of $x$ (p. 168).
> - **Abel and Galois** (box, p. 168). "The Norwegian mathematician Niels Abel proved in 1824 that no general formula in terms of radicals can be given for the solutions of the equation $p(x) = 0$, where $p$ is a polynomial of degree 5 with integer coefficients. Later the French mathematician Evariste Galois proved that it is impossible to find a general formula in terms of radicals for the solutions of an equation $p(x) = 0$, where $p$ is a polynomial of degree $n \ge 5$."
> - Figures 4 and 5 (p. 167) check Example 2: "a glance at Figure 4 confirms that this is a reasonable value for the slope at $(3, 3)$", and "Looking at Figure 5, we see that our answer is reasonable."
> - Computer-drawn curves (p. 168): Figure 6 ($\sin(x + y) = y^2 \cos x$) checks Example 3; Figures 7–9 show $(x^2 - 1)(x^2 - 4)(x^2 - 9) = y^2(y^2 - 4)(y^2 - 9)$, $\cos(x - \sin y) = \sin(y - \sin x)$ and $\sin(xy) = \sin x + \sin y$ (Exercises 43–44 create such curves).

### Horizontal and Vertical Tangents

> [!theorem] Horizontal tangents (Example 2 (c), p. 167)
> "The tangent line is horizontal if $y' = 0$." When implicit differentiation gives $y' = \dfrac{N(x, y)}{D(x, y)}$, the tangent at a point $(x, y)$ **of the curve** is horizontal where
> $$
> N(x, y) = 0 \quad \text{and} \quad D(x, y) \ne 0.
> $$
> The book: "$y' = 0$ when $2y - x^2 = 0$ (provided that $y^2 - 2x \ne 0$)."

> [!theorem] Vertical tangents (constructed; §2.6 does not state it)
> With $y' = \dfrac{N}{D}$ as above, the tangent at a point of the curve is vertical where
> $$
> D(x, y) = 0 \quad \text{and} \quad N(x, y) \ne 0,
> $$
> because there $\dfrac{dx}{dy} = \dfrac{D}{N} = 0$: regarded as a function of $y$ (as in Exercises 23–24), $x$ has a horizontal tangent. Compare the [[Vertical Tangent Line]] of §2.2. Where $N = D = 0$ (the folium at the origin), neither test says anything. Both tests read $N$ and $D$ as they come out of the differentiation, before any common factor is cancelled (a cancelled factor that is $0$ at the point can hide a point where $N = D = 0$).

### Second Derivatives of Implicit Functions

> [!note] Second derivatives (pp. 168–169)
> "The following example shows how to find the second derivative of a function that is defined implicitly." The steps of Example 4:
> 1. Find $y'$ implicitly (Equation 3: $y' = -x^3/y^3$).
> 2. Differentiate the expression for $y'$ with respect to $x$ (Quotient Rule), "remembering that $y$ is a function of $x$": a $y'$ appears again.
> 3. Substitute Equation 3 for that $y'$.
> 4. Simplify with the original equation: "the values of $x$ and $y$ must satisfy the original equation $x^4 + y^4 = 16$."
>
> Margin (p. 169): $x^4 + y^4 = 16$ is a stretched and flattened version of the circle $x^2 + y^2 = 4$ (a *fat circle*). It starts out very steep on the left but quickly becomes very flat, as $y' = -\dfrac{x^3}{y^3} = -\left(\dfrac{x}{y}\right)^3$ shows (Figure 10).

### Orthogonal Curves

> [!definition] Definition: Orthogonal curves (Exercises 51–54, p. 171)
> **Orthogonal Trajectories** Two curves are *orthogonal* if their tangent lines are perpendicular at each point of intersection. Show that the given families of curves are *orthogonal trajectories* of each other; that is, every curve in one family is orthogonal to every curve in the other family. Sketch both families of curves on the same axes.

> [!tip] How to test it
> At each intersection point, compute both slopes implicitly and show $m_1 m_2 = -1$; where one tangent is horizontal and the other vertical, they are perpendicular too. Before multiplying, rewrite each slope with the family's constant eliminated (for $y = cx^2$: $c = y/x^2$, so $m_1 = 2cx = 2y/x$).

### Curves Named in the Section

> [!note] Named curves and equations
> Folium of Descartes $x^3 + y^3 = 6xy$ (p. 165); fat circle $x^4 + y^4 = 16$ (p. 169); astroid (Ex. 27); cissoid of Diocles (28); hyperbola (29); ellipse (30); cardioid (31); conchoid of Nicomedes (32); lemniscate (33); devil's curve (34); kampyle of Eudoxus (35); Tschirnhausen cubic (36); rotated ellipse (59); van der Waals equation (57); Bessel function of order $0$ (64).

## Proofs

Ordered by how likely the exam is to ask them. Every proof here is asked in the exercises; the text itself proves nothing beyond its worked examples.

### Power Rule for Rational Exponents

> [!theorem] Power Rule for rational exponents (Exercise 50, p. 171)
> The Power Rule can be proved using implicit differentiation for the case where $n$ is a rational number, $n = p/q$, and $y = f(x) = x^n$ is assumed beforehand to be a differentiable function. If $y = x^{p/q}$, then $y^q = x^p$. Use implicit differentiation to show that
> $$
> y' = \frac{p}{q}\,x^{(p/q) - 1}
> $$

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: Let } p, q \text{ be integers, } q > 0, \text{ and } y = x^{p/q}, \text{ assumed to be a differentiable function of } x. \\
> &\quad y^q = \left(x^{p/q}\right)^q = x^p \\
> &\implies \frac{d}{dx}\left(y^q\right) = \frac{d}{dx}\left(x^p\right) && \text{(differentiate both sides w.r.t. } x\text{)} \\
> &\implies q\,y^{q-1}\,y' = p\,x^{p-1} && \text{(Chain Rule; Power Rule for integers)} \\
> &\implies y' = \frac{p\,x^{p-1}}{q\,y^{q-1}} && (q \ne 0,\ x \ne 0 \text{ so } y \ne 0) \\
> &\hphantom{\implies y'} = \frac{p}{q} \cdot \frac{x^{p-1}}{\left(x^{p/q}\right)^{q-1}} && (y = x^{p/q}) \\
> &\hphantom{\implies y'} = \frac{p}{q}\,x^{(p-1) - (p - p/q)} = \frac{p}{q}\,x^{(p/q) - 1} && \text{(laws of exponents)}
> \end{aligned}
> $$
> Hence $\dfrac{d}{dx}\,x^{p/q} = \dfrac{p}{q}\,x^{(p/q) - 1}$ for $x \ne 0$ in the domain. $\blacksquare$

\# **Points**
- Write that $y = x^{p/q}$ is *assumed* to be differentiable. Implicit differentiation only computes $y'$; it cannot show that $y'$ exists (the book: "assumed beforehand").
- $\frac{d}{dx}(y^q) = q\,y^{q-1}\,y'$: the factor $y'$ is the Chain Rule, the point most often lost.
- Divide by $q\,y^{q-1}$ only after saying it is not $0$: $q \ne 0$, and $x \ne 0$ so that $y \ne 0$.
- The answer must be in $x$ alone: replace $y^{q-1}$ by $\left(x^{p/q}\right)^{q-1} = x^{p - p/q}$.

\# The idea: raising to the $q$-th power turns the fractional power into the integer powers $y^q$ and $x^p$, whose derivatives are already known (§2.3 and the Chain Rule).

### Tangent Line to an Ellipse

> [!theorem] Tangent line to an ellipse (Exercise 46, p. 170; assigned)
> Show by implicit differentiation that the tangent line to the ellipse
> $$
> \frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
> $$
> at the point $(x_0, y_0)$ has equation
> $$
> \frac{x_0 x}{a^2} + \frac{y_0 y}{b^2} = 1
> $$

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: Assume } y \text{ is a differentiable function of } x. \\
> &\quad \frac{2x}{a^2} + \frac{2y\,y'}{b^2} = 0 && \text{(differentiate w.r.t. } x\text{; Chain Rule)} \\
> &\implies y' = -\frac{b^2 x}{a^2 y} && (y \ne 0) \\[6pt]
> &\text{Case } y_0 \ne 0\text{: the tangent at } (x_0, y_0) \text{ is} \\
> &\quad y - y_0 = -\frac{b^2 x_0}{a^2 y_0}\,(x - x_0) \\
> &\implies a^2 y_0 y - a^2 y_0^2 = -b^2 x_0 x + b^2 x_0^2 && (\times\, a^2 y_0) \\
> &\implies b^2 x_0 x + a^2 y_0 y = b^2 x_0^2 + a^2 y_0^2 \\
> &\implies \frac{x_0 x}{a^2} + \frac{y_0 y}{b^2} = \frac{x_0^2}{a^2} + \frac{y_0^2}{b^2} = 1 && (\div\, a^2 b^2\text{; } (x_0, y_0) \text{ is on the ellipse}) \\[6pt]
> &\text{Case } y_0 = 0\text{: } x_0 = \pm a\text{, and } \tfrac{dx}{dy} = -\tfrac{a^2 y}{b^2 x} = 0 \text{ there, so the tangent is the vertical line } x = x_0, \\
> &\quad \text{while } \frac{x_0 x}{a^2} = 1 \iff x = \frac{a^2}{x_0} = x_0 && (x_0^2 = a^2)
> \end{aligned}
> $$
> Hence the tangent line at $(x_0, y_0)$ is $\dfrac{x_0 x}{a^2} + \dfrac{y_0 y}{b^2} = 1$. $\blacksquare$

\# **Points**
- "Assume $y$ is a differentiable function of $x$" and "$(y \ne 0)$" when dividing.
- The last step uses that $(x_0, y_0)$ lies on the ellipse; say so, or the right side stays $\frac{x_0^2}{a^2} + \frac{y_0^2}{b^2}$.
- The points $(\pm a, 0)$, where $y'$ does not exist, need their own line.

### Sum of the Intercepts of a Tangent

> [!theorem] Intercepts of a tangent to the square-root curve (Exercise 48, p. 171; assigned)
> Show that the sum of the $x$- and $y$-intercepts of any tangent line to the curve $\sqrt{x} + \sqrt{y} = \sqrt{c}$ is equal to $c$.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: Assume } y \text{ is a differentiable function of } x, \text{ and let } (x_0, y_0) \text{ be on the curve with } x_0 > 0,\ y_0 > 0. \\
> &\quad \frac{1}{2\sqrt{x}} + \frac{y'}{2\sqrt{y}} = 0 && \text{(differentiate w.r.t. } x\text{; Chain Rule)} \\
> &\implies y' = -\frac{\sqrt{y}}{\sqrt{x}} && (x > 0) \\[6pt]
> &\text{tangent: } y - y_0 = -\frac{\sqrt{y_0}}{\sqrt{x_0}}\,(x - x_0) \\
> &x\text{-intercept } (y = 0)\text{: } x = x_0 + \frac{\sqrt{x_0}}{\sqrt{y_0}}\,y_0 = x_0 + \sqrt{x_0 y_0} \\
> &y\text{-intercept } (x = 0)\text{: } y = y_0 + \frac{\sqrt{y_0}}{\sqrt{x_0}}\,x_0 = y_0 + \sqrt{x_0 y_0} \\[6pt]
> &\text{sum} = x_0 + 2\sqrt{x_0}\sqrt{y_0} + y_0 = \left(\sqrt{x_0} + \sqrt{y_0}\right)^2 = \left(\sqrt{c}\right)^2 = c && ((x_0, y_0) \text{ is on the curve})
> \end{aligned}
> $$
> Hence the intercepts of every tangent line add up to $c$. $\blacksquare$

\# **Points**
- $x_0 > 0$ and $y_0 > 0$: at the endpoints $(c, 0)$ and $(0, c)$ the tangent is a coordinate axis and has no single intercept on it, so "any tangent line" means a tangent at a point with $x_0 > 0$ and $y_0 > 0$.
- The final step is $\sqrt{x_0} + \sqrt{y_0} = \sqrt{c}$, the curve's own equation.

### Tangent to a Circle Is Perpendicular to the Radius

> [!theorem] Tangent and radius (Exercise 49, p. 171)
> Show, using implicit differentiation, that any tangent line at a point $P$ to a circle with center $O$ is perpendicular to the radius $OP$.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: Let the circle be } (x - h)^2 + (y - k)^2 = r^2,\ O = (h, k),\ P = (x_0, y_0),\ r > 0. \\
> &\text{Assume } y \text{ is a differentiable function of } x. \\
> &\quad 2(x - h) + 2(y - k)\,y' = 0 && \text{(differentiate w.r.t. } x\text{)} \\
> &\implies y' = -\frac{x - h}{y - k} && (y \ne k) \\[6pt]
> &\text{Case } x_0 \ne h,\ y_0 \ne k\text{: } m_{\text{tangent}} \cdot m_{OP} = -\frac{x_0 - h}{y_0 - k} \cdot \frac{y_0 - k}{x_0 - h} = -1 \\
> &\text{Case } x_0 = h\text{: } y_0 - k = \pm r \ne 0,\ y' = 0\text{: the tangent is horizontal and } OP \text{ is vertical.} \\
> &\text{Case } y_0 = k\text{: } x_0 - h = \pm r\text{, the tangent is vertical } \left(\tfrac{dx}{dy} = -\tfrac{y - k}{x - h} = 0\right) \text{ and } OP \text{ is horizontal.}
> \end{aligned}
> $$
> Hence the tangent at $P$ is perpendicular to $OP$ in every case. $\blacksquare$

\# **Points**: the product of slopes is $-1$ only when both slopes exist; the horizontal and vertical cases are separate lines of the proof.

### Tangent Line to a Hyperbola

> [!theorem] Tangent line to a hyperbola (Exercise 47, p. 171)
> Find an equation of the tangent line to the hyperbola $\dfrac{x^2}{a^2} - \dfrac{y^2}{b^2} = 1$ at the point $(x_0, y_0)$.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: Assume } y \text{ is a differentiable function of } x. \\
> &\quad \frac{2x}{a^2} - \frac{2y\,y'}{b^2} = 0 \implies y' = \frac{b^2 x}{a^2 y} && (y \ne 0) \\
> &\text{Case } y_0 \ne 0\text{: } y - y_0 = \frac{b^2 x_0}{a^2 y_0}\,(x - x_0) \\
> &\implies a^2 y_0 y - a^2 y_0^2 = b^2 x_0 x - b^2 x_0^2 && (\times\, a^2 y_0) \\
> &\implies b^2 x_0 x - a^2 y_0 y = b^2 x_0^2 - a^2 y_0^2 \\
> &\implies \frac{x_0 x}{a^2} - \frac{y_0 y}{b^2} = \frac{x_0^2}{a^2} - \frac{y_0^2}{b^2} = 1 && (\div\, a^2 b^2\text{; } (x_0, y_0) \text{ is on the hyperbola}) \\
> &\text{Case } y_0 = 0\text{: } x_0 = \pm a\text{, and } \tfrac{dx}{dy} = \tfrac{a^2 y}{b^2 x} = 0 \text{ there, so the tangent is } x = x_0\text{; and } \frac{x_0 x}{a^2} = 1 \iff x = x_0.
> \end{aligned}
> $$
> Hence the tangent line is $\dfrac{x_0 x}{a^2} - \dfrac{y_0 y}{b^2} = 1$. $\blacksquare$

\# **Points**: the same three conditions as for the ellipse; only the sign of the $y$-term changes.

### Orthogonal Circles and Lines

> [!theorem] Exercise 51 (p. 171)
> Show that the families $x^2 + y^2 = r^2$ and $ax + by = 0$ are orthogonal trajectories of each other.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: Assume } y \text{ is a differentiable function of } x \text{ on each curve; } r > 0\text{, and } a, b \text{ not both } 0. \\
> &\text{circle: } 2x + 2y\,y' = 0 \implies m_1 = -\frac{x}{y} && (y \ne 0) \\
> &\text{line: } a + b\,y' = 0 \implies m_2 = -\frac{a}{b} && (b \ne 0) \\[6pt]
> &\text{Case } a \ne 0,\ b \ne 0\text{: at an intersection, } by = -ax \text{ and } x \ne 0,\ y \ne 0 && ((0, 0) \text{ is not on the circle}) \\
> &\quad m_1 m_2 = \frac{ax}{by} = \frac{ax}{-ax} = -1 \\
> &\text{Case } b = 0\text{: the line } x = 0 \text{ meets the circle at } (0, \pm r)\text{, where } m_1 = 0\text{: horizontal} \perp \text{vertical.} \\
> &\text{Case } a = 0\text{: the line } y = 0 \text{ meets the circle at } (\pm r, 0)\text{, where the circle's tangent is vertical.}
> \end{aligned}
> $$
> Hence every circle is orthogonal to every line of the family. $\blacksquare$

### Orthogonal Families of Circles

> [!theorem] Exercise 52 (p. 171)
> Show that the families $x^2 + y^2 = ax$ and $x^2 + y^2 = by$ are orthogonal trajectories of each other.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: Assume } y \text{ is a differentiable function of } x \text{ on each curve; } a \ne 0,\ b \ne 0. \\
> &2x + 2y\,y' = a \implies m_1 = \frac{a - 2x}{2y} && (y \ne 0) \\
> &2x + 2y\,y' = b\,y' \implies m_2 = \frac{2x}{b - 2y} && (b - 2y \ne 0) \\[6pt]
> &\text{At an intersection: } ax = x^2 + y^2 = by\text{; if } x = 0 \text{ or } y = 0\text{, then } x^2 + y^2 = 0\text{, so the point is } (0, 0) \\
> &\text{At an intersection with } x \ne 0,\ y \ne 0\text{: } ax = x^2 + y^2 = by \\
> &\implies a - 2x = \frac{x^2 + y^2}{x} - 2x = \frac{y^2 - x^2}{x},\qquad b - 2y = \frac{x^2 - y^2}{y} \\
> &\text{If } x^2 \ne y^2\text{: } m_1 m_2 = \frac{y^2 - x^2}{2xy} \cdot \frac{2xy}{x^2 - y^2} = -1 \\
> &\text{If } x^2 = y^2\text{: } a - 2x = 0 \text{ so } m_1 = 0\text{, and } b - 2y = 0 \text{ so the second tangent is vertical.} \\
> &\text{At } (0, 0)\text{: the first circle has the vertical tangent } x = 0\text{, the second the horizontal tangent } y = 0.
> \end{aligned}
> $$
> Hence the two families are orthogonal at every intersection. $\blacksquare$

### Orthogonal Parabolas and Ellipses

> [!theorem] Exercise 53 (p. 171)
> Show that the families $y = cx^2$ and $x^2 + 2y^2 = k$ are orthogonal trajectories of each other.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: } k > 0\text{, } c \ne 0\text{. At an intersection, } x = 0 \implies y = 0 \implies k = 0\text{; so } x \ne 0 \text{ and } y = cx^2 \ne 0. \\
> &y = cx^2 \implies m_1 = 2cx = \frac{2y}{x} && (c = y/x^2,\ x \ne 0) \\
> &x^2 + 2y^2 = k \implies 2x + 4y\,y' = 0 \implies m_2 = -\frac{x}{2y} && (y \ne 0\text{; } y \text{ assumed differentiable}) \\
> &\implies m_1 m_2 = \frac{2y}{x} \cdot \left(-\frac{x}{2y}\right) = -1 \\
> &\text{If } c = 0\text{: } y = 0 \text{ meets the ellipse at } (\pm\sqrt{k}, 0)\text{, where the ellipse's tangent is vertical.}
> \end{aligned}
> $$
> Hence the families are orthogonal trajectories. $\blacksquare$

### Orthogonal Cubics and Ellipses

> [!theorem] Exercise 54 (p. 171)
> Show that the families $y = ax^3$ and $x^2 + 3y^2 = b$ are orthogonal trajectories of each other.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: } b > 0\text{, } a \ne 0\text{. At an intersection, } x = 0 \implies y = 0 \implies b = 0\text{; so } x \ne 0 \text{ and } y = ax^3 \ne 0. \\
> &y = ax^3 \implies m_1 = 3ax^2 = \frac{3y}{x} && (a = y/x^3,\ x \ne 0) \\
> &x^2 + 3y^2 = b \implies 2x + 6y\,y' = 0 \implies m_2 = -\frac{x}{3y} && (y \ne 0) \\
> &\implies m_1 m_2 = -1 \\
> &\text{If } a = 0\text{: } y = 0 \text{ meets the ellipse at } (\pm\sqrt{b}, 0)\text{, where its tangent is vertical.}
> \end{aligned}
> $$
> $\blacksquare$

### Confocal Ellipse and Hyperbola

> [!theorem] Exercise 55 (p. 171)
> Show that the ellipse $x^2/a^2 + y^2/b^2 = 1$ and the hyperbola $x^2/A^2 - y^2/B^2 = 1$ are orthogonal trajectories if $A^2 < a^2$ and $a^2 - b^2 = A^2 + B^2$ (so the ellipse and hyperbola have the same foci).

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: } m_1 = -\frac{b^2 x}{a^2 y},\quad m_2 = \frac{B^2 x}{A^2 y} && \text{(implicit differentiation, } y \ne 0\text{)} \\
> &\implies m_1 m_2 = -\frac{b^2 B^2 x^2}{a^2 A^2 y^2} \\[6pt]
> &\text{At an intersection, subtract the equations: } x^2\left(\frac{1}{a^2} - \frac{1}{A^2}\right) + y^2\left(\frac{1}{b^2} + \frac{1}{B^2}\right) = 0 \\
> &\implies x^2\,\frac{a^2 - A^2}{a^2 A^2} = y^2\,\frac{b^2 + B^2}{b^2 B^2} \\
> &\implies \frac{x^2}{a^2 A^2} = \frac{y^2}{b^2 B^2} && (a^2 - A^2 = b^2 + B^2 > 0) \\
> &\implies b^2 B^2 x^2 = a^2 A^2 y^2 \implies m_1 m_2 = -1 \\[6pt]
> &y \ne 0 \text{ at an intersection: } y = 0 \text{ would give } x^2 = a^2 = A^2\text{, against } A^2 < a^2.
> \end{aligned}
> $$
> $\blacksquare$

### Parallel Tangents on the Rotated Ellipse

> [!theorem] Exercise 59 (p. 171)
> The equation $x^2 - xy + y^2 = 3$ represents a "rotated ellipse," that is, an ellipse whose axes are not parallel to the coordinate axes. Find the points at which this ellipse crosses the $x$-axis and show that the tangent lines at these points are parallel.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: } y = 0 \implies x^2 = 3 \implies (\sqrt{3}, 0),\ (-\sqrt{3}, 0) \\
> &\text{Assume } y \text{ is a differentiable function of } x. \\
> &2x - y - x\,y' + 2y\,y' = 0 && \text{(Product Rule on } xy\text{)} \\
> &\implies y' = \frac{2x - y}{x - 2y} && (x - 2y \ne 0) \\
> &\text{at } (\pm\sqrt{3}, 0)\text{: } y' = \frac{\pm 2\sqrt{3}}{\pm\sqrt{3}} = 2
> \end{aligned}
> $$
> Both tangent lines have slope $2$, so they are parallel. $\blacksquare$

### An Equation with No Points

> [!theorem] Exercise 58 (p. 171)
> (a) Use implicit differentiation to find $y'$ if $x^2 + xy + y^2 + 1 = 0$. (b) Plot the curve in part (a). What do you see? Prove that what you see is correct. (c) In view of part (b), what can you say about the expression for $y'$ that you found in part (a)?

> [!proof]- Proof
> **(a)** $2x + y + xy' + 2y\,y' = 0 \implies y' = -\dfrac{2x + y}{x + 2y}$ $\quad (x + 2y \ne 0)$.
>
> **(b)** Nothing is plotted: no point satisfies the equation.
> $$
> x^2 + xy + y^2 + 1 = \left(x + \tfrac{1}{2}y\right)^2 + \tfrac{3}{4}y^2 + 1 \ge 1 > 0 \quad \text{for all real } x, y.
> $$
> **(c)** The expression is meaningless: the equation defines no function $y$ of $x$ at all, so there is nothing to differentiate. Implicit differentiation silently *assumes* that such a differentiable $y$ exists. $\blacksquare$

\# **Points**: in (b), completing the square is the proof; "the graph is empty" alone is not.

### Two Formulas That Agree on the Curve

> [!theorem] Exercise 63 (p. 171)
> Use implicit differentiation to find $dy/dx$ for the equation $\dfrac{x}{y} = y^2 + 1$, $y \ne 0$, and for the equivalent equation $x = y^3 + y$, $y \ne 0$. Show that although the expressions you get for $dy/dx$ look different, they agree for all points that satisfy the given equation.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{pf: Assume } y \text{ is a differentiable function of } x. \\
> &\text{(1) } \frac{y - x\,y'}{y^2} = 2y\,y' && \text{(Quotient Rule)} \\
> &\implies y - x\,y' = 2y^3\,y' \implies y' = \frac{y}{x + 2y^3} && (x + 2y^3 \ne 0) \\
> &\text{(2) } 1 = 3y^2\,y' + y' \implies y' = \frac{1}{3y^2 + 1} \\[6pt]
> &\text{On the curve, } x = y^3 + y\text{: } \frac{y}{x + 2y^3} = \frac{y}{3y^3 + y} = \frac{1}{3y^2 + 1} && (y \ne 0)
> \end{aligned}
> $$
> Hence the two expressions agree at every point of the curve. $\blacksquare$

\# Lesson for [T/F] and [MC]: two different-looking answers for $y'$ can both be right; compare them only on the curve.

### Discovery Project Families of Implicit Curves

Optional (p. 172): graphing work, with one algebraic proof.

> [!theorem] Discovery Project 2 (p. 172)
> (a) Graph several members of the family of curves $x^2 + y^2 + cx^2y^2 = 1$. Describe how the graph changes as you change the value of $c$. (b) What happens to the curve when $c = -1$? Describe what appears on the screen. Can you prove it algebraically? (c) Find $y'$ by implicit differentiation. For the case $c = -1$, is your expression for $y'$ consistent with what you discovered in part (b)?

> [!proof]- Proof
> **(b)** For $c = -1$: $x^2 + y^2 - x^2y^2 - 1 = -(x^2 - 1)(y^2 - 1) = 0 \iff x = \pm 1$ or $y = \pm 1$: the curve is the four lines $x = \pm 1$, $y = \pm 1$.
>
> **(c)** $2x + 2y\,y' + 2cxy^2 + 2cx^2y\,y' = 0 \implies y' = -\dfrac{x(1 + cy^2)}{y(1 + cx^2)}$. For $c = -1$: $y' = -\dfrac{x(1 - y^2)}{y(1 - x^2)}$. On $y = \pm 1$ (with $x \ne \pm 1$) the numerator is $0$, so $y' = 0$: horizontal lines. On $x = \pm 1$ the denominator is $0$ and the numerator is not (for $y \ne \pm 1$): vertical lines. Consistent. $\blacksquare$

## True or False

"Book" means the statement, or its negation, is printed in the section (page given); "constructed" means it is built from the section's material for practice.

**1.** If $y$ is a differentiable function of $x$, then $\dfrac{d}{dx}\left(y^2\right) = 2y$. *(book, p. 166)*

> [!solution]- Solution
> **F.** $\dfrac{d}{dx}\left(y^2\right) = \dfrac{d}{dy}\left(y^2\right)\dfrac{dy}{dx} = 2y\,\dfrac{dy}{dx}$ by the Chain Rule. Counterexample: $y = x$ gives $\frac{d}{dx}(x^2) = 2x = 2y \cdot 1$, but $y = x^2$ gives $\frac{d}{dx}(x^4) = 4x^3 \ne 2y = 2x^2$.

**2.** If $y$ is a differentiable function of $x$, then $\dfrac{d}{dx}(xy) = y + x\,\dfrac{dy}{dx}$. *(book, p. 167)*

> [!solution]- Solution
> **T.** Product Rule: $\frac{d}{dx}(x) \cdot y + x \cdot \frac{d}{dx}(y) = y + xy'$; the book differentiates $6xy$ as $6xy' + 6y$.

**3.** If $y$ is a differentiable function of $x$, then $\dfrac{d}{dx}\sin y = \cos y$. *(constructed)*

> [!solution]- Solution
> **F.** $\dfrac{d}{dx}\sin y = \cos y \cdot y'$. With $y = 2x$: $\frac{d}{dx}\sin 2x = 2\cos 2x \ne \cos 2x$ (at $x = 0$: $2 \ne 1$).

**4.** The equation $x^2 + y^2 = 25$ defines exactly one function $y = f(x)$. *(book, p. 165)*

> [!solution]- Solution
> **F.** It defines at least two: $f(x) = \sqrt{25 - x^2}$ and $g(x) = -\sqrt{25 - x^2}$ (upper and lower semicircles).

**5.** If $f$ is defined implicitly by $x^3 + y^3 = 6xy$, then $x^3 + [f(x)]^3 = 6x f(x)$ for all $x$ in the domain of $f$. *(book, p. 165)*

> [!solution]- Solution
> **T.** This is what "defined implicitly" means.

**6.** To find $dy/dx$ from an equation in $x$ and $y$, the equation must first be solved for $y$. *(book, p. 165)*

> [!solution]- Solution
> **F.** Implicit differentiation differentiates both sides and solves for $dy/dx$ instead; for $y^5 + 3x^2y^2 + 5x^4 = 12$ solving for $y$ is impossible (p. 168), yet $y'$ is easy.

**7.** From $x^2 + y^2 = 25$, $\dfrac{dy}{dx} = -\dfrac{x}{y}$ holds both for $y = \sqrt{25 - x^2}$ and for $y = -\sqrt{25 - x^2}$. *(book, Note 1, pp. 166–167)*

> [!solution]- Solution
> **T.** Note 1: $-\frac{x}{y}$ gives $-\frac{x}{\sqrt{25 - x^2}}$ on the upper and $\frac{x}{\sqrt{25 - x^2}}$ on the lower semicircle, each the derivative of that function.

**8.** The derivative found by implicit differentiation may contain both $x$ and $y$. *(book, p. 166)*

> [!solution]- Solution
> **T.** $\frac{dy}{dx} = -\frac{x}{y}$ in Example 1; to get a number, substitute a point of the curve.

**9.** If $x^2 + y^2 = 25$, then $y'$ at $(3, 5)$ equals $-\tfrac{3}{5}$. *(constructed)*

> [!solution]- Solution
> **F.** $(3, 5)$ is not on the curve ($9 + 25 = 34 \ne 25$), so $y'$ has no value there. The formula $-x/y$ is meaningful only at points of the curve.

**10.** On $x^3 + y^3 = 6xy$, where $y' = \dfrac{2y - x^2}{y^2 - 2x}$, the tangent line is horizontal at every point of the curve where $2y - x^2 = 0$. *(book, p. 167)*

> [!solution]- Solution
> **F.** The book adds "provided that $y^2 - 2x \ne 0$". At $(0, 0)$, on the curve, $2y - x^2 = 0$ and $y^2 - 2x = 0$; the folium crosses itself there and has no single tangent.

**11.** The tangent to the folium $x^3 + y^3 = 6xy$ at $(3, 3)$ is $x + y = 6$. *(book, p. 167)*

> [!solution]- Solution
> **T.** $y' = \frac{2 \cdot 3 - 3^2}{3^2 - 2 \cdot 3} = -1$, so $y - 3 = -(x - 3)$.

**12.** The folium $x^3 + y^3 = 6xy$ has a horizontal tangent at $(2^{4/3}, 2^{5/3})$. *(book, p. 167)*

> [!solution]- Solution
> **T.** There $2y - x^2 = 2^{8/3} - 2^{8/3} = 0$ and $y^2 - 2x = 2^{10/3} - 2^{7/3} \ne 0$.

**13.** At a point of the curve where the denominator of $y' = N/D$ is $0$ and the numerator is not, the tangent line is vertical. *(constructed)*

> [!solution]- Solution
> **T.** There $\frac{dx}{dy} = \frac{D}{N} = 0$. Example: $x^2 + y^2 = 25$ at $(5, 0)$: $y' = -x/y$ has $D = 0$, $N = -5 \ne 0$, and the tangent is $x = 5$.

**14.** If $x^4 + y^4 = 16$, then $y'' = -\dfrac{48x^2}{y^7}$. *(book, p. 169)*

> [!solution]- Solution
> **T.** Example 4: $y'' = -\frac{3x^2(y^4 + x^4)}{y^7} = -\frac{3x^2 \cdot 16}{y^7}$.

**15.** To find $y''$ implicitly, it is enough to differentiate the expression for $y'$; there is no need to substitute $y'$ again. *(constructed)*

> [!solution]- Solution
> **F.** Differentiating $y'$ produces a new $y'$ (Example 4: $\frac{d}{dx}(y^3) = 3y^2y'$), which must be replaced by its expression; then the original equation simplifies the result.

**16.** The Power Rule proof by implicit differentiation (Exercise 50) shows that $x^{p/q}$ is differentiable. *(book, p. 171)*

> [!solution]- Solution
> **F.** It assumes "beforehand" that $y = x^{p/q}$ is differentiable and only computes $y'$.

**17.** Implicit differentiation of $x^2 + xy + y^2 + 1 = 0$ gives $y' = -\dfrac{2x + y}{x + 2y}$, the slope of the tangent line to this curve. *(book, Exercise 58, p. 171)*

> [!solution]- Solution
> **F.** The equation has no points: $\left(x + \frac{1}{2}y\right)^2 + \frac{3}{4}y^2 + 1 > 0$. There is no curve and no tangent; the formula is meaningless.

**18.** If two expressions for $dy/dx$ obtained from equivalent equations do not simplify to the same formula, one of them is wrong. *(book, Exercise 63, p. 171)*

> [!solution]- Solution
> **F.** $\frac{y}{x + 2y^3}$ and $\frac{1}{3y^2 + 1}$ (from $\frac{x}{y} = y^2 + 1$ and $x = y^3 + y$) look different but agree at every point of the curve.

**19.** Two curves are orthogonal if their tangent lines are perpendicular at each point of intersection. *(book, p. 171)*

> [!solution]- Solution
> **T.** The definition before Exercises 51–54.

**20.** The circles $x^2 + y^2 = r^2$ and the lines $ax + by = 0$ are orthogonal trajectories. *(book, Exercise 51, p. 171)*

> [!solution]- Solution
> **T.** At an intersection $m_1 m_2 = \frac{ax}{by} = -1$; see [[#Orthogonal Circles and Lines]].

**21.** The tangent line to $\dfrac{x^2}{a^2} + \dfrac{y^2}{b^2} = 1$ at $(x_0, y_0)$ is $\dfrac{x_0 x}{a^2} + \dfrac{y_0 y}{b^2} = 1$. *(book, Exercise 46, p. 170)*

> [!solution]- Solution
> **T.** See [[#Tangent Line to an Ellipse]].

**22.** To find $dx/dy$, regard $x$ as a function of $y$ and differentiate both sides with respect to $y$. *(book, Exercises 23–24, p. 170)*

> [!solution]- Solution
> **T.** Then every term with $x$ gets the factor $\frac{dx}{dy}$.

**23.** If $f(x) + x^2[f(x)]^3 = 10$ and $f(1) = 2$, then $f'(1) = -\tfrac{16}{13}$. *(constructed from Exercise 21)*

> [!solution]- Solution
> **T.** $f'(1) + 2 \cdot 1 \cdot 2^3 + 3 \cdot 1^2 \cdot 2^2 f'(1) = 0 \implies 13f'(1) = -16$.

**24.** If $y = x^{p/q}$ is differentiable, then $y' = \dfrac{p}{q}\,x^{(p/q) - 1}$ for $x \ne 0$ in the domain. *(book, Exercise 50, p. 171)*

> [!solution]- Solution
> **T.** See [[#Power Rule for Rational Exponents]].

**25.** The tangent line to a circle at $P$ is perpendicular to the radius $OP$. *(book, Exercise 49, p. 171)*

> [!solution]- Solution
> **T.** See [[#Tangent to a Circle Is Perpendicular to the Radius]].

**26.** The curve $x^2 - xy + y^2 = 3$ has parallel tangent lines at the two points where it crosses the $x$-axis. *(book, Exercise 59, p. 171)*

> [!solution]- Solution
> **T.** Both slopes equal $2$ at $(\pm\sqrt{3}, 0)$.

**27.** If $xy + y^3 = 1$, then $y'' = 0$ at the point where $x = 0$. *(constructed from Exercise 41)*

> [!solution]- Solution
> **T.** At $x = 0$: $y = 1$, $y' = -\frac{1}{3}$, and $2y' + 6y(y')^2 + (x + 3y^2)y'' = 0$ gives $-\frac{2}{3} + \frac{2}{3} + 3y'' = 0$.

## Problem Types

Each type has a template from the book (the page is given) or, where the book has no example, from an exercise. "Where the points are" names the lines a grader looks for.

### Find the Derivative Implicitly

> [!example] Example 2 (a), p. 167
> Find $y'$ if $x^3 + y^3 = 6xy$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &\text{Assume } y \text{ is a differentiable function of } x. \\
> &3x^2 + 3y^2\,y' = 6x\,y' + 6y && \text{(Chain Rule on } y^3\text{; Product Rule on } 6xy\text{)} \\
> &\implies y^2\,y' - 2x\,y' = 2y - x^2 && (\div\, 3\text{; collect the } y' \text{ terms}) \\
> &\implies \left(y^2 - 2x\right)y' = 2y - x^2 \\
> &\implies y' = \frac{2y - x^2}{y^2 - 2x} && (y^2 - 2x \ne 0)
> \end{aligned}
> $$

> [!example] Example 3, p. 168
> Find $y'$ if $\sin(x + y) = y^2 \cos x$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &\cos(x + y) \cdot (1 + y') = y^2(-\sin x) + (\cos x)(2y\,y') && \text{(Chain Rule left; Product and Chain Rules right)} \\
> &\implies \cos(x + y) + y^2 \sin x = (2y\cos x)\,y' - \cos(x + y)\,y' \\
> &\implies y' = \frac{y^2 \sin x + \cos(x + y)}{2y\cos x - \cos(x + y)} && (2y\cos x - \cos(x + y) \ne 0)
> \end{aligned}
> $$
> Check: at $(0, 0)$, $y' = \frac{0 + 1}{0 - 1} = -1$, as the graph (Figure 6) suggests.

**Where the points are:** the factor $y'$ on every $y$-term, both terms of each Product Rule, collecting $y'$ correctly, and the condition (denominator $\ne 0$).
**Exercises:** 5–20 (assigned: 5, 7, 9, 15, 17, 19). Answers (checked with sympy): 5: $y' = \frac{x - 2y}{2x - y}$; 7: $y' = -\frac{4x^3 + 2xy^2}{2x^2y + 3y^2}$; 9: $y' = \frac{2x - y^2 - 1}{2xy + 3y^2 + 1}$ (after clearing the denominator); 15: $y' = \frac{y\sec^2(x/y) - y^2}{y^2 + x\sec^2(x/y)}$; 17: $y' = \frac{8x^3\sqrt{x + y} - 1}{1 - 8y^3\sqrt{x + y}}$; 19: $y' = \frac{4xy\sqrt{xy} - y}{x - 2x^2\sqrt{xy}}$.

### Implicit versus Explicit and the Consistency Check

> [!example] Example 1, p. 166
> If $x^2 + y^2 = 25$, find $\dfrac{dy}{dx}$. Then find an equation of the tangent to the circle $x^2 + y^2 = 25$ at the point $(3, 4)$.

> [!solution]- Solution
> **Solution 1 (implicit).**
> $$
> \begin{aligned}
> &\frac{d}{dx}\left(x^2 + y^2\right) = \frac{d}{dx}(25) \\
> &\implies 2x + 2y\,\frac{dy}{dx} = 0 && \text{(Chain Rule on } y^2\text{)} \\
> &\implies \frac{dy}{dx} = -\frac{x}{y} && (y \ne 0) \\
> &\text{at } (3, 4)\text{: } \frac{dy}{dx} = -\frac{3}{4} \implies y - 4 = -\tfrac{3}{4}(x - 3) \iff 3x + 4y = 25
> \end{aligned}
> $$
> **Solution 2 (explicit).** $(3, 4)$ lies on the upper semicircle, so use $f(x) = \sqrt{25 - x^2}$:
> $$
> f'(x) = \tfrac{1}{2}\left(25 - x^2\right)^{-1/2}(-2x) = -\frac{x}{\sqrt{25 - x^2}},\qquad f'(3) = -\frac{3}{\sqrt{25 - 3^2}} = -\frac{3}{4}
> $$
> and, as in Solution 1, the tangent is $3x + 4y = 25$.

> [!example] Exercise 3, p. 169 (assigned)
> $\sqrt{x} + \sqrt{y} = 1$. (a) Find $y'$ by implicit differentiation. (b) Solve the equation explicitly for $y$ and differentiate to get $y'$ in terms of $x$. (c) Check that your solutions to parts (a) and (b) are consistent by substituting the expression for $y$ into your solution for part (a).

> [!solution]- Solution
> $$
> \begin{aligned}
> &\text{(a) } \frac{1}{2\sqrt{x}} + \frac{y'}{2\sqrt{y}} = 0 \implies y' = -\frac{\sqrt{y}}{\sqrt{x}} && (x > 0,\ y > 0\text{, i.e. } 0 < x < 1) \\
> &\text{(b) } \sqrt{y} = 1 - \sqrt{x} \implies y = \left(1 - \sqrt{x}\right)^2 \implies y' = 2\left(1 - \sqrt{x}\right)\left(-\frac{1}{2\sqrt{x}}\right) = -\frac{1 - \sqrt{x}}{\sqrt{x}} \\
> &\text{(c) } \sqrt{y} = 1 - \sqrt{x} \text{ in (a)}\text{: } -\frac{\sqrt{y}}{\sqrt{x}} = -\frac{1 - \sqrt{x}}{\sqrt{x}}\text{, the same as (b).}
> \end{aligned}
> $$

**Where the points are:** in the explicit route, choosing the branch the point lies on (upper semicircle); in (c), substituting $y$ (not $x$) into the implicit answer.
**Exercises:** 1–4 (assigned: 3). Exercise 1: $y' = \frac{10x}{3y^2}$, and $y = (5x^2 - 7)^{1/3}$ gives $y' = \frac{10x}{3}(5x^2 - 7)^{-2/3}$.

### Tangent Line at a Given Point

> [!example] Example 2 (b), p. 167
> Find the tangent to the folium of Descartes $x^3 + y^3 = 6xy$ at the point $(3, 3)$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &3^3 + 3^3 = 54 = 6 \cdot 3 \cdot 3 && ((3, 3) \text{ is on the curve}) \\
> &y' = \frac{2y - x^2}{y^2 - 2x} && \text{(part (a))} \\
> &\text{at } (3, 3)\text{: } y' = \frac{2 \cdot 3 - 3^2}{3^2 - 2 \cdot 3} = -1 \\
> &\implies y - 3 = -1(x - 3) \iff x + y = 6
> \end{aligned}
> $$
> A glance at Figure 4 confirms that $-1$ is a reasonable slope at $(3, 3)$.

**Where the points are:** checking the point is on the curve, the slope at the point, and the point-slope form.
**Exercises:** 25–34 (assigned: 25, 29, 31, 33), 35 (a), 36 (a), 43 (b). Answers (sympy): 25: $y = \frac{1}{2}x$; 26: $y = -x + \frac{\pi}{4}$; 27: $y = \frac{x}{\sqrt{3}} + 4$; 28: $y = \frac{7\sqrt{2}}{8}x - \frac{3\sqrt{2}}{4}$; 29: $y = \frac{3}{4}x - \frac{1}{2}$; 30: $y = -\frac{1}{2}x + 2$; 31: $y = x + \frac{1}{2}$; 32: $y = -\frac{\sqrt{3}}{5}x + \frac{11}{5}$; 33: $y = -\frac{9}{13}x + \frac{40}{13}$; 34: $y = -2$; 35 (a): $y = \frac{9}{2}x - \frac{5}{2}$; 36 (a): $y = -\frac{9}{4}x + \frac{1}{4}$; 43 (b): $y = -x + 1$ at $(0, 1)$ and $y = \frac{1}{3}x + 2$ at $(0, 2)$.

> [!example] Exercise 31, p. 170 (assigned): the cardioid
> $x^2 + y^2 = (2x^2 + 2y^2 - x)^2$ at $\left(0, \tfrac{1}{2}\right)$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &2x + 2y\,y' = 2\left(2x^2 + 2y^2 - x\right)\left(4x + 4y\,y' - 1\right) && \text{(Chain Rule on the right)} \\
> &\text{at } \left(0, \tfrac{1}{2}\right)\text{: } 2x^2 + 2y^2 - x = \tfrac{1}{2} \\
> &\implies y' = 2 \cdot \tfrac{1}{2}\left(2y' - 1\right) = 2y' - 1 \implies y' = 1 \\
> &\implies y = x + \tfrac{1}{2}
> \end{aligned}
> $$
> \# Substitute the point right after differentiating; solving for $y'$ in general first is much longer.

### Horizontal Tangents

> [!example] Example 2 (c), p. 167
> At what point in the first quadrant is the tangent line to $x^3 + y^3 = 6xy$ horizontal?

> [!solution]- Solution
> $$
> \begin{aligned}
> &y' = \frac{2y - x^2}{y^2 - 2x} = 0 \iff 2y - x^2 = 0 && (y^2 - 2x \ne 0) \\
> &y = \tfrac{1}{2}x^2 \text{ in the curve: } x^3 + \left(\tfrac{1}{2}x^2\right)^3 = 6x\left(\tfrac{1}{2}x^2\right) \\
> &\implies x^6 = 16x^3 \implies x^3 = 16 && (x \ne 0 \text{ in the first quadrant}) \\
> &\implies x = 16^{1/3} = 2^{4/3},\quad y = \tfrac{1}{2}\left(2^{8/3}\right) = 2^{5/3} \\
> &\text{check: } y^2 - 2x = 2^{10/3} - 2^{7/3} \ne 0
> \end{aligned}
> $$
> The tangent is horizontal at $(2^{4/3}, 2^{5/3}) \approx (2.5198, 3.1748)$; Figure 5 shows that this is reasonable.

**Where the points are:** "$y' = 0 \iff$ numerator $= 0$" *with* the denominator condition, substituting back into the curve, and excluding $x = 0$ before dividing.
**Exercises:** 36 (b): $(-2, \pm 2)$ ($x = 0$ gives $y = 0$, where the denominator $2y$ vanishes); 43 (a)(c): $x = 1 \pm \frac{\sqrt{3}}{3}$, 8 points; 44 (b): $x = 0, \frac{1}{2}, 1$, 9 points (at $x = 0$ and $x = 1$, the root $y = 0$ is excluded because the denominator vanishes there); 45: $\left(\pm\frac{5\sqrt{3}}{4}, \pm\frac{5}{4}\right)$, four points.

### Vertical Tangents

Constructed: the book asks only for horizontal tangents, but the section card lists vertical ones.

> [!example] Example (constructed from Example 2)
> At what point in the first quadrant is the tangent line to $x^3 + y^3 = 6xy$ vertical?

> [!solution]- Solution
> $$
> \begin{aligned}
> &\text{vertical} \iff y^2 - 2x = 0 \text{ and } 2y - x^2 \ne 0 \\
> &x = \tfrac{1}{2}y^2 \text{ in the curve: } \left(\tfrac{1}{2}y^2\right)^3 + y^3 = 6\left(\tfrac{1}{2}y^2\right)y \\
> &\implies y^6 = 16y^3 \implies y^3 = 16 && (y \ne 0) \\
> &\implies y = 2^{4/3},\quad x = 2^{5/3} \\
> &\text{check: } 2y - x^2 = 2^{7/3} - 2^{10/3} \ne 0
> \end{aligned}
> $$
> The tangent is vertical at $(2^{5/3}, 2^{4/3})$, the mirror image of the horizontal point in the line $y = x$ (the folium is symmetric in $x$ and $y$).

**Where the points are:** the numerator condition $\ne 0$; without it, $(0, 0)$ would wrongly qualify.

### Derivative at a Point of a Function Defined by an Equation

> [!example] Exercise 21, p. 169 (assigned)
> If $f(x) + x^2[f(x)]^3 = 10$ and $f(1) = 2$, find $f'(1)$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &f'(x) + 2x[f(x)]^3 + x^2 \cdot 3[f(x)]^2 f'(x) = 0 && \text{(Product and Chain Rules)} \\
> &x = 1\text{: } f'(1) + 2 \cdot 2^3 + 3 \cdot 2^2 \cdot f'(1) = 0 && (f(1) = 2) \\
> &\implies 13f'(1) = -16 \implies f'(1) = -\tfrac{16}{13}
> \end{aligned}
> $$

**Where the points are:** the Chain Rule factor $f'(x)$ in $\frac{d}{dx}[f(x)]^3$, and substituting before solving.
**Exercises:** 21–22 (assigned: 21). Exercise 22: $g(0) = 0$ from $g(0) + 0 = 0$; then $g'(x) + \sin g(x) + x\cos g(x)\,g'(x) = 2x$ gives $g'(0) = 0$.

### dx by dy with y as the Independent Variable

> [!example] Exercise 24, p. 170 (assigned)
> Regard $y$ as the independent variable and $x$ as the dependent variable and use implicit differentiation to find $dx/dy$: $y \sec x = x \tan y$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &\text{Assume } x \text{ is a differentiable function of } y\text{; write } x' = \tfrac{dx}{dy}. \\
> &\sec x + y\sec x\tan x \cdot x' = x' \tan y + x\sec^2 y && \text{(Product Rule both sides; Chain Rule on } \sec x\text{)} \\
> &\implies x'\left(y\sec x\tan x - \tan y\right) = x\sec^2 y - \sec x \\
> &\implies \frac{dx}{dy} = \frac{x\sec^2 y - \sec x}{y\sec x\tan x - \tan y} && (y\sec x\tan x - \tan y \ne 0)
> \end{aligned}
> $$

**Where the points are:** now the factor $x'$ goes on every $x$-term, and none on $y$-terms.
**Exercises:** 23–24 (assigned: 24). Exercise 23: $\frac{dx}{dy} = \frac{x^3 - 2x^4 y - 6xy^2}{4x^3y^2 - 3x^2y + 2y^3}$.

### Second Derivative

> [!example] Example 4, pp. 168–169
> Find $y''$ if $x^4 + y^4 = 16$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &4x^3 + 4y^3\,y' = 0 \implies y' = -\frac{x^3}{y^3} && (y \ne 0)\quad (3) \\
> &y'' = \frac{d}{dx}\left(-\frac{x^3}{y^3}\right) = -\frac{y^3 \cdot 3x^2 - x^3\left(3y^2\,y'\right)}{\left(y^3\right)^2} && \text{(Quotient Rule; Chain Rule on } y^3\text{)} \\
> &\hphantom{y''} = -\frac{3x^2y^3 - 3x^3y^2\left(-\frac{x^3}{y^3}\right)}{y^6} && \text{(substitute (3))} \\
> &\hphantom{y''} = -\frac{3\left(x^2y^4 + x^6\right)}{y^7} = -\frac{3x^2\left(y^4 + x^4\right)}{y^7} \\
> &\hphantom{y''} = -\frac{3x^2(16)}{y^7} = -48\,\frac{x^2}{y^7} && (x^4 + y^4 = 16)
> \end{aligned}
> $$

**Where the points are:** $3y^2y'$ (not $3y^2$) inside the Quotient Rule, substituting $y'$, and using the original equation at the end.
**Exercises:** 37–40 (assigned: 37, 39). Answers (sympy): 37: $y'' = -\frac{1}{4y^3}$; 38: $y'' = -\frac{18}{(x + 2y)^3}$; 39: $y'' = \frac{\cos x\cos^2 y + \sin^2 x\sin y}{\cos^3 y}$; 40: $y'' = -\frac{14x}{y^5}$.

### Higher Derivative at a Point

> [!example] Exercise 41, p. 170
> If $xy + y^3 = 1$, find the value of $y''$ at the point where $x = 0$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &x = 0\text{: } y^3 = 1 \implies y = 1 \\
> &y + x\,y' + 3y^2\,y' = 0 && (\ast) \\
> &\text{at } (0, 1)\text{: } 1 + 3y' = 0 \implies y' = -\tfrac{1}{3} \\
> &\text{differentiate } (\ast)\text{: } 2y' + x\,y'' + 6y\left(y'\right)^2 + 3y^2\,y'' = 0 \\
> &\text{at } (0, 1)\text{: } -\tfrac{2}{3} + 6 \cdot \tfrac{1}{9} + 3y'' = 0 \implies y'' = 0
> \end{aligned}
> $$

**Where the points are:** the point first ($y$ from the equation), then $y'$, then $y''$, substituting numbers after each differentiation.
**Exercises:** 41, 42, 64.
- Exercise 42 (p. 170): "If $x^2 + xy + y^3 = 1$, find the value of $y'''$ at the point where $x = 1$." Answer: $y = 0$, $y' = -2$, $y'' = 2$, $y''' = 42$.
- Exercise 64 (p. 171): "The *Bessel function* of order 0, $y = J(x)$, satisfies the differential equation $xy'' + y' + xy = 0$ for all values of $x$ and its value at 0 is $J(0) = 1$. (a) Find $J'(0)$. (b) Use implicit differentiation to find $J''(0)$." Answer: at $x = 0$, $0 + J'(0) + 0 = 0$, so $J'(0) = 0$; differentiating, $y'' + xy''' + y'' + y + xy' = 0$, and at $x = 0$: $2J''(0) + J(0) = 0$, so $J''(0) = -\frac{1}{2}$.

### Tangent Lines at a General Point

The exercises 46–49 are proofs; see [[#Tangent Line to an Ellipse]], [[#Tangent Line to a Hyperbola]], [[#Sum of the Intercepts of a Tangent]] and [[#Tangent to a Circle Is Perpendicular to the Radius]]. Assigned: 46, 48.

**Where the points are:** "assume $y$ is differentiable", the case $y_0 = 0$, and using that $(x_0, y_0)$ lies on the curve.

### Orthogonal Trajectories

> [!example] Exercise 56, p. 171
> Find the value of the number $a$ such that the families of curves $y = (x + c)^{-1}$ and $y = a(x + k)^{1/3}$ are orthogonal trajectories.

> [!solution]- Solution
> $$
> \begin{aligned}
> &m_1 = -(x + c)^{-2} = -y^2 && ((x + c)^{-1} = y) \\
> &m_2 = \tfrac{a}{3}(x + k)^{-2/3} = \tfrac{a}{3}\cdot\frac{a^2}{y^2} = \frac{a^3}{3y^2} && ((x + k)^{1/3} = y/a,\ y \ne 0) \\
> &m_1 m_2 = -\frac{a^3}{3} = -1 \iff a^3 = 3 \iff a = \sqrt[3]{3}
> \end{aligned}
> $$

**Where the points are:** eliminating the family constants $c$ and $k$, so that the product holds at *every* intersection.
**Exercises:** 51–55 are proofs (see [[#Orthogonal Circles and Lines]] and the four after it); 56 finds a constant.

### Normal Line Meets the Curve Again

> [!example] Exercise 60 (a), p. 171
> Where does the [[Normal Line|normal line]] to the ellipse $x^2 - xy + y^2 = 3$ at the point $(-1, 1)$ intersect the ellipse a second time?

> [!solution]- Solution
> $$
> \begin{aligned}
> &y' = \frac{2x - y}{x - 2y} && \text{(as in Exercise 59)} \\
> &\text{at } (-1, 1)\text{: } y' = \frac{-3}{-3} = 1 \implies m_{\text{normal}} = -1 \\
> &\text{normal: } y - 1 = -(x + 1) \iff y = -x \\
> &\text{in the ellipse: } x^2 + x^2 + x^2 = 3 \implies x = \pm 1
> \end{aligned}
> $$
> The second intersection is $(1, -1)$.

**Where the points are:** the normal slope $-1/y'$, and solving the line together with the curve.

### Points Where the Tangent Has a Given Slope

> [!example] Exercise 61, p. 171 (assigned)
> Find all points on the curve $x^2y^2 + xy = 2$ where the slope of the tangent line is $-1$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &2xy^2 + 2x^2y\,y' + y + x\,y' = 0 && \text{(Product Rule)} \\
> &\implies y' = -\frac{y(2xy + 1)}{x(2xy + 1)} = -\frac{y}{x} && (x \ne 0,\ 2xy + 1 \ne 0) \\
> &\text{on the curve } (xy)^2 + xy - 2 = 0 \implies xy = 1 \text{ or } -2\text{, so } 2xy + 1 \ne 0 \text{ and } x \ne 0 \\
> &y' = -1 \iff y = x \implies x^4 + x^2 - 2 = 0 \implies \left(x^2 + 2\right)\left(x^2 - 1\right) = 0 \implies x = \pm 1
> \end{aligned}
> $$
> The points are $(1, 1)$ and $(-1, -1)$.

**Where the points are:** justifying the cancellation of $2xy + 1$, and putting $y = x$ back into the curve.

### Tangent Lines Through a Point Not on the Curve

> [!example] Exercise 62, p. 171
> Find equations of both the tangent lines to the ellipse $x^2 + 4y^2 = 36$ that pass through the point $(12, 3)$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &12^2 + 4 \cdot 3^2 = 180 \ne 36 && ((12, 3) \text{ is not on the ellipse}) \\
> &\text{tangent at a point } (x_0, y_0) \text{ of the ellipse: } x_0 x + 4y_0 y = 36 && \text{(as in Exercise 46)} \\
> &\text{through } (12, 3)\text{: } 12x_0 + 12y_0 = 36 \implies x_0 = 3 - y_0 \\
> &\text{on the ellipse: } (3 - y_0)^2 + 4y_0^2 = 36 \implies 5y_0^2 - 6y_0 - 27 = 0 \implies (5y_0 + 9)(y_0 - 3) = 0 \\
> &\implies (x_0, y_0) = (0, 3) \text{ or } \left(\tfrac{24}{5}, -\tfrac{9}{5}\right)
> \end{aligned}
> $$
> The tangent lines are $y = 3$ and $2x - 3y = 15$.

**Where the points are:** the unknown is the point of tangency; never substitute $(12, 3)$ into $y'$.
**Exercises:** 62, 65. Exercise 65 (p. 171): "The figure shows a lamp located three units to the right of the $y$-axis and a shadow created by the elliptical region $x^2 + 4y^2 \le 5$. If the point $(-5, 0)$ is on the edge of the shadow, how far above the $x$-axis is the lamp located?" The tangent $x_0x + 4y_0y = 5$ passes through $(-5, 0)$ when $x_0 = -1$, so $y_0 = \pm 1$; the lamp is above the $x$-axis (figure), so the tangent point is $(-1, 1)$, the line is $-x + 4y = 5$, and at $x = 3$ the lamp is $2$ units above the $x$-axis.

### Rates in an Applied Equation

> [!example] Exercise 57, p. 171
> The van der Waals equation for $n$ moles of a gas is $\left(P + \dfrac{n^2 a}{V^2}\right)(V - nb) = nRT$. (a) If $T$ remains constant, use implicit differentiation to find $dV/dP$. (b) Find the rate of change of volume with respect to pressure of 1 mole of carbon dioxide at a volume of $V = 10$ L and a pressure of $P = 2.5$ atm. Use $a = 3.592$ L²-atm/mole² and $b = 0.04267$ L/mole.

> [!solution]- Solution
> $$
> \begin{aligned}
> &\left(1 - \frac{2n^2 a}{V^3}\,V'\right)(V - nb) + \left(P + \frac{n^2 a}{V^2}\right)V' = 0 && (V' = dV/dP\text{; } T \text{ constant}) \\
> &\implies V'\left[P + \frac{n^2 a}{V^2} - \frac{2n^2 a(V - nb)}{V^3}\right] = -(V - nb) \\
> &\implies \frac{dV}{dP} = -\frac{V^3(V - nb)}{PV^3 - n^2 aV + 2n^3 ab} && (\times\, V^3) \\
> &\text{(b) } n = 1,\ V = 10,\ P = 2.5\text{: } \frac{dV}{dP} \approx -4.04 \text{ L/atm}
> \end{aligned}
> $$

**Where the points are:** which variable is independent ($P$), and that the constant $T$ differentiates to $0$.

### Graphing Exercises

Not by hand: 35 (b), 36 (c), 43 (a)(d), 44 (a), 58 (b) (the plot; its proof is above), 60 (b), the sketches asked in 51–54 ("Sketch both families of curves on the same axes"), and the Discovery Project 1 and 2 (a). Their algebraic parts are covered above (43 (b)(c), 44 (b), 51–54, 58, Discovery Project 2 (b)(c)).

## Related

- [[CAL1 2.6 Exam Map.excalidraw]]
- [[Chain Rule]], [[Product Rule]], [[Quotient Rule]], [[Power Rule]], [[Higher Derivatives]]
- [[Tangent Line]], [[Normal Line]], [[Vertical Tangent Line]]
- [[CAL1 Index]]
