---
course: [LA1]
semester: "115-1"
chapter: ["4.2"]
tags: [linear-algebra, homework, solutions, determinants, matrix-inverse]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-11-24
questions: "[[LA1 HW 4.2(2) Questions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 4.2(2) Questions#FB 4.2.21\|FB 4.2.21]] | a. F; b. T; c. T; d. F; e. T; f. T; g. F; h. T; i. F; j. T |
| [[LA1 HW 4.2(2) Questions#FB 4.2.26\|FB 4.2.26]] | $\lambda = 4$ or $\lambda = -1$ |
| [[LA1 HW 4.2(2) Questions#FB 4.2.29\|FB 4.2.29]] | $\lambda = 1$, $6$, or $-2$ |
| [[LA1 HW 4.2(2) Questions#FB 4.2.30\|FB 4.2.30]] | Proof (by contradiction) |
| [[LA1 HW 4.2(2) Questions#FB 4.2.31\|FB 4.2.31]] | Proof |
| [[LA1 HW 4.2(2) Questions#FB 4.2.32\|FB 4.2.32]] | Proof |
| [[LA1 HW 4.2(2) Questions#FB 4.2.33\|FB 4.2.33]] | Proof |
| [[LA1 HW 4.2(2) Questions#FIS 4.2.25\|FIS 4.2.25]] | Proof |
| [[LA1 HW 4.2(2) Questions#FIS 4.2.26\|FIS 4.2.26]] | $n$ even, or $\det(A) = 0$ |
| [[LA1 HW 4.2(2) Questions#FIS 4.2.27\|FIS 4.2.27]] | Proof |
| [[LA1 HW 4.2(2) Questions#FIS 4.2.29\|FIS 4.2.29]] | Proof (three types) |

## FB §4.2 The Determinant of a Square Matrix

> [!note] Note
> The facts that the answers use.
> - **[[Determinant]] and row operations**: interchanging two rows changes the sign; multiplying one row by a scalar $r$ multiplies the determinant by $r$; adding a multiple of one row to another row does not change it. The same holds for columns, because $\det(A^T) = \det(A)$ and the columns of $A$ are the rows of $A^T$.
> - **Expansion by minors** may be done along any row or any column.
> - A [[Triangular Matrix|triangular]] matrix, in particular a [[Diagonal Matrix|diagonal]] one, has $\det =$ the product of its diagonal entries; $\det(I) = 1$.
> - $A$ is [[Invertible Matrix|invertible]] $\iff \det(A) \ne 0$. So $A$ is singular $\iff \det(A) = 0$.
> - **Multiplicative property** (Theorem 4.4): $\det(AB) = \det(A) \cdot \det(B)$. FB 4.2.30 and FB 4.2.33 must not use it.
> - For $n \times n$ matrices, $AD = I \implies DA = I$: a one-sided inverse of a square matrix is already its inverse.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FB 4.2.21
Question: [[LA1 HW 4.2(2) Questions#FB 4.2.21|FB 4.2.21]]

> [!solution] Solution
> - a. **F.** Only square matrices have a determinant; $\begin{bmatrix} 1 & 2 \end{bmatrix}$ has none.
> - b. **T.** Every $n \times n$ matrix has a determinant, defined by expansion by minors on the first row.
> - c. **T.** $\det(A)$ is a number (a sum of products of entries), not a matrix.
> - d. **F.** $A = I_2$, $c = 2$: $\det(2I_2) = \det\begin{bmatrix} 2 & 0 \\ 0 & 2 \end{bmatrix} = 4 \ne 2 = 2\det(I_2)$.
> - e. **T.** $cA$ multiplies each of the $n$ rows by $c$, one factor $c$ per row: $\det(cA) = c^{n}\det(A)$.
> - f. **T.** $\det(AA^T) = \det(A)\det(A^T) = \det(A)\det(A) = [\det(A)]^2$, and in the same way $\det(A^TA) = \det(A^T)\det(A) = [\det(A)]^2$.
> - g. **F.** Each interchange multiplies the determinant by $-1$, so two of them give $(-1)(-1) = 1$. $A = I_2$: interchanging the rows and then the columns gives $I_2$ back, and $\det(I_2) = 1 \ne -1$.
> - h. **T.** $\det(E) = -1$ (two rows interchanged), $r$ with $r \ne 0$ (a row multiplied by $r$), or $1$ (a multiple of a row added to another row): never $0$.
> - i. **F.** $A = \begin{bmatrix} 2 & 0 \\ 0 & 1 \end{bmatrix}$, $B = \begin{bmatrix} 3 & 0 \\ 0 & 1 \end{bmatrix}$: $\det(A + B) = \det\begin{bmatrix} 5 & 0 \\ 0 & 2 \end{bmatrix} = 10 \ne 5$.
> - j. **T.** $\det(AB) = \det(A)\det(B) = 2 \cdot 3 = 6$.
>
> \# d, e. Multiplying the *matrix* by $c$ multiplies *every* row by $c$, and each row gives its own factor $c$; so the factor is $c^{n}$. d forgets the $n$: it holds only in special cases (for example $n = 1$), so as a statement about every matrix it is false.
>
> \# g. Interchanging two columns acts on the determinant like interchanging two rows, because the columns of $A$ are the rows of $A^T$ and $\det(A^T) = \det(A)$. One row interchange and one column interchange are two sign changes, which cancel.
>
> \# h. An elementary matrix is $I$ after one row operation. Starting from $\det(I) = 1$, the operation multiplies the determinant by $-1$, by $r \ne 0$, or by $1$. Another way to see it: every elementary matrix is invertible.
>
> \# i, j. The determinant does not split over a sum, $\det(A + B) \ne \det(A) + \det(B)$ in general, but it does split over a product (j).

### FB 4.2.26
Question: [[LA1 HW 4.2(2) Questions#FB 4.2.26|FB 4.2.26]]

> [!solution] Solution
> $$
> \begin{aligned}
> \begin{vmatrix} 1 - \lambda & 2 \\ 3 & 2 - \lambda \end{vmatrix} &= (1 - \lambda)(2 - \lambda) - 2 \cdot 3 \\
> &= \lambda^{2} - 3\lambda + 2 - 6 = \lambda^{2} - 3\lambda - 4 = (\lambda - 4)(\lambda + 1)
> \end{aligned}
> $$
> Singular $\iff \det = 0 \iff \lambda = 4$ or $\lambda = -1$.
>
> \# Check. $\lambda = 4$: $\begin{bmatrix} -3 & 2 \\ 3 & -2 \end{bmatrix}$, row 2 $= -$row 1. $\lambda = -1$: $\begin{bmatrix} 2 & 2 \\ 3 & 3 \end{bmatrix}$, row 2 $= \tfrac{3}{2}$ row 1. Both have determinant $0$.

### FB 4.2.29
Question: [[LA1 HW 4.2(2) Questions#FB 4.2.29|FB 4.2.29]]

> [!solution] Solution
> $$
> \begin{aligned}
> \begin{vmatrix} 1 - \lambda & 0 & 2 \\ 0 & 4 - \lambda & 3 \\ 0 & 4 & -\lambda \end{vmatrix} &= (1 - \lambda)\begin{vmatrix} 4 - \lambda & 3 \\ 4 & -\lambda \end{vmatrix} && \text{(expand along column 1)} \\
> &= (1 - \lambda)\big[(4 - \lambda)(-\lambda) - 12\big] \\
> &= (1 - \lambda)(\lambda^{2} - 4\lambda - 12) = (1 - \lambda)(\lambda - 6)(\lambda + 2)
> \end{aligned}
> $$
> Singular $\iff \det = 0 \iff \lambda = 1$, $6$, or $-2$.
>
> \# Column 1 has two zeros, so only the $(1, 1)$-term survives, with sign $+$. Check $\lambda = 1$: column 1 becomes all zeros, so the determinant is $0$ at once.

### FB 4.2.30
Question: [[LA1 HW 4.2(2) Questions#FB 4.2.30|FB 4.2.30]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Suppose } AB \text{ is invertible, and let } D = (AB)^{-1}. \\
> &\implies (AB)D = I \implies A(BD) = I \qquad \text{(associativity)} \\
> &\because A \text{ and } BD \text{ are } n \times n \text{ and } A(BD) = I, \\
> &\therefore (BD)A = I \text{ too, so } A \text{ is invertible with } A^{-1} = BD. \quad (\to\leftarrow\ A \text{ is singular}) \\[6pt]
> &\therefore AB \text{ is singular.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The key step is $A(BD) = I \implies (BD)A = I$. It needs $A$ and $BD$ to be square: for square matrices a one-sided inverse is already the inverse (FB §1.5). Then $BD$ is an inverse of $A$, which is impossible because $A$ is singular. So the assumption "$AB$ invertible" was wrong.
>
> \# Why "without Theorem 4.4": with it, the proof is one line ($\det(AB) = \det(A)\det(B) = 0 \cdot \det(B) = 0$). The exercise is one step toward proving Theorem 4.4 itself: when $A$ is singular, $AB$ is singular, so $\det(AB) = 0 = \det(A)\det(B)$.

### FB 4.2.31
Question: [[LA1 HW 4.2(2) Questions#FB 4.2.31|FB 4.2.31]]

> [!proof] Proof
> $$
> \begin{aligned}
> &AA^{-1} = I \\
> &\implies \det(A)\det(A^{-1}) = \det(AA^{-1}) = \det(I) = 1 \\
> &\implies \det(A) \ne 0 \text{ and } \det(A^{-1}) = \dfrac{1}{\det(A)}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $\det(I) = 1$ because $I$ is triangular with $1$'s on the diagonal. Dividing by $\det(A)$ is allowed because the product $\det(A)\det(A^{-1})$ equals $1$: if $\det(A)$ were $0$, the product would be $0 \ne 1$.

### FB 4.2.32
Question: [[LA1 HW 4.2(2) Questions#FB 4.2.32|FB 4.2.32]]

> [!proof] Proof
> $$
> \begin{aligned}
> \det(C^{-1}AC) &= \det(C^{-1})\det(A)\det(C) && \text{(multiplicative property, twice)} \\
> &= \frac{1}{\det(C)} \cdot \det(A) \cdot \det(C) && \text{(FB 4.2.31; } \det(C) \ne 0\text{)} \\
> &= \det(A). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Matrices do not commute, so $C^{-1}AC \ne A$ in general. Their determinants are numbers, and numbers commute, so $\tfrac{1}{\det(C)}$ and $\det(C)$ cancel even though $C^{-1}$ and $C$ are not next to each other.

### FB 4.2.33
Question: [[LA1 HW 4.2(2) Questions#FB 4.2.33|FB 4.2.33]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } A: n \times n, \text{ and } B = \begin{bmatrix} b_1 & & 0 \\ & \ddots & \\ 0 & & b_n \end{bmatrix} \text{ diagonal, that is, } (B)_{kj} = 0 \text{ for } k \ne j \text{ and } (B)_{jj} = b_j. \\[6pt]
> &(AB)_{ij} = \sum_{k=1}^{n} (A)_{ik}(B)_{kj} = (A)_{ij}\,b_j \quad \forall\, i, j \qquad \text{(only } k = j \text{ is left)} \\
> &\implies \text{column } j \text{ of } AB = b_j \cdot (\text{column } j \text{ of } A), \quad j = 1, \dots, n \\[6pt]
> &\implies \det(AB) = b_1b_2\cdots b_n\det(A) \qquad \text{(take } b_j \text{ out of column } j \text{, for each } j\text{)} \\
> &\det(B) = b_1b_2\cdots b_n \qquad \text{(}B \text{ is diagonal, so triangular)} \\[6pt]
> &\implies \det(AB) = \det(A) \cdot \det(B). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Multiplying $A$ by a diagonal $B$ on the *right* scales the *columns* of $A$: column $j$ is multiplied by $b_j$. Taking a factor out of a column works like taking it out of a row, because the columns of $A$ are the rows of $A^T$ and $\det(A^T) = \det(A)$. It also works when some $b_j = 0$: then both sides are $0$.
>
> \# Small check, $n = 2$: $\begin{bmatrix} a & b \\ c & d \end{bmatrix}\begin{bmatrix} b_1 & 0 \\ 0 & b_2 \end{bmatrix} = \begin{bmatrix} b_1a & b_2b \\ b_1c & b_2d \end{bmatrix}$, whose determinant is $b_1b_2(ad - bc)$.

## FIS §4.2 Determinants of Order n

> [!note] Note
> The facts that the answers use. In FIS, $\det(A^t) = \det(A)$ and $\det(AB) = \det(A)\det(B)$ come only in §4.3, so these answers use the row facts of §4.2.
> - **Linear in each row**: when the other rows are held fixed, $\det\begin{pmatrix} \vdots \\ ku \\ \vdots \end{pmatrix} = k\det\begin{pmatrix} \vdots \\ u \\ \vdots \end{pmatrix}$.
> - Adding a multiple of one row to another row does not change the [[Determinant|determinant]]; $\det(I) = 1$.
> - $A \in \mathsf{M}_{n \times n}(F)$ is invertible $\iff \operatorname{rank}(A) = n$ ([[Rank]]); and $\operatorname{rank}(A) < n \implies \det(A) = 0$.
> - [[Elementary Matrix|Elementary matrices]]: $I$ after one elementary row operation. Type 1 interchanges two rows, type 2 multiplies a row by a nonzero scalar, type 3 adds a scalar multiple of one row to another row.
> - $Ae_j$ is column $j$ of $A$, where $e_j$ is the $j$th standard vector.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FIS 4.2.25
Question: [[LA1 HW 4.2(2) Questions#FIS 4.2.25|FIS 4.2.25]]

> [!proof] Proof
> Let $a_1, \dots, a_n$ be the rows of $A$; the rows of $kA$ are $ka_1, \dots, ka_n$. Take $k$ out of one row at a time (linear in each row):
> $$
> \det(kA) = \det\begin{pmatrix} ka_1 \\ ka_2 \\ ka_3 \\ \vdots \\ ka_n \end{pmatrix} = k\det\begin{pmatrix} a_1 \\ ka_2 \\ ka_3 \\ \vdots \\ ka_n \end{pmatrix} = k^{2}\det\begin{pmatrix} a_1 \\ a_2 \\ ka_3 \\ \vdots \\ ka_n \end{pmatrix} = \cdots = k^{n}\det\begin{pmatrix} a_1 \\ a_2 \\ a_3 \\ \vdots \\ a_n \end{pmatrix} = k^{n}\det(A). \qquad \blacksquare
> $$
>
> \# There are $n$ rows, so $k$ comes out $n$ times. The determinant is linear in *each row separately*, not in the whole matrix: $\det(kA) = k\det(A)$ is false for $n \ge 2$ (FB 4.2.21 d).

### FIS 4.2.26
Question: [[LA1 HW 4.2(2) Questions#FIS 4.2.26|FIS 4.2.26]]

> [!solution] Solution
> $$
> \det(-A) = \det\big((-1)A\big) = (-1)^{n}\det(A) \qquad \text{(FIS 4.2.25 with } k = -1\text{)}
> $$
> - $n$ even: $(-1)^{n} = 1$, so $\det(-A) = \det(A)$ for every $A$.
> - $n$ odd: $\det(-A) = -\det(A)$, so $\det(-A) = \det(A) \iff 2\det(A) = 0 \iff \det(A) = 0$ (when $2 \ne 0$ in $F$, as in $\mathbb{R}$ and $\mathbb{C}$).
>
> $\det(-A) = \det(A) \iff n$ is even or $\det(A) = 0$.
>
> \# Example with $n$ odd: $\det(-I_3) = (-1)^{3} = -1 \ne 1 = \det(I_3)$. With $n$ odd the condition $\det(A) = 0$ means that $A$ is not invertible.
>
> \# In a field where $1 + 1 = 0$ (characteristic $2$, such as $\mathbb{Z}_2$), $-1 = 1$, so $-A = A$ and $\det(-A) = \det(A)$ always holds.

### FIS 4.2.27
Question: [[LA1 HW 4.2(2) Questions#FIS 4.2.27|FIS 4.2.27]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Suppose column } j \text{ and column } k \text{ of } A \text{ are identical } (j \ne k). \text{ Let } x = e_j - e_k \ne 0. \\
> &Ax = Ae_j - Ae_k = (\text{column } j) - (\text{column } k) = 0 \\
> &\implies A \text{ is not invertible} \qquad (\text{if } A^{-1} \text{ existed, } x = A^{-1}Ax = A^{-1}0 = 0\ \to\leftarrow) \\
> &\implies \operatorname{rank}(A) < n \\
> &\implies \det(A) = 0. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $x \ne 0$ because its $j$th entry is $1$ and its $k$th entry is $-1$ ($j \ne k$). A nonzero $x$ with $Ax = 0$ cannot exist when $A$ is invertible, which is the contradiction in the third line.
>
> \# Why not simply transpose: FIS proves $\det(A^t) = \det(A)$ only in §4.3, so in §4.2 columns must be handled through invertibility and rank. Once $\det(A^t) = \det(A)$ is available (FB uses it in §4.2): $A^t$ has two identical rows, so $\det(A) = \det(A^t) = 0$.

### FIS 4.2.29
Question: [[LA1 HW 4.2(2) Questions#FIS 4.2.29|FIS 4.2.29]]

> [!proof] Proof
> Let $E$ be $n \times n$, obtained from $I$ by one elementary row operation.
> $$
> \begin{aligned}
> &\textbf{Type 1 } (\text{rows } i \text{ and } j \text{ interchanged})\text{: } E_{ij} = E_{ji} = 1,\ E_{ii} = E_{jj} = 0, \text{ other entries as in } I \\
> &\qquad \implies E^t = E \implies \det(E^t) = \det(E). \\[6pt]
> &\textbf{Type 2 } (\text{row } i \text{ multiplied by } c \ne 0)\text{: } E \text{ is diagonal} \implies E^t = E \implies \det(E^t) = \det(E). \\[6pt]
> &\textbf{Type 3 } (c \text{ times row } i \text{ added to row } j,\ i \ne j)\text{: } E = I \text{ except } E_{ji} = c \\
> &\qquad \implies E^t = I \text{ except } (E^t)_{ij} = c\text{, the type 3 matrix of } c \text{ times row } j \text{ added to row } i \\
> &\qquad \implies \det(E) = \det(I) = 1 \text{ and } \det(E^t) = \det(I) = 1 \qquad \text{(adding a multiple of a row keeps det)} \\
> &\qquad \implies \det(E^t) = \det(E). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# In each case $E^t$ is again an elementary matrix of the same type, and $\det(E) = -1$, $c$, $1$ for types 1, 2, 3. Type 3, $n = 2$: adding $c$ times row 1 to row 2 gives $E = \begin{pmatrix} 1 & 0 \\ c & 1 \end{pmatrix}$, and $E^t = \begin{pmatrix} 1 & c \\ 0 & 1 \end{pmatrix}$ adds $c$ times row 2 to row 1.
>
> \# Why the dagger: FIS uses this exercise in §4.3 to prove $\det(A^t) = \det(A)$ (an invertible $A$ is a product of elementary matrices, $A = E_m \cdots E_1$, so $A^t = E_1^t \cdots E_m^t$). The proof here therefore must not use $\det(A^t) = \det(A)$; that would be circular.
