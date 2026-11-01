---
course: [LA1]
semester: "115-1"
chapter: ["1.3", "1.5"]
tags: [linear-algebra, homework, solutions, matrix-algebra, matrix-inverse]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-10-31
questions: "[[LA1 HW 1.3 1.5 Questions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.20\|FB 1.3.20]] | $\begin{bmatrix} 1 & -1 & 2 & 5 \\ -1 & 4 & -7 & 8 \\ 2 & -7 & -1 & 6 \\ 5 & 8 & 6 & 3 \end{bmatrix}$ |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.22\|FB 1.3.22]] | Proof |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.24\|FB 1.3.24]] | $\mathbf{c}A = c_1\mathbf{r}_1 + \cdots + c_m\mathbf{r}_m$, a combination of the rows of $A$ |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.37\|FB 1.3.37]] | Proof |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.40\|FB 1.3.40]] | a. Proof; b. $(A^k)^T = (A^T)^k$ for every $k \in \mathbb{N}$ |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.41\|FB 1.3.41]] | Proof |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.44\|FB 1.3.44]] | Proof; $B = \tfrac{1}{2}(A + A^T)$, $C = \tfrac{1}{2}(A - A^T)$ |
| [[LA1 HW 1.3 1.5 Questions#FB 1.5.9\|FB 1.5.9]] | $\operatorname{diag}\left(1, -1, \tfrac{1}{2}, \tfrac{1}{3}, \tfrac{1}{4}, \tfrac{1}{5}\right)$ |
| [[LA1 HW 1.3 1.5 Questions#FB 1.5.16\|FB 1.5.16]] | $C = \begin{bmatrix} 5 & 5 \\ 4 & 4 \\ 12 & 11 \end{bmatrix}$ |
| [[LA1 HW 1.3 1.5 Questions#FB 1.5.17\|FB 1.5.17]] | $C = \begin{bmatrix} 46 & 33 & 30 \\ 39 & 29 & 26 \\ 99 & 68 & 63 \end{bmatrix}$ |
| [[LA1 HW 1.3 1.5 Questions#FB 1.5.18\|FB 1.5.18]] | $B = 2I_3$ |
| [[LA1 HW 1.3 1.5 Questions#FB 1.5.19\|FB 1.5.19]] | $B = A + 2I = \begin{bmatrix} 3 & 2 & 1 \\ 0 & 3 & 2 \\ 1 & 3 & 4 \end{bmatrix}$ |
| [[LA1 HW 1.3 1.5 Questions#FB 1.5.33\|FB 1.5.33]] | $A = I_4$, $B = -I_4$ |
| [[LA1 HW 1.3 1.5 Questions#FIS 1.3.2 (a)(d)(h)\|FIS 1.3.2 (a)(d)(h)]] | (a) $\operatorname{tr} = -5$; (d) $\operatorname{tr} = 12$; (h) symmetric, $\operatorname{tr} = 2$ |
| [[LA1 HW 1.3 1.5 Questions#FIS 1.3.6\|FIS 1.3.6]] | Proof |
| [[LA1 HW 1.3 1.5 Questions#FIS 1.3.7\|FIS 1.3.7]] | Proof |
| [[LA1 HW 1.3 1.5 Questions#FIS 2.3.13\|FIS 2.3.13]] | Proof |

## FB §1.3 Matrices and Their Algebra

> [!note] Note
> The facts that the answers use.
> - $(A)_{ij}$ is the $(i, j)$-entry of $A$, as in lecture. $A = B$ $\iff$ same size and $(A)_{ij} = (B)_{ij}$ $\forall\, i, j$.
> - **Product**: $A$: $m \times n$, $B$: $n \times p$ $\implies$ $AB$: $m \times p$, $(AB)_{ij} = \sum_{k=1}^{n} (A)_{ik}(B)_{kj}$. $A\mathbf{b} = b_1\mathbf{a}_1 + \cdots + b_n\mathbf{a}_n$, where $\mathbf{a}_j$ is column $j$ of $A$.
> - **[[Transpose]]**: $(A^T)_{ij} = (A)_{ji}$; $(A^T)^T = A$, $(A + B)^T = A^T + B^T$, $(rA)^T = rA^T$, $(AB)^T = B^TA^T$.
> - $A$ is [[Symmetric Matrix|symmetric]] if $A^T = A$, [[Skew-Symmetric Matrix|skew symmetric]] if $A^T = -A$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FB 1.3.20
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.20|FB 1.3.20]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Let } A = [a_{ij}] \text{ be the matrix.} \\
> &A \text{ is symmetric} \iff A^T = A \iff a_{ij} = a_{ji}\ \ \forall\, i, j \\
> &\implies a_{13} = a_{31} = 2,\ \ a_{21} = a_{12} = -1,\ \ a_{23} = a_{32} = -7, \\
> &\hphantom{\implies}\ \ a_{34} = a_{43} = 6,\ \ a_{41} = a_{14} = 5,\ \ a_{42} = a_{24} = 8 \\
> &\text{Hence } A = \begin{bmatrix} 1 & -1 & 2 & 5 \\ -1 & 4 & -7 & 8 \\ 2 & -7 & -1 & 6 \\ 5 & 8 & 6 & 3 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# Every missing entry has its mirror entry across the main diagonal given; the diagonal entries are free. Check: row $i$ of the answer equals its column $i$.

### FB 1.3.22
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.22|FB 1.3.22]]

> [!proof] Proof
> **a.**
> $$
> \begin{aligned}
> &\text{Let } \mathbf{x}: 1 \times m. \\
> &\mathbf{x}A \text{ is defined} \implies A \text{ has } m \text{ rows} \implies A: m \times n \text{ for some } n \\
> &\implies \mathbf{x}A: 1 \times n \quad \text{(definition of the product)} \\
> &\text{Hence } \mathbf{x}A \text{ has one row, so it is a row vector.} \qquad \blacksquare
> \end{aligned}
> $$
> **b.**
> $$
> \begin{aligned}
> &\text{Let } \mathbf{y}: n \times 1. \\
> &A\mathbf{y} \text{ is defined} \implies A \text{ has } n \text{ columns} \implies A: m \times n \text{ for some } m \\
> &\implies A\mathbf{y}: m \times 1 \quad \text{(definition of the product)} \\
> &\text{Hence } A\mathbf{y} \text{ has one column, so it is a column vector.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# A vector is a matrix with one row or one column, so only the sizes matter: $(1 \times m)(m \times n) = 1 \times n$ and $(m \times n)(n \times 1) = m \times 1$. For b. one can also transpose: $(A\mathbf{y})^T = \mathbf{y}^TA^T$ is a row vector by a.

### FB 1.3.24
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.24|FB 1.3.24]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Let } \mathbf{c} = [c_1, \dots, c_m],\ A: m \times n \text{ with row vectors } \mathbf{r}_1, \dots, \mathbf{r}_m. \\
> &\implies \text{the columns of } A^T \text{ are } \mathbf{r}_1^T, \dots, \mathbf{r}_m^T, \text{ and } \mathbf{c}^T \text{ is a column vector.} \\
> &(\mathbf{c}A)^T = A^T\mathbf{c}^T = c_1\mathbf{r}_1^T + \cdots + c_m\mathbf{r}_m^T \\
> &\implies \mathbf{c}A = \big((\mathbf{c}A)^T\big)^T = \big(c_1\mathbf{r}_1^T + \cdots + c_m\mathbf{r}_m^T\big)^T = c_1\mathbf{r}_1 + \cdots + c_m\mathbf{r}_m \\
> &\text{Hence } \mathbf{c}A \text{ is a linear combination of the rows of } A, \text{ with coefficient } c_i \text{ for row } i.
> \end{aligned}
> $$
>
> \# Line 3 uses $(XY)^T = Y^TX^T$ and then the column rule for $A^T\mathbf{c}^T$; line 4 uses the transpose of a sum and of a scalar multiple, and $(X^T)^T = X$. In short, $\mathbf{c}A$ combines the rows of $A$, $A\mathbf{b}$ the columns. Check: $[\,2,\ -1\,]\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix} = 2[1, 2, 3] - [4, 5, 6] = [-2, -1, 0]$.

### FB 1.3.37
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.37|FB 1.3.37]]

> [!proof] Proof
> $$
> \begin{aligned}
> &H_n = [h_{ij}]: n \times n,\ \ h_{ij} = \frac{1}{i + j - 1} \implies H_n^T: n \times n \\
> &(H_n^T)_{ij} = h_{ji} = \frac{1}{j + i - 1} = \frac{1}{i + j - 1} = h_{ij} \quad \forall\, i, j \\
> &\implies H_n^T = H_n \\
> &\text{Hence } H_n \text{ is symmetric.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The middle step is $j + i = i + j$ in $\mathbb{R}$: $h_{ij}$ depends only on $i + j$, so interchanging $i$ and $j$ does not change it.

### FB 1.3.40
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.40|FB 1.3.40]]

> [!proof] Proof
> **a.**
> $$
> \begin{aligned}
> &\text{Let } A: n \times n. \text{ Using } (XY)^T = Y^TX^T: \\
> &(A^2)^T = (AA)^T = A^TA^T = (A^T)^2 \\
> &(A^3)^T = (A^2A)^T = A^T(A^2)^T = A^T(A^T)^2 = (A^T)^3 \qquad \blacksquare
> \end{aligned}
> $$
> **b.** If $A$ is a square matrix, then $(A^k)^T = (A^T)^k$ for every $k \in \mathbb{N}$.
> $$
> \begin{aligned}
> &k = 1:\ (A^1)^T = A^T = (A^T)^1. \\
> &\text{Suppose } (A^k)^T = (A^T)^k \text{ for some } k \in \mathbb{N}. \\
> &\implies (A^{k+1})^T = (A^kA)^T = A^T(A^k)^T = A^T(A^T)^k = (A^T)^{k+1} \\
> &\text{Hence, by induction, } (A^k)^T = (A^T)^k\ \ \forall\, k \in \mathbb{N}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Comparing entries would need the sums $(A^2)_{ij} = \sum_{l} (A)_{il}(A)_{lj}$; the rule $(XY)^T = Y^TX^T$ avoids them, as the hint says. The inductive step is the second line of a. with $2$ replaced by $k$; the third equality there is the induction hypothesis.

### FB 1.3.41
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.41|FB 1.3.41]]

> [!proof] Proof
> **a.**
> $$
> \begin{aligned}
> &A: m \times n,\ \mathbf{e}_j: n \times 1 \implies A\mathbf{e}_j: m \times 1 \\
> &(A\mathbf{e}_j)_{i} = \sum_{k=1}^{n} (A)_{ik}(\mathbf{e}_j)_{k} = (A)_{ij} \cdot 1 = (A)_{ij},\ \ i = 1, \dots, m \quad \big((\mathbf{e}_j)_{k} = 0 \text{ for } k \ne j\big) \\
> &\text{Hence } A\mathbf{e}_j = \begin{bmatrix} (A)_{1j} \\ \vdots \\ (A)_{mj} \end{bmatrix} \text{ is the } j\text{th column vector of } A. \qquad \blacksquare
> \end{aligned}
> $$
> **b. i.**
> $$
> \begin{aligned}
> &A: m \times n,\ A\mathbf{x} = \mathbf{0}\ \ \forall\, \mathbf{x} \in \mathbb{R}^n \\
> &\text{Take } \mathbf{x} = \mathbf{e}_j:\ j\text{th column of } A = A\mathbf{e}_j = \mathbf{0},\ \ j = 1, \dots, n \quad \text{(by a.)} \\
> &\implies (A)_{ij} = 0\ \ \forall\, i, j \\
> &\text{Hence } A = O. \qquad \blacksquare
> \end{aligned}
> $$
> **b. ii.**
> $$
> \begin{aligned}
> &A\mathbf{x} = B\mathbf{x}\ \ \forall\, \mathbf{x} \implies (A - B)\mathbf{x} = A\mathbf{x} - B\mathbf{x} = \mathbf{0}\ \ \forall\, \mathbf{x} \\
> &\implies A - B = O \quad \text{(by i. for } A - B) \\
> &\text{Hence } A = B. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# In b. "for all $\mathbf{x}$" is what lets us take $\mathbf{x} = \mathbf{e}_1, \dots, \mathbf{e}_n$; one vector is not enough: $\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}\begin{bmatrix} 0 \\ 1 \end{bmatrix} = \mathbf{0}$, but the matrix is not $O$. ii. is i. applied to $A - B$, through the distributive law $(A - B)\mathbf{x} = A\mathbf{x} - B\mathbf{x}$.

### FB 1.3.44
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.44|FB 1.3.44]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } A: n \times n. \\[4pt]
> &\text{Existence: let } B = \tfrac{1}{2}(A + A^T),\ C = \tfrac{1}{2}(A - A^T). \\
> &B + C = \tfrac{1}{2}A + \tfrac{1}{2}A^T + \tfrac{1}{2}A - \tfrac{1}{2}A^T = A \\
> &B^T = \tfrac{1}{2}\big(A^T + (A^T)^T\big) = \tfrac{1}{2}(A^T + A) = B \implies B \text{ is symmetric} \\
> &C^T = \tfrac{1}{2}\big(A^T - (A^T)^T\big) = \tfrac{1}{2}(A^T - A) = -C \implies C \text{ is skew symmetric} \\[4pt]
> &\text{Uniqueness: suppose } A = B' + C',\ B' \text{ symmetric},\ C' \text{ skew symmetric.} \\
> &\implies A^T = (B')^T + (C')^T = B' - C' \\
> &\implies A + A^T = 2B',\ \ A - A^T = 2C' \\
> &\implies B' = \tfrac{1}{2}(A + A^T) = B,\ \ C' = \tfrac{1}{2}(A - A^T) = C \\
> &\text{Hence } A = B + C \text{ with } B \text{ symmetric and } C \text{ skew symmetric, uniquely.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $C$ is the matrix of [[LA1 Quiz 03#Q1 Proof|Quiz 03 Q1]] times $\tfrac{1}{2}$. For uniqueness, start from any such decomposition and solve for its parts: adding and subtracting $A = B' + C'$ and $A^T = B' - C'$ leaves no choice. Example: $\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} = \begin{bmatrix} 1 & \tfrac{5}{2} \\ \tfrac{5}{2} & 4 \end{bmatrix} + \begin{bmatrix} 0 & -\tfrac{1}{2} \\ \tfrac{1}{2} & 0 \end{bmatrix}$.

## FB §1.5 Inverses of Square Matrices

> [!note] Note
> The facts that the answers use.
> - **[[Invertible Matrix|Invertible]]**: $A$: $n \times n$ and $\exists\, C$ s.t. $AC = CA = I$; then $A^{-1} = C$, and it is unique. *Singular* means not invertible.
> - $A$ is invertible $\iff$ $A \sim I$ $\iff$ an echelon form of $A$ has $n$ pivots.
> - $A(rB) = r(AB)$, $A(B + C) = AB + AC$, $(AB)C = A(BC)$.
> - $\operatorname{diag}(d_1, \dots, d_n)$ is the [[Diagonal Matrix|diagonal matrix]] with diagonal entries $d_1, \dots, d_n$.

### FB 1.5.9
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.9|FB 1.5.9]]

> [!solution] Solution
> $$
> \begin{aligned}
> &D = \operatorname{diag}(1, -1, 2, 3, 4, 5),\ \ C := \operatorname{diag}\left(1, -1, \tfrac{1}{2}, \tfrac{1}{3}, \tfrac{1}{4}, \tfrac{1}{5}\right) \\
> &(DC)_{ij} = \sum_{k=1}^{6} (D)_{ik}(C)_{kj} = (D)_{ii}(C)_{ij} = \begin{cases} (D)_{ii}(C)_{ii} = 1, & i = j \\ 0, & i \ne j \end{cases} \implies DC = I \\
> &\text{Similarly } CD = I. \\
> &\text{Hence } D \text{ is invertible and } D^{-1} = C = \begin{bmatrix} 1 & 0 & 0 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 & 0 & 0 \\ 0 & 0 & \tfrac{1}{2} & 0 & 0 & 0 \\ 0 & 0 & 0 & \tfrac{1}{3} & 0 & 0 \\ 0 & 0 & 0 & 0 & \tfrac{1}{4} & 0 \\ 0 & 0 & 0 & 0 & 0 & \tfrac{1}{5} \end{bmatrix}.
> \end{aligned}
> $$
>
> \# $(D)_{ik} = 0$ for $k \ne i$, so only $k = i$ is left in the sum; then $(C)_{ij} = 0$ for $j \ne i$. A diagonal matrix is invertible exactly when no diagonal entry is $0$, and its inverse takes the reciprocals. Row reduction gives the same: multiply rows $2, \dots, 6$ of $[D \mid I]$ by $-1, \tfrac{1}{2}, \tfrac{1}{3}, \tfrac{1}{4}, \tfrac{1}{5}$ to reach $[I \mid C]$.

### FB 1.5.16
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.16|FB 1.5.16]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Let } M = \begin{bmatrix} 1 & 2 \\ 0 & 1 \\ 4 & 1 \end{bmatrix}. \\
> &\because A^{-1} \text{ exists} \\
> &\therefore AC = M \implies C = (A^{-1}A)C = A^{-1}(AC) = A^{-1}M, \\
> &\hphantom{\therefore}\ \text{and } A(A^{-1}M) = (AA^{-1})M = M. \\
> &C = A^{-1}M = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix}\begin{bmatrix} 1 & 2 \\ 0 & 1 \\ 4 & 1 \end{bmatrix} = \begin{bmatrix} 1 + 0 + 4 & 2 + 2 + 1 \\ 0 + 0 + 4 & 0 + 3 + 1 \\ 4 + 0 + 8 & 8 + 1 + 2 \end{bmatrix} \\
> &\text{Hence } C = \begin{bmatrix} 5 & 5 \\ 4 & 4 \\ 12 & 11 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# Multiply by $A^{-1}$ on the left, the side where $A$ stands; $A$ itself is never needed. Line 4 shows that this $C$ really works, and line 3 that it is the only one.

### FB 1.5.17
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.17|FB 1.5.17]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Let } M = \begin{bmatrix} 2 & 1 & 3 \\ -1 & 2 & 2 \\ 2 & 1 & 4 \end{bmatrix}. \\
> &\because A^{-1} \text{ exists} \\
> &\therefore ACA = M \implies C = (A^{-1}A)C(AA^{-1}) = A^{-1}(ACA)A^{-1} = A^{-1}MA^{-1}, \\
> &\hphantom{\therefore}\ \text{and } A(A^{-1}MA^{-1})A = M. \\
> &A^{-1}M = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix}\begin{bmatrix} 2 & 1 & 3 \\ -1 & 2 & 2 \\ 2 & 1 & 4 \end{bmatrix} = \begin{bmatrix} 2 & 6 & 11 \\ -1 & 7 & 10 \\ 11 & 8 & 22 \end{bmatrix} \\
> &C = (A^{-1}M)A^{-1} = \begin{bmatrix} 2 & 6 & 11 \\ -1 & 7 & 10 \\ 11 & 8 & 22 \end{bmatrix}\begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix} \\
> &\hphantom{C} = \begin{bmatrix} 2 + 0 + 44 & 4 + 18 + 11 & 2 + 6 + 22 \\ -1 + 0 + 40 & -2 + 21 + 10 & -1 + 7 + 20 \\ 11 + 0 + 88 & 22 + 24 + 22 & 11 + 8 + 44 \end{bmatrix} \\
> &\text{Hence } C = \begin{bmatrix} 46 & 33 & 30 \\ 39 & 29 & 26 \\ 99 & 68 & 63 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# $A$ stands on both sides of $C$, so $A^{-1}$ goes on both sides: $C = A^{-1}MA^{-1}$, not $(A^{-1})^2M$, because matrix multiplication is not commutative.

### FB 1.5.18
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.18|FB 1.5.18]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Let } B = 2I_3. \\
> &AB = A(2I) = 2(AI) = 2A \\
> &\text{Hence } B = \begin{bmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# $B = 2I$ works for every square $A$. Here it is also the only one: row reduction of $A$ gives the pivots $4, 3, \tfrac{1}{3}$, so $A \sim I$ and $A$ is invertible, and $AB = 2A \implies B = A^{-1}(2A) = 2I$.

### FB 1.5.19
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.19|FB 1.5.19]]

