%% unit-summary v1 · Stewart, Calculus §2.1 pp. 108–119 (scan) · 2026-10-05 %%

## 2.1 Derivatives and Rates of Change

### Tangents

secant line $PQ$, $P(a,f(a))$, $Q(x,f(x))$, $x\neq a$: $m_{PQ}=\frac{f(x)-f(a)}{x-a}$

Definition 1: The tangent line to the curve $y=f(x)$ at the point $P(a,f(a))$ is the line through $P$ with slope

$$m=\lim_{x\to a}\frac{f(x)-f(a)}{x-a}$$

provided that this limit exists.

Equation 2 ($h=x-a$):

$$m=\lim_{h\to0}\frac{f(a+h)-f(a)}{h}$$

> - tangent line = limiting position of the secant line $PQ$ as $Q\to P$
> - $x\to a$ ⇔ $h\to0$ ($h>0$: $Q$ to the right of $P$; $h<0$: to the left)
> - slope of the curve at $P$ = slope of the tangent line at $P$ (zoom in ⇒ curve ≈ its tangent line)

ex. $y=x^2$ at $(1,1)$: $m=\lim_{x\to1}\frac{x^2-1}{x-1}=2$ ⇒ $y=2x-1$

ex. $y=\frac{3}{x}$ at $(3,1)$: $m=\lim_{h\to0}\frac{\frac{3}{3+h}-1}{h}=-\frac{1}{3}$ ⇒ $x+3y-6=0$

### Velocities

position function $s=f(t)$ ($s$ = displacement from the origin at time $t$)

$$\text{average velocity}=\frac{\text{displacement}}{\text{time}}=\frac{f(a+h)-f(a)}{h}\quad(\text{over } [a,a+h])$$

Definition 3: The instantaneous velocity of an object with position function $f(t)$ at time $t=a$ is

$$v(a)=\lim_{h\to0}\frac{f(a+h)-f(a)}{h}$$

provided that this limit exists.

> - average velocity = slope of the secant line $PQ$
> - velocity at $t=a$ = slope of the tangent line at $P$

ex. $s=4.9t^2$: $v(a)=9.8a$ ⇒ $v(5)=49$ m/s; hits the ground when $4.9t^2=450$, $t\approx9.6$ s, $v\approx94$ m/s

### Derivatives

Definition 4: The derivative of a function $f$ at a number $a$, denoted by $f'(a)$, is

$$f'(a)=\lim_{h\to0}\frac{f(a+h)-f(a)}{h}$$

if this limit exists.

Equation 5 ($x=a+h$):

$$f'(a)=\lim_{x\to a}\frac{f(x)-f(a)}{x-a}$$

> - Definition 4 ⇔ Equation 5 ($h\to0$ ⇔ $x\to a$); Definition 4 often leads to simpler computations
> - $f'(a)$ is a **number**; it needs the limit to **exist**

The tangent line to $y=f(x)$ at $(a,f(a))$ is the line through $(a,f(a))$ whose slope is equal to $f'(a)$:

$$y-f(a)=f'(a)(x-a)$$

ex. $f(x)=x^2-8x+9$: $f'(a)=2a-8$, $f'(2)=-4$; tangent at $(3,-6)$: $f'(3)=-2$ ⇒ $y=-2x$

ex. $f(x)=\frac{1}{\sqrt x}$ ($a>0$): $f'(a)=-\frac{1}{2a^{3/2}}$

### Rates of Change

$y=f(x)$, $x$ changes from $x_1$ to $x_2$: $\Delta x=x_2-x_1$ (increment of $x$), $\Delta y=f(x_2)-f(x_1)$

average rate of change of $y$ with respect to $x$ over $[x_1,x_2]$ (difference quotient):

$$\frac{\Delta y}{\Delta x}=\frac{f(x_2)-f(x_1)}{x_2-x_1}$$

Equation 6:

$$\text{instantaneous rate of change}=\lim_{\Delta x\to0}\frac{\Delta y}{\Delta x}=\lim_{x_2\to x_1}\frac{f(x_2)-f(x_1)}{x_2-x_1}=f'(x_1)$$

The derivative $f'(a)$ is the instantaneous rate of change of $y=f(x)$ with respect to $x$ when $x=a$.

