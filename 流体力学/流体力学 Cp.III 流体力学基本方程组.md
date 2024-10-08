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
第一个方程就是运动方程两边点乘速度, 所以在总方程组中可以不写.

如果考虑传导电流和电磁场对磁流体能量的影响, 应当再加入一项 $\boldsymbol{J}\cdot\boldsymbol{E}=\boldsymbol{v}\cdot\boldsymbol{F_{em}}+J_{cond}^2/2$, 第一项是对机械能的影响, 第二项是对内能.
其中 $\boldsymbol{F_{em}}=\rho_e \boldsymbol{E}+\boldsymbol{J}_{cond}\times\boldsymbol{B}$, $\boldsymbol{J}_{cond}=\sigma(\boldsymbol{E}+\boldsymbol{v}\times\boldsymbol{B})=\boldsymbol{J}-\rho_e \boldsymbol{v}$

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

本构方程与运动方程联立得到纳维-斯托克斯 (Navier-Stokes) 方程.

根据理想流体的定义, 切向应力的分量全为零, 推出剪切变形速度或者第一动力黏度为 0, 而切变速度一般不为零, 所以理想流体的数学表示是 $\mu=0$.

## <font color='red'>$\S 5$  </font>状态方程

流体力学的方程组出现了 p T 等物理量, 为了建立封闭方程组, 应该引入热力学方程.

在流体力学中, 对应着热力学中理想气体的称呼为完全气体 (与理想流体区分).

范德华 (van der Waals) 方程:
$$
(p+\frac{\alpha}{V^2})(V-\beta)=RT
$$
对于极高压强的液体, 应当考虑密度随压强的变化, 柯尔 (Cole) 方程: 
$$
\frac{p+B}{1+B}=(\frac{\rho}{\rho_0})^n
$$
参数取值例: $n=7$, $B=3000$atm, $p<10^5$atm

如果流体在运动中密度只是压强的函数而和其他热力学变量无关, 则称为正压流体, 否则称为斜压流体.

热力学基本定律和物理量及热容关系不详细叙述, 参看热学.

虽然流体力学系统大多是非平衡非均匀系统, 但是实践表明可以近似使用平衡态的结果.

## <font color='red'>$\S 6$  </font>流体力学基本方程组

