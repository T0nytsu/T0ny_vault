---
course: [CAL1]
chapter: ["1.5", "1.6", "1.7", "1.8", "2.1", "2.2"]
tags: [calculus, exam, limits, continuity, derivatives]
source:
  - "CAL1 Mid-term Exam 1 (115-1), 2026-10-07, graded scan; the figure in Q2 (b) is redrawn"
  - "[[CAL1 Midterm 1 p1.jpg]]"
  - "[[CAL1 Midterm 1 p2.jpg]]"
  - "[[CAL1 Midterm 1 p3.jpg]]"
  - "[[CAL1 Midterm 1 p4.jpg]]"
  - "[[CAL1 Midterm 1 p5.jpg]]"
  - "[[CAL1 Midterm 1 p6.jpg]]"
  - "[[CAL1 Midterm 1 p7.jpg]]"
  - "[[CAL1 Midterm 1 p8.jpg]]"
created: 2026-10-12
score: "97/100"
---
> [!abstract] Result: 97/100
> - Q1 True or False: 10/10.
> - Q2 Single or multiple choice: 40/40.
> - Q3 Evaluate a limit: 10/10.
> - Q4 A limit with a parameter: 10/10.
> - Q5 Does $f'(0)$ exist: 9/10. The bound $-1 \le \sin\frac{1}{h} \le 1$ was written without "for $h \ne 0$".
> - Q6 Differentiable implies continuous: 10/10.
> - Q7 The Squeeze Theorem: 8/10. $\delta = \min\{\delta_1, \delta_2\}$ does not keep $x$ in the interval where $f(x) \le g(x) \le h(x)$ holds; a third $\delta_3$ is needed.

> [!info] Coverage
> Sections 1.5–1.8 and 2.1–2.2 of Stewart, *Calculus*: [[Limit of a Function|limits]], [[Limit Laws|the limit laws]], [[Precise Definition of a Limit|the precise definition of a limit]], [[Continuity|continuity]], and [[Derivative|derivatives]].
> - Part I. True/False questions ($5 \times 2 = 10$ points).
> - Part II. Single/multiple choice questions ($8 \times 5 = 40$ points).
> - Part III. Computational and proof questions ($5 \times 10 = 50$ points). Show all your work.

## Q1 True or False

> [!question]
> Respond with true (T) or false (F) to each of the following statements.
> - (a) (2 points) If $f$ is continuous at $x = a$, then $f$ is differentiable at $x = a$.
> - (b) (2 points) If $\lim_{x \to a} f(x)$ and $\lim_{x \to a} g(x)$ both exist, then $\displaystyle\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{\lim_{x \to a} f(x)}{\lim_{x \to a} g(x)}$.
> - (c) (2 points) The equation $-x^3 + 4x + 1 = 0$ has at least one solution in the interval $(-1, 0)$.
> - (d) (2 points) The line $x = 5$ is a vertical asymptote of the curve $y = \dfrac{x+1}{x-5}$.
> - (e) (2 points) The limit $\lim_{x \to a}[f(x) \cdot g(x)]$ may exist even though neither $\lim_{x \to a} f(x)$ nor $\lim_{x \to a} g(x)$ exists.

> [!attempt] My answer: 10/10
> - (a) F
> - (b) F
> - (c) T
> - (d) T
> - (e) T

> [!solution]- Solution
> - (a) **F.** $f(x) = \lvert x \rvert$ is continuous at $x = 0$, but $\lim_{h \to 0^-} \frac{\lvert h \rvert}{h} = -1 \ne 1 = \lim_{h \to 0^+} \frac{\lvert h \rvert}{h}$, so $f'(0)$ does not exist.
> - (b) **F.** $f(x) = g(x) = x$, $a = 0$: both limits exist (both are $0$) and $\lim_{x \to 0} \frac{x}{x} = 1$, but $\frac{0}{0}$ is undefined.
> - (c) **T.** $p(x) = -x^3 + 4x + 1$ is a polynomial, so it is continuous on $[-1, 0]$, and $p(-1) = 1 - 4 + 1 = -2 < 0 < 1 = p(0)$. By the [[Intermediate Value Theorem]], $p(c) = 0$ for some $c \in (-1, 0)$.
> - (d) **T.** $\lim_{x \to 5^+} \frac{x+1}{x-5} = \infty$, since $x + 1 \to 6 > 0$ and $x - 5 \to 0^+$.
> - (e) **T.** $f(x) = g(x) = \frac{\lvert x \rvert}{x}$, $a = 0$: $f(x)g(x) = 1$ for $x \ne 0$, so $\lim_{x \to 0} f(x)g(x) = 1$, while $\lim_{x \to 0^-} f(x) = -1 \ne 1 = \lim_{x \to 0^+} f(x)$.

