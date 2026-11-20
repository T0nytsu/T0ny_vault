---
course: [LA1]
semester: "115-1"
chapter: ["4.1", "4.2"]
tags: [linear-algebra, homework, solutions, determinants, vectors, needs-review]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-11-17
questions: "[[LA1 HW 4.1 4.2 Questions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 4.1 4.2 Questions#FB 4.1.19\|FB 4.1.19]] | a. F; b. T; c. T; d. F; e. F; f. T; g. F; h. T; i. T; j. F |
| [[LA1 HW 4.1 4.2 Questions#FB 4.1.27\|FB 4.1.27]] | $\tfrac{1}{2}\sqrt{230}$ |
| [[LA1 HW 4.1 4.2 Questions#FB 4.1.31\|FB 4.1.31]] | $\sqrt{390}$ |
| [[LA1 HW 4.1 4.2 Questions#FB 4.1.33\|FB 4.1.33]] | $\mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) = -6$; $\mathbf{a} \times (\mathbf{b} \times \mathbf{c}) = 12\mathbf{i} + 4\mathbf{k}$ |
| [[LA1 HW 4.1 4.2 Questions#FB 4.1.37\|FB 4.1.37]] | $20$ |
| [[LA1 HW 4.1 4.2 Questions#FB 4.1.57\|FB 4.1.57]] | Proof (counterexample) |
| [[LA1 HW 4.1 4.2 Questions#FB 4.1.58\|FB 4.1.58]] | Proof |
| [[LA1 HW 4.1 4.2 Questions#FB 4.1.59\|FB 4.1.59]] | Proof |
| [[LA1 HW 4.1 4.2 Questions#FB 4.2.7\|FB 4.2.7]] | $320$ |
| [[LA1 HW 4.1 4.2 Questions#FB 4.2.8\|FB 4.2.8]] | $-14$ |
| [[LA1 HW 4.1 4.2 Questions#FB 4.2.9\|FB 4.2.9]] | $0$ |
| [[LA1 HW 4.1 4.2 Questions#FB 4.2.10\|FB 4.2.10]] | $66$ |

## FB §4.1 Areas, Volumes, and Cross Products

> [!note] Note
> The facts that the answers use.
> - **[[Cross Product]]**: for $\mathbf{a} = [a_1, a_2, a_3]$ and $\mathbf{b} = [b_1, b_2, b_3]$,
> $$
> \mathbf{a} \times \mathbf{b} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \end{vmatrix} = (a_2b_3 - a_3b_2)\mathbf{i} - (a_1b_3 - a_3b_1)\mathbf{j} + (a_1b_2 - a_2b_1)\mathbf{k}.
> $$
> - **[[Determinant]] with row vectors** $\mathbf{a}$, $\mathbf{b}$, $\mathbf{c}$, written $\begin{vmatrix} \mathbf{a} \\ \mathbf{b} \\ \mathbf{c} \end{vmatrix}$: expanding along row 1 gives $\begin{vmatrix} \mathbf{a} \\ \mathbf{b} \\ \mathbf{c} \end{vmatrix} = \mathbf{a} \cdot (\mathbf{b} \times \mathbf{c})$.
> - **Area**: the parallelogram with edges $\mathbf{a}$, $\mathbf{b}$ in $\mathbb{R}^3$ has area $\lVert \mathbf{a} \times \mathbf{b} \rVert$, and a triangle is half of the parallelogram on two of its edges. **Volume**: the box with edges $\mathbf{a}$, $\mathbf{b}$, $\mathbf{c}$ has volume $\lvert \mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) \rvert$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.
>
> **Theorem 4.1** (Properties of Cross Product). Let $\mathbf{a}$, $\mathbf{b}$, and $\mathbf{c}$ be vectors in $\mathbb{R}^3$. ==(?)==
> 1. Anticommutativity: $\mathbf{b} \times \mathbf{a} = -(\mathbf{a} \times \mathbf{b})$
> 2. Nonassociativity of $\times$: $\mathbf{a} \times (\mathbf{b} \times \mathbf{c}) \ne (\mathbf{a} \times \mathbf{b}) \times \mathbf{c}$, in general
> 3. Distributive properties: $\mathbf{a} \times (\mathbf{b} + \mathbf{c}) = (\mathbf{a} \times \mathbf{b}) + (\mathbf{a} \times \mathbf{c})$ and $(\mathbf{a} + \mathbf{b}) \times \mathbf{c} = (\mathbf{a} \times \mathbf{c}) + (\mathbf{b} \times \mathbf{c})$
> 4. Perpendicular property: $\mathbf{a} \cdot (\mathbf{a} \times \mathbf{b}) = \mathbf{b} \cdot (\mathbf{a} \times \mathbf{b}) = 0$
> 5. Area property: $\lVert \mathbf{a} \times \mathbf{b} \rVert$ is the area of the parallelogram determined by $\mathbf{a}$ and $\mathbf{b}$
> 6. Volume property: $\mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) = (\mathbf{a} \times \mathbf{b}) \cdot \mathbf{c} = \pm$ the volume of the box determined by $\mathbf{a}$, $\mathbf{b}$, and $\mathbf{c}$

### FB 4.1.19
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.1.19|FB 4.1.19]]

> [!solution] Solution
> - a. **F.** It is a scalar: $\begin{vmatrix} a_1 & a_2 \\ b_1 & b_2 \end{vmatrix} = a_1b_2 - a_2b_1 \in \mathbb{R}$.
> - b. **T.** For rows 2 and 3: $\begin{vmatrix} \mathbf{a} \\ \mathbf{c} \\ \mathbf{b} \end{vmatrix} = \mathbf{a} \cdot (\mathbf{c} \times \mathbf{b}) = -\mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) = -\begin{vmatrix} \mathbf{a} \\ \mathbf{b} \\ \mathbf{c} \end{vmatrix}$ by (1); the other pairs work the same way (\# below).
> - c. **T.** Interchange rows so that the parallel ones are rows 2 and 3 (by b, only the sign changes). If $\mathbf{c} = t\mathbf{b}$, every $2 \times 2$ minor in $\mathbf{b} \times \mathbf{c}$ is $b_i(tb_j) - b_j(tb_i) = 0$, so $\mathbf{b} \times \mathbf{c} = \mathbf{0}$ and $\det = \mathbf{a} \cdot \mathbf{0} = 0$.
> - d. **F.** $\begin{vmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 1 & 1 & 0 \end{vmatrix} = 1\begin{vmatrix} 1 & 0 \\ 1 & 0 \end{vmatrix} - 0 + 0 = 0$, but no two rows are parallel.
> - e. **F.** $\begin{vmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{vmatrix} = 1 \ne 0$, but the points $(1, 0, 0)$, $(0, 1, 0)$, $(0, 0, 1)$ lie in the plane $x + y + z = 1$.
> - f. **T.** The three row vectors lie in one plane through the origin, so the box they determine is flat: $\lvert \det \rvert = \text{volume} = 0$.
> - g. **F.** $\mathbf{a} = [1, 0]$, $\mathbf{b} = [0, 2]$: $\mathbf{a} \cdot \mathbf{b} = 0$, but the parallelogram is a $1 \times 2$ rectangle, not a square.
> - h. **T.** Cube $\iff$ the edges are mutually perpendicular ($\mathbf{a} \cdot \mathbf{b} = \mathbf{a} \cdot \mathbf{c} = \mathbf{b} \cdot \mathbf{c} = 0$) and of equal length ($\lVert \mathbf{a} \rVert^2 = \mathbf{a} \cdot \mathbf{a} = \mathbf{b} \cdot \mathbf{b} = \mathbf{c} \cdot \mathbf{c}$).
> - i. **T.** $\lVert \mathbf{a} \times \mathbf{b} \rVert = \lVert \mathbf{a} \rVert \lVert \mathbf{b} \rVert \sin\tfrac{\pi}{4} = \lVert \mathbf{a} \rVert \lVert \mathbf{b} \rVert \cos\tfrac{\pi}{4} = \lvert \mathbf{a} \cdot \mathbf{b} \rvert$.
> - j. **F.** $\mathbf{i} \times \mathbf{i} = \mathbf{0}$, so $\lVert \mathbf{i} \times \mathbf{i} \rVert = 0 \ne 1 = \lVert \mathbf{i} \rVert^2$.
>
> \# b. Rows 1 and 2, with (6) and then (1): $\begin{vmatrix} \mathbf{b} \\ \mathbf{a} \\ \mathbf{c} \end{vmatrix} = \mathbf{b} \cdot (\mathbf{a} \times \mathbf{c}) = (\mathbf{b} \times \mathbf{a}) \cdot \mathbf{c} = -(\mathbf{a} \times \mathbf{b}) \cdot \mathbf{c} = -\begin{vmatrix} \mathbf{a} \\ \mathbf{b} \\ \mathbf{c} \end{vmatrix}$. Rows 1 and 3 go the same way.
>
> \# c, d, f. A $3 \times 3$ determinant is $0$ exactly when the three row vectors lie in one plane through the origin. Two parallel rows are one way this happens (c), but not the only one (d: row 3 $= [1, 1, 0]$ is the sum of rows 1 and 2). Why the box in f is flat: if $\mathbf{b} \times \mathbf{c} = \mathbf{0}$, then $\det = \mathbf{a} \cdot \mathbf{0} = 0$. Otherwise $\mathbf{b}$ and $\mathbf{c}$ are not parallel and span the plane, so $\mathbf{a} = s\mathbf{b} + t\mathbf{c}$, and $\mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) = s\,\mathbf{b} \cdot (\mathbf{b} \times \mathbf{c}) + t\,\mathbf{c} \cdot (\mathbf{b} \times \mathbf{c}) = 0$ by (4).
>
> \# e. Any three points lie in some plane, so e would make every $3 \times 3$ determinant zero. The plane has to pass through the origin, as in f.
>
> \# g, h. $\mathbf{a} \cdot \mathbf{b} = 0$ only makes a rectangle; a square also needs $\lVert \mathbf{a} \rVert = \lVert \mathbf{b} \rVert$. h has that extra condition, $\mathbf{a} \cdot \mathbf{a} = \mathbf{b} \cdot \mathbf{b} = \mathbf{c} \cdot \mathbf{c}$, which is why h is true. (If $\mathbf{a} = \mathbf{b} = \mathbf{c} = \mathbf{0}$, the "box" is a single point; a box is meant to have nonzero edges, as in g.)
>
> \# j. $\mathbf{a} \times \mathbf{a} = \mathbf{0}$ for every $\mathbf{a}$ (rows 2 and 3 are equal), so $\lVert \mathbf{a} \times \mathbf{a} \rVert = \lVert \mathbf{a} \rVert^2$ only for $\mathbf{a} = \mathbf{0}$.

### FB 4.1.27
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.1.27|FB 4.1.27]]

> [!solution] Solution
> $$
> \begin{aligned}
> &P = (2, 1, -3),\ Q = (3, 0, 4),\ R = (1, 0, 5) \\
> &\text{Edges from } P:\ \mathbf{a} = Q - P = [1, -1, 7],\ \mathbf{b} = R - P = [-1, -1, 8] \\
> &\mathbf{a} \times \mathbf{b} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & -1 & 7 \\ -1 & -1 & 8 \end{vmatrix} = (-8 + 7)\mathbf{i} - (8 + 7)\mathbf{j} + (-1 - 1)\mathbf{k} = -\mathbf{i} - 15\mathbf{j} - 2\mathbf{k} \\
> &\text{Area} = \tfrac{1}{2}\lVert \mathbf{a} \times \mathbf{b} \rVert = \tfrac{1}{2}\sqrt{1 + 225 + 4} = \tfrac{1}{2}\sqrt{230}.
> \end{aligned}
> $$
>
> \# The vertices are in $\mathbb{R}^3$, so there is no $2 \times 2$ determinant; the area is half the length of the cross product. Check that $\mathbf{a} \times \mathbf{b}$ is perpendicular to both edges: $[-1, -15, -2] \cdot [1, -1, 7] = -1 + 15 - 14 = 0$ and $[-1, -15, -2] \cdot [-1, -1, 8] = 1 + 15 - 16 = 0$.

### FB 4.1.31
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.1.31|FB 4.1.31]]

> [!solution] Solution
> $$
> \begin{aligned}
> &P = (1, 0, 1),\ Q = (3, 1, 4),\ R = (0, 2, 9),\ S = (-2, 1, 6) \\
> &Q - P = [2, 1, 3] = R - S, \quad S - P = [-3, 1, 5] = R - Q \implies PQRS \text{ is the parallelogram} \\
> &\text{Edges from } P:\ \mathbf{a} = [2, 1, 3],\ \mathbf{b} = [-3, 1, 5] \\
> &\mathbf{a} \times \mathbf{b} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & 1 & 3 \\ -3 & 1 & 5 \end{vmatrix} = (5 - 3)\mathbf{i} - (10 + 9)\mathbf{j} + (2 + 3)\mathbf{k} = 2\mathbf{i} - 19\mathbf{j} + 5\mathbf{k} \\
> &\text{Area} = \lVert \mathbf{a} \times \mathbf{b} \rVert = \sqrt{4 + 361 + 25} = \sqrt{390}.
> \end{aligned}
> $$
>
> \# The second line checks that opposite sides are equal vectors, so $Q$ and $S$ are the two neighbours of $P$. Any three of the four vertices form a triangle with half the area of the parallelogram, so using the diagonal, $(Q - P) \times (R - P) = [2, 1, 3] \times [-1, 2, 8] = [2, -19, 5]$, gives $\sqrt{390}$ as well.

### FB 4.1.33
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.1.33|FB 4.1.33]]

> [!solution] Solution
> $$
> \begin{aligned}
> \mathbf{b} \times \mathbf{c} &= \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 4 & -1 & 2 \\ 3 & 0 & 1 \end{vmatrix} = (-1 - 0)\mathbf{i} - (4 - 6)\mathbf{j} + (0 + 3)\mathbf{k} = -\mathbf{i} + 2\mathbf{j} + 3\mathbf{k} \\[6pt]
> \mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) &= (1)(-1) + (2)(2) + (-3)(3) = -1 + 4 - 9 = -6 \\[6pt]
> \mathbf{a} \times (\mathbf{b} \times \mathbf{c}) &= \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 2 & -3 \\ -1 & 2 & 3 \end{vmatrix} = (6 + 6)\mathbf{i} - (3 - 3)\mathbf{j} + (2 + 2)\mathbf{k} = 12\mathbf{i} + 4\mathbf{k}
> \end{aligned}
> $$
>
> \# Write $\mathbf{c} = 3\mathbf{i} + 0\mathbf{j} + \mathbf{k}$ before filling in row 3. The first answer is a scalar, the second a vector. Checks: $\mathbf{a} \cdot (\mathbf{b} \times \mathbf{c})$ is the determinant with rows $\mathbf{a}$, $\mathbf{b}$, $\mathbf{c}$, and $1(-1 - 0) - 2(4 - 6) + (-3)(0 + 3) = -6$; $\mathbf{a} \times (\mathbf{b} \times \mathbf{c})$ must be perpendicular to $\mathbf{b} \times \mathbf{c}$, and $[12, 0, 4] \cdot [-1, 2, 3] = -12 + 0 + 12 = 0$.

### FB 4.1.37
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.1.37|FB 4.1.37]]

> [!solution] Solution
> $$
> \begin{aligned}
> \text{Volume} &= \left\lvert \begin{vmatrix} -1 & 4 & 7 \\ 3 & -2 & -1 \\ 4 & 0 & 2 \end{vmatrix} \right\rvert = \lvert (-1)(-4 - 0) - 4(6 + 4) + 7(0 + 8) \rvert \\
> &= \lvert 4 - 40 + 56 \rvert = 20.
> \end{aligned}
> $$
>
> \# The determinant is the triple product $\mathbf{a} \cdot (\mathbf{b} \times \mathbf{c})$ of the three edges, and the volume is its absolute value; here it happens to be positive. Check along row 3, which has a $0$: $4\begin{vmatrix} 4 & 7 \\ -2 & -1 \end{vmatrix} + 2\begin{vmatrix} -1 & 4 \\ 3 & -2 \end{vmatrix} = 4(10) + 2(-10) = 20$.

### FB 4.1.57
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.1.57|FB 4.1.57]]

> [!proof] Proof
> Property (2) says the equality fails in general, so one example is enough. Take $\mathbf{a} = \mathbf{b} = \mathbf{i}$, $\mathbf{c} = \mathbf{j}$.
> $$
> \begin{aligned}
> &\mathbf{i} \times \mathbf{i} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 0 & 0 \\ 1 & 0 & 0 \end{vmatrix} = 0\mathbf{i} - 0\mathbf{j} + 0\mathbf{k} = \mathbf{0}, \qquad \mathbf{i} \times \mathbf{j} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{vmatrix} = 0\mathbf{i} - 0\mathbf{j} + 1\mathbf{k} = \mathbf{k} \\[6pt]
> &\mathbf{i} \times \mathbf{k} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{vmatrix} = 0\mathbf{i} - 1\mathbf{j} + 0\mathbf{k} = -\mathbf{j}, \qquad \mathbf{0} \times \mathbf{j} = \mathbf{0} \ \ (\text{row 2 is zero, so every minor is } 0) \\[6pt]
> &\mathbf{a} \times (\mathbf{b} \times \mathbf{c}) = \mathbf{i} \times (\mathbf{i} \times \mathbf{j}) = \mathbf{i} \times \mathbf{k} = -\mathbf{j} \\
> &(\mathbf{a} \times \mathbf{b}) \times \mathbf{c} = (\mathbf{i} \times \mathbf{i}) \times \mathbf{j} = \mathbf{0} \times \mathbf{j} = \mathbf{0} \\[6pt]
> &-\mathbf{j} \ne \mathbf{0} \implies \mathbf{a} \times (\mathbf{b} \times \mathbf{c}) \ne (\mathbf{a} \times \mathbf{b}) \times \mathbf{c}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# "In general" means "not for all $\mathbf{a}$, $\mathbf{b}$, $\mathbf{c}$", not "never": for $\mathbf{a} = \mathbf{b} = \mathbf{c}$ both sides are $\mathbf{0}$. So a counterexample, not a general computation, is what proves (2). Because of (2), $\mathbf{a} \times \mathbf{b} \times \mathbf{c}$ without parentheses has no meaning.

### FB 4.1.58
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.1.58|FB 4.1.58]]

> [!proof] Proof
> Let $\mathbf{a} = [a_1, a_2, a_3]$, $\mathbf{b} = [b_1, b_2, b_3]$, $\mathbf{c} = [c_1, c_2, c_3]$ in $\mathbb{R}^3$.
>
> **(i)** $\mathbf{a} \times (\mathbf{b} + \mathbf{c}) = (\mathbf{a} \times \mathbf{b}) + (\mathbf{a} \times \mathbf{c})$.
> $$
> \mathbf{a} \times (\mathbf{b} + \mathbf{c}) = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ a_1 & a_2 & a_3 \\ b_1 + c_1 & b_2 + c_2 & b_3 + c_3 \end{vmatrix}
> $$
> Compare the components; the distributive law in $\mathbb{R}$ splits each one into a part of $\mathbf{a} \times \mathbf{b}$ and a part of $\mathbf{a} \times \mathbf{c}$:
> $$
> \begin{aligned}
> \mathbf{i}:&\quad a_2(b_3 + c_3) - a_3(b_2 + c_2) = \underbrace{(a_2b_3 - a_3b_2)}_{\mathbf{a} \times \mathbf{b}} + \underbrace{(a_2c_3 - a_3c_2)}_{\mathbf{a} \times \mathbf{c}} \\
> \mathbf{j}:&\quad -[a_1(b_3 + c_3) - a_3(b_1 + c_1)] = \underbrace{-(a_1b_3 - a_3b_1)}_{\mathbf{a} \times \mathbf{b}} \underbrace{- (a_1c_3 - a_3c_1)}_{\mathbf{a} \times \mathbf{c}} \\
> \mathbf{k}:&\quad a_1(b_2 + c_2) - a_2(b_1 + c_1) = \underbrace{(a_1b_2 - a_2b_1)}_{\mathbf{a} \times \mathbf{b}} + \underbrace{(a_1c_2 - a_2c_1)}_{\mathbf{a} \times \mathbf{c}}
> \end{aligned}
> $$
> Every component agrees $\implies \mathbf{a} \times (\mathbf{b} + \mathbf{c}) = (\mathbf{a} \times \mathbf{b}) + (\mathbf{a} \times \mathbf{c})$.
>
> **(ii)** $(\mathbf{a} + \mathbf{b}) \times \mathbf{c} = (\mathbf{a} \times \mathbf{c}) + (\mathbf{b} \times \mathbf{c})$.
> $$
> \begin{aligned}
> (\mathbf{a} + \mathbf{b}) \times \mathbf{c} &= -[\mathbf{c} \times (\mathbf{a} + \mathbf{b})] && \text{(property (1))} \\
> &= -[(\mathbf{c} \times \mathbf{a}) + (\mathbf{c} \times \mathbf{b})] && \text{(by (i))} \\
> &= -(\mathbf{c} \times \mathbf{a}) - (\mathbf{c} \times \mathbf{b}) \\
> &= (\mathbf{a} \times \mathbf{c}) + (\mathbf{b} \times \mathbf{c}). && \text{(property (1))} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The $\mathbf{j}$-component carries the minus sign of the expansion, so keep the brackets until the split is done. Property (1) holds because swapping rows 2 and 3 of the determinant changes the sign of every $2 \times 2$ minor (Exercise 11). Part (ii) can also be checked component by component, exactly as in (i), with the sum now in row 2.

### FB 4.1.59
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.1.59|FB 4.1.59]]

> [!proof] Proof
> Let $\mathbf{a} = [a_1, a_2, a_3]$, $\mathbf{b} = [b_1, b_2, b_3]$, $\mathbf{c} = [c_1, c_2, c_3]$ in $\mathbb{R}^3$.
>
> **(i)** $\mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) = (\mathbf{a} \times \mathbf{b}) \cdot \mathbf{c}$.
> $$
> \begin{aligned}
> \mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) &= a_1(b_2c_3 - b_3c_2) - a_2(b_1c_3 - b_3c_1) + a_3(b_1c_2 - b_2c_1) \\
> &= a_1b_2c_3 - a_1b_3c_2 - a_2b_1c_3 + a_2b_3c_1 + a_3b_1c_2 - a_3b_2c_1 \\[6pt]
> (\mathbf{a} \times \mathbf{b}) \cdot \mathbf{c} &= (a_2b_3 - a_3b_2)c_1 - (a_1b_3 - a_3b_1)c_2 + (a_1b_2 - a_2b_1)c_3 \\
> &= a_2b_3c_1 - a_3b_2c_1 - a_1b_3c_2 + a_3b_1c_2 + a_1b_2c_3 - a_2b_1c_3
> \end{aligned}
> $$
> The same six terms appear in both $\implies \mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) = (\mathbf{a} \times \mathbf{b}) \cdot \mathbf{c}$.
>
> **(ii)** $\mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) = \pm$ the volume of the box with edges $\mathbf{a}$, $\mathbf{b}$, $\mathbf{c}$.
> $$
> \begin{aligned}
> &\text{Case } \mathbf{b} \times \mathbf{c} = \mathbf{0}:\ \text{the base on } \mathbf{b}, \mathbf{c} \text{ has area } \lVert \mathbf{b} \times \mathbf{c} \rVert = 0 \text{ by (5)} \implies \text{volume} = 0 = \mathbf{a} \cdot \mathbf{0}. \\[6pt]
> &\text{Case } \mathbf{b} \times \mathbf{c} \ne \mathbf{0}: \\
> &\qquad \text{base} = \text{parallelogram on } \mathbf{b}, \mathbf{c}, \quad \text{area} = \lVert \mathbf{b} \times \mathbf{c} \rVert && \text{(5)} \\
> &\qquad \mathbf{b} \times \mathbf{c} \perp \mathbf{b}, \mathbf{c} \implies \mathbf{n} = \tfrac{\mathbf{b} \times \mathbf{c}}{\lVert \mathbf{b} \times \mathbf{c} \rVert} \text{ is a unit vector } \perp \text{ base} && \text{(4)} \\
> &\qquad \text{height } h = \lvert \mathbf{a} \cdot \mathbf{n} \rvert = \tfrac{\lvert \mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) \rvert}{\lVert \mathbf{b} \times \mathbf{c} \rVert} \\
> &\qquad \text{volume} = \text{area} \cdot h = \lVert \mathbf{b} \times \mathbf{c} \rVert \cdot \tfrac{\lvert \mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) \rvert}{\lVert \mathbf{b} \times \mathbf{c} \rVert} = \lvert \mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) \rvert. \\[6pt]
> &\text{Hence } \mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) = (\mathbf{a} \times \mathbf{b}) \cdot \mathbf{c} = \pm\, \text{volume}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# (i) Expand both, then match the terms one by one; each of the six products $a_ib_jc_k$ uses each index $1, 2, 3$ once. Both sides are also the determinant with rows $\mathbf{a}$, $\mathbf{b}$, $\mathbf{c}$. (ii) The height is the length of the part of $\mathbf{a}$ along the unit normal $\mathbf{n}$: $h = \lVert \mathbf{a} \rVert \lvert \cos\varphi \rvert = \lvert \mathbf{a} \cdot \mathbf{n} \rvert$, where $\varphi$ is the angle between $\mathbf{a}$ and $\mathbf{n}$. The sign is $+$ when $\mathbf{a}$ points to the same side of the base as $\mathbf{b} \times \mathbf{c}$ and $-$ otherwise.

