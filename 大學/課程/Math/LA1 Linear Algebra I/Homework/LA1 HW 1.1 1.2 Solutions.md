---
course: [LA1]
chapter: ["1.1", "1.2"]
tags: [linear-algebra, homework, solutions, vectors]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-09-28
questions: "[[LA1 HW 1.1 1.2 Questions]]"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.1 1.2 Questions#FB 1.1.21\|FB 1.1.21]] | $c = -1$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.1.23\|FB 1.1.23]] | $c = -\tfrac{2}{5}$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.1.30\|FB 1.1.30]] | Every real number $c$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.1.35\|FB 1.1.35]] | $x[3, 1, 2] + y[-2, -1, 1] + z[4, -3, -5] = [10, 0, -3]$, written with column vectors |
| [[LA1 HW 1.1 1.2 Questions#FB 1.1.37\|FB 1.1.37]] | a. $-3p - 4r + 6s = 8$, $4p - 2q + 3r = -3$, $6p + 5q - 2r + 7s = 1$; b. $p[-3, 4, 6] + q[0, -2, 5] + r[-4, 3, -2] + s[6, 0, 7] = [8, -3, 1]$, written with column vectors |
| [[LA1 HW 1.1 1.2 Questions#FB 1.1.38\|FB 1.1.38]] | $-2r_1 + 5r_2 + 16r_3 = 5$, $3r_1 + 13r_2 = -8$, $-4r_2 - 9r_3 = 11$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.1.39\|FB 1.1.39]] | a. F; b. T; c. F; d. F; e. T; f. F; g. T; h. F; i. F; j. T |
| [[LA1 HW 1.1 1.2 Questions#FB 1.1.40\|FB 1.1.40]] | Proof |
| [[LA1 HW 1.1 1.2 Questions#FB 1.1.41\|FB 1.1.41]] | Proof |
| [[LA1 HW 1.1 1.2 Questions#FB 1.1.42\|FB 1.1.42]] | Proof; $r = \tfrac{1}{11}(5b_1 + 2b_2)$, $s = \tfrac{1}{11}(b_2 - 3b_1)$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.4\|FB 1.2.4]] | $\sqrt{122} \approx 11.05$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.7\|FB 1.2.7]] | $\tfrac{1}{\sqrt{26}}[-1, 3, 4]$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.9\|FB 1.2.9]] | $-3$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.11\|FB 1.2.11]] | $3$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.13\|FB 1.2.13]] | $\arccos\tfrac{11}{\sqrt{364}} \approx 54.8^\circ$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.14\|FB 1.2.14]] | $x = 11$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.17\|FB 1.2.17]] | $[13, -5, 7]$, or any nonzero multiple of it |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.26\|FB 1.2.26]] | Neither parallel nor perpendicular |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.27\|FB 1.2.27]] | Parallel, with opposite directions |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.31\|FB 1.2.31]] | Explanation |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.33\|FB 1.2.33]] | $\sqrt{33} \approx 5.745$ |
| [[LA1 HW 1.1 1.2 Questions#FB 1.2.40\|FB 1.2.40]] | a. T; b. T; c. F; d. F; e. T; f. F; g. T; h. F; i. F; j. F |

## FB §1.1 Vectors in Euclidean Spaces

> [!note] Note
> Facts used below (FB §1.1):
> - Two nonzero vectors are [[Parallel Vectors|parallel]] if one is a scalar multiple of the other.
> - A vector lies in the [[Span|span]] of $\mathbf{v}_1, \dots, \mathbf{v}_k$ if it is a [[Linear Combination|linear combination]] of them.
> - In a column-vector equation, each variable multiplies the column of its coefficients. Reading the equation one row at a time turns it back into a linear system.

### FB 1.1.21
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.1.21|FB 1.1.21]]

> [!solution] Solution
> Set $[c, -3] = t[2, 6]$. The second component gives $-3 = 6t$, so $t = -\tfrac{1}{2}$. Then the first component gives $c = 2t = -1$.
>
> Check: $[-1, -3] = -\tfrac{1}{2}[2, 6]$. Hence $c = -1$.

### FB 1.1.23
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.1.23|FB 1.1.23]]

> [!solution] Solution
> Set $[c, -c, 4] = t[-2, 2, 20]$. The third component gives $4 = 20t$, so $t = \tfrac{1}{5}$. Then the first component gives $c = -2t = -\tfrac{2}{5}$, and the second component, $-c = 2t = \tfrac{2}{5}$, agrees.
>
> Check: $\left[-\tfrac{2}{5}, \tfrac{2}{5}, 4\right] = \tfrac{1}{5}[-2, 2, 20]$. Hence $c = -\tfrac{2}{5}$.

### FB 1.1.30
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.1.30|FB 1.1.30]]

> [!solution] Solution
> We need scalars $r$, $s$, $t$ with $r[1, -1, 1] + s[0, 1, -3] + t[0, 0, 1] = [c, -2c, c]$. Comparing components gives the system
> $$
> \begin{aligned}
> r &= c \\
> -r + s &= -2c \\
> r - 3s + t &= c.
> \end{aligned}
> $$
> Solving from the top down: $r = c$, then $s = -2c + r = -c$, then $t = c - r + 3s = -3c$. Each equation introduces exactly one new unknown with coefficient $1$, so the system has a solution for every $c$:
> $$
> \begin{bmatrix} c \\ -2c \\ c \end{bmatrix} = c\begin{bmatrix} 1 \\ -1 \\ 1 \end{bmatrix} - c\begin{bmatrix} 0 \\ 1 \\ -3 \end{bmatrix} - 3c\begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}.
> $$
> Check: $[c, -c - c, c + 3c - 3c] = [c, -2c, c]$. Hence every real number $c$ works.

### FB 1.1.35
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.1.35|FB 1.1.35]]

> [!solution] Solution
> Collect the coefficients of $x$, $y$, and $z$ into columns:
> $$
> x\begin{bmatrix} 3 \\ 1 \\ 2 \end{bmatrix} + y\begin{bmatrix} -2 \\ -1 \\ 1 \end{bmatrix} + z\begin{bmatrix} 4 \\ -3 \\ -5 \end{bmatrix} = \begin{bmatrix} 10 \\ 0 \\ -3 \end{bmatrix}.
> $$

### FB 1.1.37
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.1.37|FB 1.1.37]]

> [!solution] Solution
> **a.** Match the first, second, and third components on both sides. The minus sign in front of $r[4, -3, 2]$ changes the signs of the entries of that vector:
> $$
> \begin{array}{rcrcrcrcr}
> -3p & & & - & 4r & + & 6s & = & 8 \\
> 4p & - & 2q & + & 3r & & & = & -3 \\
> 6p & + & 5q & - & 2r & + & 7s & = & 1
> \end{array}
> $$
>
> **b.** As a column-vector equation:
> $$
> p\begin{bmatrix} -3 \\ 4 \\ 6 \end{bmatrix} + q\begin{bmatrix} 0 \\ -2 \\ 5 \end{bmatrix} + r\begin{bmatrix} -4 \\ 3 \\ -2 \end{bmatrix} + s\begin{bmatrix} 6 \\ 0 \\ 7 \end{bmatrix} = \begin{bmatrix} 8 \\ -3 \\ 1 \end{bmatrix}.
> $$
> Keeping the original form, with $-r[4, -3, 2]$ written as a column, is equally correct.

### FB 1.1.38
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.1.38|FB 1.1.38]]

