%% unit-summary v1.2 · Stewart, Calculus §2.3 pp. 133–147 (scan) · 2026-10-18 %%

## 2.3 Differentiation Formulas

### Constant Functions

Derivative of a Constant Function

$$\frac{d}{dx}(c)=0$$

> graph of $f(x)=c$ is the horizontal line $y=c$: slope $0$

### Power Functions

Equations 1–3: $\frac{d}{dx}(x)=1$, $\frac{d}{dx}(x^2)=2x$, $\frac{d}{dx}(x^3)=3x^2$, $\frac{d}{dx}(x^4)=4x^3$ ⇒ pattern $nx^{n-1}$

The Power Rule: If $n$ is a positive integer, then

$$\frac{d}{dx}(x^n)=nx^{n-1}$$

First proof: $x^n-a^n=(x-a)(x^{n-1}+x^{n-2}a+\cdots+xa^{n-2}+a^{n-1})$

$$f'(a)=\lim_{x\to a}\frac{x^n-a^n}{x-a}=\lim_{x\to a}(x^{n-1}+x^{n-2}a+\cdots+a^{n-1})=\underbrace{a^{n-1}+\cdots+a^{n-1}}_{n\text{ terms}}=na^{n-1}$$

Second proof: Binomial Theorem, $(x+h)^n=x^n+nx^{n-1}h+\frac{n(n-1)}{2}x^{n-2}h^2+\cdots+nxh^{n-1}+h^n$

> after $-x^n$ and $\div h$, every term except $nx^{n-1}$ has $h$ as a factor ⇒ $\to0$

ex. $y=t^4$: $\frac{dy}{dt}=4t^3$; $\frac{d}{dr}(r^3)=3r^2$

### New Derivatives from Old

The Constant Multiple Rule: If $c$ is a constant and $f$ is a differentiable function, then

$$\frac{d}{dx}[cf(x)]=c\frac{d}{dx}f(x)$$

(proof: Limit Law 3)

> $y=2f(x)$: rises doubled, runs the same ⇒ slopes doubled

The Sum and Difference Rules: If $f$ and $g$ are both differentiable, then

$$\frac{d}{dx}[f(x)+g(x)]=\frac{d}{dx}f(x)+\frac{d}{dx}g(x)\qquad\frac{d}{dx}[f(x)-g(x)]=\frac{d}{dx}f(x)-\frac{d}{dx}g(x)$$

$(f+g)'=f'+g'$, $(f-g)'=f'-g'$ (Sum: Limit Law 1; Difference: $f-g=f+(-1)g$)

> - $(f+g+h)'=[(f+g)+h]'=f'+g'+h'$: any number of functions
> - Constant Multiple + Sum + Difference + Power Rule ⇒ any polynomial

ex. horizontal tangent ⇔ $\frac{dy}{dx}=0$: $y=x^4-6x^2+4$, $4x(x^2-3)=0$ ⇒ $(0,4)$, $(\pm\sqrt3,-5)$

ex. $s=2t^3-5t^2+3t+4$ (cm, s): $v=6t^2-10t+3$, $a=\frac{dv}{dt}=12t-10$, $a(2)=14\ \mathrm{cm/s^2}$

### The Product Rule

> $(fg)'\ne f'g'$, ex. $f=x$, $g=x^2$: $(fg)'=(x^3)'=3x^2$, but $f'g'=2x$ (Leibniz's false start)

The Product Rule: If $f$ and $g$ are both differentiable, then

$$\frac{d}{dx}[f(x)g(x)]=f(x)\frac{d}{dx}[g(x)]+g(x)\frac{d}{dx}[f(x)]\qquad(fg)'=fg'+gf'$$

Proof: subtract and add $f(x+h)g(x)$ in the numerator

$$F'(x)=\lim_{h\to0}\left[f(x+h)\frac{g(x+h)-g(x)}{h}+g(x)\frac{f(x+h)-f(x)}{h}\right]=f(x)g'(x)+g(x)f'(x)$$

> - $\lim_{h\to0}g(x)=g(x)$: $g(x)$ is a constant with respect to $h$
> - $\lim_{h\to0}f(x+h)=f(x)$: $f$ **differentiable** at $x$ ⇒ continuous at $x$ (Theorem 2.2.4)

the first function × the derivative of the second + the second function × the derivative of the first

ex. $F(x)=(6x^3)(7x^4)$: $F'=(6x^3)(28x^3)+(7x^4)(18x^2)=294x^6$ (or $42x^7$ first); $y=x^2\sin x$: Product Rule is the only method

