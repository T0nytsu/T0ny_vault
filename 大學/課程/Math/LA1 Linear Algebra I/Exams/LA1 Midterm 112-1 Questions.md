---
course: [LA1]
semester: "115-1"
chapter: ["1.3", "1.4", "1.5", "4.1", "10.2"]
tags: [linear-algebra, exam, questions, matrix-algebra, matrix-inverse, linear-systems, needs-review]
source:
  - "LA1 midterm 112-1: question crops pasted into a student's handwritten solution notes (PDF, 11 pages)"
created: 2026-11-02
solutions: "[[LA1 Midterm 112-1 Solutions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> A past midterm of this course: Linear Algebra I, semester 112-1, 16 questions. It covers FB §1.3–1.5, §4.1 and §10.2: the [[Transpose|transpose]], the [[Trace|trace]], [[Symmetric Matrix|symmetric]] and [[Skew-Symmetric Matrix|skew-symmetric]] matrices, [[Triangular Matrix|triangular matrices]], [[Invertible Matrix|inverses]], [[Rank|rank]] and [[Span|span]], [[Row Equivalence|row equivalence]], [[Gaussian Elimination|Gaussian elimination]], the [[LU-Factorization|LU-factorization]], [[Block Matrix|block matrices]], [[Determinant|determinants]] and [[Nilpotent Matrix|nilpotent matrices]].
>
> The source is not the original paper: each question is a photo crop in a student's solution notes. The points of Q1 and Q4–Q7 are not visible; the other questions add up to 82 points.
>
> Write it as a timed paper, then check with [[LA1 Midterm 112-1 Solutions]].

> [!note] Notation
> The paper writes the transpose as $A^{\top}$ (and $A^T$ in Q10). Vectors and $m \times 1$ matrices are not bold ($b$, $c$, $x$), and $[A \mid b] \overset{r}{\sim} [B \mid c]$ means that the two augmented matrices are row equivalent. $O$ is a zero matrix.

## Q1 True or False

True or False.
- (a) $\operatorname{tr}(AB) = \operatorname{tr}(BA)$.
- (b) If $A^2 = I$, then $A^n = I$ for all even integers $n \ge 2$.
- (c) If $A$ is invertible and skew-symmetric, then $A^{-1}$ is skew-symmetric.
- (d) If $A^2$ is invertible, then $A$, $A^{\top}$, and $A^3$ are invertible.
- (e) If $A$ and $B$ are invertible, then so is $A + B$, and $(A + B)^{-1} = A^{-1} + B^{-1}$.
- (f) If $A$ and $B$ are invertible, then so is $AB$, and $(AB)^{-1} = A^{-1}B^{-1}$.
- (g) A linear system with coefficient matrix $A$ has an infinite number of solutions if and only if $A$ can be row-reduced to an echelon matrix that includes some column containing no pivot.
- (h) A triangular matrix is invertible if and only if no diagonal entries are zero.
- (i) A linear system with fewer equations than unknowns may have no solution.

## Q2 Skew-Symmetric Entries

(3 pts) Find $a$ to $f$ so that the matrix $A$ is skew-symmetric.
$$
A = \begin{bmatrix} 1 & -1 & a & 0 \\ b & 4 & c & 8 \\ 2 & -7 & -1 & d \\ e & f & 6 & 3 \end{bmatrix}.
$$

## Q3 Rank and Span

(3+1 pts) Find the rank of $A$ and determine whether the span of the column vectors of $A$ is $\mathbb{R}^4$.
$$
A = \begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 1 & 0 & -1 & 2 \\ -3 & 0 & 0 & -1 \end{bmatrix}.
$$

## Q4 Product of Lower Triangular Matrices

==(?)== $A$ and $B$ are lower triangular $n \times n$ matrices. Prove that $AB$ is a lower triangular matrix.

## Q5 Odd Power of a Skew-Symmetric Matrix

==(?)== $A$ is skew-symmetric. Prove that $A^5$ is also skew-symmetric.

## Q6 Transpose of an Invertible Matrix

==(?)== $A$ is invertible. Prove that $A^{\top}$ is invertible.

## Q7 Diagonal of the Square of a Symmetric Matrix

==(?)== Prove that if $B = A^2$ and if $A$ is $n \times n$ and symmetric, then $b_{ii} \ge 0$ for $i = 1, \cdots, n$.

