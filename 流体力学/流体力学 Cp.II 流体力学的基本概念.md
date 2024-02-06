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

所有物理量对时间的偏导都为零的运动过程称为定常运动.

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

变形速度张量的第一基本不变量等于速度的散度, 等于体积元的变化率 (相对体积膨胀率): $I_1=\nabla\cdot\boldsymbol{v}=\frac{1}{\delta V}\frac{d}{dt}\delta V$
$$
\begin{cases}
    I_1=\epsilon_1+\epsilon_2+\epsilon_3\\
    I_2=\epsilon_2\epsilon_3+\epsilon_1\epsilon_3+\epsilon_2\epsilon_1-\frac{1}{4}(\theta_1^2+\theta_2^2+\theta_3^2)\\
    I_3=\epsilon_1\epsilon_2\epsilon_3+\frac{1}{4}\theta_1\theta_2\theta_3-\frac{1}{4}(\theta_1^2\epsilon_1+\theta_2^2\epsilon_2+\theta_3^2\epsilon_3)\\
\end{cases}
$$

反对称部分对应着矢量 $\boldsymbol{\omega}=\frac{1}{2}\nabla\times\boldsymbol{v}$

**亥姆霍兹速度分解定理:**
$$
\boldsymbol{v}=\boldsymbol{v}_0+\frac{1}{2}\mathrm{rot}\boldsymbol{v}\times\delta \boldsymbol{r}+S\cdot\delta \boldsymbol{r}=\boldsymbol{v}_0+\frac{1}{2}\mathrm{rot}\boldsymbol{v}\times\delta \boldsymbol{r}+\mathrm{grad}\phi\\
\phi=\frac{1}{2}(\epsilon_1\delta x^2+\epsilon_2\delta y^2+\epsilon_3\delta z^2+\theta_1\delta y\delta z+\theta_2\delta x\delta z+\theta_3\delta y\delta x)
$$

---
如果 $\nabla\cdot\boldsymbol{v}\ne0$, 则一般变形运动可以视为均匀膨胀 $\displaystyle\frac{1}{3}\frac{\partial v_i}{\partial x_i}\delta_{kl}$ 和无体积变化部分 $s_{kl}-\displaystyle\frac{1}{3}\frac{\partial v_i}{\partial x_i}\delta_{kl}$ 之和

任一平面变形运动可以分解为一个均匀膨胀, 一个均匀剪切和一个旋转运动. 证明: 在主轴坐标系变形运动写为标准形式, $\phi$ 的平方项组合为 $\delta\boldsymbol{r}'^2$ 和 $\delta x'^2-\delta y'^2$, 前一项为均匀膨胀, 后一项再转 45度, 得到 $\delta x''\delta y''$, 是一个旋转加一个剪切.
任一三维变形运动可以分解为一个均匀膨胀, 两个均匀剪切和一个旋转运动.

## <font color='red'>$\S 4$  </font>涡旋运动

流体的涡旋运动是局部概念, 其判据是该点处流体微元是否有自转或者 rot v 是否不为零, 而与宏观流线是不是弯曲无关.

$\boldsymbol{\Omega}=\mathrm{rot}\boldsymbol{v}$ 定义为涡量, 涡量的绝对值等于该点流体微元自转角速度的两倍. 类似速度, 涡量也可以在空间画出涡线和涡面, 涡管. 涡线的方程为:
$$
\frac{dx}{\Omega_x(a,b,c,t)}=\frac{dy}{\Omega_y(a,b,c,t)}=\frac{dz}{\Omega_z(a,b,c,t)}
$$
常常用速度环量来研究涡旋运动. 由斯托克斯公式, 速度环量等于涡通量:
$$
\int_L\boldsymbol{v}\cdot d\boldsymbol{r}=\int_S\boldsymbol{\Omega}\cdot d\boldsymbol{S}
$$

## <font color='red'>$\S 5$  </font>质量力和应力

作用在每一个质量元上的力是质量力, 比如引力, 惯性力. 单位体积内流体的重量称为比重.
作用在界面上的力称为面力, 其分布密度称为应力. $dP=p_ndS$

在运动连续时, $p_{-n}=-p_n$. 取定一个面, 面上的应力按与法向量的关系可以分为切向应力和法向应力.

在流体中取一个体积元, 当体积元趋于零时质量力比面力无穷小阶数高, 可以忽略. 此时作用在体积元上的应力可以用二阶张量表示. 利用应力在表面的合力矩为零可以证明这个张量是对称的. 应力张量可以对角化, 在主轴坐标系中的三个对角元称为法向主应力, 在与主轴垂直的面上只有法向应力.

---
理想流体或静止的流体不能承受切向变形, 所以切向应力为零, 应力张量自然成一个对角形.
可以用两种方式证明此时应力张量不同方向上的法向分量是相等的:
1. 根据 $p_n=p_x\alpha+p_b\beta+p_c\gamma$ 和切向分量 $p_{ij}=0$, $p_{nx}=p_{xx}\alpha$, 根据 nx 方向的对称性, $p_{nx}=p_{nn}\alpha$, 从而 $p_{xx}=p_{yy}=p_{zz}=p_{nn}=-p$.
2. 取一个三棱锥流体微元, 在三个侧面应用矢量三角形法则可以得出压力与面积成正比, 所以应力在任何方向都是一个常数.
所以此时应力是二阶各向同性张量, 可以用一个标量函数压强来表示.

## <font color='red'>$\S 6$  </font>物质积分的随体导数

线段元, 面积元和体积元的随体导数:
$$
\begin{cases}
\displaystyle\frac{d}{dt}\delta\boldsymbol{r}=\delta\boldsymbol{v}=\delta\boldsymbol{r}\cdot\nabla\boldsymbol{v}\\
\displaystyle\frac{d}{dt}\delta\tau=\nabla\cdot\boldsymbol{v}~\delta\tau\\
\displaystyle\frac{d}{dt}\delta S_i=\delta S_i\frac{\partial v_j}{\partial x_j}-\delta S_j\frac{\partial v_j}{\partial x_i}\\
\end{cases}
$$
线积分, 面积分和体积分的随体导数:
$$
\begin{cases}
\displaystyle\frac{d}{dt}\oint_L\boldsymbol{v}\cdot\delta\boldsymbol{r}=\oint_L\frac{d\boldsymbol{v}}{dt}\cdot\delta\boldsymbol{r}\\
\displaystyle\frac{d}{dt}\int_S\boldsymbol{\Omega}\cdot d\boldsymbol{S}=\int_S(\frac{d\boldsymbol{\Omega}}{dt}+\boldsymbol{\Omega}~\nabla\cdot\boldsymbol{v}-(\boldsymbol{\Omega}\cdot\nabla)\boldsymbol{v})\cdot\delta S\\
\displaystyle\frac{d}{dt}\int_{\tau}\phi \delta\tau=\int_{\tau}\frac{\partial \phi}{\partial t} \delta\tau+\int_{S}\phi~\boldsymbol{v}\cdot\delta\boldsymbol{S}\\
\displaystyle\frac{d}{dt}\int_{\tau}\boldsymbol{a} \delta\tau=\int_{\tau}\frac{\partial \boldsymbol{v}}{\partial t} \delta\tau+\int_{S}\boldsymbol{v}~\boldsymbol{v}\cdot\delta\boldsymbol{S}\\
\end{cases}
$$