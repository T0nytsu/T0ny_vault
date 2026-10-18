%% unit-summary v1.2 · Stewart, Calculus §2.5 pp. 156–164 (scan); CYCU and NCCU exams (web) · 2026-10-18 %%

## 2.5 The Chain Rule

ex. $F(x)=\sqrt{x^2+1}$ is a composite function: $F=f\circ g$, $f(u)=\sqrt u$, $g(x)=x^2+1$

### The Chain Rule

If $g$ is differentiable at $x$ and $f$ is differentiable at $g(x)$, then the composite function $F=f\circ g$ defined by $F(x)=f(g(x))$ is differentiable at $x$ and $F'$ is given by the product

Formula 1:

$$F'(x)=f'(g(x))\cdot g'(x)$$

In Leibniz notation, if $y=f(u)$ and $u=g(x)$ are both differentiable functions, then

Formula 2:

$$\frac{dy}{dx}=\frac{dy}{du}\,\frac{du}{dx}$$

> - $g$ **differentiable at $x$**, $f$ **differentiable at $g(x)$** (not at $x$)
> - $\frac{du}{dx}$ is not an actual quotient ($du$ has not been defined): "cancel $du$" only helps to remember Formula 2
> - rates: $u$ changes 2 times as fast as $x$, $y$ 3 times as fast as $u$ ⇒ $y$ 6 times as fast as $x$

Comments on the proof: $\frac{\Delta y}{\Delta x}=\frac{\Delta y}{\Delta u}\cdot\frac{\Delta u}{\Delta x}$, and $\Delta u\to0$ as $\Delta x\to0$ because $g$ is continuous
> flaw: $\Delta u=0$ is possible even when $\Delta x\ne0$, and we can't divide by $0$ ⇒ only *suggests* the Chain Rule (full proof at the end)

ex. $F(x)=\sqrt{x^2+1}$: $F'(x)=\frac{1}{2\sqrt{x^2+1}}\cdot2x=\frac{x}{\sqrt{x^2+1}}$
> $\frac{dy}{dx}=F'(x)=\frac{x}{\sqrt{x^2+1}}$ ($y$ as a function of $x$) whereas $\frac{dy}{du}=f'(u)=\frac{1}{2\sqrt u}$ ($y$ as a function of $u$)

NOTE: work from the outside to the inside

$$\frac{d}{dx}\underbrace{f}_{\text{outer}}\underbrace{(g(x))}_{\text{evaluated at inner}}=\underbrace{f'}_{\text{derivative of outer}}\underbrace{(g(x))}_{\text{evaluated at inner}}\cdot\underbrace{g'(x)}_{\text{derivative of inner}}$$

- ex. $\sin(x^2)$ (outer $\sin$, inner $x^2$): $2x\cos(x^2)$
- ex. $\sin^2x=(\sin x)^2$ (outer square, inner $\sin$): $2\sin x\cos x=\sin2x$

> $\sin(x^2)\ne\sin^2x$: the outer and inner functions swap

$$\frac{d}{dx}(\sin u)=\cos u\,\frac{du}{dx}\qquad(u \text{ a differentiable function of } x)$$

All the formulas for differentiating trigonometric functions combine with the Chain Rule in the same way.

### The Power Rule Combined with the Chain Rule

Rule 4: If $n$ is any real number and $u=g(x)$ is differentiable, then

$$\frac{d}{dx}(u^n)=nu^{n-1}\frac{du}{dx}\qquad\text{Alternatively,}\quad\frac{d}{dx}[g(x)]^n=n[g(x)]^{n-1}\cdot g'(x)$$

> $n$ **any real number** (Example 1 is Rule 4 with $n=\frac12$)

- ex. $(x^3-1)^{100}$: $300x^2(x^3-1)^{99}$
- ex. $\frac{1}{\sqrt[3]{x^2+x+1}}=(x^2+x+1)^{-1/3}$ (rewrite first): $-\frac13(x^2+x+1)^{-4/3}(2x+1)$
- ex. $\left(\frac{t-2}{2t+1}\right)^9$ (Power, Chain, Quotient Rules): $\frac{45(t-2)^8}{(2t+1)^{10}}$
- ex. $(2x+1)^5(x^3-x+1)^4$: Product Rule **before** Chain Rule, common factor $2(2x+1)^4(x^3-x+1)^3$ ⇒ $2(2x+1)^4(x^3-x+1)^3(17x^3+6x^2-9x+3)$

