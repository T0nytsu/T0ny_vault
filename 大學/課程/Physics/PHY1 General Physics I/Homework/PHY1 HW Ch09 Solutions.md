---
course: [PHY1]
semester: "115-1"
chapter: ["9.1", "9.2", "9.3", "9.4", "9.5", "9.6"]
tags: [physics, homework, solutions, momentum]
source:
  - "Own solutions; every number recomputed with Python, symbolic results with sympy"
  - "EUP Ch. 9 (pp. 166-190), scanned PDF: equations and answers to GOT IT? questions"
  - "[[PHY1 Ch09 Fig 9.6.png]]"
  - "[[PHY1 Ch09 Fig 9.24.png]]"
  - "[[PHY1 Ch09 Fig 9.26.png]]"
  - "[[PHY1 Ch09 Fig 9.27.png]]"
  - "[[PHY1 Ch09 Fig 9.28.png]]"
  - "[[PHY1 Ch09 Fig 9.30.png]]"
  - "[[PHY1 Ch09 Problem 9.92 fit.png]]"
created: 2026-10-21
questions: "[[PHY1 HW Ch09 Questions]]"
up: "[[PHY1 Index]]"
format: "physics-notes 1.1"
---
> [!note] 符號與公式
> - 式號照課本：質心 $\vec{r}_{\mathrm{cm}} = \sum m_{i}\vec{r}_{i}/M$ (9.2)、連續物體 $\vec{r}_{\mathrm{cm}} = \int \vec{r}\,dm/M$ (9.4)；系統動量 $\vec{P} = M\vec{v}_{\mathrm{cm}}$ (9.5)，**系統質量不變時**；$\vec{F}_{\mathrm{net\,ext}} = d\vec{P}/dt$ (9.6)；$\vec{P} = \text{constant}$ (9.7)，**只在淨外力為零時**（碰撞短暫、外力可忽略時近似成立）；系統動能 $K = K_{\mathrm{cm}} + K_{\mathrm{int}}$ (9.9)。
> - 衝量：$\Delta\vec{p} = \bar{\vec{F}}\Delta t$ (9.10a)、$\Delta\vec{p} = \vec{J} = \int \vec{F}\,dt$ (9.10b)，$\vec{F}$ 是**淨力**。
> - 完全非彈性碰撞：$m_{1}\vec{v}_{1} + m_{2}\vec{v}_{2} = (m_{1} + m_{2})\vec{v}_{\mathrm{f}}$ (9.11)。彈性碰撞：動量 (9.12) 與動能 (9.13)；**一維**時 $m_{1}(v_{\mathrm{1i}} - v_{\mathrm{1f}}) = m_{2}(v_{\mathrm{2f}} - v_{\mathrm{2i}})$ (9.12b)、$v_{\mathrm{1i}} - v_{\mathrm{2i}} = v_{\mathrm{2f}} - v_{\mathrm{1f}}$ (9.14)、末速度 (9.15a)、(9.15b)，以及 $K_{2}/K_{1} = 4m_{1}m_{2}/(m_{1} + m_{2})^{2}$ (9.16)，**$m_{2}$ 原本靜止時**。
> - 等加速度運動學（Ch. 2，**只限等加速度**）：$x = x_{0} + v_{0}t + \tfrac{1}{2}at^{2}$ (2.10)，$v^{2} = v_{0}^{2} + 2a(x - x_{0})$ (2.11)。
> - 一維碰撞中 $v$ 是沿所取正方向的速度分量，帶正負號。$g = 9.8\ \mathrm{m/s^2}$；KSU、SIU 的題目用 $9.80\ \mathrm{m/s^2}$。中間值多留一位有效數字。

## 答案總表

