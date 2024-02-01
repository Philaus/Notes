# Cp. VII 相对论性电动力学

## <font color='red'>$\S 1$  </font>自由粒子的拉氏量与运动方程

一个粒子的作用量是拉氏量对时间的积分, 粒子的运动方程由最小作用量原理给出. 
力学系统的作用量应当是一个洛伦兹不变量 (即洛伦兹标量)
$$
S=\displaystyle\int Ldt=-mc\int ds=-mc^2\int d\tau
$$
$d\tau$ 是粒子的固有时间间隔, 实际上就是在相对于粒子静止的参照系中的时间间隔

作用量对于粒子世界线的重参数化是不变的. 粒子的世界线可以描述为一组参数方程:
$$
x^\mu=x^\mu(\tau)
$$
$\tau$是一个描写粒子世界线的参数 (例如粒子的固有时, 或者固有时的任意单调增函数), 于是自由粒子作用量可以写为:
$$
S=\displaystyle -mc\int d\tau\sqrt{(\frac{dx^\mu}{d\tau})(\frac{dx_\mu}{d\tau})}
$$

世界线还可以用其他参数来描写, 比如引入 $\tilde{\tau}$, 这就是重参数化变换:
$$
x^\mu=x^\mu(\tau)=x^\mu(\tau(\tilde{\tau}))
$$

---

相对论性自由粒子的不变间隔, 拉格朗日量, 正则动量, 能量:
$$
ds=\sqrt{c^2dt^2-d\boldsymbol{x}^2}=cdt\beta\\
L=-mc^2/\gamma\\
\boldsymbol{p}=\displaystyle\frac{\partial L}{\partial \boldsymbol{v}}=\gamma m\boldsymbol{v}\\
E=p\cdot\boldsymbol{v}-L=\gamma mc^2
$$

粒子的动量, 能量和运动方程也可以用纯粹四维协变的形式写出

定义一个协变四矢量 $u_\mu=\displaystyle\frac{dx_\mu}{ds}$, 称为粒子的四维速度
这样定义的四速度是无量纲的, 有的地方会定义为 $u_\mu=\displaystyle\frac{dx_\mu}{d\tau}$, 其中 $ds=cd\tau$, 这样四速度具有速度量纲.
通常意义上的速度 u 是用参考系 K 的时间量度的位移变化率, 而 $u_\mu$ 是用固有时量度的位移变化率.
$$
\frac{dt}{d\tau}=\frac{1}{\sqrt{1-\frac{u^2}{c^2}}}\equiv \gamma_u
$$
按照固有时的定义:
$$
u_\mu=\gamma_u(c,\boldsymbol{u})\\
a_\mu=\gamma_u^4(\boldsymbol{u}\cdot \boldsymbol{a}/c,~\gamma^2\boldsymbol{a}+(\boldsymbol{u}\cdot\boldsymbol{a})\boldsymbol{u}/c^2)\\
$$

---

对作用量进行变分;
$$
\delta S=-mc\displaystyle\int \delta\sqrt{dx^\mu dx_\mu}=-mc\int \frac{dx_\mu \delta dx^\mu}{ds}
$$
分部积分, 第一项由于 $\delta x^\mu$ 在上下限处为零, 只剩下第二项
由作用量变分为零, 得到 $\displaystyle\frac{du_\mu}{ds}=0$, 表明粒子以常速度运动. 
与 $x^\mu$ 共轭的四动量为:
$$
p^\mu=mcu^\mu=mc\frac{dx_\mu}{ds}=(E/c, \boldsymbol{p})
$$
即四动量的时间分量是相对论性能量 (除以 c), 空间分量是粒子的相对论性动量. 

在一个均匀时空 (时空具有时间和空间平移不变性) 中进行的物理过程中, 力学系统的四动量一定守恒. 

## <font color='red'>$\S 2$  </font>电磁场中粒子的拉氏量