ex. $h(x)=xg(x)$, $g(3)=5$, $g'(3)=2$: $h'(3)=3g'(3)+g(3)=11$

### The Quotient Rule

The Quotient Rule: If $f$ and $g$ are differentiable, then

$$\frac{d}{dx}\left[\frac{f(x)}{g(x)}\right]=\frac{g(x)\frac{d}{dx}[f(x)]-f(x)\frac{d}{dx}[g(x)]}{[g(x)]^2}\qquad\left(\frac{f}{g}\right)'=\frac{gf'-fg'}{g^2}$$

> $g(x)\ne0$

Proof: subtract and add $f(x)g(x)$ in the numerator; $\lim_{h\to0}g(x+h)=g(x)$ ($g$ differentiable ⇒ continuous)

the denominator × the derivative of the numerator − the numerator × the derivative of the denominator, all ÷ the square of the denominator

> - any polynomial is differentiable on $\mathbb{R}$; any rational function is differentiable on its domain
> - NOTE: don't use the Quotient Rule **every** time: $F(x)=\frac{3x^2+2\sqrt x}{x}=3x+2x^{-1/2}$ first

ex. $y=\frac{x^2+x-2}{x^3+6}$: $y'=\frac{(x^3+6)(2x+1)-(x^2+x-2)(3x^2)}{(x^3+6)^2}=\frac{-x^4-2x^3+6x^2+12x+6}{(x^3+6)^2}$

### General Power Functions

If $n$ is a positive integer, then

$$\frac{d}{dx}(x^{-n})=-nx^{-n-1}$$

(proof: Quotient Rule on $\frac{1}{x^n}$: $\frac{x^n\cdot0-1\cdot nx^{n-1}}{x^{2n}}=-nx^{-n-1}$)

ex. $\frac{d}{dx}\left(\frac1x\right)=-\frac{1}{x^2}$; $\frac{d}{dt}\left(\frac{6}{t^3}\right)=6(-3)t^{-4}=-\frac{18}{t^4}$

> - $n=0$: $x^0=1$, derivative $0$ ⇒ Power Rule for any integer $n$
> - $n=\frac12$: $\frac{d}{dx}\sqrt x=\frac{1}{2\sqrt x}$ (Example 2.2.3)

The Power Rule (General Version): If $n$ is any real number, then

$$\frac{d}{dx}(x^n)=nx^{n-1}$$

> proof in Chapter 6 (rational $n$: Exercise 2.6.50); holds where $x^n$ and $x^{n-1}$ are defined ($x^{1/2}$: for $x>0$)

ex. $\frac{d}{dx}x^{\pi}=\pi x^{\pi-1}$; $y=\frac{1}{\sqrt[3]{x^2}}=x^{-2/3}$: $y'=-\frac23x^{-5/3}$

ex. $f(t)=\sqrt t\,(a+bt)$ ($a,b$ constants): Product Rule, or $at^{1/2}+bt^{3/2}$ first ⇒ $f'(t)=\frac{a+3bt}{2\sqrt t}$

The **normal line** to a curve $C$ at a point $P$ is the line through $P$ that is perpendicular to the tangent line at $P$.

> slope of the normal line $=-\dfrac{1}{\text{slope of the tangent line}}$ (negative reciprocal)

ex. $y=\frac{\sqrt x}{1+x^2}$ at $\left(1,\frac12\right)$: $y'=\frac{1-3x^2}{2\sqrt x(1+x^2)^2}$, slope $-\frac14$; tangent $y=-\frac14x+\frac34$, normal $y=4x-\frac72$

ex. $xy=12$, tangent parallel to $3x+y=0$: $y=\frac{12}{x}$, $-\frac{12}{a^2}=-3$ ⇒ $a=\pm2$ ⇒ $(2,6)$, $(-2,-6)$

Table of Differentiation Formulas

$$\begin{array}{lll} \dfrac{d}{dx}(c)=0 & \dfrac{d}{dx}(x^n)=nx^{n-1} & \\[8pt] (cf)'=cf' & (f+g)'=f'+g' & (f-g)'=f'-g' \\[8pt] (fg)'=fg'+gf' & \left(\dfrac{f}{g}\right)'=\dfrac{gf'-fg'}{g^2} & \end{array}$$

## Part 2 題型

課本習題 119 題全部分類了。★ 的題目在 Obsidian 的 [[CAL1 HW 2.3 Solutions]] 有完整解答（作業 30 題，加上網路考古題 5 題）。

