---
course: [LA1]
chapter: ["1.3", "1.5"]
tags: [linear-algebra, homework, solutions, matrix-algebra, matrix-inverse]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-09-29
questions: "[[LA1 HW 1.3 1.5 Questions]]"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.20\|FB 1.3.20]] | $\begin{bmatrix} 1 & -1 & 2 & 5 \\ -1 & 4 & -7 & 8 \\ 2 & -7 & -1 & 6 \\ 5 & 8 & 6 & 3 \end{bmatrix}$ |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.22\|FB 1.3.22]] | Proof |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.24\|FB 1.3.24]] | $\mathbf{c}A = c_1\mathbf{r}_1 + \cdots + c_m\mathbf{r}_m$, a combination of the rows of $A$ |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.37\|FB 1.3.37]] | Proof |
| [[LA1 HW 1.3 1.5 Questions#FB 1.3.40\|FB 1.3.40]] | a. Proof; b. $(A^n)^T = (A^T)^n$ for every positive integer $n$ |
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
> Facts about the [[Transpose|transpose]] and products used below (FB §1.3, Exercises 29–34):
> - Size rule: if $A$ is $m \times n$ and $B$ is $n \times s$, then $AB$ is $m \times s$. The product is defined only when the inner sizes match.
> - $(A^T)^T = A$ (Exercise 30).
> - $(A+B)^T = A^T + B^T$ (Exercise 31).
> - $(rA)^T = rA^T$, because the $(i, j)$-entry of both sides is $r\,a_{ji}$.
> - $(AB)^T = B^TA^T$ (Exercise 32).
> - $A(B+C) = AB + AC$ (Exercise 29) and $(AB)C = A(BC)$ (Exercise 33).

### FB 1.3.20
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.20|FB 1.3.20]]

> [!solution] Solution
> A matrix is [[Symmetric Matrix|symmetric]] when $A^T = A$, that is, when $a_{ij} = a_{ji}$ for all $i$ and $j$: each entry equals its mirror image across the main diagonal. Every missing entry has a given mirror entry.
>
> | Missing entry | Must equal | Value |
> | --- | --- | --- |
> | $a_{13}$ | $a_{31}$ | $2$ |
> | $a_{21}$ | $a_{12}$ | $-1$ |
> | $a_{23}$ | $a_{32}$ | $-7$ |
> | $a_{34}$ | $a_{43}$ | $6$ |
> | $a_{41}$ | $a_{14}$ | $5$ |
> | $a_{42}$ | $a_{24}$ | $8$ |
>
> $$
> \begin{bmatrix} 1 & -1 & 2 & 5 \\ -1 & 4 & -7 & 8 \\ 2 & -7 & -1 & 6 \\ 5 & 8 & 6 & 3 \end{bmatrix}
> $$

### FB 1.3.22
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.22|FB 1.3.22]]

> [!proof] Proof
> Both parts follow from the size rule for products.
>
> **a.** A row vector with $m$ components is a $1 \times m$ matrix. For $\mathbf{x}A$ to be defined, $A$ must have $m$ rows, so $A$ is $m \times n$ for some $n$. Then $\mathbf{x}A$ has size $(1 \times m)(m \times n) = 1 \times n$. A matrix with a single row is a row vector with $n$ components:
> $$
> \mathbf{x}A = \left[\ \sum_{k=1}^{m} x_k a_{k1},\ \ \sum_{k=1}^{m} x_k a_{k2},\ \ \dots,\ \ \sum_{k=1}^{m} x_k a_{kn}\ \right]. \qquad \blacksquare
> $$
>
> **b.** A column vector with $n$ components is an $n \times 1$ matrix. For $A\mathbf{y}$ to be defined, $A$ must have $n$ columns, so $A$ is $m \times n$ for some $m$. Then $A\mathbf{y}$ has size $(m \times n)(n \times 1) = m \times 1$. A matrix with a single column is a column vector with $m$ components; its $i$th component is $\sum_{k=1}^{n} a_{ik}y_k$. $\blacksquare$

> [!proof] Alternative proof of b.
> $(A\mathbf{y})^T = \mathbf{y}^TA^T$ is a row vector times a matrix, so it is a row vector by part a. Transposing it back gives a column vector. $\blacksquare$

