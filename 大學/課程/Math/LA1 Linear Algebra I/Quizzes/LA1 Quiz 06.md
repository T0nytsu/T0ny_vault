---
course: [LA1]
semester: "115-1"
chapter: ["1.5"]
tags: [linear-algebra, quiz, matrix-inverse]
source:
  - "LA1 Quiz #6 [1134] (115-1), graded scan"
  - "[[LA1 Quiz 06 p1.jpg]]"
created: 2026-10-27
score: "3/5"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
> [!abstract] Result: 3/5
> - Q1 Inverse of a Matrix: 3/5. The method, row reducing $[A \mid I]$ to $[I \mid C]$ to find the [[Invertible Matrix|inverse]], and the reasoning are right. One entry of row 2 was copied wrong in the step that only scales row 3, so the third column of $A^{-1}$ came out as $(-5, 3, -1)$ instead of $(-3, 2, -1)$.

> [!note] Notation
> - In the attempt, as written beside the matrices: $\hookleftarrow{\times}s$ on a row means that $s$ times the pivot row of the step is added to that row. The step that multiplies row 3 by $-1$ carries no mark. $\overset{r}{\sim}$ is [[Row Equivalence|row equivalence]].
> - In the solution, as in lecture: $r_{i}^{s}$ multiplies row $i$ by $s \ne 0$, and $r_{ij}^{s}$ adds $s$ times row $i$ to row $j$; $R_{i}^{s}$, $R_{ij}^{s}$ are the row-elementary matrices, and a superscript is the scalar, not a power. $\overset{R_{13}^{-1}}{\sim}$ names the operation of a step.

## Q1 Inverse of a Matrix

> [!question]
> (5 pts.) Determine whether the matrix $A = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 2 \\ 1 & 3 & 2 \end{bmatrix}$ is invertible, and find its inverse if it exists.

> [!attempt] My answer: 3/5
> $$
> \begin{aligned}
> &{[A \mid I]} = \left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 2 & 0 & 1 & 0 \\ 1 & 3 & 2 & 0 & 0 & 1 \end{array}\right]\!\begin{array}{l} \vphantom{0} \\ \vphantom{0} \\ \hookleftarrow{\times}(-1) \end{array} \overset{r}{\sim} \left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 2 & 0 & 1 & 0 \\ 0 & 1 & 1 & -1 & 0 & 1 \end{array}\right]\!\begin{array}{l} \vphantom{0} \\ \vphantom{0} \\ \hookleftarrow{\times}(-1) \end{array} \\[8pt]
> &\overset{r}{\sim} \left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 2 & 0 & 1 & 0 \\ 0 & 0 & -1 & -1 & -1 & 1 \end{array}\right] \overset{r}{\sim} \left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 2 & 0 & 1 & 1 \\ 0 & 0 & 1 & 1 & 1 & -1 \end{array}\right]\!\begin{array}{l} \hookleftarrow{\times}(-1) \\ \hookleftarrow{\times}(-2) \\ \vphantom{0} \end{array} \\[8pt]
> &\overset{r}{\sim} \left[\begin{array}{ccc|ccc} 1 & 2 & 0 & 0 & -1 & 1 \\ 0 & 1 & 0 & -2 & -1 & 3 \\ 0 & 0 & 1 & 1 & 1 & -1 \end{array}\right]\!\begin{array}{l} \hookleftarrow{\times}(-2) \\ \vphantom{0} \\ \vphantom{0} \end{array} \overset{r}{\sim} \left[\begin{array}{ccc|ccc} 1 & 0 & 0 & 4 & 1 & -5 \\ 0 & 1 & 0 & -2 & -1 & 3 \\ 0 & 0 & 1 & 1 & 1 & -1 \end{array}\right] = [I \mid C]
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\because A \overset{r}{\sim} I \\
> &\therefore A \text{ is invertible} \\
> &\qquad C[A \mid I] = [CA \mid C] = [I \mid C] \\
> &\implies A^{-1} = C = \begin{bmatrix} 4 & 1 & -5 \\ -2 & -1 & 3 \\ 1 & 1 & -1 \end{bmatrix}
> \end{aligned}
> $$
> $$
> \text{Hence } A \text{ is invertible and } A^{-1} = \begin{bmatrix} 4 & 1 & -5 \\ -2 & -1 & 3 \\ 1 & 1 & -1 \end{bmatrix}. \quad \text{✗}
> $$

