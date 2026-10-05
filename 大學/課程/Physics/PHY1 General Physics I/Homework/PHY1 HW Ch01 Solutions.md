---
course: [PHY1]
chapter: ["1.2", "1.3", "1.4"]
tags: [physics, homework, solutions, measurement]
source:
  - "Own solutions; every number recomputed with Python"
  - "EUP Ch. 1 (pp. 17-30), scanned PDF: worked examples"
created: 2026-10-05
questions: "[[PHY1 HW Ch01 Questions]]"
---
> [!note] Notation
> Units are upright and follow the number. Conversion factors are ratios equal to 1. Intermediate values keep one extra figure; only the final answer is rounded.

## Answer Key

| Problem | Answer |
| --- | --- |
| [[PHY1 HW Ch01 Questions#EUP Example 1.1\|EUP Example 1.1]] | $18\ \mathrm{m/s}$ |
| [[PHY1 HW Ch01 Questions#EUP Example 1.2\|EUP Example 1.2]] | $1.7 \times 10^{2}\ \mathrm{m/s}$ |
| [[PHY1 HW Ch01 Questions#EUP Example 1.3\|EUP Example 1.3]] | $0.008\ \mathrm{m} = 8\ \mathrm{mm}$ |
| [[PHY1 HW Ch01 Questions#EUP Example 1.4\|EUP Example 1.4]] | $y$ versus $t^{2}$; slope $\approx 5.0\ \mathrm{m/s^2}$; $g \approx 10\ \mathrm{m/s^2}$ |
| [[PHY1 HW Ch01 Questions#EUP Example 1.5\|EUP Example 1.5]] | about $1\ \mathrm{kg}$; about $10^{12}$ cells |
| [[PHY1 HW Ch01 Questions#EUP 1.26\|EUP 1.26]] | $2.5 \times 10^{2}\ \mathrm{cm^3/s} = 2.5 \times 10^{-4}\ \mathrm{m^3/s}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.67\|EUP 1.67]] | $439\ \mathrm{W}$; more than it consumed |
| [[PHY1 HW Ch01 Questions#EUP 1.17\|EUP 1.17]] | $0.58\ \mathrm{rad} \approx 33^{\circ}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.32\|EUP 1.32]] | $1.3 \times 10^{2}\ \mathrm{N \cdot m}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.33\|EUP 1.33]] | $5.00 \times 10^{7}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.35 and 1.36\|EUP 1.35 and 1.36]] | $41\ \mathrm{m}$; $41.09\ \mathrm{m}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.44\|EUP 1.44]] | $12.05\ \mathrm{h}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.45\|EUP 1.45]] | (a) $5.57$; (b) $5.65$ |
| [[PHY1 HW Ch01 Questions#EUP 1.57\|EUP 1.57]] | about $0.4\%$ and $0.05\%$ |
| [[PHY1 HW Ch01 Questions#EUP 1.65\|EUP 1.65]] | (a) $1.0\ \mathrm{m}$; (b) $1 \times 10^{-3}\ \mathrm{m^2}$; (c) $0.0\ \mathrm{m}$; (d) $1.0$ |
| [[PHY1 HW Ch01 Questions#EUP 1.53\|EUP 1.53]] | about $0.2\ \mathrm{mm}$ |
| [[PHY1 HW Ch01 Questions#EUP 1.55\|EUP 1.55]] | (a) $40\ \mathrm{nm}$; (b) about $5 \times 10^{5}$ per second |
| [[PHY1 HW Ch01 Questions#EUP 1.69\|EUP 1.69]] | (a) $d^{3}$; (b) slope $\approx 4.1\ \mathrm{g/cm^3}$, so $\rho \approx 7.8\ \mathrm{g/cm^3}$ |

## Textbook Examples

### EUP Example 1.1
Question: [[PHY1 HW Ch01 Questions#EUP Example 1.1|EUP Example 1.1]]

> [!solution] Solution
> $$
> 65\ \mathrm{km/h} = \left(\frac{65\ \mathrm{km}}{1\ \mathrm{h}}\right)\left(\frac{1000\ \mathrm{m}}{1\ \mathrm{km}}\right)\left(\frac{1\ \mathrm{h}}{3600\ \mathrm{s}}\right) = 18\ \mathrm{m/s}.
> $$

### EUP Example 1.2
Question: [[PHY1 HW Ch01 Questions#EUP Example 1.2|EUP Example 1.2]]

> [!solution] Solution
> $h = 3.0\ \mathrm{km} = 3.0 \times 10^{3}\ \mathrm{m}$, so
> $$
> \begin{aligned}
> v = \sqrt{gh} &= \sqrt{(9.8\ \mathrm{m/s^2})(3.0 \times 10^{3}\ \mathrm{m})} = \sqrt{2.94 \times 10^{4}\ \mathrm{m^2/s^2}} \\
> &= 1.7 \times 10^{2}\ \mathrm{m/s}.
> \end{aligned}
> $$

> [!warning] The book's conversion to km/h
> The book's solution goes on to convert the rounded $1.7 \times 10^{2}\ \mathrm{m/s}$ and prints $6.1 \times 10^{2}\ \mathrm{km/h}$. With the unrounded $171.5\ \mathrm{m/s}$ the result is $(171.5\ \mathrm{m/s})(3.6) = 6.2 \times 10^{2}\ \mathrm{km/h}$.

### EUP Example 1.3
Question: [[PHY1 HW Ch01 Questions#EUP Example 1.3|EUP Example 1.3]]

> [!solution] Solution
> $$
> \Delta L = 3.249\ \mathrm{m} - 3.241\ \mathrm{m} = 0.008\ \mathrm{m} = 8\ \mathrm{mm}.
> $$
> One significant figure: both lengths are known to $0.001\ \mathrm{m}$, so the difference is too.

### EUP Example 1.4
Question: [[PHY1 HW Ch01 Questions#EUP Example 1.4|EUP Example 1.4]]

> [!solution] Solution
> $y = \tfrac{1}{2}gt^{2}$, so plot $y$ versus $t^{2}$: a straight line with slope $\tfrac{1}{2}g$.
>
> | $t^{2}$ ($\mathrm{s^2}$) | 0.250 | 1.00 | 2.25 | 4.00 | 6.25 | 9.00 |
> | --- | --- | --- | --- | --- | --- | --- |
> | $y$ ($\mathrm{m}$) | 1.12 | 5.30 | 12.2 | 18.5 | 34.1 | 43.6 |
>
> The best-fit line has slope $\approx 5.0\ \mathrm{m/s^2}$, so $g = 2 \times \text{slope} \approx 10\ \mathrm{m/s^2}$.
>
> ![[PHY1 Ch01 Example 1.4 fit.png]]

### EUP Example 1.5
Question: [[PHY1 HW Ch01 Questions#EUP Example 1.5|EUP Example 1.5]]

> [!solution] Solution
> Brain: a cube about $10\ \mathrm{cm}$ across, mostly water ($1\ \mathrm{g/cm^3}$):
> $$
> V = (10\ \mathrm{cm})^{3} = 1000\ \mathrm{cm^3} = 10^{-3}\ \mathrm{m^3}, \qquad m \approx 1000\ \mathrm{g} = 1\ \mathrm{kg}.
> $$
> Cell: about $10^{-5}\ \mathrm{m}$ across (a red blood cell, Table 1.2), volume $(10^{-5}\ \mathrm{m})^{3} = 10^{-15}\ \mathrm{m^3}$:
> $$
> N = \frac{10^{-3}\ \mathrm{m^3}}{10^{-15}\ \mathrm{m^3}} = 10^{12}\ \text{cells}.
> $$

## Unit Conversion

### EUP 1.26
Question: [[PHY1 HW Ch01 Questions#EUP 1.26|EUP 1.26]]

> [!solution] Solution
> $$
> 15\ \mathrm{L/min} = \left(\frac{15\ \mathrm{L}}{1\ \mathrm{min}}\right)\left(\frac{1000\ \mathrm{cm^3}}{1\ \mathrm{L}}\right)\left(\frac{1\ \mathrm{min}}{60\ \mathrm{s}}\right) = 2.5 \times 10^{2}\ \mathrm{cm^3/s}.
> $$
> Since $1\ \mathrm{cm^3} = (10^{-2}\ \mathrm{m})^{3} = 10^{-6}\ \mathrm{m^3}$, this is $2.5 \times 10^{-4}\ \mathrm{m^3/s}$.

### EUP 1.67
Question: [[PHY1 HW Ch01 Questions#EUP 1.67|EUP 1.67]]

> [!solution] Solution
> Average power is energy divided by time; 2017 has 365 days.
> $$
> \bar{P} = \frac{E}{t} = \frac{(3849\ \mathrm{kWh})(3.6 \times 10^{6}\ \mathrm{J/kWh})}{(365)(24)(3600\ \mathrm{s})} = \frac{1.386 \times 10^{10}\ \mathrm{J}}{3.154 \times 10^{7}\ \mathrm{s}} = 439\ \mathrm{W}.
> $$
> $439\ \mathrm{W} > 392\ \mathrm{W}$: the house generated more than it consumed.

## Radians and Arc Length

### EUP 1.17
Question: [[PHY1 HW Ch01 Questions#EUP 1.17|EUP 1.17]]

> [!solution] Solution
> $$
> \theta = \frac{s}{r} = \frac{2.1\ \mathrm{km}}{3.6\ \mathrm{km}} = 0.58\ \mathrm{rad} = (0.583\ \mathrm{rad})\left(\frac{180^{\circ}}{\pi\ \mathrm{rad}}\right) \approx 33^{\circ}.
> $$

## Scientific Notation

### EUP 1.32
Question: [[PHY1 HW Ch01 Questions#EUP 1.32|EUP 1.32]]

> [!solution] Solution
> $6.8 \times 10^{3}\ \mathrm{\mu m} = 6.8 \times 10^{3} \times 10^{-4}\ \mathrm{cm} = 0.68\ \mathrm{cm}$, so
> $$
> 0.051\ \mathrm{cm} + 0.68\ \mathrm{cm} = 0.731\ \mathrm{cm} = 7.31 \times 10^{-3}\ \mathrm{m},
> $$
> $$
> (7.31 \times 10^{-3}\ \mathrm{m})(1.8 \times 10^{4}\ \mathrm{N}) = 1.3 \times 10^{2}\ \mathrm{N \cdot m}.
> $$

### EUP 1.33
Question: [[PHY1 HW Ch01 Questions#EUP 1.33|EUP 1.33]]

> [!solution] Solution
> $$
> \sqrt[3]{1.25 \times 10^{23}} = \sqrt[3]{125 \times 10^{21}} = 5 \times 10^{7}.
> $$
> To three significant figures, $5.00 \times 10^{7}$.

## Significant Figures

### EUP 1.35 and 1.36
Question: [[PHY1 HW Ch01 Questions#EUP 1.35 and 1.36|EUP 1.35 and 1.36]]

> [!solution] Solution
> $3.6\ \mathrm{cm} = 0.036\ \mathrm{m}$. In a sum, the term with the fewest digits to the right of the decimal point decides.
> - **35.** $41\ \mathrm{m} + 0.036\ \mathrm{m} = 41.036\ \mathrm{m} \approx 41\ \mathrm{m}$
> - **36.** $41.05\ \mathrm{m} + 0.036\ \mathrm{m} = 41.086\ \mathrm{m} \approx 41.09\ \mathrm{m}$

### EUP 1.44
Question: [[PHY1 HW Ch01 Questions#EUP 1.44|EUP 1.44]]

> [!solution] Solution
> $21\ \mathrm{min} = (21\ \mathrm{min})\left(\dfrac{1\ \mathrm{h}}{60\ \mathrm{min}}\right) = 0.35\ \mathrm{h}$, so
> $$
> 12.404\ \mathrm{h} - 0.35\ \mathrm{h} = 12.054\ \mathrm{h} \approx 12.05\ \mathrm{h}.
> $$

### EUP 1.45
Question: [[PHY1 HW Ch01 Questions#EUP 1.45|EUP 1.45]]

> [!solution] Solution
> - (a) $\sqrt{2} \approx 1.41$, and $1.41^{5} = 5.573 \approx 5.57$.
> - (b) $\sqrt{2} \approx 1.414$, and $1.414^{5} = 5.6526 \approx 5.65$.
>
> The exact value is $(\sqrt{2})^{5} = 4\sqrt{2} = 5.657 \approx 5.66$: rounding early costs digits.

### EUP 1.57
Question: [[PHY1 HW Ch01 Questions#EUP 1.57|EUP 1.57]]

> [!solution] Solution
> Three significant figures means the last digit is uncertain by half a unit, $\pm 0.005$:
> $$
> \frac{0.005}{1.27} \approx 0.4\%, \qquad \frac{0.005}{9.97} \approx 0.05\%.
> $$

### EUP 1.65
Question: [[PHY1 HW Ch01 Questions#EUP 1.65|EUP 1.65]]

> [!solution] Solution
> - (a) $1.0\ \mathrm{m} + 0.009\ \mathrm{m} = 1.009\ \mathrm{m} \approx 1.0\ \mathrm{m}$
> - (b) $(1.0\ \mathrm{m})(0.001\ \mathrm{m}) = 1 \times 10^{-3}\ \mathrm{m^2}$
> - (c) $1.0\ \mathrm{m} - 0.998\ \mathrm{m} = 0.002\ \mathrm{m} \approx 0.0\ \mathrm{m}$
> - (d) $\dfrac{1.0\ \mathrm{m}}{0.998\ \mathrm{m}} = 1.002 \approx 1.0$
>
> Sums and differences keep the digits to the right of the decimal point of $1.0\ \mathrm{m}$; the product keeps the one significant figure of $1\ \mathrm{mm}$, and the quotient the two of $1.0\ \mathrm{m}$.

## Estimation

### EUP 1.53
Question: [[PHY1 HW Ch01 Questions#EUP 1.53|EUP 1.53]]

> [!solution] Solution
> The volume of gum is $V = m/\rho = 7\ \mathrm{cm^3}$. As a flat sheet of area $4\pi r^{2}$ ($r = 5\ \mathrm{cm}$) and thickness $d$, $V = 4\pi r^{2}d$:
> $$
> d = \frac{V}{4\pi r^{2}} = \frac{7\ \mathrm{cm^3}}{4\pi(5\ \mathrm{cm})^{2}} = 0.02\ \mathrm{cm} = 0.2\ \mathrm{mm}.
> $$

### EUP 1.55
Question: [[PHY1 HW Ch01 Questions#EUP 1.55|EUP 1.55]]

> [!solution] Solution
> **(a)** Area per component: $\dfrac{(4 \times 10^{-3}\ \mathrm{m})^{2}}{10^{10}} = 1.6 \times 10^{-15}\ \mathrm{m^2}$, so its side is $\sqrt{16 \times 10^{-16}\ \mathrm{m^2}} = 4 \times 10^{-8}\ \mathrm{m} = 40\ \mathrm{nm}$.
>
> **(b)** Distance per calculation: $(10^{4})(10^{6})(4 \times 10^{-8}\ \mathrm{m}) = 4 \times 10^{2}\ \mathrm{m}$, at speed $\tfrac{2}{3}c = 2 \times 10^{8}\ \mathrm{m/s}$:
> $$
> t = \frac{4 \times 10^{2}\ \mathrm{m}}{2 \times 10^{8}\ \mathrm{m/s}} = 2 \times 10^{-6}\ \mathrm{s}, \qquad \frac{1}{t} = 5 \times 10^{5}\ \text{calculations per second}.
> $$

## Data and Straight-Line Fits

### EUP 1.69
Question: [[PHY1 HW Ch01 Questions#EUP 1.69|EUP 1.69]]

> [!solution] Solution
> **(a)** With diameter $d = 2r$,
> $$
> m = \rho V = \rho \cdot \tfrac{4}{3}\pi\left(\tfrac{d}{2}\right)^{3} = \frac{\pi\rho}{6}\,d^{3},
> $$
> so plot $m$ versus $d^{3}$; the slope is $\pi\rho/6$.
>
> | $d^{3}$ ($\mathrm{cm^3}$) | 0.42 | 1.00 | 3.65 | 10.1 | 16.4 |
> | --- | --- | --- | --- | --- | --- |
> | $m$ ($\mathrm{g}$) | 1.81 | 3.95 | 15.8 | 38.6 | 68.2 |
>
> **(b)** The best-fit line has slope $\approx 4.1\ \mathrm{g/cm^3}$, so $\rho = \dfrac{6}{\pi} \times \text{slope} \approx 7.8\ \mathrm{g/cm^3}$.
>
> ![[PHY1 Ch01 Problem 1.69 fit.png]]
