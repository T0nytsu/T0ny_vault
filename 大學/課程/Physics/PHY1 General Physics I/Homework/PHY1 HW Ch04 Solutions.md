---
course: [PHY1]
semester: "115-1"
chapter: ["4.1", "4.2", "4.3", "4.4", "4.5", "4.6"]
tags: [physics, homework, solutions, dynamics]
source:
  - "Own solutions; every number recomputed with Python, symbolic results with sympy"
  - "EUP Ch. 4 (pp. 70-89), scanned PDF: equations and answers to GOT IT? questions"
  - "[[PHY1 Ch04 Fig 4.21.png]]"
  - "[[PHY1 Ch04 Fig 4.23.png]]"
  - "[[PHY1 Ch04 Fig 4.24.png]]"
  - "[[PHY1 Ch04 Fig 4.25.png]]"
  - "[[PHY1 Ch04 Fig 4.27.png]]"
created: 2026-10-29
questions: "[[PHY1 HW Ch04 Questions]]"
up: "[[PHY1 Index]]"
format: "physics-notes 1.1"
---
> [!note] 符號與公式
> - 式號照課本：動量 $\vec{p} = m\vec{v}$ (4.1)；第二定律 $\vec{F}_{\mathrm{net}} = d\vec{p}/dt$ (4.2)，**質量不變時** $\vec{F}_{\mathrm{net}} = m\vec{a}$ (4.3)，兩者都**只在慣性參考系**成立；重量 $\vec{w} = m\vec{g}$ (4.5)；虎克定律 $F_{\mathrm{s}} = -kx$ (4.9)，**只對理想彈簧**。
> - 等加速度運動學（Ch. 2，**只限等加速度**）：$v = v_{0} + at$ (2.7)，$x = x_{0} + v_{0}t + \tfrac{1}{2}at^{2}$ (2.10)，$v^{2} = v_{0}^{2} + 2a(x - x_{0})$ (2.11)；等速率圓周運動 $a = v^{2}/r$ (3.16)。
> - 鉛直方向一律取 $y$ 向上。體重計或地板的讀數是正向力 $n$（視重），$n - mg = ma_{y}$。
> - $g = 9.8\ \mathrm{m/s^2}$；KSU 的題目用 $9.80\ \mathrm{m/s^2}$；月球 $g = 1.6\ \mathrm{m/s^2}$（4.4 節）。中間值多留一位有效數字。

## 答案總表

