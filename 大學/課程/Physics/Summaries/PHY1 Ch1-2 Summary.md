%% unit-summary v1.1 · Wolfson, Essential University Physics 4e (Global Edition), Vol. 1, Ch. 1–2, pp. 17–49 · 2026-10-05 · draft, not calibrated for physics yet %%

# Chapter 1 Doing Physics

## 1.1 Realms of Physics

mechanics · oscillations, waves, and fluids · thermodynamics · electromagnetism · optics · modern physics (relativity, quantum physics)

## 1.2 Measurements and Units

SI base units (seven)

length: meter (m) · time: second (s) · mass: kilogram (kg) · electric current: ampere (A) · temperature: kelvin (K) · amount of substance: mole (mol) · luminosity: candela (cd)

Angle: radian (rad), $\theta = \dfrac{s}{r}$ (arc length / radius); solid angle: steradian (sr). All other units are derived from the base units.

Explicit-constant definitions (2019): a unit is fixed by giving a constant of nature an **exact** value
- second: cesium frequency $\Delta\nu_{\mathrm{Cs}} = 9\,192\,631\,770\ \mathrm{Hz}$ ($\mathrm{Hz} = \mathrm{s^{-1}}$)
- meter: $c = 299\,792\,458\ \mathrm{m/s}$
- kilogram: Planck constant $h = 6.626\,070\,15 \times 10^{-34}\ \mathrm{J \cdot s}$ ($\mathrm{J \cdot s} = \mathrm{kg \cdot m^2 \cdot s^{-1}}$)

> - m depends on s; kg depends on m and s
> - operational definition (a laboratory procedure anyone can reproduce) replaces artifacts (the prototype kilogram, 1889–2019)
> - the book prints $h = 6.626\,070\,040 \times 10^{-34}$, the older measured value; the exact SI value is $6.626\,070\,15 \times 10^{-34}$

SI prefixes (Table 1.1)

$$
\begin{array}{llllllllll}
\mathrm{Y}\ 10^{24} & \mathrm{Z}\ 10^{21} & \mathrm{E}\ 10^{18} & \mathrm{P}\ 10^{15} & \mathrm{T}\ 10^{12} & \mathrm{G}\ 10^{9} & \mathrm{M}\ 10^{6} & \mathrm{k}\ 10^{3} & \mathrm{h}\ 10^{2} & \mathrm{da}\ 10^{1} \\
\mathrm{d}\ 10^{-1} & \mathrm{c}\ 10^{-2} & \mathrm{m}\ 10^{-3} & \mu\ 10^{-6} & \mathrm{n}\ 10^{-9} & \mathrm{p}\ 10^{-12} & \mathrm{f}\ 10^{-15} & \mathrm{a}\ 10^{-18} & \mathrm{z}\ 10^{-21} & \mathrm{y}\ 10^{-24}
\end{array}
$$

Unit symbols: lowercase, uppercase when named after a person (N), and L for liter; product $\mathrm{N \cdot m}$; quotient $\mathrm{m/s}$ or $\mathrm{m \cdot s^{-1}}$

Changing units: multiply by a ratio equal to 1 and cancel units along the chain
- ex. $(2722\ \mathrm{ft})\left(\dfrac{0.3048\ \mathrm{m}}{1\ \mathrm{ft}}\right) = 829.7\ \mathrm{m}$
- ex. $65\ \mathrm{km/h} = \left(\dfrac{65\ \mathrm{km}}{\mathrm{h}}\right)\left(\dfrac{1000\ \mathrm{m}}{1\ \mathrm{km}}\right)\left(\dfrac{1\ \mathrm{h}}{3600\ \mathrm{s}}\right) = 18\ \mathrm{m/s}$

> a numerical answer cannot be correct without the **right units**

## 1.3 Working with Numbers

Scientific notation: $4185 = 4.185 \times 10^{3}$, $0.00012 = 1.2 \times 10^{-4}$

Tactics 1.1
- add / subtract: give both the same exponent first: $3.75 \times 10^{6} + 5.2 \times 10^{5} = 3.75 \times 10^{6} + 0.52 \times 10^{6} = 4.27 \times 10^{6}$
- multiply / divide: multiply (divide) the digits, add (subtract) the exponents
- powers / roots: digits to the power, exponent times the power (ex. $\sqrt{29.4 \times 10^{3}} = \sqrt{2.94 \times 10^{4}} = 1.7 \times 10^{2}$: make the exponent even first)