Longer chain: $y=f(u)$, $u=g(x)$, $x=h(t)$ ⇒ Chain Rule twice:

$$\frac{dy}{dt}=\frac{dy}{dx}\,\frac{dx}{dt}=\frac{dy}{du}\,\frac{du}{dx}\,\frac{dx}{dt}$$

- ex. $\sin(\cos(\tan x))$: $-\cos(\cos(\tan x))\sin(\tan x)\sec^2x$
- ex. $\sqrt{\sec x^3}$ (outer $\sqrt{\ }$, middle $\sec$, inner cube): $\frac{3x^2\sec x^3\tan x^3}{2\sqrt{\sec x^3}}$

### How to Prove the Chain Rule

$y=f(x)$, $x$ changes from $a$ to $a+\Delta x$: $\Delta y=f(a+\Delta x)-f(a)$, $\lim_{\Delta x\to0}\frac{\Delta y}{\Delta x}=f'(a)$

$\varepsilon=\frac{\Delta y}{\Delta x}-f'(a)$ ⇒ $\lim_{\Delta x\to0}\varepsilon=f'(a)-f'(a)=0$; define $\varepsilon=0$ when $\Delta x=0$ ⇒ $\varepsilon$ is a continuous function of $\Delta x$

Equation 5 (for a differentiable function $f$):

$$\Delta y=f'(a)\,\Delta x+\varepsilon\,\Delta x\qquad\text{where}\quad\varepsilon\to0\ \text{as}\ \Delta x\to0$$

Proof: $u=g(x)$ differentiable at $a$, $y=f(u)$ differentiable at $b=g(a)$

$$\begin{aligned}&(6)\quad \Delta u=g'(a)\,\Delta x+\varepsilon_1\Delta x=[g'(a)+\varepsilon_1]\,\Delta x,\quad \varepsilon_1\to0\ \text{as}\ \Delta x\to0\\&(7)\quad \Delta y=f'(b)\,\Delta u+\varepsilon_2\Delta u=[f'(b)+\varepsilon_2]\,\Delta u,\quad \varepsilon_2\to0\ \text{as}\ \Delta u\to0\end{aligned}$$

(6) into (7): $\Delta y=[f'(b)+\varepsilon_2][g'(a)+\varepsilon_1]\,\Delta x$ ⇒ $\frac{\Delta y}{\Delta x}=[f'(b)+\varepsilon_2][g'(a)+\varepsilon_1]$

$\Delta x\to0$ ⇒ $\Delta u\to0$ (by 6) ⇒ $\varepsilon_1\to0$, $\varepsilon_2\to0$

$$\frac{dy}{dx}=\lim_{\Delta x\to0}\frac{\Delta y}{\Delta x}=\lim_{\Delta x\to0}[f'(b)+\varepsilon_2][g'(a)+\varepsilon_1]=f'(b)\,g'(a)=f'(g(a))\,g'(a)$$

> Equation 5 never divides by $\Delta u$ ⇒ the proof works even when $\Delta u=0$

## Part 2 題型

課本習題 88 題全部分類了。★ 的題目在 Obsidian 的 [[CAL1 HW 2.5 Solutions]] 有完整解答（作業 22 題，加上網路上找到的 5 題考古題 WEB 2.5.1–2.5.5）。考古題用了中原大學微積分（上）5 份有考到連鎖律的期中考（109-1、110-1、111-1、113-1 A 群、114-1 A 群；113-1 B 群那份範圍只到 product/quotient rule，沒有算進去），和政大 93 年轉學考的一題證明。