## FB §4.2 The Determinant of a Square Matrix

> [!note] Note
> The facts that the answers use.
> - **Cofactor** of $a_{ij}$: $(-1)^{i+j}\lvert A_{ij} \rvert$, where the minor matrix $A_{ij}$ is $A$ with row $i$ and column $j$ deleted. The signs $(-1)^{i+j}$ form a checkerboard, with $+$ at $(1, 1)$.
> - **Expansion by minors** on any row or column: $\det(A)$ is the sum of the entries of that row or column times their cofactors. Choose a row or column with many zeros.
> - **[[Elementary Row Operation|Row operations]]**: interchanging two rows changes the sign of $\det(A)$; multiplying a row by $s$ multiplies $\det(A)$ by $s$; adding a multiple of one row to another row leaves $\det(A)$ unchanged. Since $\det(A^T) = \det(A)$, the same holds for [[Elementary Column Operation|column operations]].
> - $R_i \to R_i + sR_j$ adds $s$ times row $j$ to row $i$, and $C_i \to C_i + sC_j$ does the same with columns; neither changes the determinant.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FB 4.2.7
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.2.7|FB 4.2.7]]

> [!solution] Solution
> $$
> \begin{aligned}
> \begin{vmatrix} 2 & 3 & 4 & 6 \\ 2 & 0 & -9 & 6 \\ 4 & 1 & 0 & 2 \\ 0 & 1 & -1 & 0 \end{vmatrix} &\overset{C_3 \to C_3 + C_2}{=} \begin{vmatrix} 2 & 3 & 7 & 6 \\ 2 & 0 & -9 & 6 \\ 4 & 1 & 1 & 2 \\ 0 & 1 & 0 & 0 \end{vmatrix} \\
> &= 1 \cdot (-1)^{4+2}\begin{vmatrix} 2 & 7 & 6 \\ 2 & -9 & 6 \\ 4 & 1 & 2 \end{vmatrix} && \text{(expand along row 4)} \\
> &\overset{R_2 \to R_2 - R_1}{=} \begin{vmatrix} 2 & 7 & 6 \\ 0 & -16 & 0 \\ 4 & 1 & 2 \end{vmatrix} \\
> &= (-16)(-1)^{2+2}\begin{vmatrix} 2 & 6 \\ 4 & 2 \end{vmatrix} && \text{(expand along row 2)} \\
> &= -16(4 - 24) = 320.
> \end{aligned}
> $$
>
> \# Row 4 is $[0, 1, -1, 0]$: adding column 2 to column 3 turns the $-1$ into $0$, so the expansion along row 4 has one term instead of two. In the $3 \times 3$ step, rows 1 and 2 differ only in the middle entry, so $R_2 - R_1$ leaves a single nonzero entry. Expanding the original along row 4 directly gives $1 \cdot 260 + (-1)(-60) = 320$, with two $3 \times 3$ determinants.

