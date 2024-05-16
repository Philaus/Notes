# Cp.VII 动理学简介

之前对于输运过程的讨论其实是比较粗糙的, 应为输运本质是一个非平衡态过程. 对其的严格描述应该从粒子分布函数的变化规律出发, 用统计力学方法确定系统的状态和变化. 

这种处理方法称为动理学理论.

##<font color='red'>$\S 1$ </font>动理学方程

考虑分布函数随时间的一个变化
$$
f(\boldsymbol{r}',\boldsymbol{v}',t+\delta t)=f(\boldsymbol{r},\boldsymbol{v},t)+(\frac{\partial f}{\partial t})_c \delta t
$$
$\displaystyle(\frac{\partial f}{\partial t})_c $ 是碰撞项, 表示单位时间内因碰撞而增加的净粒子数
其中
$$
\boldsymbol{r}'=\boldsymbol{r}+\boldsymbol{v}\delta t\\
\boldsymbol{v}'=\boldsymbol{v}+\frac{\boldsymbol{F}}{m}\delta t
$$
$\boldsymbol{F}$ 包括外场和内部的平均场 (自洽场)
并且利用相空间体积元不变
$$
d\boldsymbol{r}'d\boldsymbol{v}'=\frac{\partial (\boldsymbol{r}',\boldsymbol{v}')}{\partial (\boldsymbol{r},\boldsymbol{v})}d\boldsymbol{r}d\boldsymbol{v}=d\boldsymbol{r}d\boldsymbol{v}
$$
泰勒展开并保留到线性项, 得到**玻尔兹曼方程**, 也就是动理学方程:
$$
\frac{\partial f}{\partial t}+\boldsymbol{v}\cdot\frac{\partial f}{\partial \boldsymbol{r}}+\frac{\boldsymbol{F}}{m}\cdot\frac{\partial f}{\partial \boldsymbol{v}}=(\frac{\partial f}{\partial t})_c (随体导数)
$$

##<font color='red'>$\S 2$ </font>BGK 方程