考古題這次用了 8 份有 2.3 範圍題目的考卷：中原大學微積分（上）期中考 107-1、112-1 A 群、112-1 B 群、114-1 B 群；JHU 110.108 Fall 2012 Midterm 1；Columbia Math V1101 Midterm I；UW Math 124 Fall 2025 Midterm I；UBC Math 100 Fall 2012 Quiz 3。最後一欄把「方法是這一型、但函數要用到後面的 $\sin x$、$e^x$」的題目也算進去。中原 107-1 期中考的答案卷直接標了「2.3 習題 55、107、69*」，就是這一版的 #61、#119、#79（#79 換了一個數字）。

| # | 題型 | 怎麼認 | 做法 | 課本題數 | 8 份考古題裡有幾份 |
|---|---|---|---|---|---|
| 1 | Power Rule 與線性 | 只有 $x^n$、根號、$\frac{1}{x^n}$ 的和；"Differentiate" | 根號、倒數改寫成 $x^n$，逐項 $nx^{n-1}$ | 21 | 3 |
| 2 | 先改寫再微分 | "after first rewriting"；分母是單項式（$x^k$、$\sqrt x$）；乘積可以展開 | 除開或展開成冪次的和，不用 Product、Quotient Rule | 16 | 1 |
| 3 | Product Rule | 兩個因式相乘；"Use the Product Rule" | $(fg)'=fg'+gf'$ | 5 | 4 |
| 4 | Quotient Rule | 分母不是單項式；有常數 $A,B,c$；繁分式 | $\frac{gf'-fg'}{g^2}$，分母放前面；繁分式先化簡 | 16 | 4 |
| 5 | 指定點的切線、法線 | "tangent line (and normal line) ... at the point" | $y-f(a)=f'(a)(x-a)$；法線斜率 $-\frac{1}{f'(a)}$ | 8 | 4 |
| 6 | 高階導數 | $f''$、$f'''$、$f^{(n)}$ | 一次一次微；第 $n$ 階找規律 | 7 | 2 |
| 7 | 應用與意義 | 位置、速度、加速度；"interpret"；單位 | $v=s'$，$a=v'$；單位 = $y$ 的單位 / $x$ 的單位 | 10 | 0 |
| 8 | $f$、$g$ 沒有公式 | 給 $f(a)$、$f'(a)$ 的值；給圖；"find an expression" | 先寫法則，再代值；圖上讀高度和線段斜率 | 8 | 3 |
| 9 | 切線條件 | "horizontal"、"parallel to"、"normal line ... parallel"、"passes through" | 斜率條件 ⇒ 解 $f'(x)=m$；過曲線外的點：設切點 $(a,f(a))$ | 13 | 3 |
| 10 | 求未知係數 | "For what values of $a$ and $b$"、"Find a polynomial such that" | 一個條件一個方程式：同點、同斜率、$P''$ | 5 | 0 |
| 11 | 分段、絕對值的可微性 | 分段函數、$\lvert\ \ \rvert$；"differentiable everywhere"、"find $m$ and $b$" | 交界點：連續 + $f'_-=f'_+$（用定義）；其他地方用公式 | 5 | 1 |
| 12 | 證明與推廣的法則 | "Prove"、Extended Product Rule、Reciprocal Rule | 從 Product、Quotient Rule 出發，一步一個法則 | 4 | 0 |
| 13 | 極限其實是導數 | $\lim_{x\to a}\frac{f(x)-f(a)}{x-a}$ 或 $\lim_{h\to0}\frac{f(x+h)-f(x)}{h}$ 的形狀 | 認出 $f$ 和 $a$，答案是 $f'(a)$ | 1 | 3 |

題數加起來是 $21+16+5+16+8+7+10+8+13+5+5+4+1=119$。

**判斷順序：**
- 題目是極限：先看是不是導數的定義（第 13 類）。
- 只要 $f'$，看函數長相：
  - 冪次、根號的和：第 1 類
  - 分母是單項式，或乘積能展開：第 2 類（題目指定法則時照題目）
  - 乘積：第 3 類；分式：第 4 類
- 分段或絕對值：第 11 類。
- 沒有公式（給值、給圖、一般的 $g$）：第 8 類。
- 要 $f''$ 以上：第 6 類。
- 要直線：點給了是第 5 類；點要自己找是第 9 類；有未知係數是第 10 類。
- 有單位、時間、價格：第 7 類。

## 1. Power Rule 與線性

根號寫成分數指數、$\frac{1}{x^n}$ 寫成 $x^{-n}$，再逐項用 $nx^{n-1}$；常數乘法、加減法則讓每一項分開算。#1–14、25、26、53–57。

| 題目 | 出處 | 答案 |
|---|---|---|
| $f(x)=x^{3/2}+x^{-3}$ | #7 ★ | $\frac32x^{1/2}-3x^{-4}$ |
| $g(x)=\frac{1}{\sqrt x}+\sqrt[4]{x}$ | #13 ★ | $-\frac12x^{-3/2}+\frac14x^{-3/4}$ |
| $y=tx^2+t^3x$ | #25 ★ | $\frac{dy}{dx}=2tx+t^3$，$\frac{dy}{dt}=x^2+3t^2x$ |
| $P(x)=a_nx^n+\cdots+a_1x+a_0$ | #53 ★ | $na_nx^{n-1}+\cdots+2a_2x+a_1$ |
| $x^8+12x^5-4x^4+10x^3-6x+5$ | 課本 Ex 3 | $8x^7+60x^4-16x^3+30x^2-6$ |
| $f(x)=2x^{3/2}+x+9$，求 $f'(16)$ | 中原 112-1 B 期中 I.1 | $3\sqrt{16}+1=13$ |

- 負指數減 1 會更負：$-3-1=-4$，不是 $-2$。
- $\sqrt[4]{x}=x^{1/4}$，$\frac{1}{\sqrt x}=x^{-1/2}$；$\pi^2$、$\sqrt2$ 是常數，導數是 0。
- $\frac{d}{dx}$ 和 $\frac{d}{dt}$ 的變數不同，其他字母都當常數（#25）。

## 2. 先改寫再微分

分母是單項式就逐項除開（指數相減）；乘積就展開（平方差 $(a-b)(a+b)=a^2-b^2$ 最快）。#15–24、39、41、43–46。

| 題目 | 出處 | 答案 |
|---|---|---|
| $G(r)=\frac{3r^{3/2}+r^{5/2}}{r}$ | #21 ★ | $\frac32r^{-1/2}+\frac32r^{1/2}$ |
| $P(w)=\frac{2w^2-w+4}{\sqrt w}$ | #23 ★ | $3w^{1/2}-\frac12w^{-1/2}-2w^{-3/2}$ |
| $H(u)=(u-\sqrt u)(u+\sqrt u)$ | #43 ★ | $2u-1$ |
| $J(u)=\left(\frac1u+\frac1{u^2}\right)\left(u+\frac1u\right)$ | #45 ★ | $-u^{-2}-2u^{-3}-3u^{-4}$ |
| $F(x)=\frac{3x^2+2\sqrt x}{x}$ | 課本 NOTE | $3-x^{-3/2}$ |
| $y=\frac{x^3-2x^2+x-4}{2\sqrt x}$ | 中原 112-1 B 期中 II.1 | $\frac54x^{3/2}-\frac32x^{1/2}+\frac14x^{-1/2}+x^{-3/2}$ |

- 題目寫 "Do not use the Product or Quotient Rules" 就一定要改寫（#15–24）。
- 除以 $\sqrt w$ 是每個指數減 $\frac12$，常數項 $4$ 變成 $4w^{-1/2}$，不會消失。
- 分母有兩項以上（$x^2+1$）不能逐項除開，要用第 4 類。

## 3. Product Rule

前 × 後的導數 + 後 × 前的導數。兩個多項式也可以先乘開，用來驗算。#27、29–32。

| 題目 | 出處 | 答案 |
|---|---|---|
| $(1+2x^2)(x-x^2)$，兩種方法 | #27 ★ | $1-2x+6x^2-8x^3$ |
| $y=(4x^2+3)(2x+5)$ | #31 ★ | $24x^2+40x+6$ |
| $F(x)=(6x^3)(7x^4)$ | 課本 Ex 6 | $294x^6$ |
| $f(t)=\sqrt t\,(a+bt)$ | 課本 Ex 11 | $\frac{a+3bt}{2\sqrt t}$ |
| $f(x)=x^{1/2}(x^2+3x-1)$ | 中原 112-1 B 期中 I.2 | $\frac52x^{3/2}+\frac92x^{1/2}-\frac12x^{-1/2}$ |

- $(fg)'\ne f'g'$：$x\cdot x^2$ 的導數是 $3x^2$，不是 $2x$。
- 題目指定法則就要用：中原 114-1 B 期中 II.5 寫「不使用導數的乘法公式計算不予計分」。

## 4. Quotient Rule

$\left(\frac fg\right)'=\frac{gf'-fg'}{g^2}$：分母 × 分子的導數 − 分子 × 分母的導數，除以分母平方。#28、33–38、40、42、47–52、58。

| 題目 | 出處 | 答案 |
|---|---|---|
| $g(t)=\frac{3-2t}{5t+1}$ | #35 ★ | $-\frac{17}{(5t+1)^2}$ |
| $f(t)=\frac{5t}{t^3-t-1}$ | #37 ★ | $-\frac{5(2t^3+1)}{(t^3-t-1)^2}$ |
| $G(y)=\frac{B}{Ay^3+B}$ | #49 ★ | $-\frac{3ABy^2}{(Ay^3+B)^2}$ |
| $f(x)=\frac{x}{x+c/x}$ | #51 ★ | $\frac{2cx}{(x^2+c)^2}$ |
| $y=\frac{x^2+x-2}{x^3+6}$ | 課本 Ex 8 | $\frac{-x^4-2x^3+6x^2+12x+6}{(x^3+6)^2}$ |
| $f(x)=\frac{5x-2}{x^2+1}$ | 中原 112-1 A 期中 II.1(a) | $\frac{-5x^2+4x+5}{(x^2+1)^2}$ |
| $f(x)=\frac{x^2+2x}{x^3-1}$ | 中原 112-1 B 期中 II.4 | $\frac{-x^4-4x^3-2x-2}{(x^3-1)^2}$ |
| $f(x)=\left[\left(1+\frac1x\right)^{-1}+5\right]^{-1}$ | 中原 114-1 B 期中 II.10 ★ | $-\frac{1}{(6x+5)^2}$ |

- 分子的順序反了，答案差一個負號。
- 分母留著平方，不要展開；只化簡分子。
- 分子是常數（#49）：$\left(\frac cg\right)'=-\frac{cg'}{g^2}$，就是 #108 的 Reciprocal Rule。
- 繁分式、負指數（#51、中原 114-1 B II.10）：先化成一個分式，再用一次 Quotient Rule。

## 5. 指定點的切線、法線

$m=f'(a)$，切線 $y-f(a)=m(x-a)$；法線過同一點，斜率 $-\frac1m$。#59–66。

| 題目 | 出處 | 答案 |
|---|---|---|
| $y=x+\sqrt x$，$(1,2)$ | #61 ★；中原 107-1 期中 #1 | 切線 $y=\frac32x+\frac12$，法線 $y=-\frac23x+\frac83$ |
| $y=\frac{3x}{1+5x^2}$，$\left(1,\frac12\right)$ | #63 ★ | 切線 $y=-\frac13x+\frac56$，法線 $y=3x-\frac52$ |
| $y=\frac{\sqrt x}{1+x^2}$，$\left(1,\frac12\right)$ | 課本 Ex 12 | 切線 $y=-\frac14x+\frac34$，法線 $y=4x-\frac72$ |
| $y=\frac{2}{x+1}$，$x=2$ | 中原 114-1 B 期中 II.1 | $y-\frac23=-\frac29(x-2)$ |
| $f(x)=(x^3+x+1)(3x^2+2x-1)$，$x=1$ | 中原 114-1 B 期中 II.8 ★ | $y=40x-28$ |
| $y=\frac{x}{x+4}$，$(-3,-3)$ | 中原 112-1 A 期中 II.2 | $y=4x+9$ |

- 先確認點在曲線上（#63：$y(1)=\frac36=\frac12$）。
- 法線是**負**倒數；$f'(a)=0$ 時法線是鉛直線 $x=a$。
- 只要 $f'(a)$ 時，代數字進每個因式，不必展開 $f'(x)$（中原 114-1 B II.8）。

## 6. 高階導數

一次一次微；每微一次就先化簡。#67–72、98。

| 題目 | 出處 | 答案 |
|---|---|---|
| $f(x)=\frac{x^2}{1+2x}$ | #69 ★ | $f'=\frac{2x^2+2x}{(1+2x)^2}$，$f''=\frac{2}{(1+2x)^3}$ |
| $f(x)=8x^7-6x^5+4x^3-x$，求 $f'''(0)$ | 中原 112-1 B 期中 II.5 ★ | $24$ |
| $f(x)=x^n$、$f(x)=\frac1x$ 的第 $n$ 階 | #98 | $n!$；$\frac{(-1)^nn!}{x^{n+1}}$ |