### FB 4.2.8
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.2.8|FB 4.2.8]]

> [!solution] Solution
> $$
> \begin{aligned}
> \begin{vmatrix} 2 & 0 & -1 & 7 \\ 6 & 1 & 0 & 4 \\ 8 & -2 & 1 & 0 \\ 4 & 1 & 0 & 2 \end{vmatrix} &\overset{R_3 \to R_3 + R_1}{=} \begin{vmatrix} 2 & 0 & -1 & 7 \\ 6 & 1 & 0 & 4 \\ 10 & -2 & 0 & 7 \\ 4 & 1 & 0 & 2 \end{vmatrix} \\
> &= (-1)(-1)^{1+3}\begin{vmatrix} 6 & 1 & 4 \\ 10 & -2 & 7 \\ 4 & 1 & 2 \end{vmatrix} && \text{(expand along column 3)} \\
> &= -[6(-4 - 7) - 1(20 - 28) + 4(10 + 8)] \\
> &= -[-66 + 8 + 72] = -14.
> \end{aligned}
> $$
>
> \# Column 3 is $[-1, 0, 1, 0]$, with one entry to clear: adding row 1 to row 3 makes it $[-1, 0, 0, 0]$, and the expansion along column 3 leaves one $3 \times 3$ determinant. The sign at $(1, 3)$ is $(-1)^{1+3} = +$, so only the entry $-1$ brings a minus sign.