## Q2 Single or Multiple Choice

> [!question]
> Write the letter(s) of *all* correct choices in the blank. A problem may have more than one correct choice; full credit requires exactly the correct set.

### Q2 (a)

> [!question]
> (5 points) Let $f(x) = \dfrac{x-3}{x^2-9}$. Which of the following statements are true?
> - A. $f$ has a removable discontinuity at $x = 3$.
> - B. $f$ has a removable discontinuity at $x = -3$.
> - C. $f$ has an infinite discontinuity at $x = -3$.
> - D. $f$ is continuous on the interval $(-3, \infty)$.

> [!attempt] My answer: 5/5
> A.C

> [!solution]- Solution
> **A, C.** $f(x) = \frac{x-3}{(x-3)(x+3)} = \frac{1}{x+3}$ for $x \ne \pm 3$.
> - A. $\lim_{x \to 3} f(x) = \frac{1}{6}$ exists, but $f(3)$ is undefined.
> - B, C. $\lim_{x \to -3^+} f(x) = \infty$: the discontinuity at $-3$ is infinite, not removable.
> - D fails: $3 \in (-3, \infty)$ and $f(3)$ is undefined.

### Q2 (b)

> [!question]
> (5 points) The figure shows the graphs of $f$, $f'$, and $f''$. Which choice correctly identifies the curves?
>
> ![[CAL1 Midterm 1 fig 2b.png|420]]
>
> - A. $f = c,\ f' = b,\ f'' = a$
> - B. $f = a,\ f' = b,\ f'' = c$
> - C. $f = b,\ f' = a,\ f'' = c$
> - D. $f = a,\ f' = c,\ f'' = b$

> [!attempt] My answer: 5/5
> B

> [!solution]- Solution
> **B.** $b > 0$ exactly where $a$ increases, and $b$ crosses the $x$-axis where $a$ is highest, so $b = a'$. Likewise $c > 0$ where $b$ increases, and $c = 0$ at the peak of $b$, so $c = b'$. Hence $f = a$, $f' = b$, $f'' = c$.
> - A fails: $c$ decreases near $x = 0$, where $b > 0$.
> - C fails: $b$ decreases to the right of its peak, where $a > 0$.
> - D fails: $a$ increases near $x = 0$, where $c < 0$.

### Q2 (c)

> [!question]
> (5 points) Consider an $n$-th degree polynomial
> $$
> p_n(x) = a_n x^n + a_{n-1} x^{n-1} + \cdots + a_1 x + a_0, \qquad n \ge 1,\ a_n \ne 0.
> $$
> Here $p_n^{(k)}$ denotes the $k$-th derivative of $p_n$, i.e., $p_n$ differentiated $k$ times. Which of the following statements are true?
> - A. $p_n^{(n-1)}(x)$ is a constant function.
> - B. The domain of $p_n(x)$ is the whole real line $(-\infty, \infty)$.
> - C. $p_n^{(n)}(x) = 0$ for all $x$.
> - D. $p_n^{(n+1)}(x) = 0$ for all $x$.

> [!attempt] My answer: 5/5
> B.D

> [!solution]- Solution
> **B, D.** Each derivative lowers the degree by one:
> $$
> p_n^{(n-1)}(x) = n!\,a_n x + (n-1)!\,a_{n-1}, \qquad p_n^{(n)}(x) = n!\,a_n, \qquad p_n^{(n+1)}(x) = 0.
> $$
> - A fails: $p_n^{(n-1)}$ is a line with slope $n!\,a_n \ne 0$.
> - B. A polynomial is defined for every real $x$.
> - C fails: $p_n^{(n)}(x) = n!\,a_n \ne 0$.
> - D. The derivative of the constant $n!\,a_n$ is $0$.

### Q2 (d)

> [!question]
> (5 points) An equation of the tangent line to the curve $y = f(x)$ at the point where $x = 2$ is $y = 4x - 5$. Which of the following statements are true?
> - A. $f(2) = -5$.
> - B. $f'(x) = 4$ for all $x$.
> - C. $f(2) = 3$.
> - D. $f'(2) = 4$.

> [!attempt] My answer: 5/5
> C.D

> [!solution]- Solution
> **C, D.** The tangent line at $x = 2$ is $y = f(2) + f'(2)(x - 2)$: it passes through $(2, f(2))$ and has slope $f'(2)$.
> - C. $f(2) = 4 \cdot 2 - 5 = 3$; so A fails ($-5$ is the $y$-intercept of the line).
> - D. $f'(2) = 4$; the line says nothing about $f'(x)$ for $x \ne 2$, so B fails.