- 還沒有 Chain Rule（2.5）時，$(1+2x)^2$ 的導數要先展開：$8x+4=4(1+2x)$，再約掉一個 $1+2x$。
- $f'''(0)$ 只剩 $x^3$ 那一項的貢獻：$(4x^3)'''=24$。
- 第 $n$ 階：符號 $(-1)^n$ 和係數 $n!$ 分開找規律。

## 7. 應用與意義

位置 $s(t)$ ⇒ $v=s'$，$a=v'=s''$；"interpret" 要寫一句完整的話（何時、什麼量、增或減、多快、單位）。#73–78、103–106。

| 題目 | 出處 | 答案 |
|---|---|---|
| $s=2t^3-5t^2+3t+4$，$a(2)$ | 課本 Ex 5 | $a=12t-10$，$a(2)=14\ \mathrm{cm/s^2}$ |
| $s=t^3-3t$：$v$、$a$、$a(2)$、$v=0$ 時的 $a$ | #73 | $v=3t^2-3$，$a=6t$，$a(2)=12\ \mathrm{m/s^2}$；$v=0$ 時 $t=1$，$a=6\ \mathrm{m/s^2}$ |
| Boyle's Law：$V=\frac{5.3}{P}$，$\frac{dV}{dP}$ 在 $P=50$ | #77 | $-0.00212\ \mathrm{m^3/kPa}$ |
| $R(p)=pf(p)$，$f(20)=10000$，$f'(20)=-350$ | #104 | $R'(20)=f(20)+20f'(20)=3000$ |