## Q8 Row Equivalence, Gaussian Elimination and LU

$A$ and $B$ are $m \times n$ matrices. $b$ and $c$ are $m \times 1$ matrices.

**(a)** (6 pts) Prove that if $[A \mid b] \overset{r}{\sim} [B \mid c]$, then $Ax = b$ and $Bx = c$ have the same solution set.

**(b)** (6 pts) Use Gaussian method with back substitution to solve
$$
\begin{cases} 2x_1 + x_2 = 1 \\ x_2 - x_3 = 2 \\ -2x_1 + x_2 + x_3 = -2 \end{cases}
$$

**(c)** (3 pts) Find an $LU$-factorization of
$$
A = \begin{bmatrix} 2 & 1 & 0 \\ 0 & 1 & -1 \\ -2 & 1 & 1 \end{bmatrix}
$$

## Q9 Area of a Triangle

(6 pts) Find the area of the triangle in $\mathbb{R}^2$ bounded by the line $y = x$, $y = -3x + 8$, and $3y + 5x = 0$.

## Q10 When the Transpose Times A Is Zero

(6 pts) Prove that if $A$ is an $m \times n$ matrix over $\mathbb{R}$ such that $A^T A = O$, then $A = O$.

## Q11 Left Inverse and an Inverse Formula

**(a)** (3 pts) $A$ is an $n \times n$ matrix. Prove that if $A$ has a left inverse $B$, then $A$ is invertible and $A^{-1} = B$.

**(b)** (6 pts) Use (a) to show that $(A + BCD)^{-1} = A^{-1} - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}$.

## Q12 Inverse and a Matrix Equation

(6+3 pts) Let $A = \begin{bmatrix} 5 & -3 & -1 \\ 4 & -2 & -1 \\ -12 & 7 & 3 \end{bmatrix}$. Find (a) $A^{-1}$ and (b) a matrix $C$ such that $ACA = \begin{bmatrix} 2 & 1 & 3 \\ -1 & 2 & 2 \\ 2 & 1 & 4 \end{bmatrix}$.

## Q13 Inverse of a Block Upper Triangular Matrix

(6 pts) $A$ and $C$ are invertible. Find $X^{-1}$ if
$$
X = \begin{bmatrix} A_{m \times m} & B_{m \times n} \\ O & C_{n \times n} \end{bmatrix}
$$

## Q14 A System with a Parameter

(2+2+2 pts) Solve $k$ such that the following system
$$
\left\{\begin{aligned} x_1 - 2x_2 + 3x_3 &= 1 \\ 2x_1 + kx_2 + 6x_3 &= 6 \\ -x_1 + 3x_2 + (k - 3)x_3 &= 0 \end{aligned}\right.
$$
has (a) no solution; (b) a unique solution; (c) infinitely many solutions.

## Q15 Determinant and Trace

(3+3 pts) Find (a) the determinant and (b) the trace of
$$
A = \begin{bmatrix} 2 & -1 & 1 \\ -1 & 0 & 3 \\ 2 & 1 & -4 \end{bmatrix}.
$$

## Q16 Nilpotent Matrices

**(a)** (3 pts) An $n \times n$ matrix $A$ is nilpotent if $A^k = O$ for some positive integer $k$. Give an example of a nonzero nilpotent $2 \times 2$ matrix.

**(b)** (3 pts) Prove that, if $A$ is an invertible $n \times n$ matrix, then $A$ is not nilpotent.

**(c)** (6 pts) Let $N$ be an $n \times n$ matrix such that $N^k = O$ for some integer $k$. Prove that $I + N$ is invertible and find its inverse.

> [!todo] Transcription check
> - The semester 112-1 is read from the file name of the source (2023). The source pastes each question as a photo crop into handwritten solution notes; the original paper is not in it.
> - Q1: the instruction line and the points are not in the crops. Statement (a) has no crop at all; it is read from the handwritten answer, which writes only $\operatorname{tr}(AB) = \operatorname{tr}(BA)$ and assumes $A$, $B$ are $n \times n$.
> - Q4–Q7: the crops start after the points, so the points are missing; the question numbers come from the handwritten labels.
> - Q8: the photo is blurred; the system in (b) and the matrix in (c) agree with the handwritten work.