> [!solution] Solution
> Read the equation one row at a time:
> $$
> \begin{array}{rcrcrcr}
> -2r_1 & + & 5r_2 & + & 16r_3 & = & 5 \\
> 3r_1 & + & 13r_2 & & & = & -8 \\
> & & -4r_2 & - & 9r_3 & = & 11
> \end{array}
> $$

### FB 1.1.39
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.1.39|FB 1.1.39]]

> [!solution] Solution
> | Part | Answer | Reason or counterexample |
> | --- | --- | --- |
> | a | False | Vectors in $\mathbb{R}^n$ with large $n$ are useful; for example, a list of $n$ measurements or prices is a vector in $\mathbb{R}^n$. |
> | b | True | An $n$-tuple can be read as the point with those coordinates or as the arrow from the origin to that point. |
> | c | False | Addition of $n$-tuples is defined componentwise, so points can be added in the same way; only the picture differs. |
> | d | False | The arrow from the tip of $\mathbf{a}$ to the tip of $\mathbf{b}$ represents $\mathbf{b} - \mathbf{a}$, because $\mathbf{a} + (\mathbf{b} - \mathbf{a}) = \mathbf{b}$. |
> | e | True | Same reason as in d: going from the tip of $\mathbf{a}$ to the tip of $\mathbf{b}$ adds $\mathbf{b} - \mathbf{a}$. |
> | f | False | $[1, 0]$ and $[2, 0]$ are nonzero but parallel. Every linear combination $r[1, 0] + s[2, 0] = [r + 2s, 0]$ lies on the $x$-axis, so $[0, 1]$ is not in their span. |
> | g | True | Two nonparallel vectors in $\mathbb{R}^2$ point in different directions, and every vector in the plane is a linear combination of them. |
> | h | False | $[1, 0, 0]$, $[0, 1, 0]$, $[1, 1, 0]$ are nonzero and pairwise nonparallel, but every linear combination of them has third component $0$, so $[0, 0, 1]$ is not in their span. |
> | i | False | $[1, 0]$, $[0, 1]$, $[1, 1]$ span $\mathbb{R}^2$ with $k = 3$. The correct statement is $k \ge 2$. |
> | j | True | One vector spans at most a line and two vectors span at most a plane through the origin, so spanning $\mathbb{R}^3$ needs $k \ge 3$. |

