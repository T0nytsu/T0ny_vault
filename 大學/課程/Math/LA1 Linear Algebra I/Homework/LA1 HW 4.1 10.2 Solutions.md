---
course: [LA1]
semester: "115-1"
chapter: ["4.1", "10.2"]
tags: [linear-algebra, homework, solutions, determinants, vectors, linear-systems]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-10-26
questions: "[[LA1 HW 4.1 10.2 Questions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 4.1 10.2 Questions#FB 4.1.6\|FB 4.1.6]] | $41$ |
| [[LA1 HW 4.1 10.2 Questions#FB 4.1.12\|FB 4.1.12]] | Proof |
| [[LA1 HW 4.1 10.2 Questions#FB 4.1.13\|FB 4.1.13]] | $-6\mathbf{i} + 3\mathbf{j} + 5\mathbf{k}$ |
| [[LA1 HW 4.1 10.2 Questions#FB 4.1.21\|FB 4.1.21]] | $38$ |
| [[LA1 HW 4.1 10.2 Questions#FB 4.1.23\|FB 4.1.23]] | $\sqrt{62}$ |
| [[LA1 HW 4.1 10.2 Questions#FB 4.1.25\|FB 4.1.25]] | $\tfrac{19}{2}$ |
| [[LA1 HW 4.1 10.2 Questions#FB 10.2.4\|FB 10.2.4]] | $\mathbf{x} = [-4, -1]$ |
| [[LA1 HW 4.1 10.2 Questions#FB 10.2.5\|FB 10.2.5]] | $\mathbf{x} = [-27, -11, -1]$ |
| [[LA1 HW 4.1 10.2 Questions#FB 10.2.6\|FB 10.2.6]] | $\mathbf{x} = [1, -1, -4]$ |
| [[LA1 HW 4.1 10.2 Questions#FB 10.2.7\|FB 10.2.7]] | $\mathbf{x} = [1, -2, 1, 3]$ |

Exam problems from other universities, not assigned:

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 4.1 10.2 Questions#WEB 4.1.1\|WEB 4.1.1]] | 3) T; 7) F; 11) T |
| [[LA1 HW 4.1 10.2 Questions#WEB 4.1.2\|WEB 4.1.2]] | a) $(6, 0, 0)$, $(0, 2, 0)$, $(0, 0, 3)$; b) $3\sqrt{14}$ |
| [[LA1 HW 4.1 10.2 Questions#WEB 4.1.3\|WEB 4.1.3]] | 2) F; 11) T; 16) T |
| [[LA1 HW 4.1 10.2 Questions#WEB 10.2.1\|WEB 10.2.1]] | (a) $L = \begin{bmatrix} 1 & 0 & 0 \\ 1 & 1 & 0 \\ 1 & 2 & 1 \end{bmatrix}$, $U = \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 2 \\ 0 & 0 & 1 \end{bmatrix}$; (b) $x = [3, -3, 1]$ |
| [[LA1 HW 4.1 10.2 Questions#WEB 10.2.2\|WEB 10.2.2]] | (a) $L = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ -1 & -1 & 1 \end{bmatrix}$, $D = \operatorname{diag}(2, -1, 3)$, $U = \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 3 \\ 0 & 0 & 1 \end{bmatrix}$; (b) only $x = [-2, 1, 2]$ |
| [[LA1 HW 4.1 10.2 Questions#WEB 10.2.3\|WEB 10.2.3]] | (h) F; (j) F as stated ($A = O$), T for invertible $A$ |

## FB §4.1 Areas, Volumes, and Cross Products

> [!note] Note
> The facts that the answers use.
> - **[[Determinant|Determinants]]** of order 2 and 3; order 3 is expanded along row 1:
> $$
> \begin{vmatrix} a_1 & a_2 \\ b_1 & b_2 \end{vmatrix} = a_1b_2 - a_2b_1, \qquad \begin{vmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{vmatrix} = a_1\begin{vmatrix} b_2 & b_3 \\ c_2 & c_3 \end{vmatrix} - a_2\begin{vmatrix} b_1 & b_3 \\ c_1 & c_3 \end{vmatrix} + a_3\begin{vmatrix} b_1 & b_2 \\ c_1 & c_2 \end{vmatrix}
> $$
> - **[[Cross Product]]**: $\mathbf{b} \times \mathbf{c} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{vmatrix}$, expanded along row 1 like a $3 \times 3$ determinant. It is perpendicular to $\mathbf{b}$ and to $\mathbf{c}$, and $\lVert \mathbf{b} \times \mathbf{c} \rVert = \lVert \mathbf{b} \rVert \lVert \mathbf{c} \rVert \sin\theta$.
> - **Area**: the parallelogram with edges $\mathbf{a} = [a_1, a_2]$ and $\mathbf{b} = [b_1, b_2]$ in $\mathbb{R}^2$ has area $\left\lvert \det \begin{bmatrix} a_1 & a_2 \\ b_1 & b_2 \end{bmatrix} \right\rvert$; with edges $\mathbf{a}$, $\mathbf{b}$ in $\mathbb{R}^3$ it has area $\lVert \mathbf{a} \times \mathbf{b} \rVert$. A triangle is half of the parallelogram on two of its edges.
> - **Volume**: the box with edges $\mathbf{a}$, $\mathbf{b}$, $\mathbf{c}$ has volume $\lvert \mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) \rvert$, the absolute value of the determinant with rows $\mathbf{a}$, $\mathbf{b}$, $\mathbf{c}$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FB 4.1.6
Question: [[LA1 HW 4.1 10.2 Questions#FB 4.1.6|FB 4.1.6]]

> [!solution] Solution
> $$
> \begin{aligned}
> \begin{vmatrix} 1 & 4 & -2 \\ 5 & 13 & 0 \\ 2 & -1 & 3 \end{vmatrix} &= 1\begin{vmatrix} 13 & 0 \\ -1 & 3 \end{vmatrix} - 4\begin{vmatrix} 5 & 0 \\ 2 & 3 \end{vmatrix} + (-2)\begin{vmatrix} 5 & 13 \\ 2 & -1 \end{vmatrix} \\
> &= 1(39 - 0) - 4(15 - 0) - 2(-5 - 26) \\
> &= 39 - 60 + 62 = 41.
> \end{aligned}
> $$
>
> \# The sign pattern along row 1 is $+, -, +$; the third term is $(-2)(-31) = +62$, where it is easy to lose a sign. Check with the diagonal rule for order 3: $(39 + 0 + 10) - (-52 + 0 + 60) = 49 - 8 = 41$.

### FB 4.1.12
Question: [[LA1 HW 4.1 10.2 Questions#FB 4.1.12|FB 4.1.12]]

> [!proof] Proof
> Expand both determinants along row 1.
> $$
> \begin{aligned}
> \begin{vmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{vmatrix} &= a_1\begin{vmatrix} b_2 & b_3 \\ c_2 & c_3 \end{vmatrix} - a_2\begin{vmatrix} b_1 & b_3 \\ c_1 & c_3 \end{vmatrix} + a_3\begin{vmatrix} b_1 & b_2 \\ c_1 & c_2 \end{vmatrix} \\
> &= a_1(b_2c_3 - b_3c_2) - a_2(b_1c_3 - b_3c_1) + a_3(b_1c_2 - b_2c_1). \\[6pt]
> \begin{vmatrix} a_1 & a_2 & a_3 \\ c_1 & c_2 & c_3 \\ b_1 & b_2 & b_3 \end{vmatrix} &= a_1\begin{vmatrix} c_2 & c_3 \\ b_2 & b_3 \end{vmatrix} - a_2\begin{vmatrix} c_1 & c_3 \\ b_1 & b_3 \end{vmatrix} + a_3\begin{vmatrix} c_1 & c_2 \\ b_1 & b_2 \end{vmatrix} \\
> &= a_1(c_2b_3 - c_3b_2) - a_2(c_1b_3 - c_3b_1) + a_3(c_1b_2 - c_2b_1) \\
> &= -\big[a_1(b_2c_3 - b_3c_2) - a_2(b_1c_3 - b_3c_1) + a_3(b_1c_2 - b_2c_1)\big] \\
> &= -\begin{vmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{vmatrix}.
> \end{aligned}
> $$
> Multiplying by $-1$ gives the identity. $\blacksquare$
>
> \# The minus sign comes from the three $2 \times 2$ minors: each minor on the right is the minor on the left with its two rows interchanged, and that changes its sign (Exercise 11): for example $c_2b_3 - c_3b_2 = -(b_2c_3 - b_3c_2)$, by commutativity of multiplication in $\mathbb{R}$. Row 1 and the coefficients $a_1, -a_2, a_3$ stay the same.

### FB 4.1.13
Question: [[LA1 HW 4.1 10.2 Questions#FB 4.1.13|FB 4.1.13]]

> [!solution] Solution
> $$
> \begin{aligned}
> \mathbf{a} \times \mathbf{b} &= \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & -1 & 3 \\ 1 & 2 & 0 \end{vmatrix} = \begin{vmatrix} -1 & 3 \\ 2 & 0 \end{vmatrix}\mathbf{i} - \begin{vmatrix} 2 & 3 \\ 1 & 0 \end{vmatrix}\mathbf{j} + \begin{vmatrix} 2 & -1 \\ 1 & 2 \end{vmatrix}\mathbf{k} \\
> &= (0 - 6)\mathbf{i} - (0 - 3)\mathbf{j} + (4 + 1)\mathbf{k} = -6\mathbf{i} + 3\mathbf{j} + 5\mathbf{k}.
> \end{aligned}
> $$
>
> \# Write $\mathbf{b} = \mathbf{i} + 2\mathbf{j} + 0\mathbf{k}$ before filling in row 3. Check that the answer is perpendicular to both vectors: $\mathbf{a} \cdot (\mathbf{a} \times \mathbf{b}) = -12 - 3 + 15 = 0$ and $\mathbf{b} \cdot (\mathbf{a} \times \mathbf{b}) = -6 + 6 + 0 = 0$.

### FB 4.1.21
Question: [[LA1 HW 4.1 10.2 Questions#FB 4.1.21|FB 4.1.21]]

> [!solution] Solution
> $$
> \text{Area} = \left\lvert \det \begin{bmatrix} -5 & 3 \\ 1 & 7 \end{bmatrix} \right\rvert = \lvert (-5)(7) - (3)(1) \rvert = \lvert -38 \rvert = 38.
> $$
>
> \# The determinant is negative because the second edge lies clockwise from the first; the area is its absolute value.

### FB 4.1.23
Question: [[LA1 HW 4.1 10.2 Questions#FB 4.1.23|FB 4.1.23]]

> [!solution] Solution
> $$
> \begin{aligned}
> \mathbf{a} \times \mathbf{b} &= \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & -1 & 1 \\ 1 & 3 & -1 \end{vmatrix} = (1 - 3)\mathbf{i} - (-2 - 1)\mathbf{j} + (6 + 1)\mathbf{k} = -2\mathbf{i} + 3\mathbf{j} + 7\mathbf{k} \\
> \text{Area} &= \lVert \mathbf{a} \times \mathbf{b} \rVert = \sqrt{(-2)^2 + 3^2 + 7^2} = \sqrt{62}.
> \end{aligned}
> $$
>
> \# In $\mathbb{R}^3$ two vectors do not form a $2 \times 2$ matrix, so the area is the length of the cross product, as in the Note above.

### FB 4.1.25
Question: [[LA1 HW 4.1 10.2 Questions#FB 4.1.25|FB 4.1.25]]

> [!solution] Solution
> $$
> \begin{aligned}
> &P = (-1, 2),\ Q = (3, -1),\ R = (4, 3) \\
> &\text{Edges from } P:\ \mathbf{a} = Q - P = [4, -3],\ \mathbf{b} = R - P = [5, 1] \\
> &\text{Area} = \tfrac{1}{2}\left\lvert \det \begin{bmatrix} 4 & -3 \\ 5 & 1 \end{bmatrix} \right\rvert = \tfrac{1}{2}\lvert 4 + 15 \rvert = \tfrac{19}{2}.
> \end{aligned}
> $$
>
> \# The triangle is half of the parallelogram with edges $\mathbf{a}$ and $\mathbf{b}$. Any vertex can be the starting point; from $Q$, the edges $[1, 4]$ and $[-4, 3]$ give $\tfrac{1}{2}\lvert 3 + 16 \rvert = \tfrac{19}{2}$ again.

## FB §10.2 The LU-Factorization

> [!note] Note
> The facts that the answers use.
> - **[[LU-Factorization]]**: $A = LU$, where $L$ is lower triangular with all diagonal entries $1$ and $U$ is upper triangular. When $A$ is reduced to $U$ by row additions $R_i \to R_i - mR_j$ ($j < i$) only, the multiplier $m$ is the $(i, j)$-entry of $L$.
> - **Combined $L\backslash U$ display**: $U$ on and above the diagonal, the entries of $L$ below it; the diagonal entries $1$ of $L$ are not written. For example,
> $$
> L\backslash U = \begin{bmatrix} u_{11} & u_{12} \\ l_{21} & u_{22} \end{bmatrix} \implies L = \begin{bmatrix} 1 & 0 \\ l_{21} & 1 \end{bmatrix}, \quad U = \begin{bmatrix} u_{11} & u_{12} \\ 0 & u_{22} \end{bmatrix}.
> $$
> - **Solving** $A\mathbf{x} = \mathbf{b}$: $A\mathbf{x} = L(U\mathbf{x}) = \mathbf{b}$. Put $\mathbf{y} = U\mathbf{x}$, then (1) solve $L\mathbf{y} = \mathbf{b}$ from the top down (forward substitution), and (2) solve $U\mathbf{x} = \mathbf{y}$ from the bottom up (back substitution).
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FB 10.2.4
Question: [[LA1 HW 4.1 10.2 Questions#FB 10.2.4|FB 10.2.4]]

> [!solution] Solution
> $$
> L = \begin{bmatrix} 1 & 0 \\ -2 & 1 \end{bmatrix}, \quad U = \begin{bmatrix} -2 & 5 \\ 0 & 1 \end{bmatrix}
> $$
> $$
> \begin{aligned}
> &(1)\ L\mathbf{y} = \mathbf{b}:\ \begin{cases} y_1 = 3 \\ -2y_1 + y_2 = -7 \end{cases} \implies y_1 = 3,\ y_2 = -7 + 6 = -1 \\[6pt]
> &(2)\ U\mathbf{x} = \mathbf{y}:\ \begin{cases} -2x_1 + 5x_2 = 3 \\ x_2 = -1 \end{cases} \implies x_2 = -1,\ x_1 = \tfrac{3 - 5(-1)}{-2} = -4 \\[6pt]
> &\text{Hence } \mathbf{x} = \begin{bmatrix} -4 \\ -1 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# Check: $A = LU = \begin{bmatrix} -2 & 5 \\ 4 & -9 \end{bmatrix}$ and $A\mathbf{x} = [8 - 5, -16 + 9] = [3, -7] = \mathbf{b}$. The $-2$ below the diagonal belongs to $L$, the $-2$ on the diagonal to $U$.

### FB 10.2.5
Question: [[LA1 HW 4.1 10.2 Questions#FB 10.2.5|FB 10.2.5]]

> [!solution] Solution
> $$
> L = \begin{bmatrix} 1 & 0 & 0 \\ -2 & 1 & 0 \\ 0 & 1 & 1 \end{bmatrix}, \quad U = \begin{bmatrix} 1 & -3 & 4 \\ 0 & -1 & 9 \\ 0 & 0 & -6 \end{bmatrix}
> $$
> $$
> \begin{aligned}
> &(1)\ L\mathbf{y} = \mathbf{b}:\ \begin{cases} y_1 = 2 \\ -2y_1 + y_2 = -2 \\ y_2 + y_3 = 8 \end{cases} \implies y_1 = 2,\ y_2 = -2 + 4 = 2,\ y_3 = 8 - 2 = 6 \\[6pt]
> &(2)\ U\mathbf{x} = \mathbf{y}:\ \begin{cases} x_1 - 3x_2 + 4x_3 = 2 \\ -x_2 + 9x_3 = 2 \\ -6x_3 = 6 \end{cases} \implies x_3 = -1,\ x_2 = 9x_3 - 2 = -11,\ x_1 = 2 + 3x_2 - 4x_3 = -27 \\[6pt]
> &\text{Hence } \mathbf{x} = \begin{bmatrix} -27 \\ -11 \\ -1 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# Check: $A = LU = \begin{bmatrix} 1 & -3 & 4 \\ -2 & 5 & 1 \\ 0 & -1 & 3 \end{bmatrix}$ and $A\mathbf{x} = [-27 + 33 - 4, 54 - 55 - 1, 11 - 3] = [2, -2, 8] = \mathbf{b}$.

### FB 10.2.6
Question: [[LA1 HW 4.1 10.2 Questions#FB 10.2.6|FB 10.2.6]]

> [!solution] Solution
> $$
> L = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 3 & 2 & 1 \end{bmatrix}, \quad U = \begin{bmatrix} 1 & -4 & 2 \\ 0 & 2 & -1 \\ 0 & 0 & -2 \end{bmatrix}
> $$
> $$
> \begin{aligned}
> &(1)\ L\mathbf{y} = \mathbf{b}:\ \begin{cases} y_1 = -3 \\ y_2 = 2 \\ 3y_1 + 2y_2 + y_3 = 3 \end{cases} \implies y_1 = -3,\ y_2 = 2,\ y_3 = 3 + 9 - 4 = 8 \\[6pt]
> &(2)\ U\mathbf{x} = \mathbf{y}:\ \begin{cases} x_1 - 4x_2 + 2x_3 = -3 \\ 2x_2 - x_3 = 2 \\ -2x_3 = 8 \end{cases} \implies x_3 = -4,\ x_2 = \tfrac{2 + x_3}{2} = -1,\ x_1 = -3 + 4x_2 - 2x_3 = 1 \\[6pt]
> &\text{Hence } \mathbf{x} = \begin{bmatrix} 1 \\ -1 \\ -4 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# Check: $A = LU = \begin{bmatrix} 1 & -4 & 2 \\ 0 & 2 & -1 \\ 3 & -8 & 2 \end{bmatrix}$ and $A\mathbf{x} = [1 + 4 - 8, -2 + 4, 3 + 8 - 8] = [-3, 2, 3] = \mathbf{b}$.

### FB 10.2.7
Question: [[LA1 HW 4.1 10.2 Questions#FB 10.2.7|FB 10.2.7]]

> [!solution] Solution
> $$
> L = \begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ -1 & -2 & 1 & 0 \\ 2 & 1 & -1 & 1 \end{bmatrix}, \quad U = \begin{bmatrix} 1 & 0 & 0 & 1 \\ 0 & -1 & 2 & 1 \\ 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 3 \end{bmatrix}
> $$
> $$
> \begin{aligned}
> &(1)\ L\mathbf{y} = \mathbf{b}:\ \begin{cases} y_1 = 4 \\ y_2 = 7 \\ -y_1 - 2y_2 + y_3 = -8 \\ 2y_1 + y_2 - y_3 + y_4 = 14 \end{cases} \implies \begin{aligned} &y_1 = 4,\ y_2 = 7, \\ &y_3 = -8 + 4 + 14 = 10, \\ &y_4 = 14 - 8 - 7 + 10 = 9 \end{aligned} \\[6pt]
> &(2)\ U\mathbf{x} = \mathbf{y}:\ \begin{cases} x_1 + x_4 = 4 \\ -x_2 + 2x_3 + x_4 = 7 \\ x_3 + 3x_4 = 10 \\ 3x_4 = 9 \end{cases} \implies \begin{aligned} &x_4 = 3,\ x_3 = 10 - 9 = 1, \\ &x_2 = 2x_3 + x_4 - 7 = -2, \\ &x_1 = 4 - x_4 = 1 \end{aligned} \\[6pt]
> &\text{Hence } \mathbf{x} = \begin{bmatrix} 1 \\ -2 \\ 1 \\ 3 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# Check: $A = LU = \begin{bmatrix} 1 & 0 & 0 & 1 \\ 0 & -1 & 2 & 1 \\ -1 & 2 & -3 & 0 \\ 2 & -1 & 1 & 3 \end{bmatrix}$ and $A\mathbf{x} = [1 + 3, 2 + 2 + 3, -1 - 4 - 3, 2 + 2 + 1 + 9] = [4, 7, -8, 14] = \mathbf{b}$. Each step of (1) and (2) uses only values already found, so no row reduction is needed once $L$ and $U$ are known.

## Exam Problems from Other Universities

> [!note] Note
> These problems are not assigned. They come from exams of other universities and add what the assigned exercises leave out.
> - WEB 4.1.1 and 4.1.3: true-or-false items in the format of the quizzes, on the cross product and the volume of a box. They come from a calculus course (Harvard's Math 21a), whose first exam covers the same vectors and cross products as FB §4.1.
> - WEB 4.1.2: the area of a triangle in $\mathbb{R}^3$, where no $2 \times 2$ determinant applies and the cross product is needed.
> - WEB 10.2.1: an LU-factorization found from the matrix itself and then used to solve a system, as in FB 10.2 Exercises 8–13.
> - WEB 10.2.2: the LDU form, which takes the pivots out of $U$ into a diagonal matrix $D$.
> - WEB 10.2.3: an invertible matrix without an LDU decomposition, and why the LDU decomposition of an invertible symmetric matrix has $L = U^T$.

### WEB 4.1.1
Question: [[LA1 HW 4.1 10.2 Questions#WEB 4.1.1|WEB 4.1.1]]

> [!solution] Solution
> - 3) **T.** $\langle 2, 4, 6 \rangle = 2\langle 1, 2, 3 \rangle$, and $\mathbf{a} \times (2\mathbf{a}) = 2(\mathbf{a} \times \mathbf{a}) = \mathbf{0}$.
> - 7) **F.** $\mathbf{i} \cdot \mathbf{j} = 0$, so $\mathbf{i} \perp \mathbf{j}$, but $\mathbf{i} \times \mathbf{j} = \mathbf{k} \ne \mathbf{0}$.
> - 11) **T.** $\begin{vmatrix} 1 & 1 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 2 \end{vmatrix} = 1(0 - 0) - 1(2 - 0) + 1(1 - 0) = -1$, so the volume is $\lvert -1 \rvert = 1$.
>
> \# 3) Parallel vectors have cross product $\mathbf{0}$, since $\sin\theta = 0$. 7) It is the other way around: orthogonal vectors have dot product $0$, and their cross product has the largest possible length, $\lVert \mathbf{v} \rVert \lVert \mathbf{w} \rVert$. 11) The determinant may be negative; the volume is its absolute value.

### WEB 4.1.2
Question: [[LA1 HW 4.1 10.2 Questions#WEB 4.1.2|WEB 4.1.2]]

> [!solution] Solution
> **a)**
> $$
> \begin{aligned}
> &y = z = 0 \implies x = 6, \qquad x = z = 0 \implies 3y = 6,\ y = 2, \qquad x = y = 0 \implies 2z = 6,\ z = 3 \\
> &A = (6, 0, 0),\ B = (0, 2, 0),\ C = (0, 0, 3).
> \end{aligned}
> $$
> **b)**
> $$
> \begin{aligned}
> &B - A = [-6, 2, 0],\ C - A = [-6, 0, 3] \\
> &(B - A) \times (C - A) = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ -6 & 2 & 0 \\ -6 & 0 & 3 \end{vmatrix} = (6 - 0)\mathbf{i} - (-18 - 0)\mathbf{j} + (0 + 12)\mathbf{k} = [6, 18, 12] \\
> &\text{Area} = \tfrac{1}{2}\lVert [6, 18, 12] \rVert = \tfrac{1}{2} \cdot 6\lVert [1, 3, 2] \rVert = 3\sqrt{14}.
> \end{aligned}
> $$
>
> \# a) Each vertex lies on a coordinate axis, where the other two coordinates are $0$. b) $[6, 18, 12] = 6[1, 3, 2]$ is a multiple of the normal vector $[1, 3, 2]$ of the plane, as it must be: it is perpendicular to two vectors that lie in the plane.

### WEB 4.1.3
Question: [[LA1 HW 4.1 10.2 Questions#WEB 4.1.3|WEB 4.1.3]]

> [!solution] Solution
> **2) F.** For unit vectors, $\lVert \mathbf{v} \times \mathbf{w} \rVert = \lVert \mathbf{v} \rVert \lVert \mathbf{w} \rVert \sin\theta = \sin\theta \le 1 < 2$.
>
> **11) T.** Let $\theta$ be the angle between $\mathbf{v}$ and $\mathbf{w}$. For unit vectors,
> $$
> \text{volume} = \lvert \mathbf{u} \cdot (\mathbf{v} \times \mathbf{w}) \rvert \le \lVert \mathbf{u} \rVert \lVert \mathbf{v} \times \mathbf{w} \rVert = \sin\theta \le 1,
> $$
> with equality $\iff$ $\mathbf{v} \perp \mathbf{w}$ and $\mathbf{u} \parallel \mathbf{v} \times \mathbf{w}$ $\iff$ $\mathbf{u}$, $\mathbf{v}$, $\mathbf{w}$ are mutually perpendicular $\iff$ the box is a cube (of volume $1$).
>
> **16) T.** $\mathbf{i} \times \mathbf{j} = \mathbf{k}$, $\mathbf{i} \times \mathbf{k} = -\mathbf{j}$, $\mathbf{i} \times (-\mathbf{j}) = -\mathbf{k}$, so $\mathbf{i} \times (\mathbf{i} \times (\mathbf{i} \times \mathbf{j})) = -\mathbf{k} = -(\mathbf{i} \times \mathbf{j})$, a scalar multiple of $\mathbf{i} \times \mathbf{j}$.
>
> \# 11) The first $\le$ is the Schwarz inequality $\lvert \mathbf{a} \cdot \mathbf{b} \rvert \le \lVert \mathbf{a} \rVert \lVert \mathbf{b} \rVert$ of §1.2, with equality only when $\mathbf{a}$ and $\mathbf{b}$ are parallel. 16) Around the cycle $\mathbf{i} \to \mathbf{j} \to \mathbf{k} \to \mathbf{i}$, two neighbors in this order give the third ($\mathbf{k} \times \mathbf{i} = \mathbf{j}$), and in the opposite order minus the third ($\mathbf{i} \times \mathbf{k} = -\mathbf{j}$).

### WEB 10.2.1
Question: [[LA1 HW 4.1 10.2 Questions#WEB 10.2.1|WEB 10.2.1]]

> [!solution] Solution
> **(a)**
> $$
> A = \begin{bmatrix} 1 & 1 & 1 \\ 1 & 2 & 3 \\ 1 & 3 & 6 \end{bmatrix} \overset{\substack{R_2 \to R_2 - 1R_1 \\ R_3 \to R_3 - 1R_1}}{\sim} \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 2 \\ 0 & 2 & 5 \end{bmatrix} \overset{R_3 \to R_3 - 2R_2}{\sim} \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 2 \\ 0 & 0 & 1 \end{bmatrix} = U
> $$
> $$
> \text{multipliers } l_{21} = 1,\ l_{31} = 1,\ l_{32} = 2 \implies L = \begin{bmatrix} 1 & 0 & 0 \\ 1 & 1 & 0 \\ 1 & 2 & 1 \end{bmatrix}, \quad A = LU.
> $$
> **(b)**
> $$
> \begin{aligned}
> &(1)\ Ly = b:\ y_1 = 1,\ y_2 = 0 - y_1 = -1,\ y_3 = 0 - y_1 - 2y_2 = 1 \\
> &(2)\ Ux = y:\ x_3 = 1,\ x_2 = -1 - 2x_3 = -3,\ x_1 = 1 - x_2 - x_3 = 3 \\
> &\text{Hence } x = \begin{bmatrix} 3 \\ -3 \\ 1 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# Check: $Ax = [3 - 3 + 1, 3 - 6 + 3, 3 - 9 + 6] = [1, 0, 0] = b$. Since $b$ is column 1 of $I$, this $x$ is column 1 of $A^{-1}$. Here $U = L^T$: $A$ is symmetric, and its LDU decomposition has $U = L^T$ by WEB 10.2.3 (j), with $D = I$.

### WEB 10.2.2
Question: [[LA1 HW 4.1 10.2 Questions#WEB 10.2.2|WEB 10.2.2]]

> [!solution] Solution
> **(a)**
> $$
> \begin{aligned}
> A = \begin{bmatrix} 2 & 2 & 2 \\ 4 & 3 & 1 \\ -2 & -1 & 4 \end{bmatrix} &\overset{\substack{R_2 \to R_2 - 2R_1 \\ R_3 \to R_3 + R_1}}{\sim} \begin{bmatrix} 2 & 2 & 2 \\ 0 & -1 & -3 \\ 0 & 1 & 6 \end{bmatrix} \overset{R_3 \to R_3 + R_2}{\sim} \begin{bmatrix} 2 & 2 & 2 \\ 0 & -1 & -3 \\ 0 & 0 & 3 \end{bmatrix} = U_0 \\
> l_{21} = 2,\ l_{31} = -1,\ l_{32} = -1 &\implies L = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ -1 & -1 & 1 \end{bmatrix}, \quad A = LU_0
> \end{aligned}
> $$
> Divide each row of $U_0$ by its pivot:
> $$
> U_0 = \underbrace{\begin{bmatrix} 2 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 3 \end{bmatrix}}_{D}\underbrace{\begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 3 \\ 0 & 0 & 1 \end{bmatrix}}_{U} \implies A = LDU.
> $$
> **(b)**
> $$
> \begin{aligned}
> &(1)\ Lc = b:\ c_1 = 2,\ c_2 = -3 - 2c_1 = -7,\ c_3 = 11 + c_1 + c_2 = 6 \\
> &(2)\ U_0x = c:\ 3x_3 = 6 \implies x_3 = 2;\ \ {-x_2} - 3x_3 = -7 \implies x_2 = 1;\ \ 2x_1 + 2x_2 + 2x_3 = 2 \implies x_1 = -2 \\
> &\text{Three pivots} \implies \text{exactly one solution: } x = \begin{bmatrix} -2 \\ 1 \\ 2 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# $R_3 \to R_3 + R_1$ is $R_3 \to R_3 - (-1)R_1$, so $l_{31} = -1$: the entry of $L$ is the number that is subtracted. Row 2 of $U$ is $[0, -1, -3]$ divided by $-1$. Check: $Ax = [-4 + 2 + 4, -8 + 3 + 2, 4 - 1 + 8] = [2, -3, 11] = b$. "All solutions" turns out to be one solution, because $A$ is invertible.

### WEB 10.2.3
Question: [[LA1 HW 4.1 10.2 Questions#WEB 10.2.3|WEB 10.2.3]]

> [!solution] Solution
> **(h) F.**
> $$
> \begin{aligned}
> &A = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix} \text{ is invertible } (A^2 = I). \text{ Suppose } A = LDU: \\
> &\begin{bmatrix} 1 & 0 \\ l & 1 \end{bmatrix}\begin{bmatrix} d_1 & 0 \\ 0 & d_2 \end{bmatrix}\begin{bmatrix} 1 & u \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} d_1 & d_1u \\ ld_1 & ld_1u + d_2 \end{bmatrix} = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix} \\
> &(1, 1)\text{-entry: } d_1 = 0 \implies (1, 2)\text{-entry: } d_1u = 0 \ne 1, \text{ a contradiction.} \\
> &\text{Hence this invertible } A \text{ has no LDU decomposition.}
> \end{aligned}
> $$
> **(j) F as stated; T when $A$ is invertible.**
>
> Counterexample: $A = O$ ($2 \times 2$) satisfies $A = A^T$, and $A = LDU$ with $L = \begin{bmatrix} 1 & 0 \\ 1 & 1 \end{bmatrix}$, $D = O$, $U = I$, but $L \ne I = U^T$.
>
> Proof when $A$ is invertible:
> $$
> \begin{aligned}
> &A \text{ invertible} \implies D = L^{-1}AU^{-1} \text{ is invertible.} \\
> &A = A^T = (LDU)^T = U^TD^TL^T = U^TDL^T \quad (D^T = D) \\
> &\implies LDU = U^TDL^T \\
> &\implies (U^T)^{-1}L = DL^TU^{-1}D^{-1} \\
> &\text{LHS: lower triangular with diagonal entries } 1; \quad \text{RHS: upper triangular} \\
> &\implies \text{both sides are diagonal with diagonal entries } 1, \text{ that is, } I \\
> &\implies (U^T)^{-1}L = I \implies L = U^T. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# (h) This $A$ only swaps two rows; FB handles it with a permutation matrix $P$: $PA = LU$, here with $P = A$ and $PA = I$. (j) The fourth line comes from multiplying $LDU = U^TDL^T$ on the left by $(U^T)^{-1}$, and on the right by $U^{-1}$ and then $D^{-1}$. It uses that products and inverses of lower triangular matrices with diagonal entries $1$ are again of that kind, and the same for upper triangular ones; $U^T$ is lower triangular and $L^T$ upper triangular, both with diagonal entries $1$. A matrix that is lower and upper triangular at once is diagonal. No answer key is posted; if the course requires $D$ to be invertible in an LDU decomposition, then $A$ is invertible and the answer is T.
