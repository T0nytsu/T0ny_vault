---
course: [PHY1]
semester: "115-1"
chapter: ["1.2", "1.3"]
tags: [physics, homework, solutions, measurement]
source:
  - "Own solutions; every number recomputed with Python"
  - "EUP Ch. 1 (pp. 17-30), scanned PDF: Tables 1.1 and 1.2, rules for significant figures"
  - "[[PHY1 Ch01 Problem 1.69 fit.png]]"
created: 2026-11-01
questions: "[[PHY1 HW Ch01 Questions]]"
up: "[[PHY1 Index]]"
format: "physics-notes 1.1"
---
> [!note] 符號與公式
> - 本章沒有編號的式子。單位換算一律乘上**等於 1 的比值**，讓單位一路相消；換算值取附錄 C：$1\ \mathrm{ft} = 0.3048\ \mathrm{m}$、$1\ \mathrm{in} = 2.54\ \mathrm{cm}$、$1\ \mathrm{gal} = 3.785\ \mathrm{L}$、$1\ \mathrm{L} = 1000\ \mathrm{cm^3}$。
> - 弧度：$\theta = s/r$（圖 1.2）。
> - 有效數字：**乘除**取最少的有效數字位數；**加減**取最少的小數點後位數（先換成同一單位再比）。
> - 估計題取一位有效數字或 10 的次方。中間值多留一位有效數字。

## 答案總表

