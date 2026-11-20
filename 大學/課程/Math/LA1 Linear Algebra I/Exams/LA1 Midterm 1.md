---
course: [LA1]
semester: "115-1"
chapter: ["1.1", "1.2", "1.3", "1.4", "1.5", "10.2"]
tags: [linear-algebra, exam, matrix-algebra, matrix-inverse, linear-systems, needs-review]
source:
  - "115-1, Linear Algebra I – Midterm #1, printed question paper (2 pages) and graded answer sheet (7 pages), scans"
  - "[[LA1 Midterm 1 p1.jpg]]"
  - "[[LA1 Midterm 1 p2.jpg]]"
  - "[[LA1 Midterm 1 p3.jpg]]"
  - "[[LA1 Midterm 1 p4.jpg]]"
  - "[[LA1 Midterm 1 p5.jpg]]"
  - "[[LA1 Midterm 1 p6.jpg]]"
  - "[[LA1 Midterm 1 p7.jpg]]"
  - "[[LA1 Midterm 1 p8.jpg]]"
  - "[[LA1 Midterm 1 p9.jpg]]"
created: 2026-11-17
score: "80/100"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!abstract] Result: 80/100
> - Q1 True or False: 9/10. Item (e) was wrong.
> - Q2 Skew-symmetric matrix: 6/6.
> - Q3 Reduced row-echelon form: 6/6.
> - Q4 Span of two vectors: 6/6.
> - Q5 Norm and dot product: 6/6.
> - Q6 A system with a parameter: 6/6.
> - Q7 Inverse by row reduction: 9/12. (a) 3/6: invertibility was proved with "$Ax = 0$ has only $x = 0$", a result that is itself proved through $A \overset{r}{\sim} I$, and $PA = I$ and the reason why $P$ is invertible were never written. (b) 6/6.
> - Q8 Matrix from the general solution: 0/6. Left blank.
> - Q9 Product of symmetric matrices: 4/6. The steps $B^TA^T = BA$ never say that they use $A^T = A$ and $B^T = B$.
> - Q10 Row equivalence and Gaussian elimination: 10/12. (1) 6/6. (2) 4/6: back substitution gave $x_2 = 2 - 4(-2) = 10$ instead of $2 - 2(-2) = 6$, so $x = (25, 10, -2)$ instead of $(17, 6, -2)$.
> - Q11 LU factorization and solving: 6/6.
> - Q12 A commutator equal to B: 0/6. The proof reached $A - BAB^{-1} = I$ and stopped; the trace finishes it.
> - Q13 Inverse of a sum of inverses: 6/6.
> - Q14 Nilpotent matrix: 6/6.

> [!info] Coverage
> Linear Algebra I, Midterm #1, semester 115-1: 14 questions, 100 points, on FB §1.1–1.5 and §10.2. The [[Norm|norm]], the [[Dot Product|dot product]] and [[Orthogonal Vectors|orthogonal vectors]]; [[Span|span]]; [[Skew-Symmetric Matrix|skew-symmetric]], [[Symmetric Matrix|symmetric]] and [[Triangular Matrix|triangular matrices]]; [[Reduced Row-Echelon Form|reduced row-echelon form]], [[Row Equivalence|row equivalence]], [[Gaussian Elimination|Gaussian elimination]], [[Homogeneous System|homogeneous systems]] and [[Rank|rank]]; [[Invertible Matrix|inverses]], the [[LU-Factorization|LU-factorization]], [[Commuting Matrices|commuting matrices]] and [[Nilpotent Matrix|nilpotent matrices]].

> [!note] Notation
> - The paper writes the transpose as $A^{\top}$; the answers and the solutions write $A^T$. Vectors and $m \times 1$ matrices are not bold ($u$, $v$, $w$, $b$, $x$). $\overset{r}{\sim}$ is row equivalence and $[A \mid b]$ an augmented matrix. $O$ is a zero matrix.
> - In the attempts, as written beside the matrices: $\hookleftarrow{\times}s$ on a row means that $s$ times the pivot row of the step is added to that row; $\downarrow$ and $\uparrow$ beside two rows mean that the two rows are interchanged (Q4). In Q11 the second matrix keeps the multipliers $2$, $-1$, $0$ below the diagonal, where the zeros of $U$ would be; they are the entries of $L$.
> - The grader's red marks are described in words after each attempt; ✗ marks a wrong item or step.
> - In the solutions, row operations stand over $\sim$: $R_i \leftrightarrow R_j$, $R_i \to R_i + sR_j$. Each answer is written as on an exam paper; a paragraph that starts with \# is a remark and not part of the answer.

## Q1 True or False

> [!question]
> (10 pts) Make each of the following True or False.
> - (a) If $A$ and $B$ are square matrices such that $AB = O$, then $A = O$ or $B = O$.
> - (b) For any vectors $v, w \in \mathbb{R}^n$, $\lVert v + w \rVert^2 = \lVert v \rVert^2 + \lVert w \rVert^2$ if and only if $v$ and $w$ are perpendicular.
> - (c) If $A$ is an $n \times n$ matrix such that $A^{\top}$ is invertible, then $A$ is invertible.
> - (d) The product of two lower triangular matrices is lower triangular..
> - (e) A homogeneous linear system with more unknowns than equations always has infinitely many solutions.
> - (f) If $A$ is a symmetric matrix, then $A^2$ is also symmetric.
> - (g) If $A$ is an $n \times n$ invertible matrix, then $Ax = b$ has a unique solution for every vector $b \in \mathbb{R}^n$.
> - (h) If $A$ is an $n \times n$ matrix satisfying $A^3 = I$, then $A$ is invertible.
> - (i) If $A$ and $B$ are $n \times n$ matrices and $AB$ is invertible, then both $A$ and $B$ must be invertible.
> - (j) For an $m \times n$ matrix $A$, the linear system $Ax = b$ is consistent for every vector $b \in \mathbb{R}^m$ if and only if $\operatorname{rank}(A) = n$.

> [!attempt] My answer: 9/10
> - (a) F
> - (b) T
> - (c) T
> - (d) T
> - (e) F ✗
> - (f) T
> - (g) T
> - (h) T
> - (i) T
> - (j) F

> [!failure] Mistake: (e)
> A homogeneous system $Ax = 0$ is never inconsistent: $x = 0$ is always a solution. With $m$ equations and $n > m$ unknowns there are at most $m < n$ pivots, so some column has no pivot and gives a free variable. A consistent system with a free variable has infinitely many solutions, so (e) is True.