### FB 1.3.24
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.24|FB 1.3.24]]

> [!solution] Solution
> Let $\mathbf{c} = [c_1, c_2, \dots, c_m]$ and let $A$ be $m \times n$ with row vectors $\mathbf{r}_1, \dots, \mathbf{r}_m$. Then
> $$
> \boxed{\mathbf{c}A = c_1\mathbf{r}_1 + c_2\mathbf{r}_2 + \cdots + c_m\mathbf{r}_m}.
> $$
> So $\mathbf{c}A$ is a [[Linear Combination|linear combination]] of the **row vectors** of $A$, and the coefficient of the $i$th row of $A$ is $c_i$.
>
> **Justification, following the hint.** By Exercise 32,
> $$
> (\mathbf{c}A)^T = A^T\mathbf{c}^T.
> $$
> Here $\mathbf{c}^T$ is the column vector with components $c_1, \dots, c_m$, and the $i$th column of $A^T$ is $\mathbf{r}_i^{\,T}$. By the column-combination rule for a matrix times a column vector,
> $$
> (\mathbf{c}A)^T = A^T\mathbf{c}^T = c_1\mathbf{r}_1^{\,T} + c_2\mathbf{r}_2^{\,T} + \cdots + c_m\mathbf{r}_m^{\,T}.
> $$
> Transposing both sides, using $(X+Y)^T = X^T + Y^T$, $(rX)^T = rX^T$ and $(X^T)^T = X$, gives
> $$
> \mathbf{c}A = \big((\mathbf{c}A)^T\big)^T = c_1\mathbf{r}_1 + c_2\mathbf{r}_2 + \cdots + c_m\mathbf{r}_m.
> $$
>
> **Direct check.** The $j$th entry of $\mathbf{c}A$ is $\sum_{i=1}^{m} c_i a_{ij}$, which is also the $j$th entry of $\sum_{i=1}^{m} c_i\mathbf{r}_i$.

> [!example] Example
> $$
> [\,2,\ -1\,]\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix} = 2\,[1, 2, 3] + (-1)\,[4, 5, 6] = [-2, -1, 0].
> $$

### FB 1.3.37
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.37|FB 1.3.37]]

> [!proof] Proof
> Both $H_n^T$ and $H_n$ are $n \times n$. For all $i, j \in \{1, \dots, n\}$,
> $$
> (H_n^T)_{ij} = h_{ji} = \frac{1}{j+i-1} = \frac{1}{i+j-1} = h_{ij},
> $$
> by the definition of the transpose and because $j + i = i + j$. Every entry of $H_n^T$ equals the matching entry of $H_n$, so $H_n^T = H_n$. $\blacksquare$

> [!example] Example
> $$
> H_3 = \begin{bmatrix} 1 & \tfrac{1}{2} & \tfrac{1}{3} \\[2pt] \tfrac{1}{2} & \tfrac{1}{3} & \tfrac{1}{4} \\[2pt] \tfrac{1}{3} & \tfrac{1}{4} & \tfrac{1}{5} \end{bmatrix}
> $$
> The entry $h_{ij}$ depends only on $i + j$, so the entries are constant along each anti-diagonal.

### FB 1.3.40
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.40|FB 1.3.40]]

> [!proof] Proof
> $A$ is square, so every power of $A$ is defined. We use Exercise 32: $(XY)^T = Y^TX^T$.
>
> **a.**
> $$
> \begin{aligned}
> (A^2)^T &= (AA)^T = A^TA^T = (A^T)^2, \\
> (A^3)^T &= (A^2A)^T = A^T(A^2)^T = A^T(A^T)^2 = (A^T)^3. \qquad \blacksquare
> \end{aligned}
> $$
>
> **b.** *Generalization:* if $A$ is a square matrix, then $(A^n)^T = (A^T)^n$ for every positive integer $n$. We prove it by induction on $n$. Let $P(n)$ be the statement $(A^n)^T = (A^T)^n$.
>
> *Base case* ($n = 1$): $(A^1)^T = A^T = (A^T)^1$.
>
> *Inductive step:* assume that $P(k)$ holds for some $k \ge 1$, that is, $(A^k)^T = (A^T)^k$. Then
> $$
> (A^{k+1})^T \overset{(1)}{=} (A^kA)^T \overset{(2)}{=} A^T(A^k)^T \overset{(3)}{=} A^T(A^T)^k \overset{(4)}{=} (A^T)^{k+1}.
> $$
> 1. $A^{k+1} = A^kA$ by associativity.
> 2. Exercise 32.
> 3. The inductive hypothesis.
> 4. Associativity again.
>
> So $P(k+1)$ holds, and by induction $P(n)$ is true for every positive integer $n$. $\blacksquare$