| 題目 | 答案 |
| --- | --- |
| [[PHY1 HW Ch04 Questions#EUP 4.11\|EUP 4.11]] | $7.92 \times 10^{5}\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.13\|EUP 4.13]] | $9.1 \times 10^{2}\ \mathrm{kg}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.16\|EUP 4.16]] | $2.84 \times 10^{4}\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.24\|EUP 4.24]] | $5.9 \times 10^{2}\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.25\|EUP 4.25]] | $4.9 \times 10^{2}\ \mathrm{N}$，向上 |
| [[PHY1 HW Ch04 Questions#EUP 4.27\|EUP 4.27]] | $4.7 \times 10^{2}\ \mathrm{N}$，向上 |
| [[PHY1 HW Ch04 Questions#EUP 4.45\|EUP 4.45]] | $2.5\ \mathrm{m/s^2}$，向下 |
| [[PHY1 HW Ch04 Questions#EUP 4.31\|EUP 4.31]] | $5.5 \times 10^{4}\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.51\|EUP 4.51]] | $6.0\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.57\|EUP 4.57]] | (a) $419\ \mathrm{N}$；(b) $376\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.58\|EUP 4.58]] | $3.3\ \mathrm{cm}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.33\|EUP 4.33]] | $90\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.64\|EUP 4.64]] | 證明 |
| [[PHY1 HW Ch04 Questions#EUP 4.14\|EUP 4.14]] | $1.0 \times 10^{4}\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.17\|EUP 4.17]] | $6.0\ \mathrm{cm}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.29\|EUP 4.29]] | $M\left(g + \dfrac{v^{2}}{2h}\right)$ |
| [[PHY1 HW Ch04 Questions#EUP 4.21\|EUP 4.21]] | $2.1 \times 10^{2}\ \mathrm{kg}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.49\|EUP 4.49]] | $0.60\ \mathrm{s}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.62\|EUP 4.62]] | $6.8 \times 10^{2}\ \mathrm{kg}$，9 人 |
| [[PHY1 HW Ch04 Questions#EUP 4.71\|EUP 4.71]] | $12\ \mathrm{m/s^2}$，向下 |
| [[PHY1 HW Ch04 Questions#EUP 4.44\|EUP 4.44]] | $88\ \mathrm{N}$，與原方向夾 $77^{\circ}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.50\|EUP 4.50]] | $-9.00\hat{\jmath}\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.52\|EUP 4.52]] | 拖車端 $25\ \mathrm{N}$，小孩端 $29\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.73\|EUP 4.73]] | 上方 $0.92\ \mathrm{kg}$，下方 $1.4\ \mathrm{kg}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.74\|EUP 4.74]] | $T(y) = \left[M + m\left(1 - \dfrac{y}{L}\right)\right]g$ |
| [[PHY1 HW Ch04 Questions#EUP 4.67\|EUP 4.67]] | $2.5\ \mathrm{m/s^2}$，向上 |
| [[PHY1 HW Ch04 Questions#EUP 4.65\|EUP 4.65]] | 證明 |
| [[PHY1 HW Ch04 Questions#EUP 4.66\|EUP 4.66]] | $6.0 \times 10^{2}\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.69\|EUP 4.69]] | (a) $60.0\ \mathrm{m/s}$；(b) $0.672\ \mathrm{m}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.75\|EUP 4.75]] | $F_{0}\omega/M$ |
| [[PHY1 HW Ch04 Questions#EUP 4.68\|EUP 4.68]] | (a) 約 $0.5\ \mathrm{s}$，約 $1.2\ \mathrm{m}$；(b) 1 次；(c) 約 $1.9w$；(d) 約 $1.7\ \mathrm{s}$ |
| [[PHY1 HW Ch04 Questions#EUP 4.76 to 4.79\|EUP 4.76 to 4.79]] | a, a, d, b |
| [[PHY1 HW Ch04 Questions#KSUF 2.3\|KSUF 2.3]] | a |
| [[PHY1 HW Ch04 Questions#KSUF 2.5 to 2.7\|KSUF 2.5 to 2.7]] | F, F, T |
| [[PHY1 HW Ch04 Questions#KSUF 2.8\|KSUF 2.8]] | a) a；b) b |
| [[PHY1 HW Ch04 Questions#KSUS 2.5\|KSUS 2.5]] | F |
| [[PHY1 HW Ch04 Questions#KSUS 2.11 to 2.13\|KSUS 2.11 to 2.13]] | T, F, c |
| [[PHY1 HW Ch04 Questions#SIU 23.1 and 23.2\|SIU 23.1 and 23.2]] | 讀數為零；例如手推牆、牆推手 |
| [[PHY1 HW Ch04 Questions#KSUF 2.10\|KSUF 2.10]] | b) $0.640g$，向上 |
| [[PHY1 HW Ch04 Questions#KSUS 2.14\|KSUS 2.14]] | b) $9.3 \times 10^{2}\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#SIU 22.4\|SIU 22.4]] | $5.9 \times 10^{2}\ \mathrm{N}$ |
| [[PHY1 HW Ch04 Questions#SIU 22.5\|SIU 22.5]] | $11\ \mathrm{N}$，與 $\vec{F}$ 反向 |
| [[PHY1 HW Ch04 Questions#SIU 23.6\|SIU 23.6]] | $6.5\ \mathrm{m/s^2}$，向下 |

## 老師勾選：牛頓第二定律求力與質量

### EUP 4.11
題目：[[PHY1 HW Ch04 Questions#EUP 4.11|EUP 4.11]]

> [!solution] 答案
> 由 (4.3)，
> $$
> F = ma = (3.52 \times 10^{5}\ \mathrm{kg})(2.25\ \mathrm{m/s^2}) = 7.92 \times 10^{5}\ \mathrm{N}.
> $$

### EUP 4.13
題目：[[PHY1 HW Ch04 Questions#EUP 4.13|EUP 4.13]]

> [!solution] 答案
> 由 (4.3)，
> $$
> m = \frac{F}{a} = \frac{7.0 \times 10^{3}\ \mathrm{N}}{7.7\ \mathrm{m/s^2}} = 9.1 \times 10^{2}\ \mathrm{kg}.
> $$

### EUP 4.16
題目：[[PHY1 HW Ch04 Questions#EUP 4.16|EUP 4.16]]

> [!solution] 答案
> 由靜止等加速度，由 (2.10)，$x = \tfrac{1}{2}at^{2}$：
> $$
> a = \frac{2x}{t^{2}} = \frac{2(410\ \mathrm{m})}{(5.15\ \mathrm{s})^{2}} = 30.9\ \mathrm{m/s^2}.
> $$
> 由 (4.3)，$F = ma = (920\ \mathrm{kg})(30.9\ \mathrm{m/s^2}) = 2.84 \times 10^{4}\ \mathrm{N}$。

## 老師勾選：重量

### EUP 4.24
題目：[[PHY1 HW Ch04 Questions#EUP 4.24|EUP 4.24]]

> [!solution] 答案
> 由 (4.5)，用那個高度的重力加速度 $0.89g$：
> $$
> w = m(0.89g) = (68\ \mathrm{kg})(0.89)(9.8\ \mathrm{m/s^2}) = 5.9 \times 10^{2}\ \mathrm{N}.
> $$

> [!warning] 太空人不是沒有重量
> 重量還有地表的 $89\%$；看起來失重，是因為太空人和太空站一起自由落體。

## 老師勾選：鉛直方向的第二定律與視重

### EUP 4.25
題目：[[PHY1 HW Ch04 Questions#EUP 4.25|EUP 4.25]]

> [!solution] 答案
> 等速下降，$a = 0$，由 (4.3) 空氣的力與重力平衡：
> $$
> F_{\mathrm{air}} = mg = (50\ \mathrm{kg})(9.8\ \mathrm{m/s^2}) = 4.9 \times 10^{2}\ \mathrm{N} \quad \text{（向上）}.
> $$

> [!warning] 速率用不到
> 等速時淨力為零，$40\ \mathrm{km/h}$ 是多餘的數據。

### EUP 4.27
題目：[[PHY1 HW Ch04 Questions#EUP 4.27|EUP 4.27]]

> [!solution] 答案
> $y$ 向上，$a_{y} = -2.1\ \mathrm{m/s^2}$。乘客受地板的正向力 $n$ 與重力，由 (4.3)，$n - mg = ma_{y}$：
> $$
> n = m(g + a_{y}) = (61\ \mathrm{kg})(9.8\ \mathrm{m/s^2} - 2.1\ \mathrm{m/s^2}) = 4.7 \times 10^{2}\ \mathrm{N} \quad \text{（向上）}.
> $$

### EUP 4.45
題目：[[PHY1 HW Ch04 Questions#EUP 4.45|EUP 4.45]]

> [!solution] 答案
> 視重是座椅的正向力，$n = 0.75mg$。$y$ 向上，由 (4.3)，$n - mg = ma_{y}$：
> $$
> a_{y} = \frac{n - mg}{m} = -0.25g = -0.25(9.8\ \mathrm{m/s^2}) = -2.5\ \mathrm{m/s^2}.
> $$
> 加速度大小 $2.5\ \mathrm{m/s^2}$，向下。

> [!warning] 加速度向下，不代表往下運動
> 視重只告訴你加速度：飛機可能正在下降，也可能在上升中減速。

## 老師勾選：牛頓第三定律

### EUP 4.31
題目：[[PHY1 HW Ch04 Questions#EUP 4.31|EUP 4.31]]

> [!solution] 答案
> 由第三定律，大象對地球的重力與地球對大象的重力（重量）大小相等、方向相反：
> $$
> F = mg = (5600\ \mathrm{kg})(9.8\ \mathrm{m/s^2}) = 5.5 \times 10^{4}\ \mathrm{N}.
> $$

## 老師勾選：相連物體

### EUP 4.51
題目：[[PHY1 HW Ch04 Questions#EUP 4.51|EUP 4.51]]

![EUP Figure 4.21|360](../Attachments/PHY1%20Ch04%20Fig%204.21.png)

> [!solution] 答案
> 三木塊一起加速，由 (4.3)：$a = \dfrac{F}{m_{1} + m_{2} + m_{3}} = \dfrac{12\ \mathrm{N}}{6.0\ \mathrm{kg}} = 2.0\ \mathrm{m/s^2}$。最右邊的木塊只受中間木塊的水平力：
> $$
> F_{23} = m_{3}a = (3.0\ \mathrm{kg})(2.0\ \mathrm{m/s^2}) = 6.0\ \mathrm{N}.
> $$
> 由第三定律，最右邊的木塊對中間木塊的力也是 $6.0\ \mathrm{N}$（向左）。

### EUP 4.57
題目：[[PHY1 HW Ch04 Questions#EUP 4.57|EUP 4.57]]

> [!solution] 答案
> 小車與鏈條一起以 $a = 0.345\ \mathrm{m/s^2}$ 加速，冰面無摩擦，由 (4.3)：
> - (a) 拖車那端拉的是小車加鏈條：$T_{\mathrm{a}} = (1090\ \mathrm{kg} + 125\ \mathrm{kg})(0.345\ \mathrm{m/s^2}) = 419\ \mathrm{N}$。
> - (b) 小車那端只拉小車：$T_{\mathrm{b}} = (1090\ \mathrm{kg})(0.345\ \mathrm{m/s^2}) = 376\ \mathrm{N}$。

> [!warning] 鏈條有質量
> 兩端張力差 $(125\ \mathrm{kg})a = 43\ \mathrm{N}$，用來加速鏈條本身；只有無質量的繩子兩端張力才相同。

### EUP 4.58
題目：[[PHY1 HW Ch04 Questions#EUP 4.58|EUP 4.58]]

![EUP Figure 4.23|320](../Attachments/PHY1%20Ch04%20Fig%204.23.png)

> [!solution] 答案
> 兩質量以相同加速度運動（彈簧長度不再變化），整體由 (4.3)：$a = \dfrac{F}{m_{1} + m_{2}} = \dfrac{15\ \mathrm{N}}{5.0\ \mathrm{kg}} = 3.0\ \mathrm{m/s^2}$。$2.0$-kg 的質量只受彈簧力，由 (4.9)，$kx = m_{1}a$：
> $$
> x = \frac{m_{1}a}{k} = \frac{(2.0\ \mathrm{kg})(3.0\ \mathrm{m/s^2})}{180\ \mathrm{N/m}} = 0.033\ \mathrm{m} = 3.3\ \mathrm{cm}.
> $$

> [!warning] 彈簧力不是 15 N
> 彈簧只負責拉動後面的 $2.0$-kg，所以彈簧力是 $6.0\ \mathrm{N}$。

## 老師勾選：彈簧與虎克定律

### EUP 4.33
題目：[[PHY1 HW Ch04 Questions#EUP 4.33|EUP 4.33]]

> [!solution] 答案
> 由 (4.9)，大小
> $$
> F = kx = (265\ \mathrm{N/m})(0.34\ \mathrm{m}) = 90\ \mathrm{N}.
> $$

### EUP 4.64
題目：[[PHY1 HW Ch04 Questions#EUP 4.64|EUP 4.64]]

![EUP Figure 4.24|480](../Attachments/PHY1%20Ch04%20Fig%204.24.png)

> [!solution] 答案
> **(a)** 並排時兩彈簧都伸長 $x$，由 (4.9) 各施 $k_{1}x$、$k_{2}x$，合力
> $$
> F = k_{1}x + k_{2}x = (k_{1} + k_{2})x.
> $$
> **(b)** 首尾相接時，無質量的彈簧淨力為零，兩彈簧受同樣大小的力 $F$，伸長 $x_{1} = F/k_{1}$、$x_{2} = F/k_{2}$。總伸長
> $$
> x = x_{1} + x_{2} = F\left(\frac{1}{k_{1}} + \frac{1}{k_{2}}\right) \implies F = \frac{k_{1}k_{2}x}{k_{1} + k_{2}}.
> $$
> $\blacksquare$

## 加選：由運動學求力

### EUP 4.14
題目：[[PHY1 HW Ch04 Questions#EUP 4.14|EUP 4.14]]

> [!solution] 答案
> $v_{0} = 90\ \mathrm{km/h} = 25\ \mathrm{m/s}$，$0.16\ \mathrm{s}$ 內停下。平均加速度大小 $\bar{a} = \Delta v/\Delta t$，由 (4.3)：
> $$
> \bar{F} = m\frac{\Delta v}{\Delta t} = (65\ \mathrm{kg})\frac{25\ \mathrm{m/s}}{0.16\ \mathrm{s}} = 1.0 \times 10^{4}\ \mathrm{N}.
> $$

### EUP 4.17
題目：[[PHY1 HW Ch04 Questions#EUP 4.17|EUP 4.17]]

> [!solution] 答案
> 蛋的最大減速度 $a = F/m = (2.0\ \mathrm{N})/(0.083\ \mathrm{kg}) = 24.1\ \mathrm{m/s^2}$。由 (2.11)，末速為零：
> $$
> d = \frac{v_{0}^{2}}{2a} = \frac{(1.7\ \mathrm{m/s})^{2}}{2(24.1\ \mathrm{m/s^2})} = 0.060\ \mathrm{m} = 6.0\ \mathrm{cm}.
> $$

### EUP 4.29
題目：[[PHY1 HW Ch04 Questions#EUP 4.29|EUP 4.29]]

> [!solution] 答案
> 推力固定、質量不變，等加速度。由 (2.11)，從靜止上升 $h$ 達到 $v$：$a = \dfrac{v^{2}}{2h}$。$y$ 向上，由 (4.3)，$F - Mg = Ma$：
> $$
> F = M\left(g + \frac{v^{2}}{2h}\right).
> $$

> [!warning] 推力要先撐住重量
> 只寫 $F = Ma$ 會漏掉 $Mg$：推力有一部分用來抵消重力。

## 加選：質量與重量

### EUP 4.21
題目：[[PHY1 HW Ch04 Questions#EUP 4.21|EUP 4.21]]

> [!solution] 答案
> 她能施的最大向上力不變：$F = (35\ \mathrm{kg})(9.8\ \mathrm{m/s^2}) = 343\ \mathrm{N}$。月球上能舉起重量 $343\ \mathrm{N}$ 的水泥塊：
> $$
> m = \frac{F}{g_{\mathrm{Moon}}} = \frac{343\ \mathrm{N}}{1.6\ \mathrm{m/s^2}} = 2.1 \times 10^{2}\ \mathrm{kg}.
> $$

> [!warning] 不變的是力
> 舉不舉得起看的是重量；質量在月球上不變，重量才變小。

## 加選：鉛直運動與視重

### EUP 4.49
題目：[[PHY1 HW Ch04 Questions#EUP 4.49|EUP 4.49]]

> [!solution] 答案
> 乘客留在地板上需要 $n \ge 0$。由 (4.3)，$n = m(g + a_{y}) \ge 0$，所以 $a_{y} \ge -g$：減速度最大是 $g$。由 (2.7)，
> $$
> t_{\min} = \frac{v_{0}}{g} = \frac{5.9\ \mathrm{m/s}}{9.8\ \mathrm{m/s^2}} = 0.60\ \mathrm{s}.
> $$

### EUP 4.62
題目：[[PHY1 HW Ch04 Questions#EUP 4.62|EUP 4.62]]

> [!solution] 答案
> 張力上限 $T_{\max} = \tfrac{2}{3}(21.0\ \mathrm{kN}) = 14.0\ \mathrm{kN}$。張力最大是在以最大加速度向上加速時，由 (4.3)，$T = M_{\mathrm{tot}}(g + a)$：
> $$
> M_{\mathrm{tot}} = \frac{T_{\max}}{g + a} = \frac{14.0 \times 10^{3}\ \mathrm{N}}{9.8\ \mathrm{m/s^2} + 2.29\ \mathrm{m/s^2}} = 1158\ \mathrm{kg}.
> $$
> 最大載重 $1158\ \mathrm{kg} - 480\ \mathrm{kg} = 6.8 \times 10^{2}\ \mathrm{kg}$；$678\ \mathrm{kg}/75\ \mathrm{kg} = 9.04$，即 9 人。

> [!warning] 人數無條件捨去
> $9.04$ 人要取 9 人，取 10 人就超載。

### EUP 4.71
題目：[[PHY1 HW Ch04 Questions#EUP 4.71|EUP 4.71]]

> [!solution] 答案
> $y$ 向上。脆餅離開餐盤後只受重力，對地加速度 $-g$；它相對飛機的加速度是 $+2\ \mathrm{m/s^2}$，所以 $-g = a_{\mathrm{plane}} + 2\ \mathrm{m/s^2}$：
> $$
> a_{\mathrm{plane}} = -9.8\ \mathrm{m/s^2} - 2\ \mathrm{m/s^2} = -11.8\ \mathrm{m/s^2}.
> $$
> 飛機向下加速約 $12\ \mathrm{m/s^2}$。

> [!warning] 比 g 還大
> 飛機向下的加速度超過 $g$，餐盤才會比自由落下的脆餅更快往下掉。

## 加選：二維的力與動量

### EUP 4.44
題目：[[PHY1 HW Ch04 Questions#EUP 4.44|EUP 4.44]]

> [!solution] 答案
> 取 $x$ 沿原運動方向，$y$ 朝擊出的那一側。由 (4.2)，平均力 $\vec{F}_{\mathrm{avg}} = \Delta\vec{p}/\Delta t$：
> $$
> \begin{aligned}
> \vec{p}_{0} &= (0.166\ \mathrm{kg})(44.3\ \mathrm{m/s})\hat{\imath} = 7.35\hat{\imath}\ \mathrm{kg \cdot m/s}, \\
> \vec{p} &= (0.166\ \mathrm{kg})(82.1\ \mathrm{m/s})(\cos 45.0^{\circ}\hat{\imath} + \sin 45.0^{\circ}\hat{\jmath}) = (9.64\hat{\imath} + 9.64\hat{\jmath})\ \mathrm{kg \cdot m/s}, \\
> \Delta\vec{p} &= (2.28\hat{\imath} + 9.64\hat{\jmath})\ \mathrm{kg \cdot m/s}, \qquad \lvert \Delta\vec{p} \rvert = 9.90\ \mathrm{kg \cdot m/s}.
> \end{aligned}
> $$
> $$
> F_{\mathrm{avg}} = \frac{9.90\ \mathrm{kg \cdot m/s}}{0.112\ \mathrm{s}} = 88\ \mathrm{N}, \qquad \theta = \tan^{-1}\frac{9.64}{2.28} = 77^{\circ}.
> $$
> 平均力 $88\ \mathrm{N}$，與原運動方向夾 $77^{\circ}$，偏向擊出的那一側。

> [!warning] 動量要用向量相減
> $m(82.1\ \mathrm{m/s} - 44.3\ \mathrm{m/s})$ 是錯的：兩個速度方向不同。

### EUP 4.50
題目：[[PHY1 HW Ch04 Questions#EUP 4.50|EUP 4.50]]

> [!solution] 答案
> 力都沿 $y$，$x$ 方向等速：$(1.60\ \mathrm{m/s})(3.00\ \mathrm{s}) = 4.80\ \mathrm{m}$，與題目一致。$y$ 方向初速為零、等加速度，由 (2.10)：
> $$
> a_{y} = \frac{2y}{t^{2}} = \frac{2(10.8\ \mathrm{m})}{(3.00\ \mathrm{s})^{2}} = 2.40\ \mathrm{m/s^2}, \qquad F_{\mathrm{net},y} = ma_{y} = 6.00\ \mathrm{N}.
> $$
> $$
> F_{2y} = 6.00\ \mathrm{N} - 15.0\ \mathrm{N} = -9.0\ \mathrm{N} \implies \vec{F}_{2} = -9.00\hat{\jmath}\ \mathrm{N}.
> $$

## 加選：相連物體與有質量的繩

### EUP 4.52
題目：[[PHY1 HW Ch04 Questions#EUP 4.52|EUP 4.52]]

> [!solution] 答案
> 由 (4.3)：
> - 拖車端：把手只需加速拖車，$T_{\mathrm{w}} = (11\ \mathrm{kg})(2.3\ \mathrm{m/s^2}) = 25\ \mathrm{N}$。
> - 小孩端：要加速拖車加把手，$T_{\mathrm{c}} = (11\ \mathrm{kg} + 1.8\ \mathrm{kg})(2.3\ \mathrm{m/s^2}) = 29\ \mathrm{N}$。
>
> 把手有質量，兩端的差 $(1.8\ \mathrm{kg})(2.3\ \mathrm{m/s^2}) = 4.1\ \mathrm{N}$ 用來加速把手本身。

### EUP 4.73
題目：[[PHY1 HW Ch04 Questions#EUP 4.73|EUP 4.73]]

> [!solution] 答案
> $y$ 向上，由 (4.3)。下方質量 $m_{2}$ 受繩張力與重力，$T - m_{2}g = m_{2}a$；整體受 $F$ 與總重量，$F - (m_{1} + m_{2})g = (m_{1} + m_{2})a$：
> $$
> \begin{aligned}
> m_{2} &= \frac{T}{g + a} = \frac{18\ \mathrm{N}}{9.8\ \mathrm{m/s^2} + 3.2\ \mathrm{m/s^2}} = 1.4\ \mathrm{kg}, \\
> m_{1} + m_{2} &= \frac{F}{g + a} = \frac{30\ \mathrm{N}}{13.0\ \mathrm{m/s^2}} = 2.31\ \mathrm{kg} \implies m_{1} = 0.92\ \mathrm{kg}.
> \end{aligned}
> $$
> 上方 $0.92\ \mathrm{kg}$，下方 $1.4\ \mathrm{kg}$。

### EUP 4.74
題目：[[PHY1 HW Ch04 Questions#EUP 4.74|EUP 4.74]]

> [!solution] 答案
> 系統靜止。在 $y$ 處切開，下方有質量 $M$ 和長 $L - y$ 的繩子，質量 $m(L - y)/L$，張力要撐住它們的重量：
> $$
> T(y) = \left[M + m\left(1 - \frac{y}{L}\right)\right]g.
> $$
> 檢查：繩頂 $T(0) = (M + m)g$，繩底 $T(L) = Mg$。

### EUP 4.67
題目：[[PHY1 HW Ch04 Questions#EUP 4.67|EUP 4.67]]

> [!solution] 答案
> 繩子和滑輪都無質量、無摩擦，繩上張力處處是 $T$。木塊（質量 $1.25m$）不動：$T = 1.25mg$。你沿繩向上爬，$y$ 向上，由 (4.3)，$T - mg = ma$：
> $$
> a = \frac{1.25mg - mg}{m} = 0.25g = 0.25(9.8\ \mathrm{m/s^2}) = 2.5\ \mathrm{m/s^2} \quad \text{（向上）}.
> $$

## 加選：質量會變的物體

### EUP 4.65
題目：[[PHY1 HW Ch04 Questions#EUP 4.65|EUP 4.65]]

> [!solution] 答案
> 由 (4.2) 的一維形式與乘積法則，
> $$
> F = \frac{d(mv)}{dt} = m\frac{dv}{dt} + v\frac{dm}{dt} = ma + v\frac{dm}{dt}.
> $$
> $\blacksquare$

### EUP 4.66
題目：[[PHY1 HW Ch04 Questions#EUP 4.66|EUP 4.66]]

> [!solution] 答案
> 等速 $a = 0$，由 [[#EUP 4.65|EUP 4.65]]：
> $$
> F = v\frac{dm}{dt} = (1.5\ \mathrm{m/s})(400\ \mathrm{kg/s}) = 6.0 \times 10^{2}\ \mathrm{N}.
> $$

> [!warning] 等速也要力
> 落下的穀物原本沒有水平速度，要一直被加速到 $1.5\ \mathrm{m/s}$。

## 加選：隨時間變化的力

### EUP 4.69
題目：[[PHY1 HW Ch04 Questions#EUP 4.69|EUP 4.69]]

> [!solution] 答案
> 取冰球原本靜止，$T = 22.4\ \mathrm{ms}$。
>
> **(a)** 由 (4.2)，$\Delta p = \displaystyle\int_{0}^{T}F\,dt = aT + \tfrac{1}{2}bT^{2} + \tfrac{1}{3}cT^{3}$：
> $$
> \begin{aligned}
> \Delta p &= (-0.560 + 31.36 - 20.91)\ \mathrm{kg \cdot m/s} = 9.895\ \mathrm{kg \cdot m/s}, \\
> v &= \frac{\Delta p}{m} = \frac{9.895\ \mathrm{kg \cdot m/s}}{0.165\ \mathrm{kg}} = 60.0\ \mathrm{m/s}.
> \end{aligned}
> $$
> **(b)** $v(t) = \dfrac{1}{m}\left(at + \tfrac{1}{2}bt^{2} + \tfrac{1}{3}ct^{3}\right)$，再積分一次：
> $$
> \begin{aligned}
> x &= \frac{1}{m}\left(\tfrac{1}{2}aT^{2} + \tfrac{1}{6}bT^{3} + \tfrac{1}{12}cT^{4}\right) \\
> &= \frac{(-0.00627 + 0.2342 - 0.1171)\ \mathrm{kg \cdot m}}{0.165\ \mathrm{kg}} = 0.672\ \mathrm{m}.
> \end{aligned}
> $$

> [!warning] 力不是常數
> 不能用 $F = ma$ 配等加速度公式，要對時間積分。題目沒給初速，這裡取冰球原本靜止。

### EUP 4.75
題目：[[PHY1 HW Ch04 Questions#EUP 4.75|EUP 4.75]]

> [!solution] 答案
> 由 (4.3)，$a = \dfrac{F_{0}}{M}\sin\omega t$。急動度
> $$
> j = \frac{da}{dt} = \frac{F_{0}\omega}{M}\cos\omega t, \qquad j_{\max} = \frac{F_{0}\omega}{M}.
> $$

## 加選：數據題

### EUP 4.68
題目：[[PHY1 HW Ch04 Questions#EUP 4.68|EUP 4.68]]

![EUP Figure 4.25|520](../Attachments/PHY1%20Ch04%20Fig%204.25.png)

> [!solution] 答案
> 讀數是視重除以質量，也就是接觸力 $n$ 除以 $m$，以 $g$ 為單位；讀數 $0$ 代表自由落體。
> - (a) 讀數約從 $0.6\ \mathrm{s}$ 到 $1.1\ \mathrm{s}$ 為零，自由落體約 $0.5\ \mathrm{s}$。由 (2.10)，$h = \tfrac{1}{2}gt^{2} = \tfrac{1}{2}(9.8\ \mathrm{m/s^2})(0.5\ \mathrm{s})^{2} = 1.2\ \mathrm{m}$。
> - (b) 第一次撞擊（$1.16\ \mathrm{s}$ 的尖峰）後，讀數在 $1.22$ 到 $1.28\ \mathrm{s}$ 又回到零：彈起 1 次。
> - (c) 最大讀數約 $1.9g$，所以枕頭給手機的最大力約 $1.9w$（淨力約 $0.9w$，向上）。
> - (d) 約 $1.7\ \mathrm{s}$ 之後讀數穩定在 $1g$，手機完全靜止。

> [!warning] 0.25g 不是彈起
> $1.3$ 到 $1.44\ \mathrm{s}$ 讀數約 $0.25g$ 而不是零，手機仍碰著枕頭，不算離開。

## 加選：讀視重圖

### EUP 4.76 to 4.79
題目：[[PHY1 HW Ch04 Questions#EUP 4.76 to 4.79|EUP 4.76 to 4.79]]

![EUP Figure 4.27|300](../Attachments/PHY1%20Ch04%20Fig%204.27.png)

> [!solution] 答案
> 視重 $n = m(g + a_{y})$：讀數大於 $5\ \mathrm{lb}$ 時加速度向上，小於時向下，等於時 $a_{y} = 0$。
> - **76.** a. 亂流從區間 B 開始，讀數升到約 $5.5\ \mathrm{lb}$。
> - **77.** a. 讀數偏離 $5\ \mathrm{lb}$ 最多的是 B（$0.5\ \mathrm{lb}$；D 約 $0.25\ \mathrm{lb}$）。
> - **78.** d. 讀數等於 $5\ \mathrm{lb}$，加速度為零；靜止不可能（飛機在飛），只能確定鉛直速度不變。
> - **79.** b. $a = \dfrac{5.5 - 5}{5}g = 0.1g \approx 1\ \mathrm{m/s^2}$。

## 外校考題：觀念題

### KSUF 2.3
題目：[[PHY1 HW Ch04 Questions#KSUF 2.3|KSUF 2.3]]

> [!solution] 答案
> a. $\vec{N}$ 是桌子施在木塊上的力，它的力對是木塊施在桌子上、方向相反的力。重力和 $\vec{N}$ 作用在同一物體上，不是力對。

### KSUF 2.5 to 2.7
題目：[[PHY1 HW Ch04 Questions#KSUF 2.5 to 2.7|KSUF 2.5 to 2.7]]

> [!solution] 答案
> - **5.** F. 正向力垂直於路面，不能提供水平加速度；向前的力是路面對輪胎的靜摩擦力。
> - **6.** F. 自由落體只受重力，淨力是 $m\vec{g}$，不是零。
> - **7.** T. 由第三定律，地球吸你，你也以同樣大小的力吸地球。

### KSUF 2.8
題目：[[PHY1 HW Ch04 Questions#KSUF 2.8|KSUF 2.8]]

> [!solution] 答案
> - **a)** a. 向右加速，水平淨力向右：$F_{\mathrm{road}} > F_{\mathrm{air}}$。
> - **b)** b. 鉛直方向不加速：$F_{N} = mg$。

### KSUS 2.5
題目：[[PHY1 HW Ch04 Questions#KSUS 2.5|KSUS 2.5]]

> [!solution] 答案
> F. 靜止只表示**淨力**為零；物體可以受好幾個互相抵消的力，例如桌上的書受重力與正向力。

### KSUS 2.11 to 2.13
題目：[[PHY1 HW Ch04 Questions#KSUS 2.11 to 2.13|KSUS 2.11 to 2.13]]

> [!solution] 答案
> - **11.** T. 質量是物體的內在性質，與位置無關。
> - **12.** F. 月球的 $g$ 較小，重量 $mg$ 也較小。
> - **13.** c. 彈跳床對腳的力，它的力對是腳對彈跳床的力，作用在彈跳床上。

### SIU 23.1 and 23.2
題目：[[PHY1 HW Ch04 Questions#SIU 23.1 and 23.2|SIU 23.1 and 23.2]]

> [!solution] 答案
> - **1.** 零。電梯、體重計和質量都以 $g$ 下落，$n = m(g + a_{y}) = m(g - g) = 0$：表觀失重。
> - **2.** 例如手推牆、牆以同樣大小的力推手；地球吸你、你吸地球。兩個力作用在不同物體上。

## 外校考題：計算題

### KSUF 2.10
題目：[[PHY1 HW Ch04 Questions#KSUF 2.10|KSUF 2.10]]

> [!solution] 答案
> **a)** Michael 受體重計向上的正向力 $\vec{N}$ 與向下的重力 $m\vec{g}$；電梯開始上升，加速度向上，$N > mg$。
>
> **b)** 體重計把正向力換算成「公斤」：$N = (145\ \mathrm{kg})g$，$mg = (88.4\ \mathrm{kg})g$。$y$ 向上，由 (4.3)，$N - mg = ma$：
> $$
> a = \left(\frac{N}{mg} - 1\right)g = \left(\frac{145}{88.4} - 1\right)g = 0.640g \quad \text{（向上）}.
> $$

### KSUS 2.14
題目：[[PHY1 HW Ch04 Questions#KSUS 2.14|KSUS 2.14]]

> [!solution] 答案
> **a)** 向下運動且在減速，加速度**向上**。受力：彈跳繩張力 $\vec{T}$ 向上、空氣阻力 $\vec{F}_{\mathrm{air}}$ 向上（阻礙向下的運動）、重力 $m\vec{g}$ 向下。
>
> **b)** $y$ 向上，$a = \dfrac{\Delta v}{\Delta t} = \dfrac{0 - (-24\ \mathrm{m/s})}{4.0\ \mathrm{s}} = 6.0\ \mathrm{m/s^2}$。由 (4.3)，$T + F_{\mathrm{air}} - mg = ma$：
> $$
> T = m(g + a) - F_{\mathrm{air}} = (65\ \mathrm{kg})(9.80\ \mathrm{m/s^2} + 6.0\ \mathrm{m/s^2}) - 95\ \mathrm{N} = 9.3 \times 10^{2}\ \mathrm{N}.
> $$

> [!warning] 空氣阻力的方向
> 空氣阻力與速度相反，這時是向上，和張力一起減速，所以要從 $m(g + a)$ 扣掉。

### SIU 22.4
題目：[[PHY1 HW Ch04 Questions#SIU 22.4|SIU 22.4]]

> [!solution] 答案
> 向上運動但在減速，加速度向下：$a_{y} = -2.0\ \mathrm{m/s^2}$。由 (4.3)，$n - mg = ma_{y}$：
> $$
> n = m(g + a_{y}) = (75\ \mathrm{kg})(9.8\ \mathrm{m/s^2} - 2.0\ \mathrm{m/s^2}) = 5.9 \times 10^{2}\ \mathrm{N}.
> $$

> [!warning] 減速的方向
> 向上運動時減速，加速度向下，讀數比重量 $735\ \mathrm{N}$ 小。

### SIU 22.5
題目：[[PHY1 HW Ch04 Questions#SIU 22.5|SIU 22.5]]

> [!solution] 答案
> 取 $\vec{F}$ 的方向（向左）為正。整體由 (4.3)：$a = \dfrac{F}{m_{1} + m_{2}} = \dfrac{33\ \mathrm{N}}{30.0\ \mathrm{kg}} = 1.10\ \mathrm{m/s^2}$。$m_{1}$ 只受 $m_{2}$ 的推力：$F_{21} = m_{1}a = (10.0\ \mathrm{kg})(1.10\ \mathrm{m/s^2}) = 11\ \mathrm{N}$。由第三定律，$m_{1}$ 對 $m_{2}$ 的接觸力大小 $11\ \mathrm{N}$，方向與 $\vec{F}$ 相反（向右）。
>
> 檢查：$m_{2}$ 的淨力 $33\ \mathrm{N} - 11\ \mathrm{N} = 22\ \mathrm{N} = (20.0\ \mathrm{kg})(1.10\ \mathrm{m/s^2})$。

### SIU 23.6
題目：[[PHY1 HW Ch04 Questions#SIU 23.6|SIU 23.6]]

> [!solution] 答案
> 繩子無質量、不可伸長，兩質量加速度大小相同，繩上張力處處是 $T$。$m_{1}$ 水平方向：$T = m_{1}a$；$m_{2}$ 取向下為正：$m_{2}g - T = m_{2}a$。相加：
> $$
> a = \frac{m_{2}g}{m_{1} + m_{2}} = \frac{(2.0\ \mathrm{kg})(9.8\ \mathrm{m/s^2})}{3.0\ \mathrm{kg}} = 6.5\ \mathrm{m/s^2} \quad \text{（} m_{2} \text{ 向下）}.
> $$

> [!warning] 張力不是 m₂g
> $m_{2}$ 在加速，$T = m_{1}a = 6.5\ \mathrm{N}$，小於 $m_{2}g = 19.6\ \mathrm{N}$。