> [!solution]- Solution
> - (a) **F.** $A = B = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} \ne O$, but $AB = O$.
> - (b) **T.** $\lVert v + w \rVert^2 = (v + w) \cdot (v + w) = \lVert v \rVert^2 + 2\,v \cdot w + \lVert w \rVert^2$, so the equality holds $\iff v \cdot w = 0 \iff v \perp w$.
> - (c) **T.** Let $C = (A^T)^{-1}$. $C^TA = (A^TC)^T = I^T = I$ and $AC^T = (CA^T)^T = I^T = I$ $\implies$ $A^{-1} = C^T$.
> - (d) **T.** $a_{ik} = 0$ for $i < k$ and $b_{kj} = 0$ for $k < j$. For $i < j$, every term of $(AB)_{ij} = \sum_{k} a_{ik}b_{kj}$ has $k > i$ ($a_{ik} = 0$) or $k \le i < j$ ($b_{kj} = 0$) $\implies (AB)_{ij} = 0$.
> - (e) **T.** $x = 0$ is a solution, and the number of pivots is $\le m < n$ $\implies$ a free variable $\implies$ infinitely many solutions.
> - (f) **T.** $(A^2)^T = (AA)^T = A^TA^T = AA = A^2$.
> - (g) **T.** $A(A^{-1}b) = b$: a solution exists. $Ax = b \implies x = A^{-1}Ax = A^{-1}b$: it is unique.
> - (h) **T.** $A \cdot A^2 = A^2 \cdot A = A^3 = I \implies A^{-1} = A^2$.
> - (i) **T.** $Bx = 0 \implies (AB)x = 0 \implies x = 0$, so $B$ is invertible; then $A = (AB)B^{-1}$ is a product of invertible matrices.
> - (j) **F.** $A = \begin{bmatrix} 1 \\ 1 \end{bmatrix}$ ($m = 2$, $n = 1$): $\operatorname{rank}(A) = 1 = n$, but $b = \begin{bmatrix} 0 \\ 1 \end{bmatrix}$ asks for $x = 0$ and $x = 1$: no solution.
>
> \# (j): consistent for every $b$ $\iff$ $\operatorname{rank}(A) = m$, a pivot in every row. $\operatorname{rank}(A) = n$ says instead that a solution, when there is one, is unique. (i): "$Bx = 0$ has only $x = 0$ $\implies$ $B$ is invertible" holds for square $B$; it is one of the equivalent conditions for an invertible matrix.

## Q2 Skew-Symmetric Matrix

> [!question]
> (6 pts) Find $a$ to $f$ so that the matrix $A$ is skew-symmetric.
> $$
> A = \begin{bmatrix} 0 & -1 & a & 0 \\ b & 0 & c & 8 \\ 2 & -7 & 0 & d \\ e & f & 6 & 0 \end{bmatrix}.
> $$

> [!attempt] My answer: 6/6
> $$
> \begin{aligned}
> &\because A \text{ is skew-symmetric metrix} \\
> &\therefore A^T = -A \\
> &\implies a = -2,\ \ b = -(-1) = 1,\ \ c = -(-7) = 7,\ \ d = -6, \\
> &\qquad e = 0,\ \ f = -8
> \end{aligned}
> $$

> [!solution]- Solution
> $$
> \begin{aligned}
> &A^T = -A \iff a_{ji} = -a_{ij} \ \ \forall\, i, j \\
> &a = a_{13} = -a_{31} = -2, \quad b = a_{21} = -a_{12} = 1, \quad c = a_{23} = -a_{32} = 7, \\
> &d = a_{34} = -a_{43} = -6, \quad e = a_{41} = -a_{14} = 0, \quad f = a_{42} = -a_{24} = -8.
> \end{aligned}
> $$
>
> \# Each unknown is the negative of its mirror entry across the diagonal. The diagonal itself must be $0$, since $a_{ii} = -a_{ii}$, and here it is.

## Q3 Reduced Row-Echelon Form

> [!question]
> (6 pts) Reduce the matrix below to its reduced row-echelon form. (Make sure each pivot is 1.)
> $$
> \begin{bmatrix} 1 & -2 & 1 & 1 & 2 \\ -1 & 2 & 0 & 2 & 3 \\ 2 & -4 & 1 & -1 & -1 \\ 0 & 0 & 1 & 3 & 5 \end{bmatrix}.
> $$

> [!attempt] My answer: 6/6
> $$
> \begin{aligned}
> &\begin{bmatrix} 1 & -2 & 1 & 1 & 2 \\ -1 & 2 & 0 & 2 & 3 \\ 2 & -4 & 1 & -1 & -1 \\ 0 & 0 & 1 & 3 & 5 \end{bmatrix}\!\begin{matrix} \vphantom{0} \\ \hookleftarrow{\times}1 \\ \hookleftarrow{\times}(-2) \\ \vphantom{0} \end{matrix} \overset{r}{\sim} \begin{bmatrix} 1 & -2 & 1 & 1 & 2 \\ 0 & 0 & 1 & 3 & 5 \\ 0 & 0 & -1 & -3 & -5 \\ 0 & 0 & 1 & 3 & 5 \end{bmatrix}\!\begin{matrix} \vphantom{0} \\ \vphantom{0} \\ \hookleftarrow{\times}1 \\ \hookleftarrow{\times}(-1) \end{matrix} \\[8pt]
> &\overset{r}{\sim} \begin{bmatrix} 1 & -2 & 1 & 1 & 2 \\ 0 & 0 & 1 & 3 & 5 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 6 \end{bmatrix}\!\begin{matrix} \hookleftarrow{\times}(-1) \\ \vphantom{0} \\ \vphantom{0} \\ \vphantom{0} \end{matrix} \overset{r}{\sim} \begin{bmatrix} 1 & -2 & 0 & -2 & -3 \\ 0 & 0 & 1 & 3 & 5 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \end{bmatrix}
> \end{aligned}
> $$
> Entry $(4, 5)$ of the third matrix reads $6$ ==(?)==. The grader wrote a "?" above the $-2$ in row 1 of the last matrix and a large "?" beside it, and took no points off.

> [!solution]- Solution
> $$
> \begin{aligned}
> &\begin{bmatrix} 1 & -2 & 1 & 1 & 2 \\ -1 & 2 & 0 & 2 & 3 \\ 2 & -4 & 1 & -1 & -1 \\ 0 & 0 & 1 & 3 & 5 \end{bmatrix} \overset{\substack{R_2 \to R_2 + R_1 \\ R_3 \to R_3 - 2R_1}}{\sim} \begin{bmatrix} 1 & -2 & 1 & 1 & 2 \\ 0 & 0 & 1 & 3 & 5 \\ 0 & 0 & -1 & -3 & -5 \\ 0 & 0 & 1 & 3 & 5 \end{bmatrix} \\[6pt]
> &\overset{\substack{R_3 \to R_3 + R_2 \\ R_4 \to R_4 - R_2}}{\sim} \begin{bmatrix} 1 & -2 & 1 & 1 & 2 \\ 0 & 0 & 1 & 3 & 5 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \end{bmatrix} \overset{R_1 \to R_1 - R_2}{\sim} \begin{bmatrix} 1 & -2 & 0 & -2 & -3 \\ 0 & 0 & 1 & 3 & 5 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \end{bmatrix}
> \end{aligned}
> $$
>
> \# The pivots are in columns 1 and 3; each is $1$ and the only nonzero entry of its column. Column 2 has no pivot, so its $-2$ stays. Your steps are the same; label the last matrix as the reduced row-echelon form, so that the reader sees where the answer is.

