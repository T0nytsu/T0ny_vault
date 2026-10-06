---
course: [LA1]
chapter: ["1.4", "1.5"]
tags: [linear-algebra, homework, questions, linear-systems, matrix-inverse]
source:
  - "FB §1.4 exercises pp. 68-71 and §1.5 exercises pp. 84-86, scanned PDF"
  - "Nicholson, Linear Algebra with Applications (open edition, CC BY-NC-SA), exercises of §1.2, §2.4, §2.5, from the LibreTexts edition"
created: 2026-10-05
solutions: "[[LA1 HW 1.4 1.5 Solutions]]"
---
> [!info] Coverage
> FB §1.4: 3, 5, 42, 44, 45, 49, 52, 53, 54, 55. FB §1.5: 23, 24, 25, 36, 37, 38. FB is Fraleigh & Beauregard, *Linear Algebra*.
>
> Additional exercises, not assigned: FB §1.4: 9, 16, 24, 25, 29, 40, 58. FB §1.5: 5, 13, 21, 22, 26, 30, 35. They are at the bottom of this note and cover types of problems that the assigned exercises leave out.
>
> Additional exercises from the Internet, not assigned: NIC §1.2: 8. NIC §2.4: 5, 21, 24, 28, 34. NIC §2.5: 9, 14. NIC is Nicholson, *Linear Algebra with Applications*, an open textbook on the same topics as FB §1.4 and §1.5. They are at the very bottom of this note.

## FB §1.4 Solving Systems of Linear Equations

### FB 1.4.3
In Exercises 1–6, reduce the matrix to (a) row-echelon form, and (b) CC. Answers to (a) are not unique, so your answer may differ from the one at the back of the text.
$$
\begin{bmatrix} 0 & 2 & -1 & 3 \\ -1 & 1 & 2 & 0 \\ 1 & 1 & -3 & 3 \\ 1 & 5 & 5 & 9 \end{bmatrix}
$$

### FB 1.4.5
In Exercises 1–6, reduce the matrix to (a) row-echelon form, and (b) reduced row-echelon form. Answers to (a) are not unique, so your answer may differ from the one at the back of the text.
$$
\begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 1 & -3 & 0 & 0 & -1 \\ 2 & -6 & 2 & 4 & 0 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix}
$$

### FB 1.4.42
Find an elementary matrix $E$ such that
$$
E\begin{bmatrix} 1 & 3 & 1 & 4 \\ 0 & 1 & 2 & 1 \\ 3 & 4 & 5 & 1 \end{bmatrix} = \begin{bmatrix} 1 & 3 & 1 & 4 \\ 0 & 1 & 2 & 1 \\ 0 & -5 & 2 & -11 \end{bmatrix}.
$$

### FB 1.4.44
Find a matrix $C$ such that
$$
C\begin{bmatrix} 1 & 2 \\ 3 & 4 \\ 4 & 2 \end{bmatrix} = \begin{bmatrix} 1 & 2 \\ 0 & -2 \\ 0 & -6 \end{bmatrix}.
$$

### FB 1.4.45
Find a matrix $C$ such that
$$
C\begin{bmatrix} 1 & 2 \\ 3 & 4 \\ 4 & 2 \end{bmatrix} = \begin{bmatrix} 3 & 4 \\ 4 & 2 \\ 1 & 2 \end{bmatrix}.
$$

### FB 1.4.49
In Exercises 46–51, let $A$ be a $4 \times 4$ matrix. Find a matrix $C$ such that the result of applying the given sequence of elementary row operations to $A$ can also be found by computing the product $CA$.

Add 4 times row 2 to row 4; multiply row 4 by $-3$; add 5 times row 4 to row 1.

### FB 1.4.52
Exercise 24 in Section 1.3 is useful for the next three exercises.

Prove Theorem 1.8 for the row-interchange operation.

