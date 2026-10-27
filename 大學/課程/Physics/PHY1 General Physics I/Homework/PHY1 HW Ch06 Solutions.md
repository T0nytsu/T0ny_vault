---
course: [PHY1]
semester: "115-1"
chapter: ["6.1", "6.2", "6.3", "6.4", "6.5"]
tags: [physics, homework, solutions, energy]
source:
  - "Own solutions; every number recomputed with Python, symbolic results with sympy"
  - "EUP Ch. 6 (pp. 110-128), scanned PDF: equations"
  - "[[PHY1 Ch06 Fig 6.16.png]]"
  - "[[PHY1 Ch06 Fig 6.18.png]]"
  - "[[PHY1 Ch06 Fig 6.20.png]]"
  - "[[PHY1 Ch06 Problem 6.90 graph.png]]"
created: 2026-10-27
questions: "[[PHY1 HW Ch06 Questions]]"
up: "[[PHY1 Index]]"
format: "physics-notes 1.1"
---
> [!note] 符號與公式
> - 式號照課本：定力 $W = F_{x}\Delta x$ (6.1)、$W = F\,\Delta r\cos\theta$ (6.2)、$W = \vec{F} \cdot \Delta\vec{r}$ (6.5)，**只限定力、直線位移**；純量積 $\vec{A} \cdot \vec{B} = AB\cos\theta$ (6.3) $= A_{x}B_{x} + A_{y}B_{y} + A_{z}B_{z}$ (6.4)。
> - 變力：$W = \int F(x)\,dx$ (6.8)；一般 $W = \int \vec{F} \cdot d\vec{r}$ (6.11)，沿指定路徑。彈簧：從原長拉 $x$，$W = \tfrac{1}{2}kx^{2}$ (6.10)。對抗重力：$W = mgh$，地表附近、與路徑無關。
> - $K = \tfrac{1}{2}mv^{2}$ (6.13)；$\Delta K = W_{\mathrm{net}}$ (6.14)，**淨力**作的功。
> - 功率：$\bar{P} = \Delta W/\Delta t$ (6.15)，$P = dW/dt$ (6.16)；$W = P\,\Delta t$ (6.17) **只限功率固定**；$W = \int P\,dt$ (6.18)；$P = \vec{F} \cdot \vec{v}$ (6.19)。
> - 正方向在各題第一行說明（多半沿運動方向或沿斜面向上），高度 $y$ 向上為正。$g = 9.8\ \mathrm{m/s^2}$；KSU、SIU 的題目用 $9.80\ \mathrm{m/s^2}$。中間值多留一位有效數字。

## 答案總表

