---
course: [LA1]
semester: "115-1"
chapter: ["1.1", "1.2", "1.3", "1.4", "1.5", "10.2"]
tags: [linear-algebra, exam, questions, matrix-algebra, matrix-inverse, linear-systems]
source:
  - "114-1, Linear Algebra I – Midterm, printed paper with a student's graded answers, scan (PDF, 16 pages)"
created: 2026-11-02
solutions: "[[LA1 Midterm 114-1 Solutions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> A past midterm of this course: Linear Algebra I, semester 114-1, 14 questions, 100 points. It covers FB §1.1–1.5 and §10.2: the [[Norm|norm]], [[Unit Vector|unit vectors]] and the [[Dot Product|dot product]], [[Span|span]], the [[Transpose|transpose]] and [[Skew-Symmetric Matrix|skew-symmetric matrices]], [[Reduced Row-Echelon Form|reduced row-echelon form]], [[Row Equivalence|row equivalence]], [[Gaussian Elimination|Gaussian elimination]], the [[LU-Factorization|LU-factorization]], [[Invertible Matrix|inverses]] and [[Idempotent Matrix|idempotent matrices]].
>
> Write it as a timed paper, then check with [[LA1 Midterm 114-1 Solutions]].

> [!note] Notation
> The paper writes the transpose as $A^{\top}$ (and $A^T$ in Q10). Vectors and $m \times 1$ matrices are not bold ($u$, $v$, $w$, $b$, $c$, $x$), and $[A \mid b] \overset{r}{\sim} [B \mid c]$ means that the two augmented matrices are row equivalent. $O$ is a zero matrix.

## Q1 True or False

(10 pts) Make each of the following True or False.
- (a) $AB = BA$.
- (b) The dot product of a vector with itself yields the magnitude of the vector.
- (c) If $A$ is invertible, then $AA^{\top}$ is invertible.
- (d) If $A^2$ is invertible, then $A$, $A^{\top}$, and $A^3$ are invertible.
- (e) If $A$ and $B$ are invertible, then so is $A + B$, and $(A + B)^{-1} = A^{-1} + B^{-1}$.
- (f) If $A$ is invertible, then so is $A + A^{\top}$.
- (g) If $A^2 = O$, then $A$ is singular.
- (h) For vectors $v$ and $w$ in $\mathbb{R}^n$, $v - w$ and $v + w$ are perpendicular if and only if $\lVert v \rVert = \lVert w \rVert$.
- (i) A linear system with fewer equations than unknowns may have no solution.
- (j) A linear system with coefficient matrix $A$ has an infinite number of solutions if and only if $A$ can be row-reduced to an echelon matrix that includes some column containing no pivot.

## Q2 Reduced Row-Echelon Form

(6 pts) Reduce the matrix below to its reduced row-echelon form. (Make sure each pivot is 1.)
$$
\begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 1 & -3 & 0 & 0 & -1 \\ 2 & -6 & 2 & 4 & 0 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix}.
$$

## Q3 Span of Two Vectors

(6 pts) Determine whether the vector $b = [1, -1, -4]^{\top}$ is in the span of the vectors $v = [3, 1, 1]^{\top}$ and $w = [1, 3, 2]^{\top}$.

## Q4 Norm, Unit Vector and Dot Product

(2+2+2 pts) Let $u = [-1, 3, 4]$, $v = [1, 1, -1]$, and $w = [-2, -1, 3]$. Find the indicated quantity.
- (a) $\lVert u + v \rVert$.
- (b) The unit vector parallel to $u$, having the same direction.
- (c) $(u + v) \cdot w$

## Q5 LU Factorization and Solving

(4+2 pts) Let $A = \begin{bmatrix} 1 & -4 & 2 \\ 0 & 2 & -1 \\ 3 & -8 & 2 \end{bmatrix}$, $b = \begin{bmatrix} -3 \\ 2 \\ 3 \end{bmatrix}$. Find an $LU$ factorization of $A$, then solve the linear system $Ax = b$ using the factorization together with forward and back substitutions.