### Q2 (e)

> [!question]
> (5 points) The limit
> $$
> \lim_{h \to 0} \frac{\sqrt{9+h} - 3}{h}
> $$
> represents the derivative $f'(a)$ of some function $f$ at some number $a$. Which of the following choices of $f$ and $a$ are correct?
> - A. $f(x) = \sqrt{x},\ a = 9$
> - B. $f(x) = \sqrt{9+x},\ a = 0$
> - C. $f(x) = \sqrt{x},\ a = 3$
> - D. $f(x) = \sqrt{9+x} - 3,\ a = 0$

> [!attempt] My answer: 5/5
> A.B.D

> [!solution]- Solution
> **A, B, D.** $f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$, so we need $f(a+h) - f(a) = \sqrt{9+h} - 3$.
> - A. $\sqrt{9+h} - \sqrt{9} = \sqrt{9+h} - 3$.
> - B. $\sqrt{9+(0+h)} - \sqrt{9+0} = \sqrt{9+h} - 3$.
> - C fails: $\sqrt{3+h} - \sqrt{3}$.
> - D. $(\sqrt{9+h} - 3) - (\sqrt{9} - 3) = \sqrt{9+h} - 3$.

### Q2 (f)

> [!question]
> (5 points) Let $[\![x]\!]$ denote the greatest integer function, i.e., the largest integer that is less than or equal to $x$, and let $n$ be an integer. Which of the following statements are true?
> - A. $\lim_{x \to n^-} [\![x]\!] = n$.
> - B. $\lim_{x \to n^+} [\![x]\!] = n$.
> - C. $\lim_{x \to n} [\![x]\!]$ does not exist.
> - D. $\lim_{x \to n^-} [\![x]\!] = n - 1$.

> [!attempt] My answer: 5/5
> B.C.D

> [!solution]- Solution
> **B, C, D.** For $n - 1 \le x < n$, $[\![x]\!] = n - 1$; for $n \le x < n + 1$, $[\![x]\!] = n$. So
> $$
> \lim_{x \to n^-} [\![x]\!] = n - 1 \ne n = \lim_{x \to n^+} [\![x]\!],
> $$
> and $\lim_{x \to n} [\![x]\!]$ does not exist.

### Q2 (g)

> [!question]
> (5 points) Consider the limit $\displaystyle\lim_{h \to 0} \frac{\sin h}{h}$. Which of the following statements are true?
> - A. $\displaystyle\lim_{h \to 0} \frac{\sin h}{h} = 1$.
> - B. The limit does not exist, because it has the form $\tfrac{0}{0}$.
> - C. The limit equals $f'(0)$ for $f(x) = \sin x$.
> - D. The function $\dfrac{\sin h}{h}$ has a removable discontinuity at $h = 0$.

> [!attempt] My answer: 5/5
> A.C.D

> [!solution]- Solution
> **A, C, D.**
> - A. A standard trigonometric limit.
> - B fails: the form $\tfrac{0}{0}$ only says that direct substitution does not work.
> - C. $f'(0) = \lim_{h \to 0} \frac{\sin(0+h) - \sin 0}{h} = \lim_{h \to 0} \frac{\sin h}{h}$.
> - D. $\frac{\sin h}{h}$ is undefined at $h = 0$, but its limit there exists ($= 1$).

### Q2 (h)

> [!question]
> (5 points) Suppose that $\lim_{x \to a} f(x) = f(a)$. Which of the following statements are true?
> - A. The limit of $f(x)$ as $x \to a$ can be evaluated by direct substitution.
> - B. $f$ is continuous at $x = a$.
> - C. $f(a)$ is defined and $\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x) = f(a)$.
> - D. $f$ is differentiable at $x = a$.

> [!attempt] My answer: 5/5
> A.B.C

> [!solution]- Solution
> **A, B, C.**
> - B. $\lim_{x \to a} f(x) = f(a)$ is the definition of continuity at $a$.
> - A. The limit equals the value at $a$, which is what direct substitution means.
> - C. A limit equals $f(a)$ exactly when both one-sided limits equal $f(a)$.
> - D fails: $\lvert x \rvert$ is continuous at $0$ but not differentiable there (Q1 (a)).

## Q3 Evaluate a Limit

> [!question]
> (10 points) Evaluate the limit, if it exists:
> $$
> \lim_{t \to 0} \left( \frac{1}{t\sqrt{1+t}} - \frac{1}{t} \right).
> $$