> [!solution] Solution
> $$
> \begin{aligned}
> &A^2 + 2A = AA + A(2I) = A(A + 2I) \\
> &\implies B = A + 2I \text{ satisfies } AB = A^2 + 2A. \\
> &\text{Hence } B = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 2 \\ 1 & 3 & 2 \end{bmatrix} + \begin{bmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2 \end{bmatrix} = \begin{bmatrix} 3 & 2 & 1 \\ 0 & 3 & 2 \\ 1 & 3 & 4 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# Write $2A = A(2I)$, never $A(A + 2)$: a matrix plus a number is not defined. $A$ is invertible (pivots $1, 1, -1$), so $B = A^{-1}(A^2 + 2A) = A + 2I$ is the only one.

### FB 1.5.33
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.33|FB 1.5.33]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Let } A = I_4,\ B = -I_4. \\
> &I_4I_4 = I_4,\ (-I_4)(-I_4) = I_4 \implies A, B \text{ are invertible} \\
> &A + B = O,\ \ OX = O \ne I_4\ \ \forall\, X: 4 \times 4 \implies A + B \text{ is singular} \\
> &\text{Hence } A = I_4 \text{ and } B = -I_4 \text{ are such matrices.}
> \end{aligned}
> $$
>
> \# Same as [[LA1 Quiz 04#Q1 True or False|Quiz 04 Q1]] (a). A less trivial pair: $I_4$ and $\operatorname{diag}(-1, 1, 1, 1)$, whose sum $\operatorname{diag}(0, 2, 2, 2)$ has a zero first row, so the first row of $(A + B)X$ is zero for every $X$.