## Q4 Span of Two Vectors

> [!question]
> (6 pts) Determine whether the vector $b = [2, 1, 5]^{\top}$ is in the span of the vectors $v = [1, 2, 1]^{\top}$ and $w = [2, 1, 3]^{\top}$.

> [!attempt] My answer: 6/6
> $$
> \begin{aligned}
> &\text{Suppose } b \in \operatorname{span}\{v, w\}. \\
> &\implies \exists\, x, y \text{ s.t. } xv + yw = b \\[4pt]
> &\left[\begin{array}{cc|c} 1 & 2 & 2 \\ 2 & 1 & 1 \\ 1 & 3 & 5 \end{array}\right]\!\begin{matrix} \vphantom{0} \\ \hookleftarrow{\times}(-2) \\ \hookleftarrow{\times}(-1) \end{matrix} \overset{r}{\sim} \left[\begin{array}{cc|c} 1 & 2 & 2 \\ 0 & -3 & -3 \\ 0 & 1 & 3 \end{array}\right]\!\begin{matrix} \vphantom{0} \\ \downarrow \\ \uparrow \end{matrix} \overset{r}{\sim} \left[\begin{array}{cc|c} 1 & 2 & 2 \\ 0 & 1 & 3 \\ 0 & -3 & -3 \end{array}\right]\!\begin{matrix} \vphantom{0} \\ \vphantom{0} \\ \hookleftarrow{\times}3 \end{matrix} \\[8pt]
> &\overset{r}{\sim} \left[\begin{array}{cc|c} 1 & 2 & 2 \\ 0 & 1 & 3 \\ 0 & 0 & 6 \end{array}\right] \\[4pt]
> &\text{row 3 is } [0\ \ 0 \mid 6] \text{ i.e. } 0 = 6, \text{ which is impossible.} \\
> &\implies xv + yw = b \text{ has no solution} \\
> &\text{Hence } b \text{ is not in the span of the vector } v \text{ and } w.
> \end{aligned}
> $$

> [!solution]- Solution
> $$
> \begin{aligned}
> &b \in \operatorname{span}\{v, w\} \iff \exists\, x, y \text{ s.t. } xv + yw = b \iff [\,v\ \ w \mid b\,] \text{ is consistent.} \\[4pt]
> &\left[\begin{array}{cc|c} 1 & 2 & 2 \\ 2 & 1 & 1 \\ 1 & 3 & 5 \end{array}\right] \overset{\substack{R_2 \to R_2 - 2R_1 \\ R_3 \to R_3 - R_1}}{\sim} \left[\begin{array}{cc|c} 1 & 2 & 2 \\ 0 & -3 & -3 \\ 0 & 1 & 3 \end{array}\right] \overset{R_2 \leftrightarrow R_3}{\sim} \left[\begin{array}{cc|c} 1 & 2 & 2 \\ 0 & 1 & 3 \\ 0 & -3 & -3 \end{array}\right] \overset{R_3 \to R_3 + 3R_2}{\sim} \left[\begin{array}{cc|c} 1 & 2 & 2 \\ 0 & 1 & 3 \\ 0 & 0 & 6 \end{array}\right] \\[6pt]
> &\text{Row 3: } 0x + 0y = 6, \text{ impossible} \implies \text{no solution.} \\
> &\text{Hence } b \notin \operatorname{span}\{v, w\}.
> \end{aligned}
> $$
>
> \# Interchanging rows 2 and 3 makes the pivot $1$ and avoids fractions. A quick check: rows 1 and 2 alone give $x + 2y = 2$, $2x + y = 1$, so $x = 0$, $y = 1$; but then row 3 gives $0 + 3 = 3 \ne 5$.

## Q5 Norm and Dot Product

> [!question]
> (2+2+2 pts) Let $u = [2, 1, -2]$ and $v = [k, 2, 3]$.
> - (a) Find $\lVert u \rVert$.
> - (b) Find the value of $k$ such that $u$ and $v$ are orthogonal ($u \perp v$).
> - (c) If $k = 1$, find $(u + v) \cdot (u - v)$.

> [!attempt] My answer: 6/6
> $$
> \begin{aligned}
> &\text{(a)}\ \ \lVert a \rVert = \sqrt{2^2 + 1^2 + (-2)^2} = \sqrt{4 + 1 + 4} = \sqrt{9} = 3 \\[6pt]
> &\text{(b)}\ \ \text{If } u \perp v, \text{ then } u \cdot v = 0 \\
> &\qquad u \cdot v = 2 \cdot k + 1 \cdot 2 + (-2) \cdot 3 = 0 \\
> &\qquad \implies 2k = -2 + 6 \\
> &\qquad \implies k = 2 \\[6pt]
> &\text{(c)}\ \ (u + v) \cdot (u - v) \\
> &\qquad = [3, 3, 1] \cdot [1, -1, -5] \\
> &\qquad = 3 \cdot 1 + 3 \cdot (-1) \cdot 1 \cdot (-5) \\
> &\qquad = 3 - 3 - 5 \\
> &\qquad = -5
> \end{aligned}
> $$
> The norm in (a) reads $\lVert a \rVert$ ==(?)==.

> [!solution]- Solution
> $$
> \begin{aligned}
> &\text{(a)}\ \ \lVert u \rVert = \sqrt{2^2 + 1^2 + (-2)^2} = \sqrt{9} = 3. \\
> &\text{(b)}\ \ u \perp v \iff u \cdot v = 0 \iff 2k + 2 - 6 = 0 \iff k = 2. \\
> &\text{(c)}\ \ k = 1:\ v = [1, 2, 3],\ u + v = [3, 3, 1],\ u - v = [1, -1, -5] \\
> &\qquad (u + v) \cdot (u - v) = 3 \cdot 1 + 3 \cdot (-1) + 1 \cdot (-5) = -5.
> \end{aligned}
> $$
>
> \# Check (c): $(u + v) \cdot (u - v) = \lVert u \rVert^2 - \lVert v \rVert^2 = 9 - 14 = -5$. In your (c), the line $3 \cdot 1 + 3 \cdot (-1) \cdot 1 \cdot (-5)$ has a $\cdot$ where a $+$ belongs; the next line is right.

## Q6 A System with a Parameter