| 題目 | 答案 |
| --- | --- |
| [[PHY1 HW Ch01 Questions#EUP 1.18\|EUP 1.18]] | (a) $25.0\ \mathrm{m/s}$；(b) $82.0\ \mathrm{ft/s}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.23\|EUP 1.23]] | $8.10\ \mathrm{m^2/L}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.26\|EUP 1.26]] | $2.5 \times 10^{2}\ \mathrm{cm^3/s} = 2.5 \times 10^{-4}\ \mathrm{m^3/s}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.67\|EUP 1.67]] | $439\ \mathrm{W}$；發的比用的多 |
| [[PHY1 HW Ch01 Questions#EUP 1.17\|EUP 1.17]] | $0.58\ \mathrm{rad} \approx 33^{\circ}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.31\|EUP 1.31]] | $7.4 \times 10^{6}\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.32\|EUP 1.32]] | $1.3 \times 10^{2}\ \mathrm{N \cdot m}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.33\|EUP 1.33]] | $5.00 \times 10^{7}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.35 and 1.36\|EUP 1.35 and 1.36]] | $41\ \mathrm{m}$；$41.09\ \mathrm{m}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.44\|EUP 1.44]] | $12.05\ \mathrm{h}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.45\|EUP 1.45]] | (a) $5.57$；(b) $5.65$ |
| [[PHY1 HW Ch01 Questions#EUP 1.57\|EUP 1.57]] | 約 $0.4\%$ 與 $0.05\%$ |
| [[PHY1 HW Ch01 Questions#EUP 1.65\|EUP 1.65]] | (a) $1.0\ \mathrm{m}$；(b) $1 \times 10^{-3}\ \mathrm{m^2}$；(c) $0.0\ \mathrm{m}$；(d) $1.0$ |
| [[PHY1 HW Ch01 Questions#EUP 1.53\|EUP 1.53]] | 約 $0.2\ \mathrm{mm}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.55\|EUP 1.55]] | (a) $40\ \mathrm{nm}$；(b) 每秒約 $5 \times 10^{5}$ 次 |
| [[PHY1 HW Ch01 Questions#EUP 1.66\|EUP 1.66]] | 對，最多可放約 $2.4 \times 10^{10}$ 個 |
| [[PHY1 HW Ch01 Questions#EUP 1.69\|EUP 1.69]] | (a) $d^{3}$；(b) 斜率約 $4.1\ \mathrm{g/cm^3}$（密度約 $7.8\ \mathrm{g/cm^3}$） |
| [[PHY1 HW Ch01 Questions#EUP 1.70 to 1.73\|EUP 1.70 to 1.73]] | a, b, b, c |
| [[PHY1 HW Ch01 Questions#KSUS 1.3 and 1.4\|KSUS 1.3 and 1.4]] | d, c |
| [[PHY1 HW Ch01 Questions#SIU 1.1\|SIU 1.1]] | $L/T$（速度的因次） |
| [[PHY1 HW Ch01 Questions#KSUS 1.1 and 1.2\|KSUS 1.1 and 1.2]] | $24\ \mathrm{mg}$；$11.1$ 天 |
| [[PHY1 HW Ch01 Questions#KSUS 1.5 and 1.6\|KSUS 1.5 and 1.6]] | $8.9 \times 10^{2}\ \mathrm{m}$；$2.78\ \mathrm{kg}$ |

## 加選：單位換算

### EUP 1.18
題目：[[PHY1 HW Ch01 Questions#EUP 1.18|EUP 1.18]]

> [!solution] 答案
> $$
> \begin{aligned}
> \text{(a)}\quad 90.0\ \mathrm{km/h} &= \left(\frac{90.0\ \mathrm{km}}{\mathrm{h}}\right)\left(\frac{1000\ \mathrm{m}}{1\ \mathrm{km}}\right)\left(\frac{1\ \mathrm{h}}{3600\ \mathrm{s}}\right) = 25.0\ \mathrm{m/s} \\
> \text{(b)}\quad 25.0\ \mathrm{m/s} &= \left(\frac{25.0\ \mathrm{m}}{\mathrm{s}}\right)\left(\frac{1\ \mathrm{ft}}{0.3048\ \mathrm{m}}\right) = 82.0\ \mathrm{ft/s}
> \end{aligned}
> $$

### EUP 1.23
題目：[[PHY1 HW Ch01 Questions#EUP 1.23|EUP 1.23]]

> [!solution] 答案
> $$
> \frac{330\ \mathrm{ft^2}}{1\ \mathrm{gal}}\left(\frac{0.3048\ \mathrm{m}}{1\ \mathrm{ft}}\right)^{2}\left(\frac{1\ \mathrm{gal}}{3.785\ \mathrm{L}}\right) = 8.10\ \mathrm{m^2/L}
> $$

> [!warning] 面積的換算因子要平方
> $1\ \mathrm{ft^2} = (0.3048\ \mathrm{m})^{2} = 0.0929\ \mathrm{m^2}$，不是 $0.3048\ \mathrm{m^2}$。

### EUP 1.26
題目：[[PHY1 HW Ch01 Questions#EUP 1.26|EUP 1.26]]

> [!solution] 答案
> $$
> \frac{15\ \mathrm{L}}{\mathrm{min}}\left(\frac{1000\ \mathrm{cm^3}}{1\ \mathrm{L}}\right)\left(\frac{1\ \mathrm{min}}{60\ \mathrm{s}}\right) = 2.5 \times 10^{2}\ \mathrm{cm^3/s}
> $$
> 再乘 $\left(\dfrac{1\ \mathrm{m}}{100\ \mathrm{cm}}\right)^{3} = 10^{-6}$：$2.5 \times 10^{-4}\ \mathrm{m^3/s}$。

### EUP 1.67
題目：[[PHY1 HW Ch01 Questions#EUP 1.67|EUP 1.67]]

> [!solution] 答案
> 一年（2017 不是閏年）$= 365 \times 86{,}400\ \mathrm{s} = 3.154 \times 10^{7}\ \mathrm{s}$。平均發電功率
> $$
> P = \frac{E}{t} = \frac{(3849\ \mathrm{kWh})(3.6 \times 10^{6}\ \mathrm{J/kWh})}{3.154 \times 10^{7}\ \mathrm{s}} = 439\ \mathrm{W} > 392\ \mathrm{W}
> $$
> 房子發的電比用的多。

## 加選：弧度與弧長

### EUP 1.17
題目：[[PHY1 HW Ch01 Questions#EUP 1.17|EUP 1.17]]

> [!solution] 答案
> $$
> \theta = \frac{s}{r} = \frac{2.1\ \mathrm{km}}{3.6\ \mathrm{km}} = 0.58\ \mathrm{rad} = (0.58\ \mathrm{rad})\left(\frac{180^{\circ}}{\pi\ \mathrm{rad}}\right) = 33^{\circ}
> $$

## 加選：科學記號

### EUP 1.31
題目：[[PHY1 HW Ch01 Questions#EUP 1.31|EUP 1.31]]

> [!solution] 答案
> $0.57\ \mathrm{ms} = 0.57 \times 10^{-3}\ \mathrm{s}$：
> $$
> \frac{4.2 \times 10^{3}\ \mathrm{m/s}}{0.57 \times 10^{-3}\ \mathrm{s}} = 7.37 \times 10^{6}\ \mathrm{m/s^2} = 7.4 \times 10^{6}\ \mathrm{m/s^2}
> $$

> [!warning] ms 是毫秒
> $\mathrm{ms}$ 是 millisecond（$10^{-3}\ \mathrm{s}$），不是 $\mathrm{m/s}$。

### EUP 1.32
題目：[[PHY1 HW Ch01 Questions#EUP 1.32|EUP 1.32]]

> [!solution] 答案
> 先換成公尺：$5.1 \times 10^{-2}\ \mathrm{cm} = 0.00051\ \mathrm{m}$，$6.8 \times 10^{3}\ \mathrm{\mu m} = 0.0068\ \mathrm{m}$。相加取到 $0.0001\ \mathrm{m}$ 位：
> $$
> 0.00051\ \mathrm{m} + 0.0068\ \mathrm{m} = 0.0073\ \mathrm{m}
> $$
> 再乘（兩位有效數字）：
> $$
> (7.3 \times 10^{-3}\ \mathrm{m})(1.8 \times 10^{4}\ \mathrm{N}) = 1.3 \times 10^{2}\ \mathrm{N \cdot m}
> $$

> [!warning] 單位不同不能直接相加
> $5.1 \times 10^{-2}$ 和 $6.8 \times 10^{3}$ 的單位不同（cm 和 µm），要先換成同一單位才能比次方、相加。

### EUP 1.33
題目：[[PHY1 HW Ch01 Questions#EUP 1.33|EUP 1.33]]

> [!solution] 答案
> 把次方湊成 3 的倍數：
> $$
> (1.25 \times 10^{23})^{1/3} = (125 \times 10^{21})^{1/3} = 125^{1/3} \times 10^{21/3} = 5.00 \times 10^{7}
> $$

## 加選：有效數字

### EUP 1.35 and 1.36
題目：[[PHY1 HW Ch01 Questions#EUP 1.35 and 1.36|EUP 1.35 and 1.36]]

> [!solution] 答案
> 加法取最少的小數點後位數。天線長 $0.036\ \mathrm{m}$。
> - **35.** $41\ \mathrm{m} + 0.036\ \mathrm{m} = 41.036\ \mathrm{m} \to 41\ \mathrm{m}$（$41$ 只準到公尺，天線長度看不出來）。
> - **36.** $41.05\ \mathrm{m} + 0.036\ \mathrm{m} = 41.086\ \mathrm{m} \to 41.09\ \mathrm{m}$。

### EUP 1.44
題目：[[PHY1 HW Ch01 Questions#EUP 1.44|EUP 1.44]]

> [!solution] 答案
> $21\ \mathrm{min} = (21\ \mathrm{min})(1\ \mathrm{h}/60\ \mathrm{min}) = 0.35\ \mathrm{h}$。減法取到小數點後兩位：
> $$
> 12.404\ \mathrm{h} - 0.35\ \mathrm{h} = 12.054\ \mathrm{h} \to 12.05\ \mathrm{h}
> $$

### EUP 1.45
題目：[[PHY1 HW Ch01 Questions#EUP 1.45|EUP 1.45]]

> [!solution] 答案
> - (a) $\sqrt{2} \approx 1.41$，$1.41^{5} = 5.573 \to 5.57$。
> - (b) $\sqrt{2} \approx 1.414$，$1.414^{5} = 5.653 \to 5.65$。
>
> 精確值 $(\sqrt{2})^{5} = 4\sqrt{2} = 5.657 \to 5.66$：(a) 差了 $0.09$，(b) 只差最後一位。中間值的進位誤差經過五次方會放大。

### EUP 1.57
題目：[[PHY1 HW Ch01 Questions#EUP 1.57|EUP 1.57]]

> [!solution] 答案
> 準到三位有效數字，表示不確定度約為末位的一半，$\pm 0.005$：
> $$
> \frac{0.005}{1.27} = 0.4\%, \qquad \frac{0.005}{9.97} = 0.05\%
> $$
> 兩個數有效數字位數相同，但 $1.27$ 的百分比不確定度約是 $9.97$ 的 8 倍。

> [!warning] 不確定度的取法
> 若把不確定度取為末位的 $\pm 1$（$\pm 0.01$），得到 $0.8\%$ 與 $0.1\%$；比值一樣是約 8 倍。

### EUP 1.65
題目：[[PHY1 HW Ch01 Questions#EUP 1.65|EUP 1.65]]

> [!solution] 答案
> 先把 mm 換成 m。
> - (a) $1.0\ \mathrm{m} + 0.009\ \mathrm{m} = 1.009\ \mathrm{m} \to 1.0\ \mathrm{m}$（取到小數點後一位）。
> - (b) $(1.0\ \mathrm{m})(0.001\ \mathrm{m}) = 1 \times 10^{-3}\ \mathrm{m^2}$（$1\ \mathrm{mm}$ 只有一位有效數字）。
> - (c) $1.0\ \mathrm{m} - 0.998\ \mathrm{m} = 0.002\ \mathrm{m} \to 0.0\ \mathrm{m}$（取到小數點後一位，差值在精確度以下）。
> - (d) $1.0\ \mathrm{m}/0.998\ \mathrm{m} = 1.002 \to 1.0$（沒有單位）。

## 加選：估計

### EUP 1.53
題目：[[PHY1 HW Ch01 Questions#EUP 1.53|EUP 1.53]]

> [!solution] 答案
> 把泡泡攤成面積 $4\pi r^{2}$、厚度 $t$ 的薄片，$m = \rho(4\pi r^{2})t$，$r = 5\ \mathrm{cm}$：
> $$
> t = \frac{m}{4\pi r^{2}\rho} = \frac{7\ \mathrm{g}}{4\pi(5\ \mathrm{cm})^{2}(1\ \mathrm{g/cm^3})} = 0.02\ \mathrm{cm} = 0.2\ \mathrm{mm}
> $$

### EUP 1.55
題目：[[PHY1 HW Ch01 Questions#EUP 1.55|EUP 1.55]]

> [!solution] 答案
> - (a) $10^{10}$ 個正方形排成 $10^{5} \times 10^{5}$：每個邊長 $\dfrac{4\ \mathrm{mm}}{10^{5}} = 4 \times 10^{-8}\ \mathrm{m} = 40\ \mathrm{nm}$。
> - (b) 一次計算脈衝走的距離 $(10^{4})(10^{6})(4 \times 10^{-8}\ \mathrm{m}) = 400\ \mathrm{m}$，速率 $\tfrac{2}{3}c = 2 \times 10^{8}\ \mathrm{m/s}$：
> $$
> t = \frac{400\ \mathrm{m}}{2 \times 10^{8}\ \mathrm{m/s}} = 2 \times 10^{-6}\ \mathrm{s} \implies \frac{1}{t} = 5 \times 10^{5}\ \text{次/s}
> $$

### EUP 1.66
題目：[[PHY1 HW Ch01 Questions#EUP 1.66|EUP 1.66]]

> [!solution] 答案
> 晶片面積除以一個元件的面積，得最多能放的元件數：
> $$
> N_{\max} = \frac{(5 \times 10^{-3}\ \mathrm{m})^{2}}{(32 \times 10^{-9}\ \mathrm{m})^{2}} = 2.4 \times 10^{10} > 1 \times 10^{10}
> $$
> 店員說得對（100 億個佔不到晶片面積的一半）。

## 加選：數據找直線

### EUP 1.69
題目：[[PHY1 HW Ch01 Questions#EUP 1.69|EUP 1.69]]

> [!solution] 答案
> (a) $m \propto V = \tfrac{4}{3}\pi(d/2)^{3} = \tfrac{\pi}{6}d^{3}$，所以畫 $m$ 對 $d^{3}$。
>
> | $d^{3}$ ($\mathrm{cm^3}$) | $0.422$ | $1.00$ | $3.65$ | $10.1$ | $16.4$ |
> | --- | --- | --- | --- | --- | --- |
> | $m$ ($\mathrm{g}$) | $1.81$ | $3.95$ | $15.8$ | $38.6$ | $68.2$ |
>
> (b) 過原點的最佳擬合直線斜率 $\approx 4.1\ \mathrm{g/cm^3}$。由 $m = \rho\,\tfrac{\pi}{6}d^{3}$，密度 $\rho = \dfrac{6}{\pi}(4.1\ \mathrm{g/cm^3}) \approx 7.8\ \mathrm{g/cm^3}$，正是鋼的密度。
>
> ![EUP 1.69 fit|480](../Attachments/PHY1%20Ch01%20Problem%201.69%20fit.png)

## 加選：數量級（Passage Problems）

### EUP 1.70 to 1.73
題目：[[PHY1 HW Ch01 Questions#EUP 1.70 to 1.73|EUP 1.70 to 1.73]]

> [!solution] 答案
> 把細胞和原子都當成立方體：細胞 $(10^{-5}\ \mathrm{m})^{3} = 10^{-15}\ \mathrm{m^3}$，原子 $(10^{-10}\ \mathrm{m})^{3} = 10^{-30}\ \mathrm{m^3}$。
> - **70.** a. 每個細胞約 $10^{-15}/10^{-30} = 10^{15}$ 個原子，多於 $10^{14}$ 個細胞。
> - **71.** b. $10^{-15}\ \mathrm{m^3}$。
> - **72.** b. 細胞大多是水：$(10^{3}\ \mathrm{kg/m^3})(10^{-15}\ \mathrm{m^3}) = 10^{-12}\ \mathrm{kg}$。
> - **73.** c. $(10^{14})(10^{15}) = 10^{29}$，最接近 $10^{30}$。

## 外校考題：觀念題

### KSUS 1.3 and 1.4
題目：[[PHY1 HW Ch01 Questions#KSUS 1.3 and 1.4|KSUS 1.3 and 1.4]]

> [!solution] 答案
> - **3.** d. 全換成 kg：a. $25\ \mathrm{kg}$；b. $2.5\ \mathrm{g} = 2.5 \times 10^{-3}\ \mathrm{kg}$；c. $25\ \mathrm{mg} = 2.5 \times 10^{-5}\ \mathrm{kg}$；d. $0.0025 \times 10^{9}\ \mathrm{g} = 2.5 \times 10^{3}\ \mathrm{kg}$。
> - **4.** c. 全換成 cm：a. $40.6\ \mathrm{cm}$；b. $38.1\ \mathrm{cm}$；c. $45.0\ \mathrm{cm}$；d. $30.48\ \mathrm{cm}$。

### SIU 1.1
題目：[[PHY1 HW Ch01 Questions#SIU 1.1|SIU 1.1]]

> [!solution] 答案
> 相加的每一項因次必須相同，所以 $[Ct] = [B] = L$，$[C] = L/T$（速度的因次）。

## 外校考題：計算題

### KSUS 1.1 and 1.2
題目：[[PHY1 HW Ch01 Questions#KSUS 1.1 and 1.2|KSUS 1.1 and 1.2]]

> [!solution] 答案
> $$
> \begin{aligned}
> \text{1.}\quad 2.4 \times 10^{-5}\ \mathrm{kg} &= (2.4 \times 10^{-5}\ \mathrm{kg})\left(\frac{10^{3}\ \mathrm{g}}{1\ \mathrm{kg}}\right)\left(\frac{10^{3}\ \mathrm{mg}}{1\ \mathrm{g}}\right) = 24\ \mathrm{mg} \\
> \text{2.}\quad 9.57 \times 10^{5}\ \mathrm{s} &= (9.57 \times 10^{5}\ \mathrm{s})\left(\frac{1\ \mathrm{h}}{3600\ \mathrm{s}}\right)\left(\frac{1\ \mathrm{day}}{24\ \mathrm{h}}\right) = 11.1\ \text{天}
> \end{aligned}
> $$

### KSUS 1.5 and 1.6
題目：[[PHY1 HW Ch01 Questions#KSUS 1.5 and 1.6|KSUS 1.5 and 1.6]]

> [!solution] 答案
> - **5.** 乘法取最少的兩位有效數字：$(42\ \mathrm{m/s})(21.256\ \mathrm{s}) = 892.75\ \mathrm{m} \to 8.9 \times 10^{2}\ \mathrm{m}$。
> - **6.** 先換成 kg：$27.8\ \mathrm{g} = 0.0278\ \mathrm{kg}$。加法取到 $0.01\ \mathrm{kg}$ 位：$2.50 + 0.25 + 0.0278 = 2.7778\ \mathrm{kg} \to 2.78\ \mathrm{kg}$。
