---
course: [PHY1]
semester: "115-1"
chapter: ["5.1", "5.2", "5.3", "5.4", "5.5"]
tags: [physics, homework, solutions, dynamics]
source:
  - "Own solutions; every number recomputed with Python, symbolic results with sympy"
  - "EUP Ch. 5 (pp. 90-109), scanned PDF: equations, worked examples and answers to GOT IT? questions"
  - "[[PHY1 Ch05 Fig 5.31.png]]"
  - "[[PHY1 Ch05 Fig 5.32.png]]"
  - "[[PHY1 Ch05 Fig 5.33.png]]"
  - "[[PHY1 Ch05 Fig 5.34.png]]"
  - "[[PHY1 Ch05 Fig 5.35.png]]"
  - "[[PHY1 Ch05 Fig 5.37.png]]"
  - "[[PHY1 Ch05 Fig 5.38.png]]"
  - "[[PHY1 Ch05 Problem 5.76 fit.png]]"
created: 2026-10-28
questions: "[[PHY1 HW Ch05 Questions]]"
up: "[[PHY1 Index]]"
format: "physics-notes 1.1"
---
> [!note] 符號與公式
> - 式號照課本：等速圓周運動 $F_{\mathrm{net}} = mv^{2}/r$ (5.1)，**淨力指向圓心**；靜摩擦 $f_{\mathrm{s}} \le \mu_{\mathrm{s}}n$ (5.2)，**只有即將滑動時取等號**；動摩擦 $f_{\mathrm{k}} = \mu_{\mathrm{k}}n$ (5.3)，**表面相對滑動時**。
> - 等加速度 $x = x_{0} + v_{0}t + \tfrac{1}{2}at^{2}$ (2.10)、$v^{2} = v_{0}^{2} + 2a\,\Delta x$ (2.11)，**只在加速度不變時**。
> - 斜面題 $x$ 沿斜面、$y$ 垂直斜面；圓周運動 $+x$ 指向圓心；其他用水平／鉛直座標、向上為正，另有規定時以粗體註明。
> - $g = 9.8\ \mathrm{m/s^2}$；KSU 的題目用 $9.80\ \mathrm{m/s^2}$。中間值多留一位有效數字。

## 答案總表

