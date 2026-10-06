%% unit-summary v1.1 · Stewart, Calculus §2.2 pp. 120–133 (scan) · 2026-10-06 %%

## 2.2 The Derivative as a Function

### The Derivative Function

Equation 1 (fixed number $a$): $f'(a)=\lim_{h\to0}\frac{f(a+h)-f(a)}{h}$

Equation 2 (replace $a$ by a variable $x$):

$$f'(x)=\lim_{h\to0}\frac{f(x+h)-f(x)}{h}$$

$f'$ is a new function, called the derivative of $f$.

> - $f'(a)$ is a **number**; $f'$ is a **function**
> - domain of $f'$ $=\{x \mid f'(x)\text{ exists}\}$, may be smaller than the domain of $f$
> - $f'(x)$ = slope of the tangent line to the graph of $f$ at $(x,f(x))$
> - in Equation 2 the variable is $h$; $x$ is temporarily a constant

Graph of $f'$ from the graph of $f$ (Example 1): the slope of the graph of $f$ becomes the $y$-value on the graph of $f'$
> - horizontal tangent ⇒ $f'(x)=0$ (graph of $f'$ crosses the $x$-axis)
> - tangents with positive slope ⇒ $f'$ above the $x$-axis; negative slope ⇒ below
> - $f$ steepest ⇒ $\lvert f'\rvert$ largest

ex. $f(x)=x^3-x$: $f'(x)=3x^2-1$

ex. $f(x)=\sqrt x$: $f'(x)=\frac{1}{2\sqrt x}$ (rationalize the numerator); domain of $f'$ $=(0,\infty)$, domain of $f$ $=[0,\infty)$

ex. $f(x)=\frac{1-x}{2+x}$: $f'(x)=-\frac{3}{(2+x)^2}$ $\left(\frac{\frac ab-\frac cd}{e}=\frac{ad-bc}{bd}\cdot\frac1e\right)$

### Other Notations

$y=f(x)$:

$$f'(x)=y'=\frac{dy}{dx}=\frac{df}{dx}=\frac{d}{dx}f(x)=Df(x)=D_xf(x)$$

$D$ and $d/dx$: differentiation operators; differentiation = the process of calculating a derivative

$$\frac{dy}{dx}=\lim_{\Delta x\to0}\frac{\Delta y}{\Delta x}\qquad\qquad\left.\frac{dy}{dx}\right\rvert_{x=a}\ \text{or}\ \left.\frac{dy}{dx}\right]_{x=a}=f'(a)$$

> - $\frac{dy}{dx}$ is **not a ratio** (for the time being); it is a synonym for $f'(x)$
> - the vertical bar means "evaluate at"

Definition 3: A function $f$ is differentiable at $a$ if $f'(a)$ exists. It is differentiable on an open interval $(a,b)$ [or $(a,\infty)$ or $(-\infty,a)$ or $(-\infty,\infty)$] if it is differentiable at every number in the interval.

ex. $f(x)=\lvert x\rvert$: $x>0$: $f'(x)=1$; $x<0$: $f'(x)=-1$; $x=0$: $\lim_{h\to0^+}\frac{\lvert h\rvert}{h}=1$, $\lim_{h\to0^-}\frac{\lvert h\rvert}{h}=-1$ ∴ $f'(0)$ does not exist ⇒ differentiable at all $x$ except $0$

Theorem 4: If $f$ is differentiable at $a$, then $f$ is continuous at $a$.

Proof: $x\ne a$: $f(x)-f(a)=\frac{f(x)-f(a)}{x-a}(x-a)$ ⇒ $\lim_{x\to a}[f(x)-f(a)]=f'(a)\cdot0=0$ ⇒ $\lim_{x\to a}f(x)=f(a)$

> - differentiable ⇒ continuous
> - continuous ⇏ differentiable, ex. $f(x)=\lvert x\rvert$ at $0$
> - **not continuous** at $a$ ⇒ **not differentiable** at $a$

### How Can a Function Fail To Be Differentiable?

> $f$ not differentiable at $a$
> - corner or kink: left and right limits (of the difference quotient) are different, ex. $\lvert x\rvert$ at $0$
> - discontinuity: ex. a jump discontinuity
> - vertical tangent line: $f$ is **continuous** at $a$ and $\lim_{x\to a}\lvert f'(x)\rvert=\infty$ (tangent lines become steeper and steeper as $x\to a$)

> - differentiable at $a$ ⇒ zoom in toward $(a,f(a))$: the graph straightens out, more and more like a line
> - corner: no matter how much we zoom in, the corner stays

