---
course: [LA1]
semester: "115-1"
chapter: ["1.2", "1.3", "1.4", "1.5", "10.2"]
tags: [linear-algebra, exam, solutions, matrix-algebra, matrix-inverse, linear-systems]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-11-02
questions: "[[LA1 Midterm 113-1 Questions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Question | Answer |
| --- | --- |
| [[LA1 Midterm 113-1 Questions#Q1 True or False\|Q1]] | (a) F; (b) F; (c) F; (d) F; (e) F; (f) T; (g) F; (h) T; (i) F; (j) F |
| [[LA1 Midterm 113-1 Questions#Q2 Seventh Power of a Matrix\|Q2]] | $A^7 = \begin{bmatrix} 0 & 0 & 1 \\ 0 & 128 & 0 \\ -1 & 0 & 0 \end{bmatrix}$ |
| [[LA1 Midterm 113-1 Questions#Q3 Rank and Span\|Q3]] | $\operatorname{rank}(A) = 2$; no, the span is not $\mathbb{R}^4$ |
| [[LA1 Midterm 113-1 Questions#Q4 Rank Depending on t\|Q4]] | $\operatorname{rank}(A) = 1$ if $t = 0$ or $t = 1$; $3$ otherwise |
| [[LA1 Midterm 113-1 Questions#Q5 Inverse of a Skew-Symmetric Matrix\|Q5]] | Proof: $(-A^{-1})^T = A^{-1}$ |
| [[LA1 Midterm 113-1 Questions#Q6 When the Matrix Is Invertible\|Q6]] | $r \ne 0$ |
| [[LA1 Midterm 113-1 Questions#Q7 Row Equivalence, Gaussian Elimination and LU\|Q7]] | (a) Proof; (b) $x = (-1, 0, 2)$; (c) $L = \begin{bmatrix} 1 & 0 & 0 \\ 3 & 1 & 0 \\ 4 & -10 & 1 \end{bmatrix}$, $U = \begin{bmatrix} 1 & 2 & -1 \\ 0 & 1 & 5 \\ 0 & 0 & 55 \end{bmatrix}$ |
| [[LA1 Midterm 113-1 Questions#Q8 Square Invertible Implies Cube Invertible\|Q8]] | Proof: $Ax = 0 \implies A^2x = 0 \implies x = 0$ |
| [[LA1 Midterm 113-1 Questions#Q9 Perpendicular Vectors\|Q9]] | Proof: $(v - w) \cdot (v + w) = \lVert v \rVert^{2} - \lVert w \rVert^{2}$ |
| [[LA1 Midterm 113-1 Questions#Q10 Invertible Products\|Q10]] | (a) Proof: $Bx = 0 \implies x = 0$, then $A = (AB)B^{-1}$; (b) Proof: (a) twice |
| [[LA1 Midterm 113-1 Questions#Q11 Inverse by Row Reduction\|Q11]] | (a) Proof: $P[A \mid I] = [I \mid X] \implies XA = I$; (b) $A^{-1} = \begin{bmatrix} -36 & -24 & 13 \\ -19 & -13 & 7 \\ 3 & 2 & -1 \end{bmatrix}$ |
| [[LA1 Midterm 113-1 Questions#Q12 Inverse of a Block Lower Triangular Matrix\|Q12]] | $X^{-1} = \begin{bmatrix} A^{-1} & O \\ -C^{-1}BA^{-1} & C^{-1} \end{bmatrix}$ |
| [[LA1 Midterm 113-1 Questions#Q13 A System with a Parameter\|Q13]] | (a) $k = 3$; (b) $k \ne 1, 3$; (c) $k = 1$ |
| [[LA1 Midterm 113-1 Questions#Q14 Trace of a Similar Matrix\|Q14]] | True: $\operatorname{tr}(P^{-1}AP) = \operatorname{tr}(APP^{-1}) = \operatorname{tr}(A)$ |
| [[LA1 Midterm 113-1 Questions#Q15 Consistency of a System\|Q15]] | $b_2 = 3b_1$ |

> [!note] Note
> The facts that the answers use.
> - **[[Invertible Matrix|Invertible]]**: $A$ is $n \times n$ and $\exists\, C$ s.t. $AC = CA = I$. For $n \times n$ $A$: $A$ is invertible $\iff$ $Ax = 0$ has only $x = 0$ $\iff$ $A \sim I$ $\iff$ $\operatorname{rank}(A) = n$ $\iff$ the columns of $A$ span $\mathbb{R}^n$.
> - **Rules**: $(AB)^{-1} = B^{-1}A^{-1}$, $(AB)^T = B^TA^T$, $(A^T)^{-1} = (A^{-1})^T$, $\operatorname{tr}(AB) = \operatorname{tr}(BA)$.
> - **[[Row Equivalence|Row equivalence]]**: $A \sim B \iff B = E_k \cdots E_1A$ with [[Elementary Matrix|elementary matrices]] $E_t$, each invertible.
> - **Notation**: the transpose is written $A^T$, as on the board. Vectors are not bold ($x$, $b$, $v$, $w$), as on the paper. Row operations stand over $\sim$: $R_i \leftrightarrow R_j$, $R_i \to sR_i$ ($s \ne 0$), $R_i \to R_i + sR_j$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

## Q1 True or False

Question: [[LA1 Midterm 113-1 Questions#Q1 True or False|Q1]]

> [!solution] Solution
> - (a) **F.** $A = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$, $B = \begin{bmatrix} 0 & 0 \\ 1 & 0 \end{bmatrix}$: $AB = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} \ne \begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix} = BA$.
> - (b) **F.** $A = \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}$ is invertible ($A^2 = -I$, so $A^{-1} = -A$), but $A + A^T = O$.
> - (c) **F.** $x_1 + x_2 = 0$, $x_1 + x_2 = 1$: two equations, two unknowns, no solution.
> - (d) **F.** $A = \begin{bmatrix} 1 & 0 \end{bmatrix}$, $B = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$: $AB = \begin{bmatrix} 1 \end{bmatrix} = I$, but $A$ and $B$ are not square, so not invertible.
> - (e) **F.** $A = B = I$: $(A + B)^{-1} = (2I)^{-1} = \tfrac{1}{2}I \ne 2I = A^{-1} + B^{-1}$.
> - (f) **T.** $(A^T)_{ii} = a_{ii}$, so $\operatorname{tr}(A^T) = \sum_{i=1}^{n} a_{ii} = \operatorname{tr}(A)$.
> - (g) **F.** $A = \begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix} \sim \begin{bmatrix} 1 & 1 \\ 0 & 0 \end{bmatrix}$ has a column with no pivot, but $x_1 + x_2 = 0$, $x_1 + x_2 = 1$ has no solution.
> - (h) **T.** $E$ comes from $I$ by one row operation. The reverse operation (swap back, scale by $\tfrac{1}{s}$, or add $-s$ times the row) gives an elementary $E'$ with $E'E = EE' = I$.
> - (i) **F.** $A = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$: $A^2 = A$, but $A \ne O$ and $A \ne I$.
> - (j) **F.** $A = O$, $B = I$, $C = O$ ($2 \times 2$): $AB = C$, $A$ and $C$ are singular, but $B$ is invertible.
>
> \# (d): for square $A$ and $B$ the statement is true. (j): if $A$ and $B$ are the two singular ones, then $C$ is singular too, by Q10 (a); the statement fails because "two of the matrices" can also be $A$ and $C$.

## Q2 Seventh Power of a Matrix

Question: [[LA1 Midterm 113-1 Questions#Q2 Seventh Power of a Matrix|Q2]]

> [!solution] Solution
> $$
> \begin{aligned}
> &A^2 = \begin{bmatrix} 0 & 0 & -1 \\ 0 & 2 & 0 \\ 1 & 0 & 0 \end{bmatrix}\begin{bmatrix} 0 & 0 & -1 \\ 0 & 2 & 0 \\ 1 & 0 & 0 \end{bmatrix} = \begin{bmatrix} -1 & 0 & 0 \\ 0 & 4 & 0 \\ 0 & 0 & -1 \end{bmatrix} \\
> &A^6 = (A^2)^3 = \begin{bmatrix} (-1)^3 & 0 & 0 \\ 0 & 4^3 & 0 \\ 0 & 0 & (-1)^3 \end{bmatrix} = \begin{bmatrix} -1 & 0 & 0 \\ 0 & 64 & 0 \\ 0 & 0 & -1 \end{bmatrix} \\
> &A^7 = A^6A = \begin{bmatrix} -1 & 0 & 0 \\ 0 & 64 & 0 \\ 0 & 0 & -1 \end{bmatrix}\begin{bmatrix} 0 & 0 & -1 \\ 0 & 2 & 0 \\ 1 & 0 & 0 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 1 \\ 0 & 128 & 0 \\ -1 & 0 & 0 \end{bmatrix}
> \end{aligned}
> $$
>
> \# $A^2$ is diagonal, so its powers are taken entry by entry, and a diagonal matrix on the left multiplies row $i$ by its $i$-th diagonal entry.

## Q3 Rank and Span

Question: [[LA1 Midterm 113-1 Questions#Q3 Rank and Span|Q3]]

> [!solution] Solution
> $$
> \begin{aligned}
> &A = \begin{bmatrix} 1 & 2 & 3 & 4 \\ 8 & 7 & 6 & 5 \\ 9 & 10 & 11 & 12 \\ 16 & 15 & 14 & 13 \end{bmatrix} \overset{\substack{R_2 \to R_2 - 8R_1 \\ R_3 \to R_3 - 9R_1 \\ R_4 \to R_4 - 16R_1}}{\sim} \begin{bmatrix} 1 & 2 & 3 & 4 \\ 0 & -9 & -18 & -27 \\ 0 & -8 & -16 & -24 \\ 0 & -17 & -34 & -51 \end{bmatrix} \overset{\substack{R_2 \to -\tfrac{1}{9}R_2 \\ R_3 \to -\tfrac{1}{8}R_3 \\ R_4 \to -\tfrac{1}{17}R_4}}{\sim} \begin{bmatrix} 1 & 2 & 3 & 4 \\ 0 & 1 & 2 & 3 \\ 0 & 1 & 2 & 3 \\ 0 & 1 & 2 & 3 \end{bmatrix} \\[6pt]
> &\overset{\substack{R_3 \to R_3 - R_2 \\ R_4 \to R_4 - R_2}}{\sim} \begin{bmatrix} 1 & 2 & 3 & 4 \\ 0 & 1 & 2 & 3 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix} = H \\[6pt]
> &H \text{ has 2 pivots} \implies \operatorname{rank}(A) = 2. \\
> &\operatorname{rank}(A) = 2 < 4 \implies A \text{ is not invertible} \implies \text{the column vectors of } A \text{ do not span } \mathbb{R}^4.
> \end{aligned}
> $$
>
> \# After the first step, rows 2–4 are all multiples of $[0, 1, 2, 3]$, so only two rows survive. A concrete $b$ outside the span: $[H \mid e_4]$ has the row $[0\ 0\ 0\ 0 \mid 1]$, and undoing the row operations on $e_4$ gives such a $b$.

## Q4 Rank Depending on t

Question: [[LA1 Midterm 113-1 Questions#Q4 Rank Depending on t|Q4]]

> [!solution] Solution
> $$
> \begin{aligned}
> &t = 0:\ A = \begin{bmatrix} 0 & 1 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix} \implies \operatorname{rank}(A) = 1. \\[6pt]
> &t \ne 0:\ A \overset{R_1 \leftrightarrow R_3}{\sim} \begin{bmatrix} t & t & t^2 \\ t & t^2 & t \\ t^2 & 1 & t^2 \end{bmatrix} \overset{\substack{R_1 \to \tfrac{1}{t}R_1 \\ R_2 \to \tfrac{1}{t}R_2}}{\sim} \begin{bmatrix} 1 & 1 & t \\ 1 & t & 1 \\ t^2 & 1 & t^2 \end{bmatrix} \overset{\substack{R_2 \to R_2 - R_1 \\ R_3 \to R_3 - t^2R_1}}{\sim} \begin{bmatrix} 1 & 1 & t \\ 0 & t - 1 & 1 - t \\ 0 & 1 - t^2 & t^2 - t^3 \end{bmatrix} \\[6pt]
> &\quad t = 1:\ \begin{bmatrix} 1 & 1 & 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix} \implies \operatorname{rank}(A) = 1. \\[6pt]
> &\quad t \ne 0, 1:\ \overset{\substack{R_2 \to \tfrac{1}{t - 1}R_2 \\ R_3 \to \tfrac{1}{1 - t}R_3}}{\sim} \begin{bmatrix} 1 & 1 & t \\ 0 & 1 & -1 \\ 0 & 1 + t & t^2 \end{bmatrix} \overset{R_3 \to R_3 - (1 + t)R_2}{\sim} \begin{bmatrix} 1 & 1 & t \\ 0 & 1 & -1 \\ 0 & 0 & t^2 + t + 1 \end{bmatrix} \\[6pt]
> &\qquad t^2 + t + 1 = \big(t + \tfrac{1}{2}\big)^2 + \tfrac{3}{4} > 0 \implies 3 \text{ pivots} \implies \operatorname{rank}(A) = 3. \\[6pt]
> &\text{Hence } \operatorname{rank}(A) = 1 \text{ if } t = 0 \text{ or } t = 1, \text{ and } \operatorname{rank}(A) = 3 \text{ otherwise.}
> \end{aligned}
> $$
>
> \# Set the cases $t = 0$ and $t = 1$ aside before dividing by $t$ and by $t - 1$: a row operation $R_i \to sR_i$ needs $s \ne 0$. Row 3 in the third matrix: $1 - t^2 = (1 - t)(1 + t)$ and $t^2 - t^3 = t^2(1 - t)$, so dividing by $1 - t$ gives $[0,\ 1 + t,\ t^2]$.

## Q5 Inverse of a Skew-Symmetric Matrix

Question: [[LA1 Midterm 113-1 Questions#Q5 Inverse of a Skew-Symmetric Matrix|Q5]]

> [!proof] Proof
> $$
> \begin{aligned}
> &A \text{ is skew-symmetric} \implies A^T = -A. \\
> &(-A^{-1})^T = -(A^{-1})^T = -(A^T)^{-1} = -(-A)^{-1} = -(-A^{-1}) \\
> &\hphantom{(-A^{-1})^T} = A^{-1} = -(-A^{-1}). \\
> &\text{Hence } -A^{-1} \text{ is skew-symmetric.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Two facts: $(A^T)^{-1} = (A^{-1})^T$, proved as in [[LA1 Midterm 112-1 Solutions#Q6 Transpose of an Invertible Matrix|112-1 Q6]], and $(-A)^{-1} = -A^{-1}$, since $(-A)(-A^{-1}) = AA^{-1} = I$. Along the way, $A^{-1}$ itself is skew-symmetric.

## Q6 When the Matrix Is Invertible

Question: [[LA1 Midterm 113-1 Questions#Q6 When the Matrix Is Invertible|Q6]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\begin{bmatrix} 2 & 4 & 2 \\ 1 & r & 3 \\ 1 & 1 & 2 \end{bmatrix} \overset{R_1 \leftrightarrow R_3}{\sim} \begin{bmatrix} 1 & 1 & 2 \\ 1 & r & 3 \\ 2 & 4 & 2 \end{bmatrix} \overset{\substack{R_2 \to R_2 - R_1 \\ R_3 \to R_3 - 2R_1}}{\sim} \begin{bmatrix} 1 & 1 & 2 \\ 0 & r - 1 & 1 \\ 0 & 2 & -2 \end{bmatrix} \\[6pt]
> &\overset{R_2 \leftrightarrow R_3}{\sim} \begin{bmatrix} 1 & 1 & 2 \\ 0 & 2 & -2 \\ 0 & r - 1 & 1 \end{bmatrix} \overset{R_3 \to R_3 - \tfrac{r - 1}{2}R_2}{\sim} \begin{bmatrix} 1 & 1 & 2 \\ 0 & 2 & -2 \\ 0 & 0 & r \end{bmatrix} \\[6pt]
> &A \text{ is invertible} \iff A \sim I \iff 3 \text{ pivots} \iff r \ne 0.
> \end{aligned}
> $$
>
> \# Row 3 in the last step: $1 - \tfrac{r - 1}{2} \cdot (-2) = 1 + (r - 1) = r$. The same matrix is [[LA1 HW 1.5 Questions#FB 1.5.21|FB 1.5.21]]; $\det A = 2r$ gives the same answer.

## Q7 Row Equivalence, Gaussian Elimination and LU

Question: [[LA1 Midterm 113-1 Questions#Q7 Row Equivalence, Gaussian Elimination and LU|Q7]]

> [!proof] Proof of (a)
> $$
> \begin{aligned}
> &[A \mid b] \overset{r}{\sim} [B \mid c] \implies \exists\, E_1, \dots, E_k \text{ elementary s.t. } E_k \cdots E_1[A \mid b] = [B \mid c]. \\
> &\text{Let } P = E_k \cdots E_1:\ m \times m, \text{ invertible (each } E_t \text{ is invertible).} \\
> &P[A \mid b] = [PA \mid Pb] = [B \mid c] \implies PA = B,\ Pb = c. \\[4pt]
> &Ax = b \implies PAx = Pb \implies Bx = c. \\
> &Bx = c \implies PAx = Pb \implies P^{-1}PAx = P^{-1}Pb \implies Ax = b. \\
> &\text{Hence } Ax = b \text{ and } Bx = c \text{ have the same solution set.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The second direction is where $P$ must be invertible.

> [!solution] Solution
> **(b)**
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 1 & 2 & -1 & -3 \\ 3 & 7 & 2 & 1 \\ 4 & -2 & 1 & -2 \end{array}\right] \overset{\substack{R_2 \to R_2 - 3R_1 \\ R_3 \to R_3 - 4R_1}}{\sim} \left[\begin{array}{ccc|c} 1 & 2 & -1 & -3 \\ 0 & 1 & 5 & 10 \\ 0 & -10 & 5 & 10 \end{array}\right] \overset{R_3 \to R_3 + 10R_2}{\sim} \left[\begin{array}{ccc|c} 1 & 2 & -1 & -3 \\ 0 & 1 & 5 & 10 \\ 0 & 0 & 55 & 110 \end{array}\right] \\[6pt]
> &55x_3 = 110 \implies x_3 = 2 \\
> &x_2 + 5x_3 = 10 \implies x_2 = 10 - 10 = 0 \\
> &x_1 + 2x_2 - x_3 = -3 \implies x_1 = -3 - 0 + 2 = -1 \\
> &\implies x = \begin{bmatrix} -1 \\ 0 \\ 2 \end{bmatrix}
> \end{aligned}
> $$
>
> **(c)**
> $$
> \begin{aligned}
> &A = \begin{bmatrix} 1 & 2 & -1 \\ 3 & 7 & 2 \\ 4 & -2 & 1 \end{bmatrix} \overset{\substack{R_2 \to R_2 - 3R_1 \\ R_3 \to R_3 - 4R_1}}{\sim} \begin{bmatrix} 1 & 2 & -1 \\ 0 & 1 & 5 \\ 0 & -10 & 5 \end{bmatrix} \overset{R_3 \to R_3 + 10R_2}{\sim} \begin{bmatrix} 1 & 2 & -1 \\ 0 & 1 & 5 \\ 0 & 0 & 55 \end{bmatrix} = U \\[6pt]
> &L = \begin{bmatrix} 1 & 0 & 0 \\ 3 & 1 & 0 \\ 4 & -10 & 1 \end{bmatrix}, \qquad A = LU = \begin{bmatrix} 1 & 0 & 0 \\ 3 & 1 & 0 \\ 4 & -10 & 1 \end{bmatrix}\begin{bmatrix} 1 & 2 & -1 \\ 0 & 1 & 5 \\ 0 & 0 & 55 \end{bmatrix}
> \end{aligned}
> $$
>
> \# (b) and (c) use the same elimination, so (c) costs nothing extra. In $L$, entry $(i, j)$ is the multiple of row $j$ subtracted from row $i$: $\ell_{21} = 3$, $\ell_{31} = 4$, $\ell_{32} = -10$. Check row 3 of $LU$: $4 \cdot [1, 2, -1] - 10 \cdot [0, 1, 5] + [0, 0, 55] = [4, -2, 1]$.

## Q8 Square Invertible Implies Cube Invertible

Question: [[LA1 Midterm 113-1 Questions#Q8 Square Invertible Implies Cube Invertible|Q8]]

> [!proof] Proof
> $$
> \begin{aligned}
> &A^2 \text{ is defined} \implies A \text{ is } n \times n. \\
> &\text{Claim: } A \text{ is invertible.} \\
> &Ax = 0 \implies A^2x = A(Ax) = A0 = 0 \implies x = (A^2)^{-1}0 = 0. \\
> &\therefore Ax = 0 \text{ has only the trivial solution} \implies A \text{ is invertible.} \\
> &\implies A^3 = A^2A \text{ is a product of invertible matrices} \implies A^3 \text{ is invertible,} \\
> &\qquad (A^3)^{-1} = A^{-1}(A^2)^{-1}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $A^2$ invertible does not give $A^3$ invertible by itself; the step that needs work is "$A$ is invertible".

## Q9 Perpendicular Vectors

Question: [[LA1 Midterm 113-1 Questions#Q9 Perpendicular Vectors|Q9]]

> [!proof] Proof
> $$
> \begin{aligned}
> (v - w) \cdot (v + w) &= v \cdot v + v \cdot w - w \cdot v - w \cdot w \\
> &= \lVert v \rVert^{2} - \lVert w \rVert^{2} && (v \cdot w = w \cdot v) \\
> &= 0 && (\lVert v \rVert = \lVert w \rVert)
> \end{aligned}
> $$
> Hence $v - w$ and $v + w$ are perpendicular. $\blacksquare$
>
> \# The converse holds too ([[LA1 Midterm 114-1 Solutions#Q1 True or False|114-1 Q1 (h)]]). In pictures: the diagonals of a rhombus are perpendicular.

## Q10 Invertible Products

Question: [[LA1 Midterm 113-1 Questions#Q10 Invertible Products|Q10]]

> [!proof] Proof of (a)
> $$
> \begin{aligned}
> &\text{Claim 1: } B \text{ is invertible.} \\
> &Bx = 0 \implies (AB)x = A(Bx) = A0 = 0 \implies x = (AB)^{-1}0 = 0. \\
> &\therefore Bx = 0 \text{ has only the trivial solution} \implies B \text{ is invertible.} \\[4pt]
> &\text{Claim 2: } A \text{ is invertible.} \\
> &A = A(BB^{-1}) = (AB)B^{-1}: \text{ a product of invertible matrices} \implies A \text{ is invertible.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Start with $B$: from $Bx = 0$ the product $AB$ appears when $A$ is multiplied in on the left. Starting with $Ax = 0$ leads nowhere.

> [!proof] Proof of (b)
> $$
> \begin{aligned}
> &ABC = A(BC) \text{ is invertible} \overset{\text{(a)}}{\implies} BC \text{ is invertible} \overset{\text{(a)}}{\implies} B \text{ is invertible.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The first step uses (a) with $A$ and $BC$, the second with $B$ and $C$.

## Q11 Inverse by Row Reduction

Question: [[LA1 Midterm 113-1 Questions#Q11 Inverse by Row Reduction|Q11]]

> [!proof] Proof of (a)
> $$
> \begin{aligned}
> &[A \mid I] \overset{r}{\sim} [I \mid X] \implies \exists\, E_1, \dots, E_k \text{ elementary s.t. } E_k \cdots E_1[A \mid I] = [I \mid X]. \\
> &\text{Let } P = E_k \cdots E_1. \\
> &P[A \mid I] = [PA \mid PI] = [PA \mid P] = [I \mid X] \implies PA = I,\ P = X. \\
> &\implies XA = I \\
> &\implies X = XI = X(AA^{-1}) = (XA)A^{-1} = IA^{-1} = A^{-1}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The right half records the product $P$ of all the row operations, because $PI = P$. The last line uses only that $A^{-1}$ exists.

> [!solution] Solution
> **(b)**
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|ccc} -1 & 2 & 1 & 1 & 0 & 0 \\ 2 & -3 & 5 & 0 & 1 & 0 \\ 1 & 0 & 12 & 0 & 0 & 1 \end{array}\right] \overset{\substack{R_2 \to R_2 + 2R_1 \\ R_3 \to R_3 + R_1}}{\sim} \left[\begin{array}{ccc|ccc} -1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 7 & 2 & 1 & 0 \\ 0 & 2 & 13 & 1 & 0 & 1 \end{array}\right] \\[6pt]
> &\overset{R_3 \to R_3 - 2R_2}{\sim} \left[\begin{array}{ccc|ccc} -1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 7 & 2 & 1 & 0 \\ 0 & 0 & -1 & -3 & -2 & 1 \end{array}\right] \overset{R_3 \to -R_3}{\sim} \left[\begin{array}{ccc|ccc} -1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 7 & 2 & 1 & 0 \\ 0 & 0 & 1 & 3 & 2 & -1 \end{array}\right] \\[6pt]
> &\overset{\substack{R_2 \to R_2 - 7R_3 \\ R_1 \to R_1 - R_3}}{\sim} \left[\begin{array}{ccc|ccc} -1 & 2 & 0 & -2 & -2 & 1 \\ 0 & 1 & 0 & -19 & -13 & 7 \\ 0 & 0 & 1 & 3 & 2 & -1 \end{array}\right] \overset{R_1 \to R_1 - 2R_2}{\sim} \left[\begin{array}{ccc|ccc} -1 & 0 & 0 & 36 & 24 & -13 \\ 0 & 1 & 0 & -19 & -13 & 7 \\ 0 & 0 & 1 & 3 & 2 & -1 \end{array}\right] \\[6pt]
> &\overset{R_1 \to -R_1}{\sim} \left[\begin{array}{ccc|ccc} 1 & 0 & 0 & -36 & -24 & 13 \\ 0 & 1 & 0 & -19 & -13 & 7 \\ 0 & 0 & 1 & 3 & 2 & -1 \end{array}\right] \implies A^{-1} = \begin{bmatrix} -36 & -24 & 13 \\ -19 & -13 & 7 \\ 3 & 2 & -1 \end{bmatrix}
> \end{aligned}
> $$
>
> \# Check one entry of $AA^{-1}$: row 1 of $A$ times column 1 of $A^{-1}$ is $(-1)(-36) + 2(-19) + 1 \cdot 3 = 1$.

## Q12 Inverse of a Block Lower Triangular Matrix

Question: [[LA1 Midterm 113-1 Questions#Q12 Inverse of a Block Lower Triangular Matrix|Q12]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Find } Y = \begin{bmatrix} P_{m \times m} & Q_{m \times n} \\ R_{n \times m} & S_{n \times n} \end{bmatrix} \text{ with } XY = I: \\
> &XY = \begin{bmatrix} AP & AQ \\ BP + CR & BQ + CS \end{bmatrix} = \begin{bmatrix} I_m & O \\ O & I_n \end{bmatrix} \\[4pt]
> &AP = I \implies P = A^{-1} \\
> &AQ = O \implies Q = A^{-1}O = O \\
> &BQ + CS = CS = I \implies S = C^{-1} \\
> &BP + CR = O \implies CR = -BA^{-1} \implies R = -C^{-1}BA^{-1} \\[4pt]
> &\text{Check: } YX = \begin{bmatrix} A^{-1} & O \\ -C^{-1}BA^{-1} & C^{-1} \end{bmatrix}\begin{bmatrix} A & O \\ B & C \end{bmatrix} = \begin{bmatrix} I & O \\ -C^{-1}BA^{-1}A + C^{-1}B & I \end{bmatrix} = \begin{bmatrix} I & O \\ O & I \end{bmatrix}. \\[4pt]
> &\implies X^{-1} = \begin{bmatrix} A^{-1} & O \\ -C^{-1}BA^{-1} & C^{-1} \end{bmatrix}
> \end{aligned}
> $$
>
> \# [[Block Matrix|Block matrices]] multiply like $2 \times 2$ matrices, with the order inside each product kept: $R = -C^{-1}BA^{-1}$, with $C^{-1}$ on the left and $A^{-1}$ on the right. Compare [[LA1 Midterm 112-1 Solutions#Q13 Inverse of a Block Upper Triangular Matrix|112-1 Q13]], the upper triangular case.

## Q13 A System with a Parameter

Question: [[LA1 Midterm 113-1 Questions#Q13 A System with a Parameter|Q13]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 1 & k & 3 & 2 \\ 1 & 2 & 2 & 3 \\ 1 & 3 & k & k + 3 \end{array}\right] \overset{R_1 \leftrightarrow R_2}{\sim} \left[\begin{array}{ccc|c} 1 & 2 & 2 & 3 \\ 1 & k & 3 & 2 \\ 1 & 3 & k & k + 3 \end{array}\right] \overset{\substack{R_2 \to R_2 - R_1 \\ R_3 \to R_3 - R_1}}{\sim} \left[\begin{array}{ccc|c} 1 & 2 & 2 & 3 \\ 0 & k - 2 & 1 & -1 \\ 0 & 1 & k - 2 & k \end{array}\right] \\[6pt]
> &\overset{R_2 \leftrightarrow R_3}{\sim} \left[\begin{array}{ccc|c} 1 & 2 & 2 & 3 \\ 0 & 1 & k - 2 & k \\ 0 & k - 2 & 1 & -1 \end{array}\right] \overset{R_3 \to R_3 - (k - 2)R_2}{\sim} \left[\begin{array}{ccc|c} 1 & 2 & 2 & 3 \\ 0 & 1 & k - 2 & k \\ 0 & 0 & (3 - k)(k - 1) & -(k - 1)^2 \end{array}\right] \\[6pt]
> &\text{(a) } k = 3:\ \text{row 3 is } [0\ \ 0\ \ 0 \mid -4] \implies \text{no solution.} \\
> &\text{(b) } (3 - k)(k - 1) \ne 0, \text{ i.e. } k \ne 1 \text{ and } k \ne 3:\ 3 \text{ pivots} \implies \text{a unique solution.} \\
> &\text{(c) } k = 1:\ \text{row 3 is } [0\ \ 0\ \ 0 \mid 0],\ \operatorname{rank}(A) = \operatorname{rank}[A \mid b] = 2 < 3 \implies \text{infinitely many solutions.}
> \end{aligned}
> $$
>
> \# Row 3 in the last step: $1 - (k - 2)^2 = (1 - (k - 2))(1 + (k - 2)) = (3 - k)(k - 1)$ and $-1 - k(k - 2) = -(k^2 - 2k + 1) = -(k - 1)^2$. Factor before reading off the cases.

## Q14 Trace of a Similar Matrix

Question: [[LA1 Midterm 113-1 Questions#Q14 Trace of a Similar Matrix|Q14]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Claim: } \operatorname{tr}(XY) = \operatorname{tr}(YX) \text{ for } n \times n \text{ matrices } X, Y. \\
> &\operatorname{tr}(XY) = \sum_{i=1}^{n} (XY)_{ii} = \sum_{i=1}^{n}\sum_{k=1}^{n} x_{ik}y_{ki} = \sum_{k=1}^{n}\sum_{i=1}^{n} y_{ki}x_{ik} = \sum_{k=1}^{n} (YX)_{kk} = \operatorname{tr}(YX). \\[4pt]
> &\operatorname{tr}(B) = \operatorname{tr}\big(P^{-1}(AP)\big) = \operatorname{tr}\big((AP)P^{-1}\big) = \operatorname{tr}(A). \\
> &\text{Hence the statement is true: } \operatorname{tr}(A) = \operatorname{tr}(B). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The claim is used with $X = P^{-1}$ and $Y = AP$. The trace is not multiplicative ($\operatorname{tr}(XY) \ne \operatorname{tr}(X)\operatorname{tr}(Y)$ in general); only the swap $XY \to YX$ is allowed.

## Q15 Consistency of a System

Question: [[LA1 Midterm 113-1 Questions#Q15 Consistency of a System|Q15]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{cc|c} 1 & 2 & b_1 \\ 3 & 6 & b_2 \end{array}\right] \overset{R_2 \to R_2 - 3R_1}{\sim} \left[\begin{array}{cc|c} 1 & 2 & b_1 \\ 0 & 0 & b_2 - 3b_1 \end{array}\right] \\[6pt]
> &\text{Consistent} \iff \text{row 2 is not } [0\ \ 0 \mid c] \text{ with } c \ne 0 \iff b_2 - 3b_1 = 0 \iff b_2 = 3b_1.
> \end{aligned}
> $$
>
> \# Then $x_1 = b_1 - 2x_2$ with $x_2$ free: infinitely many solutions.