| # | 題型 | 怎麼認 | 做法 | 課本題數 | 5 份考古題裡有幾份 |
|---|---|---|---|---|---|
| 1 | 寫成 $f(g(x))$ | "Write the composite function in the form $f(g(x))$" | 找 inner $u=g(x)$、outer $y=f(u)$，再 $\frac{dy}{du}\frac{du}{dx}$ | 6 | 0 |
| 2 | 次方、根號包住代數式 | $(\cdots)^n$、$\sqrt{\cdots}$、$\frac{1}{(\cdots)^n}$ | 先改寫成 $[g(x)]^n$，$n[g(x)]^{n-1}g'(x)$ | 11 | 4 |
| 3 | 乘積、商再加連鎖律 | 兩個因式相乘或相除，各自是合成函數 | Product/Quotient Rule 在外面，Chain Rule 在每一個因式裡面；最後提公因式 | 11 | 1 |
| 4 | 三角函數一層包一層 | $\sin(\cos(\tan x))$、$\cos\sqrt{\cdots}$、$\sec^4(\cdots)$ | 由外往內，一層一個因式，裡面照抄 | 20 | 5 |
| 5 | 二階、$n$ 階導數 | "Find $y'$ and $y''$"、$D^{103}$、$\frac{d^{35}y}{dx^{35}}$ | 算前 4 階找週期，再用 $n$ 除以 $4$ 的餘數 | 6 | 3 |
| 6 | 切線、水平切線、垂直條件 | "tangent line"、"horizontal"、"perpendicular" | 求 $f'(a)$；水平 ⇔ $f'=0$；垂直 ⇔ 斜率相乘 $-1$ | 8 | 2 |
| 7 | 微分後用圖檢查 | "Check ... by comparing the graphs"、"graph $f'$" | 算 $f'$，看 $f$ 的水平切線、上升下降是否對得上 | 2 | 0 |
| 8 | 由數值、表格、圖求合成函數的導數 | 給 $f(a)$、$f'(a)$ 的數字、表格或折線圖 | $F'(a)=f'(g(a))\,g'(a)$：先算內層的值，再查外層的導數 | 10 | 3 |
| 9 | 抽象 $f$ 的導數式子 | "Find expressions"、"in terms of $g$, $g'$, $g''$" | 一樣由外往內，只是不代數字 | 2 | 0 |
| 10 | 應用：速度、變化率 | 位移 $s(t)$、亮度 $B(t)$、日照 $L(t)$、氣球 $V(t)$ | 對 $t$ 微分；三角函數裡的係數會跑出來 | 6 | 0 |
| 11 | 證明 | "Prove"、"Show that" | 對恆等式兩邊微分；Chain Rule 的證明用 Equation 5 | 6 | 0（政大轉學考 1） |

題數加起來是 $6+11+11+20+6+8+2+10+2+6+6=88$。

**判斷順序：**
- 有具體的函數式，要 $y'$：先看最外層
  - 乘積或商：第 3 類
  - 次方或根號，裡面是代數式：第 2 類
  - 三角函數：第 4 類（裡面有乘積時，剝到那一層再用 Product Rule）
- 要 $y''$ 或很高階的導數：第 5 類
- 給一個點要切線，或要找水平切線：第 6 類
- 沒有函數式，只有 $f$、$g$ 的數值、表格或圖：第 8 類；要的是式子：第 9 類
- 文字題（速度、變化率）：第 10 類；"Prove"、"Show"：第 11 類

## 1. 寫成 f(g(x))

#1–6。

| 題目 | 出處 | 答案 |
|---|---|---|
| $y=(5-x^4)^3$ | #1 | $u=5-x^4$，$y=u^3$；$-12x^3(5-x^4)^2$ |
| $y=\sin(\cos x)$ | #3 | $u=\cos x$，$y=\sin u$；$-\sin x\cos(\cos x)$ |
| $y=\sin\sqrt x$ | #6 | $u=\sqrt x$，$y=\sin u$；$\frac{\cos\sqrt x}{2\sqrt x}$ |

- 最後的答案要換回 $x$，不能留 $u$。

## 2. 次方、根號包住代數式

$\frac{d}{dx}[g(x)]^n=n[g(x)]^{n-1}g'(x)$，$n$ 可以是任何實數。#7–12、23–25、40、44。

