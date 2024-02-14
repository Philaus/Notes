# Cp.I 张量分析

## 场论基本运算公式

$$
\begin{aligned}

& \text { 微分公式 } \\
& \operatorname{grad}(\varphi+\psi)=\operatorname{grad} \varphi+\operatorname{grad} \psi \\
& \operatorname{grad}(\varphi \psi)=\varphi \operatorname{grad} \psi+\psi \operatorname{grad} \varphi \\
& \operatorname{grad} F(\varphi)=F^{\prime}(\varphi) \operatorname{grad} \varphi, \operatorname{grad} \varphi(r)=\varphi^{\prime}(r) \frac{r}{r} \\
& \operatorname{div}(\boldsymbol{a}+\boldsymbol{b})=\operatorname{div} \boldsymbol{a}+\operatorname{div} \boldsymbol{b} \\
& \operatorname{div}(\varphi \boldsymbol{a})=\varphi \operatorname{div} \boldsymbol{a}+\operatorname{grad} \varphi \cdot \boldsymbol{a} . \\
& \operatorname{div}(\boldsymbol{a} \times \boldsymbol{b})=\boldsymbol{b} \cdot \operatorname{rot} \boldsymbol{a}-\boldsymbol{a} \cdot \operatorname{rot} \boldsymbol{b} . \\
& \operatorname{rot}(\boldsymbol{a}+\boldsymbol{b})=\operatorname{rot} \boldsymbol{a}+\operatorname{rot} \boldsymbol{b} \\
& \operatorname{rot}(\varphi \boldsymbol{a})=\varphi \operatorname{rot} \boldsymbol{a}+\operatorname{grad} \varphi \times \boldsymbol{a} . \\
& \operatorname{rot}(\boldsymbol{a} \times \boldsymbol{b})=(\boldsymbol{b} \cdot \nabla) \boldsymbol{a}-(\boldsymbol{a} \cdot \nabla) \boldsymbol{b}+\boldsymbol{a} \operatorname{div} \boldsymbol{b}-\boldsymbol{b} \operatorname{div} \boldsymbol{a} . \\
& \operatorname{grad}(\boldsymbol{a} \cdot \boldsymbol{b})=(\boldsymbol{b} \cdot \nabla) \boldsymbol{a}+(\boldsymbol{a} \cdot \nabla) \boldsymbol{b}+\boldsymbol{b} \times \operatorname{rot} \boldsymbol{a}+\boldsymbol{a} \times \operatorname{rot} \boldsymbol{b} . \\
& \operatorname{grad} \frac{\boldsymbol{a}^2}{2}=(\boldsymbol{a} \cdot \nabla) \boldsymbol{a}+\boldsymbol{a} \times \operatorname{rot} \boldsymbol{a}, \\
& \operatorname{或}(\boldsymbol{a} \cdot \nabla) \boldsymbol{a}=\operatorname{grad} \frac{a^2}{2}-\boldsymbol{a} \times \operatorname{rot} \boldsymbol{a} . \\
& \operatorname{div} \operatorname{grad} \varphi=\Delta \varphi .\\
& \text { div } \operatorname{rot} \boldsymbol{a}=0 . \\
& \operatorname{rot} \operatorname{grad} \varphi=\mathbf{0} . \\
& \operatorname{rot} \operatorname{rot} \boldsymbol{a}=\operatorname{grad} \operatorname{div} \boldsymbol{a}-\Delta \boldsymbol{a} . \\
& \operatorname{div}(\varphi \operatorname{grad} \psi)=\varphi \Delta \psi+\operatorname{grad} \varphi \cdot \operatorname{grad} \psi . \\
& \Delta(\varphi \psi)=\psi \Delta \varphi+\varphi \Delta \psi+2 \operatorname{grad} \varphi \cdot \operatorname{grad} \psi . \\
~\\

& \text { 积分公式 } \\
& \int_V \operatorname{grad} \varphi \mathrm{d} V=\int_S \boldsymbol{n} \varphi \mathrm{d} S . \\
& \int_V \operatorname{div} \boldsymbol{a} \mathrm{d} V=\int_S \boldsymbol{n} \cdot \boldsymbol{a} \mathrm{d} S(\text { 此式即奥-高定理 }) . \\
& \int_V \operatorname{rot} \boldsymbol{a} \mathrm{d} V=\int_S \boldsymbol{n} \times \boldsymbol{a} \mathrm{d} S . \\
& \int_V(\boldsymbol{v} \cdot \nabla) \boldsymbol{a} \mathrm{d} V=\int_S(\boldsymbol{v} \cdot \boldsymbol{n}) \boldsymbol{a} \mathrm{d} S, \text { 其中v 是常矢量. } \\
& \int_V \Delta \varphi \mathrm{d} V=\int_S \frac{\partial \varphi}{\partial n} \mathrm{~d} S=\int_S \boldsymbol{n} \cdot \nabla \varphi \mathrm{d} S . \\
& \int_V \Delta \boldsymbol{a} \mathrm{d} V=\int_S \frac{\partial \boldsymbol{a}}{\partial n} \mathrm{~d} S=\int_S(\boldsymbol{n} \cdot \nabla) \boldsymbol{a} \mathrm{d} S .
\end{aligned}
$$