> [!question]
> (2+2+2 pts) Find all values of $k$ such that the following system
> $$
> \left\{\begin{aligned} x_1 + x_2 + x_3 &= 2 \\ 2x_1 + 3x_2 + 2x_3 &= 5 \\ x_1 + 2x_2 + k^2x_3 &= k + 2 \end{aligned}\right.
> $$
> has (a) no solution; (b) a unique solution; (c) infinitely many solutions.

> [!attempt] My answer: 6/6
> $$
> \begin{aligned}
> &[A \mid b] = \left[\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 2 & 3 & 2 & 5 \\ 1 & 2 & k^2 & k + 2 \end{array}\right]\!\begin{matrix} \vphantom{0} \\ \hookleftarrow{\times}(-2) \\ \hookleftarrow{\times}(-1) \end{matrix} \overset{r}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & 1 & 0 & 1 \\ 0 & 1 & k^2 - 1 & k \end{array}\right]\!\begin{matrix} \vphantom{0} \\ \vphantom{0} \\ \hookleftarrow{\times}(-1) \end{matrix} \\[8pt]
> &\overset{r}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & 1 & 0 & 1 \\ 0 & 0 & (k+1)(k-1) & k - 1 \end{array}\right] = [H \mid c]
> \end{aligned}
> $$
> $$
> \begin{array}{l|l|l}
> \text{(a)}\ \ k = -1 & \text{(b)}\ \ k \ne 1 \text{ and } k \ne -1 & \text{(c)}\ \ k = 1: \\
> \quad \text{row 3 is } [0\ 0\ 0 \mid -2] & \quad \text{every row has a pavit} & \quad \text{row 3 is } [0\ 0\ 0 \mid 0] \\
> \quad \text{i.e. } 0 = 2 & \quad \implies \operatorname{rank}(H) = 3 & \quad \implies \operatorname{rank}(H) = 2 < 3 \\
> \quad \implies \text{no solution} & \quad \implies \text{a unique solution} & \quad \implies \text{infinitely many solutions}
> \end{array}
> $$
> The word "and" in (b) was inserted by the grader. Beside each of (a), (b), (c) the grader wrote "why?" and struck it through ==(?)==.

> [!solution]- Solution
> $$
> \begin{aligned}
> &[A \mid b] \overset{\substack{R_2 \to R_2 - 2R_1 \\ R_3 \to R_3 - R_1}}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & 1 & 0 & 1 \\ 0 & 1 & k^2 - 1 & k \end{array}\right] \overset{R_3 \to R_3 - R_2}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & 1 & 0 & 1 \\ 0 & 0 & (k+1)(k-1) & k - 1 \end{array}\right] \\[6pt]
> &\text{(a)}\ \ k = -1:\ \text{row 3 is } [0\ \ 0\ \ 0 \mid -2],\ 0 = -2 \implies \text{no solution.} \\
> &\text{(b)}\ \ (k+1)(k-1) \ne 0, \text{ i.e. } k \ne 1 \text{ and } k \ne -1:\ 3 \text{ pivots} \implies \text{a unique solution.} \\
> &\text{(c)}\ \ k = 1:\ \text{row 3 is } [0\ \ 0\ \ 0 \mid 0],\ \operatorname{rank}(A) = \operatorname{rank}[A \mid b] = 2 < 3 \implies \text{infinitely many solutions.}
> \end{aligned}
> $$
>
> \# Factor the last pivot, $k^2 - 1 = (k+1)(k-1)$, and compare it with the right side $k - 1$: at $k = 1$ both are $0$, at $k = -1$ only the pivot is. In (a) your row 3 is right, but the next line should read $0 = -2$, not $0 = 2$ (no points off).

## Q7 Inverse by Row Reduction

> [!question]
> **(a)** (6 pts) Let $A$ be an $n \times n$ matrix. Prove that if $A$ is row equivalent to the identity matrix $I$, then $A$ is invertible and $A^{-1}$ can be found by $[A \mid I] \overset{r}{\sim} [I \mid A^{-1}]$.
>
> **(b)** (6 pts) Find the inverse of the matrix:
> $$
> A = \begin{bmatrix} 1 & 2 & 1 \\ 2 & 5 & 4 \\ 1 & 1 & 0 \end{bmatrix}.
> $$

> [!attempt] My answer: 9/12
> **(a)** 3/6
> $$
> \begin{aligned}
> &\because A \overset{r}{\sim} I \\
> &\therefore \exists\, E_1, \dots, E_k \text{ s.t. } E_k \cdots E_k A = I \\
> &\text{Let } P = E_k \cdots E_1 \text{ an } n \times n \text{ invertible matrix.} \\
> &Ax = 0 \implies x = Ix = (PA)x = P(Ax) = P0 = 0 \\
> &\implies A \text{ is invertible,} \\
> &P[A \mid I] = [PA \mid PI] = [I \mid P] \\
> &P = P \cdot I = P(AA^{-1}) = (PA)A^{-1} = A^{-1} \\
> &\implies [A \mid I] \overset{r}{\sim} [I \mid A^{-1}] \\[6pt]
> &\text{Hence } A \text{ is invertible and } A^{-1} \text{ can found by } [A \mid I] \overset{r}{\sim} [I \mid A^{-1}]
> \end{aligned}
> $$
> Line 2 reads $E_k \cdots E_k A$ ==(?)==. The grader underlined "Let" and "invertible" and wrote "?" above "invertible"; wrote "$\implies PA = I$ ?" after the line of $P$; underlined $(PA)$ and wrote "$I$?" under it; put "?" after $P0 = 0$; wrote "$A^{-1}$?" after "invertible,"; and put "?" after $= A^{-1}$.
>
> **(b)** 6/6
> $$
> \begin{aligned}
> &[A \mid I] = \left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 2 & 5 & 4 & 0 & 1 & 0 \\ 1 & 1 & 0 & 0 & 0 & 1 \end{array}\right]\!\begin{matrix} \vphantom{0} \\ \hookleftarrow{\times}(-2) \\ \hookleftarrow{\times}(-1) \end{matrix} \overset{r}{\sim} \left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 2 & -2 & 1 & 0 \\ 0 & -1 & -1 & -1 & 0 & 1 \end{array}\right]\!\begin{matrix} \hookleftarrow{\times}(-2) \\ \vphantom{0} \\ \hookleftarrow{\times}1 \end{matrix} \\[8pt]
> &\overset{r}{\sim} \left[\begin{array}{ccc|ccc} 1 & 0 & -3 & 5 & -2 & 0 \\ 0 & 1 & 2 & -2 & 1 & 0 \\ 0 & 0 & 1 & -3 & 1 & 1 \end{array}\right]\!\begin{matrix} \hookleftarrow{\times}3 \\ \hookleftarrow{\times}(-2) \\ \vphantom{0} \end{matrix} \overset{r}{\sim} \left[\begin{array}{ccc|ccc} 1 & 0 & 0 & -4 & 1 & 3 \\ 0 & 1 & 0 & 4 & -1 & -2 \\ 0 & 0 & 1 & -3 & 1 & 1 \end{array}\right] = [I \mid A^{-1}]\ \text{(by (a))} \\[8pt]
> &\text{Hence } A^{-1} = \begin{bmatrix} -4 & 1 & 3 \\ 4 & -1 & -2 \\ -3 & 1 & 1 \end{bmatrix}.
> \end{aligned}
> $$
> The grader rewrote the $3$ in row 1 of the last matrix in red and wrote at the bottom of the page, in Chinese: "Please write clearly; too small."