| 題目 | 出處 | 答案 |
|---|---|---|
| $(x^3-1)^{100}$ | 課本 Ex 3；中原 113-1 A | $300x^2(x^3-1)^{99}$ |
| $\frac{1}{\sqrt[3]{x^2+x+1}}$ | 課本 Ex 4 | $-\frac13(x^2+x+1)^{-4/3}(2x+1)$ |
| $\left(\frac{t-2}{2t+1}\right)^9$ | 課本 Ex 5 | $\frac{45(t-2)^8}{(2t+1)^{10}}$ |
| $(2x^3-5x^2+4)^5$ | #7 ★ | $10x(3x-5)(2x^3-5x^2+4)^4$ |
| $\frac{1}{(2t+1)^2}$ | #11 ★ | $-\frac{4}{(2t+1)^3}$ |
| $\left(\frac{u^3-1}{u^3+1}\right)^8$ | #25 ★ | $\frac{48u^2(u^3-1)^7}{(u^3+1)^9}$ |
| $(3x-2x^2)^{30}$ | 中原 110-1 | $30(3x-2x^2)^{29}(3-4x)$ |
| $\left(\frac{x+5}{x^2+2}\right)^2$ | 中原 111-1 | $\frac{2(x+5)(-x^2-10x+2)}{(x^2+2)^3}$ |
| $\sqrt{x+\sqrt{x+\sqrt x}}$ | #44；中原 109-1 | $\frac{1}{2\sqrt{x+\sqrt{x+\sqrt x}}}\left[1+\frac{1}{2\sqrt{x+\sqrt x}}\left(1+\frac{1}{2\sqrt x}\right)\right]$ |

- 最常漏的是最後乘上 $g'(x)$：只寫 $n[g(x)]^{n-1}$ 是 Power Rule，不是 Chain Rule。
- 分母是次方時先改成負次方（Ex 4、#11），比 Quotient Rule 快。
- 裡面是分式時，外面 Power Rule、裡面 Quotient Rule（Ex 5、#25）；分子常有公因式可以提。

## 3. 乘積、商再加連鎖律

Product/Quotient Rule 在外面，每個因式自己用 Chain Rule；最後提最低次方的公因式。#17–22、27、28、31、34、35。

| 題目 | 出處 | 答案 |
|---|---|---|
| $(2x+1)^5(x^3-x+1)^4$ | 課本 Ex 6 | $2(2x+1)^4(x^3-x+1)^3(17x^3+6x^2-9x+3)$ |
| $v\sqrt[3]{1+v^2}$ | #17 ★ | $\frac{3+5v^2}{3(1+v^2)^{2/3}}$ |
| $(4x+5)^3(x^2-2x+5)^4$ | #19 ★ | $4(4x+5)^2(x^2-2x+5)^3(11x^2-4x+5)$ |
| $(t+1)^{2/3}(2t^2-1)^3$ | #21 ★ | $\frac{2(2t^2-1)^2(20t^2+18t-1)}{3(t+1)^{1/3}}$ |
| $\frac{\cos x}{\sqrt{1+\sin x}}$ | #31 ★ | $-\frac12\sqrt{1+\sin x}$ |
| $t\sin\pi t$ | #18 | $\sin\pi t+\pi t\cos\pi t$ |
| $x\sin\frac1x$ | #34 | $\sin\frac1x-\frac1x\cos\frac1x$ |

- 公因式取每個底數比較低的次方：$(t+1)^{2/3}=(t+1)^{-1/3}(t+1)$。
- #31 用 $\cos^2x=1-\sin^2x$ 後幾乎全部約掉；化簡不出來時先檢查這個恆等式。
- 中原 111-1 I-8(a) 印成 "$\sqrt{4t+6}\csc(3t)$"，看不出是乘積還是相加；表格的 1 份是它。

## 4. 三角函數一層包一層

由外往內，每一層一個因式，裡面照抄。#13–16、26、29、30、32、33、36–39、41–43、45–48。

