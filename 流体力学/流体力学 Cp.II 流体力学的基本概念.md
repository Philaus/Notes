# Cp.II 流体力学的基本概念

研究流体的宏观运动有统计平均和连续介质两种路线. 为了保证统计平均和连续假设的成立性, 所选取的流体单元应该具有适当的时空尺度, 保证微观充分大和宏观充分小.

流体的宏观性质主要是:
1. 易流动性, 理想的流体不能承受切应力, 黏性流体在流动时可以产生切应力
2. 黏性, 流体所具有的的抵抗两层流体相对滑动速度 (一般地, 抵抗变形) 的性质称为黏性. 黏性依赖于流体性质, 大致正比于相对速度, 并且随温度显著变化.
3. 压缩性, 分子间存在量子型强排斥力和经典型弱吸引力, 流体分子具有一定的间隔, 但又不至于完全远离, 表现出具有一定的体积但没有确定形状, 加外力能轻微收缩.

使不同流体层内的平均物理量均匀化的性质称为输运性质, 流体的宏观性质是分子输运性质的统计平均. 理想流体忽略黏性, 即动量输运, 因此也经常忽略质量和能量的输运, 即扩散和热传导.

## <font color='red'>$\S 1$  </font>描写流体运动的两种方法

拉格朗日法的运动规律是特定质点 P(a,b,c) 随时间的位置函数, 欧拉法的运动规律是空间坐标下的速度场. 位置函数的运动方程是二阶 PDE, 几何表示是单粒子轨迹线 (曲线方程是位置函数消去 t); 速度函数的运动方程是一阶 PDE, 几何表示是速度分布场 (流线).
两者描述的是同一个物理过程, 所以是等价的. 实际中可以根据需要和建模计算难易度选择使用.

已知拉格朗日法和欧拉法运动描述下的互相转换:
1. L 转 E: 已知 $\boldsymbol{r}(a,b,c,t)$, 速度函数为 $\displaystyle\frac{\partial \boldsymbol{r}}{\partial t}$, 反解出三个拉格朗日坐标关于 r 的函数再带入 v 的方程即得欧拉变数中的速度方程.
2. E 转 L: 已知速度函数 $\boldsymbol{v}(\boldsymbol{r},t)=\displaystyle\frac{d\boldsymbol{r}}{dt}$, 构成 r 关于 t 的常微分方程组, 其解为 $\boldsymbol{r}(C_1,C_2,C_3,t)$, 由初始时刻 $\boldsymbol{r}=\boldsymbol{r}_0$ 确定, $\boldsymbol{r}_0$ 的三个坐标就是三个拉格朗日变数.

速度变化即加速度的来源主要是两个方面: 场的非定常性和非均匀性, 将速度对时间的全导数 (随体导数) 分为局部导数和位变导数两个部分.
$$
\frac{d\boldsymbol{v}}{dt}=\frac{\partial \boldsymbol{v}}{\partial t}+v\frac{\partial \boldsymbol{v}}{\partial s}=\frac{\partial \boldsymbol{v}}{\partial t}+(\boldsymbol{v}\cdot\nabla)\boldsymbol{v}
$$

随体导数的分解对于任意矢量或标量都成立:
$$
\frac{d\boldsymbol{a}}{dt}=\frac{\partial \boldsymbol{a}}{\partial t}+(\boldsymbol{v}\cdot\nabla)\boldsymbol{a}\\
\frac{d\phi}{dt}=\frac{\partial \phi}{\partial t}+\boldsymbol{v}\cdot\nabla\phi
$$

不可压缩流体的数学表示: $\displaystyle\frac{d\rho}{dt}=0$, 表示流体元密度的随体导数不变. 如果流体不可压缩而且匀质, 那么还有 $\nabla\rho=0$, 从而 $\displaystyle\frac{\partial \rho}{\partial t}=0$, 从而 $\rho=\mathrm{Const}$.

## <font color='red'>$\S 2$  </font>轨迹和流线

要用速度分布函数得到轨迹线, 需要先转到拉格朗日表示, 积分后消去 t.

