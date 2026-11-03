---
course: [PHY1]
semester: "115-1"
chapter: ["2.1", "2.2", "2.3", "2.4", "2.5", "2.6"]
tags: [physics, homework, solutions, kinematics]
source:
  - "Own solutions; every number recomputed with Python, symbolic results with sympy"
  - "EUP Ch. 2 (pp. 32-49), scanned PDF: equations and answers to GOT IT? questions"
  - "[[PHY1 Ch02 Fig 2.16.png]]"
  - "[[PHY1 Ch02 Problem 2.58 fit.png]]"
  - "[[PHY1 Ch02 KSUF 1.1 acceleration.png]]"
created: 2026-11-01
questions: "[[PHY1 HW Ch02 Questions]]"
up: "[[PHY1 Index]]"
format: "physics-notes 1.1"
---
> [!note] 符號與公式
> - 式號照課本：平均速度 $\bar{v} = \Delta x/\Delta t$ (2.1)；瞬時速度 $v = dx/dt$ (2.2b)；$\dfrac{d(bt^{n})}{dt} = nbt^{n-1}$ (2.3)；平均加速度 $\bar{a} = \Delta v/\Delta t$ (2.4)；$a = dv/dt$ (2.5)；$v(t) = \int a\,dt$ (2.12)、$x(t) = \int v\,dt$ (2.13)，要配初始條件。
> - **只限等加速度**：$v = v_{0} + at$ (2.7)，$x = x_{0} + \tfrac{1}{2}(v_{0} + v)t$ (2.9)，$x = x_{0} + v_{0}t + \tfrac{1}{2}at^{2}$ (2.10)，$v^{2} = v_{0}^{2} + 2a(x - x_{0})$ (2.11)。
> - 自由落體取 $y$ **向上**，$a = -g$，除非解答另外用粗體註明。$g = 9.8\ \mathrm{m/s^2}$；KSU、SIU 的題目用 $9.80\ \mathrm{m/s^2}$。
> - $v$–$t$ 圖：曲線下的面積是位移，斜率是加速度。中間值多留一位有效數字。

## 答案總表

