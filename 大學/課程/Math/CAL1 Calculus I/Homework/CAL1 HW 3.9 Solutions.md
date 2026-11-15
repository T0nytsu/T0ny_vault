---
course: [CAL1]
semester: "115-1"
chapter: ["3.9"]
tags: [calculus, homework, solutions, derivatives]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §3.9, pp. 283-291, scanned PDF (antiderivatives, the table of antidifferentiation formulas, rectilinear motion)"
created: 2026-11-15
questions: "[[CAL1 HW 3.9 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 3.9 Questions#ST 3.9.1\|ST 3.9.1]] | (a) $F(x) = 6x$; (b) $G(t) = t^3$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.5\|ST 3.9.5]] | $F(x) = 2x^2 + 7x + C$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.9\|ST 3.9.9]] | $F(x) = 4x^3 + 4x^2 + C$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.13\|ST 3.9.13]] | $F(x) = 2x^{3/2} - \tfrac{3}{2}x^{4/3} + C$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.15\|ST 3.9.15]] | $F(t) = \tfrac{4}{3}t^{3/2} + 3t - 8t^{1/2} + C$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.17\|ST 3.9.17]] | $F(x) = -\tfrac{5}{4x^8} + C_1$ for $x > 0$, $-\tfrac{5}{4x^8} + C_2$ for $x < 0$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.19\|ST 3.9.19]] | $F(\theta) = -2\cos\theta - 3\sec\theta + C_n$ on $(n\pi - \tfrac{\pi}{2}, n\pi + \tfrac{\pi}{2})$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.21\|ST 3.9.21]] | $H(\theta) = -2\cos\theta - \tan\theta + C_n$ on $(n\pi - \tfrac{\pi}{2}, n\pi + \tfrac{\pi}{2})$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.23\|ST 3.9.23]] | $G(v) = \tfrac{3}{5}v^{5/3} - 2\tan v + C_n$ on $(n\pi - \tfrac{\pi}{2}, n\pi + \tfrac{\pi}{2})$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.27\|ST 3.9.27]] | $f(x) = 4x^3 + Cx + D$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.31\|ST 3.9.31]] | $f(x) = 2x^2 - \tfrac{9}{28}x^{7/3} + Cx + D$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.37\|ST 3.9.37]] | $f(x) = 3x^{5/3} - 75$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.41\|ST 3.9.41]] | $f(x) = -x^4 + 2x^3 - x^2 + 12x + 4$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.43\|ST 3.9.43]] | $f(\theta) = -\sin\theta - \cos\theta + 5\theta + 4$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.49\|ST 3.9.49]] | $f(1) = 8$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.59\|ST 3.9.59]] | $s(t) = 2\sin t - 4\cos t + 7$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.61\|ST 3.9.61]] | $s(t) = \tfrac{1}{3}t^3 + \tfrac{1}{2}t^2 - 2t + 3$ |
| [[CAL1 HW 3.9 Questions#ST 3.9.66\|ST 3.9.66]] | Proof |
| [[CAL1 HW 3.9 Questions#ST 3.9.69\|ST 3.9.69]] | $\tfrac{4000}{49} \approx 81.6$ m |

## ST §3.9 Antiderivatives

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Antiderivative]]**: $F$ is an antiderivative of $f$ on an interval $I$ if $F'(x) = f(x)$ for all $x$ in $I$.
> - **Most general antiderivative**: if $F$ is an antiderivative of $f$ on an interval $I$, then every antiderivative of $f$ on $I$ is $F(x) + C$, $C$ a constant. (Two functions with the same derivative on an interval differ by a constant, a consequence of the Mean Value Theorem.) On a domain made of several intervals, each interval gets its own constant.
> - **Formulas** (read the derivative table backwards):
>
> | Function | Particular antiderivative |
> | --- | --- |
> | $x^n$, $n \ne -1$ | $\dfrac{x^{n+1}}{n+1}$ |
> | $\cos x$ | $\sin x$ |
> | $\sin x$ | $-\cos x$ |
> | $\sec^2 x$ | $\tan x$ |
> | $\sec x \tan x$ | $\sec x$ |
>
> - **Sum and constant multiple**: an antiderivative of $cf + g$ is $cF + G$.
> - **Rectilinear motion**: $s'(t) = v(t)$ and $v'(t) = a(t)$, so $v$ is an antiderivative of $a$ and $s$ is an antiderivative of $v$. Near the earth's surface $a = -9.8$ m/s² (upward positive), as in Example 7 of the section.

### ST 3.9.1
Question: [[CAL1 HW 3.9 Questions#ST 3.9.1|ST 3.9.1]]

> [!solution] Solution
> - (a) $F(x) = 6x$, since $F'(x) = 6 = f(x)$.
> - (b) $G(t) = t^3$, since $G'(t) = 3t^2 = g(t)$.
>
> \# "An antiderivative" asks for one function, so no $+C$ is needed; $6x + 5$ or $t^3 - 2$ are also correct.

### ST 3.9.5
Question: [[CAL1 HW 3.9 Questions#ST 3.9.5|ST 3.9.5]]

> [!solution] Solution
> $$
> \begin{aligned}
> &F(x) = 4 \cdot \frac{x^2}{2} + 7x + C = 2x^2 + 7x + C \\
> &\text{Check: } F'(x) = 4x + 7 = f(x)
> \end{aligned}
> $$
> Hence $F(x) = 2x^2 + 7x + C$.

### ST 3.9.9
Question: [[CAL1 HW 3.9 Questions#ST 3.9.9|ST 3.9.9]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(x) = 12x^2 + 8x \\
> &F(x) = 12 \cdot \frac{x^3}{3} + 8 \cdot \frac{x^2}{2} + C = 4x^3 + 4x^2 + C \\
> &\text{Check: } F'(x) = 12x^2 + 8x = x(12x + 8)
> \end{aligned}
> $$
> Hence $F(x) = 4x^3 + 4x^2 + C$.
>
> \# Expand the product first: there is no product rule for antiderivatives, so $x \cdot (12x + 8)$ cannot be antidifferentiated factor by factor.

### ST 3.9.13
Question: [[CAL1 HW 3.9 Questions#ST 3.9.13|ST 3.9.13]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(x) = 3x^{1/2} - 2x^{1/3} \\
> &F(x) = 3 \cdot \frac{x^{3/2}}{3/2} - 2 \cdot \frac{x^{4/3}}{4/3} + C = 2x^{3/2} - \tfrac{3}{2}x^{4/3} + C \\
> &\text{Check: } F'(x) = 2 \cdot \tfrac{3}{2}x^{1/2} - \tfrac{3}{2} \cdot \tfrac{4}{3}x^{1/3} = 3\sqrt{x} - 2\sqrt[3]{x}
> \end{aligned}
> $$
> Hence $F(x) = 2x^{3/2} - \tfrac{3}{2}x^{4/3} + C$.
>
> \# Write each root as a power, then use $x^n \mapsto \dfrac{x^{n+1}}{n+1}$. Dividing by $\tfrac{3}{2}$ is multiplying by $\tfrac{2}{3}$.

### ST 3.9.15
Question: [[CAL1 HW 3.9 Questions#ST 3.9.15|ST 3.9.15]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(t) = \frac{2t}{t^{1/2}} - \frac{4}{t^{1/2}} + \frac{3t^{1/2}}{t^{1/2}} = 2t^{1/2} - 4t^{-1/2} + 3, \quad t > 0 \\
> &F(t) = 2 \cdot \frac{t^{3/2}}{3/2} - 4 \cdot \frac{t^{1/2}}{1/2} + 3t + C = \tfrac{4}{3}t^{3/2} - 8t^{1/2} + 3t + C \\
> &\text{Check: } F'(t) = 2t^{1/2} - 4t^{-1/2} + 3 = f(t)
> \end{aligned}
> $$
> Hence $F(t) = \tfrac{4}{3}t^{3/2} + 3t - 8\sqrt{t} + C$.
>
> \# Split the fraction term by term before antidifferentiating; there is no quotient rule for antiderivatives. The domain is $t > 0$, one interval, so one constant $C$ is enough.

### ST 3.9.17
Question: [[CAL1 HW 3.9 Questions#ST 3.9.17|ST 3.9.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(x) = 10x^{-9}, \quad x \ne 0 \\
> &10 \cdot \frac{x^{-8}}{-8} = -\frac{5}{4x^8} \\
> &\text{Check: } \frac{d}{dx}\Big(-\tfrac{5}{4}x^{-8}\Big) = -\tfrac{5}{4}(-8)x^{-9} = \frac{10}{x^9} \\[6pt]
> &\text{domain } (-\infty, 0) \cup (0, \infty)\text{: one constant on each interval}
> \end{aligned}
> $$
> Hence
> $$
> F(x) = \begin{cases} -\dfrac{5}{4x^8} + C_1 & \text{if } x > 0 \\[6pt] -\dfrac{5}{4x^8} + C_2 & \text{if } x < 0 \end{cases}
> $$
>
> \# "$-\tfrac{5}{4x^8} + C$" misses some antiderivatives: the constant may jump at $x = 0$, because $0$ is not in the domain. For example, $-\tfrac{5}{4x^8} + 1$ for $x > 0$ and $-\tfrac{5}{4x^8} - 3$ for $x < 0$ still has derivative $\tfrac{10}{x^9}$ everywhere on the domain.

### ST 3.9.19
Question: [[CAL1 HW 3.9 Questions#ST 3.9.19|ST 3.9.19]]

> [!solution] Solution
> $$
> \begin{aligned}
> &(-\cos\theta)' = \sin\theta, \quad (\sec\theta)' = \sec\theta\tan\theta \\
> &2(-\cos\theta) - 3\sec\theta = -2\cos\theta - 3\sec\theta \\
> &\text{Check: } \frac{d}{d\theta}(-2\cos\theta - 3\sec\theta) = 2\sin\theta - 3\sec\theta\tan\theta \\[6pt]
> &\sec\theta \text{ is defined} \iff \cos\theta \ne 0 \iff \theta \ne n\pi + \tfrac{\pi}{2}
> \end{aligned}
> $$
> Hence $F(\theta) = -2\cos\theta - 3\sec\theta + C_n$ on each interval $(n\pi - \tfrac{\pi}{2}, n\pi + \tfrac{\pi}{2})$, $n$ an integer.
>
> \# The domain of $f$ is broken at every odd multiple of $\tfrac{\pi}{2}$, so it is infinitely many intervals, and each one gets its own constant, as in Exercise 17. Writing a single $C$ is the answer on one of these intervals.

### ST 3.9.21
Question: [[CAL1 HW 3.9 Questions#ST 3.9.21|ST 3.9.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &(-\cos\theta)' = \sin\theta, \quad (\tan\theta)' = \sec^2\theta \\
> &2(-\cos\theta) - \tan\theta = -2\cos\theta - \tan\theta \\
> &\text{Check: } \frac{d}{d\theta}(-2\cos\theta - \tan\theta) = 2\sin\theta - \sec^2\theta \\[6pt]
> &\text{domain: } \cos\theta \ne 0 \iff \theta \ne n\pi + \tfrac{\pi}{2}
> \end{aligned}
> $$
> Hence $H(\theta) = -2\cos\theta - \tan\theta + C_n$ on each interval $(n\pi - \tfrac{\pi}{2}, n\pi + \tfrac{\pi}{2})$, $n$ an integer.

### ST 3.9.23
Question: [[CAL1 HW 3.9 Questions#ST 3.9.23|ST 3.9.23]]

> [!solution] Solution
> $$
> \begin{aligned}
> &g(v) = v^{2/3} - 2\sec^2 v \\
> &\frac{v^{5/3}}{5/3} - 2\tan v = \tfrac{3}{5}v^{5/3} - 2\tan v \\
> &\text{Check: } \frac{d}{dv}\Big(\tfrac{3}{5}v^{5/3} - 2\tan v\Big) = v^{2/3} - 2\sec^2 v \\[6pt]
> &\text{domain: } \cos v \ne 0 \iff v \ne n\pi + \tfrac{\pi}{2}
> \end{aligned}
> $$
> Hence $G(v) = \tfrac{3}{5}v^{5/3} - 2\tan v + C_n$ on each interval $(n\pi - \tfrac{\pi}{2}, n\pi + \tfrac{\pi}{2})$, $n$ an integer.
>
> \# $\sqrt[3]{v^2} = v^{2/3}$ is defined for every $v$, also $v < 0$; only $\sec^2 v$ breaks the domain.

### ST 3.9.27
Question: [[CAL1 HW 3.9 Questions#ST 3.9.27|ST 3.9.27]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f''(x) = 24x \\
> &f'(x) = 24 \cdot \frac{x^2}{2} + C = 12x^2 + C \\
> &f(x) = 12 \cdot \frac{x^3}{3} + Cx + D = 4x^3 + Cx + D
> \end{aligned}
> $$
> Hence $f(x) = 4x^3 + Cx + D$, $C$ and $D$ arbitrary constants.
>
> \# Antidifferentiate twice, and add a new constant each time. The first constant $C$ is itself antidifferentiated in the second step, so it becomes $Cx$.

### ST 3.9.31
Question: [[CAL1 HW 3.9 Questions#ST 3.9.31|ST 3.9.31]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f''(x) = 4 - x^{1/3} \\
> &f'(x) = 4x - \frac{x^{4/3}}{4/3} + C = 4x - \tfrac{3}{4}x^{4/3} + C \\
> &f(x) = 4 \cdot \frac{x^2}{2} - \tfrac{3}{4} \cdot \frac{x^{7/3}}{7/3} + Cx + D = 2x^2 - \tfrac{9}{28}x^{7/3} + Cx + D
> \end{aligned}
> $$
> Hence $f(x) = 2x^2 - \tfrac{9}{28}x^{7/3} + Cx + D$.
>
> \# $\tfrac{3}{4} \cdot \tfrac{3}{7} = \tfrac{9}{28}$. Check: $f'(x) = 4x - \tfrac{9}{28} \cdot \tfrac{7}{3}x^{4/3} + C = 4x - \tfrac{3}{4}x^{4/3} + C$, and $f''(x) = 4 - x^{1/3}$.

### ST 3.9.37
Question: [[CAL1 HW 3.9 Questions#ST 3.9.37|ST 3.9.37]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f(x) = 5 \cdot \frac{x^{5/3}}{5/3} + C = 3x^{5/3} + C \\
> &f(8) = 3 \cdot 8^{5/3} + C = 3 \cdot 32 + C = 96 + C = 21 \implies C = -75
> \end{aligned}
> $$
> Hence $f(x) = 3x^{5/3} - 75$.
>
> \# $8^{5/3} = (\sqrt[3]{8})^5 = 2^5 = 32$: take the root first, then the power.

### ST 3.9.41
Question: [[CAL1 HW 3.9 Questions#ST 3.9.41|ST 3.9.41]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f'(x) = -2x + 6x^2 - 4x^3 + C \\
> &f'(0) = C = 12 \implies f'(x) = -2x + 6x^2 - 4x^3 + 12 \\[6pt]
> &f(x) = -x^2 + 2x^3 - x^4 + 12x + D \\
> &f(0) = D = 4
> \end{aligned}
> $$
> Hence $f(x) = -x^4 + 2x^3 - x^2 + 12x + 4$.
>
> \# Use $f'(0) = 12$ right after the first step, before antidifferentiating again: then the second step carries only one unknown constant.

### ST 3.9.43
Question: [[CAL1 HW 3.9 Questions#ST 3.9.43|ST 3.9.43]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f'(\theta) = -\cos\theta + \sin\theta + C \\
> &f'(0) = -1 + 0 + C = 4 \implies C = 5 \\[6pt]
> &f(\theta) = -\sin\theta - \cos\theta + 5\theta + D \\
> &f(0) = 0 - 1 + 0 + D = 3 \implies D = 4
> \end{aligned}
> $$
> Hence $f(\theta) = -\sin\theta - \cos\theta + 5\theta + 4$.
>
> \# $\cos 0 = 1$, so the conditions at $0$ do not give the constants directly as in Exercise 41: $C = 4 + 1$ and $D = 3 + 1$. Check: $f'(\theta) = -\cos\theta + \sin\theta + 5$, $f''(\theta) = \sin\theta + \cos\theta$.

### ST 3.9.49
Question: [[CAL1 HW 3.9 Questions#ST 3.9.49|ST 3.9.49]]

> [!solution] Solution
> $$
> \begin{aligned}
> &f'(x) = 3 - 4x \\
> &f(x) = 3x - 2x^2 + C \\
> &f(2) = 6 - 8 + C = 5 \implies C = 7 \\
> &f(x) = 3x - 2x^2 + 7
> \end{aligned}
> $$
> Hence $f(1) = 3 - 2 + 7 = 8$.
>
> \# The slope of the tangent line at $(x, f(x))$ is $f'(x)$, and "passes through $(2, 5)$" means $f(2) = 5$: this is Exercise 37 in words.

### ST 3.9.59
Question: [[CAL1 HW 3.9 Questions#ST 3.9.59|ST 3.9.59]]

> [!solution] Solution
> $$
> \begin{aligned}
> &s'(t) = v(t) = 2\cos t + 4\sin t \\
> &s(t) = 2\sin t - 4\cos t + C \\
> &s(0) = 0 - 4 + C = 3 \implies C = 7
> \end{aligned}
> $$
> Hence $s(t) = 2\sin t - 4\cos t + 7$.

### ST 3.9.61
Question: [[CAL1 HW 3.9 Questions#ST 3.9.61|ST 3.9.61]]

> [!solution] Solution
> $$
> \begin{aligned}
> &v'(t) = a(t) = 2t + 1 \\
> &v(t) = t^2 + t + C, \quad v(0) = C = -2 \\
> &v(t) = t^2 + t - 2 \\[6pt]
> &s(t) = \tfrac{1}{3}t^3 + \tfrac{1}{2}t^2 - 2t + D, \quad s(0) = D = 3
> \end{aligned}
> $$
> Hence $s(t) = \tfrac{1}{3}t^3 + \tfrac{1}{2}t^2 - 2t + 3$.
>
> \# Acceleration to velocity uses $v(0)$; velocity to position uses $s(0)$. Matching each condition to its step is the same as $f'(0)$ and $f(0)$ in Exercise 41.

### ST 3.9.66
Question: [[CAL1 HW 3.9 Questions#ST 3.9.66|ST 3.9.66]]

> [!proof] Proof
> Given $a(t) = a$ (a constant), $v(0) = v_0$, $s(0) = s_0$.
> $$
> \begin{aligned}
> &v'(t) = a(t) = a \implies v(t) = at + C \\
> &v(0) = C = v_0 \implies v(t) = at + v_0 \\[6pt]
> &s'(t) = v(t) = at + v_0 \implies s(t) = \tfrac{1}{2}at^2 + v_0 t + D \\
> &s(0) = D = s_0
> \end{aligned}
> $$
> Hence $s = \tfrac{1}{2}at^2 + v_0 t + s_0$. $\blacksquare$
>
> \# "$\implies v(t) = at + C$" is where the proof uses the fact that two functions with the same derivative on an interval differ by a constant: $at$ is one antiderivative of $a$, so every antiderivative, in particular $v$, is $at + C$. Without that fact we would only know that $at + v_0$ is *a* function with derivative $a$, not that it *is* $v$. Exercise 61 is this computation with $a(t) = 2t + 1$ in place of a constant.

### ST 3.9.69
Question: [[CAL1 HW 3.9 Questions#ST 3.9.69|ST 3.9.69]]

> [!solution] Solution
> Let $h$ be the height of the cliff, $s(t)$ the height of the stone above the ground $t$ seconds after it is dropped, upward positive.
> $$
> \begin{aligned}
> &a(t) = -9.8, \quad v(0) = 0 \ (\text{dropped}), \quad s(0) = h \\
> &v(t) = -9.8t \\
> &s(t) = -4.9t^2 + h \\[6pt]
> &\text{hits the ground with speed } 40\text{: } \lvert v(t_1) \rvert = 9.8t_1 = 40 \implies t_1 = \frac{40}{9.8} = \frac{200}{49} \\
> &s(t_1) = 0 \implies h = 4.9t_1^2 = 4.9 \cdot \Big(\frac{200}{49}\Big)^2 = \frac{4000}{49} \approx 81.6
> \end{aligned}
> $$
> Hence the cliff is $\tfrac{4000}{49} \approx 81.6$ m high.
>
> \# "Dropped" means the initial velocity is $0$. Speed is $\lvert v \rvert$: the velocity at impact is $-40$ m/s, because the stone moves down. Without solving for $t_1$: $h = 4.9t_1^2 = \dfrac{(9.8t_1)^2}{2 \cdot 9.8} = \dfrac{40^2}{19.6}$.
