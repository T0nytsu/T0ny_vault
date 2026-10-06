---
course: [LA1]
chapter: ["1.4", "1.5"]
tags: [linear-algebra, homework, solutions, linear-systems, matrix-inverse]
source:
  - "Own solutions; computations checked with sympy"
  - "Nicholson exercises: own solutions"
created: 2026-10-05
questions: "[[LA1 HW 1.4 1.5 Questions]]"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.3\|FB 1.4.3]] | (a) $\begin{bmatrix} -1 & 1 & 2 & 0 \\ 0 & 2 & -1 & 3 \\ 0 & 0 & 10 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix}$; (b) $\begin{bmatrix} 1 & 0 & 0 & \tfrac{3}{2} \\ 0 & 1 & 0 & \tfrac{3}{2} \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix}$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.5\|FB 1.4.5]] | (a) $\begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 0 & 0 & 2 & 6 & 8 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & -8 \end{bmatrix}$; (b) $\begin{bmatrix} 1 & -3 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix}$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.42\|FB 1.4.42]] | $E = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ -3 & 0 & 1 \end{bmatrix}$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.44\|FB 1.4.44]] | $C = \begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ -4 & 0 & 1 \end{bmatrix}$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.45\|FB 1.4.45]] | $C = \begin{bmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0 \end{bmatrix}$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.49\|FB 1.4.49]] | $C = \begin{bmatrix} 1 & -60 & 0 & -15 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & -12 & 0 & -3 \end{bmatrix}$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.52\|FB 1.4.52]] | Proof: row $i$ of $EA$ is $\mathbf{e}_jA = \mathbf{r}_j$, row $j$ is $\mathbf{e}_iA = \mathbf{r}_i$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.53\|FB 1.4.53]] | Proof: row $i$ of $EA$ is $(s\mathbf{e}_i)A = s\mathbf{r}_i$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.54\|FB 1.4.54]] | Proof: row $i$ of $EA$ is $(\mathbf{e}_i + s\mathbf{e}_j)A = \mathbf{r}_i + s\mathbf{r}_j$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.55\|FB 1.4.55]] | Proof |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.23\|FB 1.5.23]] | a. T; b. T; c. T; d. F; e. T; f. T; g. T; h. F; i. F; j. F |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.24\|FB 1.5.24]] | Proof; $(A^T)^{-1} = (A^{-1})^T$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.25\|FB 1.5.25]] | a. No: $A = \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}$; b. Yes: $(2A)^{-1} = \tfrac{1}{2}A^{-1}$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.36\|FB 1.5.36]] | $R_i \leftrightarrow R_j$: $C_i \leftrightarrow C_j$; $R_i \to sR_i$: $C_i \to sC_i$; $R_i \to R_i + sR_j$: $C_j \to C_j + sC_i$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.37\|FB 1.5.37]] | $AE$ is $A$ after the column operation that gives $E$ from $I$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.38\|FB 1.5.38]] | a. the same two columns of $A^{-1}$ are interchanged; b. that column of $A^{-1}$ is multiplied by $\tfrac{1}{r}$; c. $r$ times column $j$ of $A^{-1}$ is subtracted from column $i$ |

