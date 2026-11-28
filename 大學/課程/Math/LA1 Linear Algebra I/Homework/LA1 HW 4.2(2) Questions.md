---
course: [LA1]
semester: "115-1"
chapter: ["4.2"]
tags: [linear-algebra, homework, questions, determinants, matrix-inverse]
source:
  - "FB §4.2 exercises p. 262, scanned PDF"
  - "[[LA1 HW 4.2(2) Questions p262.pdf]]"
  - "FIS §4.2 exercises p. 222, photo"
  - "[[LA1 HW 4.2(2) Questions p222.jpg]]"
created: 2026-11-24
solutions: "[[LA1 HW 4.2(2) Solutions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> FB §4.2: 21, 26, 29, 30, 31, 32, 33. FIS §4.2: 25, 26, 27, 29. FB is Fraleigh & Beauregard, *Linear Algebra*; FIS is Friedberg, Insel & Spence, *Linear Algebra*.
>
> This is the second assignment on §4.2; the first is [[LA1 HW 4.2 Questions]].

## FB §4.2 The Determinant of a Square Matrix

### FB 4.2.21
Mark each of the following True or False.
- ==🟢a==. The determinant $\det(A)$ is defined for any matrix $A$.
- b. The determinant $\det(A)$ is defined for each square matrix $A$.
- c. The determinant of a square matrix is a scalar.
- d. If a matrix $A$ is multiplied by a scalar $c$, the determinant of the resulting matrix is $c \cdot \det(A)$.
- e. If an $n \times n$ matrix $A$ is multiplied by a scalar $c$, the determinant of the resulting matrix is $c^{n} \cdot \det(A)$.
- f. For every square matrix $A$, we have $\det(AA^T) = \det(A^TA) = [\det(A)]^2$.
- g. If two rows and also two columns of a square matrix $A$ are interchanged, the determinant changes sign.
- h. The determinant of an elementary matrix is nonzero.
- i. If $\det(A) = 2$ and $\det(B) = 3$, then $\det(A + B) = 5$.
- j. If $\det(A) = 2$ and $\det(B) = 3$, then $\det(AB) = 6$.

### FB 4.2.26
In Exercises 26–29, find the values of $\lambda$ for which the given matrix is singular.
$$
\begin{bmatrix} 1 - \lambda & 2 \\ 3 & 2 - \lambda \end{bmatrix}
$$

### FB 4.2.29
In Exercises 26–29, find the values of $\lambda$ for which the given matrix is singular.
$$
\begin{bmatrix} 1 - \lambda & 0 & 2 \\ 0 & 4 - \lambda & 3 \\ 0 & 4 & -\lambda \end{bmatrix}
$$

### FB 4.2.30
If $A$ and $B$ are $n \times n$ matrices and if $A$ is singular, prove (without using Theorem 4.4) that $AB$ is also singular. [HINT: Assume that $AB$ is invertible, and derive a contradiction.]

### FB 4.2.31
Prove that if $A$ is invertible, then $\det(A^{-1}) = 1/\det(A)$.

### FB 4.2.32
If $A$ and $C$ are $n \times n$ matrices, with $C$ invertible, prove that $\det(A) = \det(C^{-1}AC)$.

### FB 4.2.33
Without using the multiplicative property of determinants (Theorem 4.4), prove that $\det(AB) = \det(A) \cdot \det(B)$ for the case where $B$ is a diagonal matrix.

## FIS §4.2 Determinants of Order n

> [!note] Notation
> FIS writes the transpose of $A$ as $A^t$, the $(i, j)$-entry of $A$ as $A_{ij}$, and the set of $n \times n$ matrices with entries in a field $F$ as $\mathsf{M}_{n \times n}(F)$. The book marks Exercise 29 with a dagger (29.†).

### FIS 4.2.25
Prove that $\det(kA) = k^{n}\det(A)$ for any $A \in \mathsf{M}_{n \times n}(F)$.

### FIS 4.2.26
Let $A \in \mathsf{M}_{n \times n}(F)$. Under what conditions is $\det(-A) = \det(A)$?

### FIS 4.2.27
Prove that if $A \in \mathsf{M}_{n \times n}(F)$ has two identical columns, then $\det(A) = 0$.

### FIS 4.2.29
Prove that if $E$ is an elementary matrix, then $\det(E^t) = \det(E)$.
