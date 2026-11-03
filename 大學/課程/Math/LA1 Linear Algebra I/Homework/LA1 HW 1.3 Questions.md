---
course: [LA1]
semester: "115-1"
chapter: ["1.3"]
tags: [linear-algebra, homework, questions, matrix-algebra]
source:
  - "FB §1.3 exercises pp. 46-48, photos"
  - "WEB 1.3.1: OSU linear algebra exam, true or false problems 1, 3, 6, 10 (yutsumura.com, Problem 104)"
  - "WEB 1.3.2: OSU linear algebra quiz problem (yutsumura.com, Problem 111)"
  - "WEB 1.3.3: PCCU 99 transfer entrance exam, Applied Mathematics (third year), Linear Algebra, Item 8 (PCCU library)"
  - "WEB 1.3.4: Columbia University, Linear Algebra, Summer 2022, Mock Linear Algebra Midterm, Problem 6 (math.columbia.edu)"
  - "WEB 1.3.5: Problems in Mathematics, Problem 19 (yutsumura.com)"
created: 2026-11-02
solutions: "[[LA1 HW 1.3 Solutions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> FB §1.3: 13, 15, 17, 19, 21, 26, 28, 30, 31, 32, 42, 43. These are the exercises assigned for Section 1.3. FB is Fraleigh & Beauregard, *Linear Algebra*.
>
> [[LA1 HW 1.3 1.5 Questions]] has the other §1.3 exercises done so far: 20, 22, 24, 37, 40, 41, 44. Its Exercise 40 uses Exercise 32 of this note.
>
> Additional problems, not assigned: WEB 1.3.1–1.3.5, found on the web: four from linear algebra exams and quizzes of other universities and one from the problem site *Problems in Mathematics*. They are at the bottom of this note; the line under each heading names the source.

## FB §1.3 Matrices and Their Algebra

### FB 1.3.13
In Exercises 1–16, let
$$
A = \begin{bmatrix} -2 & 1 & 3 \\ 4 & 0 & -1 \end{bmatrix}, \quad B = \begin{bmatrix} 4 & 1 & -2 \\ 5 & -1 & 3 \end{bmatrix}, \quad C = \begin{bmatrix} 2 & -1 \\ 0 & 6 \\ -3 & 2 \end{bmatrix}, \quad \text{and} \quad D = \begin{bmatrix} -4 & 2 \\ 3 & 5 \\ -1 & -3 \end{bmatrix}.
$$
Compute the indicated quantity, if it is defined.

$(2A - B)D$

### FB 1.3.15
In Exercises 1–16, let
$$
A = \begin{bmatrix} -2 & 1 & 3 \\ 4 & 0 & -1 \end{bmatrix}, \quad B = \begin{bmatrix} 4 & 1 & -2 \\ 5 & -1 & 3 \end{bmatrix}, \quad C = \begin{bmatrix} 2 & -1 \\ 0 & 6 \\ -3 & 2 \end{bmatrix}, \quad \text{and} \quad D = \begin{bmatrix} -4 & 2 \\ 3 & 5 \\ -1 & -3 \end{bmatrix}.
$$
Compute the indicated quantity, if it is defined.

$(A^T)A$

### FB 1.3.17
Let
$$
A = \begin{bmatrix} 2 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 1 \end{bmatrix}.
$$
- a. Find $A^2$.
- b. Find $A^7$.

### FB 1.3.19
Consider the row and column vectors
$$
\mathbf{x} = [-2, 3, -1] \quad \text{and} \quad \mathbf{y} = \begin{bmatrix} 4 \\ -1 \\ 3 \end{bmatrix}.
$$
Compute the matrix products $\mathbf{x}\mathbf{y}$ and $\mathbf{y}\mathbf{x}$.

### FB 1.3.21
Mark each of the following True or False. The statements involve matrices $A$, $B$, and $C$ that are assumed to have appropriate size.
- a. If $A = B$, then $AC = BC$.
- b. If $AC = BC$, then $A = B$.
- c. If $AB = O$, then $A = O$ or $B = O$.
- d. If $A + C = B + C$, then $A = B$.
- e. If $A^2 = I$, then $A = \pm I$.
- f. If $B = A^2$ and if $A$ is $n \times n$ and symmetric, then $b_{ii} \ge 0$ for $i = 1, 2, \ldots, n$.
- g. If $AB = C$ and if two of the matrices are square, then so is the third.
- h. If $AB = C$ and if $C$ is a column vector, then so is $B$.
- i. If $A^2 = I$, then $A^n = I$ for all integers $n \ge 2$.
- j. If $A^2 = I$, then $A^n = I$ for all even integers $n \ge 2$.