### FB 1.3.41
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.41|FB 1.3.41]]

> [!proof] Proof
> **a.** Let $\mathbf{a}_1, \dots, \mathbf{a}_n$ be the column vectors of $A$. By the column-combination rule (FB §1.3, Summary item 3), $A\mathbf{e}_j$ is the linear combination of the columns of $A$ whose coefficients are the components of $\mathbf{e}_j$:
> $$
> A\mathbf{e}_j = 0\,\mathbf{a}_1 + \cdots + 0\,\mathbf{a}_{j-1} + 1\,\mathbf{a}_j + 0\,\mathbf{a}_{j+1} + \cdots + 0\,\mathbf{a}_n = \mathbf{a}_j.
> $$
> Entry by entry: the $i$th component of $A\mathbf{e}_j$ is $\sum_{k=1}^{n} a_{ik}(\mathbf{e}_j)_k = a_{ij}$, because $(\mathbf{e}_j)_k = 0$ for $k \ne j$ and $(\mathbf{e}_j)_j = 1$. So $A\mathbf{e}_j = [a_{1j}, a_{2j}, \dots, a_{mj}]^T$, the $j$th column of $A$. $\blacksquare$
>
> **b. i.** Let $A$ be $m \times n$ with $A\mathbf{x} = \mathbf{0}$ for every $\mathbf{x} \in \mathbb{R}^n$. In particular, this holds for $\mathbf{x} = \mathbf{e}_1, \dots, \mathbf{e}_n$. By part a,
> $$
> j\text{th column of } A = A\mathbf{e}_j = \mathbf{0}, \qquad j = 1, \dots, n.
> $$
> Every column of $A$ is the zero vector, so $A = O$. $\blacksquare$
>
> **b. ii.** Suppose $A\mathbf{x} = B\mathbf{x}$ for every $\mathbf{x}$. By the distributive law,
> $$
> (A - B)\mathbf{x} = A\mathbf{x} - B\mathbf{x} = \mathbf{0} \quad \text{for every } \mathbf{x}.
> $$
> Part i applied to the matrix $A - B$ gives $A - B = O$, so $A = B$. $\blacksquare$

> [!warning] "For all $\mathbf{x}$" is essential
> A single vector is not enough. For example, $\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}\begin{bmatrix} 0 \\ 1 \end{bmatrix} = \mathbf{0}$, but the matrix is not $O$.

### FB 1.3.44
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.3.44|FB 1.3.44]]

> [!proof] Proof
> **Existence.** Define
> $$
> B = \tfrac{1}{2}\left(A + A^T\right), \qquad C = \tfrac{1}{2}\left(A - A^T\right).
> $$
> Then $B + C = \tfrac{1}{2}A + \tfrac{1}{2}A^T + \tfrac{1}{2}A - \tfrac{1}{2}A^T = A$. By the transpose properties,
> $$
> \begin{aligned}
> B^T &= \tfrac{1}{2}\left(A^T + (A^T)^T\right) = \tfrac{1}{2}\left(A^T + A\right) = B, \\
> C^T &= \tfrac{1}{2}\left(A^T - (A^T)^T\right) = \tfrac{1}{2}\left(A^T - A\right) = -\tfrac{1}{2}\left(A - A^T\right) = -C.
> \end{aligned}
> $$
> So $B$ is symmetric and $C$ is [[Skew-Symmetric Matrix|skew symmetric]].
>
> **Uniqueness.** Suppose $A = B + C$, where $B$ is any symmetric matrix and $C$ is any skew-symmetric matrix. Taking the transpose gives
> $$
> A^T = B^T + C^T = B - C.
> $$
> Adding and subtracting the equations $A = B + C$ and $A^T = B - C$ gives $A + A^T = 2B$ and $A - A^T = 2C$, so $B = \tfrac{1}{2}(A + A^T)$ and $C = \tfrac{1}{2}(A - A^T)$. Any such decomposition is therefore the one constructed above, and the decomposition is unique. $\blacksquare$