- 時間 $t\ge0$，解出的負根要捨去（#73 的 $t=-1$）。
- 單位是「$y$ 的單位 / $x$ 的單位」。

## 8. f、g 沒有公式

先寫出含 $x$ 的法則，再代值；不能先代值再微分。#79–86。

| 題目 | 出處 | 答案 |
|---|---|---|
| $f(5)=1$，$f'(5)=6$，$g(5)=-3$，$g'(5)=2$ | #79 ★ | $(fg)'(5)=-16$，$\left(\frac fg\right)'(5)=-\frac{20}{9}$，$\left(\frac gf\right)'(5)=20$ |
| 同上但 $g'(5)=-2$ | 中原 107-1 期中 #3 | $-20$，$-\frac{16}{9}$，$16$ |
| $f(x)=\sqrt x\,g(x)$，$g(4)=8$，$g'(4)=7$ | #81 ★ | $f'(4)=16$ |
| $\left.\frac{d}{dx}\frac{h(x)}{x}\right\rvert_{x=2}$ | #82 ★ | $-\frac52$ |
| 由圖：$u=fg$，$v=\frac fg$ | #83 ★ | $u'(1)=3$，$v'(4)=-\frac{7}{12}$ |
| $xg(x)$、$\frac{x}{g(x)}$、$\frac{g(x)}{x}$ | #85 ★ | $xg'+g$，$\frac{g-xg'}{g^2}$，$\frac{xg'-g}{x^2}$ |
| $h(x)=xg(x)$，$g(3)=5$，$g'(3)=2$ | 課本 Ex 7 | $h'(3)=11$ |
| $g(x)=(x^2+1)f(x)$，$f(2)=3$，$f'(2)=-1$ | 中原 112-1 B 期中 II.2 | $g'(2)=7$ |
| $g(x)=(f(x))^2$ | 中原 114-1 B 期中 I.5 | $2f(x)f'(x)$ |

