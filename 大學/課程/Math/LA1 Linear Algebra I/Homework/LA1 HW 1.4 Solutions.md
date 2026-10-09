---
course: [LA1]
chapter: ["1.4"]
tags: [linear-algebra, homework, solutions, linear-systems]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-10-09
questions: "[[LA1 HW 1.4 Questions]]"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.4 Questions#FB 1.4.5\|FB 1.4.5]] | (a) $\begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 0 & 0 & 2 & 6 & 8 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & -8 \end{bmatrix}$; (b) $\begin{bmatrix} 1 & -3 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix}$ |
| [[LA1 HW 1.4 Questions#FB 1.4.9\|FB 1.4.9]] | $\mathbf{x} = [1 - 2r,\ -2 - r - 3s,\ r,\ s]$; particular solution $[-5, 1, 3, -2]$ |
| [[LA1 HW 1.4 Questions#FB 1.4.13\|FB 1.4.13]] | $x = 2$, $y = -4$ |
| [[LA1 HW 1.4 Questions#FB 1.4.18\|FB 1.4.18]] | $\mathbf{x} = [-1 + 2r,\ -1 + r,\ r]$ |
| [[LA1 HW 1.4 Questions#FB 1.4.21\|FB 1.4.21]] | $x_1 = -2$, $x_2 = 1$ |
| [[LA1 HW 1.4 Questions#FB 1.4.25\|FB 1.4.25]] | Yes: $\mathbf{b} = 2\mathbf{v}_1 - \mathbf{v}_3$ |
| [[LA1 HW 1.4 Questions#FB 1.4.27\|FB 1.4.27]] | No |
| [[LA1 HW 1.4 Questions#FB 1.4.29\|FB 1.4.29]] | a. F; b. F; c. T; d. T; e. F; f. T; g. T; h. T; i. F; j. T |
| [[LA1 HW 1.4 Questions#FB 1.4.35\|FB 1.4.35]] | $x_1 = 1$, $x_2 = -1$, $x_3 = 1$, $x_4 = 2$ |
| [[LA1 HW 1.4 Questions#FB 1.4.38\|FB 1.4.38]] | $b_2 = 3b_1$ |
| [[LA1 HW 1.4 Questions#FB 1.4.40\|FB 1.4.40]] | All $b_1, b_2, b_3 \in \mathbb{R}$ |

Additional exercises, not assigned:

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.4 Questions#FB 1.4.19\|FB 1.4.19]] | No solution |
| [[LA1 HW 1.4 Questions#FB 1.4.23\|FB 1.4.23]] | $\mathbf{x} = \left[-8,\ -23 - \tfrac{5}{2}t,\ -7 + \tfrac{1}{2}t,\ t\right]$ |
| [[LA1 HW 1.4 Questions#FB 1.4.36\|FB 1.4.36]] | $x_1 = -1$, $x_2 = 3$ |
| [[LA1 HW 1.4 Questions#FB 1.4.37\|FB 1.4.37]] | $x_1 = -3$, $x_2 = 5$, $x_3 = 2$, $x_4 = -3$ |
| [[LA1 HW 1.4 Questions#FB 1.4.41\|FB 1.4.41]] | $b_1 = b_2 + b_3$ |
| [[LA1 HW 1.4 Questions#FB 1.4.56\|FB 1.4.56]] | $a = 3$, $b = -2$, $c = -5$ |
| [[LA1 HW 1.4 Questions#FB 1.4.57\|FB 1.4.57]] | $a = \tfrac{1}{2} + \tfrac{1}{4}t$, $b = -2$, $c = \tfrac{7}{2} - \tfrac{5}{4}t$, $d = t$ for any $t \in \mathbb{R}$ |

## FB §1.4 Solving Systems of Linear Equations

> [!note] Note
> The notation and the facts that the answers use.
> - **[[Elementary Row Operation|Row operations]]**: $R_i \leftrightarrow R_j$, $R_i \to sR_i$ with $s \ne 0$, $R_i \to R_i + sR_j$. The operation is written over $\sim$. Row operations on the [[Augmented Matrix|augmented matrix]] do not change the solution set.
> - **[[Gaussian Elimination|Gauss method]]**: reduce $[A \mid \mathbf{b}]$ to [[Row-Echelon Form|row-echelon form]], then solve from the last equation up (back substitution). **Gauss–Jordan method**: reduce to [[Reduced Row-Echelon Form|reduced row-echelon form]] and read off the solution.
> - **Consistent** $\iff$ no row $[0 \cdots 0 \mid c]$ with $c \ne 0$.
> - **Free variables**: the variables of the columns without a pivot. A consistent system has a unique solution if every column has a pivot, and infinitely many solutions otherwise.
> - **[[Span]]**: $\mathbf{b} \in \operatorname{sp}(\mathbf{v}_1, \dots, \mathbf{v}_k) \iff x_1\mathbf{v}_1 + \cdots + x_k\mathbf{v}_k = \mathbf{b}$ is consistent $\iff [\mathbf{v}_1 \cdots \mathbf{v}_k \mid \mathbf{b}]$ has no row $[0 \cdots 0 \mid c]$, $c \ne 0$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FB 1.4.5
Question: [[LA1 HW 1.4 Questions#FB 1.4.5|FB 1.4.5]]

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

### FB 1.4.9
Question: [[LA1 HW 1.4 Questions#FB 1.4.9|FB 1.4.9]]

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

### FB 1.4.13
Question: [[LA1 HW 1.4 Questions#FB 1.4.13|FB 1.4.13]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{cc|c} 2 & -1 & 8 \\ 6 & -5 & 32 \end{array}\right] \overset{R_2 \to R_2 - 3R_1}{\sim} \left[\begin{array}{cc|c} 2 & -1 & 8 \\ 0 & -2 & 8 \end{array}\right]
> \end{aligned}
> $$
> Back substitution:
> $$
> \begin{aligned}
> &-2y = 8 \implies y = -4 \\
> &2x - y = 8 \implies 2x = 8 + (-4) = 4 \implies x = 2
> \end{aligned}
> $$
> Hence $x = 2$, $y = -4$.
>
> \# Check in the second equation: $6(2) - 5(-4) = 12 + 20 = 32$.

### FB 1.4.18
Question: [[LA1 HW 1.4 Questions#FB 1.4.18|FB 1.4.18]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 1 & -3 & 1 & 2 \\ 3 & -8 & 2 & 5 \end{array}\right] \overset{R_2 \to R_2 - 3R_1}{\sim} \left[\begin{array}{ccc|c} 1 & -3 & 1 & 2 \\ 0 & 1 & -1 & -1 \end{array}\right]
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\text{Pivots: columns 1, 2} \implies x_3 \text{ is free. Let } x_3 = r. \\
> &x_2 - x_3 = -1 \implies x_2 = -1 + r \\
> &x_1 - 3x_2 + x_3 = 2 \implies x_1 = 2 + 3(-1 + r) - r = -1 + 2r \\
> &\mathbf{x} = \begin{bmatrix} -1 + 2r \\ -1 + r \\ r \end{bmatrix} \quad \text{for any } r \in \mathbb{R}
> \end{aligned}
> $$
>
> \# Two equations and three unknowns, and the system is consistent, so one variable is free. Check with $r = 0$: $\mathbf{x} = [-1, -1, 0]$ gives $-1 + 3 = 2$ and $-3 + 8 = 5$.

### FB 1.4.21
Question: [[LA1 HW 1.4 Questions#FB 1.4.21|FB 1.4.21]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{cc|c} 3 & -2 & -8 \\ 4 & 5 & -3 \end{array}\right] \overset{R_2 \to R_2 - R_1}{\sim} \left[\begin{array}{cc|c} 3 & -2 & -8 \\ 1 & 7 & 5 \end{array}\right] \overset{R_1 \leftrightarrow R_2}{\sim} \left[\begin{array}{cc|c} 1 & 7 & 5 \\ 3 & -2 & -8 \end{array}\right] \\[6pt]
> & \overset{R_2 \to R_2 - 3R_1}{\sim} \left[\begin{array}{cc|c} 1 & 7 & 5 \\ 0 & -23 & -23 \end{array}\right] \overset{R_2 \to -\tfrac{1}{23}R_2}{\sim} \left[\begin{array}{cc|c} 1 & 7 & 5 \\ 0 & 1 & 1 \end{array}\right] \overset{R_1 \to R_1 - 7R_2}{\sim} \left[\begin{array}{cc|c} 1 & 0 & -2 \\ 0 & 1 & 1 \end{array}\right]
> \end{aligned}
> $$
> Hence $x_1 = -2$, $x_2 = 1$.
>
> \# The first step $R_2 \to R_2 - R_1$ makes a leading $1$ without fractions. Check: $3(-2) - 2(1) = -8$ and $4(-2) + 5(1) = -3$.

### FB 1.4.25
Question: [[LA1 HW 1.4 Questions#FB 1.4.25|FB 1.4.25]]

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

### FB 1.4.27
Question: [[LA1 HW 1.4 Questions#FB 1.4.27|FB 1.4.27]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\mathbf{b} \in \operatorname{sp}(\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3, \mathbf{v}_4) \iff x_1\mathbf{v}_1 + x_2\mathbf{v}_2 + x_3\mathbf{v}_3 + x_4\mathbf{v}_4 = \mathbf{b} \text{ is consistent.} \\[4pt]
> &\left[\begin{array}{cccc|c} 1 & 2 & -3 & 0 & 8 \\ 2 & 5 & -6 & 0 & 17 \\ -1 & -2 & 1 & -1 & -8 \\ 0 & 5 & -8 & -4 & 3 \end{array}\right] \overset{\substack{R_2 \to R_2 - 2R_1 \\ R_3 \to R_3 + R_1}}{\sim} \left[\begin{array}{cccc|c} 1 & 2 & -3 & 0 & 8 \\ 0 & 1 & 0 & 0 & 1 \\ 0 & 0 & -2 & -1 & 0 \\ 0 & 5 & -8 & -4 & 3 \end{array}\right] \\[6pt]
> & \overset{R_4 \to R_4 - 5R_2}{\sim} \left[\begin{array}{cccc|c} 1 & 2 & -3 & 0 & 8 \\ 0 & 1 & 0 & 0 & 1 \\ 0 & 0 & -2 & -1 & 0 \\ 0 & 0 & -8 & -4 & -2 \end{array}\right] \overset{R_4 \to R_4 - 4R_3}{\sim} \left[\begin{array}{cccc|c} 1 & 2 & -3 & 0 & 8 \\ 0 & 1 & 0 & 0 & 1 \\ 0 & 0 & -2 & -1 & 0 \\ 0 & 0 & 0 & 0 & -2 \end{array}\right]
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\text{Row 4 is } [0\ 0\ 0\ 0 \mid -2] \implies 0 = -2, \text{ so the system is inconsistent.} \\
> &\text{Hence } \mathbf{b} \text{ is not in the span.}
> \end{aligned}
> $$
>
> \# Compare [[LA1 HW 1.4 Questions#FB 1.4.25|FB 1.4.25]], where the answer is Yes. Here the coefficient part already has a zero row ($\mathbf{v}_4 = \tfrac{1}{2}\mathbf{v}_3 + \tfrac{3}{2}\mathbf{v}_1$), so the span is smaller than $\mathbb{R}^4$ and misses $\mathbf{b}$.

### FB 1.4.29
Question: [[LA1 HW 1.4 Questions#FB 1.4.29|FB 1.4.29]]

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

### FB 1.4.35
Question: [[LA1 HW 1.4 Questions#FB 1.4.35|FB 1.4.35]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\begin{bmatrix} x_1 & x_2 \\ x_3 & x_4 \end{bmatrix} \begin{bmatrix} 1 & 1 \\ 1 & 0 \end{bmatrix} = \begin{bmatrix} x_1 + x_2 & x_1 \\ x_3 + x_4 & x_3 \end{bmatrix} = \begin{bmatrix} 0 & 1 \\ 3 & 1 \end{bmatrix} \\[4pt]
> &\text{Compare entries:} \\
> &(1, 2):\ x_1 = 1, \qquad (1, 1):\ x_1 + x_2 = 0 \implies x_2 = -1 \\
> &(2, 2):\ x_3 = 1, \qquad (2, 1):\ x_3 + x_4 = 3 \implies x_4 = 2 \\
> &\text{Hence } x_1 = 1,\ x_2 = -1,\ x_3 = 1,\ x_4 = 2.
> \end{aligned}
> $$
>
> \# Two matrices are equal when all their entries are equal, so one matrix equation gives four linear equations. Here they separate into two systems: row 1 has only $x_1$, $x_2$, and row 2 only $x_3$, $x_4$.

### FB 1.4.38
Question: [[LA1 HW 1.4 Questions#FB 1.4.38|FB 1.4.38]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{cc|c} 1 & 2 & b_1 \\ 3 & 6 & b_2 \end{array}\right] \overset{R_2 \to R_2 - 3R_1}{\sim} \left[\begin{array}{cc|c} 1 & 2 & b_1 \\ 0 & 0 & b_2 - 3b_1 \end{array}\right] \\[4pt]
> &\text{Consistent} \iff \text{row 2 is not } [0\ 0 \mid c],\ c \ne 0 \iff b_2 - 3b_1 = 0. \\
> &\text{Hence the system is consistent exactly when } b_2 = 3b_1.
> \end{aligned}
> $$
>
> \# The left side of equation 2 is $3$ times the left side of equation 1, so the right sides must keep the same ratio. When $b_2 = 3b_1$ there are infinitely many solutions, because $x_2$ is free. Compare [[LA1 HW 1.4 Questions#FB 1.4.40|FB 1.4.40]], where no row of the coefficient part becomes zero.

### FB 1.4.40
Question: [[LA1 HW 1.4 Questions#FB 1.4.40|FB 1.4.40]]

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

## FB §1.4 Additional Exercises

> [!note] Note
> These exercises are not assigned. Each one adds a type of problem that the assigned exercises do not cover.
> - 19: the Gauss method on a system with no solution (13 has one solution, 18 infinitely many).
> - 23: the Gauss–Jordan method with a free variable (21 has one solution).
> - 36: a row vector times a matrix: more equations than unknowns, and still one solution.
> - 37: a matrix equation whose answer is an inverse, which leads to §1.5.
> - 41: a span question in $\mathbb{R}^3$ with a condition on $\mathbf{b}$ (38 and 40 are the same idea for a system).
> - 56, 57: fitting a curve through points; 57 has infinitely many answers.
>
> The other types of §1.4, elementary matrices (42–51) and proofs (52–55, 58), are solved in [[LA1 HW 1.4 1.5 Solutions]].

### FB 1.4.19
Question: [[LA1 HW 1.4 Questions#FB 1.4.19|FB 1.4.19]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 1 & 4 & -2 & 4 \\ 2 & 7 & -1 & -2 \\ 2 & 9 & -7 & 1 \end{array}\right] \overset{\substack{R_2 \to R_2 - 2R_1 \\ R_3 \to R_3 - 2R_1}}{\sim} \left[\begin{array}{ccc|c} 1 & 4 & -2 & 4 \\ 0 & -1 & 3 & -10 \\ 0 & 1 & -3 & -7 \end{array}\right] \overset{R_3 \to R_3 + R_2}{\sim} \left[\begin{array}{ccc|c} 1 & 4 & -2 & 4 \\ 0 & -1 & 3 & -10 \\ 0 & 0 & 0 & -17 \end{array}\right]
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\text{Row 3 is } [0\ 0\ 0 \mid -17] \implies 0 = -17. \\
> &\text{Hence the system is inconsistent: it has no solution.}
> \end{aligned}
> $$
>
> \# Stop as soon as a row $[0 \cdots 0 \mid c]$ with $c \ne 0$ appears; there is nothing to back-substitute.

### FB 1.4.23
Question: [[LA1 HW 1.4 Questions#FB 1.4.23|FB 1.4.23]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\left[\begin{array}{cccc|c} 1 & 0 & -2 & 1 & 6 \\ 2 & -1 & 1 & -3 & 0 \\ 9 & -3 & -1 & -7 & 4 \end{array}\right] \overset{\substack{R_2 \to R_2 - 2R_1 \\ R_3 \to R_3 - 9R_1}}{\sim} \left[\begin{array}{cccc|c} 1 & 0 & -2 & 1 & 6 \\ 0 & -1 & 5 & -5 & -12 \\ 0 & -3 & 17 & -16 & -50 \end{array}\right] \\[6pt]
> & \overset{R_3 \to R_3 - 3R_2}{\sim} \left[\begin{array}{cccc|c} 1 & 0 & -2 & 1 & 6 \\ 0 & -1 & 5 & -5 & -12 \\ 0 & 0 & 2 & -1 & -14 \end{array}\right] \overset{\substack{R_2 \to -R_2 \\ R_3 \to \tfrac{1}{2}R_3}}{\sim} \left[\begin{array}{cccc|c} 1 & 0 & -2 & 1 & 6 \\ 0 & 1 & -5 & 5 & 12 \\ 0 & 0 & 1 & -\tfrac{1}{2} & -7 \end{array}\right] \\[6pt]
> & \overset{\substack{R_1 \to R_1 + 2R_3 \\ R_2 \to R_2 + 5R_3}}{\sim} \left[\begin{array}{cccc|c} 1 & 0 & 0 & 0 & -8 \\ 0 & 1 & 0 & \tfrac{5}{2} & -23 \\ 0 & 0 & 1 & -\tfrac{1}{2} & -7 \end{array}\right]
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\text{Pivots: columns 1, 2, 3} \implies x_4 \text{ is free. Let } x_4 = t. \\
> &x_1 = -8, \qquad x_2 = -23 - \tfrac{5}{2}t, \qquad x_3 = -7 + \tfrac{1}{2}t \\
> &\mathbf{x} = \begin{bmatrix} -8 \\ -23 - \tfrac{5}{2}t \\ -7 + \tfrac{1}{2}t \\ t \end{bmatrix} \quad \text{for any } t \in \mathbb{R}
> \end{aligned}
> $$
>
> \# $x_1 = -8$ for every solution, because the column of $x_4$ has a $0$ in row 1. Check with $t = 0$: $[-8, -23, -7, 0]$ gives $-8 + 14 = 6$, $-16 + 23 - 7 = 0$ and $-72 + 69 + 7 = 4$.

### FB 1.4.36
Question: [[LA1 HW 1.4 Questions#FB 1.4.36|FB 1.4.36]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\begin{bmatrix} x_1 & x_2 \end{bmatrix} \begin{bmatrix} 3 & 0 & 4 \\ 2 & 1 & -1 \end{bmatrix} = \begin{bmatrix} 3x_1 + 2x_2 & x_2 & 4x_1 - x_2 \end{bmatrix} = \begin{bmatrix} 3 & 3 & -7 \end{bmatrix} \\[4pt]
> &\text{Entry 2: } x_2 = 3 \\
> &\text{Entry 1: } 3x_1 + 2(3) = 3 \implies x_1 = -1 \\
> &\text{Entry 3: } 4(-1) - 3 = -7 \quad \checkmark \\
> &\text{Hence } x_1 = -1,\ x_2 = 3.
> \end{aligned}
> $$
>
> \# Three equations and two unknowns: two of them fix $x_1$, $x_2$, and the third must be checked. If it failed, there would be no solution.

### FB 1.4.37
Question: [[LA1 HW 1.4 Questions#FB 1.4.37|FB 1.4.37]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\begin{bmatrix} x_1 & x_2 \\ x_3 & x_4 \end{bmatrix} \begin{bmatrix} 3 & 5 \\ 2 & 3 \end{bmatrix} = \begin{bmatrix} 3x_1 + 2x_2 & 5x_1 + 3x_2 \\ 3x_3 + 2x_4 & 5x_3 + 3x_4 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} \\[4pt]
> &\text{Row 1: } \begin{cases} 3x_1 + 2x_2 = 1 \\ 5x_1 + 3x_2 = 0 \end{cases} \implies x_2 = 5,\ x_1 = -3 \\
> &\text{Row 2: } \begin{cases} 3x_3 + 2x_4 = 0 \\ 5x_3 + 3x_4 = 1 \end{cases} \implies x_4 = -3,\ x_3 = 2 \\
> &\text{Hence } x_1 = -3,\ x_2 = 5,\ x_3 = 2,\ x_4 = -3.
> \end{aligned}
> $$
>
> \# Each system: $5 \cdot (\text{first}) - 3 \cdot (\text{second})$ removes $x_1$ (or $x_3$). The answer $X = \begin{bmatrix} -3 & 5 \\ 2 & -3 \end{bmatrix}$ satisfies $X\begin{bmatrix} 3 & 5 \\ 2 & 3 \end{bmatrix} = I$: it is the [[Invertible Matrix|inverse]] of that matrix, as in §1.5.

### FB 1.4.41
Question: [[LA1 HW 1.4 Questions#FB 1.4.41|FB 1.4.41]]

> [!solution] Solution
> $$
> \begin{aligned}
> &\mathbf{b} \in \operatorname{sp}(\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3) \iff [\mathbf{v}_1\ \mathbf{v}_2\ \mathbf{v}_3 \mid \mathbf{b}] \text{ is consistent} \quad (\text{vectors as columns}) \\[4pt]
> &\left[\begin{array}{ccc|c} 1 & 3 & -1 & b_1 \\ 1 & -1 & 2 & b_2 \\ 0 & 4 & -3 & b_3 \end{array}\right] \overset{R_2 \to R_2 - R_1}{\sim} \left[\begin{array}{ccc|c} 1 & 3 & -1 & b_1 \\ 0 & -4 & 3 & b_2 - b_1 \\ 0 & 4 & -3 & b_3 \end{array}\right] \\[6pt]
> &\overset{R_3 \to R_3 + R_2}{\sim} \left[\begin{array}{ccc|c} 1 & 3 & -1 & b_1 \\ 0 & -4 & 3 & b_2 - b_1 \\ 0 & 0 & 0 & b_3 + b_2 - b_1 \end{array}\right] \\[4pt]
> &\text{Consistent} \iff b_3 + b_2 - b_1 = 0. \\
> &\text{Hence } \mathbf{b} \text{ is in the span exactly when } b_1 = b_2 + b_3.
> \end{aligned}
> $$
>
> \# The span is a plane in $\mathbb{R}^3$, not all of $\mathbb{R}^3$, because $\mathbf{v}_3$ is a combination of $\mathbf{v}_1$ and $\mathbf{v}_2$. Check: $\mathbf{v}_1$, $\mathbf{v}_2$, $\mathbf{v}_3$ each satisfy $b_1 = b_2 + b_3$.

### FB 1.4.56
Question: [[LA1 HW 1.4 Questions#FB 1.4.56|FB 1.4.56]]

> [!solution] Solution
> $$
> \begin{aligned}
> &(1, -4):\ a + b + c = -4, \qquad (-1, 0):\ a - b + c = 0, \qquad (2, 3):\ 4a + 2b + c = 3 \\[4pt]
> &\left[\begin{array}{ccc|c} 1 & 1 & 1 & -4 \\ 1 & -1 & 1 & 0 \\ 4 & 2 & 1 & 3 \end{array}\right] \overset{\substack{R_2 \to R_2 - R_1 \\ R_3 \to R_3 - 4R_1}}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & 1 & -4 \\ 0 & -2 & 0 & 4 \\ 0 & -2 & -3 & 19 \end{array}\right] \\[6pt]
> & \overset{R_3 \to R_3 - R_2}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & 1 & -4 \\ 0 & -2 & 0 & 4 \\ 0 & 0 & -3 & 15 \end{array}\right]
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &-3c = 15 \implies c = -5 \\
> &-2b = 4 \implies b = -2 \\
> &a + b + c = -4 \implies a = -4 + 2 + 5 = 3 \\
> &\text{Hence } y = 3x^2 - 2x - 5.
> \end{aligned}
> $$
>
> \# Each point gives one linear equation in the unknowns $a$, $b$, $c$. Check $(2, 3)$: $12 - 4 - 5 = 3$.

### FB 1.4.57
Question: [[LA1 HW 1.4 Questions#FB 1.4.57|FB 1.4.57]]

> [!solution] Solution
> $$
> \begin{aligned}
> &(1, 2):\ a + b + c + d = 2, \qquad (-1, 6):\ a - b + c + d = 6 \\
> &(-2, 38):\ 16a - 8b + 4c + d = 38, \qquad (2, 6):\ 16a + 8b + 4c + d = 6 \\[4pt]
> &\left[\begin{array}{cccc|c} 1 & 1 & 1 & 1 & 2 \\ 1 & -1 & 1 & 1 & 6 \\ 16 & -8 & 4 & 1 & 38 \\ 16 & 8 & 4 & 1 & 6 \end{array}\right] \overset{\substack{R_2 \to R_2 - R_1 \\ R_3 \to R_3 - 16R_1 \\ R_4 \to R_4 - 16R_1}}{\sim} \left[\begin{array}{cccc|c} 1 & 1 & 1 & 1 & 2 \\ 0 & -2 & 0 & 0 & 4 \\ 0 & -24 & -12 & -15 & 6 \\ 0 & -8 & -12 & -15 & -26 \end{array}\right] \\[6pt]
> & \overset{\substack{R_3 \to R_3 - 12R_2 \\ R_4 \to R_4 - 4R_2}}{\sim} \left[\begin{array}{cccc|c} 1 & 1 & 1 & 1 & 2 \\ 0 & -2 & 0 & 0 & 4 \\ 0 & 0 & -12 & -15 & -42 \\ 0 & 0 & -12 & -15 & -42 \end{array}\right] \overset{R_4 \to R_4 - R_3}{\sim} \left[\begin{array}{cccc|c} 1 & 1 & 1 & 1 & 2 \\ 0 & -2 & 0 & 0 & 4 \\ 0 & 0 & -12 & -15 & -42 \\ 0 & 0 & 0 & 0 & 0 \end{array}\right]
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\text{Pivots: columns } a, b, c \implies d \text{ is free. Let } d = t. \\
> &-12c - 15t = -42 \implies c = \tfrac{7}{2} - \tfrac{5}{4}t \\
> &-2b = 4 \implies b = -2 \\
> &a + b + c + d = 2 \implies a = 2 + 2 - \left(\tfrac{7}{2} - \tfrac{5}{4}t\right) - t = \tfrac{1}{2} + \tfrac{1}{4}t \\
> &\text{Hence } a = \tfrac{1}{2} + \tfrac{1}{4}t,\ b = -2,\ c = \tfrac{7}{2} - \tfrac{5}{4}t,\ d = t \text{ for any } t \in \mathbb{R}.
> \end{aligned}
> $$
>
> \# Four points do not fix the curve here. The points come in pairs $x = \pm 1$, $x = \pm 2$, and the curve has no $x$ term, so $y(1) - y(-1) = 2b$ and $y(2) - y(-2) = 16b$: both differences give $b = -2$, and one of the four equations repeats. Example $t = 2$: $y = x^4 - 2x^3 + x^2 + 2$, which passes through all four points.