> - average rate of change = $m_{PQ}$; instantaneous rate of change = slope of the tangent at $P$
> - $f'(a)$ = slope of the tangent line = instantaneous rate of change = velocity (if $s=f(t)$)
> - $f'(a)$ large ⇒ curve steep, $y$ changes rapidly; $f'(a)$ small ⇒ curve flat, $y$ changes slowly
> - speed = $\lvert f'(a)\rvert$ (velocity has a sign, speed does not)
> - units of $f'(x)$ = units of $y$ per unit of $x$ (the units of $\frac{\Delta y}{\Delta x}$)

ex. cost $C=f(x)$ dollars for $x$ meters: $f'(x)$ = marginal cost, dollars per meter; $f'(1000)=9$ ⇒ the 1000th (or 1001st) meter costs about \$9

ex. table $D(t)$: $D'(2008)$ between $775.93$ and $1433.23$ ⇒ average, $D'(2008)\approx1105$ billion dollars per year

## Part 2 題型

課本習題 60 題全部分類了。考古題這次找到東華大學 92、93 學年期中考、UBC 的期中考範例和南臺 OCW 講義；中原大學的小考題目這次連不上，沒有用到。

| # | 題型 | 怎麼認 | 做法 | 課本與考古題 |
|---|---|---|---|---|
| 1 | 切線方程式 | 給曲線和一個點，求 tangent line | 先求斜率 $m=f'(a)$，再代 $y-f(a)=f'(a)(x-a)$ | Ex 1、2、6；#1、3–10、29–32；南臺講義 |
| 2 | 用定義求 $f'(a)$ | "Use Definition 4 / Equation 5"、"Find $f'(a)$" | 代定義，消掉分母的 $h$（或 $x-a$）：展開、通分、有理化 | Ex 4、5；#19–26；UBC 期中 |
| 3 | 速度與速率 | position function $s=f(t)$，問 velocity、speed | $v(a)=f'(a)$，speed $=\lvert v(a)\rvert$ | Ex 3；#11–14、35、36 |
| 4 | 切線、$f(a)$、$f'(a)$ 互換 | 沒給函數式，只給切線或 $f(a)$、$f'(a)$ 的值 | 切點在切線上 ⇒ $f(a)$；切線斜率 ⇒ $f'(a)$ | #27、28、33、34；UBC 期中 |
| 5 | 認出極限是哪個導數 | "Each limit represents the derivative of some function $f$ at some number $a$" | 對照 Definition 4 或 Equation 5，讀出 $f$ 和 $a$ | #43–48 |
| 6 | 圖形題 | 給圖比較 $f'$ 大小，或給條件畫圖 | $f'(a)$ = 切線斜率：看正負、看陡不陡 | #2、15–18、37–42 |
| 7 | 變化率：平均、瞬時、意義與單位 | rate of change、cost、表格、"meaning"、"units" | 平均 = $\frac{\Delta y}{\Delta x}$；瞬時 = $f'(a)$；表格用兩側平均 | Ex 7、8；#49–56、60 |
| 8 | $f'(0)$ 是否存在 | 分段函數，"Determine whether $f'(0)$ exists" | 一定用定義；極限不存在或用 Squeeze Theorem | #57–59；東華 92、93 期中；UBC 期中 |

**判斷順序：**
- 有函數式、要算數字：先看問什麼。
  - 切線：第 1 類
  - $f'(a)$：第 2 類
  - velocity、speed：第 3 類
  - rate of change：第 7 類
- 沒有函數式：
  - 只有切線或幾個值：第 4 類
  - 只有一個極限：第 5 類
  - 只有圖或表格：第 6、7 類
- 分段函數、在分段點：第 8 類。

## 1. 切線方程式

先用 Definition 1 或 Equation 2 求斜率 $m$，再用 point-slope form $y-f(a)=f'(a)(x-a)$。