> [!failure] Mistake: (a) proves invertibility with a result that rests on (a)
> "$Ax = 0$ has only $x = 0$ $\implies$ $A$ is invertible" is one of the equivalent conditions for an invertible matrix, and in lecture it is proved by going through $A \overset{r}{\sim} I$, the very statement of (a). Using it here argues in a circle. The proof also never writes $PA = I$ (it is the line $E_k \cdots E_1A = I$) or says why $P$ is invertible, and the last steps use both. These two facts finish the proof at once: $A = P^{-1}(PA) = P^{-1}$, so $A$ is invertible and $A^{-1} = P$. The grader's "?" marks stand at these places.

> [!proof]- Proof of (a)
> $$
> \begin{aligned}
> &\because A \overset{r}{\sim} I \\
> &\therefore \exists \text{ row-elementary } E_1, \dots, E_k \text{ s.t. } E_k \cdots E_1A = I. \\
> &\text{Let } P = E_k \cdots E_1 \implies PA = I. \\
> &\text{Each } E_t \text{ is invertible (its inverse undoes the row operation)} \implies P \text{ is invertible.} \\
> &\implies A = P^{-1}(PA) = P^{-1}I = P^{-1} \\
> &\implies A \text{ is invertible and } A^{-1} = (P^{-1})^{-1} = P. \\[6pt]
> &P[A \mid I] = [PA \mid PI] = [I \mid P] = [I \mid A^{-1}], \\
> &\text{i.e. the row operations of } E_1, \dots, E_k \text{ take } [A \mid I] \text{ to } [I \mid A^{-1}]:\ [A \mid I] \overset{r}{\sim} [I \mid A^{-1}]. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The order matters: first $PA = I$ and $P$ invertible, then $A = P^{-1}$. No result about $Ax = 0$ is needed, and $A^{-1}$ is known to exist before it is used. Your lines $P[A \mid I] = [I \mid P]$ and $P = A^{-1}$ are right once these come first.

> [!solution]- Solution
> **(b)**
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 2 & 5 & 4 & 0 & 1 & 0 \\ 1 & 1 & 0 & 0 & 0 & 1 \end{array}\right] \overset{\substack{R_2 \to R_2 - 2R_1 \\ R_3 \to R_3 - R_1}}{\sim} \left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 2 & -2 & 1 & 0 \\ 0 & -1 & -1 & -1 & 0 & 1 \end{array}\right] \\[6pt]
> &\overset{\substack{R_1 \to R_1 - 2R_2 \\ R_3 \to R_3 + R_2}}{\sim} \left[\begin{array}{ccc|ccc} 1 & 0 & -3 & 5 & -2 & 0 \\ 0 & 1 & 2 & -2 & 1 & 0 \\ 0 & 0 & 1 & -3 & 1 & 1 \end{array}\right] \overset{\substack{R_1 \to R_1 + 3R_3 \\ R_2 \to R_2 - 2R_3}}{\sim} \left[\begin{array}{ccc|ccc} 1 & 0 & 0 & -4 & 1 & 3 \\ 0 & 1 & 0 & 4 & -1 & -2 \\ 0 & 0 & 1 & -3 & 1 & 1 \end{array}\right] \\[6pt]
> &\implies A^{-1} = \begin{bmatrix} -4 & 1 & 3 \\ 4 & -1 & -2 \\ -3 & 1 & 1 \end{bmatrix}
> \end{aligned}
> $$
>
> \# Check one column: $A\begin{bmatrix} 3 \\ -2 \\ 1 \end{bmatrix} = \begin{bmatrix} 3 - 4 + 1 \\ 6 - 10 + 4 \\ 3 - 2 + 0 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}$, the third column of $I$.

## Q8 Matrix from the General Solution

> [!question]
> (6 pts) If $b = \begin{bmatrix} 2 \\ 1 \\ 4 \end{bmatrix}$ and the general solution to $Ax = b$ is $x = \begin{bmatrix} 1 \\ 0 \\ 2 \end{bmatrix} + \alpha\begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix} + \beta\begin{bmatrix} -2 \\ 0 \\ 1 \end{bmatrix}$, where $\alpha$ and $\beta$ are free parameters, determine the matrix $A$.

> [!attempt] My answer: 0/6
> Left blank.

> [!failure] Mistake: no answer
> The general solution gives three equations for $A$. With $p = [1, 0, 2]^T$, $u_1 = [1, 1, 0]^T$, $u_2 = [-2, 0, 1]^T$: $\alpha = \beta = 0$ gives $Ap = b$; $\alpha = 1$, $\beta = 0$ gives $A(p + u_1) = b$, so $Au_1 = 0$; in the same way $Au_2 = 0$. These determine $A$.

> [!solution]- Solution
> $$
> \begin{aligned}
> &x, b \in \mathbb{R}^3 \implies A \text{ is } 3 \times 3. \text{ Let } p = \begin{bmatrix} 1 \\ 0 \\ 2 \end{bmatrix},\ u_1 = \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix},\ u_2 = \begin{bmatrix} -2 \\ 0 \\ 1 \end{bmatrix}. \\
> &\alpha = \beta = 0:\ Ap = b. \qquad \alpha = 1,\ \beta = 0:\ A(p + u_1) = b \implies Au_1 = 0. \qquad \text{Similarly } Au_2 = 0. \\[6pt]
> &\text{Each row } r = [\,r_1\ \ r_2\ \ r_3\,] \text{ of } A \text{ satisfies } ru_1 = 0,\ ru_2 = 0: \\
> &\qquad r_1 + r_2 = 0,\ \ -2r_1 + r_3 = 0 \implies r = r_1\,[\,1\ \ {-1}\ \ 2\,]. \\
> &\text{Row } i \text{ of } Ap = b:\ r_1\big(1 \cdot 1 + (-1) \cdot 0 + 2 \cdot 2\big) = 5r_1 = b_i \implies r_1 = \tfrac{1}{5}b_i. \\[6pt]
> &\implies A = \frac{1}{5}\begin{bmatrix} 2 \\ 1 \\ 4 \end{bmatrix}\begin{bmatrix} 1 & -1 & 2 \end{bmatrix} = \frac{1}{5}\begin{bmatrix} 2 & -2 & 4 \\ 1 & -1 & 2 \\ 4 & -4 & 8 \end{bmatrix}
> \end{aligned}
> $$
>
> \# Check: $Ap = \tfrac{1}{5}b\,(1 + 0 + 4) = b$, $Au_1 = \tfrac{1}{5}b\,(1 - 1 + 0) = 0$, $Au_2 = \tfrac{1}{5}b\,(-2 + 0 + 2) = 0$. Conversely, $Ax = b \iff x_1 - x_2 + 2x_3 = 5$, a plane, which is exactly $p + \alpha u_1 + \beta u_2$. The same idea as [[LA1 Midterm 114-1 Solutions#Q7 Matrix from the General Solution|114-1 Q7]]: $p$ is a particular solution, and $u_1$, $u_2$ solve $Ax = 0$.