Left- and right-hand derivatives (Exercises 62–63):

$$f'_-(a)=\lim_{h\to0^-}\frac{f(a+h)-f(a)}{h}\qquad f'_+(a)=\lim_{h\to0^+}\frac{f(a+h)-f(a)}{h}$$

> $f'(a)$ exists ⇔ $f'_-(a)$ and $f'_+(a)$ **exist** and are **equal**

### Higher Derivatives

$f$ differentiable ⇒ $f'$ is also a function ⇒ second derivative $(f')'=f''$

$$\frac{d}{dx}\left(\frac{dy}{dx}\right)=\frac{d^2y}{dx^2}\qquad y'''=f'''(x)=\frac{d}{dx}\left(\frac{d^2y}{dx^2}\right)=\frac{d^3y}{dx^3}\qquad y^{(n)}=f^{(n)}(x)=\frac{d^ny}{dx^n}$$

> - $f''(x)$ = slope of the curve $y=f'(x)$ = rate of change of the slope of $y=f(x)$ (a rate of change of a rate of change)
> - $f'''=(f'')'$; $f''''$ is written $f^{(4)}$; $f^{(n)}$: differentiate $n$ times

position function $s=s(t)$:

$$v(t)=s'(t)=\frac{ds}{dt}\qquad a(t)=v'(t)=s''(t)=\frac{dv}{dt}=\frac{d^2s}{dt^2}\qquad j=\frac{da}{dt}=\frac{d^3s}{dt^3}$$

acceleration = instantaneous rate of change of velocity with respect to time; jerk = rate of change of acceleration

ex. $f(x)=x^3-x$: $f'(x)=3x^2-1$, $f''(x)=6x$, $f'''(x)=6$ (slope of the line $y=6x$), $f^{(4)}(x)=0$

## Part 2 題型

課本習題 66 題全部分類了。★ 的題目在 Obsidian 的 [[CAL1 HW 2.2 Solutions]] 有完整解答（作業 12 題加上補充 6 題）。考古題這次用到中原大學微積分（上）兩份期中考、東華大學 93 學年期中考、一份 Math 1101 的 practice midterm；這四份都沒有「看圖畫 $f'$」的題目，所以圖形題的頻率是 0，只能參考課本的題數。

| # | 題型 | 怎麼認 | 做法 | 課本題數 | 4 份考古題裡有幾份 |
|---|---|---|---|---|---|
| 1 | 由 $f$ 的圖估 $f'$、畫 $f'$ 的圖 | "Use the given graph to estimate"、"sketch the graph of $f'$" | 水平切線 ⇒ $f'=0$；上升 ⇒ $f'>0$；下降 ⇒ $f'<0$；越陡 $\lvert f'\rvert$ 越大 | 18 | 0 |
| 2 | 配對、辨認 $f$、$f'$、$f''$ 的圖 | "Match"、"Identify each curve"、"Which is bigger" | 找水平切線：$p$ 有水平切線的地方，$p'$ 要是 $0$ | 7 | 0 |
| 3 | 用定義求 $f'(x)$ 和定義域 | "using the definition of derivative"、"State the domain" | 代 Equation 2，消掉分母的 $h$：展開、通分、有理化 | 17 | 2 |
| 4 | 由表格估 $f'$ | 給一張表，"construct a table of estimated values" | 左右兩個區間的平均變化率再取平均；端點只能用一邊 | 3 | 0 |
| 5 | $\frac{dy}{dx}$ 的意義 | "What does $dP/dt$ represent"、"Interpret" | 一句完整的話：何時、什麼量、增加或減少、多快、單位 | 2 | 0 |
| 6 | 由圖判斷哪裡不可微 | "State, with reasons, the numbers at which $f$ is not differentiable" | 找三種圖：corner、discontinuity、vertical tangent | 6 | 0 |
| 7 | 高階導數 | $f''$、$f'''$、$f^{(4)}$、acceleration、jerk | 對前一個導函數再用一次定義 | 3 | 1 |
| 8 | 在一點可不可微（用定義） | 絕對值、分段函數、$\sqrt[3]{x}$、"is not differentiable at"、$f'_-$、$f'_+$ | 在那一點代定義，左右極限分開算；不連續就直接不可微 | 8 | 4 |
| 9 | 證明與其他 | "Prove"、angle of inclination | 從定義出發；$\tan\phi=f'(a)$ | 2 | 1 |

題數加起來是 $18+7+17+3+2+6+3+8+2=66$。

**判斷順序：**
- 只有圖：
  - 要畫 $f'$ 或估 $f'$ 的值：第 1 類
  - 好幾條曲線要分辨：第 2 類
  - 問哪裡不可微：第 6 類
- 有函數式：
  - 一般的 $x$，求 $f'(x)$：第 3 類；還要 $f''$、$f'''$：第 7 類
  - 指定一個點（公式在那裡換、有絕對值、有根號）：第 8 類
