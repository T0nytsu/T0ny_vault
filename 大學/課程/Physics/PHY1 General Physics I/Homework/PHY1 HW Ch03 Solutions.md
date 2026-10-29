---
course: [PHY1]
semester: "115-1"
chapter: ["3.1", "3.2", "3.3", "3.4", "3.5", "3.6"]
tags: [physics, homework, solutions, kinematics]
source:
  - "Own solutions; every number recomputed with Python, symbolic results with sympy"
  - "EUP Ch. 3 (pp. 50-69), scanned PDF: equations and answers to GOT IT? questions"
  - "[[PHY1 Ch03 Fig 3.24.png]]"
  - "[[PHY1 Ch03 Fig 3.25.png]]"
  - "[[PHY1 Ch03 Fig 3.26.png]]"
  - "[[PHY1 Ch03 Fig 3.27.png]]"
  - "[[PHY1 Ch03 Fig 3.28.png]]"
  - "[[PHY1 Ch03 Problem 3.73 path.png]]"
created: 2026-10-29
questions: "[[PHY1 HW Ch03 Questions]]"
up: "[[PHY1 Index]]"
format: "physics-notes 1.1"
---
> [!note] 符號與公式
> - 式號照課本：大小與方向 $A = \sqrt{A_{x}^{2} + A_{y}^{2}}$、$\tan\theta = A_{y}/A_{x}$ (3.1)；分量 $A_{x} = A\cos\theta$、$A_{y} = A\sin\theta$ (3.2)，$\theta$ 從 $+x$ 軸逆時針量起；平均速度 $\Delta\vec{r}/\Delta t$ (3.3)、瞬時速度 $d\vec{r}/dt$ (3.4)、平均加速度 $\Delta\vec{v}/\Delta t$ (3.5)、瞬時加速度 $d\vec{v}/dt$ (3.6)；相對速度 $\vec{v} = \vec{v}' + \vec{V}$ (3.7)。
> - **加速度為常數時** $\vec{v} = \vec{v}_{0} + \vec{a}t$ (3.8)、$\vec{r} = \vec{r}_{0} + \vec{v}_{0}t + \tfrac{1}{2}\vec{a}t^{2}$ (3.9)。拋體 $v_{x} = v_{x0}$ (3.10)、$v_{y} = v_{y0} - gt$ (3.11)、$x = x_{0} + v_{x0}t$ (3.12)、$y = y_{0} + v_{y0}t - \tfrac{1}{2}gt^{2}$ (3.13)，**只在地表附近、忽略空氣阻力**；軌跡 $y = x\tan\theta_{0} - \frac{g}{2v_{0}^{2}\cos^{2}\theta_{0}}x^{2}$ (3.14)，原點在發射點；水平射程 $x = \frac{v_{0}^{2}}{g}\sin 2\theta_{0}$ (3.15)，**只限落回發射高度**。
> - 等速圓周運動 $a = v^{2}/r$ (3.16)，指向圓心，**不是等加速度**；非等速時徑向 $a_{r} = v^{2}/r$、切向 $a_{t} = dv/dt$。
> - $y$ 一律鉛直向上為正；地圖方向取 $x$ 向東、$y$ 向北。$g = 9.8\ \mathrm{m/s^2}$；KSU、SIU 的題目用 $9.80\ \mathrm{m/s^2}$。中間值多留一位有效數字。

## 答案總表