- 圖：$f(a)$ 讀**高度**，$f'(a)$ 讀那一段的**斜率**；轉折點的導數不存在。
- $\left(\frac fg\right)'$ 和 $\left(\frac gf\right)'$ 的分母不同，不是互為負數。

## 9. 切線條件

條件換成斜率：水平 ⇒ $f'(x)=0$；平行 ⇒ 同斜率；法線平行 ⇒ 切線斜率是負倒數。解出 $x$，再用點斜式。過曲線外的點：切點未知，設 $(a,f(a))$，把那個點代進切線。#87–96、116–118。

| 題目 | 出處 | 答案 |
|---|---|---|
| $y=x^4-6x^2+4$ 的水平切線 | 課本 Ex 4 | $(0,4)$、$(\pm\sqrt3,-5)$ |
| $xy=12$ 上平行 $3x+y=0$ 的切線 | 課本 Ex 13 | $(2,6)$、$(-2,-6)$ |
| $y=x^3+3x^2-9x+10$ 的水平切線 | #87 ★ | $(-3,37)$、$(1,5)$ |
| $y=x^3-3x^2+3x-3$，平行 $3x-y=15$ | #91 ★ | $y=3x-3$、$y=3x-7$ |
| $y=\sqrt x$ 的法線平行 $2x+y=1$ | #93 ★ | $y=-2x+3$ |
| $f(x)=\frac14x^2+1$ 的切線過原點 | JHU Fall 2012 Midterm 1 #5 ★ | $a=\pm2$（$y=\pm x$） |
| $f(x)=x^3-x$ 平行 $y=11x$ 的切線 | Columbia V1101 Midterm I #6 | $y=11(x-2)+6$、$y=11(x+2)-6$ |

