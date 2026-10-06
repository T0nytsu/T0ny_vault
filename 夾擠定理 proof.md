用 ε-δ 證最直接，考試寫這個版本就夠（可直接貼進 Obsidian）：

> [!theorem] Squeeze Theorem
> If $f(x)\le g(x)\le h(x)$ when $x$ is near $a$ (except possibly at $a$) and $\lim_{x\to a}f(x)=\lim_{x\to a}h(x)=L$, then $\lim_{x\to a}g(x)=L$.

> [!proof]-
> $$
> \begin{aligned}
> &\text{Given } \varepsilon>0.\\
> &\exists\,\delta_0>0 \text{ s.t. } 0<\lvert x-a\rvert<\delta_0 \implies f(x)\le g(x)\le h(x)\\
> &\because \lim_{x\to a}f(x)=L,\ \exists\,\delta_1>0 \text{ s.t. } 0<\lvert x-a\rvert<\delta_1 \implies L-\varepsilon<f(x)\\
> &\because \lim_{x\to a}h(x)=L,\ \exists\,\delta_2>0 \text{ s.t. } 0<\lvert x-a\rvert<\delta_2 \implies h(x)<L+\varepsilon\\
> &\text{Choose } \delta=\min\{\delta_0,\delta_1,\delta_2\}.\\
> &\text{If } 0<\lvert x-a\rvert<\delta, \text{ then } L-\varepsilon<f(x)\le g(x)\le h(x)<L+\varepsilon\\
> &\therefore \lvert g(x)-L\rvert<\varepsilon\\
> &\text{Hence } \lim_{x\to a}g(x)=L \text{ by the precise definition of a limit.} \qquad \blacksquare
> \end{aligned}
> $$
> \# $\lvert f(x)-L\rvert<\varepsilon$ means $L-\varepsilon<f(x)<L+\varepsilon$. Only the left half is needed for $f$ and only the right half for $h$.

重點：
- **只用半邊不等式**：$f$ 負責下界 $L-\varepsilon$，$h$ 負責上界 $L+\varepsilon$，$g$ 被夾在中間。
- **δ 取 min**：三個條件要同時成立，跟 1.7 的 Sum Law 證法（$\min\{\delta_1,\delta_2\}$）是同一招。
- **$\delta_0$ 不要漏**：$f\le g\le h$ 只在 $a$ 附近成立；若題目說對所有 $x$ 都成立，這行可省，$\delta=\min\{\delta_1,\delta_2\}$。
- 這題不用 $\frac{\varepsilon}{2}$，因為沒有兩個誤差相加。

其他方法：也可以寫 $0\le g-f\le h-f$，其中 $\lim(h-f)=0$，但「被 0 夾住所以趨近 0」這一步還是得用 ε-δ，沒有比較省。所以考試直接寫上面這個。