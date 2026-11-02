---
course: [LA1]
semester: "115-1"
chapter: ["1.1", "1.2", "1.3", "1.4", "1.5", "10.2"]
tags: [linear-algebra, exam, solutions, matrix-algebra, matrix-inverse, linear-systems]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-11-02
questions: "[[LA1 Midterm 114-1 Questions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Question | Answer |
| --- | --- |
| [[LA1 Midterm 114-1 Questions#Q1 True or False\|Q1]] | (a) F; (b) F; (c) T; (d) T; (e) F; (f) F; (g) T; (h) T; (i) T; (j) F |
| [[LA1 Midterm 114-1 Questions#Q2 Reduced Row-Echelon Form\|Q2]] | $\begin{bmatrix} 1 & -3 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix}$ |
| [[LA1 Midterm 114-1 Questions#Q3 Span of Two Vectors\|Q3]] | No: the system gives $0 = 28$ |
| [[LA1 Midterm 114-1 Questions#Q4 Norm, Unit Vector and Dot Product\|Q4]] | (a) $5$; (b) $\tfrac{1}{\sqrt{26}}[-1, 3, 4]$; (c) $5$ |
| [[LA1 Midterm 114-1 Questions#Q5 LU Factorization and Solving\|Q5]] | $L = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 3 & 2 & 1 \end{bmatrix}$, $U = \begin{bmatrix} 1 & -4 & 2 \\ 0 & 2 & -1 \\ 0 & 0 & -2 \end{bmatrix}$; $x = (1, -1, -4)$ |
| [[LA1 Midterm 114-1 Questions#Q6 A System with a Parameter\|Q6]] | (a) $k = -4$; (b) $k \ne 0, -4$; (c) $k = 0$ |
| [[LA1 Midterm 114-1 Questions#Q7 Matrix from the General Solution\|Q7]] | $A = \begin{bmatrix} -2 & 1 & -2 \\ -6 & 3 & -6 \\ 0 & 0 & 0 \\ -4 & 2 & -4 \end{bmatrix}$ |
| [[LA1 Midterm 114-1 Questions#Q8 Inverse of I plus B\|Q8]] | $(I + B)^{-1} = \tfrac{1}{2}(I + A) = \begin{bmatrix} 1 & 0 & 0 & 0 \\ 1 & 2 & 0 & 0 \\ 0 & -2 & 3 & 0 \\ 0 & 0 & -3 & 4 \end{bmatrix}$ |
| [[LA1 Midterm 114-1 Questions#Q9 Inverse by Row Reduction\|Q9]] | (a) Proof; (b) $A^{-1} = \begin{bmatrix} -7 & 5 & 3 \\ 3 & -2 & -2 \\ 3 & -2 & -1 \end{bmatrix}$ |
| [[LA1 Midterm 114-1 Questions#Q10 A Minus Its Transpose Is Skew-Symmetric\|Q10]] | Proof: $(A - A^T)^T = -(A - A^T)$ |
| [[LA1 Midterm 114-1 Questions#Q11 Row Equivalence and Gaussian Elimination\|Q11]] | (1) Proof; (2) $x = (-1, 2, 0)$ |
| [[LA1 Midterm 114-1 Questions#Q12 A Commutator Equal to A\|Q12]] | Proof: if $A^{-1}$ existed, $B - A^{-1}BA = I$ and the traces give $0 = n$ |
| [[LA1 Midterm 114-1 Questions#Q13 Left Inverse and an Inverse Formula\|Q13]] | (a) Proof; (b) Proof: $B(A + B)^{-1}A \cdot (A^{-1} + B^{-1}) = I$, then (a) |
| [[LA1 Midterm 114-1 Questions#Q14 Idempotent Matrix\|Q14]] | $(I - cA)^{-1} = I + \tfrac{c}{1 - c}A$ |

> [!note] Note
> The facts that the answers use.
> - **[[Invertible Matrix|Invertible]]**: $A$ is $n \times n$ and $\exists\, C$ s.t. $AC = CA = I$. For $n \times n$ $A$: $A$ is invertible $\iff$ $Ax = 0$ has only $x = 0$ $\iff$ $A \sim I$ $\iff$ $\operatorname{rank}(A) = n$.
> - **Rules**: $(AB)^{-1} = B^{-1}A^{-1}$, $(AB)^T = B^TA^T$, $(A^T)^{-1} = (A^{-1})^T$, $\operatorname{tr}(AB) = \operatorname{tr}(BA)$, $v \cdot v = \lVert v \rVert^{2}$.
> - **[[Row Equivalence|Row equivalence]]**: $A \sim B \iff B = E_k \cdots E_1A$ with [[Elementary Matrix|elementary matrices]] $E_t$, each invertible.
> - **Notation**: the transpose is written $A^T$, as on the board. Vectors are not bold ($u$, $v$, $w$, $x$, $b$), as on the paper. Row operations stand over $\sim$: $R_i \leftrightarrow R_j$, $R_i \to sR_i$ ($s \ne 0$), $R_i \to R_i + sR_j$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

## Q1 True or False

Question: [[LA1 Midterm 114-1 Questions#Q1 True or False|Q1]]

> [!solution] Solution
> - (a) **F.** $A = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$, $B = \begin{bmatrix} 0 & 0 \\ 1 & 0 \end{bmatrix}$: $AB = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} \ne \begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix} = BA$.
> - (b) **F.** $v \cdot v = \lVert v \rVert^{2}$: $v = [2, 0]$ gives $v \cdot v = 4 \ne 2 = \lVert v \rVert$.
> - (c) **T.** $A$, $A^T$ are invertible $\implies$ $AA^T$ is invertible, $(AA^T)^{-1} = (A^T)^{-1}A^{-1} = (A^{-1})^TA^{-1}$.
> - (d) **T.** $Ax = 0 \implies A^2x = A(Ax) = 0 \implies x = 0$, so $A$ is invertible; then $(A^T)^{-1} = (A^{-1})^T$ and $(A^3)^{-1} = A^{-1}(A^2)^{-1}$.
> - (e) **F.** $A = I$, $B = -I$: both invertible, but $A + B = O$ is not.
> - (f) **F.** $A = \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}$ is invertible ($A^2 = -I$, so $A^{-1} = -A$), but $A + A^T = O$.
> - (g) **T.** If $A$ were invertible, $A = A^{-1}A^2 = A^{-1}O = O$, and $O$ is not invertible $(\rightarrow\leftarrow)$.
> - (h) **T.** $(v - w) \cdot (v + w) = \lVert v \rVert^{2} - \lVert w \rVert^{2}$, which is $0 \iff \lVert v \rVert^{2} = \lVert w \rVert^{2} \iff \lVert v \rVert = \lVert w \rVert$ (norms are $\ge 0$).
> - (i) **T.** $x_1 + x_2 + x_3 = 0$, $x_1 + x_2 + x_3 = 1$: two equations, three unknowns, no solution.
> - (j) **F.** $A = \begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix} \sim \begin{bmatrix} 1 & 1 \\ 0 & 0 \end{bmatrix}$ has a column with no pivot, but $x_1 + x_2 = 0$, $x_1 + x_2 = 1$ has no solution.
>
> \# (b): "magnitude" is the norm $\lVert v \rVert = \sqrt{v \cdot v}$; the dot product gives its square. (j): "infinitely many solutions $\implies$ a column with no pivot" is true; the other direction fails because the system can be inconsistent. (i) says "may": one example is enough.

## Q2 Reduced Row-Echelon Form

Question: [[LA1 Midterm 114-1 Questions#Q2 Reduced Row-Echelon Form|Q2]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 1 & -3 & 0 & 0 & -1 \\ 2 & -6 & 2 & 4 & 0 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix} \overset{\substack{R_2 \to R_2 + R_1 \\ R_3 \to R_3 + 2R_1}}{\sim} \begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 2 & 6 & 8 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix} \overset{\substack{R_1 \to -R_1 \\ R_3 \to \tfrac{1}{2}R_3}}{\sim} \begin{bmatrix} 1 & -3 & 0 & -1 & -4 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 1 & 3 & 4 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix} \\[6pt]
> &\overset{R_2 \leftrightarrow R_3}{\sim} \begin{bmatrix} 1 & -3 & 0 & -1 & -4 \\ 0 & 0 & 1 & 3 & 4 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix} \overset{R_4 \to R_4 - R_2}{\sim} \begin{bmatrix} 1 & -3 & 0 & -1 & -4 \\ 0 & 0 & 1 & 3 & 4 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & -8 \end{bmatrix} \overset{R_4 \to -\tfrac{1}{8}R_4}{\sim} \begin{bmatrix} 1 & -3 & 0 & -1 & -4 \\ 0 & 0 & 1 & 3 & 4 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix} \\[6pt]
> &\overset{\substack{R_3 \to R_3 - 3R_4 \\ R_2 \to R_2 - 4R_4 \\ R_1 \to R_1 + 4R_4}}{\sim} \begin{bmatrix} 1 & -3 & 0 & -1 & 0 \\ 0 & 0 & 1 & 3 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix} \overset{\substack{R_2 \to R_2 - 3R_3 \\ R_1 \to R_1 + R_3}}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix}
> \end{aligned}
> $$
>
> \# Reduced row-echelon form: every pivot is $1$ and is the only nonzero entry of its column. Column 2 has no pivot, so $-3$ stays. After the forward pass, clear the columns above the pivots from the last pivot backwards.

## Q3 Span of Two Vectors

Question: [[LA1 Midterm 114-1 Questions#Q3 Span of Two Vectors|Q3]]

> [!solution] Solution
> $$
> \begin{aligned}
> &b \in \operatorname{span}\{v, w\} \iff \exists\, x, y \text{ s.t. } xv + yw = b \iff [\,v\ \ w \mid b\,] \text{ is consistent.} \\
> &\left[\begin{array}{cc|c} 3 & 1 & 1 \\ 1 & 3 & -1 \\ 1 & 2 & -4 \end{array}\right] \overset{R_1 \leftrightarrow R_3}{\sim} \left[\begin{array}{cc|c} 1 & 2 & -4 \\ 1 & 3 & -1 \\ 3 & 1 & 1 \end{array}\right] \overset{\substack{R_2 \to R_2 - R_1 \\ R_3 \to R_3 - 3R_1}}{\sim} \left[\begin{array}{cc|c} 1 & 2 & -4 \\ 0 & 1 & 3 \\ 0 & -5 & 13 \end{array}\right] \overset{R_3 \to R_3 + 5R_2}{\sim} \left[\begin{array}{cc|c} 1 & 2 & -4 \\ 0 & 1 & 3 \\ 0 & 0 & 28 \end{array}\right] \\[6pt]
> &\text{Row 3: } 0x + 0y = 28, \text{ impossible} \implies \text{no solution.} \\
> &\text{Hence } b \text{ is not in the span of } v \text{ and } w.
> \end{aligned}
> $$
>
> \# Write the conclusion with its reason, the row $[0\ \ 0 \mid 28]$: the reason is what is graded.

## Q4 Norm, Unit Vector and Dot Product

Question: [[LA1 Midterm 114-1 Questions#Q4 Norm, Unit Vector and Dot Product|Q4]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{(a) } u + v = [0, 4, 3],\quad \lVert u + v \rVert = \sqrt{0^2 + 4^2 + 3^2} = \sqrt{25} = 5. \\
> &\text{(b) } \lVert u \rVert = \sqrt{(-1)^2 + 3^2 + 4^2} = \sqrt{26},\quad \frac{1}{\lVert u \rVert}u = \frac{1}{\sqrt{26}}[-1, 3, 4] = \Big[-\frac{1}{\sqrt{26}}, \frac{3}{\sqrt{26}}, \frac{4}{\sqrt{26}}\Big]. \\
> &\text{(c) } (u + v) \cdot w = [0, 4, 3] \cdot [-2, -1, 3] = 0 \cdot (-2) + 4 \cdot (-1) + 3 \cdot 3 = 5.
> \end{aligned}
> $$
>
> \# (b): "the same direction" means a positive multiple, so divide by $+\lVert u \rVert$.

## Q5 LU Factorization and Solving

Question: [[LA1 Midterm 114-1 Questions#Q5 LU Factorization and Solving|Q5]]

> [!solution] Solution
> $$
> \begin{aligned}
> &A = \begin{bmatrix} 1 & -4 & 2 \\ 0 & 2 & -1 \\ 3 & -8 & 2 \end{bmatrix} \overset{R_3 \to R_3 - 3R_1}{\sim} \begin{bmatrix} 1 & -4 & 2 \\ 0 & 2 & -1 \\ 0 & 4 & -4 \end{bmatrix} \overset{R_3 \to R_3 - 2R_2}{\sim} \begin{bmatrix} 1 & -4 & 2 \\ 0 & 2 & -1 \\ 0 & 0 & -2 \end{bmatrix} = U \\[6pt]
> &L = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 3 & 2 & 1 \end{bmatrix}, \qquad A = LU. \\[6pt]
> &Ax = b \iff L(Ux) = b. \text{ Let } y = Ux. \\
> &\text{Forward: } Ly = b:\ y_1 = -3,\ y_2 = 2,\ 3y_1 + 2y_2 + y_3 = 3 \implies y_3 = 3 + 9 - 4 = 8. \\
> &\text{Back: } Ux = y:\ -2x_3 = 8 \implies x_3 = -4, \\
> &\qquad 2x_2 - x_3 = 2 \implies x_2 = \tfrac{1}{2}(2 + x_3) = -1, \\
> &\qquad x_1 - 4x_2 + 2x_3 = -3 \implies x_1 = -3 + 4x_2 - 2x_3 = -3 - 4 + 8 = 1. \\
> &\implies x = \begin{bmatrix} 1 \\ -1 \\ -4 \end{bmatrix}
> \end{aligned}
> $$
>
> \# In $L$, entry $(i, j)$ is the multiple of row $j$ subtracted from row $i$: $\ell_{21} = 0$, $\ell_{31} = 3$, $\ell_{32} = 2$. Check: $A x = [1 + 4 - 8,\ -2 + 4,\ 3 + 8 - 8] = [-3, 2, 3] = b$.

## Q6 A System with a Parameter

Question: [[LA1 Midterm 114-1 Questions#Q6 A System with a Parameter|Q6]]

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
> \# The same system is [[LA1 Midterm 112-1 Solutions#Q14 A System with a Parameter|112-1 Q14]]. Interchange rows 2 and 3 first, so that the pivot is $1$ and not $k + 4$, which can be $0$.

## Q7 Matrix from the General Solution

Question: [[LA1 Midterm 114-1 Questions#Q7 Matrix from the General Solution|Q7]]

> [!solution] Solution
> $$
> \begin{aligned}
> &x \in \mathbb{R}^3,\ b \in \mathbb{R}^4 \implies A \text{ is } 4 \times 3. \text{ Let } p = \begin{bmatrix} 1 \\ 1 \\ -1 \end{bmatrix},\ u_1 = \begin{bmatrix} 1 \\ 2 \\ 0 \end{bmatrix},\ u_2 = \begin{bmatrix} 2 \\ 2 \\ -1 \end{bmatrix}. \\
> &\alpha = \beta = 0:\ Ap = b. \qquad \alpha = 1,\ \beta = 0:\ A(p + u_1) = b \implies Au_1 = 0. \qquad \text{Similarly } Au_2 = 0. \\
> &\implies A\,[\,p\ \ u_1\ \ u_2\,] = [\,b\ \ 0\ \ 0\,], \quad X = [\,p\ \ u_1\ \ u_2\,] = \begin{bmatrix} 1 & 1 & 2 \\ 1 & 2 & 2 \\ -1 & 0 & -1 \end{bmatrix}. \\[4pt]
> &\text{Find } r = [\,r_1\ \ r_2\ \ r_3\,] \text{ with } rX = [\,1\ \ 0\ \ 0\,]: \\
> &\quad \begin{cases} r_1 + r_2 - r_3 = 1 \\ r_1 + 2r_2 = 0 \\ 2r_1 + 2r_2 - r_3 = 0 \end{cases} \implies r_1 = -2r_2,\ \ r_3 = 2r_1 + 2r_2 = -2r_2,\ \ r_1 + r_2 - r_3 = r_2 = 1 \\
> &\quad \implies r = [\,-2\ \ 1\ \ {-2}\,] \text{ (unique, so } X \text{ is invertible and } r \text{ is row 1 of } X^{-1}). \\[4pt]
> &A = [\,b\ \ 0\ \ 0\,]X^{-1} = b\,[\,1\ \ 0\ \ 0\,]X^{-1} = b\,r = \begin{bmatrix} 1 \\ 3 \\ 0 \\ 2 \end{bmatrix}\begin{bmatrix} -2 & 1 & -2 \end{bmatrix} = \begin{bmatrix} -2 & 1 & -2 \\ -6 & 3 & -6 \\ 0 & 0 & 0 \\ -4 & 2 & -4 \end{bmatrix}
> \end{aligned}
> $$
>
> \# Check: $rp = -2 + 1 + 2 = 1$, $ru_1 = -2 + 2 + 0 = 0$, $ru_2 = -4 + 2 + 2 = 0$, so $Ap = b$, $Au_1 = Au_2 = 0$. Conversely $Ax = b \iff (rx)\,b = b \iff rx = 1$, a plane in $\mathbb{R}^3$, which is exactly $p + \alpha u_1 + \beta u_2$. Finding the one row $r$ is shorter than computing all of $X^{-1}$.

> [!warning] A is 4 by 3
> The graded answer in the source computes $A = bX^{-1}$ as a $3 \times 3$ product with a wrong $X^{-1}$. Since $b$ has 4 entries and $x$ has 3, $A$ must be $4 \times 3$.

## Q8 Inverse of I plus B

Question: [[LA1 Midterm 114-1 Questions#Q8 Inverse of I plus B|Q8]]

> [!solution] Solution
> $$
> \begin{aligned}
> &I + A = \begin{bmatrix} 2 & 0 & 0 & 0 \\ 2 & 4 & 0 & 0 \\ 0 & -4 & 6 & 0 \\ 0 & 0 & -6 & 8 \end{bmatrix}:\ \text{lower triangular, diagonal } 2, 4, 6, 8 \ne 0 \implies \text{invertible.} \\[4pt]
> &I + B = (I + A)^{-1}(I + A) + (I + A)^{-1}(I - A) = (I + A)^{-1}\big[(I + A) + (I - A)\big] = (I + A)^{-1}(2I) = 2(I + A)^{-1} \\[4pt]
> &\implies (I + B)^{-1} = \tfrac{1}{2}(I + A) = \begin{bmatrix} 1 & 0 & 0 & 0 \\ 1 & 2 & 0 & 0 \\ 0 & -2 & 3 & 0 \\ 0 & 0 & -3 & 4 \end{bmatrix}
> \end{aligned}
> $$
>
> \# Write $I = (I + A)^{-1}(I + A)$ to factor out $(I + A)^{-1}$ on the left. Then $\big(2(I + A)^{-1}\big)^{-1} = \tfrac{1}{2}(I + A)$, because $(cX)^{-1} = \tfrac{1}{c}X^{-1}$ for $c \ne 0$. No inverse has to be computed.

## Q9 Inverse by Row Reduction

Question: [[LA1 Midterm 114-1 Questions#Q9 Inverse by Row Reduction|Q9]]

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
> \# Say where $P$ comes from: each row operation is multiplication on the left by an elementary matrix. The right half records $P$ itself, because $PI = P$.

> [!solution] Solution
> **(b)**
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|ccc} 2 & 1 & 4 & 1 & 0 & 0 \\ 3 & 2 & 5 & 0 & 1 & 0 \\ 0 & -1 & 1 & 0 & 0 & 1 \end{array}\right] \overset{R_2 \to R_2 - R_1}{\sim} \left[\begin{array}{ccc|ccc} 2 & 1 & 4 & 1 & 0 & 0 \\ 1 & 1 & 1 & -1 & 1 & 0 \\ 0 & -1 & 1 & 0 & 0 & 1 \end{array}\right] \\[6pt]
> &\overset{R_1 \leftrightarrow R_2}{\sim} \left[\begin{array}{ccc|ccc} 1 & 1 & 1 & -1 & 1 & 0 \\ 2 & 1 & 4 & 1 & 0 & 0 \\ 0 & -1 & 1 & 0 & 0 & 1 \end{array}\right] \overset{R_2 \to R_2 - 2R_1}{\sim} \left[\begin{array}{ccc|ccc} 1 & 1 & 1 & -1 & 1 & 0 \\ 0 & -1 & 2 & 3 & -2 & 0 \\ 0 & -1 & 1 & 0 & 0 & 1 \end{array}\right] \\[6pt]
> &\overset{R_3 \to R_3 - R_2}{\sim} \left[\begin{array}{ccc|ccc} 1 & 1 & 1 & -1 & 1 & 0 \\ 0 & -1 & 2 & 3 & -2 & 0 \\ 0 & 0 & -1 & -3 & 2 & 1 \end{array}\right] \overset{R_3 \to -R_3}{\sim} \left[\begin{array}{ccc|ccc} 1 & 1 & 1 & -1 & 1 & 0 \\ 0 & -1 & 2 & 3 & -2 & 0 \\ 0 & 0 & 1 & 3 & -2 & -1 \end{array}\right] \\[6pt]
> &\overset{\substack{R_2 \to R_2 - 2R_3 \\ R_1 \to R_1 - R_3}}{\sim} \left[\begin{array}{ccc|ccc} 1 & 1 & 0 & -4 & 3 & 1 \\ 0 & -1 & 0 & -3 & 2 & 2 \\ 0 & 0 & 1 & 3 & -2 & -1 \end{array}\right] \overset{R_2 \to -R_2}{\sim} \left[\begin{array}{ccc|ccc} 1 & 1 & 0 & -4 & 3 & 1 \\ 0 & 1 & 0 & 3 & -2 & -2 \\ 0 & 0 & 1 & 3 & -2 & -1 \end{array}\right] \\[6pt]
> &\overset{R_1 \to R_1 - R_2}{\sim} \left[\begin{array}{ccc|ccc} 1 & 0 & 0 & -7 & 5 & 3 \\ 0 & 1 & 0 & 3 & -2 & -2 \\ 0 & 0 & 1 & 3 & -2 & -1 \end{array}\right] \implies A^{-1} = \begin{bmatrix} -7 & 5 & 3 \\ 3 & -2 & -2 \\ 3 & -2 & -1 \end{bmatrix}
> \end{aligned}
> $$
>
> \# $R_2 \to R_2 - R_1$ first makes a row starting with $1$, which avoids fractions. Check one entry: row 1 of $A$ times column 1 of $A^{-1}$ is $2(-7) + 1 \cdot 3 + 4 \cdot 3 = 1$.

## Q10 A Minus Its Transpose Is Skew-Symmetric

Question: [[LA1 Midterm 114-1 Questions#Q10 A Minus Its Transpose Is Skew-Symmetric|Q10]]

> [!proof] Proof
> $$
> \begin{aligned}
> &A: n \times n \implies A - A^T \text{ is defined and } n \times n. \\
> &(A - A^T)^T = A^T - (A^T)^T = A^T - A = -(A - A^T). \\
> &\text{Hence } A - A^T \text{ is skew-symmetric.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Uses $(X - Y)^T = X^T - Y^T$ and $(A^T)^T = A$. Similarly $A + A^T$ is symmetric, and $A = \tfrac{1}{2}(A + A^T) + \tfrac{1}{2}(A - A^T)$.

## Q11 Row Equivalence and Gaussian Elimination

Question: [[LA1 Midterm 114-1 Questions#Q11 Row Equivalence and Gaussian Elimination|Q11]]

> [!proof] Proof of (1)
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
> \# The first line answers "why does $P$ exist?": row operations are multiplications by elementary matrices.

> [!solution] Solution
> **(2)**
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 2 & 1 & -3 & 0 \\ 6 & 3 & -8 & 0 \\ 2 & -1 & 5 & -4 \end{array}\right] \overset{\substack{R_2 \to R_2 - 3R_1 \\ R_3 \to R_3 - R_1}}{\sim} \left[\begin{array}{ccc|c} 2 & 1 & -3 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & -2 & 8 & -4 \end{array}\right] \overset{R_2 \leftrightarrow R_3}{\sim} \left[\begin{array}{ccc|c} 2 & 1 & -3 & 0 \\ 0 & -2 & 8 & -4 \\ 0 & 0 & 1 & 0 \end{array}\right] \\[6pt]
> &x_3 = 0 \\
> &-2x_2 + 8x_3 = -4 \implies x_2 = 2 \\
> &2x_1 + x_2 - 3x_3 = 0 \implies 2x_1 = -2 \implies x_1 = -1 \\
> &\implies x = \begin{bmatrix} -1 \\ 2 \\ 0 \end{bmatrix}
> \end{aligned}
> $$

## Q12 A Commutator Equal to A

Question: [[LA1 Midterm 114-1 Questions#Q12 A Commutator Equal to A|Q12]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Suppose } A \text{ is invertible.} \\
> &AB - BA = A \implies A^{-1}(AB - BA) = A^{-1}A \implies B - A^{-1}BA = I. \\
> &\implies \operatorname{tr}(B) - \operatorname{tr}(A^{-1}BA) = \operatorname{tr}(I) = n. \\
> &\operatorname{tr}(A^{-1}BA) = \operatorname{tr}\big((A^{-1}B)A\big) = \operatorname{tr}\big(A(A^{-1}B)\big) = \operatorname{tr}(B) \quad (\operatorname{tr}(XY) = \operatorname{tr}(YX)) \\
> &\implies 0 = n \quad (\rightarrow\leftarrow) \\
> &\text{Hence } A \text{ is singular.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The trace of $AB - BA = A$ itself gives only $\operatorname{tr}(A) = 0$, which does not make $A$ singular. Multiplying by $A^{-1}$ first turns the right side into $I$, whose trace is $n \ne 0$. Such $A$ exist: $A = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$, $B = \begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix}$ give $AB - BA = A$.

> [!warning] The step AB equals BA
> The graded answer in the source writes "if $A$ is invertible, then $AB = BA$", which does not follow from anything; the trace is what produces the contradiction.

## Q13 Left Inverse and an Inverse Formula

Question: [[LA1 Midterm 114-1 Questions#Q13 Left Inverse and an Inverse Formula|Q13]]

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

> [!proof] Proof of (b)
> $$
> \begin{aligned}
> &\text{Let } M = B(A + B)^{-1}A. \\
> &M(A^{-1} + B^{-1}) = B(A + B)^{-1}A(A^{-1} + B^{-1}) = B(A + B)^{-1}(I + AB^{-1}) \\
> &\hphantom{M(A^{-1} + B^{-1})} = B(A + B)^{-1}(B + A)B^{-1} = BIB^{-1} = I. \\
> &\therefore M \text{ is a left inverse of } A^{-1} + B^{-1} \overset{\text{(a)}}{\implies} A^{-1} + B^{-1} \text{ is invertible and} \\
> &\qquad (A^{-1} + B^{-1})^{-1} = M = B(A + B)^{-1}A. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Factor $I + AB^{-1} = (B + A)B^{-1}$: $B^{-1}$ comes out on the right, because it stands on the right of $A$. Then $(A + B)^{-1}(A + B) = I$ cancels in the middle.

## Q14 Idempotent Matrix

Question: [[LA1 Midterm 114-1 Questions#Q14 Idempotent Matrix|Q14]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Try } (I - cA)^{-1} = I + kA,\ k \text{ a scalar.} \\
> &(I - cA)(I + kA) = I + kA - cA - ckA^2 = I + (k - c - ck)A \quad (A^2 = A) \\
> &= I \iff k(1 - c) = c \iff k = \frac{c}{1 - c} \quad (c \ne 1). \\
> &(I + kA)(I - cA) = I + (k - c - ck)A = I \text{ as well.} \\
> &\implies (I - cA)^{-1} = I + \frac{c}{1 - c}A.
> \end{aligned}
> $$
>
> \# Guess the inverse in the form $I + kA$: every power of $A$ is $A$, so the products stay of this form. Formally, $\tfrac{1}{1 - cx} = 1 + cx + c^2x^2 + \cdots$ with every $x^j$ replaced by $A$ gives $I + (c + c^2 + \cdots)A = I + \tfrac{c}{1 - c}A$. For $c = 1$ and $A \ne O$, $A(I - A) = A - A^2 = O$, so $I - A$ is singular.
