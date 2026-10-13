---
course: [LA1]
chapter: ["1.4", "1.5"]
tags: [linear-algebra, quiz, matrix-inverse]
source:
  - "LA1 Quiz #4 [1134] (115-1), graded scan"
  - "[[LA1 Quiz 04 p1.jpg]]"
created: 2026-10-13
score: "10/10"
---
> [!abstract] Result: 10/10
> - Q1 True or False: 5/5. Properties of [[Invertible Matrix|inverses]] and [[Elementary Matrix|elementary matrices]].
> - Q2 Elementary Matrix: 5/5. One [[Elementary Row Operation|row operation]], applied to $I$.
> - From the homework: Q1 is [[LA1 HW 1.4 1.5 Questions#FB 1.5.23|FB 1.5.23]] i, a, j, e, g; Q2 is [[LA1 HW 1.4 1.5 Questions#FB 1.4.42|FB 1.4.42]] with another right-hand side.

> [!note] Notation
> As in lecture: $r_{ij}(A)$ swaps rows $i$ and $j$, $r_{i}^{s}(A)$ multiplies row $i$ by $s \ne 0$, and $r_{ij}^{s}(A)$ adds $s$ times row $i$ to row $j$. The row-elementary matrices are $R_{ij} = r_{ij}(I)$, $R_{i}^{s} = r_{i}^{s}(I)$, $R_{ij}^{s} = r_{ij}^{s}(I)$; a superscript is the scalar, not a power. $\overset{R_{12}^{2}}{\sim}$ names the operation of that step.

## Q1 True or False

> [!question]
> (5 pts.) Make each of the following True or False.
> - (a) If $A$ and $B$ are invertible matrices, then so is $A+B$, and $(A+B)^{-1} = A^{-1} + B^{-1}$.
> - (b) If $AC = BC$ and $C$ is invertible, then $A = B$.
> - (c) If $A$ and $B$ are invertible, then so is $AB$, and $(AB)^{-1} = A^{-1}B^{-1}$.
> - (d) If $A^2$ is invertible, then $A^3$ is invertible.
> - (e) Every elementary matris is invertible.

> [!attempt] My answer: 5/5
> - (a) F
> - (b) T
> - (c) F
> - (d) T
> - (e) T

> [!solution]- Solution
> **(a) F.** $A = I$, $B = -I$ are invertible, but $A + B = O$, and $OX = O \ne I$ for every $X$, so $A + B$ is not invertible.
>
> **(b) T.** $C^{-1}$ exists, so
> $$
> AC = BC \implies (AC)C^{-1} = (BC)C^{-1} \implies A(CC^{-1}) = B(CC^{-1}) \implies AI = BI \implies A = B.
> $$
>
> **(c) F.** $A = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}$, $B = \begin{bmatrix} 1 & 0 \\ 1 & 1 \end{bmatrix}$ are invertible, with $A^{-1} = \begin{bmatrix} 1 & -1 \\ 0 & 1 \end{bmatrix}$, $B^{-1} = \begin{bmatrix} 1 & 0 \\ -1 & 1 \end{bmatrix}$. Then
> $$
> \begin{aligned}
> (AB)^{-1} &= B^{-1}A^{-1} = \begin{bmatrix} 1 & -1 \\ -1 & 2 \end{bmatrix}, \\
> A^{-1}B^{-1} &= \begin{bmatrix} 2 & -1 \\ -1 & 1 \end{bmatrix},
> \end{aligned}
> $$
> and the $(1, 1)$-entries differ ($1 \ne 2$), so $(AB)^{-1} \ne A^{-1}B^{-1}$.
>
> \# The first half is true: $AB$ is invertible. Only the order is wrong: $(AB)^{-1} = B^{-1}A^{-1}$, and the order matters because $A^{-1}B^{-1} \ne B^{-1}A^{-1}$ in general.
>
> **(d) T.** $A^2$ is defined, so $A$ is square. Let $X = (A^2)^{-1}$, so $A^2X = XA^2 = I$. Then
> $$
> \begin{aligned}
> A^3(XAX) &= A(A^2X)AX = A\,AX = A^2X = I, \\
> (XAX)A^3 &= XA(XA^2)A = XA\,A = XA^2 = I.
> \end{aligned}
> $$
> $\therefore$ $A^3$ is invertible, and $(A^3)^{-1} = XAX = (A^2)^{-1}A(A^2)^{-1}$.
>
> \# Split $A^3 = A \cdot A^2 = A^2 \cdot A$ so that $A^2$ always meets an $X$ and becomes $I$. The homework route is longer: $A^2$ invertible $\implies$ $A$ invertible ([[LA1 HW 1.4 1.5 Questions#FB 1.5.26|FB 1.5.26]]) $\implies$ $A^3 = AAA$ invertible.
>
> **(e) T.** Multiplying by a row-elementary matrix on the left performs its row operation, and each row operation is undone by one of the same type:
> $$
> \begin{aligned}
> R_{ij}R_{ij} &= r_{ij}\big(r_{ij}(I)\big) = I, \\
> R_{i}^{s}R_{i}^{1/s} &= r_{i}^{s}\big(r_{i}^{1/s}(I)\big) = I = R_{i}^{1/s}R_{i}^{s} \qquad (s \ne 0), \\
> R_{ij}^{s}R_{ij}^{-s} &= r_{ij}^{s}\big(r_{ij}^{-s}(I)\big) = I = R_{ij}^{-s}R_{ij}^{s}.
> \end{aligned}
> $$
> $\therefore$ every elementary matrix is invertible, and its inverse is again elementary: $(R_{ij})^{-1} = R_{ij}$, $(R_{i}^{s})^{-1} = R_{i}^{1/s}$, $(R_{ij}^{s})^{-1} = R_{ij}^{-s}$.

## Q2 Elementary Matrix

> [!question]
> (5 pts.) Find an elementary matrix $E$ such that
> $$
> E\begin{bmatrix} 1 & 3 & 1 & 4 \\ 0 & 1 & 2 & 1 \\ 3 & 4 & 5 & 1 \end{bmatrix} = \begin{bmatrix} 1 & 3 & 1 & 4 \\ 2 & 7 & 4 & 9 \\ 3 & 4 & 5 & 1 \end{bmatrix}.
> $$

> [!attempt] My answer: 5/5
> $$
> \because \begin{bmatrix} 1 & 3 & 1 & 4 \\ 0 & 1 & 2 & 1 \\ 3 & 4 & 5 & 1 \end{bmatrix} \overset{R_{12}^{2}}{\sim} \begin{bmatrix} 1 & 3 & 1 & 4 \\ 2 & 7 & 4 & 9 \\ 3 & 4 & 5 & 1 \end{bmatrix}
> $$
> $$
> \begin{aligned}
> \therefore\ E &= r_{12}^{2}(I) \\
> &= \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}
> \end{aligned}
> $$

> [!solution]- Solution
> Rows 1 and 3 are unchanged, and row 2 becomes
> $$
> \begin{bmatrix} 2 & 7 & 4 & 9 \end{bmatrix} = \begin{bmatrix} 0 & 1 & 2 & 1 \end{bmatrix} + 2\begin{bmatrix} 1 & 3 & 1 & 4 \end{bmatrix} \quad (\text{row } 2 + 2 \times \text{row } 1).
> $$
> $$
> \because \begin{bmatrix} 1 & 3 & 1 & 4 \\ 0 & 1 & 2 & 1 \\ 3 & 4 & 5 & 1 \end{bmatrix} \overset{R_{12}^{2}}{\sim} \begin{bmatrix} 1 & 3 & 1 & 4 \\ 2 & 7 & 4 & 9 \\ 3 & 4 & 5 & 1 \end{bmatrix}
> $$
> $$
> \therefore\ E = R_{12}^{2} = r_{12}^{2}(I) = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}.
> $$
>
> \# A row operation on a matrix $M$ is the same as multiplying $M$ on the left by the matrix that the operation makes from $I$: $r(M) = r(I)\,M$. So find the row operation first, then apply it to $I$.