| 題目 | 出處 | 答案 |
|---|---|---|
| $\sin(x^2)$、$\sin^2x$ | 課本 Ex 2 | $2x\cos(x^2)$；$2\sin x\cos x$ |
| $\sin(\cos(\tan x))$ | 課本 Ex 7；中原 109-1 | $-\cos(\cos(\tan x))\sin(\tan x)\sec^2x$ |
| $\sqrt{\sec x^3}$ | 課本 Ex 8 | $\frac{3x^2\sec x^3\tan x^3}{2\sqrt{\sec x^3}}$ |
| $\cos(\theta^2)$ | #15 ★ | $-2\theta\sin(\theta^2)$ |
| $\cos(\sec4x)$ | #29 ★ | $-4\sin(\sec4x)\sec4x\tan4x$ |
| $\tan\sqrt{1+t^2}$ | #37 ★ | $\frac{t\sec^2\sqrt{1+t^2}}{\sqrt{1+t^2}}$ |
| $\tan(\sec(\cos t))$ | #43 ★ | $-\sin t\sec^2(\sec(\cos t))\sec(\cos t)\tan(\cos t)$ |
| $\cos\sqrt{\sin(\tan\pi x)}$ | #47 ★ | $-\frac{\pi\cos(\tan\pi x)\sec^2(\pi x)\sin\sqrt{\sin(\tan\pi x)}}{2\sqrt{\sin(\tan\pi x)}}$ |
| $\sin(\theta+\tan(\theta+\cos\theta))$ | #46；中原 114-1 A | $\cos(\theta+\tan(\theta+\cos\theta))\left[1+\sec^2(\theta+\cos\theta)(1-\sin\theta)\right]$ |
| $\tan^2(\sec^4(x^2+1))$ | 中原 114-1 A（WEB 2.5.2 ★） | $16x\tan(\sec^4(x^2+1))\sec^2(\sec^4(x^2+1))\sec^4(x^2+1)\tan(x^2+1)$ |
| $\cos(\sin(\tan x))$ | 中原 113-1 A | $-\sin(\sin(\tan x))\cos(\tan x)\sec^2x$ |
| $\tan(\sec(\sin x))$ | 中原 111-1 | $\sec^2(\sec(\sin x))\sec(\sin x)\tan(\sin x)\cos x$ |
| $\sec(\tan(\sin x))$ | 中原 114-1 A | $\sec(\tan(\sin x))\tan(\tan(\sin x))\sec^2(\sin x)\cos x$ |
| $\sin\sqrt{\cot(3\pi x)}$ | 中原 110-1 | $-\frac{3\pi\csc^2(3\pi x)\cos\sqrt{\cot(3\pi x)}}{2\sqrt{\cot(3\pi x)}}$ |
| $\sin^2\frac1x$ | 中原 113-1 A | $-\frac{1}{x^2}\sin\frac2x$ |

- 先數有幾層，答案就有幾個因式（#47 有 5 層；最後的 $\pi$ 最常漏）。
- $\sin(x^2)$ 和 $\sin^2x$ 的外層、內層相反（#15 和 #16 是同一組）。
- 中原 114-1 A 規定只寫答案必須完全正確；最後把數字乘一遍：$2\cdot4\cdot2x=16x$。
- 中原 113-1 A、114-1 A 每份都有 2–3 題這一類，5 份考古題全部都有。

## 5. 二階、n 階導數

$y''$：對 $y'$ 再微分一次（通常要再用 Product Rule）。很高階：算前 4 階找週期。#49–52、75、76。

| 題目 | 出處 | 答案 |
|---|---|---|
| $y=\cos(\sin3\theta)$，$y''$ | #49 | $y'=-3\cos3\theta\sin(\sin3\theta)$；$y''=9\sin3\theta\sin(\sin3\theta)-9\cos^23\theta\cos(\sin3\theta)$ |
| $D^{103}\cos2x$ | #75 ★ | $2^{103}\sin2x$ |
| $D^{35}\,x\sin\pi x$ | #76 | $-\pi^{35}x\cos\pi x-35\pi^{34}\sin\pi x$ |
| $y=x\sin x$，$\frac{d^{35}y}{dx^{35}}$ | 中原 113-1 A（WEB 2.5.5 ★） | $-35\sin x-x\cos x$ |
| $\cos x$ 的 30、98、101 階導數 | 中原 109-1、111-1、113-1 A | $-\cos x$、$-\cos x$、$-\sin x$ |

- 三角函數的導數週期是 4：用 $n$ 除以 $4$ 的餘數。
- 有 $\cos2x$、$\sin\pi x$ 時，每微分一次多乘一個 $2$ 或 $\pi$：係數是 $2^n$、$\pi^n$。
- 乘上 $x$ 時（$x\sin x$），前面的係數每次加 $1$：$1,2,3,\dots,n$。
- 找到規律後，先用算出來的前幾階驗證一次再套到第 $n$ 階。