> [!proof] Alternative proof of uniqueness
> If $B + C = B' + C'$ with $B$, $B'$ symmetric and $C$, $C'$ skew symmetric, then $M := B - B' = C' - C$ is both symmetric and skew symmetric. So $M = M^T = -M$, which gives $2M = O$ and $M = O$. $\blacksquare$

> [!example] Example
> $$
> \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} = \underbrace{\begin{bmatrix} 1 & \tfrac{5}{2} \\[2pt] \tfrac{5}{2} & 4 \end{bmatrix}}_{\text{symmetric}} + \underbrace{\begin{bmatrix} 0 & -\tfrac{1}{2} \\[2pt] \tfrac{1}{2} & 0 \end{bmatrix}}_{\text{skew symmetric}}
> $$

## FB §1.5 Inverses of Square Matrices

### FB 1.5.9
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.9|FB 1.5.9]]

> [!solution] Solution
> The matrix is the [[Diagonal Matrix|diagonal matrix]] $D = \operatorname{diag}(1, -1, 2, 3, 4, 5)$. Every diagonal entry is nonzero.
>
> **Gauss–Jordan.** Start from $[D \mid I]$. Multiply row 2 by $-1$, row 3 by $\tfrac{1}{2}$, row 4 by $\tfrac{1}{3}$, row 5 by $\tfrac{1}{4}$ and row 6 by $\tfrac{1}{5}$. This turns the left block into $I$, and the same operations turn the right block into
> $$
> D^{-1} = \begin{bmatrix} 1 & 0 & 0 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 & 0 & 0 \\ 0 & 0 & \tfrac{1}{2} & 0 & 0 & 0 \\ 0 & 0 & 0 & \tfrac{1}{3} & 0 & 0 \\ 0 & 0 & 0 & 0 & \tfrac{1}{4} & 0 \\ 0 & 0 & 0 & 0 & 0 & \tfrac{1}{5} \end{bmatrix}.
> $$
>
> **Check.** Diagonal matrices multiply entry by entry along the diagonal: $\operatorname{diag}(d_1, \dots, d_n)\operatorname{diag}(e_1, \dots, e_n) = \operatorname{diag}(d_1e_1, \dots, d_ne_n)$. So $DD^{-1} = \operatorname{diag}(1, 1, 1, 1, 1, 1) = I$, and $D^{-1}D = I$ in the same way.

> [!note] Note
> A diagonal matrix is [[Invertible Matrix|invertible]] if and only if every diagonal entry is nonzero. In that case its inverse is the diagonal matrix of the reciprocals.

### FB 1.5.16
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.16|FB 1.5.16]]

> [!solution] Solution
> Call the right-hand matrix $M$. Since $A^{-1}$ exists, multiply $AC = M$ on the **left** by $A^{-1}$:
> $$
> A^{-1}(AC) = (A^{-1}A)C = IC = C \implies C = A^{-1}M.
> $$
> Conversely, $A(A^{-1}M) = M$, so this $C$ works, and it is the only one. We never need to find $A$ itself.
> $$
> C = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix} \begin{bmatrix} 1 & 2 \\ 0 & 1 \\ 4 & 1 \end{bmatrix} = \begin{bmatrix} 1 + 0 + 4 & 2 + 2 + 1 \\ 0 + 0 + 4 & 0 + 3 + 1 \\ 4 + 0 + 8 & 8 + 1 + 2 \end{bmatrix} = \boxed{\begin{bmatrix} 5 & 5 \\ 4 & 4 \\ 12 & 11 \end{bmatrix}}
> $$

### FB 1.5.17
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.17|FB 1.5.17]]

