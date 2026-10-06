%% unit-summary v1 · Stewart, Calculus §1.7 pp. 73–82 (scan) · 2026-10-02 %%

## 1.7 The Precise Definition of a Limit

### Precise Definition of a Limit

Definition 2: $\lim_{x\to a} f(x)=L$ if for every $\varepsilon>0$ there is a number $\delta>0$ such that

$$\text{if } 0<\lvert x-a\rvert<\delta \text{ then } \lvert f(x)-L\rvert<\varepsilon$$

($f$ defined on some open interval that contains $a$, except possibly at $a$ itself)

> - $0<\lvert x-a\rvert$ ⇔ $x\neq a$: $f(a)$ never matters
> - in intervals: $x\in(a-\delta,a+\delta)$, $x\neq a$ ⇒ $f(x)\in(L-\varepsilon,L+\varepsilon)$
> - $\delta$ depends on $\varepsilon$: smaller $\varepsilon$ ⇒ smaller $\delta$ may be required
> - a $\delta$ works ⇒ any smaller $\delta$ also works
> - $\delta$ for one $\varepsilon$ (Example 1: graph, $\varepsilon=0.2$ → $\delta=0.08$) ⇏ proof; a proof gives a $\delta$ for every $\varepsilon$

Proof = guess $\delta$ (preliminary analysis) → show this $\delta$ works

ex. $\lim_{x\to3}(4x-5)=7$: $\lvert(4x-5)-7\rvert=4\lvert x-3\rvert$ ⇒ $\delta=\frac{\varepsilon}{4}$

ex. $\lim_{x\to3}x^2=9$: $\lvert x-3\rvert<1$ ⇒ $\lvert x+3\rvert<7$ ⇒ $\delta=\min\{1,\frac{\varepsilon}{7}\}$

### One-Sided Limits

Definition 3: $\lim_{x\to a^-} f(x)=L$ if for every $\varepsilon>0$ there is $\delta>0$ such that if $a-\delta<x<a$ then $\lvert f(x)-L\rvert<\varepsilon$

Definition 4: $\lim_{x\to a^+} f(x)=L$ if for every $\varepsilon>0$ there is $\delta>0$ such that if $a<x<a+\delta$ then $\lvert f(x)-L\rvert<\varepsilon$

> Definitions 3, 4 = Definition 2 with $x$ only in the left half $(a-\delta,a)$ / right half $(a,a+\delta)$

ex. $\lim_{x\to0^+}\sqrt{x}=0$: $\delta=\varepsilon^2$

### The Limit Laws

> the Limit Laws can be proved from Definition 2, so complicated limits need no $\varepsilon$-$\delta$

Triangle Inequality: $\lvert a+b\rvert\le\lvert a\rvert+\lvert b\rvert$

ex. Sum Law: $\lvert f(x)-L\rvert<\frac{\varepsilon}{2}$ and $\lvert g(x)-M\rvert<\frac{\varepsilon}{2}$, $\delta=\min\{\delta_1,\delta_2\}$

### Infinite Limits

Definition 6: $\lim_{x\to a} f(x)=\infty$ if for every $M>0$ there is $\delta>0$ such that if $0<\lvert x-a\rvert<\delta$ then $f(x)>M$

Definition 7: $\lim_{x\to a} f(x)=-\infty$ if for every $N<0$ there is $\delta>0$ such that if $0<\lvert x-a\rvert<\delta$ then $f(x)<N$

($f$ defined on some open interval that contains $a$, except possibly at $a$ itself)

> $\lvert f(x)-L\rvert<\varepsilon$ becomes $f(x)>M$ / $f(x)<N$; larger $M$ ⇒ smaller $\delta$ may be required

ex. $\lim_{x\to0}\frac{1}{x^2}=\infty$: $\delta=\frac{1}{\sqrt{M}}$

## Part 2 題型

上次找的中原大學 4 份 10 月小考，極限題裡沒有 ε-δ 證明。這次的考古題來自清大 OCW 講義、清大習題和師大轉學考。

