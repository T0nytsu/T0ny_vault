---
course: [LA1]
semester: "115-1"
chapter: ["4.3"]
tags: [linear-algebra, homework, questions, determinants, matrix-inverse, linear-systems]
source:
  - "FB §4.3 exercises pp. 271-273, scanned PDFs"
  - "[[LA1 HW 4.3 Questions p271.pdf]]"
  - "[[LA1 HW 4.3 Questions p272.pdf]]"
  - "[[LA1 HW 4.3 Questions p273.pdf]]"
  - "FIS §4.3 exercises pp. 228-230, photos"
  - "[[LA1 HW 4.3 Questions p228.jpg]]"
  - "[[LA1 HW 4.3 Questions p229.jpg]]"
  - "[[LA1 HW 4.3 Questions p230.jpg]]"
created: 2026-11-25
solutions: "[[LA1 HW 4.3 Solutions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!info] Coverage
> FB §4.3: 17, 21, 22, 28, 35, 37, 38, 39. FIS §4.3: 1, 10, 12, 16, 20, 21, 22. FB is Fraleigh & Beauregard, *Linear Algebra*; FIS is Friedberg, Insel & Spence, *Linear Algebra*.
>
> FIS 4.3.22 refers to Exercise 22 of FIS §2.4, which is not among these photos. The Solutions note states what that exercise shows.

## FB §4.3 Computation of Determinants and Cramer's Rule

### FB 4.3.17
In Exercises 14–19, use the corollary to Theorem 4.6 to find $A^{-1}$ if $A$ is invertible.
$$
A = \begin{bmatrix} 3 & 0 & 4 \\ -2 & 1 & 1 \\ 3 & 1 & 2 \end{bmatrix}
$$

### FB 4.3.21
Find the adjoint of the matrix $\begin{bmatrix} 2 & 1 & 0 \\ 3 & 1 & 4 \\ 0 & 2 & 1 \end{bmatrix}$.

### FB 4.3.22
Given that $A^{-1} = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$ and $\det(A^{-1}) = 3$, find the matrix $A$.

### FB 4.3.28
In Exercises 24–31, solve the given system of linear equations by Cramer's rule wherever it is possible.
$$
\begin{aligned}
5x_1 - 2x_2 + x_3 &= 1 \\
x_2 + x_3 &= 0 \\
x_1 + 6x_2 - x_3 &= 4
\end{aligned}
$$

### FB 4.3.35
Let $A$ be a square matrix. Mark each of the following True or False.
- a. The determinant of a square matrix is the product of the entries on its main diagonal.
- b. The determinant of an upper-triangular square matrix is the product of the entries on its main diagonal.
- c. The determinant of a lower-triangular square matrix is the product of the entries on its main diagonal.
- d. A square matrix is nonsingular if and only if its determinant is positive.
- e. The column vectors of an $n \times n$ matrix are independent if and only if the determinant of the matrix is nonzero.
- f. A homogeneous square linear system has a nontrivial solution if and only if the determinant of its coefficient matrix is zero.
- g. The product of a square matrix and its adjoint is the identity matrix.
- h. The product of a square matrix and its adjoint is equal to some scalar times the identity matrix.
- i. The transpose of the adjoint of $A$ is the matrix of cofactors of $A$.
- j. The formula $A^{-1} = (1/\det(A))\operatorname{adj}(A)$ is of practical use in computing the inverse of a large nonsingular matrix.

### FB 4.3.37
Prove that a square matrix is invertible if and only if its adjoint is an invertible matrix.

### FB 4.3.38
Let $A$ be an $n \times n$ matrix. Prove that $\det(\operatorname{adj}(A)) = \det(A)^{n-1}$.

### FB 4.3.39
Let $A$ be an invertible $n \times n$ matrix with $n > 1$. Using Exercises 37 and 38, prove that $\operatorname{adj}(\operatorname{adj}(A)) = (\det(A))^{n-2}A$.

## FIS §4.3 Properties of Determinants

> [!note] Notation
> FIS writes the transpose of $A$ as $A^t$, the $(i, j)$-entry of $A$ as $A_{ij}$, matrices with parentheses, the set of $n \times n$ matrices with entries in a field $F$ as $\mathsf{M}_{n \times n}(F)$ (with $C$ and $R$ for the complex and the real numbers), the polynomials of degree at most $n$ as $\mathsf{P}_{n}(F)$, and the matrix of $\mathsf{T}$ relative to the ordered bases $\beta$ and $\gamma$ as $[\mathsf{T}]_{\beta}^{\gamma}$. The book marks Exercise 21 with a dagger (21.†).