- 只有表格：第 4 類；只有文字敘述和 $\frac{dP}{dt}$：第 5 類

## 1. 由 f 的圖估 f'、畫 f' 的圖

在 $f$ 的圖上選幾個點畫切線、估斜率，把斜率當成 $f'$ 的高度點在正下方，再連起來。課本 Example 1；#1、2、4–16、54、64、65。

| 題目 | 出處 | 答案 |
|---|---|---|
| 給 $f$ 的圖，畫 $f'$ | 課本 Ex 1 | $f'(3)\approx-\frac23$；$B$、$D$ 是水平切線 ⇒ $f'=0$；$C$ 最陡 ⇒ $f'$ 最大約 $1$ |
| 畫 $y=\sin x$ 的導函數，猜它是什麼 | #16 | 看起來是 $\cos x$ |
| 位置圖 ⇒ 速度圖 ⇒ 加速度圖 | #54 | 對圖做兩次同樣的事 |

- 只看斜率，不看高度：$f$ 在 $x$ 軸上面或下面和 $f'$ 的正負無關。
- $f$ 的最高點和最低點是 $f'$ 的零點，不是 $f'$ 的最高點。
- $f$ 有 corner 的地方 $f'$ 要畫空心點（#9、10）；$f$ 是直線段的地方 $f'$ 是水平線。

## 2. 配對、辨認 f、f'、f'' 的圖

判斷「$q$ 是不是 $p$ 的導函數」：$p$ 有水平切線的地方 $q$ 必須是 $0$，$p$ 上升的地方 $q$ 必須是正的。#3、45–50。

| 題目 | 出處 | 答案 |
|---|---|---|
| (a)–(d) 配 I–IV | #3 ★ | (a) II、(b) IV、(c) I、(d) III |
| $f'(-1)$ 和 $f''(1)$ 哪個大 | #45 ★ | $f'(-1)<0<f''(1)$ |
| 三條曲線是 $f$、$f'$、$f''$ | #47 ★ | $a=f$、$b=f'$、$c=f''$ |
| 位置、速度、加速度（、jerk） | #49、50 | 同樣的判斷法，多一層 |

- 先數水平切線的個數最快（#3 是 2、0、1、3）。
- $f'(a)$ 讀的是**高度**，$f''(a)$ 讀的是 $f'$ 圖形的**斜率**（#45）。
- 在最後一名的曲線有極值的地方，其他曲線都不是 $0$：它就是最高階的那個導函數（#47 的 $c$）。

## 3. 用定義求 f'(x) 和定義域

$f'(x)=\lim_{h\to0}\frac{f(x+h)-f(x)}{h}$，$h$ 是變數、$x$ 當常數。#17–33。

| $f$ 的形式 | 消掉 $h$ 的方法 | 題目 |
|---|---|---|
| 多項式 | 展開，$h$ 提出來 | Ex 2、#19–24、28、33 |
| 分式 | 通分 | Ex 4、#25–27、32 |
| 根號 | 乘共軛（有理化分子） | Ex 3、#31 |
| 根號在分母 | 先通分，再有理化 | #29、30 |

| 題目 | 出處 | 答案 |
|---|---|---|
| $f(x)=x^3-x$ | 課本 Ex 2 | $3x^2-1$ |
| $f(x)=\sqrt x$ | 課本 Ex 3；中原 113 期中 | $\frac{1}{2\sqrt x}$；$f$：$[0,\infty)$，$f'$：$(0,\infty)$ |
| $f(x)=\frac{1-x}{2+x}$ | 課本 Ex 4 | $-\frac{3}{(2+x)^2}$ |
| $f(x)=3x-8$ | #19 ★ | $3$；都是 $\mathbb R$ |
| $A(p)=4p^3+3p$ | #23 ★ | $12p^2+3$；都是 $\mathbb R$ |
| $g(u)=\frac{u+1}{4u-1}$ | #27 ★ | $-\frac{5}{(4u-1)^2}$；都是 $u\ne\frac14$ |
| $f(x)=\frac{1}{\sqrt{1+x}}$ | #29 ★ | $-\frac{1}{2(1+x)^{3/2}}$；都是 $(-1,\infty)$ |
| $f(x)=x^2$ | 中原 113 期中 | $2x$ |
| $f(x)=\sqrt[3]{x}$，證明 $f'(x)=\frac13x^{-2/3}$ | 中原 1141 期中 | 用 $A^3-B^3=(A-B)(A^2+AB+B^2)$ |
| $f(x)=\frac{1}{\sqrt[3]{x}}$（$x\ne0$），證明 $f'(x)=-\frac13x^{-4/3}$ | 中原 1141 期中 | 先通分，再用同一個公式 |

