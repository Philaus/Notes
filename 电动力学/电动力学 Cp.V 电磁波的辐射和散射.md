# Cp.V 电磁波的辐射和散射

电动力学通常采用洛伦兹规范: $\displaystyle\nabla\cdot A+\frac{1}{c^2}\frac{\partial \varphi}{\partial t}=0$, 方程应用这个规范能显示出良好的对称性.
将电磁势和规范带入麦克斯韦方程得到**达朗贝尔方程**:
$$
\begin{cases}
\displaystyle\nabla^2A-\frac{1}{c^2}\frac{\partial A}{\partial t}=-\mu_0J\\
~\\
\displaystyle\nabla^2\varphi-\frac{1}{c^2}\frac{\partial \varphi}{\partial t}=-\frac{\rho}{\epsilon_0}
\end{cases}
$$

对于平面波情形, 应用洛伦兹规范后电磁势仍然不能唯一确定 (采用库伦规范不会有这个问题), 此时最简单的选择是令 $k\cdot A=0$, 也就是磁矢势只有横向分量.

## <font color='red'>$\S 1$  </font>电磁波动方程的推迟解

电磁势的波动方程可以统一写为 $\displaystyle\nabla^2\Phi-\frac{1}{c^2}\frac{\partial^2 \Phi}{\partial t^2}=-4\pi f(x,t)$, 知道了源的分布即可求解电磁势.

所有函数对时间傅里叶变换, 满足亥姆霍兹方程:
$$
(\nabla^2+k^2)\tilde{\Psi}(x,\omega)=-4\pi \tilde{f}(x,\omega)
$$
求解非齐次亥姆霍兹方程, 先求解相应的格林函数:
$$
G_k(R)=\frac{e^{\pm \mathrm{i}kr}}{R}
$$
其中正负号分别代表推迟和超前格林函数

$$
(\nabla^2-\frac{1}{c^2}\frac{\partial^2 }{\partial t^2})G=-4\pi\delta^3(R)\delta(\tau)\\
~\\
G=\frac{1}{2\pi}\int_\infty d\omega \frac{e^{\pm \mathrm{i}kr}}{R}e^{- i\omega \tau}
$$
如果介质是不色散的真空, 那么这个解就是推迟 $\delta$ 势.
$$
G=\frac{\delta(\tau\mp\frac{R}{c})}{R}=\frac{\delta(t-[t'\pm\frac{|x-x'|}{c}])}{|x-x'|}
$$
对均匀空间点源函数积分可以写出对应的推迟势:
$$
A(x,t)=\frac{\mu_0}{4\pi}\int d^3x'\frac{J(x',t-R/c)}{R}\\
~\\
\varphi(x,t)=\frac{1}{4\pi\epsilon_0}\int d^3x'\frac{\rho(x',t-R/c)}{R}\\
$$

## <font color='red'>$\S 2$  </font>谐振电荷和电流分布的电磁辐射

假设电流和电荷分布随时间的变化是谐振的, 且满足电荷守恒连续性方程.

磁矢势关于位置的部分就可以写出, 时间分量为同频加推迟相移, 标势可以用洛伦兹规范得到.
$$
A(x)=\frac{\mu_0}{4\pi}\int d^3x'J(x')\frac{e^{\mathrm{i}kR}}{R}
$$
$e^{\mathrm{i}kR}$ 代表了传播至 x 点时的相位滞后 $kR=\omega R/c$

进一步可以计算场量
$$
H=\frac{1}{\mu_0}\nabla\times A\\
~\\
E=\frac{iZ_0}{k}\nabla\times H
$$

---

近区: $r\ll \lambda,~kr\rightarrow 0,~e^{ikr}\approx1$, 此时推迟效应可以忽略, 近区的场近似为一个稳定场, 场强与 r 平方反比. 近区的场会反过来影响场源, 所以要通过求解边值问题才能给出准确解.

远区: 假设关注的尺度 r 和波长 $\lambda$ 总是远大于辐射源的尺度 d, 并且 $r\gg \lambda,~kr\gg 1$.
对 R 做关于 x' 的泰勒展开, $|x-x'|\approx r-n\cdot x'$ ,n 为 r 方向的单位矢量.