- 題目問 "points" 要寫兩個座標。
- 法線條件不能直接設 $y'=-2$（#93），要先換成切線斜率 $\frac12$。
- 過 $(0,-4)$、$(2,-3)$ 這種不在曲線上的點（#95、96）：設切點，不能把那個點當切點。

## 10. 求未知係數

一個未知數要一個方程式：「同點」給一個、「同斜率」給一個、$P''$ 再給一個。#97、99–102。

| 題目 | 出處 | 答案 |
|---|---|---|
| $2x+y=b$ 在 $x=2$ 切 $y=ax^2$ | #97 ★ | $a=-\frac12$，$b=2$ |
| $P(2)=5$，$P'(2)=3$，$P''(2)=2$ 的二次多項式 | #99 | $P(x)=x^2-x+3$ |
| $y=Ax^2+Bx+C$ 滿足 $y''+y'-2y=x^2$ | #100 | $A=-\frac12$，$B=-\frac12$，$C=-\frac34$ |
| 在 $(-2,6)$、$(2,0)$ 有水平切線的三次函數 | #101 | $y=\frac{3}{16}x^3-\frac94x+3$ |

- 切點要同時在直線上和曲線上（#97 的 $b$ 是用「同點」求的）。
- 多項式恆等：同次項係數相等（#100）。

## 11. 分段、絕對值的可微性

交界點 $a$：先看連續，不連續就直接不可微；連續時用定義算 $f'_-(a)$、$f'_+(a)$，相等才可微。交界點以外用公式。#111–115。

| 題目 | 出處 | 答案 |
|---|---|---|
| $x^2+1$（$x<1$）、$x+1$（$x\ge1$） | #111 ★ | $f'_-(1)=2\ne1=f'_+(1)$，在 $1$ 不可微 |
| $2x$、$2x-x^2$、$2-x$（交界 $0$、$2$） | #112 | 在 $0$ 可微（$2=2$）；在 $2$ 不可微（$-2\ne-1$） |
| $f(x)=\lvert x^2-9\rvert$ | #113 | 在 $\pm3$ 不可微（在 $3$：$-6\ne6$） |
| $h(x)=\lvert x-1\rvert+\lvert x+2\rvert$ | #114 | 在 $1$、$-2$ 不可微 |
| $x^2$（$x\le2$）、$mx+b$（$x>2$） | #115 ★ | $m=4$，$b=-4$ |
| $4+x$（$x<2$）、$3x$（$x\ge2$） | 中原 114-1 B 期中 II.6 | $f'_-(2)=1\ne3=f'_+(2)$，在 $2$ 不可微 |

- 兩個未知數：連續（兩段接起來）+ 同斜率（沒有尖角）。少了連續，$f'_+$ 會是 $\pm\infty$（#115）。
- $f(a)$ 用包含 $a$ 的那一段；$f(a+h)$ 看 $h$ 的正負用對應的一段。
- 絕對值先拆成分段函數，拆開的點就是要檢查的點。

## 12. 證明與推廣的法則

| 題目 | 出處 | 答案 |
|---|---|---|
| $(fgh)'$，$\frac{d}{dx}[f(x)]^3$ | #107 ★ | $f'gh+fg'h+fgh'$；$3[f(x)]^2f'(x)$ |
| Reciprocal Rule | #108 | $\left(\frac1g\right)'=-\frac{g'}{g^2}$（Quotient Rule 的 $f=1$） |
| 先假設 $F'$ 存在，證 Quotient Rule | #109 | $f=Fg$ ⇒ $f'=F'g+Fg'$ ⇒ $F'=\frac{gf'-fg'}{g^2}$ |
| $F=fg$ 的 $F''$ | #110 | $f''g+2f'g'+fg''$ |
| Power Rule 的兩個證明 | 課本 | 因式分解 $x^n-a^n$；二項式定理 |

- 每一步寫用了哪個法則（Product Rule 用在哪兩個因式）。
- #107(b) 就是 2.5 Chain Rule 的第一個例子。

## 13. 極限其實是導數