Significant figures
- $\times$ $\div$: the answer has as many significant figures as the **least precise** quantity
- $+$ $-$: the answer has as many digits to the right of the decimal point as the term with the **fewest**

> - calculating cannot add precision: $2\pi R_{\mathrm{E}}$ with $R_{\mathrm{E}} = 6.37 \times 10^{6}\ \mathrm{m}$ has three significant figures however many digits of $\pi$ are used
> - subtraction loses precision: $3.249\ \mathrm{m} - 3.241\ \mathrm{m} = 0.008\ \mathrm{m}$, one significant figure ($8\ \mathrm{mm}$, not $8.000\ \mathrm{mm}$)
> - intermediate results: keep at least one extra figure, round only the final answer
> - whole numbers ending in zero: $60$, $300$ have one significant figure, $410$ has two; write $6.0 \times 10^{1}$, $3.00 \times 10^{2}$, $4.10 \times 10^{2}$

Working with data: plot against the quantity that makes the relation a straight line, draw a best-fit line, read the physics from the slope
- ex. falling ball, $y \propto t^{2}$: plot $y$ versus $t^{2}$; slope $= 5.0\ \mathrm{m/s^2} = \tfrac{1}{2}g$ ⇒ $g \approx 10\ \mathrm{m/s^2}$

Estimation: a rough size, one significant figure, powers of 10
- ex. brain: $(10\ \mathrm{cm})^{3} = 10^{-3}\ \mathrm{m^3}$ of water ⇒ about $1\ \mathrm{kg}$; cell $(10^{-5}\ \mathrm{m})^{3} = 10^{-15}\ \mathrm{m^3}$ ⇒ $N = \dfrac{10^{-3}}{10^{-15}} = 10^{12}$ cells

## 1.4 Strategies for Learning Physics

Problem-Solving Strategy 1.1 (IDEA)
- **Interpret**: what is asked; which concepts and principles apply; which objects are the players
- **Develop**: draw a diagram and label it; pick the equations that contain the givens and the unknowns
- **Evaluate**: solve in symbols first, put in the numbers at the end
- **Assess**: units correct? numbers reasonable? special cases (a quantity zero or infinite) behave?

# Chapter 2 Motion in a Straight Line

Kinematics: the study of motion without regard to its cause. position → (rate of change) → velocity → (rate of change) → acceleration

## 2.1 Average Motion

displacement: $\Delta x = x_{2} - x_{1}$ (net change in position)

$$
\bar{v} = \frac{\Delta x}{\Delta t} \qquad \text{(average velocity)} \tag{2.1}
$$

average speed $= \dfrac{\text{total distance}}{\text{time}}$

> - average speed ≠ $\lvert \bar{v} \rvert$ in general: $\bar{v}$ depends only on $\Delta x$ and $\Delta t$, not on the route
> - equal only when the motion never reverses direction
> - coordinate system: origin and positive direction are **your choice**; the sign of $\Delta x$, $\bar{v}$ is the direction

- ex. pizza round trip, $10\ \mathrm{km}$ each way in $30\ \mathrm{min}$: $\bar{v} = 0$, average speed $40\ \mathrm{km/h}$
- ex. $1000\ \mathrm{km}$ north via a stop $700\ \mathrm{km}$ beyond, $4.0\ \mathrm{h}$: $\bar{v} = 250\ \mathrm{km/h}$, average speed $\dfrac{2400\ \mathrm{km}}{4.0\ \mathrm{h}} = 600\ \mathrm{km/h}$

## 2.2 Instantaneous Velocity

$$
v = \lim_{\Delta t \to 0} \frac{\Delta x}{\Delta t} = \frac{dx}{dt} \qquad \text{(instantaneous velocity)} \tag{2.2}
$$

instantaneous speed $= \lvert v \rvert$

> - $\bar{v}$ = slope of the line through two points of the $x$–$t$ graph; $v$ = slope of the **tangent** line
> - "at" a time ⇒ instantaneous; "over" an interval ⇒ average

