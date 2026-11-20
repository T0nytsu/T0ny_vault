---
course: [LA1]
semester: "115-1"
chapter: ["4.1", "4.2"]
tags: [linear-algebra, homework, questions, determinants]
source:
  - "FB §4.2 exercises pp. 261-262, scanned PDFs"
  - "FIS §4.1 exercises pp. 207-208 and §4.2 exercises pp. 220-222, photos"
created: 2026-11-17
solutions: "[[LA1 HW 4.2 Solutions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> FB §4.2: 17, 18. FIS §4.1: 5, 6, 8. FIS §4.2: 1 (a)–(f), 2, 3, 7, 8, 11, 15, 16, 17. FB is Fraleigh & Beauregard, *Linear Algebra*; FIS is Friedberg, Insel & Spence, *Linear Algebra*.

## FB §4.2 The Determinant of a Square Matrix

### FB 4.2.17
In Exercises 15–20, let $A$ be a $3 \times 3$ matrix with $\det(A) = 2$.

Find $\det(3A)$.

### FB 4.2.18
In Exercises 15–20, let $A$ be a $3 \times 3$ matrix with $\det(A) = 2$.

Find $\det(A + A)$.

## FIS §4.1 Determinants of Order 2

> [!note] Notation
> FIS writes the transpose of $A$ as $A^t$, the $(i, j)$-entry of $A$ as $A_{ij}$, matrices with parentheses, and the set of $m \times n$ matrices with entries in a field $F$ as $\mathsf{M}_{m \times n}(F)$.

### FIS 4.1.5
Prove that if $B$ is the matrix obtained by interchanging the rows of a $2 \times 2$ matrix $A$, then $\det(B) = -\det(A)$.

### FIS 4.1.6
Prove that if the two columns of $A \in \mathsf{M}_{2 \times 2}(F)$ are identical, then $\det(A) = 0$.

### FIS 4.1.8
Prove that if $A \in \mathsf{M}_{2 \times 2}(F)$ is upper triangular, then $\det(A)$ equals the product of the diagonal entries of $A$.

## FIS §4.2 Determinants of Order n

### FIS 4.2.1 (a)-(f)
Label the following statements as true or false.
- (a) The function $\det\colon \mathsf{M}_{n \times n}(F) \to F$ is a linear transformation.
- (b) The determinant of a square matrix can be evaluated by cofactor expansion along any row.
- (c) If two rows of a square matrix $A$ are identical, then $\det(A) = 0$.
- (d) If $B$ is a matrix obtained from a square matrix $A$ by interchanging any two rows, then $\det(B) = -\det(A)$.
- (e) If $B$ is a matrix obtained from a square matrix $A$ by multiplying a row of $A$ by a scalar, then $\det(B) = \det(A)$.
- (f) If $B$ is a matrix obtained from a square matrix $A$ by adding $k$ times row $i$ to row $j$, then $\det(B) = k\det(A)$.

### FIS 4.2.2
Find the value of $k$ that satisfies the following equation:
$$
\det\begin{pmatrix} 3a_1 & 3a_2 & 3a_3 \\ 3b_1 & 3b_2 & 3b_3 \\ 3c_1 & 3c_2 & 3c_3 \end{pmatrix} = k\det\begin{pmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{pmatrix}.
$$

### FIS 4.2.3
Find the value of $k$ that satisfies the following equation:
$$
\det\begin{pmatrix} 2a_1 & 2a_2 & 2a_3 \\ 3b_1 + 5c_1 & 3b_2 + 5c_2 & 3b_3 + 5c_3 \\ 7c_1 & 7c_2 & 7c_3 \end{pmatrix} = k\det\begin{pmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{pmatrix}.
$$

### FIS 4.2.7
In Exercises 5–12, evaluate the determinant of the given matrix by cofactor expansion along the indicated row.
$$
\begin{pmatrix} 0 & 1 & 2 \\ -1 & 0 & -3 \\ 2 & 3 & 0 \end{pmatrix}
$$
along the second row

### FIS 4.2.8
In Exercises 5–12, evaluate the determinant of the given matrix by cofactor expansion along the indicated row.
$$
\begin{pmatrix} 1 & 0 & 2 \\ 0 & 1 & 5 \\ -1 & 3 & 0 \end{pmatrix}
$$
along the third row

### FIS 4.2.11
In Exercises 5–12, evaluate the determinant of the given matrix by cofactor expansion along the indicated row.
$$
\begin{pmatrix} 0 & 2 & 1 & 3 \\ 1 & 0 & -2 & 2 \\ 3 & -1 & 0 & 1 \\ -1 & 1 & 2 & 0 \end{pmatrix}
$$
along the fourth row

### FIS 4.2.15
In Exercises 13–22, evaluate the determinant of the given matrix by any legitimate method.
$$
\begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{pmatrix}
$$

### FIS 4.2.16
In Exercises 13–22, evaluate the determinant of the given matrix by any legitimate method.
$$
\begin{pmatrix} -1 & 3 & 2 \\ 4 & -8 & 1 \\ 2 & 2 & 5 \end{pmatrix}
$$

### FIS 4.2.17
In Exercises 13–22, evaluate the determinant of the given matrix by any legitimate method.
$$
\begin{pmatrix} 0 & 1 & 1 \\ 1 & 2 & -5 \\ 6 & -4 & 3 \end{pmatrix}
$$
