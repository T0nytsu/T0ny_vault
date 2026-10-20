---
course: [LA1]
semester: "115-1"
chapter: ["1.4"]
tags: [linear-algebra, quiz, linear-systems]
source:
  - "LA1 Quiz #5 [1134] (115-1), graded scan"
  - "[[LA1 Quiz 05 p1.jpg]]"
created: 2026-10-20
score: "10/10"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!abstract] Result: 10/10
> - Q1 Reduced Row-Echelon Form: 5/5. The matrix of [[LA1 HW 1.4 Questions#FB 1.4.5|FB 1.4.5]] (b). One entry of an intermediate matrix is miscomputed, without changing the answer (not marked).
> - Q2 Gauss Method: 5/5. [[Gaussian Elimination|Gauss method]] with back substitution; one solution, $(x, y, z) = (-1, 2, 3)$. Worded as FB Exercises 1.4.13–20.

> [!note] Notation
> - In the attempts, as written beside the matrices: $\hookleftarrow{\times}s$ on a row means that $s$ times the pivot row of the step is added to that row, and a pair $\Lsh$ … $\hookleftarrow$ without a multiplier swaps those two rows. $\overset{r}{\sim}$ is row equivalence.
> - In the solutions, as in lecture: $r_{ij}$ swaps rows $i$ and $j$, $r_{i}^{s}$ multiplies row $i$ by $s \ne 0$, and $r_{ij}^{s}$ adds $s$ times row $i$ to row $j$; $R_{ij}$, $R_{i}^{s}$, $R_{ij}^{s}$ are the row-elementary matrices, and a superscript is the scalar, not a power. $\overset{R_{12}}{\sim}$ names the operation of a step.

## Q1 Reduced Row-Echelon Form

> [!question]
> (5 pts.) Reduce the matix to reduced row-echelon form, making all pivots 1.
> $$
> \begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 1 & -3 & 0 & 0 & -1 \\ 2 & -6 & 2 & 4 & 0 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix}
> $$

> [!attempt] My answer: 5/5
> $$
> \begin{aligned}
> &\begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 1 & -3 & 0 & 0 & -1 \\ 2 & -6 & 2 & 4 & 0 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix}\!\begin{array}{l} \Lsh \\ \hookleftarrow \\ \vphantom{0} \\ \vphantom{0} \end{array} \overset{r}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ -1 & 3 & 0 & 1 & 4 \\ 2 & -6 & 2 & 4 & 0 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix}\!\begin{array}{l} \vphantom{0} \\ \hookleftarrow{\times}1 \\ \hookleftarrow{\times}(-2) \\ \vphantom{0} \end{array} \overset{r}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 2 & 4 & 2 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix}\!\begin{array}{l} \vphantom{0} \\ \Lsh \\ \vphantom{0} \\ \hookleftarrow \end{array} \\[8pt]
> &\overset{r}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 1 & 3 & -4 \\ 0 & 0 & 2 & 4 & 2 \\ 0 & 0 & 0 & 1 & 3 \end{bmatrix}\!\begin{array}{l} \vphantom{0} \\ \vphantom{0} \\ \hookleftarrow{\times}(-2) \\ \vphantom{0} \end{array} \overset{r}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 1 & 3 & -4 \\ 0 & 0 & 0 & -2 & 2 \\ 0 & 0 & 0 & 1 & 3 \end{bmatrix}\!\begin{array}{l} \vphantom{0} \\ \vphantom{0} \\ \Lsh \\ \hookleftarrow \end{array} \overset{r}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 1 & 3 & -4 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & -2 & 2 \end{bmatrix}\!\begin{array}{l} \vphantom{0} \\ \hookleftarrow{\times}(-3) \\ \vphantom{0} \\ \hookleftarrow{\times}2 \end{array} \\[8pt]
> &\overset{r}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 1 & 0 & -13 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & 8 \end{bmatrix} \overset{R_{4}^{\frac{1}{8}}}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 1 & 0 & -13 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix}\!\begin{array}{l} \hookleftarrow{\times}1 \\ \hookleftarrow{\times}13 \\ \hookleftarrow{\times}(-3) \\ \vphantom{0} \end{array} \sim \begin{bmatrix} 1 & -3 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix}
> \end{aligned}
> $$

> [!failure] Mistake: one entry in the second line (not marked)
> In the second matrix of the second line, row 3 is
> $$
> \begin{bmatrix} 0 & 0 & 2 & 4 & 2 \end{bmatrix} - 2\begin{bmatrix} 0 & 0 & 1 & 3 & -4 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 0 & -2 & 10 \end{bmatrix},
> $$
> since $2 - 2(-4) = 10$, not $2$. The slip carries over to the last entry of the first matrix of the third line ($16$, not $8$). The final answer is still right, because that entry only has to be nonzero: it is scaled to the pivot $1$ and then clears its column. In a linear system, the same slip would change the solution.