Tactics 2.1: $x = bt^{n}$ ⇒ $\dfrac{dx}{dt} = nbt^{n-1}$ (2.3)

- ex. rocket $x = bt^{2}$: $v = 2bt$, and from $0$ to $t$: $\bar{v} = \dfrac{bt^{2}}{t} = bt = \tfrac{1}{2}v$

## 2.3 Acceleration

$$
\bar{a} = \frac{\Delta v}{\Delta t} \quad (2.4) \qquad\qquad a = \lim_{\Delta t \to 0} \frac{\Delta v}{\Delta t} = \frac{dv}{dt} \quad (2.5) \qquad\qquad a = \frac{d}{dt}\left(\frac{dx}{dt}\right) = \frac{d^{2}x}{dt^{2}} \quad (2.6)
$$

SI unit: $\mathrm{m/s^2}$

> - $a$ in the direction of $v$: speeds up; $a$ opposite to $v$: slows (one dimension)
> - $v$ = slope of $x$–$t$; $a$ = slope of $v$–$t$
> - $x$ at a maximum ⇒ $v = 0$; $v$ at a peak ⇒ $a = 0$
> - $v = 0$ ⇏ $a = 0$, ex. ball at the peak of its flight: $v = 0$, $a = -9.8\ \mathrm{m/s^2}$

## 2.4 Constant Acceleration

Table 2.1 Equations of Motion for Constant Acceleration

$$
\begin{array}{lll}
v = v_{0} + at & v,\ a,\ t;\ \text{no } x & (2.7) \\[2pt]
x = x_{0} + \tfrac{1}{2}(v_{0} + v)t & x,\ v,\ t;\ \text{no } a & (2.9) \\[2pt]
x = x_{0} + v_{0}t + \tfrac{1}{2}at^{2} & x,\ a,\ t;\ \text{no } v & (2.10) \\[2pt]
v^{2} = v_{0}^{2} + 2a(x - x_{0}) & x,\ v,\ a;\ \text{no } t & (2.11)
\end{array}
$$

$\bar{v} = \tfrac{1}{2}(v_{0} + v)$ (2.8)

> - **only for constant acceleration** (2.8 too)
> - $x_{0}$, $v_{0}$: position and velocity at $t = 0$
> - $a$ opposite to $v$ ⇒ opposite signs (braking with $v > 0$: $a < 0$)
> - mixed units ⇒ convert to SI first ($270\ \mathrm{km/h} = 75\ \mathrm{m/s}$)

Problem-Solving Strategy 2.1: is $a$ constant? → which object? → diagram, coordinate system → the equation of Table 2.1 that contains the givens and the unknown → symbols first → assess

- ex. landing at $270\ \mathrm{km/h}$, $a = -4.5\ \mathrm{m/s^2}$, $v = 0$: $\Delta x = \dfrac{-v_{0}^{2}}{2a} = 625\ \mathrm{m}$
- ex. two objects, same origin and same $t = 0$: speeder $x_{\mathrm{s}} = v_{\mathrm{s0}}t$, police $x_{\mathrm{p}} = \tfrac{1}{2}a_{\mathrm{p}}t^{2}$; equal ⇒ $t = 0$ or $t = \dfrac{2v_{\mathrm{s0}}}{a_{\mathrm{p}}}$; then $v_{\mathrm{p}} = 2v_{\mathrm{s0}}$

## 2.5 The Acceleration of Gravity

free fall: motion under the influence of **gravity alone** ⇒ constant acceleration, the same for all objects; $g \approx 9.8\ \mathrm{m/s^2}$ near Earth's surface

Upward positive, $y$ vertical ⇒ $a = -g$:

$$
v = v_{0} - gt \qquad y = y_{0} + v_{0}t - \tfrac{1}{2}gt^{2} \qquad v^{2} = v_{0}^{2} - 2g(y - y_{0})
$$

> - $g$ is a magnitude (positive); the sign comes from the coordinate system
> - $a = -g$ going up, at the peak, and coming down
> - air resistance present ⇒ not free fall
> - an object thrown up returns to its initial height with the same speed
> - multiple answers: think what each one means before discarding it