> [!attempt] My answer: 10/10
> $$
> \begin{aligned}
> &\lim_{t \to 0} \left( \frac{1}{t\sqrt{1+t}} - \frac{1}{t} \right) \\
> &\quad = \lim_{t \to 0} \left( \frac{1 - \sqrt{1+t}}{t\sqrt{1+t}} \right) \\
> &\quad = \lim_{t \to 0} \left( \frac{1 - \sqrt{1+t}}{t\sqrt{1+t}} \cdot \frac{1 + \sqrt{1+t}}{1 + \sqrt{1+t}} \right) \\
> &\quad = \lim_{t \to 0} \left[ \frac{1 - (1+t)}{t\sqrt{1+t}\,(1 + \sqrt{1+t})} \right] \\
> &\quad = \lim_{t \to 0} \left[ \frac{-t}{t\sqrt{1+t}\,(1 + \sqrt{1+t})} \right] \\
> &\quad = \lim_{t \to 0} \left[ \frac{-1}{\sqrt{1+t}\,(1 + \sqrt{1+t})} \right] && (t \ne 0) \\
> &\quad = \frac{\lim\limits_{t \to 0}(-1)}{\lim\limits_{t \to 0} \left[ \sqrt{1+t}\,(1 + \sqrt{1+t}) \right]} && \text{(by Quotient Law)} \\
> &\quad = \frac{\lim\limits_{t \to 0}(-1)}{\lim\limits_{t \to 0} \sqrt{1+t} \cdot \lim\limits_{t \to 0}(1 + \sqrt{1+t})} && \text{(by Product Law)} \\
> &\quad = \frac{\lim\limits_{t \to 0}(-1)}{\lim\limits_{t \to 0} \sqrt{1+t} \cdot \left( \lim\limits_{t \to 0} 1 + \lim\limits_{t \to 0} \sqrt{1+t} \right)} && \text{(by Sum Law)} \\
> &\quad = \frac{\lim\limits_{t \to 0}(-1)}{\sqrt{\lim\limits_{t \to 0}(1+t)} \cdot \left( \lim\limits_{t \to 0} 1 + \sqrt{\lim\limits_{t \to 0}(1+t)} \right)} && \text{(by Root Law)} \\
> &\quad = \frac{\lim\limits_{t \to 0}(-1)}{\sqrt{\lim\limits_{t \to 0} 1 + \lim\limits_{t \to 0} t} \cdot \left( \lim\limits_{t \to 0} 1 + \sqrt{\lim\limits_{t \to 0} 1 + \lim\limits_{t \to 0} t} \right)} && \text{(by Sum Law)} \\
> &\quad = \frac{-1}{\sqrt{1+0} \cdot (1 + \sqrt{1+0})} = \frac{-1}{1 \cdot 2} = -\frac{1}{2}
> \end{aligned}
> $$
> Hence $\lim_{t \to 0} \left( \frac{1}{t\sqrt{1+t}} - \frac{1}{t} \right) = -\frac{1}{2}$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &\lim_{t \to 0} \left( \frac{1}{t\sqrt{1+t}} - \frac{1}{t} \right) \\
> &\quad = \lim_{t \to 0} \frac{1 - \sqrt{1+t}}{t\sqrt{1+t}} \\
> &\quad = \lim_{t \to 0} \left( \frac{1 - \sqrt{1+t}}{t\sqrt{1+t}} \cdot \frac{1 + \sqrt{1+t}}{1 + \sqrt{1+t}} \right) \\
> &\quad = \lim_{t \to 0} \frac{1 - (1+t)}{t\sqrt{1+t}\,(1 + \sqrt{1+t})} \\
> &\quad = \lim_{t \to 0} \frac{-t}{t\sqrt{1+t}\,(1 + \sqrt{1+t})} \\
> &\quad = \lim_{t \to 0} \frac{-1}{\sqrt{1+t}\,(1 + \sqrt{1+t})} && (t \ne 0) \\
> &\quad = \frac{\lim\limits_{t \to 0}(-1)}{\lim\limits_{t \to 0} \left[ \sqrt{1+t}\,(1 + \sqrt{1+t}) \right]} && \text{(by Quotient Law)} \\
> &\quad = \frac{\lim\limits_{t \to 0}(-1)}{\lim\limits_{t \to 0} \sqrt{1+t} \cdot \lim\limits_{t \to 0}(1 + \sqrt{1+t})} && \text{(by Product Law)} \\
> &\quad = \frac{\lim\limits_{t \to 0}(-1)}{\lim\limits_{t \to 0} \sqrt{1+t} \cdot \left( \lim\limits_{t \to 0} 1 + \lim\limits_{t \to 0} \sqrt{1+t} \right)} && \text{(by Sum Law)} \\
> &\quad = \frac{\lim\limits_{t \to 0}(-1)}{\sqrt{\lim\limits_{t \to 0}(1+t)} \cdot \left( \lim\limits_{t \to 0} 1 + \sqrt{\lim\limits_{t \to 0}(1+t)} \right)} && \text{(by Root Law)} \\
> &\quad = \frac{\lim\limits_{t \to 0}(-1)}{\sqrt{\lim\limits_{t \to 0} 1 + \lim\limits_{t \to 0} t} \cdot \left( \lim\limits_{t \to 0} 1 + \sqrt{\lim\limits_{t \to 0} 1 + \lim\limits_{t \to 0} t} \right)} && \text{(by Sum Law)} \\
> &\quad = \frac{-1}{\sqrt{1+0} \cdot (1 + \sqrt{1+0})} = \frac{-1}{1 \cdot 2} = -\frac{1}{2} && (\lim\limits_{t \to 0} c = c,\ \lim\limits_{t \to 0} t = 0)
> \end{aligned}
> $$
> Hence $\lim_{t \to 0} \left( \frac{1}{t\sqrt{1+t}} - \frac{1}{t} \right) = -\frac{1}{2}$.