### FB 4.2.9
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.2.9|FB 4.2.9]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Row } 1 = \text{row } 5 = [1, 2, 0, -1, 2, 4] \\
> &R_5 \to R_5 - R_1 \ (\det \text{ unchanged}) \implies \text{row } 5 = [0, 0, 0, 0, 0, 0] \\
> &\text{Expand along row } 5 \implies \det = 0.
> \end{aligned}
> $$
>
> \# Before computing, look for two equal (or proportional) rows or columns. A $6 \times 6$ determinant by minors alone takes at least $6! = 720$ multiplications (Exercise 38).

### FB 4.2.10
Question: [[LA1 HW 4.1 4.2 Questions#FB 4.2.10|FB 4.2.10]]

> [!solution] Solution
> $$
> \begin{aligned}
> \begin{vmatrix} 1 & 0 & 1 & 2 \\ 3 & 4 & 1 & 2 \\ 6 & 1 & 0 & 0 \\ 0 & 1 & 2 & 1 \end{vmatrix} &= 6(-1)^{3+1}\begin{vmatrix} 0 & 1 & 2 \\ 4 & 1 & 2 \\ 1 & 2 & 1 \end{vmatrix} + 1(-1)^{3+2}\begin{vmatrix} 1 & 1 & 2 \\ 3 & 1 & 2 \\ 0 & 2 & 1 \end{vmatrix} && \text{(expand along row 3)} \\
> &= 6[0 - 1(4 - 2) + 2(8 - 1)] - [1(1 - 4) - 1(3 - 0) + 2(6 - 0)] \\
> &= 6(12) - 6 = 66.
> \end{aligned}
> $$
>
> \# Row 3 is $[6, 1, 0, 0]$, so the expansion has two terms; the sign at $(3, 2)$ is $(-1)^{5} = -$. Another way: $C_1 \to C_1 - 6C_2$ makes row 3 $[0, 1, 0, 0]$ and leaves one $3 \times 3$ determinant, but with larger entries ($-21$, $-6$ in column 1).

> [!todo] Transcription check
> - Theorem 4.1 is not on the scanned pages (pp. 248–249, 261–262). Its statement in the Note of §4.1, and with it the meaning of properties (2), (3), and (6) in Exercises 57–59, is written from the third edition of FB and not read from a scan ==(?)==. Check it against the book.