- ex. drop from $10\ \mathrm{m}$ ($v_{0} = 0$): $\lvert v \rvert = \sqrt{-2g(y - y_{0})} = 14\ \mathrm{m/s}$ ($v = -14\ \mathrm{m/s}$), $t = \dfrac{v_{0} - v}{g} = 1.4\ \mathrm{s}$
- ex. toss up at $7.3\ \mathrm{m/s}$ from $y_{0} = 1.5\ \mathrm{m}$: floor at $t = \dfrac{v_{0} \pm \sqrt{v_{0}^{2} + 2y_{0}g}}{g} = 1.7\ \mathrm{s}$ (or $-0.18\ \mathrm{s}$: when it would have been at the floor earlier); peak $y = y_{0} + \dfrac{v_{0}^{2}}{2g} = 4.2\ \mathrm{m}$; back at $1.5\ \mathrm{m}$: $v = \pm 7.3\ \mathrm{m/s}$

## 2.6 When Acceleration Isn't Constant

Table 2.1 does not apply.

$$
v(t) = \int a(t)\,dt \quad (2.12) \qquad\qquad x(t) = \int v(t)\,dt \quad (2.13)
$$

> - plus the **initial conditions** (the values at $t = 0$): they are the constants of integration
> - constant $a$: $\int a\,dt = v_{0} + at$, $\int (v_{0} + at)\,dt = x_{0} + v_{0}t + \tfrac{1}{2}at^{2}$, i.e. (2.7) and (2.10)

# Problem Types 題型

範圍：Wolfson Ch. 1–2 的 Exercises、Problems、Passage Problems（For Thought and Discussion 另列）。題號寫成「章.題」，例如 2.53。答案都用 Python 重算過。這份還沒有你的 quiz 或老師的重點可以參考，所以「題數」欄是課本習題的分布，不是考題頻率。

## Chapter 1

| # | 題型 | 怎麼認 | 做法 | 課本題數 |
| --- | --- | --- | --- | --- |
| 1 | Unit conversion | 「express in …」「how many … in …」、SI prefix | 乘上等於 1 的 conversion factor，單位一路約掉 | 24 |
| 2 | Radian 與 arc length | arc、radius、angle | $\theta = s/r$（rad） | 3 |
| 3 | Scientific notation 運算 | add / divide / root 加上 $10^{n}$ | 先同單位、同指數；開根號前把指數調成可整除 | 5 |
| 4 | Significant figures | 「what do you report」「how would you report」 | $\times$ $\div$ 看有效位數；$+$ $-$ 看小數位 | 9 |
| 5 | Estimation | 「estimate」「roughly」「order of magnitude」 | 簡化形狀、1 位有效數字、用 10 的次方算 | 21 |
| 6 | Data 找直線 | DATA 表格 | 選橫軸讓關係變直線，從 slope 讀物理量 | 1 |

判斷順序：先把所有量換成同一組單位 → 再算 → 最後才依 significant figures 進位。

### 題型 1：Unit conversion

寫出每個 conversion factor（分子分母相等），讓不要的單位上下約掉。課本題：1.11–1.15、1.18–1.26、1.28、1.29、1.37–1.40、1.59、1.60、1.67、1.68。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| $15\ \mathrm{L/min}$ 換成 $\mathrm{cm^3/s}$、$\mathrm{m^3/s}$ | 1.26 | $2.5 \times 10^{2}\ \mathrm{cm^3/s} = 2.5 \times 10^{-4}\ \mathrm{m^3/s}$ |
| $65\ \mathrm{km/h}$ 換成 $\mathrm{m/s}$ | Example 1.1 | $18\ \mathrm{m/s}$ |
| $3849\ \mathrm{kWh}$ 一年的平均功率 | 1.67 | $439\ \mathrm{W}$ |

陷阱
- 面積、體積的換算要把 factor 平方、立方：$1\ \mathrm{m^3} = 10^{6}\ \mathrm{cm^3}$，不是 $10^{2}$（1.21）。
- $\mathrm{km/h} \to \mathrm{m/s}$ 是除以 $3.6$，不是乘。
- 題目混用單位（$\mathrm{cm}$ 與 $\mathrm{\mu m}$、$\mathrm{h}$ 與 $\mathrm{min}$）時，先換成同一個再加減。

