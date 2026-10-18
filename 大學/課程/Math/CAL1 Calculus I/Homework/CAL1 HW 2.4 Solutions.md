---
course: [CAL1]
semester: "115-1"
chapter: ["2.4"]
tags: [calculus, homework, solutions, derivatives, limits]
source:
  - "Own solutions; computations checked with sympy"
  - "Stewart, Calculus, §2.4, pp. 148-155, scanned PDF (formulas and equation numbers)"
  - "Past CYCU Calculus I midterm exams (107-1, 113-1, 114-1), used to choose the additional exercises"
created: 2026-10-18
questions: "[[CAL1 HW 2.4 Questions]]"
up: "[[CAL1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 2.4 Questions#ST 2.4.9\|ST 2.4.9]] | $f'(\theta) = \sin\theta + \sin^{2}\theta + \theta\cos\theta - \cos^{2}\theta$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.13\|ST 2.4.13]] | $f'(\theta) = \dfrac{1}{1 + \cos\theta}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.15\|ST 2.4.15]] | $y' = \dfrac{2 - \tan x + x\sec^{2}x}{(2 - \tan x)^{2}}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.17\|ST 2.4.17]] | $f'(w) = \dfrac{2\sec w\tan w}{(1 - \sec w)^{2}}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.19\|ST 2.4.19]] | $y' = \dfrac{\sin t + t\cos t + t^{2}\cos t}{(1 + t)^{2}}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.21\|ST 2.4.21]] | $f'(\theta) = \sin\theta\cos\theta + \theta(\cos^{2}\theta - \sin^{2}\theta)$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.23\|ST 2.4.23]] | Proof |
| [[CAL1 HW 2.4 Questions#ST 2.4.25\|ST 2.4.25]] | Proof |
| [[CAL1 HW 2.4 Questions#ST 2.4.29\|ST 2.4.29]] | $y = 2x - \pi$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.35\|ST 2.4.35]] | $g'(\theta) = \dfrac{\theta\cos\theta - \sin\theta}{\theta^{2}}$, $g''(\theta) = \dfrac{2\sin\theta - 2\theta\cos\theta - \theta^{2}\sin\theta}{\theta^{3}}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.38\|ST 2.4.38]] | (a) $2 - \sqrt{3}$; (b) $\dfrac{1 - 2\sqrt{3}}{16}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.41\|ST 2.4.41]] | (a) $v = 8\cos t$, $a = -8\sin t$; (b) $x = 4\sqrt{3}$ cm, $v = -4$ cm/s, $a = -4\sqrt{3}$ cm/s², moving to the left |
| [[CAL1 HW 2.4 Questions#ST 2.4.43\|ST 2.4.43]] | $\dfrac{dx}{d\theta} = 3$ m/rad |
| [[CAL1 HW 2.4 Questions#ST 2.4.47\|ST 2.4.47]] | $3$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.49\|ST 2.4.49]] | $0$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.51\|ST 2.4.51]] | $2$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.53\|ST 2.4.53]] | $-\tfrac{3}{4}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.55\|ST 2.4.55]] | $\tfrac{1}{2}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.57\|ST 2.4.57]] | $-\tfrac{1}{4}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.59\|ST 2.4.59]] | $-\sqrt{2}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.61\|ST 2.4.61]] | $-\cos x$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.67\|ST 2.4.67]] | $1$ |

Additional exercises, not assigned:

| Exercise | Answer |
| --- | --- |
| [[CAL1 HW 2.4 Questions#ST 2.4.26\|ST 2.4.26]] | Proof |
| [[CAL1 HW 2.4 Questions#ST 2.4.40\|ST 2.4.40]] | $\left(\tfrac{7\pi}{6} + 2n\pi, -\tfrac{\sqrt{3}}{3}\right)$ and $\left(\tfrac{11\pi}{6} + 2n\pi, \tfrac{\sqrt{3}}{3}\right)$, $n$ an integer |
| [[CAL1 HW 2.4 Questions#ST 2.4.52\|ST 2.4.52]] | $\tfrac{1}{7}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.56\|ST 2.4.56]] | $1$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.60\|ST 2.4.60]] | $\tfrac{1}{3}$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.62\|ST 2.4.62]] | $-x\cos x - 35\sin x$ |
| [[CAL1 HW 2.4 Questions#ST 2.4.63\|ST 2.4.63]] | $A = -\tfrac{3}{10}$, $B = -\tfrac{1}{10}$ |

## ST §2.4 Derivatives of Trigonometric Functions

> [!note] Note
> The facts that the answers use, each under its name. An answer writes the formula itself; the numbers are those of ST §2.4 and matter only where a question names them.
> - **[[Derivatives of Trigonometric Functions]]** ($x$ in radians):
> $$
> \begin{array}{ll}
> (\sin x)' = \cos x & (\csc x)' = -\csc x\cot x \\
> (\cos x)' = -\sin x & (\sec x)' = \sec x\tan x \\
> (\tan x)' = \sec^{2}x & (\cot x)' = -\csc^{2}x
> \end{array}
> $$
> The minus signs go with the cofunctions: cosine, cosecant, cotangent.
> - **[[Product Rule]]**: $(fg)' = f'g + fg'$. **[[Quotient Rule]]**: $\left(\dfrac{f}{g}\right)' = \dfrac{gf' - fg'}{g^{2}}$.
> - **[[Special Trigonometric Limits]]** (Equations 5 and 6): $\displaystyle\lim_{\theta \to 0} \frac{\sin\theta}{\theta} = 1$ and $\displaystyle\lim_{\theta \to 0} \frac{\cos\theta - 1}{\theta} = 0$. The same holds with $\theta = kx$ ($k \ne 0$) as $x \to 0$, because then $\theta \to 0$ too.
> - **Identities**: $\sin^{2}x + \cos^{2}x = 1$, $\tan^{2}x + 1 = \sec^{2}x$; addition formulas $\sin(x + h) = \sin x\cos h + \cos x\sin h$, $\cos(x + h) = \cos x\cos h - \sin x\sin h$.
> - **[[Tangent Line]]** at $(a, f(a))$: $y - f(a) = f'(a)(x - a)$. Horizontal tangent $\iff f'(a) = 0$.
> - **Motion**: $v = \dfrac{dx}{dt}$, $a = \dfrac{dv}{dt}$; the sign of $v$ is the direction of motion, and the speed is $\lvert v \rvert$.
> - Each answer is written as on an exam paper: the computation first, one $=$ per line, then the conclusion on a Hence line. A paragraph that starts with \# is a remark and is not part of the answer.

### ST 2.4.9
Question: [[CAL1 HW 2.4 Questions#ST 2.4.9|ST 2.4.9]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(\theta) &= (\theta - \cos\theta)'\sin\theta + (\theta - \cos\theta)(\sin\theta)' && \text{(Product Rule)} \\
> &= (1 + \sin\theta)\sin\theta + (\theta - \cos\theta)\cos\theta \\
> &= \sin\theta + \sin^{2}\theta + \theta\cos\theta - \cos^{2}\theta
> \end{aligned}
> $$
>
> \# $(-\cos\theta)' = -(-\sin\theta) = +\sin\theta$: the two minus signs make a plus, and this is the step where a sign gets lost. Since $\sin^{2}\theta - \cos^{2}\theta = -\cos 2\theta$, the answer can also be written $\sin\theta + \theta\cos\theta - \cos 2\theta$.

### ST 2.4.13
Question: [[CAL1 HW 2.4 Questions#ST 2.4.13|ST 2.4.13]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(\theta) &= \frac{(1 + \cos\theta)\cos\theta - \sin\theta\,(-\sin\theta)}{(1 + \cos\theta)^{2}} && \text{(Quotient Rule)} \\
> &= \frac{\cos\theta + \cos^{2}\theta + \sin^{2}\theta}{(1 + \cos\theta)^{2}} \\
> &= \frac{1 + \cos\theta}{(1 + \cos\theta)^{2}} && (\sin^{2}\theta + \cos^{2}\theta = 1) \\
> &= \frac{1}{1 + \cos\theta}
> \end{aligned}
> $$
>
> \# Always look for $\sin^{2} + \cos^{2}$ in the numerator: here it turns the numerator into $1 + \cos\theta$, which cancels one factor of the denominator. Note that $f'(\theta)$ is never $0$. A past midterm (CYCU 113-1, I.1) asked for $a$ with $f'(a) = 0$ for $f(x) = \dfrac{\tan x}{1 + \sec x}$; multiplying the numerator and the denominator by $\cos x$ gives $\dfrac{\sin x}{\cos x + 1}$, which is this exercise, so no such $a$ exists, and the item was scored as free points.

### ST 2.4.15
Question: [[CAL1 HW 2.4 Questions#ST 2.4.15|ST 2.4.15]]

> [!solution] Solution
> $$
> \begin{aligned}
> y' &= \frac{(2 - \tan x) \cdot 1 - x\,(-\sec^{2}x)}{(2 - \tan x)^{2}} && \text{(Quotient Rule)} \\
> &= \frac{2 - \tan x + x\sec^{2}x}{(2 - \tan x)^{2}}
> \end{aligned}
> $$
>
> \# The derivative of the denominator is $(2 - \tan x)' = -\sec^{2}x$, and the Quotient Rule subtracts it, so $-x(-\sec^{2}x) = +x\sec^{2}x$.

### ST 2.4.17
Question: [[CAL1 HW 2.4 Questions#ST 2.4.17|ST 2.4.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(w) &= \frac{(1 - \sec w)\sec w\tan w - (1 + \sec w)(-\sec w\tan w)}{(1 - \sec w)^{2}} && \text{(Quotient Rule)} \\
> &= \frac{\sec w\tan w\left[(1 - \sec w) + (1 + \sec w)\right]}{(1 - \sec w)^{2}} \\
> &= \frac{2\sec w\tan w}{(1 - \sec w)^{2}}
> \end{aligned}
> $$
>
> \# Both terms of the numerator contain $\sec w\tan w$; factor it out before expanding, and the $\sec w$ terms cancel inside the bracket.

### ST 2.4.19
Question: [[CAL1 HW 2.4 Questions#ST 2.4.19|ST 2.4.19]]

> [!solution] Solution
> $(t\sin t)' = \sin t + t\cos t$ (Product Rule).
> $$
> \begin{aligned}
> y' &= \frac{(1 + t)(\sin t + t\cos t) - t\sin t \cdot 1}{(1 + t)^{2}} && \text{(Quotient Rule)} \\
> &= \frac{\sin t + t\sin t + t\cos t + t^{2}\cos t - t\sin t}{(1 + t)^{2}} \\
> &= \frac{\sin t + t\cos t + t^{2}\cos t}{(1 + t)^{2}}
> \end{aligned}
> $$
>
> \# The numerator $t\sin t$ is itself a product, so the Product Rule sits inside the Quotient Rule. Work it out first on its own line, then substitute.

### ST 2.4.21
Question: [[CAL1 HW 2.4 Questions#ST 2.4.21|ST 2.4.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> f'(\theta) &= (\theta)'\cos\theta\sin\theta + \theta(\cos\theta)'\sin\theta + \theta\cos\theta(\sin\theta)' \\
> &= \cos\theta\sin\theta - \theta\sin^{2}\theta + \theta\cos^{2}\theta \\
> &= \sin\theta\cos\theta + \theta(\cos^{2}\theta - \sin^{2}\theta)
> \end{aligned}
> $$
>
> \# For a product of three factors, $(fgh)' = f'gh + fg'h + fgh'$: differentiate one factor at a time and keep the other two. This is the Product Rule used twice, $(f \cdot gh)' = f'gh + f(gh)'$. With $\sin 2\theta = 2\sin\theta\cos\theta$ and $\cos 2\theta = \cos^{2}\theta - \sin^{2}\theta$ the answer is $\tfrac{1}{2}\sin 2\theta + \theta\cos 2\theta$.

### ST 2.4.23
Question: [[CAL1 HW 2.4 Questions#ST 2.4.23|ST 2.4.23]]

> [!proof] Proof
> $\csc x = \dfrac{1}{\sin x}$, for $\sin x \ne 0$.
> $$
> \begin{aligned}
> \frac{d}{dx}(\csc x) &= \frac{\sin x \cdot 0 - 1 \cdot \cos x}{\sin^{2}x} && \text{(Quotient Rule)} \\
> &= -\frac{\cos x}{\sin^{2}x} \\
> &= -\frac{1}{\sin x} \cdot \frac{\cos x}{\sin x} \\
> &= -\csc x\cot x \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The only idea is to split $\dfrac{\cos x}{\sin^{2}x}$ into two fractions, $\dfrac{1}{\sin x} = \csc x$ and $\dfrac{\cos x}{\sin x} = \cot x$. The derivative of the constant numerator $1$ is $0$.

### ST 2.4.25
Question: [[CAL1 HW 2.4 Questions#ST 2.4.25|ST 2.4.25]]

> [!proof] Proof
> $\cot x = \dfrac{\cos x}{\sin x}$, for $\sin x \ne 0$.
> $$
> \begin{aligned}
> \frac{d}{dx}(\cot x) &= \frac{\sin x\,(-\sin x) - \cos x \cdot \cos x}{\sin^{2}x} && \text{(Quotient Rule)} \\
> &= -\frac{\sin^{2}x + \cos^{2}x}{\sin^{2}x} \\
> &= -\frac{1}{\sin^{2}x} && (\sin^{2}x + \cos^{2}x = 1) \\
> &= -\csc^{2}x \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Compare the textbook's proof of $(\tan x)' = \sec^{2}x$: the same steps with $\sin$ and $\cos$ exchanged, and a minus sign because $(\cos x)' = -\sin x$.

### ST 2.4.29
Question: [[CAL1 HW 2.4 Questions#ST 2.4.29|ST 2.4.29]]

> [!solution] Solution
> $$
> \begin{aligned}
> y' &= 1 + \sec^{2}x \\
> y'(\pi) &= 1 + \sec^{2}\pi = 1 + (-1)^{2} = 2
> \end{aligned}
> $$
> $$
> y - \pi = 2(x - \pi)
> $$
> Hence the tangent line is $y = 2x - \pi$.
>
> \# $\sec\pi = \dfrac{1}{\cos\pi} = \dfrac{1}{-1} = -1$, and the square removes the sign. The point is on the curve: $\pi + \tan\pi = \pi + 0 = \pi$.

### ST 2.4.35
Question: [[CAL1 HW 2.4 Questions#ST 2.4.35|ST 2.4.35]]

> [!solution] Solution
> $$
> g'(\theta) = \frac{\theta\cos\theta - \sin\theta \cdot 1}{\theta^{2}} = \frac{\theta\cos\theta - \sin\theta}{\theta^{2}}
> $$
> $(\theta\cos\theta - \sin\theta)' = \cos\theta - \theta\sin\theta - \cos\theta = -\theta\sin\theta$.
> $$
> \begin{aligned}
> g''(\theta) &= \frac{\theta^{2}(-\theta\sin\theta) - (\theta\cos\theta - \sin\theta) \cdot 2\theta}{\theta^{4}} && \text{(Quotient Rule)} \\
> &= \frac{-\theta^{3}\sin\theta - 2\theta^{2}\cos\theta + 2\theta\sin\theta}{\theta^{4}} \\
> &= \frac{2\sin\theta - 2\theta\cos\theta - \theta^{2}\sin\theta}{\theta^{3}} && (\theta \ne 0)
> \end{aligned}
> $$
>
> \# Every term of the numerator contains $\theta$, so one factor $\theta$ cancels. A shorter route: write $g(\theta) = \theta^{-1}\sin\theta$ and use the Product Rule twice. Then $g' = -\theta^{-2}\sin\theta + \theta^{-1}\cos\theta$ and $g'' = 2\theta^{-3}\sin\theta - 2\theta^{-2}\cos\theta - \theta^{-1}\sin\theta$, the same answer.

### ST 2.4.38
Question: [[CAL1 HW 2.4 Questions#ST 2.4.38|ST 2.4.38]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> g'(x) &= f'(x)\sin x + f(x)\cos x && \text{(Product Rule)} \\
> g'(\pi/3) &= (-2) \cdot \frac{\sqrt{3}}{2} + 4 \cdot \frac{1}{2} = 2 - \sqrt{3}
> \end{aligned}
> $$
> **(b)**
> $$
> \begin{aligned}
> h'(x) &= \frac{f(x)(-\sin x) - \cos x \cdot f'(x)}{\left[f(x)\right]^{2}} && \text{(Quotient Rule)} \\
> h'(\pi/3) &= \frac{4 \cdot \left(-\frac{\sqrt{3}}{2}\right) - \frac{1}{2} \cdot (-2)}{4^{2}} = \frac{-2\sqrt{3} + 1}{16} = \frac{1 - 2\sqrt{3}}{16}
> \end{aligned}
> $$
>
> \# Differentiate first with $f$ as an unknown function, and substitute $x = \pi/3$ only at the end: $\sin\frac{\pi}{3} = \frac{\sqrt{3}}{2}$, $\cos\frac{\pi}{3} = \frac{1}{2}$, $f = 4$, $f' = -2$.

### ST 2.4.41
Question: [[CAL1 HW 2.4 Questions#ST 2.4.41|ST 2.4.41]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> v(t) &= x'(t) = 8\cos t \\
> a(t) &= v'(t) = -8\sin t
> \end{aligned}
> $$
> **(b)** $t = \dfrac{2\pi}{3}$: $\sin\dfrac{2\pi}{3} = \dfrac{\sqrt{3}}{2}$, $\cos\dfrac{2\pi}{3} = -\dfrac{1}{2}$.
> $$
> \begin{aligned}
> x\left(\tfrac{2\pi}{3}\right) &= 8 \cdot \frac{\sqrt{3}}{2} = 4\sqrt{3} \text{ cm} \\
> v\left(\tfrac{2\pi}{3}\right) &= 8 \cdot \left(-\frac{1}{2}\right) = -4 \text{ cm/s} \\
> a\left(\tfrac{2\pi}{3}\right) &= -8 \cdot \frac{\sqrt{3}}{2} = -4\sqrt{3} \text{ cm/s}^{2}
> \end{aligned}
> $$
> $v < 0$. Hence at $t = \dfrac{2\pi}{3}$ the mass is moving to the left (toward the equilibrium position).
>
> \# The $x$-axis in the figure points to the right, so the sign of $v$ gives the direction: $v < 0$ means to the left. The mass is at $x = 4\sqrt{3} > 0$, to the right of $0$, so moving left means moving back toward equilibrium. Note $a(t) = -x(t)$: the acceleration always points toward the equilibrium position.

### ST 2.4.43
Question: [[CAL1 HW 2.4 Questions#ST 2.4.43|ST 2.4.43]]

> [!solution] Solution
> ![ST 2.4.43 figure|260](../Attachments/CAL1%20HW%202.4%20Solutions%20fig%2043.png)
>
> $\theta$ is at the top of the ladder, and $x$ is the side opposite $\theta$: $\sin\theta = \dfrac{x}{6}$.
> $$
> \begin{aligned}
> x &= 6\sin\theta \\
> \frac{dx}{d\theta} &= 6\cos\theta \\
> \left.\frac{dx}{d\theta}\right\rvert_{\theta = \pi/3} &= 6 \cdot \frac{1}{2} = 3
> \end{aligned}
> $$
> Hence $x$ changes at a rate of $3$ m/rad when $\theta = \dfrac{\pi}{3}$.
>
> \# Draw the right triangle first: the wall and the floor meet at a right angle, the ladder is the hypotenuse $6$, and the angle $\theta$ is at the wall. "How fast does $x$ change with respect to $\theta$" asks for $\dfrac{dx}{d\theta}$, in meters per radian. It is positive: as the ladder slides, $\theta$ grows and $x$ grows.

### ST 2.4.47
Question: [[CAL1 HW 2.4 Questions#ST 2.4.47|ST 2.4.47]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{t \to 0} \frac{\sin 3t}{\sin t} &= \lim_{t \to 0} \left( 3 \cdot \frac{\sin 3t}{3t} \cdot \frac{1}{\frac{\sin t}{t}} \right) && (t \ne 0) \\
> &= 3 \cdot 1 \cdot \frac{1}{1} \\
> &= 3
> \end{aligned}
> $$
>
> \# Make each sine sit over its own argument: $\sin 3t$ over $3t$, $\sin t$ over $t$. With $\theta = 3t$, $\theta \to 0$ as $t \to 0$, so $\dfrac{\sin 3t}{3t} \to 1$. The answer is not $\dfrac{3t}{t}$ by "cancelling" the sines: $\sin 3t \ne 3\sin t$.

### ST 2.4.49
Question: [[CAL1 HW 2.4 Questions#ST 2.4.49|ST 2.4.49]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{x \to 0} \frac{\sin x - \sin x\cos x}{x^{2}} &= \lim_{x \to 0} \left( \frac{\sin x}{x} \cdot \frac{1 - \cos x}{x} \right) \\
> &= \lim_{x \to 0} \frac{\sin x}{x} \cdot \left( -\lim_{x \to 0} \frac{\cos x - 1}{x} \right) \\
> &= 1 \cdot (-0) \\
> &= 0
> \end{aligned}
> $$
>
> \# Factor $\sin x$ out of the numerator and split $x^{2} = x \cdot x$: one $x$ goes under $\sin x$, the other under $1 - \cos x$. Both limits exist, so the limit of the product is the product of the limits.

### ST 2.4.51
Question: [[CAL1 HW 2.4 Questions#ST 2.4.51|ST 2.4.51]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{x \to 0} \frac{\tan 2x}{x} &= \lim_{x \to 0} \frac{\sin 2x}{x\cos 2x} \\
> &= \lim_{x \to 0} \left( 2 \cdot \frac{\sin 2x}{2x} \cdot \frac{1}{\cos 2x} \right) \\
> &= 2 \cdot 1 \cdot \frac{1}{\cos 0} \\
> &= 2
> \end{aligned}
> $$
>
> \# Write $\tan$ as $\dfrac{\sin}{\cos}$ first. $\cos 2x \to \cos 0 = 1$ because cosine is continuous. A past midterm (CYCU 113-1, II.1 (a)) asked exactly this limit.

### ST 2.4.53
Question: [[CAL1 HW 2.4 Questions#ST 2.4.53|ST 2.4.53]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{x \to 0} \frac{\sin 3x}{5x^{3} - 4x} &= \lim_{x \to 0} \left( \frac{\sin 3x}{3x} \cdot \frac{3x}{x(5x^{2} - 4)} \right) \\
> &= \lim_{x \to 0} \left( \frac{\sin 3x}{3x} \cdot \frac{3}{5x^{2} - 4} \right) && (x \ne 0) \\
> &= 1 \cdot \frac{3}{0 - 4} \\
> &= -\frac{3}{4}
> \end{aligned}
> $$
>
> \# Factor $x$ out of the denominator, then supply the $3$ that $\sin 3x$ needs. The other factor is a rational function whose denominator is $-4 \ne 0$ at $0$, so direct substitution works. This exercise was asked word for word on a past midterm (CYCU 113-1, II.1 (b)).

### ST 2.4.55
Question: [[CAL1 HW 2.4 Questions#ST 2.4.55|ST 2.4.55]]

> [!solution] Solution
> Divide the numerator and the denominator by $\theta \ne 0$:
> $$
> \begin{aligned}
> \lim_{\theta \to 0} \frac{\sin\theta}{\theta + \tan\theta} &= \lim_{\theta \to 0} \frac{\frac{\sin\theta}{\theta}}{1 + \frac{\sin\theta}{\theta} \cdot \frac{1}{\cos\theta}} \\
> &= \frac{1}{1 + 1 \cdot 1} \\
> &= \frac{1}{2}
> \end{aligned}
> $$
>
> \# A sum in the denominator cannot be split like a product, so divide every term by $\theta$: each $\theta$ is then inside $\dfrac{\sin\theta}{\theta}$ or becomes $1$. The limit $\dfrac{\sin 2\theta}{6\theta - \tan\theta}$ of Q2 (b) in [[CAL1 Quiz 01]] is the same type (answer $\tfrac{2}{5}$).

### ST 2.4.57
Question: [[CAL1 HW 2.4 Questions#ST 2.4.57|ST 2.4.57]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{\theta \to 0} \frac{\cos\theta - 1}{2\theta^{2}} &= \lim_{\theta \to 0} \frac{(\cos\theta - 1)(\cos\theta + 1)}{2\theta^{2}(\cos\theta + 1)} \\
> &= \lim_{\theta \to 0} \frac{\cos^{2}\theta - 1}{2\theta^{2}(\cos\theta + 1)} \\
> &= \lim_{\theta \to 0} \frac{-\sin^{2}\theta}{2\theta^{2}(\cos\theta + 1)} && (\sin^{2}\theta + \cos^{2}\theta = 1) \\
> &= -\lim_{\theta \to 0} \left( \left(\frac{\sin\theta}{\theta}\right)^{2} \cdot \frac{1}{2(\cos\theta + 1)} \right) \\
> &= -1^{2} \cdot \frac{1}{2 \cdot 2} \\
> &= -\frac{1}{4}
> \end{aligned}
> $$
>
> \# $\lim \dfrac{\cos\theta - 1}{\theta} = 0$ is not enough here, because the denominator has $\theta^{2}$: splitting gives $\dfrac{\cos\theta - 1}{\theta} \cdot \dfrac{1}{2\theta}$, a form $0 \cdot \infty$. Multiply by $\cos\theta + 1$, as in the textbook's proof of Equation 6, to turn $\cos\theta - 1$ into $-\sin^{2}\theta$. This exercise was asked on a past midterm (CYCU 107-1, problem 5).

### ST 2.4.59
Question: [[CAL1 HW 2.4 Questions#ST 2.4.59|ST 2.4.59]]

> [!solution] Solution
> $1 - \tan x = 1 - \dfrac{\sin x}{\cos x} = \dfrac{\cos x - \sin x}{\cos x}$.
> $$
> \begin{aligned}
> \lim_{x \to \pi/4} \frac{1 - \tan x}{\sin x - \cos x} &= \lim_{x \to \pi/4} \frac{\cos x - \sin x}{\cos x\,(\sin x - \cos x)} \\
> &= \lim_{x \to \pi/4} \frac{-1}{\cos x} && (\sin x - \cos x \ne 0 \text{ for } x \ne \tfrac{\pi}{4} \text{ near } \tfrac{\pi}{4}) \\
> &= \frac{-1}{\frac{\sqrt{2}}{2}} \\
> &= -\sqrt{2}
> \end{aligned}
> $$
>
> \# Here $x \to \dfrac{\pi}{4}$, not $0$, so $\dfrac{\sin\theta}{\theta}$ plays no part: this is a $\dfrac{0}{0}$ form that factors, as in Section 1.6. Write $\tan$ as $\dfrac{\sin}{\cos}$ and $\cos x - \sin x = -(\sin x - \cos x)$ cancels. Then $\dfrac{-1}{\cos x}$ is continuous at $\dfrac{\pi}{4}$.

### ST 2.4.61
Question: [[CAL1 HW 2.4 Questions#ST 2.4.61|ST 2.4.61]]

> [!solution] Solution
> $$
> \begin{aligned}
> \frac{d}{dx}(\sin x) &= \cos x \\
> \frac{d^{2}}{dx^{2}}(\sin x) &= -\sin x \\
> \frac{d^{3}}{dx^{3}}(\sin x) &= -\cos x \\
> \frac{d^{4}}{dx^{4}}(\sin x) &= \sin x
> \end{aligned}
> $$
> The derivatives repeat in a cycle of length $4$, so $\dfrac{d^{n}}{dx^{n}}(\sin x) = \sin x$ whenever $n$ is a multiple of $4$.
> $$
> 99 = 4 \cdot 24 + 3 \implies \frac{d^{96}}{dx^{96}}(\sin x) = \sin x \implies \frac{d^{99}}{dx^{99}}(\sin x) = \frac{d^{3}}{dx^{3}}(\sin x) = -\cos x
> $$
>
> \# Only the remainder of $n$ divided by $4$ matters: remainder $1, 2, 3, 0$ gives $\cos x$, $-\sin x$, $-\cos x$, $\sin x$. This is the textbook's Example 4 with $\sin$ instead of $\cos$. Past midterms asked the same: the 99th derivative of $\sin x$ (CYCU 107-1, problem 6) and the 101st derivative of $\cos x$ (CYCU 113-1, I.2).

### ST 2.4.67
Question: [[CAL1 HW 2.4 Questions#ST 2.4.67|ST 2.4.67]]

> [!solution] Solution
> ![ST 2.4.67 figure|300](../Attachments/CAL1%20HW%202.4%20Solutions%20fig%2067.png)
>
> Let $r$ be the radius. The bisector of $\theta$ is perpendicular to the chord and cuts it in half: $\sin\dfrac{\theta}{2} = \dfrac{d/2}{r}$.
> $$
> s = r\theta, \qquad d = 2r\sin\frac{\theta}{2}
> $$
> $$
> \begin{aligned}
> \lim_{\theta \to 0^{+}} \frac{s}{d} &= \lim_{\theta \to 0^{+}} \frac{r\theta}{2r\sin\frac{\theta}{2}} \\
> &= \lim_{\theta \to 0^{+}} \frac{\frac{\theta}{2}}{\sin\frac{\theta}{2}} \\
> &= \frac{1}{1} = 1 && \left(\tfrac{\theta}{2} \to 0^{+}\right)
> \end{aligned}
> $$
>
> \# $s = r\theta$ is the definition of radian measure, which is also why $\dfrac{\sin\theta}{\theta} \to 1$ needs radians. The result says that for a small angle the arc and its chord have almost the same length.

## ST §2.4 Additional Exercises

> [!note] Note
> These exercises are not assigned. Each one adds a type of problem that the assigned exercises do not cover. Five of them are types asked on past Calculus I midterms of Chung Yuan Christian University (CYCU), which take many problems straight from these exercises: [107-1](https://mathwww.cycu.edu.tw/wp-content/uploads/10712%E9%A1%8C%E7%9B%AE.pdf), [113-1](https://mathwww.cycu.edu.tw/wp-content/uploads/11312-A-%E9%A1%8C%E7%9B%AE.pdf), [114-1](https://mathwww.cycu.edu.tw/wp-content/uploads/11412%E9%A1%8C%E7%9B%AE.pdf).
> - 26: a derivative formula proved from the definition. CYCU 107-1 (problem 4) and 114-1 (II.6) both asked the same proof for $\sin x$, which is the textbook's proof of Formula 2.
> - 40: horizontal tangents of a quotient: solve $y' = 0$. CYCU 113-1 (I.1) asked this type.
> - 52: a quotient of $\sin$ and $\tan$. CYCU 114-1 (II.2) asked $\displaystyle\lim_{x \to 0} \tan 4x\cot 3x$, the same method (answer $\tfrac{4}{3}$).
> - 56: the substitution $t = \sin x$ inside $\dfrac{\sin t}{t}$.
> - 60: $x \to 1$, so the substitution is $\theta = x - 1$. CYCU 114-1 (I.1) asked it with $x^{2} + 2x - 3$ in the denominator (answer $\tfrac{1}{4}$).
> - 62: the pattern of the derivatives of a product. CYCU 113-1 (II.8) asked exactly this, together with $y'$, $y''$ and $y^{(4)}$.
> - 63: derivatives put into an equation, then the coefficients of $\sin x$ and $\cos x$ compared.

### ST 2.4.26
Question: [[CAL1 HW 2.4 Questions#ST 2.4.26|ST 2.4.26]]

> [!proof] Proof
> $$
> \begin{aligned}
> f'(x) &= \lim_{h \to 0} \frac{f(x + h) - f(x)}{h} \\
> &= \lim_{h \to 0} \frac{\cos(x + h) - \cos x}{h} \\
> &= \lim_{h \to 0} \frac{\cos x\cos h - \sin x\sin h - \cos x}{h} && \text{(addition formula for cosine)} \\
> &= \lim_{h \to 0} \left[ \cos x \cdot \frac{\cos h - 1}{h} - \sin x \cdot \frac{\sin h}{h} \right] \\
> &= \lim_{h \to 0} \cos x \cdot \lim_{h \to 0} \frac{\cos h - 1}{h} - \lim_{h \to 0} \sin x \cdot \lim_{h \to 0} \frac{\sin h}{h} \\
> &= \cos x \cdot 0 - \sin x \cdot 1 \\
> &= -\sin x \qquad \blacksquare
> \end{aligned}
> $$
>
> \# In the limit $h$ is the variable and $x$ is a constant, so $\lim_{h \to 0} \cos x = \cos x$. The proof for $\sin x$ (on two CYCU midterms) is the same with $\sin(x + h) = \sin x\cos h + \cos x\sin h$, and ends with $\sin x \cdot 0 + \cos x \cdot 1 = \cos x$. Write the step that splits the limit into four limits: it is allowed because each of the four limits exists.

### ST 2.4.40
Question: [[CAL1 HW 2.4 Questions#ST 2.4.40|ST 2.4.40]]

> [!solution] Solution
> $$
> \begin{aligned}
> y' &= \frac{(2 + \sin x)(-\sin x) - \cos x \cdot \cos x}{(2 + \sin x)^{2}} && \text{(Quotient Rule)} \\
> &= \frac{-2\sin x - (\sin^{2}x + \cos^{2}x)}{(2 + \sin x)^{2}} \\
> &= -\frac{2\sin x + 1}{(2 + \sin x)^{2}}
> \end{aligned}
> $$
> $$
> \begin{aligned}
> y' = 0 &\iff 2\sin x + 1 = 0 && (2 + \sin x \ge 1 > 0) \\
> &\iff \sin x = -\frac{1}{2} \\
> &\iff x = \frac{7\pi}{6} + 2n\pi \ \text{ or } \ x = \frac{11\pi}{6} + 2n\pi, \quad n \in \mathbb{Z}
> \end{aligned}
> $$
> At these $x$, $y = \dfrac{\cos x}{2 - \frac{1}{2}} = \dfrac{2}{3}\cos x$:
> $$
> \begin{aligned}
> x = \tfrac{7\pi}{6} + 2n\pi:&\quad y = \frac{2}{3} \cdot \left(-\frac{\sqrt{3}}{2}\right) = -\frac{\sqrt{3}}{3} \\
> x = \tfrac{11\pi}{6} + 2n\pi:&\quad y = \frac{2}{3} \cdot \frac{\sqrt{3}}{2} = \frac{\sqrt{3}}{3}
> \end{aligned}
> $$
> Hence the tangent is horizontal at the points $\left(\tfrac{7\pi}{6} + 2n\pi, -\tfrac{\sqrt{3}}{3}\right)$ and $\left(\tfrac{11\pi}{6} + 2n\pi, \tfrac{\sqrt{3}}{3}\right)$, $n$ an integer.
>
> \# A fraction is $0$ exactly when its numerator is $0$ and its denominator is not; here the denominator is never $0$. The question asks for points, so compute the $y$-values too. Write all solutions of $\sin x = -\tfrac{1}{2}$ with $+2n\pi$, as the textbook's Example 2 writes $x = \tfrac{\pi}{4} + n\pi$.

### ST 2.4.52
Question: [[CAL1 HW 2.4 Questions#ST 2.4.52|ST 2.4.52]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{\theta \to 0} \frac{\sin\theta}{\tan 7\theta} &= \lim_{\theta \to 0} \frac{\sin\theta\cos 7\theta}{\sin 7\theta} \\
> &= \lim_{\theta \to 0} \left( \frac{1}{7} \cdot \frac{\sin\theta}{\theta} \cdot \frac{1}{\frac{\sin 7\theta}{7\theta}} \cdot \cos 7\theta \right) && (\theta \ne 0) \\
> &= \frac{1}{7} \cdot 1 \cdot 1 \cdot 1 \\
> &= \frac{1}{7}
> \end{aligned}
> $$
>
> \# $\dfrac{1}{\tan 7\theta} = \dfrac{\cos 7\theta}{\sin 7\theta}$. The numbers come from $\dfrac{\theta}{7\theta} = \dfrac{1}{7}$. The CYCU 114-1 limit is the same: $\tan 4x\cot 3x = \dfrac{\sin 4x}{\cos 4x} \cdot \dfrac{\cos 3x}{\sin 3x} \to \dfrac{4x}{3x} = \dfrac{4}{3}$.

### ST 2.4.56
Question: [[CAL1 HW 2.4 Questions#ST 2.4.56|ST 2.4.56]]

> [!solution] Solution
> Let $t = \sin x$. As $x \to 0$, $t \to \sin 0 = 0$, and $t \ne 0$ for $0 < \lvert x \rvert < \pi$.
> $$
> \begin{aligned}
> \lim_{x \to 0} \csc x\sin(\sin x) &= \lim_{x \to 0} \frac{\sin(\sin x)}{\sin x} \\
> &= \lim_{t \to 0} \frac{\sin t}{t} \\
> &= 1
> \end{aligned}
> $$
>
> \# $\dfrac{\sin(\text{something})}{\text{the same something}} \to 1$ whenever the something goes to $0$ and is not $0$. Here the something is $\sin x$, and $\csc x = \dfrac{1}{\sin x}$ supplies exactly that denominator.

### ST 2.4.60
Question: [[CAL1 HW 2.4 Questions#ST 2.4.60|ST 2.4.60]]

> [!solution] Solution
> $$
> \begin{aligned}
> \lim_{x \to 1} \frac{\sin(x - 1)}{x^{2} + x - 2} &= \lim_{x \to 1} \frac{\sin(x - 1)}{(x - 1)(x + 2)} \\
> &= \lim_{x \to 1} \left( \frac{\sin(x - 1)}{x - 1} \cdot \frac{1}{x + 2} \right) \\
> &= 1 \cdot \frac{1}{3} && (\theta = x - 1 \to 0) \\
> &= \frac{1}{3}
> \end{aligned}
> $$
>
> \# Factor the denominator so that $x - 1$, the argument of the sine, appears. With $\theta = x - 1$, $\theta \to 0$ as $x \to 1$, so $\dfrac{\sin(x - 1)}{x - 1} \to 1$. CYCU 114-1: $\dfrac{\sin(x - 1)}{x^{2} + 2x - 3} = \dfrac{\sin(x - 1)}{(x - 1)(x + 3)} \to \dfrac{1}{4}$.

### ST 2.4.62
Question: [[CAL1 HW 2.4 Questions#ST 2.4.62|ST 2.4.62]]

> [!solution] Solution
> $f(x) = x\sin x$.
> $$
> \begin{aligned}
> f'(x) &= \sin x + x\cos x \\
> f''(x) &= \cos x + \cos x - x\sin x = 2\cos x - x\sin x \\
> f'''(x) &= -2\sin x - \sin x - x\cos x = -3\sin x - x\cos x \\
> f^{(4)}(x) &= -3\cos x - \cos x + x\sin x = x\sin x - 4\cos x
> \end{aligned}
> $$
> Every four derivatives, $x\sin x$ comes back and the coefficient of $\cos x$ decreases by $4$: $f^{(4k)}(x) = x\sin x - 4k\cos x$. So $f^{(32)}(x) = x\sin x - 32\cos x$, and
> $$
> \begin{aligned}
> f^{(33)}(x) &= \sin x + x\cos x + 32\sin x = x\cos x + 33\sin x \\
> f^{(34)}(x) &= \cos x - x\sin x + 33\cos x = -x\sin x + 34\cos x \\
> f^{(35)}(x) &= -\sin x - x\cos x - 34\sin x = -x\cos x - 35\sin x
> \end{aligned}
> $$
> Hence $\dfrac{d^{35}}{dx^{35}}(x\sin x) = -x\cos x - 35\sin x$.
>
> \# The same plan as the textbook's Example 4: find a derivative of order a multiple of $4$, then differentiate the last few times by hand. Check against the pattern $f^{(n)} = x \cdot (\sin x)^{(n)} + n \cdot (\sin x)^{(n-1)}$: for $n = 35$, $(\sin x)^{(35)} = -\cos x$ and $(\sin x)^{(34)} = -\sin x$, which gives the same answer.

### ST 2.4.63
Question: [[CAL1 HW 2.4 Questions#ST 2.4.63|ST 2.4.63]]

> [!solution] Solution
> $$
> \begin{aligned}
> y &= A\sin x + B\cos x \\
> y' &= A\cos x - B\sin x \\
> y'' &= -A\sin x - B\cos x
> \end{aligned}
> $$
> $$
> \begin{aligned}
> y'' + y' - 2y &= (-A - B - 2A)\sin x + (-B + A - 2B)\cos x \\
> &= (-3A - B)\sin x + (A - 3B)\cos x
> \end{aligned}
> $$
> $y'' + y' - 2y = \sin x$ for all $x$:
> $$
> \begin{aligned}
> x = 0:&\quad A - 3B = 0 \\
> x = \tfrac{\pi}{2}:&\quad -3A - B = 1
> \end{aligned}
> $$
> $A = 3B \implies -9B - B = 1 \implies B = -\dfrac{1}{10},\ A = -\dfrac{3}{10}$.
>
> Hence $A = -\dfrac{3}{10}$ and $B = -\dfrac{1}{10}$.
>
> \# Collect the $\sin x$ terms and the $\cos x$ terms, then compare coefficients with $1 \cdot \sin x + 0 \cdot \cos x$. Putting $x = 0$ and $x = \tfrac{\pi}{2}$ into the identity is the reason the comparison is allowed: those two values of $x$ give the two equations. Check: $y = -\tfrac{3}{10}\sin x - \tfrac{1}{10}\cos x$ gives $y'' + y' - 2y = \sin x$.
