---
course: [LA1]
chapter: ["1.4", "1.5"]
tags: [linear-algebra, lecture, matrix-inverse, linear-systems, needs-review]
source:
  - "LA1 lecture 2026-09-29, board photos (28 pages)"
created: 2026-09-30
---
> [!info] Coverage
> Properties of [[Invertible Matrix|inverses]] and Theorem 1.10 (§1.5); [[Linear System|linear systems]] in matrix form, the [[Augmented Matrix|augmented matrix]], [[Elementary Row Operation|elementary row operations]] and [[Elementary Matrix|row-elementary matrices]] with Theorem 1.8, [[Row Equivalence|row equivalence]], [[Row-Echelon Form|row-echelon form]], [[Reduced Row-Echelon Form|reduced row-echelon form]], and [[Gaussian Elimination|Gaussian elimination]] (§1.4).

> [!note] Notation
> The board writes vectors without bold ($x$, $b$) and uses these symbols:
> - $A_{(i)}$ is the $i$th row of $A$.
> - $r_{ij}(A)$, $r_{i}^{s}(A)$ and $r_{ij}^{s}(A)$ are the three elementary row operations applied to $A$; $R_{ij}$, $R_{i}^{s}$ and $R_{ij}^{s}$ are the matching row-elementary matrices, obtained by applying the operation to $I$.
> - A superscript on $r$ or $R$ is the scalar $s$, not a power or an inverse: $R_{2}^{-1}$ multiplies row 2 by $-1$.
> - $A \overset{r}{\sim} B$ means that $A$ is row equivalent to $B$.

## Properties of Inverses

> [!theorem] Proposition
> Let $A$ be an invertible matrix, $k \in \mathbb{N}$, and $\alpha \in \mathbb{R} \setminus \{0\}$. Then $A^{-1}$, $A^{k}$, $\alpha A$, and $A^T$ are invertible, and
> - (1) $(A^{-1})^{-1} = A$
> - (2) $(A^{k})^{-1} = (A^{-1})^{k}$
> - (3) $(\alpha A)^{-1} = \frac{1}{\alpha}A^{-1}$ ==(?)==
> - (4) $(A^T)^{-1} = (A^{-1})^T$ ==(?)==

> [!proof]- Proof of (1) and (2)
> $\because$ $A$ is invertible, $\therefore$ $\exists\, A^{-1}$ s.t. $A^{-1}A = AA^{-1} = I$.
>
> **(1)** By definition, $(A^{-1})^{-1} = A$.
>
> **(2)**
> $$
> (A^{-1})^{k}A^{k} = \underbrace{A^{-1}A^{-1}\cdots A^{-1}}_{k \text{ times}}\,\underbrace{AA\cdots A}_{k \text{ times}} = I.
> $$
> Similarly, $A^{k}(A^{-1})^{k} = I$. $\implies (A^{k})^{-1} = (A^{-1})^{k}$. $\blacksquare$

## Inverse of a Product

> [!theorem] Theorem 1.10
> Let $A$ and $B$ be invertible $n \times n$ matrices. Then $AB$ is invertible, and $(AB)^{-1} = B^{-1}A^{-1}$.

> [!proof]- Proof
> $\because$ $A$ and $B$ are invertible, $\therefore$ $A^{-1}$ and $B^{-1}$ exist s.t. $AA^{-1} = A^{-1}A = I$ and $BB^{-1} = B^{-1}B = I$.
> $$
> \implies
> \begin{aligned}
> (B^{-1}A^{-1})(AB) &= B^{-1}IB = B^{-1}B = I, \\
> (AB)(B^{-1}A^{-1}) &= AIA^{-1} = AA^{-1} = I.
> \end{aligned}
> $$
> $\implies$ $AB$ is invertible and $(AB)^{-1} = B^{-1}A^{-1}$. $\blacksquare$

> [!note] Note
> - $(AB)^T = B^TA^T$
> - $(A+B)^T = A^T + B^T$
> - $(AB)^{-1} = B^{-1}A^{-1}$

> [!warning] Does not necessarily hold
> $(A+B)^{-1} = A^{-1} + B^{-1}$ does **not** necessarily hold.