### 題型 2：Radian 與 arc length

$\theta = s/r$ 得到的是 rad；要 degree 再乘 $180^{\circ}/\pi$。課本題：1.16、1.17、1.27。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| 沿半徑 $3.6\ \mathrm{km}$ 的圓弧飛 $2.1\ \mathrm{km}$，轉了幾度 | 1.17 | $0.58\ \mathrm{rad} = 33^{\circ}$ |

陷阱：$s$ 和 $r$ 要同單位（1.16 是 $\mathrm{cm}$，1.17 是 $\mathrm{km}$）。

### 題型 3：Scientific notation 運算

課本題：1.30–1.34。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| $5.1 \times 10^{-2}\ \mathrm{cm} + 6.8 \times 10^{3}\ \mathrm{\mu m}$，再乘 $1.8 \times 10^{4}\ \mathrm{N}$ | 1.32 | $1.3 \times 10^{2}\ \mathrm{N \cdot m}$ |
| $\sqrt[3]{1.25 \times 10^{23}}$，不用計算機 | 1.33 | $5 \times 10^{7}$ |

陷阱：開 $n$ 次方根前，先把指數調成 $n$ 的倍數（$1.25 \times 10^{23} = 125 \times 10^{21}$）。

### 題型 4：Significant figures

課本題：1.35、1.36、1.41–1.45、1.57、1.65。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| $41\ \mathrm{m} + 3.6\ \mathrm{cm}$；$41.05\ \mathrm{m} + 3.6\ \mathrm{cm}$ | 1.35、1.36 | $41\ \mathrm{m}$；$41.09\ \mathrm{m}$ |
| $12.404\ \mathrm{h} - 21\ \mathrm{min}$ | 1.44 | $12.05\ \mathrm{h}$ |
| $1.0\ \mathrm{m} - 998\ \mathrm{mm}$ | 1.65 (c) | $0.0\ \mathrm{m}$ |
| $(\sqrt{2})^{5}$，中間先進位到 3 位或 4 位 | 1.45 | $5.57$；$5.65$（正確值 $5.66$） |

陷阱
- 加減法看的是小數位，不是有效位數；相近的數相減會掉很多位（Example 1.3、1.65 (c)）。
- 中間結果至少多留一位，最後才進位（1.45）。
- $60$、$300$ 這種結尾是 $0$ 的整數只有 1 位有效數字。

### 題型 5：Estimation

課本題：1.46–1.56、1.58、1.61–1.64、1.66、1.70–1.73。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| $7\ \mathrm{g}$ 的口香糖吹成直徑 $10\ \mathrm{cm}$ 的泡泡，厚度 | 1.53 | 約 $0.2\ \mathrm{mm}$ |
| $4\ \mathrm{mm}$ 見方的 chip 上有 $10^{10}$ 個元件，每個多大；每秒可做幾次計算 | 1.55 | $40\ \mathrm{nm}$；$5 \times 10^{5}$ 次 |
| 腦的質量與細胞數 | Example 1.5 | $1\ \mathrm{kg}$；$10^{12}$ |

陷阱：答案只給 1 位有效數字或 10 的次方就好；寫 $1.16 \times 10^{6}\ \mathrm{kg}$ 這種估計值是假的精確（For Thought and Discussion 1.10）。

### 題型 6：Data 找直線

課本題：1.69，以及 Example 1.4。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| 鋼球的 mass 對什麼作圖會是直線，slope 是多少 | 1.69 | 對 $d^{3}$；slope $\approx 4.1\ \mathrm{g/cm^3}$，密度 $\approx 7.8\ \mathrm{g/cm^3}$ |

陷阱：slope 不一定就是要的物理量（1.69 的 slope 是 $\pi\rho/6$；Example 1.4 的 slope 是 $\tfrac{1}{2}g$）。

## Chapter 2