### FB 1.1.40
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.1.40|FB 1.1.40]]

> [!proof] Proof
> Let $\mathbf{u} = [u_1, \dots, u_n]$, $\mathbf{v} = [v_1, \dots, v_n]$, and $\mathbf{w} = [w_1, \dots, w_n]$ be vectors in $\mathbb{R}^n$. Each property of Theorem 1.1 follows componentwise from the matching law for real numbers.
>
> **a.** (A1) $(\mathbf{u}+\mathbf{v})+\mathbf{w} = \mathbf{u}+(\mathbf{v}+\mathbf{w})$.
> $$
> \begin{aligned}
> (\mathbf{u}+\mathbf{v})+\mathbf{w} &= [u_1+v_1, \dots, u_n+v_n] + [w_1, \dots, w_n] && \text{(definition of vector addition)} \\
> &= [(u_1+v_1)+w_1, \dots, (u_n+v_n)+w_n] && \text{(definition of vector addition)} \\
> &= [u_1+(v_1+w_1), \dots, u_n+(v_n+w_n)] && \text{(associativity of addition in \(\mathbb{R}\))} \\
> &= [u_1, \dots, u_n] + [v_1+w_1, \dots, v_n+w_n] && \text{(definition of vector addition)} \\
> &= \mathbf{u}+(\mathbf{v}+\mathbf{w}). && \text{(definition of vector addition)} \qquad \blacksquare
> \end{aligned}
> $$
>
> **b.** (A3) $\mathbf{0}+\mathbf{v} = \mathbf{v}$.
> $$
> \begin{aligned}
> \mathbf{0}+\mathbf{v} &= [0+v_1, \dots, 0+v_n] && \text{(definitions of \(\mathbf{0}\) and vector addition)} \\
> &= [v_1, \dots, v_n] = \mathbf{v}. && \text{(\(0 + a = a\) for every \(a \in \mathbb{R}\))} \qquad \blacksquare
> \end{aligned}
> $$
>
> **c.** (A4) $\mathbf{v}+(-\mathbf{v}) = \mathbf{0}$. By definition, $-\mathbf{v} = [-v_1, \dots, -v_n]$.
> $$
> \begin{aligned}
> \mathbf{v}+(-\mathbf{v}) &= [v_1+(-v_1), \dots, v_n+(-v_n)] && \text{(definitions of \(-\mathbf{v}\) and vector addition)} \\
> &= [0, \dots, 0] = \mathbf{0}. && \text{(\(a + (-a) = 0\) for every \(a \in \mathbb{R}\))} \qquad \blacksquare
> \end{aligned}
> $$

### FB 1.1.41
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.1.41|FB 1.1.41]]

> [!note] Note
> The book prints a stray "42." beside the parts of this exercise; parts a–c (S1, S3, S4) belong to Exercise 41.