> [!note] Note
> The page with Theorem 1.8 is not in the scan. Summary item 11 of §1.4 (p. 68) states it: "An elementary matrix $E$ is one obtained by applying a single elementary row operation to an identity matrix $I$. Multiplication of a matrix $A$ on the left by $E$ effects the same elementary row operation on $A$." Exercise 24 of §1.3 is [[LA1 HW 1.3 1.5 Questions#FB 1.3.24|FB 1.3.24]].

### FB 1.4.53
Prove Theorem 1.8 for the row-scaling operation.

### FB 1.4.54
Prove Theorem 1.8 for the row-addition operation.

### FB 1.4.55
Prove that row equivalence $\sim$ is an equivalence relation by verifying the following for $m \times n$ matrices $A$, $B$, and $C$.
- a. $A \sim A$. (Reflexive Property)
- b. If $A \sim B$, then $B \sim A$. (Symmetric Property)
- c. If $A \sim B$ and $B \sim C$, then $A \sim C$. (Transitive Property)

## FB §1.5 Inverses of Square Matrices

### FB 1.5.23
Mark each of the following True or False. The statements involve matrices $A$, $B$, and $C$, which are assumed to be of appropriate size.
- a. If $AC = BC$ and $C$ is invertible, then $A = B$.
- b. If $AB = O$ and $B$ is invertible, then $A = O$.
- c. If $AB = C$ and two of the matrices are invertible, then so is the third.
- d. If $AB = C$ and two of the matrices are singular, then so is the third.
- e. If $A^2$ is invertible, then $A^3$ is invertible.
- f. If $A^3$ is invertible, then $A^2$ is invertible.
- g. Every elementary matrix is invertible.
- h. Every invertible matrix is an elementary matrix.
- i. If $A$ and $B$ are invertible matrices, then so is $A + B$, and $(A + B)^{-1} = A^{-1} + B^{-1}$.
- j. If $A$ and $B$ are invertible, then so is $AB$, and $(AB)^{-1} = A^{-1}B^{-1}$.

### FB 1.5.24
Show that, if $A$ is an invertible $n \times n$ matrix, then $A^T$ is invertible. Describe $(A^T)^{-1}$ in terms of $A^{-1}$.

### FB 1.5.25
- a. If $A$ is invertible, is $A + A^T$ always invertible?
- b. If $A$ is invertible, is $A + A$ always invertible?

### FB 1.5.36
Exercises 36–38 develop elementary column operations.

For each type of elementary matrix $E$, explain how $E$ can be obtained from the identity matrix by means of operations on columns.

### FB 1.5.37
Let $A$ be a square matrix, and let $E$ be an elementary matrix of the same size. Find the effect on $A$ of multiplying $A$ on the right by $E$. [HINT: Use Exercise 36.]

### FB 1.5.38
Let $A$ be an invertible square matrix. Recall that $(BA)^{-1} = A^{-1}B^{-1}$, and use Exercise 37 to answer the following questions:
- a. If two rows of $A$ are interchanged, how does the inverse of the resulting matrix compare with $A^{-1}$?
- b. Answer the question in part (a) if, instead, a row of $A$ is multiplied by a nonzero scalar $r$.
- c. Answer the question in part (a) if, instead, $r$ times the $i$th row of $A$ is added to the $j$th row.

## FB §1.4 Additional Exercises

### FB 1.4.9
In Exercises 7–12, describe all solutions of a linear system whose corresponding augmented matrix can be row-reduced to the given matrix. If requested, also give the indicated particular solution, if it exists.
$$
\left[\begin{array}{cccc|c} 1 & 0 & 2 & 0 & 1 \\ 0 & 1 & 1 & 3 & -2 \\ 0 & 0 & 0 & 0 & 0 \end{array}\right],
$$
solution with $x_3 = 3$, $x_4 = -2$

### FB 1.4.16
In Exercises 13–20, find all solutions of the given linear system, using the Gauss method with back substitution.
$$
\begin{aligned}
2x + \phantom{3}y - 3z &= 0 \\
6x + 3y - 8z &= 0 \\
2x - \phantom{3}y + 5z &= -4
\end{aligned}
$$

### FB 1.4.24
In Exercises 21–24, find all solutions of the linear system, using the Gauss–Jordan method.
$$
\begin{aligned}
x_1 + 2x_2 - 3x_3 + \phantom{2}x_4 &= 2 \\
3x_1 + 6x_2 - 8x_3 - 2x_4 &= 1
\end{aligned}
$$

### FB 1.4.25
In Exercises 25–28, determine whether the vector $\mathbf{b}$ is in the span of the vectors $\mathbf{v}_i$.
$$
\mathbf{b} = \begin{bmatrix} 3 \\ 5 \\ 3 \end{bmatrix}, \quad \mathbf{v}_1 = \begin{bmatrix} 0 \\ 2 \\ 4 \end{bmatrix}, \quad \mathbf{v}_2 = \begin{bmatrix} 1 \\ 4 \\ -2 \end{bmatrix}, \quad \mathbf{v}_3 = \begin{bmatrix} -3 \\ -1 \\ 5 \end{bmatrix}
$$

### FB 1.4.29
Mark each of the following True or False.
- a. Every linear system with the same number of equations as unknowns has a unique solution.
- b. Every linear system with the same number of equations as unknowns has at least one solution.
- c. A linear system with more equations than unknowns may have an infinite number of solutions.
- d. A linear system with fewer equations than unknowns may have no solution.
- e. Every matrix is row equivalent to a unique matrix in row-echelon form.
- f. Every matrix is row equivalent to a unique matrix in reduced row-echelon form.
- g. If $[A \mid \mathbf{b}]$ and $[B \mid \mathbf{c}]$ are row-equivalent partitioned matrices, the linear systems $A\mathbf{x} = \mathbf{b}$ and $B\mathbf{x} = \mathbf{c}$ have the same solution set.
- h. A linear system with a square coefficient matrix $A$ has a unique solution if and only if $A$ is row equivalent to the identity matrix.
- i. A linear system with coefficient matrix $A$ has an infinite number of solutions if and only if $A$ can be row-reduced to an echelon matrix that includes some column containing no pivot.
- j. A consistent linear system with coefficient matrix $A$ has an infinite number of solutions if and only if $A$ can be row-reduced to an echelon matrix that includes some column containing no pivot.

### FB 1.4.40
Determine all values of the $b_i$ that make the linear system
$$
\begin{aligned}
x_1 + \phantom{2}x_2 - x_3 &= b_1 \\
2x_2 + x_3 &= b_2 \\
x_2 - x_3 &= b_3
\end{aligned}
$$
consistent.

### FB 1.4.58
Let $A$ be an $m \times n$ matrix, and let $\mathbf{c}$ be a column vector such that $A\mathbf{x} = \mathbf{c}$ has a unique solution.
- a. Prove that $m \ge n$.
- b. If $m = n$, must the system $A\mathbf{x} = \mathbf{b}$ be consistent for every choice of $\mathbf{b}$?
- c. Answer part (b) for the case where $m > n$.

## FB §1.5 Additional Exercises

### FB 1.5.5
In Exercises 1–8, (a) find the inverse of the square matrix, if it exists, and (b) express each invertible matrix as a product of elementary matrices.
$$
\begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & -1 \end{bmatrix}
$$

### FB 1.5.13
**a.** Show that the matrix
$$
A = \begin{bmatrix} 2 & -3 \\ 5 & -7 \end{bmatrix}
$$
is invertible, and find its inverse.

**b.** Use the result in (a) to find the solution of the system of equations
$$
2x_1 - 3x_2 = 4, \qquad 5x_1 - 7x_2 = -3.
$$

### FB 1.5.21
Find all numbers $r$ such that
$$
\begin{bmatrix} 2 & 4 & 2 \\ 1 & r & 3 \\ 1 & 1 & 2 \end{bmatrix}
$$
is invertible.

### FB 1.5.22
Let $A$ and $B$ be two $m \times n$ matrices. Show that $A$ and $B$ are row equivalent if and only if there exists an invertible $m \times m$ matrix $C$ such that $CA = B$.

### FB 1.5.26
Let $A$ be a matrix such that $A^2$ is invertible. Prove that $A$ is invertible.

### FB 1.5.30
A square matrix $A$ is said to be **idempotent** if $A^2 = A$.
- a. Give an example of an idempotent matrix other than $O$ and $I$.
- b. Show that, if a matrix $A$ is both idempotent and invertible, then $A = I$.

### FB 1.5.35
Consider the $2 \times 2$ matrix
$$
A = \begin{bmatrix} a & b \\ c & d \end{bmatrix},
$$
and let $h = ad - bc$.

**a.** Show that, if $h \ne 0$, then
$$
\begin{bmatrix} d/h & -b/h \\ -c/h & a/h \end{bmatrix}
$$
is the inverse of $A$.

**b.** Show that $A$ is invertible if and only if $h \ne 0$.

## NIC §1.2 Gaussian Elimination

> [!note] Note
> The exercises under the NIC headings are from W. Keith Nicholson, *Linear Algebra with Applications* (open edition, CC BY-NC-SA 4.0), read from the LibreTexts edition. The statements were read from the web page and may differ from the book in a word or two; only the listed parts of each exercise are kept. NIC §1.2 covers the topics of FB §1.4, and NIC §2.4 and §2.5 those of FB §1.5.

### NIC 1.2.8
In each of the following, find (if possible) conditions on $a$ and $b$ such that the system has no solution, one solution, and infinitely many solutions.

Second system:
$$
\begin{aligned}
x + by &= -1 \\
ax + 2y &= 5
\end{aligned}
$$

## NIC §2.4 Matrix Inverses

> [!note] Notation
> Nicholson writes the zero matrix as $0$, where FB writes $O$.

### NIC 2.4.5
Find $A$ when:
- (1) $(3A)^{-1} = \begin{bmatrix} 1 & -1 \\ 0 & 1 \end{bmatrix}$
- (3) $(I + 3A)^{-1} = \begin{bmatrix} 2 & 0 \\ 1 & -1 \end{bmatrix}$

### NIC 2.4.21
Suppose $AB = 0$, where $A$ and $B$ are square matrices. Show that:
- (1) If one of $A$ and $B$ has an inverse, the other is zero.
- (2) It is impossible for both $A$ and $B$ to have inverses.
- (3) $(BA)^2 = 0$.

### NIC 2.4.24
Assume that a square matrix $A$ satisfies $A^3 - 3A + 2I = 0$. Show that $A$ is invertible, and find $A^{-1}$ in terms of $A$.

### NIC 2.4.28
Let $A$ denote an $n \times n$ matrix and let $I$ denote the $n \times n$ identity matrix.
- (1) If $A^2 = 0$, verify that $(I - A)^{-1} = I + A$.
- (2) If $A^3 = 0$, verify that $(I - A)^{-1} = I + A + A^2$.
- (3) Find the inverse of $\begin{bmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \\ 0 & 0 & 1 \end{bmatrix}$.

### NIC 2.4.34
Let $A$ and $B$ denote $n \times n$ matrices such that $AB$ is invertible. Show that both $A$ and $B$ are invertible.

## NIC §2.5 Elementary Matrices

### NIC 2.5.9
Let $E$ be an elementary matrix.
- (1) Show that $E^T$ is also elementary of the same type.
- (2) Show that $E^T = E$ if $E$ is of type I or II.

> [!note] Note
> Nicholson's types: type I interchanges two rows, type II multiplies a row by a nonzero number, and type III adds a multiple of one row to another row.

### NIC 2.5.14
While trying to invert $A$, $[A \mid I]$ is carried to $[P \mid Q]$ by row operations. Show that $P = QA$.