Additional exercises, not assigned:

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.9\|FB 1.4.9]] | $\mathbf{x} = [1 - 2r,\ -2 - r - 3s,\ r,\ s]$; particular solution $[-5, 1, 3, -2]$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.16\|FB 1.4.16]] | $x = -1$, $y = 2$, $z = 0$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.24\|FB 1.4.24]] | $\mathbf{x} = [-13 - 2r + 14s,\ r,\ -5 + 5s,\ s]$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.25\|FB 1.4.25]] | Yes: $\mathbf{b} = 2\mathbf{v}_1 - \mathbf{v}_3$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.29\|FB 1.4.29]] | a. F; b. F; c. T; d. T; e. F; f. T; g. T; h. T; i. F; j. T |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.40\|FB 1.4.40]] | All $b_1, b_2, b_3 \in \mathbb{R}$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.4.58\|FB 1.4.58]] | a. Proof; b. Yes; c. No |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.5\|FB 1.5.5]] | $A^{-1} = A$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.13\|FB 1.5.13]] | a. $A^{-1} = \begin{bmatrix} -7 & 3 \\ -5 & 2 \end{bmatrix}$; b. $x_1 = -37$, $x_2 = -26$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.21\|FB 1.5.21]] | $r \ne 0$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.22\|FB 1.5.22]] | Proof |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.26\|FB 1.5.26]] | Proof: $A^{-1} = A(A^2)^{-1}$ |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.30\|FB 1.5.30]] | a. $\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$; b. Proof |
| [[LA1 HW 1.4 1.5 Questions#FB 1.5.35\|FB 1.5.35]] | Proof |

Additional exercises from the Internet (Nicholson), not assigned:

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.4 1.5 Questions#NIC 1.2.8\|NIC 1.2.8]] | One solution: $ab \ne 2$; no solution: $ab = 2$, $a \ne -5$; infinitely many: $a = -5$, $b = -\tfrac{2}{5}$ |
| [[LA1 HW 1.4 1.5 Questions#NIC 2.4.5\|NIC 2.4.5]] | (1) $A = \begin{bmatrix} \tfrac{1}{3} & \tfrac{1}{3} \\ 0 & \tfrac{1}{3} \end{bmatrix}$; (3) $A = \begin{bmatrix} -\tfrac{1}{6} & 0 \\ \tfrac{1}{6} & -\tfrac{2}{3} \end{bmatrix}$ |
| [[LA1 HW 1.4 1.5 Questions#NIC 2.4.21\|NIC 2.4.21]] | Proof |
| [[LA1 HW 1.4 1.5 Questions#NIC 2.4.24\|NIC 2.4.24]] | $A^{-1} = \tfrac{1}{2}(3I - A^2)$ |
| [[LA1 HW 1.4 1.5 Questions#NIC 2.4.28\|NIC 2.4.28]] | (1), (2) Proofs; (3) $\begin{bmatrix} 1 & -2 & 7 \\ 0 & 1 & -3 \\ 0 & 0 & 1 \end{bmatrix}$ |
| [[LA1 HW 1.4 1.5 Questions#NIC 2.4.34\|NIC 2.4.34]] | Proof: $A^{-1} = B(AB)^{-1}$, $B^{-1} = (AB)^{-1}A$ |
| [[LA1 HW 1.4 1.5 Questions#NIC 2.5.9\|NIC 2.5.9]] | Proof |
| [[LA1 HW 1.4 1.5 Questions#NIC 2.5.14\|NIC 2.5.14]] | Proof: the row operations are a left multiplication by $U = Q$ |

## FB §1.4 Solving Systems of Linear Equations

> [!note] Note
> The notation and the facts that the answers use.
> - **[[Elementary Row Operation|Row operations]]**: $R_i \leftrightarrow R_j$ (row-interchange), $R_i \to sR_i$ with $s \ne 0$ (row-scaling), $R_i \to R_i + sR_j$ (row-addition). The operation is written over $\sim$.
> - **[[Row Equivalence|Row equivalent]]**, $A \sim B$: $B$ is obtained from $A$ by a sequence of elementary row operations.
> - **[[Elementary Matrix|Elementary matrix]]** $E$: one elementary row operation applied to $I$.
> - **Left multiplication by an elementary matrix** (Theorem 1.8): $EA$ is $A$ after the row operation that gives $E$ from $I$.
> - **Rows of a product**: row $k$ of $EA$ $=$ (row $k$ of $E$)$A$, because the $(k, j)$-entry of $EA$ is (row $k$ of $E$) $\cdot$ (column $j$ of $A$).
> - **A row vector times a matrix** ([[LA1 HW 1.3 1.5 Solutions#FB 1.3.24|FB 1.3.24]]): $\mathbf{c}A = c_1\mathbf{r}_1 + \cdots + c_m\mathbf{r}_m$, where $\mathbf{r}_1, \dots, \mathbf{r}_m$ are the rows of $A$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FB 1.4.3
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.3|FB 1.4.3]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> &\begin{bmatrix} 0 & 2 & -1 & 3 \\ -1 & 1 & 2 & 0 \\ 1 & 1 & -3 & 3 \\ 1 & 5 & 5 & 9 \end{bmatrix} \overset{R_1 \leftrightarrow R_2}{\sim} \begin{bmatrix} -1 & 1 & 2 & 0 \\ 0 & 2 & -1 & 3 \\ 1 & 1 & -3 & 3 \\ 1 & 5 & 5 & 9 \end{bmatrix} \\[6pt]
> & \overset{\substack{R_3 \to R_3 + R_1 \\ R_4 \to R_4 + R_1}}{\sim} \begin{bmatrix} -1 & 1 & 2 & 0 \\ 0 & 2 & -1 & 3 \\ 0 & 2 & -1 & 3 \\ 0 & 6 & 7 & 9 \end{bmatrix} \overset{\substack{R_3 \to R_3 - R_2 \\ R_4 \to R_4 - 3R_2}}{\sim} \begin{bmatrix} -1 & 1 & 2 & 0 \\ 0 & 2 & -1 & 3 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 10 & 0 \end{bmatrix} \\[6pt]
> & \overset{R_3 \leftrightarrow R_4}{\sim} \begin{bmatrix} -1 & 1 & 2 & 0 \\ 0 & 2 & -1 & 3 \\ 0 & 0 & 10 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix}
> \end{aligned}
> $$
> **(b)** Continue from (a):
> $$
> \begin{aligned}
> &\begin{bmatrix} -1 & 1 & 2 & 0 \\ 0 & 2 & -1 & 3 \\ 0 & 0 & 10 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix} \overset{R_3 \to \tfrac{1}{10}R_3}{\sim} \begin{bmatrix} -1 & 1 & 2 & 0 \\ 0 & 2 & -1 & 3 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix} \\[6pt]
> & \overset{\substack{R_1 \to R_1 - 2R_3 \\ R_2 \to R_2 + R_3}}{\sim} \begin{bmatrix} -1 & 1 & 0 & 0 \\ 0 & 2 & 0 & 3 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix} \overset{R_2 \to \tfrac{1}{2}R_2}{\sim} \begin{bmatrix} -1 & 1 & 0 & 0 \\ 0 & 1 & 0 & \tfrac{3}{2} \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix} \\[6pt]
> & \overset{R_1 \to R_1 - R_2}{\sim} \begin{bmatrix} -1 & 0 & 0 & -\tfrac{3}{2} \\ 0 & 1 & 0 & \tfrac{3}{2} \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix} \overset{R_1 \to -R_1}{\sim} \begin{bmatrix} 1 & 0 & 0 & \tfrac{3}{2} \\ 0 & 1 & 0 & \tfrac{3}{2} \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix}
> \end{aligned}
> $$
>
> \# (a) [[Row-Echelon Form|Row-echelon form]]: go down, column by column. Get a nonzero pivot at the top, make zeros below it, move the zero row to the bottom. (b) [[Reduced Row-Echelon Form|Reduced row-echelon form]]: go up from the last pivot. Make the pivot $1$, then make zeros above it. The answer to (a) is not unique; the answer to (b) is.

### FB 1.4.5
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.5|FB 1.4.5]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> &\begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 1 & -3 & 0 & 0 & -1 \\ 2 & -6 & 2 & 4 & 0 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix} \\[6pt]
> & \overset{\substack{R_2 \to R_2 + R_1 \\ R_3 \to R_3 + 2R_1}}{\sim} \begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 2 & 6 & 8 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix} \overset{R_2 \leftrightarrow R_3}{\sim} \begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 0 & 0 & 2 & 6 & 8 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix} \\[6pt]
> & \overset{R_4 \to R_4 - \tfrac{1}{2}R_2}{\sim} \begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 0 & 0 & 2 & 6 & 8 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & -8 \end{bmatrix}
> \end{aligned}
> $$
> **(b)** Continue from (a):
> $$
> \begin{aligned}
> &\begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 0 & 0 & 2 & 6 & 8 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & -8 \end{bmatrix} \\[6pt]
> & \overset{\substack{R_2 \to \tfrac{1}{2}R_2 \\ R_4 \to -\tfrac{1}{8}R_4}}{\sim} \begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 0 & 0 & 1 & 3 & 4 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix} \overset{\substack{R_1 \to R_1 - 4R_4 \\ R_2 \to R_2 - 4R_4 \\ R_3 \to R_3 - 3R_4}}{\sim} \begin{bmatrix} -1 & 3 & 0 & 1 & 0 \\ 0 & 0 & 1 & 3 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix} \\[6pt]
> & \overset{\substack{R_1 \to R_1 - R_3 \\ R_2 \to R_2 - 3R_3}}{\sim} \begin{bmatrix} -1 & 3 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix} \overset{R_1 \to -R_1}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix}
> \end{aligned}
> $$
>
> \# Column 2 never gets a pivot: after column 1 is cleared, column 2 is zero below row 1, so the next pivot is in column 3. Pivots: columns 1, 3, 4, 5.

### FB 1.4.42
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.42|FB 1.4.42]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Rows 1, 2 are unchanged, and } [0, -5, 2, -11] = [3, 4, 5, 1] - 3[1, 3, 1, 4] \\
> &\implies \text{the operation is } R_3 \to R_3 - 3R_1. \\
> &\text{Apply it to } I:\quad E = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ -3 & 0 & 1 \end{bmatrix}
> \end{aligned}
> $$
>
> \# First find the row operation, then do the same operation on $I$. $E$ is $3 \times 3$ because the matrix has $3$ rows.

### FB 1.4.44
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.44|FB 1.4.44]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\begin{bmatrix} 1 & 2 \\ 3 & 4 \\ 4 & 2 \end{bmatrix} \overset{R_2 \to R_2 - 3R_1}{\sim} \begin{bmatrix} 1 & 2 \\ 0 & -2 \\ 4 & 2 \end{bmatrix} \overset{R_3 \to R_3 - 4R_1}{\sim} \begin{bmatrix} 1 & 2 \\ 0 & -2 \\ 0 & -6 \end{bmatrix}
> \end{aligned}
> $$
> Apply the same operations to $I$:
> $$
> \begin{aligned}
> &\begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \overset{R_2 \to R_2 - 3R_1}{\sim} \begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \overset{R_3 \to R_3 - 4R_1}{\sim} \begin{bmatrix} 1 & 0 & 0 \\ -3 & 1 & 0 \\ -4 & 0 & 1 \end{bmatrix} = C
> \end{aligned}
> $$
>
> \# $C = E_2E_1$, where $E_1$, $E_2$ are the elementary matrices of the two operations: $E_2(E_1A) = (E_2E_1)A$. Doing the operations on $I$ gives $E_2E_1I = C$ without any multiplication. $C$ is not elementary, because it takes two operations.

### FB 1.4.45
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.45|FB 1.4.45]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\begin{bmatrix} 1 & 2 \\ 3 & 4 \\ 4 & 2 \end{bmatrix} \overset{R_1 \leftrightarrow R_2}{\sim} \begin{bmatrix} 3 & 4 \\ 1 & 2 \\ 4 & 2 \end{bmatrix} \overset{R_2 \leftrightarrow R_3}{\sim} \begin{bmatrix} 3 & 4 \\ 4 & 2 \\ 1 & 2 \end{bmatrix}
> \end{aligned}
> $$
> Apply the same operations to $I$:
> $$
> \begin{aligned}
> &\begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \overset{R_1 \leftrightarrow R_2}{\sim} \begin{bmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix} \overset{R_2 \leftrightarrow R_3}{\sim} \begin{bmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0 \end{bmatrix} = C
> \end{aligned}
> $$
>
> \# Moving three rows around takes two interchanges. Check by rows: row 1 of $C$ is $[0, 1, 0]$, so row 1 of $CA$ is row 2 of $A$.

### FB 1.4.49
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.49|FB 1.4.49]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{The operations are } R_4 \to R_4 + 4R_2,\ \ R_4 \to -3R_4,\ \ R_1 \to R_1 + 5R_4. \text{ Apply them to } I: \\[4pt]
> &\begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{bmatrix} \overset{R_4 \to R_4 + 4R_2}{\sim} \begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 4 & 0 & 1 \end{bmatrix} \\[6pt]
> & \overset{R_4 \to -3R_4}{\sim} \begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & -12 & 0 & -3 \end{bmatrix} \overset{R_1 \to R_1 + 5R_4}{\sim} \begin{bmatrix} 1 & -60 & 0 & -15 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & -12 & 0 & -3 \end{bmatrix} = C
> \end{aligned}
> $$
>
> \# $C = E_3E_2E_1$: the first operation is next to $A$, because $CA = E_3(E_2(E_1A))$. The order matters: row 4 is already $[0, -12, 0, -3]$ when $5$ times row 4 is added to row 1.

