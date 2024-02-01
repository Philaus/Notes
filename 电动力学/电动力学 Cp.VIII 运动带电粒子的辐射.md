# Cp.VIII 运动带电粒子的辐射

##<font color='red'>$\S 1$ </font>李纳-维谢尔势

由上一章中的有源麦克斯韦方程代入场强张量可以得到四维有源的波动方程:
$$
\partial_\mu F^{\mu\nu}=\frac{4\pi}{c}J^\nu\\
\ \\
\partial_\mu\partial^\mu A^\nu=\frac{4\pi}{c}J^\nu
$$

为了求这个方程四维协变形式的解, 定义达朗贝尔算符四维协变形式的格林函数:
$$
\partial_\mu\partial^\mu D(x,x')=\delta^4(x-x')
$$
(事实上, 任何只依赖于 $x-x'=R$ 的函数都可以这样写出格林函数)

然后利用傅里叶变换求解, 写为:
$$
D(x,x')=\int \frac{d^4k}{(2\pi)^4}\tilde{D}(k)e^{-ik\cdot (x-x')}
$$
利用 $\delta$ 函数的傅里叶变换
$$
\mathscr{F}\partial_\mu\partial^\mu D(x,x')=\mathscr{F}\delta^4(x-x')=1\\
\partial_\mu\partial^\mu\mathscr{F} D(x,x')=\partial_\mu\partial^\mu\tilde{D}(k)=-k^2\tilde{D}(k)\\
\ \\
\tilde{D}(k)=-(1/k^2)\ \ \ (k^2=k_\mu k^\mu)\\
D(x,x')=-\int \frac{d^4k}{(2\pi)^4}\frac{e^{-ik\cdot (x-x')}}{k^2}
$$
现在这个积分在实轴上存在奇点, 需要进一步给出一个非奇异的定义, 也就是为其选择合适的路径. 其中只有推迟格林函数才是符合因果性的函数, 对应的路径是沿实轴上侧和无穷大上半圆. 此外还应绕开实轴上的两个奇点.
$$
D^{(+)}(x,x')=-\int \frac{d^4k}{(2\pi)^4}\frac{e^{-ik\cdot (x-x')}}{(k_0+i\epsilon)^2-\boldsymbol{k}\cdot \boldsymbol{k}}
$$