例如最低阶可以表示为
$$
A(x)=\frac{\mu_0e^{\mathrm{i}kr}}{4\pi r}\int d^3x'J(x')e^{\mathrm{i}kn\cdot x'}
$$
更高阶的展开可以利用
$$
\frac{e^{\mathrm{i}k|x-x'|}}{|x-x'|}=\frac{e^{\mathrm{i}kr}}{r}(1+\frac{n\cdot x'}{r}+\dots)(1-\mathrm{i}k(n\cdot x')+\dots)
$$

## <font color='red'>$\S 3$  </font>电偶极辐射, 磁偶极辐射, 电四极辐射

保留展开式的首项, 得到
$$
\begin{aligned}
    A(x)&=\frac{\mu_0e^{\mathrm{i}kr}}{4\pi r}\int d^3x'~J(x')\\
    &=-\frac{\mu_0e^{\mathrm{i}kr}}{4\pi r}\int d^3x'~x'(\nabla'\cdot J)\\
    &=-i\omega\frac{\mu_0e^{\mathrm{i}kr}}{4\pi r}\int d^3x'~x'\rho(x')\\
    &=-\frac{i\mu_0\omega }{4\pi }\boldsymbol{p}\frac{e^{\mathrm{i}kr}}{r}\\
\end{aligned}
$$
(已经假设了 $\dot{\boldsymbol{p}}=-i\omega\boldsymbol{p}$, 一般地 $\dot{\boldsymbol{p}}=\int \boldsymbol{J}(\boldsymbol{x}')~d^3x'$)
这就是电偶极辐射的势, 其中 $\boldsymbol{p}$ 是场源复电极矩的振幅

可以计算出电磁场为
$$
\begin{cases}
\boldsymbol{H}&=\displaystyle\frac{ck^2}{4\pi}(\boldsymbol{n}\times\boldsymbol{p})\frac{e^{\mathrm{i}kr}}{r}(1-\frac{1}{\mathrm{i}kr})\\
~\\
\boldsymbol{E}&=\displaystyle\frac{1}{4\pi \epsilon}\{k^2(\boldsymbol{n}\times\boldsymbol{p})\times\boldsymbol{n}\frac{e^{\mathrm{i}kr}}{r}\\
&+[3\boldsymbol{n}(\boldsymbol{n}\cdot\boldsymbol{p})-\displaystyle\boldsymbol{p}](\frac{1}{r^3}-\frac{\mathrm{i}k}{r^2})e^{\mathrm{i}kr}\}
\end{cases}
$$

磁场总是与方向向量 $\boldsymbol{n}$ 垂直, 是围绕磁极的圆周. 电场线沿经度方向, 由于 $\nabla\cdot E=0$, 电场线必须闭合, 在近场区有平行于 $\boldsymbol{n}$ 的分量, 类似于一个静电偶极场, 在远场区略去高次项近似为只有横向分量.
电磁辐射场有 TEM 波的形式.

在远场区电磁场都显示出球面波辐射场的形式
$$
\begin{cases}
\boldsymbol{H}=\displaystyle\frac{ck^2}{4\pi}(\boldsymbol{n}\times\boldsymbol{p})\frac{e^{\mathrm{i}kr}}{r}\\
\boldsymbol{E}=Z_0\boldsymbol{H}\times\boldsymbol{n}
\end{cases}
$$

远场区辐射能流
$$
S=\frac{|p''|^2}{32\pi^2\varepsilon_0 c^3r^2}\rm{sin}^2\theta ~\boldsymbol{e}_r
$$
辐射功率角分布可以用坡印廷矢量在无穷远处的实部获得
$$
\frac{dP}{d\Omega_n}=\frac{1}{2}\rm{Re}[r^2\boldsymbol{n}\cdot(\boldsymbol{E}\times\boldsymbol{H}^*)]_{r\rightarrow\infty}
$$
对于电偶极辐射, 这个角分布是
$$
\frac{c^2Z_0}{32\pi^2}k^4|\boldsymbol{p}|^2\rm{sin}^2\theta
$$
积分得到电偶极辐射总功率
$$
\frac{\omega^4Z_0}{12\pi c^2}|\boldsymbol{p}|^2
$$
利用电子元件发射电磁辐射时, 总发射功率等于电路上的额外负载, 可以等效为一个辐射电阻.

---

观察展开式的下一项
$$
A(x)=\frac{\mu_0e^{\mathrm{i}kr}}{4\pi r}(\frac{1}{r}-\mathrm{i}k)\int d^3x'~(\boldsymbol{n}\cdot\boldsymbol{x}')J(x')
$$
将 $(\boldsymbol{n}\cdot\boldsymbol{x}')J(x')$ 分为对称和反对称部分
$$
(n_jx_j')J_i=\frac{1}{2}n_j(x_j'J_i+J_jx_i')+\frac{1}{2}n_j(x_j'J_i-J_jx_i')
$$
反对称部分对空间积分成为体系的磁矩
$$
\boldsymbol{m}=\frac{1}{2}\int d^3x'~[\boldsymbol{x}'\times\boldsymbol{J}(\boldsymbol{x}')]
$$

$$
\boldsymbol{A}(x)=\frac{\mathrm{i}k\mu_0}{4\pi }(\boldsymbol{n}\times \boldsymbol{m})\frac{e^{\mathrm{i}kr}}{r}(1-\frac{1}{\mathrm{i}kr})
$$

$$
\begin{cases}
\boldsymbol{E}&=-\displaystyle\frac{Z_0k^2}{4\pi}(\boldsymbol{n}\times\boldsymbol{m})\frac{e^{\mathrm{i}kr}}{r}(1-\frac{1}{\mathrm{i}kr})\\
~\\
\boldsymbol{H}&=\displaystyle\frac{1}{4\pi}\{k^2(\boldsymbol{n}\times\boldsymbol{m})\times\boldsymbol{n}\frac{e^{\mathrm{i}kr}}{r}\\
&+[3\boldsymbol{n}(\boldsymbol{n}\cdot\boldsymbol{m})-\displaystyle\boldsymbol{m}](\frac{1}{r^3}-\frac{\mathrm{i}k}{r^2})e^{\mathrm{i}kr}\}
\end{cases}
$$

磁偶极电磁场的形式与电偶极完全一样, 只需要作下面的替换
$p\rightarrow m/c, ~E\rightarrow Z_0H, ~Z_0H\rightarrow -E$
$$
\frac{dP}{d\Omega}=\frac{Z_0}{32\pi^2}k^4|\boldsymbol{m}|^2\rm{sin}^2\theta
$$

$$
P=\frac{Z_0}{12\pi}k^4|\boldsymbol{m}|^2
$$

---

继续讨论上一小节中的对称部分, 利用分部积分和电荷连续性方程:
$$
\frac{1}{2}\int~d^3x'~n_j(x_j'J_i+J_jx_i')=\frac{-i\omega}{2}\int ~d^3x'~x'(n'\cdot x')\rho(x')
$$

$$
\begin{aligned}
    \boldsymbol{A}(x)&=-\frac{ck^2\mu_0}{8\pi }\frac{e^{\mathrm{i}kr}}{r}(1-\frac{1}{\mathrm{i}kr})\int ~d^3x'~x'(n'\cdot x')\rho(x')\\
    &=-\frac{\mathrm{i}k\mu_0}{24\pi }\frac{e^{\mathrm{i}kr}}{r}(1-\frac{1}{\mathrm{i}kr})\boldsymbol{n}\cdot\boldsymbol{D}
\end{aligned}
$$

如果仅考虑远场区的电磁场:
$$
\begin{cases}
\boldsymbol{E}&=\mathrm{i}kZ_0(\boldsymbol{n}\times \boldsymbol{A})\times \boldsymbol{n}/\mu_0\\
\boldsymbol{B}&=\mathrm{i}k\boldsymbol{n}\times \boldsymbol{A}\\
\boldsymbol{H}&=-\displaystyle\frac{ick^3}{24\pi}\frac{e^{\mathrm{i}kr}}{r}\boldsymbol{n}\times(\boldsymbol{D} \cdot \boldsymbol{n})
\end{cases}
$$
电四极矩是一个对称而且无迹的二阶张量:
$$
D_{ij}=\int~d^3x'~[3x_i'x_j'-(x'\cdot x')\delta_{ij}]\rho(x')
$$

$$
\frac{dP}{d\Omega}=\frac{c^2Z_0}{1152\pi^2}k^6|[\boldsymbol{n}\times(\boldsymbol{D}\cdot\boldsymbol{n})]\times\boldsymbol{n}|^2
$$

$$
P=\frac{c^2Z_0}{1440\pi}k^6D_{ij}D^*_{ij}
$$

## <font color='red'>$\S 4$  </font>电磁波的衍射

衍射是电磁波在传播中透过或者绕过障碍物行进的现象, 由于衍射涉及到物质结构的具体形式所以十分多样化.

衍射的一般问题就是根据边界条件解出在物体前后的电磁场分布, 尤其是障碍物后方的角分布, 即衍射图样. 衍射理论的基础是分波前惠更斯原理.

电磁场由两个互相耦合的矢量场 E 和 B 构成．用严格的矢量场理论来讨论衍射间题较为复杂．一般在光学中常常忽略场的矢量性质，而把电磁场的每一直角分量看作标量场，用标量场的衍射理论来求解．当衍射角不大时这种方法是较好的近似.

对于电磁场任意直角分量, 孤立地将其视为一个标量场, 应用边界上的函数值和导数值表示出区域内的值, 这就是标量衍射理论.

利用亥姆霍兹方程的格林函数形式写出表达式
$$
(\nabla^2+k^2)\psi=0\\
(\nabla^2+k^2)G=-4\pi\delta^3(x-x')\\
G(x,x')=\frac{e^{\mathrm{i}kr}}{r}
$$
带入格林公式得到**基尔霍夫公式**
$$
\psi(x)=-\frac{1}{4\pi}\oiint_{\partial V}~\frac{e^{\mathrm{i}kr}}{r}e_n\cdot[\nabla'\psi+(\mathrm{i}k-\frac{1}{r})e_r\psi]dS'
$$
这就是惠更斯原理的数学表达式, 将区域内部的场用区域边界上的值和导数表达出来.

公式中 $e^{\mathrm{i}kr}/r$ 表示由界面上的点 x' 向区域内的点 x 发射的球面波, 波振幅的强度由 x' 点的 $\psi$ 和 $\nabla'\psi$ 决定. 表明界面上的每一点都是一个次级光源, 区域内的场是这些次级光源的辐射的叠加.

## <font color='red'>$\S 5$  </font>电磁波的散射