| # | 題型 | 怎麼認 | 做法 | 課本題數 |
| --- | --- | --- | --- | --- |
| 1 | Average velocity、average speed | 「average」加上分段行程 | $\bar{v} = \Delta x/\Delta t$；speed 用 total distance | 11 |
| 2 | 由 $x(t)$ 求 $v$、$a$ | 給了 $x(t)$ 的式子 | 微分：$v = dx/dt$，$a = dv/dt$ | 4 |
| 3 | Average acceleration | 兩個速度與一段時間 | $\bar{a} = \Delta v/\Delta t$ | 6 |
| 4 | Constant acceleration，一個物體 | 「constant acceleration」「brakes」「comes to a stop」 | 列出 $x - x_{0}$、$v_{0}$、$v$、$a$、$t$，用 Table 2.1 中不含「沒給也沒問」那個量的式子 | 24 |
| 5 | Constant acceleration，兩個物體 | 兩台車、「catch up」「collide」 | 同一個 origin 與 $t = 0$，各寫 $x(t)$ 再令相等；或改用 relative motion | 5 |
| 6 | Free fall，一個物體 | 「drops」「thrown straight up」 | $y$ 向上為正、$a = -g$，套 Table 2.1 | 24 |
| 7 | Free fall，兩個物體 | 兩顆球、同時丟 | 兩個 $y(t)$ 相減，$\tfrac{1}{2}gt^{2}$ 抵消，相對運動是等速 | 5 |
| 8 | Nonconstant acceleration | $a(t)$ 或 $v(t)$ 是 $t$ 的函數 | 積分，再用 initial conditions 定常數 | 5 |
| 9 | 讀圖 | $x$–$t$、$v$–$t$ 圖 | $v$ 是 $x$–$t$ 的 slope；$a$ 是 $v$–$t$ 的 slope | 7 |
| 10 | Data 找直線 | DATA 表格 | 從靜止出發：$x$ 對 $t^{2}$，slope $= \tfrac{1}{2}a$ | 1 |

判斷順序：先定正方向 → $a$ 是不是 constant？不是就微分或積分（題型 2、8）→ 是的話看有幾個物體 → 一個：選 Table 2.1 的式子；兩個：各寫 $x(t)$ 令相等。

### 題型 1：Average velocity、average speed

課本題：2.11–2.16、2.49–2.52、2.83。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| 往北 $24\ \mathrm{km}$ 花 $2.5\ \mathrm{h}$，回家花 $1.5\ \mathrm{h}$ | 2.13 | 去程 $+9.6\ \mathrm{km/h}$，回程 $-16\ \mathrm{km/h}$，全程 $0$ |
| 一半時間 $v_{1}$、一半時間 $v_{2}$；一半距離 $v_{1}$、一半距離 $v_{2}$ | 2.83 | $\tfrac{1}{2}(v_{1} + v_{2})$；$\dfrac{2v_{1}v_{2}}{v_{1} + v_{2}}$ |
| 兩架飛機相向，$10\,886\ \mathrm{km}$，$1040$ 與 $765\ \mathrm{km/h}$ | 2.52 | $6.03\ \mathrm{h}$ 後，離 London $6.27 \times 10^{3}\ \mathrm{km}$ |

陷阱
- average velocity 只看頭尾位置；來回一趟是 $0$，但 average speed 不是。
- 「速度的平均」只有在兩段時間相等時才等於 average speed；兩段距離相等時不是（2.83、For Thought and Discussion 2.9、2.10）。

### 題型 2：由 $x(t)$ 求 $v$、$a$

課本題：2.19、2.53、2.54、2.84。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| $x = bt + ct^{3}$，區間縮小時的 $\bar{v}$ 與 $t = 2\ \mathrm{s}$ 的 $v$ | 2.53 | $9.82$、$9.34$、$9.18\ \mathrm{m/s}$；$v = 9.18\ \mathrm{m/s}$ |
| $x = bt^{2}$ 的 $v$ 與 $\bar{v}$ | Example 2.2 | $v = 2bt$，$\bar{v} = bt$ |

陷阱：「at」某個時刻是 instantaneous，「over」一段時間是 average；兩個不要混用。

### 題型 3：Average acceleration

課本題：2.20–2.25。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| 從靜止加速到 $25\ \mathrm{m/s}$ 再煞車，$48\ \mathrm{s}$ 後是 $18\ \mathrm{m/s}$ | 2.21 | $0.38\ \mathrm{m/s^2}$ |

陷阱：只看頭尾速度；2.21 的 $25\ \mathrm{m/s}$ 是多給的。速度是 $\mathrm{km/h}$ 時先換成 $\mathrm{m/s}$（2.20、2.24、2.25）。