## Q9 Product of Symmetric Matrices

> [!question]
> (6 pts) Let $A$ and $B$ be $n \times n$ symmetric matrices. Prove that $AB$ is symmetric if and only if $A$ and $B$ commute (i.e., $AB = BA$).

> [!attempt] My answer: 4/6
> $$
> \begin{aligned}
> &\text{(⇒)}\ \ AB \text{ is symmetric} \\
> &\qquad \implies (AB)^T = AB \\
> &\qquad \implies B^TA^T = AB \\
> &\qquad \implies BA = AB \implies A \text{ and } B \text{ commute} \\[6pt]
> &\text{(⇐)}\ \ A \text{ and } B \text{ commute} \implies AB = BA \\
> &\qquad (AB)^T = B^TA^T \\
> &\qquad \hphantom{(AB)^T} = BA \\
> &\qquad \hphantom{(AB)^T} = AB \quad (\text{by } AB = BA) \\
> &\qquad \implies AB \text{ is symmetric} \\[6pt]
> &\text{Hence } AB \text{ is symmetric iff } A \text{ and } B \text{ commute.}
> \end{aligned}
> $$
> The grader circled the $\implies$ before $BA = AB$ in (⇒) and the $=$ before $BA$ in (⇐), with a "?" beside each. Lower on the page, apart from the proof, is the scratch "$A^T = A$ symmetric".

> [!failure] Mistake: the symmetry of A and B is never used
> $B^TA^T = BA$ holds because $A$ and $B$ are symmetric: $A^T = A$ and $B^T = B$. Without this, $B^TA^T$ and $BA$ are different matrices, and the two circled steps have no reason. The fact appears only as scratch lower on the page; it has to stand at the step, in both directions.

> [!proof]- Proof
> $$
> \begin{aligned}
> &A, B \text{ symmetric} \implies A^T = A,\ B^T = B \implies (AB)^T = B^TA^T = BA. \\[4pt]
> &\text{(⇒)}\ \ AB \text{ symmetric} \implies AB = (AB)^T = BA. \\
> &\text{(⇐)}\ \ AB = BA \implies (AB)^T = BA = AB \implies AB \text{ symmetric.} \\
> &\text{Hence } AB \text{ is symmetric} \iff AB = BA. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Write the hypothesis $A^T = A$, $B^T = B$ once at the top, then both directions are one line each.

## Q10 Row Equivalence and Gaussian Elimination

> [!question]
> $A$ and $B$ are $m \times n$ matrices. $b$ and $c$ are $m \times 1$ matrices.
>
> **(1)** (6 pts) Prove that if $[A \mid b] \overset{r}{\sim} [B \mid c]$, then $Ax = b$ and $Bx = c$ have the same solution set.
>
> **(2)** (6 pts) Use Gaussian elimination with back substitution to solve
> $$
> \begin{cases} x_1 - 2x_2 + x_3 = 3 \\ 2x_1 - 3x_2 + 4x_3 = 8 \\ -x_1 + 4x_2 + 2x_3 = 3 \end{cases}.
> $$

> [!attempt] My answer: 10/12
> **(1)** 6/6
> $$
> \begin{aligned}
> &[A \mid b] \overset{r}{\sim} [B \mid c] \implies \exists\, E_1, \dots, E_k \text{ s.t. } E_k \cdots E_1[A \mid b] = [B \mid c] \\
> &\text{let } P = E_k \cdots E_1 \text{ an } m \times m \text{ invertible metric} \\
> &P[A \mid b] = [PA \mid Pb] = [B \mid c] \implies PA = B,\ Pb = c \\
> &Ax = b \implies PAx = Pb \implies Bx = c. \\
> &Bx = c \implies PAx = Pb \implies P^{-1}PAx = P^{-1}Pb \implies Ax = b \\
> &\text{Hence if } [A \mid b] \overset{r}{\sim} [B \mid c], \text{ then } Ax = b \text{ and } Bx = c \text{ have the same solution set.}
> \end{aligned}
> $$
>
> **(2)** 4/6
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 1 & -2 & 1 & 3 \\ 2 & -3 & 4 & 8 \\ -1 & 4 & 2 & 3 \end{array}\right]\!\begin{matrix} \vphantom{0} \\ \hookleftarrow{\times}(-2) \\ \hookleftarrow{\times}1 \end{matrix} \overset{r}{\sim} \left[\begin{array}{ccc|c} 1 & -2 & 1 & 3 \\ 0 & 1 & 2 & 2 \\ 0 & 2 & 3 & 6 \end{array}\right]\!\begin{matrix} \vphantom{0} \\ \vphantom{0} \\ \hookleftarrow{\times}(-2) \end{matrix} \overset{r}{\sim} \left[\begin{array}{ccc|c} 1 & -2 & 1 & 3 \\ 0 & 1 & 2 & 2 \\ 0 & 0 & -1 & 2 \end{array}\right] \\[8pt]
> &\implies \begin{cases} x_1 - 2x_2 + x_3 = 3 \implies x_1 = 3 + 2 \cdot 10 - (-2) = 25 \\ x_2 + 2x_3 = 2 \implies x_2 = 2 - 4(-2) = 10 \\ -x_3 = 2 \implies x_3 = -2 \end{cases} \\[8pt]
> &\implies x = \begin{bmatrix} 25 \\ 10 \\ -2 \end{bmatrix}
> \end{aligned}
> $$
> The grader circled $25$ and $10$ in the last line.

> [!failure] Mistake: (2) a coefficient changed in back substitution
> Row 2 says $x_2 + 2x_3 = 2$, so $x_2 = 2 - 2x_3 = 2 - 2(-2) = 6$; the attempt wrote $2 - 4(-2) = 10$. Row 1 then carried the wrong $x_2$: $x_1 = 3 + 2 \cdot 6 - (-2) = 17$, not $25$. The row reduction is right. Putting the answer back into the second original equation would have caught it: $2 \cdot 25 - 3 \cdot 10 + 4(-2) = 12 \ne 8$.