> [!proof] Proof
> Let $\mathbf{v} = [v_1, \dots, v_n]$ and $\mathbf{w} = [w_1, \dots, w_n]$ be vectors in $\mathbb{R}^n$, and let $r$ and $s$ be scalars.
>
> **a.** (S1) $r(\mathbf{v}+\mathbf{w}) = r\mathbf{v}+r\mathbf{w}$.
> $$
> \begin{aligned}
> r(\mathbf{v}+\mathbf{w}) &= r[v_1+w_1, \dots, v_n+w_n] && \text{(definition of vector addition)} \\
> &= [r(v_1+w_1), \dots, r(v_n+w_n)] && \text{(definition of scalar multiplication)} \\
> &= [rv_1+rw_1, \dots, rv_n+rw_n] && \text{(distributive law in \(\mathbb{R}\))} \\
> &= [rv_1, \dots, rv_n] + [rw_1, \dots, rw_n] && \text{(definition of vector addition)} \\
> &= r\mathbf{v}+r\mathbf{w}. && \text{(definition of scalar multiplication)} \qquad \blacksquare
> \end{aligned}
> $$
>
> **b.** (S3) $r(s\mathbf{v}) = (rs)\mathbf{v}$.
> $$
> \begin{aligned}
> r(s\mathbf{v}) &= r[sv_1, \dots, sv_n] && \text{(definition of scalar multiplication)} \\
> &= [r(sv_1), \dots, r(sv_n)] && \text{(definition of scalar multiplication)} \\
> &= [(rs)v_1, \dots, (rs)v_n] && \text{(associativity of multiplication in \(\mathbb{R}\))} \\
> &= (rs)\mathbf{v}. && \text{(definition of scalar multiplication)} \qquad \blacksquare
> \end{aligned}
> $$
>
> **c.** (S4) $1\mathbf{v} = \mathbf{v}$.
> $$
> \begin{aligned}
> 1\mathbf{v} &= [1 \cdot v_1, \dots, 1 \cdot v_n] && \text{(definition of scalar multiplication)} \\
> &= [v_1, \dots, v_n] = \mathbf{v}. && \text{(\(1 \cdot a = a\) for every \(a \in \mathbb{R}\))} \qquad \blacksquare
> \end{aligned}
> $$

### FB 1.1.42
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.1.42|FB 1.1.42]]

> [!proof] Proof
> Let $b_1, b_2 \in \mathbb{R}$. We show that
> $$
> r = \frac{5b_1 + 2b_2}{11}, \qquad s = \frac{b_2 - 3b_1}{11}
> $$
> is a solution of the system $r - 2s = b_1$, $3r + 5s = b_2$.
>
> **Derivation.** The first equation gives $r = b_1 + 2s$. Substituting this into the second equation gives $3(b_1 + 2s) + 5s = b_2$, so $11s = b_2 - 3b_1$ and $s = \frac{b_2 - 3b_1}{11}$. Then $r = b_1 + 2s = \frac{5b_1 + 2b_2}{11}$.
>
> **Check by substitution.**
> $$
> \begin{aligned}
> r - 2s &= \frac{5b_1 + 2b_2 - 2b_2 + 6b_1}{11} = \frac{11b_1}{11} = b_1, \\
> 3r + 5s &= \frac{15b_1 + 6b_2 + 5b_2 - 15b_1}{11} = \frac{11b_2}{11} = b_2.
> \end{aligned}
> $$
> The formulas divide only by $11 \ne 0$, so they give a solution for every choice of $b_1$ and $b_2$. $\blacksquare$

> [!tip] Intuition
> The system says $r[1, 3] + s[-2, 5] = [b_1, b_2]$. The vectors $[1, 3]$ and $[-2, 5]$ are not parallel, so they span all of $\mathbb{R}^2$.

## FB §1.2 The Norm and the Dot Product

> [!note] Note
> Exercises 4, 7, 9, 11, 13, 14, and 17 use $\mathbf{u} = [-1, 3, 4]$, $\mathbf{v} = [2, 1, -1]$, and $\mathbf{w} = [-2, -1, 3]$. Two values are used repeatedly:
> $$
> \lVert \mathbf{u} \rVert = \sqrt{1 + 9 + 16} = \sqrt{26}, \qquad \lVert \mathbf{w} \rVert = \sqrt{4 + 1 + 9} = \sqrt{14}.
> $$

### FB 1.2.4
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.4|FB 1.2.4]]

> [!solution] Solution
> We have $\mathbf{v} - 2\mathbf{u} = [2 + 2, 1 - 6, -1 - 8] = [4, -5, -9]$, so by the definition of the [[Norm|norm]],
> $$
> \lVert \mathbf{v} - 2\mathbf{u} \rVert = \sqrt{16 + 25 + 81} = \sqrt{122} \approx 11.05.
> $$

### FB 1.2.7
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.7|FB 1.2.7]]

