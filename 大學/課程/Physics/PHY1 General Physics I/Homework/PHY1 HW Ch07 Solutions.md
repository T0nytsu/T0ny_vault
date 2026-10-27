---
course: [PHY1]
semester: "115-1"
chapter: ["7.1", "7.2", "7.3", "7.4", "7.5", "7.6"]
tags: [physics, homework, solutions, energy]
source:
  - "Own solutions; every number recomputed with Python, symbolic results with sympy"
  - "EUP Ch. 7 (pp. 129-149), scanned PDF: equations and answers to GOT IT? questions"
  - "[[PHY1 Ch07 Fig 7.15.png]]"
  - "[[PHY1 Ch07 Fig 7.16.png]]"
  - "[[PHY1 Ch07 Fig 7.19.png]]"
  - "[[PHY1 Ch07 Fig 7.21.png]]"
  - "[[PHY1 Ch07 Fig 7.22.png]]"
  - "[[PHY1 Ch07 Fig 7.24.png]]"
  - "[[PHY1 Ch07 Problem 7.51 U.png]]"
  - "[[PHY1 Ch07 Problem 7.69 fit.png]]"
created: 2026-10-28
questions: "[[PHY1 HW Ch07 Questions]]"
up: "[[PHY1 Index]]"
format: "physics-notes 1.1"
---
> [!note] 符號與公式
> - 式號照課本：保守力 $\oint \vec{F} \cdot d\vec{r} = 0$ (7.1)；位能 $\Delta U = -\int_{A}^{B}\vec{F} \cdot d\vec{r}$ (7.2)，一維 $\Delta U = -\int_{x_{1}}^{x_{2}}F(x)\,dx$ (7.2a)，**力是常數時** $\Delta U = -F(x_{2} - x_{1})$ (7.2b)。
> - 重力位能 $\Delta U = mg\,\Delta y$ (7.3)，**只在地表附近**；彈性位能 $U = \tfrac{1}{2}kx^{2}$ (7.4)，**只對理想彈簧**，$x = 0$ 時 $U = 0$。
> - 力學能守恆 $K + U = K_{0} + U_{0}$ (7.6)，**只有保守力作功時**；有動摩擦時 $\Delta K + \Delta U = -f_{\mathrm{k}}d$ (7.7)；一般 $\Delta K + \Delta U + \Delta E_{\mathrm{int}} = W_{\mathrm{ext}}$ (7.8)；由位能求力 $F_{x} = -dU/dx$ (7.9)。
> - 高度 $y$ 一律向上為正。$g = 9.8\ \mathrm{m/s^2}$；KSU 的題目用 $9.80\ \mathrm{m/s^2}$。中間值多留一位有效數字。

## 答案總表