### FB 1.4.52
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.52|FB 1.4.52]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } A \text{ be } m \times n \text{ with rows } \mathbf{r}_1, \dots, \mathbf{r}_m, \text{ and let } \mathbf{e}_k \text{ be row } k \text{ of the } m \times m \text{ matrix } I. \\
> &\mathbf{e}_kA = 0\mathbf{r}_1 + \cdots + 1\mathbf{r}_k + \cdots + 0\mathbf{r}_m = \mathbf{r}_k && \text{(Exercise 24, §1.3)} \\
> &\text{Let } E \text{ be } I \text{ after } R_i \leftrightarrow R_j. \text{ Then}
> \end{aligned}
> $$
> $$
> EA = \begin{bmatrix} \mathbf{e}_1 \\ \vdots \\ \mathbf{e}_j \\ \vdots \\ \mathbf{e}_i \\ \vdots \\ \mathbf{e}_m \end{bmatrix} A = \begin{bmatrix} \mathbf{e}_1A \\ \vdots \\ \mathbf{e}_jA \\ \vdots \\ \mathbf{e}_iA \\ \vdots \\ \mathbf{e}_mA \end{bmatrix} = \begin{bmatrix} \mathbf{r}_1 \\ \vdots \\ \mathbf{r}_j \\ \vdots \\ \mathbf{r}_i \\ \vdots \\ \mathbf{r}_m \end{bmatrix} \begin{matrix} \vphantom{\mathbf{r}_1} \\ \vphantom{\vdots} \\ \leftarrow \text{row } i \\ \vphantom{\vdots} \\ \leftarrow \text{row } j \\ \vphantom{\vdots} \\ \vphantom{\mathbf{r}_m} \end{matrix}
> $$
> Hence $EA$ is $A$ with rows $i$ and $j$ interchanged. $\blacksquare$
>
> \# Two facts carry Exercises 52–54: row $k$ of $EA$ is (row $k$ of $E$)$A$, and $\mathbf{e}_kA$ picks out row $k$ of $A$. After that, only row $i$ (and row $j$) of $E$ differs from $I$.

### FB 1.4.53
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.53|FB 1.4.53]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } A,\ \mathbf{r}_k,\ \mathbf{e}_k \text{ be as in Exercise 52, so } \mathbf{e}_kA = \mathbf{r}_k. \\
> &\text{Let } E \text{ be } I \text{ after } R_i \to sR_i,\ s \ne 0. \text{ Then}
> \end{aligned}
> $$
> $$
> EA = \begin{bmatrix} \mathbf{e}_1 \\ \vdots \\ s\mathbf{e}_i \\ \vdots \\ \mathbf{e}_m \end{bmatrix} A = \begin{bmatrix} \mathbf{e}_1A \\ \vdots \\ (s\mathbf{e}_i)A \\ \vdots \\ \mathbf{e}_mA \end{bmatrix} = \begin{bmatrix} \mathbf{r}_1 \\ \vdots \\ s\mathbf{r}_i \\ \vdots \\ \mathbf{r}_m \end{bmatrix} \begin{matrix} \vphantom{\mathbf{r}_1} \\ \vphantom{\vdots} \\ \leftarrow \text{row } i \\ \vphantom{\vdots} \\ \vphantom{\mathbf{r}_m} \end{matrix}
> $$
> because $(s\mathbf{e}_i)A = s(\mathbf{e}_iA) = s\mathbf{r}_i$. Hence $EA$ is $A$ with row $i$ multiplied by $s$. $\blacksquare$

### FB 1.4.54
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.54|FB 1.4.54]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } A,\ \mathbf{r}_k,\ \mathbf{e}_k \text{ be as in Exercise 52, so } \mathbf{e}_kA = \mathbf{r}_k. \\
> &\text{Let } E \text{ be } I \text{ after } R_i \to R_i + sR_j,\ i \ne j. \text{ Then}
> \end{aligned}
> $$
> $$
> EA = \begin{bmatrix} \mathbf{e}_1 \\ \vdots \\ \mathbf{e}_i + s\mathbf{e}_j \\ \vdots \\ \mathbf{e}_m \end{bmatrix} A = \begin{bmatrix} \mathbf{e}_1A \\ \vdots \\ (\mathbf{e}_i + s\mathbf{e}_j)A \\ \vdots \\ \mathbf{e}_mA \end{bmatrix} = \begin{bmatrix} \mathbf{r}_1 \\ \vdots \\ \mathbf{r}_i + s\mathbf{r}_j \\ \vdots \\ \mathbf{r}_m \end{bmatrix} \begin{matrix} \vphantom{\mathbf{r}_1} \\ \vphantom{\vdots} \\ \leftarrow \text{row } i \\ \vphantom{\vdots} \\ \vphantom{\mathbf{r}_m} \end{matrix}
> $$
> because $(\mathbf{e}_i + s\mathbf{e}_j)A = \mathbf{e}_iA + s(\mathbf{e}_jA) = \mathbf{r}_i + s\mathbf{r}_j$ (distributive law). Hence $EA$ is $A$ with $s$ times row $j$ added to row $i$. $\blacksquare$
>
> \# Row $j$ of $E$ is still $\mathbf{e}_j$, so row $j$ of $EA$ is still $\mathbf{r}_j$.

### FB 1.4.55
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.55|FB 1.4.55]]

> [!proof] Proof
> **a.**
> $$
> \begin{aligned}
> &R_1 \to 1R_1 \text{ is an elementary row operation, and it gives } A \text{ from } A. \\
> &\text{Hence } A \sim A.
> \end{aligned}
> $$
> **b.**
> $$
> \begin{aligned}
> &A \sim B \implies \exists\, E_1, \dots, E_k \text{ elementary s.t. } B = E_k \cdots E_2E_1A. \\
> &\because \text{each row operation is undone by a row operation:} \\
> &\qquad R_i \leftrightarrow R_j \text{ by } R_i \leftrightarrow R_j, \quad R_i \to sR_i \text{ by } R_i \to \tfrac{1}{s}R_i, \quad R_i \to R_i + sR_j \text{ by } R_i \to R_i - sR_j \\
> &\therefore \text{each } E_t \text{ is invertible and } E_t^{-1} \text{ is elementary.} \\
> &\implies A = E_1^{-1}E_2^{-1} \cdots E_k^{-1}B \\
> &\text{Hence } B \sim A.
> \end{aligned}
> $$
> **c.**
> $$
> \begin{aligned}
> &A \sim B \implies B = E_k \cdots E_1A, \qquad B \sim C \implies C = F_l \cdots F_1B \quad (E_t,\ F_t \text{ elementary}) \\
> &\implies C = F_l \cdots F_1E_k \cdots E_1A \\
> &\text{Hence } A \sim C. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# A row operation on $A$ is a left multiplication by an elementary matrix (Exercises 52–54), so "a sequence of row operations" becomes "a product of elementary matrices". In words: b. undo the operations in the reverse order; c. do the first sequence, then the second.

## FB §1.5 Inverses of Square Matrices