| 題目 | 出處 | 答案 |
|---|---|---|
| $y=x^2$，$(1,1)$ | 課本 Ex 1 | $m=2$，$y=2x-1$ |
| $y=\frac{3}{x}$，$(3,1)$ | 課本 Ex 2 | $m=-\frac{1}{3}$，$x+3y-6=0$ |
| $y=x^2+3x$，$(-1,-2)$ | #3 | $m=1$，$y=x-1$ |
| $y=x^3+1$，$(1,2)$ | #4 | $m=3$，$y=3x-1$ |
| $y=2x^2-5x+1$，$(3,4)$ | #5（作業） | $m=7$，$y=7x-17$ |
| $y=x^2-2x^3$，$(1,-1)$ | #6 | $m=-4$，$y=-4x+3$ |
| $y=\frac{x+2}{x-3}$，$(2,-4)$ | #7（作業） | $m=-5$，$y=-5x+6$ |
| $y=\sqrt{1-3x}$，$(-1,2)$ | #8 | $m=-\frac{3}{4}$，$y=-\frac{3}{4}x+\frac{5}{4}$ |
| $y=3+4x^2-2x^3$，$x=a$；$(1,5)$、$(2,3)$ | #9 | $m=8a-6a^2$；$y=2x+3$、$y=-8x+19$ |
| $y=2\sqrt x$，$x=a$；$(1,2)$、$(9,6)$ | #10 | $m=\frac{1}{\sqrt a}$；$y=x+1$、$y=\frac{1}{3}x+3$ |
| $y=3x^2-x^3$，$(1,2)$ | #29（作業） | $f'(1)=3$，$y=3x-1$ |
| $y=x^4-2$，$(1,-1)$ | #30 | $g'(1)=4$，$y=4x-5$ |
| $y=\frac{5x}{1+x^2}$，$(2,2)$ | #31 | $F'(2)=-\frac{3}{5}$，$y=-\frac{3}{5}x+\frac{16}{5}$ |
| $y=4x^2-x^3$，$(2,8)$、$(3,9)$ | #32 | $G'(a)=8a-3a^2$；$y=4x$、$y=-3x+18$ |
| $f(x)=x^2$，$(2,4)$ | 南臺講義 | $y=4x-4$ |

- 題目要兩個以上的點（#9、10、32）：先算一般的 $a$，再代數字。
- 分子的常數項一定會消掉；沒消掉就是 $f(a)$ 算錯。
- 答案要寫成直線方程式，只寫斜率不算做完。

## 2. 用定義求 f'(a)

代 $f'(a)=\lim_{h\to0}\frac{f(a+h)-f(a)}{h}$ 或 $\lim_{x\to a}\frac{f(x)-f(a)}{x-a}$，把分母的 $h$（或 $x-a$）消掉。

| $f$ 的形式 | 消掉 $h$ 的方法 | 題目 |
|---|---|---|
| 多項式 | 展開，$h$ 提出來 | Ex 4、#20、23、24、29、30 |
| 分式 | 通分 | Ex 2、#21、25、26、31 |
| 根號 | 乘共軛（有理化） | #8、10、19 |
| 根號在分母 | 先通分，再有理化 | Ex 5、#22；UBC 期中 |

| 題目 | 出處 | 答案 |
|---|---|---|
| $f(x)=x^2-8x+9$，$a=2$、一般的 $a$ | 課本 Ex 4 | $-4$；$2a-8$ |
| $f(x)=\frac{1}{\sqrt x}$ | 課本 Ex 5；UBC 期中 | $-\frac{1}{2a^{3/2}}$ |
| $f(x)=\sqrt{4x+1}$，$a=6$ | #19 | $\frac{2}{5}$ |
| $f(x)=5x^4$，$a=-1$ | #20 | $-20$ |
| $f(x)=\frac{x^2}{x+6}$，$a=3$ | #21（作業） | $\frac{5}{9}$ |
| $f(x)=\frac{1}{\sqrt{2x+2}}$，$a=1$ | #22 | $-\frac{1}{8}$ |
| $f(x)=2x^2-5x+3$ | #23（作業） | $4a-5$ |
| $f(t)=t^3-3t$ | #24 | $3a^2-3$ |
| $f(t)=\frac{1}{t^2+1}$ | #25（作業） | $-\frac{2a}{(a^2+1)^2}$ |
| $f(x)=\frac{x}{1-4x}$ | #26 | $\frac{1}{(1-4a)^2}$ |
| $f(x)=x^2+3x+1$，$f'(2)$、$f'(x)$ | 南臺講義 | $7$；$2x+3$ |

- 題目指定 Definition 4（$h\to0$）或 Equation 5（$x\to a$）時要照做（#19–22）。
- $a$ 是固定的數，只有 $h$ 在動。
- 這一節還沒有微分公式，考試寫「用定義」就不能直接寫公式的結果。

## 3. 速度與速率

$v(a)=f'(a)$，speed $=\lvert v(a)\rvert$。問「何時落地」就先解 $s$ 的方程式，再代進 $v$。