格林第一公式
$$
\begin{aligned}
& \int_V(\varphi \Delta \psi+\operatorname{grad} \varphi \cdot \operatorname{grad} \psi) \mathrm{d} V=\int_S \varphi \frac{\partial \psi}{\partial n} \mathrm{~d} S \\
& \int_V(\psi \Delta \varphi+\operatorname{grad} \psi \cdot \operatorname{grad} \varphi) \mathrm{d} V=\int_S \psi \frac{\partial \varphi}{\partial n} \mathrm{~d} S
\end{aligned}
$$
格林第二公式
$$
\int_V(\varphi \Delta \psi-\psi \Delta \varphi) d V=\int_S\left(\varphi \frac{\partial \psi}{\partial n}-\psi \frac{\partial \varphi}{\partial n}\right) d S \text {. }\\~\\
$$
$$\int_V(\operatorname{grad} \varphi)^2 \mathrm{~d} V=\int_S \varphi \frac{\partial \varphi}{\partial n} \mathrm{~d} S$$

其中 $\varphi$ 满足 $\Delta \varphi=0$.
式中 $V$ 是单连通风域.

---


物理量独立于坐标系, 在不同坐标系的数量表征之间有确定的变换律.

例如在每个坐标系给出 $3^n$ 个数 $p_{j_1j_2\dotsc j_n}$, 当坐标变换时满足:
$$
p'_{j_1j_2\dotsc j_n}=\alpha_{i_1j_1}\alpha_{i_2j_2}\dotsc \alpha_{i_nj_n}p_{j_1j_2\dotsc j_n}
$$
则此 $3^n$ 个数定义一个 n 阶张量, 张量的阶数由其满足的运算规则确定.
其中 $\alpha_{i_nj_n}$ 是两个正交基向量组之间变换矩阵的矩阵元, 满足:
$$
\alpha_{ij}\alpha_{jk}=\alpha_{ji}\alpha_{ki}=\delta_{jk}
$$

---
n 阶张量可以写成并矢形式 $p_{i_1i_2\dotsc i_n}\boldsymbol{e}_{i_1}\boldsymbol{e}_{i_2}\dotsc\boldsymbol{e}_{i_n}$

对于一个 n 阶并矢 $AB$, 其中的偶数组指标可以做缩并运算, 得到一个 n-2k 阶的张量. 其中一次缩并称作内积, 记作 $A\cdot B$, 实例有矢量的内积和矩阵的乘法.

用张量的并矢和缩并运算可以直接判断张量的阶数.

---
二阶张量的一个实例就是矩阵, 矩阵的性质和运算都可以推广应用到二阶张量.

不随坐标变换改变的量称为不变量, **二阶张量的基本不变量**有:
$$
\begin{cases}
I_1=\lambda_1+\lambda_2+\lambda_3=\mathrm{tr}{A}\\
I_2=\lambda_1\lambda_2+\lambda_2\lambda_3+\lambda_1\lambda_3\\
I_3=\lambda_1\lambda_2\lambda_3=|A|
\end{cases}
$$
用基本不变量可以构造出任意不变量.

二阶张量的共轭对应着矩阵的转置操作, 交换指标.
二阶张量的主轴对应着矩阵特征值的特征向量.

二阶张量可以唯一地分解为一个对称张量和一个反对称张量之和, 任意二阶张量的问题可以分解到具有对称性的部分中研究.
$$
P=\frac{1}{2}(P+P^T)+\frac{1}{2}(P-P^T)
$$

---
二阶反对称张量的形式是:
$$
\begin{vmatrix}
    0 &-\omega_3 & \omega_2\\
    \omega_3 & 0 & \omega_1\\
    -\omega_2 &\omega_1 & 0\\
\end{vmatrix}
$$
只有三个独立元素, 对角线元素都是 0. 
对称性和反对称性不因坐标变换而改变.

三个独立分量如果组成一个矢量 $\boldsymbol{\omega}=(\omega_1, \omega_2, \omega_3)$, 则:
$$
A\cdot \boldsymbol{b}=\boldsymbol{\omega}\times \boldsymbol{b}
$$

二阶对称张量的三个主值都是实数, 并且一定存在三个互相垂直的主轴.
二次有心曲面和二阶对称张量一一对应, 所以可以作为其几何表示, 一个标准二次有心曲面的方程可以写为 $s_{ij}x_ix_j=\mathrm{Const}$.
椭球面是正定二阶对称张量的几何表示, 设椭球方程为 $F=s_{ij}x_ix_j$, 则 $\boldsymbol{S}\cdot\boldsymbol{r}=\frac{1}{2}\nabla F$.

---
**张量的微分运算**
梯度 $\nabla P=\displaystyle\frac{\partial }{\partial x_k}p_{i_1i_2\dotsc i_n}$, 简记为 $p_{i_1i_2\dotsc i_n, k}$, 是 n+1 阶张量, 偏导分母的指标不同于任何张量指标.

散度 $\nabla \cdot P=\displaystyle\frac{\partial }{\partial x_k}p_{ki_2\dotsc i_n}$, 是 n-1 阶张量, 由 $\nabla P$ 缩并一次得到. 偏导分母的指标是张量指标的其中一个.

---
经过坐标变换后任意元素都不改变的张量称为**各向同性张量**.

对于张量的某个元素 $p_{i_1i_2\dotsc i_n}$, 对所有下标作相同的循环置换 (如变为 $p_{i_ni_1\dotsc i_{n-1}}$) 得到另一个分量, 如果张量是各向同性的, 则这两个分量相等.

零阶张量都是各向同性的
一阶张量只有零矢量各向同性
二阶各向同性张量的形式一定为 $\lambda\delta_{ij}$
三阶各向同性张量的形式一定为 $\lambda\epsilon_{ijk}$
四阶各向同性张量的形式一定为 $\lambda_1\delta_{ij}\delta_{kl}+\lambda_2\delta_{ik}\delta_{jl}+\lambda_3\delta_{il}\delta_{jk}$, 或者 $\lambda_1\delta_{ij}\delta_{kl}+\lambda(\delta_{ik}\delta_{jl}+\delta_{il}\delta_{jk})$