| 題目 | 出處 | 答案 |
|---|---|---|
| $\lim_{x\to1}\frac{x^{1000}-1}{x-1}$ | #119 ★；中原 107-1 期中 #2 | $f(x)=x^{1000}$，$f'(1)=1000$ |
| $\lim_{h\to0}\frac{\frac{1}{x+3+h}-\frac{1}{x+3}}{h}$ | UW Fall 2025 Midterm I 2(d) ★ | $f(x)=\frac{1}{x+3}$，$-\frac{1}{(x+3)^2}$ |
| 把 $\lim_{h\to0}\frac{\cos(e^{7+h})-\cos(e^7)}{h}$ 寫成導數 | UBC Math 100 Fall 2012 Quiz 3 #1 | $f'(7)$，$f(x)=\cos(e^x)$ |

- 兩種形狀都要認得：$x\to a$（#119）和 $h\to0$（UW）。
- 答案要寫出 $f$ 和 $a$，再算 $f'(a)$。

## 考古題對照

| 考卷 | 題目 | 題型 |
|---|---|---|
| 中原 107-1 期中 | #1 = 課本 #61；#2 = #119；#3 = #79（$g'(5)=-2$） | 5、13、8 |
| 中原 112-1 A 群期中 | I.4 $(x\cos x)''$；II.1(a) 分式；II.1(b) $x^2\tan x$；II.2 切線 | 6、4、3、5 |
| 中原 112-1 B 群期中 | I.1、II.3 冪次；I.2 乘積；II.1 改寫；II.2 給值；II.4 分式；II.5 $f'''(0)$；II.9 $x\sin\frac1x$ 的切線 | 1、3、2、8、4、6、5 |
| 中原 114-1 B 群期中 | I.1、II.1、II.8 切線；I.2、I.4 冪次；I.5 $(f^2)'$；II.5 乘積；II.6 分段；II.10 繁分式 | 5、1、8、3、11、4 |
| JHU 110.108 Fall 2012 Midterm 1 | #5 過原點的切線 | 9 |
| Columbia Math V1101 Midterm I | 5.1 冪次；5.2 分式；5.3 乘積；#6 平行切線 | 1、4、3、9 |
| UW Math 124 Fall 2025 Midterm I | 2(d) | 13 |
| UBC Math 100 Fall 2012 Quiz 3 | #1 極限寫成導數；#3 過原點的切線（$e^x$） | 13、9 |

## 常一起考的

- **2.2 導數的定義、單邊導數：** 分段函數同一題問連續和可微（#111、#115；中原 114-1 B II.6）。
- **2.1 $x\to a$ 形式的定義：** #119 型的極限。
- **2.4 三角函數、2.5 Chain Rule：** 中原每份期中考都把它們和 2.3 的法則放在同一題（$x^2\tan x$、$(x^2+x+1)^{100}$）；#107(b) 就是 Chain Rule 的第一步。
- **是非題：** 老師的考卷有是非題；這一節最常見的陷阱是 $(fg)'=f'g'$、$\left(\frac fg\right)'=\frac{f'}{g'}$（都是錯的）和「連續 ⇒ 可微」（錯）。

## Sources

- [中原大學 微積分（上）B 群 114 學年度上學期期中考](https://mathwww.cycu.edu.tw/wp-content/uploads/1141-B群題目.pdf)
- [中原大學 微積分（上）B 群 112 學年度上學期期中考](https://mathwww.cycu.edu.tw/wp-content/uploads/1121-B-題目.pdf)
- [中原大學 微積分（上）A 群 112 學年度上學期期中考](https://mathwww.cycu.edu.tw/wp-content/uploads/1121-A-題目.pdf)
- [中原大學 微積分（上）107 學年度上學期期中考](https://mathwww.cycu.edu.tw/wp-content/uploads/10712%E9%A1%8C%E7%9B%AE.pdf)
- [JHU 110.108 Calculus I, Fall 2012 Midterm 1](https://math.jhu.edu/~bernstein/math108Fall2015/Midterm1_Practice3.pdf)
- [Columbia Math V1101 Calculus I, Solutions to Midterm I](https://www.math.columbia.edu/~chaoli/SolutionI.pdf)
- [UW Math 124, Fall 2025 Midterm I](https://sites.math.washington.edu/~m124/source/Exams/Midterm1/bekyel_mid1_au25.pdf)
- [UBC Math 100, Fall 2012 Quiz 3 (solutions)](https://personal.math.ubc.ca/~lior/teaching/1213/100_F12/Quiz/100_Quiz03_soln.pdf)
