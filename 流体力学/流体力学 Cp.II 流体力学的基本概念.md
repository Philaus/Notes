# Cp.II 流体力学的基本概念

拉格朗日法的运动规律是特定质点 (a,b,c) 随时间的位置函数, 欧拉法的运动规律是空间坐标下的速度场.
两者描述的是同一个物理过程, 所以是等价的. 实际中可以根据需要和建模计算难易度选择使用.

已知拉格朗日法和欧拉法运动描述下的互相转换:
1. L 转 E: 已知 $\boldsymbol{r}(a,b,c,t)$, 速度函数为 $\displaystyle\frac{\partial \boldsymbol{r}}{\partial t}$, 反解出三个拉格朗日坐标关于 r 的函数再带入 v 的方程即得欧拉变数中的速度方程.
2. E 转 L: 已知速度函数 $\boldsymbol{v}(\boldsymbol{r},t)=\displaystyle\frac{d\boldsymbol{r}}{dt}$, 构成 r 的常微分方程组, 其解为 $\boldsymbol{r}(C_1,C_2,C_3,t)$, 由初始时刻 $\boldsymbol{r}=\boldsymbol{r}_0$ 确定, $\boldsymbol{r}_0$ 的三个坐标就是三个拉格朗日变数.