## Q4 A Limit with a Parameter

> [!question]
> (10 points) Is there a number $a$ such that
> $$
> \lim_{x \to -2} \frac{3x^2 + ax + a + 3}{x^2 + x - 2}
> $$
> exists? If so, find the value of $a$ and the value of the limit.

> [!attempt] My answer: 10/10
> $$
> \begin{aligned}
> &\text{Since } \lim_{x \to -2}(x^2 + x - 2) = 0 \text{ and } \lim_{x \to -2} \frac{3x^2 + ax + a + 3}{x^2 + x - 2} \text{ exist,} \\
> &\lim_{x \to -2}(3x^2 + ax + a + 3) = 0 \\
> &\because 3x^2 + ax + a + 3 \text{ is a polynominal} \\
> &\therefore \lim_{x \to -2}(3x^2 + ax + a + 3) = 3(-2)^2 + a(-2) + a + 3 = 0 \implies a = 15
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\lim_{x \to -2} \frac{3x^2 + ax + a + 3}{x^2 + x - 2} \\
> &\quad = \lim_{x \to -2} \frac{3x^2 + 15x + 18}{x^2 + x - 2} \\
> &\quad = \lim_{x \to -2} \frac{3(x+2)(x+3)}{(x+2)(x-1)} \\
> &\quad = \lim_{x \to -2} \frac{3(x+3)}{x-1} && (x + 2 = x - (-2) \ne 0) \\
> &\quad = \frac{\lim\limits_{x \to -2} [3(x+3)]}{\lim\limits_{x \to -2}(x-1)} && \text{(by Quotient Law)} \\
> &\quad = \frac{3 \lim\limits_{x \to -2}(x+3)}{\lim\limits_{x \to -2}(x-1)} && \text{(by Constant Multiple Law)} \\
> &\quad = \frac{3 \left( \lim\limits_{x \to -2} x + \lim\limits_{x \to -2} 3 \right)}{\lim\limits_{x \to -2} x + \lim\limits_{x \to -2}(-1)} && \text{(by Sum Law)} \\
> &\quad = \frac{3(-2+3)}{-2-1} \\
> &\quad = -1
> \end{aligned}
> $$
> Hence $a = 15$ and $\lim_{x \to -2} \frac{3x^2 + ax + a + 3}{x^2 + x - 2} = -1$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &\text{Since } \lim_{x \to -2}(x^2 + x - 2) = 0 \text{ and } \lim_{x \to -2} \frac{3x^2 + ax + a + 3}{x^2 + x - 2} \text{ exists,} \\
> &\lim_{x \to -2}(3x^2 + ax + a + 3) = 0. \\
> &\because 3x^2 + ax + a + 3 \text{ is a polynomial,} \\
> &\therefore \lim_{x \to -2}(3x^2 + ax + a + 3) = 3(-2)^2 + a(-2) + a + 3 = 15 - a = 0 \\
> &\implies a = 15.
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\lim_{x \to -2} \frac{3x^2 + 15x + 18}{x^2 + x - 2} \\
> &\quad = \lim_{x \to -2} \frac{3(x+2)(x+3)}{(x+2)(x-1)} \\
> &\quad = \lim_{x \to -2} \frac{3(x+3)}{x-1} && (x + 2 \ne 0) \\
> &\quad = \frac{\lim\limits_{x \to -2} [3(x+3)]}{\lim\limits_{x \to -2}(x-1)} && \text{(by Quotient Law)} \\
> &\quad = \frac{3 \lim\limits_{x \to -2}(x+3)}{\lim\limits_{x \to -2}(x-1)} && \text{(by Constant Multiple Law)} \\
> &\quad = \frac{3 \left( \lim\limits_{x \to -2} x + \lim\limits_{x \to -2} 3 \right)}{\lim\limits_{x \to -2} x + \lim\limits_{x \to -2}(-1)} && \text{(by Sum Law)} \\
> &\quad = \frac{3(-2+3)}{-2-1} = -1 && (\lim\limits_{x \to -2} x = -2,\ \lim\limits_{x \to -2} c = c)
> \end{aligned}
> $$
> Hence $a = 15$ and $\lim_{x \to -2} \frac{3x^2 + ax + a + 3}{x^2 + x - 2} = -1$.
>
> \# Why the numerator must tend to $0$: for $x \ne -2$, the numerator equals $\frac{3x^2 + ax + a + 3}{x^2 + x - 2} \cdot (x^2 + x - 2)$, so by the Product Law its limit is $(\text{the limit}) \cdot 0 = 0$, the same trick as in Q6. For $a \ne 15$ the numerator tends to $15 - a \ne 0$ while the denominator tends to $0$, so $a = 15$ is the only value.