| 題目 | 答案 |
| --- | --- |
| [[PHY1 HW Ch05 Questions#EUP 5.12\|EUP 5.12]] | $3.7\hat{\imath} + 1.1\hat{\jmath}\ \mathrm{N}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.42\|EUP 5.42]] | 左繩（$71^{\circ}$）$2.3 \times 10^{2}\ \mathrm{N}$；右繩（$28^{\circ}$）$84\ \mathrm{N}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.14\|EUP 5.14]] | $27\ \mathrm{s}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.18\|EUP 5.18]] | (a) $6.0\ \mathrm{kg}$；(b) $3.6\ \mathrm{kg}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.21\|EUP 5.21]] | 證明 |
| [[PHY1 HW Ch05 Questions#EUP 5.43\|EUP 5.43]] | (a) $m_{2}g$；(b) $2\pi\sqrt{m_{1}R/(m_{2}g)}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.62\|EUP 5.62]] | $\sqrt{gL/(2\sqrt{3})} \approx 0.54\sqrt{gL}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.25\|EUP 5.25]] | $1.3 \times 10^{2}\ \mathrm{m/s}$（約 $450\ \mathrm{km/h}$） |
| [[PHY1 HW Ch05 Questions#EUP 5.47\|EUP 5.47]] | $1.0 \times 10^{4}\ \mathrm{m}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.27\|EUP 5.27]] | $0.10$ |
| [[PHY1 HW Ch05 Questions#EUP 5.53\|EUP 5.53]] | 來得及：$133\ \mathrm{m}$ 內停下，剩約 $17\ \mathrm{m}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.44\|EUP 5.44]] | $58\ \mathrm{N}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.75\|EUP 5.75]] | 行得通：最大張力 $89\ \mathrm{N}$（另兩條 $57\ \mathrm{N}$、$34\ \mathrm{N}$） |
| [[PHY1 HW Ch05 Questions#EUP 5.19\|EUP 5.19]] | (a) $3.8\ \mathrm{m/s^2}$；(b) $5.5 \times 10^{2}\ \mathrm{N}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.51\|EUP 5.51]] | $0.26\ \mathrm{m/s^2}$；$20\ \mathrm{s}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.50\|EUP 5.50]] | $4.4 \times 10^{2}\ \mathrm{N}$，約重量的 $1.7$ 倍 |
| [[PHY1 HW Ch05 Questions#EUP 5.57\|EUP 5.57]] | $4.2\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.60\|EUP 5.60]] | 證明（$\mu_{\mathrm{s}} \ge \cot 50^{\circ} = 0.84$） |
| [[PHY1 HW Ch05 Questions#EUP 5.61\|EUP 5.61]] | (a) $9.8\ \mathrm{cm}$；(b) 不會 |
| [[PHY1 HW Ch05 Questions#EUP 5.70\|EUP 5.70]] | 證明 |
| [[PHY1 HW Ch05 Questions#EUP 5.55\|EUP 5.55]] | $0.23 \le \mu_{\mathrm{s}} < 0.30$ |
| [[PHY1 HW Ch05 Questions#EUP 5.23\|EUP 5.23]] | $71\ \mathrm{km/h}$，超速 |
| [[PHY1 HW Ch05 Questions#EUP 5.45\|EUP 5.45]] | (a) $2.0 \times 10^{2}\ \mathrm{N}$ 向下；(b) $0$；(c) 不會怎樣，乘客仍壓在座椅上 |
| [[PHY1 HW Ch05 Questions#EUP 5.67\|EUP 5.67]] | $16\ \mathrm{rev/min}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.63\|EUP 5.63]] | 可能；最快 $110\ \mathrm{km/h}$，超速約 $34\ \mathrm{km/h}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.72\|EUP 5.72]] | $0.28$ |
| [[PHY1 HW Ch05 Questions#EUP 5.69\|EUP 5.69]] | 煞車：所需距離只有轉向的一半 |
| [[PHY1 HW Ch05 Questions#EUP 5.73\|EUP 5.73]] | $v = \dfrac{mg}{b}\left(1 - e^{-bt/m}\right)$ |
| [[PHY1 HW Ch05 Questions#EUP 5.76\|EUP 5.76]] | $a$ 對 $m_{1}/(m_{1} + m_{2})$ 作圖；$g = 9.8\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch05 Questions#EUP 5.77 to 5.80\|EUP 5.77 to 5.80]] | a, a, b, c |
| [[PHY1 HW Ch05 Questions#KSUF 2.1 and 2.2\|KSUF 2.1 and 2.2]] | e, b |
| [[PHY1 HW Ch05 Questions#KSUF 2.13 to 2.17\|KSUF 2.13 to 2.17]] | F, F, F, T, T |
| [[PHY1 HW Ch05 Questions#KSUS 2.6 and 2.7\|KSUS 2.6 and 2.7]] | F, T |
| [[PHY1 HW Ch05 Questions#KSUS 2.15 and 2.16\|KSUS 2.15 and 2.16]] | F, F |
| [[PHY1 HW Ch05 Questions#SIU 22.2\|SIU 22.2]] | 向前，與速度同方向 |
| [[PHY1 HW Ch05 Questions#SIU 23.3 and 23.4\|SIU 23.3 and 23.4]] | 都做不到 |
| [[PHY1 HW Ch05 Questions#KSUF 2.11\|KSUF 2.11]] | $6.11\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch05 Questions#KSUF 2.12\|KSUF 2.12]] | a) $21.2\ \mathrm{m/s}$；b) $27.2\ \mathrm{s}$ |
| [[PHY1 HW Ch05 Questions#KSUF 2.18\|KSUF 2.18]] | a) $35.9\ \mathrm{m/s}$；b) $3.46 \times 10^{3}\ \mathrm{N}$ |
| [[PHY1 HW Ch05 Questions#KSUS 2.18\|KSUS 2.18]] | a) $0.16$；b) $9.1^{\circ}$ |
| [[PHY1 HW Ch05 Questions#KSUS 2.19\|KSUS 2.19]] | a) 鋼索張力的水平分量；b) $1.9 \times 10^{2}\ \mathrm{N}$；c) $14^{\circ}$ |
| [[PHY1 HW Ch05 Questions#SIU 22.7\|SIU 22.7]] | $3.0\ \mathrm{ms}$ |
| [[PHY1 HW Ch05 Questions#SIU 23.7\|SIU 23.7]] | $83\ \mathrm{m}$ |

## 老師勾選：二維的力與靜力平衡

### EUP 5.12
題目：[[PHY1 HW Ch05 Questions#EUP 5.12|EUP 5.12]]

> [!solution] 解
> $\vec{F}_{1} + \vec{F}_{2} = m\vec{a}$：
> $$
> \begin{aligned}
> \vec{F}_{2} = m\vec{a} - \vec{F}_{1} &= (3.1\ \mathrm{kg})(0.95\hat{\imath} - 0.32\hat{\jmath})\ \mathrm{m/s^2} - (-0.80\hat{\imath} - 2.1\hat{\jmath})\ \mathrm{N} \\
> &= (2.95\hat{\imath} - 0.99\hat{\jmath})\ \mathrm{N} + (0.80\hat{\imath} + 2.1\hat{\jmath})\ \mathrm{N} = 3.7\hat{\imath} + 1.1\hat{\jmath}\ \mathrm{N}.
> \end{aligned}
> $$

### EUP 5.42
題目：[[PHY1 HW Ch05 Questions#EUP 5.42|EUP 5.42]]

![EUP Figure 5.32|400](../Attachments/PHY1%20Ch05%20Fig%205.32.png)

> [!solution] 解
> 左繩張力 $T_{1}$ 與水平成 $71^{\circ}$，右繩 $T_{2}$ 成 $28^{\circ}$，背包靜止：
> $$
> x:\ T_{2}\cos 28^{\circ} - T_{1}\cos 71^{\circ} = 0, \qquad y:\ T_{1}\sin 71^{\circ} + T_{2}\sin 28^{\circ} - mg = 0
> $$
> 由 $x$ 式 $T_{2} = T_{1}\cos 71^{\circ}/\cos 28^{\circ}$，代入 $y$ 式，$T_{1}\sin(71^{\circ} + 28^{\circ})/\cos 28^{\circ} = mg$：
> $$
> \begin{aligned}
> T_{1} &= \frac{mg\cos 28^{\circ}}{\sin 99^{\circ}} = \frac{(26\ \mathrm{kg})(9.8\ \mathrm{m/s^2})\cos 28^{\circ}}{\sin 99^{\circ}} = 2.3 \times 10^{2}\ \mathrm{N}, \\
> T_{2} &= \frac{mg\cos 71^{\circ}}{\sin 99^{\circ}} = 84\ \mathrm{N}.
> \end{aligned}
> $$

> [!warning] 不對稱
> 兩繩角度不同，張力不相等，不能套 Example 5.2 的 $T = mg/(2\sin\theta)$；較陡的繩承受較大的張力。

## 老師勾選：斜面與相連物體

### EUP 5.14
題目：[[PHY1 HW Ch05 Questions#EUP 5.14|EUP 5.14]]

> [!solution] 解
> $x$ 沿坡往下，同 Example 5.1，$a = g\sin\theta$。由靜止出發，由 (2.10)，$L = \tfrac{1}{2}at^{2}$：
> $$
> t = \sqrt{\frac{2L}{g\sin\theta}} = \sqrt{\frac{2(1.5 \times 10^{3}\ \mathrm{m})}{(9.8\ \mathrm{m/s^2})\sin 24^{\circ}}} = 27\ \mathrm{s}.
> $$

### EUP 5.18
題目：[[PHY1 HW Ch05 Questions#EUP 5.18|EUP 5.18]]

![EUP Figure 5.31|400](../Attachments/PHY1%20Ch05%20Fig%205.31.png)

> [!solution] 解
> 左邊 $m_{1}$ 在 $52^{\circ}$ 面、右邊 $m_{2}$ 在 $25^{\circ}$ 面，無摩擦。取 **$m_{2}$ 沿坡往下**（$m_{1}$ 沿坡往上）為正，兩者加速度大小相同、繩中張力 $T$ 相同：
> $$
> m_{2}:\ m_{2}g\sin 25^{\circ} - T = m_{2}a, \qquad m_{1}:\ T - m_{1}g\sin 52^{\circ} = m_{1}a
> $$
> 相加消去 $T$：
> $$
> m_{2} = m_{1}\frac{g\sin 52^{\circ} + a}{g\sin 25^{\circ} - a}, \qquad g\sin 52^{\circ} = 7.72\ \mathrm{m/s^2}, \quad g\sin 25^{\circ} = 4.14\ \mathrm{m/s^2}.
> $$
> - (a) $a = +0.64\ \mathrm{m/s^2}$：$m_{2} = (2.5\ \mathrm{kg})\dfrac{7.72 + 0.64}{4.14 - 0.64} = 6.0\ \mathrm{kg}$。
> - (b) $a = -0.76\ \mathrm{m/s^2}$：$m_{2} = (2.5\ \mathrm{kg})\dfrac{7.72 - 0.76}{4.14 + 0.76} = 3.6\ \mathrm{kg}$。

> [!warning] 自行假設
> 題目沒說有沒有摩擦，也沒標哪個角在哪邊；這裡取無摩擦，並依圖取較陡的左面為 $52^{\circ}$。

## 老師勾選：圓周運動

### EUP 5.21
題目：[[PHY1 HW Ch05 Questions#EUP 5.21|EUP 5.21]]

> [!solution] 解
> 一個週期走一圈，$v = 2\pi r/T$。由 (5.1)，
> $$
> F = \frac{mv^{2}}{r} = \frac{m}{r}\left(\frac{2\pi r}{T}\right)^{2} = \frac{4\pi^{2}mr}{T^{2}}. \qquad \blacksquare
> $$

### EUP 5.43
題目：[[PHY1 HW Ch05 Questions#EUP 5.43|EUP 5.43]]

![EUP Figure 5.33|300](../Attachments/PHY1%20Ch05%20Fig%205.33.png)

> [!solution] 解
> 週期記為 $P$，避免和張力 $T$ 混淆。
> - (a) $m_{2}$ 靜止，$T - m_{2}g = 0$：$T = m_{2}g$。
> - (b) 張力是 $m_{1}$ 受的唯一水平力，由 (5.1) 與 $v = 2\pi R/P$：
> $$
> m_{2}g = \frac{m_{1}v^{2}}{R} = \frac{4\pi^{2}m_{1}R}{P^{2}} \implies P = 2\pi\sqrt{\frac{m_{1}R}{m_{2}g}}.
> $$

### EUP 5.62
題目：[[PHY1 HW Ch05 Questions#EUP 5.62|EUP 5.62]]

> [!solution] 解
> 繩與**鉛直**夾 $\theta = \pi/6$，半徑 $r = L\sin\theta = L/2$。$+x$ 指向圓心：
> $$
> x:\ T\sin\theta = \frac{mv^{2}}{r}, \qquad y:\ T\cos\theta - mg = 0 \implies \tan\theta = \frac{v^{2}}{gr}.
> $$
> $$
> v = \sqrt{gr\tan\theta} = \sqrt{\frac{gL}{2} \cdot \frac{1}{\sqrt{3}}} = \sqrt{\frac{gL}{2\sqrt{3}}} \approx 0.54\sqrt{gL}.
> $$

> [!warning] 角從鉛直量
> Example 5.5 的 $\theta$ 是和水平的夾角（$r = L\cos\theta$）；這題和鉛直的夾角，$r = L\sin\theta$。

## 老師勾選：傾斜轉彎

### EUP 5.25
題目：[[PHY1 HW Ch05 Questions#EUP 5.25|EUP 5.25]]

> [!solution] 解
> 升力垂直機翼，機翼與水平成 $\theta = 22^{\circ}$，所以升力與鉛直成 $\theta$。同 Example 5.6：
> $$
> F_{\mathrm{w}}\sin\theta = \frac{mv^{2}}{r}, \quad F_{\mathrm{w}}\cos\theta = mg \implies \tan\theta = \frac{v^{2}}{gr}.
> $$
> $$
> \begin{aligned}
> v = \sqrt{gr\tan\theta} &= \sqrt{(9.8\ \mathrm{m/s^2})(4.0 \times 10^{3}\ \mathrm{m})\tan 22^{\circ}} \\
> &= 1.3 \times 10^{2}\ \mathrm{m/s}\ (\approx 450\ \mathrm{km/h}).
> \end{aligned}
> $$

### EUP 5.47
題目：[[PHY1 HW Ch05 Questions#EUP 5.47|EUP 5.47]]

![EUP Figure 5.35|300](../Attachments/PHY1%20Ch05%20Fig%205.35.png)

> [!solution] 解
> $v = 960\ \mathrm{km/h} = 266.7\ \mathrm{m/s}$。由 [[#EUP 5.25|EUP 5.25]] 的 $\tan\theta = v^{2}/(gr)$，$r = v^{2}/(g\tan\theta)$ 隨 $\theta$ 增大而減小，所以最大傾斜角給最小半徑：
> $$
> r_{\min} = \frac{v^{2}}{g\tan 35^{\circ}} = \frac{(266.7\ \mathrm{m/s})^{2}}{(9.8\ \mathrm{m/s^2})\tan 35^{\circ}} = 1.0 \times 10^{4}\ \mathrm{m}.
> $$

## 老師勾選：摩擦與煞車

### EUP 5.27
題目：[[PHY1 HW Ch05 Questions#EUP 5.27|EUP 5.27]]

> [!solution] 解
> 唯一的水平力是動摩擦，$\mu_{\mathrm{k}}mg = ma$，$a = \mu_{\mathrm{k}}g$（Example 5.8）。由 (2.11)，末速為零，$v_{0}^{2} = 2\mu_{\mathrm{k}}gd$：
> $$
> \mu_{\mathrm{k}} = \frac{v_{0}^{2}}{2gd} = \frac{(11\ \mathrm{m/s})^{2}}{2(9.8\ \mathrm{m/s^2})(60\ \mathrm{m})} = 0.10.
> $$

### EUP 5.53
題目：[[PHY1 HW Ch05 Questions#EUP 5.53|EUP 5.53]]

> [!solution] 解
> 車輪不打滑，是靜摩擦，最大減速度 $\mu_{\mathrm{s}}g$。$v_{0} = 140\ \mathrm{km/h} = 38.9\ \mathrm{m/s}$，同 Example 5.8：
> $$
> \Delta x = \frac{v_{0}^{2}}{2\mu_{\mathrm{s}}g} = \frac{(38.9\ \mathrm{m/s})^{2}}{2(0.58)(9.8\ \mathrm{m/s^2})} = 133\ \mathrm{m} < 150\ \mathrm{m}.
> $$
> 來得及，停下時離那輛車約 $17\ \mathrm{m}$。

## 加選：靜力平衡

### EUP 5.44
題目：[[PHY1 HW Ch05 Questions#EUP 5.44|EUP 5.44]]

![EUP Figure 5.34|300](../Attachments/PHY1%20Ch05%20Fig%205.34.png)

> [!solution] 解
> 滑輪無質量、無摩擦，$m$ 靜止，整條繩的張力 $T = mg$。腿上的滑輪被兩段繩拉：上段與水平成 $70^{\circ}$、下段成 $20^{\circ}$，水平分量同向：
> $$
> F = T\cos 70^{\circ} + T\cos 20^{\circ} = (4.6\ \mathrm{kg})(9.8\ \mathrm{m/s^2})(\cos 70^{\circ} + \cos 20^{\circ}) = 58\ \mathrm{N}.
> $$

> [!warning] 牽引力大於 mg
> 繩繞過腿上的滑輪，兩段都拉它，所以水平牽引力是 $1.28mg$，不是 $mg$。

### EUP 5.75
題目：[[PHY1 HW Ch05 Questions#EUP 5.75|EUP 5.75]]

![EUP Figure 5.38|300](../Attachments/PHY1%20Ch05%20Fig%205.38.png)

> [!solution] 解
> 左繩 $T_{1}$（與水平成 $54.0^{\circ}$）、右繩 $T_{2}$（$68.0^{\circ}$）、中間繩 $T_{3}$（低於水平 $13.9^{\circ}$）。把兩盆花和中間的線當一個系統，$T_{3}$ 是內力：
> $$
> \begin{aligned}
> x&:\ T_{2}\cos 68.0^{\circ} - T_{1}\cos 54.0^{\circ} = 0, \\
> y&:\ T_{1}\sin 54.0^{\circ} + T_{2}\sin 68.0^{\circ} = (m_{1} + m_{2})g
> \end{aligned}
> $$
> 同 [[#EUP 5.42|EUP 5.42]] 的解法，$(m_{1} + m_{2})g = (13.13\ \mathrm{kg})(9.8\ \mathrm{m/s^2}) = 128.7\ \mathrm{N}$：
> $$
> \begin{aligned}
> T_{1} &= \frac{(m_{1} + m_{2})g\cos 68.0^{\circ}}{\sin 122.0^{\circ}} = 56.8\ \mathrm{N}, \\
> T_{2} &= \frac{(m_{1} + m_{2})g\cos 54.0^{\circ}}{\sin 122.0^{\circ}} = 89.2\ \mathrm{N}.
> \end{aligned}
> $$
> 左盆的水平分量：$T_{3}\cos 13.9^{\circ} = T_{1}\cos 54.0^{\circ}$，$T_{3} = 34.4\ \mathrm{N}$（鉛直分量 $T_{1}\sin 54.0^{\circ} - T_{3}\sin 13.9^{\circ} = 37.7\ \mathrm{N} = m_{1}g$，一致）。最大張力 $89\ \mathrm{N} < 100\ \mathrm{N}$，行得通。

## 加選：相連物體

### EUP 5.19
題目：[[PHY1 HW Ch05 Questions#EUP 5.19|EUP 5.19]]

> [!solution] 解
> 各自沿坡往下為正。單獨下滑時上方者 $g\sin 16^{\circ} = 2.70\ \mathrm{m/s^2}$、下方者 $g\sin 32^{\circ} = 5.19\ \mathrm{m/s^2}$，下方者較快，繩是拉緊的：
> $$
> m_{1}g\sin 16^{\circ} + T = m_{1}a, \qquad m_{2}g\sin 32^{\circ} - T = m_{2}a
> $$
> **(a)** 相加：
> $$
> \begin{aligned}
> a &= \frac{(m_{1}\sin 16^{\circ} + m_{2}\sin 32^{\circ})g}{m_{1} + m_{2}} \\
> &= \frac{(80\ \mathrm{kg})\sin 16^{\circ} + (65\ \mathrm{kg})\sin 32^{\circ}}{145\ \mathrm{kg}}(9.8\ \mathrm{m/s^2}) = 3.8\ \mathrm{m/s^2}.
> \end{aligned}
> $$
> **(b)** 靜止時冰斧的力平衡兩人重力沿坡的分量：
> $$
> F = (m_{1}\sin 16^{\circ} + m_{2}\sin 32^{\circ})g = 5.5 \times 10^{2}\ \mathrm{N}.
> $$

> [!warning] 先確認繩子拉緊
> 若下方者單獨下滑較慢，繩會鬆，兩人各以 $g\sin\theta$ 下滑。

### EUP 5.51
題目：[[PHY1 HW Ch05 Questions#EUP 5.51|EUP 5.51]]

> [!solution] 解
> 石頭多了向左的動摩擦 $\mu_{\mathrm{k}}m_{\mathrm{r}}g$：
> $$
> \text{rock:}\ T - \mu_{\mathrm{k}}m_{\mathrm{r}}g = m_{\mathrm{r}}a, \qquad \text{climber:}\ m_{\mathrm{c}}g - T = m_{\mathrm{c}}a
> $$
> $$
> a = \frac{(m_{\mathrm{c}} - \mu_{\mathrm{k}}m_{\mathrm{r}})g}{m_{\mathrm{c}} + m_{\mathrm{r}}} = \frac{(73\ \mathrm{kg} - 0.049 \times 940\ \mathrm{kg})(9.8\ \mathrm{m/s^2})}{1013\ \mathrm{kg}} = 0.26\ \mathrm{m/s^2}.
> $$
> 由 (2.10)，$t = \sqrt{2x/a} = \sqrt{2(51\ \mathrm{m})/(0.261\ \mathrm{m/s^2})} = 20\ \mathrm{s}$。

> [!warning] 假設石頭會動
> 題目只給 $\mu_{\mathrm{k}}$；石頭要開始動，需 $\mu_{\mathrm{s}} < m_{\mathrm{c}}/m_{\mathrm{r}} = 0.078$。

## 加選：斜拉、斜推與驅動輪的摩擦

### EUP 5.50
題目：[[PHY1 HW Ch05 Questions#EUP 5.50|EUP 5.50]]

> [!solution] 解
> 沿把手推，力 $F$ 指向前下方、低於水平 $37^{\circ}$。等速：
> $$
> y:\ n = mg + F\sin 37^{\circ}, \qquad x:\ F\cos 37^{\circ} = \mu n = \mu(mg + F\sin 37^{\circ})
> $$
> $$
> F = \frac{\mu mg}{\cos 37^{\circ} - \mu\sin 37^{\circ}} = \frac{(0.68)(26\ \mathrm{kg})(9.8\ \mathrm{m/s^2})}{\cos 37^{\circ} - 0.68\sin 37^{\circ}} = 4.4 \times 10^{2}\ \mathrm{N},
> $$
> 約為重量 $mg = 255\ \mathrm{N}$ 的 $1.7$ 倍。

> [!warning] 往下推，正向力變大
> $n = mg + F\sin\theta$，不是 $mg$；推力的向下分量增加摩擦（對照 Example 5.11 的往上拉）。

### EUP 5.57
題目：[[PHY1 HW Ch05 Questions#EUP 5.57|EUP 5.57]]

> [!solution] 解
> 只有前輪驅動，向前的靜摩擦只能來自前輪，前輪的正向力 $0.70mg$：
> $$
> a_{\max} = \frac{\mu(0.70mg)}{m} = (0.70)(0.61)(9.8\ \mathrm{m/s^2}) = 4.2\ \mathrm{m/s^2}.
> $$

> [!warning] 不是 μg
> 後輪不驅動，它的正向力不提供向前的摩擦。

### EUP 5.60
題目：[[PHY1 HW Ch05 Questions#EUP 5.60|EUP 5.60]]

> [!solution] 解
> 推力 $F$ 低於水平 $50^{\circ}$，$n = mg + F\sin 50^{\circ}$。推不動的條件是水平推力不超過最大靜摩擦：
> $$
> F\cos 50^{\circ} \le \mu_{\mathrm{s}}(mg + F\sin 50^{\circ}) \iff F(\cos 50^{\circ} - \mu_{\mathrm{s}}\sin 50^{\circ}) \le \mu_{\mathrm{s}}mg.
> $$
> 若 $\mu_{\mathrm{s}} \ge \cos 50^{\circ}/\sin 50^{\circ} = \cot 50^{\circ} = 0.84$，左邊對任何 $F > 0$ 都 $\le 0$，不等式恆成立：再用力也推不動。$\blacksquare$

## 加選：斜面上的摩擦

### EUP 5.61
題目：[[PHY1 HW Ch05 Questions#EUP 5.61|EUP 5.61]]

> [!solution] 解
> **(a)** $x$ 沿坡往上。上滑時摩擦沿坡往下，$n = mg\cos\theta$：
> $$
> a = -g(\sin 22^{\circ} + \mu_{\mathrm{k}}\cos 22^{\circ}) = -(9.8\ \mathrm{m/s^2})(0.375 + 0.649) = -10.0\ \mathrm{m/s^2}.
> $$
> 由 (2.11)，$d = \dfrac{v_{0}^{2}}{2\lvert a \rvert} = \dfrac{(1.4\ \mathrm{m/s})^{2}}{2(10.0\ \mathrm{m/s^2})} = 0.098\ \mathrm{m} = 9.8\ \mathrm{cm}$。
>
> **(b)** 靜止時，同 Example 5.10，滑下的條件是 $\tan 22^{\circ} = 0.40 > \mu_{\mathrm{s}}$。$\mu_{\mathrm{s}} \ge \mu_{\mathrm{k}} = 0.70 > 0.40$，所以不會滑回來。

> [!warning] 上滑和下滑的摩擦方向相反
> 上滑時重力分量和摩擦同向（都往下坡），減速度 $g(\sin\theta + \mu\cos\theta)$；下滑時兩者反向。

### EUP 5.70
題目：[[PHY1 HW Ch05 Questions#EUP 5.70|EUP 5.70]]

> [!solution] 解
> 摩擦永遠和運動反向。上滑與下滑的加速度大小：
> $$
> a_{\mathrm{up}} = g(\sin\theta + \mu_{\mathrm{k}}\cos\theta), \qquad a_{\mathrm{down}} = g(\sin\theta - \mu_{\mathrm{k}}\cos\theta).
> $$
> 上去和下來走同一段距離 $d$，由 (2.11)，$v_{0}^{2} = 2a_{\mathrm{up}}d$、$(v_{0}/2)^{2} = 2a_{\mathrm{down}}d$，相除得 $a_{\mathrm{down}} = a_{\mathrm{up}}/4$：
> $$
> \begin{aligned}
> 4(\sin\theta - \mu_{\mathrm{k}}\cos\theta) &= \sin\theta + \mu_{\mathrm{k}}\cos\theta \\
> \implies 3\sin\theta = 5\mu_{\mathrm{k}}\cos\theta &\implies \mu_{\mathrm{k}} = \tfrac{3}{5}\tan\theta. \qquad \blacksquare
> \end{aligned}
> $$

## 加選：疊放物體的靜摩擦

### EUP 5.55
題目：[[PHY1 HW Ch05 Questions#EUP 5.55|EUP 5.55]]

> [!solution] 解
> 平裝書受的水平力只有課本對它的靜摩擦，$f = ma \le \mu_{\mathrm{s}}mg$，所以不滑動需 $a \le \mu_{\mathrm{s}}g$。
> - 加速時一起動：$a_{1} = \dfrac{0.96\ \mathrm{m/s}}{0.42\ \mathrm{s}} = 2.29\ \mathrm{m/s^2} \le \mu_{\mathrm{s}}g$，$\mu_{\mathrm{s}} \ge 0.233$。
> - 停下時滑落：要跟著停需 $a_{2} = \dfrac{0.96\ \mathrm{m/s}}{0.33\ \mathrm{s}} = 2.91\ \mathrm{m/s^2}$，它滑了，所以 $\mu_{\mathrm{s}}g < a_{2}$，$\mu_{\mathrm{s}} < 0.297$。
>
> $0.23 \le \mu_{\mathrm{s}} < 0.30$。

## 加選：圓周運動

### EUP 5.23
題目：[[PHY1 HW Ch05 Questions#EUP 5.23|EUP 5.23]]

> [!solution] 解
> 吊環只受重力和吊帶張力，和車一起做半徑 $r$ 的圓周運動。張力與鉛直成 $\theta$，同 [[#EUP 5.62|EUP 5.62]]，$\tan\theta = v^{2}/(gr)$：
> $$
> \begin{aligned}
> v = \sqrt{gr\tan\theta} &= \sqrt{(9.8\ \mathrm{m/s^2})(150\ \mathrm{m})\tan 15^{\circ}} \\
> &= 19.8\ \mathrm{m/s} = 71\ \mathrm{km/h} > 50\ \mathrm{km/h}.
> \end{aligned}
> $$
> 列車超速。

### EUP 5.45
題目：[[PHY1 HW Ch05 Questions#EUP 5.45|EUP 5.45]]

> [!solution] 解
> 頂端取 **$+y$ 向下**（指向圓心）。乘客倒過來，座椅在他上方，只能把他往下（圓心方向）推；安全帶只能把他往上拉向座椅。所需的淨力
> $$
> \frac{mv^{2}}{r} = \frac{(55\ \mathrm{kg})(9.5\ \mathrm{m/s})^{2}}{6.7\ \mathrm{m}} = 741\ \mathrm{N} > mg = 539\ \mathrm{N},
> $$
> 重力不夠，差額由座椅向下推補足，安全帶不用出力：
> - (a) $n = mv^{2}/r - mg = 2.0 \times 10^{2}\ \mathrm{N}$，向下。
> - (b) $0$。
> - (c) 不會怎樣：乘客仍被壓在座椅上（同 Conceptual Example 5.1）。

### EUP 5.67
題目：[[PHY1 HW Ch05 Questions#EUP 5.67|EUP 5.67]]

> [!solution] 解
> 牆的正向力指向圓心，提供向心力；向上的靜摩擦撐住重力：
> $$
> n = m\omega^{2}r, \qquad \mu_{\mathrm{s}}n \ge mg \implies \omega \ge \sqrt{\frac{g}{\mu_{\mathrm{s}}r}} = \sqrt{\frac{9.8\ \mathrm{m/s^2}}{(0.72)(5.1\ \mathrm{m})}} = 1.63\ \mathrm{rad/s}.
> $$
> $1.63\ \mathrm{rad/s} \times \dfrac{60\ \mathrm{s/min}}{2\pi\ \mathrm{rad/rev}} = 16\ \mathrm{rev/min}$。

## 加選：傾斜彎道與摩擦

### EUP 5.63
題目：[[PHY1 HW Ch05 Questions#EUP 5.63|EUP 5.63]]

> [!solution] 解
> 設計角由 Example 5.6：$v_{0} = 76\ \mathrm{km/h} = 21.1\ \mathrm{m/s}$，$\tan\theta = \dfrac{v_{0}^{2}}{gR} = \dfrac{(21.1\ \mathrm{m/s})^{2}}{(9.8\ \mathrm{m/s^2})(230\ \mathrm{m})} = 0.198$（$\theta = 11.2^{\circ}$）。最快時摩擦沿坡往下、取最大值 $\mu n$，$+x$ 指向圓心：
> $$
> x:\ n\sin\theta + \mu n\cos\theta = \frac{mv^{2}}{R}, \qquad y:\ n\cos\theta - \mu n\sin\theta - mg = 0
> $$
> 相除：
> $$
> \begin{aligned}
> v_{\max} &= \sqrt{gR\,\frac{\tan\theta + \mu}{1 - \mu\tan\theta}} = \sqrt{(9.8\ \mathrm{m/s^2})(230\ \mathrm{m})\frac{0.198 + 0.20}{1 - (0.20)(0.198)}} \\
> &= 30.6\ \mathrm{m/s} = 110\ \mathrm{km/h}.
> \end{aligned}
> $$
> 有可能超速，最多約 $34\ \mathrm{km/h}$。

> [!warning] 留在車道上不代表是設計速率
> 有摩擦時，從 $v_{\min}$ 到 $v_{\max}$ 的速率都能過彎；設計速率只是不需要摩擦的那一個。

### EUP 5.72
題目：[[PHY1 HW Ch05 Questions#EUP 5.72|EUP 5.72]]

> [!solution] 解
> 設計速率 $v_{0} = 16.7\ \mathrm{m/s}$，$\tan\theta = v_{0}^{2}/(gR) = 0.258$（$\theta = 14.4^{\circ}$）。$v = 25\ \mathrm{m/s} > v_{0}$，摩擦沿坡往下。[[#EUP 5.63|EUP 5.63]] 的兩式解 $\mu$：
> $$
> \mu = \frac{v^{2} - gR\tan\theta}{gR + v^{2}\tan\theta} = \frac{(25\ \mathrm{m/s})^{2} - (16.7\ \mathrm{m/s})^{2}}{(9.8\ \mathrm{m/s^2})(110\ \mathrm{m}) + (25\ \mathrm{m/s})^{2}(0.258)} = 0.28.
> $$
> 代入 $\tan\theta = v_{0}^{2}/(gR)$，一般式是 $\mu = \dfrac{gR(v^{2} - v_{0}^{2})}{g^{2}R^{2} + v^{2}v_{0}^{2}}$（Problem 66）。

## 加選：煞車還是轉向

### EUP 5.69
題目：[[PHY1 HW Ch05 Questions#EUP 5.69|EUP 5.69]]

![EUP Figure 5.37|300](../Attachments/PHY1%20Ch05%20Fig%205.37.png)

> [!solution] 解
> 煞車（Example 5.8）：停下需要的距離 $d = \dfrac{v^{2}}{2\mu_{\mathrm{s}}g}$。
>
> 轉向（Example 5.9）：等速轉彎的最小半徑 $r = \dfrac{v^{2}}{\mu_{\mathrm{s}}g}$；轉 $90^{\circ}$ 閃開時，車往前要走 $r$。
>
> $r = 2d$：煞車只需轉向一半的距離，煞車比較安全。

## 加選：拖曳力

### EUP 5.73
題目：[[PHY1 HW Ch05 Questions#EUP 5.73|EUP 5.73]]

> [!solution] 解
> **(a)** 取 **$+y$ 向下**，$m\dfrac{dv}{dt} = mg - bv$。分離變數，由 $v = 0$、$t = 0$ 積分：
> $$
> \begin{aligned}
> \int_{0}^{v}\frac{dv}{g - (b/m)v} = \int_{0}^{t}dt &\implies -\frac{m}{b}\ln\left(1 - \frac{bv}{mg}\right) = t \\
> &\implies v(t) = \frac{mg}{b}\left(1 - e^{-bt/m}\right).
> \end{aligned}
> $$
> **(b)** $t \to \infty$ 時 $e^{-bt/m} \to 0$，$v \to mg/b$；此時 $mg = bv$，淨力為零，速率不再改變。$\blacksquare$

## 加選：數據題

### EUP 5.76
題目：[[PHY1 HW Ch05 Questions#EUP 5.76|EUP 5.76]]

> [!solution] 解
> **(a)** 同 Example 5.4：$m_{1}g - T = m_{1}a$，$T = m_{2}a$，所以
> $$
> a = g\,\frac{m_{1}}{m_{1} + m_{2}}.
> $$
> $a$ 對 $m_{1}/(m_{1} + m_{2})$ 作圖是通過原點、斜率 $g$ 的直線。
>
> **(b)**
>
> | $m_{1}/(m_{1} + m_{2})$ | $0.0556$ | $0.0357$ | $0.0263$ | $0.1053$ | $0.0690$ | $0.0513$ |
> | --- | --- | --- | --- | --- | --- | --- |
> | $a$ ($\mathrm{m/s^2}$) | $0.521$ | $0.376$ | $0.274$ | $1.06$ | $0.652$ | $0.534$ |
>
> 最小平方擬合：斜率 $9.77\ \mathrm{m/s^2}$，截距 $0.011\ \mathrm{m/s^2}$（約為零，和理論一致）。實驗值 $g = 9.8\ \mathrm{m/s^2}$。
>
> ![EUP 5.76 fit|480](../Attachments/PHY1%20Ch05%20Problem%205.76%20fit.png)

## 加選：轉彎時的傾斜

### EUP 5.77 to 5.80
題目：[[PHY1 HW Ch05 Questions#EUP 5.77 to 5.80|EUP 5.77 to 5.80]]

> [!solution] 解
> 冰對冰刀的力有鉛直分量 $n = mg$ 和水平分量（摩擦）$f = ma$，合力要通過質心選手才不會倒，所以身體與鉛直的傾角滿足 $\tan\theta = f/n = a/g$（和 [[#EUP 5.62|EUP 5.62]] 的錐擺同樣的關係）。
> - **77.** a。身體向她的左側傾斜，轉彎時人要向圓心傾斜，所以她在左轉。
> - **78.** a。淨力指向轉彎的圓心，也就是她的左邊。
> - **79.** b。半徑相同時速率越大，$a = v^{2}/r$ 越大，$\tan\theta = a/g$ 越大。
> - **80.** c。$a = g\tan\theta = (9.8\ \mathrm{m/s^2})(0.5) = 4.9\ \mathrm{m/s^2} \approx 5\ \mathrm{m/s^2}$。

> [!warning] 照片沒附
> 77 要看照片；這裡依課本圖 5.40 的描述作答（選手面向鏡頭，身體向畫面右側、也就是她的左側傾斜）。

## 外校考題：觀念題

### KSUF 2.1 and 2.2
題目：[[PHY1 HW Ch05 Questions#KSUF 2.1 and 2.2|KSUF 2.1 and 2.2]]

> [!solution] 解
> - **1.** e。淨力決定的是**加速度**（向東北，$\sqrt{2}(3.0\ \mathrm{N})/(1.5\ \mathrm{kg}) = 2.8\ \mathrm{m/s^2}$），不是速度；不知道原來的速度，它可能朝任何方向運動。
> - **2.** b。等速度，$\vec{a} = \vec{0}$，淨力為零；仍可以有多個力（例如重力和正向力）互相抵消。

### KSUF 2.13 to 2.17
題目：[[PHY1 HW Ch05 Questions#KSUF 2.13 to 2.17|KSUF 2.13 to 2.17]]

> [!solution] 解
> - **13.** F。靜摩擦可以使物體加速：走路、汽車加速都是靜摩擦（圖 5.21、5.22）。
> - **14.** F。把箱子放到運轉中的輸送帶上，動摩擦使箱子加速，直到和皮帶同速。
> - **15.** F。向心加速度指向圓心。
> - **16.** T。平坦彎道上，輪胎受的水平力只有摩擦（Example 5.9）。
> - **17.** T。設計速率時正向力的水平分量就提供全部向心力（Example 5.6）。

### KSUS 2.6 and 2.7
題目：[[PHY1 HW Ch05 Questions#KSUS 2.6 and 2.7|KSUS 2.6 and 2.7]]

> [!solution] 解
> - **6.** F。大小 $v^{2}/r$ 不變，但方向一直指向圓心、不斷改變，加速度向量不是常數。
> - **7.** T。圓心在左邊，向心加速度指向左。

### KSUS 2.15 and 2.16
題目：[[PHY1 HW Ch05 Questions#KSUS 2.15 and 2.16|KSUS 2.15 and 2.16]]

> [!solution] 解
> - **15.** F。同 [[#KSUF 2.13 to 2.17|KSUF 2.13]]。
> - **16.** F。向心力指向內。水離開是因為衣服和桶壁的孔洞**無法**提供水做圓周運動所需的向心力，水就沿切線直線飛出（牛頓第一定律）。

### SIU 22.2
題目：[[PHY1 HW Ch05 Questions#SIU 22.2|SIU 22.2]]

> [!solution] 解
> 杯子受的水平力只有桌面的靜摩擦，杯子要跟著飛機向前加速，所以摩擦力**向前**，和飛機速度同方向（只要 $a \le \mu_{\mathrm{s}}g = 4.9\ \mathrm{m/s^2}$，杯子不滑）。

### SIU 23.3 and 23.4
題目：[[PHY1 HW Ch05 Questions#SIU 23.3 and 23.4|SIU 23.3 and 23.4]]

> [!solution] 解
> - **3.** 做不到。$F$ 和 $N$ 都是水平的，牆無摩擦，沒有任何向上的力平衡 $mg$；$F$ 再大物體也會往下掉（真實的牆是靠靜摩擦 $\mu_{\mathrm{s}}N \ge mg$ 撐住）。
> - **4.** 做不到。平坦無摩擦的路面無法對車施水平力，沒有向心力就不能轉彎，車會直線前進（牛頓第一定律）。

## 外校考題：計算題

### KSUF 2.11
題目：[[PHY1 HW Ch05 Questions#KSUF 2.11|KSUF 2.11]]

> [!solution] 解
> 正確煞車＝車輪不打滑，用靜摩擦。$x$ 沿坡往下；最大靜摩擦 $\mu_{\mathrm{s}}n$ 沿坡往上，$n = mg\cos\theta$：
> $$
> \begin{aligned}
> a = g\sin\theta - \mu_{\mathrm{s}}g\cos\theta &= (9.80\ \mathrm{m/s^2})(\sin 12.0^{\circ} - 0.85\cos 12.0^{\circ}) \\
> &= -6.11\ \mathrm{m/s^2}.
> \end{aligned}
> $$
> 最大減速度 $6.11\ \mathrm{m/s^2}$。

> [!warning] 多餘數據
> 速率 $26.8\ \mathrm{m/s}$ 和 $\mu_{\mathrm{k}}$ 都用不到；下坡時重力分量抵掉一部分摩擦，減速度比平路的 $\mu_{\mathrm{s}}g$ 小。

### KSUF 2.12
題目：[[PHY1 HW Ch05 Questions#KSUF 2.12|KSUF 2.12]]

> [!solution] 解
> 「感覺到 $0.500g$」指地板的正向力是 $0.500mg$，它提供向心力：
> - a) $\dfrac{mv^{2}}{r} = 0.500mg \implies v = \sqrt{0.500gr} = \sqrt{(0.500)(9.80\ \mathrm{m/s^2})(92.0\ \mathrm{m})} = 21.2\ \mathrm{m/s}$。
> - b) $T = \dfrac{2\pi r}{v} = \dfrac{2\pi(92.0\ \mathrm{m})}{21.2\ \mathrm{m/s}} = 27.2\ \mathrm{s}$。

### KSUF 2.18
題目：[[PHY1 HW Ch05 Questions#KSUF 2.18|KSUF 2.18]]

> [!solution] 解
> - a) 同 Example 5.9：$v_{\max} = \sqrt{\mu_{\mathrm{s}}gr} = \sqrt{(0.850)(9.80\ \mathrm{m/s^2})(155\ \mathrm{m})} = 35.9\ \mathrm{m/s}$。
> - b) 摩擦只需提供所需的向心力：
> $$
> f = \frac{m(v_{\max}/2)^{2}}{r} = \frac{\mu_{\mathrm{s}}mg}{4} = \frac{(0.850)(1660\ \mathrm{kg})(9.80\ \mathrm{m/s^2})}{4} = 3.46 \times 10^{3}\ \mathrm{N}.
> $$

> [!warning] 靜摩擦不是 μs n
> 沒有即將打滑時，靜摩擦只有需要的大小；$\mu_{\mathrm{k}}$ 用不到。

### KSUS 2.18
題目：[[PHY1 HW Ch05 Questions#KSUS 2.18|KSUS 2.18]]

> [!solution] 解
> - a) 四輪驅動，四個輪子都提供向前的靜摩擦，最大值 $\mu_{\mathrm{s}}mg = m(0.16g)$：$\mu_{\mathrm{s}} = 0.16$。
> - b) 等速爬坡，靜摩擦平衡重力沿坡分量：$mg\sin\theta \le \mu_{\mathrm{s}}mg\cos\theta$，最陡 $\tan\theta = \mu_{\mathrm{s}}$（同 Example 5.10）：$\theta = \tan^{-1}(0.16) = 9.1^{\circ}$。

> [!warning] 多餘數據
> 鎖死打滑的 $-0.080g$ 給的是 $\mu_{\mathrm{k}} = 0.080$，兩小題都用不到。

### KSUS 2.19
題目：[[PHY1 HW Ch05 Questions#KSUS 2.19|KSUS 2.19]]

> [!solution] 解
> - a) 鞦韆鋼索張力的水平分量（指向轉軸）。
> - b) 由 [[#EUP 5.21|EUP 5.21]]，$F = \dfrac{4\pi^{2}mr}{T^{2}} = \dfrac{4\pi^{2}(75\ \mathrm{kg})(4.0\ \mathrm{m})}{(8.0\ \mathrm{s})^{2}} = 1.9 \times 10^{2}\ \mathrm{N}$。
> - c) $T_{\mathrm{c}}\sin\varphi = F$、$T_{\mathrm{c}}\cos\varphi = mg$（$T_{\mathrm{c}}$ 是鋼索張力）：$\tan\varphi = \dfrac{F}{mg} = \dfrac{185\ \mathrm{N}}{(75\ \mathrm{kg})(9.80\ \mathrm{m/s^2})} = 0.252$，$\varphi = 14^{\circ}$。

### SIU 22.7
題目：[[PHY1 HW Ch05 Questions#SIU 22.7|SIU 22.7]]

> [!solution] 解
> $v = 0.95v_{\mathrm{T}} \implies e^{-t/\tau} = 0.05 \implies t = \tau\ln 20$，$\tau = v_{\mathrm{T}}/g$：
> $$
> t = \frac{9.8 \times 10^{-3}\ \mathrm{m/s}}{9.8\ \mathrm{m/s^2}}\ln 20 = (1.0 \times 10^{-3}\ \mathrm{s})(3.00) = 3.0\ \mathrm{ms}.
> $$

### SIU 23.7
題目：[[PHY1 HW Ch05 Questions#SIU 23.7|SIU 23.7]]

> [!solution] 解
> 鎖死打滑用動摩擦，同 Example 5.8：
> $$
> \Delta x = \frac{v_{0}^{2}}{2\mu_{\mathrm{k}}g} = \frac{(31.3\ \mathrm{m/s})^{2}}{2(0.60)(9.8\ \mathrm{m/s^2})} = 83\ \mathrm{m}.
> $$
