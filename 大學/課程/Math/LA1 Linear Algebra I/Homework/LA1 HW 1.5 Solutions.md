---
course: [LA1]
semester: "115-1"
chapter: ["1.5"]
tags: [linear-algebra, homework, solutions, matrix-inverse, linear-systems]
source:
  - "Own solutions; computations checked with sympy"
created: 2026-10-19
questions: "[[LA1 HW 1.5 Questions]]"
up: "[[LA1 Index]]"
format: "math-notes 2.3"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.5 Questions#FB 1.5.11\|FB 1.5.11]] | Yes: four pivots, so $A \sim I$ |
| [[LA1 HW 1.5 Questions#FB 1.5.12\|FB 1.5.12]] | No: the span is $\{\mathbf{b} : b_4 = 2b_1 + b_2 + b_3\}$; for example $\mathbf{e}_4$ is not in it |
| [[LA1 HW 1.5 Questions#FB 1.5.13\|FB 1.5.13]] | a. $A^{-1} = \begin{bmatrix} -7 & 3 \\ -5 & 2 \end{bmatrix}$; b. $x_1 = -37$, $x_2 = -26$ |
| [[LA1 HW 1.5 Questions#FB 1.5.21\|FB 1.5.21]] | $r \ne 0$ |
| [[LA1 HW 1.5 Questions#FB 1.5.22\|FB 1.5.22]] | Proof |
| [[LA1 HW 1.5 Questions#FB 1.5.27\|FB 1.5.27]] | a., b. Proofs |
| [[LA1 HW 1.5 Questions#FB 1.5.29\|FB 1.5.29]] | a. $\begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}$; b. Proof |

Exam problems from other universities, not assigned:

| Exercise | Answer |
| --- | --- |
| [[LA1 HW 1.5 Questions#WEB 1.5.1\|WEB 1.5.1]] | Proof: $E_k \cdots E_1A = I \implies A = E_1^{-1} \cdots E_k^{-1}$ |
| [[LA1 HW 1.5 Questions#WEB 1.5.2\|WEB 1.5.2]] | Proof: $AY = 0 \implies X_0 + Y$ is a solution $\implies Y = 0$ |
| [[LA1 HW 1.5 Questions#WEB 1.5.3\|WEB 1.5.3]] | Proof: $B\mathbf{x} = \mathbf{0} \implies \mathbf{x} = \mathbf{0}$, so $B$ is invertible and $A = B^{-1}$ |
| [[LA1 HW 1.5 Questions#WEB 1.5.4\|WEB 1.5.4]] | Proof by contrapositive: $A\big(B(AB)^{-1}\big) = I$ |
| [[LA1 HW 1.5 Questions#WEB 1.5.5\|WEB 1.5.5]] | (a) F; (b) F; (c) F; (d) T; (e) T |

## FB §1.5 Inverses of Square Matrices

> [!note] Note
> The facts that the answers use.
> - **[[Invertible Matrix|Invertible]]**: $A$ is $n \times n$ and $\exists\, C$ s.t. $AC = CA = I$; then $C = A^{-1}$, and it is unique. *Singular* means not invertible.
> - **Inverse of a product**: $A$, $B$ invertible $\implies$ $AB$ invertible and $(AB)^{-1} = B^{-1}A^{-1}$; with more factors, the inverses come in reverse order.
> - **[[Elementary Matrix|Elementary matrices]]**: a row operation on $A$ is $EA$, where $E$ is the same row operation on $I$. Every elementary matrix is invertible, and $E^{-1}$ is the elementary matrix of the operation that undoes it.
> - **Equivalent conditions** for an $n \times n$ matrix $A$ (Thm 1.12 in lecture, [[LA1 1.5 Thm 1.2 Map.canvas|map]]): $A$ is invertible $\iff$ $A\mathbf{x} = \mathbf{b}$ has a unique solution for every $\mathbf{b}$ $\iff$ $A\mathbf{x} = \mathbf{0}$ has only $\mathbf{x} = \mathbf{0}$ $\iff$ $A \sim I$ $\iff$ $A$ is a product of elementary matrices $\iff$ the column vectors of $A$ span $\mathbb{R}^n$ $\iff$ $A\mathbf{x} = \mathbf{b}$ has a solution for every $\mathbf{b}$ $\iff$ $\operatorname{rank}(A) = n$.
> - **[[Span]]**: $\mathbf{b} \in \operatorname{sp}(\text{columns of } A) \iff A\mathbf{x} = \mathbf{b}$ is consistent $\iff$ $[A \mid \mathbf{b}]$ has no row $[0 \cdots 0 \mid c]$ with $c \ne 0$.
> - **[[Elementary Row Operation|Row operations]]**: $R_i \leftrightarrow R_j$, $R_i \to sR_i$ with $s \ne 0$, $R_i \to R_i + sR_j$, written over $\sim$.
> - Each answer is written as on an exam paper. A paragraph that starts with \# is a remark and is not part of the answer.

### FB 1.5.11
Question: [[LA1 HW 1.5 Questions#FB 1.5.11|FB 1.5.11]]

> [!solution] Solution
> $$
> \begin{aligned}
> A &= \begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 1 & 0 & -1 & 2 \\ -3 & 0 & 0 & -1 \end{bmatrix} \overset{\substack{R_3 \to R_3 - R_1 \\ R_4 \to R_4 + 3R_1}}{\sim} \begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 0 & 0 & -2 & 3 \\ 0 & 0 & 3 & -4 \end{bmatrix} \overset{R_4 \to R_4 + R_3}{\sim} \begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 0 & 0 & -2 & 3 \\ 0 & 0 & 1 & -1 \end{bmatrix} \\[6pt]
> &\overset{R_3 \leftrightarrow R_4}{\sim} \begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & -2 & 3 \end{bmatrix} \overset{R_4 \to R_4 + 2R_3}{\sim} \begin{bmatrix} 1 & 0 & 1 & -1 \\ 0 & -1 & -3 & 4 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 1 \end{bmatrix} = H
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &H \text{ has a pivot in every row (no zero row).} \\
> &\implies \forall\, \mathbf{b} \in \mathbb{R}^4:\ [A \mid \mathbf{b}] \sim [H \mid \mathbf{c}] \text{ has no row } [0\ 0\ 0\ 0 \mid c] \text{ with } c \ne 0 \\
> &\implies A\mathbf{x} = \mathbf{b} \text{ is consistent } \forall\, \mathbf{b} \in \mathbb{R}^4 \\
> &\implies \text{every } \mathbf{b} \in \mathbb{R}^4 \text{ is a linear combination of the column vectors of } A. \\
> &\text{Hence the span of the column vectors is } \mathbb{R}^4.
> \end{aligned}
> $$
>
> \# Four pivots in a $4 \times 4$ matrix also means $A \sim I$, so $A$ is invertible: for a square matrix, "the columns span $\mathbb{R}^n$" and "invertible" are the same condition. The step $R_4 \to R_4 + R_3$ and the interchange avoid fractions; $R_4 \to R_4 + \tfrac{3}{2}R_3$ right away gives the last pivot $\tfrac{1}{2}$ instead.

### FB 1.5.12
Question: [[LA1 HW 1.5 Questions#FB 1.5.12|FB 1.5.12]]

> [!solution] Solution
> $$
> \begin{aligned}
> [A \mid \mathbf{b}] &= \left[\begin{array}{cccc|c} 1 & -2 & 1 & 0 & b_1 \\ -3 & 5 & 0 & 2 & b_2 \\ 0 & 1 & 2 & -4 & b_3 \\ -1 & 2 & 4 & -2 & b_4 \end{array}\right] \overset{\substack{R_2 \to R_2 + 3R_1 \\ R_4 \to R_4 + R_1}}{\sim} \left[\begin{array}{cccc|c} 1 & -2 & 1 & 0 & b_1 \\ 0 & -1 & 3 & 2 & b_2 + 3b_1 \\ 0 & 1 & 2 & -4 & b_3 \\ 0 & 0 & 5 & -2 & b_4 + b_1 \end{array}\right] \\[6pt]
> &\overset{R_3 \to R_3 + R_2}{\sim} \left[\begin{array}{cccc|c} 1 & -2 & 1 & 0 & b_1 \\ 0 & -1 & 3 & 2 & b_2 + 3b_1 \\ 0 & 0 & 5 & -2 & b_3 + b_2 + 3b_1 \\ 0 & 0 & 5 & -2 & b_4 + b_1 \end{array}\right] \overset{R_4 \to R_4 - R_3}{\sim} \left[\begin{array}{cccc|c} 1 & -2 & 1 & 0 & b_1 \\ 0 & -1 & 3 & 2 & b_2 + 3b_1 \\ 0 & 0 & 5 & -2 & b_3 + b_2 + 3b_1 \\ 0 & 0 & 0 & 0 & b_4 - 2b_1 - b_2 - b_3 \end{array}\right]
> \end{aligned}
> $$
> $$
> \begin{aligned}
> &A\mathbf{x} = \mathbf{b} \text{ is consistent} \iff b_4 - 2b_1 - b_2 - b_3 = 0 \\
> &\text{Take } \mathbf{b} = \mathbf{e}_4 = [0, 0, 0, 1]^T:\ b_4 - 2b_1 - b_2 - b_3 = 1 \ne 0 \\
> &\implies A\mathbf{x} = \mathbf{e}_4 \text{ is inconsistent} \implies \mathbf{e}_4 \notin \operatorname{sp}(\text{column vectors of } A). \\
> &\text{Hence the span of the column vectors is not } \mathbb{R}^4.
> \end{aligned}
> $$
>
> \# The zero row of the echelon form is what lets some $\mathbf{b}$ fail; one explicit $\mathbf{b}$ that fails is the complete answer. The span is the set of $\mathbf{b}$ with $b_4 = 2b_1 + b_2 + b_3$. Check with column 1: $2(1) + (-3) + 0 = -1 = b_4$. Only three pivots, so $A$ is not invertible either.

### FB 1.5.13
Question: [[LA1 HW 1.5 Questions#FB 1.5.13|FB 1.5.13]]

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
Question: [[LA1 HW 1.5 Questions#FB 1.5.21|FB 1.5.21]]

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
Question: [[LA1 HW 1.5 Questions#FB 1.5.22|FB 1.5.22]]

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
> \# $(\implies)$ uses: a product of invertible matrices is invertible. $(\impliedby)$ uses: every invertible matrix is a product of elementary matrices, proved in WEB 1.5.1 below.

### FB 1.5.27
Question: [[LA1 HW 1.5 Questions#FB 1.5.27|FB 1.5.27]]

> [!proof] Proof
> **a.**
> $$
> \begin{aligned}
> &\because A \text{ is invertible} \\
> &\therefore A^{-1} \text{ exists and } AA^{-1} = A^{-1}A = I. \\[4pt]
> &\text{Existence: } A(A^{-1}B) = (AA^{-1})B = IB = B, \text{ so } X = A^{-1}B \text{ is a solution.} \\
> &\text{Uniqueness: } AX = B \implies X = IX = (A^{-1}A)X = A^{-1}(AX) = A^{-1}B. \\
> &\text{Hence } X = A^{-1}B \text{ is the unique solution.} \qquad \blacksquare
> \end{aligned}
> $$
> **b.**
> $$
> \begin{aligned}
> &\text{Suppose row operations with elementary matrices } E_1, \dots, E_k \text{ reduce } A \text{ to } I: \\
> &\qquad E_k \cdots E_1A = I. \\
> &\text{Let } P = E_k \cdots E_1. \text{ Then } PA = I \implies P = P(AA^{-1}) = (PA)A^{-1} = A^{-1}. \\
> &\text{The same row operations on } [A \mid B] \text{ multiply it on the left by } P: \\
> &\qquad P[A \mid B] = [PA \mid PB] = [I \mid A^{-1}B]. \\
> &\text{Hence } [A \mid B] \sim [I \mid A^{-1}B], \text{ that is, } B \text{ is reduced to } X = A^{-1}B. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $P[A \mid B] = [PA \mid PB]$ because column $j$ of $PM$ is $P$ times column $j$ of $M$. Which row operations are used does not matter: any $P$ with $PA = I$ is $A^{-1}$. Part a. is Exercise 13 b. with a matrix $B$ in place of the column $\mathbf{b}$, and for $B = I$ part b. is the method $[A \mid I] \sim [I \mid A^{-1}]$.

### FB 1.5.29
Question: [[LA1 HW 1.5 Questions#FB 1.5.29|FB 1.5.29]]

> [!solution] Solution
> **a.**
> $$
> A = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} \ne O, \qquad A^2 = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}\begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix} = O,
> $$
> so $A$ is nilpotent, with $r = 2$.

> [!proof] Proof of b.
> $$
> \begin{aligned}
> &\text{Suppose } A \text{ is invertible and } A^r = O \text{ for some positive integer } r. \\
> &\because A^{-1} \text{ exists and } A^{-1}A = I \\
> &\therefore I = (A^{-1})^{r}A^{r} = (A^{-1})^{r}O = O, \text{ a contradiction, since } I \ne O. \\
> &\text{Hence } A \text{ is not nilpotent.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# $(A^{-1})^{r}A^{r} = A^{-1} \cdots A^{-1}\,A \cdots A = I$: the middle pair $A^{-1}A = I$ cancels, $r$ times, as in the lecture's proof of $(A^{k})^{-1} = (A^{-1})^{k}$. Another way to say it: $A^{r}$ is invertible as a product of invertible matrices, but $O$ is not.

## Exam Problems from Other Universities

> [!note] Note
> These problems are not assigned. They come from linear algebra exams of other universities and add what the assigned exercises leave out.
> - WEB 1.5.1: the proof that an invertible matrix is a product of elementary matrices; Exercise 22 only uses it.
> - WEB 1.5.2: invertibility from a unique solution for one right-hand side only.
> - WEB 1.5.3: a one-sided inverse of a square matrix is enough: $AB = I \implies BA = I$.
> - WEB 1.5.4: a "not invertible" statement, proved through its contrapositive.
> - WEB 1.5.5: a true-or-false set in the format of the quizzes, with $ABA^{-1}$ and an idempotent matrix.
> - The field $\mathbb{F}$ (or $F$) of WEB 1.5.2 and 1.5.3 is $\mathbb{R}$ in this course; the proofs work for any field.

### WEB 1.5.1
Question: [[LA1 HW 1.5 Questions#WEB 1.5.1|WEB 1.5.1]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } A \text{ be an invertible } n \times n \text{ matrix.} \\[4pt]
> (1)\ \ &A\mathbf{x} = \mathbf{0} \implies \mathbf{x} = I\mathbf{x} = (A^{-1}A)\mathbf{x} = A^{-1}(A\mathbf{x}) = A^{-1}\mathbf{0} = \mathbf{0}. \\
> &\text{So } A\mathbf{x} = \mathbf{0} \text{ has only the trivial solution.} \\[4pt]
> (2)\ \ &\text{Reduce } A \text{ to its reduced row-echelon form } H:\ E_k \cdots E_1A = H,\ E_t \text{ elementary.} \\
> &[A \mid \mathbf{0}] \sim [H \mid \mathbf{0}] \implies H\mathbf{x} = \mathbf{0} \text{ has only } \mathbf{x} = \mathbf{0} \\
> &\implies \text{no free variable} \implies \text{a pivot in each of the } n \text{ columns} \\
> &\implies H = I \quad (H \text{ is } n \times n \text{ and reduced}). \\[4pt]
> (3)\ \ &E_k \cdots E_1A = I \\
> &\implies A = E_1^{-1}E_2^{-1} \cdots E_k^{-1} \quad (\text{multiply on the left by } E_k^{-1}, \dots, E_1^{-1} \text{ in turn}). \\
> &\because \text{the inverse of an elementary matrix is an elementary matrix} \\
> &\therefore A \text{ is a product of elementary matrices.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# This is the way around the board's equivalence theorem from "invertible" through "$A\mathbf{x} = \mathbf{0}$ has only $\mathbf{x} = \mathbf{0}$" and "$A \sim I$" to "product of elementary matrices". Step (2) is the one to write in full on an exam: $n$ pivots in an $n \times n$ reduced matrix put a $1$ on every diagonal entry and $0$ everywhere else.

### WEB 1.5.2
Question: [[LA1 HW 1.5 Questions#WEB 1.5.2|WEB 1.5.2]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } X_0 \text{ be the unique solution: } AX_0 = b. \\
> &\text{Suppose } AY = 0. \text{ Then } A(X_0 + Y) = AX_0 + AY = b + 0 = b, \\
> &\text{so } X_0 + Y \text{ is also a solution} \implies X_0 + Y = X_0 \implies Y = 0. \\
> &\therefore AX = 0 \text{ has only the trivial solution.} \\
> &\implies \text{the reduced row-echelon form of } A \text{ is } I \quad (\text{as in WEB 1.5.1 (2)}) \\
> &\implies E_k \cdots E_1A = I \implies A = E_1^{-1} \cdots E_k^{-1}, \text{ a product of invertible matrices.} \\
> &\text{Hence } A \text{ is invertible.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# The hypothesis is about one $b$ only, not every $b$. Every nonzero $Y$ with $AY = 0$ would give a second solution $X_0 + Y$, so uniqueness for a single $b$ already rules out the nonzero solutions of $AX = 0$.

### WEB 1.5.3
Question: [[LA1 HW 1.5 Questions#WEB 1.5.3|WEB 1.5.3]]

> [!proof] Proof
> $$
> \begin{aligned}
> (\implies)\ \ &A \text{ is invertible} \implies B = A^{-1} \text{ gives } AB = I. \\[4pt]
> (\impliedby)\ \ &\text{Suppose } AB = I. \\
> &B\mathbf{x} = \mathbf{0} \implies \mathbf{x} = I\mathbf{x} = (AB)\mathbf{x} = A(B\mathbf{x}) = A\mathbf{0} = \mathbf{0} \\
> &\therefore B\mathbf{x} = \mathbf{0} \text{ has only the trivial solution} \implies B \text{ is invertible (as in WEB 1.5.2).} \\
> &\implies A = AI = A(BB^{-1}) = (AB)B^{-1} = IB^{-1} = B^{-1}. \\
> &\text{Hence } A = B^{-1} \text{ is invertible, with } A^{-1} = B. \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Work with $B$, not with $A$: from $AB = I$, the equation $B\mathbf{x} = \mathbf{0}$ can be multiplied by $A$ on the left. Starting from $A\mathbf{x} = \mathbf{0}$ leads nowhere, because $B$ stands on the wrong side. As a result, for square matrices $AB = I$ is enough, and then $BA = BB^{-1} = I$ as well.

### WEB 1.5.4
Question: [[LA1 HW 1.5 Questions#WEB 1.5.4|WEB 1.5.4]]

> [!proof] Proof
> $$
> \begin{aligned}
> &\text{Let } A, B \text{ be } n \times n. \text{ Suppose } AB \text{ is invertible, and let } C = (AB)^{-1}. \\
> &\implies A(BC) = (AB)C = I \\
> &\implies A \text{ is invertible} \quad (AD = I \text{ with } D = BC; \text{ WEB 1.5.3}). \\
> &\therefore AB \text{ invertible} \implies A \text{ invertible.} \\
> &\text{Hence, by the contrapositive, } A \text{ not invertible} \implies AB \text{ not invertible.} \qquad \blacksquare
> \end{aligned}
> $$
>
> \# Showing "not invertible" directly means showing that no inverse exists, which is hard; the contrapositive needs only one product equal to $I$. The sizes matter: $A = \begin{bmatrix} 1 & 0 \end{bmatrix}$ is not invertible (not square), $B = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$, and $AB = \begin{bmatrix} 1 \end{bmatrix}$ is invertible. [[LA1 HW 1.4 1.5 Solutions#NIC 2.4.34|NIC 2.4.34]] proves more: $AB$ invertible $\implies$ $A$ and $B$ invertible.

### WEB 1.5.5
Question: [[LA1 HW 1.5 Questions#WEB 1.5.5|WEB 1.5.5]]

> [!solution] Solution
> - (a) **F.** $B = O$: $AB = AO = O = B$ for every $A$, but $O \ne I$.
> - (b) **F.** $A$ invertible $\implies$ the system has exactly one solution, $\mathbf{x} = A^{-1}\mathbf{b}$.
> - (c) **F.** $A = \begin{bmatrix} 1 & 1 \\ 0 & 1 \end{bmatrix}$, $B = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$: $ABA^{-1} = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}\begin{bmatrix} 1 & -1 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} 1 & -1 \\ 0 & 0 \end{bmatrix} \ne B$.
> - (d) **T.** $A^2 = A$ and $A^{-1}$ exists $\implies$ $A = A^{-1}A^2 = A^{-1}A = I$.
> - (e) **T.** $\mathbf{v} = [0, 0, 1]$ is a solution $\implies$ $A(t\mathbf{v}) = tA\mathbf{v} = \mathbf{0}$ $\forall\, t \in \mathbb{R}$ $\implies$ infinitely many solutions.
>
> \# (c) $ABA^{-1} = B \iff AB = BA$ (multiply by $A$ on the right); here $AB = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} \ne \begin{bmatrix} 1 & 1 \\ 0 & 0 \end{bmatrix} = BA$. (d) $A^{-1}A^2 = (A^{-1}A)A = A$ on one side, and $A^{-1}A^2 = A^{-1}A = I$ by $A^2 = A$ on the other; it is the board's $A^2 = A \implies A = I$ or $A$ singular. (e) is §1.4: a homogeneous system with a nonzero solution has infinitely many.