| # | 題型 | 怎麼認 | 做法 | 課本與考古題 |
|---|---|---|---|---|
| 1 | 給定 ε 找 δ | 題目給具體的 ε（0.2、0.1…）或給圖 | 解 $f(x)=L\pm\varepsilon$，取離 $a$ 較近的距離 | #1–8、13、14、35 |
| 2 | 一次式（含先約分） | $f$ 是一次式，或約分後是一次式 | $\lvert f(x)-L\rvert=\lvert k\rvert\lvert x-a\rvert$，$\delta=\frac{\varepsilon}{\lvert k\rvert}$ | #15–24、27；清大講義 |
| 3 | 二次以上：先限制 $\lvert x-a\rvert<1$ | 拆成 $\lvert x-a\rvert$ 乘另一個因式 | 求界 $C$，$\delta=\min\{1,\frac{\varepsilon}{C}\}$ | Ex 3、#30–34、36、37；清大講義 |
| 4 | 在 0 或端點的冪次、根號 | $x^n$、$\sqrt[n]{x}$ 趨近 0，常是單邊 | 直接解不等式：$\delta=\varepsilon^{1/n}$ 或 $\varepsilon^n$ | Ex 4、#25、26、28、29 |
| 5 | 無限極限 | 要證 $=\infty$ 或 $-\infty$ | 解 $f(x)>M$（或 $f(x)<N$） | Ex 5、#9、10、41–43 |
| 6 | 用定義證極限不存在 | 證明 lim 不存在 | 反證：假設 $=L$，取 $\varepsilon=\frac12$ | #38、39 |
| 7 | 寫定義、證一般性質 | 寫出定義、證 Limit Law 或定理 | 三角不等式、$\frac{\varepsilon}{2}$、$\delta=\min\{\delta_1,\delta_2\}$ | Sum Law、#40、44；清大習題、師大轉學考 |
| 8 | 應用題（誤差容許） | 給容許誤差 ± | 對應出 $x$、$f(x)$、$a$、$L$、$\varepsilon$、$\delta$ | #11、12 |

**判斷順序：**
- 題目要的是某個 ε 的 δ：第 1 類。
- 要證明對所有 ε 都成立，先看 $f$：
  - 一次式：第 2 類
  - 二次以上：第 3 類
  - 在 0 的冪次或根號：第 4 類
  - $=\pm\infty$：第 5 類
  - 要證不存在：第 6 類

## 1. 給定 ε 找 δ

解 $f(x)=L-\varepsilon$ 和 $f(x)=L+\varepsilon$，算出兩個解到 $a$ 的距離，$\delta$ 取較小的那個。

| 題目 | 出處 | 答案 |
|---|---|---|
| $x^3-5x+6$ 在 1 附近，$\varepsilon=0.2$ | 課本 Ex 1 | $x\approx0.911$、$1.124$，$\delta=0.08$ |
| $\lvert x^2-1\rvert<\frac12$ | #4 | $\sqrt{0.5}<x<\sqrt{1.5}$，$\delta\approx0.22$ |
| $\lvert\sqrt{x^2+5}-3\rvert<0.3$，$x$ 在 2 附近 | #5 | $1.513<x<2.427$，$\delta\approx0.42$ |
| $\lvert 4x-8\rvert<\varepsilon$，$\varepsilon=0.1$、$0.01$ | #13 | $\delta=\frac{\varepsilon}{4}$：$0.025$、$0.0025$ |

- 區間通常不對稱，取比較近的那一側（Ex 1 取 0.08，不是 0.12）。任何更小的 δ 也可以。
- 估計值要往 $a$ 的方向取整：課本把 0.911 寫成 0.92、1.124 寫成 1.12。
- 只算出某個 ε 的 δ，不算證明。

## 2. 一次式（含先約分）

把 $\lvert f(x)-L\rvert$ 化成 $\lvert k\rvert\lvert x-a\rvert$，取 $\delta=\frac{\varepsilon}{\lvert k\rvert}$。證明分兩段寫：
1. 先猜 δ。
2. 再寫「Given $\varepsilon>0$, choose $\delta=\dots$. If $0<\lvert x-a\rvert<\delta$, then … $<\varepsilon$」。

| 題目 | 出處 | δ |
|---|---|---|
| $\lim_{x\to3}(4x-5)=7$ | 課本 Ex 2 | $\frac{\varepsilon}{4}$ |
| $\lim_{x\to2}(2x-1)=3$ | 清大講義 | $\frac{\varepsilon}{2}$ |
| $\lim_{x\to2}(2-3x)=-4$ | #16 | $\frac{\varepsilon}{3}$ |
| $\lim_{x\to9}(1-\frac13x)=-2$ | #19 | $3\varepsilon$ |
| $\lim_{x\to4}\frac{x^2-2x-8}{x-4}=6$ | #21 | $x\neq4$ 時 $=x+2$，所以 $\varepsilon$ |
| $\lim_{x\to-1.5}\frac{9-4x^2}{3+2x}=6$ | #22 | $x\neq-1.5$ 時 $=3-2x$，所以 $\frac{\varepsilon}{2}$ |