> [!proof]- Proof of (1)
> $$
> \begin{aligned}
> &[A \mid b] \overset{r}{\sim} [B \mid c] \implies \exists \text{ row-elementary } E_1, \dots, E_k \text{ s.t. } E_k \cdots E_1[A \mid b] = [B \mid c]. \\
> &\text{Let } P = E_k \cdots E_1:\ m \times m, \text{ invertible (each } E_t \text{ is invertible).} \\
> &P[A \mid b] = [PA \mid Pb] = [B \mid c] \implies PA = B,\ Pb = c. \\[4pt]
> &Ax = b \implies PAx = Pb \implies Bx = c. \\
> &Bx = c \implies PAx = Pb \implies P^{-1}PAx = P^{-1}Pb \implies Ax = b. \\
> &\text{Hence } Ax = b \text{ and } Bx = c \text{ have the same solution set.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# This is your proof, with the reason why $P$ is invertible added: each row-elementary matrix is.

> [!solution]- Solution
> **(2)**
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 1 & -2 & 1 & 3 \\ 2 & -3 & 4 & 8 \\ -1 & 4 & 2 & 3 \end{array}\right] \overset{\substack{R_2 \to R_2 - 2R_1 \\ R_3 \to R_3 + R_1}}{\sim} \left[\begin{array}{ccc|c} 1 & -2 & 1 & 3 \\ 0 & 1 & 2 & 2 \\ 0 & 2 & 3 & 6 \end{array}\right] \overset{R_3 \to R_3 - 2R_2}{\sim} \left[\begin{array}{ccc|c} 1 & -2 & 1 & 3 \\ 0 & 1 & 2 & 2 \\ 0 & 0 & -1 & 2 \end{array}\right] \\[6pt]
> &-x_3 = 2 \implies x_3 = -2 \\
> &x_2 + 2x_3 = 2 \implies x_2 = 2 - 2(-2) = 6 \\
> &x_1 - 2x_2 + x_3 = 3 \implies x_1 = 3 + 2 \cdot 6 - (-2) = 17 \\
> &\implies x = \begin{bmatrix} 17 \\ 6 \\ -2 \end{bmatrix}
> \end{aligned}
> $$
>
> \# Back substitution goes from the last row up. Check in the original system: $17 - 12 - 2 = 3$, $34 - 18 - 8 = 8$, $-17 + 24 - 4 = 3$.

## Q11 LU Factorization and Solving

> [!question]
> (4+2 pts) Let $A = \begin{bmatrix} 1 & 2 & -1 \\ 2 & 5 & 1 \\ -1 & -2 & 3 \end{bmatrix}$, $b = \begin{bmatrix} 2 \\ 7 \\ 2 \end{bmatrix}$. Find an $LU$ factorization of $A$, then solve the linear system $Ax = b$ using the factorization together with forward and back substitutions.