| 題目 | 答案 |
| --- | --- |
| [[PHY1 HW Ch02 Questions#EUP 2.12\|EUP 2.12]] | 約 $1.7 \times 10^{3}\ \mathrm{km/h}$（約 $460\ \mathrm{m/s}$） |
| [[PHY1 HW Ch02 Questions#EUP 2.50\|EUP 2.50]] | $\tfrac{6}{5}v = 1.2v$ |
| [[PHY1 HW Ch02 Questions#EUP 2.19\|EUP 2.19]] | (a) $v = b - 2ct$；(b) $8.2\ \mathrm{s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.53\|EUP 2.53]] | (a) $9.82\ \mathrm{m/s}$；(b) $9.34\ \mathrm{m/s}$；(c) $9.18\ \mathrm{m/s}$；(d) $v = b + 3ct^{2}$，$9.18\ \mathrm{m/s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.21\|EUP 2.21]] | $0.38\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.24\|EUP 2.24]] | $31\ \mathrm{s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.29\|EUP 2.29]] | (a) $\dfrac{v^{2}}{2h}$；(b) $\dfrac{2h}{v}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.34\|EUP 2.34]] | $\dfrac{v_{0}^{2}}{2d}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.63\|EUP 2.63]] | (a) $16\ \mathrm{ms}$；(b) $59\ \mathrm{cm}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.67\|EUP 2.67]] | (a) $25\ \mathrm{m/s}$；(b) $1.8 \times 10^{2}\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.36\|EUP 2.36]] | $10\ \mathrm{m/s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.37\|EUP 2.37]] | (a) $\dfrac{v^{2}}{2g}$；(b) $\dfrac{v}{\sqrt{2}}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.75\|EUP 2.75]] | $\tfrac{1}{2}\sqrt{gh}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.78\|EUP 2.78]] | $2.4\ \mathrm{s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.95\|EUP 2.95]] | (a) $\sqrt{\dfrac{2b}{c}}$；(b) $-5b$ |
| [[PHY1 HW Ch02 Questions#EUP 2.13\|EUP 2.13]] | (a) $24\ \mathrm{km}$ 向北；(b) $9.6\ \mathrm{km/h}$ 向北；(c) $16\ \mathrm{km/h}$ 向南；(d) $0$；(e) $0$ |
| [[PHY1 HW Ch02 Questions#EUP 2.83\|EUP 2.83]] | (a) $\tfrac{1}{2}(v_{1} + v_{2})$；(b) $\dfrac{2v_{1}v_{2}}{v_{1} + v_{2}}$；(c) 情況 (a) |
| [[PHY1 HW Ch02 Questions#EUP 2.84\|EUP 2.84]] | (a) $0.282\ \mathrm{m/s^4}$；(b) $9.25\ \mathrm{m/s}$；(c) $-18.2\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.23\|EUP 2.23]] | (a) $9.82\ \mathrm{m/s^2}$；(b) $82.7\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.66\|EUP 2.66]] | (a) $21\ \mathrm{m/s}$（$77\ \mathrm{km/h}$）；(b) $2.6\ \mathrm{s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.55\|EUP 2.55]] | $14.1\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.70\|EUP 2.70]] | 不會相撞；最接近時相距 $4.3\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.81\|EUP 2.81]] | 會相撞，相對速率 $4.8\ \mathrm{m/s}$（$17\ \mathrm{km/h}$） |
| [[PHY1 HW Ch02 Questions#EUP 2.59\|EUP 2.59]] | $2.75\ \mathrm{s}$（爆炸後 $3.38\ \mathrm{s}$ 到 $6.14\ \mathrm{s}$） |
| [[PHY1 HW Ch02 Questions#EUP 2.73\|EUP 2.73]] | $2.7 \times 10^{2}\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.86\|EUP 2.86]] | 窗戶上緣上方 $1.2\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.90\|EUP 2.90]] | (a) $-9.1\ \mathrm{m/s}$；(b) $-9.1\ \mathrm{m/s}$；(c) $0.18\ \mathrm{s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.77\|EUP 2.77]] | (a) $7.88\ \mathrm{m/s}$ 與 $7.67\ \mathrm{m/s}$；(b) 往上跳的人先入水，早 $0.16\ \mathrm{s}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.97\|EUP 2.97]] | (a) $v_{0} > \sqrt{\dfrac{gh_{0}}{2}}$；(b) $h_{0} - \dfrac{gh_{0}^{2}}{2v_{0}^{2}}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.88\|EUP 2.88]] | (a) $v_{0} + a_{0}t + \tfrac{1}{2}bt^{2}$；(b) $x_{0} + v_{0}t + \tfrac{1}{2}a_{0}t^{2} + \tfrac{1}{6}bt^{3}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.96\|EUP 2.96]] | (a) $\dfrac{a_{0}}{b}\left(1 - e^{-bt}\right)$；(b) 不會；(c) 會 |
| [[PHY1 HW Ch02 Questions#EUP 2.58\|EUP 2.58]] | $x$ 對 $t^{2}$；斜率約 $1.6\ \mathrm{m/s^2}$，$a \approx 3.2\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch02 Questions#EUP 2.98 to 2.102\|EUP 2.98 to 2.102]] | b, c, b, c, b |
| [[PHY1 HW Ch02 Questions#SIU 1.2\|SIU 1.2]] | 減慢 |
| [[PHY1 HW Ch02 Questions#KSUS 1.8\|KSUS 1.8]] | a) $200\ \mathrm{m}$；b) $12.5\ \mathrm{m/s}$；c) $0$ |
| [[PHY1 HW Ch02 Questions#KSUS 1.9\|KSUS 1.9]] | a) $3.5 \times 10^{2}\ \mathrm{m/s^2}$；b) $0.82\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#KSUS 1.10\|KSUS 1.10]] | $19.2\ \mathrm{m/s^2} = 1.96g$ |
| [[PHY1 HW Ch02 Questions#KSUS 1.11\|KSUS 1.11]] | a) $145\ \mathrm{m}$；b) $54.6\ \mathrm{m/s}$ |
| [[PHY1 HW Ch02 Questions#KSUF 1.1\|KSUF 1.1]] | a) $18.8\ \mathrm{m}$；b) $1.8\ \mathrm{m/s}$；c) $0$、$10\ \mathrm{m/s^2}$、$0$ |
| [[PHY1 HW Ch02 Questions#KSUF 1.3\|KSUF 1.3]] | a) $3.2 \times 10^{4}\ \mathrm{m/s^2}$，向北；b) $2.1\ \mathrm{cm}$，向北 |
| [[PHY1 HW Ch02 Questions#KSUF 1.4\|KSUF 1.4]] | a) $49.0\ \mathrm{m/s}$；b) $123\ \mathrm{m}$ |
| [[PHY1 HW Ch02 Questions#SIU 1.5\|SIU 1.5]] | $11\ \mathrm{m}$ |

## 老師勾選：平均速度與平均速率

### EUP 2.12
題目：[[PHY1 HW Ch02 Questions#EUP 2.12|EUP 2.12]]

> [!solution] 答案
> 赤道上一點每 $24\ \mathrm{h}$ 繞一圈，走過周長 $\pi D$：
> $$
> v = \frac{\pi D}{T} = \frac{\pi(12{,}700\ \mathrm{km})}{24\ \mathrm{h}} = 1.66 \times 10^{3}\ \mathrm{km/h} \approx 1.7 \times 10^{3}\ \mathrm{km/h} \approx 460\ \mathrm{m/s}
> $$

### EUP 2.50
題目：[[PHY1 HW Ch02 Questions#EUP 2.50|EUP 2.50]]

> [!solution] 答案
> 總距離 $D$，總時間
> $$
> t = \frac{D/3}{2v} + \frac{2D/3}{v} = \frac{5D}{6v} \implies \bar{v} = \frac{D}{t} = \frac{6}{5}v = 1.2v
> $$

> [!warning] 不是速率的平均
> 不是 $\tfrac{1}{2}(2v + v) = 1.5v$：平均速率是總距離除以總時間，慢的那段花的時間較多。

## 老師勾選：由位置函數求速度

### EUP 2.19
題目：[[PHY1 HW Ch02 Questions#EUP 2.19|EUP 2.19]]

> [!solution] 答案
> (a) 由 (2.2b) 與 (2.3)：
> $$
> v = \frac{dy}{dt} = b - 2ct = 80\ \mathrm{m/s} - (9.8\ \mathrm{m/s^2})t
> $$
> (b) $v = 0$ 時 $t = \dfrac{b}{2c} = \dfrac{80\ \mathrm{m/s}}{2(4.9\ \mathrm{m/s^2})} = 8.2\ \mathrm{s}$。

### EUP 2.53
題目：[[PHY1 HW Ch02 Questions#EUP 2.53|EUP 2.53]]

> [!solution] 答案
> 由 (2.1)，用 $t_{2}^{3} - t_{1}^{3} = (t_{2} - t_{1})(t_{1}^{2} + t_{1}t_{2} + t_{2}^{2})$：
> $$
> \bar{v} = \frac{x(t_{2}) - x(t_{1})}{t_{2} - t_{1}} = b + c\left(t_{1}^{2} + t_{1}t_{2} + t_{2}^{2}\right)
> $$
> - (a) $1.50 + 0.640(1 + 3 + 9) = 9.82\ \mathrm{m/s}$。
> - (b) $1.50 + 0.640(2.25 + 3.75 + 6.25) = 9.34\ \mathrm{m/s}$。
> - (c) $1.50 + 0.640(3.8025 + 3.9975 + 4.2025) = 9.18\ \mathrm{m/s}$。
> - (d) $v = \dfrac{dx}{dt} = b + 3ct^{2}$，$v(2\ \mathrm{s}) = 1.50 + 3(0.640)(4) = 9.18\ \mathrm{m/s}$。區間越短，平均速度越接近瞬時速度。

## 老師勾選：平均加速度

### EUP 2.21
題目：[[PHY1 HW Ch02 Questions#EUP 2.21|EUP 2.21]]

> [!solution] 答案
> 由 (2.4)，只看起點和終點的速度：
> $$
> \bar{a} = \frac{\Delta v}{\Delta t} = \frac{18\ \mathrm{m/s} - 0}{48\ \mathrm{s}} = 0.38\ \mathrm{m/s^2}
> $$

> [!warning] 多餘的數據
> 中間的最高速率 $25\ \mathrm{m/s}$ 用不到。

### EUP 2.24
題目：[[PHY1 HW Ch02 Questions#EUP 2.24|EUP 2.24]]

> [!solution] 答案
> $v = 320\ \mathrm{km/h} = 88.9\ \mathrm{m/s}$，由靜止加速，由 (2.4)：
> $$
> \Delta t = \frac{\Delta v}{\bar{a}} = \frac{88.9\ \mathrm{m/s}}{2.9\ \mathrm{m/s^2}} = 31\ \mathrm{s}
> $$

## 老師勾選：等加速度（一個物體）

### EUP 2.29
題目：[[PHY1 HW Ch02 Questions#EUP 2.29|EUP 2.29]]

> [!solution] 答案
> $v_{0} = 0$。(a) 由 (2.11)：$v^{2} = 2ah \implies a = \dfrac{v^{2}}{2h}$。(b) 由 (2.9)：$h = \tfrac{1}{2}(0 + v)t \implies t = \dfrac{2h}{v}$。

### EUP 2.34
題目：[[PHY1 HW Ch02 Questions#EUP 2.34|EUP 2.34]]

> [!solution] 答案
> 取行駛方向為 $+x$，最遲在 $\Delta x = d$ 處停下（$v = 0$）。由 (2.11)：
> $$
> 0 = v_{0}^{2} + 2ad \implies \lvert a \rvert = \frac{v_{0}^{2}}{2d}
> $$
> 加速度大小至少要這麼大。

### EUP 2.63
題目：[[PHY1 HW Ch02 Questions#EUP 2.63|EUP 2.63]]

> [!solution] 答案
> $v_{0} = 30\ \mathrm{m/s}$，$v = 18\ \mathrm{m/s}$，$\Delta x = 0.38\ \mathrm{m}$。(a) 由 (2.9)：
> $$
> t = \frac{2\Delta x}{v_{0} + v} = \frac{2(0.38\ \mathrm{m})}{48\ \mathrm{m/s}} = 0.016\ \mathrm{s} = 16\ \mathrm{ms}
> $$
> (b) 由 (2.11)，$a = \dfrac{v^{2} - v_{0}^{2}}{2\Delta x} = -758\ \mathrm{m/s^2}$。停下所需厚度：
> $$
> d = \frac{v_{0}^{2}}{2\lvert a \rvert} = \Delta x\,\frac{v_{0}^{2}}{v_{0}^{2} - v^{2}} = (0.38\ \mathrm{m})\frac{900}{576} = 0.59\ \mathrm{m} = 59\ \mathrm{cm}
> $$

### EUP 2.67
題目：[[PHY1 HW Ch02 Questions#EUP 2.67|EUP 2.67]]

> [!solution] 答案
> (a) 由 (2.9)，$\Delta x = \tfrac{1}{2}(v_{0} + v)t$：
> $$
> v_{0} = \frac{2\Delta x}{t} - v = \frac{2(140\ \mathrm{m})}{3.6\ \mathrm{s}} - 53\ \mathrm{m/s} = 24.8\ \mathrm{m/s} \approx 25\ \mathrm{m/s}
> $$
> (b) $a = \dfrac{v - v_{0}}{t} = \dfrac{53 - 24.8}{3.6} = 7.84\ \mathrm{m/s^2}$。從靜止到末速 $53\ \mathrm{m/s}$，由 (2.11)：
> $$
> x = \frac{v^{2}}{2a} = \frac{(53\ \mathrm{m/s})^{2}}{2(7.84\ \mathrm{m/s^2})} = 1.8 \times 10^{2}\ \mathrm{m}
> $$

> [!warning] 不是從靜止出發
> 這 $140\ \mathrm{m}$ 開始時車已經在動，不能用 $140 = \tfrac{1}{2}at^{2}$。

## 老師勾選：自由落體

### EUP 2.36
題目：[[PHY1 HW Ch02 Questions#EUP 2.36|EUP 2.36]]

> [!solution] 答案
> 恰好到達表示到她那裡時 $v = 0$。由 (2.11)，$0 = v_{0}^{2} - 2gh$：
> $$
> v_{0} = \sqrt{2gh} = \sqrt{2(9.8\ \mathrm{m/s^2})(5.1\ \mathrm{m})} = 10\ \mathrm{m/s}
> $$

### EUP 2.37
題目：[[PHY1 HW Ch02 Questions#EUP 2.37|EUP 2.37]]

> [!solution] 答案
> 由 (2.11)，$v_{y}^{2} = v^{2} - 2gy$。
> - (a) 最高點 $v_{y} = 0$：$y_{\max} = \dfrac{v^{2}}{2g}$。
> - (b) $y = \tfrac{1}{2}y_{\max}$：$v_{y}^{2} = v^{2} - \tfrac{1}{2}v^{2}$，速率 $\dfrac{v}{\sqrt{2}}$。

### EUP 2.75
題目：[[PHY1 HW Ch02 Questions#EUP 2.75|EUP 2.75]]

> [!solution] 答案
> 取 $y$ **向下**，$a = +g$。朋友的球由靜止落下 $h/2$：$\tfrac{h}{2} = \tfrac{1}{2}gt^{2}$，$t = \sqrt{h/g}$。你的球在同一時間落下 $h$，由 (2.10)：
> $$
> h = v_{0}t + \tfrac{1}{2}gt^{2} = v_{0}t + \tfrac{h}{2} \implies v_{0} = \frac{h/2}{\sqrt{h/g}} = \tfrac{1}{2}\sqrt{gh}
> $$

### EUP 2.78
題目：[[PHY1 HW Ch02 Questions#EUP 2.78|EUP 2.78]]

> [!solution] 答案
> 取地面為原點、$y$ 向上。球的初速 $10 + 12 = 22\ \mathrm{m/s}$，乘客等速 $10\ \mathrm{m/s}$。由 (2.10)：
> $$
> (22\ \mathrm{m/s})t - \tfrac{1}{2}gt^{2} = (10\ \mathrm{m/s})t \implies t = \frac{2(12\ \mathrm{m/s})}{9.8\ \mathrm{m/s^2}} = 2.4\ \mathrm{s}
> $$
> （$t = 0$ 是丟出的瞬間。）

> [!warning] 氣球的速度用不到
> 答案只和相對速度 $12\ \mathrm{m/s}$ 有關：在等速上升的氣球上看，就是一般的上拋。

## 老師勾選：非等加速度

### EUP 2.95
題目：[[PHY1 HW Ch02 Questions#EUP 2.95|EUP 2.95]]

> [!solution] 答案
> 由 (2.13)，$x(0) = 0$：
> $$
> x = \int_{0}^{t}(bt' - ct'^{3})\,dt' = \tfrac{1}{2}bt^{2} - \tfrac{1}{4}ct^{4} = t^{2}\left(\tfrac{1}{2}b - \tfrac{1}{4}ct^{2}\right)
> $$
> - (a) $x = 0$ 且 $t > 0$：$t = \sqrt{\dfrac{2b}{c}}$。
> - (b) $a = \dfrac{dv}{dt} = b - 3ct^{2} = b - 3c\left(\dfrac{2b}{c}\right) = -5b$。

## 加選：平均速度與平均速率

### EUP 2.13
題目：[[PHY1 HW Ch02 Questions#EUP 2.13|EUP 2.13]]

> [!solution] 答案
> 取北為正、家為原點。
> - (a) $\Delta x = +24\ \mathrm{km}$（向北）。
> - (b) $\bar{v} = \dfrac{24\ \mathrm{km}}{2.5\ \mathrm{h}} = 9.6\ \mathrm{km/h}$，向北。
> - (c) $\bar{v} = \dfrac{-24\ \mathrm{km}}{1.5\ \mathrm{h}} = -16\ \mathrm{km/h}$，即 $16\ \mathrm{km/h}$ 向南。
> - (d) 回到家，$\Delta x = 0$。
> - (e) $\bar{v} = 0/(4.0\ \mathrm{h}) = 0$（平均速率是 $48\ \mathrm{km}/4.0\ \mathrm{h} = 12\ \mathrm{km/h}$）。

### EUP 2.83
題目：[[PHY1 HW Ch02 Questions#EUP 2.83|EUP 2.83]]

> [!solution] 答案
> - (a) 總時間 $T$，各用 $T/2$：$L = v_{1}\tfrac{T}{2} + v_{2}\tfrac{T}{2}$，$\bar{v} = \dfrac{L}{T} = \tfrac{1}{2}(v_{1} + v_{2})$。
> - (b) 各走 $L/2$：$T = \dfrac{L}{2v_{1}} + \dfrac{L}{2v_{2}}$，$\bar{v} = \dfrac{L}{T} = \dfrac{2v_{1}v_{2}}{v_{1} + v_{2}}$。
> - (c) 兩者相減：
> $$
> \tfrac{1}{2}(v_{1} + v_{2}) - \frac{2v_{1}v_{2}}{v_{1} + v_{2}} = \frac{(v_{1} - v_{2})^{2}}{2(v_{1} + v_{2})} \geq 0
> $$
> 情況 (a) 較大（$v_{1} = v_{2}$ 時相等）。

## 加選：由位置函數求速度與加速度

### EUP 2.84
題目：[[PHY1 HW Ch02 Questions#EUP 2.84|EUP 2.84]]

> [!solution] 答案
> (a) $0 = bt^{2} - ct^{4}$，$t \neq 0$：$c = \dfrac{b}{t^{2}} = \dfrac{1.82\ \mathrm{m/s^2}}{(2.54\ \mathrm{s})^{2}} = 0.282\ \mathrm{m/s^4}$。
>
> 代入 $ct^{2} = b$：
> - (b) $v = 2bt - 4ct^{3} = 2bt - 4bt = -2bt = -9.25\ \mathrm{m/s}$，速率 $9.25\ \mathrm{m/s}$。
> - (c) $a = 2b - 12ct^{2} = -10b = -18.2\ \mathrm{m/s^2}$。

## 加選：平均加速度

### EUP 2.23
題目：[[PHY1 HW Ch02 Questions#EUP 2.23|EUP 2.23]]

> [!solution] 答案
> 由 (2.4)：
> - (a) $\lvert \bar{a} \rvert = \dfrac{11.0\ \mathrm{m/s}}{1.12\ \mathrm{s}} = 9.82\ \mathrm{m/s^2}$。
> - (b) $\lvert \bar{a} \rvert = \dfrac{11.0\ \mathrm{m/s}}{0.133\ \mathrm{s}} = 82.7\ \mathrm{m/s^2}$。

## 加選：等加速度（一個物體）

### EUP 2.66
題目：[[PHY1 HW Ch02 Questions#EUP 2.66|EUP 2.66]]

> [!solution] 答案
> 取行駛方向為正：$v = 18\ \mathrm{km/h} = 5.0\ \mathrm{m/s}$，$a = -6.3\ \mathrm{m/s^2}$，$\Delta x = 34\ \mathrm{m}$。(a) 由 (2.11)：
> $$
> v_{0} = \sqrt{v^{2} - 2a\Delta x} = \sqrt{(5.0\ \mathrm{m/s})^{2} + 2(6.3\ \mathrm{m/s^2})(34\ \mathrm{m})} = 21\ \mathrm{m/s} = 77\ \mathrm{km/h}
> $$
> (b) 由 (2.7)：$t = \dfrac{v - v_{0}}{a} = \dfrac{5.0 - 21.3}{-6.3}\ \mathrm{s} = 2.6\ \mathrm{s}$。

> [!warning] 末速度不是零
> 撞上時車速還有 $18\ \mathrm{km/h}$，不能令 $v = 0$。

## 加選：等加速度（兩個物體）

### EUP 2.55
題目：[[PHY1 HW Ch02 Questions#EUP 2.55|EUP 2.55]]

> [!solution] 答案
> 兩車都由靜止出發，由 (2.10)，$L = 400\ \mathrm{m} = \tfrac{1}{2}at^{2}$。勝者 $t_{\mathrm{w}} = \sqrt{2L/a_{\mathrm{w}}} = 13.72\ \mathrm{s}$；敗者 $t_{\mathrm{L}} = t_{\mathrm{w}} + 0.248\ \mathrm{s} = 13.97\ \mathrm{s}$。勝者到終點時，敗者走了
> $$
> x_{\mathrm{L}} = \tfrac{1}{2}a_{\mathrm{L}}t_{\mathrm{w}}^{2} = L\left(\frac{t_{\mathrm{w}}}{t_{\mathrm{L}}}\right)^{2} = (400\ \mathrm{m})\left(\frac{13.72}{13.97}\right)^{2} = 385.9\ \mathrm{m}
> $$
> 落後 $400\ \mathrm{m} - 385.9\ \mathrm{m} = 14.1\ \mathrm{m}$。

### EUP 2.70
題目：[[PHY1 HW Ch02 Questions#EUP 2.70|EUP 2.70]]

> [!solution] 答案
> 取 $x = 0$ 在你的車、$t = 0$ 在開始煞車：$v_{1} - v_{2} = 25\ \mathrm{km/h} = 6.94\ \mathrm{m/s}$，$a = 4.2\ \mathrm{m/s^2}$（大小），$d = 10\ \mathrm{m}$。兩車間距
> $$
> s(t) = (d + v_{2}t) - \left(v_{1}t - \tfrac{1}{2}at^{2}\right) = d - (v_{1} - v_{2})t + \tfrac{1}{2}at^{2}
> $$
> 在 $\dfrac{ds}{dt} = 0$，即 $t = \dfrac{v_{1} - v_{2}}{a} = 1.65\ \mathrm{s}$ 時最小：
> $$
> s_{\min} = d - \frac{(v_{1} - v_{2})^{2}}{2a} = 10\ \mathrm{m} - \frac{(6.94\ \mathrm{m/s})^{2}}{2(4.2\ \mathrm{m/s^2})} = 4.3\ \mathrm{m} > 0
> $$
> 不會相撞；最接近時相距 $4.3\ \mathrm{m}$。

> [!warning] 最接近的時刻
> 最接近發生在兩車速度相等時，不是你的車停下時。

### EUP 2.81
題目：[[PHY1 HW Ch02 Questions#EUP 2.81|EUP 2.81]]

> [!solution] 答案
> 在慢車上看（慢車等速，這個參考系中加速度不變）：快車的相對初速 $u_{0} = 80 - 25 = 55\ \mathrm{km/h} = 15.3\ \mathrm{m/s}$，相對加速度 $-2.1\ \mathrm{m/s^2}$，要拉近 $50\ \mathrm{m}$。由 (2.11)：
> $$
> u^{2} = u_{0}^{2} - 2(2.1\ \mathrm{m/s^2})(50\ \mathrm{m}) = 233.4 - 210 = 23.4\ \mathrm{m^2/s^2} > 0
> $$
> 會相撞，相對速率 $u = 4.8\ \mathrm{m/s} = 17\ \mathrm{km/h}$。（撞擊時快車仍在前進，約 $12\ \mathrm{m/s}$。）

## 加選：自由落體（一個物體）

### EUP 2.59
題目：[[PHY1 HW Ch02 Questions#EUP 2.59|EUP 2.59]]

> [!solution] 答案
> 地面 $y = 0$，$y_{0} = 82.0\ \mathrm{m}$。由 (2.10)，$0 = y_{0} + v_{0}t - \tfrac{1}{2}gt^{2}$，取正根：
> $$
> t = \frac{v_{0} + \sqrt{v_{0}^{2} + 2gy_{0}}}{g}
> $$
> - 最早落地（$v_{0} = -7.68\ \mathrm{m/s}$）：$t = 3.38\ \mathrm{s}$。
> - 最晚落地（$v_{0} = +16.7\ \mathrm{m/s}$）：$t = 6.14\ \mathrm{s}$。
>
> 碎片在爆炸後 $3.38\ \mathrm{s}$ 到 $6.14\ \mathrm{s}$ 之間落地，區間長 $2.75\ \mathrm{s}$。

### EUP 2.73
題目：[[PHY1 HW Ch02 Questions#EUP 2.73|EUP 2.73]]

> [!solution] 答案
> 總時間 $T$，$h = \tfrac{1}{2}gT^{2}$。前 $T - 1\ \mathrm{s}$ 落下 $\tfrac{3}{4}h$：
> $$
> \begin{aligned}
> \tfrac{1}{2}g(T - 1\ \mathrm{s})^{2} = \tfrac{3}{4}\cdot\tfrac{1}{2}gT^{2} &\implies \frac{T - 1\ \mathrm{s}}{T} = \frac{\sqrt{3}}{2} \\
> &\implies T = \frac{1\ \mathrm{s}}{1 - \sqrt{3}/2} = 7.46\ \mathrm{s}
> \end{aligned}
> $$
> （另一根 $T = 0.54\ \mathrm{s} < 1\ \mathrm{s}$，不合。）$h = \tfrac{1}{2}(9.8\ \mathrm{m/s^2})(7.46\ \mathrm{s})^{2} = 2.7 \times 10^{2}\ \mathrm{m}$。

### EUP 2.86
題目：[[PHY1 HW Ch02 Questions#EUP 2.86|EUP 2.86]]

> [!solution] 答案
> 取 $y$ **向下**，$a = +g$。設水球到窗戶上緣時速度 $v_{\mathrm{t}}$，通過窗戶，由 (2.10)：
> $$
> \Delta y = v_{\mathrm{t}}t + \tfrac{1}{2}gt^{2} \implies v_{\mathrm{t}} = \frac{1.3\ \mathrm{m} - \tfrac{1}{2}(9.8\ \mathrm{m/s^2})(0.22\ \mathrm{s})^{2}}{0.22\ \mathrm{s}} = 4.83\ \mathrm{m/s}
> $$
> 從靜止到窗戶上緣，由 (2.11)：
> $$
> H = \frac{v_{\mathrm{t}}^{2}}{2g} = \frac{(4.83\ \mathrm{m/s})^{2}}{2(9.8\ \mathrm{m/s^2})} = 1.2\ \mathrm{m}
> $$

> [!warning] 不是從靜止通過窗戶
> 不能令 $1.3\ \mathrm{m} = \tfrac{1}{2}gt^{2}$：水球到窗戶上緣時已經在動。

### EUP 2.90
題目：[[PHY1 HW Ch02 Questions#EUP 2.90|EUP 2.90]]

> [!solution] 答案
> 地板 $y = 0$，$y_{0} = 1.5\ \mathrm{m}$。(a)、(b) 由 (2.11)，落到地板時 $v^{2} = v_{0}^{2} + 2gy_{0}$，只和 $v_{0}^{2}$ 有關，往上或往下丟都一樣：
> $$
> v = -\sqrt{(7.3\ \mathrm{m/s})^{2} + 2(9.8\ \mathrm{m/s^2})(1.5\ \mathrm{m})} = -9.1\ \mathrm{m/s}
> $$
> (c) 由 (2.10)，$0 = 1.5 - 7.3t - 4.9t^{2}$（SI 單位）：
> $$
> t = \frac{-7.3 \pm 9.09}{9.8}\ \mathrm{s} = 0.18\ \mathrm{s} \ \text{或} \ -1.67\ \mathrm{s}
> $$
> 第二顆球在 $0.18\ \mathrm{s}$ 落地。負根表示：若這顆球一直在自由落體，它會在 $1.67\ \mathrm{s}$ 前從地板往上出發，經過手時恰好以 $7.3\ \mathrm{m/s}$ 往下（與第一顆球的運動對稱）。

## 加選：自由落體（兩個物體）

### EUP 2.77
題目：[[PHY1 HW Ch02 Questions#EUP 2.77|EUP 2.77]]

> [!solution] 答案
> 水面 $y = 0$，跳台 $y_{0} = 3.00\ \mathrm{m}$，從第一人往下經過跳台時計時：第一人 $v_{0} = -1.80\ \mathrm{m/s}$（回到跳台時速率不變），第二人 $v_{0} = 0$。
>
> (a) 由 (2.11)：
> $$
> \begin{aligned}
> v_{1} &= \sqrt{(1.80\ \mathrm{m/s})^{2} + 2(9.8\ \mathrm{m/s^2})(3.00\ \mathrm{m})} = 7.88\ \mathrm{m/s} \\
> v_{2} &= \sqrt{2(9.8\ \mathrm{m/s^2})(3.00\ \mathrm{m})} = 7.67\ \mathrm{m/s}
> \end{aligned}
> $$
> (b) 由 (2.10)，$3.00 = 1.80t_{1} + 4.9t_{1}^{2}$ 得 $t_{1} = 0.620\ \mathrm{s}$；$t_{2} = \sqrt{2(3.00)/9.8}\ \mathrm{s} = 0.782\ \mathrm{s}$。往上跳的人先入水，早 $0.16\ \mathrm{s}$。

### EUP 2.97
題目：[[PHY1 HW Ch02 Questions#EUP 2.97|EUP 2.97]]

> [!solution] 答案
> 地面 $y = 0$。由 (2.10)：$y_{1} = h_{0} - \tfrac{1}{2}gt^{2}$，$y_{2} = v_{0}t - \tfrac{1}{2}gt^{2}$。令 $y_{1} = y_{2}$：$t = \dfrac{h_{0}}{v_{0}}$。
>
> (a) 要在第二顆球落回地面（$t = 2v_{0}/g$）之前相撞：
> $$
> \frac{h_{0}}{v_{0}} < \frac{2v_{0}}{g} \implies v_{0} > \sqrt{\frac{gh_{0}}{2}}
> $$
> （這也保證第一顆球還沒落地：$h_{0}/v_{0} < \sqrt{2h_{0}/g}$ 是同一個條件。）
>
> (b) $y = h_{0} - \tfrac{1}{2}g\left(\dfrac{h_{0}}{v_{0}}\right)^{2} = h_{0} - \dfrac{gh_{0}^{2}}{2v_{0}^{2}}$。

## 加選：非等加速度

### EUP 2.88
題目：[[PHY1 HW Ch02 Questions#EUP 2.88|EUP 2.88]]

> [!solution] 答案
> 由 (2.12)、(2.13)，積分常數由 $v(0) = v_{0}$、$x(0) = x_{0}$ 決定：
> $$
> \begin{aligned}
> v &= v_{0} + \int_{0}^{t}(a_{0} + bt')\,dt' = v_{0} + a_{0}t + \tfrac{1}{2}bt^{2} \\
> x &= x_{0} + \int_{0}^{t}v\,dt' = x_{0} + v_{0}t + \tfrac{1}{2}a_{0}t^{2} + \tfrac{1}{6}bt^{3}
> \end{aligned}
> $$

### EUP 2.96
題目：[[PHY1 HW Ch02 Questions#EUP 2.96|EUP 2.96]]

> [!solution] 答案
> (a) 由 (2.12)，$v(0) = 0$：
> $$
> v = \int_{0}^{t}a_{0}e^{-bt'}\,dt' = \frac{a_{0}}{b}\left(1 - e^{-bt}\right)
> $$
> - (b) 不會。$t \to \infty$ 時 $v \to a_{0}/b$，速率趨近這個上限。
> - (c) 會。速度趨近定值 $a_{0}/b > 0$，$x = \dfrac{a_{0}}{b}t - \dfrac{a_{0}}{b^{2}}\left(1 - e^{-bt}\right)$ 隨時間無限增加。

## 加選：數據題

### EUP 2.58
題目：[[PHY1 HW Ch02 Questions#EUP 2.58|EUP 2.58]]

> [!solution] 答案
> 由靜止出發、等加速度，(2.10) 成為 $x = \tfrac{1}{2}at^{2}$，所以畫 $x$ 對 $t^{2}$：
>
> | $t^{2}$ ($\mathrm{s^2}$) | $0$ | $1$ | $4$ | $9$ | $16$ | $25$ |
> | --- | --- | --- | --- | --- | --- | --- |
> | $x$ ($\mathrm{m}$) | $0$ | $1.7$ | $6.2$ | $17$ | $24$ | $40$ |
>
> 過原點的最佳擬合直線斜率 $\approx 1.6\ \mathrm{m/s^2} = \tfrac{1}{2}a$，所以 $a \approx 3.2\ \mathrm{m/s^2}$。
>
> ![EUP 2.58 fit|480](../Attachments/PHY1%20Ch02%20Problem%202.58%20fit.png)

## 加選：讀速度–時間圖

### EUP 2.98 to 2.102
題目：[[PHY1 HW Ch02 Questions#EUP 2.98 to 2.102|EUP 2.98 to 2.102]]

![EUP Figure 2.16|400](../Attachments/PHY1%20Ch02%20Fig%202.16.png)

> [!solution] 答案
> $v$–$t$ 圖上，曲線的高度是 $v$，斜率是 $a$，曲線下的面積是位移。
> - **98.** b. $v = 0$ 在曲線碰到時間軸處：A、E、H。
> - **99.** c. $a = 0$ 在斜率為零處：C 和 F。
> - **100.** b. $\lvert v \rvert$ 最大在 C（離時間軸最遠）。
> - **101.** c. 斜率最陡在 D。
> - **102.** b. A 到 E 之間 $v > 0$，老虎一直遠離起點；E 之後 $v < 0$ 往回走。所以 E 時最遠。

## 外校考題：觀念題

### SIU 1.2
題目：[[PHY1 HW Ch02 Questions#SIU 1.2|SIU 1.2]]

> [!solution] 答案
> 減慢。$x$–$t$ 曲線的斜率是速度：$2.0\ \mathrm{h}$ 時斜率為正，但越來越平，到 $3.0\ \mathrm{h}$ 的最高點變成零，所以速率在減少（$v > 0$、$a < 0$）。

## 外校考題：計算題

### KSUS 1.8
題目：[[PHY1 HW Ch02 Questions#KSUS 1.8|KSUS 1.8]]

> [!solution] 答案
> - a) 位移是 $v$–$t$ 曲線下的三角形面積：$\Delta x = \tfrac{1}{2}(12.0\ \mathrm{s})(25\ \mathrm{m/s}) = 150\ \mathrm{m}$，$x = 50.0\ \mathrm{m} + 150\ \mathrm{m} = 200\ \mathrm{m}$。
> - b) $\bar{v} = \dfrac{150\ \mathrm{m}}{12.0\ \mathrm{s}} = 12.5\ \mathrm{m/s}$。
> - c) 始末速度都是 $0$：$\bar{a} = \dfrac{0 - 0}{12.0\ \mathrm{s}} = 0$。

### KSUS 1.9
題目：[[PHY1 HW Ch02 Questions#KSUS 1.9|KSUS 1.9]]

> [!solution] 答案
> 取原方向為正：$v_{0} = 24\ \mathrm{m/s}$，$v = -18\ \mathrm{m/s}$。
> - a) $\lvert \bar{a} \rvert = \dfrac{\lvert -18 - 24 \rvert\ \mathrm{m/s}}{0.120\ \mathrm{s}} = 350\ \mathrm{m/s^2} = 3.5 \times 10^{2}\ \mathrm{m/s^2}$。
> - b) 由 (2.11)，$v = 0$：$\Delta x = \dfrac{v_{0}^{2}}{2\lvert a \rvert} = \dfrac{(24\ \mathrm{m/s})^{2}}{2(350\ \mathrm{m/s^2})} = 0.82\ \mathrm{m}$。

> [!warning] 反轉方向
> 速度改變量是 $24 + 18 = 42\ \mathrm{m/s}$，不是 $24 - 18$。

### KSUS 1.10
題目：[[PHY1 HW Ch02 Questions#KSUS 1.10|KSUS 1.10]]

> [!solution] 答案
> 取搶匪經過警車時 $x = 0$、$t = 0$。由 (2.10)，$x_{\mathrm{r}} = vt$，$x_{\mathrm{p}} = \tfrac{1}{2}at^{2}$；在 $t = 5.00\ \mathrm{s}$ 相等：
> $$
> a = \frac{2v}{t} = \frac{2(48.0\ \mathrm{m/s})}{5.00\ \mathrm{s}} = 19.2\ \mathrm{m/s^2} = \frac{19.2}{9.80}g = 1.96g
> $$

### KSUS 1.11
題目：[[PHY1 HW Ch02 Questions#KSUS 1.11|KSUS 1.11]]

> [!solution] 答案
> 取拋出點 $y = 0$、向上為正，$v_{0} = 12.0\ \mathrm{m/s}$，$t = 6.80\ \mathrm{s}$。
> - a) 由 (2.10)：$y = v_{0}t - \tfrac{1}{2}gt^{2} = (12.0)(6.80) - \tfrac{1}{2}(9.80)(6.80)^{2} = -145\ \mathrm{m}$，懸崖高 $145\ \mathrm{m}$。
> - b) 由 (2.7)：$v = v_{0} - gt = 12.0 - (9.80)(6.80) = -54.6\ \mathrm{m/s}$，速率 $54.6\ \mathrm{m/s}$。

### KSUF 1.1
題目：[[PHY1 HW Ch02 Questions#KSUF 1.1|KSUF 1.1]]

> [!solution] 答案
> - a) 位移是曲線下的有號面積：
> $$
> \Delta x = (-5\ \mathrm{m/s})(2.0\ \mathrm{s}) + \tfrac{1}{2}(-5 + 10)\ \mathrm{m/s}\,(1.5\ \mathrm{s}) + (10\ \mathrm{m/s})(1.5\ \mathrm{s}) = 8.75\ \mathrm{m}
> $$
> $x = 10.0\ \mathrm{m} + 8.75\ \mathrm{m} = 18.8\ \mathrm{m}$。
> - b) $\bar{v} = \dfrac{8.75\ \mathrm{m}}{5.0\ \mathrm{s}} = 1.8\ \mathrm{m/s}$。
> - c) $a$ 是斜率：$0$ 到 $2.0\ \mathrm{s}$ 為 $0$；$2.0$ 到 $3.5\ \mathrm{s}$ 為 $\dfrac{15\ \mathrm{m/s}}{1.5\ \mathrm{s}} = 10\ \mathrm{m/s^2}$；$3.5$ 到 $5.0\ \mathrm{s}$ 為 $0$。
>
> ![KSUF 1.1 acceleration|420](../Attachments/PHY1%20Ch02%20KSUF%201.1%20acceleration.png)

### KSUF 1.3
題目：[[PHY1 HW Ch02 Questions#KSUF 1.3|KSUF 1.3]]

> [!solution] 答案
> 取北為正，$1\ \mathrm{mph} = 0.4470\ \mathrm{m/s}$：$v_{0} = -98\ \mathrm{mph} = -43.8\ \mathrm{m/s}$，$v = 128\ \mathrm{mph} = 57.2\ \mathrm{m/s}$，$t = 3.2 \times 10^{-3}\ \mathrm{s}$。
> - a) 由 (2.4)：$\bar{a} = \dfrac{57.2 - (-43.8)}{3.2 \times 10^{-3}}\ \mathrm{m/s^2} = 3.2 \times 10^{4}\ \mathrm{m/s^2}$，向北。
> - b) 由 (2.9)：$\Delta x = \tfrac{1}{2}(v_{0} + v)t = \tfrac{1}{2}(13.4\ \mathrm{m/s})(3.2 \times 10^{-3}\ \mathrm{s}) = 2.1 \times 10^{-2}\ \mathrm{m} = 2.1\ \mathrm{cm}$，向北。

### KSUF 1.4
題目：[[PHY1 HW Ch02 Questions#KSUF 1.4|KSUF 1.4]]

> [!solution] 答案
> - a) 上升與下降時間對稱，上升 $5.00\ \mathrm{s}$ 到 $v = 0$，由 (2.7)：$v_{0} = gt_{\mathrm{up}} = (9.80\ \mathrm{m/s^2})(5.00\ \mathrm{s}) = 49.0\ \mathrm{m/s}$。
> - b) 由 (2.11)：$h = \dfrac{v_{0}^{2}}{2g} = \dfrac{(49.0\ \mathrm{m/s})^{2}}{2(9.80\ \mathrm{m/s^2})} = 123\ \mathrm{m}$。

### SIU 1.5
題目：[[PHY1 HW Ch02 Questions#SIU 1.5|SIU 1.5]]

> [!solution] 答案
> 最高點 $v = 0$，由 (2.11)：
> $$
> \Delta y = \frac{v_{0}^{2}}{2g} = \frac{(15\ \mathrm{m/s})^{2}}{2(9.80\ \mathrm{m/s^2})} = 11\ \mathrm{m}
> $$

> [!warning] 建築高度用不到
> 問的是建築上方多高，$50.0\ \mathrm{m}$ 是多餘的數據。