### 題型 4：Constant acceleration，一個物體

課本題：2.26–2.34、2.41–2.44、2.56、2.57、2.61–2.67、2.80、2.87。其中 2.27、2.56 是推導題。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| 以 $6.3\ \mathrm{m/s^2}$ 煞車 $34\ \mathrm{m}$ 後以 $18\ \mathrm{km/h}$ 撞上 | 2.66 | 初速 $21\ \mathrm{m/s}$（$77\ \mathrm{km/h}$），$2.6\ \mathrm{s}$ |
| $270\ \mathrm{km/h}$ 落地，以 $4.5\ \mathrm{m/s^2}$ 減速，最短跑道 | Example 2.3 | $625\ \mathrm{m}$ |

陷阱
- 減速時 $a$ 與 $v$ 異號；把 $a$ 當正的代進 (2.11) 會得到負數開根號。
- Table 2.1 只適用於 constant acceleration。
- 2.61：stopping distance 少 $51\%$，時間也少 $51\%$（初速相同時 $\Delta x = \tfrac{1}{2}v_{0}t$）。

### 題型 5：Constant acceleration，兩個物體

課本題：2.55、2.68–2.70、2.81，以及 Example 2.4。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| $400\ \mathrm{m}$ drag race，贏家 $4.25\ \mathrm{m/s^2}$，早 $248\ \mathrm{ms}$ 到 | 2.55 | 輸家落後 $14.1\ \mathrm{m}$ |
| 兩車各 $88\ \mathrm{km/h}$ 對開，相距 $85\ \mathrm{m}$ 時以 $8\ \mathrm{m/s^2}$ 煞車 | 2.68 | 不會撞，停下時相距約 $10\ \mathrm{m}$ |
| $85\ \mathrm{km/h}$ 追前方 $10\ \mathrm{m}$、$60\ \mathrm{km/h}$ 的車，以 $4.2\ \mathrm{m/s^2}$ 煞車 | 2.70 | 不會撞，最近 $4.3\ \mathrm{m}$ |

陷阱
- 兩個物體要用同一個 origin、同一個 $t = 0$。
- 「最近距離」發生在兩者速度相等的時候，不是後車停下的時候（2.70）。
- 方程式的兩個解都有意義（Example 2.4 的 $t = 0$ 是一開始錯身的那一刻）。

### 題型 6：Free fall，一個物體

課本題：2.35–2.40、2.45–2.48、2.59、2.60、2.71–2.74、2.76、2.79、2.82、2.85、2.86、2.89–2.91。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| 以 $v$ 往上發射：最大高度；高度一半時的 speed | 2.37 | $\dfrac{v^{2}}{2g}$；$\dfrac{v}{\sqrt{2}}$ |
| $82.0\ \mathrm{m}$ 高爆炸，碎片速度從向下 $7.68$ 到向上 $16.7\ \mathrm{m/s}$ | 2.59 | 爆炸後 $3.38\ \mathrm{s}$ 到 $6.14\ \mathrm{s}$ |
| 最後 $1\ \mathrm{s}$ 掉了全程的 $\tfrac{1}{4}$ | 2.73 | 約 $2.7 \times 10^{2}\ \mathrm{m}$ |
| 跳到最高 $h$，在上半段的時間比例 | 2.85 | $\dfrac{1}{\sqrt{2}} \approx 71\%$ |
| 水球 $0.22\ \mathrm{s}$ 通過 $1.3\ \mathrm{m}$ 高的窗戶 | 2.86 | 從窗頂上方 $1.2\ \mathrm{m}$ 掉下 |
| $19.6\ \mathrm{cm}$ 高的水龍頭，空中同時有四滴 | 2.91 | 每秒 $15$ 滴 |

陷阱
- 向上為正時 $a = -g$；$g$ 本身永遠是正的 $9.8\ \mathrm{m/s^2}$。
- 最高點 $v = 0$，但 $a$ 仍然是 $-g$。
- 二次方程式會給兩個時間：負的那個是「如果一直都在 free fall，之前什麼時候在那裡」（Example 2.6）；2.73 的另一個根 $T < 1\ \mathrm{s}$ 不合題意。
- 不是從靜止開始的那一段（2.86 的窗戶）不能用 $\tfrac{1}{2}gt^{2}$，要帶 $v_{0}t$。