> [!note] Note
> The facts that the answers use.
> - **[[Invertible Matrix|Invertible]]**: $A$ is $n \times n$ and $\exists\, C$ s.t. $AC = CA = I$; then $C = A^{-1}$. *Singular* means not invertible.
> - **Inverse of a product**: $A$, $B$ invertible $\implies$ $AB$ invertible and $(AB)^{-1} = B^{-1}A^{-1}$.
> - **Invertible and elementary matrices**: $A$ invertible $\iff$ $A \sim I$ $\iff$ $A$ is a product of elementary matrices.
> - **[[Transpose]] of a product**: $(AB)^T = B^TA^T$.
> - **Columns of a product**: column $k$ of $AE$ $=$ $A$(column $k$ of $E$), and $A\mathbf{e}_k$ is column $k$ of $A$, where $\mathbf{e}_k$ is column $k$ of $I$ ([[LA1 HW 1.3 1.5 Solutions#FB 1.3.41|FB 1.3.41]]).
> - **[[Elementary Column Operation|Column operations]]**: $C_i \leftrightarrow C_j$, $C_i \to sC_i$, $C_j \to C_j + sC_i$, as for rows.

### FB 1.5.23
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.23|FB 1.5.23]]

> [!solution] Solution
> - a. **T.** $AC = BC \implies (AC)C^{-1} = (BC)C^{-1} \implies A = B$.
> - b. **T.** $A = (AB)B^{-1} = OB^{-1} = O$.
> - c. **T.** $A$, $B$ invertible $\implies$ $C = AB$ invertible. $A$, $C$ invertible $\implies$ $B = A^{-1}C$ invertible. $B$, $C$ invertible $\implies$ $A = CB^{-1}$ invertible.
> - d. **F.** $A = O$, $B = I$, $C = O$: $AB = C$, and $A$, $C$ are singular, but $B$ is invertible.
> - e. **T.** $A^2$ invertible $\implies$ $A$ invertible $\implies$ $A^3 = AAA$ invertible.
> - f. **T.** Let $D = (A^3)^{-1}$. $A(A^2D) = I = (DA^2)A \implies A$ invertible $\implies$ $A^2 = AA$ invertible.
> - g. **T.** Each row operation is undone by a row operation, whose elementary matrix is $E^{-1}$.
> - h. **F.** $\begin{bmatrix} 2 & 0 \\ 0 & 3 \end{bmatrix}$ is invertible, but it takes two row operations to get it from $I$.
> - i. **F.** $A = I$, $B = -I$: both invertible, but $A + B = O$ is singular.
> - j. **F.** $A = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}$, $B = \begin{bmatrix} 1 & 0 \\ 1 & 1 \end{bmatrix}$: $(AB)^{-1} = \begin{bmatrix} 1 & -1 \\ -1 & 2 \end{bmatrix} \ne \begin{bmatrix} 2 & -1 \\ -1 & 1 \end{bmatrix} = A^{-1}B^{-1}$.
>
> \# d. $A$, $B$ singular does force $C = AB$ singular; the statement fails only when $C$ is one of the two. e. The first step is [[LA1 HW 1.4 1.5 Questions#FB 1.5.26|FB 1.5.26]], solved below; f. is the same argument. j. $AB$ is invertible; only the formula is wrong: $(AB)^{-1} = B^{-1}A^{-1}$.

### FB 1.5.24
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.24|FB 1.5.24]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\because A \text{ is invertible} \\
> &\therefore \exists\, A^{-1} \text{ s.t. } AA^{-1} = A^{-1}A = I. \\
> &A^T(A^{-1})^T = (A^{-1}A)^T = I^T = I && \left((XY)^T = Y^TX^T\right) \\
> &(A^{-1})^TA^T = (AA^{-1})^T = I^T = I \\
> &\text{Hence } A^T \text{ is invertible and } (A^T)^{-1} = (A^{-1})^T. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# To show that a matrix is invertible, name a candidate for the inverse and multiply on both sides. Here the candidate is $(A^{-1})^T$.

### FB 1.5.25
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.25|FB 1.5.25]]

> [!solution] Solution
> **a.** No.
> $$
> \begin{aligned}
> &\text{Let } A = \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}. \\
> &A\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} = I = \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}A \implies A \text{ is invertible.} \\
> &A + A^T = \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix} + \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} = O, \text{ which is singular.}
> \end{aligned}
> $$
> **b.** Yes.
> $$
> \begin{aligned}
> &A + A = 2A \\
> &(2A)\left(\tfrac{1}{2}A^{-1}\right) = AA^{-1} = I = A^{-1}A = \left(\tfrac{1}{2}A^{-1}\right)(2A) \\
> &\text{Hence } A + A \text{ is invertible and } (A + A)^{-1} = \tfrac{1}{2}A^{-1}.
> \end{aligned}
> $$
>
> \# a. Any invertible $A$ with $A^T = -A$ works. "Always" is refuted by one counterexample; a "Yes" needs a proof for every $A$.

### FB 1.5.36
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.36|FB 1.5.36]]

> [!solution] Solution
> $$
> \begin{aligned}
> &E = I \text{ after } R_i \leftrightarrow R_j: && E = I \text{ after } C_i \leftrightarrow C_j \\
> &E = I \text{ after } R_i \to sR_i: && E = I \text{ after } C_i \to sC_i \\
> &E = I \text{ after } R_i \to R_i + sR_j: && E = I \text{ after } C_j \to C_j + sC_i
> \end{aligned}
> $$
> Reasons, with $\mathbf{e}_k$ = column $k$ of $I$:
> $$
> \begin{aligned}
> &R_i \leftrightarrow R_j: && \text{the } 1\text{'s of rows } i, j \text{ move to the places } (i, j), (j, i) \implies \text{column } i = \mathbf{e}_j,\ \text{column } j = \mathbf{e}_i \\
> &R_i \to sR_i: && \text{the only change is the entry } s \text{ at } (i, i) \implies \text{column } i = s\mathbf{e}_i \\
> &R_i \to R_i + sR_j: && \text{the only change is the entry } s \text{ at } (i, j) \implies \text{column } j = \mathbf{e}_j + s\mathbf{e}_i
> \end{aligned}
> $$
>
> \# In the third type the indices change places: the row operation adds row $j$ to row $i$, and the column operation adds column $i$ to column $j$. Example: $\begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ s & 0 & 1 \end{bmatrix}$ is $I$ after $R_3 \to R_3 + sR_1$, and also $I$ after $C_1 \to C_1 + sC_3$.

### FB 1.5.37
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.37|FB 1.5.37]]

> [!solution] Solution
> $AE$ is $A$ after the column operation that gives $E$ from $I$ (Exercise 36).
> $$
> \begin{aligned}
> &\text{Let } \mathbf{a}_k \text{ be column } k \text{ of } A, \text{ so } A\mathbf{e}_k = \mathbf{a}_k. \quad \text{Column } k \text{ of } AE = A(\text{column } k \text{ of } E). \\[4pt]
> &E = I \text{ after } C_i \leftrightarrow C_j: && \text{column } i \text{ of } AE = A\mathbf{e}_j = \mathbf{a}_j,\ \ \text{column } j = A\mathbf{e}_i = \mathbf{a}_i \\
> &E = I \text{ after } C_i \to sC_i: && \text{column } i \text{ of } AE = A(s\mathbf{e}_i) = s\mathbf{a}_i \\
> &E = I \text{ after } C_j \to C_j + sC_i: && \text{column } j \text{ of } AE = A(\mathbf{e}_j + s\mathbf{e}_i) = \mathbf{a}_j + s\mathbf{a}_i \\[4pt]
> &\text{Every other column of } E \text{ is } \mathbf{e}_k, \text{ so that column of } AE \text{ is } \mathbf{a}_k.
> \end{aligned}
> $$
>
> \# $EA$ works on the rows of $A$, $AE$ on the columns. This is Exercises 52–54 with columns in place of rows.