> [!example] Example
> Find $(AB)^{-1}$ if $A^{-1} = \begin{bmatrix} 7 & -3 & -3 \\ -1 & 1 & 0 \\ -1 & 0 & 1 \end{bmatrix}$ and $B^{-1} = \begin{bmatrix} 1 & -2 & 1 \\ -1 & 1 & 0 \\ \frac{2}{3} & 0 & -\frac{1}{3} \end{bmatrix}$.

> [!solution]- Solution
> $$
> (AB)^{-1} = B^{-1}A^{-1} = \begin{bmatrix} 1 & -2 & 1 \\ -1 & 1 & 0 \\ \frac{2}{3} & 0 & -\frac{1}{3} \end{bmatrix} \begin{bmatrix} 7 & -3 & -3 \\ -1 & 1 & 0 \\ -1 & 0 & 1 \end{bmatrix} = \begin{bmatrix} 8 & -5 & -2 \\ -8 & 4 & 3 \\ 5 & -2 & -\frac{7}{3} \end{bmatrix}.
> $$

## Consequences of Invertibility

> [!theorem] Proposition
> - (1) If $C$ is invertible and $AC = BC$, then $A = B$. ==(?)==
> - (3) If $A$ is invertible and $AB = O$, then $B = O$. ==(?)==
> - (4) If $B$ is invertible and $AB^{-1} = B^{-1}A$, then $AB = BA$. ==(?)==
> - (6) If $A^2 = A$, then $A = I$ or $A$ is singular.

> [!proof]- Proof of (1), (3), (4) and (6)
> **(1)** $\because$ $C$ is invertible, $\therefore$ $C^{-1}$ exists and $C^{-1}C = CC^{-1} = I$. $\because$ $AC = BC$,
> $$
> ACC^{-1} = BCC^{-1} \implies A = B.
> $$
>
> **(3)** $\because$ $A$ is invertible, $\therefore$ $A^{-1}$ exists s.t. $A^{-1}A = AA^{-1} = I$. $\because$ $AB = O$,
> $$
> A^{-1}AB = A^{-1}O = O \implies B = O.
> $$
>
> **(4)** $\because$ $B$ is invertible, $\therefore$ $B^{-1}$ exists and $B^{-1}B = BB^{-1} = I$. $\because$ $AB^{-1} = B^{-1}A$,
> $$
> AB^{-1}B = B^{-1}AB \quad (A = B^{-1}AB) \implies BA = BB^{-1}AB = AB.
> $$
>
> **(6)** If $A$ is not singular ($A$ is invertible), then $A^{-1}$ exists and $A^{-1}A = AA^{-1} = I$. $\because$ $A^2 = A$,
> $$
> \underbrace{A^{-1}A^{2}}_{=\,A} = A^{-1}A = I \implies A = I. \qquad \blacksquare
> $$

## Linear Systems

This part of the lecture is §1.4, Solving Systems of Linear Equations. Recall that the linear system
$$
\begin{cases} \alpha - 2\beta = -t \\ 3\alpha + 5\beta = 19t \end{cases}
$$
can be written as
$$
\alpha \begin{bmatrix} 1 \\ 3 \end{bmatrix} + \beta \begin{bmatrix} -2 \\ 5 \end{bmatrix} = \begin{bmatrix} -t \\ 19t \end{bmatrix} \iff \underbrace{\begin{bmatrix} 1 & -2 \\ 3 & 5 \end{bmatrix}}_{A} \underbrace{\begin{bmatrix} \alpha \\ \beta \end{bmatrix}}_{x} = \underbrace{\begin{bmatrix} -t \\ 19t \end{bmatrix}}_{b}.
$$
Does the system have a unique solution, infinitely many solutions, or no solution? What conditions on $A$ are required? How do we solve for $\alpha$ and $\beta$?

In general, the linear system
$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n = b_1 \\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n = b_2 \\
\qquad \vdots \\
a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n = b_m
\end{cases}
$$
with
$$
A = \begin{bmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ a_{21} & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m1} & a_{m2} & \cdots & a_{mn} \end{bmatrix}, \quad x = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}, \quad b = \begin{bmatrix} b_1 \\ b_2 \\ \vdots \\ b_m \end{bmatrix}
$$
is equivalent to $Ax = b$.

> [!note] Note
> For a linear system, one of the following is true:
> - (a) It has exactly one solution.
> - (b) It has infinitely many solutions.
> - (c) It has no solution.
>
> In cases (a) and (b) the system is **consistent**; in case (c) it is **inconsistent**.