> [!solution] Solution
> Divide $\mathbf{u}$ by its norm $\sqrt{26}$:
> $$
> \frac{1}{\lVert \mathbf{u} \rVert}\mathbf{u} = \frac{1}{\sqrt{26}}[-1, 3, 4] = \left[-\frac{1}{\sqrt{26}}, \frac{3}{\sqrt{26}}, \frac{4}{\sqrt{26}}\right] \approx [-0.196, 0.588, 0.784].
> $$
> This is a [[Unit Vector|unit vector]], and it has the same direction as $\mathbf{u}$ because $\tfrac{1}{\sqrt{26}} > 0$.

### FB 1.2.9
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.9|FB 1.2.9]]

> [!solution] Solution
> By the definition of the [[Dot Product|dot product]],
> $$
> \mathbf{u} \cdot \mathbf{v} = (-1)(2) + (3)(1) + (4)(-1) = -2 + 3 - 4 = -3.
> $$

### FB 1.2.11
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.11|FB 1.2.11]]

> [!solution] Solution
> Since $\mathbf{u} + \mathbf{v} = [1, 4, 3]$,
> $$
> (\mathbf{u} + \mathbf{v}) \cdot \mathbf{w} = (1)(-2) + (4)(-1) + (3)(3) = -2 - 4 + 9 = 3.
> $$
> Check with the distributive law: $\mathbf{u} \cdot \mathbf{w} + \mathbf{v} \cdot \mathbf{w} = 11 + (-8) = 3$.

### FB 1.2.13
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.13|FB 1.2.13]]

> [!solution] Solution
> First, $\mathbf{u} \cdot \mathbf{w} = (-1)(-2) + (3)(-1) + (4)(3) = 2 - 3 + 12 = 11$. The angle $\theta$ between $\mathbf{u}$ and $\mathbf{w}$ satisfies
> $$
> \cos\theta = \frac{\mathbf{u} \cdot \mathbf{w}}{\lVert \mathbf{u} \rVert \, \lVert \mathbf{w} \rVert} = \frac{11}{\sqrt{26}\,\sqrt{14}} = \frac{11}{\sqrt{364}} \approx 0.5766,
> $$
> so $\theta = \arccos\frac{11}{\sqrt{364}} \approx 54.8^\circ$, or about $0.956$ radians.

### FB 1.2.14
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.14|FB 1.2.14]]

> [!solution] Solution
> Two vectors are [[Orthogonal Vectors|perpendicular]] exactly when their dot product is $0$:
> $$
> [x, -3, 5] \cdot [-1, 3, 4] = -x - 9 + 20 = 11 - x = 0,
> $$
> so $x = 11$.

### FB 1.2.17
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.17|FB 1.2.17]]

> [!solution] Solution
> We need $[x, y, z]$ whose dot product with both $\mathbf{u}$ and $\mathbf{w}$ is $0$:
> $$
> \begin{aligned}
> -x + 3y + 4z &= 0 \\
> -2x - y + 3z &= 0.
> \end{aligned}
> $$
> The first equation gives $x = 3y + 4z$. Substituting this into the second equation gives $-2(3y + 4z) - y + 3z = -7y - 5z = 0$, so $y = -\tfrac{5}{7}z$. Choosing $z = 7$ gives $y = -5$ and $x = -15 + 28 = 13$.
>
> Check: $\mathbf{u} \cdot [13, -5, 7] = -13 - 15 + 28 = 0$ and $\mathbf{w} \cdot [13, -5, 7] = -26 + 5 + 21 = 0$. Hence $[13, -5, 7]$ is such a vector, and so is every nonzero multiple of it.

### FB 1.2.26
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.26|FB 1.2.26]]

> [!solution] Solution
> To classify a pair, first check whether one vector is a scalar multiple of the other (parallel), then whether the dot product is $0$ (perpendicular).
>
> Since $[-2, -1] \cdot [5, 2] = -10 - 2 = -12 \ne 0$, the vectors are not perpendicular. If $[5, 2] = t[-2, -1]$, the first component needs $t = -\tfrac{5}{2}$ but the second needs $t = -2$, so the vectors are not parallel. Hence they are neither parallel nor perpendicular.

### FB 1.2.27
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.27|FB 1.2.27]]

> [!solution] Solution
> We have $[-9, -6, -3] = -3[3, 2, 1]$. The scalar is negative, so the vectors are parallel with opposite directions.

### FB 1.2.31
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.31|FB 1.2.31]]