### FB 1.5.38
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.38|FB 1.5.38]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{The resulting matrix is } EA,\ E \text{ elementary, and } (EA)^{-1} = A^{-1}E^{-1}. \\
> &E^{-1} \text{ is elementary, so } A^{-1}E^{-1} \text{ is } A^{-1} \text{ after a column operation (Exercise 37).}
> \end{aligned}
> $$
> **a.**
> $$
> \begin{aligned}
> &E = I \text{ after } R_i \leftrightarrow R_j \implies E^{-1} = E = I \text{ after } C_i \leftrightarrow C_j \\
> &\text{Hence the inverse is } A^{-1} \text{ with columns } i \text{ and } j \text{ interchanged.}
> \end{aligned}
> $$
> **b.**
> $$
> \begin{aligned}
> &E = I \text{ after } R_i \to rR_i \implies E^{-1} = I \text{ after } R_i \to \tfrac{1}{r}R_i = I \text{ after } C_i \to \tfrac{1}{r}C_i \\
> &\text{Hence the inverse is } A^{-1} \text{ with column } i \text{ multiplied by } \tfrac{1}{r}.
> \end{aligned}
> $$
> **c.**
> $$
> \begin{aligned}
> &E = I \text{ after } R_j \to R_j + rR_i \implies E^{-1} = I \text{ after } R_j \to R_j - rR_i = I \text{ after } C_i \to C_i - rC_j \\
> &\text{Hence the inverse is } A^{-1} \text{ with } r \text{ times column } j \text{ subtracted from column } i.
> \end{aligned}
> $$
>
> \# A row operation on $A$ becomes the inverse operation on the columns of $A^{-1}$. In c. the indices change places as in Exercise 36: rows "$i$ into $j$", columns "$j$ out of $i$".

## FB §1.4 Additional Exercises

> [!note] Note
> These exercises are not assigned. Each one adds a type of problem that the assigned exercises do not cover.
> - 9: reading the general solution, with free variables, from a reduced augmented matrix.
> - 16: the Gauss method with back substitution; a unique solution.
> - 24: the Gauss–Jordan method; infinitely many solutions.
> - 25: a [[Span|span]] question turned into a linear system.
> - 29: True or False about the number of solutions, the form of the quizzes.
> - 40: a system with letters on the right side; when is it consistent?
> - 58: a proof that counts pivots.

### FB 1.4.9
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.9|FB 1.4.9]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\text{Pivots: columns 1, 2} \implies x_3,\ x_4 \text{ are free. Let } x_3 = r,\ x_4 = s. \\
> &\text{Row 1: } x_1 + 2x_3 = 1 \implies x_1 = 1 - 2r \\
> &\text{Row 2: } x_2 + x_3 + 3x_4 = -2 \implies x_2 = -2 - r - 3s \\
> &\mathbf{x} = \begin{bmatrix} 1 - 2r \\ -2 - r - 3s \\ r \\ s \end{bmatrix} \quad \text{for any } r, s \in \mathbb{R} \\
> &r = 3,\ s = -2: \quad \mathbf{x} = \begin{bmatrix} -5 \\ 1 \\ 3 \\ -2 \end{bmatrix}
> \end{aligned}
> $$
>
> \# A column without a pivot gives a free variable. The row $[0\ 0\ 0\ 0 \mid 0]$ says $0 = 0$ and is dropped.

### FB 1.4.16
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.16|FB 1.4.16]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 2 & 1 & -3 & 0 \\ 6 & 3 & -8 & 0 \\ 2 & -1 & 5 & -4 \end{array}\right] \overset{\substack{R_2 \to R_2 - 3R_1 \\ R_3 \to R_3 - R_1}}{\sim} \left[\begin{array}{ccc|c} 2 & 1 & -3 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & -2 & 8 & -4 \end{array}\right] \overset{R_2 \leftrightarrow R_3}{\sim} \left[\begin{array}{ccc|c} 2 & 1 & -3 & 0 \\ 0 & -2 & 8 & -4 \\ 0 & 0 & 1 & 0 \end{array}\right]
> \end{aligned}
> $$
> Back substitution:
> $$
> \begin{aligned}
> &z = 0 \\
> &-2y + 8z = -4 \implies y = 2 \\
> &2x + y - 3z = 0 \implies x = -1
> \end{aligned}
> $$
> Hence $x = -1$, $y = 2$, $z = 0$.
>
> \# Gauss: reduce only to row-echelon form, then solve from the last equation up. Check in the third equation: $2(-1) - 2 + 5(0) = -4$.

### FB 1.4.24
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.24|FB 1.4.24]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{cccc|c} 1 & 2 & -3 & 1 & 2 \\ 3 & 6 & -8 & -2 & 1 \end{array}\right] \overset{R_2 \to R_2 - 3R_1}{\sim} \left[\begin{array}{cccc|c} 1 & 2 & -3 & 1 & 2 \\ 0 & 0 & 1 & -5 & -5 \end{array}\right] \\[6pt]
> & \overset{R_1 \to R_1 + 3R_2}{\sim} \left[\begin{array}{cccc|c} 1 & 2 & 0 & -14 & -13 \\ 0 & 0 & 1 & -5 & -5 \end{array}\right]
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\text{Pivots: columns 1, 3} \implies x_2,\ x_4 \text{ are free. Let } x_2 = r,\ x_4 = s. \\
> &x_1 = -13 - 2r + 14s, \qquad x_3 = -5 + 5s \\
> &\mathbf{x} = \begin{bmatrix} -13 - 2r + 14s \\ r \\ -5 + 5s \\ s \end{bmatrix} \quad \text{for any } r, s \in \mathbb{R}
> \end{aligned}
> $$
>
> \# Gauss–Jordan: reduce to reduced row-echelon form, then read the solution with no back substitution.

### FB 1.4.25
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.25|FB 1.4.25]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\mathbf{b} \in \operatorname{sp}(\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3) \iff x_1\mathbf{v}_1 + x_2\mathbf{v}_2 + x_3\mathbf{v}_3 = \mathbf{b} \text{ is consistent.} \\[4pt]
> &\left[\begin{array}{ccc|c} 0 & 1 & -3 & 3 \\ 2 & 4 & -1 & 5 \\ 4 & -2 & 5 & 3 \end{array}\right] \overset{R_1 \leftrightarrow R_2}{\sim} \left[\begin{array}{ccc|c} 2 & 4 & -1 & 5 \\ 0 & 1 & -3 & 3 \\ 4 & -2 & 5 & 3 \end{array}\right] \\[6pt]
> & \overset{R_3 \to R_3 - 2R_1}{\sim} \left[\begin{array}{ccc|c} 2 & 4 & -1 & 5 \\ 0 & 1 & -3 & 3 \\ 0 & -10 & 7 & -7 \end{array}\right] \overset{R_3 \to R_3 + 10R_2}{\sim} \left[\begin{array}{ccc|c} 2 & 4 & -1 & 5 \\ 0 & 1 & -3 & 3 \\ 0 & 0 & -23 & 23 \end{array}\right]
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &-23x_3 = 23 \implies x_3 = -1 \\
> &x_2 - 3x_3 = 3 \implies x_2 = 0 \\
> &2x_1 + 4x_2 - x_3 = 5 \implies x_1 = 2 \\
> &\text{Hence } \mathbf{b} = 2\mathbf{v}_1 - \mathbf{v}_3, \text{ so } \mathbf{b} \text{ is in the span.}
> \end{aligned}
> $$
>
> \# The vectors $\mathbf{v}_i$ are the columns of the coefficient matrix. For "is $\mathbf{b}$ in the span" the row-echelon form is enough: no row $[0\ 0\ 0 \mid c]$ with $c \ne 0$ means Yes.

### FB 1.4.29
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.29|FB 1.4.29]]

> [!solution] Solution
> - a. **F.** $x + y = 1$, $x + y = 2$ has no solution.
> - b. **F.** The same system.
> - c. **T.** $x + y = 1$, $2x + 2y = 2$, $3x + 3y = 3$.
> - d. **T.** $x + y + z = 0$, $x + y + z = 1$.
> - e. **F.** $\begin{bmatrix} 1 & 2 \end{bmatrix} \sim \begin{bmatrix} 2 & 4 \end{bmatrix}$, and both are in row-echelon form.
> - f. **T.** The reduced row-echelon form of a matrix is unique.
> - g. **T.** Elementary row operations do not change the solution set.
> - h. **T.** Unique solution $\iff$ a pivot in every column of an echelon form of $A$ $\iff$ $n$ pivots in an $n \times n$ matrix $\iff$ $A \sim I$.
> - i. **F.** The system may be inconsistent: $x + y = 1$, $x + y = 2$ has a column without a pivot and no solution.
> - j. **T.** Consistent, and a column without a pivot $\iff$ a free variable $\iff$ infinitely many solutions.
>
> \# a., b. The number of equations decides nothing; the pivots do. i. and j. differ only by the word "consistent".

