---
course: [LA1]
chapter: ["1.1", "1.2"]
tags: [linear-algebra, quiz, vectors]
source:
  - "LA1 Quiz #1 (115-1), 2026-09-15, graded scan"
created: 2026-09-30
score: "5/10"
---
> [!abstract] Result: 5/10
> - Q1 True or False: 5/5.
> - Q2 Proof: 0/5. The proof distributed $r$ over the vector sum in one step instead of working componentwise.

> [!note] Notation
> The quiz writes vectors in italics ($v$, $w$) rather than in bold.

## Q1 True or False

> [!question]
> (5 pts.) Make each of the following True or False.
> - (a) The span of any two nonzero vectors in $\mathbb{R}^2$ is all of $\mathbb{R}^2$.
> - (b) Every nonzero vector in $\mathbb{R}^n$ has nonzero magnitude.
> - (c) Every nonzero vector $v$ in $\mathbb{R}^n$ has exactly one unit vector parallel to it.
> - (d) The dot product of a vector with itself yields the magnitude of the vector.
> - (e) There are exactly two unit vectors parallel to any given nonzero vector in $\mathbb{R}^n$.

> [!attempt] My answer: 5/5
> - (a) F
> - (b) T
> - (c) F
> - (d) F
> - (e) T

> [!solution]- Solution
> - (a) **F.** The nonzero vectors $[1, 0]$ and $[2, 0]$ are parallel; their [[Span|span]] is only the $x$-axis, not all of $\mathbb{R}^2$.
> - (b) **T.** If $v = [v_1, \dots, v_n] \ne 0$, then some $v_i \ne 0$, so $\lVert v \rVert^2 = v_1^2 + \cdots + v_n^2 \ge v_i^2 > 0$.
> - (c) **F.** Both $\frac{1}{\lVert v \rVert}v$ and $-\frac{1}{\lVert v \rVert}v$ are unit vectors parallel to $v$, and they are different.
> - (d) **F.** By the definition of the [[Dot Product|dot product]], $v \cdot v = \lVert v \rVert^2$, the square of the magnitude. For example, $[2, 0] \cdot [2, 0] = 4$, while $\lVert [2, 0] \rVert = 2$.
> - (e) **T.** A unit vector parallel to $v$ has the form $cv$ with $\lvert c \rvert\,\lVert v \rVert = 1$, so $c = \pm\frac{1}{\lVert v \rVert}$. This gives exactly two vectors.

## Q2 Proof

> [!question]
> (5 pts.) Let $v, w$ be any vectors in $\mathbb{R}^n$, and let $r$ be any scalar in $\mathbb{R}$. Show that $r(v + w) = rv + rw$.

> [!attempt] My answer: 0/5
> Writing $v = [v_1, v_2, \dots, v_n]$, $rv = [rv_1, rv_2, \dots, rv_n]$,
> $w = [w_1, w_2, \dots, w_n]$, $rw = [rw_1, rw_2, \dots, rw_n]$.
> $$
> \begin{aligned}
> r(v+w) &= r\big([v_1, v_2, \dots, v_n] + [w_1, w_2, \dots, w_n]\big) \\
> &= [rv_1, rv_2, \dots, rv_n] + [rw_1, rw_2, \dots, rw_n] \quad \text{✗} \\
> &= rv + rw
> \end{aligned}
> $$
> Hence $r(v+w) = rv + rw$.

> [!failure] Mistake: the step that needed a proof was skipped
> The second equality distributes $r$ over the vector sum in one step, but that is exactly the property to be proved. First compute the components of $v + w$, then apply the distributive law of $\mathbb{R}$ in each component: $r(v_i + w_i) = rv_i + rw_i$.

> [!proof]- Proof
> Let $v = [v_1, \dots, v_n]$ and $w = [w_1, \dots, w_n]$. Then
> $$
> \begin{aligned}
> r(v+w) &= r[v_1 + w_1, \dots, v_n + w_n] && \text{(definition of vector addition)} \\
> &= [r(v_1 + w_1), \dots, r(v_n + w_n)] && \text{(definition of scalar multiplication)} \\
> &= [rv_1 + rw_1, \dots, rv_n + rw_n] && \text{(distributive law in \(\mathbb{R}\))} \\
> &= [rv_1, \dots, rv_n] + [rw_1, \dots, rw_n] && \text{(definition of vector addition)} \\
> &= rv + rw. && \text{(definition of scalar multiplication)} \qquad \blacksquare
> \end{aligned}
> $$