| 題目 | 出處 | 答案 |
|---|---|---|
| $s=4.9t^2$，450 m 高 | 課本 Ex 3 | $v(a)=9.8a$；$v(5)=49$ m/s；落地 $t\approx9.6$ s，$v\approx94$ m/s |
| $d(t)=4.9t^2$，30 m 高 | #11 | $t\approx2.5$ s；$v\approx24.2$ m/s |
| $H=10t-1.86t^2$ | #12 | $v(1)=6.28$；$v(a)=10-3.72a$；$t\approx5.4$ s；$v=-10$ m/s |
| $s=\frac{1}{t^2}$ | #13 | $v(a)=-\frac{2}{a^3}$；$-2$、$-\frac{1}{4}$、$-\frac{2}{27}$ m/s |
| $s=\frac{1}{2}t^2-6t+23$ | #14 | 平均：$0$、$1$、$3$、$4$ m/s；$v(8)=2$ m/s |
| $f(t)=80t-6t^2$，$t=4$ | #35（作業） | velocity $32$ m/s，speed $32$ m/s |
| $f(t)=10+\frac{45}{t+1}$，$t=4$ | #36 | velocity $-\frac{9}{5}$ m/s，speed $\frac{9}{5}$ m/s |

- velocity 有正負，speed 沒有：#36 是 $-\frac{9}{5}$ 和 $\frac{9}{5}$，#12(d) 是 $-10$ m/s。
- 要寫單位。
- #14 的平均速度在 $[4,8]$ 是 $0$，不代表沒有動。

## 4. 切線、f(a)、f'(a) 互換

切線通過切點 $(a,f(a))$，斜率是 $f'(a)$。

| 題目 | 出處 | 答案 |
|---|---|---|
| $B(6)=0$，$B'(6)=-\frac{1}{2}$，求切線 | #27（作業） | $y=-\frac{1}{2}x+3$ |
| $g(5)=-3$，$g'(5)=4$，求切線 | #28 | $y=4x-23$ |
| $a=2$ 的切線是 $y=4x-5$ | #33（作業） | $f(2)=3$，$f'(2)=4$ |
| 在 $(4,3)$ 的切線通過 $(0,2)$ | #34 | $f(4)=3$，$f'(4)=\frac{1}{4}$ |
| 寫出 $y=f(x)$ 在 $x=a$ 的切線方程式 | UBC 期中 | $y-f(a)=f'(a)(x-a)$ |

- #34 的 $(0,2)$ 在切線上，不在曲線上，所以和 $f(0)$ 無關。

## 5. 認出極限是哪個導數

| 題目 | 出處 | 答案 |
|---|---|---|
| $\lim_{h\to0}\frac{\sqrt{9+h}-3}{h}$ | #43（作業） | $f(x)=\sqrt x$，$a=9$ |
| $\lim_{h\to0}\frac{2^{3+h}-8}{h}$ | #44 | $f(x)=2^x$，$a=3$ |
| $\lim_{x\to2}\frac{x^6-64}{x-2}$ | #45（作業） | $f(x)=x^6$，$a=2$ |
| $\lim_{x\to1/4}\frac{\frac{1}{x}-4}{x-\frac{1}{4}}$ | #46 | $f(x)=\frac{1}{x}$，$a=\frac{1}{4}$ |
| $\lim_{h\to0}\frac{\tan(\frac{\pi}{4}+h)-1}{h}$ | #47（作業） | $f(x)=\tan x$，$a=\frac{\pi}{4}$ |
| $\lim_{\theta\to\pi/6}\frac{\sin\theta-\frac{1}{2}}{\theta-\frac{\pi}{6}}$ | #48 | $f(\theta)=\sin\theta$，$a=\frac{\pi}{6}$ |

- $h\to0$ 的是 Definition 4；$x\to a$ 的是 Equation 5。
- 被減掉的那個數要等於 $f(a)$，拿來驗算：$\sqrt9=3$、$2^6=64$、$\tan\frac{\pi}{4}=1$。
- 答案不唯一：#43 也可以寫 $f(x)=\sqrt{9+x}$，$a=0$。
- 只問 $f$ 和 $a$，不用算極限值。

## 6. 圖形題

$f'(a)$ 是切線斜率：上升為正、下降為負、水平為 $0$，越陡絕對值越大。

| 題目 | 出處 | 答案 |
|---|---|---|
| 把 $0$、$g'(-2)$、$g'(0)$、$g'(2)$、$g'(4)$ 由小到大排 | #17（作業） | $g'(0)<0<g'(4)<g'(2)<g'(-2)$ |
| 畫 $f$：$f(0)=0$、$f'(0)=3$、$f'(1)=0$、$f'(2)=-1$ | #39（作業） | 先畫三段切線，再連成曲線 |
| 畫 $g$：在 $(-5,5)$ 連續，含單邊極限的條件 | #41（作業） | 漸近線 $x=-5$，右端 $(5,3)$ 是空心點 |

