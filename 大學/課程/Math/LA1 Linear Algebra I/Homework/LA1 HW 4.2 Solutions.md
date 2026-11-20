---
course: [LA1]
semester: "115-1"
chapter: ["4.1", "4.2"]
tags: [linear-algebra, homework, solutions, determinants]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-11-17
questions: "[[LA1 HW 4.2 Questions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 4.2 Questions#FB 4.2.17\|FB 4.2.17]] | $54$ |
| [[LA1 HW 4.2 Questions#FB 4.2.18\|FB 4.2.18]] | $16$ |
| [[LA1 HW 4.2 Questions#FIS 4.1.5\|FIS 4.1.5]] | Proof |
| [[LA1 HW 4.2 Questions#FIS 4.1.6\|FIS 4.1.6]] | Proof |
| [[LA1 HW 4.2 Questions#FIS 4.1.8\|FIS 4.1.8]] | Proof |
| [[LA1 HW 4.2 Questions#FIS 4.2.1 (a)-(f)\|FIS 4.2.1 (a)-(f)]] | (a) F; (b) T; (c) T; (d) T; (e) F; (f) F |
| [[LA1 HW 4.2 Questions#FIS 4.2.2\|FIS 4.2.2]] | $k = 27$ |
| [[LA1 HW 4.2 Questions#FIS 4.2.3\|FIS 4.2.3]] | $k = 42$ |
| [[LA1 HW 4.2 Questions#FIS 4.2.7\|FIS 4.2.7]] | $-12$ |
| [[LA1 HW 4.2 Questions#FIS 4.2.8\|FIS 4.2.8]] | $-13$ |
| [[LA1 HW 4.2 Questions#FIS 4.2.11\|FIS 4.2.11]] | $-3$ |
| [[LA1 HW 4.2 Questions#FIS 4.2.15\|FIS 4.2.15]] | $0$ |
| [[LA1 HW 4.2 Questions#FIS 4.2.16\|FIS 4.2.16]] | $36$ |
| [[LA1 HW 4.2 Questions#FIS 4.2.17\|FIS 4.2.17]] | $-49$ |

## FB §4.2 The Determinant of a Square Matrix

> [!note] Note
> The facts that the answers use.
> - **[[Determinant]] and row scaling**: if a single row of $A$ is multiplied by a scalar $r$, the determinant is multiplied by $r$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FB 4.2.17
Question: [[LA1 HW 4.2 Questions#FB 4.2.17|FB 4.2.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> &3A:\ \text{each of the } 3 \text{ rows of } A \text{ is multiplied by } 3 \\
> &\det(3A) = 3 \cdot 3 \cdot 3 \cdot \det(A) = 3^{3} \cdot 2 = 54.
> \end{aligned}
> $$
>
> \# Each row multiplied by $3$ gives one factor $3$, and $3A$ multiplies all three rows, so the factor is $3^3 = 27$, not $3$. In general $\det(rA) = r^{n}\det(A)$ for an $n \times n$ matrix $A$. The answer $\det(3A) = 3 \cdot 2 = 6$ is the usual mistake.

### FB 4.2.18
Question: [[LA1 HW 4.2 Questions#FB 4.2.18|FB 4.2.18]]

> [!solution] Solution
> $$
> \det(A + A) = \det(2A) = 2^{3}\det(A) = 8 \cdot 2 = 16.
> $$
>
> \# $A + A = 2A$ multiplies all three rows by $2$, as in FB 4.2.17. Note $\det(A + A) = 16 \ne 4 = \det(A) + \det(A)$: the determinant does not split over a sum of matrices (FIS 4.2.1 (a)).

## FIS §4.1 Determinants of Order 2

> [!note] Note
> The facts that the answers use.
> - **Determinant of order 2**: $\det(A) = A_{11}A_{22} - A_{12}A_{21}$, that is, $\det\begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc$.
> - **[[Triangular Matrix|Upper triangular]]**: $A_{ij} = 0$ whenever $i > j$ (every entry below the diagonal is $0$).
> - FIS writes matrices with parentheses and $\mathsf{M}_{2 \times 2}(F)$ for the $2 \times 2$ matrices with entries in a field $F$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FIS 4.1.5
Question: [[LA1 HW 4.2 Questions#FIS 4.1.5|FIS 4.1.5]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } A = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \in \mathsf{M}_{2 \times 2}(F). \text{ Interchanging the rows gives } B = \begin{pmatrix} c & d \\ a & b \end{pmatrix}. \\[6pt]
> &\det(B) = cb - da = -(ad - bc) = -\det(A). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The middle step uses only $cb = bc$ and $da = ad$: multiplication in $F$ is commutative. In the $A_{ij}$ notation, row 1 of $B$ is row 2 of $A$ and row 2 of $B$ is row 1 of $A$, so $\det(B) = B_{11}B_{22} - B_{12}B_{21} = A_{21}A_{12} - A_{22}A_{11}$, the two products of $\det(A)$ with the signs exchanged.

### FIS 4.1.6
Question: [[LA1 HW 4.2 Questions#FIS 4.1.6|FIS 4.1.6]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{The two columns of } A \text{ are identical: } A = \begin{pmatrix} a & a \\ b & b \end{pmatrix}. \\[6pt]
> &\det(A) = a \cdot b - a \cdot b = 0. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Column 1 $=$ column 2 means $A_{11} = A_{12} = a$ and $A_{21} = A_{22} = b$. In $\det(A) = A_{11}A_{22} - A_{12}A_{21}$ both products are then $ab$, so they cancel. Two identical rows give $0$ in the same way: $\det\begin{pmatrix} a & b \\ a & b \end{pmatrix} = ab - ba = 0$ (FIS 4.2.1 (c)).

### FIS 4.1.8
Question: [[LA1 HW 4.2 Questions#FIS 4.1.8|FIS 4.1.8]]

> [!proof] Proof
> $$
> \begin{aligned}
> &A \text{ is upper triangular} \implies A_{21} = 0, \text{ so } A = \begin{pmatrix} a & b \\ 0 & d \end{pmatrix}. \\[6pt]
> &\det(A) = ad - b \cdot 0 = ad, \text{ the product of the diagonal entries } a \text{ and } d. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# In a $2 \times 2$ matrix the only entry below the diagonal ($i > j$) is $A_{21}$. The entry $b$ above the diagonal can be anything: it is multiplied by $A_{21} = 0$ and drops out.

## FIS §4.2 Determinants of Order n

> [!note] Note
> The facts that the answers use.
> - **Cofactor expansion along row $i$**: $\det(A) = \sum_{j=1}^{n} (-1)^{i+j}A_{ij}\det(\tilde{A}_{ij})$, where $\tilde{A}_{ij}$ is $A$ with row $i$ and column $j$ deleted. It may be done along any row. The signs $(-1)^{i+j}$ form a checkerboard that starts with $+$ in the $(1, 1)$-position:
> $$
> \begin{pmatrix} + & - & + & - \\ - & + & - & + \\ + & - & + & - \\ - & + & - & + \end{pmatrix}
> $$
> - **[[Elementary Row Operation|Row operations]]**, with $B$ obtained from $A$:
>     - interchanging two rows: $\det(B) = -\det(A)$;
>     - multiplying a row by a scalar $k$: $\det(B) = k\det(A)$;
>     - adding a multiple of one row to another row: $\det(B) = \det(A)$.
> - Two identical rows $\implies \det(A) = 0$. An upper triangular matrix has $\det(A) =$ the product of its diagonal entries.
> - $R_3 \to R_3 - R_2$ means: replace row 3 by row 3 minus row 2.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FIS 4.2.1 (a)-(f)
Question: [[LA1 HW 4.2 Questions#FIS 4.2.1 (a)-(f)|FIS 4.2.1 (a)-(f)]]

> [!solution] Solution
> - (a) **F.** For $n \ge 2$: $\det(2I) = 2^{n} \ne 2 = 2\det(I)$, so $\det(cA) = c\det(A)$ fails.
> - (b) **T.** $\det(A) = \sum_{j=1}^{n} (-1)^{i+j}A_{ij}\det(\tilde{A}_{ij})$ for every row $i = 1, \dots, n$.
> - (c) **T.** $n = 2$: $\det\begin{pmatrix} a & b \\ a & b \end{pmatrix} = ab - ba = 0$. $n \ge 3$: expand along a row other than the two identical rows; every $\tilde{A}_{ij}$ still has two identical rows, so every term is $0$ (induction on $n$).
> - (d) **T.** Interchanging two rows changes the sign of the determinant; for $n = 2$ this is FIS 4.1.5.
> - (e) **F.** $A = I_{2}$, multiply row 1 by $2$: $B = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}$, $\det(B) = 2 \ne 1 = \det(A)$.
> - (f) **F.** $A = I_{2}$, add $2$ times row 1 to row 2: $B = \begin{pmatrix} 1 & 0 \\ 2 & 1 \end{pmatrix}$, $\det(B) = 1 \ne 2 = 2\det(A)$.
>
> \# (a) The determinant is linear in *each row separately* while the other rows are held fixed, not in the whole matrix; for $n = 1$, $\det(a) = a$ is linear, so the statement fails only for $n \ge 2$. (e) The correct rule is $\det(B) = k\det(A)$ when the row is multiplied by $k$. (f) Adding a multiple of one row to another row never changes the determinant: $\det(B) = \det(A)$, whatever $k$ is.

### FIS 4.2.2
Question: [[LA1 HW 4.2 Questions#FIS 4.2.2|FIS 4.2.2]]

> [!solution] Solution
> $$
> \det\begin{pmatrix} 3a_1 & 3a_2 & 3a_3 \\ 3b_1 & 3b_2 & 3b_3 \\ 3c_1 & 3c_2 & 3c_3 \end{pmatrix} = 3 \cdot 3 \cdot 3\det\begin{pmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{pmatrix} \implies k = 27.
> $$
>
> \# Take the factor $3$ out of row 1, then out of row 2, then out of row 3: one factor per row. This is FB 4.2.17 again: $\det(3A) = 3^{3}\det(A)$.

### FIS 4.2.3
Question: [[LA1 HW 4.2 Questions#FIS 4.2.3|FIS 4.2.3]]

> [!solution] Solution
> $$
> \begin{aligned}
> \det\begin{pmatrix} 2a_1 & 2a_2 & 2a_3 \\ 3b_1 + 5c_1 & 3b_2 + 5c_2 & 3b_3 + 5c_3 \\ 7c_1 & 7c_2 & 7c_3 \end{pmatrix} &= 2 \cdot 7\det\begin{pmatrix} a_1 & a_2 & a_3 \\ 3b_1 + 5c_1 & 3b_2 + 5c_2 & 3b_3 + 5c_3 \\ c_1 & c_2 & c_3 \end{pmatrix} && \text{(take } 2 \text{ out of } R_1 \text{, } 7 \text{ out of } R_3\text{)} \\
> &= 14\det\begin{pmatrix} a_1 & a_2 & a_3 \\ 3b_1 & 3b_2 & 3b_3 \\ c_1 & c_2 & c_3 \end{pmatrix} && (R_2 \to R_2 - 5R_3) \\
> &= 14 \cdot 3\det\begin{pmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{pmatrix} && \text{(take } 3 \text{ out of } R_2\text{)}
> \end{aligned}
> $$
> Hence $k = 42$.
>
> \# The $5c$ in row 2 contributes nothing: once row 3 is $c$, subtracting $5$ times row 3 from row 2 removes it without changing the determinant. Only the factors $2$, $3$, $7$ remain, and $2 \cdot 3 \cdot 7 = 42$.

### FIS 4.2.7
Question: [[LA1 HW 4.2 Questions#FIS 4.2.7|FIS 4.2.7]]

> [!solution] Solution
> Row 2 is $(-1, 0, -3)$, with signs $-, +, -$.
> $$
> \begin{aligned}
> \det(A) &= (-1)^{2+1}(-1)\det\begin{pmatrix} 1 & 2 \\ 3 & 0 \end{pmatrix} + (-1)^{2+2}(0)\det\begin{pmatrix} 0 & 2 \\ 2 & 0 \end{pmatrix} + (-1)^{2+3}(-3)\det\begin{pmatrix} 0 & 1 \\ 2 & 3 \end{pmatrix} \\
> &= (1)(0 - 6) + 0 + (3)(0 - 2) \\
> &= -6 - 6 = -12.
> \end{aligned}
> $$
>
> \# Two minus signs meet in each outer term: $(-1)^{2+1}(-1) = +1$ and $(-1)^{2+3}(-3) = +3$. Check along row 1, which is FIS 4.2.5 (the same matrix): $0 - 1(0 + 6) + 2(-3 - 0) = -12$.

### FIS 4.2.8
Question: [[LA1 HW 4.2 Questions#FIS 4.2.8|FIS 4.2.8]]

> [!solution] Solution
> Row 3 is $(-1, 3, 0)$, with signs $+, -, +$.
> $$
> \begin{aligned}
> \det(A) &= (-1)^{3+1}(-1)\det\begin{pmatrix} 0 & 2 \\ 1 & 5 \end{pmatrix} + (-1)^{3+2}(3)\det\begin{pmatrix} 1 & 2 \\ 0 & 5 \end{pmatrix} + (-1)^{3+3}(0)\det\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \\
> &= (-1)(0 - 2) - 3(5 - 0) + 0 \\
> &= 2 - 15 = -13.
> \end{aligned}
> $$
>
> \# The $0$ in the $(3, 3)$-position makes the last term vanish, so its minor need not be computed. Check along row 1, which is FIS 4.2.6 (the same matrix): $1(0 - 15) - 0 + 2(0 + 1) = -13$.

### FIS 4.2.11
Question: [[LA1 HW 4.2 Questions#FIS 4.2.11|FIS 4.2.11]]

> [!solution] Solution
> Row 4 is $(-1, 1, 2, 0)$, with signs $-, +, -, +$.
> $$
> \begin{aligned}
> \det(A) &= (-1)^{4+1}(-1)\det(\tilde{A}_{41}) + (-1)^{4+2}(1)\det(\tilde{A}_{42}) + (-1)^{4+3}(2)\det(\tilde{A}_{43}) + (-1)^{4+4}(0)\det(\tilde{A}_{44}) \\
> &= \det(\tilde{A}_{41}) + \det(\tilde{A}_{42}) - 2\det(\tilde{A}_{43}).
> \end{aligned}
> $$
> Each $3 \times 3$ determinant, expanded along its row 1:
> $$
> \begin{aligned}
> \det(\tilde{A}_{41}) &= \det\begin{pmatrix} 2 & 1 & 3 \\ 0 & -2 & 2 \\ -1 & 0 & 1 \end{pmatrix} = 2(-2 - 0) - 1(0 + 2) + 3(0 - 2) = -4 - 2 - 6 = -12 \\
> \det(\tilde{A}_{42}) &= \det\begin{pmatrix} 0 & 1 & 3 \\ 1 & -2 & 2 \\ 3 & 0 & 1 \end{pmatrix} = 0 - 1(1 - 6) + 3(0 + 6) = 5 + 18 = 23 \\
> \det(\tilde{A}_{43}) &= \det\begin{pmatrix} 0 & 2 & 3 \\ 1 & 0 & 2 \\ 3 & -1 & 1 \end{pmatrix} = 0 - 2(1 - 6) + 3(-1 - 0) = 10 - 3 = 7
> \end{aligned}
> $$
> $$
> \det(A) = -12 + 23 - 2 \cdot 7 = -3.
> $$
>
> \# $\tilde{A}_{4j}$ is $A$ without row 4 and column $j$, so each one is built from rows 1–3 of $A$. The $0$ in the $(4, 4)$-position saves one $3 \times 3$ determinant. Watch the first term: $(-1)^{5}(-1) = +1$.

### FIS 4.2.15
Question: [[LA1 HW 4.2 Questions#FIS 4.2.15|FIS 4.2.15]]

> [!solution] Solution
> $$
> \begin{aligned}
> \det\begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{pmatrix} &= \det\begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 3 & 3 & 3 \end{pmatrix} && (R_3 \to R_3 - R_2) \\
> &= \det\begin{pmatrix} 1 & 2 & 3 \\ 3 & 3 & 3 \\ 3 & 3 & 3 \end{pmatrix} && (R_2 \to R_2 - R_1) \\
> &= 0 && \text{(two identical rows)}
> \end{aligned}
> $$
>
> \# Do $R_3 \to R_3 - R_2$ first, while row 2 is still $(4, 5, 6)$. Each step adds a multiple of one row to another, so the determinant does not change. Check along row 1: $1(45 - 48) - 2(36 - 42) + 3(32 - 35) = -3 + 12 - 9 = 0$.

### FIS 4.2.16
Question: [[LA1 HW 4.2 Questions#FIS 4.2.16|FIS 4.2.16]]

> [!solution] Solution
> $$
> \begin{aligned}
> \det\begin{pmatrix} -1 & 3 & 2 \\ 4 & -8 & 1 \\ 2 & 2 & 5 \end{pmatrix} &= \det\begin{pmatrix} -1 & 3 & 2 \\ 0 & 4 & 9 \\ 0 & 8 & 9 \end{pmatrix} && (R_2 \to R_2 + 4R_1,\ R_3 \to R_3 + 2R_1) \\
> &= \det\begin{pmatrix} -1 & 3 & 2 \\ 0 & 4 & 9 \\ 0 & 0 & -9 \end{pmatrix} && (R_3 \to R_3 - 2R_2) \\
> &= (-1)(4)(-9) = 36 && \text{(upper triangular)}
> \end{aligned}
> $$
>
> \# Only row additions are used, so no sign change and no factor appear. Check along row 1: $-1(-40 - 2) - 3(20 - 2) + 2(8 + 16) = 42 - 54 + 48 = 36$.

### FIS 4.2.17
Question: [[LA1 HW 4.2 Questions#FIS 4.2.17|FIS 4.2.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> \det\begin{pmatrix} 0 & 1 & 1 \\ 1 & 2 & -5 \\ 6 & -4 & 3 \end{pmatrix} &= -\det\begin{pmatrix} 1 & 2 & -5 \\ 0 & 1 & 1 \\ 6 & -4 & 3 \end{pmatrix} && (R_1 \leftrightarrow R_2) \\
> &= -\det\begin{pmatrix} 1 & 2 & -5 \\ 0 & 1 & 1 \\ 0 & -16 & 33 \end{pmatrix} && (R_3 \to R_3 - 6R_1) \\
> &= -\det\begin{pmatrix} 1 & 2 & -5 \\ 0 & 1 & 1 \\ 0 & 0 & 49 \end{pmatrix} && (R_3 \to R_3 + 16R_2) \\
> &= -(1)(1)(49) = -49 && \text{(upper triangular)}
> \end{aligned}
> $$
>
> \# The interchange is needed because the $(1, 1)$-entry is $0$, and it costs one minus sign. Check along row 1: $0 - 1(3 + 30) + 1(-4 - 12) = -33 - 16 = -49$.