## Augmented Matrix

> [!definition] Augmented Matrix
> The *augmented matrix* or *partitioned matrix* of the linear system $Ax = b$ is defined by
> $$
> [A \mid b] = \left[\begin{array}{cccc|c} a_{11} & a_{12} & \cdots & a_{1n} & b_1 \\ a_{21} & a_{22} & \cdots & a_{2n} & b_2 \\ \vdots & \vdots & \ddots & \vdots & \vdots \\ a_{m1} & a_{m2} & \cdots & a_{mn} & b_m \end{array}\right].
> $$

> [!definition] Rows of a Matrix
> For an $m \times n$ matrix $A$, write
> $$
> A = \begin{bmatrix} A_{(1)} \\ A_{(2)} \\ \vdots \\ A_{(m)} \end{bmatrix},
> $$
> where $A_{(i)}$ is the $i$th row of $A$.

## Elementary Row Operations

> [!definition] Elementary Row Operations
> The three elementary row operations on an $m \times n$ matrix $A$ are the following.
>
> **(1)** Interchange two rows: $r_{ij}(A)$ has $A_{(j)}$ in row $i$ and $A_{(i)}$ in row $j$,
> $$
> r_{ij}(A) = \begin{bmatrix} A_{(1)} \\ \vdots \\ A_{(j)} \\ \vdots \\ A_{(i)} \\ \vdots \\ A_{(m)} \end{bmatrix}.
> $$
>
> **(2)** Multiply a row by a nonzero constant $s$: $r_{i}^{s}(A)$ has $sA_{(i)}$ in row $i$,
> $$
> r_{i}^{s}(A) = \begin{bmatrix} A_{(1)} \\ \vdots \\ sA_{(i)} \\ \vdots \\ A_{(m)} \end{bmatrix}.
> $$
>
> **(3)** Add $s$ times row $i$ to row $j$: $r_{ij}^{s}(A)$. ==(?)==

> [!example] Example
> Compute $r_{13}\left(\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}\right)$.

> [!solution]- Solution
> $$
> r_{13}\left(\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}\right) = \begin{bmatrix} 7 & 8 & 9 \\ 4 & 5 & 6 \\ 1 & 2 & 3 \end{bmatrix}
> $$

## Row-Elementary Matrices

> [!example] Example
> Let $A = \begin{bmatrix} 0 & 2 & 1 \\ 1 & -3 & 6 \\ 3 & 2 & -1 \end{bmatrix}$. Compute $R_{12}A$ and $R_{2}^{-1}A$.

> [!solution]- Solution
> $$
> \begin{aligned}
> R_{12}A &= \begin{bmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} 0 & 2 & 1 \\ 1 & -3 & 6 \\ 3 & 2 & -1 \end{bmatrix} = \begin{bmatrix} 1 & -3 & 6 \\ 0 & 2 & 1 \\ 3 & 2 & -1 \end{bmatrix} = r_{12}(A), \\
> R_{2}^{-1}A &= \begin{bmatrix} 1 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} 0 & 2 & 1 \\ 1 & -3 & 6 \\ 3 & 2 & -1 \end{bmatrix} = \begin{bmatrix} 0 & 2 & 1 \\ -1 & 3 & -6 \\ 3 & 2 & -1 \end{bmatrix} = r_{2}^{-1}(A).
> \end{aligned}
> $$
> In the same way, $R_{12}^{3}A = \cdots = r_{12}^{3}(A)$.

> [!theorem] Theorem 1.8
> Let $A$ be an $m \times n$ matrix and $I$ the $m \times m$ identity matrix. Then
> $$
> r_{ij}(A) = R_{ij}A, \qquad r_{i}^{s}(A) = R_{i}^{s}A, \qquad r_{ij}^{s}(A) = R_{ij}^{s}A,
> $$
> where
> $$
> R_{ij} = r_{ij}(I) = \begin{bmatrix} e_1 \\ \vdots \\ e_j \\ \vdots \\ e_i \\ \vdots \\ e_m \end{bmatrix}, \qquad I = \begin{bmatrix} e_1 \\ e_2 \\ \vdots \\ e_m \end{bmatrix},
> $$
> and $e_i$ is the $i$th row of $I$ ==(?)==.