## 6. 切線、水平切線、垂直條件

切線 $y-f(a)=f'(a)(x-a)$；水平切線 ⇔ $f'(x)=0$；和斜率 $m$ 的直線垂直 ⇔ 切線斜率 $-\frac1m$。#53–58、61、62。

| 題目 | 出處 | 答案 |
|---|---|---|
| $y=(3x-1)^{-6}$，$(0,1)$ | #53 ★ | $y=18x+1$ |
| $y=\sqrt{1+x^3}$，$(2,3)$ | #54 | $y=2x-1$ |
| $y=\sin(\sin x)$，$(\pi,0)$ | #55 ★ | $y=-x+\pi$ |
| $f(x)=2\sin x+\sin^2x$ 的水平切線 | #61 ★ | $\left(\frac\pi2+2n\pi,3\right)$、$\left(\frac{3\pi}2+2n\pi,-1\right)$ |
| $y=\sqrt{1+2x}$ 的切線垂直於 $6x+2y=1$ | #62 | $(4,3)$ |
| $y=\sqrt{x^2+8x}$ 在 $(1,3)$ 的切線 $y=b+ax$，求 $2a+b$ | 中原 110-1 | $a=\frac53$，$b=\frac43$，$2a+b=\frac{14}3$ |
| $f(x)=2\cos x+\sin2x$ 在 $(0,2\pi)$ 的水平切線 | 中原 111-1（WEB 2.5.4 ★） | $\left(\frac\pi6,\frac{3\sqrt3}2\right)$、$\left(\frac{5\pi}6,-\frac{3\sqrt3}2\right)$、$\left(\frac{3\pi}2,0\right)$ |

- 負次方代負數要小心：#53 的 $(-1)^{-7}=-1$，斜率是 $+18$。
- "Find all points" 要寫成點（兩個座標），沒有限制區間時要加 $2n\pi$。
- $f'(x)=0$ 有 $\sin2x$、$\cos2x$ 時，用倍角公式全部換成 $\sin x$ 或 $\cos x$，解二次方程式。

## 7. 微分後用圖檢查

#59、60。

| 題目 | 出處 | 答案 |
|---|---|---|
| $f(x)=x\sqrt{2-x^2}$ | #59 | $f'(x)=\frac{2-2x^2}{\sqrt{2-x^2}}$；$f$ 在 $x=\pm1$ 有水平切線 |
| $f(x)=\sin(x+\sin2x)$ | #60 | $f'(x)=\cos(x+\sin2x)(1+2\cos2x)$ |

- 考試不會叫你用電腦畫圖；這一類只要會算 $f'$。

## 8. 由數值、表格、圖求合成函數的導數

$F'(a)=f'(g(a))\,g'(a)$：先算內層的值 $g(a)$，再查外層在那個值的導數。#63–69、71、73、74。

| 題目 | 出處 | 答案 |
|---|---|---|
| $F=f\circ g$，給 5 個數值，求 $F'(5)$ | #63 ★ | $f'(-2)\cdot6=24$ |
| $h=\sqrt{4+3f}$，$f(1)=7$，$f'(1)=4$ | #64 | $h'(1)=\frac{3\cdot4}{2\sqrt{25}}=\frac65$ |
| 表格：$h=f\circ g$、$H=g\circ f$ 在 $1$ | #65 ★ | $30$、$36$ |
| 同一張表：$f\circ f$ 在 $2$、$g\circ g$ 在 $3$ | #66 | $20$、$63$ |
| 折線圖：$f\circ g$、$g\circ f$、$g\circ g$ 在 $1$ | #67 ★ | $\frac14$、$-2$、$-\frac12$ |
| $g=\sqrt f$，切線圖，求 $g'(3)$ | #69 | $\frac{-2/3}{2\sqrt2}=-\frac{\sqrt2}6$ |
| $r=f\circ g\circ h$ 在 $1$ | #71 | $6\cdot5\cdot4=120$ |
| $F(x)=f(3f(4f(x)))$，$f(0)=0$，$f'(0)=2$ | #73 ★ | $96$ |
| $F(x)=f(xf(xf(x)))$ 在 $1$ | #74 | $6\cdot33=198$ |
| $F(x)=f(2f(xf(x)))$，$f(0)=0$，$f'(0)=3$ | 中原 109-1（WEB 2.5.3 ★） | $0$ |
| $F=f\circ g$ 在 $3$；$h=\sqrt{2+2f(x)}$ 在 $1$ | 中原 113-1 A | $f'(5)\cdot2=4$；$\frac{2\cdot2}{2\sqrt{16}}=\frac12$ |
| $f=[g(x)]^3$，$g(5)=-3$，$g'(5)=6$ | 中原 111-1 | $3\cdot9\cdot6=162$ |