## FIS §1.3 Subspaces

> [!note] Notation
> FIS writes the transpose of $A$ as $A^t$, the $(i, j)$-entry of $A$ as $A_{ij}$, and matrices with parentheses.

> [!note] Note
> The facts that the answers use.
> - $(A^t)_{ij} = A_{ji}$; $A$ is symmetric if $A^t = A$.
> - An $n \times n$ matrix $A$ is diagonal if $A_{ij} = 0$ whenever $i \ne j$.
> - [[Trace]]: $\operatorname{tr}(A) = \sum_{i=1}^{n} A_{ii}$.

### FIS 1.3.2 (a)(d)(h)
Question: [[LA1 HW 1.3 1.5 Questions#FIS 1.3.2 (a)(d)(h)|FIS 1.3.2 (a)(d)(h)]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{(a)}\ \ A^t = \begin{pmatrix} -4 & 5 \\ 2 & -1 \end{pmatrix}, \quad \operatorname{tr}(A) = -4 + (-1) = -5 \\[6pt]
> &\text{(d)}\ \ A^t = \begin{pmatrix} 10 & 2 & -5 \\ 0 & -4 & 7 \\ -8 & 3 & 6 \end{pmatrix}, \quad \operatorname{tr}(A) = 10 + (-4) + 6 = 12 \\[6pt]
> &\text{(h)}\ \ A^t = \begin{pmatrix} -4 & 0 & 6 \\ 0 & 1 & -3 \\ 6 & -3 & 5 \end{pmatrix} = A, \quad \operatorname{tr}(A) = -4 + 1 + 5 = 2
> \end{aligned}
> $$
>
> \# Row $i$ of $A$ becomes column $i$ of $A^t$. The diagonal does not move, so $\operatorname{tr}(A^t) = \operatorname{tr}(A)$; (h) is symmetric.

### FIS 1.3.6
Question: [[LA1 HW 1.3 1.5 Questions#FIS 1.3.6|FIS 1.3.6]]

> [!proof] Proof
> Let $A, B \in \mathsf{M}_{n \times n}(F)$ and $a, b \in F$.
> $$
> \begin{aligned}
> \operatorname{tr}(aA + bB) &= \sum_{i=1}^{n} (aA + bB)_{ii} = \sum_{i=1}^{n} (aA_{ii} + bB_{ii}) \\
> &= a\sum_{i=1}^{n} A_{ii} + b\sum_{i=1}^{n} B_{ii} = a\operatorname{tr}(A) + b\operatorname{tr}(B). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The second equality is the definition of the sum and of the scalar multiple, entry $(i, i)$; the third uses commutativity, associativity and distributivity in $F$. So $\operatorname{tr}\colon \mathsf{M}_{n \times n}(F) \to F$ is linear.

### FIS 1.3.7
Question: [[LA1 HW 1.3 1.5 Questions#FIS 1.3.7|FIS 1.3.7]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } A \in \mathsf{M}_{n \times n}(F) \text{ be diagonal: } A_{ij} = 0 \text{ for } i \ne j. \\
> &i = j:\ (A^t)_{ii} = A_{ii} \\
> &i \ne j:\ (A^t)_{ij} = A_{ji} = 0 = A_{ij} \\
> &\implies (A^t)_{ij} = A_{ij}\ \ \forall\, i, j \implies A^t = A \\
> &\text{Hence } A \text{ is symmetric.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Off the diagonal both $A_{ij}$ and $A_{ji}$ are $0$, because $i \ne j$ also means $j \ne i$; on the diagonal the transpose moves nothing.

## FIS §2.3 Composition of Linear Transformations and Matrix Multiplication

### FIS 2.3.13
Question: [[LA1 HW 1.3 1.5 Questions#FIS 2.3.13|FIS 2.3.13]]

> [!proof] Proof
> $$
> \begin{aligned}
> \operatorname{tr}(AB) &= \sum_{i=1}^{n} (AB)_{ii} = \sum_{i=1}^{n}\sum_{k=1}^{n} A_{ik}B_{ki} \\
> &= \sum_{k=1}^{n}\sum_{i=1}^{n} B_{ki}A_{ik} = \sum_{k=1}^{n} (BA)_{kk} = \operatorname{tr}(BA) \\[6pt]
> \operatorname{tr}(A^t) &= \sum_{i=1}^{n} (A^t)_{ii} = \sum_{i=1}^{n} A_{ii} = \operatorname{tr}(A). \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Line 2 adds the same $n^2$ products in another order, with $A_{ik}B_{ki} = B_{ki}A_{ik}$ in $F$. The traces agree even when $AB \ne BA$: for $X = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}$, $Y = \begin{pmatrix} 0 & 1 \\ 1 & 1 \end{pmatrix}$, $XY = \begin{pmatrix} 2 & 3 \\ 4 & 7 \end{pmatrix} \ne \begin{pmatrix} 3 & 4 \\ 4 & 6 \end{pmatrix} = YX$, but both traces are $9$.