> [!proof]- Proof of $r_{ij}(A) = R_{ij}A$
> Each $e_k$ is $1 \times m$ and $A$ is $m \times n$, so
> $$
> R_{ij}A = \begin{bmatrix} e_1 \\ \vdots \\ e_j \\ \vdots \\ e_i \\ \vdots \\ e_m \end{bmatrix} A = \begin{bmatrix} e_1A \\ \vdots \\ e_jA \\ \vdots \\ e_iA \\ \vdots \\ e_mA \end{bmatrix} = \begin{bmatrix} A_{(1)} \\ \vdots \\ A_{(j)} \\ \vdots \\ A_{(i)} \\ \vdots \\ A_{(m)} \end{bmatrix} = r_{ij}(A). \qquad \blacksquare
> $$

> [!note] Note
> Every row-elementary matrix is invertible, and its inverse is also a row-elementary matrix.

> [!proof]- Proof
> **(1)** $R_{ij}R_{ij} = I = R_{ij}R_{ij}$.
>
> **(2)** $R_{i}^{1/s}R_{i}^{s} = I = R_{i}^{s}R_{i}^{1/s}$.
>
> **(3)** $R_{ij}^{-s}R_{ij}^{s} = I = R_{ij}^{s}R_{ij}^{-s}$. $\blacksquare$

> [!example] Example
> Find the inverses of the row-elementary matrices
> $$
> E_1 = \begin{bmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix}, \quad E_2 = \begin{bmatrix} 3 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} = R_{1}^{3}, \quad E_3 = \begin{bmatrix} 1 & 0 & 4 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} = R_{31}^{4}.
> $$

> [!solution]- Solution
> $$
> E_1^{-1} = \begin{bmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix}, \qquad E_2^{-1} = R_{1}^{1/3} = \begin{bmatrix} \frac{1}{3} & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix},
> $$
> and $E_3^{-1} = R_{31}^{-4} = \begin{bmatrix} 1 & 0 & -4 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$ ==(?)==.

## Row Equivalence

> [!definition] Row Equivalence
> If a matrix $B$ can be obtained from a matrix $A$ by using a sequence of elementary row operations, then $A$ is *row equivalent* to $B$, denoted by $A \overset{r}{\sim} B$. That is, if $\exists\, E_1, E_2, \dots, E_k$ row-elementary matrices s.t. $E_k \cdots E_2E_1A = B$, then $A \overset{r}{\sim} B$.

> [!note] Note
> $A \overset{r}{\sim} B \implies \exists\, E_1, \dots, E_k$ row-elementary matrices s.t. $E_kE_{k-1}\cdots E_2E_1A = B$. $\because$ each $E_i$ is invertible, $\therefore$ $P = E_kE_{k-1}\cdots E_2E_1$ is invertible. $\implies \exists\, P$ invertible s.t. $PA = B$.

## Row-Echelon Form

> [!definition] Row-Echelon Form
> A matrix is called *row-echelon* if
> - (a) All rows containing only zeros appear below rows with nonzero entries.
> - (b) The first nonzero entry in any row appears in a column to the right of the first nonzero entry in any preceding row.
>
> The first nonzero entry in a row is the *pivot* for that row.

> [!example] Example
> Determine which of the matrices are in row-echelon form:
> $$
> A = \begin{bmatrix} 1 & 3 & 2 \\ 0 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix}, \quad B = \begin{bmatrix} 2 & 4 & 0 \\ 1 & 3 & 2 \\ 0 & 0 & 0 \end{bmatrix}, \quad C = \begin{bmatrix} 0 & -1 & 2 \\ 0 & 0 & 3 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}, \quad D = \begin{bmatrix} 1 & 3 & 2 & 5 \\ 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \end{bmatrix}.
> $$

> [!solution]- Solution
> $A$ ✗, $B$ ✗, $C$ ✓, $D$ ✓. **$C$: pivots $-1$, $3$. $D$: pivots $1$, $1$, $1$.**

## Reduced Row-Echelon Form

> [!definition] Reduced Row-Echelon Form
> A matrix is in **reduced** row-echelon form if
> - (a) It is row-echelon.
> - (b) Each **pivot** is equal to **1** and each column which contains the pivot of some row has all its other entries $0$.