- 題目寫 "using the definition" 就不能直接寫公式的結果。
- 兩個定義域都要寫；$f'$ 的定義域可能比 $f$ 小（$\sqrt x$ 少了 $0$）。
- 立方根用立方差公式，角色和共軛一樣。

## 4. 由表格估 f'

| 題目 | 出處 | 做法 |
|---|---|---|
| $N(t)$，2000–2014 每 2 年 | #34 | 中間的年份：左右兩個平均變化率取平均；2000 和 2014 只有一邊 |
| 樹高 $H(t)$ | #35 | 同上，單位 meters per year |
| 重量 $W(x)$，溫度間隔不相等 | #36 | 每個區間用自己的 $\Delta x$；單位 g/°C |

- 間隔不相等時不能直接拿兩邊的值相減除以固定的數。
- 要寫單位（$y$ 的單位 / $x$ 的單位）。

## 5. dy/dx 的意義

| 題目 | 出處 | 答案 |
|---|---|---|
| $P$ 是太陽能發電的百分比，$\frac{dP}{dt}$ 的意義；$\left.\frac{dP}{dt}\right\rvert_{t=2}=3.5$ | #37 ★ | 百分比對時間的變化率；2022 年 1 月 1 日時每年增加 $3.5$ 個百分點 |
| $N$ 是開車旅遊的人數，$p$ 是油價，$\frac{dN}{dp}$ 的正負 | #38 | 負的：油價上升，人數下降 |

- $\left.\frac{dy}{dx}\right\rvert_{x=a}$ 就是 $f'(a)$。

## 6. 由圖判斷哪裡不可微

| 題目 | 出處 | 答案 |
|---|---|---|
| 圖 | #39 ★ | $-4$（corner）、$0$（discontinuity） |
| 圖 | #40 | $-1$（discontinuity）、$2$（corner） |
| 圖 | #41 ★ | $1$（discontinuity）、$5$（vertical tangent） |
| 圖 | #42 | $-2$（corner）、$1$（discontinuity）、$3$（corner） |

- 一定要寫理由（題目寫 "with reasons"）。
- 很陡但平滑的地方不算；水平切線（極值）也不算，那裡 $f'=0$。
- #43、44 是用放大來看：可微的點放大後變直線，corner 放大後還是 corner。

## 7. 高階導數

| 題目 | 出處 | 答案 |
|---|---|---|
| $f(x)=x^3-x$ | 課本 Ex 6、7；中原 113 期中（求 $f''(1)$） | $f''(x)=6x$，$f'''(x)=6$，$f^{(4)}(x)=0$；$f''(1)=6$ |
| $f(x)=3x^2+2x+1$ | #51 | $f'(x)=6x+2$，$f''(x)=6$ |
| $f(x)=x^3-3x$ | #52 | $f'(x)=3x^2-3$，$f''(x)=6x$ |
| $f(x)=2x^2-x^3$ | #53 ★ | $4x-3x^2$，$4-6x$，$-6$，$0$ |

- $f''$ 是對 $f'$ 用定義，不是對 $f$ 再用一次。
- 直線的導函數是它的斜率，常數函數的導函數是 $0$：$f'''$ 和 $f^{(4)}$ 可以直接寫。
- $a(t)=v'(t)=s''(t)$，jerk $=s'''(t)$；單位是 m/s²、m/s³。

## 8. 在一點可不可微（用定義）

在那一點代 $\lim_{h\to0}\frac{f(a+h)-f(a)}{h}$；公式在 $a$ 的兩邊不一樣時，$h\to0^-$ 和 $h\to0^+$ 分開算（就是 $f'_-(a)$ 和 $f'_+(a)$）。#55–60、62、63。