- $f'$ 要在 $g(a)$ 算，不是在 $a$：#63 故意多給 $f'(5)$。
- 圖的題目：先看要用的點是不是折線的轉角（corner），轉角的地方導數不存在（#67 這一版三個都存在）。
- 裡面有 $xf(x)$ 時要先用 Product Rule：在 $0$ 時 $f(0)+0\cdot f'(0)=0$，整題答案變 $0$（中原 109-1）。

## 9. 抽象 f 的導數式子

#70、72。

| 題目 | 出處 | 答案 |
|---|---|---|
| $F(x)=f(x^\alpha)$、$G(x)=[f(x)]^\alpha$ | #70 ★ | $\alpha x^{\alpha-1}f'(x^\alpha)$；$\alpha[f(x)]^{\alpha-1}f'(x)$ |
| $f(x)=xg(x^2)$，求 $f''$ | #72 | $f'=g(x^2)+2x^2g'(x^2)$；$f''=6xg'(x^2)+4x^3g''(x^2)$ |

- $g'(x^2)$ 再微分要再乘 $2x$：$\frac{d}{dx}g'(x^2)=2xg''(x^2)$。

## 10. 應用：速度、變化率

#77–82。

| 題目 | 出處 | 答案 |
|---|---|---|
| $s(t)=10+\frac14\sin(10\pi t)$ 的速度 | #77 | $\frac{5\pi}{2}\cos(10\pi t)$ cm/s |
| $s=A\cos(\omega t+\delta)$ | #78 | $v=-A\omega\sin(\omega t+\delta)$；$v=0$ 當 $\omega t+\delta=n\pi$ |
| $B(t)=4.0+0.35\sin\frac{2\pi t}{5.4}$ | #79 | $B'(t)=\frac{7\pi}{54}\cos\frac{2\pi t}{5.4}$；$B'(1)\approx0.16$ |
| $L(t)=12+2.8\sin\left[\frac{2\pi}{365}(t-80)\right]$ | #80 | $L'(80)\approx0.0482$ h/day（約 2.9 分鐘），$L'(141)\approx0.0240$ h/day（約 1.4 分鐘） |
| $a=v\frac{dv}{ds}$ | #81 | $\frac{dv}{dt}=\frac{dv}{ds}\frac{ds}{dt}$ |
| 氣球 $V(t)$、$r(t)$ | #82 | $\frac{dV}{dt}=4\pi r^2\frac{dr}{dt}$ |

- $\sin(kt)$ 微分會多乘 $k$：#77 的 $10\pi$ 和 $\frac14$ 相乘。
- 答案要帶單位。

## 11. 證明

#83–88。