> [!example] Example
> For each matrix, decide whether it is row-echelon and whether it is in reduced row-echelon form.
> $$
> \begin{aligned}
> M_1 &= \begin{bmatrix} 1 & 0 & 5 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \end{bmatrix}, & M_2 &= \begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & -1 & 0 \\ 0 & 0 & 1 & 0 \end{bmatrix}, & M_3 &= \begin{bmatrix} 0 & 2 & 1 \\ 1 & 0 & -3 \\ 0 & 0 & 0 \end{bmatrix}, \\
> M_4 &= \begin{bmatrix} 1 & 2 & -1 & 4 \\ 0 & 1 & 0 & 3 \\ 0 & 0 & 1 & -2 \end{bmatrix}, & M_5 &= \begin{bmatrix} 1 & 2 & -3 & 4 \\ 0 & 2 & 1 & -1 \\ 0 & 0 & 1 & -3 \end{bmatrix}, & M_6 &= \begin{bmatrix} 0 & 1 & 0 & 5 \\ 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 \end{bmatrix}.
> \end{aligned}
> $$
> The entry $-1$ in $M_2$ is hard to read ==(?)==.

> [!solution]- Solution
> | Matrix | Row-echelon | Reduced row-echelon |
> | --- | --- | --- |
> | $M_1$ | ✓ | ✓ |
> | $M_2$ | ✓ | ✗ |
> | $M_3$ | ✗ | ✗ |
> | $M_4$ | ✓ | ✗ |
> | $M_5$ | ✓ | ✗ |
> | $M_6$ | ✓ | ✓ |

## Gaussian Elimination

> [!definition] Gaussian Elimination
> *Gaussian elimination*: use elementary row operations to transform a matrix $A$ into row-echelon form.

> [!example] Example
> Reduce the matrix
> $$
> A = \begin{bmatrix} 2 & -4 & 2 & -2 \\ 2 & -4 & 3 & -4 \\ 4 & -8 & 3 & -2 \\ 0 & 0 & -1 & 2 \end{bmatrix}
> $$
> to row-echelon form.

> [!solution]- Solution
> Add $(-1) \times$ row 1 to row 2 and $(-2) \times$ row 1 to row 3; then add row 2 to rows 3 and 4:
> $$
> A \overset{r}{\sim} \begin{bmatrix} 2 & -4 & 2 & -2 \\ 0 & 0 & 1 & -2 \\ 0 & 0 & -1 & 2 \\ 0 & 0 & -1 & 2 \end{bmatrix} \overset{r}{\sim} \begin{bmatrix} 2 & -4 & 2 & -2 \\ 0 & 0 & 1 & -2 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix} = H.
> $$
> The pivots of $H$ are $2$ and $1$. In terms of row-elementary matrices,
> $$
> \boxed{R_{24}^{1}R_{23}^{1}R_{13}^{-2}R_{12}^{-1}A = H}.
> $$

> [!todo] Transcription check
> - Properties of Inverses, (3) and (4): the answers are only partly visible at the left edge of page 3 of the photo PDF; read as $(\alpha A)^{-1} = \frac{1}{\alpha}A^{-1}$ and $(A^T)^{-1} = (A^{-1})^T$. Their proofs are not in the photos.
> - Consequences of Invertibility: the statements are not in the photos (perhaps they were on the handout). Items (1), (3) and (4) are read off their proofs; (6) is on the board. Items (2) and (5) are missing; only the end of the proof of (5), "→← (contradiction)", is visible on page 7.
> - Elementary Row Operations, (3): the board defining $r_{ij}^{s}$ is not in the photos. "Add $s$ times row $i$ to row $j$" is inferred from $E_3 = R_{31}^{4}$ (page 18) and from the reduction under Gaussian Elimination (pages 26–28).
> - Theorem 1.8: the description of $e_i$ next to $I$ is partly erased (page 16); read as "the $i$th row of $I$".
> - Row-elementary matrices, example: $E_3^{-1}$ is partly hidden by the teacher (page 18); the entries follow the rule $R_{ij}^{-s}R_{ij}^{s} = I$ in the Note above it.
> - Row Equivalence: the board reads "a sequence of elementary row elementary operators" (page 19); written here as "a sequence of elementary row operations". The Note on page 20 labels the converse (⇐), but its proof is not in the photos.
> - Reduced Row-Echelon Form, example: entry $(2, 3)$ of $M_2$ is read as $-1$ (page 24).
