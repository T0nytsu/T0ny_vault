---
course: [LA1]
chapter: ["1.4"]
tags: [linear-algebra, homework, questions, linear-systems]
source:
  - "FB §1.4 exercises pp. 68-71, scanned PDF"
created: 2026-10-09
solutions: "[[LA1 HW 1.4 Solutions]]"
---
> [!info] Coverage
> FB §1.4: 5, 9, 13, 18, 21, 25, 27, 29, 35, 38, 40. FB is Fraleigh & Beauregard, *Linear Algebra*.
>
> Additional exercises, not assigned: FB §1.4: 19, 23, 36, 37, 41, 56, 57. They are at the bottom of this note and cover types of problems that the assigned exercises leave out.
>
> Exercises 5, 9, 25, 29 and 40 are also in [[LA1 HW 1.4 1.5 Questions]], with the same solutions. That note also has the §1.4 exercises on elementary matrices (42, 44, 45, 49) and the proofs (52–55, 58).

## FB §1.4 Solving Systems of Linear Equations

### FB 1.4.5
In Exercises 1–6, reduce the matrix to (a) row-echelon form, and (b) reduced row-echelon form. Answers to (a) are not unique, so your answer may differ from the one at the back of the text.
$$
\begin{bmatrix} -1 & 3 & 0 & 1 & 4 \\ 1 & -3 & 0 & 0 & -1 \\ 2 & -6 & 2 & 4 & 0 \\ 0 & 0 & 1 & 3 & -4 \end{bmatrix}
$$

### FB 1.4.9
In Exercises 7–12, describe all solutions of a linear system whose corresponding augmented matrix can be row-reduced to the given matrix. If requested, also give the indicated particular solution, if it exists.
$$
\left[\begin{array}{cccc|c} 1 & 0 & 2 & 0 & 1 \\ 0 & 1 & 1 & 3 & -2 \\ 0 & 0 & 0 & 0 & 0 \end{array}\right],
$$
solution with $x_3 = 3$, $x_4 = -2$

### FB 1.4.13
In Exercises 13–20, find all solutions of the given linear system, using the Gauss method with back substitution.
$$
\begin{aligned}
2x - \phantom{5}y &= 8 \\
6x - 5y &= 32
\end{aligned}
$$

### FB 1.4.18
In Exercises 13–20, find all solutions of the given linear system, using the Gauss method with back substitution.
$$
\begin{aligned}
x_1 - 3x_2 + \phantom{2}x_3 &= 2 \\
3x_1 - 8x_2 + 2x_3 &= 5
\end{aligned}
$$

### FB 1.4.21
In Exercises 21–24, find all solutions of the linear system, using the Gauss–Jordan method.
$$
\begin{aligned}
3x_1 - 2x_2 &= -8 \\
4x_1 + 5x_2 &= -3
\end{aligned}
$$

### FB 1.4.25
In Exercises 25–28, determine whether the vector $\mathbf{b}$ is in the span of the vectors $\mathbf{v}_i$.
$$
\mathbf{b} = \begin{bmatrix} 3 \\ 5 \\ 3 \end{bmatrix}, \quad \mathbf{v}_1 = \begin{bmatrix} 0 \\ 2 \\ 4 \end{bmatrix}, \quad \mathbf{v}_2 = \begin{bmatrix} 1 \\ 4 \\ -2 \end{bmatrix}, \quad \mathbf{v}_3 = \begin{bmatrix} -3 \\ -1 \\ 5 \end{bmatrix}
$$

### FB 1.4.27
In Exercises 25–28, determine whether the vector $\mathbf{b}$ is in the span of the vectors $\mathbf{v}_i$.
$$
\mathbf{b} = \begin{bmatrix} 8 \\ 17 \\ -8 \\ 3 \end{bmatrix}, \quad \mathbf{v}_1 = \begin{bmatrix} 1 \\ 2 \\ -1 \\ 0 \end{bmatrix}, \quad \mathbf{v}_2 = \begin{bmatrix} 2 \\ 5 \\ -2 \\ 5 \end{bmatrix}, \quad \mathbf{v}_3 = \begin{bmatrix} -3 \\ -6 \\ 1 \\ -8 \end{bmatrix}, \quad \mathbf{v}_4 = \begin{bmatrix} 0 \\ 0 \\ -1 \\ -4 \end{bmatrix}
$$

