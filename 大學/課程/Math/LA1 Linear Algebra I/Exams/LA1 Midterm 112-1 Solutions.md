---
course: [LA1]
semester: "115-1"
chapter: ["1.3", "1.4", "1.5", "4.1", "10.2"]
tags: [linear-algebra, exam, solutions, matrix-algebra, matrix-inverse, linear-systems]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-11-02
questions: "[[LA1 Midterm 112-1 Questions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Question | Answer |
| --- | --- |
| [[LA1 Midterm 112-1 Questions#Q1 True or False\|Q1]] | (a) T; (b) T; (c) T; (d) T; (e) F; (f) F; (g) F; (h) T; (i) T |
| [[LA1 Midterm 112-1 Questions#Q2 Skew-Symmetric Entries\|Q2]] | No such $a, \dots, f$: the diagonal entries are not $0$ |
| [[LA1 Midterm 112-1 Questions#Q3 Rank and Span\|Q3]] | $\operatorname{rank}(A) = 4$; yes, the span is $\mathbb{R}^4$ |
| [[LA1 Midterm 112-1 Questions#Q4 Product of Lower Triangular Matrices\|Q4]] | Proof: split $\sum_{k} a_{ik}b_{kj}$ at $k = i$ |
| [[LA1 Midterm 112-1 Questions#Q5 Odd Power of a Skew-Symmetric Matrix\|Q5]] | Proof: $(A^5)^T = (A^T)^5 = (-A)^5 = -A^5$ |
| [[LA1 Midterm 112-1 Questions#Q6 Transpose of an Invertible Matrix\|Q6]] | Proof: $(A^T)^{-1} = (A^{-1})^T$ |
| [[LA1 Midterm 112-1 Questions#Q7 Diagonal of the Square of a Symmetric Matrix\|Q7]] | Proof: $b_{ii} = \sum_{k} a_{ik}^{2}$ |
| [[LA1 Midterm 112-1 Questions#Q8 Row Equivalence, Gaussian Elimination and LU\|Q8]] | (a) Proof; (b) $x = (\tfrac{1}{3}, \tfrac{1}{3}, -\tfrac{5}{3})$; (c) $L = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ -1 & 2 & 1 \end{bmatrix}$, $U = \begin{bmatrix} 2 & 1 & 0 \\ 0 & 1 & -1 \\ 0 & 0 & 3 \end{bmatrix}$ |
| [[LA1 Midterm 112-1 Questions#Q9 Area of a Triangle\|Q9]] | $16$ |
| [[LA1 Midterm 112-1 Questions#Q10 When the Transpose Times A Is Zero\|Q10]] | Proof: $(A^TA)_{jj} = \sum_{i} a_{ij}^{2}$ |
| [[LA1 Midterm 112-1 Questions#Q11 Left Inverse and an Inverse Formula\|Q11]] | (a) Proof; (b) Proof: $M(A + BCD) = I$, then (a) |
| [[LA1 Midterm 112-1 Questions#Q12 Inverse and a Matrix Equation\|Q12]] | (a) $A^{-1} = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix}$; (b) $C = \begin{bmatrix} 46 & 33 & 30 \\ 39 & 29 & 26 \\ 99 & 68 & 63 \end{bmatrix}$ |
| [[LA1 Midterm 112-1 Questions#Q13 Inverse of a Block Upper Triangular Matrix\|Q13]] | $X^{-1} = \begin{bmatrix} A^{-1} & -A^{-1}BC^{-1} \\ O & C^{-1} \end{bmatrix}$ |
| [[LA1 Midterm 112-1 Questions#Q14 A System with a Parameter\|Q14]] | (a) $k = -4$; (b) $k \ne 0, -4$; (c) $k = 0$ |
| [[LA1 Midterm 112-1 Questions#Q15 Determinant and Trace\|Q15]] | (a) $-9$; (b) $-2$ |
| [[LA1 Midterm 112-1 Questions#Q16 Nilpotent Matrices\|Q16]] | (a) $\begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$; (b) Proof; (c) $(I + N)^{-1} = I - N + N^2 - \cdots + (-1)^{k-1}N^{k-1}$ |

> [!note] Note
> The facts that the answers use.
> - **[[Invertible Matrix|Invertible]]**: $A$ is $n \times n$ and $\exists\, C$ s.t. $AC = CA = I$. For $n \times n$ $A$: $A$ is invertible $\iff$ $Ax = 0$ has only $x = 0$ $\iff$ $A \sim I$ $\iff$ $\operatorname{rank}(A) = n$ $\iff$ the columns of $A$ span $\mathbb{R}^n$.
> - **Rules**: $(AB)^{-1} = B^{-1}A^{-1}$, $(AB)^T = B^TA^T$, $(A^T)^{-1} = (A^{-1})^T$, $\operatorname{tr}(AB) = \operatorname{tr}(BA)$.
> - **[[Row Equivalence|Row equivalence]]**: $A \sim B \iff B = E_k \cdots E_1A$ with [[Elementary Matrix|elementary matrices]] $E_t$, each invertible.
> - **Notation**: the transpose is written $A^T$, as on the board. Vectors are not bold ($x$, $b$), as on the paper. Row operations stand over $\sim$: $R_i \leftrightarrow R_j$, $R_i \to sR_i$ ($s \ne 0$), $R_i \to R_i + sR_j$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

## Q1 True or False

Question: [[LA1 Midterm 112-1 Questions#Q1 True or False|Q1]]

> [!solution] Solution
> - (a) **T.** For $A$: $m \times n$ and $B$: $n \times m$: $\operatorname{tr}(AB) = \sum_{i=1}^{m}\sum_{k=1}^{n} a_{ik}b_{ki} = \sum_{k=1}^{n}\sum_{i=1}^{m} b_{ki}a_{ik} = \operatorname{tr}(BA)$.
> - (b) **T.** $n = 2m$ with $m \ge 1$ $\implies$ $A^n = (A^2)^m = I^m = I$.
> - (c) **T.** $(A^{-1})^T = (A^T)^{-1} = (-A)^{-1} = -A^{-1}$.
> - (d) **T.** $Ax = 0 \implies A^2x = A(Ax) = 0 \implies x = 0$, so $A$ is invertible; then $(A^T)^{-1} = (A^{-1})^T$ and $(A^3)^{-1} = A^{-1}(A^2)^{-1}$.
> - (e) **F.** $A = I$, $B = -I$: both invertible, but $A + B = O$ is not.
> - (f) **F.** $A = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}$, $B = \begin{bmatrix} 1 & 0 \\ 1 & 1 \end{bmatrix}$: $(AB)^{-1} = \begin{bmatrix} 1 & -1 \\ -1 & 2 \end{bmatrix} \ne \begin{bmatrix} 2 & -1 \\ -1 & 1 \end{bmatrix} = A^{-1}B^{-1}$. The rule is $(AB)^{-1} = B^{-1}A^{-1}$.
> - (g) **F.** $A = \begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix} \sim \begin{bmatrix} 1 & 1 \\ 0 & 0 \end{bmatrix}$ has a column with no pivot, but $x_1 + x_2 = 0$, $x_1 + x_2 = 1$ has no solution.
> - (h) **T.** For a triangular $A$, $\det A = a_{11}a_{22} \cdots a_{nn}$, and $A$ is invertible $\iff \det A \ne 0$.
> - (i) **T.** $x_1 + x_2 + x_3 = 0$, $x_1 + x_2 + x_3 = 1$: two equations, three unknowns, no solution.
>
> \# (d): $A^2$ is defined only for a square $A$, so "$Ax = 0$ has only $x = 0$" is enough. (g): "infinitely many solutions $\implies$ a column with no pivot" is true; the other direction fails because the system can be inconsistent. (h): without determinants, nonzero diagonal entries are $n$ pivots, so $A \sim I$.

## Q2 Skew-Symmetric Entries

Question: [[LA1 Midterm 112-1 Questions#Q2 Skew-Symmetric Entries|Q2]]

> [!solution] Solution
> $$
> \begin{aligned}
> &A \text{ is skew-symmetric} \iff A^T = -A \iff a_{ji} = -a_{ij}\ \ \forall\, i, j. \\
> &i = j:\ a_{ii} = -a_{ii} \implies a_{ii} = 0. \\
> &\text{But } a_{11} = 1,\ a_{22} = 4,\ a_{33} = -1,\ a_{44} = 3 \text{ are not } 0. \\
> &\text{Hence no } a, b, c, d, e, f \text{ make } A \text{ skew-symmetric.}
> \end{aligned}
> $$
>
> \# The entries off the diagonal alone would give $a = -2$, $b = 1$, $c = 7$, $d = -6$, $e = 0$, $f = -8$. The diagonal is what makes it impossible; if the paper meant zeros there, these six values are the answer.

## Q3 Rank and Span

Question: [[LA1 Midterm 112-1 Questions#Q3 Rank and Span|Q3]]

> [!solution] Solution
> $$
> \begin{aligned}
> &A = \begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 1 & 0 & -1 & 2 \\ -3 & 0 & 0 & -1 \end{bmatrix} \overset{\substack{R_3 \to R_3 - R_1 \\ R_4 \to R_4 + 3R_1}}{\sim} \begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 0 & 0 & -2 & 3 \\ 0 & 0 & 3 & -4 \end{bmatrix} \overset{R_4 \to R_4 + R_3}{\sim} \begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 0 & 0 & -2 & 3 \\ 0 & 0 & 1 & -1 \end{bmatrix} \\[6pt]
> &\overset{R_3 \leftrightarrow R_4}{\sim} \begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & -2 & 3 \end{bmatrix} \overset{R_4 \to R_4 + 2R_3}{\sim} \begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 1 \end{bmatrix} = H
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &H \text{ has 4 pivots} \implies \operatorname{rank}(A) = 4. \\
> &\operatorname{rank}(A) = 4 = n \implies A \text{ is invertible} \implies Ax = b \text{ is consistent } \forall\, b \in \mathbb{R}^4. \\
> &\text{Hence the span of the column vectors of } A \text{ is } \mathbb{R}^4.
> \end{aligned}
> $$
>
> \# The same matrix is [[LA1 HW 1.5 Questions#FB 1.5.11|FB 1.5.11]]. The step $R_4 \to R_4 + R_3$ and the interchange avoid fractions.

## Q4 Product of Lower Triangular Matrices

Question: [[LA1 Midterm 112-1 Questions#Q4 Product of Lower Triangular Matrices|Q4]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } A = [a_{ij}],\ B = [b_{ij}]: n \times n \text{ lower triangular, i.e. } a_{ij} = 0 \text{ and } b_{ij} = 0\ \ \forall\, i < j. \\
> &\text{Claim: } (AB)_{ij} = 0\ \ \forall\, i < j. \\
> &\text{Let } i < j. \text{ Then} \\
> &(AB)_{ij} = \sum_{k=1}^{n} a_{ik}b_{kj} = \sum_{k=1}^{i} a_{ik}\underbrace{b_{kj}}_{0\ (k \le i < j)} + \sum_{k=i+1}^{n} \underbrace{a_{ik}}_{0\ (i < k)}b_{kj} = 0. \\
> &\forall\, i < j \implies AB \text{ is lower triangular.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Split the sum at $k = i$, so that every term has a zero factor: if $k \le i$, then $k < j$ and $b_{kj} = 0$; if $k > i$, then $a_{ik} = 0$.

## Q5 Odd Power of a Skew-Symmetric Matrix

Question: [[LA1 Midterm 112-1 Questions#Q5 Odd Power of a Skew-Symmetric Matrix|Q5]]

> [!proof] Proof
> $$
> \begin{aligned}
> &A \text{ is skew-symmetric} \implies A^T = -A. \\
> &(A^5)^T = (AAAAA)^T = A^TA^TA^TA^TA^T = (A^T)^5 = (-A)^5 = (-1)^5A^5 = -A^5. \\
> &\text{Hence } A^5 \text{ is skew-symmetric.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $(XY)^T = Y^TX^T$ reverses the order, but every factor is $A$, so the order does not matter. In the same way every odd power of a skew-symmetric matrix is skew-symmetric, and every even power is symmetric.

## Q6 Transpose of an Invertible Matrix

Question: [[LA1 Midterm 112-1 Questions#Q6 Transpose of an Invertible Matrix|Q6]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\because A \text{ is invertible} \\
> &\therefore \exists\, A^{-1} \text{ s.t. } AA^{-1} = A^{-1}A = I. \\
> &\text{Claim: } (A^T)^{-1} = (A^{-1})^T. \\
> &A^T(A^{-1})^T = (A^{-1}A)^T = I^T = I, \\
> &(A^{-1})^TA^T = (AA^{-1})^T = I^T = I. \\
> &\text{Hence } A^T \text{ is invertible and } (A^T)^{-1} = (A^{-1})^T. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Both lines use $(XY)^T = Y^TX^T$, read from right to left.

## Q7 Diagonal of the Square of a Symmetric Matrix

Question: [[LA1 Midterm 112-1 Questions#Q7 Diagonal of the Square of a Symmetric Matrix|Q7]]

> [!proof] Proof
> $$
> \begin{aligned}
> &A \text{ is symmetric} \implies a_{ki} = a_{ik}\ \ \forall\, i, k. \\
> &b_{ii} = (A^2)_{ii} = \sum_{k=1}^{n} a_{ik}a_{ki} = \sum_{k=1}^{n} a_{ik}^{2} \ge 0, \quad i = 1, \dots, n. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# A sum of squares of real numbers is $\ge 0$. Without symmetry it fails: $A = \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}$ gives $A^2 = -I$.

## Q8 Row Equivalence, Gaussian Elimination and LU

Question: [[LA1 Midterm 112-1 Questions#Q8 Row Equivalence, Gaussian Elimination and LU|Q8]]

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
> \# The second direction is where $P$ must be invertible. $P[A \mid b] = [PA \mid Pb]$ because $P$ multiplies each column of $[A \mid b]$ separately.

> [!solution] Solution
> **(b)**
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 2 & 1 & 0 & 1 \\ 0 & 1 & -1 & 2 \\ -2 & 1 & 1 & -2 \end{array}\right] \overset{R_3 \to R_3 + R_1}{\sim} \left[\begin{array}{ccc|c} 2 & 1 & 0 & 1 \\ 0 & 1 & -1 & 2 \\ 0 & 2 & 1 & -1 \end{array}\right] \overset{R_3 \to R_3 - 2R_2}{\sim} \left[\begin{array}{ccc|c} 2 & 1 & 0 & 1 \\ 0 & 1 & -1 & 2 \\ 0 & 0 & 3 & -5 \end{array}\right] \\[6pt]
> &3x_3 = -5 \implies x_3 = -\tfrac{5}{3} \\
> &x_2 - x_3 = 2 \implies x_2 = 2 + x_3 = \tfrac{1}{3} \\
> &2x_1 + x_2 = 1 \implies x_1 = \tfrac{1}{2}\big(1 - \tfrac{1}{3}\big) = \tfrac{1}{3} \\
> &\implies x = \begin{bmatrix} \tfrac{1}{3} \\ \tfrac{1}{3} \\ -\tfrac{5}{3} \end{bmatrix}
> \end{aligned}
> $$
>
> **(c)**
> $$
> \begin{aligned}
> &A = \begin{bmatrix} 2 & 1 & 0 \\ 0 & 1 & -1 \\ -2 & 1 & 1 \end{bmatrix} \overset{R_3 \to R_3 + R_1}{\sim} \begin{bmatrix} 2 & 1 & 0 \\ 0 & 1 & -1 \\ 0 & 2 & 1 \end{bmatrix} \overset{R_3 \to R_3 - 2R_2}{\sim} \begin{bmatrix} 2 & 1 & 0 \\ 0 & 1 & -1 \\ 0 & 0 & 3 \end{bmatrix} = U \\[6pt]
> &L = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ -1 & 2 & 1 \end{bmatrix}, \qquad A = LU = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ -1 & 2 & 1 \end{bmatrix}\begin{bmatrix} 2 & 1 & 0 \\ 0 & 1 & -1 \\ 0 & 0 & 3 \end{bmatrix}
> \end{aligned}
> $$
>
> \# In $L$, entry $(i, j)$ is the multiple of row $j$ that was subtracted from row $i$: $R_3 \to R_3 + R_1$ subtracts $-1$ times row 1, so $\ell_{31} = -1$; $R_3 \to R_3 - 2R_2$ gives $\ell_{32} = 2$; nothing was subtracted from row 2, so $\ell_{21} = 0$. Check row 3 of $LU$: $-1 \cdot [2, 1, 0] + 2 \cdot [0, 1, -1] + [0, 0, 3] = [-2, 1, 1]$.

## Q9 Area of a Triangle

Question: [[LA1 Midterm 112-1 Questions#Q9 Area of a Triangle|Q9]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\begin{cases} y = x \\ y = -3x + 8 \end{cases} \implies (2, 2), \qquad \begin{cases} y = x \\ 3y + 5x = 0 \end{cases} \implies (0, 0), \qquad \begin{cases} y = -3x + 8 \\ 3y + 5x = 0 \end{cases} \implies (6, -10). \\[4pt]
> &\text{Edges from } (0, 0):\ a = [2, 2],\ b = [6, -10]. \\
> &\text{Area} = \tfrac{1}{2}\left\lvert \det \begin{bmatrix} 2 & 2 \\ 6 & -10 \end{bmatrix} \right\rvert = \tfrac{1}{2}\lvert -20 - 12 \rvert = 16.
> \end{aligned}
> $$
>
> \# Third vertex: $3(-3x + 8) + 5x = 0 \implies -4x + 24 = 0 \implies x = 6$, $y = -10$. $\lvert \det \rvert$ of the two edge vectors is the area of the parallelogram they span, and the triangle is half of it.

## Q10 When the Transpose Times A Is Zero

Question: [[LA1 Midterm 112-1 Questions#Q10 When the Transpose Times A Is Zero|Q10]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } A = [a_{ij}]: m \times n. \text{ For each } j = 1, \dots, n: \\
> &0 = (A^TA)_{jj} = \sum_{i=1}^{m} (A^T)_{ji}(A)_{ij} = \sum_{i=1}^{m} a_{ij}^{2} \\
> &\implies a_{ij} = 0\ \ \forall\, i \quad \text{(a sum of squares of real numbers is } 0 \text{ only if each square is } 0\text{)} \\
> &\forall\, i, j \implies A = O. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Only the diagonal of $A^TA$ is needed: $(A^TA)_{jj}$ is the squared norm of column $j$ of $A$. "Over $\mathbb{R}$" matters: $A = \begin{bmatrix} 1 \\ i \end{bmatrix}$ with $i^2 = -1$ gives $A^TA = 1 + i^2 = 0$, but $A \ne O$.

## Q11 Left Inverse and an Inverse Formula

Question: [[LA1 Midterm 112-1 Questions#Q11 Left Inverse and an Inverse Formula|Q11]]

> [!proof] Proof of (a)
> $$
> \begin{aligned}
> &BA = I. \\
> &\text{Claim: } Ax = 0 \text{ has only the trivial solution.} \\
> &Ax = 0 \implies x = Ix = (BA)x = B(Ax) = B0 = 0. \\
> &\therefore A\ (n \times n) \text{ is invertible: } \exists\, A^{-1} \text{ s.t. } AA^{-1} = A^{-1}A = I. \\
> &B = BI = B(AA^{-1}) = (BA)A^{-1} = IA^{-1} = A^{-1}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Work with $Ax = 0$, because $B$ stands on the left of $A$ and can be multiplied in.

> [!proof] Proof of (b)
> Let $S = C^{-1} + DA^{-1}B$ and $M = A^{-1} - A^{-1}BS^{-1}DA^{-1}$. By (a), it suffices to show $M(A + BCD) = I$.
> $$
> \begin{aligned}
> M(A + BCD) &= A^{-1}A + A^{-1}BCD - A^{-1}BS^{-1}DA^{-1}A - A^{-1}BS^{-1}DA^{-1}BCD \\
> &= I + A^{-1}B\big[\,C - S^{-1} - S^{-1}DA^{-1}BC\,\big]D \\
> &= I + A^{-1}B\big[\,C - S^{-1}(C^{-1} + DA^{-1}B)C\,\big]D \\
> &= I + A^{-1}B\big[\,C - S^{-1}SC\,\big]D = I + A^{-1}B\,[\,C - C\,]\,D = I.
> \end{aligned}
> $$
> By (a), $A + BCD$ is invertible and $(A + BCD)^{-1} = M = A^{-1} - A^{-1}B(C^{-1} + DA^{-1}B)^{-1}DA^{-1}$. $\blacksquare$
>
> \# The formula needs $A$ ($n \times n$) and $C$ ($k \times k$) invertible, $B$: $n \times k$, $D$: $k \times n$, and $S$ invertible; the crop of the question does not show these hypotheses. Line 3 uses $S^{-1} + S^{-1}DA^{-1}BC = S^{-1}(C^{-1}C + DA^{-1}BC) = S^{-1}(C^{-1} + DA^{-1}B)C$. Part (a) is what makes one product enough.

## Q12 Inverse and a Matrix Equation

Question: [[LA1 Midterm 112-1 Questions#Q12 Inverse and a Matrix Equation|Q12]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|ccc} 5 & -3 & -1 & 1 & 0 & 0 \\ 4 & -2 & -1 & 0 & 1 & 0 \\ -12 & 7 & 3 & 0 & 0 & 1 \end{array}\right] \overset{R_1 \to R_1 - R_2}{\sim} \left[\begin{array}{ccc|ccc} 1 & -1 & 0 & 1 & -1 & 0 \\ 4 & -2 & -1 & 0 & 1 & 0 \\ -12 & 7 & 3 & 0 & 0 & 1 \end{array}\right] \\[6pt]
> &\overset{\substack{R_2 \to R_2 - 4R_1 \\ R_3 \to R_3 + 12R_1}}{\sim} \left[\begin{array}{ccc|ccc} 1 & -1 & 0 & 1 & -1 & 0 \\ 0 & 2 & -1 & -4 & 5 & 0 \\ 0 & -5 & 3 & 12 & -12 & 1 \end{array}\right] \overset{R_3 \to R_3 + 2R_2}{\sim} \left[\begin{array}{ccc|ccc} 1 & -1 & 0 & 1 & -1 & 0 \\ 0 & 2 & -1 & -4 & 5 & 0 \\ 0 & -1 & 1 & 4 & -2 & 1 \end{array}\right] \\[6pt]
> &\overset{R_2 \leftrightarrow R_3}{\sim} \left[\begin{array}{ccc|ccc} 1 & -1 & 0 & 1 & -1 & 0 \\ 0 & -1 & 1 & 4 & -2 & 1 \\ 0 & 2 & -1 & -4 & 5 & 0 \end{array}\right] \overset{R_3 \to R_3 + 2R_2}{\sim} \left[\begin{array}{ccc|ccc} 1 & -1 & 0 & 1 & -1 & 0 \\ 0 & -1 & 1 & 4 & -2 & 1 \\ 0 & 0 & 1 & 4 & 1 & 2 \end{array}\right] \\[6pt]
> &\overset{R_2 \to R_2 - R_3}{\sim} \left[\begin{array}{ccc|ccc} 1 & -1 & 0 & 1 & -1 & 0 \\ 0 & -1 & 0 & 0 & -3 & -1 \\ 0 & 0 & 1 & 4 & 1 & 2 \end{array}\right] \overset{R_2 \to -R_2}{\sim} \left[\begin{array}{ccc|ccc} 1 & -1 & 0 & 1 & -1 & 0 \\ 0 & 1 & 0 & 0 & 3 & 1 \\ 0 & 0 & 1 & 4 & 1 & 2 \end{array}\right] \\[6pt]
> &\overset{R_1 \to R_1 + R_2}{\sim} \left[\begin{array}{ccc|ccc} 1 & 0 & 0 & 1 & 2 & 1 \\ 0 & 1 & 0 & 0 & 3 & 1 \\ 0 & 0 & 1 & 4 & 1 & 2 \end{array}\right] \implies A^{-1} = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix}
> \end{aligned}
> $$
>
> **(b)** Let $M = \begin{bmatrix} 2 & 1 & 3 \\ -1 & 2 & 2 \\ 2 & 1 & 4 \end{bmatrix}$.
> $$
> \begin{aligned}
> &ACA = M \implies A^{-1}(ACA)A^{-1} = A^{-1}MA^{-1} \implies C = A^{-1}MA^{-1}. \\
> &A^{-1}M = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix}\begin{bmatrix} 2 & 1 & 3 \\ -1 & 2 & 2 \\ 2 & 1 & 4 \end{bmatrix} = \begin{bmatrix} 2 & 6 & 11 \\ -1 & 7 & 10 \\ 11 & 8 & 22 \end{bmatrix} \\
> &C = (A^{-1}M)A^{-1} = \begin{bmatrix} 2 & 6 & 11 \\ -1 & 7 & 10 \\ 11 & 8 & 22 \end{bmatrix}\begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix} = \begin{bmatrix} 46 & 33 & 30 \\ 39 & 29 & 26 \\ 99 & 68 & 63 \end{bmatrix}
> \end{aligned}
> $$
>
> \# (a): $R_1 \to R_1 - R_2$ first gives a pivot $1$ without fractions. (b): multiply by $A^{-1}$ on the left and on the right; $C = A^{-1}MA^{-1}$, not $(A^{-1})^2M$, since matrix products do not commute.

## Q13 Inverse of a Block Upper Triangular Matrix

Question: [[LA1 Midterm 112-1 Questions#Q13 Inverse of a Block Upper Triangular Matrix|Q13]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Find } Y = \begin{bmatrix} P_{m \times m} & Q_{m \times n} \\ R_{n \times m} & S_{n \times n} \end{bmatrix} \text{ with } XY = I: \\
> &XY = \begin{bmatrix} AP + BR & AQ + BS \\ CR & CS \end{bmatrix} = \begin{bmatrix} I_m & O \\ O & I_n \end{bmatrix} \\[4pt]
> &CR = O \implies R = C^{-1}O = O \\
> &CS = I \implies S = C^{-1} \\
> &AP + BR = AP = I \implies P = A^{-1} \\
> &AQ + BS = O \implies AQ = -BC^{-1} \implies Q = -A^{-1}BC^{-1} \\[4pt]
> &\text{Check: } YX = \begin{bmatrix} A^{-1} & -A^{-1}BC^{-1} \\ O & C^{-1} \end{bmatrix}\begin{bmatrix} A & B \\ O & C \end{bmatrix} = \begin{bmatrix} I & A^{-1}B - A^{-1}BC^{-1}C \\ O & I \end{bmatrix} = \begin{bmatrix} I & O \\ O & I \end{bmatrix}. \\[4pt]
> &\implies X^{-1} = \begin{bmatrix} A^{-1} & -A^{-1}BC^{-1} \\ O & C^{-1} \end{bmatrix}
> \end{aligned}
> $$
>
> \# [[Block Matrix|Block matrices]] multiply like $2 \times 2$ matrices, as long as the order inside each product is kept. Solve the equations in the order $R$, $S$, $P$, $Q$: each uses the ones before it.

## Q14 A System with a Parameter

Question: [[LA1 Midterm 112-1 Questions#Q14 A System with a Parameter|Q14]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 1 & -2 & 3 & 1 \\ 2 & k & 6 & 6 \\ -1 & 3 & k - 3 & 0 \end{array}\right] \overset{\substack{R_2 \to R_2 - 2R_1 \\ R_3 \to R_3 + R_1}}{\sim} \left[\begin{array}{ccc|c} 1 & -2 & 3 & 1 \\ 0 & k + 4 & 0 & 4 \\ 0 & 1 & k & 1 \end{array}\right] \overset{R_2 \leftrightarrow R_3}{\sim} \left[\begin{array}{ccc|c} 1 & -2 & 3 & 1 \\ 0 & 1 & k & 1 \\ 0 & k + 4 & 0 & 4 \end{array}\right] \\[6pt]
> &\overset{R_3 \to R_3 - (k + 4)R_2}{\sim} \left[\begin{array}{ccc|c} 1 & -2 & 3 & 1 \\ 0 & 1 & k & 1 \\ 0 & 0 & -k(k + 4) & -k \end{array}\right] \\[6pt]
> &\text{(a) } k = -4:\ \text{row 3 is } [0\ \ 0\ \ 0 \mid 4] \implies \text{no solution.} \\
> &\text{(b) } k(k + 4) \ne 0, \text{ i.e. } k \ne 0 \text{ and } k \ne -4:\ 3 \text{ pivots} \implies \text{a unique solution.} \\
> &\text{(c) } k = 0:\ \text{row 3 is } [0\ \ 0\ \ 0 \mid 0],\ \operatorname{rank}(A) = \operatorname{rank}[A \mid b] = 2 < 3 \implies \text{infinitely many solutions.}
> \end{aligned}
> $$
>
> \# Interchange rows 2 and 3 before eliminating, so that the pivot is $1$ and not $k + 4$, which can be $0$. Row 3 in the last step: $4 - (k + 4) \cdot 1 = -k$.

## Q15 Determinant and Trace

Question: [[LA1 Midterm 112-1 Questions#Q15 Determinant and Trace|Q15]]

> [!solution] Solution
> $$
> \begin{aligned}
> \text{(a) } \det A &= 2\begin{vmatrix} 0 & 3 \\ 1 & -4 \end{vmatrix} - (-1)\begin{vmatrix} -1 & 3 \\ 2 & -4 \end{vmatrix} + 1\begin{vmatrix} -1 & 0 \\ 2 & 1 \end{vmatrix} \\
> &= 2(0 - 3) + (4 - 6) + (-1 - 0) = -6 - 2 - 1 = -9 \\[4pt]
> \text{(b) } \operatorname{tr}(A) &= 2 + 0 + (-4) = -2
> \end{aligned}
> $$
>
> \# Expansion along row 1 with the signs $+, -, +$. The trace is the sum of the diagonal entries only.

## Q16 Nilpotent Matrices

Question: [[LA1 Midterm 112-1 Questions#Q16 Nilpotent Matrices|Q16]]

> [!solution] Solution
> **(a)** $A = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} \ne O$, and $A^2 = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}\begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} = O$.

> [!proof] Proof of (b)
> $$
> \begin{aligned}
> &\text{Suppose } A \text{ is invertible and } A^k = O \text{ for some positive integer } k. \\
> &\because A^{-1} \text{ exists and } A^{-1}A = I \\
> &\therefore I = (A^{-1})^{k}A^{k} = (A^{-1})^{k}O = O, \text{ a contradiction, since } I \ne O. \\
> &\text{Hence } A \text{ is not nilpotent.} \qquad \blacksquare
> \end{aligned}
> $$

> [!proof] Proof of (c)
> $$
> \begin{aligned}
> &N^k = O,\ k \ge 1. \text{ Let } S = I - N + N^2 - \cdots + (-1)^{k-1}N^{k-1}. \\
> &(I + N)S = \big(I - N + N^2 - \cdots + (-1)^{k-1}N^{k-1}\big) + \big(N - N^2 + \cdots + (-1)^{k-2}N^{k-1} + (-1)^{k-1}N^{k}\big) \\
> &\phantom{(I + N)S} = I + (-1)^{k-1}N^{k} = I + O = I. \\
> &S(I + N) = I \text{ in the same way } (S \text{ is a sum of powers of } N, \text{ so it commutes with } N). \\
> &\text{Hence } I + N \text{ is invertible and } (I + N)^{-1} = I - N + N^2 - \cdots + (-1)^{k-1}N^{k-1}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The middle terms cancel in pairs, as in $(1 + x)(1 - x + x^2 - \cdots + (-1)^{k-1}x^{k-1}) = 1 + (-1)^{k-1}x^{k}$. For $N^2 = O$: $(I + N)^{-1} = I - N$. "For some integer $k$" means $k \ge 1$, since $N^0 = I \ne O$.

> [!warning] Signs for every k
> The handwritten answer in the source ends the inverse with $-N + I$, which has the right signs only for odd $k$. With the signs $(-1)^{j}N^{j}$ the formula works for every $k$.
