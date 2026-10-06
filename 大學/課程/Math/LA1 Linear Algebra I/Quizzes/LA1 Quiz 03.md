---
course: [LA1]
chapter: ["1.3"]
tags: [linear-algebra, quiz, matrix-algebra]
source:
  - "LA1 Quiz #3 (115-1, 2026-09-29), graded scan"
  - "[[LA1 Quiz 03 p1.jpg]]"
created: 2026-10-06
score: "10/10"
---
> [!abstract] Result: 10/10
> - Q1 Proof: 5/5.
> - Q2 Trace: 5/5.

## Q1 Proof

> [!question]
> (5 pts.) Prove that, if $A$ is a square matrix, then the matrix $A - A^T$ is skew symmetric.

> [!attempt] My answer: 5/5
> Let $A = [a_{ij}]_{n \times n}$
>
> we have
> $$
> \begin{aligned}
> (A - A^T)^T &= A^T - (A^T)^T \\
> &= A^T - A
> \end{aligned}
> $$
> $$
> \because (A - A^T)^T = A^T - A = -(A - A^T)
> $$
> Hence $A - A^T$ is skew symmetric

> [!proof]- Proof
> Let $A$ be an $n \times n$ matrix. Then $A^T$ and $A - A^T$ are also $n \times n$, and
> $$
> \begin{aligned}
> (A - A^T)^T &= A^T - (A^T)^T && \text{(transpose of a difference)} \\
> &= A^T - A && \text{(\((A^T)^T = A\))} \\
> &= -(A - A^T).
> \end{aligned}
> $$
> Hence $A - A^T$ is [[Skew-Symmetric Matrix|skew symmetric]]. $\blacksquare$
>
> \# A matrix $B$ is skew symmetric if $B^T = -B$, so the whole proof is: take the [[Transpose|transpose]] of $B = A - A^T$ and arrive at $-B$. The compare-entries method is not needed here, because the two transpose rules already give an equation between matrices.

## Q2 Trace

> [!question]
> (5 pts.) Compute the trace of $A$, where $A = \begin{pmatrix} 2 & 0 & 1 \\ 0 & -1 & -3 \\ 1 & -3 & 3 \end{pmatrix}$.

> [!attempt] My answer: 5/5
> By the definition, $\operatorname{tr}(A) = \sum_{i=1}^{3} A_{ii}$
> $$
> \begin{aligned}
> \operatorname{tr}(A) &= 2 + (-1) + 3 \\
> &= 4
> \end{aligned}
> $$

> [!solution]- Solution
> The [[Trace|trace]] is the sum of the diagonal entries:
> $$
> \operatorname{tr}(A) = \sum_{i=1}^{3} A_{ii} = 2 + (-1) + 3 = 4.
> $$
