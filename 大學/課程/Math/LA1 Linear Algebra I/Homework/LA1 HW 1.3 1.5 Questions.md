---
course: [LA1]
chapter: ["1.3", "1.5"]
tags: [linear-algebra, homework, questions, matrix-algebra, matrix-inverse]
source:
  - "FB §1.3 exercises pp. 46-48 and §1.5 exercises pp. 84-86, photos and scans"
  - "FIS §1.3 exercises p. 20 and §2.3 exercises p. 97, photos"
created: 2026-09-29
solutions: "[[LA1 HW 1.3 1.5 Solutions]]"
---
> [!info] Coverage
> FB §1.3: 20, 22, 24, 37, 40, 41, 44. FB §1.5: 9, 16, 17, 18, 19, 33. FIS §1.3: 2 (a)(d)(h), 6, 7. FIS §2.3: 13.

## FB §1.3 Matrices and Their Algebra

### FB 1.3.20
Fill in the missing entries in the $4 \times 4$ matrix
$$
\begin{bmatrix} 1 & -1 & \square & 5 \\ \square & 4 & \square & 8 \\ 2 & -7 & -1 & \square \\ \square & \square & 6 & 3 \end{bmatrix}
$$
so that the matrix is symmetric.

### FB 1.3.22
- a. Prove that, if $A$ is a matrix and $\mathbf{x}$ is a row vector, then $\mathbf{x}A$ (if defined) is again a row vector.
- b. Prove that, if $A$ is a matrix and $\mathbf{y}$ is a column vector, then $A\mathbf{y}$ (if defined) is again a column vector.

### FB 1.3.24
The product $A\mathbf{b}$ of a matrix and a column vector is equal to a linear combination of columns of $A$ where the scalar coefficient of the $j$th column of $A$ is $b_j$. In a similar fashion, describe the product $\mathbf{c}A$ of a row vector $\mathbf{c}$ and a matrix $A$ as a linear combination of vectors. [HINT: Consider $((\mathbf{c}A)^T)^T$.]

### FB 1.3.37
The Hilbert matrix $H_n$ is the $n \times n$ matrix $[h_{ij}]$, where $h_{ij} = 1/(i + j - 1)$. Prove that the matrix $H_n$ is symmetric.

### FB 1.3.40
- a. Prove that, if $A$ is a square matrix, then $(A^2)^T = (A^T)^2$ and $(A^3)^T = (A^T)^3$. [HINT: Don't try to show that the matrices have equal entries; instead use Exercise 32.]
- b. State the generalization of part (a), and give a proof using mathematical induction (see Appendix A).

### FB 1.3.41
- a. Let $A$ be an $m \times n$ matrix, and let $\mathbf{e}_j$ be the $n \times 1$ column vector whose $j$th component is $1$ and whose other components are $0$. Show that $A\mathbf{e}_j$ is the $j$th column vector of $A$.
- b. Let $A$ and $B$ be matrices of the same size.
    - i. Prove that, if $A\mathbf{x} = \mathbf{0}$ (the zero vector) for all $\mathbf{x}$, then $A = O$, the zero matrix. [HINT: Use part (a).]
    - ii. Prove that, if $A\mathbf{x} = B\mathbf{x}$ for all $\mathbf{x}$, then $A = B$. [HINT: Consider $A - B$.]

### FB 1.3.44
An $n \times n$ matrix $C$ is **skew symmetric** if $C^T = -C$. Prove that every square matrix $A$ can be written *uniquely* as $A = B + C$ where $B$ is symmetric and $C$ is skew symmetric.

## FB §1.5 Inverses of Square Matrices

### FB 1.5.9
In Exercises 9 and 10, find the inverse of the matrix, if it exists.
$$
\begin{bmatrix} 1 & 0 & 0 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 & 0 & 0 \\ 0 & 0 & 2 & 0 & 0 & 0 \\ 0 & 0 & 0 & 3 & 0 & 0 \\ 0 & 0 & 0 & 0 & 4 & 0 \\ 0 & 0 & 0 & 0 & 0 & 5 \end{bmatrix}
$$

### FB 1.5.16
Let
$$
A^{-1} = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix}.
$$
If possible, find a matrix $C$ such that
$$
AC = \begin{bmatrix} 1 & 2 \\ 0 & 1 \\ 4 & 1 \end{bmatrix}.
$$

### FB 1.5.17
Let
$$
A^{-1} = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix}.
$$
If possible, find a matrix $C$ such that
$$
ACA = \begin{bmatrix} 2 & 1 & 3 \\ -1 & 2 & 2 \\ 2 & 1 & 4 \end{bmatrix}.
$$

### FB 1.5.18
Let
$$
A = \begin{bmatrix} 4 & 2 & 2 \\ 0 & 3 & 1 \\ 2 & 0 & 1 \end{bmatrix}.
$$
If possible, find a matrix $B$ such that $AB = 2A$.

### FB 1.5.19
Let
$$
A = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 2 \\ 1 & 3 & 2 \end{bmatrix}.
$$
If possible, find a matrix $B$ such that $AB = A^2 + 2A$.

### FB 1.5.33
Give an example of two invertible $4 \times 4$ matrices whose sum is singular.

## FIS §1.3 Subspaces

> [!note] Notation
> FIS writes the transpose of $A$ as $A^t$, the $(i, j)$-entry of $A$ as $A_{ij}$, and matrices with parentheses.

### FIS 1.3.2 (a)(d)(h)
Determine the transpose of each of the matrices that follow. In addition, if the matrix is square, compute its trace.
- (a) $\begin{pmatrix} -4 & 2 \\ 5 & -1 \end{pmatrix}$
- (d) $\begin{pmatrix} 10 & 0 & -8 \\ 2 & -4 & 3 \\ -5 & 7 & 6 \end{pmatrix}$
- (h) $\begin{pmatrix} -4 & 0 & 6 \\ 0 & 1 & -3 \\ 6 & -3 & 5 \end{pmatrix}$

### FIS 1.3.6
Prove that $\operatorname{tr}(aA + bB) = a\operatorname{tr}(A) + b\operatorname{tr}(B)$ for any $A, B \in \mathsf{M}_{n \times n}(F)$.

### FIS 1.3.7
Prove that diagonal matrices are symmetric matrices.

## FIS §2.3 Composition of Linear Transformations and Matrix Multiplication

### FIS 2.3.13
Let $A$ and $B$ be $n \times n$ matrices. Recall that the trace of $A$ is defined by
$$
\operatorname{tr}(A) = \sum_{i=1}^{n} A_{ii}.
$$
Prove that $\operatorname{tr}(AB) = \operatorname{tr}(BA)$ and $\operatorname{tr}(A) = \operatorname{tr}(A^t)$.