> [!attempt] My answer: 6/6
> $$
> \begin{aligned}
> &\begin{bmatrix} 1 & 2 & -1 \\ 2 & 5 & 1 \\ -1 & -2 & 3 \end{bmatrix}\!\begin{matrix} \vphantom{0} \\ \hookleftarrow{\times}(-2) \\ \hookleftarrow{\times}1 \end{matrix} \overset{r}{\sim} \begin{bmatrix} 1 & 2 & -1 \\ 2 & 1 & 3 \\ -1 & 0 & 2 \end{bmatrix} \implies L = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ -1 & 0 & 1 \end{bmatrix},\ \ U = \begin{bmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \\ 0 & 0 & 2 \end{bmatrix} \\[8pt]
> &\text{Let } Ux = y \\
> &Ax = b \implies (LU)x = b \implies L(Ux) = b \implies Ly = b \\
> &Ly = b: \\
> &\qquad \begin{cases} y_1 = 2 \implies y_1 = 2 \\ 2y_1 + y_2 = 7 \implies y_2 = 7 - 2 \cdot 2 = 3 \\ -y_1 + y_3 = 2 \implies y_3 = 2 + 2 = 4 \end{cases} \\[8pt]
> &Ux = y: \\
> &\qquad \begin{cases} x_1 + 2x_2 - x_3 = 2 \implies x_1 = 2 - 2 \cdot (-3) + 2 = 10 \\ x_2 + 3x_3 = 3 \implies x_2 = 3 - 3 \cdot 2 = -3 \\ 2x_3 = 4 \implies x_3 = 2 \end{cases} \\[8pt]
> &\implies x = \begin{bmatrix} 10 \\ -3 \\ 2 \end{bmatrix}
> \end{aligned}
> $$

> [!solution]- Solution
> $$
> \begin{aligned}
> &A \overset{\substack{R_2 \to R_2 - 2R_1 \\ R_3 \to R_3 + R_1}}{\sim} \begin{bmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \\ 0 & 0 & 2 \end{bmatrix} = U, \qquad L = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ -1 & 0 & 1 \end{bmatrix}, \qquad A = LU. \\[6pt]
> &Ax = b \iff L(Ux) = b. \text{ Let } y = Ux. \\
> &\text{Forward: } Ly = b:\ y_1 = 2,\ \ y_2 = 7 - 2y_1 = 3,\ \ y_3 = 2 + y_1 = 4. \\
> &\text{Back: } Ux = y:\ 2x_3 = 4 \implies x_3 = 2,\ \ x_2 = 3 - 3x_3 = -3,\ \ x_1 = 2 - 2x_2 + x_3 = 10. \\
> &\implies x = \begin{bmatrix} 10 \\ -3 \\ 2 \end{bmatrix}
> \end{aligned}
> $$
>
> \# In $L$, entry $(i, j)$ is the multiple of row $j$ subtracted from row $i$: $\ell_{21} = 2$, $\ell_{31} = -1$, $\ell_{32} = 0$, since row 3 needed no second step. Your second matrix stores exactly these numbers below the diagonal. Check: $Ax = [10 - 6 - 2,\ 20 - 15 + 2,\ -10 + 6 + 6] = [2, 7, 2] = b$.

## Q12 A Commutator Equal to B

> [!question]
> (6 pts) Let $A$ and $B$ be $n \times n$ matrices. If $AB - BA = B$, then $B$ must be singular.

> [!attempt] My answer: 0/6
> $$
> \begin{aligned}
> &\text{Suppose } B \text{ is invertible.} \\
> &B^{-1}B = BB^{-1} = I \\
> &BB^{-1} = (AB - BA) \cdot B^{-1} \\
> &\hphantom{BB^{-1}} = ABB^{-1} - BAB^{-1} \\
> &\hphantom{BB^{-1}} = A - BAB^{-1} \\
> &\hphantom{BB^{-1}} = B^{-1}(BA) - BAB^{-1} \\
> &\hphantom{BB^{-1}} = \qquad \text{✗}
> \end{aligned}
> $$

> [!failure] Mistake: the proof stops after the right equation
> The attempt reaches $I = A - BAB^{-1}$, which is the right equation, then rewrites $A$ as $B^{-1}(BA)$, which leads nowhere. The missing idea is the [[Trace|trace]]: $\operatorname{tr}(BAB^{-1}) = \operatorname{tr}(A)$, so the right side has trace $0$, while $\operatorname{tr}(I) = n$. Taking the trace of $AB - BA = B$ directly gives only $\operatorname{tr}(B) = 0$, which does not make $B$ singular.

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{Suppose } B \text{ is invertible.} \\
> &AB - BA = B \implies (AB - BA)B^{-1} = BB^{-1} \implies A - BAB^{-1} = I. \\
> &\implies \operatorname{tr}(A) - \operatorname{tr}(BAB^{-1}) = \operatorname{tr}(I) = n. \\
> &\operatorname{tr}(BAB^{-1}) = \operatorname{tr}\big((BA)B^{-1}\big) = \operatorname{tr}\big(B^{-1}(BA)\big) = \operatorname{tr}(A) \quad (\operatorname{tr}(XY) = \operatorname{tr}(YX)) \\
> &\implies 0 = n \quad (\rightarrow\leftarrow) \\
> &\text{Hence } B \text{ is singular.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The same idea as [[LA1 Midterm 114-1 Solutions#Q12 A Commutator Equal to A|114-1 Q12]], with the roles of $A$ and $B$ exchanged: multiply by the inverse so that one side becomes $I$, whose trace is $n \ne 0$. Such matrices exist: $A = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$ and $B = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$ give $AB - BA = B$, and this $B$ is singular.

## Q13 Inverse of a Sum of Inverses

> [!question]
> (6 pts) Let $A$ and $B$ be $n \times n$ invertible matrices such that $A + B$ is invertible. Show that $(A^{-1} + B^{-1})^{-1} = A(A + B)^{-1}B$.

> [!attempt] My answer: 6/6
> $$
> \begin{aligned}
> &(A^{-1} + B^{-1}) \cdot A(A + B)^{-1}B \\
> &= A^{-1}A(A + B)^{-1}B + B^{-1}A(A + B)^{-1}B \\
> &= (A + B)^{-1}B + B^{-1}A(A + B)^{-1}B \\
> &= (I + B^{-1}A)(A + B)^{-1}B \\
> &= B^{-1}(B + A)(A + B)^{-1}B \\
> &= B^{-1}(A + B)(A + B)^{-1}B \\
> &= B^{-1}B \\
> &= I \\[6pt]
> &\because A(A + B)^{-1}B \text{ is right inverse of } (A^{-1} + B^{-1}) \text{ and } (A^{-1} + B^{-1}) \text{ is square matrices} \\
> &\therefore A(A + B)^{-1}B \text{ is the invose of } (A^{-1} + B^{-1}) \\
> &\text{Hence } (A^{-1} + B^{-1})^{-1} = A(A + B)^{-1}B.
> \end{aligned}
> $$

> [!proof]- Proof
> $$
> \begin{aligned}
> &\text{Let } M = A(A + B)^{-1}B. \\
> &(A^{-1} + B^{-1})M = A^{-1}A(A + B)^{-1}B + B^{-1}A(A + B)^{-1}B = (I + B^{-1}A)(A + B)^{-1}B \\
> &\hphantom{(A^{-1} + B^{-1})M} = B^{-1}(B + A)(A + B)^{-1}B = B^{-1}IB = I. \\
> &\therefore M \text{ is a right inverse of the square matrix } A^{-1} + B^{-1} \\
> &\implies A^{-1} + B^{-1} \text{ is invertible and } (A^{-1} + B^{-1})^{-1} = M = A(A + B)^{-1}B. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Factor $I + B^{-1}A = B^{-1}B + B^{-1}A = B^{-1}(B + A)$: $B^{-1}$ comes out on the left because it stands on the left of $A$. The last step uses that a one-sided inverse of a square matrix is its inverse; [[LA1 Midterm 114-1 Solutions#Q13 Left Inverse and an Inverse Formula|114-1 Q13 (a)]] proves it for a left inverse, and $XM = I$ says that $X$ is a left inverse of $M$, so $M^{-1} = X$ and $X^{-1} = M$.

## Q14 Nilpotent Matrix

> [!question]
> (6 pts) An $n \times n$ matrix $A$ is called nilpotent if $A^k = O$ for some positive integer $k$. If $A^3 = O$, find the inverse of $I - A$ in terms of $I$, $A$, and $A^2$ ==(?)==.

> [!attempt] My answer: 6/6
> $$
> \begin{aligned}
> (I - A)(I + A + A^2) &= I + A + A^2 - A - A^2 - A^3 \\
> &= I - A^3 \\
> &= I - O \\
> &= I \\
> (I + A + A^2)(I - A) &= I - A + A - A^2 + A^2 - A^3 \\
> &= I - A^3 \\
> &= I - O \\
> &= I
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\because (I - A)(I + A + A^2) = (I + A + A^2)(1 - A) = I \\
> &\therefore I + A + A^2 \text{ is the inverse of } 1 - A.
> \end{aligned}
> $$

> [!solution]- Solution
> $$
> \begin{aligned}
> &(I - A)(I + A + A^2) = I + A + A^2 - A - A^2 - A^3 = I - A^3 = I - O = I, \\
> &(I + A + A^2)(I - A) = I - A + A - A^2 + A^2 - A^3 = I - A^3 = I. \\
> &\implies (I - A)^{-1} = I + A + A^2.
> \end{aligned}
> $$
>
> \# The same algebra as $(1 - x)(1 + x + x^2) = 1 - x^3$ for numbers; it works for matrices because $I$ and $A$ commute. In general, $A^k = O$ gives $(I - A)^{-1} = I + A + \cdots + A^{k-1}$.

> [!todo] Transcription check
> - Q3: in the third matrix of the attempt, entry $(4, 5)$ reads $6$; the step gives $0$, and the next matrix is computed with $0$.
> - Q5 (a): the norm in the attempt reads $\lVert a \rVert$; $\lVert u \rVert$ is meant.
> - Q6: the red "why?" beside each of (a), (b), (c) looks struck through, so it is read as withdrawn.
> - Q7 (a): line 2 of the attempt reads $E_k \cdots E_k A = I$; $E_k \cdots E_1 A = I$ is meant, as in the next line.
> - Q14: the last line of the question is cut off at the bottom edge of the print; the last power is read as $A^2$.
