---
course: [CAL1]
semester: "115-1"
chapter: ["4.5"]
tags: [calculus, homework, solutions, integrals]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §4.5, pp. 349-353, scanned PDF (the Substitution Rule, for indefinite and definite integrals)"
created: 2026-11-25
questions: "[[CAL1 HW 4.5 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 4.5 Questions#ST 4.5.5\|ST 4.5.5]] | $-\dfrac{1}{4(x^4 - 5)} + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.6\|ST 4.5.6]] | $-\tfrac{2}{3}\left(1 + \tfrac{1}{x}\right)^{3/2} + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.7\|ST 4.5.7]] | $2\sin\sqrt{t} + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.8\|ST 4.5.8]] | $\tfrac{2}{5}(z - 1)^{5/2} + \tfrac{2}{3}(z - 1)^{3/2} + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.9\|ST 4.5.9]] | $-\tfrac{1}{3}(1 - x^2)^{3/2} + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.11\|ST 4.5.11]] | $\tfrac{1}{3}\sin(x^3) + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.13\|ST 4.5.13]] | $-\tfrac{3}{\pi}\cos(\pi t/3) + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.15\|ST 4.5.15]] | $\tfrac{1}{3}\sec 3t + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.17\|ST 4.5.17]] | $\tfrac{1}{5}\sin(1 + 5t) + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.19\|ST 4.5.19]] | $-\tfrac{1}{4}\cos^4\theta + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.21\|ST 4.5.21]] | $\tfrac{1}{12}\left(x^2 + \tfrac{2}{x}\right)^6 + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.23\|ST 4.5.23]] | $\tfrac{2}{3}\sqrt{3ax + bx^3} + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.25\|ST 4.5.25]] | $\tfrac{1}{2}(1 + z^3)^{2/3} + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.27\|ST 4.5.27]] | $-\tfrac{2}{3}(\cot x)^{3/2} + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.29\|ST 4.5.29]] | $\tfrac{1}{3}\sec^3 x + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.31\|ST 4.5.31]] | $\tfrac{1}{40}(2x + 5)^{10} - \tfrac{5}{36}(2x + 5)^9 + C$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.41\|ST 4.5.41]] | $\tfrac{2}{\sqrt{3}} - 1 \approx 0.155$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.43\|ST 4.5.43]] | $0$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.45\|ST 4.5.45]] | $3$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.47\|ST 4.5.47]] | $\tfrac{2\sqrt{2} - 1}{3}a^3$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.48\|ST 4.5.48]] | $0$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.49\|ST 4.5.49]] | $\tfrac{16}{15}$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.51\|ST 4.5.51]] | $\tfrac{1}{2}(\sin 4 - \sin 1) \approx -0.799$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.59\|ST 4.5.59]] | $5$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.60\|ST 4.5.60]] | $2$ |
| [[CAL1 HW 4.5 Questions#ST 4.5.61\|ST 4.5.61]] | Proof; diagram of two mirror-image regions |
| [[CAL1 HW 4.5 Questions#ST 4.5.63\|ST 4.5.63]] | Proof |
| [[CAL1 HW 4.5 Questions#ST 4.5.64\|ST 4.5.64]] | Proof |
| [[CAL1 HW 4.5 Questions#ST 4.5.65\|ST 4.5.65]] | Proof |
| [[CAL1 HW 4.5 Questions#ST 4.5.85\|ST 4.5.85]] | $\tfrac{\pi^2}{4} \approx 2.467$ |

## ST §4.5 The Substitution Rule

> [!note] Note
> The facts that the answers use, each under its name.
> - **[[Substitution Rule]]**: if $u = g(x)$ is a differentiable function whose range is an interval $I$ and $f$ is continuous on $I$, then $\int f(g(x))\,g'(x)\,dx = \int f(u)\,du$. In practice: choose $u$ (usually the inside function, whose derivative also appears up to a constant factor), write $du = g'(x)\,dx$, rewrite the whole integrand in $u$ (a leftover $x$ too), integrate, and put $u = g(x)$ back.
> - **Substitution Rule for Definite Integrals**: if $g'$ is continuous on $[a, b]$ and $f$ is continuous on the range of $u = g(x)$, then $\int_a^b f(g(x))\,g'(x)\,dx = \int_{g(a)}^{g(b)} f(u)\,du$. The limits become the values of $u$ at $x = a$ and $x = b$, and there is no return to $x$.
> - **[[Integrals of Symmetric Functions]]** (textbook p. 354, not in the scan): let $f$ be continuous on $[-a, a]$. If $f$ is even, $f(-x) = f(x)$, then $\int_{-a}^{a} f(x)\,dx = 2\int_0^a f(x)\,dx$. If $f$ is odd, $f(-x) = -f(x)$, then $\int_{-a}^{a} f(x)\,dx = 0$.
> - **Limits and the variable**: $\int_q^p f(u)\,du = -\int_p^q f(u)\,du$, and the letter of the variable does not matter: $\int_a^b f(u)\,du = \int_a^b f(x)\,dx$.
> - **Antiderivatives**: $u^n \to \dfrac{u^{n+1}}{n+1}$ ($n \ne -1$), $\sin u \to -\cos u$, $\cos u \to \sin u$, $\sec u\tan u \to \sec u$; and, from Chapter 6 (Exercise 85 only), $\dfrac{1}{1 + u^2} \to \arctan u$.
> - **Identities**: $\sin(\pi - u) = \sin u$, $\cos(\tfrac{\pi}{2} - u) = \sin u$, $\cos^2 x = 1 - \sin^2 x$.
> - Each answer is written as on an exam paper: the substitution ($u$, $du$, and for a definite integral the new limits), the computation, then the conclusion on a Hence line. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 4.5.5
Question: [[CAL1 HW 4.5 Questions#ST 4.5.5|ST 4.5.5]]

> [!solution] Solution
> Let $u = x^4 - 5$. Then $du = 4x^3\,dx$, so $x^3\,dx = \tfrac{1}{4}\,du$.
> $$
> \begin{aligned}
> \int \frac{x^3}{(x^4 - 5)^2}\,dx &= \int \frac{1}{u^2} \cdot \frac{1}{4}\,du = \frac{1}{4}\int u^{-2}\,du \\
> &= \frac{1}{4} \cdot \frac{u^{-1}}{-1} + C = -\frac{1}{4u} + C
> \end{aligned}
> $$
> Hence $\int \dfrac{x^3}{(x^4 - 5)^2}\,dx = -\dfrac{1}{4(x^4 - 5)} + C$.
>
> \# The numerator $x^3$ is the derivative of the inside $x^4 - 5$ up to the factor $4$: that is the sign that this $u$ works. At the end, $u$ goes back to $x^4 - 5$.

### ST 4.5.6
Question: [[CAL1 HW 4.5 Questions#ST 4.5.6|ST 4.5.6]]

> [!solution] Solution
> Let $u = 1 + \tfrac{1}{x}$. Then $du = -\tfrac{1}{x^2}\,dx$, so $\tfrac{1}{x^2}\,dx = -du$.
> $$
> \begin{aligned}
> \int \frac{1}{x^2}\sqrt{1 + \frac{1}{x}}\,dx &= \int \sqrt{u}\,(-du) = -\int u^{1/2}\,du \\
> &= -\frac{u^{3/2}}{3/2} + C = -\frac{2}{3}u^{3/2} + C
> \end{aligned}
> $$
> Hence $\int \dfrac{1}{x^2}\sqrt{1 + \dfrac{1}{x}}\,dx = -\tfrac{2}{3}\left(1 + \tfrac{1}{x}\right)^{3/2} + C$.
>
> \# $\left(\tfrac{1}{x}\right)' = (x^{-1})' = -x^{-2}$, so the minus sign goes with $du$.

### ST 4.5.7
Question: [[CAL1 HW 4.5 Questions#ST 4.5.7|ST 4.5.7]]

> [!solution] Solution
> Let $u = \sqrt{t}$. Then $du = \dfrac{1}{2\sqrt{t}}\,dt$, so $\dfrac{dt}{\sqrt{t}} = 2\,du$.
> $$
> \int \frac{\cos\sqrt{t}}{\sqrt{t}}\,dt = \int \cos u \cdot 2\,du = 2\sin u + C
> $$
> Hence $\int \dfrac{\cos\sqrt{t}}{\sqrt{t}}\,dt = 2\sin\sqrt{t} + C$ $(t > 0)$.
>
> \# The $\tfrac{1}{\sqrt{t}}$ in the integrand is $du$ up to the factor $2$, because $(\sqrt{t})' = \tfrac{1}{2\sqrt{t}}$.

### ST 4.5.8
Question: [[CAL1 HW 4.5 Questions#ST 4.5.8|ST 4.5.8]]

> [!solution] Solution
> Let $u = z - 1$. Then $du = dz$ and $z = u + 1$.
> $$
> \begin{aligned}
> \int z\sqrt{z - 1}\,dz &= \int (u + 1)\,u^{1/2}\,du = \int \left(u^{3/2} + u^{1/2}\right)du \\
> &= \frac{2}{5}u^{5/2} + \frac{2}{3}u^{3/2} + C
> \end{aligned}
> $$
> Hence $\int z\sqrt{z - 1}\,dz = \tfrac{2}{5}(z - 1)^{5/2} + \tfrac{2}{3}(z - 1)^{3/2} + C$.
>
> \# Here $du = dz$ uses up nothing, so the extra factor $z$ must also be written in $u$, from $u = z - 1$. Then expand and use the power rule, as in Example 5 of the textbook ($x^2 = u - 1$).

### ST 4.5.9
Question: [[CAL1 HW 4.5 Questions#ST 4.5.9|ST 4.5.9]]

> [!solution] Solution
> Let $u = 1 - x^2$. Then $du = -2x\,dx$, so $x\,dx = -\tfrac{1}{2}\,du$.
> $$
> \int x\sqrt{1 - x^2}\,dx = -\frac{1}{2}\int u^{1/2}\,du = -\frac{1}{2} \cdot \frac{2}{3}u^{3/2} + C = -\frac{1}{3}u^{3/2} + C
> $$
> Hence $\int x\sqrt{1 - x^2}\,dx = -\tfrac{1}{3}(1 - x^2)^{3/2} + C$.
>
> \# $x$ is the derivative of $1 - x^2$ up to the factor $-2$.

### ST 4.5.11
Question: [[CAL1 HW 4.5 Questions#ST 4.5.11|ST 4.5.11]]

> [!solution] Solution
> Let $u = x^3$. Then $du = 3x^2\,dx$, so $x^2\,dx = \tfrac{1}{3}\,du$.
> $$
> \int x^2\cos(x^3)\,dx = \frac{1}{3}\int \cos u\,du = \frac{1}{3}\sin u + C
> $$
> Hence $\int x^2\cos(x^3)\,dx = \tfrac{1}{3}\sin(x^3) + C$.
>
> \# Take $u$ = the inside of $\cos$; its derivative $3x^2$ is the other factor up to $3$.

### ST 4.5.13
Question: [[CAL1 HW 4.5 Questions#ST 4.5.13|ST 4.5.13]]

> [!solution] Solution
> Let $u = \tfrac{\pi t}{3}$. Then $du = \tfrac{\pi}{3}\,dt$, so $dt = \tfrac{3}{\pi}\,du$.
> $$
> \int \sin(\pi t/3)\,dt = \frac{3}{\pi}\int \sin u\,du = -\frac{3}{\pi}\cos u + C
> $$
> Hence $\int \sin(\pi t/3)\,dt = -\tfrac{3}{\pi}\cos(\pi t/3) + C$.
>
> \# A linear inside function $kt$ only brings the constant $\tfrac{1}{k}$: if $F' = f$, then $\int f(kt)\,dt = \tfrac{1}{k}F(kt) + C$. Exercises 15 and 17 work the same way.

### ST 4.5.15
Question: [[CAL1 HW 4.5 Questions#ST 4.5.15|ST 4.5.15]]

> [!solution] Solution
> Let $u = 3t$. Then $du = 3\,dt$, so $dt = \tfrac{1}{3}\,du$.
> $$
> \int \sec 3t\tan 3t\,dt = \frac{1}{3}\int \sec u\tan u\,du = \frac{1}{3}\sec u + C
> $$
> Hence $\int \sec 3t\tan 3t\,dt = \tfrac{1}{3}\sec 3t + C$.
>
> \# $(\sec u)' = \sec u\tan u$.

### ST 4.5.17
Question: [[CAL1 HW 4.5 Questions#ST 4.5.17|ST 4.5.17]]

> [!solution] Solution
> Let $u = 1 + 5t$. Then $du = 5\,dt$, so $dt = \tfrac{1}{5}\,du$.
> $$
> \int \cos(1 + 5t)\,dt = \frac{1}{5}\int \cos u\,du = \frac{1}{5}\sin u + C
> $$
> Hence $\int \cos(1 + 5t)\,dt = \tfrac{1}{5}\sin(1 + 5t) + C$.
>
> \# The constant $1$ in $1 + 5t$ does not change $du$.

### ST 4.5.19
Question: [[CAL1 HW 4.5 Questions#ST 4.5.19|ST 4.5.19]]

> [!solution] Solution
> Let $u = \cos\theta$. Then $du = -\sin\theta\,d\theta$, so $\sin\theta\,d\theta = -du$.
> $$
> \int \cos^3\theta\,\sin\theta\,d\theta = \int u^3\,(-du) = -\frac{u^4}{4} + C
> $$
> Hence $\int \cos^3\theta\,\sin\theta\,d\theta = -\tfrac{1}{4}\cos^4\theta + C$.
>
> \# $\cos^3\theta$ means $(\cos\theta)^3$. Choose $u = \cos\theta$ because its derivative $-\sin\theta$ is the other factor.

### ST 4.5.21
Question: [[CAL1 HW 4.5 Questions#ST 4.5.21|ST 4.5.21]]

> [!solution] Solution
> Let $u = x^2 + \tfrac{2}{x}$. Then $du = \left(2x - \tfrac{2}{x^2}\right)dx = 2\left(x - \tfrac{1}{x^2}\right)dx$, so $\left(x - \tfrac{1}{x^2}\right)dx = \tfrac{1}{2}\,du$.
> $$
> \int \left(x - \frac{1}{x^2}\right)\left(x^2 + \frac{2}{x}\right)^5 dx = \frac{1}{2}\int u^5\,du = \frac{1}{2} \cdot \frac{u^6}{6} + C = \frac{1}{12}u^6 + C
> $$
> Hence $\int \left(x - \tfrac{1}{x^2}\right)\left(x^2 + \tfrac{2}{x}\right)^5 dx = \tfrac{1}{12}\left(x^2 + \tfrac{2}{x}\right)^6 + C$.
>
> \# Expanding the fifth power would be hopeless. The first factor is half the derivative of the inside: $\left(\tfrac{2}{x}\right)' = (2x^{-1})' = -\tfrac{2}{x^2}$. The answer holds on each interval with $x \ne 0$.

### ST 4.5.23
Question: [[CAL1 HW 4.5 Questions#ST 4.5.23|ST 4.5.23]]

> [!solution] Solution
> Let $u = 3ax + bx^3$. Then $du = (3a + 3bx^2)\,dx = 3(a + bx^2)\,dx$, so $(a + bx^2)\,dx = \tfrac{1}{3}\,du$.
> $$
> \int \frac{a + bx^2}{\sqrt{3ax + bx^3}}\,dx = \frac{1}{3}\int u^{-1/2}\,du = \frac{1}{3} \cdot 2u^{1/2} + C = \frac{2}{3}u^{1/2} + C
> $$
> Hence $\int \dfrac{a + bx^2}{\sqrt{3ax + bx^3}}\,dx = \tfrac{2}{3}\sqrt{3ax + bx^3} + C$.
>
> \# $a$ and $b$ are constants. The numerator is the derivative of the expression under the root up to the factor $3$.

### ST 4.5.25
Question: [[CAL1 HW 4.5 Questions#ST 4.5.25|ST 4.5.25]]

> [!solution] Solution
> Let $u = 1 + z^3$. Then $du = 3z^2\,dz$, so $z^2\,dz = \tfrac{1}{3}\,du$.
> $$
> \int \frac{z^2}{\sqrt[3]{1 + z^3}}\,dz = \frac{1}{3}\int u^{-1/3}\,du = \frac{1}{3} \cdot \frac{u^{2/3}}{2/3} + C = \frac{1}{2}u^{2/3} + C
> $$
> Hence $\int \dfrac{z^2}{\sqrt[3]{1 + z^3}}\,dz = \tfrac{1}{2}(1 + z^3)^{2/3} + C$.
>
> \# $\dfrac{1}{\sqrt[3]{u}} = u^{-1/3}$, and $-\tfrac{1}{3} + 1 = \tfrac{2}{3}$.

### ST 4.5.27
Question: [[CAL1 HW 4.5 Questions#ST 4.5.27|ST 4.5.27]]

> [!solution] Solution
> Let $u = \cot x$. Then $du = -\csc^2 x\,dx$, so $\csc^2 x\,dx = -du$.
> $$
> \int \sqrt{\cot x}\,\csc^2 x\,dx = -\int u^{1/2}\,du = -\frac{2}{3}u^{3/2} + C
> $$
> Hence $\int \sqrt{\cot x}\,\csc^2 x\,dx = -\tfrac{2}{3}(\cot x)^{3/2} + C$.
>
> \# $(\cot x)' = -\csc^2 x$. The answer holds on each interval where $\cot x > 0$.

### ST 4.5.29
Question: [[CAL1 HW 4.5 Questions#ST 4.5.29|ST 4.5.29]]

> [!solution] Solution
> $\sec^3 x\tan x = \sec^2 x \cdot \sec x\tan x$. Let $u = \sec x$. Then $du = \sec x\tan x\,dx$.
> $$
> \int \sec^3 x\tan x\,dx = \int \sec^2 x \cdot \sec x\tan x\,dx = \int u^2\,du = \frac{u^3}{3} + C
> $$
> Hence $\int \sec^3 x\tan x\,dx = \tfrac{1}{3}\sec^3 x + C$.
>
> \# Split off $\sec x\tan x$, the derivative of $\sec x$; what is left is a power of $\sec x$.

### ST 4.5.31
Question: [[CAL1 HW 4.5 Questions#ST 4.5.31|ST 4.5.31]]

> [!solution] Solution
> Let $u = 2x + 5$. Then $du = 2\,dx$, $dx = \tfrac{1}{2}\,du$, and $x = \tfrac{u - 5}{2}$.
> $$
> \begin{aligned}
> \int x(2x + 5)^8\,dx &= \int \frac{u - 5}{2} \cdot u^8 \cdot \frac{1}{2}\,du = \frac{1}{4}\int \left(u^9 - 5u^8\right)du \\
> &= \frac{1}{4}\left(\frac{u^{10}}{10} - \frac{5u^9}{9}\right) + C = \frac{1}{40}u^{10} - \frac{5}{36}u^9 + C
> \end{aligned}
> $$
> Hence $\int x(2x + 5)^8\,dx = \tfrac{1}{40}(2x + 5)^{10} - \tfrac{5}{36}(2x + 5)^9 + C$.
>
> \# As in Exercise 8, the extra factor $x$ is written in $u$. Expanding $(2x + 5)^8$ instead would give nine terms.

### ST 4.5.41
Question: [[CAL1 HW 4.5 Questions#ST 4.5.41|ST 4.5.41]]

> [!solution] Solution
> Let $u = \cos t$. Then $du = -\sin t\,dt$. When $t = 0$, $u = 1$; when $t = \tfrac{\pi}{6}$, $u = \tfrac{\sqrt{3}}{2}$.
> $$
> \begin{aligned}
> \int_0^{\pi/6} \frac{\sin t}{\cos^2 t}\,dt &= \int_1^{\sqrt{3}/2} \frac{-du}{u^2} = \int_{\sqrt{3}/2}^{1} u^{-2}\,du \\
> &= \Big[-\frac{1}{u}\Big]_{\sqrt{3}/2}^{1} = -1 + \frac{2}{\sqrt{3}}
> \end{aligned}
> $$
> Hence $\int_0^{\pi/6} \dfrac{\sin t}{\cos^2 t}\,dt = \tfrac{2}{\sqrt{3}} - 1 = \tfrac{2\sqrt{3} - 3}{3} \approx 0.155$.
>
> \# Reversing the limits, $\int_1^{\sqrt{3}/2} = -\int_{\sqrt{3}/2}^{1}$, cancels the minus sign of $du$. Check: $\tfrac{\sin t}{\cos^2 t} = \sec t\tan t$, so the integral is $\Big[\sec t\Big]_0^{\pi/6} = \tfrac{2}{\sqrt{3}} - 1$.

### ST 4.5.43
Question: [[CAL1 HW 4.5 Questions#ST 4.5.43|ST 4.5.43]]

> [!solution] Solution
> $f(x) = x^3 + x^4\tan x$ is continuous on $[-\tfrac{\pi}{4}, \tfrac{\pi}{4}]$ ($\cos x > 0$ there), and
> $$
> f(-x) = (-x)^3 + (-x)^4\tan(-x) = -x^3 - x^4\tan x = -f(x)
> $$
> so $f$ is odd. Hence $\int_{-\pi/4}^{\pi/4} (x^3 + x^4\tan x)\,dx = 0$.
>
> \# We have no antiderivative of $x^4\tan x$, so the symmetry is the way in. Why an odd function gives $0$: by Exercise 61 with $a = 0$ and $b = \tfrac{\pi}{4}$, $\int_{-\pi/4}^{0} f(x)\,dx = \int_0^{\pi/4} f(-x)\,dx = -\int_0^{\pi/4} f(x)\,dx$, so the two halves cancel.

### ST 4.5.45
Question: [[CAL1 HW 4.5 Questions#ST 4.5.45|ST 4.5.45]]

> [!solution] Solution
> Let $u = 1 + 2x$. Then $du = 2\,dx$. When $x = 0$, $u = 1$; when $x = 13$, $u = 27$.
> $$
> \int_0^{13} \frac{dx}{\sqrt[3]{(1 + 2x)^2}} = \frac{1}{2}\int_1^{27} u^{-2/3}\,du = \frac{1}{2}\Big[3u^{1/3}\Big]_1^{27} = \frac{3}{2}(3 - 1) = 3
> $$
> Hence $\int_0^{13} \dfrac{dx}{\sqrt[3]{(1 + 2x)^2}} = 3$.
>
> \# $\sqrt[3]{u^2} = u^{2/3}$, $-\tfrac{2}{3} + 1 = \tfrac{1}{3}$, and $\sqrt[3]{27} = 3$.

### ST 4.5.47
Question: [[CAL1 HW 4.5 Questions#ST 4.5.47|ST 4.5.47]]

> [!solution] Solution
> Let $u = x^2 + a^2$. Then $du = 2x\,dx$. When $x = 0$, $u = a^2$; when $x = a$, $u = 2a^2$.
> $$
> \begin{aligned}
> \int_0^a x\sqrt{x^2 + a^2}\,dx &= \frac{1}{2}\int_{a^2}^{2a^2} u^{1/2}\,du = \frac{1}{3}\Big[u^{3/2}\Big]_{a^2}^{2a^2} \\
> &= \frac{1}{3}\left((2a^2)^{3/2} - (a^2)^{3/2}\right) = \frac{1}{3}\left(2\sqrt{2}\,a^3 - a^3\right)
> \end{aligned}
> $$
> Hence $\int_0^a x\sqrt{x^2 + a^2}\,dx = \tfrac{2\sqrt{2} - 1}{3}a^3$.
>
> \# $a$ is a constant, so $a^2$ does not change $du$. $a > 0$ is used in $(a^2)^{3/2} = a^3$ and $(2a^2)^{3/2} = 2\sqrt{2}\,a^3$.

### ST 4.5.48
Question: [[CAL1 HW 4.5 Questions#ST 4.5.48|ST 4.5.48]]

> [!solution] Solution
> $f(x) = x^4\sin x$ is continuous on $[-\tfrac{\pi}{3}, \tfrac{\pi}{3}]$, and
> $$
> f(-x) = (-x)^4\sin(-x) = -x^4\sin x = -f(x)
> $$
> so $f$ is odd. Hence $\int_{-\pi/3}^{\pi/3} x^4\sin x\,dx = 0$.
>
> \# $x^4$ is even and $\sin x$ is odd, and even times odd is odd. Substitution does not give an antiderivative here; the symmetry does the work, as in Exercise 43.

### ST 4.5.49
Question: [[CAL1 HW 4.5 Questions#ST 4.5.49|ST 4.5.49]]

> [!solution] Solution
> Let $u = x - 1$. Then $du = dx$ and $x = u + 1$. When $x = 1$, $u = 0$; when $x = 2$, $u = 1$.
> $$
> \begin{aligned}
> \int_1^2 x\sqrt{x - 1}\,dx &= \int_0^1 (u + 1)\,u^{1/2}\,du = \int_0^1 \left(u^{3/2} + u^{1/2}\right)du \\
> &= \Big[\tfrac{2}{5}u^{5/2} + \tfrac{2}{3}u^{3/2}\Big]_0^1 = \frac{2}{5} + \frac{2}{3} = \frac{16}{15}
> \end{aligned}
> $$
> Hence $\int_1^2 x\sqrt{x - 1}\,dx = \tfrac{16}{15}$.
>
> \# The same integrand as Exercise 8, now with limits: change them to $u$ and never go back to $x$.

### ST 4.5.51
Question: [[CAL1 HW 4.5 Questions#ST 4.5.51|ST 4.5.51]]

> [!solution] Solution
> Let $u = x^{-2}$. Then $du = -2x^{-3}\,dx$, so $\dfrac{dx}{x^3} = -\tfrac{1}{2}\,du$. When $x = \tfrac{1}{2}$, $u = 4$; when $x = 1$, $u = 1$.
> $$
> \begin{aligned}
> \int_{1/2}^{1} \frac{\cos(x^{-2})}{x^3}\,dx &= -\frac{1}{2}\int_4^1 \cos u\,du = \frac{1}{2}\int_1^4 \cos u\,du \\
> &= \frac{1}{2}\Big[\sin u\Big]_1^4 = \frac{1}{2}(\sin 4 - \sin 1)
> \end{aligned}
> $$
> Hence $\int_{1/2}^{1} \dfrac{\cos(x^{-2})}{x^3}\,dx = \tfrac{1}{2}(\sin 4 - \sin 1) \approx -0.799$.
>
> \# $\left(\tfrac{1}{2}\right)^{-2} = 2^2 = 4$. The numbers $4$ and $1$ are radians.

### ST 4.5.59
Question: [[CAL1 HW 4.5 Questions#ST 4.5.59|ST 4.5.59]]

> [!solution] Solution
> Let $u = 2x$. Then $du = 2\,dx$. When $x = 0$, $u = 0$; when $x = 2$, $u = 4$.
> $$
> \int_0^2 f(2x)\,dx = \frac{1}{2}\int_0^4 f(u)\,du = \frac{1}{2} \cdot 10 = 5
> $$
> Hence $\int_0^2 f(2x)\,dx = 5$.
>
> \# $\int_0^4 f(u)\,du = \int_0^4 f(x)\,dx = 10$: only the letter changed. The rule applies because $f$ is continuous.

### ST 4.5.60
Question: [[CAL1 HW 4.5 Questions#ST 4.5.60|ST 4.5.60]]

> [!solution] Solution
> Let $u = x^2$. Then $du = 2x\,dx$. When $x = 0$, $u = 0$; when $x = 3$, $u = 9$.
> $$
> \int_0^3 xf(x^2)\,dx = \frac{1}{2}\int_0^9 f(u)\,du = \frac{1}{2} \cdot 4 = 2
> $$
> Hence $\int_0^3 xf(x^2)\,dx = 2$.
>
> \# The factor $x$ is what makes $u = x^2$ work: $x\,dx = \tfrac{1}{2}\,du$.

### ST 4.5.61
Question: [[CAL1 HW 4.5 Questions#ST 4.5.61|ST 4.5.61]]

> [!proof] Proof
> Let $u = -x$. Then $du = -dx$. When $x = a$, $u = -a$; when $x = b$, $u = -b$. The Substitution Rule for Definite Integrals applies because $u' = -1$ is continuous and $f$ is continuous on $\mathbb{R}$.
> $$
> \begin{aligned}
> \int_a^b f(-x)\,dx &= \int_{-a}^{-b} f(u)\,(-du) = -\int_{-a}^{-b} f(u)\,du \\
> &= \int_{-b}^{-a} f(u)\,du = \int_{-b}^{-a} f(x)\,dx \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Third equality: reversing the limits changes the sign, which cancels the minus sign from $du$. Last equality: renaming $u$ as $x$ changes nothing.

> [!solution] Solution
> ![ST 4.5.61 figure|440](../Attachments/CAL1%20HW%204.5%20Solutions%20fig%2061.png)
>
> Let $f(x) \ge 0$ and $0 < a < b$. The right side $\int_{-b}^{-a} f(x)\,dx$ is the area under $y = f(x)$ from $x = -b$ to $x = -a$ (blue). The left side $\int_a^b f(-x)\,dx$ is the area under $y = f(-x)$ from $x = a$ to $x = b$ (red). The graph of $y = f(-x)$ is the reflection of the graph of $y = f(x)$ in the $y$-axis, and this reflection carries the blue region onto the red one. A reflection does not change area, so the two areas are equal.
>
> \# The point $(x, y)$ on $y = f(x)$ goes to $(-x, y)$, which lies on $y = f(-x)$ because $f(-(-x)) = f(x) = y$; and $-b \le x \le -a$ becomes $a \le -x \le b$.

### ST 4.5.63
Question: [[CAL1 HW 4.5 Questions#ST 4.5.63|ST 4.5.63]]

> [!proof] Proof
> Let $u = 1 - x$. Then $du = -dx$ and $x = 1 - u$. When $x = 0$, $u = 1$; when $x = 1$, $u = 0$. Since $a > 0$ and $b > 0$, $x^a(1 - x)^b$ is continuous on $[0, 1]$, and $u' = -1$ is continuous, so the Substitution Rule for Definite Integrals applies.
> $$
> \begin{aligned}
> \int_0^1 x^a(1 - x)^b\,dx &= \int_1^0 (1 - u)^a\,u^b\,(-du) = \int_0^1 u^b(1 - u)^a\,du \\
> &= \int_0^1 x^b(1 - x)^a\,dx \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The substitution exchanges the roles of $x$ and $1 - x$: $x$ becomes $1 - u$ and $1 - x$ becomes $u$. $a > 0$ makes $x^a$ continuous at $x = 0$ ($0^a = 0$); for $a < 0$ it would blow up there.

### ST 4.5.64
Question: [[CAL1 HW 4.5 Questions#ST 4.5.64|ST 4.5.64]]

> [!proof] Proof
> Let $I = \int_0^\pi xf(\sin x)\,dx$. Since $0 \le \sin x \le 1$ for $0 \le x \le \pi$ and $f$ is continuous on $[0, \pi]$, $f(\sin x)$ is continuous on $[0, \pi]$.
>
> Let $u = \pi - x$. Then $du = -dx$, $x = \pi - u$, and $\sin x = \sin(\pi - u) = \sin u$. When $x = 0$, $u = \pi$; when $x = \pi$, $u = 0$.
> $$
> \begin{aligned}
> I &= \int_\pi^0 (\pi - u)\,f(\sin u)\,(-du) = \int_0^\pi (\pi - u)\,f(\sin u)\,du \\
> &= \pi\int_0^\pi f(\sin u)\,du - \int_0^\pi uf(\sin u)\,du = \pi\int_0^\pi f(\sin x)\,dx - I \\
> &\implies 2I = \pi\int_0^\pi f(\sin x)\,dx \\
> &\implies \int_0^\pi xf(\sin x)\,dx = \frac{\pi}{2}\int_0^\pi f(\sin x)\,dx \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The key step: after the substitution, the same integral $I$ comes back on the right side (rename $u$ as $x$), so move it to the left and solve for $I$ like an equation. $\sin(\pi - u) = \sin\pi\cos u - \cos\pi\sin u = \sin u$.

### ST 4.5.65
Question: [[CAL1 HW 4.5 Questions#ST 4.5.65|ST 4.5.65]]

> [!proof] Proof
> Let $u = \tfrac{\pi}{2} - x$. Then $du = -dx$ and $\cos x = \cos(\tfrac{\pi}{2} - u) = \sin u$. When $x = 0$, $u = \tfrac{\pi}{2}$; when $x = \tfrac{\pi}{2}$, $u = 0$. Since $f$ is continuous, $f(\cos x)$ and $f(\sin u)$ are continuous, and $u' = -1$ is continuous.
> $$
> \begin{aligned}
> \int_0^{\pi/2} f(\cos x)\,dx &= \int_{\pi/2}^{0} f(\sin u)\,(-du) = \int_0^{\pi/2} f(\sin u)\,du \\
> &= \int_0^{\pi/2} f(\sin x)\,dx \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $\cos(\tfrac{\pi}{2} - u) = \cos\tfrac{\pi}{2}\cos u + \sin\tfrac{\pi}{2}\sin u = \sin u$. In pictures: $\cos x = \sin(\tfrac{\pi}{2} - x)$, so the graph of $f(\cos x)$ on $[0, \tfrac{\pi}{2}]$ is the graph of $f(\sin x)$ reflected in the line $x = \tfrac{\pi}{4}$, with the same area.

### ST 4.5.85
Question: [[CAL1 HW 4.5 Questions#ST 4.5.85|ST 4.5.85]]

> [!solution] Solution
> $1 + \cos^2 x = 2 - \sin^2 x$, so $\dfrac{x\sin x}{1 + \cos^2 x} = xf(\sin x)$ with $f(t) = \dfrac{t}{2 - t^2}$, which is continuous for $0 \le t \le 1$ ($2 - t^2 \ge 1$). By Exercise 64,
> $$
> \int_0^\pi \frac{x\sin x}{1 + \cos^2 x}\,dx = \frac{\pi}{2}\int_0^\pi \frac{\sin x}{1 + \cos^2 x}\,dx
> $$
> Let $u = \cos x$. Then $du = -\sin x\,dx$. When $x = 0$, $u = 1$; when $x = \pi$, $u = -1$.
> $$
> \begin{aligned}
> \frac{\pi}{2}\int_0^\pi \frac{\sin x}{1 + \cos^2 x}\,dx &= \frac{\pi}{2}\int_1^{-1} \frac{-du}{1 + u^2} = \frac{\pi}{2}\int_{-1}^{1} \frac{du}{1 + u^2} \\
> &= \frac{\pi}{2}\Big[\arctan u\Big]_{-1}^{1} = \frac{\pi}{2}\left(\frac{\pi}{4} - \left(-\frac{\pi}{4}\right)\right) = \frac{\pi^2}{4}
> \end{aligned}
> $$
> Hence $\int_0^\pi \dfrac{x\sin x}{1 + \cos^2 x}\,dx = \tfrac{\pi^2}{4} \approx 2.467$.
>
> \# Exercise 64 needs a function of $\sin x$ alone, so first trade $\cos^2 x$ for $1 - \sin^2 x$. Exercise 64 assumes $f$ continuous on $[0, \pi]$, but its proof only uses $f(\sin x)$, and $0 \le \sin x \le 1$; this $f$ is continuous on $[0, 1]$ (it fails only at $t = \sqrt{2} \approx 1.41$, which $\sin x$ never reaches). $(\arctan u)' = \dfrac{1}{1 + u^2}$ is from Chapter 6, and $\arctan 1 = \tfrac{\pi}{4}$, $\arctan(-1) = -\tfrac{\pi}{4}$.