**应力形式**
$$
\begin{aligned}
& \begin{cases}
\displaystyle\frac{\partial \rho}{\partial t}+\operatorname{div}(\rho \boldsymbol{v})=0, & \text { 连续性方程 } \\
~\\
\displaystyle\rho \frac{\mathrm{d} \boldsymbol{v}}{\mathrm{d} t}=\rho \boldsymbol{F}+\operatorname{div} \boldsymbol{P}, & \text { 运动方程 } \\
~\\
\displaystyle\rho \frac{\mathrm{d} U}{\mathrm{~d} t}=\boldsymbol{P}: \boldsymbol{S}+\operatorname{div}(k~ \operatorname{grad} T)+\rho q, & \text { 能量方程 } \\
\displaystyle\boldsymbol{P}=-p \boldsymbol{I}+2 \mu\left(\boldsymbol{S}-\frac{1}{3} \boldsymbol{I} \operatorname{div} \boldsymbol{v}\right)+\mu^{\prime} \boldsymbol{I} \operatorname{div} \boldsymbol{v}, & \text { 本构方程 } \\
\displaystyle p=f(\rho, T), & \text { 状态方程 }\end{cases} \\
\end{aligned}
$$
如果在界面上特征量存在突变或一阶偏导数不连续, 则不能在间断面上使用微分形式, 前三个方程应该写为积分形式
$$
\left\{\begin{array}{l}
\displaystyle \int_\tau \frac{\partial \rho}{\partial t} \mathrm{~d} \tau+\int_S \rho v_n \mathrm{~d} S=0, \\
~\\
\displaystyle \int_\tau \frac{\partial(\rho \boldsymbol{v})}{\partial t} \mathrm{~d} \tau+\int_S \rho v_n \boldsymbol{v} \mathrm{d} S=\int_\tau \rho \boldsymbol{F} \mathrm{d} \tau+\int_S \boldsymbol{p}_n \mathrm{~d} S, \\
~\\
\displaystyle \int_\tau \frac{\partial}{\partial t}\left[\rho\left(U+\frac{V^2}{2}\right)\right] \mathrm{d} \tau+\int_S \rho v_n\left(U+\frac{V^2}{2}\right) \mathrm{d} S \\
\displaystyle \quad=\int_\tau \rho \boldsymbol{F} \cdot \boldsymbol{v} \mathrm{d} \tau+\int_S \boldsymbol{p}_n \cdot \boldsymbol{v} \mathrm{d} S+\int_S k \frac{\partial T}{\partial n} \mathrm{~d} S+\int_\tau \rho q \mathrm{~d} \tau, \\
~\\
\displaystyle \int_\tau\left[r \times \frac{\partial(\rho \boldsymbol{v})}{\partial t}\right] \mathrm{d} \tau+\int_S\left(\boldsymbol{r} \times \rho v_n \boldsymbol{v}\right) \mathrm{d} S \\
\displaystyle \quad=\int_\tau \boldsymbol{r} \times \rho \boldsymbol{F} \mathrm{d} \tau+\int_S \boldsymbol{r} \times \boldsymbol{p}_n \mathrm{~d} S,
\end{array}\right.
$$

**矢量形式**
应力做功的功率分为三个部分: 体积变化时应力做的功, 膨胀时黏性耗散的机械能, 剪切黏性耗散的机械能.
$$
\boldsymbol{P}: \boldsymbol{S}=-p\operatorname{div} \boldsymbol{v}+\mu^{\prime}(\operatorname{div} \boldsymbol{v})^2+(2 \mu \boldsymbol{S}: \boldsymbol{S}-\frac{2}{3} \mu(\operatorname{div} \boldsymbol{v})^2)
$$
只考虑黏性耗散的机械能, 定义耗散函数:
$$
\begin{aligned}
\Phi=\left(\mu^{\prime}-\frac{2}{3} \mu\right)(\operatorname{div} \boldsymbol{v})^2+2 \mu \boldsymbol{S}: \boldsymbol{S}\\
\end{aligned}
$$

利用本构方程将运动方程和能量方程中的应力张量消去, 可以重写这两个方程, 其中为了区分变形速度 S ,用 s 表示熵:
$$
\left\{\begin{array}{l}
\displaystyle\rho \frac{\mathrm{d} \boldsymbol{v}}{\mathrm{d} t}=\rho \boldsymbol{F}-\operatorname{grad} p+2 \operatorname{div}(\mu \boldsymbol{S})-\frac{2}{3} \operatorname{grad}(\mu \operatorname{div} \boldsymbol{v})+\operatorname{grad}\left(\mu^{\prime} \operatorname{div} \boldsymbol{v}\right)\\
\displaystyle(当\mu ~\mu'为常数)= \rho \boldsymbol{F}-\operatorname{grad} p+\mu \Delta \boldsymbol{v}+\left(\mu^{\prime}+\frac{\mu}{3}\right) \operatorname{grad} \operatorname{div} \boldsymbol{v}, \\
\displaystyle\rho T \frac{\mathrm{d} s}{\mathrm{~d} t}=\Phi+\operatorname{div}(k \operatorname{grad} T)+\rho q, \\
\end{array}\right.
$$
其中第一式称为纳维-斯托克斯 (Navier-Stokes) 方程.

**黏性不可压缩流体**

流体是不可压缩均质时状态方程为 $\rho=$ 常数, 其次设 $\mu=$ 常数, 于是黏性不可压缩均质流体的基本方程组为
$$
\left\{\begin{array}{l}
\operatorname{div} \boldsymbol{v}=0, \\
\displaystyle\rho \frac{\mathrm{d} \boldsymbol{v}}{\mathrm{d} t}=\rho \boldsymbol{F}-\operatorname{grad} p+\mu \Delta \boldsymbol{v}, \\
\displaystyle\rho T \frac{\mathrm{d} s}{\mathrm{~d} t}=\Phi+\operatorname{div}(k \operatorname{grad} T)+\rho q, \\
\boldsymbol{P}=-p \boldsymbol{I}+2 \mu \boldsymbol{S} .
\end{array}\right.
$$
**理想可压缩流体**
设气体是理想绝热而且是完全的, 此时基本方程组为
$$
\left\{\begin{array}{l}
\displaystyle\frac{\partial \rho}{\partial t}+\operatorname{div}(\rho \boldsymbol{v})=0, \\
\displaystyle\rho \frac{\mathrm{d} \boldsymbol{v}}{\mathrm{d} t}=\rho \boldsymbol{F}-\operatorname{grad} p, \\
\displaystyle\frac{\mathrm{d}}{\mathrm{d} t}\left(\frac{p}{\rho^\gamma}\right)=0 ~~理想绝热.
\end{array}\right.
$$
**理想不可压缩流体情形**

如果流体既是理想又是不可压缩均质的, 则方程组采取如下形式:
$$
\left\{\begin{array}{l}
\operatorname{div} \boldsymbol{v}=0, \\
\displaystyle\rho \frac{\mathrm{d} \boldsymbol{v}}{\mathrm{d} t}=\rho \boldsymbol{F}-\operatorname{grad} p .
\end{array}\right.
$$

---
一般情况下, 两介质界面处的速度矢量和温度是连续的, 如果忽略输运(理想流体), 那么也可以是间断的.

应力的边界条件
$$
\boldsymbol{P}^{(1)}\cdot\boldsymbol{n}-\boldsymbol{P}^{(2)}\cdot\boldsymbol{n}=-\gamma(\frac{1}{R_1}+\frac{1}{R_2})\boldsymbol{n}
$$

对于固定边界处, 采用粘附条件, 即 $\boldsymbol{v}_1=\boldsymbol{v}_2, T_1=T_2, (k\frac{\partial T}{\partial n})_1=(k\frac{\partial T}{\partial n})_2$.
如果气体很稀薄, 那么滑移速度与分子平均自由程同数量级.