> [!solution] Solution
> Call the right-hand matrix $M$. Multiply $ACA = M$ on the **left** and on the **right** by $A^{-1}$:
> $$
> A^{-1}(ACA)A^{-1} = (A^{-1}A)\,C\,(AA^{-1}) = C \implies C = A^{-1}MA^{-1}.
> $$
> Conversely, $A(A^{-1}MA^{-1})A = M$, so $C$ exists and is unique.
>
> **Step 1:** $A^{-1}M$.
> $$
> \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix} \begin{bmatrix} 2 & 1 & 3 \\ -1 & 2 & 2 \\ 2 & 1 & 4 \end{bmatrix} = \begin{bmatrix} 2 - 2 + 2 & 1 + 4 + 1 & 3 + 4 + 4 \\ 0 - 3 + 2 & 0 + 6 + 1 & 0 + 6 + 4 \\ 8 - 1 + 4 & 4 + 2 + 2 & 12 + 2 + 8 \end{bmatrix} = \begin{bmatrix} 2 & 6 & 11 \\ -1 & 7 & 10 \\ 11 & 8 & 22 \end{bmatrix}
> $$
>
> **Step 2:** $(A^{-1}M)A^{-1}$.
> $$
> \begin{bmatrix} 2 & 6 & 11 \\ -1 & 7 & 10 \\ 11 & 8 & 22 \end{bmatrix} \begin{bmatrix} 1 & 2 & 1 \\ 0 & 3 & 1 \\ 4 & 1 & 2 \end{bmatrix} = \begin{bmatrix} 2 + 0 + 44 & 4 + 18 + 11 & 2 + 6 + 22 \\ -1 + 0 + 40 & -2 + 21 + 10 & -1 + 7 + 20 \\ 11 + 0 + 88 & 22 + 24 + 22 & 11 + 8 + 44 \end{bmatrix}
> $$
> $$
> C = \boxed{\begin{bmatrix} 46 & 33 & 30 \\ 39 & 29 & 26 \\ 99 & 68 & 63 \end{bmatrix}}
> $$

> [!warning] Order matters
> $C = A^{-1}MA^{-1}$, **not** $(A^{-1})^2M$, because matrix multiplication is not commutative.

### FB 1.5.18
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.18|FB 1.5.18]]

> [!solution] Solution
> Take $B = 2I_3$. Then
> $$
> A(2I) = 2(AI) = 2A, \qquad B = \boxed{\begin{bmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2 \end{bmatrix}}.
> $$
> This choice works for any square matrix $A$.
>
> **Uniqueness.** Row-reduce $A$:
> $$
> \begin{bmatrix} 4 & 2 & 2 \\ 0 & 3 & 1 \\ 2 & 0 & 1 \end{bmatrix} \xrightarrow{R_3 - \frac{1}{2}R_1} \begin{bmatrix} 4 & 2 & 2 \\ 0 & 3 & 1 \\ 0 & -1 & 0 \end{bmatrix} \xrightarrow{R_3 + \frac{1}{3}R_2} \begin{bmatrix} 4 & 2 & 2 \\ 0 & 3 & 1 \\ 0 & 0 & \tfrac{1}{3} \end{bmatrix}
> $$
> There are three nonzero pivots, so $A$ is row equivalent to $I$ and $A$ is invertible. From $AB = 2A$ we get $B = A^{-1}(2A) = 2I$. So $B = 2I$ is the **only** solution.

### FB 1.5.19
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.19|FB 1.5.19]]

