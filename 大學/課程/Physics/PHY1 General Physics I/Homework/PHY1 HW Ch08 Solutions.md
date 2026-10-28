---
course: [PHY1]
semester: "115-1"
chapter: ["8.1", "8.2", "8.3", "8.4", "8.5"]
tags: [physics, homework, solutions, gravitation]
source:
  - "Own solutions; every number recomputed with Python, symbolic results with sympy"
  - "EUP Ch. 8 (pp. 150-165), scanned PDF: equations and the Earth and Sun data used in the text"
  - "[[PHY1 Ch08 Fig 8.16.png]]"
  - "[[PHY1 Ch08 Fig 8.17.png]]"
  - "[[PHY1 Ch08 Problem 8.69 fit.png]]"
created: 2026-10-28
questions: "[[PHY1 HW Ch08 Questions]]"
up: "[[PHY1 Index]]"
format: "physics-notes 1.1"
---
> [!note] 符號與公式
> - 式號照課本：萬有引力 $F = Gm_{1}m_{2}/r^{2}$ (8.1)，**質點或球對稱物體，$r$ 從中心量起**；重力加速度 $a = GM/r^{2}$ (8.2)。
> - 圓軌道（**$M \gg m$**）：$v = \sqrt{GM/r}$ (8.3)，$T^{2} = 4\pi^{2}r^{3}/GM$ (8.4)；能量 $E = -K = \tfrac{1}{2}U = -GMm/2r$ (8.8)，**只限圓軌道**。
> - 位能 $\Delta U = GMm(1/r_{1} - 1/r_{2})$ (8.5)；$U = -GMm/r$ (8.6)，**取 $r = \infty$ 時 $U = 0$**；脫離速率 $v_{\mathrm{esc}} = \sqrt{2GM/r}$ (8.7)；力學能守恆 $K + U = K_{0} + U_{0}$ (7.6)；$F_{x} = -dU/dx$ (7.9)。
> - $r$ 一律是離中心的距離，高度 $h$ 要加上半徑：$r = R + h$。
> - 課本內文的數據：$G = 6.67 \times 10^{-11}\ \mathrm{N \cdot m^2/kg^2}$；$M_{\mathrm{E}} = 5.97 \times 10^{24}\ \mathrm{kg}$，$R_{\mathrm{E}} = 6.37 \times 10^{6}\ \mathrm{m}$，$GM_{\mathrm{E}} = 3.982 \times 10^{14}\ \mathrm{m^3/s^2}$；$M_{\mathrm{Sun}} = 1.99 \times 10^{30}\ \mathrm{kg}$，$GM_{\mathrm{Sun}} = 1.327 \times 10^{20}\ \mathrm{m^3/s^2}$。KSU 的題目用考卷給的 $R_{\mathrm{E}} = 6380\ \mathrm{km}$ 與 $g = 9.80\ \mathrm{m/s^2}$。中間值多留一位有效數字。

## 答案總表