## Q5 Does the Derivative Exist at 0

> [!question]
> (10 points) Determine whether $f'(0)$ exists, where
> $$
> f(x) = \begin{cases} x^2 \sin \dfrac{1}{x} & \text{if } x \ne 0 \\ 0 & \text{if } x = 0. \end{cases}
> $$
> Justify your answer.

> [!attempt] My answer: 9/10
> $$
> \begin{aligned}
> f(0) &= 0 \\
> f'(0) &= \lim_{h \to 0} \frac{f(h+0) - f(0)}{h} \\
> &= \lim_{h \to 0} \frac{h^2 \sin\frac{1}{h} - 0}{h} \\
> &= \lim_{h \to 0} \frac{h^2 \sin\frac{1}{h}}{h} && (h \ne 0) \\
> &= \lim_{h \to 0} \left( h \cdot \sin\frac{1}{h} \right)
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &{-1} \le \sin\frac{1}{h} \le 1 \implies -\lvert h \rvert \le \lvert h \rvert \sin\frac{1}{h} \le \lvert h \rvert \quad \text{✗} \\
> &\hphantom{{-1} \le \sin\frac{1}{h} \le 1} \implies -\lvert h \rvert \le h \sin\frac{1}{h} \le \lvert h \rvert \\[6pt]
> &\because \lim_{h \to 0}(-\lvert h \rvert) = 0,\ \lim_{h \to 0} \lvert h \rvert = 0 \text{ and } {-\lvert h \rvert} \le h \sin\frac{1}{h} \le \lvert h \rvert \\
> &\therefore \lim_{h \to 0} \left( h \cdot \sin\frac{1}{h} \right) = 0 \text{ by The Squeeze Theorem.} \\[6pt]
> &\text{Since } \lim_{h \to 0} \left( h \cdot \sin\frac{1}{h} \right) \text{ exists, } f'(0) \text{ exists.}
> \end{aligned}
> $$

> [!failure] Mistake: the bound on the sine needs h ≠ 0
> $\sin\frac{1}{h}$ is defined only for $h \ne 0$, so $-1 \le \sin\frac{1}{h} \le 1$, and the squeeze inequality that follows from it, hold only for $h \ne 0$. The grader inserted "for $h \ne 0$" after $-1 \le \sin\frac{1}{h} \le 1$ (−1). This is all the [[Squeeze Theorem]] needs: the inequality near $0$, except possibly at $0$.

> [!solution]- Solution
> $$
> \begin{aligned}
> f(0) &= 0 \\
> f'(0) &= \lim_{h \to 0} \frac{f(h+0) - f(0)}{h} \\
> &= \lim_{h \to 0} \frac{h^2 \sin\frac{1}{h} - 0}{h} \\
> &= \lim_{h \to 0} \frac{h^2 \sin\frac{1}{h}}{h} \\
> &= \lim_{h \to 0} \left( h \cdot \sin\frac{1}{h} \right) && (h \ne 0)
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &{-1} \le \sin\frac{1}{h} \le 1 \text{ for } h \ne 0 \\
> &\implies -\lvert h \rvert \le \lvert h \rvert \sin\frac{1}{h} \le \lvert h \rvert && (\lvert h \rvert > 0) \\
> &\implies -\lvert h \rvert \le h \sin\frac{1}{h} \le \lvert h \rvert && (h = \pm\lvert h \rvert) \\[6pt]
> &\because \lim_{h \to 0}(-\lvert h \rvert) = 0,\ \lim_{h \to 0} \lvert h \rvert = 0 \\
> &\quad \text{and } {-\lvert h \rvert} \le h \sin\frac{1}{h} \le \lvert h \rvert \text{ for } h \ne 0 \\
> &\therefore \lim_{h \to 0} \left( h \cdot \sin\frac{1}{h} \right) = 0 \text{ by the Squeeze Theorem.} \\[6pt]
> &\text{Hence } f'(0) \text{ exists, and } f'(0) = 0.
> \end{aligned}
> $$