### FB 1.4.40
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.40|FB 1.4.40]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 1 & 1 & -1 & b_1 \\ 0 & 2 & 1 & b_2 \\ 0 & 1 & -1 & b_3 \end{array}\right] \overset{R_3 \to R_3 - \tfrac{1}{2}R_2}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & -1 & b_1 \\ 0 & 2 & 1 & b_2 \\ 0 & 0 & -\tfrac{3}{2} & b_3 - \tfrac{1}{2}b_2 \end{array}\right] \\[4pt]
> &\because \text{every row has a pivot to the left of the partition} \\
> &\therefore \text{there is no row } [0\ 0\ 0 \mid c],\ c \ne 0. \\
> &\text{Hence the system is consistent for all } b_1, b_2, b_3 \in \mathbb{R}.
> \end{aligned}
> $$
>
> \# A condition on the $b_i$ appears only when a row of the coefficient part becomes zero; then its right side must be $0$.

### FB 1.4.58
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.4.58|FB 1.4.58]]

> [!proof] Proof of a.
> $$
> \begin{aligned}
> &\text{Reduce } [A \mid \mathbf{c}] \sim [H \mid \mathbf{c}'],\ H \text{ in row-echelon form.} \\
> &\because A\mathbf{x} = \mathbf{c} \text{ has a unique solution} \\
> &\therefore \text{there is no free variable} \implies \text{every column of } H \text{ has a pivot} \implies H \text{ has } n \text{ pivots.} \\
> &\text{Since each row has at most one pivot, } n \le m. \qquad \blacksquare
> \end{aligned}
> $$

> [!solution] Solution
> **b.** Yes.
> $$
> \begin{aligned}
> &m = n \implies H \text{ has } n \text{ pivots in } n \text{ rows} \implies H \text{ has no zero row.} \\
> &\implies [A \mid \mathbf{b}] \sim [H \mid \mathbf{b}'] \text{ has no row } [0 \cdots 0 \mid c],\ c \ne 0. \\
> &\text{Hence } A\mathbf{x} = \mathbf{b} \text{ is consistent for every } \mathbf{b}.
> \end{aligned}
> $$
> **c.** No.
> $$
> \begin{aligned}
> &m > n \implies H \text{ has only } n \text{ pivots} \implies \text{row } m \text{ of } H \text{ is zero.} \\
> &\text{Let } P = E_k \cdots E_1 \text{ with } PA = H, \text{ and let } \mathbf{b} = P^{-1}\mathbf{e}_m. \\
> &\implies [A \mid \mathbf{b}] \sim [PA \mid P\mathbf{b}] = [H \mid \mathbf{e}_m], \text{ with last row } [0 \cdots 0 \mid 1]. \\
> &\text{Hence } A\mathbf{x} = \mathbf{b} \text{ is inconsistent for this } \mathbf{b}.
> \end{aligned}
> $$
>
> \# Count pivots: one per column (unique solution), at most one per row. In c., $\mathbf{e}_m$ is the column vector with $1$ in the last place; undoing the row operations on $[H \mid \mathbf{e}_m]$ gives the bad $\mathbf{b}$.

## FB §1.5 Additional Exercises

> [!note] Note
> These exercises are not assigned. Each one adds a type of problem that the assigned exercises do not cover.
> - 5: finding $A^{-1}$ from $[A \mid I]$, and writing $A$ as a product of elementary matrices.
> - 13: solving a system with $A^{-1}$.
> - 21: invertibility with an unknown entry.
> - 22: row equivalence as $CA = B$; it finishes the $(\impliedby)$ direction left open in [[LA1 Lecture 2026-09-29]].
> - 26: the proof behind items e. and f. of Exercise 23.
> - 30: a short proof with $A^{-1}$ and an [[Idempotent Matrix|idempotent matrix]].
> - 35: the inverse of a $2 \times 2$ matrix.

### FB 1.5.5
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.5|FB 1.5.5]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|ccc} 1 & 0 & 1 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & -1 & 0 & 0 & 1 \end{array}\right] \overset{R_3 \to -R_3}{\sim} \left[\begin{array}{ccc|ccc} 1 & 0 & 1 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & 1 & 0 & 0 & -1 \end{array}\right] \\[6pt]
> & \overset{\substack{R_1 \to R_1 - R_3 \\ R_2 \to R_2 - R_3}}{\sim} \left[\begin{array}{ccc|ccc} 1 & 0 & 0 & 1 & 0 & 1 \\ 0 & 1 & 0 & 0 & 1 & 1 \\ 0 & 0 & 1 & 0 & 0 & -1 \end{array}\right]
> \end{aligned}
> $$
> $$
> A^{-1} = \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & -1 \end{bmatrix} = A
> $$
> **(b)**
> $$
> \begin{aligned}
> &E_1: R_3 \to -R_3, \quad E_2: R_1 \to R_1 - R_3, \quad E_3: R_2 \to R_2 - R_3 \\
> &E_3E_2E_1A = I \implies A = E_1^{-1}E_2^{-1}E_3^{-1} \\
> &A = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & -1 \end{bmatrix} \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{bmatrix}
> \end{aligned}
> $$
>
> \# (b) Each $E_t^{-1}$ is the matrix of the undoing operation: $R_3 \to -R_3$, $R_1 \to R_1 + R_3$, $R_2 \to R_2 + R_3$. The order turns around: $(E_3E_2E_1)^{-1} = E_1^{-1}E_2^{-1}E_3^{-1}$. The answer is not unique.

### FB 1.5.13
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.13|FB 1.5.13]]

> [!solution] Solution
> **a.**
> $$
> \begin{aligned}
> &\left[\begin{array}{cc|cc} 2 & -3 & 1 & 0 \\ 5 & -7 & 0 & 1 \end{array}\right] \overset{R_1 \to \tfrac{1}{2}R_1}{\sim} \left[\begin{array}{cc|cc} 1 & -\tfrac{3}{2} & \tfrac{1}{2} & 0 \\ 5 & -7 & 0 & 1 \end{array}\right] \\[6pt]
> & \overset{R_2 \to R_2 - 5R_1}{\sim} \left[\begin{array}{cc|cc} 1 & -\tfrac{3}{2} & \tfrac{1}{2} & 0 \\ 0 & \tfrac{1}{2} & -\tfrac{5}{2} & 1 \end{array}\right] \overset{R_2 \to 2R_2}{\sim} \left[\begin{array}{cc|cc} 1 & -\tfrac{3}{2} & \tfrac{1}{2} & 0 \\ 0 & 1 & -5 & 2 \end{array}\right] \overset{R_1 \to R_1 + \tfrac{3}{2}R_2}{\sim} \left[\begin{array}{cc|cc} 1 & 0 & -7 & 3 \\ 0 & 1 & -5 & 2 \end{array}\right]
> \end{aligned}
> $$
> $$
> A \sim I \implies A \text{ is invertible, and } A^{-1} = \begin{bmatrix} -7 & 3 \\ -5 & 2 \end{bmatrix}.
> $$
> **b.**
> $$
> \begin{aligned}
> &A\mathbf{x} = \mathbf{b},\ \mathbf{b} = \begin{bmatrix} 4 \\ -3 \end{bmatrix} \implies \mathbf{x} = A^{-1}\mathbf{b} = \begin{bmatrix} -7 & 3 \\ -5 & 2 \end{bmatrix}\begin{bmatrix} 4 \\ -3 \end{bmatrix} = \begin{bmatrix} -37 \\ -26 \end{bmatrix} \\
> &\text{Hence } x_1 = -37,\ x_2 = -26.
> \end{aligned}
> $$
>
> \# Check: $2(-37) - 3(-26) = 4$ and $5(-37) - 7(-26) = -3$.