- 係數是負的要取絕對值：#16 是 $\lvert-3\rvert$，所以 $\frac{\varepsilon}{3}$。
- 可以約分，是因為定義只看 $0<\lvert x-a\rvert$，也就是 $x\neq a$。
- $\lim_{x\to a}c=c$（#24）任何 δ 都可以；$\lim_{x\to a}x=a$（#23）取 $\delta=\varepsilon$。

## 3. 二次以上：先限制 |x − a| < 1

把 $f(x)-L$ 拆成 $(x-a)\cdot g(x)$。先假設 $\lvert x-a\rvert<1$，求出 $\lvert g(x)\rvert<C$，再取 $\delta=\min\{1,\frac{\varepsilon}{C}\}$。

| 題目 | 出處 | δ |
|---|---|---|
| $\lim_{x\to3}x^2=9$ | 課本 Ex 3 | $\min\{1,\frac{\varepsilon}{7}\}$ |
| $\lim_{x\to2}x^2=4$ | 清大講義 | $\min\{1,\frac{\varepsilon}{5}\}$ |
| $\lim_{x\to-2}(x^2-1)=3$ | #31 | $\min\{1,\frac{\varepsilon}{5}\}$ |
| $\lim_{x\to2}x^3=8$ | #32 | $\min\{1,\frac{\varepsilon}{19}\}$ |
| $\lim_{x\to2}\frac1x=\frac12$ | #36 | $\min\{1,2\varepsilon\}$ |
| $\lim_{x\to a}\sqrt x=\sqrt a$（$a>0$） | #37 | $\min\{a,\sqrt a\,\varepsilon\}$ |

- 一定要取 min：$C$ 只有在 $\lvert x-a\rvert<1$ 時才成立（清大講義也特別強調這點）。
- 界的取法不唯一：#33 改用 $\lvert x-3\rvert<2$，得 $\min\{2,\frac{\varepsilon}{8}\}$ 也對。#34 要你證明 $\lim_{x\to3}x^2=9$ 最大可行的 δ 是 $\sqrt{9+\varepsilon}-3$。

## 4. 在 0 或端點的冪次、根號

直接解不等式。根號只在一側有定義時，用單邊定義（Definition 3、4）。

| 題目 | 出處 | δ |
|---|---|---|
| $\lim_{x\to0^+}\sqrt x=0$ | 課本 Ex 4 | $\varepsilon^2$ |
| $\lim_{x\to0}x^3=0$ | #26 | $\sqrt[3]{\varepsilon}$ |
| $\lim_{x\to-6^+}\sqrt[8]{6+x}=0$ | #28 | $\varepsilon^8$ |
| $\lim_{x\to2}(x^2-4x+5)=1$ | #29 | 化成 $(x-2)^2$，所以 $\sqrt\varepsilon$ |

- 單邊的條件寫成 $a<x<a+\delta$（或 $a-\delta<x<a$），不是 $0<\lvert x-a\rvert<\delta$。

## 5. 無限極限

把 $\lvert f(x)-L\rvert<\varepsilon$ 換成 $f(x)>M$（$-\infty$ 時用 $f(x)<N$，$N<0$），再解出 $\lvert x-a\rvert$ 的範圍。

| 題目 | 出處 | 答案 |
|---|---|---|
| $\lim_{x\to0}\frac{1}{x^2}=\infty$ | 課本 Ex 5 | $\delta=\frac{1}{\sqrt M}$ |
| $\frac{1}{(x+3)^4}>10000$ | #41 | $\lvert x+3\rvert<0.1$ |
| $\lim_{x\to-3}\frac{1}{(x+3)^4}=\infty$ | #42 | $\delta=M^{-1/4}$ |
| $\lim_{x\to-1^-}\frac{5}{(x+1)^3}=-\infty$ | #43 | $\delta=\sqrt[3]{5/\lvert N\rvert}$ |
| $\csc^2x>M$，$x$ 在 $\pi$ 附近，$M=500$、$1000$ | #10 | $\delta\approx0.0447$、$0.0316$ |