| 題目 | 答案 |
| --- | --- |
| [[PHY1 HW Ch06 Questions#EUP 6.11\|EUP 6.11]] | $1.3\ \mathrm{kJ}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.12\|EUP 6.12]] | $5.7 \times 10^{2}\ \mathrm{J}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.16\|EUP 6.16]] | $\tfrac{11}{10}mgh$ |
| [[PHY1 HW Ch06 Questions#EUP 6.49\|EUP 6.49]] | (a) $4.0 \times 10^{2}\ \mathrm{J}$；(b) $31\ \mathrm{kg}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.51\|EUP 6.51]] | $25^{\circ}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.18\|EUP 6.18]] | $1.6 \times 10^{2}\ \mathrm{J}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.20\|EUP 6.20]] | (a) $60\ \mathrm{kJ}$；(b) $20\ \mathrm{kJ}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.21\|EUP 6.21]] | (a) $1.0\ \mathrm{J}$；(b) $3.0\ \mathrm{J}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.23\|EUP 6.23]] | $33\ \mathrm{cm}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.54\|EUP 6.54]] | $2.2 \times 10^{2}\ \mathrm{J}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.85\|EUP 6.85]] | (a) $\tfrac{1}{2}kL_{0}^{2} + \tfrac{1}{3}bL_{0}^{3} + \tfrac{1}{4}cL_{0}^{4} + \tfrac{1}{5}dL_{0}^{5}$；(b) $12\ \mathrm{kJ}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.25\|EUP 6.25]] | $2.2 \times 10^{9}\ \mathrm{J}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.29\|EUP 6.29]] | $42\ \mathrm{m/s}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.59\|EUP 6.59]] | $1:3$（重的那個速率是輕的 $\tfrac{1}{3}$） |
| [[PHY1 HW Ch06 Questions#EUP 6.33\|EUP 6.33]] | (a) $1 \times 10^{2}\ \mathrm{kW}$；(b) $2\ \mathrm{kW}$；(c) $80\ \mathrm{W}$（未進位：$120\ \mathrm{kW}$、$83\ \mathrm{W}$） |
| [[PHY1 HW Ch06 Questions#EUP 6.53\|EUP 6.53]] | (a) $0$；(b) $90^{\circ}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.73\|EUP 6.73]] | $0.60$ |
| [[PHY1 HW Ch06 Questions#EUP 6.55\|EUP 6.55]] | $k_{\mathrm{B}} = 8k_{\mathrm{A}}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.56\|EUP 6.56]] | (a) $37.2\ \mathrm{J}$；(b) $16.8\ \mathrm{J}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.58\|EUP 6.58]] | 證明 |
| [[PHY1 HW Ch06 Questions#EUP 6.86\|EUP 6.86]] | 證明 |
| [[PHY1 HW Ch06 Questions#EUP 6.87\|EUP 6.87]] | $135\ \mathrm{J}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.88\|EUP 6.88]] | (a) $90\ \mathrm{J}$；(b) $360\ \mathrm{J}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.91\|EUP 6.91]] | 約 $4\ \mathrm{kN}$，約腿重的 31 倍 |
| [[PHY1 HW Ch06 Questions#EUP 6.72\|EUP 6.72]] | $7.2^{\circ}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.75\|EUP 6.75]] | (a) $49.1\ \mathrm{W}$；(b) $1.38\ \mathrm{kJ}$；(c) $58.0\ \mathrm{W}$、$1.63\ \mathrm{kJ}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.89\|EUP 6.89]] | 29 人 |
| [[PHY1 HW Ch06 Questions#EUP 6.81\|EUP 6.81]] | 證明：$W = P_{0}t_{0}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.82\|EUP 6.82]] | $v = \sqrt{2Pt/M}$；$x = \tfrac{2}{3}\sqrt{2P/M}\,t^{3/2}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.90\|EUP 6.90]] | 約 $2.1\ \mathrm{J}$ |
| [[PHY1 HW Ch06 Questions#EUP 6.92 to 6.95\|EUP 6.92 to 6.95]] | c、c、a、c |
| [[PHY1 HW Ch06 Questions#KSUS 3.1 to 3.3\|KSUS 3.1 to 3.3]] | c、a、b |
| [[PHY1 HW Ch06 Questions#KSUS 3.4\|KSUS 3.4]] | a) $-$；b) $+$；c) $0$；d) 見解答 |
| [[PHY1 HW Ch06 Questions#KSUS 3.6 and 3.7\|KSUS 3.6 and 3.7]] | T、T |
| [[PHY1 HW Ch06 Questions#KSUF 2.19\|KSUF 2.19]] | T |
| [[PHY1 HW Ch06 Questions#SIU 26.1 and 26.2\|SIU 26.1 and 26.2]] | $25\ \mathrm{J}$；$0$ |
| [[PHY1 HW Ch06 Questions#SIU 24.1 and 24.2\|SIU 24.1 and 24.2]] | 淨功（$= \Delta K$）；$0$ |
| [[PHY1 HW Ch06 Questions#KSUS 3.5\|KSUS 3.5]] | a) $-104\ \mathrm{J}$；b) $-41.6\ \mathrm{W}$ |
| [[PHY1 HW Ch06 Questions#KSUS 3.8\|KSUS 3.8]] | a) $2.2 \times 10^{6}\ \mathrm{J}$；b) $-1.3 \times 10^{6}\ \mathrm{J}$；c) $32\ \mathrm{m/s}$ |
| [[PHY1 HW Ch06 Questions#KSUF 2.21\|KSUF 2.21]] | a) $4.00 \times 10^{5}\ \mathrm{J}$；b) $18.9\ \mathrm{m/s}$；c) $3.02 \times 10^{4}\ \mathrm{W}$ |
| [[PHY1 HW Ch06 Questions#SIU 26.5\|SIU 26.5]] | $-5.4 \times 10^{2}\ \mathrm{J}$ |

## 老師勾選：定力作功

### EUP 6.11
題目：[[PHY1 HW Ch06 Questions#EUP 6.11|EUP 6.11]]

> [!solution] 解
> 力和位移同方向。由 (6.1)，
> $$
> W = F\,\Delta x = (65\ \mathrm{N})(20\ \mathrm{m}) = 1.3\ \mathrm{kJ}
> $$

### EUP 6.12
題目：[[PHY1 HW Ch06 Questions#EUP 6.12|EUP 6.12]]

> [!solution] 解
> 等速，所以你的推力等於動摩擦力；水平地面 $n = mg$：
> $$
> F = \mu_{\mathrm{k}}mg = (0.22)(55\ \mathrm{kg})(9.8\ \mathrm{m/s^2}) = 118.6\ \mathrm{N}
> $$
> 由 (6.1)，$W = F\,\Delta x = (118.6\ \mathrm{N})(4.8\ \mathrm{m}) = 5.7 \times 10^{2}\ \mathrm{J}$。

### EUP 6.16
題目：[[PHY1 HW Ch06 Questions#EUP 6.16|EUP 6.16]]

> [!solution] 解
> 取向上為正。電梯受纜繩張力 $T$ 與重力，由牛頓第二定律：
> $$
> T - mg = m\left(\tfrac{1}{10}g\right) \implies T = \tfrac{11}{10}mg
> $$
> $T$ 固定且和位移同方向，由 (6.1)，$W = Th = \tfrac{11}{10}mgh$。

> [!warning] 不是 mgh
> 電梯在加速，纜繩的力大於重量。

### EUP 6.49
題目：[[PHY1 HW Ch06 Questions#EUP 6.49|EUP 6.49]]

> [!solution] 解
> 取沿斜面向上為正。上升 $\Delta y = 1\ \mathrm{m}$ 時，沿斜面走 $s = \Delta y/\sin 30^{\circ} = 2.0\ \mathrm{m}$。
>
> **(a)** 你的力和位移同方向，由 (6.1)，$W = Fs = (200\ \mathrm{N})(2.0\ \mathrm{m}) = 4.0 \times 10^{2}\ \mathrm{J}$。
>
> **(b)** 等速，沿斜面合力為零；$n = mg\cos\theta$：
> $$
> F = mg\sin\theta + \mu_{\mathrm{k}}mg\cos\theta
> $$
> $$
> m = \frac{F}{g(\sin\theta + \mu_{\mathrm{k}}\cos\theta)} = \frac{200\ \mathrm{N}}{(9.8\ \mathrm{m/s^2})(\sin 30^{\circ} + 0.18\cos 30^{\circ})} = 31\ \mathrm{kg}
> $$

### EUP 6.51
題目：[[PHY1 HW Ch06 Questions#EUP 6.51|EUP 6.51]]

![EUP Figure 6.18|400](../Attachments/PHY1%20Ch06%20Fig%206.18.png)

> [!solution] 解
> 由 (6.2)，$W = Td\cos\theta$：
> $$
> \cos\theta = \frac{W}{Td} = \frac{2500\ \mathrm{J}}{(120\ \mathrm{N})(23\ \mathrm{m})} = 0.906 \implies \theta = 25^{\circ}
> $$

## 老師勾選：純量積

### EUP 6.18
題目：[[PHY1 HW Ch06 Questions#EUP 6.18|EUP 6.18]]

> [!solution] 解
> 由 (6.5) 與 (6.4)，$\Delta\vec{r} = 24\hat{\imath} + 45\hat{\jmath}\ \mathrm{m}$：
> $$
> \begin{aligned}
> W &= F_{x}\Delta x + F_{y}\Delta y = (3.1\ \mathrm{N})(24\ \mathrm{m}) + (1.9\ \mathrm{N})(45\ \mathrm{m}) \\
> &= 74.4\ \mathrm{J} + 85.5\ \mathrm{J} = 1.6 \times 10^{2}\ \mathrm{J}
> \end{aligned}
> $$

## 老師勾選：變力作功與彈簧

### EUP 6.20
題目：[[PHY1 HW Ch06 Questions#EUP 6.20|EUP 6.20]]

![EUP Figure 6.16|400](../Attachments/PHY1%20Ch06%20Fig%206.16.png)

> [!solution] 解
> 由 (6.8)，功是 $F$–$x$ 圖下的面積；兩段都是三角形，$x$ 換成 m。
> - (a) $W = \tfrac{1}{2}(3000\ \mathrm{m})(40\ \mathrm{N}) = 6.0 \times 10^{4}\ \mathrm{J} = 60\ \mathrm{kJ}$。
> - (b) $W = \tfrac{1}{2}(1000\ \mathrm{m})(40\ \mathrm{N}) = 20\ \mathrm{kJ}$。

### EUP 6.21
題目：[[PHY1 HW Ch06 Questions#EUP 6.21|EUP 6.21]]

> [!solution] 解
> 由 (6.8)，從 $x_{1}$ 拉到 $x_{2}$：$W = \int_{x_{1}}^{x_{2}}kx\,dx = \tfrac{1}{2}k(x_{2}^{2} - x_{1}^{2})$。
> - (a) $W = \tfrac{1}{2}(200\ \mathrm{N/m})(0.10\ \mathrm{m})^{2} = 1.0\ \mathrm{J}$。
> - (b) $W = \tfrac{1}{2}(200\ \mathrm{N/m})\left[(0.20\ \mathrm{m})^{2} - (0.10\ \mathrm{m})^{2}\right] = 3.0\ \mathrm{J}$。

> [!warning] 第二段不是 ½k(0.10 m)²
> (6.10) 只適用於從原長拉起；第二個 $10\ \mathrm{cm}$ 的功是第一個的 3 倍。

### EUP 6.23
題目：[[PHY1 HW Ch06 Questions#EUP 6.23|EUP 6.23]]

> [!solution] 解
> 由 (6.10)，$W = \tfrac{1}{2}kx^{2}$：
> $$
> x = \sqrt{\frac{2W}{k}} = \sqrt{\frac{2(9.5\ \mathrm{J})}{175\ \mathrm{N/m}}} = 0.33\ \mathrm{m} = 33\ \mathrm{cm}
> $$

### EUP 6.54
題目：[[PHY1 HW Ch06 Questions#EUP 6.54|EUP 6.54]]

> [!solution] 解
> 由 (6.8) 與 (6.9)，
> $$
> W = \int_{0}^{6.0\ \mathrm{m}}ax^{2}\,dx = \frac{a}{3}x^{3}\Big|_{0}^{6.0\ \mathrm{m}} = \frac{3.0\ \mathrm{N/m^2}}{3}(6.0\ \mathrm{m})^{3} = 2.2 \times 10^{2}\ \mathrm{J}
> $$

### EUP 6.85
題目：[[PHY1 HW Ch06 Questions#EUP 6.85|EUP 6.85]]

> [!solution] 解
> 拉繩的力和繩的力等大反向：$F_{\mathrm{you}} = kx + bx^{2} + cx^{3} + dx^{4}$。拉到兩倍長就是伸長量從 $0$ 到 $L_{0}$。
>
> **(a)** 由 (6.8) 與 (6.9)，
> $$
> W = \int_{0}^{L_{0}}(kx + bx^{2} + cx^{3} + dx^{4})\,dx = \tfrac{1}{2}kL_{0}^{2} + \tfrac{1}{3}bL_{0}^{3} + \tfrac{1}{4}cL_{0}^{4} + \tfrac{1}{5}dL_{0}^{5}
> $$
> **(b)** $L_{0} = 10\ \mathrm{m}$：
> $$
> \begin{aligned}
> W &= \tfrac{1}{2}(420)(10)^{2} + \tfrac{1}{3}(-86)(10)^{3} + \tfrac{1}{4}(12)(10)^{4} + \tfrac{1}{5}(-0.50)(10)^{5}\ \mathrm{J} \\
> &= 21.0\ \mathrm{kJ} - 28.7\ \mathrm{kJ} + 30.0\ \mathrm{kJ} - 10.0\ \mathrm{kJ} = 12\ \mathrm{kJ}
> \end{aligned}
> $$

## 老師勾選：動能與功–動能定理

### EUP 6.25
題目：[[PHY1 HW Ch06 Questions#EUP 6.25|EUP 6.25]]

> [!solution] 解
> $$
> v = \left(\frac{850\ \mathrm{km}}{\mathrm{h}}\right)\left(\frac{1000\ \mathrm{m}}{1\ \mathrm{km}}\right)\left(\frac{1\ \mathrm{h}}{3600\ \mathrm{s}}\right) = 236.1\ \mathrm{m/s}
> $$
> 由 (6.13)，$K = \tfrac{1}{2}mv^{2} = \tfrac{1}{2}(7.9 \times 10^{4}\ \mathrm{kg})(236.1\ \mathrm{m/s})^{2} = 2.2 \times 10^{9}\ \mathrm{J}$。

### EUP 6.29
題目：[[PHY1 HW Ch06 Questions#EUP 6.29|EUP 6.29]]

> [!solution] 解
> 樹的力 $F$ 和鉛筆的運動反向，在 $d = 0.058\ \mathrm{m}$ 內使鉛筆從 $v$ 停下。由 (6.14)，
> $$
> -Fd = 0 - \tfrac{1}{2}mv^{2} \implies v = \sqrt{\frac{2Fd}{m}} = \sqrt{\frac{2(76\ \mathrm{N})(0.058\ \mathrm{m})}{0.0050\ \mathrm{kg}}} = 42\ \mathrm{m/s}
> $$

### EUP 6.59
題目：[[PHY1 HW Ch06 Questions#EUP 6.59|EUP 6.59]]

> [!solution] 解
> 由 (6.13)，$\tfrac{1}{2}m_{1}v_{1}^{2} = \tfrac{1}{2}m_{2}v_{2}^{2}$，所以
> $$
> \frac{v_{1}}{v_{2}} = \sqrt{\frac{m_{2}}{m_{1}}} = \sqrt{\frac{1}{9}} = \frac{1}{3}
> $$
> 質量 $9$ 的粒子速率是質量 $1$ 的 $\tfrac{1}{3}$：速率比 $1:3$。

## 老師勾選：功率

### EUP 6.33
題目：[[PHY1 HW Ch06 Questions#EUP 6.33|EUP 6.33]]

> [!solution] 解
> 由 (6.15)，$\bar{P} = E/\Delta t$，$E = 2\ \mathrm{kW \cdot h}$：
> - (a) $\bar{P} = \dfrac{2\ \mathrm{kW \cdot h}}{(1/60)\ \mathrm{h}} = 120\ \mathrm{kW} \approx 1 \times 10^{2}\ \mathrm{kW}$。
> - (b) $\bar{P} = \dfrac{2\ \mathrm{kW \cdot h}}{1\ \mathrm{h}} = 2\ \mathrm{kW}$。
> - (c) $\bar{P} = \dfrac{2\ \mathrm{kW \cdot h}}{24\ \mathrm{h}} = 0.083\ \mathrm{kW} \approx 80\ \mathrm{W}$。
>
> 「約 $2\ \mathrm{kW \cdot h}$」只有一位有效數字。

## 加選：純量積

### EUP 6.53
題目：[[PHY1 HW Ch06 Questions#EUP 6.53|EUP 6.53]]

> [!solution] 解
> **(a)** 由 (6.4)，$(a\hat{\imath} + b\hat{\jmath}) \cdot (b\hat{\imath} - a\hat{\jmath}) = ab + b(-a) = 0$。
>
> **(b)** 兩向量都不是零向量，由 (6.3)，$\cos\theta = 0$，$\theta = 90^{\circ}$。

## 加選：定力作功

### EUP 6.73
題目：[[PHY1 HW Ch06 Questions#EUP 6.73|EUP 6.73]]

> [!solution] 解
> 等速，推力 $F$ 沿斜面向上，等於重力沿斜面分量加摩擦力；$n = mg\cos\theta$。由 (6.1)，$W = Fd$：
> $$
> \frac{W}{d} = mg\sin\theta + \mu mg\cos\theta \implies \mu = \frac{W/(mgd) - \sin\theta}{\cos\theta}
> $$
> $$
> \frac{W}{mgd} = \frac{2.2 \times 10^{3}\ \mathrm{J}}{(78\ \mathrm{kg})(9.8\ \mathrm{m/s^2})(3.1\ \mathrm{m})} = 0.928, \qquad \mu = \frac{0.928 - \sin 22^{\circ}}{\cos 22^{\circ}} = 0.60
> $$

> [!warning] 推力不只對抗摩擦
> 在斜坡上，推力還要平衡重力沿斜面的分量 $mg\sin\theta$。

## 加選：變力作功與彈簧

### EUP 6.55
題目：[[PHY1 HW Ch06 Questions#EUP 6.55|EUP 6.55]]

> [!solution] 解
> 由 (6.10)，$W_{\mathrm{A}} = \tfrac{1}{2}k_{\mathrm{A}}x^{2}$，$W_{\mathrm{B}} = \tfrac{1}{2}k_{\mathrm{B}}\left(\tfrac{1}{2}x\right)^{2} = \tfrac{1}{8}k_{\mathrm{B}}x^{2}$。$W_{\mathrm{B}} = 2W_{\mathrm{A}}$：
> $$
> \tfrac{1}{8}k_{\mathrm{B}}x^{2} = k_{\mathrm{A}}x^{2} \implies k_{\mathrm{B}} = 8k_{\mathrm{A}}
> $$

### EUP 6.56
題目：[[PHY1 HW Ch06 Questions#EUP 6.56|EUP 6.56]]

> [!solution] 解
> 由 (6.8) 與 (6.9)，
> $$
> W = \int_{x_{1}}^{x_{2}}\left(a\sqrt{x} - bx^{2}\right)dx = \left[\tfrac{2}{3}ax^{3/2} - \tfrac{1}{3}bx^{3}\right]_{x_{1}}^{x_{2}}
> $$
> - (a) $W = \tfrac{2}{3}(25.2)(2.00)^{3/2}\ \mathrm{J} - \tfrac{1}{3}(3.87)(2.00)^{3}\ \mathrm{J} = 47.5\ \mathrm{J} - 10.3\ \mathrm{J} = 37.2\ \mathrm{J}$。
> - (b) $W = \tfrac{2}{3}(25.2)\left[(3.75)^{3/2} - (2.00)^{3/2}\right]\ \mathrm{J} - \tfrac{1}{3}(3.87)\left[(3.75)^{3} - (2.00)^{3}\right]\ \mathrm{J} = 74.5\ \mathrm{J} - 57.7\ \mathrm{J} = 16.8\ \mathrm{J}$。

> [!warning] 力在途中變號
> $F = 0$ 在 $x = (a/b)^{2/3} = 3.49\ \mathrm{m}$；之後力反向、作負功。積分自動把正負相加，不能用端點的力相乘。

## 加選：功與路徑

### EUP 6.58
題目：[[PHY1 HW Ch06 Questions#EUP 6.58|EUP 6.58]]

> [!solution] 解
> 慢慢拉，所以 $\Delta K = 0$，由 (6.14) 淨功為零：$W_{\mathrm{you}} + W_{\mathrm{g}} + W_{T} = 0$。鏈的張力沿半徑、垂直於圓弧運動，$W_{T} = 0$。妹妹上升 $h = L - L\cos\varphi$，重力作功 $W_{\mathrm{g}} = -mgh$（6.3 節）。所以
> $$
> W_{\mathrm{you}} = mgh = mgL(1 - \cos\varphi) \qquad \blacksquare
> $$

### EUP 6.86
題目：[[PHY1 HW Ch06 Questions#EUP 6.86|EUP 6.86]]

> [!solution] 解
> 從圓心看，$\theta$ 由最低點量起；$h < R$，物體在下半圈。慢慢推，$v^{2}/R \approx 0$，徑向方程式給 $n - mg\cos\theta = 0$，所以摩擦力 $f = \mu mg\cos\theta$，沿弧長 $ds = R\,d\theta$。由 (6.11)，對抗摩擦的功
> $$
> W = \int_{0}^{\theta_{\mathrm{f}}}\mu mg\cos\theta\,R\,d\theta = \mu mgR\sin\theta_{\mathrm{f}}
> $$
> 高度 $h = R - R\cos\theta_{\mathrm{f}}$，所以 $R\sin\theta_{\mathrm{f}} = \sqrt{R^{2} - (R - h)^{2}} = \sqrt{2hR - h^{2}}$：
> $$
> W = \mu mg\sqrt{2hR - h^{2}} \qquad \blacksquare
> $$

### EUP 6.87
題目：[[PHY1 HW Ch06 Questions#EUP 6.87|EUP 6.87]]

> [!solution] 解
> 由 (6.11)，$\vec{F} \cdot d\vec{r} = cxy\,dx + d\,dy$。沿曲線把 $y = ax^{2} - bx$ 代入第一項：
> $$
> \begin{aligned}
> W &= c\int_{0}^{3\ \mathrm{m}}x(ax^{2} - bx)\,dx + d\int_{0}^{6\ \mathrm{m}}dy = c\left[\tfrac{1}{4}ax^{4} - \tfrac{1}{3}bx^{3}\right]_{0}^{3\ \mathrm{m}} + d(6\ \mathrm{m}) \\
> &= (10\ \mathrm{N/m^2})(40.5\ \mathrm{m^3} - 36\ \mathrm{m^3}) + (15\ \mathrm{N})(6\ \mathrm{m}) = 45\ \mathrm{J} + 90\ \mathrm{J} = 135\ \mathrm{J}
> \end{aligned}
> $$

### EUP 6.88
題目：[[PHY1 HW Ch06 Questions#EUP 6.88|EUP 6.88]]

> [!solution] 解
> 沿 $x$ 方向的段 $dy = 0$，只剩 $cxy\,dx$；沿 $y$ 方向的段 $dx = 0$，只剩 $d\,dy$。
>
> **(a)** 沿 $x$ 軸 $y = 0$，功為 $0$；再沿 $x = 3\ \mathrm{m}$ 往上：$(15\ \mathrm{N})(6\ \mathrm{m}) = 90\ \mathrm{J}$。$W = 90\ \mathrm{J}$。
>
> **(b)** 沿 $y$ 軸：$(15\ \mathrm{N})(6\ \mathrm{m}) = 90\ \mathrm{J}$；再沿 $y = 6\ \mathrm{m}$ 往右：
> $$
> \int_{0}^{3\ \mathrm{m}}c(6\ \mathrm{m})x\,dx = (10\ \mathrm{N/m^2})(6\ \mathrm{m})\tfrac{1}{2}(3\ \mathrm{m})^{2} = 270\ \mathrm{J}
> $$
> $W = 90\ \mathrm{J} + 270\ \mathrm{J} = 360\ \mathrm{J}$。三條路徑的功（$135$、$90$、$360\ \mathrm{J}$）都不同：這個力的功與路徑有關。

## 加選：功–動能定理

### EUP 6.91
題目：[[PHY1 HW Ch06 Questions#EUP 6.91|EUP 6.91]]

> [!solution] 解
> 取向下為正；從開始落下到停下，$\Delta K = 0$。重力作功 $mg(h + d)$，地板的平均力 $\bar{F}$ 只在最後 $d$ 內作功 $-\bar{F}d$。由 (6.14)，
> $$
> mg(h + d) - \bar{F}d = 0 \implies \bar{F} = mg\left(1 + \frac{h}{d}\right)
> $$
> $$
> \bar{F} = (14\ \mathrm{kg})(9.8\ \mathrm{m/s^2})\left(1 + \frac{0.6\ \mathrm{m}}{0.02\ \mathrm{m}}\right) = 4 \times 10^{3}\ \mathrm{N}
> $$
> 約 $4\ \mathrm{kN}$，是腿重 $140\ \mathrm{N}$ 的 31 倍。

> [!warning] 撞擊力不是重量
> 停下的距離越短，平均力越大：$\bar{F} \approx mg\,h/d$。

## 加選：功率與速度

### EUP 6.72
題目：[[PHY1 HW Ch06 Questions#EUP 6.72|EUP 6.72]]

> [!solution] 解
> 等速，驅動輪推車的力 $F = F_{\mathrm{air}} + mg\sin\theta$；$v = 60\ \mathrm{km/h} = 16.67\ \mathrm{m/s}$。由 (6.19)，$P = Fv$：
> $$
> \begin{aligned}
> \sin\theta &= \frac{P/v - F_{\mathrm{air}}}{mg} = \frac{(38 \times 10^{3}\ \mathrm{W})/(16.67\ \mathrm{m/s}) - 550\ \mathrm{N}}{(1400\ \mathrm{kg})(9.8\ \mathrm{m/s^2})} \\
> &= \frac{2280\ \mathrm{N} - 550\ \mathrm{N}}{13{,}720\ \mathrm{N}} = 0.126
> \end{aligned}
> $$
> $\theta = 7.2^{\circ}$。

### EUP 6.75
題目：[[PHY1 HW Ch06 Questions#EUP 6.75|EUP 6.75]]

> [!solution] 解
> 等速，推力等於阻力，和運動同方向；$P = Fv$ (6.19)，$W = Fd$ (6.1)。
>
> 水平：$F = \mu mg = (0.595)(68.5\ \mathrm{kg})(9.8\ \mathrm{m/s^2}) = 399.4\ \mathrm{N}$。
> - (a) $P = (399.4\ \mathrm{N})(0.123\ \mathrm{m/s}) = 49.1\ \mathrm{W}$。
> - (b) $W = (399.4\ \mathrm{N})(3.45\ \mathrm{m}) = 1.38\ \mathrm{kJ}$。
>
> **(c)** 斜坡：$n = mg\cos\theta$，
> $$
> \begin{aligned}
> F &= mg(\sin\theta + \mu\cos\theta) \\
> &= (68.5\ \mathrm{kg})(9.8\ \mathrm{m/s^2})(\sin 6.35^{\circ} + 0.595\cos 6.35^{\circ}) = 471.2\ \mathrm{N}
> \end{aligned}
> $$
> $P = (471.2\ \mathrm{N})(0.123\ \mathrm{m/s}) = 58.0\ \mathrm{W}$，$W = (471.2\ \mathrm{N})(3.45\ \mathrm{m}) = 1.63\ \mathrm{kJ}$。

### EUP 6.89
題目：[[PHY1 HW Ch06 Questions#EUP 6.89|EUP 6.89]]

> [!solution] 解
> 車廂重量由配重平衡，馬達只抬 $N$ 個人；等速上升，$F = Nmg$。$v = 1010\ \mathrm{m/min} = 16.83\ \mathrm{m/s}$。由 (6.19)，$P = Nmgv$：
> $$
> N = \frac{P}{mgv} = \frac{330 \times 10^{3}\ \mathrm{W}}{(67\ \mathrm{kg})(9.8\ \mathrm{m/s^2})(16.83\ \mathrm{m/s})} = 29.9
> $$
> 最多 29 人（30 人就超過馬達功率）。

## 加選：隨時間變化的功率

### EUP 6.81
題目：[[PHY1 HW Ch06 Questions#EUP 6.81|EUP 6.81]]

> [!solution] 解
> 由 (6.18)，
> $$
> W = \int_{0}^{\infty}\frac{P_{0}t_{0}^{2}}{(t + t_{0})^{2}}\,dt = P_{0}t_{0}^{2}\left[-\frac{1}{t + t_{0}}\right]_{0}^{\infty} = P_{0}t_{0}^{2}\left(0 + \frac{1}{t_{0}}\right) = P_{0}t_{0} \qquad \blacksquare
> $$

### EUP 6.82
題目：[[PHY1 HW Ch06 Questions#EUP 6.82|EUP 6.82]]

> [!solution] 解
> 功率全部變成動能，由 (6.17) 與 (6.14)，從靜止：$\tfrac{1}{2}Mv^{2} = Pt$，所以
> $$
> v = \sqrt{\frac{2Pt}{M}}, \qquad x = \int_{0}^{t}v\,dt = \sqrt{\frac{2P}{M}}\int_{0}^{t}t^{1/2}\,dt = \frac{2}{3}\sqrt{\frac{2P}{M}}\,t^{3/2}
> $$

> [!warning] 功率固定不是力固定
> $F = P/v$ 隨速率增加而變小，等加速度公式不能用。

## 加選：數據題

### EUP 6.90
題目：[[PHY1 HW Ch06 Questions#EUP 6.90|EUP 6.90]]

> [!solution] 解
> 由 (6.8)，功是 $F$–$x$ 圖下的面積。相鄰兩點連直線，用梯形求面積，$\Delta x = 5.00\ \mathrm{cm} = 0.0500\ \mathrm{m}$：
> $$
> \begin{aligned}
> W &= \Delta x\left[\tfrac{1}{2}(F_{0} + F_{8}) + F_{1} + F_{2} + \cdots + F_{7}\right] \\
> &= (0.0500\ \mathrm{m})\left[\tfrac{1}{2}(0 + 12.7\ \mathrm{N}) + 34.915\ \mathrm{N}\right] = 2.06\ \mathrm{J} \approx 2.1\ \mathrm{J}
> \end{aligned}
> $$
>
> ![EUP 6.90 graph|480](../Attachments/PHY1%20Ch06%20Problem%206.90%20graph.png)

## 加選：讀功率–時間圖

### EUP 6.92 to 6.95
題目：[[PHY1 HW Ch06 Questions#EUP 6.92 to 6.95|EUP 6.92 to 6.95]]

![EUP Figure 6.20|480](../Attachments/PHY1%20Ch06%20Fig%206.20.png)

> [!solution] 解
> 縱軸是功率 $P = dW/dt$，就是動能增加的速率。
> - **92.** c. 峰值是功率最大；動能、速率和總功在功率回到零之前都還在增加。
> - **93.** c. 功率為正時動能一直增加，到 $185\ \mathrm{ms}$ 功率回到零，速率最大。
> - **94.** a. 由 (6.18)，$\Delta K$ 是曲線下面積；每格 $(0.01\ \mathrm{s})(1\ \mathrm{kW}) = 10\ \mathrm{J}$，約 57 格，約 $5.7 \times 10^{2}\ \mathrm{J}$。
> - **95.** c. $P = Fv$，峰值處 $\dfrac{dP}{dt} = \dfrac{dF}{dt}v + Fa = 0$；球在加速，$Fa > 0$，所以 $\dfrac{dF}{dt} < 0$：力在峰值時已經在減小，最大值在峰值之前。

## 外校考題：觀念題

### KSUS 3.1 to 3.3
題目：[[PHY1 HW Ch06 Questions#KSUS 3.1 to 3.3|KSUS 3.1 to 3.3]]

> [!solution] 解
> - **1.** c. 由 (6.2)，$\cos 90^{\circ} = 0$。
> - **2.** a. 重力向下、位移向上：$W = -mgh = -(600\ \mathrm{N})(20\ \mathrm{m}) = -12\ \mathrm{kJ}$。速率 $2.0\ \mathrm{m/s}$ 用不到。
> - **3.** b. 動能增加，所以淨力的功率 $\vec{F} \cdot \vec{v} > 0$ (6.19)：$\vec{v}$ 要有 $+x$ 分量，選項中只有 $+\hat{\imath}$。

### KSUS 3.4
題目：[[PHY1 HW Ch06 Questions#KSUS 3.4|KSUS 3.4]]

> [!solution] 解
> - a) $-$：摩擦力和運動反向。
> - b) $+$：重力和位移都向下。
> - c) $0$：正向力垂直於地面，鞋子踩地時也沒有沿正向力方向的位移。
> - d) 依課本 6.2 節，位移是**施力點**的位移：輪胎著地點不滑動，靜摩擦作功 $0$。但這份考卷的第 8 題把 $f_{\mathrm{s}}$ 當成推動整台車的力，算成作正功 $f_{\mathrm{s}}d$（和 Example 6.9 單車的算法一樣），所以考卷預期的答案可能是 $+$。

> [!warning] 兩種看法
> 嚴格說，車加速的能量來自引擎，不是路面。考試遇到時，寫清楚你用的是哪種看法。

### KSUS 3.6 and 3.7
題目：[[PHY1 HW Ch06 Questions#KSUS 3.6 and 3.7|KSUS 3.6 and 3.7]]

> [!solution] 解
> - **6.** T. $\Delta K = W_{\mathrm{net}}$ (6.14)。
> - **7.** T. $P = \dfrac{1\ \mathrm{J}}{1 \times 10^{-6}\ \mathrm{s}} = 1 \times 10^{6}\ \mathrm{W} = 1\ \mathrm{MW}$。

### KSUF 2.19
題目：[[PHY1 HW Ch06 Questions#KSUF 2.19|KSUF 2.19]]

> [!solution] 解
> T。力與位移大小固定時，$W = F\,\Delta r\cos\theta$ (6.2) 在 $\theta = 0$ 最大。

### SIU 26.1 and 26.2
題目：[[PHY1 HW Ch06 Questions#SIU 26.1 and 26.2|SIU 26.1 and 26.2]]

> [!solution] 解
> - **1.** 由 (6.13)，$v^{2} = v_{x}^{2} + v_{y}^{2}$：$K = \tfrac{1}{2}(2.0\ \mathrm{kg})\left[(4.0\ \mathrm{m/s})^{2} + (3.0\ \mathrm{m/s})^{2}\right] = 25\ \mathrm{J}$。
> - **2.** $0$。重力作的功只和起點、終點的位置有關，與路徑無關；太空人從地表出發、回到地表，總功為零。

### SIU 24.1 and 24.2
題目：[[PHY1 HW Ch06 Questions#SIU 24.1 and 24.2|SIU 24.1 and 24.2]]

> [!solution] 解
> - **1.** 淨功。由牛頓第二定律 $m\vec{a} = \vec{F}_{\mathrm{net}}$，所以 $\int m\vec{a} \cdot d\vec{r} = \int \vec{F}_{\mathrm{net}} \cdot d\vec{r} = W_{\mathrm{net}}$ (6.11)，由 (6.14) 也等於 $\Delta K$。
> - **2.** $0$。正向力處處垂直於曲面，也就垂直於運動方向，$\vec{n} \cdot d\vec{r} = 0$。

## 外校考題：計算題

### KSUS 3.5
題目：[[PHY1 HW Ch06 Questions#KSUS 3.5|KSUS 3.5]]

> [!solution] 解
> $\Delta\vec{r} = \vec{r}_{2} - \vec{r}_{1} = (8.00\hat{\imath} - 15.0\hat{\jmath})\ \mathrm{m}$。
>
> **a)** 由 (6.5) 與 (6.4)，$W = (32.0\ \mathrm{N})(8.00\ \mathrm{m}) + (24.0\ \mathrm{N})(-15.0\ \mathrm{m}) = 256\ \mathrm{J} - 360\ \mathrm{J} = -104\ \mathrm{J}$。
>
> **b)** 由 (6.15)，$\bar{P} = \dfrac{W}{\Delta t} = \dfrac{-104\ \mathrm{J}}{2.50\ \mathrm{s}} = -41.6\ \mathrm{W}$。

### KSUS 3.8
題目：[[PHY1 HW Ch06 Questions#KSUS 3.8|KSUS 3.8]]

> [!solution] 解
> 取沿坡向上為正，$d = 500\ \mathrm{m}$；照考卷的模型，$f_{\mathrm{s}}$ 沿坡向上推公車。
>
> **a)** $W_{\mathrm{f}} = f_{\mathrm{s}}d = 0.24mgd = 0.24(1900\ \mathrm{kg})(9.80\ \mathrm{m/s^2})(500\ \mathrm{m}) = 2.2 \times 10^{6}\ \mathrm{J}$
>
> **b)** $W_{\mathrm{g}} = -mgd\sin 8.0^{\circ} = -(1900\ \mathrm{kg})(9.80\ \mathrm{m/s^2})(500\ \mathrm{m})(\sin 8.0^{\circ}) = -1.3 \times 10^{6}\ \mathrm{J}$
>
> **c)** 正向力不作功。由 (6.14)，$\tfrac{1}{2}mv^{2} = \tfrac{1}{2}mv_{0}^{2} + W_{\mathrm{f}} + W_{\mathrm{g}}$：
> $$
> \begin{aligned}
> v &= \sqrt{v_{0}^{2} + \frac{2(W_{\mathrm{f}} + W_{\mathrm{g}})}{m}} \\
> &= \sqrt{(8.0\ \mathrm{m/s})^{2} + \frac{2(2.234 \times 10^{6}\ \mathrm{J} - 1.296 \times 10^{6}\ \mathrm{J})}{1900\ \mathrm{kg}}} = 32\ \mathrm{m/s}
> \end{aligned}
> $$

### KSUF 2.21
題目：[[PHY1 HW Ch06 Questions#KSUF 2.21|KSUF 2.21]]

> [!solution] 解
> 取沿坡向上為正，$d = 125\ \mathrm{m}$。正向力和重力的垂直分量抵消，合力
> $$
> \begin{aligned}
> F_{\mathrm{net}} &= F_{\mathrm{road}} - mg\sin 15.0^{\circ} \\
> &= 8880\ \mathrm{N} - (2240\ \mathrm{kg})(9.80\ \mathrm{m/s^2})(\sin 15.0^{\circ}) = 3198\ \mathrm{N}
> \end{aligned}
> $$
> **a)** $W_{\mathrm{net}} = F_{\mathrm{net}}d = (3198\ \mathrm{N})(125\ \mathrm{m}) = 4.00 \times 10^{5}\ \mathrm{J}$
>
> **b)** 由 (6.14)，從靜止：$v = \sqrt{\dfrac{2W_{\mathrm{net}}}{m}} = \sqrt{\dfrac{2(4.00 \times 10^{5}\ \mathrm{J})}{2240\ \mathrm{kg}}} = 18.9\ \mathrm{m/s}$
>
> **c)** 等加速，$\Delta t = \dfrac{2d}{v} = \dfrac{2(125\ \mathrm{m})}{18.9\ \mathrm{m/s}} = 13.2\ \mathrm{s}$。由 (6.15)，$\bar{P} = \dfrac{4.00 \times 10^{5}\ \mathrm{J}}{13.2\ \mathrm{s}} = 3.02 \times 10^{4}\ \mathrm{W}$。

> [!warning] 哪個功率
> (c) 接 (a) 的「所有力」，取淨功。只算 $F_{\mathrm{road}}$ 的話是 $(8.88\ \mathrm{kN})(125\ \mathrm{m})/(13.2\ \mathrm{s}) = 84\ \mathrm{kW}$。

### SIU 26.5
題目：[[PHY1 HW Ch06 Questions#SIU 26.5|SIU 26.5]]

> [!solution] 解
> 正向力垂直於運動，不作功；重力作功 $mgh$（與曲面形狀無關）。由 (6.14)，$mgh + W_{\mathrm{f}} = \tfrac{1}{2}mv^{2} - 0$：
> $$
> \begin{aligned}
> W_{\mathrm{f}} &= \tfrac{1}{2}mv^{2} - mgh \\
> &= \tfrac{1}{2}(25\ \mathrm{kg})(4.0\ \mathrm{m/s})^{2} - (25\ \mathrm{kg})(9.80\ \mathrm{m/s^2})(3.0\ \mathrm{m}) \\
> &= 200\ \mathrm{J} - 735\ \mathrm{J} = -5.4 \times 10^{2}\ \mathrm{J}
> \end{aligned}
> $$
