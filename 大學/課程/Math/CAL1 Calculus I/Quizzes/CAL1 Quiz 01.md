---
course: [CAL1]
chapter: ["1.5", "1.6"]
tags: [calculus, quiz, limits, needs-review]
source:
  - "CAL1 G-Quiz 1 (2026-09-21, sections 1.5-1.6), graded scan"
  - "[[CAL1 Quiz 01 p1.jpg]]"
created: 2026-10-05
score: "10/12"
---
> [!abstract] Result: 10/12
> - Q1 Short-Answer Questions: 1/3. Items (b) and (c) have the wrong sign.
> - Q2 Evaluate the limits: 9/9, marked "6+3". Parts (a) and (c) are correct. Part (b) stops after the first step and lost 3 points, but it is outside the range of the quiz, so its 3 points were given to everyone. The total is marked "7+3".

## Q1 Short-Answer Questions

> [!question]
> 1. Short-Answer Questions (3 points).
> - (a) $\displaystyle\lim_{x \to -1} \frac{x^2+3x}{x^2+2x+1} =$
> - (b) $\displaystyle\lim_{x \to (\pi/2)^{+}} \frac{1}{x}\sec x =$
> - (c) $\displaystyle\lim_{x \to -2^{-}} \frac{x-5}{x^2(x+2)} =$

> [!attempt] My answer: 1/3
> - (a) $-\infty$ ✓
> - (b) $\infty$ ✗ (the grader added a circled $-$ in front)
> - (c) $\mp\infty$ ==(?)== ✗

> [!failure] Mistake: (b) the sign of sec x to the right of π/2
> For $x$ slightly larger than $\frac{\pi}{2}$, the angle is in the second quadrant, so $\cos x < 0$. Then $\cos x \to 0^{-}$ and $\sec x = \frac{1}{\cos x} \to -\infty$, not $\infty$. The factor $\frac{1}{x} \to \frac{2}{\pi} > 0$ does not change the sign.

> [!failure] Mistake: (c) a negative number over a negative number
> As $x \to -2^{-}$, the numerator tends to $-7 < 0$ and the denominator $x^2(x+2)$ tends to $0$ through negative values, because $x^2 > 0$ and $x+2 < 0$. A negative numerator over a negative denominator is positive, so the limit is $\infty$. An [[Infinite Limit|infinite limit]] has one sign; decide it from the sign of each factor.

> [!solution]- Solution
> **(a)**
> $$
> \begin{aligned}
> &\lim_{x \to -1} (x^2+3x) = -2 < 0 \\
> &x^2+2x+1 = (x+1)^2 \to 0^{+} \text{ as } x \to -1 \\
> &\text{Hence } \lim_{x \to -1} \frac{x^2+3x}{x^2+2x+1} = -\infty
> \end{aligned}
> $$
>
> **(b)**
> $$
> \begin{aligned}
> &\lim_{x \to (\pi/2)^{+}} \frac{1}{x} = \frac{2}{\pi} > 0 \\
> &\cos x < 0 \text{ for } \frac{\pi}{2} < x < \pi, \text{ so } \cos x \to 0^{-} \text{ as } x \to (\pi/2)^{+} \\
> &\therefore \sec x = \frac{1}{\cos x} \to -\infty \\
> &\text{Hence } \lim_{x \to (\pi/2)^{+}} \frac{1}{x}\sec x = -\infty
> \end{aligned}
> $$
>
> **(c)**
> $$
> \begin{aligned}
> &\lim_{x \to -2^{-}} (x-5) = -7 < 0 \\
> &x^2 \to 4 > 0, \text{ while } x+2 \to 0^{-} \text{ as } x \to -2^{-} \\
> &\therefore x^2(x+2) \to 0^{-} \\
> &\text{Hence } \lim_{x \to -2^{-}} \frac{x-5}{x^2(x+2)} = \infty
> \end{aligned}
> $$

## Q2 Evaluate the Limits

> [!question]
> 2. (9 points) Evaluate the limits. You **can not** use the L'Hospital's rule.
> - (a) $\displaystyle\lim_{x \to -4} \frac{x^2+x-12}{3x^2+11x-4}$
> - (b) $\displaystyle\lim_{\theta \to 0} \frac{\sin(2\theta)}{6\theta-\tan\theta}$
> - (c) $\displaystyle\lim_{t \to 0} \left(\frac{1}{t\sqrt{4+t}} - \frac{1}{2t}\right)$