> [!solution]- Solution
> $$
> \begin{aligned}
> A &\overset{R_{12}}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ -1 & 3 & 0 & 1 & 4 \\ 2 & -6 & 2 & 4 & 0 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix} \overset{\substack{R_{12}^{1} \\ R_{13}^{-2}}}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 2 & 4 & 2 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix} \\[8pt]
> &\overset{R_{24}}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 1 & 3 & -4 \\ 0 & 0 & 2 & 4 & 2 \\ 0 & 0 & 0 & 1 & 3 \end{bmatrix} \overset{R_{23}^{-2}}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 1 & 3 & -4 \\ 0 & 0 & 0 & -2 & 10 \\ 0 & 0 & 0 & 1 & 3 \end{bmatrix} \\[8pt]
> &\overset{R_{34}}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 1 & 3 & -4 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & -2 & 10 \end{bmatrix} \overset{\substack{R_{32}^{-3} \\ R_{34}^{2}}}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 1 & 0 & -13 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & 16 \end{bmatrix} \\[8pt]
> &\overset{R_{4}^{1/16}}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & -1 \\ 0 & 0 & 1 & 0 & -13 \\ 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix} \overset{\substack{R_{41}^{1} \\ R_{42}^{13} \\ R_{43}^{-3}}}{\sim} \begin{bmatrix} 1 & -3 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 1 \end{bmatrix}.
> \end{aligned}
> $$
>
> \# The pivots end up in columns 1, 3, 4, 5. Once the last row is $\begin{bmatrix} 0 & 0 & 0 & 0 & c \end{bmatrix}$ with $c \ne 0$, scaling makes $c = 1$, and that $1$ clears the last column; so the exact value of $c$ does not matter, only that $c \ne 0$. Column 2 has no pivot, and its entry $-3$ stays.

## Q2 Gauss Method

> [!question]
> (5 pts.) Find all solutions of the given linear system, using the Gauss method with back substitution.
> $$
> \left\{\begin{aligned} y + z &= 5 \\ 3x - y + z &= -2 \\ x + y - 3z &= -8 \end{aligned}\right.
> $$

> [!attempt] My answer: 5/5
> $$
> \begin{aligned}
> &\left[\begin{array}{ccc|c} 0 & 1 & 1 & 5 \\ 3 & -1 & 1 & -2 \\ 1 & 1 & -3 & -8 \end{array}\right]\!\begin{array}{l} \Lsh \\ \vphantom{0} \\ \hookleftarrow \end{array} \overset{r}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & -3 & -8 \\ 3 & -1 & 1 & -2 \\ 0 & 1 & 1 & 5 \end{array}\right]\!\begin{array}{l} \vphantom{0} \\ \hookleftarrow{\times}(-3) \\ \vphantom{0} \end{array} \overset{r}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & -3 & -8 \\ 0 & -4 & 10 & 22 \\ 0 & 1 & 1 & 5 \end{array}\right]\!\begin{array}{l} \vphantom{0} \\ \Lsh \\ \hookleftarrow \end{array} \\[8pt]
> &\overset{r}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & -3 & -8 \\ 0 & 1 & 1 & 5 \\ 0 & -4 & 10 & 22 \end{array}\right]\!\begin{array}{l} \vphantom{0} \\ \vphantom{0} \\ \hookleftarrow{\times}4 \end{array} \overset{r}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & -3 & -8 \\ 0 & 1 & 1 & 5 \\ 0 & 0 & 14 & 42 \end{array}\right]
> \end{aligned}
> $$
> $$
> \left\{\begin{aligned} x + y - 3z &= -8 \\ y + z &= 5 \\ 14z &= 42 \end{aligned}\right.
> $$
> $$
> \begin{aligned}
> &14z = 42 \implies z = 3 \\
> &y + z = y + 3 = 5 \implies y = 2 \\
> &x + y - 3z = x + 2 - 9 = -8 \implies x = -1
> \end{aligned}
> $$
> Hence $x = -1$, $y = 2$, $z = 3$ by using Gauss method with back substitution.

> [!solution]- Solution
> $$
> \begin{aligned}
> {[A \mid b]} = \left[\begin{array}{ccc|c} 0 & 1 & 1 & 5 \\ 3 & -1 & 1 & -2 \\ 1 & 1 & -3 & -8 \end{array}\right] &\overset{R_{13}}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & -3 & -8 \\ 3 & -1 & 1 & -2 \\ 0 & 1 & 1 & 5 \end{array}\right] \overset{R_{12}^{-3}}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & -3 & -8 \\ 0 & -4 & 10 & 22 \\ 0 & 1 & 1 & 5 \end{array}\right] \\[8pt]
> &\overset{R_{23}}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & -3 & -8 \\ 0 & 1 & 1 & 5 \\ 0 & -4 & 10 & 22 \end{array}\right] \overset{R_{23}^{4}}{\sim} \left[\begin{array}{ccc|c} 1 & 1 & -3 & -8 \\ 0 & 1 & 1 & 5 \\ 0 & 0 & 14 & 42 \end{array}\right].
> \end{aligned}
> $$
> Back substitution, from the last row up:
> $$
> \begin{aligned}
> 14z = 42 &\implies z = 3 \\
> y + z = 5 &\implies y = 5 - 3 = 2 \\
> x + y - 3z = -8 &\implies x = -8 - 2 + 9 = -1
> \end{aligned}
> $$
> $\therefore$ the system has exactly one solution, $(x, y, z) = (-1, 2, 3)$.
>
> \# The question asks for all solutions, so say how many there are: every column of the coefficient part has a pivot, so no variable is free and the solution is unique. Check: $y + z = 2 + 3 = 5$, $3x - y + z = -3 - 2 + 3 = -2$, $x + y - 3z = -1 + 2 - 9 = -8$.
