---
course: [CAL1]
chapter: ["1.7"]
tags: [calculus, homework, solutions, limits]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-10-02
questions: "[[CAL1 HW 1.7 Questions]]"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 1.7 Questions#ST 1.7.3\|ST 1.7.3]] | $\delta = 1.44$ (or any smaller positive number) |
| [[CAL1 HW 1.7 Questions#ST 1.7.13\|ST 1.7.13]] | (a) $\delta = 0.025$; (b) $\delta = 0.0025$ (or any smaller positive numbers) |
| [[CAL1 HW 1.7 Questions#ST 1.7.15\|ST 1.7.15]] | Proof with $\delta = 2\varepsilon$, and a diagram |
| [[CAL1 HW 1.7 Questions#ST 1.7.17\|ST 1.7.17]] | Proof with $\delta = \tfrac{\varepsilon}{2}$, and a diagram |
| [[CAL1 HW 1.7 Questions#ST 1.7.19\|ST 1.7.19]] | Proof with $\delta = 3\varepsilon$ |
| [[CAL1 HW 1.7 Questions#ST 1.7.21\|ST 1.7.21]] | Proof with $\delta = \varepsilon$ |
| [[CAL1 HW 1.7 Questions#ST 1.7.23\|ST 1.7.23]] | Proof with $\delta = \varepsilon$ |
| [[CAL1 HW 1.7 Questions#ST 1.7.25\|ST 1.7.25]] | Proof with $\delta = \sqrt{\varepsilon}$ |
| [[CAL1 HW 1.7 Questions#ST 1.7.27\|ST 1.7.27]] | Proof with $\delta = \varepsilon$ |
| [[CAL1 HW 1.7 Questions#ST 1.7.29\|ST 1.7.29]] | Proof with $\delta = \sqrt{\varepsilon}$ |
| [[CAL1 HW 1.7 Questions#ST 1.7.31\|ST 1.7.31]] | Proof with $\delta = \min\left\{1, \tfrac{\varepsilon}{5}\right\}$ |
| [[CAL1 HW 1.7 Questions#ST 1.7.41\|ST 1.7.41]] | Within $0.1$ of $-3$: $0 < \lvert x + 3 \rvert < 0.1$ |
| [[CAL1 HW 1.7 Questions#ST 1.7.43\|ST 1.7.43]] | Proof with $\delta = \sqrt[3]{-\tfrac{5}{N}}$ for each $N < 0$ |

## ST §1.7 The Precise Definition of a Limit

> [!note] Note
> Definitions of ST §1.7 and facts about real numbers used below.
> - **Definition 2** (the [[Precise Definition of a Limit|precise definition of a limit]]): $\lim_{x \to a} f(x) = L$ means that for every number $\varepsilon > 0$ there is a number $\delta > 0$ such that if $0 < \lvert x - a \rvert < \delta$ then $\lvert f(x) - L \rvert < \varepsilon$.
> - **Definition 6** (an [[Infinite Limit|infinite limit]]): $\lim_{x \to a} f(x) = \infty$ means that for every positive number $M$ there is a positive number $\delta$ such that if $0 < \lvert x - a \rvert < \delta$ then $f(x) > M$.
> - **Definition 7**: $\lim_{x \to a} f(x) = -\infty$ means that for every negative number $N$ there is a positive number $\delta$ such that if $0 < \lvert x - a \rvert < \delta$ then $f(x) < N$. For the [[One-Sided Limit|left-hand limit]] $\lim_{x \to a^{-}} f(x) = -\infty$, the condition $0 < \lvert x - a \rvert < \delta$ is replaced by $a - \delta < x < a$, exactly as Definition 3 does for a finite left-hand limit.
> - Absolute value: $\lvert uv \rvert = \lvert u \rvert\lvert v \rvert$, and for $c > 0$, $\lvert u \rvert < c$ if and only if $-c < u < c$.
> - Order: multiplying or dividing an inequality by a positive number keeps its direction, and by a negative number reverses it. For positive $p$ and $q$, $p > q$ if and only if $\tfrac{1}{p} < \tfrac{1}{q}$.
> - Powers: for $u, v \ge 0$ and a positive integer $n$, $u < v$ if and only if $u^n < v^n$. For all real $u$ and $v$, $u < v$ if and only if $u^3 < v^3$.
> - Method: as in Example 2 of ST §1.7, each $\varepsilon$, $\delta$ proof has two steps. The preliminary analysis guesses $\delta$ by working backwards from $\lvert f(x) - L \rvert < \varepsilon$. The proof then starts from $0 < \lvert x - a \rvert < \delta$ and derives $\lvert f(x) - L \rvert < \varepsilon$. Only the second step is the proof.

### ST 1.7.3
Question: [[CAL1 HW 1.7 Questions#ST 1.7.3|ST 1.7.3]]

> [!solution] Solution
> The inequality $\lvert \sqrt{x} - 2 \rvert < 0.4$ means $-0.4 < \sqrt{x} - 2 < 0.4$, that is,
> $$
> 1.6 < \sqrt{x} < 2.4.
> $$
> On the graph, the horizontal lines $y = 1.6$ and $y = 2.4$ meet the curve $y = \sqrt{x}$ above the two points of the $x$-axis marked "?". Solving $\sqrt{x} = 1.6$ and $\sqrt{x} = 2.4$ gives these points:
> $$
> x = 1.6^2 = 2.56 \qquad \text{and} \qquad x = 2.4^2 = 5.76.
> $$
> Since $u < v$ if and only if $u^2 < v^2$ for $u, v \ge 0$, the inequality $1.6 < \sqrt{x} < 2.4$ holds exactly when $2.56 < x < 5.76$. The condition $\lvert x - 4 \rvert < \delta$ describes the interval $(4 - \delta, 4 + \delta)$, which is centered at $4$ and must lie inside $(2.56, 5.76)$. The distances from $4$ to $2.56$ and to $5.76$ are
> $$
> 4 - 2.56 = 1.44 \qquad \text{and} \qquad 5.76 - 4 = 1.76.
> $$
> We choose the smaller distance, $\delta = 1.44$. Then
> $$
> \begin{aligned}
> \lvert x - 4 \rvert < 1.44 &\implies 2.56 < x < 5.44 \\
> &\implies 2.56 < x < 5.76 \\
> &\implies 1.6 < \sqrt{x} < 2.4 \\
> &\implies \lvert \sqrt{x} - 2 \rvert < 0.4.
> \end{aligned}
> $$
> In the figure, the strip $\lvert x - 4 \rvert < 1.44$ is shaded. Above it, the curve stays between the lines $y = 1.6$ and $y = 2.4$.
>
> ![[CAL1 HW 1.7 Solutions fig 3.svg|380]]
>
> **Answer.** $\delta = 1.44$, or any smaller positive number. A larger $\delta$ does not work: if $\delta > 1.44$, then $x = 2.56$ satisfies $\lvert x - 4 \rvert < \delta$, but $\lvert \sqrt{2.56} - 2 \rvert = 0.4$.

### ST 1.7.13
Question: [[CAL1 HW 1.7 Questions#ST 1.7.13|ST 1.7.13]]

> [!solution] Solution
> For every real number $x$,
> $$
> \lvert 4x - 8 \rvert = \lvert 4(x - 2) \rvert = 4\lvert x - 2 \rvert.
> $$
> Hence $\lvert 4x - 8 \rvert < \varepsilon$ if and only if $\lvert x - 2 \rvert < \tfrac{\varepsilon}{4}$, and $\delta = \tfrac{\varepsilon}{4}$ works: if $\lvert x - 2 \rvert < \tfrac{\varepsilon}{4}$, then $\lvert 4x - 8 \rvert = 4\lvert x - 2 \rvert < 4 \cdot \tfrac{\varepsilon}{4} = \varepsilon$.
> - (a) For $\varepsilon = 0.1$: $\delta = \tfrac{0.1}{4} = 0.025$.
> - (b) For $\varepsilon = 0.01$: $\delta = \tfrac{0.01}{4} = 0.0025$.
>
> In both parts any smaller positive number also works. The smaller $\varepsilon$ of part (b) requires a smaller $\delta$.

### ST 1.7.15
Question: [[CAL1 HW 1.7 Questions#ST 1.7.15|ST 1.7.15]]

> [!solution] Solution
> **Preliminary analysis (guessing a value for $\delta$).** Let $\varepsilon > 0$ be given. We want a number $\delta > 0$ such that
> $$
> \text{if} \quad 0 < \lvert x - 4 \rvert < \delta \quad \text{then} \quad \left\lvert \left(\tfrac{1}{2}x - 1\right) - 1 \right\rvert < \varepsilon.
> $$
> But
> $$
> \left\lvert \left(\tfrac{1}{2}x - 1\right) - 1 \right\rvert = \left\lvert \tfrac{1}{2}x - 2 \right\rvert = \left\lvert \tfrac{1}{2}(x - 4) \right\rvert = \tfrac{1}{2}\lvert x - 4 \rvert,
> $$
> so we want $\tfrac{1}{2}\lvert x - 4 \rvert < \varepsilon$, that is, $\lvert x - 4 \rvert < 2\varepsilon$. This suggests that we choose $\delta = 2\varepsilon$.
>
> **Diagram.** The line $y = \tfrac{1}{2}x - 1$ meets the horizontal lines $y = 1 - \varepsilon$ and $y = 1 + \varepsilon$ at $x = 4 - 2\varepsilon$ and $x = 4 + 2\varepsilon$. With $\delta = 2\varepsilon$, for every $x$ between $4 - \delta$ and $4 + \delta$ the point of the line above $x$ lies between the heights $1 - \varepsilon$ and $1 + \varepsilon$.
>
> ![[CAL1 HW 1.7 Solutions fig 15.svg|400]]

> [!proof] Proof
> Given $\varepsilon > 0$, choose $\delta = 2\varepsilon$; then $\delta > 0$. If $0 < \lvert x - 4 \rvert < \delta$, then
> $$
> \begin{aligned}
> \left\lvert \left(\tfrac{1}{2}x - 1\right) - 1 \right\rvert &= \left\lvert \tfrac{1}{2}(x - 4) \right\rvert \\
> &= \tfrac{1}{2}\lvert x - 4 \rvert && \text{(\(\lvert uv \rvert = \lvert u \rvert\lvert v \rvert\))} \\
> &< \tfrac{1}{2}\delta && \text{(\(\lvert x - 4 \rvert < \delta\))} \\
> &= \tfrac{1}{2}(2\varepsilon) = \varepsilon. && \text{(choice of \(\delta\))}
> \end{aligned}
> $$
> Thus if $0 < \lvert x - 4 \rvert < \delta$, then $\left\lvert \left(\tfrac{1}{2}x - 1\right) - 1 \right\rvert < \varepsilon$. Therefore, by Definition 2, $\lim_{x \to 4} \left(\tfrac{1}{2}x - 1\right) = 1$. $\blacksquare$

### ST 1.7.17
Question: [[CAL1 HW 1.7 Questions#ST 1.7.17|ST 1.7.17]]

> [!solution] Solution
> **Preliminary analysis (guessing a value for $\delta$).** Let $\varepsilon > 0$ be given. Since $x - (-2) = x + 2$, we want a number $\delta > 0$ such that
> $$
> \text{if} \quad 0 < \lvert x + 2 \rvert < \delta \quad \text{then} \quad \lvert (-2x + 1) - 5 \rvert < \varepsilon.
> $$
> But
> $$
> \lvert (-2x + 1) - 5 \rvert = \lvert -2x - 4 \rvert = \lvert -2(x + 2) \rvert = \lvert -2 \rvert\lvert x + 2 \rvert = 2\lvert x + 2 \rvert,
> $$
> so we want $2\lvert x + 2 \rvert < \varepsilon$, that is, $\lvert x + 2 \rvert < \tfrac{\varepsilon}{2}$. This suggests that we choose $\delta = \tfrac{\varepsilon}{2}$.
>
> **Diagram.** The line $y = -2x + 1$ falls from left to right, so it meets $y = 5 + \varepsilon$ at $x = -2 - \tfrac{\varepsilon}{2}$ and $y = 5 - \varepsilon$ at $x = -2 + \tfrac{\varepsilon}{2}$. With $\delta = \tfrac{\varepsilon}{2}$, for every $x$ between $-2 - \delta$ and $-2 + \delta$ the point of the line above $x$ lies between the heights $5 - \varepsilon$ and $5 + \varepsilon$.
>
> ![[CAL1 HW 1.7 Solutions fig 17.svg|400]]

> [!proof] Proof
> Given $\varepsilon > 0$, choose $\delta = \tfrac{\varepsilon}{2}$; then $\delta > 0$. If $0 < \lvert x - (-2) \rvert < \delta$, that is, $0 < \lvert x + 2 \rvert < \delta$, then
> $$
> \begin{aligned}
> \lvert (-2x + 1) - 5 \rvert &= \lvert -2(x + 2) \rvert \\
> &= 2\lvert x + 2 \rvert && \text{(\(\lvert uv \rvert = \lvert u \rvert\lvert v \rvert\) and \(\lvert -2 \rvert = 2\))} \\
> &< 2\delta && \text{(\(\lvert x + 2 \rvert < \delta\))} \\
> &= 2 \cdot \tfrac{\varepsilon}{2} = \varepsilon. && \text{(choice of \(\delta\))}
> \end{aligned}
> $$
> Therefore, by Definition 2, $\lim_{x \to -2} \, (-2x + 1) = 5$. $\blacksquare$

### ST 1.7.19
Question: [[CAL1 HW 1.7 Questions#ST 1.7.19|ST 1.7.19]]

> [!solution] Solution
> **Preliminary analysis (guessing a value for $\delta$).** Let $\varepsilon > 0$ be given. We want a number $\delta > 0$ such that
> $$
> \text{if} \quad 0 < \lvert x - 9 \rvert < \delta \quad \text{then} \quad \left\lvert \left(1 - \tfrac{1}{3}x\right) - (-2) \right\rvert < \varepsilon.
> $$
> But
> $$
> \left\lvert \left(1 - \tfrac{1}{3}x\right) - (-2) \right\rvert = \left\lvert 3 - \tfrac{1}{3}x \right\rvert = \left\lvert -\tfrac{1}{3}(x - 9) \right\rvert = \tfrac{1}{3}\lvert x - 9 \rvert,
> $$
> so we want $\tfrac{1}{3}\lvert x - 9 \rvert < \varepsilon$, that is, $\lvert x - 9 \rvert < 3\varepsilon$. This suggests that we choose $\delta = 3\varepsilon$.

> [!proof] Proof
> Given $\varepsilon > 0$, choose $\delta = 3\varepsilon$; then $\delta > 0$. If $0 < \lvert x - 9 \rvert < \delta$, then
> $$
> \begin{aligned}
> \left\lvert \left(1 - \tfrac{1}{3}x\right) - (-2) \right\rvert &= \left\lvert -\tfrac{1}{3}(x - 9) \right\rvert \\
> &= \tfrac{1}{3}\lvert x - 9 \rvert && \text{(\(\lvert uv \rvert = \lvert u \rvert\lvert v \rvert\) and \(\left\lvert -\tfrac{1}{3} \right\rvert = \tfrac{1}{3}\))} \\
> &< \tfrac{1}{3}\delta && \text{(\(\lvert x - 9 \rvert < \delta\))} \\
> &= \tfrac{1}{3}(3\varepsilon) = \varepsilon. && \text{(choice of \(\delta\))}
> \end{aligned}
> $$
> Therefore, by Definition 2, $\lim_{x \to 9} \left(1 - \tfrac{1}{3}x\right) = -2$. $\blacksquare$

> [!tip] Intuition
> Exercises 13, 15, 17 and 19 follow one pattern. For a linear function $f(x) = mx + b$ with $m \ne 0$, we have $\lvert f(x) - f(a) \rvert = \lvert m \rvert\lvert x - a \rvert$, so $\delta = \tfrac{\varepsilon}{\lvert m \rvert}$ always works. Here $\lvert m \rvert = 4$, $\tfrac{1}{2}$, $2$ and $\tfrac{1}{3}$, which gives $\delta = \tfrac{\varepsilon}{4}$, $2\varepsilon$, $\tfrac{\varepsilon}{2}$ and $3\varepsilon$: a steeper line needs a smaller $\delta$. Exercises 21 and 23 below are the case $m = 1$.

### ST 1.7.21
Question: [[CAL1 HW 1.7 Questions#ST 1.7.21|ST 1.7.21]]

> [!solution] Solution
> **Preliminary analysis (guessing a value for $\delta$).** Let $f(x) = \dfrac{x^2 - 2x - 8}{x - 4}$, which is defined for every $x \ne 4$. The numerator factors as $x^2 - 2x - 8 = (x - 4)(x + 2)$, so for $x \ne 4$
> $$
> f(x) = \frac{(x - 4)(x + 2)}{x - 4} = x + 2,
> $$
> and therefore
> $$
> \lvert f(x) - 6 \rvert = \lvert (x + 2) - 6 \rvert = \lvert x - 4 \rvert.
> $$
> We want $\lvert x - 4 \rvert < \varepsilon$ whenever $0 < \lvert x - 4 \rvert < \delta$. This suggests that we choose $\delta = \varepsilon$. The number $4$, where $f$ is not defined, causes no trouble: Definition 2 considers only those $x$ with $0 < \lvert x - 4 \rvert$, that is, $x \ne 4$.

> [!proof] Proof
> Given $\varepsilon > 0$, choose $\delta = \varepsilon$. If $0 < \lvert x - 4 \rvert < \delta$, then $x \ne 4$, so $x - 4 \ne 0$ and
> $$
> \begin{aligned}
> \left\lvert \frac{x^2 - 2x - 8}{x - 4} - 6 \right\rvert &= \left\lvert \frac{(x - 4)(x + 2)}{x - 4} - 6 \right\rvert && \text{(factoring)} \\
> &= \lvert (x + 2) - 6 \rvert && \text{(cancelling \(x - 4 \ne 0\))} \\
> &= \lvert x - 4 \rvert \\
> &< \delta && \text{(\(\lvert x - 4 \rvert < \delta\))} \\
> &= \varepsilon. && \text{(choice of \(\delta\))}
> \end{aligned}
> $$
> Therefore, by Definition 2, $\lim_{x \to 4} \dfrac{x^2 - 2x - 8}{x - 4} = 6$. $\blacksquare$

### ST 1.7.23
Question: [[CAL1 HW 1.7 Questions#ST 1.7.23|ST 1.7.23]]

> [!solution] Solution
> **Preliminary analysis (guessing a value for $\delta$).** Here $f(x) = x$ and $L = a$, so $\lvert f(x) - L \rvert = \lvert x - a \rvert$. The inequality we want, $\lvert x - a \rvert < \varepsilon$, is the hypothesis $\lvert x - a \rvert < \delta$ itself when $\delta = \varepsilon$.

> [!proof] Proof
> Given $\varepsilon > 0$, choose $\delta = \varepsilon$. If $0 < \lvert x - a \rvert < \delta$, then
> $$
> \lvert x - a \rvert < \delta = \varepsilon.
> $$
> This is the inequality $\lvert f(x) - L \rvert < \varepsilon$ for $f(x) = x$ and $L = a$. Therefore, by Definition 2, $\lim_{x \to a} x = a$. $\blacksquare$

### ST 1.7.25
Question: [[CAL1 HW 1.7 Questions#ST 1.7.25|ST 1.7.25]]

> [!solution] Solution
> **Preliminary analysis (guessing a value for $\delta$).** We want $\lvert x^2 - 0 \rvert < \varepsilon$ whenever $0 < \lvert x - 0 \rvert < \delta$. Now $\lvert x^2 - 0 \rvert = \lvert x \rvert^2$, and since $\lvert x \rvert$ and $\sqrt{\varepsilon}$ are not negative,
> $$
> \lvert x \rvert^2 < \varepsilon \iff \lvert x \rvert < \sqrt{\varepsilon}.
> $$
> This suggests that we choose $\delta = \sqrt{\varepsilon}$.

> [!proof] Proof
> Given $\varepsilon > 0$, choose $\delta = \sqrt{\varepsilon}$; then $\delta > 0$. If $0 < \lvert x - 0 \rvert < \delta$, then $0 < \lvert x \rvert < \sqrt{\varepsilon}$, and
> $$
> \begin{aligned}
> \lvert x^2 - 0 \rvert &= \lvert x \rvert^2 && \text{(\(\lvert uv \rvert = \lvert u \rvert\lvert v \rvert\))} \\
> &< \left(\sqrt{\varepsilon}\right)^2 && \text{(squaring \(0 \le \lvert x \rvert < \sqrt{\varepsilon}\))} \\
> &= \varepsilon.
> \end{aligned}
> $$
> Therefore, by Definition 2, $\lim_{x \to 0} x^2 = 0$. $\blacksquare$

### ST 1.7.27
Question: [[CAL1 HW 1.7 Questions#ST 1.7.27|ST 1.7.27]]

> [!solution] Solution
> **Preliminary analysis (guessing a value for $\delta$).** Here $f(x) = \lvert x \rvert$ and $L = 0$. Because $\lvert x \rvert \ge 0$, the absolute value of $\lvert x \rvert$ is $\lvert x \rvert$ itself, so
> $$
> \big\lvert \lvert x \rvert - 0 \big\rvert = \lvert x \rvert = \lvert x - 0 \rvert.
> $$
> The inequality we want is again the hypothesis itself when $\delta = \varepsilon$.

> [!proof] Proof
> Given $\varepsilon > 0$, choose $\delta = \varepsilon$. If $0 < \lvert x - 0 \rvert < \delta$, then
> $$
> \begin{aligned}
> \big\lvert \lvert x \rvert - 0 \big\rvert &= \lvert x \rvert && \text{(\(\lvert x \rvert \ge 0\))} \\
> &= \lvert x - 0 \rvert \\
> &< \delta && \text{(\(\lvert x - 0 \rvert < \delta\))} \\
> &= \varepsilon. && \text{(choice of \(\delta\))}
> \end{aligned}
> $$
> Therefore, by Definition 2, $\lim_{x \to 0} \, \lvert x \rvert = 0$. $\blacksquare$

### ST 1.7.29
Question: [[CAL1 HW 1.7 Questions#ST 1.7.29|ST 1.7.29]]

> [!solution] Solution
> **Preliminary analysis (guessing a value for $\delta$).** We want $\lvert (x^2 - 4x + 5) - 1 \rvert < \varepsilon$ whenever $0 < \lvert x - 2 \rvert < \delta$. The difference is a perfect square:
> $$
> \lvert (x^2 - 4x + 5) - 1 \rvert = \lvert x^2 - 4x + 4 \rvert = \lvert (x - 2)^2 \rvert = \lvert x - 2 \rvert^2.
> $$
> Since $\lvert x - 2 \rvert$ and $\sqrt{\varepsilon}$ are not negative, $\lvert x - 2 \rvert^2 < \varepsilon$ if and only if $\lvert x - 2 \rvert < \sqrt{\varepsilon}$. This suggests that we choose $\delta = \sqrt{\varepsilon}$.

> [!proof] Proof
> Given $\varepsilon > 0$, choose $\delta = \sqrt{\varepsilon}$; then $\delta > 0$. If $0 < \lvert x - 2 \rvert < \delta$, then
> $$
> \begin{aligned}
> \lvert (x^2 - 4x + 5) - 1 \rvert &= \lvert x^2 - 4x + 4 \rvert \\
> &= \lvert (x - 2)^2 \rvert && \text{(perfect square)} \\
> &= \lvert x - 2 \rvert^2 && \text{(\(\lvert uv \rvert = \lvert u \rvert\lvert v \rvert\))} \\
> &< \delta^2 && \text{(squaring \(0 \le \lvert x - 2 \rvert < \delta\))} \\
> &= \left(\sqrt{\varepsilon}\right)^2 = \varepsilon. && \text{(choice of \(\delta\))}
> \end{aligned}
> $$
> Therefore, by Definition 2, $\lim_{x \to 2} \, (x^2 - 4x + 5) = 1$. $\blacksquare$

### ST 1.7.31
Question: [[CAL1 HW 1.7 Questions#ST 1.7.31|ST 1.7.31]]

> [!solution] Solution
> **Preliminary analysis (guessing a value for $\delta$).** Since $x - (-2) = x + 2$, we want $\lvert (x^2 - 1) - 3 \rvert < \varepsilon$ whenever $0 < \lvert x + 2 \rvert < \delta$. Factoring gives
> $$
> \lvert (x^2 - 1) - 3 \rvert = \lvert x^2 - 4 \rvert = \lvert x + 2 \rvert\lvert x - 2 \rvert.
> $$
> The factor $\lvert x + 2 \rvert$ is small when $x$ is near $-2$, but the factor $\lvert x - 2 \rvert$ is not, so we look for a constant $C$ with $\lvert x - 2 \rvert < C$. We are interested only in $x$ near $-2$, so we may assume $\lvert x + 2 \rvert < 1$. Then
> $$
> \begin{aligned}
> \lvert x + 2 \rvert < 1 &\implies -1 < x + 2 < 1 \\
> &\implies -3 < x < -1 \\
> &\implies -5 < x - 2 < -3 \\
> &\implies \lvert x - 2 \rvert < 5,
> \end{aligned}
> $$
> so $C = 5$ and $\lvert x + 2 \rvert\lvert x - 2 \rvert < 5\lvert x + 2 \rvert$. To make $5\lvert x + 2 \rvert < \varepsilon$ we need $\lvert x + 2 \rvert < \tfrac{\varepsilon}{5}$. Both restrictions, $\lvert x + 2 \rvert < 1$ and $\lvert x + 2 \rvert < \tfrac{\varepsilon}{5}$, must hold, so we choose $\delta = \min\left\{1, \tfrac{\varepsilon}{5}\right\}$.

> [!proof] Proof
> Given $\varepsilon > 0$, choose $\delta = \min\left\{1, \tfrac{\varepsilon}{5}\right\}$; then $\delta > 0$, $\delta \le 1$ and $\delta \le \tfrac{\varepsilon}{5}$. Suppose $0 < \lvert x - (-2) \rvert < \delta$, that is, $0 < \lvert x + 2 \rvert < \delta$.
>
> Since $\lvert x + 2 \rvert < \delta \le 1$, we have $-1 < x + 2 < 1$, so $-3 < x < -1$ and $-5 < x - 2 < -3$. Hence $\lvert x - 2 \rvert < 5$.
>
> Since $\lvert x + 2 \rvert < \delta \le \tfrac{\varepsilon}{5}$, we have $\lvert x + 2 \rvert < \tfrac{\varepsilon}{5}$. Therefore
> $$
> \begin{aligned}
> \lvert (x^2 - 1) - 3 \rvert &= \lvert x^2 - 4 \rvert \\
> &= \lvert x + 2 \rvert\lvert x - 2 \rvert && \text{(factoring, \(\lvert uv \rvert = \lvert u \rvert\lvert v \rvert\))} \\
> &< 5\lvert x + 2 \rvert && \text{(\(\lvert x - 2 \rvert < 5\) and \(\lvert x + 2 \rvert > 0\))} \\
> &< 5 \cdot \tfrac{\varepsilon}{5} = \varepsilon. && \text{(\(\lvert x + 2 \rvert < \tfrac{\varepsilon}{5}\))}
> \end{aligned}
> $$
> Therefore, by Definition 2, $\lim_{x \to -2} \, (x^2 - 1) = 3$. $\blacksquare$

> [!tip] Intuition
> In Exercises 25 and 29, $\lvert f(x) - L \rvert$ is exactly $\lvert x - a \rvert^2$, so we can solve for $\lvert x - a \rvert$ directly and $\delta = \sqrt{\varepsilon}$. In Exercise 31, $\lvert f(x) - L \rvert = \lvert x + 2 \rvert\lvert x - 2 \rvert$ has a second factor that depends on $x$. We cannot choose $\delta = \tfrac{\varepsilon}{\lvert x - 2 \rvert}$, because $\delta$ may depend only on $\varepsilon$, not on $x$. So we first restrict $\lvert x + 2 \rvert < 1$ to bound the second factor by the constant $5$, and the minimum makes both restrictions hold at once.

### ST 1.7.41
Question: [[CAL1 HW 1.7 Questions#ST 1.7.41|ST 1.7.41]]

> [!solution] Solution
> The fraction is defined for $x \ne -3$, and then $(x + 3)^4 > 0$, so both sides of the inequality are positive. Hence
> $$
> \begin{aligned}
> \frac{1}{(x + 3)^4} > 10{,}000 &\overset{(1)}{\iff} (x + 3)^4 < \frac{1}{10{,}000} \\
> &\overset{(2)}{\iff} \lvert x + 3 \rvert^4 < \left(\tfrac{1}{10}\right)^4 \\
> &\overset{(3)}{\iff} \lvert x + 3 \rvert < \tfrac{1}{10}.
> \end{aligned}
> $$
> 1. For positive $p$ and $q$, $p > q$ if and only if $\tfrac{1}{p} < \tfrac{1}{q}$.
> 2. $(x + 3)^4 = \lvert x + 3 \rvert^4$ and $\tfrac{1}{10{,}000} = \left(\tfrac{1}{10}\right)^4$.
> 3. For $u, v \ge 0$, $u < v$ if and only if $u^4 < v^4$.
>
> **Answer.** We have to take $x$ within $0.1$ of $-3$, with $x \ne -3$: $0 < \lvert x + 3 \rvert < 0.1$, that is, $-3.1 < x < -2.9$ and $x \ne -3$. In the language of Definition 6, for the limit $\lim_{x \to -3} \dfrac{1}{(x + 3)^4} = \infty$ the number $M = 10{,}000$ corresponds to $\delta = 0.1$.

### ST 1.7.43
Question: [[CAL1 HW 1.7 Questions#ST 1.7.43|ST 1.7.43]]

> [!solution] Solution
> **What must be shown.** By the left-hand form of Definition 7 (see the note at the top of this section), we must show that for every negative number $N$ there is a number $\delta > 0$ such that
> $$
> \text{if} \quad {-1} - \delta < x < -1 \quad \text{then} \quad \frac{5}{(x + 1)^3} < N.
> $$
>
> **Preliminary analysis (guessing a value for $\delta$).** Let $N < 0$ be given, and let $x < -1$. Then $x + 1 < 0$, so $(x + 1)^3 < 0$. Multiplying by the negative number $(x + 1)^3$ reverses the inequality, and so does dividing by the negative number $N$:
> $$
> \begin{aligned}
> \frac{5}{(x + 1)^3} < N &\iff 5 > N(x + 1)^3 && \text{(multiplying by \((x + 1)^3 < 0\))} \\
> &\iff \frac{5}{N} < (x + 1)^3 && \text{(dividing by \(N < 0\))} \\
> &\iff \sqrt[3]{\frac{5}{N}} < x + 1. && \text{(taking cube roots)}
> \end{aligned}
> $$
> Since $\sqrt[3]{\tfrac{5}{N}} = -\sqrt[3]{-\tfrac{5}{N}}$, the last inequality is $-1 - \sqrt[3]{-\tfrac{5}{N}} < x$. This suggests that we choose $\delta = \sqrt[3]{-\tfrac{5}{N}}$, which is positive because $-\tfrac{5}{N} > 0$.

> [!proof] Proof
> Let $N$ be a negative number, and choose $\delta = \sqrt[3]{-\tfrac{5}{N}}$. Since $-\tfrac{5}{N} > 0$, we have $\delta > 0$ and $\delta^3 = -\tfrac{5}{N}$. If $-1 - \delta < x < -1$, then
> $$
> \begin{aligned}
> &{-\delta} < x + 1 < 0 && \text{(adding \(1\))} \\
> &\implies -\delta^3 < (x + 1)^3 < 0 && \text{(\(u < v \iff u^3 < v^3\))} \\
> &\implies \frac{5}{N} < (x + 1)^3 < 0 && \text{(\(\delta^3 = -\tfrac{5}{N}\))} \\
> &\implies 5 > N(x + 1)^3 && \text{(multiplying by \(N < 0\))} \\
> &\implies \frac{5}{(x + 1)^3} < N. && \text{(dividing by \((x + 1)^3 < 0\))}
> \end{aligned}
> $$
> Thus for every negative number $N$ there is a $\delta > 0$ such that if $-1 - \delta < x < -1$, then $\dfrac{5}{(x + 1)^3} < N$. Therefore $\lim_{x \to -1^{-}} \dfrac{5}{(x + 1)^3} = -\infty$. $\blacksquare$
