---
course: [LA1]
semester: "115-1"
chapter: ["4.1", "10.2"]
tags: [linear-algebra, homework, questions, determinants, vectors, linear-systems]
source:
  - "FB §4.1 exercises pp. 248-249 and §10.2 exercises pp. 524-525, scanned PDFs"
  - "WEB 4.1.1 and 4.1.2: Harvard Math 21a, Summer 2007, First Midterm (O. Knill), Problems 1 and 8, with posted solutions (people.math.harvard.edu)"
  - "WEB 4.1.3: Harvard Math 21a, Fall 2012, First Hourly, Problem 1, with posted solutions (people.math.harvard.edu)"
  - "WEB 10.2.1: MIT 18.06, Fall 2003, Quiz 1, Problem 1 (exam archive of G. Strang's Introduction to Linear Algebra, math.mit.edu)"
  - "WEB 10.2.2: MIT 18.06, Fall 2004, Quiz 1, Problem 1 (same archive)"
  - "WEB 10.2.3: UC Davis MAT 167, Fall 2008, Midterm Exam (B. Temple), Problem 1 (h) and (j) (math.ucdavis.edu)"
created: 2026-10-26
solutions: "[[LA1 HW 4.1 10.2 Solutions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> FB §4.1: 6, 12, 13, 21, 23, 25. FB §10.2: 4, 5, 6, 7. These are the exercises assigned for Sections 4.1 and 10.2. FB is Fraleigh & Beauregard, *Linear Algebra*.
>
> Additional exercises, not assigned: WEB 4.1.1–4.1.3 and WEB 10.2.1–10.2.3, six problems from exams of other universities, found on the web. They are at the bottom of this note; the line under each heading names the exam.

## FB §4.1 Areas, Volumes, and Cross Products

### FB 4.1.6
In Exercises 6–9, find the indicated determinant.
$$
\begin{vmatrix} 1 & 4 & -2 \\ 5 & 13 & 0 \\ 2 & -1 & 3 \end{vmatrix}
$$

### FB 4.1.12
Show by direct computation that
$$
\begin{vmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{vmatrix} = -\begin{vmatrix} a_1 & a_2 & a_3 \\ c_1 & c_2 & c_3 \\ b_1 & b_2 & b_3 \end{vmatrix}.
$$

### FB 4.1.13
In Exercises 13–18, find $\mathbf{a} \times \mathbf{b}$.

$\mathbf{a} = 2\mathbf{i} - \mathbf{j} + 3\mathbf{k}$, $\mathbf{b} = \mathbf{i} + 2\mathbf{j}$

### FB 4.1.21
In Exercises 20–24, find the area of the parallelogram with vertex at the origin and with the given vectors as edges.

$-5\mathbf{i} + 3\mathbf{j}$ and $\mathbf{i} + 7\mathbf{j}$

### FB 4.1.23
In Exercises 20–24, find the area of the parallelogram with vertex at the origin and with the given vectors as edges.

$2\mathbf{i} - \mathbf{j} + \mathbf{k}$ and $\mathbf{i} + 3\mathbf{j} - \mathbf{k}$

### FB 4.1.25
In Exercises 25–32, find the area of the given geometric configuration.

The triangle with vertices $(-1, 2)$, $(3, -1)$, and $(4, 3)$

## FB §10.2 The LU-Factorization

### FB 10.2.4
In Exercises 3–7, find the solution of $A\mathbf{x} = \mathbf{b}$ from the given combined $L\backslash U$ display of the matrix $A$ and the given vector $\mathbf{b}$.
$$
L\backslash U = \begin{bmatrix} -2 & 5 \\ -2 & 1 \end{bmatrix}, \quad \mathbf{b} = \begin{bmatrix} 3 \\ -7 \end{bmatrix}
$$

### FB 10.2.5
In Exercises 3–7, find the solution of $A\mathbf{x} = \mathbf{b}$ from the given combined $L\backslash U$ display of the matrix $A$ and the given vector $\mathbf{b}$.
$$
L\backslash U = \begin{bmatrix} 1 & -3 & 4 \\ -2 & -1 & 9 \\ 0 & 1 & -6 \end{bmatrix}, \quad \mathbf{b} = \begin{bmatrix} 2 \\ -2 \\ 8 \end{bmatrix}
$$

### FB 10.2.6
In Exercises 3–7, find the solution of $A\mathbf{x} = \mathbf{b}$ from the given combined $L\backslash U$ display of the matrix $A$ and the given vector $\mathbf{b}$.
$$
L\backslash U = \begin{bmatrix} 1 & -4 & 2 \\ 0 & 2 & -1 \\ 3 & 2 & -2 \end{bmatrix}, \quad \mathbf{b} = \begin{bmatrix} -3 \\ 2 \\ 3 \end{bmatrix}
$$

### FB 10.2.7
In Exercises 3–7, find the solution of $A\mathbf{x} = \mathbf{b}$ from the given combined $L\backslash U$ display of the matrix $A$ and the given vector $\mathbf{b}$.
$$
L\backslash U = \begin{bmatrix} 1 & 0 & 0 & 1 \\ 0 & -1 & 2 & 1 \\ -1 & -2 & 1 & 3 \\ 2 & 1 & -1 & 3 \end{bmatrix}, \quad \mathbf{b} = \begin{bmatrix} 4 \\ 7 \\ -8 \\ 14 \end{bmatrix}
$$

## Exam Problems from Other Universities

> [!note] Notation
> Harvard writes vectors with arrows, a vector by its components as $\langle 1, 2, 3 \rangle$, and the length of $\mathbf{v}$ as $\lvert \mathbf{v} \rvert$; FB writes the length as $\lVert \mathbf{v} \rVert$. Here vectors are bold, as in FB. MIT writes vectors in plain letters ($x$, $b$). In an *LDU decomposition* $A = LDU$, $L$ is lower triangular and $U$ upper triangular, both with all diagonal entries $1$, and $D$ is diagonal.

### WEB 4.1.1
Harvard University, Math 21a (Multivariable Calculus), Summer 2007, First Midterm (O. Knill), Problem 1, items 3, 7 and 11 of 20. Each item is marked True or False.

Problem 1) (20 points) No justifications are needed.
- 3) $\langle 1, 2, 3 \rangle \times \langle 2, 4, 6 \rangle = \langle 0, 0, 0 \rangle$.
- 7) If two vectors $\mathbf{v}$, $\mathbf{w}$ are orthogonal, then their cross product is the zero vector.
- 11) The volume of a parallelepiped spanned by $(1, 1, 1)$, $(1, 0, 0)$ and $(0, 1, 2)$ is equal to $1$.

