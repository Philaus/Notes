# Cp.I~III 静电场与静磁场

用势函数写出的波动方程:
$$
\begin{cases}
    \displaystyle\nabla^2\Phi-\frac{1}{c^2}\frac{\partial^2 \Phi}{\partial t^2}=-\rho/\epsilon_0\\
    \ \\
    \displaystyle\nabla^2A-\frac{1}{c^2}\frac{\partial^2 A}{\partial t^2}=-\mu_0J\\
\end{cases}
$$

介质边界面条件:
$$
\begin{cases}
    n\cdot(D_1-D_2)=\sigma_e\\
    n\cdot(B_1-B_2)=0\\
    n\times(E_1-E_2)=0\\
    n\times(H_1-H_2)=\sigma_J\\
\end{cases}
$$

电磁场能量密度:
$$
w=\frac{1}{2}(E\cdot D+B\cdot H)=\epsilon_0E^2=B^2/\mu_0
$$

麦克斯韦应力张量 (动量流密度张量)
$$
T_{ij}=\epsilon_0[E_iE_j+c^2B_iB_j-1/2(E\cdot E+c^2B\cdot B)\delta_{ij}]
$$
应力密度 (负号表示压力)
$$
f+\frac{\partial g}{\partial t}=\nabla\cdot T\\
T=cg\boldsymbol{e_k}\boldsymbol{e_k}=w \boldsymbol{e_k}\boldsymbol{e_k}
$$
电磁波对宏观物体表面的辐射压力: ($e_n$ 是物体外表面法向) (注意这个算出的是瞬时值, 谐波平均值是这个的 1/2)
$$
f_S=-\boldsymbol{e_n}\cdot T
$$
单位时间内区域内粒子动量的下降, 等于该区域电磁场动量的上升加通过该区域边界净流出的场对外界作用的动量变化率, 场对外界作用的动量变化率等于应力张量在边界面积分的负值.
$T_{ij}n_j$ 代表通过该处单位面积单位时间流入场的动量的 i 分量.

电磁场动量密度 $g=S/c^2=\epsilon_0\mu_0 S=\varepsilon_0E\times B=\displaystyle\frac{w}{c}e_k(即\boldsymbol{k})$
角动量密度 $\mathscr{M}=x\times g=x\times(E\times H)/c^2$

当所有场都不随时间变化, 关于电场和磁场的问题可以完全分离.

## <font color='red'>$\S 1$  </font>泊松方程与静电边值问题

均匀各向同介质中静电问题可以表示为:
$$
\begin{cases}
    \nabla\cdot D=\rho\\
    \nabla\times E=0
\end{cases}
$$
由于电场旋度为零, 可以定义静电势 $E=-\nabla \Phi$
得到泊松方程 $\nabla^2\Phi=-\rho(x)/\epsilon $

