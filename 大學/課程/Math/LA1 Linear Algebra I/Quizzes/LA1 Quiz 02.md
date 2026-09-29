---
course: [LA1]
chapter: ["1.3"]
tags: [linear-algebra, quiz, matrix-algebra]
source:
  - "LA1 Quiz #2 (115-1), graded scan"
created: 2026-09-30
score: "4/10"
---
> [!abstract] Result: 4/10
> - Q1 True or False: 4/5. Item (c) was wrong.
> - Q2 Proof: 0/5. The proof replaced each matrix by the sum of its entries and never compared entries.

## Q1 True or False

> [!question]
> (5 pts.) Make each of the following True or False. The statements involve matrices $A$, $B$, and $C$ that are assumed to have appropriate size.
> - (a) If $A^n = O$, then $A = O$.
> - (b) If $A^2 = A$, then $A = O$ or $A = I$.
> - (c) If $A^2 = I$, then $A = \pm I$.
> - (d) If $A^2 = I$, then $A^n = I$ for all integers $n \ge 2$.
> - (e) If $A + C = B + C$, then $A = B$.

> [!attempt] My answer: 4/5
> - (a) F
> - (b) F
> - (c) T ✗
> - (d) F
> - (e) T

> [!failure] Mistake: (c)
> The equation $A^2 = I$ says only that $A$ is its own inverse; it does not force $A = \pm I$. A diagonal matrix may have $1$ in one diagonal entry and $-1$ in another, as in the counterexample below.

> [!solution]- Solution
> - (a) **F.** $A = \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} \ne O$, but $A^2 = O$.
> - (b) **F.** $A = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$ satisfies $A^2 = A$, but $A \ne O$ and $A \ne I$.
> - (c) **F.** $A = \begin{bmatrix} 1 & 0 \\ 0 & -1 \end{bmatrix}$ satisfies $A^2 = I$, but $A \ne \pm I$.
> - (d) **F.** $A = -I$ satisfies $A^2 = I$, but $A^3 = -I \ne I$.
> - (e) **T.** Adding $-C$ to both sides gives $(A + C) + (-C) = (B + C) + (-C)$. By associativity of matrix addition, $(A + C) + (-C) = A + (C + (-C)) = A + O = A$, and in the same way the right side equals $B$. Hence $A = B$.

## Q2 Proof

> [!question]
> (5 pts.) Let $A$, $B$, and $C$ be $m \times n$ matrices. Prove that $(A + B) + C = A + (B + C)$.

> [!attempt] My answer: 0/5
> $$
> \begin{aligned}
> (A+B)+C &= \sum_{i=1}^{m}\sum_{j=1}^{n} [a_{ij} + b_{ij}] + \sum_{i=1}^{m}\sum_{j=1}^{n} [c_{ij}] \quad \text{✗} \\
> &= \sum_{i=1}^{m}\sum_{j=1}^{n} [a_{ij}] + \sum_{i=1}^{m}\sum_{j=1}^{n} [b_{ij}] + \sum_{i=1}^{m}\sum_{j=1}^{n} [c_{ij}] \\
> &= \sum_{i=1}^{m}\sum_{j=1}^{n} [a_{ij}] + \sum_{i=1}^{m}\sum_{j=1}^{n} [b_{ij} + c_{ij}] \\
> &= A + (B+C)
> \end{aligned}
> $$
> Therefore $(A+B)+C = A+(B+C)$.

> [!failure] Mistake: a matrix is not the sum of its entries
> The expression $\sum_{i}\sum_{j} [a_{ij}]$ is a number, namely the sum of all entries of $A$; it is not the matrix $A$. The first equality therefore already fails. To prove that two matrices are equal, show that they have the same size and that their $(i, j)$-entries are equal for every $i$ and $j$.

> [!proof]- Proof
> Write $A = [a_{ij}]$, $B = [b_{ij}]$, $C = [c_{ij}]$. Both sides are $m \times n$ matrices. For every $i = 1, \dots, m$ and $j = 1, \dots, n$,
> $$
> \begin{aligned}
> \big((A+B)+C\big)_{ij} &= (A+B)_{ij} + c_{ij} = (a_{ij} + b_{ij}) + c_{ij} \\
> &\overset{(1)}{=} a_{ij} + (b_{ij} + c_{ij}) = a_{ij} + (B+C)_{ij} = \big(A+(B+C)\big)_{ij}.
> \end{aligned}
> $$
> 1. Associativity of addition in $\mathbb{R}$.
>
> Every entry agrees, so $(A+B)+C = A+(B+C)$. $\blacksquare$
