---
course: [PHY1]
chapter: ["1.2", "1.3"]
tags: [physics, problems, solutions, measurement]
source:
  - "Own solutions in the IDEA format of EUP; every number checked with Python"
created: 2026-10-05
questions: "[[PHY1 Ch01 Questions]]"
---
## Answer Key

| Exercise | Answer |
| --- | --- |
| [[PHY1 Ch01 Questions#EUP 1.17\|EUP 1.17]] | $0.58\ \mathrm{rad} = 33^{\circ}$ |
| [[PHY1 Ch01 Questions#EUP 1.20\|EUP 1.20]] | About $0.45\%$ too small |
| [[PHY1 Ch01 Questions#EUP 1.26\|EUP 1.26]] | $2.5 \times 10^{2}\ \mathrm{cm^3/s} = 2.5 \times 10^{-4}\ \mathrm{m^3/s}$ |
| [[PHY1 Ch01 Questions#EUP 1.32\|EUP 1.32]] | $1.3 \times 10^{2}\ \mathrm{N \cdot m}$ |
| [[PHY1 Ch01 Questions#EUP 1.33\|EUP 1.33]] | $5 \times 10^{7}$ |
| [[PHY1 Ch01 Questions#EUP 1.35\|EUP 1.35]] | $41\ \mathrm{m}$ |
| [[PHY1 Ch01 Questions#EUP 1.36\|EUP 1.36]] | $41.09\ \mathrm{m}$ |
| [[PHY1 Ch01 Questions#EUP 1.44\|EUP 1.44]] | $12.05\ \mathrm{h}$ |
| [[PHY1 Ch01 Questions#EUP 1.45\|EUP 1.45]] | (a) $5.57$; (b) $5.65$ |
| [[PHY1 Ch01 Questions#EUP 1.53\|EUP 1.53]] | About $0.2\ \mathrm{mm}$ |
| [[PHY1 Ch01 Questions#EUP 1.55\|EUP 1.55]] | (a) $40\ \mathrm{nm}$; (b) $5 \times 10^{5}$ per second |
| [[PHY1 Ch01 Questions#EUP 1.65\|EUP 1.65]] | (a) $1.0\ \mathrm{m}$; (b) $1 \times 10^{-3}\ \mathrm{m^2}$; (c) $0.0\ \mathrm{m}$; (d) $1.0$ |
| [[PHY1 Ch01 Questions#EUP 1.67\|EUP 1.67]] | $439\ \mathrm{W}$; more than it consumed |
| [[PHY1 Ch01 Questions#EUP 1.69\|EUP 1.69]] | (a) $d^{3}$; (b) slope about $4.1\ \mathrm{g/cm^3}$, density about $7.8\ \mathrm{g/cm^3}$ |

## EUP §1.2 Measurements and Units

### EUP 1.17
Question: [[PHY1 Ch01 Questions#EUP 1.17|EUP 1.17]]

> [!solution] Solution
> **Interpret.** The turn is an arc of a circle, and we want the angle that the arc subtends.
>
> **Develop.** The angle in radians is defined as the ratio of the arc length $s$ to the radius $r$: $\theta = s/r$.
>
> **Evaluate.**
> $$
> \theta = \frac{s}{r} = \frac{2.1\ \mathrm{km}}{3.6\ \mathrm{km}} = 0.58\ \mathrm{rad} = (0.58\ \mathrm{rad})\left(\frac{180^{\circ}}{\pi\ \mathrm{rad}}\right) = 33^{\circ}
> $$
>
> **Assess.** The kilometers cancel, so the radian is a pure ratio. The arc is a little more than half the radius, so the angle is a little more than half a radian, about a third of a right angle.

### EUP 1.20
Question: [[PHY1 Ch01 Questions#EUP 1.20|EUP 1.20]]

> [!solution] Solution
> **Interpret.** We compare the approximation $\pi \times 10^{7}\ \mathrm{s}$ with the length of a year in seconds.
>
> **Develop.** Convert one year to seconds with a chain of conversion factors, taking $1\ \mathrm{y} = 365.25\ \mathrm{d}$. The percentage error is the difference divided by the true value.
>
> **Evaluate.**
> $$
> \begin{aligned}
> 1\ \mathrm{y} &= (365.25\ \mathrm{d})\left(\frac{24\ \mathrm{h}}{1\ \mathrm{d}}\right)\left(\frac{3600\ \mathrm{s}}{1\ \mathrm{h}}\right) = 3.1558 \times 10^{7}\ \mathrm{s}, \\
> \frac{\pi \times 10^{7}\ \mathrm{s} - 3.1558 \times 10^{7}\ \mathrm{s}}{3.1558 \times 10^{7}\ \mathrm{s}} &= -0.0045 = -0.45\%.
> \end{aligned}
> $$
> The figure is too small by about $0.45\%$.
>
> **Assess.** With a $365$-day year the error is $0.38\%$. Either way $\pi \times 10^{7}\ \mathrm{s}$ is good to better than half a percent, which is why it is a handy number for estimates.

### EUP 1.26
Question: [[PHY1 Ch01 Questions#EUP 1.26|EUP 1.26]]

> [!solution] Solution
> **Interpret.** The flow is a volume per time. Both units change: liters to $\mathrm{cm^3}$ or $\mathrm{m^3}$, and minutes to seconds.
>
> **Develop.** Use $1\ \mathrm{L} = 1000\ \mathrm{cm^3}$, $1\ \mathrm{min} = 60\ \mathrm{s}$, and $1\ \mathrm{m} = 100\ \mathrm{cm}$, so that $1\ \mathrm{m^3} = (100\ \mathrm{cm})^{3} = 10^{6}\ \mathrm{cm^3}$.
>
> **Evaluate.**
> $$
> \begin{aligned}
> 15\ \mathrm{L/min} &= \left(\frac{15\ \mathrm{L}}{\mathrm{min}}\right)\left(\frac{1000\ \mathrm{cm^3}}{1\ \mathrm{L}}\right)\left(\frac{1\ \mathrm{min}}{60\ \mathrm{s}}\right) = 2.5 \times 10^{2}\ \mathrm{cm^3/s}, \\
> 2.5 \times 10^{2}\ \mathrm{cm^3/s} &= \left(\frac{2.5 \times 10^{2}\ \mathrm{cm^3}}{\mathrm{s}}\right)\left(\frac{1\ \mathrm{m^3}}{10^{6}\ \mathrm{cm^3}}\right) = 2.5 \times 10^{-4}\ \mathrm{m^3/s}.
> \end{aligned}
> $$
>
> **Assess.** A quarter of a liter each second is a reasonable tap. The conversion factor for a volume is the cube of the factor for a length: $10^{6}$, not $10^{2}$.

## EUP §1.3 Working with Numbers

### EUP 1.32
Question: [[PHY1 Ch01 Questions#EUP 1.32|EUP 1.32]]

> [!solution] Solution
> **Interpret.** Two lengths in different units are added, and the sum is multiplied by a force.
>
> **Develop.** Convert both lengths to meters with $1\ \mathrm{cm} = 10^{-2}\ \mathrm{m}$ and $1\ \mathrm{\mu m} = 10^{-6}\ \mathrm{m}$, give them the same exponent, add, and then multiply. Keep one extra figure in the sum and round at the end.
>
> **Evaluate.**
> $$
> \begin{aligned}
> 5.1 \times 10^{-2}\ \mathrm{cm} &= 5.1 \times 10^{-4}\ \mathrm{m} = 0.51 \times 10^{-3}\ \mathrm{m}, \\
> 6.8 \times 10^{3}\ \mathrm{\mu m} &= 6.8 \times 10^{-3}\ \mathrm{m}, \\
> 0.51 \times 10^{-3}\ \mathrm{m} + 6.8 \times 10^{-3}\ \mathrm{m} &= 7.31 \times 10^{-3}\ \mathrm{m}, \\
> (7.31 \times 10^{-3}\ \mathrm{m})(1.8 \times 10^{4}\ \mathrm{N}) &= 1.3 \times 10^{2}\ \mathrm{N \cdot m}.
> \end{aligned}
> $$
>
> **Assess.** The sum is known only to the tenths place of $10^{-3}\ \mathrm{m}$, that is, $7.3 \times 10^{-3}\ \mathrm{m}$, and the force has two significant figures, so the product has two. The unit is the newton-meter.

### EUP 1.33
Question: [[PHY1 Ch01 Questions#EUP 1.33|EUP 1.33]]

> [!solution] Solution
> **Interpret.** We need a cube root of a number in scientific notation.
>
> **Develop.** For a root, take the root of the digits and divide the exponent by $3$. The exponent $23$ is not a multiple of $3$, so first rewrite the number with the exponent $21$.
>
> **Evaluate.**
> $$
> \sqrt[3]{1.25 \times 10^{23}} = \sqrt[3]{125 \times 10^{21}} = \sqrt[3]{125} \times 10^{21/3} = 5 \times 10^{7}
> $$
>
> **Assess.** Check by cubing: $(5 \times 10^{7})^{3} = 125 \times 10^{21} = 1.25 \times 10^{23}$.

### EUP 1.35
Question: [[PHY1 Ch01 Questions#EUP 1.35|EUP 1.35]]

> [!solution] Solution
> **Interpret.** Two lengths are added, one known to the meter and one to the millimeter.
>
> **Develop.** In addition, the answer has as many digits to the right of the decimal point as the term with the fewest. Here $41\ \mathrm{m}$ has none.
>
> **Evaluate.**
> $$
> 41\ \mathrm{m} + 0.036\ \mathrm{m} = 41.036\ \mathrm{m} \to 41\ \mathrm{m}
> $$
>
> **Assess.** The original length is uncertain by about half a meter, so an antenna of $3.6\ \mathrm{cm}$ makes no difference that we can state.

### EUP 1.36
Question: [[PHY1 Ch01 Questions#EUP 1.36|EUP 1.36]]

> [!solution] Solution
> **Interpret.** The same sum as in EUP 1.35, with the original length now known to the centimeter.
>
> **Develop.** The term with the fewest decimal places is $41.05\ \mathrm{m}$, with two.
>
> **Evaluate.**
> $$
> 41.05\ \mathrm{m} + 0.036\ \mathrm{m} = 41.086\ \mathrm{m} \to 41.09\ \mathrm{m}
> $$
>
> **Assess.** Now the antenna changes the last stated digit. The same addition gives different answers because the precision of the data differs, not the arithmetic.

## EUP Chapter 1 Example Variations

### EUP 1.44
Question: [[PHY1 Ch01 Questions#EUP 1.44|EUP 1.44]]

> [!solution] Solution
> **Interpret.** A subtraction of two times given in different units, as in Example 1.3.
>
> **Develop.** Convert the decrease to hours, subtract, and keep as many decimal places as the term with the fewest.
>
> **Evaluate.**
> $$
> \begin{aligned}
> 21\ \mathrm{min} &= (21\ \mathrm{min})\left(\frac{1\ \mathrm{h}}{60\ \mathrm{min}}\right) = 0.35\ \mathrm{h}, \\
> 12.404\ \mathrm{h} - 0.35\ \mathrm{h} &= 12.054\ \mathrm{h} \to 12.05\ \mathrm{h}.
> \end{aligned}
> $$
>
> **Assess.** The decrease is known to two decimal places in hours, so the new period is too. The third decimal place of the original period is lost.

## EUP Chapter 1 Problems

### EUP 1.45
Question: [[PHY1 Ch01 Questions#EUP 1.45|EUP 1.45]]

> [!solution] Solution
> **Interpret.** The same quantity is computed twice, with different rounding of the intermediate result.
>
> **Develop.** $\sqrt{2} = 1.41421\ldots$, which is $1.41$ to three significant figures and $1.414$ to four.
>
> **Evaluate.**
> - (a) $(1.41)^{5} = 5.573 \to 5.57$
> - (b) $(1.414)^{5} = 5.653 \to 5.65$
>
> **Assess.** The exact value is $(\sqrt{2})^{5} = 4\sqrt{2} = 5.657$, which is $5.66$ to three significant figures. Rounding the intermediate result to three figures gives an error of about $0.08$. One extra figure brings the answer within $0.01$, and still not exactly to $5.66$, because raising to the fifth power multiplies the relative error by five. Keep the unrounded value in the calculator and round only the final answer.

### EUP 1.53
Question: [[PHY1 Ch01 Questions#EUP 1.53|EUP 1.53]]

> [!solution] Solution
> **Interpret.** The gum keeps its volume when it is blown into a thin spherical shell. We want the thickness of the shell.
>
> **Develop.** The volume is $V = m/\rho$. A thin shell is a flat sheet of area $A = 4\pi r^{2}$ and thickness $t$, so $V = At$.
>
> **Evaluate.**
> $$
> \begin{aligned}
> V &= \frac{m}{\rho} = \frac{7\ \mathrm{g}}{1\ \mathrm{g/cm^3}} = 7\ \mathrm{cm^3}, \\
> A &= 4\pi r^{2} = 4\pi (5\ \mathrm{cm})^{2} \approx 300\ \mathrm{cm^2}, \\
> t &= \frac{V}{A} \approx \frac{7\ \mathrm{cm^3}}{300\ \mathrm{cm^2}} \approx 0.02\ \mathrm{cm} = 0.2\ \mathrm{mm}.
> \end{aligned}
> $$
>
> **Assess.** A few tenths of a millimeter is a few sheets of paper, reasonable for a bubble about to burst. The radius is $5\ \mathrm{cm}$, half the diameter. An estimate carries one significant figure.

### EUP 1.55
Question: [[PHY1 Ch01 Questions#EUP 1.55|EUP 1.55]]

> [!solution] Solution
> **Interpret.** Part (a) asks for the side of one component, part (b) for a rate limited by the travel time of the impulses.
>
> **Develop.** A square array of $10^{10}$ components has $\sqrt{10^{10}} = 10^{5}$ components along each side. For part (b), find the distance traveled in one calculation, then the time at speed $\tfrac{2}{3}c$ with $c = 3 \times 10^{8}\ \mathrm{m/s}$.
>
> **Evaluate.**
> - (a) The side of one component is
> $$
> \frac{4\ \mathrm{mm}}{10^{5}} = \frac{4 \times 10^{-3}\ \mathrm{m}}{10^{5}} = 4 \times 10^{-8}\ \mathrm{m} = 40\ \mathrm{nm}.
> $$
> - (b) One calculation covers $10^{4}$ components a million times:
> $$
> \begin{aligned}
> d &= (10^{4})(10^{6})(4 \times 10^{-8}\ \mathrm{m}) = 400\ \mathrm{m}, \\
> t &= \frac{d}{\tfrac{2}{3}c} = \frac{400\ \mathrm{m}}{2 \times 10^{8}\ \mathrm{m/s}} = 2 \times 10^{-6}\ \mathrm{s}.
> \end{aligned}
> $$
> The chip can do $1/t = 5 \times 10^{5}$ such calculations each second.
>
> **Assess.** $40\ \mathrm{nm}$ is a few hundred atomic diameters, the scale of chip technology in EUP 1.66. The speed of light limits a chip a few millimeters across to about half a million such calculations per second.

### EUP 1.65
Question: [[PHY1 Ch01 Questions#EUP 1.65|EUP 1.65]]

> [!solution] Solution
> **Interpret.** Four operations on $1.0\ \mathrm{m}$ and a length in millimeters; each needs the right rule for significant figures.
>
> **Develop.** Convert millimeters to meters first. Addition and subtraction keep the decimal places of the less precise term, which is $1.0\ \mathrm{m}$ with one. Multiplication and division keep the significant figures of the less precise factor.
>
> **Evaluate.**
> - (a) $1.0\ \mathrm{m} + 0.009\ \mathrm{m} = 1.009\ \mathrm{m} \to 1.0\ \mathrm{m}$
> - (b) $(1.0\ \mathrm{m})(0.001\ \mathrm{m}) = 1 \times 10^{-3}\ \mathrm{m^2}$, one significant figure, as in $1\ \mathrm{mm}$
> - (c) $1.0\ \mathrm{m} - 0.998\ \mathrm{m} = 0.002\ \mathrm{m} \to 0.0\ \mathrm{m}$
> - (d) $\dfrac{1.0\ \mathrm{m}}{0.998\ \mathrm{m}} = 1.002 \to 1.0$, two significant figures and no unit
>
> **Assess.** In (c) the calculator shows $2\ \mathrm{mm}$, but $1.0\ \mathrm{m}$ is known only to about $\pm 0.05\ \mathrm{m}$, so the difference is zero to the precision of the data. In (d) the meters cancel and the answer is a pure number.

### EUP 1.67
Question: [[PHY1 Ch01 Questions#EUP 1.67|EUP 1.67]]

> [!solution] Solution
> **Interpret.** An energy generated in one year is turned into an average power, to compare with the average power consumed.
>
> **Develop.** Average power is energy divided by time. Convert the energy to joules and the year 2017, which has $365$ days, to seconds.
>
> **Evaluate.**
> $$
> \begin{aligned}
> E &= (3849\ \mathrm{kWh})\left(\frac{3.6 \times 10^{6}\ \mathrm{J}}{1\ \mathrm{kWh}}\right) = 1.386 \times 10^{10}\ \mathrm{J}, \\
> t &= (365\ \mathrm{d})\left(\frac{86\,400\ \mathrm{s}}{1\ \mathrm{d}}\right) = 3.154 \times 10^{7}\ \mathrm{s}, \\
> P &= \frac{E}{t} = \frac{1.386 \times 10^{10}\ \mathrm{J}}{3.154 \times 10^{7}\ \mathrm{s}} = 439\ \mathrm{W}.
> \end{aligned}
> $$
> Since $439\ \mathrm{W} > 392\ \mathrm{W}$, the house generated more electrical energy than it consumed.
>
> **Assess.** The other way round: $392\ \mathrm{W}$ for $8760\ \mathrm{h}$ is $3434\ \mathrm{kWh}$, less than the $3849\ \mathrm{kWh}$ generated. The factor $3.6\ \mathrm{MJ}$ per kWh is exact, since $1\ \mathrm{kWh} = (1000\ \mathrm{W})(3600\ \mathrm{s})$.

### EUP 1.69
Question: [[PHY1 Ch01 Questions#EUP 1.69|EUP 1.69]]

> [!solution] Solution
> **Interpret.** We look for a variable that turns the relation between mass and diameter into a straight line, as in Example 1.4.
>
> **Develop.** With density $\rho$ and radius $r = d/2$,
> $$
> m = \rho V = \rho \cdot \tfrac{4}{3}\pi \left(\frac{d}{2}\right)^{3} = \frac{\pi \rho}{6}\, d^{3}.
> $$
> So $m$ is proportional to $d^{3}$: a plot of $m$ against $d^{3}$ is a straight line through the origin with slope $\pi\rho/6$.
>
> **Evaluate.**
> - (a) The quantity is the diameter cubed, $d^{3}$.
> - (b) The values of $d^{3}$ are:
>
> | $d^{3}$ ($\mathrm{cm^3}$) | 0.42 | 1.00 | 3.65 | 10.1 | 16.4 |
> | --- | --- | --- | --- | --- | --- |
> | $m$ (g) | 1.81 | 3.95 | 15.8 | 38.6 | 68.2 |
>
> ![[PHY1 EUP 1.69 fit.png]]
>
> The best-fit line through the origin has slope about $4.1\ \mathrm{g/cm^3}$. Then
> $$
> \rho = \frac{6}{\pi}(\text{slope}) = \frac{6}{\pi}(4.1\ \mathrm{g/cm^3}) \approx 7.8\ \mathrm{g/cm^3}.
> $$
>
> **Assess.** The points lie close to a straight line, which confirms $m \propto d^{3}$, and $7.8\ \mathrm{g/cm^3}$ is the density of steel. The slope is not the density itself: it is $\pi\rho/6$.