## Q6 Differentiable Implies Continuous

> [!question]
> (10 points) Prove that if $f$ is differentiable at $x = a$, then $f$ is continuous at $x = a$.

> [!attempt] My answer: 10/10
> Since $f$ is differentiable at $x = a$, $f'(a) = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$ exists.
> $$
> \begin{aligned}
> \lim_{x \to a}(f(x) - f(a)) &= \lim_{x \to a} \left[ \frac{f(x) - f(a)}{x - a} \cdot (x - a) \right] \\
> &= \lim_{x \to a} \frac{f(x) - f(a)}{x - a} \cdot \lim_{x \to a}(x - a) && \text{(by Product Law)} \\
> &= f'(a) \cdot \left( \lim_{x \to a} x + \lim_{x \to a}(-a) \right) && \text{(by Sum Law)} \\
> &= f'(a) \cdot (a - a) = f'(a) \cdot 0 = 0
> \end{aligned}
> $$
> $$
> \begin{aligned}
> \lim_{x \to a} f(x) &= \lim_{x \to a} \left[ f(a) + (f(x) - f(a)) \right] \\
> &= \lim_{x \to a} f(a) + \lim_{x \to a}(f(x) - f(a)) && \text{(by Sum Law)} \\
> &= f(a) + 0 \\
> &= f(a)
> \end{aligned}
> $$
> Hence $f$ is differentiable at $x = a$, then $f$ is continuous at $x = a$.

> [!proof]- Proof
> Since $f$ is differentiable at $x = a$, $f'(a) = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$ exists.
> $$
> \begin{aligned}
> \lim_{x \to a}(f(x) - f(a)) &= \lim_{x \to a} \left[ \frac{f(x) - f(a)}{x - a} \cdot (x - a) \right] && (x \ne a) \\
> &= \lim_{x \to a} \frac{f(x) - f(a)}{x - a} \cdot \lim_{x \to a}(x - a) && \text{(by Product Law)} \\
> &= f'(a) \cdot \left( \lim_{x \to a} x + \lim_{x \to a}(-a) \right) && \text{(by Sum Law)} \\
> &= f'(a) \cdot (a - a) = f'(a) \cdot 0 = 0
> \end{aligned}
> $$
> $$
> \begin{aligned}
> \lim_{x \to a} f(x) &= \lim_{x \to a} \left[ f(a) + (f(x) - f(a)) \right] \\
> &= \lim_{x \to a} f(a) + \lim_{x \to a}(f(x) - f(a)) && \text{(by Sum Law)} \\
> &= f(a) + 0 = f(a)
> \end{aligned}
> $$
> Hence $f$ is continuous at $x = a$ by the definition of continuity. $\blacksquare$
>
> \# Writing $f(x) - f(a) = \frac{f(x) - f(a)}{x - a} \cdot (x - a)$ needs $x \ne a$. A limit as $x \to a$ never uses $x = a$, so the note $(x \ne a)$ is enough; it is the same kind of condition as the "for $h \ne 0$" that cost a point in Q5.

## Q7 The Squeeze Theorem

> [!question]
> (10 points) **The Squeeze Theorem.** Suppose that $f(x) \le g(x) \le h(x)$ for all $x$ in an open interval containing $a$, except possibly at $x = a$, and
> $$
> \lim_{x \to a} f(x) = \lim_{x \to a} h(x) = L.
> $$
> Prove, using the $\varepsilon$, $\delta$ definition of a limit, that $\lim_{x \to a} g(x) = L$.
>
> *Hint:* $f \le g \le h$ on an open interval containing $a$ (except possibly at $a$) implies that there exists a $\delta > 0$ such that $f(x) \le g(x) \le h(x)$ whenever $0 < \lvert x - a \rvert < \delta$.