### WEB 4.1.2
Harvard University, Math 21a (Multivariable Calculus), Summer 2007, First Midterm (O. Knill), Problem 8.

Problem 8) (10 points) If you cut the plane $x + 3y + 2z = 6$ by the coordinate planes, we get a triangle.
- a) (4 points) What are the vertices $A$, $B$, $C$ of this triangle?
- b) (6 points) Find the area of this triangle.

### WEB 4.1.3
Harvard University, Math 21a (Multivariable Calculus), Fall 2012, First Hourly (10/2/2012), Problem 1, items 2, 11 and 16 of 20.

Problem 1) True/False (TF) questions (20 points). Mark for each of the 20 questions the correct letter. No justifications are needed.
- 2) There are unit vectors $\mathbf{v}$ and $\mathbf{w}$ in space for which $\lvert \mathbf{v} \times \mathbf{w} \rvert = 2$.
- 11) If $\mathbf{u}$, $\mathbf{v}$, and $\mathbf{w}$ are unit vectors then the volume of the parallelepiped spanned by $\mathbf{u}$, $\mathbf{v}$, and $\mathbf{w}$ is largest when the parallelepiped is a cube.
- 16) $(\mathbf{i} \times \mathbf{j})$ and $(\mathbf{i} \times (\mathbf{i} \times (\mathbf{i} \times \mathbf{j})))$ are parallel.

### WEB 10.2.1
MIT (Massachusetts Institute of Technology), 18.06 Linear Algebra, Fall 2003, Quiz 1 (October 1, 2003), Problem 1. Read from the text layer of the archive's PDF.

**(a)** (15 points) Find an LU-decomposition of the $3 \times 3$ matrix
$$
A = \begin{bmatrix} 1 & 1 & 1 \\ 1 & 2 & 3 \\ 1 & 3 & 6 \end{bmatrix}.
$$

**(b)** (10 points) Solve $Ax = b$ where
$$
b = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}.
$$

### WEB 10.2.2
MIT (Massachusetts Institute of Technology), 18.06 Linear Algebra, Fall 2004, Quiz 1 (October 13, 2004), Problem 1. Read from the text layer of the archive's PDF, which does not show the points of part (b).
$$
A = \begin{bmatrix} 2 & 2 & 2 \\ 4 & 3 & 1 \\ -2 & -1 & 4 \end{bmatrix}
$$

**(a)** (15 points) Compute an LDU factorization of $A$ if one exists.

**(b)** Give all solutions to $Ax = b$ where
$$
b = \begin{bmatrix} 2 \\ -3 \\ 11 \end{bmatrix}.
$$

### WEB 10.2.3
UC Davis (University of California, Davis), MAT 167 Applied Linear Algebra, Fall 2008, Midterm Exam (B. Temple), Problem 1, items (h) and (j).

Problem 1. (20pts) True or False:

(Here $A$ is an arbitrary $m \times n$ matrix, $\operatorname{Col}(A) = C(A)$ denotes the Column Space of $A$, and $\operatorname{Row}(A)$ the Row Space of $A$.)
- (h) Every invertible $n \times n$ matrix $A$ has an LDU decomposition. (L=lower triangular, 1's on diagonal, U=upper triangular, 1's on diagonal, D=diagonal.)
- (j) If $A = A^T$ and $A = LDU$ is an LDU-decomposition of $A$, then $L = U^T$.