### 題型 7：Free fall，兩個物體

課本題：2.75、2.77、2.78、2.92、2.97。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| $h_{0}$ 高處放下一球，同時從地面以 $v_{0}$ 上拋另一球 | 2.97 | $t = \dfrac{h_{0}}{v_{0}}$，高度 $h_{0} - \dfrac{gh_{0}^{2}}{2v_{0}^{2}}$，需要 $v_{0} > \sqrt{\dfrac{gh_{0}}{2}}$ |
| $3.00\ \mathrm{m}$ 跳台，一人以 $1.80\ \mathrm{m/s}$ 往上跳，回到台面時另一人走下去 | 2.77 | $7.88$ 與 $7.67\ \mathrm{m/s}$；先跳的人早 $0.16\ \mathrm{s}$ |
| 以 $10\ \mathrm{m/s}$ 上升的氣球上，相對氣球以 $12\ \mathrm{m/s}$ 上拋 | 2.78 | $2.4\ \mathrm{s}$ |

陷阱：兩個物體的加速度相同時，相對運動是等速；2.78 的 $10\ \mathrm{m/s}$ 用不到。

### 題型 8：Nonconstant acceleration

課本題：2.88、2.93–2.96。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| $a = a_{0} + bt$ | 2.88 | $v = v_{0} + a_{0}t + \tfrac{1}{2}bt^{2}$；$x = x_{0} + v_{0}t + \tfrac{1}{2}a_{0}t^{2} + \tfrac{1}{6}bt^{3}$ |
| $v = bt - ct^{3}$，何時回到 $x = 0$，當時的 $a$ | 2.95 | $t = \sqrt{2b/c}$；$a = -5b$ |
| $a = a_{0}e^{-bt}$，從靜止開始 | 2.96 | $v = \dfrac{a_{0}}{b}\left(1 - e^{-bt}\right)$，趨近 $\dfrac{a_{0}}{b}$；會走無限遠 |

陷阱：不要用 Table 2.1；積分後一定要用 $t = 0$ 的條件定常數。

### 題型 9：讀圖

課本題：2.17、2.18、2.98–2.102；For Thought and Discussion 2.8；GOT IT? 2.2、2.6。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| $v$–$t$ 圖：哪裡不動、哪裡沒有加速度、哪裡最快、哪裡加速度最大、哪裡離起點最遠 | 2.98–2.102 | b、c、b、c、b |

陷阱：在 $v$–$t$ 圖上，「不動」是 $v = 0$（碰到橫軸），「沒有加速度」是 slope 為 $0$（峰或谷）；離起點最遠是 $v$ 由正變負的那一點，不是 $v$ 最大的那一點。

### 題型 10：Data 找直線

課本題：2.58。

| 題目 | 來源 | 答案 |
| --- | --- | --- |
| drag race 的 $x$ 對 $t$ 資料，求 $a$ | 2.58 | $x$ 對 $t^{2}$ 作圖，slope $\approx 1.6\ \mathrm{m/s^2}$，$a \approx 3.2\ \mathrm{m/s^2}$ |

## 會混進來的其他章節

- Ch. 1 的 unit conversion 與 significant figures 出現在 Ch. 2 的每一題（$\mathrm{km/h} \to \mathrm{m/s}$、答案的位數）。
- 微積分：$bt^{n}$ 的微分與積分（題型 2、8），指數函數的積分（2.96）。
- 符號題（答案是式子）：2.29、2.34、2.37、2.50、2.54、2.62、2.75、2.83、2.88、2.89、2.92、2.95–2.97。

## Sources

- Wolfson, *Essential University Physics*, 4th ed., Global Edition, Vol. 1, Ch. 1–2（pp. 17–49）。
- [King Saud University, Physics 1 lecture slides: Motion in One Dimension](https://faculty.ksu.edu.sa/sites/default/files/physics1_02_motion_in_one_dimension.pdf)：只用來對照題型有沒有漏。
- 網路上沒有找到這個範圍可用的大學小考或考古題，所以這次沒有外校題目。