- #15、16（位置圖讀速度）、#18（圖上的平均變化率）、#37、38、40、42 是同一類。
- 畫圖題答案不唯一，但每個條件都要畫得出來。
- 不在定義域裡的端點要畫空心點（#41 的 $x=5$）。

## 7. 變化率：平均、瞬時、意義與單位

| 題目 | 出處 | 答案 |
|---|---|---|
| $C(x)=5000+10x+0.05x^2$ | #49（作業） | 平均：$20.25$、$20.05$ dollars/unit；$C'(100)=20$ dollars/unit |
| $f'(x)$ 的意義和單位（$C=f(x)$ dollars，$x$ meters） | 課本 Ex 7 | 生產成本對產量的變化率（marginal cost），dollars per meter |
| 由圖估 $S'(16)$ | #53（作業） | 約 $-0.25$ (mg/L)/°C |
| 由表估 $D'(2008)$ | 課本 Ex 8 | $\frac{775.93+1433.23}{2}\approx1105$ billion dollars per year |
| 由表估 $C'(2)$ | #55 | 平均：$-0.015$、$-0.012$、$-0.012$、$-0.011$；$C'(2)\approx-0.012$ (g/dL)/h |
| symmetric difference quotient，$f(x)=x^3-2x^2+2$，$a=1$，$d=0.4$ | #60(c) | $-0.84$ |

- 單位是「$y$ 的單位 / $x$ 的單位」。
- 「解釋意義」要寫成一句完整的話：在什麼時候、什麼量、以多少的速率增加或減少。
- 表格題用左右兩個最短區間的平均變化率再取平均。
- #50–52、54、56 是同一類（意義、單位、正負）。

## 8. f'(0) 是否存在

分段點一定用定義：$f'(0)=\lim_{h\to0}\frac{f(h)-f(0)}{h}$。

| 題目 | 出處 | 答案 |
|---|---|---|
| $f(x)=x\sin\frac{1}{x}$（$x\neq0$），$f(0)=0$ | #57（作業）；東華 92、93 期中 | $\lim_{h\to0}\sin\frac{1}{h}$ 不存在 ⇒ $f'(0)$ 不存在 |
| $f(x)=x^2\sin\frac{1}{x}$（$x\neq0$），$f(0)=0$ | #58（作業）；東華 92、93 期中 | Squeeze Theorem ⇒ $f'(0)=0$ |
| $f(x)=x\cos\frac{1}{x}$（$x\neq0$），$f(0)=0$ | UBC 期中 | $\lim_{h\to0}\cos\frac{1}{h}$ 不存在 ⇒ 不可微 |
| $f(x)=\lvert x\rvert$，$f'(0)$ | 南臺講義 | 左極限 $-1$、右極限 $1$ ⇒ 不存在 |

- $f(0)$ 用第二行的值，$f(h)$ 用第一行的式子（$h\neq0$）。
- Squeeze 的上下界要寫 $\pm\lvert h\rvert$，不是 $\pm h$。
- 東華的題目還要先證 $f$ 在 $0$ 連續（也是 Squeeze Theorem）：連續 ⇏ 可微。
- #59 用圖形放大來猜 $f'(0)$，第一次的猜測會錯。

## 常一起考的

- **1.6 極限技巧：** 展開、通分、有理化，都是 2.1 的定義題在用的。
- **1.8 連續：** 東華兩份期中考把「在 0 連續」和「在 0 是否可微」放在同一題。
- **2.2 可微與連續：** differentiable ⇒ continuous，反過來不對（$\lvert x\rvert$）。課本下一節。
- **三角極限：** #47、48 的極限值要等到後面學了 $\lim_{\theta\to0}\frac{\sin\theta}{\theta}=1$ 才算得出來。

## Sources

- [東華大學應數系 93 學年度微積分第一次期中考](https://am.ndhu.edu.tw/var/file/38/1038/img/1326/93-1-1.pdf)
- [東華大學應數系 92 學年度微積分第一次期中考](https://am.ndhu.edu.tw/var/file/38/1038/img/1326/92-1-1.pdf)
- [UBC Math 100 Sample Midterm (solutions)](https://personal.math.ubc.ca/~sjer/math100sec101/Review/samplemt4.pdf)
- [南臺科技大學 OCW 初等微積分 2-1 導數的定義](https://ocw.stust.edu.tw/Sysid/ocw/files/初等微積分(非同步)/2-1導數的定義.pdf)