| 題目 | 出處 | 答案 |
|---|---|---|
| $f(x)=\lvert x\rvert$ 在 $0$ | 課本 Ex 5；中原 113、1141 期中 | 右 $1$、左 $-1$ ⇒ 不可微 |
| $f(x)=\sqrt[3]{x}$ | #55 ★ | $f'(a)=\frac{1}{3a^{2/3}}$；$f'(0)$ 不存在；$(0,0)$ 有 vertical tangent |
| $g(x)=x^{2/3}$ | #56 | $g'(a)=\frac{2}{3a^{1/3}}$；$g'(0)$ 不存在（右 $\infty$、左 $-\infty$） |
| $f(x)=\lvert x-6\rvert$ | #57 ★ | 在 $6$ 不可微；$f'(x)=1$（$x>6$）、$-1$（$x<6$） |
| $f(x)=[\![x]\!]$ | #58 ★ | 在整數不可微（不連續）；其他地方 $f'(x)=0$ |
| $f(x)=x\lvert x\rvert$ | #59 ★ | 處處可微，$f'(x)=2\lvert x\rvert$ |
| $g(x)=x+\lvert x\rvert$ | #60 | $x\ne0$ 可微；$g'(x)=2$（$x>0$）、$0$（$x<0$） |
| $f=0$（$x\le0$）、$x$ 或 $x^2$（$x>0$） | #62 ★ | (a) $0$、$1$，不可微；(b) $0$、$0$，可微 |
| 三段的分段函數 | #63 ★ | $f'_-(4)=-1$、$f'_+(4)=1$；不連續：$0$、$5$；不可微：$0$、$4$、$5$ |
| $f(x)=4+x$（$x<2$）、$3x$（$x\ge2$），證明在 $2$ 不可微 | 中原 1141 期中 | $f'_-(2)=1$、$f'_+(2)=3$ |
| $f(x)=2\lvert x-3\rvert$ 在 $3$ | Math 1101 practice midterm | 左 $-2$、右 $2$ ⇒ 不可微 |
| $x\sin\frac1x$、$x^2\sin\frac1x$、$x^3\sin\frac1x$ 在 $0$ | 東華 93 期中；中原 1141 期中 | 第一個不可微；後兩個 $f'(0)=0$（Squeeze Theorem） |

- $f(a)$ 用包含 $a$ 的那一段；$f(a+h)$ 看 $h$ 的正負用對應的那一段。
- 不連續 ⇒ 不可微，可以直接寫；連續 ⇏ 可微，還是要算。
- 有絕對值不一定不可微：$x\lvert x\rvert$ 在 $0$ 可微（#59）。
- $f'(0)$ 是 $\infty$ 也算不存在；vertical tangent 還要加上「$f$ 在那裡連續」。

## 9. 證明與其他

| 題目 | 出處 | 答案 |
|---|---|---|
| 偶函數的導函數是奇函數，奇函數的導函數是偶函數 | #61 ★ | 從 $f'(-x)$ 的定義出發，令 $k=-h$ |
| 可微 ⇒ 連續 的證明 | 課本 Theorem 4；中原 1141 期中 | $f(x)-f(a)=\frac{f(x)-f(a)}{x-a}(x-a)\to f'(a)\cdot0$ |
| $y=x^2$ 在 $(1,1)$ 的切線的 angle of inclination | #66 | $\tan\phi=2$，$\phi\approx63^\circ$ |

- Theorem 4 的證明會考，Part 1 那一行要會寫成完整的式子。

## 常一起考的

- **1.6 極限技巧：** 展開、通分、有理化，都是定義題在用的。
- **1.8 連續：** 分段函數常同一題問「連續嗎」和「可微嗎」（#63；東華 93 期中）。
- **2.1 在一點的導數：** $x\sin\frac1x$ 那一類（2.1 #57、58）和這一節的第 8 類是同一種題目。
- **2.3 微分公式：** 中原的期中考同一份裡已經有 product rule、quotient rule 的題目。

## Sources

- [中原大學 微積分（上）B 群 期中考題目（檔名 1141）](https://mathwww.cycu.edu.tw/wp-content/uploads/1141-B群題目.pdf)
- [中原大學 微積分 113 學年度期中考題目（檔名 11311）](https://mathwww.cycu.edu.tw/wp-content/uploads/11311題目.pdf)
- [東華大學應數系 93 學年度微積分第一次期中考](https://am.ndhu.edu.tw/var/file/38/1038/img/1326/93-1-1.pdf)
- [Math 1101 Calculus I Practice Midterm 1 (solutions)](https://idv.sinica.edu.tw/cli/CalcI_s20PM1Sol.pdf)