## Q6 A System with a Parameter

(2+2+2 pts) Solve $k$ such that the following system
$$
\left\{\begin{aligned} x_1 - 2x_2 + 3x_3 &= 1 \\ 2x_1 + kx_2 + 6x_3 &= 6 \\ -x_1 + 3x_2 + (k - 3)x_3 &= 0 \end{aligned}\right.
$$
has (a) no solution; (b) a unique solution; (c) infinitely many solutions.

## Q7 Matrix from the General Solution

(6 pts) If $b = \begin{bmatrix} 1 \\ 3 \\ 0 \\ 2 \end{bmatrix}$ and the general solution to $Ax = b$ is $x = \begin{bmatrix} 1 \\ 1 \\ -1 \end{bmatrix} + \alpha\begin{bmatrix} 1 \\ 2 \\ 0 \end{bmatrix} + \beta\begin{bmatrix} 2 \\ 2 \\ -1 \end{bmatrix}$, where $\alpha$ and $\beta$ are free parameters, determine the matrix $A$.

## Q8 Inverse of I plus B

(6 pts) $A = \begin{bmatrix} 1 & 0 & 0 & 0 \\ 2 & 3 & 0 & 0 \\ 0 & -4 & 5 & 0 \\ 0 & 0 & -6 & 7 \end{bmatrix}$, $B = (I + A)^{-1}(I - A)$. Find $(I + B)^{-1}$.

## Q9 Inverse by Row Reduction

**(a)** (6 pts) Let $A$ be an $n \times n$ matrix with $A$ invertible. Prove that $X = A^{-1}$ can be found by the following row reduction:
$$
[A \mid I] \overset{r}{\sim} [I \mid X].
$$
That is, if $A$ is reduced to the identity matrix $I$, then the matrix $I$ will be reduced to $A^{-1}$.

**(b)** (6 pts) Find the inverse of the matrix:
$$
A = \begin{bmatrix} 2 & 1 & 4 \\ 3 & 2 & 5 \\ 0 & -1 & 1 \end{bmatrix}.
$$

## Q10 A Minus Its Transpose Is Skew-Symmetric

(6 pts) Prove that, if $A$ is a square matrix, then the matrix $A - A^T$ is skew symmetric.

## Q11 Row Equivalence and Gaussian Elimination

$A$ and $B$ are $m \times n$ matrices. $b$ and $c$ are $m \times 1$ matrices.

**(1)** (5 pts) Prove that if $[A \mid b] \overset{r}{\sim} [B \mid c]$, then $Ax = b$ and $Bx = c$ have the same solution set.

**(2)** (5 pts) Use Gaussian method with back substitution to solve
$$
\begin{cases} 2x_1 + x_2 - 3x_3 = 0 \\ 6x_1 + 3x_2 - 8x_3 = 0 \\ 2x_1 - x_2 + 5x_3 = -4 \end{cases}.
$$

## Q12 A Commutator Equal to A

(5 pts) Let $A$ and $B$ be $n \times n$ matrices. If $AB - BA = A$, show that $A$ is singular.

## Q13 Left Inverse and an Inverse Formula

**(a)** (5 pts) $A$ is an $n \times n$ matrix. Prove that if $A$ has a left inverse $B$, then $A$ is invertible and $A^{-1} = B$.

**(b)** (5 pts) Let $A$ and $B$ be invertible matrices such that $A + B$ is invertible. Show that $(A^{-1} + B^{-1})^{-1} = B(A + B)^{-1}A$.

## Q14 Idempotent Matrix

(5 pts) An $n \times n$ matrix $A$ is called idempotent if $A^2 = A$. If $A$ is idempotent, find the inverse of $I - cA$ (if possible) for some scalar $c \ne 1$.