- $-\infty$ 用負數 $N$，不等號是 $f(x)<N$。
- #43 是左極限，條件要寫 $-1-\delta<x<-1$。

## 6. 用定義證明極限不存在

用反證：假設 $\lim=L$，取 $\varepsilon=\frac12$，在左右兩側各找一點，推出矛盾。

| 題目 | 出處 | 關鍵 |
|---|---|---|
| $\lim_{t\to0}H(t)$ 不存在 | #38 | 右側 $\lvert1-L\rvert<\frac12$、左側 $\lvert L\rvert<\frac12$，所以 $1\le\lvert1-L\rvert+\lvert L\rvert<1$ |
| $f=0$（有理數）、$1$（無理數），$\lim_{x\to0}f(x)$ | #39 | 任何區間都同時有有理數和無理數，同樣推出矛盾 |

- 兩個 $<\frac12$ 要用 Triangle Inequality 加起來，才會出現矛盾。

## 7. 寫定義、證一般性質

| 題目 | 出處 | 關鍵 |
|---|---|---|
| 寫出 $\lim f(x)=2$ 的 ε-δ 定義 | 師大 102 轉學考 | 照 Definition 2 完整寫出 |
| $f$ 連續、$f(0)>0$ ⇒ 存在 $\delta$ 使 $f>0$ on $(-\delta,\delta)$ | 師大 102 轉學考 | 取 $\varepsilon=\frac{f(0)}{2}$ |
| 已知兩個極限，用 ε-δ 證 $\lim[3f(x)-g(x)]=14$、$\lim[2f(x)g(x)]=10$ | 清大習題 | 仿照 Sum Law 的證法 |
| Sum Law | 課本 | $\frac{\varepsilon}{2}+\frac{\varepsilon}{2}$，$\delta=\min\{\delta_1,\delta_2\}$ |
| $\lim f=\infty$、$\lim g=c$ ⇒ $\lim(f+g)=\infty$ | #44 | 先讓 $\lvert g(x)-c\rvert<1$，再讓 $f(x)>M-c+1$ |

- 寫定義最常漏掉的是「$0<$」。
- 順序也常寫反：先給 ε，再找 δ，δ 是由 ε 決定的。

## 8. 應用題（誤差容許）

| 題目 | 出處 | 答案 |
|---|---|---|
| 圓盤面積 1000 cm²，容許 ±5 cm² | #11 | $r\approx17.84$ cm，$\lvert r-17.84\rvert<0.0445$。對應：$x=r$、$f(x)=\pi r^2$、$a=\sqrt{1000/\pi}$、$L=1000$、$\varepsilon=5$、$\delta\approx0.0445$ |
| $T(w)=0.1w^2+2.155w+20$，維持 200 ± 1 °C | #12 | $w\approx33.0$ W，範圍約 32.88–33.11 W；$\varepsilon=1$、$\delta\approx0.11$ |

## 常一起考的

- **1.8 連續：** 用 ε-δ 證連續，以及保號性（師大轉學考那題）。
- **1.6 Limit Laws 的證明：** 清大習題。
- **$x\to\infty$ 的精確定義：** 例如清大習題的 $\lim_{x\to\infty}\frac{1}{x^2}=0$。課本後面才教。

## Sources

- [清大 OCW 講義 L05：證明極限存在、極限的定理證明](https://ocw.nthu.edu.tw/ocw/upload/7/news/L05_%E8%AD%89%E6%98%8E%E6%A5%B5%E9%99%90%E5%AD%98%E5%9C%A8%202.3%20%E6%A5%B5%E9%99%90%E7%9A%84%E5%AE%9A%E7%90%86%E8%AD%89%E6%98%8E.pdf)
- [清大 OCW 微積分（一）習題](https://ocw.nthu.edu.tw/ocw/upload/7/23/%E5%BE%AE%E7%A9%8D%E5%88%86%EF%BC%88%E4%B8%80%EF%BC%89%E7%BF%92%E9%A1%8C(ok).pdf)
- [師大 102 學年轉學考 微積分（阿摩）](https://yamol.tw/item_essay-+++%28a%29Write+out+the+%CE%B5%CE%B4+definition+of+the-520421.htm)