一个微观粒子所带的电荷也是洛伦兹不变量. 带电粒子会在空间产生电磁场, 在外电磁场中会发生相互作用. 
假设外电磁场用四矢量势 $A_\mu(x)=(\Phi(x),\boldsymbol{A}(x))$ 描写, 那么唯一可能洛伦兹不变的作用量必定可以写成:
$$
S=-mc\displaystyle\int ds-\frac{e}{c}\int A_\mu(x)dx_\mu
$$
利用作用量对时间的积分表达, 可以写出外电磁场中相对论性粒子的拉氏量;
$$
L=-mc^2\displaystyle/\gamma+\frac{e}{c}\boldsymbol{v}\cdot\boldsymbol{A}-e\Phi=-mc^2\displaystyle/\gamma-\frac{e}{c}A^\mu u_\mu
$$
立即得到粒子的正则动量和哈密顿量:
$$
\boldsymbol{P}=\frac{\partial L}{\partial \boldsymbol{v}}=\gamma m\boldsymbol{v}+\frac{e}{c}\boldsymbol{A}=\boldsymbol{p}+\frac{e}{c}\boldsymbol{A}\\
~\\
\mathscr{H}=\boldsymbol{v}\cdot\boldsymbol{P}-L=\sqrt{((P-qA)c)^2+(mc^2)^2}+q\phi
$$
正则四动量
$$
P^\mu=p^\mu+qA^\mu=(\mathscr{H}/c, P)
$$
四维力, 其中 u 和 f 分别是三维的速度和力
$$
F^\mu=\gamma(\boldsymbol{f}\cdot \boldsymbol{u}/c, \boldsymbol{f})
$$
三维和四维洛伦兹力密度:
$$
f=\rho E+J\times B\\
f^\mu=F^{\nu\mu}J_\nu=((E\cdot J)/c, f)
$$

## <font color='red'>$\S 3$  </font>运动方程与规范不变性

四维的运动方程 $\dot{P^\mu}=-\displaystyle\frac{\partial \mathscr{H}}{\partial q_\mu}$ 实际上包含三维力方程和能量方程:
$$
\begin{cases}
    \displaystyle\frac{d\boldsymbol{p}}{dt}=\boldsymbol{F}=e\boldsymbol{E}+\frac{e}{c}\boldsymbol{v}\times\boldsymbol{B}\\
    ~\\
    \displaystyle\frac{dE}{dt}=\boldsymbol{F}\cdot \boldsymbol{v}=e\boldsymbol{v}\cdot\boldsymbol{E}
\end{cases}
$$
一个粒子的拉氏量可以相差任意函数对时间的全导数而不改变运动方程. 对一个相对论性粒子在电磁场中的作用量, 电磁势在变换 $A_\mu(x)\rightarrow A_\mu(x)+\partial_\mu f(x)$ 下不变. 这称为电磁场的规范对称性, 上面的变换称规范变换. 

其中, 四维微商算符的具体形式是:
$$
\partial_\mu\equiv\frac{\partial }{\partial x_\mu}=(\frac{1}{c}\frac{\partial }{\partial t},\nabla)\\
\partial_\mu\partial_\mu\equiv\frac{\partial }{\partial x_\mu}\frac{\partial }{\partial x_\mu}=\nabla^2-\frac{1}{c^2}\frac{\partial^2 }{\partial t^2}
$$

与自由粒子的情形类似, 对电磁场中的作用量变分可以得到运动方程:
$$
\begin{aligned}
    \delta S&=\displaystyle mc\int\frac{du_\mu}{ds}\delta x^\mu ds-\frac{e}{c}\int(\delta A_\mu dx^\mu+ A_\mu\delta dx^\mu)\\
    &=\displaystyle mc\int\frac{du_\mu}{ds}\delta x^\mu ds-\frac{e}{c}\int(\partial_\nu A_\mu\delta x^\nu dx^\mu-\partial_\nu A_\mu d x^\nu \delta x^\mu)
\end{aligned}
$$
第二步中, 先应用 $\delta A_\mu=\partial_\nu A_\mu\delta x^\nu$, 第二项 $A_\mu\delta dx^\mu$ 分部积分, 由 $\delta x^\mu$ 端点为 0 和 $dA_\mu=\partial_\nu A_\mu dx^\nu$ 得出

