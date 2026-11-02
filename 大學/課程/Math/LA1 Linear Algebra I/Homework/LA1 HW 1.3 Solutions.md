---
course: [LA1]
semester: "115-1"
chapter: ["1.3"]
tags: [linear-algebra, homework, solutions, matrix-algebra]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-11-02
questions: "[[LA1 HW 1.3 Questions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.3 Questions#FB 1.3.13\|FB 1.3.13]] | $\begin{bmatrix} 27 & -35 \\ -4 & 26 \end{bmatrix}$ |
| [[LA1 HW 1.3 Questions#FB 1.3.15\|FB 1.3.15]] | $\begin{bmatrix} 20 & -2 & -10 \\ -2 & 1 & 3 \\ -10 & 3 & 10 \end{bmatrix}$ |
| [[LA1 HW 1.3 Questions#FB 1.3.17\|FB 1.3.17]] | a. $\operatorname{diag}(4, 1, 1)$; b. $\operatorname{diag}(128, -1, 1)$ |
| [[LA1 HW 1.3 Questions#FB 1.3.19\|FB 1.3.19]] | $\mathbf{x}\mathbf{y} = [-14]$; $\mathbf{y}\mathbf{x} = \begin{bmatrix} -8 & 12 & -4 \\ 2 & -3 & 1 \\ -6 & 9 & -3 \end{bmatrix}$ |
| [[LA1 HW 1.3 Questions#FB 1.3.21\|FB 1.3.21]] | a. T; b. F; c. F; d. T; e. F; f. T; g. T; h. T; i. F; j. T |
| [[LA1 HW 1.3 Questions#FB 1.3.26\|FB 1.3.26]] | Proof |
| [[LA1 HW 1.3 Questions#FB 1.3.28\|FB 1.3.28]] | Proof |
| [[LA1 HW 1.3 Questions#FB 1.3.30\|FB 1.3.30]] | Proof |
| [[LA1 HW 1.3 Questions#FB 1.3.31\|FB 1.3.31]] | Proof |
| [[LA1 HW 1.3 Questions#FB 1.3.32\|FB 1.3.32]] | Proof |
| [[LA1 HW 1.3 Questions#FB 1.3.42\|FB 1.3.42]] | No: $(A + B)^2 = A^2 + AB + BA + B^2$; true $\iff$ $AB = BA$ |
| [[LA1 HW 1.3 Questions#FB 1.3.43\|FB 1.3.43]] | No: $(A + B)(A - B) = A^2 - AB + BA - B^2$; true $\iff$ $AB = BA$ |

Additional problems from the web, not assigned:

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.3 Questions#WEB 1.3.1\|WEB 1.3.1]] | Problem 1 F; Problem 3 T; Problem 6 T; Problem 10 F |
| [[LA1 HW 1.3 Questions#WEB 1.3.2\|WEB 1.3.2]] | Proof: $(AB)^T = B^TA^T = BA$ |
| [[LA1 HW 1.3 Questions#WEB 1.3.3\|WEB 1.3.3]] | Proof: $(ABA)^T = A^TB^TA^T = ABA$ |
| [[LA1 HW 1.3 Questions#WEB 1.3.4\|WEB 1.3.4]] | Proof: compare $DM$ and $MD$ for one well-chosen $M$ |
| [[LA1 HW 1.3 Questions#WEB 1.3.5\|WEB 1.3.5]] | (a) $\sum_{i=1}^{n}\sum_{k=1}^{n} a_{ik}b_{ik}$; (b), (c) Proofs |

## FB §1.3 Matrices and Their Algebra

> [!note] Note
> The facts that the answers use.
> - $(A)_{ij}$ is the $(i, j)$-entry of $A$, as in lecture. $A = B$ $\iff$ same size and $(A)_{ij} = (B)_{ij}$ $\forall\, i, j$.
> - **Sum and scalar multiple**: $(A + B)_{ij} = (A)_{ij} + (B)_{ij}$, $(rA)_{ij} = r(A)_{ij}$.
> - **Product**: $A$: $m \times n$, $B$: $n \times p$ $\implies$ $AB$: $m \times p$, $(AB)_{ij} = \sum_{k=1}^{n} (A)_{ik}(B)_{kj}$.
> - **[[Transpose]]**: $A$: $m \times n$ $\implies$ $A^T$: $n \times m$, $(A^T)_{ij} = (A)_{ji}$. $A$ is [[Symmetric Matrix|symmetric]] if $A^T = A$.
> - The proofs of 26–32 follow the lecture's pattern: sizes first, then $(\text{LHS})_{ij} = \cdots = (\text{RHS})_{ij}$, then $\forall\, i, j$. [[LA1 Quiz 02#Q2 Proof|Quiz 02 Q2]] was Exercise 26.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FB 1.3.13
Question: [[LA1 HW 1.3 Questions#FB 1.3.13|FB 1.3.13]]

> [!solution] Solution
> $$
> \begin{aligned}
> &2A - B = \begin{bmatrix} -4 & 2 & 6 \\ 8 & 0 & -2 \end{bmatrix} - \begin{bmatrix} 4 & 1 & -2 \\ 5 & -1 & 3 \end{bmatrix} = \begin{bmatrix} -8 & 1 & 8 \\ 3 & 1 & -5 \end{bmatrix} \\[4pt]
> &2A - B: 2 \times 3,\ \ D: 3 \times 2 \implies (2A - B)D \text{ is defined, } 2 \times 2. \\[4pt]
> &(2A - B)D = \begin{bmatrix} -8 & 1 & 8 \\ 3 & 1 & -5 \end{bmatrix}\begin{bmatrix} -4 & 2 \\ 3 & 5 \\ -1 & -3 \end{bmatrix} \\
> &\hphantom{(2A - B)D} = \begin{bmatrix} 32 + 3 - 8 & -16 + 5 - 24 \\ -12 + 3 + 5 & 6 + 5 + 15 \end{bmatrix} = \begin{bmatrix} 27 & -35 \\ -4 & 26 \end{bmatrix}
> \end{aligned}
> $$
>
> \# Check the sizes first: $(2 \times 3)(3 \times 2)$ is defined and gives $2 \times 2$. Entry $(i, j)$ is row $i$ of $2A - B$ times column $j$ of $D$; for example, entry $(1, 2)$ is $(-8)(2) + (1)(5) + (8)(-3) = -35$. By the distributive law, $2(AD) - BD$ gives the same matrix.

### FB 1.3.15
Question: [[LA1 HW 1.3 Questions#FB 1.3.15|FB 1.3.15]]

> [!solution] Solution
> $$
> \begin{aligned}
> &A^T = \begin{bmatrix} -2 & 4 \\ 1 & 0 \\ 3 & -1 \end{bmatrix}: 3 \times 2,\ \ A: 2 \times 3 \implies (A^T)A \text{ is defined, } 3 \times 3. \\[4pt]
> &(A^T)A = \begin{bmatrix} -2 & 4 \\ 1 & 0 \\ 3 & -1 \end{bmatrix}\begin{bmatrix} -2 & 1 & 3 \\ 4 & 0 & -1 \end{bmatrix} \\
> &\hphantom{(A^T)A} = \begin{bmatrix} 4 + 16 & -2 + 0 & -6 - 4 \\ -2 + 0 & 1 + 0 & 3 + 0 \\ -6 - 4 & 3 + 0 & 9 + 1 \end{bmatrix} = \begin{bmatrix} 20 & -2 & -10 \\ -2 & 1 & 3 \\ -10 & 3 & 10 \end{bmatrix}
> \end{aligned}
> $$
>
> \# Row $i$ of $A^T$ is column $i$ of $A$, so entry $(i, j)$ of $A^TA$ is (column $i$ of $A$) $\cdot$ (column $j$ of $A$). That is why the answer is symmetric; in general $(A^TA)^T = A^T(A^T)^T = A^TA$ by Exercises 32 and 30. The other order, $AA^T$, is $2 \times 2$.

### FB 1.3.17
Question: [[LA1 HW 1.3 Questions#FB 1.3.17|FB 1.3.17]]

> [!solution] Solution
> **a.**
> $$
> A^2 = \begin{bmatrix} 2 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 1 \end{bmatrix}\begin{bmatrix} 2 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 1 \end{bmatrix} = \begin{bmatrix} 2 \cdot 2 & 0 & 0 \\ 0 & (-1)(-1) & 0 \\ 0 & 0 & 1 \cdot 1 \end{bmatrix} = \begin{bmatrix} 4 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}
> $$
> **b.**
> $$
> \begin{aligned}
> &P, Q: 3 \times 3 \text{ diagonal} \implies (PQ)_{ij} = \sum_{k=1}^{3} (P)_{ik}(Q)_{kj} = (P)_{ii}(Q)_{ij} = \begin{cases} (P)_{ii}(Q)_{ii}, & i = j \\ 0, & i \ne j \end{cases} \\
> &\implies PQ \text{ is diagonal, with the products of the diagonal entries.} \\
> &\implies A^7 = \begin{bmatrix} 2^7 & 0 & 0 \\ 0 & (-1)^7 & 0 \\ 0 & 0 & 1^7 \end{bmatrix} = \begin{bmatrix} 128 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 1 \end{bmatrix}
> \end{aligned}
> $$
>
> \# In the sum only $k = i$ is left, because $(P)_{ik} = 0$ for $k \ne i$; then $(Q)_{ij} = 0$ for $j \ne i$. Applying this six times, $A^7 = A \cdot A \cdots A$ multiplies each diagonal entry by itself seven times. This shortcut is only for diagonal matrices; for a matrix that is not diagonal, such as the one in Exercise 18, compute $A^2$ by the row–column rule first.

### FB 1.3.19
Question: [[LA1 HW 1.3 Questions#FB 1.3.19|FB 1.3.19]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\mathbf{x}: 1 \times 3,\ \ \mathbf{y}: 3 \times 1 \implies \mathbf{x}\mathbf{y}: 1 \times 1,\ \ \mathbf{y}\mathbf{x}: 3 \times 3 \\[4pt]
> &\mathbf{x}\mathbf{y} = [-2, 3, -1]\begin{bmatrix} 4 \\ -1 \\ 3 \end{bmatrix} = [(-2)(4) + (3)(-1) + (-1)(3)] = [-14] \\[4pt]
> &\mathbf{y}\mathbf{x} = \begin{bmatrix} 4 \\ -1 \\ 3 \end{bmatrix}[-2, 3, -1] = \begin{bmatrix} 4(-2) & 4(3) & 4(-1) \\ (-1)(-2) & (-1)(3) & (-1)(-1) \\ 3(-2) & 3(3) & 3(-1) \end{bmatrix} = \begin{bmatrix} -8 & 12 & -4 \\ 2 & -3 & 1 \\ -6 & 9 & -3 \end{bmatrix}
> \end{aligned}
> $$
>
> \# $\mathbf{x}\mathbf{y}$ is the dot product $\mathbf{x}^T \cdot \mathbf{y}$ written as a $1 \times 1$ matrix. In $\mathbf{y}\mathbf{x}$ entry $(i, j)$ is $y_ix_j$: row $i$ is $y_i$ times $\mathbf{x}$. Here $\mathbf{x}\mathbf{y}$ and $\mathbf{y}\mathbf{x}$ do not even have the same size.

### FB 1.3.21
Question: [[LA1 HW 1.3 Questions#FB 1.3.21|FB 1.3.21]]

> [!solution] Solution
> - a. **T.** $A = B \implies AC$ and $BC$ are the same product $\implies AC = BC$.
> - b. **F.** $A = I_2$, $B = C = O_2$: $AC = O = BC$, but $A \ne B$.
> - c. **F.** $A = B = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} \ne O$, but $AB = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} = O$.
> - d. **T.** $A = A + (C - C) = (A + C) - C = (B + C) - C = B + (C - C) = B$.
> - e. **F.** $A = \begin{bmatrix} 1 & 0 \\ 0 & -1 \end{bmatrix}$: $A^2 = I$, but $A \ne \pm I$.
> - f. **T.** $b_{ii} = (A^2)_{ii} = \sum_{k=1}^{n} a_{ik}a_{ki} = \sum_{k=1}^{n} a_{ik}^{2} \ge 0$, since $a_{ki} = a_{ik}$ ($A$ symmetric).
> - g. **T.** $A$: $m \times n$, $B$: $n \times p$, $C$: $m \times p$. Any two square gives two of $m = n$, $n = p$, $m = p$, hence $m = n = p$, and all three are $n \times n$.
> - h. **T.** $C$: $m \times p$ is a column vector $\implies p = 1 \implies B$: $n \times 1$, a column vector.
> - i. **F.** $A = -I$: $A^2 = I$, but $A^3 = -I \ne I$.
> - j. **T.** $n = 2k$ $\implies$ $A^n = (A^2)^k = I^k = I$.
>
> \# d., e., i. are items (e), (c), (d) of [[LA1 Quiz 02#Q1 True or False|Quiz 02 Q1]]. b. against d.: a sum can always be cancelled (add $-C$), a product cannot, because $C$ need not have an inverse; b. fails even for $C \ne O$: $A = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$, $B = O$, $C = \begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix}$. f. uses real entries: a sum of squares of real numbers is $\ge 0$. h.: the number of columns of $C$ is the number of columns of $B$.

### FB 1.3.26
Question: [[LA1 HW 1.3 Questions#FB 1.3.26|FB 1.3.26]]

> [!proof] Proof
> Let $A, B, C$: $m \times n$. Both sides are $m \times n$, and for all $i, j$:
> $$
> \begin{aligned}
> \big((A + B) + C\big)_{ij} &= (A + B)_{ij} + (C)_{ij} && \text{(def. of sum)} \\
> &= \big((A)_{ij} + (B)_{ij}\big) + (C)_{ij} && \text{(def. of sum)} \\
> &= (A)_{ij} + \big((B)_{ij} + (C)_{ij}\big) && \text{(associativity in \(\mathbb{R}\))} \\
> &= (A)_{ij} + (B + C)_{ij} && \text{(def. of sum)} \\
> &= \big(A + (B + C)\big)_{ij} && \text{(def. of sum)}
> \end{aligned}
> $$
> $\forall\, i, j \implies (A + B) + C = A + (B + C)$. $\blacksquare$
>
> \# The only step that is not a definition is line 3, where the law of $\mathbb{R}$ does the work. This is the proof that [[LA1 Quiz 02#Q2 Proof|Quiz 02 Q2]] asked for: compare entries, never sum them.

### FB 1.3.28
Question: [[LA1 HW 1.3 Questions#FB 1.3.28|FB 1.3.28]]

> [!proof] Proof
> Let $A$: $m \times n$, $r, s \in \mathbb{R}$. Both sides are $m \times n$, and for all $i, j$:
> $$
> \begin{aligned}
> \big((rs)A\big)_{ij} &= (rs)(A)_{ij} && \text{(def. of scalar multiple)} \\
> &= r\big(s(A)_{ij}\big) && \text{(associativity in \(\mathbb{R}\))} \\
> &= r(sA)_{ij} && \text{(def. of scalar multiple)} \\
> &= \big(r(sA)\big)_{ij} && \text{(def. of scalar multiple)}
> \end{aligned}
> $$
> $\forall\, i, j \implies (rs)A = r(sA)$. $\blacksquare$
>
> \# Line 2 is associativity of multiplication in $\mathbb{R}$: $(rs)a = r(sa)$. Line 3 reads $s(A)_{ij}$ as the entry $(sA)_{ij}$.

### FB 1.3.30
Question: [[LA1 HW 1.3 Questions#FB 1.3.30|FB 1.3.30]]

> [!proof] Proof
> Let $A$: $m \times n$. Then $A^T$: $n \times m$, so $(A^T)^T$: $m \times n$, the size of $A$. For all $i, j$:
> $$
> \begin{aligned}
> \big((A^T)^T\big)_{ij} &= (A^T)_{ji} && \text{(def. of transpose)} \\
> &= (A)_{ij} && \text{(def. of transpose)}
> \end{aligned}
> $$
> $\forall\, i, j \implies (A^T)^T = A$. $\blacksquare$
>
> \# The definition $(X^T)_{ij} = (X)_{ji}$ is used twice: first with $X = A^T$, then with $X = A$ and the indices $j, i$. Transposing twice swaps $i$ and $j$ twice.

### FB 1.3.31
Question: [[LA1 HW 1.3 Questions#FB 1.3.31|FB 1.3.31]]

> [!proof] Proof
> Let $A, B$: $m \times n$. Then $(A + B)^T$ and $A^T + B^T$ are $n \times m$. For all $i, j$:
> $$
> \begin{aligned}
> \big((A + B)^T\big)_{ij} &= (A + B)_{ji} && \text{(def. of transpose)} \\
> &= (A)_{ji} + (B)_{ji} && \text{(def. of sum)} \\
> &= (A^T)_{ij} + (B^T)_{ij} && \text{(def. of transpose)} \\
> &= (A^T + B^T)_{ij} && \text{(def. of sum)}
> \end{aligned}
> $$
> $\forall\, i, j \implies (A + B)^T = A^T + B^T$. $\blacksquare$
>
> \# Lines 1–2 go from the left side down to entries of $A$ and $B$, lines 3–4 build the right side back up. The same chain with $(rA)_{ji} = r(A)_{ji}$ proves $(rA)^T = rA^T$.

### FB 1.3.32
Question: [[LA1 HW 1.3 Questions#FB 1.3.32|FB 1.3.32]]

> [!proof] Proof
> Let $A$: $m \times n$, $B$: $n \times p$. Then $AB$: $m \times p$, so $(AB)^T$: $p \times m$; and $B^T$: $p \times n$, $A^T$: $n \times m$, so $B^TA^T$: $p \times m$. For all $i = 1, \dots, p$, $j = 1, \dots, m$:
> $$
> \begin{aligned}
> \big((AB)^T\big)_{ij} &= (AB)_{ji} && \text{(def. of transpose)} \\
> &= \sum_{k=1}^{n} (A)_{jk}(B)_{ki} && \text{(def. of product)} \\
> &= \sum_{k=1}^{n} (B)_{ki}(A)_{jk} && \text{(commutativity in \(\mathbb{R}\))} \\
> &= \sum_{k=1}^{n} (B^T)_{ik}(A^T)_{kj} && \text{(def. of transpose)} \\
> &= (B^TA^T)_{ij} && \text{(def. of product)}
> \end{aligned}
> $$
> $\forall\, i, j \implies (AB)^T = B^TA^T$. $\blacksquare$
>
> \# Line 3 swaps the two numbers in each product so that the index $k$ sits in the middle, $(\,\cdot\,)_{ik}(\,\cdot\,)_{kj}$, which is the pattern of a product. The sizes explain the reversed order: $A^TB^T$ is $(n \times m)(p \times n)$, not even defined unless $m = p$.

### FB 1.3.42
Question: [[LA1 HW 1.3 Questions#FB 1.3.42|FB 1.3.42]]

> [!solution] Solution
> No.
> $$
> \begin{aligned}
> (A + B)^2 &= (A + B)(A + B) = A(A + B) + B(A + B) && \text{(distributive law)} \\
> &= A^2 + AB + BA + B^2 && \text{(distributive law)}
> \end{aligned}
> $$
> Counterexample: $A = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$, $B = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$.
> $$
> \begin{aligned}
> &AB = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix},\ \ BA = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix},\ \ A^2 = A,\ \ B^2 = O \\
> &(A + B)^2 = \begin{bmatrix} 1 & 1 \\ 0 & 0 \end{bmatrix}\begin{bmatrix} 1 & 1 \\ 0 & 0 \end{bmatrix} = \begin{bmatrix} 1 & 1 \\ 0 & 0 \end{bmatrix} \\
> &A^2 + 2AB + B^2 = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} + \begin{bmatrix} 0 & 2 \\ 0 & 0 \end{bmatrix} + O = \begin{bmatrix} 1 & 2 \\ 0 & 0 \end{bmatrix} \ne (A + B)^2
> \end{aligned}
> $$
> Condition:
> $$
> \begin{aligned}
> (A + B)^2 = A^2 + 2AB + B^2 &\iff A^2 + AB + BA + B^2 = A^2 + 2AB + B^2 \\
> &\iff BA = AB
> \end{aligned}
> $$
> Hence the equation is true exactly when $A$ and $B$ [[Commuting Matrices|commute]], $AB = BA$.
>
> \# For numbers $ab + ba = 2ab$; for matrices the middle terms $AB$ and $BA$ stay apart. The last $\iff$ cancels $A^2 + AB + B^2$ from both sides (add its negative, as in 21 d.). Pairs that commute: $B = I$, $B = A$, $B = rA$, or any two diagonal matrices.

### FB 1.3.43
Question: [[LA1 HW 1.3 Questions#FB 1.3.43|FB 1.3.43]]

> [!solution] Solution
> No.
> $$
> \begin{aligned}
> (A + B)(A - B) &= A(A - B) + B(A - B) && \text{(distributive law)} \\
> &= A^2 - AB + BA - B^2 && \text{(distributive law)}
> \end{aligned}
> $$
> Counterexample: $A = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$, $B = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$.
> $$
> \begin{aligned}
> &(A + B)(A - B) = \begin{bmatrix} 1 & 1 \\ 0 & 0 \end{bmatrix}\begin{bmatrix} 1 & -1 \\ 0 & 0 \end{bmatrix} = \begin{bmatrix} 1 & -1 \\ 0 & 0 \end{bmatrix} \\
> &A^2 - B^2 = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} - \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} \ne (A + B)(A - B)
> \end{aligned}
> $$
> Condition:
> $$
> \begin{aligned}
> (A + B)(A - B) = A^2 - B^2 &\iff A^2 - AB + BA - B^2 = A^2 - B^2 \\
> &\iff BA - AB = O \iff AB = BA
> \end{aligned}
> $$
> Hence the equation is true exactly when $A$ and $B$ commute, $AB = BA$.
>
> \# Line 2 uses $A(-B) = -(AB)$, that is, $A(rB) = r(AB)$ with $r = -1$. The same pair $A$, $B$ breaks both 42 and 43, because $AB \ne BA$ is all that is needed.

## Additional Problems from the Web

> [!note] Note
> These problems are not assigned. They come from the web and add what the assigned exercises leave out.
> - WEB 1.3.1: true-or-false items in the format of the quizzes: the transpose of a product of non-square matrices, powers of commuting matrices, $AB = O$ but $BA \ne O$, and a product of symmetric matrices.
> - WEB 1.3.2: a product of symmetric matrices is symmetric exactly when they commute.
> - WEB 1.3.3: $ABA$ is always symmetric, although $AB$ need not be.
> - WEB 1.3.4: commuting with *every* matrix forces a multiple of $I$; Exercises 45 and 46 ask the same question for one given matrix.
> - WEB 1.3.5: the trace of $AA^T$ is the sum of the squares of the entries of $A$, the computation behind Exercise 21 f.

### WEB 1.3.1
Question: [[LA1 HW 1.3 Questions#WEB 1.3.1|WEB 1.3.1]]

> [!solution] Solution
> - Problem 1. **F.** If $m \ne n$: $(AB)^T$ is $m \times m$, but $A^TB^T$ is $(n \times m)(m \times n) = n \times n$, a different size. The rule is $(AB)^T = B^TA^T$.
> - Problem 3. **T.** $AB = BA \implies A^2B = A(AB) = A(BA) = (AB)A = (BA)A = BA^2$.
> - Problem 6. **T.** $A = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$, $B = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$: $AB = O$, but $BA = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} \ne O$.
> - Problem 10. **F.** $A = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$, $B = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}$ are symmetric, but $AB = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$ is not.
>
> \# Problem 1 fails for $m = n$ too: with $A$, $B$ of Exercise 42, $(AB)^T = \begin{bmatrix} 0 & 0 \\ 1 & 0 \end{bmatrix}$ but $A^TB^T = O$. Problem 3 uses only associativity of the product; repeating it, $A^k$ commutes with $B$ for every $k$. Problem 6: for $n > 2$ put these $2 \times 2$ matrices in the top left corner and zeros elsewhere. Problem 10: here $AB \ne BA$, and WEB 1.3.2 shows that this is exactly what goes wrong.

### WEB 1.3.2
Question: [[LA1 HW 1.3 Questions#WEB 1.3.2|WEB 1.3.2]]

> [!proof] Proof
> $A^T = A$, $B^T = B$.
> $$
> \begin{aligned}
> \text{(a)}\ \ (\implies)\ \ &AB \text{ symmetric} \implies AB = (AB)^T = B^TA^T = BA \\
> (\impliedby)\ \ &AB = BA \implies (AB)^T = B^TA^T = BA = AB \implies AB \text{ symmetric} \\[4pt]
> \text{(b)}\ \ &AB \text{ diagonal} \implies AB \text{ symmetric} \implies AB = BA \quad \text{(by (a))} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Both directions use only $(AB)^T = B^TA^T$ and $A^T = A$, $B^T = B$. In (b), a [[Diagonal Matrix|diagonal matrix]] is symmetric: [[LA1 HW 1.3 1.5 Solutions#FIS 1.3.7|FIS 1.3.7]].

### WEB 1.3.3
Question: [[LA1 HW 1.3 Questions#WEB 1.3.3|WEB 1.3.3]]

> [!proof] Proof
> $$
> \begin{aligned}
> &A^T = A,\ B^T = B \quad (A, B: n \times n,\ \text{so } ABA \text{ is defined}) \\
> &(ABA)^T = \big((AB)A\big)^T = A^T(AB)^T = A^TB^TA^T = ABA \quad \big(\text{using } (XY)^T = Y^TX^T \text{ twice}\big) \\
> &\text{Hence } ABA \text{ is symmetric.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Transposing reverses the order of the factors, and $ABA$ reads the same backwards, so no commuting is needed; compare $AB$ in WEB 1.3.2. The same idea shows that $A^TA$ (Exercise 15) and $AA^T$ are symmetric for every matrix $A$.

### WEB 1.3.4
Question: [[LA1 HW 1.3 Questions#WEB 1.3.4|WEB 1.3.4]]

> [!proof] Proof
> $$
> \begin{aligned}
> &D = \begin{bmatrix} a & 0 & 0 \\ 0 & b & 0 \\ 0 & 0 & c \end{bmatrix} \text{ commutes with every } 3 \times 3 \text{ matrix. Take } M = \begin{bmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{bmatrix}: \\[4pt]
> &DM = \begin{bmatrix} 0 & a & 0 \\ 0 & 0 & b \\ 0 & 0 & 0 \end{bmatrix}, \quad MD = \begin{bmatrix} 0 & b & 0 \\ 0 & 0 & c \\ 0 & 0 & 0 \end{bmatrix} \\[4pt]
> &DM = MD \implies a = b \ (\text{entry } (1, 2)),\ \ b = c \ (\text{entry } (2, 3)) \\
> &\text{Hence } D = \begin{bmatrix} a & 0 & 0 \\ 0 & a & 0 \\ 0 & 0 & a \end{bmatrix} = aI. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $DM$ multiplies row $i$ of $M$ by the $i$th diagonal entry of $D$, and $MD$ multiplies column $j$ of $M$ by the $j$th: $(DM)_{ij} = d_i(M)_{ij}$, $(MD)_{ij} = (M)_{ij}d_j$. So $DM = MD$ means $(d_i - d_j)(M)_{ij} = 0$ for all $i, j$, and one $M$ with nonzero entries at $(1, 2)$ and $(2, 3)$ ties all three diagonal entries together. "Every" is what lets us choose $M$. Conversely, $aI$ commutes with every $M$: $(aI)M = aM = M(aI)$.

### WEB 1.3.5
Question: [[LA1 HW 1.3 Questions#WEB 1.3.5|WEB 1.3.5]]

> [!solution] Solution
> **(a)**
> $$
> \operatorname{tr}(AB^T) = \sum_{i=1}^{n} (AB^T)_{ii} = \sum_{i=1}^{n}\sum_{k=1}^{n} a_{ik}(B^T)_{ki} = \sum_{i=1}^{n}\sum_{k=1}^{n} a_{ik}b_{ik}
> $$

> [!proof] Proof of (b) and (c)
> $$
> \begin{aligned}
> \text{(b)}\ \ &B = A \text{ in (a)} \implies \operatorname{tr}(AA^T) = \sum_{i=1}^{n}\sum_{k=1}^{n} a_{ik}^{2}, \text{ the sum of the squares of all entries of } A. \\[4pt]
> \text{(c)}\ \ &A^T = A \implies A^2 = AA = AA^T \implies \operatorname{tr}(A^2) = \operatorname{tr}(AA^T) = \sum_{i=1}^{n}\sum_{k=1}^{n} a_{ik}^{2} \quad \text{(by (b))} \\
> &A \ne O \implies a_{pq} \ne 0 \text{ for some } p, q \implies \sum_{i=1}^{n}\sum_{k=1}^{n} a_{ik}^{2} \ge a_{pq}^{2} > 0 \\
> &\text{Hence } \operatorname{tr}(A^2) > 0. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# (a) pairs each entry of $A$ with the entry of $B$ in the same place. In (c) the diagonal entries $(A^2)_{ii} = \sum_{k} a_{ik}^{2}$ are those of Exercise 21 f., and the trace adds them up. "Real" matters: over $\mathbb{C}$, $A = \begin{bmatrix} 1 & i \\ i & -1 \end{bmatrix}$ is symmetric and nonzero, but $A^2 = O$. The same sum gives $A^TA = O \implies A = O$ for real $A$.