| 題目 | 答案 |
| --- | --- |
| [[PHY1 HW Ch08 Questions#EUP 8.11\|EUP 8.11]] | $R_{\mathrm{E}}/\sqrt{3} = 3.68 \times 10^{6}\ \mathrm{m}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.15\|EUP 8.15]] | $8.6\ \mathrm{kg}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.18\|EUP 8.18]] | $1.7 \times 10^{3}\ \mathrm{km}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.20\|EUP 8.20]] | $1.87$ 年 |
| [[PHY1 HW Ch08 Questions#EUP 8.48\|EUP 8.48]] | $T_{\mathrm{A}} = 3^{3/2}T_{\mathrm{B}} = 5.2\,T_{\mathrm{B}}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.26\|EUP 8.26]] | $1.8 \times 10^{3}\ \mathrm{km}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.27\|EUP 8.27]] | $4.5\ \mathrm{km/s}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.63\|EUP 8.63]] | $3.8\ \mathrm{km/s}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.28\|EUP 8.28]] | $7.0 \times 10^{6}\ \mathrm{m}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.53\|EUP 8.53]] | 證明 |
| [[PHY1 HW Ch08 Questions#EUP 8.17\|EUP 8.17]] | $631\ \mathrm{m}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.40\|EUP 8.40]] | $2 \times 10^{-7}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.42\|EUP 8.42]] | 證明：$F_{r} = -GMm/r^{2}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.66\|EUP 8.66]] | 證明 |
| [[PHY1 HW Ch08 Questions#EUP 8.44\|EUP 8.44]] | (a) $4.6 \times 10^{6}\ \mathrm{m/s}$；(b) $8.8\ \mathrm{s}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.47\|EUP 8.47]] | $T = 2\pi\sqrt{L^{3}/3GM}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.59\|EUP 8.59]] | (a) $2.1 \times 10^{3}\ \mathrm{km}$；(b) $8.3 \times 10^{2}\ \mathrm{km}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.67\|EUP 8.67]] | $1.4 \times 10^{3}\ \mathrm{km}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.56\|EUP 8.56]] | (a) $11\ \mathrm{km/s}$；(b) $9.9\ \mathrm{km/s}$；(c) 不會 |
| [[PHY1 HW Ch08 Questions#EUP 8.58\|EUP 8.58]] | $v = \sqrt{2GM(1/R + 1/r)}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.62\|EUP 8.62]] | $7.95\ \mathrm{km/s}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.41\|EUP 8.41]] | $E = +3.6 \times 10^{10}\ \mathrm{J}$，不被束縛 |
| [[PHY1 HW Ch08 Questions#EUP 8.51\|EUP 8.51]] | 雙曲線（$v > v_{\mathrm{esc}} = 377\ \mathrm{km/s}$） |
| [[PHY1 HW Ch08 Questions#EUP 8.54\|EUP 8.54]] | $\sqrt{2}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.57\|EUP 8.57]] | 證明 |
| [[PHY1 HW Ch08 Questions#EUP 8.64\|EUP 8.64]] | (a) $8.7 \times 10^{10}\ \mathrm{m}$；(b) $0.57\ \mathrm{TJ}$；(c) $39\ \mathrm{km/s}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.72\|EUP 8.72]] | $15\ \mathrm{km}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.69\|EUP 8.69]] | $a$ 對 $1/r^{2}$ 作圖；斜率 $1.05 \times 10^{6}\ \mathrm{m^3/s^2}$；$M = 1.6 \times 10^{16}\ \mathrm{kg}$ |
| [[PHY1 HW Ch08 Questions#EUP 8.76 to 8.79\|EUP 8.76 to 8.79]] | c, d, b, d |
| [[PHY1 HW Ch08 Questions#KSUS 5.4 to 5.6\|KSUS 5.4 to 5.6]] | c；T；F |
| [[PHY1 HW Ch08 Questions#KSUF 4.6 and 4.8\|KSUF 4.6 and 4.8]] | F；T |
| [[PHY1 HW Ch08 Questions#KSUF 6.10 and 6.11\|KSUF 6.10 and 6.11]] | F；b |
| [[PHY1 HW Ch08 Questions#SIU 4.3\|SIU 4.3]] | 場是每單位質量受的力 $\vec{g}$；力是 $m\vec{g}$ |
| [[PHY1 HW Ch08 Questions#KSUS 5.7\|KSUS 5.7]] | b) $r = (GM_{\mathrm{E}}T^{2}/4\pi^{2})^{1/3}$；c) $6.70 \times 10^{4}\ \mathrm{km}$ |
| [[PHY1 HW Ch08 Questions#KSUS 5.8\|KSUS 5.8]] | $9.12\ \mathrm{km/s}$ |
| [[PHY1 HW Ch08 Questions#KSUF 4.9\|KSUF 4.9]] | a) $0.254\ \mathrm{m/s^2}$；b) 不會（$v_{\mathrm{esc}} = 367\ \mathrm{m/s}$）；第二個 b) $7.9\ \mathrm{m}$ |
| [[PHY1 HW Ch08 Questions#KSUS 6.15\|KSUS 6.15]] | $8R_{\mathrm{E}}$ |
| [[PHY1 HW Ch08 Questions#KSUF 6.12\|KSUF 6.12]] | $v_{0} = \sqrt{2/3}\,v_{\mathrm{e}}$ |

## 老師勾選：萬有引力與平方反比

### EUP 8.11
題目：[[PHY1 HW Ch08 Questions#EUP 8.11|EUP 8.11]]

> [!solution] 解
> 重量三倍即表面重力加速度三倍。質量相同，由 (8.2)：
> $$
> \frac{GM_{\mathrm{E}}}{R^{2}} = 3\,\frac{GM_{\mathrm{E}}}{R_{\mathrm{E}}^{2}} \implies R = \frac{R_{\mathrm{E}}}{\sqrt{3}} = \frac{6.37 \times 10^{6}\ \mathrm{m}}{\sqrt{3}} = 3.68 \times 10^{6}\ \mathrm{m}.
> $$

### EUP 8.15
題目：[[PHY1 HW Ch08 Questions#EUP 8.15|EUP 8.15]]

> [!solution] 解
> 球對稱，$r$ 是球心距離。由 (8.1)，$m_{1} = m_{2} = m$：
> $$
> \begin{aligned}
> F = \frac{Gm^{2}}{r^{2}} \implies m &= r\sqrt{\frac{F}{G}} \\
> &= (0.14\ \mathrm{m})\sqrt{\frac{0.25 \times 10^{-6}\ \mathrm{N}}{6.67 \times 10^{-11}\ \mathrm{N \cdot m^2/kg^2}}} = 8.6\ \mathrm{kg}.
> \end{aligned}
> $$

## 老師勾選：圓軌道的速率與週期

### EUP 8.18
題目：[[PHY1 HW Ch08 Questions#EUP 8.18|EUP 8.18]]

> [!solution] 解
> $T = 2.0\ \mathrm{h} = 7200\ \mathrm{s}$。由 (8.4)：
> $$
> r = \left(\frac{GM_{\mathrm{E}}T^{2}}{4\pi^{2}}\right)^{1/3} = \left(\frac{(3.982 \times 10^{14}\ \mathrm{m^3/s^2})(7200\ \mathrm{s})^{2}}{4\pi^{2}}\right)^{1/3} = 8.06 \times 10^{6}\ \mathrm{m}.
> $$
> 高度 $h = r - R_{\mathrm{E}} = 8.06 \times 10^{6}\ \mathrm{m} - 6.37 \times 10^{6}\ \mathrm{m} = 1.7 \times 10^{6}\ \mathrm{m} = 1.7 \times 10^{3}\ \mathrm{km}$。

### EUP 8.20
題目：[[PHY1 HW Ch08 Questions#EUP 8.20|EUP 8.20]]

> [!solution] 解
> 兩者都繞太陽，由 (8.4)，$T^{2} \propto r^{3}$；直徑比就是半徑比。地球 $T_{\mathrm{E}} = 1.00$ 年：
> $$
> T_{\mathrm{M}} = T_{\mathrm{E}}\left(\frac{r_{\mathrm{M}}}{r_{\mathrm{E}}}\right)^{3/2} = (1.00\ \text{年})(1.52)^{3/2} = 1.87\ \text{年}.
> $$

### EUP 8.48
題目：[[PHY1 HW Ch08 Questions#EUP 8.48|EUP 8.48]]

> [!solution] 解
> 由 (8.4)，同一個 $M$ 時 $T \propto r^{3/2}$：
> $$
> \frac{T_{\mathrm{A}}}{T_{\mathrm{B}}} = \left(\frac{r_{\mathrm{A}}}{r_{\mathrm{B}}}\right)^{3/2} = 3^{3/2} = 5.2.
> $$
> A 的週期是 B 的 $5.2$ 倍。

## 老師勾選：重力位能與能量守恆

### EUP 8.26
題目：[[PHY1 HW Ch08 Questions#EUP 8.26|EUP 8.26]]

> [!solution] 解
> 最高點 $K = 0$。由 (7.6) 與 (8.6)，$\tfrac{1}{2}mv_{0}^{2} - \dfrac{GM_{\mathrm{E}}m}{R_{\mathrm{E}}} = -\dfrac{GM_{\mathrm{E}}m}{r}$：
> $$
> \begin{aligned}
> r &= \left(\frac{1}{R_{\mathrm{E}}} - \frac{v_{0}^{2}}{2GM_{\mathrm{E}}}\right)^{-1} = \left(\frac{1}{6.37 \times 10^{6}\ \mathrm{m}} - \frac{(5.2 \times 10^{3}\ \mathrm{m/s})^{2}}{2(3.982 \times 10^{14}\ \mathrm{m^3/s^2})}\right)^{-1} \\
> &= 8.13 \times 10^{6}\ \mathrm{m}.
> \end{aligned}
> $$
> 最大高度 $h = r - R_{\mathrm{E}} = 1.76 \times 10^{6}\ \mathrm{m} \approx 1.8 \times 10^{3}\ \mathrm{km}$。

> [!warning] 不能用 mgh
> 用 $h = v_{0}^{2}/2g$ 會得到 $1.4 \times 10^{3}\ \mathrm{km}$：高度和地球半徑相比不小，重力已經明顯減弱。

### EUP 8.27
題目：[[PHY1 HW Ch08 Questions#EUP 8.27|EUP 8.27]]

> [!solution] 解
> 最高點 $r = R_{\mathrm{E}} + h = 7.57 \times 10^{6}\ \mathrm{m}$，$K = 0$。由 (7.6)，$\tfrac{1}{2}v_{0}^{2} - \dfrac{GM_{\mathrm{E}}}{R_{\mathrm{E}}} = -\dfrac{GM_{\mathrm{E}}}{r}$：
> $$
> \begin{aligned}
> v_{0} &= \sqrt{2GM_{\mathrm{E}}\left(\frac{1}{R_{\mathrm{E}}} - \frac{1}{r}\right)} \\
> &= \sqrt{2(3.982 \times 10^{14}\ \mathrm{m^3/s^2})\left(\frac{1}{6.37 \times 10^{6}\ \mathrm{m}} - \frac{1}{7.57 \times 10^{6}\ \mathrm{m}}\right)} \\
> &= 4.45 \times 10^{3}\ \mathrm{m/s} \approx 4.5\ \mathrm{km/s}.
> \end{aligned}
> $$

### EUP 8.63
題目：[[PHY1 HW Ch08 Questions#EUP 8.63|EUP 8.63]]

> [!solution] 解
> 最高點 $r = R_{\mathrm{E}} + 1500\ \mathrm{km} = 7.87 \times 10^{6}\ \mathrm{m}$。由 (7.6)，$\tfrac{1}{2}v^{2} - \dfrac{GM_{\mathrm{E}}}{r} = \tfrac{1}{2}v_{0}^{2} - \dfrac{GM_{\mathrm{E}}}{R_{\mathrm{E}}}$：
> $$
> \begin{aligned}
> v &= \sqrt{v_{0}^{2} - 2GM_{\mathrm{E}}\left(\frac{1}{R_{\mathrm{E}}} - \frac{1}{r}\right)} \\
> &= \sqrt{(6.2 \times 10^{3}\ \mathrm{m/s})^{2} - (7.964 \times 10^{14}\ \mathrm{m^3/s^2})(2.992 \times 10^{-8}\ \mathrm{m^{-1}})} \\
> &= 3.8 \times 10^{3}\ \mathrm{m/s} = 3.8\ \mathrm{km/s}.
> \end{aligned}
> $$

> [!warning] 最高點速率不是零
> 飛彈不是垂直發射，在最高點仍有水平速度；只有垂直發射的火箭（[[#EUP 8.26|EUP 8.26]]）在最高點才靜止。

## 老師勾選：脫離速率

### EUP 8.28
題目：[[PHY1 HW Ch08 Questions#EUP 8.28|EUP 8.28]]

> [!solution] 解
> 由 (8.7)，$v_{\mathrm{esc}}^{2} = 2GM/R$：
> $$
> R = \frac{2GM}{v_{\mathrm{esc}}^{2}} = \frac{2(6.67 \times 10^{-11}\ \mathrm{N \cdot m^2/kg^2})(2.5 \times 10^{24}\ \mathrm{kg})}{(6.9 \times 10^{3}\ \mathrm{m/s})^{2}} = 7.0 \times 10^{6}\ \mathrm{m}.
> $$

### EUP 8.53
題目：[[PHY1 HW Ch08 Questions#EUP 8.53|EUP 8.53]]

> [!solution] 解
> 從 $r_{0}$ 由靜止釋放，到地表 $R_{\mathrm{E}}$。由 (7.6) 與 (8.6)：
> $$
> \tfrac{1}{2}mv^{2} - \frac{GM_{\mathrm{E}}m}{R_{\mathrm{E}}} = 0 - \frac{GM_{\mathrm{E}}m}{r_{0}} \implies v = \sqrt{2GM_{\mathrm{E}}\left(\frac{1}{R_{\mathrm{E}}} - \frac{1}{r_{0}}\right)}.
> $$
> 非常遠時 $r_{0} \gg R_{\mathrm{E}}$，$1/r_{0}$ 可忽略：$v \approx \sqrt{2GM_{\mathrm{E}}/R_{\mathrm{E}}} = v_{\mathrm{esc}}$ (8.7)。$\blacksquare$

## 加選：萬有引力與平方反比

### EUP 8.17
題目：[[PHY1 HW Ch08 Questions#EUP 8.17|EUP 8.17]]

> [!solution] 解
> 由 (8.2)，$g(r) = GM_{\mathrm{E}}/r^{2}$，$\dfrac{dg}{dr} = -\dfrac{2GM_{\mathrm{E}}}{r^{3}} = -\dfrac{2g}{r}$。高度 $h \ll R_{\mathrm{E}}$，$\lvert\Delta g\rvert \approx 2gh/R_{\mathrm{E}}$，街面 $g = GM_{\mathrm{E}}/R_{\mathrm{E}}^{2} = 9.81\ \mathrm{m/s^2}$：
> $$
> h = \frac{R_{\mathrm{E}}\lvert\Delta g\rvert}{2g} = \frac{(6.37 \times 10^{6}\ \mathrm{m})(1.944 \times 10^{-3}\ \mathrm{m/s^2})}{2(9.81\ \mathrm{m/s^2})} = 631\ \mathrm{m}.
> $$
> （不用近似，直接解 $GM_{\mathrm{E}}/(R_{\mathrm{E}} + h)^{2} = g - \lvert\Delta g\rvert$，也是 $631\ \mathrm{m}$。）

### EUP 8.40
題目：[[PHY1 HW Ch08 Questions#EUP 8.40|EUP 8.40]]

> [!solution] 解
> 球形水槽可視為質點，$r = 10\ \mathrm{m}$。水的引力和你的重量之比，由 (8.1)：
> $$
> \frac{GM_{\mathrm{w}}m/r^{2}}{mg} = \frac{GM_{\mathrm{w}}}{r^{2}g} = \frac{(6.67 \times 10^{-11}\ \mathrm{N \cdot m^2/kg^2})(3 \times 10^{6}\ \mathrm{kg})}{(10\ \mathrm{m})^{2}(9.8\ \mathrm{m/s^2})} = 2 \times 10^{-7}.
> $$
> 重量減少約 $2 \times 10^{-7}$（千萬分之二）。

## 加選：由位能求力

### EUP 8.42
題目：[[PHY1 HW Ch08 Questions#EUP 8.42|EUP 8.42]]

> [!solution] 解
> 沿徑向 $r$ 套用 (7.9)：
> $$
> F_{r} = -\frac{dU}{dr} = -\frac{d}{dr}\left(-\frac{GMm}{r}\right) = -\frac{GMm}{r^{2}}.
> $$
> 大小 $GMm/r^{2}$ 就是 (8.1)；負號表示力指向 $r$ 減小的方向，是吸引力。$\blacksquare$

### EUP 8.66
題目：[[PHY1 HW Ch08 Questions#EUP 8.66|EUP 8.66]]

> [!solution] 解
> 令 $r_{2} = r_{1} + \Delta r$，$\Delta r \ll r_{1}$，二項式近似 $(1 + x)^{-1} \approx 1 - x$：
> $$
> \frac{1}{r_{1}} - \frac{1}{r_{1} + \Delta r} = \frac{1}{r_{1}}\left[1 - \left(1 + \frac{\Delta r}{r_{1}}\right)^{-1}\right] \approx \frac{1}{r_{1}}\cdot\frac{\Delta r}{r_{1}} = \frac{\Delta r}{r_{1}^{2}}.
> $$
> 代入 (8.5)，並由 (8.2) 令 $g = GM/r_{1}^{2}$：
> $$
> \Delta U = GMm\,\frac{\Delta r}{r_{1}^{2}} = m\,\frac{GM}{r_{1}^{2}}\,\Delta r = mg\,\Delta r. \qquad \blacksquare
> $$

## 加選：圓軌道

### EUP 8.44
題目：[[PHY1 HW Ch08 Questions#EUP 8.44|EUP 8.44]]

> [!solution] 解
> $M = M_{\mathrm{Sun}}$，表面正上方 $r \approx R_{\mathrm{E}}$。由 (8.3)：
> - (a) $v = \sqrt{\dfrac{GM_{\mathrm{Sun}}}{R_{\mathrm{E}}}} = \sqrt{\dfrac{1.327 \times 10^{20}\ \mathrm{m^3/s^2}}{6.37 \times 10^{6}\ \mathrm{m}}} = 4.6 \times 10^{6}\ \mathrm{m/s}$。
> - (b) $T = \dfrac{2\pi R_{\mathrm{E}}}{v} = \dfrac{2\pi(6.37 \times 10^{6}\ \mathrm{m})}{4.56 \times 10^{6}\ \mathrm{m/s}} = 8.8\ \mathrm{s}$。

### EUP 8.47
題目：[[PHY1 HW Ch08 Questions#EUP 8.47|EUP 8.47]]

> [!solution] 解
> 三顆星繞三角形中心轉，每顆離中心 $r_{\mathrm{c}} = L/\sqrt{3}$。另外兩顆對它各施 $GM^{2}/L^{2}$，與指向中心的方向各夾 $30^{\circ}$，合力指向中心：
> $$
> F = 2\,\frac{GM^{2}}{L^{2}}\cos 30^{\circ} = \frac{\sqrt{3}\,GM^{2}}{L^{2}}.
> $$
> 它提供向心力 $\dfrac{Mv^{2}}{r_{\mathrm{c}}} = \dfrac{4\pi^{2}Mr_{\mathrm{c}}}{T^{2}}$：
> $$
> \frac{\sqrt{3}\,GM^{2}}{L^{2}} = \frac{4\pi^{2}M}{T^{2}}\cdot\frac{L}{\sqrt{3}} \implies T^{2} = \frac{4\pi^{2}L^{3}}{3GM}, \qquad T = 2\pi\sqrt{\frac{L^{3}}{3GM}}.
> $$

> [!warning] 兩個不同的距離
> 萬有引力用星與星的距離 $L$；圓周運動的半徑是星到中心的 $L/\sqrt{3}$。

### EUP 8.59
題目：[[PHY1 HW Ch08 Questions#EUP 8.59|EUP 8.59]]

> [!solution] 解
> $r_{0} = R_{\mathrm{E}} + 5800\ \mathrm{km} = 1.217 \times 10^{7}\ \mathrm{m}$。
> - (a) 由 (8.3)，$v \propto r^{-1/2}$，$r = r_{0}/(1.10)^{2} = 1.006 \times 10^{7}\ \mathrm{m}$：降低 $r_{0} - r = 2.1 \times 10^{6}\ \mathrm{m} = 2.1 \times 10^{3}\ \mathrm{km}$。
> - (b) 由 (8.4)，$T \propto r^{3/2}$，$r = r_{0}(0.90)^{2/3} = 1.134 \times 10^{7}\ \mathrm{m}$：降低 $8.3 \times 10^{5}\ \mathrm{m} = 8.3 \times 10^{2}\ \mathrm{km}$。

### EUP 8.67
題目：[[PHY1 HW Ch08 Questions#EUP 8.67|EUP 8.67]]

![EUP Figure 8.17|360](../Attachments/PHY1%20Ch08%20Fig%208.17.png)

> [!solution] 解
> 同步軌道 $r_{0} = 4.22 \times 10^{7}\ \mathrm{m}$、週期 $T$（Example 8.3）。下降的衛星週期 $T'$，每繞一圈領先 $T - T'$；10 圈要追上半圈 $T/2$：
> $$
> 10(T - T') = \tfrac{1}{2}T \implies T' = 0.95\,T.
> $$
> 由 (8.4)，$r \propto T^{2/3}$：
> $$
> \begin{aligned}
> r &= r_{0}(0.95)^{2/3} = (4.22 \times 10^{7}\ \mathrm{m})(0.9664) = 4.08 \times 10^{7}\ \mathrm{m}, \\
> r_{0} - r &= 1.4 \times 10^{6}\ \mathrm{m} = 1.4 \times 10^{3}\ \mathrm{km}.
> \end{aligned}
> $$

> [!warning] 「10 圈」是誰的圈
> 這裡取下降衛星自己繞 10 圈；若改成同步衛星的 10 圈，$T' = T/1.05$，下降 $1.35 \times 10^{3}\ \mathrm{km}$，到兩位有效數字仍是 $1.4 \times 10^{3}\ \mathrm{km}$。

## 加選：能量守恆與軌道

### EUP 8.56
題目：[[PHY1 HW Ch08 Questions#EUP 8.56|EUP 8.56]]

![EUP Figure 8.16|360](../Attachments/PHY1%20Ch08%20Fig%208.16.png)

> [!solution] 解
> $r_{0} = 2.50 \times 10^{8}\ \mathrm{m}$，$v_{0} = 2.9 \times 10^{3}\ \mathrm{m/s}$。由 (7.6) 與 (8.6)，$v = \sqrt{v_{0}^{2} + 2GM_{\mathrm{E}}(1/r - 1/r_{0})}$：
> - (a) $r = R_{\mathrm{E}}$：$v = \sqrt{8.41 \times 10^{6}\ \mathrm{m^2/s^2} + 1.218 \times 10^{8}\ \mathrm{m^2/s^2}} = 1.1 \times 10^{4}\ \mathrm{m/s} = 11\ \mathrm{km/s}$。
> - (b) $r = 8.5 \times 10^{6}\ \mathrm{m}$：$v = \sqrt{8.41 \times 10^{6}\ \mathrm{m^2/s^2} + 9.05 \times 10^{7}\ \mathrm{m^2/s^2}} = 9.9\ \mathrm{km/s}$。
> - (c) 每單位質量的總能量
> $$
> \begin{aligned}
> \frac{E}{m} &= \tfrac{1}{2}v_{0}^{2} - \frac{GM_{\mathrm{E}}}{r_{0}} = 4.21 \times 10^{6}\ \mathrm{J/kg} - 1.59 \times 10^{6}\ \mathrm{J/kg} \\
> &= +2.6 \times 10^{6}\ \mathrm{J/kg} > 0,
> \end{aligned}
> $$
> 開放的雙曲線軌道：不會回來。

### EUP 8.58
題目：[[PHY1 HW Ch08 Questions#EUP 8.58|EUP 8.58]]

> [!solution] 解
> $v_{0} = \sqrt{2}\,v_{\mathrm{esc}}$，由 (8.7)，$v_{0}^{2} = 2 \cdot \dfrac{2GM}{R} = \dfrac{4GM}{R}$。由 (7.6) 與 (8.6)：
> $$
> \tfrac{1}{2}v^{2} - \frac{GM}{r} = \tfrac{1}{2}v_{0}^{2} - \frac{GM}{R} = \frac{GM}{R} \implies v = \sqrt{2GM\left(\frac{1}{R} + \frac{1}{r}\right)}.
> $$
> （$r \to \infty$ 時 $v \to \sqrt{2GM/R}$，即表面的脫離速率。）

### EUP 8.62
題目：[[PHY1 HW Ch08 Questions#EUP 8.62|EUP 8.62]]

> [!solution] 解
> $r_{\mathrm{h}} = R_{\mathrm{E}} + 890\ \mathrm{km} = 7.26 \times 10^{6}\ \mathrm{m}$，$r_{\mathrm{l}} = R_{\mathrm{E}} + 230\ \mathrm{km} = 6.60 \times 10^{6}\ \mathrm{m}$。由 (7.6)：
> $$
> \begin{aligned}
> v_{\mathrm{l}} &= \sqrt{v_{\mathrm{h}}^{2} + 2GM_{\mathrm{E}}\left(\frac{1}{r_{\mathrm{l}}} - \frac{1}{r_{\mathrm{h}}}\right)} \\
> &= \sqrt{(7.23 \times 10^{3}\ \mathrm{m/s})^{2} + (7.964 \times 10^{14}\ \mathrm{m^3/s^2})(1.377 \times 10^{-8}\ \mathrm{m^{-1}})} \\
> &= 7.95\ \mathrm{km/s}.
> \end{aligned}
> $$

> [!warning] 橢圓軌道不能用 (8.3)
> $v = \sqrt{GM/r}$ 只對圓軌道成立；橢圓軌道上要用能量守恆連結兩點。

## 加選：總能量、束縛與脫離

### EUP 8.41
題目：[[PHY1 HW Ch08 Questions#EUP 8.41|EUP 8.41]]

> [!solution] 解
> $v = 51{,}000\ \mathrm{km/h} = 1.417 \times 10^{4}\ \mathrm{m/s}$，$r = 6.5 \times 10^{12}\ \mathrm{m}$。由 (8.6)：
> $$
> \begin{aligned}
> E &= \tfrac{1}{2}mv^{2} - \frac{GM_{\mathrm{Sun}}m}{r} \\
> &= \tfrac{1}{2}(450\ \mathrm{kg})(1.417 \times 10^{4}\ \mathrm{m/s})^{2} - \frac{(1.327 \times 10^{20}\ \mathrm{m^3/s^2})(450\ \mathrm{kg})}{6.5 \times 10^{12}\ \mathrm{m}} \\
> &= 4.52 \times 10^{10}\ \mathrm{J} - 0.92 \times 10^{10}\ \mathrm{J} = +3.6 \times 10^{10}\ \mathrm{J}.
> \end{aligned}
> $$
> $E > 0$：不被太陽束縛，會永遠離開太陽系。

### EUP 8.51
題目：[[PHY1 HW Ch08 Questions#EUP 8.51|EUP 8.51]]

> [!solution] 解
> 比較近日點的速率和該處相對太陽的脫離速率 (8.7)：
> $$
> \begin{aligned}
> v_{\mathrm{esc}} &= \sqrt{\frac{2GM_{\mathrm{Sun}}}{r}} = \sqrt{\frac{2(1.327 \times 10^{20}\ \mathrm{m^3/s^2})}{1.87 \times 10^{9}\ \mathrm{m}}} \\
> &= 3.77 \times 10^{5}\ \mathrm{m/s} = 377\ \mathrm{km/s}.
> \end{aligned}
> $$
> $378\ \mathrm{km/s} > 377\ \mathrm{km/s}$，總能量 $E > 0$：雙曲線軌道。

> [!warning] 差距只有 0.3%
> 結論只差 $1\ \mathrm{km/s}$，對 $G$、$M_{\mathrm{Sun}}$ 的有效位數很敏感；用課本的三位有效數字得到的是雙曲線。

### EUP 8.54
題目：[[PHY1 HW Ch08 Questions#EUP 8.54|EUP 8.54]]

> [!solution] 解
> 由 (8.3) 與 (8.7)，同一個 $r$：
> $$
> \frac{v_{\mathrm{esc}}}{v} = \frac{\sqrt{2GM/r}}{\sqrt{GM/r}} = \sqrt{2} = 1.41.
> $$

### EUP 8.57
題目：[[PHY1 HW Ch08 Questions#EUP 8.57|EUP 8.57]]

> [!solution] 解
> 不計自轉，衛星在地表靜止：$E_{0} = -GM_{\mathrm{E}}m/R_{\mathrm{E}}$ (8.6)。在 $r = R_{\mathrm{E}} + h$ 的圓軌道上，由 (8.8b)，$E = -\dfrac{GM_{\mathrm{E}}m}{2(R_{\mathrm{E}} + h)}$。所需能量
> $$
> \begin{aligned}
> E - E_{0} &= \frac{GM_{\mathrm{E}}m}{R_{\mathrm{E}}} - \frac{GM_{\mathrm{E}}m}{2(R_{\mathrm{E}} + h)} = \frac{GM_{\mathrm{E}}m}{R_{\mathrm{E}}}\cdot\frac{2(R_{\mathrm{E}} + h) - R_{\mathrm{E}}}{2(R_{\mathrm{E}} + h)} \\
> &= \left(\frac{GM_{\mathrm{E}}m}{R_{\mathrm{E}}}\right)\left(\frac{R_{\mathrm{E}} + 2h}{2(R_{\mathrm{E}} + h)}\right). \qquad \blacksquare
> \end{aligned}
> $$

### EUP 8.64
題目：[[PHY1 HW Ch08 Questions#EUP 8.64|EUP 8.64]]

> [!solution] 解
> 圓軌道，用 (8.8)：
> - (a) $E = -\dfrac{GM_{\mathrm{Sun}}m}{2r}$：$r = -\dfrac{GM_{\mathrm{Sun}}m}{2E} = \dfrac{(1.327 \times 10^{20}\ \mathrm{m^3/s^2})(750\ \mathrm{kg})}{2(0.57 \times 10^{12}\ \mathrm{J})} = 8.7 \times 10^{10}\ \mathrm{m}$（約 $0.58$ 倍地日距離）。
> - (b) $K = -E = 0.57\ \mathrm{TJ}$。
> - (c) $v = \sqrt{\dfrac{2K}{m}} = \sqrt{\dfrac{2(0.57 \times 10^{12}\ \mathrm{J})}{750\ \mathrm{kg}}} = 3.9 \times 10^{4}\ \mathrm{m/s} = 39\ \mathrm{km/s}$。

### EUP 8.72
題目：[[PHY1 HW Ch08 Questions#EUP 8.72|EUP 8.72]]

> [!solution] 解
> 假設起跳速率和在地球上一樣：$v_{0}^{2} = 2gh_{\mathrm{E}}$，$h_{\mathrm{E}} = 2.8\ \mathrm{m}$。小行星 $M = \tfrac{4}{3}\pi R^{3}\rho$，由 (8.7)，$v_{\mathrm{esc}}^{2} = \dfrac{2GM}{R} = \tfrac{8}{3}\pi G\rho R^{2}$。要落回，$v_{0} < v_{\mathrm{esc}}$，即 $\tfrac{8}{3}\pi G\rho R^{2} > 2gh_{\mathrm{E}}$：
> $$
> \begin{aligned}
> R &> \sqrt{\frac{3gh_{\mathrm{E}}}{4\pi G\rho}} \\
> &= \sqrt{\frac{3(9.8\ \mathrm{m/s^2})(2.8\ \mathrm{m})}{4\pi(6.67 \times 10^{-11}\ \mathrm{N \cdot m^2/kg^2})(1700\ \mathrm{kg/m^3})}} = 7.6 \times 10^{3}\ \mathrm{m}.
> \end{aligned}
> $$
> 最小直徑 $2R = 15\ \mathrm{km}$。

## 加選：數據題

### EUP 8.69
題目：[[PHY1 HW Ch08 Questions#EUP 8.69|EUP 8.69]]

> [!solution] 解
> 由 (8.2)，$a = GM/r^{2}$：$a$ 對 $1/r^{2}$ 作圖是通過原點的直線，斜率 $GM$。換成 SI：
>
> | $1/r^{2}$ ($10^{-10}\ \mathrm{m^{-2}}$) | $1.563$ | $3.306$ | $6.250$ | $8.163$ | $11.11$ |
> | --- | --- | --- | --- | --- | --- |
> | $a$ ($10^{-3}\ \mathrm{m/s^2}$) | $0.172$ | $0.353$ | $0.704$ | $0.858$ | $1.18$ |
>
> 最小平方擬合：斜率 $1.05 \times 10^{6}\ \mathrm{m^3/s^2}$，截距 $1.3 \times 10^{-5}\ \mathrm{m/s^2}$（約為零）。
> $$
> M = \frac{\text{斜率}}{G} = \frac{1.05 \times 10^{6}\ \mathrm{m^3/s^2}}{6.67 \times 10^{-11}\ \mathrm{N \cdot m^2/kg^2}} = 1.6 \times 10^{16}\ \mathrm{kg}.
> $$
>
> ![EUP 8.69 fit|480](../Attachments/PHY1%20Ch08%20Problem%208.69%20fit.png)

## 加選：GPS 衛星

### EUP 8.76 to 8.79
題目：[[PHY1 HW Ch08 Questions#EUP 8.76 to 8.79|EUP 8.76 to 8.79]]

> [!solution] 解
> $r = R_{\mathrm{E}} + 20{,}200\ \mathrm{km} = 2.657 \times 10^{7}\ \mathrm{m}$。
> - **76.** c. 由 (8.4)，$T = 2\pi\sqrt{r^{3}/GM_{\mathrm{E}}} = 4.31 \times 10^{4}\ \mathrm{s} = 12.0\ \mathrm{h}$。
> - **77.** d. 由 (8.3)，$v = \sqrt{GM_{\mathrm{E}}/r} = 3.87\ \mathrm{km/s}$。
> - **78.** b. 由 (8.7)，$v_{\mathrm{esc}} = \sqrt{2}\,v = 5.47\ \mathrm{km/s}$。
> - **79.** d. 由 (8.8b)，$E = -\dfrac{GM_{\mathrm{E}}m}{2r} = -\dfrac{(3.982 \times 10^{14}\ \mathrm{m^3/s^2})(844\ \mathrm{kg})}{2(2.657 \times 10^{7}\ \mathrm{m})} = -6.3\ \mathrm{GJ}$。

## 外校考題：觀念題

### KSUS 5.4 to 5.6
題目：[[PHY1 HW Ch08 Questions#KSUS 5.4 to 5.6|KSUS 5.4 to 5.6]]

> [!solution] 解
> - **4.** c. 高度 $2R_{\mathrm{E}}$ 是離地心 $3R_{\mathrm{E}}$；由 (8.2)，$g \propto 1/r^{2}$，變成 $1/3^{2} = 1/9$。
> - **5.** T. 軌道上唯一的力是指向地心的重力，加速度與它同向。
> - **6.** F. 地球同步衛星的週期是 24 小時，和地球自轉相同。

> [!warning] 高度不是離地心的距離
> 第 4 題的 $2R_{\mathrm{E}}$ 是高度，要加上地球半徑；選 b 就是把它當成離地心的距離。

### KSUF 4.6 and 4.8
題目：[[PHY1 HW Ch08 Questions#KSUF 4.6 and 4.8|KSUF 4.6 and 4.8]]

> [!solution] 解
> - **6.** F. 由 (8.2)，$g = GM/R^{2}$，質量不變、$R$ 加倍，$g$ 變成 $1/4$。
> - **8.** T. 圓軌道上 $GMm/r^{2} = mv^{2}/r$，所以 $v^{2}/r = GM/r^{2} = g(r)$。

### KSUF 6.10 and 6.11
題目：[[PHY1 HW Ch08 Questions#KSUF 6.10 and 6.11|KSUF 6.10 and 6.11]]

> [!solution] 解
> - **10.** F. 由 (8.3)，$v = \sqrt{GM/r} \propto 1/\sqrt{r}$，與半徑的平方根成反比。
> - **11.** b. 由 (8.2)，$g \propto M/R^{2}$：$2/2^{2} = 1/2$。

### SIU 4.3
題目：[[PHY1 HW Ch08 Questions#SIU 4.3|SIU 4.3]]

> [!solution] 解
> 重力場 $\vec{g}$ 是空間中每一點「每單位質量會受的力」，由產生重力的質量決定（球形質量 $M$：$\vec{g} = -(GM/r^{2})\hat{r}$ (8.10)），不論那裡有沒有放物體都存在，單位 $\mathrm{N/kg}$。重力是放在那一點的質量 $m$ 實際受的力 $\vec{F} = m\vec{g}$，單位 $\mathrm{N}$，與 $m$ 成正比。

## 外校考題：計算題

### KSUS 5.7
題目：[[PHY1 HW Ch08 Questions#KSUS 5.7|KSUS 5.7]]

> [!solution] 解
> **a)** 重力提供向心力，$v = 2\pi r/T$：
> $$
> \frac{GM_{\mathrm{E}}m}{r^{2}} = \frac{mv^{2}}{r} = \frac{4\pi^{2}mr}{T^{2}}.
> $$
> **b)** $r = \left(\dfrac{GM_{\mathrm{E}}T^{2}}{4\pi^{2}}\right)^{1/3}$（$m$ 消去）。
>
> **c)** $T = 48.0\ \mathrm{h} = 1.728 \times 10^{5}\ \mathrm{s}$：
> $$
> \begin{aligned}
> r &= \left(\frac{(6.67 \times 10^{-11}\ \mathrm{N \cdot m^2/kg^2})(5.97 \times 10^{24}\ \mathrm{kg})(1.728 \times 10^{5}\ \mathrm{s})^{2}}{4\pi^{2}}\right)^{1/3} \\
> &= 6.70 \times 10^{7}\ \mathrm{m} = 6.70 \times 10^{4}\ \mathrm{km}.
> \end{aligned}
> $$

### KSUS 5.8
題目：[[PHY1 HW Ch08 Questions#KSUS 5.8|KSUS 5.8]]

> [!solution] 解
> 高度 $2R_{\mathrm{E}}$ 即 $r_{0} = 3R_{\mathrm{E}}$，由靜止釋放。由 (7.6) 與 (8.6)：
> $$
> \tfrac{1}{2}mv^{2} = GM_{\mathrm{E}}m\left(\frac{1}{R_{\mathrm{E}}} - \frac{1}{3R_{\mathrm{E}}}\right) = \frac{2GM_{\mathrm{E}}m}{3R_{\mathrm{E}}}
> $$
> $$
> \begin{aligned}
> v &= \sqrt{\frac{4GM_{\mathrm{E}}}{3R_{\mathrm{E}}}} = \sqrt{\frac{4(6.67 \times 10^{-11}\ \mathrm{N \cdot m^2/kg^2})(5.97 \times 10^{24}\ \mathrm{kg})}{3(6.38 \times 10^{6}\ \mathrm{m})}} \\
> &= 9.12 \times 10^{3}\ \mathrm{m/s} = 9.12\ \mathrm{km/s}.
> \end{aligned}
> $$

### KSUF 4.9
題目：[[PHY1 HW Ch08 Questions#KSUF 4.9|KSUF 4.9]]

> [!solution] 解
> **a)** 由 (8.2)：
> $$
> g = \frac{GM}{R^{2}} = \frac{(6.67 \times 10^{-11}\ \mathrm{N \cdot m^2/kg^2})(2.67 \times 10^{20}\ \mathrm{kg})}{(2.65 \times 10^{5}\ \mathrm{m})^{2}} = 0.254\ \mathrm{m/s^2}.
> $$
> **b)** 由 (8.7)，$v_{\mathrm{esc}} = \sqrt{2GM/R} = \sqrt{2(0.254\ \mathrm{m/s^2})(2.65 \times 10^{5}\ \mathrm{m})} = 367\ \mathrm{m/s}$。$10\ \mathrm{m/s}$ 遠小於它（也遠小於貼地圓軌道速率 $\sqrt{GM/R} = 259\ \mathrm{m/s}$）：不會跑離小行星。
>
> **b)（第二個）** $h \ll R$，$g$ 視為常數：
> $$
> h = \frac{v_{0}^{2}}{2g} = \frac{(2.0\ \mathrm{m/s})^{2}}{2(0.254\ \mathrm{m/s^2})} = 7.9\ \mathrm{m}.
> $$

### KSUS 6.15
題目：[[PHY1 HW Ch08 Questions#KSUS 6.15|KSUS 6.15]]

> [!solution] 解
> $v_{0}^{2} = \tfrac{8}{9}v_{\mathrm{e}}^{2} = \tfrac{16}{9}\dfrac{GM_{\mathrm{E}}}{R_{\mathrm{E}}}$。最高點 $K = 0$，由 (7.6) 與 (8.6)：
> $$
> \tfrac{1}{2}v_{0}^{2} - \frac{GM_{\mathrm{E}}}{R_{\mathrm{E}}} = -\frac{GM_{\mathrm{E}}}{r} \implies \frac{8}{9}\frac{GM_{\mathrm{E}}}{R_{\mathrm{E}}} - \frac{GM_{\mathrm{E}}}{R_{\mathrm{E}}} = -\frac{GM_{\mathrm{E}}}{r} \implies r = 9R_{\mathrm{E}}.
> $$
> 最大高度 $h = r - R_{\mathrm{E}} = 8R_{\mathrm{E}}$。

> [!warning] 高度從地表量
> $9R_{\mathrm{E}}$ 是離地心的距離，題目問的高度是 $8R_{\mathrm{E}}$。

### KSUF 6.12
題目：[[PHY1 HW Ch08 Questions#KSUF 6.12|KSUF 6.12]]

> [!solution] 解
> 最大高度 $2R_{\mathrm{E}}$，離地心 $r = 3R_{\mathrm{E}}$，那裡 $K = 0$。由 (7.6) 與 (8.6)：
> $$
> \tfrac{1}{2}mv_{0}^{2} = GMm\left(\frac{1}{R_{\mathrm{E}}} - \frac{1}{3R_{\mathrm{E}}}\right) = \frac{2}{3}\cdot\frac{GMm}{R_{\mathrm{E}}} \implies v_{0}^{2} = \frac{2}{3}\cdot\frac{2GM}{R_{\mathrm{E}}} = \frac{2}{3}v_{\mathrm{e}}^{2}.
> $$
> $v_{0} = \sqrt{2/3}\,v_{\mathrm{e}} = 0.816\,v_{\mathrm{e}}$。