### FB 1.3.26
In Exercises 25–34, prove that the given relation holds for all vectors, matrices, and scalars for which the expressions are defined.

$(A + B) + C = A + (B + C)$

### FB 1.3.28
In Exercises 25–34, prove that the given relation holds for all vectors, matrices, and scalars for which the expressions are defined.

$(rs)A = r(sA)$

### FB 1.3.30
In Exercises 25–34, prove that the given relation holds for all vectors, matrices, and scalars for which the expressions are defined.

$(A^T)^T = A$

### FB 1.3.31
In Exercises 25–34, prove that the given relation holds for all vectors, matrices, and scalars for which the expressions are defined.

$(A + B)^T = A^T + B^T$

### FB 1.3.32
In Exercises 25–34, prove that the given relation holds for all vectors, matrices, and scalars for which the expressions are defined.

$(AB)^T = B^TA^T$

### FB 1.3.42
Let $A$ and $B$ be square matrices. Is
$$
(A + B)^2 = A^2 + 2AB + B^2?
$$
If so, prove it; if not, give a counterexample and state under what conditions the equation is true.

### FB 1.3.43
Let $A$ and $B$ be square matrices. Is
$$
(A + B)(A - B) = A^2 - B^2?
$$
If so, prove it; if not, give a counterexample and state under what conditions the equation is true.

## Additional Problems from the Web

> [!note] Notation
> $O$ is the zero matrix. $\operatorname{tr}(A)$ is the [[Trace|trace]] of a square matrix $A$, the sum of its diagonal entries. $\mathbb{N}$ is the set of positive integers.

### WEB 1.3.1
OSU (The Ohio State University), linear algebra exam, as posted on *Problems in Mathematics* (yutsumura.com), Problem 104. Problems 1, 3, 6 and 10 of the ten; the other six are close to Exercises 21, 42 and 43 or are about linear transformations.

Determine whether each of the following sentences is True or False.
- Problem 1. Suppose that $A$ is an $m \times n$ matrix and $B$ is an $n \times m$ matrix. Then $(AB)^T = A^TB^T$.
- Problem 3. Let $A$ and $B$ be $n \times n$ matrices. If $A$ and $B$ commute, then matrices $A^2$ and $B$ must commute.
- Problem 6. There are $n \times n$ matrices $A$ and $B$ such that $AB = O$ but $BA \ne O$.
- Problem 10. If $A$ and $B$ are symmetric $n \times n$ matrices, then the product $AB$ is also symmetric.

### WEB 1.3.2
OSU (The Ohio State University), Introduction to Linear Algebra, quiz problem, as posted on *Problems in Mathematics* (yutsumura.com), Problem 111.

Let $A$ and $B$ be $n \times n$ real symmetric matrices. Prove the following.
- (a) The product $AB$ is symmetric if and only if $AB = BA$.
- (b) If the product $AB$ is a diagonal matrix, then $AB = BA$.

### WEB 1.3.3
PCCU (Chinese Culture University), 99 transfer entrance exam, Department of Applied Mathematics (third year), Linear Algebra, Item 8. Read from the text layer of the scanned paper.

Let $A$ and $B$ be symmetric. Prove $ABA$ is also symmetric.

### WEB 1.3.4
Columbia University, Linear Algebra, Summer 2022, Mock Linear Algebra Midterm, Problem 6, from the instructor's course page (math.columbia.edu).

(Extra: 10 points) A $3 \times 3$ matrix is diagonal if it is of the form
$$
\begin{bmatrix} a & 0 & 0 \\ 0 & b & 0 \\ 0 & 0 & c \end{bmatrix}
$$
for some $a, b, c \in \mathbb{R}$. Prove that if a diagonal matrix $D$ commutes with every other $3 \times 3$ matrix, then $D$ is of the form
$$
\begin{bmatrix} a & 0 & 0 \\ 0 & a & 0 \\ 0 & 0 & a \end{bmatrix}
$$
In other words, $D$ must be a multiple of the identity matrix.

### WEB 1.3.5
*Problems in Mathematics* (yutsumura.com), Problem 19, "Questions about the trace of a matrix". Not from an exam.

Let $A = (a_{ij})$ and $B = (b_{ij})$ be $n \times n$ real matrices for some $n \in \mathbb{N}$. Then answer the following questions about the trace of a matrix.
- (a) Express $\operatorname{tr}(AB^T)$ in terms of the entries of the matrices $A$ and $B$.
- (b) Show that $\operatorname{tr}(AA^T)$ is the sum of the squares of the entries of $A$.
- (c) Show that if $A$ is a nonzero symmetric matrix, then $\operatorname{tr}(A^2) > 0$.
