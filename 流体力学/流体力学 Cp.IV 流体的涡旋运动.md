# Cp.IV 流体的涡旋运动

涡量的散度为零, 涡管中任意横截面上的通量保持一致, 所以可以用通量 $\Omega\sigma$ 表征涡旋的强度, 称为涡管强度.

涡管不能在流体中突然出现或消失, 因此只能在流体中自我封闭形成涡环, 或者连接到无穷远或流体边界.

展开流体微团角动量的积分表达式, 可以得到 $\boldsymbol{L}=\frac{J}{2}\boldsymbol{\Omega}$ ,所以 $\boldsymbol{\Omega}/2$ 是单位转动惯量上动量矩.

## <font color='red'>$\S 1$  </font>涡旋基本方程

假设 $\mu=Const,~\mu'=0$, 对兰姆-格罗麦卡方程两边取旋度:
$$
\frac{d\boldsymbol{v}}{dt}=\frac{\partial \boldsymbol{v}}{\partial t}+\mathrm{grad} \frac{V^2}{2}+\mathrm{rot} \boldsymbol{v}\times\boldsymbol{v}=\boldsymbol{F}-\frac{1}{\rho}\nabla p+\nu\Delta\boldsymbol{v}+\frac{1}{3}\nu\nabla(\nabla\cdot\boldsymbol{v})\\
$$
$$
\begin{aligned}
    &\frac{d\boldsymbol{\Omega}}{dt}-(\boldsymbol{\Omega}\cdot\nabla)\boldsymbol{v}+\boldsymbol{\Omega}(\nabla\cdot\boldsymbol{v})\\
    =&\nabla\times\boldsymbol{F}-\nabla\times(\frac{1}{\rho}\nabla p)+\nabla\times(\nu\Delta\boldsymbol{v})+\frac{1}{3}\nabla\times(\nu\nabla(\nabla\cdot\boldsymbol{v}))
\end{aligned}
$$
这就是涡量在假设 $\mu=Const,~\mu'=0$ 下满足的方程.
方程表明随体运动中引起单位转动惯量上动量矩变化的因素有: 外力, 压强梯度, 黏性应力, 流体元的膨胀或压缩, 涡线的拉伸压缩或扭曲.

如果流体是理想正压的而且外力有势, 则:可以将外力和密度的项作为一个函数的梯度, 从而其旋度为零, 方程变为
$$
\frac{d\boldsymbol{\Omega}}{dt}-(\boldsymbol{\Omega}\cdot\nabla)\boldsymbol{v}+\boldsymbol{\Omega}(\nabla\cdot\boldsymbol{v})=0
$$
这就是亥姆霍兹方程.

对于匀质不可压缩黏性流体, 外力有势, 方程变为:
$$
\frac{d\boldsymbol{\Omega}}{dt}-(\boldsymbol{\Omega}\cdot\nabla)\boldsymbol{v}=\nu\Delta\boldsymbol{\Omega}
$$

---
对于理想正压流体且外力有势的情况:
**开尔文定理**
沿任意封闭物质线的速度环量和通过任意物质面的涡通量在运动过程中不变.
**拉格朗日定理**
如果流体的某一部分初始有旋, 那么在之后任意时刻该部分都有旋, 反之任意时刻该部分都无旋.
**亥姆霍兹定理**
某一时刻组成涡线的流体质点在前一或后一时刻永远组成涡线, 而且涡管强度在运动中保持不变.

黏性是使流体的涡旋情况产生改变的最常见的因素, 如果存在黏性, 涡旋就会具有扩散性, 通过输运从高旋度位置向低旋度方向扩散, 最后趋于平均.

## <font color='red'>$\S 2$  </font>涡旋导出的速度场

根据涡旋分布可以推出速度分布, 如果流场是无旋的, 也可能假设出一个理想的奇点涡旋分布来作为速度的源.
定义涡层强度和涡线:
$$
\boldsymbol{\Omega}d\tau=\boldsymbol{\pi}d\sigma=\boldsymbol{\Gamma}dl
$$

将速度分解为有源无旋和有旋无源分量:
$$
\boldsymbol{v}=\boldsymbol{v}_1+\boldsymbol{v}_2=\nabla\phi+\nabla\times\boldsymbol{A}\\
\nabla\cdot\boldsymbol{v}_1=\Theta,~\nabla\times\boldsymbol{v}_2=\boldsymbol{\Omega}\\
\Delta\phi=\Theta,~\Delta \boldsymbol{A}=-\boldsymbol{\Omega}
$$
可以用泊松方程的基本解写出源函数:
$$
\phi=-\frac{1}{4\pi}\int\frac{\Theta}{r}d\tau\\
\boldsymbol{A}=\frac{1}{4\pi}\int\frac{\boldsymbol{\Omega}}{r}d\tau\\
$$
这样就表示出了速度场. 如果涡旋分布是奇点型, 可以更换积分方式, 比如涡丝诱导的速度元:
$$
d\boldsymbol{v}=\frac{\Gamma}{4\pi}\frac{d\boldsymbol{l}\times\boldsymbol{r}}{r^3}
$$
这正是毕奥-萨伐尔公式.