| 題目 | 出處 | 答案 |
|---|---|---|
| 偶函數的導函數是奇函數，奇函數的導函數是偶函數 | #83 ★ | 對 $f(-x)=\pm f(x)$ 兩邊微分，$\frac{d}{dx}f(-x)=-f'(-x)$ |
| 用 Chain Rule 和 Product Rule 證明 Quotient Rule | #84 | $\frac fg=f\cdot g^{-1}$ |
| $\theta$ 用度數時 $\frac{d}{d\theta}\sin\theta=\frac{\pi}{180}\cos\theta$ | #85 | $\sin\theta^\circ=\sin\frac{\pi\theta}{180}$ |
| $\frac{d}{dx}\lvert x\rvert=\frac{x}{\lvert x\rvert}$ | #86 | $\lvert x\rvert=\sqrt{x^2}$ |
| $(f\circ g\circ h)'$、$(f\circ g)''$ | #87、88 | $f'(g(h(x)))g'(h(x))h'(x)$；$f''(g(x))[g'(x)]^2+f'(g(x))g''(x)$ |
| Prove the Chain Rule. | 政大 93 轉學考（WEB 2.5.1 ★） | 課本最後的證明：Equation 5、6、7 |

- #83 和 2.2 #61 是同一個敘述：2.2 用定義（$k=-h$），這裡一行就好。
- 證明 Chain Rule 不能直接寫 $\frac{\Delta y}{\Delta u}\cdot\frac{\Delta u}{\Delta x}$：$\Delta u$ 可能是 $0$。

## 外面的考古題

| 考古題 | 題目 | 類型 |
|---|---|---|
| 中原 109-1 期中 | I-2 $\sqrt{x+\sqrt{x+\sqrt x}}$；I-3 $\sin(\cos(\tan x))$；I-4 $f(2f(xf(x)))$；I-1 $\cos x$ 的 30 階 | 2、4、8、5 |
| 中原 110-1 期中 | I-1 $\sin\sqrt{\cot(3\pi x)}$；II-3 $(3x-2x^2)^{30}$；II-5 $\sqrt{x^2+8x}$ 的切線 | 4、2、6 |
| 中原 111-1 期中 | I-5 $5\cos^2(\pi t)$、$\left(\frac{x+5}{x^2+2}\right)^2$；I-7 水平切線；I-8(a)；II-1 $\cos x$ 的 98 階；II-2 $[g(x)]^3$；II-3 $\tan(\sec(\sin x))$ | 4、2、6、3、5、8、4 |
| 中原 113-1 A 期中 | I-2 $\cos x$ 的 101 階；I-3 $\cos(\sin(\tan x))$；II-2 $(x^3-1)^{100}$、$\sin^2\frac1x$；II-5 數值；II-8 $x\sin x$ 的 35 階 | 5、4、2、4、8、5 |
| 中原 114-1 A 期中 | I-3 $\sec(\tan(\sin x))$；II-3 $\tan^2(\sec^4(x^2+1))$；II-4 $\sin(x+\tan(x+\cos x))$ | 4、4、4 |
| 政大 93 轉學考 | 6. Prove the Chain Rule. | 11 |

## 常一起考的

- **2.6 隱函數微分：** 中原每一份都有，$\sin(x+y)$、$y^2$、$\cos2y$ 對 $x$ 微分都是 Chain Rule（要乘 $y'$）。
- **2.4 三角函數的導數：** $\sec x$、$\csc x$、$\cot x$ 的導數要背熟，第 4 類全部要用；同一份也常考 $\lim_{x\to0}\frac{\sin x}{x}$ 類的極限。
- **2.3 Product、Quotient Rule：** 第 3 類的外層。
- **2.9 線性近似、3.1 極值：** $\sqrt{x+8}$ 的 linearization、$(t^2-4)^3$ 的絕對極值，第一步都是用 Chain Rule 微分。

## Sources

- [中原大學 微積分（上）109 學年度上學期期中考（檔名 10912）](https://mathwww.cycu.edu.tw/wp-content/uploads/10912題目.pdf)
- [中原大學 微積分（上）110 學年度上學期期中考（檔名 11012）](https://mathwww.cycu.edu.tw/wp-content/uploads/11012題目.pdf)
- [中原大學 微積分（上）111 學年度上學期期中考（檔名 11112）](https://mathwww.cycu.edu.tw/wp-content/uploads/11112題目.pdf)
- [中原大學 微積分（上）A 群 113 學年度上學期期中考（檔名 11312-A）](https://mathwww.cycu.edu.tw/wp-content/uploads/11312-A-題目.pdf)
- [中原大學 微積分（上）B 群 113 學年度上學期期中考（檔名 11312-B，沒有連鎖律）](https://mathwww.cycu.edu.tw/wp-content/uploads/11312-B-題目.pdf)
- [中原大學 微積分（上）A 群 114 學年度上學期期中考（檔名 11412）](https://mathwww.cycu.edu.tw/wp-content/uploads/11412題目.pdf)
- [政大 93 年轉學考 應數系 微積分（一）第 6 題（阿摩）](https://api.yamol.tw/item_essay-6.+Prove+the+Chain+Rule.-520951.htm)