| 題目 | 答案 |
| --- | --- |
| [[PHY1 HW Ch03 Questions#EUP 3.14\|EUP 3.14]] | $5.0\ \mathrm{m}$，左方偏下 $37^{\circ}$（從 $+x$ 軸量起 $217^{\circ}$） |
| [[PHY1 HW Ch03 Questions#EUP 3.16\|EUP 3.16]] | $64\ \mathrm{m}$；$61^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.17\|EUP 3.17]] | (a) $\sqrt{2} = 1.41$；(b) $45^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.19\|EUP 3.19]] | $135^{\circ}$ 或 $-45^{\circ}$（$315^{\circ}$） |
| [[PHY1 HW Ch03 Questions#EUP 3.21\|EUP 3.21]] | $+x$ 方向（$\vec{a} = 3ct^{2}\hat{\imath}$） |
| [[PHY1 HW Ch03 Questions#EUP 3.23\|EUP 3.23]] | (a) $-2.2 \times 10^{-6}\hat{\jmath}\ \mathrm{m/s}$；(b) $-3.2 \times 10^{-10}\hat{\imath}\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.55\|EUP 3.55]] | (a) $t = \dfrac{4c}{3d}$；(b) $t = \dfrac{c}{3d}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.27\|EUP 3.27]] | (a) 偏上游 $26^{\circ}$；(b) $54\ \mathrm{s}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.31\|EUP 3.31]] | $45\ \mathrm{m}$，與原方向夾 $6.5^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.63\|EUP 3.63]] | $0.50\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.64\|EUP 3.64]] | (a) $16\ \mathrm{s}$；(b) $3.2 \times 10^{2}\ \mathrm{m}$；(c) $25\ \mathrm{m/s}$，從 $+x$ 軸量起 $116^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.35\|EUP 3.35]] | $3.4 \times 10^{-8}\ \mathrm{m}$（$34\ \mathrm{nm}$） |
| [[PHY1 HW Ch03 Questions#EUP 3.37\|EUP 3.37]] | $1.0\ \mathrm{km}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.66\|EUP 3.66]] | $v_{0} = \sqrt{\dfrac{g(R^{2} + 16h^{2})}{8h}}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.72\|EUP 3.72]] | $\vec{v}_{0} = 6.4\hat{\imath} + 10\hat{\jmath}\ \mathrm{m/s}$（$12\ \mathrm{m/s}$，仰角 $58^{\circ}$） |
| [[PHY1 HW Ch03 Questions#EUP 3.77\|EUP 3.77]] | $30^{\circ}$ 或 $67^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.83\|EUP 3.83]] | $2h$ |
| [[PHY1 HW Ch03 Questions#EUP 3.39\|EUP 3.39]] | $2.59 \times 10^{-7}\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.54\|EUP 3.54]] | $233\ \mathrm{km/h}$，吹向東偏北 $44^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.60\|EUP 3.60]] | (a) 偏上游 $\sin^{-1}(V/v')$；(b) 無解，到不了正對岸 |
| [[PHY1 HW Ch03 Questions#EUP 3.58\|EUP 3.58]] | (a) $10\hat{\imath} - 21\hat{\jmath}\ \mathrm{m/s}$；(b) $13\ \mathrm{m/s}$；(c) $89^{\circ}$；(d) $at = 43\ \mathrm{m/s}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.59\|EUP 3.59]] | (a) $0.249\ \mathrm{m/s}$；(b) $7.00 \times 10^{-4}\ \mathrm{m/s^2}$；(c) 瞬時 $7.21 \times 10^{-4}\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.75\|EUP 3.75]] | 至少 $45\ \mathrm{km/h}$，不能斷定超速 |
| [[PHY1 HW Ch03 Questions#EUP 3.84\|EUP 3.84]] | $110\ \mathrm{km}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.78\|EUP 3.78]] | (a) $2\sqrt{(2 - \sqrt{2})gh}$；(b) $67.5^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.86\|EUP 3.86]] | $7.2\ \mathrm{m/s}$，仰角 $77^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.82\|EUP 3.82]] | $89\ \mathrm{m/s}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.94\|EUP 3.94]] | $26.6^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.85\|EUP 3.85]] | $20\ \mathrm{m}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.88\|EUP 3.88]] | 水平以下 $38^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.90\|EUP 3.90]] | $34^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.81\|EUP 3.81]] | $63.4\ \mathrm{m}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.93\|EUP 3.93]] | (a) $a_{t}\sqrt{1 + \pi^{2}} = 3.30a_{t}$；(b) $252^{\circ}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.73\|EUP 3.73]] | 半徑 $2.50\ \mathrm{m}$ 的半圓；$6.54\ \mathrm{m/s}$；$17.1\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch03 Questions#EUP 3.95 to 3.98\|EUP 3.95 to 3.98]] | c, a, c, d |
| [[PHY1 HW Ch03 Questions#KSUS 2.1 to 2.3\|KSUS 2.1 to 2.3]] | b, b, b |
| [[PHY1 HW Ch03 Questions#KSUS 2.9\|KSUS 2.9]] | d |
| [[PHY1 HW Ch03 Questions#SIU 1.4\|SIU 1.4]] | $25\ \mathrm{m/s}$，水平 |
| [[PHY1 HW Ch03 Questions#SIU 2.1\|SIU 2.1]] | 垂直指向地軸（與指向地心的方向夾 $38^{\circ}$）；$0.027\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch03 Questions#KSUS 2.8\|KSUS 2.8]] | a) 東偏南 $36.9^{\circ}$；b) $75\ \mathrm{s}$ |
| [[PHY1 HW Ch03 Questions#KSUS 2.10\|KSUS 2.10]] | a) $(6.12, 13.1)\ \mathrm{m/s}$；b) $8.80\ \mathrm{m}$ |
| [[PHY1 HW Ch03 Questions#KSUF 1.5\|KSUF 1.5]] | a) $(12.0\hat{\imath} + 17.8\hat{\jmath})\ \mathrm{m/s}$；b) $43.6\ \mathrm{m}$ |
| [[PHY1 HW Ch03 Questions#KSUF 1.6\|KSUF 1.6]] | $126\ \mathrm{km/h}$ |
| [[PHY1 HW Ch03 Questions#SIU 1.6\|SIU 1.6]] | $5.00\ \mathrm{m}$，從 $+x$ 軸逆時針 $120^{\circ}$ |
| [[PHY1 HW Ch03 Questions#SIU 1.7\|SIU 1.7]] | $1.4 \times 10^{2}\ \mathrm{m}$ |

## 老師勾選：向量運算

### EUP 3.14
題目：[[PHY1 HW Ch03 Questions#EUP 3.14|EUP 3.14]]

> [!solution] 答案
> $x$ 向右、$y$ 向上：$\vec{C} = -(\vec{A} + \vec{B}) = -4.0\hat{\imath} - 3.0\hat{\jmath}\ \mathrm{m}$。由 (3.1)，
> $$
> C = \sqrt{(4.0\ \mathrm{m})^{2} + (3.0\ \mathrm{m})^{2}} = 5.0\ \mathrm{m}, \qquad \tan^{-1}\frac{3.0}{4.0} = 37^{\circ}
> $$
> 兩分量都負：$\vec{C}$ 指向左下，在左方（$-x$）下方 $37^{\circ}$，即從 $+x$ 軸量起 $217^{\circ}$。

### EUP 3.16
題目：[[PHY1 HW Ch03 Questions#EUP 3.16|EUP 3.16]]

> [!solution] 答案
> 由 (3.1)，
> $$
> A = \sqrt{(31\ \mathrm{m})^{2} + (56\ \mathrm{m})^{2}} = 64\ \mathrm{m}, \qquad \theta = \tan^{-1}\frac{56}{31} = 61^{\circ}
> $$
> 兩分量都正，在第一象限：與 $+x$ 軸夾 $61^{\circ}$。

### EUP 3.17
題目：[[PHY1 HW Ch03 Questions#EUP 3.17|EUP 3.17]]

> [!solution] 答案
> 由 (3.1)：
> - (a) $\lvert \hat{\imath} + \hat{\jmath} \rvert = \sqrt{1^{2} + 1^{2}} = \sqrt{2} = 1.41$（單位向量沒有單位）。
> - (b) $\tan\theta = 1/1$，$\theta = 45^{\circ}$。

## 老師勾選：速度與加速度向量

### EUP 3.19
題目：[[PHY1 HW Ch03 Questions#EUP 3.19|EUP 3.19]]

> [!solution] 答案
> 由 (3.1)，$\tan\theta = v_{y}/v_{x} = -1$。$v_{x} < 0$、$v_{y} > 0$ 在第二象限；$v_{x} > 0$、$v_{y} < 0$ 在第四象限：
> $$
> \theta = 135^{\circ} \quad \text{or} \quad \theta = -45^{\circ}\ (= 315^{\circ})
> $$

> [!warning] 反正切只給一個角
> 計算機的 $\tan^{-1}(-1)$ 只給 $-45^{\circ}$；相差 $180^{\circ}$ 的 $135^{\circ}$ 也滿足 $\tan\theta = -1$，要自己補上。

### EUP 3.21
題目：[[PHY1 HW Ch03 Questions#EUP 3.21|EUP 3.21]]

> [!solution] 答案
> 由 (3.6)，
> $$
> \vec{a} = \frac{d\vec{v}}{dt} = 3ct^{2}\hat{\imath}
> $$
> （$d$ 是常數，微分為零）。$c > 0$，所以 $t \ne 0$ 時加速度指向 $+x$ 方向；$t = 0$ 時 $\vec{a} = \vec{0}$。

### EUP 3.23
題目：[[PHY1 HW Ch03 Questions#EUP 3.23|EUP 3.23]]

> [!solution] 答案
> $R = 2.4\ \mathrm{cm}$，$\Delta t = 6.0\ \mathrm{h} = 2.16 \times 10^{4}\ \mathrm{s}$。中午尖端在 12：$\vec{r}_{1} = R\hat{\jmath}$；下午 6 點在 6：$\vec{r}_{2} = -R\hat{\jmath}$。
>
> **(a)** 由 (3.3)，
> $$
> \bar{\vec{v}} = \frac{\vec{r}_{2} - \vec{r}_{1}}{\Delta t} = \frac{-2(2.4\ \mathrm{cm})\hat{\jmath}}{6.0\ \mathrm{h}} = -0.80\hat{\jmath}\ \mathrm{cm/h} = -2.2 \times 10^{-6}\hat{\jmath}\ \mathrm{m/s}
> $$
> **(b)** 時針 $12\ \mathrm{h}$ 轉一圈，尖端速率 $v = \dfrac{2\pi R}{12\ \mathrm{h}} = 1.26\ \mathrm{cm/h}$。中午在 12 往 3 走：$\vec{v}_{1} = v\hat{\imath}$；下午 6 點在 6 往 9 走：$\vec{v}_{2} = -v\hat{\imath}$。由 (3.5)，
> $$
> \bar{\vec{a}} = \frac{\vec{v}_{2} - \vec{v}_{1}}{\Delta t} = \frac{-2(1.26\ \mathrm{cm/h})\hat{\imath}}{6.0\ \mathrm{h}} = -0.42\hat{\imath}\ \mathrm{cm/h^2} = -3.2 \times 10^{-10}\hat{\imath}\ \mathrm{m/s^2}
> $$

### EUP 3.55
題目：[[PHY1 HW Ch03 Questions#EUP 3.55|EUP 3.55]]

> [!solution] 答案
> 由 (3.4)，
> $$
> \vec{v} = \frac{d\vec{r}}{dt} = (2ct - 6dt^{2})\hat{\imath} + (4ct - 3dt^{2})\hat{\jmath}
> $$
> - (a) 沿 $x$ 方向運動：$v_{y} = t(4c - 3dt) = 0$，$t > 0$ 給 $t = \dfrac{4c}{3d}$。此時 $v_{x} = -\dfrac{8c^{2}}{d} \ne 0$，往 $-x$ 方向。
> - (b) 沿 $y$ 方向運動：$v_{x} = 2t(c - 3dt) = 0$，$t = \dfrac{c}{3d}$。此時 $v_{y} = \dfrac{c^{2}}{d} > 0$，往 $+y$ 方向。

> [!warning] 另一個分量不能也是零
> 「沿 $x$ 方向運動」要 $v_{y} = 0$ 且 $v_{x} \ne 0$；兩個根都要代回去確認。

## 老師勾選：相對運動

### EUP 3.27
題目：[[PHY1 HW Ch03 Questions#EUP 3.27|EUP 3.27]]

> [!solution] 答案
> $x$ 沿水流、$y$ 指向對岸。由 (3.7)，$\vec{v} = \vec{v}' + \vec{V}$，要 $\vec{v}$ 只有 $y$ 分量。船頭從正對岸偏上游 $\varphi$，$x$ 分量 $-v'\sin\varphi + V = 0$：
> $$
> \varphi = \sin^{-1}\frac{V}{v'} = \sin^{-1}\frac{0.57\ \mathrm{m/s}}{1.3\ \mathrm{m/s}} = 26^{\circ}
> $$
> - (a) 船頭朝上游，偏離正對岸 $26^{\circ}$。
> - (b) 過河速率 $v = \sqrt{v'^{2} - V^{2}} = \sqrt{(1.3\ \mathrm{m/s})^{2} - (0.57\ \mathrm{m/s})^{2}} = 1.17\ \mathrm{m/s}$，$t = \dfrac{63\ \mathrm{m}}{1.17\ \mathrm{m/s}} = 54\ \mathrm{s}$。

## 老師勾選：二維等加速度運動

### EUP 3.31
題目：[[PHY1 HW Ch03 Questions#EUP 3.31|EUP 3.31]]

> [!solution] 答案
> $x$ 沿原方向，原點在陣風開始處：$v_{x0} = 6.5\ \mathrm{m/s}$、$v_{y0} = 0$，$a_{x} = (0.53\ \mathrm{m/s^2})\cos 35^{\circ}$、$a_{y} = (0.53\ \mathrm{m/s^2})\sin 35^{\circ}$。由 (3.9)，$t = 5.8\ \mathrm{s}$：
> $$
> \begin{aligned}
> x &= v_{x0}t + \tfrac{1}{2}a_{x}t^{2} = 37.7\ \mathrm{m} + 7.30\ \mathrm{m} = 45.0\ \mathrm{m} \\
> y &= \tfrac{1}{2}a_{y}t^{2} = 5.11\ \mathrm{m}
> \end{aligned}
> $$
> $$
> r = \sqrt{x^{2} + y^{2}} = 45\ \mathrm{m}, \qquad \theta = \tan^{-1}\frac{5.11\ \mathrm{m}}{45.0\ \mathrm{m}} = 6.5^{\circ}
> $$
> 位移 $45\ \mathrm{m}$，與原方向夾 $6.5^{\circ}$，偏向加速度那一側。

> [!warning] 位移方向不是加速度方向
> 加速度與原方向夾 $35^{\circ}$，但初速度很大，位移只偏了 $6.5^{\circ}$。

### EUP 3.63
題目：[[PHY1 HW Ch03 Questions#EUP 3.63|EUP 3.63]]

> [!solution] 答案
> 原點在加速開始處。$x$ 方向等速、$y$ 方向由 $v_{y0} = 0$ 等加速，由 (3.9)，$x = v_{x0}t$、$y = \tfrac{1}{2}at^{2}$。令 $x = y$：
> $$
> v_{x0}t = \tfrac{1}{2}at^{2} \implies a = \frac{2v_{x0}}{t} = \frac{2(5.5\ \mathrm{m/s})}{22\ \mathrm{s}} = 0.50\ \mathrm{m/s^2}
> $$

### EUP 3.64
題目：[[PHY1 HW Ch03 Questions#EUP 3.64|EUP 3.64]]

> [!solution] 答案
> 由 (3.9)，$\vec{r}_{0} = \vec{0}$：$x = v_{x0}t + \tfrac{1}{2}a_{x}t^{2}$，$y = v_{y0}t + \tfrac{1}{2}a_{y}t^{2}$。
>
> **(a)** 穿過 $y$ 軸時 $x = 0$：$t\left(v_{x0} + \tfrac{1}{2}a_{x}t\right) = 0$，捨去出發時的 $t = 0$：
> $$
> t = -\frac{2v_{x0}}{a_{x}} = -\frac{2(11\ \mathrm{m/s})}{-1.4\ \mathrm{m/s^2}} = 15.7\ \mathrm{s} \approx 16\ \mathrm{s}
> $$
> **(b)** $y = (18\ \mathrm{m/s})(15.7\ \mathrm{s}) + \tfrac{1}{2}(0.27\ \mathrm{m/s^2})(15.7\ \mathrm{s})^{2} = 283\ \mathrm{m} + 33\ \mathrm{m} = 3.2 \times 10^{2}\ \mathrm{m}$。
>
> **(c)** 由 (3.8)，$v_{x} = 11\ \mathrm{m/s} + (-1.4\ \mathrm{m/s^2})(15.7\ \mathrm{s}) = -11\ \mathrm{m/s}$，$v_{y} = 18\ \mathrm{m/s} + (0.27\ \mathrm{m/s^2})(15.7\ \mathrm{s}) = 22.2\ \mathrm{m/s}$：
> $$
> v = \sqrt{(11\ \mathrm{m/s})^{2} + (22.2\ \mathrm{m/s})^{2}} = 25\ \mathrm{m/s}, \qquad \theta = 180^{\circ} - \tan^{-1}\frac{22.2}{11} = 116^{\circ}
> $$
> 從 $+x$ 軸量起 $116^{\circ}$：往 $-x$、$+y$（第二象限）。

## 老師勾選：拋體運動

### EUP 3.35
題目：[[PHY1 HW Ch03 Questions#EUP 3.35|EUP 3.35]]

> [!solution] 答案
> 水平等速，由 (3.12)，$t = \dfrac{x}{v_{x0}} = \dfrac{1.0 \times 10^{-3}\ \mathrm{m}}{12\ \mathrm{m/s}} = 8.33 \times 10^{-5}\ \mathrm{s}$。鉛直由 $v_{y0} = 0$ 落下，由 (3.13)，
> $$
> \Delta y = \tfrac{1}{2}gt^{2} = \tfrac{1}{2}(9.8\ \mathrm{m/s^2})(8.33 \times 10^{-5}\ \mathrm{s})^{2} = 3.4 \times 10^{-8}\ \mathrm{m} = 34\ \mathrm{nm}
> $$

### EUP 3.37
題目：[[PHY1 HW Ch03 Questions#EUP 3.37|EUP 3.37]]

> [!solution] 答案
> 初速與仰角相同，球落回擊出的高度，由 (3.15)，射程 $x \propto 1/g$：
> $$
> x_{\mathrm{M}} = x_{\mathrm{E}}\frac{g_{\mathrm{E}}}{g_{\mathrm{M}}} = (170\ \mathrm{m})\frac{9.8\ \mathrm{m/s^2}}{1.62\ \mathrm{m/s^2}} = 1.0 \times 10^{3}\ \mathrm{m} = 1.0\ \mathrm{km}
> $$

> [!warning] 題目沒給月球的 g
> 要用附錄 E 的 $g_{\mathrm{M}} = 1.62\ \mathrm{m/s^2}$（約地球的六分之一）。

### EUP 3.66
題目：[[PHY1 HW Ch03 Questions#EUP 3.66|EUP 3.66]]

> [!solution] 答案
> 鉛直：最高點 $v_{y} = 0$，由 (3.11)、(3.13)，$v_{y0} = \sqrt{2gh}$，飛行時間 $T = \dfrac{2v_{y0}}{g}$。水平：由 (3.12)，$v_{x0} = \dfrac{R}{T} = \dfrac{gR}{2\sqrt{2gh}}$。
> $$
> v_{0} = \sqrt{v_{x0}^{2} + v_{y0}^{2}} = \sqrt{\frac{gR^{2}}{8h} + 2gh} = \sqrt{\frac{g(R^{2} + 16h^{2})}{8h}}
> $$

### EUP 3.72
題目：[[PHY1 HW Ch03 Questions#EUP 3.72|EUP 3.72]]

![EUP Figure 3.24|300](../Attachments/PHY1%20Ch03%20Fig%203.24.png)

> [!solution] 答案
> 能量棒到同伴時水平運動，表示同伴在軌跡的最高點。原點在你手上：$\Delta x = (8.6\ \mathrm{m})\cos 39^{\circ} = 6.68\ \mathrm{m}$，$\Delta y = (8.6\ \mathrm{m})\sin 39^{\circ} = 5.41\ \mathrm{m}$。最高點 $v_{y} = 0$，由 (3.11)、(3.13)：
> $$
> v_{y0} = \sqrt{2g\,\Delta y} = \sqrt{2(9.8\ \mathrm{m/s^2})(5.41\ \mathrm{m})} = 10.3\ \mathrm{m/s}, \qquad t = \frac{v_{y0}}{g} = 1.05\ \mathrm{s}
> $$
> 由 (3.12)，$v_{x0} = \dfrac{\Delta x}{t} = \dfrac{6.68\ \mathrm{m}}{1.05\ \mathrm{s}} = 6.36\ \mathrm{m/s}$：
> $$
> \vec{v}_{0} = 6.4\hat{\imath} + 10\hat{\jmath}\ \mathrm{m/s}
> $$
> 即大小 $12\ \mathrm{m/s}$、仰角 $\tan^{-1}(10.3/6.36) = 58^{\circ}$。

### EUP 3.77
題目：[[PHY1 HW Ch03 Questions#EUP 3.77|EUP 3.77]]

> [!solution] 答案
> 原點在出手點：$x = 4.5\ \mathrm{m}$，$y = 3.05\ \mathrm{m} - 2.5\ \mathrm{m} = 0.55\ \mathrm{m}$，$v_{0} = 8\ \mathrm{m/s}$。(3.14) 用 $\dfrac{1}{\cos^{2}\theta} = 1 + \tan^{2}\theta$ 改寫成 $\tan\theta$ 的二次式：
> $$
> \frac{gx^{2}}{2v_{0}^{2}}\tan^{2}\theta - x\tan\theta + \left(\frac{gx^{2}}{2v_{0}^{2}} + y\right) = 0
> $$
> $\dfrac{gx^{2}}{2v_{0}^{2}} = \dfrac{(9.8\ \mathrm{m/s^2})(4.5\ \mathrm{m})^{2}}{2(8\ \mathrm{m/s})^{2}} = 1.55\ \mathrm{m}$：
> $$
> (1.55\ \mathrm{m})\tan^{2}\theta - (4.5\ \mathrm{m})\tan\theta + 2.10\ \mathrm{m} = 0 \implies \tan\theta = 0.584 \ \text{or}\ 2.32
> $$
> $\theta = 30^{\circ}$ 或 $67^{\circ}$。

> [!warning] 兩個根都是答案
> 低弧線 $30^{\circ}$ 和高弧線 $67^{\circ}$ 都會通過籃框中心，兩個都要寫。

### EUP 3.83
題目：[[PHY1 HW Ch03 Questions#EUP 3.83|EUP 3.83]]

> [!solution] 答案
> 鉛直上拋到 $h$：最高點 $v_{y} = 0$，由 (3.11)、(3.13)，$v_{0}^{2} = 2gh$。同一速率在 $45^{\circ}$ 射程最大，由 (3.15)，
> $$
> x_{\max} = \frac{v_{0}^{2}}{g}\sin 90^{\circ} = \frac{2gh}{g} = 2h
> $$

## 老師勾選：等速圓周運動

### EUP 3.39
題目：[[PHY1 HW Ch03 Questions#EUP 3.39|EUP 3.39]]

> [!solution] 答案
> 分針 $T = 60\ \mathrm{min} = 3600\ \mathrm{s}$ 轉一圈，尖端做等速圓周運動，$v = 2\pi r/T$。由 (3.16)，
> $$
> a = \frac{v^{2}}{r} = \frac{4\pi^{2}r}{T^{2}} = \frac{4\pi^{2}(0.0850\ \mathrm{m})}{(3600\ \mathrm{s})^{2}} = 2.59 \times 10^{-7}\ \mathrm{m/s^2}
> $$

## 加選：相對運動

### EUP 3.54
題目：[[PHY1 HW Ch03 Questions#EUP 3.54|EUP 3.54]]

> [!solution] 答案
> $x$ 向東、$y$ 向北。對地速度正南：$v = \dfrac{1280\ \mathrm{km}}{(115/60)\ \mathrm{h}} = 668\ \mathrm{km/h}$，$\vec{v} = -668\hat{\jmath}\ \mathrm{km/h}$。對空速度南偏西 $11.5^{\circ}$：
> $$
> \vec{v}' = -(846\ \mathrm{km/h})\sin 11.5^{\circ}\,\hat{\imath} - (846\ \mathrm{km/h})\cos 11.5^{\circ}\,\hat{\jmath} = -169\hat{\imath} - 829\hat{\jmath}\ \mathrm{km/h}
> $$
> 由 (3.7)，$\vec{V} = \vec{v} - \vec{v}' = 169\hat{\imath} + 161\hat{\jmath}\ \mathrm{km/h}$：
> $$
> V = \sqrt{(169\ \mathrm{km/h})^{2} + (161\ \mathrm{km/h})^{2}} = 233\ \mathrm{km/h}, \qquad \theta = \tan^{-1}\frac{161}{169} = 44^{\circ}
> $$
> 風速 $233\ \mathrm{km/h}$，吹向東偏北 $44^{\circ}$（從西南方吹來）。

### EUP 3.60
題目：[[PHY1 HW Ch03 Questions#EUP 3.60|EUP 3.60]]

> [!solution] 答案
> $x$ 沿水流、$y$ 指向正對岸。船頭從正對岸偏上游 $\theta$，由 (3.7)，$x$ 分量 $-v'\sin\theta + V = 0$：
> - (a) $\theta = \sin^{-1}\dfrac{V}{v'}$，偏向上游。
> - (b) $V > v'$ 時 $\sin\theta > 1$，無解：不論船頭朝哪裡都會被沖向下游，到不了正對岸。

## 加選：速度變化與平均加速度

### EUP 3.58
題目：[[PHY1 HW Ch03 Questions#EUP 3.58|EUP 3.58]]

> [!solution] 答案
> **(a)** 由 (3.8)，
> $$
> \vec{v}_{0} = \vec{v} - \vec{a}t = (33 - 23)\hat{\imath} + (15 - 36)\hat{\jmath}\ \mathrm{m/s} = 10\hat{\imath} - 21\hat{\jmath}\ \mathrm{m/s}
> $$
> **(b)** 由 (3.1)，$v_{0} = \sqrt{10^{2} + 21^{2}}\ \mathrm{m/s} = 23.3\ \mathrm{m/s}$，$v = \sqrt{33^{2} + 15^{2}}\ \mathrm{m/s} = 36.2\ \mathrm{m/s}$：速率增加 $13\ \mathrm{m/s}$。
>
> **(c)** $\theta_{0} = \tan^{-1}(-21/10) = -64.5^{\circ}$，$\theta = \tan^{-1}(15/33) = 24.4^{\circ}$：方向逆時針轉了 $89^{\circ}$。
>
> **(d)** $at = \sqrt{2.3^{2} + 3.6^{2}}\ \mathrm{m/s^2} \times 10\ \mathrm{s} = 43\ \mathrm{m/s} \ne 13\ \mathrm{m/s}$。$at = \lvert\Delta\vec{v}\rvert$ 是速度**向量**變化的大小；$\vec{a}$ 不平行於速度，一部分加速度用來改變方向，所以速率的改變 $\lvert\vec{v}\rvert - \lvert\vec{v}_{0}\rvert$ 較小。

### EUP 3.59
題目：[[PHY1 HW Ch03 Questions#EUP 3.59|EUP 3.59]]

> [!solution] 答案
> $R = 91.5\ \mathrm{m}$，$T = 37.3\ \mathrm{min} = 2238\ \mathrm{s}$，$\Delta t = 300\ \mathrm{s}$ 內轉過 $\Delta\theta = 360^{\circ} \times \dfrac{5.00}{37.3} = 48.3^{\circ}$。位置向量與速度向量的大小不變、方向都轉了 $\Delta\theta$，所以 $\lvert\Delta\vec{r}\rvert = 2R\sin(\Delta\theta/2)$、$\lvert\Delta\vec{v}\rvert = 2v\sin(\Delta\theta/2)$。
> - (a) 由 (3.3)，$\bar{v} = \dfrac{2(91.5\ \mathrm{m})\sin 24.1^{\circ}}{300\ \mathrm{s}} = \dfrac{74.8\ \mathrm{m}}{300\ \mathrm{s}} = 0.249\ \mathrm{m/s}$。
> - (b) $v = \dfrac{2\pi R}{T} = 0.257\ \mathrm{m/s}$；由 (3.5)，$\bar{a} = \dfrac{2(0.257\ \mathrm{m/s})\sin 24.1^{\circ}}{300\ \mathrm{s}} = 7.00 \times 10^{-4}\ \mathrm{m/s^2}$。
> - (c) 由 (3.16)，瞬時加速度 $a = \dfrac{v^{2}}{R} = 7.21 \times 10^{-4}\ \mathrm{m/s^2}$，大小固定、指向圓心；平均值是它的 $97\%$，因為 $\lvert\Delta\vec{v}\rvert$（弦）比弧長 $v\,\Delta\theta$ 短。

## 加選：拋體運動

### EUP 3.75
題目：[[PHY1 HW Ch03 Questions#EUP 3.75|EUP 3.75]]

> [!solution] 答案
> 把騎士當成從路面拋出的拋體。由 (3.15)，射程 $16\ \mathrm{m}$ 所需的速率在 $45^{\circ}$ 最小：
> $$
> v_{\min} = \sqrt{gx} = \sqrt{(9.8\ \mathrm{m/s^2})(16\ \mathrm{m})} = 12.5\ \mathrm{m/s} = 45\ \mathrm{km/h}
> $$
> 這只說明他至少有 $45\ \mathrm{km/h}$，低於速限 $50\ \mathrm{km/h}$；不能據此斷定他超速。

> [!warning] 只能給下限
> 實際的拋出角不是 $45^{\circ}$ 時需要更大的速率，所以落地距離只給出速率的下限；這裡忽略了座位的高度與空氣阻力。

### EUP 3.84
題目：[[PHY1 HW Ch03 Questions#EUP 3.84|EUP 3.84]]

> [!solution] 答案
> 由 (3.15)，最大射程在 $45^{\circ}$：$x_{\max} = v_{0}^{2}/g$。鉛直發射到最高點 $v = 0$，由 (3.11)、(3.13)，
> $$
> h = \frac{v_{0}^{2}}{2g} = \frac{x_{\max}}{2} = \frac{220\ \mathrm{km}}{2} = 110\ \mathrm{km}
> $$

### EUP 3.78
題目：[[PHY1 HW Ch03 Questions#EUP 3.78|EUP 3.78]]

> [!solution] 答案
> 原點在桌緣。最高點在桌面上方 $h$：$v_{y0} = \sqrt{2gh}$，上升時間 $t_{1} = \sqrt{2h/g}$。從最高點（離地 $2h$）由 $v_{y} = 0$ 落到地板：$t_{2} = \sqrt{4h/g} = 2\sqrt{h/g}$。由 (3.12)，
> $$
> v_{x0} = \frac{2h}{t_{1} + t_{2}} = \frac{2h}{(2 + \sqrt{2})\sqrt{h/g}} = (2 - \sqrt{2})\sqrt{gh}
> $$
> - (a) $v_{0} = \sqrt{v_{x0}^{2} + v_{y0}^{2}} = \sqrt{gh}\sqrt{(2 - \sqrt{2})^{2} + 2} = 2\sqrt{(2 - \sqrt{2})gh} \approx 1.53\sqrt{gh}$。
> - (b) $\tan\theta = \dfrac{v_{y0}}{v_{x0}} = \dfrac{\sqrt{2}}{2 - \sqrt{2}} = 1 + \sqrt{2}$，$\theta = 67.5^{\circ}$（$\tan 67.5^{\circ} = 1 + \sqrt{2}$）。

> [!warning] 上升和下降時間不同
> 落點比發射點低 $h$，下降段從離地 $2h$ 落下，不能把上升時間乘 2。

### EUP 3.86
題目：[[PHY1 HW Ch03 Questions#EUP 3.86|EUP 3.86]]

> [!solution] 答案
> 原點在跳板末端。最高點在跳板上方 $2.5\ \mathrm{m}$：$v_{y0} = \sqrt{2(9.8\ \mathrm{m/s^2})(2.5\ \mathrm{m})} = 7.0\ \mathrm{m/s}$，上升 $t_{1} = v_{y0}/g = 0.714\ \mathrm{s}$。從最高點（水面上方 $3\ \mathrm{m} + 2.5\ \mathrm{m} = 5.5\ \mathrm{m}$）落下：$t_{2} = \sqrt{2(5.5\ \mathrm{m})/(9.8\ \mathrm{m/s^2})} = 1.06\ \mathrm{s}$。由 (3.12)，
> $$
> v_{x0} = \frac{2.8\ \mathrm{m}}{0.714\ \mathrm{s} + 1.06\ \mathrm{s}} = 1.58\ \mathrm{m/s}
> $$
> $$
> v_{0} = \sqrt{(1.58\ \mathrm{m/s})^{2} + (7.0\ \mathrm{m/s})^{2}} = 7.2\ \mathrm{m/s}, \qquad \theta = \tan^{-1}\frac{7.0}{1.58} = 77^{\circ}
> $$

### EUP 3.82
題目：[[PHY1 HW Ch03 Questions#EUP 3.82|EUP 3.82]]

![EUP Figure 3.26|460](../Attachments/PHY1%20Ch03%20Fig%203.26.png)

> [!solution] 答案
> 由圖 3.26：從地面以 $70^{\circ}$ 發射，落在水平距離 $390\ \mathrm{m}$、高 $270\ \mathrm{m}$ 的岩架上。原點在發射點、$x$ 指向岩架，由 (3.14) 解 $v_{0}$：
> $$
> \begin{aligned}
> v_{0} &= \sqrt{\frac{gx^{2}}{2\cos^{2}\theta_{0}\,(x\tan\theta_{0} - y)}} \\
> &= \sqrt{\frac{(9.8\ \mathrm{m/s^2})(390\ \mathrm{m})^{2}}{2\cos^{2}70^{\circ}\,(1072\ \mathrm{m} - 270\ \mathrm{m})}} = 89\ \mathrm{m/s}
> \end{aligned}
> $$

### EUP 3.94
題目：[[PHY1 HW Ch03 Questions#EUP 3.94|EUP 3.94]]

> [!solution] 答案
> 由 (3.15)，$R = \dfrac{2v_{0}^{2}\sin\theta\cos\theta}{g}$，所以 $\dfrac{g}{2v_{0}^{2}\cos^{2}\theta} = \dfrac{\tan\theta}{R}$，(3.14) 成為 $y = x\tan\theta - \dfrac{\tan\theta}{R}x^{2}$。代入 $x = 2R$、$y = -R$：
> $$
> -R = 2R\tan\theta - 4R\tan\theta = -2R\tan\theta \implies \tan\theta = \tfrac{1}{2}, \quad \theta = 26.6^{\circ}
> $$

## 加選：斜坡與最佳發射角

### EUP 3.85
題目：[[PHY1 HW Ch03 Questions#EUP 3.85|EUP 3.85]]

> [!solution] 答案
> 平地：由 (3.15)，$v_{0}^{2} = \dfrac{gR}{\sin 2\theta}$，$R = 33\ \mathrm{m}$，$\theta = 37^{\circ}$。坡面上的落點是軌跡 (3.14) 與坡面 $y = x\tan\alpha$（$\alpha = 17^{\circ}$）的交點：
> $$
> x\tan\alpha = x\tan\theta - \frac{gx^{2}}{2v_{0}^{2}\cos^{2}\theta} \implies x = \frac{2v_{0}^{2}\cos^{2}\theta}{g}(\tan\theta - \tan\alpha)
> $$
> 代入 $v_{0}^{2}$，用 $\sin 2\theta = 2\sin\theta\cos\theta$：
> $$
> x = R\left(1 - \frac{\tan\alpha}{\tan\theta}\right) = (33\ \mathrm{m})\left(1 - \frac{\tan 17^{\circ}}{\tan 37^{\circ}}\right) = 20\ \mathrm{m}
> $$

### EUP 3.88
題目：[[PHY1 HW Ch03 Questions#EUP 3.88|EUP 3.88]]

![EUP Figure 3.27|440](../Attachments/PHY1%20Ch03%20Fig%203.27.png)

> [!solution] 答案
> 原點在跳台末端，$x$ 水平向前：$v_{x0} = (28\ \mathrm{m/s})\cos 9.5^{\circ} = 27.6\ \mathrm{m/s}$，$v_{y0} = -(28\ \mathrm{m/s})\sin 9.5^{\circ} = -4.62\ \mathrm{m/s}$。落地時 $t = \dfrac{55\ \mathrm{m}}{27.6\ \mathrm{m/s}} = 1.99\ \mathrm{s}$，由 (3.11)，
> $$
> v_{y} = -4.62\ \mathrm{m/s} - (9.8\ \mathrm{m/s^2})(1.99\ \mathrm{s}) = -24.1\ \mathrm{m/s}
> $$
> 落地速度在水平以下 $\tan^{-1}\dfrac{24.1}{27.6} = 41^{\circ}$。軌跡比地面陡 $3.0^{\circ}$，所以地面坡度為水平以下 $41^{\circ} - 3^{\circ} = 38^{\circ}$。

### EUP 3.90
題目：[[PHY1 HW Ch03 Questions#EUP 3.90|EUP 3.90]]

> [!solution] 答案
> 原點在懸崖頂，落點 $y = -h$，$h = 75\ \mathrm{m}$。(3.14) 用 $u = \tan\theta$、$1/\cos^{2}\theta = 1 + u^{2}$：
> $$
> -h = xu - \frac{gx^{2}}{2v_{0}^{2}}(1 + u^{2})
> $$
> 射程最大時 $dx/du = 0$，對 $u$ 微分得 $0 = x - \dfrac{gx^{2}}{v_{0}^{2}}u$，即 $x = \dfrac{v_{0}^{2}}{gu}$。代回上式：
> $$
> -h = \frac{v_{0}^{2}}{g} - \frac{v_{0}^{2}(1 + u^{2})}{2gu^{2}} \implies \tan\theta = \frac{v_{0}}{\sqrt{v_{0}^{2} + 2gh}}
> $$
> $$
> \tan\theta = \frac{36\ \mathrm{m/s}}{\sqrt{(36\ \mathrm{m/s})^{2} + 2(9.8\ \mathrm{m/s^2})(75\ \mathrm{m})}} = 0.685 \implies \theta = 34^{\circ}
> $$
> 懸崖高度有影響：$34^{\circ}$ 的射程 $193\ \mathrm{m}$，比 $45^{\circ}$ 的 $186\ \mathrm{m}$ 遠。

> [!warning] 45° 只對同高度成立
> (3.15) 推導時令落點 $y = 0$；從高處發射時，最佳角度小於 $45^{\circ}$。

## 加選：圓周運動

### EUP 3.81
題目：[[PHY1 HW Ch03 Questions#EUP 3.81|EUP 3.81]]

![EUP Figure 3.25|360](../Attachments/PHY1%20Ch03%20Fig%203.25.png)

> [!solution] 答案
> 由圖 3.25，車沿四分之一圓弧轉向，轉完時與卡車平行而避開；開始轉向處到卡車的距離就是圓弧半徑。速率不變，$v = 80.0\ \mathrm{km/h} = 22.2\ \mathrm{m/s}$，加速度最大 $0.795g$ 時半徑最小，由 (3.16)，
> $$
> r = \frac{v^{2}}{a} = \frac{(22.2\ \mathrm{m/s})^{2}}{(0.795)(9.8\ \mathrm{m/s^2})} = 63.4\ \mathrm{m}
> $$
> 至少要在離卡車 $63.4\ \mathrm{m}$ 處開始轉向。

### EUP 3.93
題目：[[PHY1 HW Ch03 Questions#EUP 3.93|EUP 3.93]]

> [!solution] 答案
> 從靜止沿圓周走 $s = \tfrac{1}{2}\pi R$，切向等加速度，同一維的 (2.11)：$v^{2} = 2a_{t}s = \pi a_{t}R$。由 (3.16)，徑向加速度 $a_{r} = \dfrac{v^{2}}{R} = \pi a_{t}$。
> - (a) $a = \sqrt{a_{t}^{2} + a_{r}^{2}} = a_{t}\sqrt{1 + \pi^{2}} = 3.30a_{t}$。
> - (b) 在 $(0, R)$ 逆時針運動，速度指向 $-x$：$a_{t}$ 沿速度（$-x$），$a_{r}$ 指向圓心（$-y$），$\vec{a} = -a_{t}\hat{\imath} - \pi a_{t}\hat{\jmath}$。在第三象限，從 $+x$ 軸量起 $180^{\circ} + \tan^{-1}\pi = 252^{\circ}$。

## 加選：數據題與讀圖

### EUP 3.73
題目：[[PHY1 HW Ch03 Questions#EUP 3.73|EUP 3.73]]

> [!solution] 答案
> $y$ 對 $x$ 作圖：各點落在圓心 $(0, 2.50\ \mathrm{m})$、半徑 $R = 2.50\ \mathrm{m}$ 的半圓上（最小平方圓擬合，各點到圓心的距離 $2.495$–$2.504\ \mathrm{m}$）。從圓心看，每 $0.10\ \mathrm{s}$ 轉 $15^{\circ}$：等速率的圓周運動，$1.20\ \mathrm{s}$ 走半圈。由 (3.16)，
> $$
> \begin{aligned}
> v &= \frac{\pi R}{1.20\ \mathrm{s}} = \frac{\pi(2.50\ \mathrm{m})}{1.20\ \mathrm{s}} = 6.54\ \mathrm{m/s} \\
> a &= \frac{v^{2}}{R} = \frac{(6.54\ \mathrm{m/s})^{2}}{2.50\ \mathrm{m}} = 17.1\ \mathrm{m/s^2}
> \end{aligned}
> $$
> 加速度指向圓心 $(0, 2.50\ \mathrm{m})$。
>
> ![EUP 3.73 path|360](../Attachments/PHY1%20Ch03%20Problem%203.73%20path.png)

### EUP 3.95 to 3.98
題目：[[PHY1 HW Ch03 Questions#EUP 3.95 to 3.98|EUP 3.95 to 3.98]]

![EUP Figure 3.28|300](../Attachments/PHY1%20Ch03%20Fig%203.28.png)

> [!solution] 答案
> - **95.** c. 直線最短，A 最小；C 的弧繞得最遠：C > B > A。
> - **96.** a. 三人的起點和終點相同，位移相等。
> - **97.** c. 時間相同，平均速率等於路程除以時間，順序同路程：C > B > A。
> - **98.** d. A 等速率走直線，加速度為零。B、C 等速率走圓弧，由 (3.16)，$a = v^{2}/r$：C 的路程較長，速率較大；C 的弧接近半圓，半徑接近弦長的一半，是同一條弦能有的最小半徑，B 的弧較平、半徑較大。所以 $a_{\mathrm{C}} > a_{\mathrm{B}} > a_{\mathrm{A}} = 0$。

## 外校考題：觀念題

### KSUS 2.1 to 2.3
題目：[[PHY1 HW Ch03 Questions#KSUS 2.1 to 2.3|KSUS 2.1 to 2.3]]

> [!solution] 答案
> - **1.** b. 由 (3.1)，$\sqrt{(-3.0\ \mathrm{m})^{2} + (4.0\ \mathrm{m})^{2}} = 5.0\ \mathrm{m}$。
> - **2.** b. 南偏西 $32^{\circ}$ 從正南量起，向南的分量是 $(42\ \mathrm{m/s})\cos 32^{\circ}$，沿北方的軸取負號。
> - **3.** b. 由 (3.1)，第一個力在 $\tan^{-1}(-4.0/2.0) = -63.4^{\circ}$，第二個在 $\tan^{-1}(3.0/6.0) = 26.6^{\circ}$，兩者相差 $90^{\circ}$。

> [!warning] 原卷筆誤
> 原卷第二個力也寫成 $\vec{F}_{1}$，應是 $\vec{F}_{2}$。

### KSUS 2.9
題目：[[PHY1 HW Ch03 Questions#KSUS 2.9|KSUS 2.9]]

> [!solution] 答案
> - **9.** d. $v_{0}^{2} = 2gh$，在 $45^{\circ}$ 射程最大，由 (3.15)，$x_{\max} = v_{0}^{2}/g = 2h = 56.0\ \mathrm{m}$（同 [[#EUP 3.83|EUP 3.83]]）。

### SIU 1.4
題目：[[PHY1 HW Ch03 Questions#SIU 1.4|SIU 1.4]]

> [!solution] 答案
> 最高點 $v_{y} = 0$，只剩不變的水平分量，由 (3.10)，
> $$
> v = v_{0}\cos\theta_{0} = (32\ \mathrm{m/s})\cos 40^{\circ} = 25\ \mathrm{m/s}
> $$
> 方向水平，朝拋體前進的方向。

### SIU 2.1
題目：[[PHY1 HW Ch03 Questions#SIU 2.1|SIU 2.1]]

> [!solution] 答案
> Carbondale 隨地球自轉，沿北緯 $38^{\circ}$ 的緯線圓做等速圓周運動。這個圓的圓心在地軸上，不在地心，半徑 $r = R\cos 38^{\circ}$。所以向心加速度垂直指向地軸、平行於赤道面，與指向地心的方向夾 $38^{\circ}$（偏向赤道一側）。由 (3.16)，大小
> $$
> a = \frac{4\pi^{2}R\cos\theta}{T^{2}} = \frac{4\pi^{2}(6.4 \times 10^{6}\ \mathrm{m})\cos 38^{\circ}}{(86400\ \mathrm{s})^{2}} = 0.027\ \mathrm{m/s^2}
> $$

> [!warning] 圓心不是地心
> 只有在赤道上，向心加速度才指向地心。

## 外校考題：計算題

### KSUS 2.8
題目：[[PHY1 HW Ch03 Questions#KSUS 2.8|KSUS 2.8]]

> [!solution] 答案
> $x$ 向東、$y$ 向北。由 (3.7)，$\vec{v}_{\mathrm{BS}} = \vec{v}_{\mathrm{BW}} + \vec{v}_{\mathrm{WS}}$，$\vec{v}_{\mathrm{WS}} = 3.0\hat{\jmath}\ \mathrm{m/s}$，要 $\vec{v}_{\mathrm{BS}}$ 正東。船頭從正東偏南 $\varphi$，$y$ 分量 $-(5.0\ \mathrm{m/s})\sin\varphi + 3.0\ \mathrm{m/s} = 0$。
>
> **a)** $\varphi = \sin^{-1}\dfrac{3.0}{5.0} = 36.9^{\circ}$：船頭朝東偏南 $36.9^{\circ}$（即南偏東 $53.1^{\circ}$）。
>
> **b)** $v_{\mathrm{BS}} = (5.0\ \mathrm{m/s})\cos 36.9^{\circ} = 4.0\ \mathrm{m/s}$，$t = \dfrac{300\ \mathrm{m}}{4.0\ \mathrm{m/s}} = 75\ \mathrm{s}$。

### KSUS 2.10
題目：[[PHY1 HW Ch03 Questions#KSUS 2.10|KSUS 2.10]]

> [!solution] 答案
> 原點在出手點。Nathan 在最高點接到球：$v_{y} = 0$。
>
> **a)** 由 (3.11)，$v_{0y} = gt = (9.80\ \mathrm{m/s^2})(1.34\ \mathrm{s}) = 13.1\ \mathrm{m/s}$；由 (3.12)，$v_{0x} = \dfrac{8.20\ \mathrm{m}}{1.34\ \mathrm{s}} = 6.12\ \mathrm{m/s}$。
>
> **b)** 由 (3.13)，$y = v_{0y}t - \tfrac{1}{2}gt^{2} = \tfrac{1}{2}gt^{2} = \tfrac{1}{2}(9.80\ \mathrm{m/s^2})(1.34\ \mathrm{s})^{2} = 8.80\ \mathrm{m}$。

### KSUF 1.5
題目：[[PHY1 HW Ch03 Questions#KSUF 1.5|KSUF 1.5]]

> [!solution] 答案
> 原點在開球點，$x$ 沿地面、$y$ 向上。
>
> **a)** 由 (3.10)、(3.11)：$v_{x0} = v_{x} = 12.0\ \mathrm{m/s}$，$v_{y0} = v_{y} + gt = 8.0\ \mathrm{m/s} + (9.80\ \mathrm{m/s^2})(1.00\ \mathrm{s}) = 17.8\ \mathrm{m/s}$：$\vec{v}_{0} = (12.0\hat{\imath} + 17.8\hat{\jmath})\ \mathrm{m/s}$。
>
> **b)** 落回地面 $y = 0$，由 (3.13)，$T = \dfrac{2v_{y0}}{g} = 3.63\ \mathrm{s}$；由 (3.12)，$x = v_{x0}T = (12.0\ \mathrm{m/s})(3.63\ \mathrm{s}) = 43.6\ \mathrm{m}$。

### KSUF 1.6
題目：[[PHY1 HW Ch03 Questions#KSUF 1.6|KSUF 1.6]]

> [!solution] 答案
> 由 (3.16)，令 $a = v^{2}/r = g$：
> $$
> v = \sqrt{gr} = \sqrt{(9.80\ \mathrm{m/s^2})(125\ \mathrm{m})} = 35.0\ \mathrm{m/s} = 126\ \mathrm{km/h}
> $$

### SIU 1.6
題目：[[PHY1 HW Ch03 Questions#SIU 1.6|SIU 1.6]]

> [!solution] 答案
> 由 (3.2)，$\vec{A} = -5.00\hat{\imath}\ \mathrm{m}$，$\vec{B} = (5.00\ \mathrm{m})(\cos 60^{\circ}\,\hat{\imath} + \sin 60^{\circ}\,\hat{\jmath}) = 2.50\hat{\imath} + 4.33\hat{\jmath}\ \mathrm{m}$：
> $$
> \vec{A} + \vec{B} = -2.50\hat{\imath} + 4.33\hat{\jmath}\ \mathrm{m}, \qquad \lvert\vec{A} + \vec{B}\rvert = \sqrt{(2.50\ \mathrm{m})^{2} + (4.33\ \mathrm{m})^{2}} = 5.00\ \mathrm{m}
> $$
> 在第二象限：$\theta = 180^{\circ} - \tan^{-1}\dfrac{4.33}{2.50} = 120^{\circ}$，從 $+x$ 軸逆時針量起。

### SIU 1.7
題目：[[PHY1 HW Ch03 Questions#SIU 1.7|SIU 1.7]]

> [!solution] 答案
> 槍水平指向靶心中央，子彈水平射出，$v_{y0} = 0$。由 (3.13)，落下 $0.25\ \mathrm{m}$ 的時間 $t = \sqrt{\dfrac{2(0.25\ \mathrm{m})}{9.80\ \mathrm{m/s^2}}} = 0.226\ \mathrm{s}$；由 (3.12)，
> $$
> x = v_{x0}t = (600\ \mathrm{m/s})(0.226\ \mathrm{s}) = 1.4 \times 10^{2}\ \mathrm{m}
> $$

> [!warning] 假設水平瞄準
> 原卷沒說槍是水平的；槍口與靶心等高、直接指向靶心時才是水平射出，這裡照此假設。