如果问题再无穷大空间求解, 那么解可以直接写出:
$$
\Phi(x)=\frac{1}{4\pi\epsilon}\int d^3x'\frac{\rho(x')}{|x-x'|}
$$

如果有限区域内存在边界, 则在边界上的面电荷分布是不能知道的, 所以仅由体电荷分布不能算出静电势.

设函数 $G$ 在内部满足:
$$
\nabla^2G=-4\pi\delta^3(x-x')
$$
并且在边界上满足边值条件, 则称其为相应的格林函数, 物理上相当于一个点电荷.

格林函数总可以写为:
$$
G(x,x')=\frac{1}{|x-x'|}+F(x,x')
$$
函数 F 满足拉普拉斯方程, 是调和函数, 需要被恰当选取来满足 G 的边值条件

利用格林公式:
$$
\int d^3x(\phi \nabla^2\psi-\psi \nabla^2\phi)=\oint dS[\phi\frac{\partial \psi}{\partial n}-\psi\frac{\partial \phi}{\partial n}]
$$
得到边值问题的格林函数解:
$$ 
\Phi(x)=\frac{1}{4\pi\epsilon}\int d^3x'G\rho(x')+\frac{1}{4\pi}\oint dS'(G\frac{\partial \Phi(x')}{\partial n'}-\Phi(x')\frac{\partial G}{\partial n'})
$$
其中势在边界上的值和偏导数由边值条件给出.
这个格林函数只是一个形式解, 后面几节将根据坐标系给出明显解.

对于狄利克雷条件, 可以选择 F 使得格林函数在边界上恒为零, 这样就抹去了边界上偏导值的影响.
对于诺依曼条件, 不能直接令边界上的偏导为零, 此时最简单的方式就是令边界上的格林函数的偏导为定值 $-4\pi/S$, 面积分的第二项就变为静电势在边界上的平均值.

---
导体中的边值关系:
1. 边界上势为常数
2. $\displaystyle\frac{\partial \Phi}{\partial n}=-\frac{\sigma}{\epsilon}$

静电能:
$$
U=\frac{1}{2}\int E\cdot D dx^3= \frac{1}{2}\sum \Phi_iQ_i=\frac{1}{2}\sum C_{ij}\Phi_i\Phi_j
$$
其中 C 的对角元是电容系数, 非对角元是感应系数.

---

导体球的镜像法结果:
$$
r'=\frac{R^2}{r}\\
Q'=-Q\frac{R}{r}
$$
## <font color='red'>$\S 2$  </font>泊松方程的分离变量法

当静电问题具有某种对称性时, 可以采用特别的坐标系来分离变量. 以下涉及的特殊函数都构成完备函数基, 所以理论上任何边值问题都可以用这些特殊函数展开, 只需要用边界确定系数.

下面给出拉普拉斯方程三种基础坐标系的分离变量结果, 对泊松方程, 总可以将无边界泊松方程的形式解叠加上一个拉普拉斯方程, 因而是等价的.

---
**直角坐标系**
$$
\Phi(x)=X(x)Y(y)Z(z)\\
X\propto e^{k_1x}, Y\propto e^{k_2y}, Z\propto e^{k_3z}\\
k_1^2+k_2^2+k_3^2=0
$$
如果某个方向的尺度是有限的, 那么参数 k 一般只能取分离的纯虚数, 形成驻波, 本征函数是三角函数.

---
**柱坐标系**
$$
\Phi(x)=Z(z)\Phi(\phi)R(r)\\
Z\propto e^{\pm kz}, \Phi(\phi)\propto e^{\pm im\phi}, R(r)\propto J_m(kr)\&N_n(kr)
$$
为什么保证静电势的单值性, m 必须为整数

对于 k ,如果是实数, 则径向函数是标准贝塞尔函数 $J_m(kr)$ $N_n(kr)$ 的线性组合, 前者在 r=0 处有限而后者发散, 要根据需要选择.
如果 k 是纯虚数, 径向函数是虚宗量贝塞尔函数 $I_m(|k|r)$ $K_n(|k|r)$ 的线性组合, 前者在 r=0 处有限而后者发散.

对有限区间条件 $[0,a]$, 柱面波解的形式一般取为 $J_m(x_{mn}r/a)$, $x_{mn}$ 是 $J_m$ 在正实轴上的第 n 个零点.

正交归一关系
$$
\int^a_0rJ_m(\frac{x_{mn}r}{a})J_m(\frac{x_{mn}'r}{a})dr=\frac{a^2}{2}[J_{m+1}(x_{mn})]^2\delta_{nn'}
$$

---
**球坐标系**
$$
\Phi(r,\theta,\phi)=\sum^\infty_{l=0}\sum^l_{m=-l}(A_{lm}r^l+\frac{B_{lm}}{r^{l+1}})Y_{lm}(\theta,\phi)
$$
$Y_{lm}(\theta,\phi)$ 是球谐函数, $A_{lm}$ $B_{lm}$ 完全由边界条件决定.

球谐函数是角动量平方算符的本征函数组
$$
\hat{L}^2Y_{lm}(\theta,\phi)=l(l+1)Y_{lm}(\theta,\phi)\\
Y_{lm}(\theta,\phi)=\sqrt{\frac{2l+1}{4\pi}\frac{(l-m)!}{(l+m)!}}P_l^{|m|}(cos\theta)e^{im\phi}
$$
球谐函数的宇称:
$$
Y_{l,-m}(\theta,\phi)=(-1)^mY_{lm}^*(\theta,\phi)
$$
球谐函数对所有 l m 模式具有正交归一性和完备性.

如果问题具有 $\phi$ 方向的对称性, 球谐函数将只含有 m=0 项, 连带勒让德函数就退化为勒让德多项式.

球谐函数的加法定理 (也就是对点源函数的展开式):
$$
\frac{1}{|x-x'|}=\sum^\infty_{l=0}\sum^l_{m=-l}\frac{4\pi}{2l+1}\frac{r^l_<}{r^{l+1}_>}Y_{lm}^*(n')Y_{lm}(n)
$$
特别的, 当问题具有关于一轴的对称性, 则 m=0, 加法定理写为:
$$
\frac{1}{|x-x'|}=\sum^\infty_{l=0}\frac{r^l_<}{r^{l+1}_>}P_l^*(cos\theta')P_l(cos\theta)
$$
勒让德多项式就是解关于幂函数展开的系数.

## <font color='red'>$\S 3$  </font>静电问题的数值解法



## <font color='red'>$\S 4$  </font>静电多极展开
利用加法定理带入静电势的形式表达式, 并且假设源区距离我们感兴趣的场区距离很远. 将所有与源区相关的量合并为一个因子, 这个因子就是与电荷分布对应的多极矩, 表示如下:
$$
q_{lm}=\int Y_{lm}^*(n')(r')^l\rho(x')d^3x'\\
\Phi(x)=\frac{1}{\epsilon_0}\sum_{l,m}\frac{1}{2l+1}q_{lm}\frac{Y_{lm}(n)}{r^{l+1}}
$$
具体计算出 $q_{lm}$ 的表达式, 每个 l 对应着一阶的矩展开, 利用同 l 不同 m 的值可以计算出各阶矩所有的分量值. 比如零阶可以计算出总电量, 一阶为电偶极矩矢量, 二阶是电四极矩矩阵.
$$
Q=\int d^3x'\rho(x')\\
p_i=\int d^3x'\rho(x')x'_i\\
D_{ij}=\int d^3x'\rho(x')(3x'_ix'_j-(r')^2\delta_{ij})\\
$$

## <font color='red'>$\S 5$  </font>静磁基本原理