此外, 也可以在速度场中取一个点 $M_1$, 沿该点速度向前延伸至 $M_2$ 点, 然后依次继续, 当两点间时间趋于零时折线就趋于质点的轨迹线. 已知速度场绘制流线的步骤与轨迹基本相同, 但是不需要改变时间, 只在空间中取下一个点.

流线是同一时刻空间中不同质点的运动方向的表示. 根据流线的定义, $d\boldsymbol{r}\times\boldsymbol{v}=0$, 展开写为: (其中 t 是参数, 不是自变量)
$$
\frac{dx}{v_x(a,b,c,t)}=\frac{dy}{v_y(a,b,c,t)}=\frac{dz}{v_z(a,b,c,t)}
$$

定常运动的轨迹和流线是重合的, 但在非定常运动下, 由于时间流逝 $\Delta t$ 后的速度场与初始速度场不相等, 这样轨迹和流线就不重合.
从微分方程的角度也能证明这一点, 虽然轨迹和流线的方程形式基本一致, 但是轨迹方程中 t 是自变量, 所以方程一般不同; 对于定常情况, 最终的方程中 t 可以消去, 所以是一样的.

选择不同的惯性参照系, 问题的定常性可能发生变化, 并且相应的流线和轨迹线可能截然不同.

流体中选择非轨迹且不相交的封闭曲线, 过曲线上每一点做轨迹, 得到射流面, 包围的流体称为射流; 在某一时刻选择非流线且不自相交的曲线, 过曲线上每一点做流线, 得到流面, 如果初始曲线封闭则为流管.

## <font color='red'>$\S 3$  </font>速度分解定理

不同于刚体的速度分解定理, 流体还能发生变形, 流体质点的速度由平动, 转动和变形三个部分合成.

在一点的邻域内用变分展开流体速度:
$$
v_i=v_{0i}+\frac{\partial v_i}{\partial x_j}\delta x_j
$$
注意到 $\frac{\partial v_i}{\partial x_j}$是二阶张量, 将其分解为对称和反对称部分:
$$
\frac{\partial v_i}{\partial x_j}=\frac{1}{2}(\frac{\partial v_i}{\partial x_j}-\frac{\partial v_j}{\partial x_i})+\frac{1}{2}(\frac{\partial v_i}{\partial x_j}+\frac{\partial v_j}{\partial x_i})=a_{ij}+s_{ij}\\
~\\
S=\begin{vmatrix}
    \epsilon_1 &\frac{1}{2}\theta_3 & \frac{1}{2}\theta_2\\
    \frac{1}{2}\theta_3 & \epsilon_2 & \frac{1}{2}\theta_1\\
    \frac{1}{2}\theta_2 & \frac{1}{2}\theta_1 & \epsilon_3 \\
\end{vmatrix}
$$
S 称为变形速度张量或应变率张量, 其对角元的物理意义是坐标轴上线段元的相对拉伸 (压缩) 速度, 非对角元对应着两两坐标轴之间剪切角速度的负值.
变形速度张量可以对角化写成标准形式 $diag(\epsilon'_1,\epsilon'_2\epsilon'_3)$, 对角元称为主相对拉伸速度, 恒有三个互相垂直的主轴, 在主轴上的质点线段元以主相对拉伸速度变形, 变形后仍在主轴方向.

反对称部分对应着矢量 $\boldsymbol{\omega}=\frac{1}{2}\nabla\times\boldsymbol{v}$

**亥姆霍兹速度分解定理:**
$$
\boldsymbol{v}=\boldsymbol{v}_0+\frac{1}{2}\mathrm{rot}\boldsymbol{v}\times\delta \boldsymbol{r}+S\cdot\delta \boldsymbol{r}=\boldsymbol{v}_0+\frac{1}{2}\mathrm{rot}\boldsymbol{v}\times\delta \boldsymbol{r}+\mathrm{grad}\phi\\
\phi=\frac{1}{2}(\epsilon_1\delta x^2+\epsilon_2\delta y^2+\epsilon_3\delta z^2+\theta_1\delta y\delta z+\theta_2\delta x\delta z+\theta_3\delta y\delta x)
$$