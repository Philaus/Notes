# <center>4 磁流体力学
###  $\S$1 速度矩方程的导出 

流体力学方程的建立基于 Boltzmann 方程取速度矩
单粒子 Boltzmann 方程：
$$
\frac{\partial f_\alpha}{\partial t}+\pmb{v}\cdot\frac{\partial f_\alpha}{\partial \pmb{r}}+\frac{\pmb{F_\alpha}}{m_\alpha}\cdot\frac{\partial f_\alpha}{\partial \pmb{v}}=\sum_{\beta}(\frac{\partial f_\alpha}{\partial t})_{c,\alpha\beta}
$$
右边的是碰撞项

速度矩的定义：
$$
\begin{align}
\langle\psi(\pmb{v})\rangle=\frac{\int\psi(\pmb{v})f(\pmb{r},\pmb{v},t)d\pmb{v}}{\int f(\pmb{r},\pmb{v},t)d\pmb{v}}\\
=\frac{\int\psi(\pmb{v})f(\pmb{r},\pmb{v},t)d\pmb{v}}{n(\pmb{r},t)}\\
\end{align}
$$