---
具体计算结果是
$$
\begin{aligned}
    D^{(+)}(x,x')&=\frac{\eta(x_0-x_0')}{4\pi R}\delta(x_0-x_0'-R)\\
    &=\frac{\eta(x_0-x_0')}{2\pi}\delta[(x-x')^2]
\end{aligned}
$$
利用了
$$
\begin{aligned}
    \delta[(x-x')^2]&=\delta[(x_0-x_0')^2-(x-x')^2]\\
    &=\delta[(x_0-x_0')^2-R^2]\\
    &=\delta[(x_0-x_0'-|R|)(x_0-x_0'+|R|)]\\
    &第二项恒正,忽略\\
    &=\delta(x_0-x_0'-R)
\end{aligned}\\
且\ \ \delta[f(\tau)]=\sum_i \frac{\delta (\tau-\tau_i)}{|\displaystyle\frac{df}{d\tau}|_{\tau_i}}
$$

现在可以写出电磁势四维协变解
$$
A^\mu(x)=\frac{4\pi}{c}\int d^4xD^{(+)}(x,x')J^\mu(x')
$$

带电粒子世界线取为 $r^\mu(\tau)$ , 则点电荷电流密度四矢量为
$$
J^\mu(x)=ec^2\int d\tau u^\mu(\tau)\delta^4[(x-r(\tau))^2]=(\rho c,\rho \boldsymbol{v})
$$
由于 $\delta$ 函数的存在, 积分只在某个特定时间有贡献, 满足光锥条件, 此时粒子发射电磁波与观测这两个事件是类光的, 不变间隔为 0. 发射电磁波的是粒子世界线与观测点过去光锥的交点.

---

**李纳-维谢尔势:**
$$
A^\mu(x)=\frac{eu^\mu(\tau)}{u\cdot [x-r(\tau)]}|_{\tau=\tau_0}
$$
将这个表达式写成三维形式更加直观
$$
\Phi(\boldsymbol{x},t)=[\frac{e}{(1-\boldsymbol{\beta}\cdot\boldsymbol{n})R}]_{ret}\\
\ \\
\boldsymbol{A}(\boldsymbol{x},t)=[\frac{e\boldsymbol{\beta}}{(1-\boldsymbol{\beta}\cdot\boldsymbol{n})R}]_{ret}
$$
其中 $\boldsymbol{n}$ 是粒子发射电磁波时的位置指向观测点的单位矢量

原则上, 由上面的势经过微分就可以得到运动电荷的电磁场, 但是这个过程必须正确处理推迟效应, 因而比较复杂.

**运动电荷的电磁场**
$$
\boldsymbol{E}=[\frac{e(\boldsymbol{n}-\boldsymbol{\beta})}{\gamma
^2(1-\boldsymbol{\beta}\cdot\boldsymbol{n})^3R^2}+\frac{e}{c}\frac{\boldsymbol{n}\times[(\boldsymbol{n}-\boldsymbol{\beta})\times\dot{\boldsymbol{\beta}}]}{(1-\boldsymbol{\beta}\cdot\boldsymbol{n})^3R}]_{ret}\\
\ \\
\boldsymbol{B}=(\boldsymbol{n}\times\boldsymbol{E})_{ret}
$$
电场的第一项是典型的静场, 正比于 $R^{-2}$ ,第二项是典型的辐射场, 正比于 $R^{-1}$ 并且正比于粒子加速度.

李纳-维谢尔势 的另一种推导方式就是先在静止系写出库伦场然后作洛伦兹变换, 但是这预先假定了电磁势只依赖于粒子的速度, 所以得不到有关加速度的第二项

##<font color='red'>$\S 2$ </font>拉莫尔公式与汤姆孙散射

带电粒子辐射的功率只来自于电磁势的第二项. 在 $\beta\ll1$ 的近似下电场的辐射场部分可以写成
$$
\boldsymbol{E}=[\frac{e}{c}\frac{\boldsymbol{n}\times[\boldsymbol{n}\times\dot{\boldsymbol{\beta}}]}{R}]_{ret}
$$
这样就可以写出辐射场的功率
$$
\frac{dP}{d\Omega}=\frac{c}{4\pi}R[\boldsymbol{E}\times\boldsymbol{H}]=\frac{e^2}{4\pi c^3}|\dot{\boldsymbol{v}}|^2\sin^2\Theta
$$
立体角积分得到总功率, 第一行就是 **拉莫尔公式**
$$
\begin{aligned}
    P&=\frac{2}{3}\frac{e^2}{c^3}|\dot{\boldsymbol{v}}|^2\\
    &=\frac{2}{3}\frac{e^2}{m^2c^3}\frac{d\boldsymbol{p}}{dt}\cdot\frac{d\boldsymbol{p}}{dt}\\
    &=-\frac{2}{3}\frac{e^2}{m^2c^3}\frac{dp^\mu}{d\tau}\cdot\frac{dp_\mu}{d\tau}\\
    &=\frac{2}{3}\frac{e^2}{c}\gamma^6[(\dot{\boldsymbol{\beta}})^2-(\boldsymbol{\beta}\times\dot{\boldsymbol{\beta}})^2]\\
    &(dt=\gamma d\tau)\\
\end{aligned}
$$
最后这一行就是 **李纳公式**, 是拉莫尔公式的相对论性推广
由于能量和时间都是四矢量的零分量, 所以辐射功率是一个洛伦兹不变量

##<font color='red'>$\S 3$ </font>相对论性加速电荷的辐射

利用运动带电粒子电场的远场项,写出坡印廷矢量沿 $\boldsymbol{n}$ 的投影 $(\boldsymbol{S}\cdot\boldsymbol{n})_{ret}$, 表示在 $(t,\boldsymbol{x})$ 观测到的能流.
粒子在 $t'=T_1$ 到 $t'=T_2$ 之间辐射的总能量
$$
E=\int_{T_1+R(T_1)/c}^{T_2+R(T_2)/c}(\boldsymbol{S}\cdot\boldsymbol{n})_{ret}dt=\int_{T_1}^{T_2}(\boldsymbol{S}\cdot\boldsymbol{n})\frac{dt}{dt'}dt'
$$
我们想知道的物理量是 $\displaystyle(\boldsymbol{S}\cdot\boldsymbol{n})\frac{dt}{dt'}$, 由 $dt'-dt=-\displaystyle\frac{d|\boldsymbol{x}=\boldsymbol{r}(t')|}{c}$, 得到 $dt=dt'(1-\boldsymbol{\beta}\cdot\boldsymbol{n})$

所以**相对论性粒子辐射角功率**为
$$
\frac{dP(t')}{d\Omega}=R^2\displaystyle(\boldsymbol{S}\cdot\boldsymbol{n})\frac{dt}{dt'}=\frac{e^2}{4\pi c}\frac{|\boldsymbol{n}\times[(\boldsymbol{n}-\boldsymbol{\beta})\times\dot{\boldsymbol{\beta}}]|^2}{(1-\boldsymbol{\beta}\cdot\boldsymbol{n})^5}\\
$$

对于直线加速的粒子, 功率角分布可以用角度表示为 $\displaystyle\frac{e^2\dot{v}^2}{4\pi c^3}\frac{\sin\theta^2}{(1-\beta \cos\theta)^5}$ 
功率极大值的角度为 $\cos\theta_m=\displaystyle\frac{\sqrt{1+15\beta^2}-1}{3\beta}$
粒子速度越趋近光速, 辐射会越集中于粒子速度方向.

圆周运动下也能用极坐标表示出角分布
$$
\frac{dP(t')}{d\Omega}=\frac{e^2}{4\pi c^3}\frac{\dot{v}^2}{(1-\beta \cos\theta)^3}[1-\frac{\sin^2\theta \cos^2\phi}{\gamma^2(1-\beta \cos\theta)^2}]
$$

相同情况下, 回旋粒子加速器在辐射中损耗的能量是直线加速器的 $\gamma^2$ 倍, 这个能量是相当可观的.

##<font color='red'>$\S 4$ </font>粒子辐射的频谱

对于频谱的分析一般采用观测者时间 t, 修正后将这个观测者角分布记作 A(t).
$$
\frac{d P(t)}{d \Omega_{\mathbf{n}}}=\frac{e^2}{4 \pi c}\left[\frac{\mathbf{n} \times[(\mathbf{n}-\boldsymbol{\beta}) \times \dot{\boldsymbol{\beta}}]}{(1-\boldsymbol{\beta} \cdot \mathbf{n})^3}\right]_{\mathrm{ret}}^2 \equiv|\mathbf{A}(t)|^2
$$
要计算频谱, 对时间谱作傅里叶变换
$$
\mathbf{A}(\omega)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty\mathbf{A}(t)e^{i\omega t}dt
$$
假设频率是正的, 并且 $\mathbf{A}(t)$ 是实矢量场.
$$
\mathbf{A}(\omega)=\mathbf{A}(-\omega)^*\\
\frac{d^2I}{d\Omega d\omega}\equiv|\mathbf{A}(\omega)|^2+|\mathbf{A}(-\omega)|^2=2|\mathbf{A}(\omega)|^2\\
~\\
\frac{dW}{d\Omega}=\int_{-\infty}^\infty|\mathbf{A}(t)|^2dt=\int_{-\infty}^\infty|\mathbf{A}(\omega)|^2d\omega=\int_{0}^\infty\frac{d^2I}{d\Omega d\omega}d\omega
$$
带入 $\mathbf{A}(t)$ 的具体形式得到
$$
\mathbf{A}(\omega)=\sqrt{\frac{e^2}{8 \pi^2 c}} \int_{-\infty}^{\infty} e^{i \omega\left(t^{\prime}+R\left(t^{\prime}\right) / c\right)} \frac{\mathbf{n} \times[(\mathbf{n}-\boldsymbol{\beta}) \times \dot{\boldsymbol{\beta}}]}{(1-\boldsymbol{\beta} \cdot \mathbf{n})^2} d t^{\prime}
$$

##<font color='red'>$\S 5$ </font>同步辐射的频谱