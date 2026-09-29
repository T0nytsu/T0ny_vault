---
title: "115-1 Linear Algebra I – Quiz #1"
course: 線性代數(一)
semester: 115-1
type: quiz
quiz_no: 1
version: "1134"
score: 5
total: 10
date:
student_number: "4115053134"
name: 林恩同
tags:
  - linear-algebra
  - quiz
  - semester/115-1
---

# 115-1, Linear Algebra I – Quiz #1 `[1134]`

**Student number:** 4115053134　**Name:** 林恩同　**Score:** 5 / 10

> [!info] Margin note on the paper
> 請正楷書寫

---

## 1. True or False (5 pts.) — +5 ✅

Make each of the following True or False.

- **F** (a) The span of any two nonzero vectors in $\mathbb{R}^2$ is all of $\mathbb{R}^2$.
- **T** (b) Every nonzero vector in $\mathbb{R}^n$ has nonzero magnitude.
- **F** (c) Every nonzero vector $v$ in $\mathbb{R}^n$ has exactly one unit vector parallel to it.
- **F** (d) The dot product of a vector with itself yields the magnitude of the vector.
- **T** (e) There are exactly two unit vectors parallel to any given nonzero vector in $\mathbb{R}^n$.

> [!note]- Why (review)
> - (a) Two parallel vectors, e.g. $(1,0)$ and $(2,0)$, only span a line.
> - (b) $\lVert v \rVert = 0$ only when $v = 0$.
> - (c), (e) Both $\dfrac{v}{\lVert v \rVert}$ and $-\dfrac{v}{\lVert v \rVert}$ are unit vectors parallel to $v$.
> - (d) $v \cdot v = \lVert v \rVert^2$ — the magnitude **squared**.

---

## 2. Proof (5 pts.) — +0 ❌

Let $v, w$ be any vectors in $\mathbb{R}^n$, and let $r$ be any scalar in $\mathbb{R}$.
Show that $r(v + w) = rv + rw$.

**Proof:** *(handwritten answer)*

Writing

$$
\begin{aligned}
v &= [v_1, v_2, \dots, v_n], & rv &= [rv_1, rv_2, \dots, rv_n] \\
w &= [w_1, w_2, \dots, w_n], & rw &= [rw_1, rw_2, \dots, rw_n]
\end{aligned}
$$

$$
\begin{aligned}
r(v + w) &= r\big([v_1, v_2, \dots, v_n] + [w_1, w_2, \dots, w_n]\big) \\
&= [rv_1, rv_2, \dots, rv_n] + [rw_1, rw_2, \dots, rw_n] \quad \longleftarrow \text{marked ✗} \\
&= rv + rw
\end{aligned}
$$

Hence $r(v + w) = rv + rw$.

> [!tip] Corrected proof *(added afterwards — not on the original quiz)*
> The ✗ line jumps from $r(v+w)$ straight to $[rv_i] + [rw_i]$, which is the distributive property the question asks you to prove. Justify it component by component:
>
> $$
> \begin{aligned}
> r(v + w) &= r\,[v_1 + w_1, \dots, v_n + w_n] && \text{(def. of vector addition)} \\
> &= [r(v_1 + w_1), \dots, r(v_n + w_n)] && \text{(def. of scalar multiplication)} \\
> &= [rv_1 + rw_1, \dots, rv_n + rw_n] && \text{(distributive law in } \mathbb{R}\text{)} \\
> &= [rv_1, \dots, rv_n] + [rw_1, \dots, rw_n] && \text{(def. of vector addition)} \\
> &= rv + rw && \text{(def. of scalar multiplication)}
> \end{aligned}
> $$