> [!solution] Solution
> Factor out $A$ on the left using the distributive law:
> $$
> A^2 + 2A = AA + A(2I) = A(A + 2I).
> $$
> So $B = A + 2I$ works:
> $$
> B = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 2 \\ 1 & 3 & 2 \end{bmatrix} + \begin{bmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2 \end{bmatrix} = \boxed{\begin{bmatrix} 3 & 2 & 1 \\ 0 & 3 & 2 \\ 1 & 3 & 4 \end{bmatrix}}
> $$
>
> **Uniqueness.** Row-reduce $A$:
> $$
> \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 2 \\ 1 & 3 & 2 \end{bmatrix} \xrightarrow{R_3 - R_1} \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 2 \\ 0 & 1 & 1 \end{bmatrix} \xrightarrow{R_3 - R_2} \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 2 \\ 0 & 0 & -1 \end{bmatrix}
> $$
> There are three nonzero pivots, so $A$ is invertible. Then $B = A^{-1}(A^2 + 2A) = A + 2I$ is the only solution.

> [!warning] Common mistake
> Writing $A^2 + 2A = A(A + 2)$ is meaningless, because "matrix $+$ scalar" is not defined. The identity matrix is needed: $A(A + 2I)$.

### FB 1.5.33
Question: [[LA1 HW 1.3 1.5 Questions#FB 1.5.33|FB 1.5.33]]

> [!solution] Solution
> Take $A = I_4$ and $B = -I_4$.
> - $A$ is invertible, with $I^{-1} = I$.
> - $B$ is invertible: $(-I)(-I) = I$, so $(-I)^{-1} = -I$.
> - $A + B = O_{4 \times 4}$ is singular: for every $4 \times 4$ matrix $X$, $OX = O \ne I$, so $O$ has no inverse.
>
> So a sum of invertible matrices does not have to be invertible.

> [!example] Example
> A less trivial pair: let $A = I_4$ and $B = \operatorname{diag}(-1, 1, 1, 1)$. $B$ is invertible because $B^2 = I$. But
> $$
> A + B = \operatorname{diag}(0, 2, 2, 2).
> $$
> Its first row is zero, so the first row of $(A+B)X$ is zero for every $X$, and $(A+B)X$ can never equal $I$. So $A + B$ is singular.

## FIS §1.3 Subspaces

> [!note] Notation
> This section follows FIS: the transpose of $A$ is $A^t$, the $(i, j)$-entry of $A$ is $A_{ij}$, and matrices use parentheses.

> [!note] Note
> Definitions used (FIS §1.3):
> - Transpose: $(A^t)_{ij} = A_{ji}$.
> - $A$ is **symmetric** if $A^t = A$.
> - An $n \times n$ matrix $M$ is **diagonal** if $M_{ij} = 0$ whenever $i \ne j$.
> - [[Trace]]: $\operatorname{tr}(M) = M_{11} + M_{22} + \cdots + M_{nn}$.

### FIS 1.3.2 (a)(d)(h)
Question: [[LA1 HW 1.3 1.5 Questions#FIS 1.3.2 (a)(d)(h)|FIS 1.3.2 (a)(d)(h)]]

> [!solution] Solution
> The rows of $A$ become the columns of $A^t$. All three matrices are square, so each has a trace.
>
> **(a)**
> $$
> A^t = \begin{pmatrix} -4 & 5 \\ 2 & -1 \end{pmatrix}, \qquad \operatorname{tr}(A) = -4 + (-1) = \boxed{-5}
> $$
>
> **(d)**
> $$
> A^t = \begin{pmatrix} 10 & 2 & -5 \\ 0 & -4 & 7 \\ -8 & 3 & 6 \end{pmatrix}, \qquad \operatorname{tr}(A) = 10 + (-4) + 6 = \boxed{12}
> $$
>
> **(h)**
> $$
> A^t = \begin{pmatrix} -4 & 0 & 6 \\ 0 & 1 & -3 \\ 6 & -3 & 5 \end{pmatrix} = A \quad (\text{the matrix is symmetric}), \qquad \operatorname{tr}(A) = -4 + 1 + 5 = \boxed{2}
> $$

> [!note] Note
> Transposing does not move the diagonal entries, so $\operatorname{tr}(A^t) = \operatorname{tr}(A)$. See FIS 2.3.13.

### FIS 1.3.6
Question: [[LA1 HW 1.3 1.5 Questions#FIS 1.3.6|FIS 1.3.6]]

> [!proof] Proof
> Let $A, B \in \mathsf{M}_{n \times n}(F)$ and $a, b \in F$. By the definitions of matrix addition and scalar multiplication,
> $$
> (aA + bB)_{ii} = aA_{ii} + bB_{ii} \qquad (1 \le i \le n).
> $$
> Therefore
> $$
> \begin{aligned}
> \operatorname{tr}(aA + bB) &= \sum_{i=1}^{n} (aA + bB)_{ii} && \text{(definition of the trace)} \\
> &= \sum_{i=1}^{n} \left(aA_{ii} + bB_{ii}\right) && \text{(entries of \(aA + bB\))} \\
> &= a\sum_{i=1}^{n} A_{ii} + b\sum_{i=1}^{n} B_{ii} && \text{(commutativity, associativity and distributivity in \(F\))} \\
> &= a\operatorname{tr}(A) + b\operatorname{tr}(B). && \text{(definition of the trace)} \qquad \blacksquare
> \end{aligned}
> $$

> [!tip] Intuition
> This says that $\operatorname{tr}\colon \mathsf{M}_{n \times n}(F) \to F$ is a **linear** map, in the language of Chapter 2.

### FIS 1.3.7
Question: [[LA1 HW 1.3 1.5 Questions#FIS 1.3.7|FIS 1.3.7]]

> [!proof] Proof
> Let $A \in \mathsf{M}_{n \times n}(F)$ be diagonal, so $A_{ij} = 0$ whenever $i \ne j$. We must show $A^t = A$, that is, $(A^t)_{ij} = A_{ij}$ for all $i$ and $j$. By definition, $(A^t)_{ij} = A_{ji}$.
> - **Case $i = j$:** $(A^t)_{ii} = A_{ii}$.
> - **Case $i \ne j$:** then $j \ne i$ too, so $A_{ji} = 0$ because $A$ is diagonal, and also $A_{ij} = 0$. Hence $(A^t)_{ij} = A_{ji} = 0 = A_{ij}$.
>
> Every entry agrees, so $A^t = A$ and $A$ is symmetric. $\blacksquare$

## FIS §2.3 Composition of Linear Transformations and Matrix Multiplication

### FIS 2.3.13
Question: [[LA1 HW 1.3 1.5 Questions#FIS 2.3.13|FIS 2.3.13]]

> [!proof] Proof
> **(1) $\operatorname{tr}(AB) = \operatorname{tr}(BA)$.** By the definition of the matrix product, $(AB)_{ij} = \sum_{k=1}^{n} A_{ik}B_{kj}$. So
> $$
> \operatorname{tr}(AB) = \sum_{i=1}^{n} (AB)_{ii} = \sum_{i=1}^{n}\sum_{k=1}^{n} A_{ik}B_{ki}.
> $$
> In the same way, $(BA)_{kk} = \sum_{i=1}^{n} B_{ki}A_{ik}$, so
> $$
> \operatorname{tr}(BA) = \sum_{k=1}^{n} (BA)_{kk} = \sum_{k=1}^{n}\sum_{i=1}^{n} B_{ki}A_{ik}.
> $$
> Multiplication in the field $F$ is commutative, so $B_{ki}A_{ik} = A_{ik}B_{ki}$, and a finite double sum can be added in either order. Therefore
> $$
> \operatorname{tr}(BA) = \sum_{k=1}^{n}\sum_{i=1}^{n} A_{ik}B_{ki} = \sum_{i=1}^{n}\sum_{k=1}^{n} A_{ik}B_{ki} = \operatorname{tr}(AB).
> $$
>
> **(2) $\operatorname{tr}(A) = \operatorname{tr}(A^t)$.** For each $i$, $(A^t)_{ii} = A_{ii}$, since transposition does not change the diagonal. So
> $$
> \operatorname{tr}(A^t) = \sum_{i=1}^{n} (A^t)_{ii} = \sum_{i=1}^{n} A_{ii} = \operatorname{tr}(A). \qquad \blacksquare
> $$

> [!example] Example
> Here $\operatorname{tr}(XY) = \operatorname{tr}(YX)$ even though $XY \ne YX$. Let $X = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}$ and $Y = \begin{pmatrix} 0 & 1 \\ 1 & 1 \end{pmatrix}$. Then
> $$
> XY = \begin{pmatrix} 2 & 3 \\ 4 & 7 \end{pmatrix} \ne \begin{pmatrix} 3 & 4 \\ 4 & 6 \end{pmatrix} = YX, \qquad \text{but } \operatorname{tr}(XY) = 9 = \operatorname{tr}(YX).
> $$

> [!note] Note
> The same proof works when $A$ is $m \times n$ and $B$ is $n \times m$. Then $AB$ is $m \times m$ and $BA$ is $n \times n$, but $\operatorname{tr}(AB) = \operatorname{tr}(BA)$ still holds.
