---
course: [LA1]
semester: "115-1"
chapter: ["4.3"]
tags: [linear-algebra, homework, solutions, determinants, matrix-inverse, linear-systems]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-11-25
questions: "[[LA1 HW 4.3 Questions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 4.3 Questions#FB 4.3.17\|FB 4.3.17]] | $\det(A) = -17$; $A^{-1} = \tfrac{1}{17}\begin{bmatrix} -1 & -4 & 4 \\ -7 & 6 & 11 \\ 5 & 3 & -3 \end{bmatrix}$ |
| [[LA1 HW 4.3 Questions#FB 4.3.21\|FB 4.3.21]] | $\begin{bmatrix} -7 & -1 & 4 \\ -3 & 2 & -8 \\ 6 & -4 & -1 \end{bmatrix}$ |
| [[LA1 HW 4.3 Questions#FB 4.3.22\|FB 4.3.22]] | $A = \tfrac{1}{3}\begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$ |
| [[LA1 HW 4.3 Questions#FB 4.3.28\|FB 4.3.28]] | $x_1 = \tfrac{1}{2}$, $x_2 = \tfrac{1}{2}$, $x_3 = -\tfrac{1}{2}$ |
| [[LA1 HW 4.3 Questions#FB 4.3.35\|FB 4.3.35]] | a. F; b. T; c. T; d. F; e. T; f. T; g. F; h. T; i. T; j. F |
| [[LA1 HW 4.3 Questions#FB 4.3.37\|FB 4.3.37]] | Proof |
| [[LA1 HW 4.3 Questions#FB 4.3.38\|FB 4.3.38]] | Proof (two cases) |
| [[LA1 HW 4.3 Questions#FB 4.3.39\|FB 4.3.39]] | Proof |
| [[LA1 HW 4.3 Questions#FIS 4.3.1\|FIS 4.3.1]] | (a) F; (b) T; (c) F; (d) T; (e) F; (f) T; (g) F; (h) F |
| [[LA1 HW 4.3 Questions#FIS 4.3.10\|FIS 4.3.10]] | Proof |
| [[LA1 HW 4.3 Questions#FIS 4.3.12\|FIS 4.3.12]] | Proof |
| [[LA1 HW 4.3 Questions#FIS 4.3.16\|FIS 4.3.16]] | Proof |
| [[LA1 HW 4.3 Questions#FIS 4.3.20\|FIS 4.3.20]] | Proof (induction on the size of $I$) |
| [[LA1 HW 4.3 Questions#FIS 4.3.21\|FIS 4.3.21]] | Proof (factor $M$ into two block matrices) |
| [[LA1 HW 4.3 Questions#FIS 4.3.22\|FIS 4.3.22]] | (a) column $j + 1$ of $M$ is $[\mathsf{T}(x^{j})]_{\gamma}$; (b) Proof; (c) Proof (induction) |

## FB §4.3 Computation of Determinants and Cramer's Rule

> [!note] Note
> The facts that the answers use.
> - **[[Cofactor|Cofactors]]**: $a'_{ij} = (-1)^{i+j}\det(A_{ij})$, where $A_{ij}$ is $A$ with row $i$ and column $j$ deleted. The signs $(-1)^{i+j}$ form a checkerboard with $+$ at $(1, 1)$. $A' = [a'_{ij}]$ is the matrix of cofactors.
> - **[[Classical Adjoint|Adjoint]]**: $\operatorname{adj}(A) = (A')^T$, so the cofactors of row $i$ of $A$ form column $i$ of $\operatorname{adj}(A)$. For every square $A$, $\operatorname{adj}(A)A = A\operatorname{adj}(A) = \det(A)\,I$.
> - $A$ is [[Invertible Matrix|invertible]] $\iff \det(A) \ne 0$, and then $A^{-1} = \dfrac{1}{\det(A)}\operatorname{adj}(A)$.
> - $2 \times 2$: $\operatorname{adj}\begin{bmatrix} a & b \\ c & d \end{bmatrix} = \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$ (swap the diagonal entries, change the sign of the other two).
> - **[[Cramer's Rule]]**: if $\det(A) \ne 0$, the unique solution of $A\mathbf{x} = \mathbf{b}$ is $x_k = \dfrac{\det(B_k)}{\det(A)}$, where $B_k$ is $A$ with column $k$ replaced by $\mathbf{b}$.
> - $\det(AB) = \det(A) \cdot \det(B)$; $\det(rI) = r^{n}$ for the $n \times n$ identity; a [[Triangular Matrix|triangular]] matrix has determinant equal to the product of its diagonal entries.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FB 4.3.17
Question: [[LA1 HW 4.3 Questions#FB 4.3.17|FB 4.3.17]]

> [!solution] Solution
> Cofactors $a'_{ij} = (-1)^{i+j}\det(A_{ij})$:
> $$
> \begin{aligned}
> a'_{11} &= +\begin{vmatrix} 1 & 1 \\ 1 & 2 \end{vmatrix} = 1, & a'_{12} &= -\begin{vmatrix} -2 & 1 \\ 3 & 2 \end{vmatrix} = 7, & a'_{13} &= +\begin{vmatrix} -2 & 1 \\ 3 & 1 \end{vmatrix} = -5, \\
> a'_{21} &= -\begin{vmatrix} 0 & 4 \\ 1 & 2 \end{vmatrix} = 4, & a'_{22} &= +\begin{vmatrix} 3 & 4 \\ 3 & 2 \end{vmatrix} = -6, & a'_{23} &= -\begin{vmatrix} 3 & 0 \\ 3 & 1 \end{vmatrix} = -3, \\
> a'_{31} &= +\begin{vmatrix} 0 & 4 \\ 1 & 1 \end{vmatrix} = -4, & a'_{32} &= -\begin{vmatrix} 3 & 4 \\ -2 & 1 \end{vmatrix} = -11, & a'_{33} &= +\begin{vmatrix} 3 & 0 \\ -2 & 1 \end{vmatrix} = 3.
> \end{aligned}
> $$
> $$
> \det(A) = 3a'_{11} + 0a'_{12} + 4a'_{13} = 3(1) + 0 + 4(-5) = -17 \ne 0 \implies A \text{ is invertible.} \qquad \text{(row 1)}
> $$
> $$
> \operatorname{adj}(A) = (A')^T = \begin{bmatrix} 1 & 4 & -4 \\ 7 & -6 & -11 \\ -5 & -3 & 3 \end{bmatrix}, \qquad A^{-1} = \frac{1}{\det(A)}\operatorname{adj}(A) = \frac{1}{17}\begin{bmatrix} -1 & -4 & 4 \\ -7 & 6 & 11 \\ 5 & 3 & -3 \end{bmatrix}.
> $$
>
> \# The cofactors of row $i$ of $A$ become column $i$ of $\operatorname{adj}(A)$: row 1 of $A'$ is $(1, 7, -5)$, which is column 1 of $\operatorname{adj}(A)$. The same cofactors of row 1 also give $\det(A)$, so no extra work is needed to check that $A$ is invertible.
>
> \# Check, $A\operatorname{adj}(A) = \det(A)\,I$: row 1 of $A$ times column 1 of $\operatorname{adj}(A)$ is $3(1) + 0(7) + 4(-5) = -17$, and row 1 of $A$ times column 2 is $3(4) + 0(-6) + 4(-3) = 0$. A row of $A$ times the cofactors of a *different* row always gives $0$.

### FB 4.3.21
Question: [[LA1 HW 4.3 Questions#FB 4.3.21|FB 4.3.21]]

> [!solution] Solution
> Let $A = \begin{bmatrix} 2 & 1 & 0 \\ 3 & 1 & 4 \\ 0 & 2 & 1 \end{bmatrix}$. Cofactors:
> $$
> \begin{aligned}
> a'_{11} &= +\begin{vmatrix} 1 & 4 \\ 2 & 1 \end{vmatrix} = -7, & a'_{12} &= -\begin{vmatrix} 3 & 4 \\ 0 & 1 \end{vmatrix} = -3, & a'_{13} &= +\begin{vmatrix} 3 & 1 \\ 0 & 2 \end{vmatrix} = 6, \\
> a'_{21} &= -\begin{vmatrix} 1 & 0 \\ 2 & 1 \end{vmatrix} = -1, & a'_{22} &= +\begin{vmatrix} 2 & 0 \\ 0 & 1 \end{vmatrix} = 2, & a'_{23} &= -\begin{vmatrix} 2 & 1 \\ 0 & 2 \end{vmatrix} = -4, \\
> a'_{31} &= +\begin{vmatrix} 1 & 0 \\ 1 & 4 \end{vmatrix} = 4, & a'_{32} &= -\begin{vmatrix} 2 & 0 \\ 3 & 4 \end{vmatrix} = -8, & a'_{33} &= +\begin{vmatrix} 2 & 1 \\ 3 & 1 \end{vmatrix} = -1.
> \end{aligned}
> $$
> $$
> \operatorname{adj}(A) = (A')^T = \begin{bmatrix} -7 & -1 & 4 \\ -3 & 2 & -8 \\ 6 & -4 & -1 \end{bmatrix}
> $$
>
> \# Check: $\det(A) = 2(-7) + 1(-3) + 0(6) = -17$ (row 1), and $A\operatorname{adj}(A) = -17I$. For example, row 1 of $A$ times column 2 of $\operatorname{adj}(A)$ is $2(-1) + 1(2) + 0(-4) = 0$.
>
> \# The most common slip is to forget the transpose, that is, to give $A'$ instead of $\operatorname{adj}(A)$.

### FB 4.3.22
Question: [[LA1 HW 4.3 Questions#FB 4.3.22|FB 4.3.22]]

> [!solution] Solution
> $$
> \begin{aligned}
> A = (A^{-1})^{-1} &= \frac{1}{\det(A^{-1})}\operatorname{adj}(A^{-1}) \\
> &= \frac{1}{3}\begin{bmatrix} d & -b \\ -c & a \end{bmatrix}
> \end{aligned}
> $$
>
> \# $A^{-1}$ is itself an invertible matrix whose inverse is $A$, so the inverse formula is applied to $A^{-1}$. Here $\det(A^{-1}) = ad - bc = 3$, and the $2 \times 2$ adjoint swaps $a$ and $d$ and changes the signs of $b$ and $c$.
>
> \# Check: $\dfrac{1}{3}\begin{bmatrix} d & -b \\ -c & a \end{bmatrix}\begin{bmatrix} a & b \\ c & d \end{bmatrix} = \dfrac{1}{3}\begin{bmatrix} ad - bc & 0 \\ 0 & ad - bc \end{bmatrix} = \dfrac{1}{3}(3I) = I$. Also $\det(A) = 1/\det(A^{-1}) = \tfrac{1}{3}$.

### FB 4.3.28
Question: [[LA1 HW 4.3 Questions#FB 4.3.28|FB 4.3.28]]

> [!solution] Solution
> $$
> A = \begin{bmatrix} 5 & -2 & 1 \\ 0 & 1 & 1 \\ 1 & 6 & -1 \end{bmatrix}, \qquad \mathbf{b} = \begin{bmatrix} 1 \\ 0 \\ 4 \end{bmatrix}
> $$
> $$
> \det(A) = 5\begin{vmatrix} 1 & 1 \\ 6 & -1 \end{vmatrix} + 1\begin{vmatrix} -2 & 1 \\ 1 & 1 \end{vmatrix} = 5(-7) + (-3) = -38 \ne 0 \qquad \text{(column 1)}
> $$
> So Cramer's rule applies. $B_k$ is $A$ with column $k$ replaced by $\mathbf{b}$:
> $$
> \begin{aligned}
> \det(B_1) &= \begin{vmatrix} 1 & -2 & 1 \\ 0 & 1 & 1 \\ 4 & 6 & -1 \end{vmatrix} = 1(-7) + 4(-3) = -19 && \text{(column 1)} \\
> \det(B_2) &= \begin{vmatrix} 5 & 1 & 1 \\ 0 & 0 & 1 \\ 1 & 4 & -1 \end{vmatrix} = -1\begin{vmatrix} 5 & 1 \\ 1 & 4 \end{vmatrix} = -19 && \text{(row 2)} \\
> \det(B_3) &= \begin{vmatrix} 5 & -2 & 1 \\ 0 & 1 & 0 \\ 1 & 6 & 4 \end{vmatrix} = +1\begin{vmatrix} 5 & 1 \\ 1 & 4 \end{vmatrix} = 19 && \text{(row 2)}
> \end{aligned}
> $$
> $$
> x_1 = \frac{-19}{-38} = \frac{1}{2}, \qquad x_2 = \frac{-19}{-38} = \frac{1}{2}, \qquad x_3 = \frac{19}{-38} = -\frac{1}{2}
> $$
>
> \# Expand along the row or column with the most zeros: column 1 of $A$ and of $B_1$ has a $0$, and row 2 of $B_2$ and of $B_3$ has only one nonzero entry. In $B_2$ that entry is in position $(2, 3)$, sign $(-1)^{2+3} = -1$; in $B_3$ it is in position $(2, 2)$, sign $+1$.
>
> \# Check in the three equations: $5(\tfrac{1}{2}) - 2(\tfrac{1}{2}) + (-\tfrac{1}{2}) = 1$, $\ \tfrac{1}{2} + (-\tfrac{1}{2}) = 0$, $\ \tfrac{1}{2} + 6(\tfrac{1}{2}) - (-\tfrac{1}{2}) = 4$.

### FB 4.3.35
Question: [[LA1 HW 4.3 Questions#FB 4.3.35|FB 4.3.35]]

> [!solution] Solution
> - a. **F.** $\det\begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix} = -1$, but the product of the diagonal entries is $0$.
> - b. **T.** Expand along column 1 again and again: only the diagonal entry of each column survives.
> - c. **T.** $\det(A) = \det(A^T)$, and $A^T$ is upper triangular with the same diagonal.
> - d. **F.** $\begin{bmatrix} -1 & 0 \\ 0 & 1 \end{bmatrix}$ is nonsingular, but its determinant is $-1 < 0$. The correct statement is "nonzero".
> - e. **T.** Columns independent $\iff \operatorname{rank}(A) = n \iff A$ invertible $\iff \det(A) \ne 0$.
> - f. **T.** $A\mathbf{x} = \mathbf{0}$ has a nontrivial solution $\iff A$ is singular $\iff \det(A) = 0$.
> - g. **F.** $A\operatorname{adj}(A) = \det(A)\,I$. $A = 2I_2$: $\operatorname{adj}(A) = 2I_2$, so $A\operatorname{adj}(A) = 4I_2 \ne I_2$.
> - h. **T.** $A\operatorname{adj}(A) = \det(A)\,I$; the scalar is $\det(A)$.
> - i. **T.** $\operatorname{adj}(A) = (A')^T \implies (\operatorname{adj}(A))^T = A'$.
> - j. **F.** It needs $n^{2}$ cofactors, each an $(n-1) \times (n-1)$ determinant; row reduction of $[A \mid I]$ is far faster.
>
> \# g, h. The product is $I$ exactly when $\det(A) = 1$. This is why the inverse formula divides by $\det(A)$.
>
> \# e, f. These are two more conditions in the list of equivalent conditions for an invertible $n \times n$ matrix, now including $\det(A) \ne 0$.

### FB 4.3.37
Question: [[LA1 HW 4.3 Questions#FB 4.3.37|FB 4.3.37]]

> [!proof] Proof
> Use $\operatorname{adj}(A)A = A\operatorname{adj}(A) = \det(A)\,I$.
>
> **(⇒)**
> $$
> \begin{aligned}
> &A \text{ invertible} \implies \det(A) \ne 0 \\
> &\implies \operatorname{adj}(A)\Big(\frac{1}{\det(A)}A\Big) = \frac{1}{\det(A)}\operatorname{adj}(A)A = \frac{1}{\det(A)}\det(A)\,I = I, \\
> &\hphantom{\implies}\ \Big(\frac{1}{\det(A)}A\Big)\operatorname{adj}(A) = \frac{1}{\det(A)}A\operatorname{adj}(A) = I \\
> &\implies \operatorname{adj}(A) \text{ is invertible, and } \operatorname{adj}(A)^{-1} = \frac{1}{\det(A)}A.
> \end{aligned}
> $$
>
> **(⇐)**
> $$
> \begin{aligned}
> &\text{Suppose } \operatorname{adj}(A) \text{ is invertible but } A \text{ is not.} \\
> &\implies \det(A) = 0 \implies A\operatorname{adj}(A) = 0 \cdot I = O \\
> &\implies A = A\operatorname{adj}(A)\operatorname{adj}(A)^{-1} = O\operatorname{adj}(A)^{-1} = O \\
> &\implies \text{every cofactor of } O \text{ is } \pm\det(\text{an } (n-1) \times (n-1) \text{ zero matrix}) = 0 \qquad (n \ge 2) \\
> &\implies \operatorname{adj}(A) = O, \text{ which is not invertible.} \quad (\to\leftarrow) \\[6pt]
> &\therefore A \text{ is invertible.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# (⇒) To show a matrix is invertible, write down a matrix that multiplies it to $I$ on both sides. The identity $\operatorname{adj}(A)A = \det(A)\,I$ almost gives $A^{-1}$ already; dividing by $\det(A) \ne 0$ finishes it.
>
> \# (⇐) The contradiction: if $\det(A) = 0$, then $A\operatorname{adj}(A) = O$, and cancelling the invertible $\operatorname{adj}(A)$ forces $A = O$. But the zero matrix has adjoint $O$, which is not invertible, against the assumption. So $\det(A) = 0$ is impossible.
>
> \# Why $n \ge 2$: a $1 \times 1$ matrix has no $(n-1) \times (n-1)$ submatrices, and with the usual convention $\operatorname{adj}([a]) = [1]$, which is invertible even for $a = 0$. FB 4.3.39 assumes $n > 1$ for the same reason.

### FB 4.3.38
Question: [[LA1 HW 4.3 Questions#FB 4.3.38|FB 4.3.38]]

> [!proof] Proof
> $$
> \begin{aligned}
> &A\operatorname{adj}(A) = \det(A)\,I \\
> &\implies \det(A)\det(\operatorname{adj}(A)) = \det\big(\det(A)\,I\big) = \det(A)^{n} \qquad (\det(rI) = r^{n}) \\[6pt]
> &\textbf{Case } \det(A) \ne 0\text{: divide by } \det(A) \implies \det(\operatorname{adj}(A)) = \det(A)^{n-1}. \\[6pt]
> &\textbf{Case } \det(A) = 0\text{: } A \text{ is not invertible} \\
> &\qquad \implies \operatorname{adj}(A) \text{ is not invertible} \qquad \text{(FB 4.3.37)} \\
> &\qquad \implies \det(\operatorname{adj}(A)) = 0 = 0^{n-1} = \det(A)^{n-1} \qquad (n \ge 2) \\[6pt]
> &\therefore \det(\operatorname{adj}(A)) = \det(A)^{n-1}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Why two cases: dividing by $\det(A)$ is allowed only when $\det(A) \ne 0$. When $\det(A) = 0$, the second line reads $0 = 0$ and says nothing about $\det(\operatorname{adj}(A))$, so FB 4.3.37 is needed.
>
> \# $\det(A)\,I$ is diagonal with $n$ diagonal entries $\det(A)$, so its determinant is $\det(A)^{n}$, not $\det(A)$.
>
> \# Check, $n = 2$: $\operatorname{adj}\begin{bmatrix} a & b \\ c & d \end{bmatrix} = \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$ has determinant $da - bc = \det(A)^{1}$.

### FB 4.3.39
Question: [[LA1 HW 4.3 Questions#FB 4.3.39|FB 4.3.39]]

> [!proof] Proof
> $$
> \begin{aligned}
> &A \text{ invertible} \implies \operatorname{adj}(A) \text{ is invertible, with } \operatorname{adj}(A)^{-1} = \frac{1}{\det(A)}A \qquad \text{(FB 4.3.37)} \\[6pt]
> &\operatorname{adj}(B)B = \det(B)\,I \text{ with } B = \operatorname{adj}(A)\text{:} \\
> &\operatorname{adj}(\operatorname{adj}(A))\operatorname{adj}(A) = \det(\operatorname{adj}(A))\,I = \det(A)^{n-1}I \qquad \text{(FB 4.3.38)} \\
> &\implies \operatorname{adj}(\operatorname{adj}(A)) = \det(A)^{n-1}\operatorname{adj}(A)^{-1} \qquad \text{(multiply by } \operatorname{adj}(A)^{-1} \text{ on the right)} \\
> &\hphantom{\implies \operatorname{adj}(\operatorname{adj}(A))} = \det(A)^{n-1} \cdot \frac{1}{\det(A)}A = (\det(A))^{n-2}A. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The identity $\operatorname{adj}(B)B = \det(B)\,I$ holds for *every* square matrix $B$, so it may be applied to $B = \operatorname{adj}(A)$. Then FB 4.3.38 replaces $\det(\operatorname{adj}(A))$, and FB 4.3.37 supplies $\operatorname{adj}(A)^{-1}$.
>
> \# Check, $n = 2$: taking the adjoint of $\begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$ gives back $\begin{bmatrix} a & b \\ c & d \end{bmatrix} = (\det(A))^{0}A$.

## FIS §4.3 Properties of Determinants

> [!note] Note
> The facts that the answers use. Notation follows FIS: $A^t$, $A_{ij}$, $\mathsf{M}_{n \times n}(F)$.
> - $\det(AB) = \det(A) \cdot \det(B)$ and $\det(A^t) = \det(A)$ for $A, B \in \mathsf{M}_{n \times n}(F)$.
> - Because $\det(A^t) = \det(A)$, what holds for rows holds for columns: cofactor expansion along any column, and adding a multiple of one column to another column does not change the [[Determinant|determinant]].
> - **Cofactor expansion along row $i$**: $\det(A) = \sum_{j=1}^{n} (-1)^{i+j}A_{ij}\det(\tilde{A}_{ij})$, where $\tilde{A}_{ij}$ is $A$ with row $i$ and column $j$ deleted.
> - The determinant is linear in each row: a common factor of one row can be taken out.
> - $A$ is invertible $\iff \det(A) \ne 0 \iff \operatorname{rank}(A) = n$.
> - For a linear transformation $\mathsf{T}\colon \mathsf{V} \to \mathsf{W}$ between spaces of the same finite dimension, with ordered bases $\beta$ and $\gamma$: $\mathsf{T}$ is invertible $\iff [\mathsf{T}]_{\beta}^{\gamma}$ is invertible.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FIS 4.3.1
Question: [[LA1 HW 4.3 Questions#FIS 4.3.1|FIS 4.3.1]]

> [!solution] Solution
> - (a) **F.** $E = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}$ (row 1 of $I$ multiplied by $2$) has $\det(E) = 2$.
> - (b) **T.** The multiplicative property.
> - (c) **F.** Invertible $\iff \det(M) \ne 0$. $M = I$ is invertible, but $\det(I) = 1 \ne 0$.
> - (d) **T.** $\operatorname{rank}(M) = n \iff M$ invertible $\iff \det(M) \ne 0$.
> - (e) **F.** $\det(A^t) = \det(A)$. $A = I$ in $\mathsf{M}_{2 \times 2}(R)$: $\det(I^t) = 1 \ne -1$.
> - (f) **T.** Expansion along column $j$ of $A$ is expansion along row $j$ of $A^t$, and $\det(A^t) = \det(A)$.
> - (g) **F.** Cramer's rule needs $\det(A) \ne 0$. The system $x_1 + x_2 = 1$, $x_1 + x_2 = 2$ has $\det\begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix} = 0$ and no solution at all.
> - (h) **F.** Column $k$ must be replaced by $b$, not row $k$ by $b^t$. $A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$, $b = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$: the solution is $x = \begin{pmatrix} -1 \\ 1 \end{pmatrix}$, but $M_1 = \begin{pmatrix} 0 & 1 \\ 0 & 1 \end{pmatrix}$ gives $\dfrac{\det(M_1)}{\det(A)} = \dfrac{0}{1} = 0 \ne -1$.
>
> \# (h) With column 1 replaced by $b$: $\det\begin{pmatrix} 0 & 1 \\ 1 & 1 \end{pmatrix} = -1$, so $x_1 = \tfrac{-1}{1} = -1$, which is correct. Column $k$ holds the coefficients of $x_k$, which is why $b$ goes into column $k$.
>
> \# (a) The three types of elementary matrices have determinants $-1$ (two rows interchanged), $c$ (a row multiplied by $c \ne 0$), and $1$ (a multiple of a row added to another). Only types 1 and 3 give $\pm 1$.

### FIS 4.3.10
Question: [[LA1 HW 4.3 Questions#FIS 4.3.10|FIS 4.3.10]]

> [!proof] Proof
> $$
> \begin{aligned}
> M^k = O &\implies [\det(M)]^{k} = \det(M^k) = \det(O) = 0 \\
> &\implies \det(M) = 0. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $\det(M^k) = \det(M)^{k}$ is the multiplicative property used $k - 1$ times. $\det(O) = 0$ because $O$ has a row of zeros. In the last step, $\det(M)$ is a complex number whose $k$th power is $0$; a product of nonzero complex numbers is never $0$, so $\det(M) = 0$.
>
> \# Example: $M = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}$ has $M^2 = O$ and $\det(M) = 0$. The converse is false: $\begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$ has determinant $0$, but all its powers equal itself, never $O$.

### FIS 4.3.12
Question: [[LA1 HW 4.3 Questions#FIS 4.3.12|FIS 4.3.12]]

> [!proof] Proof
> $$
> \begin{aligned}
> QQ^t = I &\implies \det(Q)\det(Q^t) = \det(QQ^t) = \det(I) = 1 \\
> &\implies [\det(Q)]^{2} = 1 \qquad (\det(Q^t) = \det(Q)) \\
> &\implies \det(Q) = \pm 1 \qquad (\det(Q) \in R). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The entries of $Q$ are real, so $\det(Q)$ is a real number, and the only real numbers with square $1$ are $1$ and $-1$. For a complex matrix the conclusion becomes $\lvert \det(Q) \rvert = 1$ (FIS 4.3.13).
>
> \# Both signs occur: the rotation $\begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}$ has determinant $1$, and the reflection $\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$ has determinant $-1$.

### FIS 4.3.16
Question: [[LA1 HW 4.3 Questions#FIS 4.3.16|FIS 4.3.16]]

> [!proof] Proof
> $$
> \begin{aligned}
> AB = I &\implies \det(A)\det(B) = \det(AB) = \det(I) = 1 \\
> &\implies \det(A) \ne 0 \\
> &\implies A \text{ is invertible.} \\[6pt]
> B = IB = (A^{-1}A)B &= A^{-1}(AB) = A^{-1}I = A^{-1}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Why $\det(A) \ne 0$: if $\det(A) = 0$, then $\det(A)\det(B) = 0 \cdot \det(B) = 0$, which contradicts $\det(A)\det(B) = 1$.
>
> \# The matrices must be square: $A = \begin{pmatrix} 1 & 0 \end{pmatrix}$ and $B = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$ give $AB = (1) = I_1$, but $A$ is not invertible. Determinants are defined only for square matrices, so the proof uses that $A, B \in \mathsf{M}_{n \times n}(F)$.

### FIS 4.3.20
Question: [[LA1 HW 4.3 Questions#FIS 4.3.20|FIS 4.3.20]]

> [!proof] Proof
> Let $A$ be $k \times k$ and $I = I_r$ be $r \times r$, so that $k + r = n$. Induction on $r$.
> $$
> \begin{aligned}
> &r = 1\text{: } M = \begin{pmatrix} A & b \\ 0 \cdots 0 & 1 \end{pmatrix}, \text{ and row } n \text{ of } M \text{ is } (0, \dots, 0, 1). \\
> &\qquad \text{Expand along row } n\text{: } \det(M) = (-1)^{n+n} \cdot 1 \cdot \det(\tilde{M}_{nn}) = \det(A). \\[6pt]
> &r \ge 2\text{: assume the result for } I_{r-1}. \text{ Row } n \text{ of } M \text{ is again } (0, \dots, 0, 1). \\
> &\qquad \det(M) = (-1)^{n+n} \cdot 1 \cdot \det(\tilde{M}_{nn}), \qquad \tilde{M}_{nn} = \begin{pmatrix} A & B' \\ O & I_{r-1} \end{pmatrix} \quad (B' = B \text{ without its last column}) \\
> &\qquad \phantom{\det(M)} = \det(A). \qquad \text{(induction hypothesis)} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $\tilde{M}_{nn}$ is $M$ with row $n$ and column $n$ deleted. Only the $(n, n)$-entry of row $n$ is nonzero, so only one term of the expansion is left, with sign $(-1)^{2n} = +1$. Deleting the last row and column removes the last row and column of $I$ and the last column of $B$; what is left has the same shape with $I_{r-1}$, which is why induction works.
>
> \# Example, $k = 1$, $r = 2$: $\det\begin{pmatrix} a & b_1 & b_2 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} = a$. The entries of $B$ never matter.

### FIS 4.3.21
Question: [[LA1 HW 4.3 Questions#FIS 4.3.21|FIS 4.3.21]]

> [!proof] Proof
> Let $A$ be $k \times k$ and $C$ be $r \times r$. Multiply in blocks:
> $$
> \begin{pmatrix} I_k & O \\ O & C \end{pmatrix}\begin{pmatrix} A & B \\ O & I_r \end{pmatrix} = \begin{pmatrix} I_kA + O\,O & I_kB + O\,I_r \\ O\,A + C\,O & O\,B + C\,I_r \end{pmatrix} = \begin{pmatrix} A & B \\ O & C \end{pmatrix} = M.
> $$
> $$
> \begin{aligned}
> \det(M) &= \det\begin{pmatrix} I_k & O \\ O & C \end{pmatrix} \cdot \det\begin{pmatrix} A & B \\ O & I_r \end{pmatrix} && (\det(XY) = \det(X)\det(Y)) \\
> &= \det(C) \cdot \det(A) && \text{(see below; FIS 4.3.20)} \\
> &= \det(A) \cdot \det(C). \qquad \blacksquare
> \end{aligned}
> $$
> First factor: row 1 of $\begin{pmatrix} I_k & O \\ O & C \end{pmatrix}$ is $(1, 0, \dots, 0)$. Expanding along row 1 gives $(+1) \cdot 1 \cdot \det\begin{pmatrix} I_{k-1} & O \\ O & C \end{pmatrix}$; after $k$ such steps (induction on $k$, as in FIS 4.3.20) only $\det(C)$ is left.
>
> \# The idea is to split $M$ into two block matrices of the kind FIS 4.3.20 handles, one with $A$ alone and one with $C$ alone, and then use the multiplicative property. The block sizes fit: $I_k$ and $A$ are $k \times k$, $C$ and $I_r$ are $r \times r$, $B$ is $k \times r$.
>
> \# Example: $\det\begin{pmatrix} 1 & 2 & 5 \\ 3 & 4 & 6 \\ 0 & 0 & 7 \end{pmatrix} = \det\begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} \cdot 7 = (-2)(7) = -14$.

### FIS 4.3.22
Question: [[LA1 HW 4.3 Questions#FIS 4.3.22|FIS 4.3.22]]

> [!note] Note
> Exercise 22 of FIS §2.4 proves that $\mathsf{T}$ is an isomorphism. Reason: if $\mathsf{T}(f) = 0$, then $f$ has the $n + 1$ distinct roots $c_0, \dots, c_n$ but degree at most $n$, so $f = 0$; thus $\mathsf{N}(\mathsf{T}) = \{0\}$, and $\dim \mathsf{P}_{n}(F) = n + 1 = \dim \mathsf{F}^{n+1}$ makes $\mathsf{T}$ onto as well.

> [!proof] Proof of (a)
> $\beta = \{1, x, x^2, \dots, x^n\}$ and $\gamma = \{e_1, e_2, \dots, e_{n+1}\}$. For $j = 0, 1, \dots, n$:
> $$
> \mathsf{T}(x^{j}) = (c_0^{j}, c_1^{j}, \dots, c_n^{j}) = c_0^{j}e_1 + c_1^{j}e_2 + \cdots + c_n^{j}e_{n+1} \implies [\mathsf{T}(x^{j})]_{\gamma} = \begin{pmatrix} c_0^{j} \\ c_1^{j} \\ \vdots \\ c_n^{j} \end{pmatrix}
> $$
> Column $j + 1$ of $M = [\mathsf{T}]_{\beta}^{\gamma}$ is $[\mathsf{T}(x^{j})]_{\gamma}$, so the $(i + 1, j + 1)$-entry of $M$ is $c_i^{j}$ for $0 \le i, j \le n$. This is the Vandermonde matrix: column 1 comes from $\mathsf{T}(1) = (1, 1, \dots, 1)$, column 2 from $\mathsf{T}(x) = (c_0, \dots, c_n)$, and so on. $\blacksquare$
>
> \# Row $i + 1$ of $M$ is $(1, c_i, c_i^2, \dots, c_i^n)$: the basis polynomials evaluated at $c_i$.

> [!proof] Proof of (b)
> $$
> \begin{aligned}
> &\mathsf{T} \text{ is an isomorphism, so invertible} \qquad \text{(Exercise 22 of Section 2.4)} \\
> &\implies M = [\mathsf{T}]_{\beta}^{\gamma} \text{ is invertible} \qquad (\mathsf{T} \text{ invertible} \iff [\mathsf{T}]_{\beta}^{\gamma} \text{ invertible}) \\
> &\implies \det(M) \ne 0. \qquad \blacksquare
> \end{aligned}
> $$

> [!proof] Proof of (c)
> For scalars $d_0, d_1, \dots, d_m$ ($m \ge 1$) let $V(d_0, \dots, d_m)$ be the determinant of the Vandermonde matrix whose rows are $(1, d_i, d_i^2, \dots, d_i^m)$. We prove $V(d_0, \dots, d_m) = \prod_{0 \le i < j \le m} (d_j - d_i)$ by induction on $m$.
> $$
> m = 1\text{: } V(d_0, d_1) = \begin{vmatrix} 1 & d_0 \\ 1 & d_1 \end{vmatrix} = d_1 - d_0.
> $$
> $m \ge 2$: assume the formula for $m$ scalars. Do the column operations column $(j + 1) \leftarrow$ column $(j + 1) - d_0 \cdot$ column $j$ for $j = m, m - 1, \dots, 1$, from right to left. They do not change the determinant, and $d_i^{j} - d_0d_i^{j-1} = d_i^{j-1}(d_i - d_0)$:
> $$
> \begin{aligned}
> V(d_0, \dots, d_m) &= \begin{vmatrix} 1 & 0 & 0 & \cdots & 0 \\ 1 & d_1 - d_0 & d_1(d_1 - d_0) & \cdots & d_1^{m-1}(d_1 - d_0) \\ \vdots & \vdots & \vdots & & \vdots \\ 1 & d_m - d_0 & d_m(d_m - d_0) & \cdots & d_m^{m-1}(d_m - d_0) \end{vmatrix} \\
> &= \begin{vmatrix} d_1 - d_0 & d_1(d_1 - d_0) & \cdots & d_1^{m-1}(d_1 - d_0) \\ \vdots & \vdots & & \vdots \\ d_m - d_0 & d_m(d_m - d_0) & \cdots & d_m^{m-1}(d_m - d_0) \end{vmatrix} && \text{(expand along row 1)} \\
> &= (d_1 - d_0)(d_2 - d_0)\cdots(d_m - d_0)\begin{vmatrix} 1 & d_1 & \cdots & d_1^{m-1} \\ \vdots & \vdots & & \vdots \\ 1 & d_m & \cdots & d_m^{m-1} \end{vmatrix} && \text{(take } d_i - d_0 \text{ out of the row of } d_i\text{)} \\
> &= \prod_{j=1}^{m} (d_j - d_0) \cdot \prod_{1 \le i < j \le m} (d_j - d_i) && \text{(induction hypothesis)} \\
> &= \prod_{0 \le i < j \le m} (d_j - d_i).
> \end{aligned}
> $$
> With $m = n$ and $d_i = c_i$: $\det(M) = \prod_{0 \le i < j \le n} (c_j - c_i)$. $\blacksquare$
>
> \# Why right to left: each step uses column $j$ while it still holds the original powers $d_i^{j-1}$. Row 1 becomes $(1, 0, \dots, 0)$ because $d_0^{j} - d_0 \cdot d_0^{j-1} = 0$, so the expansion along row 1 has only one term.
>
> \# The last step joins the factors with $i = 0$ to those with $1 \le i < j$; together they are all pairs $0 \le i < j \le m$. Example, $n = 2$: $\det(M) = (c_1 - c_0)(c_2 - c_0)(c_2 - c_1)$.
>
> \# (c) does not need the $c_i$ to be distinct. When they are distinct, every factor $c_j - c_i$ is nonzero, so $\det(M) \ne 0$: a second proof of (b).