| 題目 | 答案 |
| --- | --- |
| [[PHY1 HW Ch09 Questions#EUP 9.11\|EUP 9.11]] | $2m$ |
| [[PHY1 HW Ch09 Questions#EUP 9.41\|EUP 9.41]] | 在對稱軸上、缺角的另一側，離五邊形中心 $\dfrac{a}{12\tan 36^{\circ}} \approx 0.115a$ |
| [[PHY1 HW Ch09 Questions#EUP 9.86\|EUP 9.86]] | 圓心上方 $\dfrac{2R}{\pi} \approx 0.64R$ |
| [[PHY1 HW Ch09 Questions#EUP 9.91\|EUP 9.91]] | (a) $\dfrac{M}{1 + a}$；(b) $\dfrac{1 + a}{2 + a}L$；(c) 符合：$M$ 與 $\tfrac{1}{2}L$ |
| [[PHY1 HW Ch09 Questions#EUP 9.45\|EUP 9.45]] | 老鼠的質量是碗的 $\tfrac{1}{4}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.59\|EUP 9.59]] | 相對推車 $9.0\ \mathrm{m/s}$，向右 |
| [[PHY1 HW Ch09 Questions#EUP 9.63\|EUP 9.63]] | (a) $37.7^{\circ}$ 或 $52.3^{\circ}$；(b) $0.657\ \mathrm{m/s}$ 或 $0.508\ \mathrm{m/s}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.65\|EUP 9.65]] | 爆炸後 $6.1\ \mathrm{s}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.54\|EUP 9.54]] | $(2.1\hat{\imath} - 1.5\hat{\jmath}) \times 10^{5}\ \mathrm{m/s}$：$2.6 \times 10^{5}\ \mathrm{m/s}$，在 $x$ 軸下方 $36^{\circ}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.57\|EUP 9.57]] | $(4.0\hat{\imath} + 2.8\hat{\jmath})\ \mathrm{m/s}$：$4.9\ \mathrm{m/s}$，從 $x$ 軸逆時針 $35^{\circ}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.20\|EUP 9.20]] | $3$ |
| [[PHY1 HW Ch09 Questions#EUP 9.43\|EUP 9.43]] | $K_{\mathrm{cm}} = 1.74\ \mathrm{J}$；$K_{\mathrm{int}} = 32.8\ \mathrm{J}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.22\|EUP 9.22]] | (a) $2.2 \times 10^{-4}\ \mathrm{N}$；(b) $2.6 \times 10^{-7}\ \mathrm{N \cdot s}$；(c) $2.6 \times 10^{-7}\ \mathrm{kg \cdot m/s}$；都向上 |
| [[PHY1 HW Ch09 Questions#EUP 9.60\|EUP 9.60]] | $2.9 \times 10^{-3}\ \mathrm{N}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.68\|EUP 9.68]] | $J = 17\ \mathrm{N \cdot s}$，符合規格 |
| [[PHY1 HW Ch09 Questions#EUP 9.92\|EUP 9.92]] | $h$ 對 $(J/m)^{2}$ 作圖；斜率 $0.0443\ \mathrm{s^2/m}$；$g \approx 11\ \mathrm{m/s^2}$，空氣阻力使它偏大 |
| [[PHY1 HW Ch09 Questions#EUP 9.24\|EUP 9.24]] | (a) $5.4\ \mathrm{mi/h}$；(b) $13\%$ |
| [[PHY1 HW Ch09 Questions#EUP 9.26\|EUP 9.26]] | $(10.9\hat{\imath} + 26.7\hat{\jmath})\ \mathrm{Mm/s}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.71\|EUP 9.71]] | $120^{\circ}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.49\|EUP 9.49]] | (a) $0.99\ \mathrm{m}$；(b) $3.9\ \mathrm{m/s}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.69\|EUP 9.69]] | Leaf 在速限時，休旅車 $76\ \mathrm{km/h}$；休旅車在速限時，Leaf $92\ \mathrm{km/h}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.88\|EUP 9.88]] | $0.30\ \mathrm{J}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.29\|EUP 9.29]] | $48\ \mathrm{m/s}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.72\|EUP 9.72]] | $4.00\ \mathrm{u}$；$1.08\ \mathrm{Mm/s}$，沿質子原本的方向 |
| [[PHY1 HW Ch09 Questions#EUP 9.81\|EUP 9.81]] | $\tfrac{1}{8}v$ 與 $\tfrac{7}{8}v$，都沿原方向 |
| [[PHY1 HW Ch09 Questions#EUP 9.74\|EUP 9.74]] | $A$：$\tfrac{1}{3}v$ 向左；$B$：$\tfrac{2}{9}v$、$C$：$\tfrac{8}{9}v$，向右 |
| [[PHY1 HW Ch09 Questions#EUP 9.80\|EUP 9.80]] | $9h$ |
| [[PHY1 HW Ch09 Questions#EUP 9.82\|EUP 9.82]] | $8.0\ \mathrm{s}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.76\|EUP 9.76]] | 證明 |
| [[PHY1 HW Ch09 Questions#EUP 9.78\|EUP 9.78]] | $-\tfrac{1}{5}v_{0}\hat{\imath}$；$\tfrac{3}{5}v_{0}\hat{\imath} \pm \tfrac{\sqrt{3}}{5}v_{0}\hat{\jmath}$ |
| [[PHY1 HW Ch09 Questions#EUP 9.94 to 9.97\|EUP 9.94 to 9.97]] | c, b, b, a |
| [[PHY1 HW Ch09 Questions#KSUF 3.6 to 3.8\|KSUF 3.6 to 3.8]] | T, T, F |
| [[PHY1 HW Ch09 Questions#KSUS 4.1\|KSUS 4.1]] | c |
| [[PHY1 HW Ch09 Questions#KSUS 4.4 to 4.6\|KSUS 4.4 to 4.6]] | F, F, F |
| [[PHY1 HW Ch09 Questions#KSUF 3.9\|KSUF 3.9]] | a) $12.0\ \mathrm{m/s}$，向東；b) $1.1 \times 10^{3}\ \mathrm{N}$，向東 |
| [[PHY1 HW Ch09 Questions#KSUF 3.10\|KSUF 3.10]] | a) $17\ \mathrm{m/s}$；b) $18\ \mathrm{m}$ |
| [[PHY1 HW Ch09 Questions#KSUS 4.7\|KSUS 4.7]] | a) $28\ \mathrm{m/s}$；b) $4.6 \times 10^{2}\ \mathrm{N}$ |
| [[PHY1 HW Ch09 Questions#SIUF 3.6\|SIUF 3.6]] | $245\ \mathrm{m/s}$ |
| [[PHY1 HW Ch09 Questions#SIUF 3.7\|SIUF 3.7]] | $0.67\ \mathrm{m}$ |

## 加選：離散質點的質心

### EUP 9.11
題目：[[PHY1 HW Ch09 Questions#EUP 9.11|EUP 9.11]]

> [!solution] 答案
> 取底邊為 $y = 0$，第三個頂點在高 $h$ 處，質量 $m_{3}$。由 (9.2)，
> $$
> y_{\mathrm{cm}} = \frac{m(0) + m(0) + m_{3}h}{2m + m_{3}} = \frac{h}{2} \implies 2m_{3} = 2m + m_{3} \implies m_{3} = 2m.
> $$

### EUP 9.41
題目：[[PHY1 HW Ch09 Questions#EUP 9.41|EUP 9.41]]

![EUP Figure 9.24|300](../Attachments/PHY1%20Ch09%20Fig%209.24.png)

> [!solution] 答案
> 把完整的五邊形分成五個頂點都在中心 $O$ 的全等三角形。每個的高（$O$ 到邊的中點）為 $r = \dfrac{a}{2\tan 36^{\circ}}$，由 Example 9.3，它的質心離 $O$ 為 $\tfrac{2}{3}r$。取 $y$ 沿對稱軸、背離缺角的方向，$m$ 為一個三角形的質量。完整五邊形的質心在 $O$，由 (9.2)，
> $$
> 5m(0) = 4m\,y_{\mathrm{cm}} + m\left(-\tfrac{2}{3}r\right) \implies y_{\mathrm{cm}} = \frac{r}{6} = \frac{a}{12\tan 36^{\circ}} = 0.115a.
> $$
> 質心在對稱軸上，離五邊形中心 $0.115a$，在缺角的另一側。

## 加選：用積分求質心

### EUP 9.86
題目：[[PHY1 HW Ch09 Questions#EUP 9.86|EUP 9.86]]

![EUP Figure 9.6|300](../Attachments/PHY1%20Ch09%20Fig%209.6.png)

> [!solution] 答案
> 原點在半圓圓心，$y$ 向上。$\theta$ 到 $\theta + d\theta$ 之間的一段線，$y = R\sin\theta$，$dm = \dfrac{M}{\pi R}R\,d\theta = \dfrac{M}{\pi}d\theta$。由 (9.4)，
> $$
> y_{\mathrm{cm}} = \frac{1}{M}\int y\,dm = \frac{1}{\pi}\int_{0}^{\pi} R\sin\theta\,d\theta = \frac{2R}{\pi} = 0.64R.
> $$
> 由對稱 $x_{\mathrm{cm}} = 0$：質心在圓心上方 $2R/\pi$（A 點）。

### EUP 9.91
題目：[[PHY1 HW Ch09 Questions#EUP 9.91|EUP 9.91]]

> [!solution] 答案
> **(a)**
> $$
> m = \int_{0}^{L} \mu\,dx = \frac{M}{L^{1+a}}\int_{0}^{L} x^{a}\,dx = \frac{M}{L^{1+a}} \cdot \frac{L^{1+a}}{1 + a} = \frac{M}{1 + a}.
> $$
> **(b)** 由 (9.4)，
> $$
> x_{\mathrm{cm}} = \frac{1}{m}\int_{0}^{L} x\mu\,dx = \frac{1 + a}{M} \cdot \frac{M}{L^{1+a}} \cdot \frac{L^{2+a}}{2 + a} = \frac{1 + a}{2 + a}L.
> $$
> **(c)** $a = 0$ 時 $m = M$、$x_{\mathrm{cm}} = \tfrac{1}{2}L$，正是均勻細棒的結果。

## 加選：質心不動

### EUP 9.45
題目：[[PHY1 HW Ch09 Questions#EUP 9.45|EUP 9.45]]

> [!solution] 答案
> 流理台不施水平力，老鼠落下時沒有水平速度，所以老鼠加碗的質心水平位置不變。老鼠相對碗移動 $\tfrac{1}{2}D$（碗緣到碗底），碗往反方向移動 $\tfrac{1}{10}D$，所以老鼠相對流理台移動 $\tfrac{1}{2}D - \tfrac{1}{10}D = \tfrac{2}{5}D$。由 (9.2)，$\Delta x_{\mathrm{cm}} = 0$：
> $$
> m\left(\tfrac{2}{5}D\right) - M\left(\tfrac{1}{10}D\right) = 0 \implies \frac{m}{M} = \frac{1}{4}.
> $$

> [!warning] 用對地的位移
> 老鼠的 $\tfrac{1}{2}D$ 是相對碗的；質心的式子要用相對流理台的位移。

## 加選：一維動量守恆

### EUP 9.59
題目：[[PHY1 HW Ch09 Questions#EUP 9.59|EUP 9.59]]

> [!solution] 答案
> 取 $+x$ 向右。選手加推車沒有水平外力，由 (9.7)，且她最後對地速度為 $0$：
> $$
> (55\ \mathrm{kg} + 180\ \mathrm{kg})(-6.9\ \mathrm{m/s}) = (180\ \mathrm{kg})v_{\mathrm{c}} \implies v_{\mathrm{c}} = -9.01\ \mathrm{m/s}.
> $$
> 她相對推車的速度：$0 - (-9.01\ \mathrm{m/s}) = 9.0\ \mathrm{m/s}$，向右。

> [!warning] 相對速度
> 動量守恆要用對地的速度；相對推車的速率最後才換算。

### EUP 9.63
題目：[[PHY1 HW Ch09 Questions#EUP 9.63|EUP 9.63]]

> [!solution] 答案
> 取 $+x$ 沿丟出方向；石頭（$m = 4.50\ \mathrm{kg}$）以 $v_{0} = 12.0\ \mathrm{m/s}$、仰角 $\theta$ 離手，落在丟出時的高度。冰不施水平力，由 (9.7)，你（$M = 65.0\ \mathrm{kg}$）以 $V = \dfrac{m}{M}v_{0}\cos\theta$ 反衝。石頭飛行時間 $t = \dfrac{2v_{0}\sin\theta}{g}$，兩者的距離以 $v_{0}\cos\theta + V$ 增加：
> $$
> d = \left(1 + \frac{m}{M}\right)v_{0}\cos\theta \cdot \frac{2v_{0}\sin\theta}{g} = \left(1 + \frac{m}{M}\right)\frac{v_{0}^{2}\sin 2\theta}{g}
> $$
> $$
> \sin 2\theta = \frac{gd}{(1 + m/M)v_{0}^{2}} = \frac{(9.8\ \mathrm{m/s^2})(15.2\ \mathrm{m})}{(1.0692)(12.0\ \mathrm{m/s})^{2}} = 0.9675.
> $$
> **(a)** $2\theta = 75.35^{\circ}$ 或 $104.65^{\circ}$：$\theta = 37.7^{\circ}$ 或 $52.3^{\circ}$。
>
> **(b)** $V = \dfrac{4.50\ \mathrm{kg}}{65.0\ \mathrm{kg}}(12.0\ \mathrm{m/s})\cos\theta$：$37.7^{\circ}$ 時 $0.657\ \mathrm{m/s}$，$52.3^{\circ}$ 時 $0.508\ \mathrm{m/s}$。

> [!warning] 丟的人也在動
> $15.2\ \mathrm{m}$ 是離你的距離，而石頭飛行時你也在往後滑；兩個角度都是答案。

### EUP 9.65
題目：[[PHY1 HW Ch09 Questions#EUP 9.65|EUP 9.65]]

> [!solution] 答案
> 取 $y$ 向上、地面為原點。最高點 $H = \dfrac{v_{0}^{2}}{2g} = \dfrac{(40\ \mathrm{m/s})^{2}}{2(9.8\ \mathrm{m/s^2})} = 81.6\ \mathrm{m}$，火箭在那裡瞬間靜止；由 (9.7)，兩塊等質量碎片的鉛直速度等大反向。第一塊由 (2.10)，$0 = H + u_{1}t_{1} - \tfrac{1}{2}gt_{1}^{2}$，$t_{1} = 2.75\ \mathrm{s}$：
> $$
> u_{1} = \frac{\tfrac{1}{2}gt_{1}^{2} - H}{t_{1}} = \frac{37.06\ \mathrm{m} - 81.63\ \mathrm{m}}{2.75\ \mathrm{s}} = -16.21\ \mathrm{m/s}.
> $$
> 第二塊以 $u_{2} = +16.21\ \mathrm{m/s}$ 向上，經過 $2u_{2}/g$ 回到爆炸點、以 $16.21\ \mathrm{m/s}$ 向下，之後的運動和第一塊完全一樣：
> $$
> t_{2} = t_{1} + \frac{2u_{2}}{g} = 2.75\ \mathrm{s} + \frac{2(16.21\ \mathrm{m/s})}{9.8\ \mathrm{m/s^2}} = 6.1\ \mathrm{s} \quad \text{（爆炸後）}.
> $$

> [!warning] 落地時間不同
> 速度等大反向不代表時間相同：向上的那塊要先上升再回來。

## 加選：二維動量守恆

### EUP 9.54
題目：[[PHY1 HW Ch09 Questions#EUP 9.54|EUP 9.54]]

> [!solution] 答案
> 質量用 $\mathrm{u}$（只有比值重要）：$238$、$4$、$234$。由 (9.7)，$238\,\vec{v}_{\mathrm{U}} = 4\,\vec{v}_{\alpha} + 234\,\vec{v}_{\mathrm{Th}}$：
> $$
> \begin{aligned}
> v_{\mathrm{Th},x} &= \frac{238(4.1 \times 10^{5}\ \mathrm{m/s}) - 4(1.5 \times 10^{7}\ \mathrm{m/s})\cos 36^{\circ}}{234} = 2.1 \times 10^{5}\ \mathrm{m/s}, \\
> v_{\mathrm{Th},y} &= -\frac{4(1.5 \times 10^{7}\ \mathrm{m/s})\sin 36^{\circ}}{234} = -1.5 \times 10^{5}\ \mathrm{m/s}.
> \end{aligned}
> $$
> $\vec{v}_{\mathrm{Th}} = (2.1\hat{\imath} - 1.5\hat{\jmath}) \times 10^{5}\ \mathrm{m/s}$：$2.6 \times 10^{5}\ \mathrm{m/s}$，在 $x$ 軸下方 $36^{\circ}$。

> [!warning] 母核在動
> 鈾核在運動，所以衰變後的動量加起來是 $238\,\vec{v}_{\mathrm{U}}$，不是 $\vec{0}$。

### EUP 9.57
題目：[[PHY1 HW Ch09 Questions#EUP 9.57|EUP 9.57]]

> [!solution] 答案
> 原本全部靜止，由 (9.7)，相機的動量 $\vec{p}_{\mathrm{c}} = -(\vec{p}_{\mathrm{t}} + \vec{p}_{\mathrm{a}})$，其中
> $$
> \begin{aligned}
> \vec{p}_{\mathrm{t}} &= (18\ \mathrm{kg})(1.1\ \mathrm{m/s})\hat{\imath} = 19.8\hat{\imath}\ \mathrm{kg \cdot m/s}, \\
> \vec{p}_{\mathrm{a}} &= (67\ \mathrm{kg})(0.66\ \mathrm{m/s})(\cos 200^{\circ}\hat{\imath} + \sin 200^{\circ}\hat{\jmath}) = (-41.55\hat{\imath} - 15.12\hat{\jmath})\ \mathrm{kg \cdot m/s}.
> \end{aligned}
> $$
> $$
> \vec{v}_{\mathrm{c}} = \frac{(21.75\hat{\imath} + 15.12\hat{\jmath})\ \mathrm{kg \cdot m/s}}{5.4\ \mathrm{kg}} = (4.0\hat{\imath} + 2.8\hat{\jmath})\ \mathrm{m/s},
> $$
> 也就是 $4.9\ \mathrm{m/s}$，從 $x$ 軸逆時針 $35^{\circ}$。

## 加選：系統的動能

### EUP 9.20
題目：[[PHY1 HW Ch09 Questions#EUP 9.20|EUP 9.20]]

> [!solution] 答案
> 設物體質量 $M$、速率 $v$，$K = \tfrac{1}{2}Mv^{2}$。爆炸中沒有外力，$\vec{v}_{\mathrm{cm}}$ 不變，所以 $K_{\mathrm{cm}} = \tfrac{1}{2}Mv^{2} = K$。爆炸後每塊的速率都是 $2v$：
> $$
> K_{\mathrm{after}} = \tfrac{1}{2}m_{1}(2v)^{2} + \tfrac{1}{2}m_{2}(2v)^{2} = 4\left(\tfrac{1}{2}Mv^{2}\right) = 4K.
> $$
> 由 (9.9)，$K_{\mathrm{int}} = 4K - K = 3K$，所以 $\dfrac{K_{\mathrm{int}}}{K_{\mathrm{cm}}} = 3$。

### EUP 9.43
題目：[[PHY1 HW Ch09 Questions#EUP 9.43|EUP 9.43]]

> [!solution] 答案
> 每個質量 $m = 0.200\ \mathrm{kg}$，$M = 0.600\ \mathrm{kg}$。由 (9.5)，
> $$
> \vec{v}_{\mathrm{cm}} = \frac{\vec{v}_{1} + \vec{v}_{2} + \vec{v}_{3}}{3} = \frac{(15.0 - 3.45 - 4.32)\hat{\jmath}\ \mathrm{m/s}}{3} = 2.41\hat{\jmath}\ \mathrm{m/s},
> $$
> 所以 $K_{\mathrm{cm}} = \tfrac{1}{2}Mv_{\mathrm{cm}}^{2} = \tfrac{1}{2}(0.600\ \mathrm{kg})(2.41\ \mathrm{m/s})^{2} = 1.74\ \mathrm{J}$。
> $$
> \begin{aligned}
> K &= \tfrac{1}{2}m\left(v_{1}^{2} + v_{2}^{2} + v_{3}^{2}\right) \\
> &= \tfrac{1}{2}(0.200\ \mathrm{kg})(225 + 56.79 + 63.55)\ \mathrm{m^2/s^2} = 34.53\ \mathrm{J}.
> \end{aligned}
> $$
> 由 (9.9)，$K_{\mathrm{int}} = K - K_{\mathrm{cm}} = 34.53\ \mathrm{J} - 1.74\ \mathrm{J} = 32.8\ \mathrm{J}$。

## 加選：衝量與平均力

### EUP 9.22
題目：[[PHY1 HW Ch09 Questions#EUP 9.22|EUP 9.22]]

> [!solution] 答案
> 取 $y$ 向上；$m = 220\ \mathrm{\mu g} = 2.20 \times 10^{-7}\ \mathrm{kg}$，$\bar{a} = 100g$，$\Delta t = 1.2 \times 10^{-3}\ \mathrm{s}$。跳蚤的第二定律：$\bar{F} - mg = m\bar{a}$。
> - (a) $\bar{F} = m(\bar{a} + g) = 101mg = 101(2.20 \times 10^{-7}\ \mathrm{kg})(9.8\ \mathrm{m/s^2}) = 2.2 \times 10^{-4}\ \mathrm{N}$，向上。
> - (b) $J = \bar{F}\Delta t = (2.18 \times 10^{-4}\ \mathrm{N})(1.2 \times 10^{-3}\ \mathrm{s}) = 2.6 \times 10^{-7}\ \mathrm{N \cdot s}$，向上。
> - (c) 由 (9.10a)，用淨力：$\Delta p = m\bar{a}\Delta t = 100mg\,\Delta t = 2.6 \times 10^{-7}\ \mathrm{kg \cdot m/s}$，向上。

> [!warning] 地面的力不是淨力
> 動量變化來自淨力 $\bar{F} - mg$；地面的衝量大 $1\%$，只因為 $\bar{a} \gg g$ 才在四捨五入後看不出差別。

### EUP 9.60
題目：[[PHY1 HW Ch09 Questions#EUP 9.60|EUP 9.60]]

> [!solution] 答案
> 每團麵團落下時沒有水平速度，必須被帶到輸送帶的速率 $v = 0.52\ \mathrm{m/s}$。由 (9.6)，機構的力等於麵團獲得水平動量的速率：
> $$
> \bar{F} = \frac{\Delta m}{\Delta t}v = \frac{0.011\ \mathrm{kg}}{2\ \mathrm{s}}(0.52\ \mathrm{m/s}) = 2.9 \times 10^{-3}\ \mathrm{N}.
> $$

### EUP 9.68
題目：[[PHY1 HW Ch09 Questions#EUP 9.68|EUP 9.68]]

> [!solution] 答案
> 由 (9.10b)，
> $$
> \begin{aligned}
> J &= \int_{0}^{\Delta t} at(t - \Delta t)\,dt = a\left(\frac{\Delta t^{3}}{3} - \frac{\Delta t^{3}}{2}\right) = -\frac{a\,\Delta t^{3}}{6} \\
> &= -\frac{(-4.6\ \mathrm{N/s^2})(2.8\ \mathrm{s})^{3}}{6} = 17\ \mathrm{N \cdot s}.
> \end{aligned}
> $$
> $10\ \mathrm{N \cdot s} < J < 20\ \mathrm{N \cdot s}$：符合規格。

## 加選：數據題

### EUP 9.92
題目：[[PHY1 HW Ch09 Questions#EUP 9.92|EUP 9.92]]

> [!solution] 答案
> 馬達的衝量給火箭動量，$J = mv_{0}$ (9.10b)，之後火箭只受重力上升，由 (2.11)，$h = \dfrac{v_{0}^{2}}{2g} = \dfrac{1}{2g}\left(\dfrac{J}{m}\right)^{2}$。以 $h$ 對 $(J/m)^{2}$ 作圖：通過原點的直線，斜率 $\dfrac{1}{2g}$。
>
> | $(J/m)^{2}$ ($\mathrm{m^2/s^2}$) | $625$ | $259$ | $370$ | $1111$ | $514$ |
> | --- | --- | --- | --- | --- | --- |
> | $h$ ($\mathrm{m}$) | $22$ | $13$ | $19$ | $51$ | $23$ |
>
> 通過原點的最佳擬合直線斜率 $0.0443\ \mathrm{s^2/m}$，所以 $g = \dfrac{1}{2(0.0443\ \mathrm{s^2/m})} = 11\ \mathrm{m/s^2}$。
>
> 空氣阻力使每次的最大高度都偏低，斜率因此偏小、$g$ 偏大（這裡大約 $15\%$）。
>
> ![EUP 9.92 fit|480](../Attachments/PHY1%20Ch09%20Problem%209.92%20fit.png)

## 加選：完全非彈性碰撞

### EUP 9.24
題目：[[PHY1 HW Ch09 Questions#EUP 9.24|EUP 9.24]]

> [!solution] 答案
> 取 $+x$ 沿運動方向。ton 和 $\mathrm{mi/h}$ 只以比值出現，不必換算。
>
> **(a)** 由 (9.11)，
> $$
> v_{\mathrm{f}} = \frac{m_{1}v_{1} + m_{2}v_{2}}{m_{1} + m_{2}} = \frac{(56\ \mathrm{ton})(7.0\ \mathrm{mi/h}) + (31\ \mathrm{ton})(2.6\ \mathrm{mi/h})}{87\ \mathrm{ton}} = 5.4\ \mathrm{mi/h}.
> $$
> **(b)**
> $$
> \frac{K_{\mathrm{i}} - K_{\mathrm{f}}}{K_{\mathrm{i}}} = 1 - \frac{(m_{1} + m_{2})v_{\mathrm{f}}^{2}}{m_{1}v_{1}^{2} + m_{2}v_{2}^{2}} = 1 - \frac{(87)(5.43)^{2}}{(56)(7.0)^{2} + (31)(2.6)^{2}} = 0.13
> $$
> 損失了 $13\%$ 的動能。

### EUP 9.26
題目：[[PHY1 HW Ch09 Questions#EUP 9.26|EUP 9.26]]

> [!solution] 答案
> 由 (9.11)，$m_{\mathrm{n}}\vec{v}_{\mathrm{n}} + m_{\mathrm{d}}\vec{v}_{\mathrm{d}} = m_{\mathrm{t}}\vec{v}_{\mathrm{t}}$，質量用 $\mathrm{u}$：
> $$
> \begin{aligned}
> \vec{v}_{\mathrm{d}} &= \frac{m_{\mathrm{t}}\vec{v}_{\mathrm{t}} - m_{\mathrm{n}}\vec{v}_{\mathrm{n}}}{m_{\mathrm{d}}} = \frac{3.02(15.1\hat{\imath} + 22.6\hat{\jmath}) - 1.01(23.5\hat{\imath} + 14.4\hat{\jmath})}{2.01}\ \mathrm{Mm/s} \\
> &= (10.9\hat{\imath} + 26.7\hat{\jmath})\ \mathrm{Mm/s}.
> \end{aligned}
> $$

### EUP 9.71
題目：[[PHY1 HW Ch09 Questions#EUP 9.71|EUP 9.71]]

> [!solution] 答案
> 兩物體質量 $m$、速率 $v$，速度夾角 $\varphi$。由 (9.11)，$m\vec{v}_{1} + m\vec{v}_{2} = 2m\vec{v}_{\mathrm{f}}$，且 $v_{\mathrm{f}} = \tfrac{1}{2}v$，所以 $\lvert \vec{v}_{1} + \vec{v}_{2} \rvert = v$：
> $$
> \lvert \vec{v}_{1} + \vec{v}_{2} \rvert^{2} = v^{2} + v^{2} + 2v^{2}\cos\varphi = v^{2} \implies \cos\varphi = -\tfrac{1}{2} \implies \varphi = 120^{\circ}.
> $$

## 加選：碰撞之後接另一個過程

### EUP 9.49
題目：[[PHY1 HW Ch09 Questions#EUP 9.49|EUP 9.49]]

> [!solution] 答案
> **連結**（短暫，彈簧還來不及作用），由 (9.11)：
> $$
> V = \frac{m_{2}v_{2}}{m_{1} + m_{2}} = \frac{(9400\ \mathrm{kg})(8.5\ \mathrm{m/s})}{20{,}400\ \mathrm{kg}} = 3.92\ \mathrm{m/s}.
> $$
> **壓縮**（力學能守恆）：$\tfrac{1}{2}(m_{1} + m_{2})V^{2} = \tfrac{1}{2}kx^{2}$。
>
> **(a)**
> $$
> x = V\sqrt{\frac{m_{1} + m_{2}}{k}} = (3.92\ \mathrm{m/s})\sqrt{\frac{20{,}400\ \mathrm{kg}}{0.32 \times 10^{6}\ \mathrm{N/m}}} = 0.99\ \mathrm{m}.
> $$
> **(b)** 彈簧把能量全部還回來：$3.9\ \mathrm{m/s}$，離開緩衝器。

> [!warning] 分兩段
> 連結時動能不守恆：碰撞用動量，只有彈簧那一段用能量。

### EUP 9.69
題目：[[PHY1 HW Ch09 Questions#EUP 9.69|EUP 9.69]]

> [!solution] 答案
> **滑行**：殘骸（$M = 4860\ \mathrm{kg}$）在摩擦把動能消耗完時停下，$\mu_{\mathrm{k}}Mgd = \tfrac{1}{2}MV^{2}$：
> $$
> V = \sqrt{2\mu_{\mathrm{k}}gd} = \sqrt{2(0.697)(9.8\ \mathrm{m/s^2})(17.6\ \mathrm{m})} = 15.51\ \mathrm{m/s},
> $$
> 所以 $P = MV = 7.536 \times 10^{4}\ \mathrm{kg \cdot m/s}$。
> **碰撞**，由 (9.11)：兩個動量互相垂直，$p_{\mathrm{L}}^{2} + p_{\mathrm{S}}^{2} = P^{2}$。速限 $70\ \mathrm{km/h} = 19.44\ \mathrm{m/s}$。
> - Leaf 在速限：$p_{\mathrm{L}} = 3.189 \times 10^{4}\ \mathrm{kg \cdot m/s}$，所以 $p_{\mathrm{S}} = \sqrt{P^{2} - p_{\mathrm{L}}^{2}} = 6.828 \times 10^{4}\ \mathrm{kg \cdot m/s}$，$v_{\mathrm{S}} = 21.2\ \mathrm{m/s} = 76\ \mathrm{km/h}$。
> - 休旅車在速限：$p_{\mathrm{S}} = 6.261 \times 10^{4}\ \mathrm{kg \cdot m/s}$，所以 $p_{\mathrm{L}} = 4.194 \times 10^{4}\ \mathrm{kg \cdot m/s}$，$v_{\mathrm{L}} = 25.6\ \mathrm{m/s} = 92\ \mathrm{km/h}$。
>
> 不論哪一種，另一輛都超過 $70\ \mathrm{km/h}$，所以至少有一輛超速。

### EUP 9.88
題目：[[PHY1 HW Ch09 Questions#EUP 9.88|EUP 9.88]]

> [!solution] 答案
> 彈丸 $m = 0.52 \times 10^{-3}\ \mathrm{kg}$，擺錘 $M = 0.400\ \mathrm{kg}$。**擺動**（力學能守恆）：擺錘離開時 $V = \sqrt{2gh} = \sqrt{2(9.8\ \mathrm{m/s^2})(0.52 \times 10^{-3}\ \mathrm{m})} = 0.1010\ \mathrm{m/s}$。**穿過**（動量守恆，(9.7)），$v_{0} = \sqrt{2K_{0}/m} = 111.8\ \mathrm{m/s}$：$mv_{0} = mv + MV$，所以
> $$
> \begin{aligned}
> v &= v_{0} - \frac{M}{m}V \\
> &= 111.8\ \mathrm{m/s} - \frac{0.400\ \mathrm{kg}}{0.52 \times 10^{-3}\ \mathrm{kg}}(0.1010\ \mathrm{m/s}) = 34.1\ \mathrm{m/s}.
> \end{aligned}
> $$
> $$
> K = \tfrac{1}{2}mv^{2} = \tfrac{1}{2}(0.52 \times 10^{-3}\ \mathrm{kg})(34.1\ \mathrm{m/s})^{2} = 0.30\ \mathrm{J}.
> $$

> [!warning] 不是完全非彈性
> 彈丸穿過去了，Example 9.9 的 $mv = (m + M)V$ 不能用：彈丸和擺錘最後的速度不同。

## 加選：一維彈性碰撞

### EUP 9.29
題目：[[PHY1 HW Ch09 Questions#EUP 9.29|EUP 9.29]]

> [!solution] 答案
> 取 $+x$ 朝向汽車。車的質量大得多，它的速度 $v_{2} = -15\ \mathrm{m/s}$ 不變。由 (9.14)，$v_{\mathrm{1i}} - v_{2} = v_{2} - v_{\mathrm{1f}}$：
> $$
> v_{\mathrm{1f}} = 2v_{2} - v_{\mathrm{1i}} = 2(-15\ \mathrm{m/s}) - 18\ \mathrm{m/s} = -48\ \mathrm{m/s}.
> $$
> 球以 $48\ \mathrm{m/s}$ 彈回。

> [!warning] 牆在動
> 球不是只把 $18\ \mathrm{m/s}$ 反向：相對汽車，它以 $33\ \mathrm{m/s}$ 撞上、以 $33\ \mathrm{m/s}$ 彈開。

### EUP 9.72
題目：[[PHY1 HW Ch09 Questions#EUP 9.72|EUP 9.72]]

> [!solution] 答案
> 取 $+x$ 沿質子的初速度：$v_{\mathrm{1i}} = 6.90\ \mathrm{Mm/s}$，$v_{\mathrm{2i}} = -2.80\ \mathrm{Mm/s}$，$v_{\mathrm{1f}} = -8.62\ \mathrm{Mm/s}$。由 (9.14)，
> $$
> v_{\mathrm{2f}} = v_{\mathrm{1i}} - v_{\mathrm{2i}} + v_{\mathrm{1f}} = (6.90 + 2.80 - 8.62)\ \mathrm{Mm/s} = 1.08\ \mathrm{Mm/s}.
> $$
> 由 (9.12b)，
> $$
> m_{2} = m_{1}\frac{v_{\mathrm{1i}} - v_{\mathrm{1f}}}{v_{\mathrm{2f}} - v_{\mathrm{2i}}} = (1\ \mathrm{u})\frac{(6.90 + 8.62)\ \mathrm{Mm/s}}{(1.08 + 2.80)\ \mathrm{Mm/s}} = 4.00\ \mathrm{u}.
> $$
> 第二個粒子質量 $4.00\ \mathrm{u}$，以 $1.08\ \mathrm{Mm/s}$ 沿質子原本的方向運動。

### EUP 9.81
題目：[[PHY1 HW Ch09 Questions#EUP 9.81|EUP 9.81]]

> [!solution] 答案
> 質量相等，取 $+x$ 沿 $v$。動量守恆 (9.7) 與剩下的動能給出
> $$
> v_{1} + v_{2} = v, \qquad v_{1}^{2} + v_{2}^{2} = \left(1 - \tfrac{7}{32}\right)v^{2} = \tfrac{25}{32}v^{2}.
> $$
> 第一式平方，得 $2v_{1}v_{2} = v^{2} - \tfrac{25}{32}v^{2} = \tfrac{7}{32}v^{2}$，所以 $v_{1}$、$v_{2}$ 是 $u^{2} - vu + \tfrac{7}{64}v^{2} = 0$ 的兩根：$u = \tfrac{1}{8}v$ 或 $\tfrac{7}{8}v$。被撞的車在前面，必須比較快：
> $$
> v_{1} = \tfrac{1}{8}v, \qquad v_{2} = \tfrac{7}{8}v \quad \text{（都沿原方向）}.
> $$

> [!warning] 兩個根
> $v_{1} = \tfrac{7}{8}v$、$v_{2} = \tfrac{1}{8}v$ 等於讓第一輛車穿過第二輛。

## 加選：連續碰撞

### EUP 9.74
題目：[[PHY1 HW Ch09 Questions#EUP 9.74|EUP 9.74]]

![EUP Figure 9.26|300](../Attachments/PHY1%20Ch09%20Fig%209.26.png)

> [!solution] 答案
> 取 $+x$ 向右。每次碰撞都是彈性的、被撞的木塊原本靜止，用 $v_{\mathrm{2i}} = 0$ 的 (9.15)。
> - $A$（$m$）撞 $B$（$2m$）：$v_{A} = \dfrac{m - 2m}{3m}v = -\tfrac{1}{3}v$，$v_{B} = \dfrac{2m}{3m}v = \tfrac{2}{3}v$。
> - $B$（$2m$）撞 $C$（$m$）：$v_{B}' = \dfrac{2m - m}{3m}\left(\tfrac{2}{3}v\right) = \tfrac{2}{9}v$，$v_{C} = \dfrac{2(2m)}{3m}\left(\tfrac{2}{3}v\right) = \tfrac{8}{9}v$。
>
> $A$ 向左、$v_{B}' < v_{C}$，不會再碰撞：$A$ 以 $\tfrac{1}{3}v$ 向左，$B$ 以 $\tfrac{2}{9}v$、$C$ 以 $\tfrac{8}{9}v$ 向右。

> [!warning] 檢查還會不會撞
> 每次碰撞後都比較速度：要等沒有木塊追得上另一塊，碰撞才算結束。

### EUP 9.80
題目：[[PHY1 HW Ch09 Questions#EUP 9.80|EUP 9.80]]

> [!solution] 答案
> 取 $y$ 向上。兩球以 $v = \sqrt{2gh}$ 落地。大球從地板彈性反彈，速度 $+v$，接著遇上仍以 $-v$ 落下的小球。由 (9.15a)，小球為物體 1，$M \gg m$：
> $$
> v_{\mathrm{1f}} = \frac{m - M}{m + M}(-v) + \frac{2M}{m + M}(+v) \approx v + 2v = 3v.
> $$
> 小球上升到 $\dfrac{(3v)^{2}}{2g} = 9\dfrac{v^{2}}{2g} = 9h$。

### EUP 9.82
題目：[[PHY1 HW Ch09 Questions#EUP 9.82|EUP 9.82]]

![EUP Figure 9.28|400](../Attachments/PHY1%20Ch09%20Fig%209.28.png)

> [!solution] 答案
> $200$-g 木塊到斜面底端時 $v_{0} = \sqrt{2gh} = \sqrt{2(9.8\ \mathrm{m/s^2})(0.25\ \mathrm{m})} = 2.214\ \mathrm{m/s}$。由 (9.15)，$m_{1} = 0.2\ \mathrm{kg}$，$m_{2} = 0.8\ \mathrm{kg}$：
> $$
> \begin{aligned}
> v_{1} &= \frac{m_{1} - m_{2}}{m_{1} + m_{2}}v_{0} = -\tfrac{3}{5}v_{0} = -1.328\ \mathrm{m/s}, \\
> v_{2} &= \frac{2m_{1}}{m_{1} + m_{2}}v_{0} = \tfrac{2}{5}v_{0} = 0.885\ \mathrm{m/s}.
> \end{aligned}
> $$
> 木塊 1 退回 $d = 1.4\ \mathrm{m}$ 要 $t_{a} = d/\lvert v_{1} \rvert = 1.054\ \mathrm{s}$，以加速度 $g\sin 30^{\circ}$ 上斜面再下來要 $t_{b} = \dfrac{2\lvert v_{1} \rvert}{g\sin 30^{\circ}} = 0.542\ \mathrm{s}$，在 $T_{0} = 1.596\ \mathrm{s}$ 以 $1.328\ \mathrm{m/s}$ 離開斜面底端。這時木塊 2 離底端 $d + v_{2}T_{0} = 2.813\ \mathrm{m}$，木塊 1 以 $\lvert v_{1} \rvert - v_{2} = 0.443\ \mathrm{m/s}$ 追近：
> $$
> T = T_{0} + \frac{2.813\ \mathrm{m}}{0.443\ \mathrm{m/s}} = 1.596\ \mathrm{s} + 6.35\ \mathrm{s} = 8.0\ \mathrm{s}.
> $$

## 加選：二維彈性碰撞

### EUP 9.76
題目：[[PHY1 HW Ch09 Questions#EUP 9.76|EUP 9.76]]

> [!solution] 答案
> 等質量從 (9.12)、(9.13) 消去，且 $\vec{v}_{\mathrm{2i}} = \vec{0}$：
> $$
> \vec{v}_{\mathrm{1i}} = \vec{v}_{\mathrm{1f}} + \vec{v}_{\mathrm{2f}}, \qquad v_{\mathrm{1i}}^{2} = v_{\mathrm{1f}}^{2} + v_{\mathrm{2f}}^{2}.
> $$
> 第一式和自己作內積，得 $v_{\mathrm{1i}}^{2} = v_{\mathrm{1f}}^{2} + v_{\mathrm{2f}}^{2} + 2\vec{v}_{\mathrm{1f}} \cdot \vec{v}_{\mathrm{2f}}$，所以 $\vec{v}_{\mathrm{1f}} \cdot \vec{v}_{\mathrm{2f}} = 0$。不是正面碰撞，兩個末速度都不為零：它們互相垂直。$\blacksquare$

### EUP 9.78
題目：[[PHY1 HW Ch09 Questions#EUP 9.78|EUP 9.78]]

![EUP Figure 9.27|300](../Attachments/PHY1%20Ch09%20Fig%209.27.png)

> [!solution] 答案
> 接觸時三個球心成正三角形，接觸力沿球心連線，把 2 號球推往 $x$ 軸上方 $30^{\circ}$、11 號球推往下方 $30^{\circ}$。由對稱，兩球以相同速率 $u$ 離開，入射球留在 $x$ 軸上，速度 $v_{1}$。由 (9.12)、(9.13)，消去相等的質量：
> $$
> v_{0} = v_{1} + 2u\cos 30^{\circ} = v_{1} + \sqrt{3}u, \qquad v_{0}^{2} = v_{1}^{2} + 2u^{2}.
> $$
> 代入 $u = (v_{0} - v_{1})/\sqrt{3}$：$v_{0}^{2} - v_{1}^{2} = \tfrac{2}{3}(v_{0} - v_{1})^{2}$，所以 $v_{0} + v_{1} = \tfrac{2}{3}(v_{0} - v_{1})$，$v_{1} = -\tfrac{1}{5}v_{0}$，$u = \dfrac{2\sqrt{3}}{5}v_{0}$（另一根 $v_{1} = v_{0}$ 是沒有碰撞）。
> $$
> \vec{v}_{1} = -\tfrac{1}{5}v_{0}\hat{\imath}, \qquad \vec{v}_{2} = \tfrac{3}{5}v_{0}\hat{\imath} + \tfrac{\sqrt{3}}{5}v_{0}\hat{\jmath}, \qquad \vec{v}_{11} = \tfrac{3}{5}v_{0}\hat{\imath} - \tfrac{\sqrt{3}}{5}v_{0}\hat{\jmath}.
> $$

## 加選：頻閃照片中的碰撞

### EUP 9.94 to 9.97
題目：[[PHY1 HW Ch09 Questions#EUP 9.94 to 9.97|EUP 9.94 to 9.97]]

![EUP Figure 9.30|400](../Attachments/PHY1%20Ch09%20Fig%209.30.png)

> [!solution] 答案
> - **94.** c. 球會彈起來，但一次比一次低。
> - **95.** b. 在最高點，力學能幾乎全是 $mgh$（水平速率幾乎不變）。第二次碰撞後的最高點約為前一個的 $0.6$，所以大約損失 $40\%$。
> - **96.** b. 各影像的水平間距大致不變；鉛直速度反向並變小。
> - **97.** a. 和長長的弧線相比，球碰到地板的時間很短。

## 外校考題：觀念題

### KSUF 3.6 to 3.8
題目：[[PHY1 HW Ch09 Questions#KSUF 3.6 to 3.8|KSUF 3.6 to 3.8]]

> [!solution] 答案
> - **6.** T. 淨力的衝量等於動量變化 (9.10b)。
> - **7.** T. 衝量一定時 $\bar{F} = J/\Delta t$ (9.10a)：時間越長，平均力越小。
> - **8.** F. 任何碰撞的動量都守恆；非彈性碰撞損失的是動能。

### KSUS 4.1
題目：[[PHY1 HW Ch09 Questions#KSUS 4.1|KSUS 4.1]]

> [!solution] 答案
> c. 火箭和氣體不受外力，由 (9.7)，兩者的動量變化大小相等、方向相反。

### KSUS 4.4 to 4.6
題目：[[PHY1 HW Ch09 Questions#KSUS 4.4 to 4.6|KSUS 4.4 to 4.6]]

> [!solution] 答案
> - **4.** F. 衝量是平均力乘時間間隔，$\vec{J} = \bar{\vec{F}}\Delta t$ (9.10a)，是向量。
> - **5.** F. 由功–動能定理 $\bar{F}d = \tfrac{1}{2}mv^{2}$：停止距離越短，平均力越大。
> - **6.** F. 完全非彈性碰撞的動量守恆 (9.11)；損失的只有動能。

## 外校考題：計算題

### KSUF 3.9
題目：[[PHY1 HW Ch09 Questions#KSUF 3.9|KSUF 3.9]]

> [!solution] 答案
> 取 $+x$ 向東；$m = 0.160\ \mathrm{kg}$。等質量的一維彈性碰撞，兩球交換速度（(9.15) 取 $m_{1} = m_{2}$）。
>
> **a)** 2 號球以 $12.0\ \mathrm{m/s}$ 向東運動。
>
> **b)** 由 (9.10a)，對 2 號球：
> $$
> \bar{F} = \frac{m\,\Delta v}{\Delta t} = \frac{(0.160\ \mathrm{kg})[12.0\ \mathrm{m/s} - (-4.5\ \mathrm{m/s})]}{2.5 \times 10^{-3}\ \mathrm{s}} = 1.1 \times 10^{3}\ \mathrm{N} \quad \text{（向東）}.
> $$

### KSUF 3.10
題目：[[PHY1 HW Ch09 Questions#KSUF 3.10|KSUF 3.10]]

> [!solution] 答案
> 取 $x$ 向東、$y$ 向北。由 (9.11)，
> $$
> \begin{aligned}
> \vec{P} &= (1800\ \mathrm{kg})(18.0\ \mathrm{m/s})\hat{\imath} + (3200\ \mathrm{kg})(24\ \mathrm{m/s})\hat{\jmath} \\
> &= (3.24\hat{\imath} + 7.68\hat{\jmath}) \times 10^{4}\ \mathrm{kg \cdot m/s}.
> \end{aligned}
> $$
> **a)** $V = \dfrac{P}{M} = \dfrac{8.34 \times 10^{4}\ \mathrm{kg \cdot m/s}}{5000\ \mathrm{kg}} = 16.7\ \mathrm{m/s} \approx 17\ \mathrm{m/s}$，往東偏北 $67^{\circ}$。
>
> **b)** 摩擦把動能消耗完，$\mu_{\mathrm{k}}Mgd = \tfrac{1}{2}MV^{2}$：
> $$
> d = \frac{V^{2}}{2\mu_{\mathrm{k}}g} = \frac{(16.67\ \mathrm{m/s})^{2}}{2(0.80)(9.80\ \mathrm{m/s^2})} = 18\ \mathrm{m}.
> $$

### KSUS 4.7
題目：[[PHY1 HW Ch09 Questions#KSUS 4.7|KSUS 4.7]]

> [!solution] 答案
> 取 $+x$ 沿藥球的速度；$m_{1} = 5.0\ \mathrm{kg}$，$m_{2} = 0.62\ \mathrm{kg}$，$v_{\mathrm{2i}} = 0$。
>
> **a)** 由 (9.15b)，
> $$
> v_{\mathrm{2f}} = \frac{2m_{1}}{m_{1} + m_{2}}v_{\mathrm{1i}} = \frac{2(5.0\ \mathrm{kg})}{5.62\ \mathrm{kg}}(16.0\ \mathrm{m/s}) = 28\ \mathrm{m/s}.
> $$
> **b)** 由 (9.10a)，
> $$
> \bar{F} = \frac{m_{2}\,\Delta v_{2}}{\Delta t} = \frac{(0.62\ \mathrm{kg})(28.47\ \mathrm{m/s})}{38 \times 10^{-3}\ \mathrm{s}} = 4.6 \times 10^{2}\ \mathrm{N}.
> $$

### SIUF 3.6
題目：[[PHY1 HW Ch09 Questions#SIUF 3.6|SIUF 3.6]]

> [!solution] 答案
> **碰撞**（動量守恆，(9.11)）：$m_{1}v = (m_{1} + m_{2})V$。**上升**（力學能守恆）：$\tfrac{1}{2}(m_{1} + m_{2})V^{2} = (m_{1} + m_{2})gh$，所以 $V = \sqrt{2gh}$。
> $$
> v = \frac{m_{1} + m_{2}}{m_{1}}\sqrt{2gh} = \frac{3.030\ \mathrm{kg}}{0.03000\ \mathrm{kg}}\sqrt{2(9.80\ \mathrm{m/s^2})(0.300\ \mathrm{m})} = 245\ \mathrm{m/s}.
> $$

### SIUF 3.7
題目：[[PHY1 HW Ch09 Questions#SIUF 3.7|SIUF 3.7]]

> [!solution] 答案
> 這裡 $\rho(x) = bx$ 是每單位長度的質量，所以 $dm = bx\,dx$。由 (9.4)，
> $$
> x_{\mathrm{cm}} = \frac{\int_{0}^{L} x(bx)\,dx}{\int_{0}^{L} bx\,dx} = \frac{bL^{3}/3}{bL^{2}/2} = \frac{2}{3}L = 0.67\ \mathrm{m}.
> $$
> 這就是 EUP 9.91 取 $a = 1$。
