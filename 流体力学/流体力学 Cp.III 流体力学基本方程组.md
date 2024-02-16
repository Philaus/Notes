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

**牛顿黏性定律**
牛顿所做的最简单的剪切运动实验表明剪应力与剪切变形速度有线性关系, 比例系数定义为(动力)黏度, 表征流体抗拒变形的内摩擦:
$$
\tau=\mu\frac{dv_x}{dy}
$$
又定义运动黏度 $\nu=\mu/\rho$.

黏度显著依赖于温度, 而与压强关系不大. 对于液体, 温度升高黏性降低, 而气体相反.
对于气体, 黏性温度关系可以表示为萨瑟兰 (Sutherland) 公式, 其中 C=110.4K, 这个公式对 T<2000K 的空气适用:
$$
\mu=\mathrm{Const}~\frac{T^{3/2}}{T+C}
$$
可以用幂次近似表示为, n 在 3000K 以上趋于 1/2, 在低温趋于 1:
$$
\frac{\mu}{\mu_0}=(\frac{T}{T_0})^n
$$

---
**广义牛顿黏性定律**
运动流体在趋于静止时应力张量应该趋于各向同性, 所以分离表示为:
$$
\boldsymbol{P}=-p\boldsymbol{I}+\boldsymbol{P}'\\
p_{ij}=-p\delta_{ij}+\tau_{ij}
$$
值得一提的是这里的 p 不是静止压强, 而是运动压强函数, 只在速度趋于零时趋于静止压强. P' 称偏应力张量.

假设偏应力张量的所有元只线性依赖于变形速度张量的元, 是其线性齐次函数.
再假设流体各向同性, 则上述的依赖关系只剩下两个自由系数:
$$
\tau_{ij}=c_{ijkl}\frac{\partial v_k}{\partial x_l}=[\lambda\delta_{ij}\delta_{kl}+\mu(\delta_{ik}\delta_{jl}+\delta_{il}\delta_{jk})](s_{kl}-\epsilon_{klm}\omega_m)
$$
再根据变形速度的对称性和旋转速度的反对称性, 第二个因式的第二项为零
$$
\tau_{ij}=\lambda s_{kk}\delta_{ij}+2\mu s_{ij}
$$
带入应力张量的表达式, 得到**各向同性流体的本构方程**
$$
p_{ij}=-p\delta_{ij}+2\mu(s_{ij}-s_{kk}\delta_{ij}/3)+\mu's_{kk}\delta_{ij}\\
\mu'=\lambda+2/3~\mu
$$

取一个微小球面计算应力平均值, 发现所有方向法向应力的平均值等于三个坐标轴方向法向应力的平均值, 等于 $-p+\mu'\mathrm{div}\boldsymbol{v}$.
对于不可压缩流体(通常的液体和低速定常气体), $\mathrm{div}\boldsymbol{v}=0$. 如果流体元发生体积变化, 将引起平均法向应力的变化, 系数 $\mu'$ 称为第二动力黏度(或膨胀黏度, 体积黏度).

从微观来说, 气体体积变化是在平衡态之间转换的不平衡状态, 是不可逆过程, 有熵增, 这种有序能量的耗散在宏观就体现为第二黏度. 如果非平衡态的弛豫时间相对于研究的尺度足够小, 那么则可以忽略, 气体运动除了高温和高频声波等极端情况都可以忽略. 这种认为平均法向应力不依赖于膨胀率 $\mathrm{div}\boldsymbol{v}$ 的假设称为斯托克斯假设.

广义牛顿黏性定律是在假设偏应力张量对速度梯度张量有线性依赖的基础上推出的, 但是实验表明其适用范围相当广, 包括高超音速气体. 符合广义牛顿黏性定律的流体称为牛顿流体.
$$
p_{ij}=-p\delta_{ij}+2\mu(s_{ij}-s_{kk}\delta_{ij}/3)\\
\boldsymbol{P}=-p\boldsymbol{I}+2\mu(\boldsymbol{S}-1/3~\boldsymbol{I}\mathrm{div}\boldsymbol{v})
$$

本构方程与运动方程联立得到纳维-斯托克斯 (Navier-Stokes) 方程

## <font color='red'>$\S 5$  </font>状态方程