### FIS 4.3.1
Label the following statements as true or false.
- (a) If $E$ is an elementary matrix, then $\det(E) = \pm 1$.
- (b) For any $A, B \in \mathsf{M}_{n \times n}(F)$, $\det(AB) = \det(A) \cdot \det(B)$.
- (c) A matrix $M \in \mathsf{M}_{n \times n}(F)$ is invertible if and only if $\det(M) = 0$.
- (d) A matrix $M \in \mathsf{M}_{n \times n}(F)$ has rank $n$ if and only if $\det(M) \ne 0$.
- (e) For any $A \in \mathsf{M}_{n \times n}(F)$, $\det(A^t) = -\det(A)$.
- (f) The determinant of a square matrix can be evaluated by cofactor expansion along any column.
- (g) Every system of $n$ linear equations in $n$ unknowns can be solved by Cramer's rule.
- (h) Let $Ax = b$ be the matrix form of a system of $n$ linear equations in $n$ unknowns, where $x = (x_1, x_2, \dots, x_n)^t$. If $\det(A) \ne 0$ and if $M_k$ is the $n \times n$ matrix obtained from $A$ by replacing row $k$ of $A$ by $b^t$, then the unique solution of $Ax = b$ is
$$
x_k = \frac{\det(M_k)}{\det(A)} \quad \text{for } k = 1, 2, \dots, n.
$$

### FIS 4.3.10
A matrix $M \in \mathsf{M}_{n \times n}(C)$ is called **nilpotent** if, for some positive integer $k$, $M^k = O$, where $O$ is the $n \times n$ zero matrix. Prove that if $M$ is nilpotent, then $\det(M) = 0$.

### FIS 4.3.12
A matrix $Q \in \mathsf{M}_{n \times n}(R)$ is called **orthogonal** if $QQ^t = I$. Prove that if $Q$ is orthogonal, then $\det(Q) = \pm 1$.

### FIS 4.3.16
Use determinants to prove that if $A, B \in \mathsf{M}_{n \times n}(F)$ are such that $AB = I$, then $A$ is invertible (and hence $B = A^{-1}$).

### FIS 4.3.20
Suppose that $M \in \mathsf{M}_{n \times n}(F)$ can be written in the form
$$
M = \begin{pmatrix} A & B \\ O & I \end{pmatrix},
$$
where $A$ is a square matrix. Prove that $\det(M) = \det(A)$.

### FIS 4.3.21
Prove that if $M \in \mathsf{M}_{n \times n}(F)$ can be written in the form
$$
M = \begin{pmatrix} A & B \\ O & C \end{pmatrix},
$$
where $A$ and $C$ are square matrices, then $\det(M) = \det(A) \cdot \det(C)$.

### FIS 4.3.22
Let $\mathsf{T}\colon \mathsf{P}_{n}(F) \to \mathsf{F}^{n+1}$ be the linear transformation defined in Exercise 22 of Section 2.4 by $\mathsf{T}(f) = (f(c_0), f(c_1), \dots, f(c_n))$, where $c_0, c_1, \dots, c_n$ are distinct scalars in an infinite field $F$. Let $\beta$ be the standard ordered basis for $\mathsf{P}_{n}(F)$ and $\gamma$ be the standard ordered basis for $\mathsf{F}^{n+1}$.

**(a)** Show that $M = [\mathsf{T}]_{\beta}^{\gamma}$ has the form
$$
\begin{pmatrix} 1 & c_0 & c_0^2 & \cdots & c_0^n \\ 1 & c_1 & c_1^2 & \cdots & c_1^n \\ \vdots & \vdots & \vdots & & \vdots \\ 1 & c_n & c_n^2 & \cdots & c_n^n \end{pmatrix}.
$$
A matrix with this form is called a **Vandermonde matrix**.

**(b)** Use Exercise 22 of Section 2.4 to prove that $\det(M) \ne 0$.

**(c)** Prove that
$$
\det(M) = \prod_{0 \le i < j \le n} (c_j - c_i),
$$
the product of all terms of the form $c_j - c_i$ for $0 \le i < j \le n$.