### FB 1.4.29
Mark each of the following True or False.
- a. Every linear system with the same number of equations as unknowns has a unique solution.
- b. Every linear system with the same number of equations as unknowns has at least one solution.
- c. A linear system with more equations than unknowns may have an infinite number of solutions.
- d. A linear system with fewer equations than unknowns may have no solution.
- e. Every matrix is row equivalent to a unique matrix in row-echelon form.
- f. Every matrix is row equivalent to a unique matrix in reduced row-echelon form.
- g. If $[A \mid \mathbf{b}]$ and $[B \mid \mathbf{c}]$ are row-equivalent partitioned matrices, the linear systems $A\mathbf{x} = \mathbf{b}$ and $B\mathbf{x} = \mathbf{c}$ have the same solution set.
- h. A linear system with a square coefficient matrix $A$ has a unique solution if and only if $A$ is row equivalent to the identity matrix.
- i. A linear system with coefficient matrix $A$ has an infinite number of solutions if and only if $A$ can be row-reduced to an echelon matrix that includes some column containing no pivot.
- j. A consistent linear system with coefficient matrix $A$ has an infinite number of solutions if and only if $A$ can be row-reduced to an echelon matrix that includes some column containing no pivot.

### FB 1.4.35
In Exercises 30–37, describe all possible values for the unknowns $x_i$ so that the matrix equation is valid.
$$
\begin{bmatrix} x_1 & x_2 \\ x_3 & x_4 \end{bmatrix} \begin{bmatrix} 1 & 1 \\ 1 & 0 \end{bmatrix} = \begin{bmatrix} 0 & 1 \\ 3 & 1 \end{bmatrix}
$$

### FB 1.4.38
Determine all values of the $b_i$ that make the linear system
$$
\begin{aligned}
x_1 + 2x_2 &= b_1 \\
3x_1 + 6x_2 &= b_2
\end{aligned}
$$
consistent.

### FB 1.4.40
Determine all values of the $b_i$ that make the linear system
$$
\begin{aligned}
x_1 + \phantom{2}x_2 - x_3 &= b_1 \\
2x_2 + x_3 &= b_2 \\
x_2 - x_3 &= b_3
\end{aligned}
$$
consistent.

## FB §1.4 Additional Exercises

### FB 1.4.19
In Exercises 13–20, find all solutions of the given linear system, using the Gauss method with back substitution.
$$
\begin{aligned}
x_1 + 4x_2 - 2x_3 &= 4 \\
2x_1 + 7x_2 - \phantom{2}x_3 &= -2 \\
2x_1 + 9x_2 - 7x_3 &= 1
\end{aligned}
$$

### FB 1.4.23
In Exercises 21–24, find all solutions of the linear system, using the Gauss–Jordan method.
$$
\begin{aligned}
x_1 \phantom{{}- 3x_2} - 2x_3 + \phantom{3}x_4 &= 6 \\
2x_1 - \phantom{3}x_2 + \phantom{2}x_3 - 3x_4 &= 0 \\
9x_1 - 3x_2 - \phantom{2}x_3 - 7x_4 &= 4
\end{aligned}
$$

### FB 1.4.36
In Exercises 30–37, describe all possible values for the unknowns $x_i$ so that the matrix equation is valid.
$$
\begin{bmatrix} x_1 & x_2 \end{bmatrix} \begin{bmatrix} 3 & 0 & 4 \\ 2 & 1 & -1 \end{bmatrix} = \begin{bmatrix} 3 & 3 & -7 \end{bmatrix}
$$

### FB 1.4.37
In Exercises 30–37, describe all possible values for the unknowns $x_i$ so that the matrix equation is valid.
$$
\begin{bmatrix} x_1 & x_2 \\ x_3 & x_4 \end{bmatrix} \begin{bmatrix} 3 & 5 \\ 2 & 3 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}
$$

### FB 1.4.41
Determine all values $b_1$, $b_2$, and $b_3$ such that $\mathbf{b} = [b_1, b_2, b_3]$ lies in the span of $\mathbf{v}_1 = [1, 1, 0]$, $\mathbf{v}_2 = [3, -1, 4]$, and $\mathbf{v}_3 = [-1, 2, -3]$.

### FB 1.4.56
Find $a$, $b$, and $c$ such that the parabola $y = ax^2 + bx + c$ passes through the points $(1, -4)$, $(-1, 0)$, and $(2, 3)$.

### FB 1.4.57
Find $a$, $b$, $c$, and $d$ such that the quartic curve $y = ax^4 + bx^3 + cx^2 + d$ passes through $(1, 2)$, $(-1, 6)$, $(-2, 38)$, and $(2, 6)$.