> [!attempt] My answer: 9/9
> **(a)** ✓ (−0)
> $$
> \begin{aligned}
> &\phantom{={}} \lim_{x \to -4} \frac{x^2+x-12}{3x^2+11x-4} \\
> &= \lim_{x \to -4} \frac{(x+4)(x-3)}{(x+4)(3x-1)} \quad (x+4 \ne 0) \\
> &= \lim_{x \to -4} \frac{x-3}{3x-1} \\
> &= \lim_{x \to -4} \frac{-4-3}{-12-1} \\
> &= \frac{7}{13} \quad \blacksquare
> \end{aligned}
> $$
>
> **(b)** ✗ (−3, then +3: outside the range of the quiz)
> $$
> \begin{aligned}
> &\phantom{={}} \lim_{\theta \to 0} \frac{\sin 2\theta}{6\theta-\tan\theta} \\
> &= \lim_{\theta \to 0} \frac{2 \cdot \sin\theta\cos\theta}{6\theta-\frac{\sin\theta}{\cos\theta}} \\
> &= \lim_{\theta \to 0}
> \end{aligned}
> $$
> The answer stops here. The grader wrote "Then?".
>
> **(c)** ✓ (−0)
> $$
> \begin{aligned}
> &\phantom{={}} \lim_{t \to 0} \left(\frac{1}{t\sqrt{4+t}} - \frac{1}{2t}\right) \\
> &= \lim_{t \to 0} \frac{2-\sqrt{4+t}}{2t\sqrt{4+t}} \\
> &= \lim_{t \to 0} \frac{2-\sqrt{4+t}}{2t\sqrt{4+t}} \cdot \frac{2+\sqrt{4+t}}{2+\sqrt{4+t}} \\
> &= \lim_{t \to 0} \frac{4-(4+t)}{2t\sqrt{4+t}\,(2+\sqrt{4+t})} \\
> &= \lim_{t \to 0} \frac{-t}{2t\sqrt{4+t}\,(2+\sqrt{4+t})} \quad (t \ne 0) \\
> &= \lim_{t \to 0} \frac{-1}{2\sqrt{4+t}\,(2+\sqrt{4+t})} \\
> &= \lim_{t \to 0} \frac{-1}{2 \cdot \sqrt{4}\,(2+\sqrt{4})} \\
> &= \frac{-1}{4 \cdot 4} \\
> &= -\frac{1}{16} \quad \blacksquare
> \end{aligned}
> $$

> [!failure] Mistake: (b) no step that produces sin θ / θ
> Rewriting $\sin 2\theta$ and $\tan\theta$ is correct, but the quotient is still of the form $\frac{0}{0}$, and nothing cancels. The missing step is to divide the numerator and the denominator by $\theta$. Every $\theta$ then appears inside $\frac{\sin\theta}{\theta}$, whose limit is $1$, and the denominator tends to $6-1 = 5 \ne 0$.

> [!solution]- Solution
> **(a)**
> $$
> \begin{aligned}
> \lim_{x \to -4} \frac{x^2+x-12}{3x^2+11x-4} &= \lim_{x \to -4} \frac{(x+4)(x-3)}{(x+4)(3x-1)} && \text{(factor)} \\
> &= \lim_{x \to -4} \frac{x-3}{3x-1} && \text{(\(x \ne -4\))} \\
> &= \frac{-4-3}{3(-4)-1} && \text{(rational function, denominator \(-13 \ne 0\))} \\
> &= \frac{7}{13}
> \end{aligned}
> $$
>
> **(b)**
> $$
> \begin{aligned}
> \lim_{\theta \to 0} \frac{\sin 2\theta}{6\theta-\tan\theta} &= \lim_{\theta \to 0} \frac{2\sin\theta\cos\theta}{6\theta-\frac{\sin\theta}{\cos\theta}} && \text{(double-angle formula)} \\
> &= \lim_{\theta \to 0} \frac{2 \cdot \frac{\sin\theta}{\theta} \cdot \cos\theta}{6-\frac{\sin\theta}{\theta} \cdot \frac{1}{\cos\theta}} && \text{(divide by \(\theta \ne 0\))}
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\because \lim_{\theta \to 0} \frac{\sin\theta}{\theta} = 1 \text{ and } \lim_{\theta \to 0} \cos\theta = \cos 0 = 1 \\
> &\therefore \text{the numerator} \to 2 \cdot 1 \cdot 1 = 2, \text{ the denominator} \to 6 - 1 \cdot 1 = 5 \ne 0 \\
> &\text{Hence } \lim_{\theta \to 0} \frac{\sin 2\theta}{6\theta-\tan\theta} = \frac{2}{5} && \text{(Quotient Law)}
> \end{aligned}
> $$
> \# The first line is the step already written in the quiz. Dividing by $\theta$ is the only new idea: it is allowed because $\theta \ne 0$ inside a limit as $\theta \to 0$.
>
> **(c)**
> $$
> \begin{aligned}
> \lim_{t \to 0} \left(\frac{1}{t\sqrt{4+t}} - \frac{1}{2t}\right) &= \lim_{t \to 0} \frac{2-\sqrt{4+t}}{2t\sqrt{4+t}} && \text{(common denominator)} \\
> &= \lim_{t \to 0} \frac{2-\sqrt{4+t}}{2t\sqrt{4+t}} \cdot \frac{2+\sqrt{4+t}}{2+\sqrt{4+t}} && \text{(rationalize the numerator)} \\
> &= \lim_{t \to 0} \frac{-t}{2t\sqrt{4+t}\,(2+\sqrt{4+t})} \\
> &= \lim_{t \to 0} \frac{-1}{2\sqrt{4+t}\,(2+\sqrt{4+t})} && \text{(\(t \ne 0\))} \\
> &= \frac{-1}{2\sqrt{4}\,(2+\sqrt{4})} && \text{(Direct Substitution, denominator \(16 \ne 0\))} \\
> &= -\frac{1}{16}
> \end{aligned}
> $$

> [!todo] Transcription check
> - Q1 (c): the handwritten sign is read as $\mp$ (a $+$ written over with $-$, or the reverse). The item was marked wrong together with (b) by a single "−2"; no separate ✗ is on it.
