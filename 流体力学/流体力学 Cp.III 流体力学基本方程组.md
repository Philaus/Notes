# Cp.III 流体力学基本方程组

## <font color='red'>$\S 1$  </font>连续性方程

从质量守恒出发可以推导出连续性方程
$$
\frac{dm}{dt}=\frac{d}{dt}\int \rho d\tau=0
$$
根据物质积分的随体导数, 得到积分形式的连续性方程:
$$
\int \frac{\partial \rho}{\partial t}d\tau+\int \rho v_n dS=\int (\frac{d\rho}{dt}+\rho \nabla\cdot \boldsymbol{v})d\tau=\int (\frac{\partial \rho}{\partial t}+ \nabla\cdot(\rho\boldsymbol{v}) )d\tau=0
$$
以及微分形式的连续性方程:
$$
\frac{\partial \rho}{\partial t}+ \nabla\cdot(\rho\boldsymbol{v})=\frac{d\rho}{dt}+\rho \nabla\cdot \boldsymbol{v}=0
$$

---
如果考虑单个流体质量元的守恒性, 得到:
$$
\frac{1}{\rho}\frac{d\rho}{dt}+\frac{1}{\delta\tau}\frac{d\delta\tau}{dt}=\frac{1}{\rho}\frac{d\rho}{dt}+\mathrm{div} \boldsymbol{v}=0
$$
这种表达方式能直观的看出物理意义, 第一项是相对密度变化率, 第二项是相对体积变化率.

应用欧拉观点一样可以推到出连续性方程, 在空间中取一个立方体的控制面, 考虑内部的源和面上进出的流.

---
对于定常运动, $\frac{\partial \rho}{\partial t}=0$; 对于不可压缩流体, $\frac{d\rho}{dt}=0$.

流管中的质量守恒方程: $\rho v S=\mathrm{Const}$

## <font color='red'>$\S 2$  </font>运动方程

从动量定理出发推导运动方程, 考虑控制面内的质量力 F 和面上的应力 p.
$$
\frac{d}{dt}\int \rho\boldsymbol{v}\delta\tau=\int \rho\boldsymbol{F}\delta\tau+\int \boldsymbol{p}_n\delta S\\
\rho \frac{d\boldsymbol{v}}{dt}=\rho\boldsymbol{F}+\mathrm{div} \boldsymbol{P}
$$
积分形式的动量矩定理:
$$
\int [\boldsymbol{r}\times \frac{\partial \rho\boldsymbol{v}}{\partial t}]\delta\tau+\int [\boldsymbol{r}\times \rho\boldsymbol{v}v_n]\delta S=\int \boldsymbol{r}\times\rho\boldsymbol{F} \delta\tau+\int \boldsymbol{r}\times\boldsymbol{p}_n\delta S
$$
微分形式的动量矩定理只能给出应力张量的对称性这个已知结论.

---
如果把加速度的位势部分和涡旋部分分开:
$$
\frac{d\boldsymbol{v}}{dt}=\frac{\partial \boldsymbol{v}}{\partial t}+\boldsymbol{v}\cdot\nabla\boldsymbol{v}=\frac{\partial \boldsymbol{v}}{\partial t}+\mathrm{grad} \frac{V^2}{2}+\mathrm{rot} \boldsymbol{v}\times\boldsymbol{v}\\
~\\
\rho(\frac{\partial \boldsymbol{v}}{\partial t}+\mathrm{grad} \frac{V^2}{2}+\mathrm{rot} \boldsymbol{v}\times\boldsymbol{v})=\rho\boldsymbol{F}+\mathrm{div} \boldsymbol{P}
$$
以上就是兰姆-格罗麦卡 (Lamb-Громека) 方程.

---
运动坐标系中的运动方程:
$$
相对加速度 \frac{d'\boldsymbol{v}_r}{dt}=\boldsymbol{F}+\mathrm{div} \boldsymbol{P}/\rho-\boldsymbol{a}_0-2(\boldsymbol{\omega}\times\boldsymbol{v})
$$
外力可以写成虚拟外力 $\boldsymbol{F}'=\boldsymbol{F}-\boldsymbol{a}_0-2(\boldsymbol{\omega}\times\boldsymbol{v})$

## <font color='red'>$\S 3$  </font>能量方程

能量守恒定律
$$
\frac{d}{dt}\int\rho (U+\frac{V^2}{2})d\tau=\int \rho\boldsymbol{F}\cdot\boldsymbol{v}d\tau+\int \boldsymbol{p}_n\cdot\boldsymbol{v}dS+\int k\frac{\partial T}{\partial n}dS+\int \rho q d\tau\\
~\\
\rho\frac{d\frac{V^2}{2}}{dt}+\rho\frac{dU}{dt}=\rho\boldsymbol{F}\cdot\boldsymbol{v}+\mathrm{div}(\boldsymbol{P}\cdot\boldsymbol{v})+\mathrm{div}(k~\mathrm{grad}~T)+\rho q 
$$

把 $\mathrm{div}(\boldsymbol{P}\cdot\boldsymbol{v})$ 用张量指标展开, 速度外导数写成变形速度
$$
\mathrm{div}(\boldsymbol{P}\cdot\boldsymbol{v})=\boldsymbol{v}\cdot\mathrm{div}\boldsymbol{P}+\boldsymbol{P}:\boldsymbol{S}
$$
这样表明面力对单位体积做功功率来自面力合力的功率和流体变形后面力的功率

动能 内能变化来源分离表示:
$$
\rho\frac{d\frac{V^2}{2}}{dt}=\rho\boldsymbol{F}\cdot\boldsymbol{v}+\boldsymbol{v}\cdot\mathrm{div}\boldsymbol{P}\\
~\\
\rho\frac{dU}{dt}=\boldsymbol{P}:\boldsymbol{S}+\mathrm{div}(k~\mathrm{grad}~T)+\rho q 
$$

## <font color='red'>$\S 4$  </font>本构方程


本构方程与运动方程联立得到纳维-斯托克斯 (Navier-Stokes) 方程


## <font color='red'>$\S 5$  </font>状态方程