### FB 1.5.21
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.21|FB 1.5.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\begin{bmatrix} 2 & 4 & 2 \\ 1 & r & 3 \\ 1 & 1 & 2 \end{bmatrix} \overset{R_1 \to \tfrac{1}{2}R_1}{\sim} \begin{bmatrix} 1 & 2 & 1 \\ 1 & r & 3 \\ 1 & 1 & 2 \end{bmatrix} \overset{\substack{R_2 \to R_2 - R_1 \\ R_3 \to R_3 - R_1}}{\sim} \begin{bmatrix} 1 & 2 & 1 \\ 0 & r - 2 & 2 \\ 0 & -1 & 1 \end{bmatrix} \\[6pt]
> &\overset{R_2 \leftrightarrow R_3}{\sim} \begin{bmatrix} 1 & 2 & 1 \\ 0 & -1 & 1 \\ 0 & r - 2 & 2 \end{bmatrix} \overset{R_3 \to R_3 + (r - 2)R_2}{\sim} \begin{bmatrix} 1 & 2 & 1 \\ 0 & -1 & 1 \\ 0 & 0 & r \end{bmatrix} \\[6pt]
> &\text{The matrix is invertible} \iff \text{it is row equivalent to } I \iff \text{three pivots} \iff r \ne 0. \\
> &\text{Hence } r \ne 0.
> \end{aligned}
> $$
>
> \# Interchange rows 2 and 3 first, so that no division by $r - 2$ is needed. In Exercise 20 row 1 is $2$ times row 3, so that matrix is singular for every $r$.

### FB 1.5.22
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.22|FB 1.5.22]]

> [!proof] Proof
> $$
> \begin{aligned}
> (\implies)\ \ &A \sim B \implies \exists\, E_1, \dots, E_k \text{ elementary s.t. } B = E_k \cdots E_1A. \\
> &\text{Let } C = E_k \cdots E_1. \\
> &\because \text{each } E_t \text{ is invertible} \\
> &\therefore C \text{ is invertible, } m \times m, \text{ and } CA = B. \\[4pt]
> (\impliedby)\ \ &\because C \text{ is invertible} \\
> &\therefore C = E_k \cdots E_1 \text{ for some elementary } E_1, \dots, E_k. \\
> &\implies B = CA = E_k \cdots E_1A \\
> &\text{Hence } B \text{ is obtained from } A \text{ by elementary row operations: } A \sim B. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $(\implies)$ uses: a product of invertible matrices is invertible. $(\impliedby)$ uses: every invertible matrix is a product of elementary matrices.

### FB 1.5.26
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.26|FB 1.5.26]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } D = (A^2)^{-1}, \text{ so } A^2D = DA^2 = I. \\
> &A(AD) = A^2D = I, \qquad (DA)A = DA^2 = I \\
> &AD = \big((DA)A\big)(AD) = (DA)\big(A(AD)\big) = DA \\
> &\text{Let } C = AD = DA. \text{ Then } AC = CA = I. \\
> &\text{Hence } A \text{ is invertible, and } A^{-1} = A(A^2)^{-1}. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $A^2 = AA$ is defined only for a square $A$. The third line shows that the right inverse $AD$ and the left inverse $DA$ are the same matrix.

### FB 1.5.30
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.30|FB 1.5.30]]

> [!solution] Solution
> **a.**
> $$
> A = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}: \qquad A^2 = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} = A, \qquad A \ne O,\ A \ne I
> $$

> [!proof] Proof of b.
> $$
> \begin{aligned}
> &\because A^2 = A,\ A^{-1} \text{ exists} \\
> &\therefore A^{-1}(A^2) = A^{-1}A \implies (A^{-1}A)A = I \implies A = I. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# b. Multiply both sides by $A^{-1}$ on the same side. So an idempotent matrix other than $I$ is singular.