> [!attempt] My answer: 8/10
> $$
> \begin{aligned}
> &\text{Given } \varepsilon > 0. \\[6pt]
> &\text{Since } \lim_{x \to a} f(x) = L, \\
> &\quad \exists\, \delta_1 > 0 \text{ s.t. } 0 < \lvert x - a \rvert < \delta_1 \implies \lvert f(x) - L \rvert < \varepsilon \implies L - \varepsilon < f(x) \\
> &\text{Since } \lim_{x \to a} h(x) = L, \\
> &\quad \exists\, \delta_2 > 0 \text{ s.t. } 0 < \lvert x - a \rvert < \delta_2 \implies \lvert h(x) - L \rvert < \varepsilon \implies h(x) < L + \varepsilon \\
> &\text{we choose } \delta := \min\{\delta_1, \delta_2\} > 0 \implies \delta \le \delta_1 \text{ and } \delta \le \delta_2 \quad \text{✗} \\[6pt]
> &\text{If } 0 < \lvert x - a \rvert < \delta, \text{ then} \\
> &\qquad L - \varepsilon < f(x) \le g(x) \le h(x) < L + \varepsilon \\
> &\qquad \implies L - \varepsilon < g(x) < L + \varepsilon \\
> &\qquad \implies -\varepsilon < g(x) - L < \varepsilon \\
> &\qquad \implies \lvert g(x) - L \rvert < \varepsilon \\[6pt]
> &\text{Hence } \lim_{x \to a} g(x) = L \text{ by the definition of limit.}
> \end{aligned}
> $$

> [!failure] Mistake: f ≤ g ≤ h holds only near a
> The hypothesis was read as $f(x) \le g(x) \le h(x)$ for every real $x$, so no third $\delta$ seemed necessary. It is given only for $x$ in an open interval containing $a$, except possibly at $a$. The chain $L - \varepsilon < f(x) \le g(x) \le h(x) < L + \varepsilon$ uses three facts, and each must hold for every $x$ with $0 < \lvert x - a \rvert < \delta$:
> - $L - \varepsilon < f(x)$ needs $\delta \le \delta_1$;
> - $f(x) \le g(x) \le h(x)$ needs $\delta \le \delta_3$, which keeps $x$ in the interval: if the interval is $(p, q)$, take $\delta_3 = \min\{a - p,\ q - a\}$ (the Hint);
> - $h(x) < L + \varepsilon$ needs $\delta \le \delta_2$.
>
> $\delta_1$ and $\delta_2$ come from $f$ and $h$ alone and can be wider than the interval. For example, let $a = 0$, $L = 0$, $f(x) = -x^2$, $h(x) = x^2$, and $g(x) = 0$ for $\lvert x \rvert < 1$, $g(x) = 5$ for $\lvert x \rvert \ge 1$, so that $f \le g \le h$ on $(-1, 1)$. For $\varepsilon = 4$, $\delta_1 = \delta_2 = 2$ work, but $x = 1.5$ satisfies $0 < \lvert x \rvert < 2$ while $\lvert g(1.5) - 0 \rvert = 5 > \varepsilon$. The grader added $\delta_3$ and took $\delta = \min\{\delta_1, \delta_2, \delta_3\}$ (−2).

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{Given } \varepsilon > 0. \\[6pt]
> &\text{Since } \lim_{x \to a} f(x) = L, \\
> &\quad \exists\, \delta_1 > 0 \text{ s.t. } 0 < \lvert x - a \rvert < \delta_1 \implies \lvert f(x) - L \rvert < \varepsilon \implies L - \varepsilon < f(x). \\
> &\text{Since } \lim_{x \to a} h(x) = L, \\
> &\quad \exists\, \delta_2 > 0 \text{ s.t. } 0 < \lvert x - a \rvert < \delta_2 \implies \lvert h(x) - L \rvert < \varepsilon \implies h(x) < L + \varepsilon. \\
> &\text{Since } f(x) \le g(x) \le h(x) \text{ for } x \ne a \text{ in an open interval containing } a, \\
> &\quad \exists\, \delta_3 > 0 \text{ s.t. } 0 < \lvert x - a \rvert < \delta_3 \implies f(x) \le g(x) \le h(x). \\[6pt]
> &\text{We choose } \delta := \min\{\delta_1, \delta_2, \delta_3\} > 0 \implies \delta \le \delta_1,\ \delta \le \delta_2 \text{ and } \delta \le \delta_3. \\[6pt]
> &\text{If } 0 < \lvert x - a \rvert < \delta, \text{ then} \\
> &\qquad L - \varepsilon < f(x) \le g(x) \le h(x) < L + \varepsilon \\
> &\qquad \implies L - \varepsilon < g(x) < L + \varepsilon \\
> &\qquad \implies -\varepsilon < g(x) - L < \varepsilon \\
> &\qquad \implies \lvert g(x) - L \rvert < \varepsilon. \\[6pt]
> &\text{Hence } \lim_{x \to a} g(x) = L \text{ by the definition of limit.} \qquad \blacksquare
> \end{aligned}
> $$