第二个积分中x的指标可以互换, 从而将第二项的两个项合并, 给出相对论性粒子四维协变形式的运动方程;
$$
mc\displaystyle\frac{du_\mu}{dt}=\frac{e}{c}F_{\mu\nu}u^\nu\\
~\\
电磁场场强二阶反对称张量:F_{\mu\nu}=\partial_\mu A_\nu-\partial_\nu A_\mu\\
洛伦兹力密度:f_\mu=\rho F_{\mu\nu}u^\nu=F_{\mu\nu}J^\nu=(\boldsymbol{E}\cdot \boldsymbol{J}/c,\boldsymbol{f})
$$
影响粒子运动方程的不是电磁四矢量, 而是电磁场张量, 电磁场张量在规范变换下不变. 在经典电动力学中, 电磁势是不可直接测量的, 电磁场张量才是粒子直接感受到的相互作用. 

具体写出电磁场张量的分量:
$$
F_{\mu\nu}=\begin{vmatrix}
    0& E_1& E_2& E_3\\
    -E_1 & 0&-B_3 &+B_2 \\
    -E_2 &+B_3 & 0& -B_1\\
    -E_3 &-B_2 &+B_1 & 0\\
\end{vmatrix}
$$
可见, 在狭义相对论中, 电磁场结合成一个整体. 
电场出现在张量的时空部分, 磁场出现在张量的纯空间部分. 

对于 $F^{\mu\nu}$, 由于时间指标升降不改变, 空间分量反号, 所以 $F^{\mu\nu}$ 的电场部分差一个负号, 而磁场部分不变. 

## <font color='red'>$\S 4$  </font>电磁场的作用量与电动力学的协变性

电磁场场强在洛伦兹变换下按照一个二阶反对称张量进行:
$$
F'^{\mu\nu}=\Lambda^{\mu}{}_{\alpha}\Lambda^{\nu}{}_{\beta} F^{\alpha\beta}
$$

具体地用分量写出电磁场在一般洛伦兹变换下的规则是相当复杂的, 但是如果变换仅含有推促, 而没有三维空间的转动, 那么可以得到明显表达式:
$$
E'=\gamma(E+\beta\times cB)-\displaystyle\frac{\gamma^2}{1+\gamma}(\beta\cdot E)\beta\\
B'=\gamma(B-\beta\times E/c)-\displaystyle\frac{\gamma^2}{1+\gamma}(\beta\cdot B)\beta\\
$$

---

按照电磁场张量的反对称特性, 给出其比安基 (bianchi) 恒等式:
$$
\partial_\mu F_{\nu\alpha}+\partial_\nu F_{\alpha\mu}+\partial_\alpha F_{\mu\nu}=0
$$
这个式子用三维形式写出, 就是麦克斯韦方程组中的两个齐次方程 (无源磁高斯方程和法拉第方程)

比安基恒等式的另一种表示方法是定义对偶张量:
$$
\partial_\mu\tilde{F_{\mu\nu}}=0\\
其中~\tilde{F_{\mu\nu}}=\frac{1}{2}\epsilon_{\mu\nu\alpha\beta}F^{\alpha\beta}
$$
$\epsilon_{\mu\nu\alpha\beta}$ 是四维完全反对称张量, 具有与三维的列维-奇塔张量相同的轮换性, 而且 $\epsilon_{\mu\nu\alpha\beta}$ 和 $\epsilon^{\mu\nu\alpha\beta}$ 相差一个负号
$$
\tilde{F_{\mu\nu}}=\begin{vmatrix}
    0& -B_1& -B_2& -B_3\\
    B_1 & 0&-E_3 &+E_2 \\
    B_2 &+E_3 & 0& -E_1\\
    B_3 &-E_2 &+E_1 & 0\\
\end{vmatrix}
$$
对偶张量中电场和磁场的位置刚好互换. 

---

下面研究利用电磁场场强张量构造电磁场本身的作用量, 这个作用量必须是一个洛伦兹标量
构造需要两个场强张量, 可能的组合有 $F_{\mu\nu}F^{\mu\nu}\propto(E^2-B^2)$ 和 $\epsilon_{\mu\nu\alpha\beta}F^{\mu\nu}F^{\alpha\beta}\propto(E\cdot B)$ 
后者是一个赝标量, 因为它在宇称变换下变号, 所以采用前者

($F_{\mu\nu}F_{\mu\nu}=-4E\cdot B/c$,  $F_{\mu\nu}F^{\mu\nu}=-2(E^2/c^2-B^2)$)