| 題目 | 答案 |
| --- | --- |
| [[PHY1 HW Ch07 Questions#EUP 7.9\|EUP 7.9]] | (a) $2\mu mgL$；(b) $\sqrt{2}\mu mgL$ |
| [[PHY1 HW Ch07 Questions#EUP 7.12\|EUP 7.12]] | (a) $1.5\ \mathrm{MJ}$；(b) $-66\ \mathrm{kJ}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.14\|EUP 7.14]] | $8.8\ \mathrm{J}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.37\|EUP 7.37]] | $777\ \mathrm{J}$，比 Example 7.3 的 $741\ \mathrm{J}$ 多 $4.9\%$ |
| [[PHY1 HW Ch07 Questions#EUP 7.26\|EUP 7.26]] | (a) $-9.9\ \mathrm{N}$；(b) $0$；(c) $+6.5\ \mathrm{N}$（$x$ 分量） |
| [[PHY1 HW Ch07 Questions#EUP 7.17\|EUP 7.17]] | $22\ \mathrm{m/s}$；$35\ \mathrm{m/s}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.19\|EUP 7.19]] | $1.1 \times 10^{2}\ \mathrm{m}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.42\|EUP 7.42]] | $4.1\ \mathrm{m/s}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.49\|EUP 7.49]] | 證明 |
| [[PHY1 HW Ch07 Questions#EUP 7.23\|EUP 7.23]] | $0.72$ |
| [[PHY1 HW Ch07 Questions#EUP 7.25\|EUP 7.25]] | $x = \pm 2.1\ \mathrm{m}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.50\|EUP 7.50]] | $x = 0.25\ \mathrm{m}$ 與 $4.5\ \mathrm{m}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.10\|EUP 7.10]] | 兩條路徑都是 $-mgL$ |
| [[PHY1 HW Ch07 Questions#EUP 7.51\|EUP 7.51]] | (a) $U = 8.83x^{3} - 3.05x^{4}$（J，$x$ 單位 m）；(c) $0 < x < 3\ \mathrm{m}$ 內沒有；轉折點在 $x = -0.95\ \mathrm{m}$ 與 $3.02\ \mathrm{m}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.63\|EUP 7.63]] | $v = \sqrt{\dfrac{4ax^{3/2}}{3m}}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.68\|EUP 7.68]] | $\tfrac{1}{2}(4 + a)kx_{1}^{2}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.41\|EUP 7.41]] | $\dfrac{kx^{2}}{2mg\sin\theta} - x$ |
| [[PHY1 HW Ch07 Questions#EUP 7.45\|EUP 7.45]] | (a) $14\ \mathrm{cm}$；(b) $7.0\ \mathrm{m/s}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.69\|EUP 7.69]] | $h$ 對 $x^{2}/m$ 作圖；斜率 $9.42\ \mathrm{kg/m}$；$k = 1.8 \times 10^{2}\ \mathrm{N/m}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.47\|EUP 7.47]] | $\tfrac{5}{2}R$ |
| [[PHY1 HW Ch07 Questions#EUP 7.59\|EUP 7.59]] | $2.8\ \mathrm{m}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.62\|EUP 7.62]] | 證明 |
| [[PHY1 HW Ch07 Questions#EUP 7.53\|EUP 7.53]] | $20\ \mathrm{m/s}$；$30\ \mathrm{m/s}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.55\|EUP 7.55]] | $1.3\ \mathrm{m}$（從放開處量起） |
| [[PHY1 HW Ch07 Questions#EUP 7.57\|EUP 7.57]] | 摩擦區左端右方 $0.62\ \mathrm{m}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.64\|EUP 7.64]] | 能；頂端動能 $1.6\ \mathrm{J}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.24\|EUP 7.24]] | (a) $4.8\ \mathrm{m/s}$；(b) $7.0\ \mathrm{m/s}$；(c) $x \approx 11\ \mathrm{m}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.52\|EUP 7.52]] | $0.282\ \mathrm{nm}$ |
| [[PHY1 HW Ch07 Questions#EUP 7.70 to 7.73\|EUP 7.70 to 7.73]] | c, d, c, b |
| [[PHY1 HW Ch07 Questions#KSUF 3.1 and 3.2\|KSUF 3.1 and 3.2]] | a, b |
| [[PHY1 HW Ch07 Questions#SIU 3.1 and 3.2\|SIU 3.1 and 3.2]] | 封閉路徑上作功為零的力，如重力、彈簧力；力的分量 $F_{x}$ |
| [[PHY1 HW Ch07 Questions#KSUS 3.9 and 3.10\|KSUS 3.9 and 3.10]] | T；c |
| [[PHY1 HW Ch07 Questions#KSUS 3.12 to 3.14\|KSUS 3.12 to 3.14]] | T, F, T |
| [[PHY1 HW Ch07 Questions#KSUS 3.16 and 3.17\|KSUS 3.16 and 3.17]] | T, F |
| [[PHY1 HW Ch07 Questions#KSUS 3.11\|KSUS 3.11]] | a) $1.23 \times 10^{3}\ \mathrm{N/m}$；b) $2.45\ \mathrm{m}$ |
| [[PHY1 HW Ch07 Questions#KSUF 3.5\|KSUF 3.5]] | a) $0.376\ \mathrm{m}$；b) $0.188\ \mathrm{m}$；c) $2.21\ \mathrm{J}$ |
| [[PHY1 HW Ch07 Questions#KSUS 3.15\|KSUS 3.15]] | a) $mgR$；b) $3mgR$；c) $7mg$ |
| [[PHY1 HW Ch07 Questions#KSUS 3.18\|KSUS 3.18]] | $4.6 \times 10^{4}\ \mathrm{W}$ |
| [[PHY1 HW Ch07 Questions#SIU 3.5\|SIU 3.5]] | (a) $x = 0$；(b) $x = 0$；(c) $2a > 0$，穩定 |

## 老師勾選：保守力的功

### EUP 7.9
題目：[[PHY1 HW Ch07 Questions#EUP 7.9|EUP 7.9]]

![EUP Figure 7.15|300](../Attachments/PHY1%20Ch07%20Fig%207.15.png)

> [!solution] 解
> 水平面上 $n = mg$，動摩擦力 $\mu mg$。等速，你的力與摩擦力等大反向、沿位移方向，所以 $W = \mu mg \times (\text{路徑長})$：
> - (a) 路徑長 $L + L$：$W_{a} = 2\mu mgL$。
> - (b) 路徑長 $\sqrt{2}L$：$W_{b} = \sqrt{2}\mu mgL$。
>
> 兩者不同：摩擦力是非保守力，作功和路徑有關。

## 老師勾選：位能與由位能求力

### EUP 7.12
題目：[[PHY1 HW Ch07 Questions#EUP 7.12|EUP 7.12]]

> [!solution] 解
> 海平面 $y = 0$，由 (7.3)，$U = mgy$：
> - (a) $U = (78\ \mathrm{kg})(9.8\ \mathrm{m/s^2})(1900\ \mathrm{m}) = 1.5 \times 10^{6}\ \mathrm{J} = 1.5\ \mathrm{MJ}$。
> - (b) $U = (78\ \mathrm{kg})(9.8\ \mathrm{m/s^2})(-86\ \mathrm{m}) = -6.6 \times 10^{4}\ \mathrm{J} = -66\ \mathrm{kJ}$。

### EUP 7.14
題目：[[PHY1 HW Ch07 Questions#EUP 7.14|EUP 7.14]]

> [!solution] 解
> 由 (7.4)，
> $$
> U = \tfrac{1}{2}kx^{2} = \tfrac{1}{2}(440\ \mathrm{N/m})(0.20\ \mathrm{m})^{2} = 8.8\ \mathrm{J}.
> $$

### EUP 7.37
題目：[[PHY1 HW Ch07 Questions#EUP 7.37|EUP 7.37]]

> [!solution] 解
> 力與伸長同方向，由 (7.2a)，取 $x = 0$ 時 $U = 0$：
> $$
> U = -\int_{0}^{x}(-kx + bx^{2} - cx^{3})\,dx = \tfrac{1}{2}kx^{2} - \tfrac{1}{3}bx^{3} + \tfrac{1}{4}cx^{4}.
> $$
> 代入 $k = 223\ \mathrm{N/m}$，$b = 4.10\ \mathrm{N/m^2}$，$c = 3.1\ \mathrm{N/m^3}$，$x = 2.62\ \mathrm{m}$：
> $$
> U = 765.4\ \mathrm{J} - 24.6\ \mathrm{J} + 36.5\ \mathrm{J} = 777\ \mathrm{J}, \qquad \frac{777\ \mathrm{J} - 741\ \mathrm{J}}{741\ \mathrm{J}} = 4.9\%.
> $$
> 比 Example 7.3 多 $4.9\%$（約 $5\%$）。

### EUP 7.26
題目：[[PHY1 HW Ch07 Questions#EUP 7.26|EUP 7.26]]

> [!solution] 解
> 由 (7.9)，$F_{x} = -\dfrac{dU}{dx} = -(3.4\ \mathrm{J/m^2})x$：
> - (a) $F_{x} = -(3.4\ \mathrm{J/m^2})(2.9\ \mathrm{m}) = -9.9\ \mathrm{N}$（指向 $-x$）。
> - (b) $F_{x} = 0$。
> - (c) $F_{x} = -(3.4\ \mathrm{J/m^2})(-1.9\ \mathrm{m}) = +6.5\ \mathrm{N}$（指向 $+x$）。

> [!warning] 用不到 b
> 常數 $b$ 只移動位能零點，微分後消失，不影響力。

## 老師勾選：力學能守恆

### EUP 7.17
題目：[[PHY1 HW Ch07 Questions#EUP 7.17|EUP 7.17]]

> [!solution] 解
> 由靜止出發、無摩擦，由 (7.6)，$\tfrac{1}{2}mv^{2} = mg\,\lvert\Delta y\rvert$，$\lvert\Delta y\rvert$ 是從起點算起的總落差：
> $$
> \begin{aligned}
> v_{1} &= \sqrt{2(9.8\ \mathrm{m/s^2})(25\ \mathrm{m})} = 22\ \mathrm{m/s}, \\
> v_{2} &= \sqrt{2(9.8\ \mathrm{m/s^2})(25\ \mathrm{m} + 38\ \mathrm{m})} = 35\ \mathrm{m/s}.
> \end{aligned}
> $$

> [!warning] 坡角用不到
> 沒有摩擦時速率只看鉛直落差；有摩擦時坡角才有影響（[[#EUP 7.53|EUP 7.53]]）。

### EUP 7.19
題目：[[PHY1 HW Ch07 Questions#EUP 7.19|EUP 7.19]]

> [!solution] 解
> 從拉弓處量起高度，初、末都靜止，由 (7.6)，$\tfrac{1}{2}kx^{2} = mgh$：
> $$
> h = \frac{kx^{2}}{2mg} = \frac{(400\ \mathrm{N/m})(0.85\ \mathrm{m})^{2}}{2(0.130\ \mathrm{kg})(9.8\ \mathrm{m/s^2})} = 1.1 \times 10^{2}\ \mathrm{m}.
> $$

### EUP 7.42
題目：[[PHY1 HW Ch07 Questions#EUP 7.42|EUP 7.42]]

> [!solution] 解
> 最低點最快。從最大擺角到最低點下降 $L(1 - \cos\theta)$，由 (7.6)，
> $$
> v_{\max} = \sqrt{2gL(1 - \cos\theta)} = \sqrt{2(9.8\ \mathrm{m/s^2})(3.8\ \mathrm{m})(1 - \cos 39^{\circ})} = 4.1\ \mathrm{m/s}.
> $$

### EUP 7.49
題目：[[PHY1 HW Ch07 Questions#EUP 7.49|EUP 7.49]]

> [!solution] 解
> 令最大壓縮量為 $x$，重力位能零點取在最低點。質量從靜止落下 $h + x$，在最低點瞬間靜止，由 (7.6)：
> $$
> mg(h + x) = \tfrac{1}{2}kx^{2} \implies \tfrac{1}{2}kx^{2} - mgx - mgh = 0.
> $$
> $$
> x = \frac{mg \pm \sqrt{m^{2}g^{2} + 2kmgh}}{k} = \frac{mg}{k}\left(1 \pm \sqrt{1 + \frac{2kh}{mg}}\right).
> $$
> 取 $+$（$-$ 號給出 $x < 0$，不是壓縮），即得證。$\blacksquare$

## 老師勾選：摩擦與內能

### EUP 7.23
題目：[[PHY1 HW Ch07 Questions#EUP 7.23|EUP 7.23]]

> [!solution] 解
> $\Delta E_{\mathrm{int}} = f_{\mathrm{k}}d = \mu_{\mathrm{k}}mgd$（水平地面 $n = mg$）：
> $$
> \mu_{\mathrm{k}} = \frac{\Delta E_{\mathrm{int}}}{mgd} = \frac{1.7 \times 10^{3}\ \mathrm{J}}{(65\ \mathrm{kg})(9.8\ \mathrm{m/s^2})(3.7\ \mathrm{m})} = 0.72.
> $$

## 老師勾選：位能曲線與轉折點

### EUP 7.25
題目：[[PHY1 HW Ch07 Questions#EUP 7.25|EUP 7.25]]

> [!solution] 解
> 最低點 $y = 0$ 時 $U = 0$，速率最大；轉折點 $K = 0$。由 (7.6)，$mgax^{2} = \tfrac{1}{2}mv_{\max}^{2}$：
> $$
> x = \pm\frac{v_{\max}}{\sqrt{2ga}} = \pm\frac{9.2\ \mathrm{m/s}}{\sqrt{2(9.8\ \mathrm{m/s^2})(0.95\ \mathrm{m^{-1}})}} = \pm 2.1\ \mathrm{m}.
> $$

### EUP 7.50
題目：[[PHY1 HW Ch07 Questions#EUP 7.50|EUP 7.50]]

> [!solution] 解
> 轉折點 $U = E$：$7.0 - 8.0x + 1.7x^{2} = 5.1$，即 $1.7x^{2} - 8.0x + 1.9 = 0$：
> $$
> x = \frac{8.0 \pm \sqrt{(8.0)^{2} - 4(1.7)(1.9)}}{2(1.7)} = 0.25\ \mathrm{m} \ \text{或}\ 4.5\ \mathrm{m}.
> $$

## 加選：保守力的功

### EUP 7.10
題目：[[PHY1 HW Ch07 Questions#EUP 7.10|EUP 7.10]]

> [!solution] 解
> 點 2 比點 1 高 $L$。重力 $-mg\hat{\jmath}$ 是常數，只有鉛直位移作功，$W = -mg\,\Delta y$：
> - (a) 先上 $L$ 再水平 $L$：$W = -mgL + 0 = -mgL$。
> - (b) 斜線，鉛直分量 $L$：$W = -mgL$。
>
> 相同：重力是保守力。

## 加選：由力積分求位能

### EUP 7.51
題目：[[PHY1 HW Ch07 Questions#EUP 7.51|EUP 7.51]]

> [!solution] 解
> **(a)** 由 (7.2a)，取 $x = 0$ 時 $U = 0$：
> $$
> \begin{aligned}
> U(x) &= -\int_{0}^{x}(ax^{2} + bx^{3})\,dx = -\frac{a}{3}x^{3} - \frac{b}{4}x^{4} \\
> &= (8.83\ \mathrm{J/m^3})x^{3} - (3.05\ \mathrm{J/m^4})x^{4}.
> \end{aligned}
> $$
> **(b)** 見圖。$dU/dx = 0$ 在 $x = -a/b = 2.17\ \mathrm{m}$，$U = 22.6\ \mathrm{J}$ 是最大值；$U = 0$ 在 $x = 2.90\ \mathrm{m}$；$U(3\ \mathrm{m}) = -8.55\ \mathrm{J}$。
>
> **(c)** 在 $0 < x < 3\ \mathrm{m}$ 上 $U \ge -8.55\ \mathrm{J} > -10.0\ \mathrm{J}$，直線 $E = -10.0\ \mathrm{J}$ 和曲線在這個區間內沒有交點：物體不可能在這裡。把圖延伸，交點（轉折點）在
> $$
> x = -0.95\ \mathrm{m} \quad \text{與} \quad x = 3.02\ \mathrm{m},
> $$
> 物體只能在 $x \le -0.95\ \mathrm{m}$ 或 $x \ge 3.02\ \mathrm{m}$ 運動。
>
> ![EUP 7.51 U|480](../Attachments/PHY1%20Ch07%20Problem%207.51%20U.png)

> [!warning] 交點在區間外
> 題目要求畫 $0 < x < 3\ \mathrm{m}$，但 $E = -10.0\ \mathrm{J}$ 的轉折點都在這個區間外；右邊的 $3.02\ \mathrm{m}$ 剛好在端點外一點。

### EUP 7.63
題目：[[PHY1 HW Ch07 Questions#EUP 7.63|EUP 7.63]]

> [!solution] 解
> 由 (7.2a)，取 $x = 0$ 時 $U = 0$：
> $$
> U(x) = -\int_{0}^{x}a\sqrt{x}\,dx = -\tfrac{2}{3}ax^{3/2}.
> $$
> 原點靜止，$K_{0} = U_{0} = 0$，由 (7.6)，$\tfrac{1}{2}mv^{2} - \tfrac{2}{3}ax^{3/2} = 0$：
> $$
> v = \sqrt{\frac{4ax^{3/2}}{3m}}
> $$
> （$a > 0$，力指向 $+x$，輕推後才會往 $+x$ 加速。）

### EUP 7.68
題目：[[PHY1 HW Ch07 Questions#EUP 7.68|EUP 7.68]]

> [!solution] 解
> $x > x_{1}$ 時兩個彈簧同時作用，第二個從 $x_{1}$ 才開始伸長，伸長量 $x - x_{1}$。由 (7.4) 把兩個彈簧的位能相加，在 $x = 2x_{1}$：
> $$
> U = \tfrac{1}{2}k(2x_{1})^{2} + \tfrac{1}{2}(ak)(2x_{1} - x_{1})^{2} = 2kx_{1}^{2} + \tfrac{1}{2}akx_{1}^{2} = \tfrac{1}{2}(4 + a)kx_{1}^{2}.
> $$

## 加選：力學能守恆的彈簧與重力

### EUP 7.41
題目：[[PHY1 HW Ch07 Questions#EUP 7.41|EUP 7.41]]

> [!solution] 解
> 彈簧沿斜坡放置。從壓縮處到最高點沿斜坡共走 $s$，上升 $s\sin\theta$，初、末都靜止，由 (7.6)：
> $$
> \tfrac{1}{2}kx^{2} = mgs\sin\theta \implies s = \frac{kx^{2}}{2mg\sin\theta}.
> $$
> 其中 $x$ 是在彈簧上走的，離開彈簧後走 $s - x = \dfrac{kx^{2}}{2mg\sin\theta} - x$。

> [!warning] 彈簧放在哪
> 若彈簧在斜坡底的水平面上，離開彈簧時還沒上升，答案就是 $\dfrac{kx^{2}}{2mg\sin\theta}$。

### EUP 7.45
題目：[[PHY1 HW Ch07 Questions#EUP 7.45|EUP 7.45]]

![EUP Figure 7.18|300](../Attachments/PHY1%20Ch07%20Fig%207.18.png)

> [!solution] 解
> 無摩擦，力學能守恆；兩個最大壓縮時木塊都靜止。
> - (a) $\tfrac{1}{2}k_{2}x_{2}^{2} = \tfrac{1}{2}k_{1}x_{1}^{2}$：$x_{2} = x_{1}\sqrt{\dfrac{k_{1}}{k_{2}}} = (21\ \mathrm{cm})\sqrt{\dfrac{110\ \mathrm{N/m}}{240\ \mathrm{N/m}}} = 14\ \mathrm{cm}$。
> - (b) 兩彈簧之間 $U = 0$：$\tfrac{1}{2}mv^{2} = \tfrac{1}{2}k_{1}x_{1}^{2}$，$v = x_{1}\sqrt{\dfrac{k_{1}}{m}} = (0.21\ \mathrm{m})\sqrt{\dfrac{110\ \mathrm{N/m}}{0.100\ \mathrm{kg}}} = 7.0\ \mathrm{m/s}$。

### EUP 7.69
題目：[[PHY1 HW Ch07 Questions#EUP 7.69|EUP 7.69]]

> [!solution] 解
> 由 (7.6)，$\tfrac{1}{2}kx^{2} = mgh$，所以
> $$
> h = \frac{k}{2g}\cdot\frac{x^{2}}{m}:
> $$
> $h$ 對 $x^{2}/m$ 作圖是通過原點的直線，斜率 $k/(2g)$。換成 SI：
>
> | $x^{2}/m$ ($\mathrm{m^2/kg}$) | $0.01152$ | $0.01179$ | $0.02314$ | $0.03681$ | $0.003931$ |
> | --- | --- | --- | --- | --- | --- |
> | $h$ ($\mathrm{m}$) | $0.103$ | $0.112$ | $0.198$ | $0.352$ | $0.0381$ |
>
> 最小平方擬合：斜率 $9.42\ \mathrm{kg/m}$，截距 $-0.004\ \mathrm{m}$（約為零）。
> $$
> k = 2g \times \text{斜率} = 2(9.8\ \mathrm{m/s^2})(9.42\ \mathrm{kg/m}) = 1.8 \times 10^{2}\ \mathrm{N/m}.
> $$
>
> ![EUP 7.69 fit|480](../Attachments/PHY1%20Ch07%20Problem%207.69%20fit.png)

## 加選：圓周運動與能量守恆

### EUP 7.47
題目：[[PHY1 HW Ch07 Questions#EUP 7.47|EUP 7.47]]

![EUP Figure 7.19|300](../Attachments/PHY1%20Ch07%20Fig%207.19.png)

> [!solution] 解
> 高度從圈底量起。剛好繞過頂端（高 $2R$）時正向力為零，只靠重力提供向心力：$mg = \dfrac{mv_{\mathrm{top}}^{2}}{R}$，$v_{\mathrm{top}}^{2} = gR$。由 (7.6)，
> $$
> mgh = mg(2R) + \tfrac{1}{2}m(gR) \implies h = \tfrac{5}{2}R.
> $$

> [!warning] 頂端不是靜止
> 用 $h = 2R$ 是錯的：在頂端速率若為零，木塊早就掉下來了。

### EUP 7.59
題目：[[PHY1 HW Ch07 Questions#EUP 7.59|EUP 7.59]]

![EUP Figure 7.22|400](../Attachments/PHY1%20Ch07%20Fig%207.22.png)

> [!solution] 解
> 圈底和發射處同高，頂端高 $2R$，剛好不脫軌時 $v_{\mathrm{top}}^{2} = gR$（同 [[#EUP 7.47|EUP 7.47]]）。由 (7.6)，
> $$
> \begin{aligned}
> \tfrac{1}{2}kx^{2} &= mg(2R) + \tfrac{1}{2}mgR = \tfrac{5}{2}mgR \\
> \implies x &= \sqrt{\frac{5mgR}{k}} = \sqrt{\frac{5(710\ \mathrm{kg})(9.8\ \mathrm{m/s^2})(7.5\ \mathrm{m})}{34 \times 10^{3}\ \mathrm{N/m}}} = 2.8\ \mathrm{m}.
> \end{aligned}
> $$

### EUP 7.62
題目：[[PHY1 HW Ch07 Questions#EUP 7.62|EUP 7.62]]

> [!solution] 解
> 蟲從頭頂近乎靜止出發，$\theta$ 是它和球心連線偏離鉛直的角度，已下降 $R(1 - \cos\theta)$。由 (7.6)，$v^{2} = 2gR(1 - \cos\theta)$。沿半徑向內：
> $$
> mg\cos\theta - n = \frac{mv^{2}}{R} = 2mg(1 - \cos\theta).
> $$
> 離開頭部時 $n = 0$：$\cos\theta = 2(1 - \cos\theta)$，$\cos\theta = \tfrac{2}{3}$，下降 $R(1 - \tfrac{2}{3}) = \tfrac{1}{3}R$。$\blacksquare$

## 加選：摩擦與內能

### EUP 7.53
題目：[[PHY1 HW Ch07 Questions#EUP 7.53|EUP 7.53]]

> [!solution] 解
> 傾角 $\theta$、落差 $\Delta y$ 的斜坡長 $\Delta y/\sin\theta$，正向力 $mg\cos\theta$，摩擦生的內能 $\mu mg\cos\theta\cdot\Delta y/\sin\theta = \mu mg\,\Delta y/\tan\theta$。由 (7.7)，每段斜坡 $\Delta\left(\tfrac{1}{2}v^{2}\right) = g\,\Delta y\left(1 - \dfrac{\mu}{\tan\theta}\right)$：
> $$
> \begin{aligned}
> v_{1} &= \sqrt{2(9.8\ \mathrm{m/s^2})(25\ \mathrm{m})\left(1 - \frac{0.11}{\tan 32^{\circ}}\right)} = 20\ \mathrm{m/s}, \\
> v_{2} &= \sqrt{v_{1}^{2} + 2(9.8\ \mathrm{m/s^2})(38\ \mathrm{m})\left(1 - \frac{0.11}{\tan 20^{\circ}}\right)} = 30\ \mathrm{m/s}.
> \end{aligned}
> $$

### EUP 7.55
題目：[[PHY1 HW Ch07 Questions#EUP 7.55|EUP 7.55]]

> [!solution] 解
> 摩擦從放開就開始作用。最後全部的彈性位能轉成內能，由 (7.7)，$\tfrac{1}{2}kx^{2} = \mu mgd$：
> $$
> d = \frac{kx^{2}}{2\mu mg} = \frac{(290\ \mathrm{N/m})(0.22\ \mathrm{m})^{2}}{2(0.29)(1.9\ \mathrm{kg})(9.8\ \mathrm{m/s^2})} = 1.3\ \mathrm{m}
> $$
> （從放開處量起；木塊到彈簧原長時還有 $7.02\ \mathrm{J} - 1.19\ \mathrm{J} = 5.8\ \mathrm{J}$ 動能，確實會離開彈簧。）

> [!warning] 彈簧伸長時也有摩擦
> 不能先用 $\tfrac{1}{2}kx^{2} = \tfrac{1}{2}mv^{2}$ 求離開彈簧的速率：那段 $22\ \mathrm{cm}$ 也在摩擦面上。

### EUP 7.57
題目：[[PHY1 HW Ch07 Questions#EUP 7.57|EUP 7.57]]

![EUP Figure 7.21|400](../Attachments/PHY1%20Ch07%20Fig%207.21.png)

> [!solution] 解
> 只有摩擦區消耗力學能；彈簧和彎曲上坡都無摩擦，會把木塊送回來。由 (7.7)，在摩擦區內走的總距離
> $$
> \begin{aligned}
> D &= \frac{\tfrac{1}{2}kx^{2}}{\mu mg} = \frac{\tfrac{1}{2}(200\ \mathrm{N/m})(0.15\ \mathrm{m})^{2}}{(0.27)(0.190\ \mathrm{kg})(9.8\ \mathrm{m/s^2})} \\
> &= \frac{2.25\ \mathrm{J}}{0.503\ \mathrm{N}} = 4.48\ \mathrm{m} = 5.27 \times (0.85\ \mathrm{m}).
> \end{aligned}
> $$
> 完整穿過 5 次（第 1、3、5 次向右，第 2、4 次向左），第 6 次從右端向左走 $4.48\ \mathrm{m} - 5(0.85\ \mathrm{m}) = 0.23\ \mathrm{m}$ 後停下：停在摩擦區左端右方 $0.85\ \mathrm{m} - 0.23\ \mathrm{m} = 0.62\ \mathrm{m}$。

### EUP 7.64
題目：[[PHY1 HW Ch07 Questions#EUP 7.64|EUP 7.64]]

> [!solution] 解
> 取木塊從放開處沿斜面走 $d = 2.0\ \mathrm{m}$ 到頂端，摩擦全程作用，$mg = 4.5\ \mathrm{N}$。彈簧給 $\tfrac{1}{2}(2.0 \times 10^{3}\ \mathrm{N/m})(0.10\ \mathrm{m})^{2} = 10\ \mathrm{J}$。由 (7.7)，到頂端需要
> $$
> \begin{aligned}
> mgd\sin 30^{\circ} + \mu mg\cos 30^{\circ}\,d &= (4.5\ \mathrm{N})(2.0\ \mathrm{m})(0.50) \\
> &\quad + (0.50)(4.5\ \mathrm{N})(0.866)(2.0\ \mathrm{m}) \\
> &= 4.5\ \mathrm{J} + 3.9\ \mathrm{J} = 8.4\ \mathrm{J}.
> \end{aligned}
> $$
> $10\ \mathrm{J} > 8.4\ \mathrm{J}$：能到頂端，動能 $K = 10\ \mathrm{J} - 8.4\ \mathrm{J} = 1.6\ \mathrm{J}$。

## 加選：位能曲線、轉折點與平衡

### EUP 7.24
題目：[[PHY1 HW Ch07 Questions#EUP 7.24|EUP 7.24]]

![EUP Figure 7.16|480](../Attachments/PHY1%20Ch07%20Fig%207.16.png)

> [!solution] 解
> 由圖，$h_{A} = 3.8\ \mathrm{m}$，$h_{B} = 2.6\ \mathrm{m}$，$h_{C} = 1.3\ \mathrm{m}$。從 $A$ 靜止出發，由 (7.6)，$v = \sqrt{2g(h_{A} - h)}$：
> - (a) $v_{B} = \sqrt{2(9.8\ \mathrm{m/s^2})(1.2\ \mathrm{m})} = 4.8\ \mathrm{m/s}$。
> - (b) $v_{C} = \sqrt{2(9.8\ \mathrm{m/s^2})(2.5\ \mathrm{m})} = 7.0\ \mathrm{m/s}$。
> - (c) 轉折點在軌道再次升到 $h_{A} = 3.8\ \mathrm{m}$ 處：由圖約 $x \approx 11\ \mathrm{m}$。

### EUP 7.52
題目：[[PHY1 HW Ch07 Questions#EUP 7.52|EUP 7.52]]

> [!solution] 解
> 平衡處 $F = -dU/dr = 0$：
> $$
> \begin{aligned}
> \frac{dU}{dr} &= -\frac{nb}{r^{n+1}} + \frac{a}{r^{2}} = 0 \implies r_{0} = \left(\frac{nb}{a}\right)^{1/(n-1)}, \\
> r_{0} &= \left(\frac{(8.22)(5.52 \times 10^{-98})}{4.04 \times 10^{-28}}\right)^{1/7.22} = 2.82 \times 10^{-10}\ \mathrm{m}.
> \end{aligned}
> $$
> 平衡間距 $0.282\ \mathrm{nm}$。

### EUP 7.70 to 7.73
題目：[[PHY1 HW Ch07 Questions#EUP 7.70 to 7.73|EUP 7.70 to 7.73]]

![EUP Figure 7.24|400](../Attachments/PHY1%20Ch07%20Fig%207.24.png)

> [!solution] 解
> 由 (7.9)，力是 $-dU/dr$：曲線的斜率。
> - **70.** c. 斜率為零在井底（約 $1.5\ \mathrm{fm}$，不在選項中）和障壁頂端（約 $5\ \mathrm{fm}$）。
> - **71.** d. 要越過約 $0.3\ \mathrm{MeV}$ 高的障壁；遠處 $U = 0$。
> - **72.** c. 從遠處的 $U = 0$ 到井底約 $-3.3\ \mathrm{MeV}$。
> - **73.** b. $4\ \mathrm{fm}$ 處曲線向右上升，$dU/dr > 0$，力指向 $r$ 減小的方向：吸力。

## 外校考題：觀念題

### KSUF 3.1 and 3.2
題目：[[PHY1 HW Ch07 Questions#KSUF 3.1 and 3.2|KSUF 3.1 and 3.2]]

> [!solution] 解
> - **1.** a. 保守力的功與路徑無關，所以能定義位能 (7.2)。
> - **2.** b. 封閉系統總能量守恆 (7.8)，力學能減少多少，內能等其他形式就增加多少。

### SIU 3.1 and 3.2
題目：[[PHY1 HW Ch07 Questions#SIU 3.1 and 3.2|SIU 3.1 and 3.2]]

> [!solution] 解
> - **1.** 沿任意封閉路徑作功為零的力 (7.1)；等價地，兩點間的功與路徑無關，可以定義位能。例：重力、理想彈簧的力（靜電力也是）。
> - **2.** 力的 $x$ 分量：$F_{x} = -dU/dx$ (7.9)。

### KSUS 3.9 and 3.10
題目：[[PHY1 HW Ch07 Questions#KSUS 3.9 and 3.10|KSUS 3.9 and 3.10]]

> [!solution] 解
> - **9.** T. $U = \tfrac{1}{2}kx^{2} \propto x^{2}$，$x$ 加倍則 $U$ 變四倍。
> - **10.** c. 只有重力有對應的位能；正向力和靜摩擦力定義不出位能，空氣阻力是非保守力。

### KSUS 3.12 to 3.14
題目：[[PHY1 HW Ch07 Questions#KSUS 3.12 to 3.14|KSUS 3.12 to 3.14]]

> [!solution] 解
> - **12.** T. 保守系統 $\Delta K + \Delta U = 0$ (7.5)。
> - **13.** F. 位能零點可以任選，負位能很常見（例如 Example 7.1 的街道）。
> - **14.** T. 這就是 (7.2)。

### KSUS 3.16 and 3.17
題目：[[PHY1 HW Ch07 Questions#KSUS 3.16 and 3.17|KSUS 3.16 and 3.17]]

> [!solution] 解
> - **16.** T. $F_{x} = -dU/dx$ (7.9)。
> - **17.** F. 轉折點在 $U = E$ 處；$U$ 的極小值是穩定平衡點，經過那裡時速率最大。

## 外校考題：計算題

### KSUS 3.11
題目：[[PHY1 HW Ch07 Questions#KSUS 3.11|KSUS 3.11]]

> [!solution] 解
> **a)** 平衡時彈簧力等於重力：
> $$
> k = \frac{mg}{x_{\mathrm{eq}}} = \frac{(2.50\ \mathrm{kg})(9.80\ \mathrm{m/s^2})}{0.0200\ \mathrm{m}} = 1.23 \times 10^{3}\ \mathrm{N/m}.
> $$
> **b)** 離地 $20.0\ \mathrm{cm}$ 時彈簧壓縮 $x = 50.0\ \mathrm{cm} - 20.0\ \mathrm{cm} = 0.300\ \mathrm{m}$。球沒有黏在彈簧上，在彈簧原長處離開後繼續上升。重力位能零點取在放開處，由 (7.6)，$\tfrac{1}{2}kx^{2} = mg(h - 0.200\ \mathrm{m})$：
> $$
> h = 0.200\ \mathrm{m} + \frac{(1225\ \mathrm{N/m})(0.300\ \mathrm{m})^{2}}{2(2.50\ \mathrm{kg})(9.80\ \mathrm{m/s^2})} = 0.200\ \mathrm{m} + 2.25\ \mathrm{m} = 2.45\ \mathrm{m}.
> $$

### KSUF 3.5
題目：[[PHY1 HW Ch07 Questions#KSUF 3.5|KSUF 3.5]]

> [!solution] 解
> $x$ 是彈簧伸長量，向下為正；重力位能零點取在掛上的位置，所以伸長 $x$ 時重力位能是 $-mgx$。
>
> **a)** 從靜止放開，到最低點又瞬間靜止，由 (7.6)，$0 = \tfrac{1}{2}kx_{\max}^{2} - mgx_{\max}$：
> $$
> x_{\max} = \frac{2mg}{k} = \frac{2(2.40\ \mathrm{kg})(9.80\ \mathrm{m/s^2})}{125\ \mathrm{N/m}} = 0.376\ \mathrm{m}.
> $$
> **b)** 停在平衡點，$kx_{\mathrm{f}} = mg$：$x_{\mathrm{f}} = \dfrac{mg}{k} = 0.188\ \mathrm{m}$。
>
> **c)** 初、末都靜止，轉成熱能的是力學能的減少：
> $$
> \Delta E_{\mathrm{th}} = mgx_{\mathrm{f}} - \tfrac{1}{2}kx_{\mathrm{f}}^{2} = \frac{(mg)^{2}}{2k} = \frac{\left[(2.40\ \mathrm{kg})(9.80\ \mathrm{m/s^2})\right]^{2}}{2(125\ \mathrm{N/m})} = 2.21\ \mathrm{J}.
> $$

> [!warning] 最大伸長不是平衡點
> 突然放開時最大伸長是平衡伸長的兩倍：在平衡點質量還在動。

### KSUS 3.15
題目：[[PHY1 HW Ch07 Questions#KSUS 3.15|KSUS 3.15]]

> [!solution] 解
> **a)** 頂端時座椅的正向力和重力都指向圓心（向下）：$mg + mg = \dfrac{mv_{\mathrm{t}}^{2}}{R}$，所以 $K_{\mathrm{t}} = \tfrac{1}{2}mv_{\mathrm{t}}^{2} = mgR$。
>
> **b)** 由 (7.6)，從頂端下降 $2R$：$K_{\mathrm{b}} = K_{\mathrm{t}} + mg(2R) = 3mgR$。
>
> **c)** 底端正向力向上、重力向下：
> $$
> n - mg = \frac{mv_{\mathrm{b}}^{2}}{R} = \frac{2K_{\mathrm{b}}}{R} = 6mg \implies n = 7mg.
> $$

### KSUS 3.18
題目：[[PHY1 HW Ch07 Questions#KSUS 3.18|KSUS 3.18]]

> [!solution] 解
> 等減速度，平均速度 $v_{0}/2$，煞車時間 $t = \dfrac{2d}{v_{0}} = \dfrac{2(250\ \mathrm{m})}{36\ \mathrm{m/s}} = 13.9\ \mathrm{s}$。轉成熱能的是全部動能：
> $$
> P = \frac{\tfrac{1}{2}mv_{0}^{2}}{t} = \frac{\tfrac{1}{2}(980\ \mathrm{kg})(36\ \mathrm{m/s})^{2}}{13.9\ \mathrm{s}} = \frac{6.35 \times 10^{5}\ \mathrm{J}}{13.9\ \mathrm{s}} = 4.6 \times 10^{4}\ \mathrm{W}.
> $$

### SIU 3.5
題目：[[PHY1 HW Ch07 Questions#SIU 3.5|SIU 3.5]]

> [!solution] 解
> **(a)** $U = x^{2}(a + bx^{2}) = 0$；$a + bx^{2} > 0$，所以只有 $x = 0$。
>
> **(b)** 由 (7.9)，$F = -\dfrac{dU}{dx} = -2x(a + 2bx^{2}) = 0$；$a + 2bx^{2} > 0$，所以只有 $x = 0$。
>
> **(c)** $\dfrac{d^{2}U}{dx^{2}} = 2a + 12bx^{2}$，在 $x = 0$ 為 $2a > 0$：$U$ 在那裡是極小值，稍微偏離時力指回 $x = 0$，所以是穩定點。