### FB 1.5.35
Question: [[LA1 HW 1.4 1.5 Questions#FB 1.5.35|FB 1.5.35]]

> [!proof] Proof of a.
> $$
> \begin{aligned}
> &\begin{bmatrix} a & b \\ c & d \end{bmatrix}\begin{bmatrix} d/h & -b/h \\ -c/h & a/h \end{bmatrix} = \frac{1}{h}\begin{bmatrix} ad - bc & -ab + ba \\ cd - dc & -cb + da \end{bmatrix} = \frac{1}{h}\begin{bmatrix} h & 0 \\ 0 & h \end{bmatrix} = I \\[4pt]
> &\begin{bmatrix} d/h & -b/h \\ -c/h & a/h \end{bmatrix}\begin{bmatrix} a & b \\ c & d \end{bmatrix} = \frac{1}{h}\begin{bmatrix} da - bc & db - bd \\ -ca + ac & -cb + ad \end{bmatrix} = \frac{1}{h}\begin{bmatrix} h & 0 \\ 0 & h \end{bmatrix} = I \\[4pt]
> &\text{Hence the matrix is the inverse of } A. \qquad \blacksquare
> \end{aligned}
> $$

> [!proof] Proof of b.
> $$
> \begin{aligned}
> (\impliedby)\ \ &h \ne 0 \implies A \text{ is invertible, by part a.} \\[4pt]
> (\implies)\ \ &\text{Suppose } A \text{ is invertible and } h = 0. \text{ Let } B = \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}. \\
> &AB = \begin{bmatrix} h & 0 \\ 0 & h \end{bmatrix} = O \implies B = A^{-1}(AB) = A^{-1}O = O \\
> &\implies a = b = c = d = 0 \implies A = O, \text{ which is singular. Contradiction.} \\
> &\text{Hence } h \ne 0. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# To remember: interchange $a$ and $d$, change the signs of $b$ and $c$, divide by $h = ad - bc$. With Exercise 13: $h = 2(-7) - (-3)(5) = 1$.

## NIC §1.2 Gaussian Elimination

> [!note] Note
> These exercises are not assigned. They are from Nicholson, *Linear Algebra with Applications* (see the Questions note), and each one adds a type of problem that the FB exercises above do not cover.
> - 1.2.8: a system with letters in the coefficients; split into cases.
> - 2.4.5: solving a matrix equation for $A$ by undoing inverses.
> - 2.4.21: short proofs from $AB = 0$.
> - 2.4.24: an inverse read off from a polynomial equation in $A$.
> - 2.4.28: $(I - A)^{-1}$ for a nilpotent $A$.
> - 2.4.34: $AB$ invertible $\implies$ $A$ and $B$ invertible.
> - 2.5.9: the transpose of an elementary matrix.
> - 2.5.14: why the reduction $[A \mid I] \sim [I \mid A^{-1}]$ works.

### NIC 1.2.8
Question: [[LA1 HW 1.4 1.5 Questions#NIC 1.2.8|NIC 1.2.8]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{cc|c} 1 & b & -1 \\ a & 2 & 5 \end{array}\right] \overset{R_2 \to R_2 - aR_1}{\sim} \left[\begin{array}{cc|c} 1 & b & -1 \\ 0 & 2 - ab & 5 + a \end{array}\right] \\[6pt]
> &ab \ne 2: && \text{a pivot in each column} \implies \text{one solution.} \\
> &ab = 2,\ a \ne -5: && \text{row 2 is } [0\ 0 \mid 5 + a],\ 5 + a \ne 0 \implies \text{no solution.} \\
> &ab = 2,\ a = -5: && \text{row 2 is } [0\ 0 \mid 0],\ y \text{ is free} \implies \text{infinitely many solutions.}
> \end{aligned}
> $$
> The last case is $a = -5$, $b = -\tfrac{2}{5}$.
>
> \# Reduce with the letters in place, then ask of the last row: is the pivot place $0$? If it is, is the right side $0$ too? This is [[LA1 HW 1.4 1.5 Questions#FB 1.4.40|FB 1.4.40]] with the letters on the left side.

## NIC §2.4 Matrix Inverses

> [!note] Notation
> In this section and the next, the zero matrix is $0$, as in Nicholson.

### NIC 2.4.5
Question: [[LA1 HW 1.4 1.5 Questions#NIC 2.4.5|NIC 2.4.5]]

> [!solution] Solution
> **(1)**
> $$
> \begin{aligned}
> &3A = \left((3A)^{-1}\right)^{-1} = \begin{bmatrix} 1 & -1 \\ 0 & 1 \end{bmatrix}^{-1} = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix} \\
> &\text{Hence } A = \tfrac{1}{3}\begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} \tfrac{1}{3} & \tfrac{1}{3} \\ 0 & \tfrac{1}{3} \end{bmatrix}.
> \end{aligned}
> $$
> **(3)**
> $$
> \begin{aligned}
> &I + 3A = \begin{bmatrix} 2 & 0 \\ 1 & -1 \end{bmatrix}^{-1} = \frac{1}{-2}\begin{bmatrix} -1 & 0 \\ -1 & 2 \end{bmatrix} = \begin{bmatrix} \tfrac{1}{2} & 0 \\ \tfrac{1}{2} & -1 \end{bmatrix} \\
> &3A = \begin{bmatrix} \tfrac{1}{2} & 0 \\ \tfrac{1}{2} & -1 \end{bmatrix} - I = \begin{bmatrix} -\tfrac{1}{2} & 0 \\ \tfrac{1}{2} & -2 \end{bmatrix} \\
> &\text{Hence } A = \begin{bmatrix} -\tfrac{1}{6} & 0 \\ \tfrac{1}{6} & -\tfrac{2}{3} \end{bmatrix}.
> \end{aligned}
> $$
>
> \# Undo from the outside in: first the inverse, by $(X^{-1})^{-1} = X$, then the $I$, then the $3$. The $2 \times 2$ inverses are from the formula of [[LA1 HW 1.4 1.5 Questions#FB 1.5.35|FB 1.5.35]].

### NIC 2.4.21
Question: [[LA1 HW 1.4 1.5 Questions#NIC 2.4.21|NIC 2.4.21]]

> [!proof] Proof
> **(1)**
> $$
> \begin{aligned}
> &A^{-1} \text{ exists} \implies B = A^{-1}(AB) = A^{-1}0 = 0 \\
> &B^{-1} \text{ exists} \implies A = (AB)B^{-1} = 0B^{-1} = 0
> \end{aligned}
> $$
> **(2)**
> $$
> \begin{aligned}
> &\text{Suppose } A^{-1},\ B^{-1} \text{ both exist. By (1), } B = 0. \\
> &\text{But } 0X = 0 \ne I \text{ for every } X, \text{ so } 0 \text{ has no inverse. Contradiction.}
> \end{aligned}
> $$
> **(3)**
> $$
> (BA)^2 = (BA)(BA) = B(AB)A = B0A = 0 \qquad \blacksquare
> $$
>
> \# (3) $BA$ itself need not be $0$: $A = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$, $B = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$ give $AB = 0$ and $BA = A \ne 0$.

### NIC 2.4.24
Question: [[LA1 HW 1.4 1.5 Questions#NIC 2.4.24|NIC 2.4.24]]

> [!solution] Solution
> $$
> \begin{aligned}
> &A^3 - 3A + 2I = 0 \implies 3A - A^3 = 2I \\
> &\implies A\left[\tfrac{1}{2}(3I - A^2)\right] = I = \left[\tfrac{1}{2}(3I - A^2)\right]A \\
> &\text{Hence } A \text{ is invertible and } A^{-1} = \tfrac{1}{2}(3I - A^2).
> \end{aligned}
> $$
>
> \# Move the $I$ term to one side, factor $A$ out of the rest, and divide by the number in front of $I$. $A$ can be factored out on the left and on the right, so both products are $I$. The method needs the $I$ term to be nonzero.

### NIC 2.4.28
Question: [[LA1 HW 1.4 1.5 Questions#NIC 2.4.28|NIC 2.4.28]]

> [!proof] Proof of (1) and (2)
> $$
> \begin{aligned}
> (1)\ \ &(I - A)(I + A) = I + A - A - A^2 = I - A^2 = I = (I + A)(I - A) \\
> (2)\ \ &(I - A)(I + A + A^2) = I + A + A^2 - A - A^2 - A^3 = I - A^3 = I = (I + A + A^2)(I - A) \qquad \blacksquare
> \end{aligned}
> $$

> [!solution] Solution
> **(3)**
> $$
> \begin{aligned}
> &\begin{bmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \\ 0 & 0 & 1 \end{bmatrix} = I - A, \qquad A = \begin{bmatrix} 0 & -2 & 1 \\ 0 & 0 & -3 \\ 0 & 0 & 0 \end{bmatrix} \\
> &A^2 = \begin{bmatrix} 0 & 0 & 6 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}, \qquad A^3 = 0 \\
> &\text{By (2): } (I - A)^{-1} = I + A + A^2 = \begin{bmatrix} 1 & -2 & 7 \\ 0 & 1 & -3 \\ 0 & 0 & 1 \end{bmatrix}
> \end{aligned}
> $$
>
> \# The pattern is the geometric series $\tfrac{1}{1 - x} = 1 + x + x^2 + \cdots$, which stops because a power of $A$ is $0$. In (3), $A$ is strictly upper triangular, so its powers move up and vanish.

### NIC 2.4.34
Question: [[LA1 HW 1.4 1.5 Questions#NIC 2.4.34|NIC 2.4.34]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } D = (AB)^{-1}, \text{ so } (AB)D = D(AB) = I. \\
> &A(BD) = I \implies (BD)A = I && (A,\ BD \text{ are } n \times n) \\
> &\implies A \text{ is invertible, and } A^{-1} = BD. \\
> &B = A^{-1}(AB) \text{ is a product of invertible matrices} \implies B \text{ is invertible.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The second line uses: for square matrices, $AC = I \implies CA = I$. It is a theorem of FB §1.5, and it is false when the matrices are not square. With [[LA1 HW 1.4 1.5 Questions#FB 1.5.23|FB 1.5.23]] c.: $AB$ is invertible $\iff$ $A$ and $B$ are both invertible.

## NIC §2.5 Elementary Matrices

### NIC 2.5.9
Question: [[LA1 HW 1.4 1.5 Questions#NIC 2.5.9|NIC 2.5.9]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Type I, } E = I \text{ after } R_i \leftrightarrow R_j: && E \text{ differs from } I \text{ only in the entries } (i, i),\ (j, j) = 0 \text{ and } (i, j),\ (j, i) = 1 \\
> & && \implies E^T = E. \\
> &\text{Type II, } E = I \text{ after } R_i \to sR_i: && E \text{ is diagonal} \implies E^T = E. \\
> &\text{Type III, } E = I \text{ after } R_i \to R_i + sR_j: && E \text{ is } I \text{ with the entry } s \text{ at } (i, j) \\
> & && \implies E^T \text{ is } I \text{ with the entry } s \text{ at } (j, i) \\
> & && \implies E^T = I \text{ after } R_j \to R_j + sR_i, \text{ type III.}
> \end{aligned}
> $$
> Hence $E^T$ is elementary of the same type, and $E^T = E$ for types I and II. $\blacksquare$
>
> \# For type III the two rows change roles, as in [[LA1 HW 1.4 1.5 Questions#FB 1.5.36|FB 1.5.36]]. With $(EA)^T = A^TE^T$, this turns a row operation on $A$ into a column operation on $A^T$.

### NIC 2.5.14
Question: [[LA1 HW 1.4 1.5 Questions#NIC 2.5.14|NIC 2.5.14]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{The row operations are a left multiplication by } U = E_k \cdots E_1,\ E_t \text{ elementary.} \\
> &U[A \mid I] = [UA \mid UI] = [UA \mid U] = [P \mid Q] \\
> &\implies UA = P,\ U = Q \\
> &\text{Hence } P = QA. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The right half records the product of all the elementary matrices used so far. If $P = I$, then $QA = I$ and $Q = A^{-1}$: this is why $[A \mid I] \sim [I \mid A^{-1}]$ gives the inverse.