电磁场的作用量一定可以写为:
$$
S_{em}=-\displaystyle\frac{1}{16\pi c}\int d^4xF_{\mu\nu}F^{\mu\nu}
$$
拉莫尔于 1900 年首先写出了这个作用量 (Maxwell-Lamor作用量). 
系数依赖于单位制的选取, 目前选用高斯单位制. 

---

为了得到电磁场的运动方程, 需要改写带电粒子与电磁场相互作用部分的作用量. 引入空间一点的电荷密度 $\rho(x)$. 总电荷量 $\rho(x)d^3x$ 是一个洛伦兹不变量. 
带电粒子作用量中与电磁场相关的那一项可以写为:
$$
\begin{aligned}
    S_{int}&=\displaystyle-\frac{e}{c}\int A_\mu dx^\mu\\
    &=\displaystyle-\frac{1}{c}\int A_\mu\rho\frac{dx^\mu}{dt}dtd^3x\\
    &=-\frac{1}{c^2}\int A_\mu\rho\frac{dx^\mu}{dt}d^4x\\
\end{aligned}
$$
发现 $\displaystyle\rho\frac{dx^\mu}{dt}$ 是一个逆变四矢量, 于是可以定义电流密度四矢量:
$$
J^\mu=\rho\frac{dx^\mu}{dt}=(c\rho, \boldsymbol{J})
$$
这样闵氏时空中的电荷守恒定律可以写成协变形式:
$$
\partial_\mu J^\mu=0
$$
将两个作用量合并起来, 得到电磁场有关的总作用量:
$$
S=S_{em}+S_{int}=-\frac{1}{c^2}\int A_\mu J^\mu d^4x-\displaystyle\frac{1}{16\pi c}\int d^4xF_{\mu\nu}F^{\mu\nu}\\
S=\int d^4x \mathscr{L}\\
\mathrm{Lagrange~density}~~\mathscr{L}=-\frac{1}{16\pi c}F_{\mu\nu}F^{\mu\nu}-A_\mu J^\mu
$$
再利用最小作用量原理 $\delta S/\delta A_\mu$ 得到在给定外源下的运动方程:
$$
\partial_\mu F^{\mu\nu}=\frac{4\pi}{c}J^\nu
$$
这就是两个有源的麦克斯韦方程


除此之外, 利用协变场量还能写出四维形式的其他重要关系式:
$$
\begin{cases}
    \partial_\mu J_\mu=0,电荷守恒定律\\
    \partial_\mu A_\mu=0,洛伦兹规范\\
    \partial_\nu \partial_\nu A_\mu=-\mu_0 J_\mu,达朗贝尔方程\\
    \begin{cases}
    \partial_\mu F^{\mu\nu}=4\pi/c~J^\nu\\
    \partial_\mu F_{\nu\alpha}+\partial_\nu F_{\alpha\mu}+\partial_\alpha F_{\mu\nu}=0,麦克斯韦方程
    \end{cases}\\
    f_\mu=\partial_\lambda T_{\mu \lambda},能量动量守恒定律
\end{cases}
$$
其中电磁场能量动量张量:
$$
T_{\mu \lambda}=\frac{1}{\mu_0}\left(F_{\mu \nu} F_{\nu \lambda}+\frac{1}{4} \delta_{\mu \lambda} F_{\nu \tau} F_{\nu \tau}\right) \\
~\\
T_{\mu \lambda}=\left[\begin{array}{cccc}
w & cg_1 & cg_2 & cg_3 \\
S_1/c & -T_{11} & -T_{12} & -T_{13}\\
S_2/c & -T_{21} & -T_{22} & -T_{23}\\
S_3/c & -T_{31} & -T_{32} & -T_{33}\\
\end{array}\right]
$$
这是一个无迹对称张量, 即 $ T_{\mu \lambda}=T_{\lambda \mu}, T_{\mu \mu}=0 $

## <font color='red'>$\S 5$  </font>运动物体中的电磁场



## <font color='red'>$\S 6$  </font>均匀静电磁场中带电粒子的运动

四矢量和坐标四矢量的耦合, 一个洛伦兹标量, 耦合的强度表征了

准静态近似, 位移电流远小于欧姆电流

电流必须为零才能稳态, 否则有耗散, 则不为稳态
静止参考系中的电场为零

粒子和场的作用量