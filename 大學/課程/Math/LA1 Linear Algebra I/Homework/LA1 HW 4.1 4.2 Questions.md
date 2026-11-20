---
course:
  - LA1
semester: 115-1
chapter:
  - "4.1"
  - "4.2"
tags:
  - homework
  - questions
  - determinants
  - vectors
source:
  - FB §4.1 exercises pp. 248-249 and §4.2 exercises pp. 261-262, scanned PDFs
  - "[[LA1 HW 4.1 4.2 Questions p248.pdf]]"
  - "[[LA1 HW 4.1 4.2 Questions p249.pdf]]"
  - "[[LA1 HW 4.1 4.2 Questions p261.pdf]]"
  - "[[LA1 HW 4.1 4.2 Questions p262.pdf]]"
created: 2026-11-17
solutions: "[[LA1 HW 4.1 4.2 Solutions]]"
up: "[[LA1 Index]]"
format: math-notes 2.3
---
> [!info] Coverage
> FB §4.1: 19, 27, 31, 33, 37, 57, 58, 59. FB §4.2: 7, 8, 9, 10. FB is Fraleigh & Beauregard, *Linear Algebra*.
>
> Exercises 57–59 refer to Theorem 4.1 (Properties of Cross Product), which is stated earlier in §4.1, on a page that is not among these scans. The Solutions note restates it.

## FB §4.1 Areas, Volumes, and Cross Products

### FB 4.1.19
Mark each of the following True or False.
- a. The determinant of a $2 \times 2$ matrix is a vector.
- b. If two rows of a $3 \times 3$ matrix are interchanged, the sign of the determinant is changed.
- c. The determinant of a $3 \times 3$ matrix is zero if two rows of the matrix are parallel vectors in $\mathbb{R}^3$.
- d. In order for the determinant of a $3 \times 3$ matrix to be zero, two rows of the matrix must be parallel vectors in $\mathbb{R}^3$.
- e. The determinant of a $3 \times 3$ matrix is zero if the points in $\mathbb{R}^3$ given by the rows of the matrix lie in a plane.
- f. The determinant of a $3 \times 3$ matrix is zero if the points in $\mathbb{R}^3$ given by the rows of the matrix lie in a plane through the origin.
- g. The parallelogram in $\mathbb{R}^2$ determined by nonzero vectors $\mathbf{a}$ and $\mathbf{b}$ is a square if and only if $\mathbf{a} \cdot \mathbf{b} = 0$.
- h. The box in $\mathbb{R}^3$ determined by vectors $\mathbf{a}$, $\mathbf{b}$, and $\mathbf{c}$ is a cube if and only if $\mathbf{a} \cdot \mathbf{b} = \mathbf{a} \cdot \mathbf{c} = \mathbf{b} \cdot \mathbf{c} = 0$ and $\mathbf{a} \cdot \mathbf{a} = \mathbf{b} \cdot \mathbf{b} = \mathbf{c} \cdot \mathbf{c}$.
- i. If the angle between vectors $\mathbf{a}$ and $\mathbf{b}$ in $\mathbb{R}^3$ is $\pi/4$, then $\lVert \mathbf{a} \times \mathbf{b} \rVert = \lvert \mathbf{a} \cdot \mathbf{b} \rvert$.
- j. For any vector $\mathbf{a}$ in $\mathbb{R}^3$, we have $\lVert \mathbf{a} \times \mathbf{a} \rVert = \lVert \mathbf{a} \rVert^2$.

### FB 4.1.27
In Exercises 25–32, find the area of the given geometric configuration.

The triangle with vertices $(2, 1, -3)$, $(3, 0, 4)$, and $(1, 0, 5)$

### FB 4.1.31
In Exercises 25–32, find the area of the given geometric configuration.

The parallelogram with vertices $(1, 0, 1)$, $(3, 1, 4)$, $(0, 2, 9)$, and $(-2, 1, 6)$

### FB 4.1.33
In Exercises 33–36, find $\mathbf{a} \cdot (\mathbf{b} \times \mathbf{c})$ and $\mathbf{a} \times (\mathbf{b} \times \mathbf{c})$.

$\mathbf{a} = \mathbf{i} + 2\mathbf{j} - 3\mathbf{k}$, $\mathbf{b} = 4\mathbf{i} - \mathbf{j} + 2\mathbf{k}$, $\mathbf{c} = 3\mathbf{i} + \mathbf{k}$

### FB 4.1.37
In Exercises 37–40, find the volume of the box having the given vectors as adjacent edges.

$-\mathbf{i} + 4\mathbf{j} + 7\mathbf{k}$, $3\mathbf{i} - 2\mathbf{j} - \mathbf{k}$, $4\mathbf{i} + 2\mathbf{k}$

### FB 4.1.57
Prove property (2) of Theorem 4.1.

### FB 4.1.58
Prove property (3) of Theorem 4.1.

### FB 4.1.59
Prove property (6) of Theorem 4.1.

## FB §4.2 The Determinant of a Square Matrix

### FB 4.2.7
In Exercises 1–10, find the determinant of the given matrix.
$$
\begin{bmatrix} 2 & 3 & 4 & 6 \\ 2 & 0 & -9 & 6 \\ 4 & 1 & 0 & 2 \\ 0 & 1 & -1 & 0 \end{bmatrix}
$$

### FB 4.2.8
In Exercises 1–10, find the determinant of the given matrix.
$$
\begin{bmatrix} 2 & 0 & -1 & 7 \\ 6 & 1 & 0 & 4 \\ 8 & -2 & 1 & 0 \\ 4 & 1 & 0 & 2 \end{bmatrix}
$$

### FB 4.2.9
In Exercises 1–10, find the determinant of the given matrix.
$$
\begin{bmatrix} 1 & 2 & 0 & -1 & 2 & 4 \\ 6 & 2 & 8 & 1 & -1 & 1 \\ 4 & 2 & 1 & 2 & 2 & -5 \\ 4 & 5 & 4 & 5 & 1 & 2 \\ 1 & 2 & 0 & -1 & 2 & 4 \\ 1 & 0 & 1 & 8 & 1 & 5 \end{bmatrix}
$$

### FB 4.2.10
In Exercises 1–10, find the determinant of the given matrix.
$$
\begin{bmatrix} 1 & 0 & 1 & 2 \\ 3 & 4 & 1 & 2 \\ 6 & 1 & 0 & 0 \\ 0 & 1 & 2 & 1 \end{bmatrix}
$$
