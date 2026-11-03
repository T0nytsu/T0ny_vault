---
course: [LA1]
semester: "115-1"
chapter: ["1.2", "1.3", "1.4", "1.5", "10.2"]
tags: [linear-algebra, exam, questions, matrix-algebra, matrix-inverse, linear-systems]
source:
  - "113-1, Linear Algebra I – Midterm, printed paper, photo (2 pages)"
created: 2026-11-02
solutions: "[[LA1 Midterm 113-1 Solutions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> A past midterm of this course: Linear Algebra I, semester 113-1, 15 questions, 100 points. It covers FB §1.2–1.5 and §10.2: [[Orthogonal Vectors|perpendicular vectors]], the [[Transpose|transpose]] and the [[Trace|trace]], [[Skew-Symmetric Matrix|skew-symmetric matrices]], [[Elementary Matrix|elementary matrices]], [[Invertible Matrix|inverses]], [[Rank|rank]] and [[Span|span]], [[Row Equivalence|row equivalence]], [[Gaussian Elimination|Gaussian elimination]], the [[LU-Factorization|LU-factorization]], [[Block Matrix|block matrices]] and consistency of [[Linear System|linear systems]].
>
> Write it as a timed paper, then check with [[LA1 Midterm 113-1 Solutions]].

> [!note] Notation
> The paper writes the transpose as $A^{\top}$. Vectors and $m \times 1$ matrices are not bold ($v$, $w$, $b$, $c$, $x$), and $[A \mid b] \overset{r}{\sim} [B \mid c]$ means that the two augmented matrices are row equivalent. $O$ is a zero matrix.

## Q1 True or False

(10 pts) Label the following statements as True or False.
- (a) $AB = BA$.
- (b) If $A$ is invertible, then $A + A^{\top}$ is invertible.
- (c) Every linear system with the same number of equations as unknowns has a unique solution.
- (d) $AB = I$ implies that $A$ and $B$ are invertable.
- (e) If $A$ and $B$ are invertible, then $(A + B)^{-1} = A^{-1} + B^{-1}$.
- (f) If $A$ is an $n \times n$ matrix, then $\operatorname{tr}(A) = \operatorname{tr}(A^{\top})$.
- (g) A linear system with coefficient matrix $A$ has an infinite number of solutions if and only if $A$ can be row-reduced to an echelon matrix that includes some column containing no pivot.
- (h) Every elementary matrix is invertible.
- (i) If $A^2 = A$, then $A = O$ or $A = I$.
- (j) If $AB = C$ and two of the matrices are singular, then so is the third.

## Q2 Seventh Power of a Matrix

(5 pts) Let
$$
A = \begin{bmatrix} 0 & 0 & -1 \\ 0 & 2 & 0 \\ 1 & 0 & 0 \end{bmatrix}.
$$
Find $A^7$.

## Q3 Rank and Span

(4+1 pts) Find the rank of $A$ and determine whether the span of the column vectors of $A$ is $\mathbb{R}^4$.
$$
A = \begin{bmatrix} 1 & 2 & 3 & 4 \\ 8 & 7 & 6 & 5 \\ 9 & 10 & 11 & 12 \\ 16 & 15 & 14 & 13 \end{bmatrix}.
$$

## Q4 Rank Depending on t

(5 pts) $t \in \mathbb{R}$. Compute the rank of the following matrix, which depends on $t$.
$$
A = \begin{bmatrix} t^2 & 1 & t^2 \\ t & t^2 & t \\ t & t & t^2 \end{bmatrix}.
$$

## Q5 Inverse of a Skew-Symmetric Matrix

(5 pts) If $A$ is invertible and skew-symmetric, then $-A^{-1}$ is skew-symmetric.

## Q6 When the Matrix Is Invertible

(5 pts) Find all numbers $r$ such that
$$
A = \begin{bmatrix} 2 & 4 & 2 \\ 1 & r & 3 \\ 1 & 1 & 2 \end{bmatrix}
$$
is invertible.

## Q7 Row Equivalence, Gaussian Elimination and LU

$A$ and $B$ are $m \times n$ matrices. $b$ and $c$ are $m \times 1$ matrices.

**(a)** (5 pts) Prove that if $[A \mid b] \overset{r}{\sim} [B \mid c]$, then $Ax = b$ and $Bx = c$ have the same solution set.

**(b)** (5 pts) Use Gaussian method with back substitution to solve
$$
\begin{cases} x_1 + 2x_2 - x_3 = -3, \\ 3x_1 + 7x_2 + 2x_3 = 1, \\ 4x_1 - 2x_2 + x_3 = -2. \end{cases}
$$

**(c)** (5 pts) Find an $LU$-factorization of
$$
A = \begin{bmatrix} 1 & 2 & -1 \\ 3 & 7 & 2 \\ 4 & -2 & 1 \end{bmatrix}.
$$

## Q8 Square Invertible Implies Cube Invertible

(5 pts) Let $A$ be a matrix such that $A^2$ is invertible. Prove that $A^3$ is invertible.

## Q9 Perpendicular Vectors

(5 pts) For vectors $v$ and $w$ in $\mathbb{R}^n$, prove that $v - w$ and $v + w$ are perpendicular if $\lVert v \rVert = \lVert w \rVert$.

## Q10 Invertible Products

**(a)** (5 pts) Let $A$ and $B$ be $n \times n$ matrices such that $AB$ is invertible. Prove that $A$ and $B$ are invertible.

**(b)** (5 pts) Let $A$, $B$, and $C$ be three $n \times n$ matrices. Prove that if $ABC$ is invertible, then $B$ is invertible.

## Q11 Inverse by Row Reduction

**(a)** (5 pts) Let $A$ be an $n \times n$ matrix with $A$ invertible. Prove that $X = A^{-1}$ can be found by the following row reduction:
$$
[A \mid I] \overset{r}{\sim} [I \mid X].
$$
That is, if $A$ is reduced to the identity matrix $I$, then the matrix $I$ will be reduced to $A^{-1}$.

**(b)** (5 pts) Find the inverse of the matrix:
$$
A = \begin{bmatrix} -1 & 2 & 1 \\ 2 & -3 & 5 \\ 1 & 0 & 12 \end{bmatrix}.
$$

## Q12 Inverse of a Block Lower Triangular Matrix

(5 pts) $A$ and $C$ are invertible, and $O$ is a zero matrix. Find $X^{-1}$ if
$$
X = \begin{bmatrix} A_{m \times m} & O \\ B_{n \times m} & C_{n \times n} \end{bmatrix}.
$$

## Q13 A System with a Parameter

(5 pts) Solve $k$ such that the system
$$
\left\{\begin{aligned} x_1 + kx_2 + 3x_3 &= 2, \\ x_1 + 2x_2 + 2x_3 &= 3, \\ x_1 + 3x_2 + kx_3 &= k + 3, \end{aligned}\right.
$$
has (a) no solution; (b) a unique solution; (c) infinitely many solutions.

## Q14 Trace of a Similar Matrix

(5 pts) Let $A$ and $B$ be $n \times n$ matrices. If there exists an invertible matrix $P$ such that $P^{-1}AP = B$, prove or disprove that $\operatorname{tr}(A) = \operatorname{tr}(B)$.

## Q15 Consistency of a System

(5 pts) Determine all values of $b_i$ that make the linear system
$$
\begin{cases} x_1 + 2x_2 = b_1, \\ 3x_1 + 6x_2 = b_2, \end{cases}
$$
consistent.
