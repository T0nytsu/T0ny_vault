---
course: [CAL1]
chapter: ["2.2"]
tags: [calculus, homework, solutions, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §2.2, pp. 120-128, scanned PDF (definitions and equation numbers)"
created: 2026-10-05
questions: "[[CAL1 HW 2.2 Questions]]"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 2.2 Questions#ST 2.2.3\|ST 2.2.3]] | (a) II, (b) IV, (c) I, (d) III |
| [[CAL1 HW 2.2 Questions#ST 2.2.19\|ST 2.2.19]] | $f'(x) = 3$; domain of $f$ and of $f'$: $\mathbb{R}$ |
| [[CAL1 HW 2.2 Questions#ST 2.2.23\|ST 2.2.23]] | $A'(p) = 12p^2 + 3$; domain of $A$ and of $A'$: $\mathbb{R}$ |
| [[CAL1 HW 2.2 Questions#ST 2.2.27\|ST 2.2.27]] | $g'(u) = -\dfrac{5}{(4u - 1)^2}$; domain of $g$ and of $g'$: $u \ne \tfrac{1}{4}$ |
| [[CAL1 HW 2.2 Questions#ST 2.2.39\|ST 2.2.39]] | $-4$ (corner), $0$ (discontinuity) |
| [[CAL1 HW 2.2 Questions#ST 2.2.41\|ST 2.2.41]] | $1$ (discontinuity), $5$ (vertical tangent) |
| [[CAL1 HW 2.2 Questions#ST 2.2.45\|ST 2.2.45]] | $f''(1)$ is bigger: $f'(-1) < 0 < f''(1)$ |
| [[CAL1 HW 2.2 Questions#ST 2.2.47\|ST 2.2.47]] | $a = f$, $b = f'$, $c = f''$ |
| [[CAL1 HW 2.2 Questions#ST 2.2.55\|ST 2.2.55]] | (a) $f'(a) = \dfrac{1}{3a^{2/3}}$; (b), (c) shown |
| [[CAL1 HW 2.2 Questions#ST 2.2.57\|ST 2.2.57]] | $f'(x) = 1$ if $x > 6$, $f'(x) = -1$ if $x < 6$; $f'(6)$ does not exist |
| [[CAL1 HW 2.2 Questions#ST 2.2.59\|ST 2.2.59]] | (b) all $x$; (c) $f'(x) = 2\lvert x \rvert$ |
| [[CAL1 HW 2.2 Questions#ST 2.2.63\|ST 2.2.63]] | (a) $f'_{-}(4) = -1$, $f'_{+}(4) = 1$; (c) at $0$ and $5$; (d) at $0$, $4$ and $5$ |

Additional exercises, not assigned:

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 2.2 Questions#ST 2.2.29\|ST 2.2.29]] | $f'(x) = -\dfrac{1}{2(1 + x)^{3/2}}$; domain of $f$ and of $f'$: $(-1, \infty)$ |
| [[CAL1 HW 2.2 Questions#ST 2.2.37\|ST 2.2.37]] | (a) the rate at which the percentage changes, in percentage points per year; (b) on January 1, 2022 it is increasing at $3.5$ percentage points per year |
| [[CAL1 HW 2.2 Questions#ST 2.2.53\|ST 2.2.53]] | $f'(x) = 4x - 3x^2$, $f''(x) = 4 - 6x$, $f'''(x) = -6$, $f^{(4)}(x) = 0$ |
| [[CAL1 HW 2.2 Questions#ST 2.2.58\|ST 2.2.58]] | not differentiable at the integers; $f'(x) = 0$ if $x$ is not an integer |
| [[CAL1 HW 2.2 Questions#ST 2.2.61\|ST 2.2.61]] | Proof |
| [[CAL1 HW 2.2 Questions#ST 2.2.62\|ST 2.2.62]] | (a) $f'_{-}(0) = 0$, $f'_{+}(0) = 1$, not differentiable; (b) $f'_{-}(0) = 0 = f'_{+}(0)$, differentiable |

## ST §2.2 The Derivative as a Function

> [!note] Note
> The facts that the answers use, each under its name. An answer writes the formula itself; the numbers are those of ST §2.2 and matter only where a question names them.
> - **[[Derivative]] as a function** (Equation 2): $f'(x) = \lim_{h \to 0} \dfrac{f(x + h) - f(x)}{h}$. In the limit $h$ is the variable and $x$ is a constant. The domain of $f'$ is $\{x \mid f'(x) \text{ exists}\}$; it may be smaller than the domain of $f$.
> - **Graph of $f'$**: $f'(x)$ is the slope of the tangent line to $y = f(x)$ at $(x, f(x))$. Horizontal tangent $\implies f'(x) = 0$; $f$ increasing $\implies f' \ge 0$; $f$ decreasing $\implies f' \le 0$.
> - **[[Differentiable Function|Differentiable]] at $a$** (Definition 3): $f'(a)$ exists. Differentiable on an open interval: differentiable at every number in the interval.
> - **Differentiable $\implies$ continuous**: if $f$ is differentiable at $a$, then $f$ is continuous at $a$. So not continuous at $a$ $\implies$ not differentiable at $a$. The converse is false: $\lvert x \rvert$ is continuous at $0$ and not differentiable at $0$.
> - **Three ways for $f$ not to be differentiable at $a$**: a corner (the left and right limits of the difference quotient are different), a discontinuity, a [[Vertical Tangent Line|vertical tangent line]] ($f$ continuous at $a$ and $\lim_{x \to a} \lvert f'(x) \rvert = \infty$).
> - **[[One-Sided Derivative|Left- and right-hand derivatives]]** (Exercises 62–63): $f'_{-}(a) = \lim_{h \to 0^{-}} \dfrac{f(a + h) - f(a)}{h}$, $f'_{+}(a) = \lim_{h \to 0^{+}} \dfrac{f(a + h) - f(a)}{h}$. $f'(a)$ exists $\iff$ both exist and $f'_{-}(a) = f'_{+}(a)$.
> - **[[Higher Derivatives|Second derivative]]**: $f'' = (f')'$, so $f''(x)$ is the slope of the curve $y = f'(x)$. Then $f''' = (f'')'$ and $f^{(4)} = (f''')'$.
> - **Derivative with $x \to a$** (Equation 2.1.5): $f'(a) = \lim_{x \to a} \dfrac{f(x) - f(a)}{x - a}$.
> - Each answer is written as on an exam paper: the computation first, one $=$ per line, then the conclusion on a Hence line. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 2.2.3
Question: [[CAL1 HW 2.2 Questions#ST 2.2.3|ST 2.2.3]]

> [!solution] Solution
> $$
> \text{(a) II} \qquad \text{(b) IV} \qquad \text{(c) I} \qquad \text{(d) III}
> $$
> $$
> \begin{aligned}
> \text{(a)}\ \ &f \text{ is decreasing, increasing, decreasing} \implies f' \text{ is } -,\ +,\ - \\
> &2 \text{ horizontal tangents} \implies f' = 0 \text{ at } 2 \text{ numbers} \implies \text{II} \\[4pt]
> \text{(b)}\ \ &\text{the graph is } 3 \text{ line segments} \implies f' \text{ is constant on each: } +,\ -,\ + \\
> &2 \text{ corners} \implies f' \text{ does not exist there (open dots)} \implies \text{IV} \\[4pt]
> \text{(c)}\ \ &f \text{ is decreasing for } x < 0,\ \text{increasing for } x > 0 \implies f' < 0,\ \text{then } f' > 0 \\
> &\text{horizontal tangent at } 0 \implies f'(0) = 0;\ \ f \text{ flattens far from } 0 \implies f' \to 0 \implies \text{I} \\[4pt]
> \text{(d)}\ \ &f \text{ is increasing, decreasing, increasing, decreasing} \implies f' \text{ is } +,\ -,\ +,\ - \\
> &3 \text{ horizontal tangents} \implies f' = 0 \text{ at } 3 \text{ numbers} \implies \text{III}
> \end{aligned}
> $$
> ![[CAL1 HW 2.2 Solutions fig 3.png|640]]
>
> \# Read only two things from the graph of $f$: where the tangent is horizontal (there $f'$ crosses the $x$-axis) and where $f$ goes up or down (the sign of $f'$). The height of $f$ does not matter. The fastest way to match is to count the horizontal tangents: 2, 0, 1, 3.

### ST 2.2.19
Question: [[CAL1 HW 2.2 Questions#ST 2.2.19|ST 2.2.19]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(x) &= \lim_{h \to 0} \frac{f(x + h) - f(x)}{h} \\
> &= \lim_{h \to 0} \frac{\left[3(x + h) - 8\right] - \left[3x - 8\right]}{h} \\
> &= \lim_{h \to 0} \frac{3h}{h} \\
> &= \lim_{h \to 0} 3 && (h \ne 0) \\
> &= 3
> \end{aligned}
> $$
> Domain of $f$: $\mathbb{R}$. Domain of $f'$: $\mathbb{R}$.
>
> \# The graph of $f$ is a line with slope $3$, so every tangent line is the line itself and $f'(x) = 3$ for all $x$. The question asks for both domains; do not forget to write them.

### ST 2.2.23
Question: [[CAL1 HW 2.2 Questions#ST 2.2.23|ST 2.2.23]]

> [!solution] Solution
> $$
> \begin{aligned}
> A'(p) &= \lim_{h \to 0} \frac{A(p + h) - A(p)}{h} \\
> &= \lim_{h \to 0} \frac{\left[4(p + h)^3 + 3(p + h)\right] - \left[4p^3 + 3p\right]}{h} \\
> &= \lim_{h \to 0} \frac{4p^3 + 12p^2h + 12ph^2 + 4h^3 + 3p + 3h - 4p^3 - 3p}{h} \\
> &= \lim_{h \to 0} \frac{12p^2h + 12ph^2 + 4h^3 + 3h}{h} \\
> &= \lim_{h \to 0} \left(12p^2 + 12ph + 4h^2 + 3\right) && (h \ne 0) \\
> &= 12p^2 + 3
> \end{aligned}
> $$
> Domain of $A$: $\mathbb{R}$. Domain of $A'$: $\mathbb{R}$.
>
> \# $(p + h)^3 = p^3 + 3p^2h + 3ph^2 + h^3$. The variable of the limit is $h$; $p$ is a constant. Every term without $h$ must cancel before the division by $h$.

### ST 2.2.27
Question: [[CAL1 HW 2.2 Questions#ST 2.2.27|ST 2.2.27]]

> [!solution] Solution
> $$
> \begin{aligned}
> g'(u) &= \lim_{h \to 0} \frac{g(u + h) - g(u)}{h} \\
> &= \lim_{h \to 0} \frac{1}{h}\left[\frac{u + h + 1}{4(u + h) - 1} - \frac{u + 1}{4u - 1}\right] \\
> &= \lim_{h \to 0} \frac{(u + h + 1)(4u - 1) - (u + 1)(4u + 4h - 1)}{h(4u + 4h - 1)(4u - 1)} \\
> &= \lim_{h \to 0} \frac{h(4u - 1) - 4h(u + 1)}{h(4u + 4h - 1)(4u - 1)} \\
> &= \lim_{h \to 0} \frac{-5h}{h(4u + 4h - 1)(4u - 1)} \\
> &= \lim_{h \to 0} \frac{-5}{(4u + 4h - 1)(4u - 1)} && (h \ne 0) \\
> &= -\frac{5}{(4u - 1)^2}
> \end{aligned}
> $$
> Domain of $g$: $\left\{u \mid u \ne \tfrac{1}{4}\right\} = \left(-\infty, \tfrac{1}{4}\right) \cup \left(\tfrac{1}{4}, \infty\right)$. Domain of $g'$: the same set.
>
> \# In the numerator, write $(u + h + 1) = (u + 1) + h$ and $(4u + 4h - 1) = (4u - 1) + 4h$: the product $(u + 1)(4u - 1)$ appears twice and cancels, and only $h(4u - 1) - 4h(u + 1) = -5h$ is left. Leave the denominator factored. $g'$ has the same domain as $g$ because $g$ is not even defined at $\tfrac{1}{4}$.

### ST 2.2.39
Question: [[CAL1 HW 2.2 Questions#ST 2.2.39|ST 2.2.39]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f \text{ is not differentiable at } {-4} \text{ and at } 0. \\
> &{-4}:\ \text{the graph has a corner} \implies \text{no tangent line at } x = -4. \\
> &0:\ f \text{ is not continuous at } 0 \text{ (jump)} \implies f \text{ is not differentiable at } 0.
> \end{aligned}
> $$
> ![[CAL1 HW 2.2 Solutions fig 39.png|440]]
>
> \# Look for the three pictures: corner, discontinuity, vertical tangent. Near $x = 2.3$ the curve is steep but it is still smooth, so it is not on the list. At a corner the slope from the left and the slope from the right are different numbers.

### ST 2.2.41
Question: [[CAL1 HW 2.2 Questions#ST 2.2.41|ST 2.2.41]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f \text{ is not differentiable at } 1 \text{ and at } 5. \\
> &1:\ f \text{ is not continuous at } 1 \text{ (infinite discontinuity)} \implies f \text{ is not differentiable at } 1. \\
> &5:\ \text{the graph has a vertical tangent line at } x = 5.
> \end{aligned}
> $$
> ![[CAL1 HW 2.2 Solutions fig 41.png|440]]
>
> \# At $x = 5$ the function is continuous and the curve is smooth, but the tangent lines become steeper and steeper, $\lim_{x \to 5} \lvert f'(x) \rvert = \infty$, so the slope is not a number. The minimum near $x = 4$ is a horizontal tangent, where $f' = 0$; that is differentiable.

### ST 2.2.45
Question: [[CAL1 HW 2.2 Questions#ST 2.2.45|ST 2.2.45]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{The W-shaped curve is } f': \text{ it is } 0 \text{ exactly where the other curve has horizontal tangents.} \\
> &f'(-1) < 0 && (\text{the graph of } f' \text{ is below the } x\text{-axis at } {-1}) \\
> &f''(1) = \text{the slope of } y = f'(x) \text{ at } x = 1 > 0 && (f' \text{ is increasing at } 1) \\
> &\text{Hence } f''(1) > f'(-1).
> \end{aligned}
> $$
> ![[CAL1 HW 2.2 Solutions fig 45.png|420]]
>
> \# First decide which curve is which, then read a **height** for $f'(-1)$ and a **slope** for $f''(1)$. Only the signs are needed. Check on $f$: at $-1$ the graph of $f$ is going down, so $f'(-1) < 0$.

### ST 2.2.47
Question: [[CAL1 HW 2.2 Questions#ST 2.2.47|ST 2.2.47]]

> [!solution] Solution
> $$
> a = f, \qquad b = f', \qquad c = f''
> $$
> $$
> \begin{aligned}
> &a \text{ is increasing, then has a horizontal tangent, then is decreasing;} \\
> &b \text{ is } +,\ \text{then } 0 \text{ at the same number, then } - \implies b = a'. \\[4pt]
> &b \text{ is increasing, then has a maximum, then is decreasing (until its minimum);} \\
> &c \text{ is } +,\ \text{then } 0 \text{ at the same number, then } - \implies c = b'. \\[4pt]
> &\text{Hence } a = f,\ b = f',\ c = f''.
> \end{aligned}
> $$
> ![[CAL1 HW 2.2 Solutions fig 47.png|440]]
>
> \# The test for "$q$ is the derivative of $p$": wherever $p$ has a horizontal tangent, $q$ must be $0$, and $q$ must be positive where $p$ goes up. To exclude the other orders quickly: $c$ has a minimum where $a$ and $b$ are not $0$, so neither is $c'$, and $c$ must be the last one.

### ST 2.2.55
Question: [[CAL1 HW 2.2 Questions#ST 2.2.55|ST 2.2.55]]

> [!solution] Solution
> **(a)** $x - a = \left(x^{1/3}\right)^3 - \left(a^{1/3}\right)^3 = \left(x^{1/3} - a^{1/3}\right)\left(x^{2/3} + x^{1/3}a^{1/3} + a^{2/3}\right)$.
> $$
> \begin{aligned}
> f'(a) &= \lim_{x \to a} \frac{f(x) - f(a)}{x - a} \\
> &= \lim_{x \to a} \frac{x^{1/3} - a^{1/3}}{\left(x^{1/3} - a^{1/3}\right)\left(x^{2/3} + x^{1/3}a^{1/3} + a^{2/3}\right)} \\
> &= \lim_{x \to a} \frac{1}{x^{2/3} + x^{1/3}a^{1/3} + a^{2/3}} && (x \ne a) \\
> &= \frac{1}{3a^{2/3}} && (a \ne 0)
> \end{aligned}
> $$
> **(b)**
> $$
> \begin{aligned}
> f'(0) &= \lim_{h \to 0} \frac{f(0 + h) - f(0)}{h} \\
> &= \lim_{h \to 0} \frac{h^{1/3} - 0}{h} \\
> &= \lim_{h \to 0} \frac{1}{h^{2/3}} = \infty && (h^{2/3} > 0,\ h^{2/3} \to 0)
> \end{aligned}
> $$
> The limit is not a number. Hence $f'(0)$ does not exist.
>
> **(c)**
> $$
> \begin{aligned}
> &\because f \text{ is continuous at } 0 \text{ (root function), and} \\
> &\phantom{\because}\ \lim_{x \to 0} \lvert f'(x) \rvert = \lim_{x \to 0} \frac{1}{3\lvert x \rvert^{2/3}} = \infty \quad \text{(by (a))} \\
> &\therefore y = \sqrt[3]{x} \text{ has a vertical tangent line at } (0, 0): \text{ the line } x = 0.
> \end{aligned}
> $$
>
> \# (a) uses $A^3 - B^3 = (A - B)(A^2 + AB + B^2)$ with $A = x^{1/3}$, $B = a^{1/3}$: it plays the part that the conjugate plays for square roots. (b) $h^{2/3} = \left(h^{1/3}\right)^2$ is positive for $h$ on both sides of $0$, so the quotient goes to $+\infty$ from both sides. (c) is exactly the definition of a vertical tangent line: continuous at $a$ and $\lvert f'(x) \rvert \to \infty$.

### ST 2.2.57
Question: [[CAL1 HW 2.2 Questions#ST 2.2.57|ST 2.2.57]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(6) &= \lim_{h \to 0} \frac{f(6 + h) - f(6)}{h} = \lim_{h \to 0} \frac{\lvert h \rvert - 0}{h} \\[4pt]
> \lim_{h \to 0^{+}} \frac{\lvert h \rvert}{h} &= \lim_{h \to 0^{+}} \frac{h}{h} = 1 \\
> \lim_{h \to 0^{-}} \frac{\lvert h \rvert}{h} &= \lim_{h \to 0^{-}} \frac{-h}{h} = -1
> \end{aligned}
> $$
> $\because 1 \ne -1$, $\therefore f'(6)$ does not exist. Hence $f$ is not differentiable at $6$.
> $$
> \begin{aligned}
> x > 6:\quad f'(x) &= \lim_{h \to 0} \frac{(x + h - 6) - (x - 6)}{h} = \lim_{h \to 0} \frac{h}{h} = 1 \\
> x < 6:\quad f'(x) &= \lim_{h \to 0} \frac{-(x + h - 6) + (x - 6)}{h} = \lim_{h \to 0} \frac{-h}{h} = -1
> \end{aligned}
> $$
> $$
> f'(x) = \begin{cases} 1 & \text{if } x > 6 \\ -1 & \text{if } x < 6 \end{cases}
> $$
> ![[CAL1 HW 2.2 Solutions fig 57.png|400]]
>
> \# The graph of $\lvert x - 6 \rvert$ is the graph of $\lvert x \rvert$ shifted $6$ to the right, so the corner is at $6$. For $x > 6$, $h$ is taken so small that $x + h > 6$ too, and then $\lvert x + h - 6 \rvert = x + h - 6$; the same for $x < 6$. The graph of $f'$ has open dots at $x = 6$ because $f'(6)$ does not exist.

### ST 2.2.59
Question: [[CAL1 HW 2.2 Questions#ST 2.2.59|ST 2.2.59]]

> [!solution] Solution
> **(a)** $f(x) = x\lvert x \rvert = \begin{cases} x^2 & \text{if } x \ge 0 \\ -x^2 & \text{if } x < 0 \end{cases}$
>
> ![[CAL1 HW 2.2 Solutions fig 59.png|340]]
>
> **(b)**
> $$
> \begin{aligned}
> x > 0:\quad f'(x) &= \lim_{h \to 0} \frac{(x + h)^2 - x^2}{h} = \lim_{h \to 0} (2x + h) = 2x \\
> x < 0:\quad f'(x) &= \lim_{h \to 0} \frac{-(x + h)^2 + x^2}{h} = \lim_{h \to 0} (-2x - h) = -2x \\
> x = 0:\quad f'(0) &= \lim_{h \to 0} \frac{h\lvert h \rvert - 0}{h} = \lim_{h \to 0} \lvert h \rvert = 0
> \end{aligned}
> $$
> Hence $f$ is differentiable for all $x$.
>
> **(c)**
> $$
> f'(x) = \begin{cases} 2x & \text{if } x \ge 0 \\ -2x & \text{if } x < 0 \end{cases} \ = 2\lvert x \rvert
> $$
>
> \# An absolute value does not always make a corner. Here the two parabolas $x^2$ and $-x^2$ both have slope $0$ at the origin, so they join smoothly. The only number that needs the definition at the point itself is $0$, where the formula changes; there $h\lvert h \rvert / h = \lvert h \rvert$.

### ST 2.2.63
Question: [[CAL1 HW 2.2 Questions#ST 2.2.63|ST 2.2.63]]

> [!solution] Solution
> **(a)** $f(4) = \dfrac{1}{5 - 4} = 1$.
> $$
> \begin{aligned}
> f'_{-}(4) &= \lim_{h \to 0^{-}} \frac{f(4 + h) - f(4)}{h} \\
> &= \lim_{h \to 0^{-}} \frac{\left[5 - (4 + h)\right] - 1}{h} && (4 + h < 4) \\
> &= \lim_{h \to 0^{-}} \frac{-h}{h} = -1 \\[6pt]
> f'_{+}(4) &= \lim_{h \to 0^{+}} \frac{f(4 + h) - f(4)}{h} \\
> &= \lim_{h \to 0^{+}} \frac{1}{h}\left[\frac{1}{5 - (4 + h)} - 1\right] && (4 + h > 4) \\
> &= \lim_{h \to 0^{+}} \frac{1}{h} \cdot \frac{1 - (1 - h)}{1 - h} \\
> &= \lim_{h \to 0^{+}} \frac{1}{1 - h} = 1
> \end{aligned}
> $$
> **(b)**
>
> ![[CAL1 HW 2.2 Solutions fig 63.png|460]]
>
> **(c)**
> $$
> \begin{aligned}
> &0:\ \lim_{x \to 0^{-}} f(x) = 0 \ne 5 = \lim_{x \to 0^{+}} f(x) \implies \text{discontinuous at } 0 \text{ (jump)} \\
> &5:\ f(5) \text{ is not defined},\ \lim_{x \to 5^{-}} f(x) = \infty \implies \text{discontinuous at } 5 \text{ (infinite)} \\
> &4:\ \lim_{x \to 4^{-}} f(x) = 1 = \lim_{x \to 4^{+}} f(x) = f(4) \implies \text{continuous at } 4
> \end{aligned}
> $$
> Hence $f$ is discontinuous at $0$ and at $5$.
>
> **(d)**
> $$
> \begin{aligned}
> &0,\ 5:\ f \text{ is not continuous} \implies f \text{ is not differentiable} \\
> &4:\ f'_{-}(4) = -1 \ne 1 = f'_{+}(4) \implies f'(4) \text{ does not exist (corner)}
> \end{aligned}
> $$
> Hence $f$ is not differentiable at $0$, $4$ and $5$.
>
> \# In (a), which formula to use for $f(4 + h)$ depends on the side: $h < 0$ gives the middle piece $5 - x$, $h > 0$ gives $\dfrac{1}{5 - x}$; $f(4)$ itself comes from the last piece ($x \ge 4$). (d) is (c) plus the corner: every discontinuity is on the list at once, and $4$ is added by the one-sided derivatives. $f$ is continuous at $4$ and still not differentiable there.

## ST §2.2 Additional Exercises

> [!note] Note
> These exercises are not assigned. Each one adds a type of problem that the assigned exercises do not cover.
> - 29: the definition with a square root in the denominator: a common denominator, then the conjugate (the types of Examples 3 and 4 in ST §2.2 together).
> - 37: the meaning of $\dfrac{dP}{dt}$ and of $\left.\dfrac{dP}{dt}\right\rvert_{t = 2}$ in words, with units (the part Other Notations).
> - 53: $f''$, $f'''$, $f^{(4)}$ by repeating the definition (the part Higher Derivatives, Examples 6 and 7).
> - 58: not differentiable because not continuous, written out for a formula instead of a graph.
> - 61: a proof about $f'$ for a general $f$, with the substitution $k = -h$.
> - 62: one-sided derivatives in the simplest case, and a case where they are equal, so that $f$ is differentiable at the point where its formula changes.

### ST 2.2.29
Question: [[CAL1 HW 2.2 Questions#ST 2.2.29|ST 2.2.29]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(x) &= \lim_{h \to 0} \frac{f(x + h) - f(x)}{h} \\
> &= \lim_{h \to 0} \frac{1}{h}\left[\frac{1}{\sqrt{1 + x + h}} - \frac{1}{\sqrt{1 + x}}\right] \\
> &= \lim_{h \to 0} \frac{\sqrt{1 + x} - \sqrt{1 + x + h}}{h\sqrt{1 + x + h}\sqrt{1 + x}} \\
> &= \lim_{h \to 0} \frac{\sqrt{1 + x} - \sqrt{1 + x + h}}{h\sqrt{1 + x + h}\sqrt{1 + x}} \cdot \frac{\sqrt{1 + x} + \sqrt{1 + x + h}}{\sqrt{1 + x} + \sqrt{1 + x + h}} \\
> &= \lim_{h \to 0} \frac{(1 + x) - (1 + x + h)}{h\sqrt{1 + x + h}\sqrt{1 + x}\left(\sqrt{1 + x} + \sqrt{1 + x + h}\right)} \\
> &= \lim_{h \to 0} \frac{-1}{\sqrt{1 + x + h}\sqrt{1 + x}\left(\sqrt{1 + x} + \sqrt{1 + x + h}\right)} && (h \ne 0) \\
> &= \frac{-1}{\sqrt{1 + x}\sqrt{1 + x} \cdot 2\sqrt{1 + x}} = -\frac{1}{2(1 + x)^{3/2}}
> \end{aligned}
> $$
> Domain of $f$: $1 + x > 0$, that is, $(-1, \infty)$. Domain of $f'$: $(-1, \infty)$.
>
> \# Two tools in a fixed order: the common denominator first, then the conjugate of the numerator. Here the two domains are equal, because $f$ already needs $1 + x > 0$. Compare $\sqrt{x}$ in Example 3: its domain is $[0, \infty)$ and the domain of its derivative is $(0, \infty)$.

### ST 2.2.37
Question: [[CAL1 HW 2.2 Questions#ST 2.2.37|ST 2.2.37]]

> [!solution] Solution
> **(a)** $\dfrac{dP}{dt}$ is the rate at which the percentage of the city's electrical power produced by solar panels changes with respect to time, in percentage points per year.
>
> **(b)** $2$ years after January 1, 2020 (on January 1, 2022), the percentage of the city's electrical power produced by solar panels is increasing at a rate of $3.5$ percentage points per year.
>
> \# $\left.\dfrac{dP}{dt}\right\rvert_{t = 2}$ is another way to write $P'(2)$; the bar means "evaluate at". An interpretation is one full sentence: when, which quantity, increasing or decreasing, at what rate, with units (units of $P$ per unit of $t$).

### ST 2.2.53
Question: [[CAL1 HW 2.2 Questions#ST 2.2.53|ST 2.2.53]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(x) &= \lim_{h \to 0} \frac{\left[2(x + h)^2 - (x + h)^3\right] - \left[2x^2 - x^3\right]}{h} \\
> &= \lim_{h \to 0} \frac{4xh + 2h^2 - 3x^2h - 3xh^2 - h^3}{h} \\
> &= \lim_{h \to 0} \left(4x + 2h - 3x^2 - 3xh - h^2\right) = 4x - 3x^2 \\[6pt]
> f''(x) &= \lim_{h \to 0} \frac{\left[4(x + h) - 3(x + h)^2\right] - \left[4x - 3x^2\right]}{h} \\
> &= \lim_{h \to 0} \frac{4h - 6xh - 3h^2}{h} = \lim_{h \to 0} (4 - 6x - 3h) = 4 - 6x \\[6pt]
> f'''(x) &= \lim_{h \to 0} \frac{\left[4 - 6(x + h)\right] - \left[4 - 6x\right]}{h} = \lim_{h \to 0} \frac{-6h}{h} = -6 \\[6pt]
> f^{(4)}(x) &= \lim_{h \to 0} \frac{(-6) - (-6)}{h} = \lim_{h \to 0} 0 = 0
> \end{aligned}
> $$
> The graphs are consistent: each graph is positive where the one before it is increasing, negative where it is decreasing, and $0$ where it has a horizontal tangent.
>
> \# Each derivative is the derivative of the one before it, so the same definition is used four times. From $f''$ on there is a shortcut: $y = 4 - 6x$ is a line with slope $-6$, so $f'''(x) = -6$; a constant function has slope $0$, so $f^{(4)}(x) = 0$. Example of the check: $f''(x) = 4 - 6x = 0$ at $x = \tfrac{2}{3}$, which is where the parabola $f'$ has its maximum.

### ST 2.2.58
Question: [[CAL1 HW 2.2 Questions#ST 2.2.58|ST 2.2.58]]

> [!solution] Solution
> $$
> \begin{aligned}
> &n \text{ an integer}:\ \lim_{x \to n^{-}} [\![ x ]\!] = n - 1 \ne n = \lim_{x \to n^{+}} [\![ x ]\!] \\
> &\implies f \text{ is not continuous at } n \implies f \text{ is not differentiable at } n. \\[4pt]
> &x \text{ not an integer},\ n < x < n + 1:\ f = n \text{ near } x \\
> &\implies f'(x) = \lim_{h \to 0} \frac{n - n}{h} = 0.
> \end{aligned}
> $$
> Hence $f$ is not differentiable at the integers, and $f'(x) = 0$ if $x$ is not an integer.
>
> ![[CAL1 HW 2.2 Solutions fig 58.png|400]]
>
> \# The graph of $[\![ x ]\!]$ is a staircase: flat pieces (slope $0$) with a jump at every integer. The graph of $f'$ is the $x$-axis with an open dot at every integer. Not continuous $\implies$ not differentiable is the fastest reason; no difference quotient is needed at $n$.

### ST 2.2.61
Question: [[CAL1 HW 2.2 Questions#ST 2.2.61|ST 2.2.61]]

> [!proof] Proof
> Let $f$ be differentiable at $x$.
>
> **(a)** $f$ even: $f(-x + h) = f(-(x - h)) = f(x - h)$ and $f(-x) = f(x)$.
> $$
> \begin{aligned}
> f'(-x) &= \lim_{h \to 0} \frac{f(-x + h) - f(-x)}{h} \\
> &= \lim_{h \to 0} \frac{f(x - h) - f(x)}{h} \\
> &= \lim_{k \to 0} \frac{f(x + k) - f(x)}{-k} && (k = -h;\ h \to 0 \iff k \to 0) \\
> &= -\lim_{k \to 0} \frac{f(x + k) - f(x)}{k} \\
> &= -f'(x)
> \end{aligned}
> $$
> Hence $f'$ is odd.
>
> **(b)** $f$ odd: $f(-x + h) = -f(x - h)$ and $f(-x) = -f(x)$.
> $$
> \begin{aligned}
> f'(-x) &= \lim_{h \to 0} \frac{f(-x + h) - f(-x)}{h} \\
> &= \lim_{h \to 0} \frac{-f(x - h) + f(x)}{h} \\
> &= \lim_{k \to 0} \frac{-f(x + k) + f(x)}{-k} && (k = -h) \\
> &= \lim_{k \to 0} \frac{f(x + k) - f(x)}{k} \\
> &= f'(x)
> \end{aligned}
> $$
> Hence $f'$ is even. $\blacksquare$
>
> \# Start from the definition of $f'$ at the number $-x$, use the symmetry of $f$ to move the minus sign inside, and rename $-h$ as $k$ so that the definition of $f'(x)$ appears. Picture: an even graph is a mirror image in the $y$-axis, so the slopes at $x$ and $-x$ are opposite. Examples from this section: $x^2$ is even and $2x$ is odd; $x^3 - x$ is odd and $3x^2 - 1$ is even.

### ST 2.2.62
Question: [[CAL1 HW 2.2 Questions#ST 2.2.62|ST 2.2.62]]

> [!solution] Solution
> **(a)** $f(0) = 0$.
> $$
> \begin{aligned}
> f'_{-}(0) &= \lim_{h \to 0^{-}} \frac{f(h) - f(0)}{h} = \lim_{h \to 0^{-}} \frac{0 - 0}{h} = 0 \\
> f'_{+}(0) &= \lim_{h \to 0^{+}} \frac{f(h) - f(0)}{h} = \lim_{h \to 0^{+}} \frac{h - 0}{h} = 1
> \end{aligned}
> $$
> $\because f'_{-}(0) \ne f'_{+}(0)$, $\therefore f$ is not differentiable at $0$.
>
> **(b)** $f(0) = 0$.
> $$
> \begin{aligned}
> f'_{-}(0) &= \lim_{h \to 0^{-}} \frac{0 - 0}{h} = 0 \\
> f'_{+}(0) &= \lim_{h \to 0^{+}} \frac{h^2 - 0}{h} = \lim_{h \to 0^{+}} h = 0
> \end{aligned}
> $$
> $\because f'_{-}(0) = f'_{+}(0) = 0$, $\therefore f$ is differentiable at $0$ and $f'(0) = 0$.
>
> \# $h < 0$ uses the piece for $x \le 0$ and $h > 0$ uses the piece for $x > 0$. Both functions are continuous at $0$; (a) has a corner there, and in (b) the parabola leaves the origin with slope $0$, the same slope as the flat piece, so there is no corner. Compare [[#ST 2.2.63]], where the two one-sided derivatives at $4$ are $-1$ and $1$.
