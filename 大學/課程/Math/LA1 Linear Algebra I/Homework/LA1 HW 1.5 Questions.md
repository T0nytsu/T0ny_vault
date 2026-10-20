---
course: [LA1]
semester: "115-1"
chapter: ["1.5"]
tags: [linear-algebra, homework, questions, matrix-inverse, linear-systems]
source:
  - "FB §1.5 exercises pp. 84-86, scanned PDF"
  - "WEB 1.5.1: NCCU 110 master's entrance exam, Applied Mathematics, Linear Algebra, Problem 4 (yamol.tw)"
  - "WEB 1.5.2: NTHU 109 master's entrance exam, Mathematics, Linear Algebra (0102), Problem 4 (NTHU Library exam archive)"
  - "WEB 1.5.3: NCUE 98 doctoral entrance exam, Mathematics, Linear Algebra, Problem 2 (NCUE library)"
  - "WEB 1.5.4: PCCU 100 transfer entrance exam, Applied Mathematics (third year), Linear Algebra, Item 11 (PCCU library)"
  - "WEB 1.5.5: OSU linear algebra Midterm Exam 1, Spring 2018, true or false problems (yutsumura.com)"
created: 2026-10-19
solutions: "[[LA1 HW 1.5 Solutions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> FB §1.5: 11, 12, 13, 21, 22, 27, 29. These are the exercises assigned for Section 1.5. FB is Fraleigh & Beauregard, *Linear Algebra*.
>
> Exercises 13, 21 and 22 are also in [[LA1 HW 1.4 1.5 Questions]], with the same solutions. That note and [[LA1 HW 1.3 1.5 Questions]] have the other §1.5 exercises done so far: 5, 9, 16–19, 23–26, 30, 33, 35–38.
>
> Additional exercises, not assigned: WEB 1.5.1–1.5.5, five problems from linear algebra exams of other universities, found on the web. They are at the bottom of this note; the line under each heading names the exam.

## FB §1.5 Inverses of Square Matrices

### FB 1.5.11
In Exercises 11 and 12, determine whether the span of the column vectors of the given matrix is $\mathbb{R}^4$.
$$
\begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 1 & 0 & -1 & 2 \\ -3 & 0 & 0 & -1 \end{bmatrix}
$$

### FB 1.5.12
In Exercises 11 and 12, determine whether the span of the column vectors of the given matrix is $\mathbb{R}^4$.
$$
\begin{bmatrix} 1 & -2 & 1 & 0 \\ -3 & 5 & 0 & 2 \\ 0 & 1 & 2 & -4 \\ -1 & 2 & 4 & -2 \end{bmatrix}
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

### FB 1.5.27
Let $A$ and $B$ be $n \times n$ matrices with $A$ invertible.

**a.** Show that $AX = B$ has the unique solution $X = A^{-1}B$.

**b.** Show that $X = A^{-1}B$ can be found by the following row reduction:
$$
[A \mid B] \sim [I \mid X].
$$
That is, if the matrix $A$ is reduced to the identity matrix $I$, then the matrix $B$ will be reduced to $A^{-1}B$.

### FB 1.5.29
An $n \times n$ matrix $A$ is **nilpotent** if $A^r = O$ (the $n \times n$ zero matrix) for some positive integer $r$.
- a. Give an example of a nonzero nilpotent $2 \times 2$ matrix.
- b. Show that, if $A$ is an invertible $n \times n$ matrix, then $A$ is not nilpotent.

## Exam Problems from Other Universities

> [!note] Notation
> $\mathbb{F}$ and $F$ denote a field; in this course the field is $\mathbb{R}$. $M_{n \times n}(\mathbb{F})$ and $M_n(F)$ are the $n \times n$ matrices with entries in the field, and $\mathbb{F}^n$ holds the columns with $n$ entries. *Nonsingular* means invertible.

### WEB 1.5.1
NCCU (National Chengchi University), 110 master's entrance exam, Department of Applied Mathematics, Linear Algebra, Problem 4.

(20%) Prove that every invertible matrix is a product of elementary matrices.

### WEB 1.5.2
NTHU (National Tsing Hua University), 109 master's entrance exam, Department of Mathematics, Linear Algebra (0102), Problem 4. Read from the text layer of the scanned paper.

(10%) Prove the following theorem: For $A \in M_{n \times n}(\mathbb{F})$, $b \in \mathbb{F}^n$, if the system $AX = b$ has exactly one solution, then $A$ is invertible.

### WEB 1.5.3
NCUE (National Changhua University of Education), 98 doctoral entrance exam, Department of Mathematics, Linear Algebra, Problem 2. Read from the text layer of the scanned paper.

(15%) Let $A$ be an $n \times n$ matrix over a field $F$, that is, $A \in M_n(F)$. Prove that $A$ is invertible if and only if $AB = I$ for some $B \in M_n(F)$, where $I$ is the identity matrix.

### WEB 1.5.4
PCCU (Chinese Culture University), 100 transfer entrance exam, Department of Applied Mathematics (third year), Linear Algebra, Item 11.

Prove that if $A$ is not invertible, then $AB$ is not invertible.

### WEB 1.5.5
OSU (The Ohio State University), linear algebra, Midterm Exam 1, Spring 2018, as posted on *Problems in Mathematics* (yutsumura.com).

The following problems are True or False.

Let $A$ and $B$ be $n \times n$ matrices.
- (a) If $AB = B$, then $B$ is the identity matrix.
- (b) If the coefficient matrix $A$ of the system $A\mathbf{x} = \mathbf{b}$ is invertible, then the system has infinitely many solutions.
- (c) If $A$ is invertible, then $ABA^{-1} = B$.
- (d) If $A$ is an idempotent nonsingular matrix, then $A$ must be the identity matrix.
- (e) If $x_1 = 0, x_2 = 0, x_3 = 1$ is a solution to a homogeneous system of linear equation, then the system has infinitely many solutions.