> [!failure] Mistake: an entry of row 2 copied wrong
> The step from the third to the fourth matrix only multiplies row 3 by $-1$, so rows 1 and 2 are copied unchanged. Row 2 was copied as
> $$
> \left[\begin{array}{ccc|ccc} 0 & 1 & 2 & 0 & 1 & 1 \end{array}\right] \quad \text{instead of} \quad \left[\begin{array}{ccc|ccc} 0 & 1 & 2 & 0 & 1 & 0 \end{array}\right].
> $$
> Every later step is computed correctly from that row, so the wrong $1$ moves into the third column of $C$. Adding $-2$ times row 3 to row 2 gives $1 - 2(-1) = 3$ instead of $0 - 2(-1) = 2$ in entry $(2, 3)$ of $C$; adding $-2$ times row 2 to row 1 then gives $1 - 2 \cdot 3 = -5$ instead of $1 - 2 \cdot 2 = -3$ in entry $(1, 3)$. These are the two entries the grader circled. The row reduction and the reasoning ($A \overset{r}{\sim} I$, so $A$ is invertible, and $C[A \mid I] = [I \mid C]$) are right.
>
> Multiplying back would have caught it: with this $C$, the third column of $AC$ is $\begin{bmatrix} 0 \\ 1 \\ 2 \end{bmatrix}$, not $\begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}$.

> [!solution]- Solution
> $$
> \begin{aligned}
> {[A \mid I]} = \left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 2 & 0 & 1 & 0 \\ 1 & 3 & 2 & 0 & 0 & 1 \end{array}\right] &\overset{R_{13}^{-1}}{\sim} \left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 2 & 0 & 1 & 0 \\ 0 & 1 & 1 & -1 & 0 & 1 \end{array}\right] \\[8pt]
> &\overset{R_{23}^{-1}}{\sim} \left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 2 & 0 & 1 & 0 \\ 0 & 0 & -1 & -1 & -1 & 1 \end{array}\right] \overset{R_{3}^{-1}}{\sim} \left[\begin{array}{ccc|ccc} 1 & 2 & 1 & 1 & 0 & 0 \\ 0 & 1 & 2 & 0 & 1 & 0 \\ 0 & 0 & 1 & 1 & 1 & -1 \end{array}\right] \\[8pt]
> &\overset{\substack{R_{31}^{-1} \\ R_{32}^{-2}}}{\sim} \left[\begin{array}{ccc|ccc} 1 & 2 & 0 & 0 & -1 & 1 \\ 0 & 1 & 0 & -2 & -1 & 2 \\ 0 & 0 & 1 & 1 & 1 & -1 \end{array}\right] \overset{R_{21}^{-2}}{\sim} \left[\begin{array}{ccc|ccc} 1 & 0 & 0 & 4 & 1 & -3 \\ 0 & 1 & 0 & -2 & -1 & 2 \\ 0 & 0 & 1 & 1 & 1 & -1 \end{array}\right] = [I \mid C]
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &\because A \overset{r}{\sim} I \quad \therefore A \text{ is invertible} \\
> &C := R_{21}^{-2}R_{31}^{-1}R_{32}^{-2}R_{3}^{-1}R_{23}^{-1}R_{13}^{-1} \implies C[A \mid I] = [CA \mid C] = [I \mid C] \\
> &\implies CA = I \implies A^{-1} = C
> \end{aligned}
> $$
> $$
> \text{Hence } A \text{ is invertible and } A^{-1} = \begin{bmatrix} 4 & 1 & -3 \\ -2 & -1 & 2 \\ 1 & 1 & -1 \end{bmatrix}.
> $$
>
> \# A step that changes one row leaves the other rows as they are, so copy them straight from the line above. Then check by multiplying back, one column at a time; for the third column, $A\begin{bmatrix} -3 \\ 2 \\ -1 \end{bmatrix} = \begin{bmatrix} -3 + 4 - 1 \\ 0 + 2 - 2 \\ -3 + 6 - 2 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}$, the third column of $I$. $C$ is the product of the [[Elementary Matrix|row-elementary matrices]] of the steps, which is why $C[A \mid I] = [I \mid C]$ gives the inverse.