> [!solution] Solution
> Defining the distance between the points $\mathbf{v}$ and $\mathbf{w}$ as $\lVert \mathbf{v} - \mathbf{w} \rVert$ is reasonable for three reasons.
> 1. **It measures the segment between the points.** Drawn as an arrow, $\mathbf{v} - \mathbf{w}$ goes from the point $\mathbf{w}$ to the point $\mathbf{v}$ (tip to tip, as in FB 1.1.39 e). Its length is the length of that segment.
> 2. **It matches the familiar formula.** Written out, $\lVert \mathbf{v}-\mathbf{w} \rVert = \sqrt{(v_1-w_1)^2 + (v_2-w_2)^2 + \cdots + (v_n-w_n)^2}$. This is the Pythagorean distance formula that we already use in $\mathbb{R}^2$ and $\mathbb{R}^3$; the definition extends it to $n$ coordinates.
> 3. **It behaves like a distance.** It is never negative, it is $0$ only when the points coincide, it is symmetric because $\lVert \mathbf{v} - \mathbf{w} \rVert = \lVert \mathbf{w} - \mathbf{v} \rVert$, and it satisfies the triangle inequality.

### FB 1.2.33
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.33|FB 1.2.33]]

> [!solution] Solution
> The vector from $(2, -1, 3)$ to $(4, 1, -2)$ is $[4 - 2, 1 - (-1), -2 - 3] = [2, 2, -5]$, so the distance is
> $$
> \lVert [2, 2, -5] \rVert = \sqrt{4 + 4 + 25} = \sqrt{33} \approx 5.745.
> $$

### FB 1.2.40
Question: [[LA1 HW 1.1 1.2 Questions#FB 1.2.40|FB 1.2.40]]

> [!solution] Solution
> | Part | Answer | Reason or counterexample |
> | --- | --- | --- |
> | a | True | If $\mathbf{v} \ne \mathbf{0}$, some component $v_i \ne 0$, so $\lVert \mathbf{v} \rVert^2 \ge v_i^2 > 0$. |
> | b | True | $\lVert \mathbf{0} \rVert = 0$, so a vector with nonzero magnitude cannot be $\mathbf{0}$. |
> | c | False | Take $\mathbf{w} = -\mathbf{v}$ with $\mathbf{v} \ne \mathbf{0}$. Then $\lVert \mathbf{v} + \mathbf{w} \rVert = 0 < \lVert \mathbf{v} \rVert$. |
> | d | False | There are two: $\frac{1}{\lVert \mathbf{v} \rVert}\mathbf{v}$ and $-\frac{1}{\lVert \mathbf{v} \rVert}\mathbf{v}$. |
> | e | True | Exactly $\pm\frac{1}{\lVert \mathbf{v} \rVert}\mathbf{v}$: a unit vector $t\mathbf{v}$ needs $\lvert t \rvert \, \lVert \mathbf{v} \rVert = 1$, so $t = \pm\frac{1}{\lVert \mathbf{v} \rVert}$. |
> | f | False | In $\mathbb{R}^3$ the unit vectors perpendicular to $[0, 0, 1]$ form a whole circle, for example $[\cos t, \sin t, 0]$ for every $t$. The statement holds only in $\mathbb{R}^2$. |
> | g | True | $\cos\theta = \frac{\mathbf{v} \cdot \mathbf{w}}{\lVert \mathbf{v} \rVert \, \lVert \mathbf{w} \rVert}$ has a positive denominator, and for $0^\circ \le \theta \le 180^\circ$ we have $\cos\theta > 0$ exactly when $\theta < 90^\circ$. |
> | h | False | $\mathbf{v} \cdot \mathbf{v} = \lVert \mathbf{v} \rVert^2$, the square of the magnitude. For example, $[2, 0] \cdot [2, 0] = 4$, but $\lVert [2, 0] \rVert = 2$. |
> | i | False | $\lVert r\mathbf{v} \rVert = \lvert r \rvert \, \lVert \mathbf{v} \rVert$. With $r = -1$ and $\mathbf{v} \ne \mathbf{0}$, $\lVert -\mathbf{v} \rVert = \lVert \mathbf{v} \rVert$, not $-\lVert \mathbf{v} \rVert$. |
> | j | False | $\mathbf{v} = [1, 0]$ and $\mathbf{w} = [0, 1]$ both have magnitude $1$, but $\lVert \mathbf{v} - \mathbf{w} \rVert = \lVert [1, -1] \rVert = \sqrt{2}$. |
