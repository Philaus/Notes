# Cp.IV 标架与曲面论基本定理
##<font color='red'>$\S 1$ </font>活动标架
参数曲面 $S$ 上的向量场 $\boldsymbol{x}(u,v)$ 是指对于 $S$ 上任意一点, $\boldsymbol{x}(u,v)$ 是从 $\boldsymbol{r}(u,v)$ 出发的一个向量,并且光滑地依赖于参数 $(u,v)$.
例如切向量场 法向量场 自然标架场等.

比自然标架场更一般,有活动标架场. $\{\boldsymbol{r}(u,v);\boldsymbol{x}_1(u,v),\boldsymbol{x}_2(u,v),\boldsymbol{x}_3(u,v)\}$ 
只要求基向量线性无关,并且是正定向的 $((\boldsymbol{x}_1,\boldsymbol{x}_2,\boldsymbol{x}_3)>0)$.
为了使标架准确反映曲面的几何性质,再要求 $\boldsymbol{x}_1,\boldsymbol{x}_2$ 是曲面的切向量.

通过曲面上任意标架来研究曲面与标架无关的几何性质,是微分几何的一个基本方法.

简单正交活动标架的最简单形式刚好就是 Frenet 标架.
##<font color='red'>$\S 2$ </font>自然标架的运动方程
$$
\boldsymbol{r}_\alpha=\frac{\partial \boldsymbol{r}}{\partial u^\alpha}\\
\boldsymbol{r}_{\alpha\beta}=\frac{\partial^2 \boldsymbol{r}}{\partial u^\alpha\partial u^\beta}(u^1,u^2)\\
g_{\alpha\beta}=\langle\boldsymbol{r}_\alpha,\boldsymbol{r}_\beta\rangle\\
b_{\alpha\beta}=\langle\boldsymbol{r}_{\alpha\beta},\boldsymbol{n}\rangle=-\langle\boldsymbol{r}_{\alpha},\boldsymbol{n}_\beta\rangle\\
\ \\
(b_{\alpha\beta})^{-1}=b^{\alpha\beta}\\
g=det(g_{\alpha\beta}),b=det(b_{\alpha\beta})\\
g_{\alpha\beta}g^{\beta\gamma}=\delta^\gamma_\alpha
$$
$g_{\alpha\beta}$ 和 $b_{\alpha\beta}$ 就是曲面的第一和第二基本形式在参数 $(u^1,u^2)$ 下的系数矩阵.并且关于两个下标对称.
这样两个基本形式可以表示为:
$$
I=g_{\alpha\beta}du^\alpha du^\beta\\
II=b_{\alpha\beta}du^\alpha du^\beta
$$

下面用这些张量记号表示出自然标架关于参数偏导数的表达式,称为曲面自然标架的运动方程.
自然标架的运动由两个基本形式的系数完全确定.
$$
\begin{cases}
    \boldsymbol{r}_{\alpha\beta}=\Gamma^\gamma_{\alpha\beta}\boldsymbol{r}_\gamma+b_{\alpha\beta}\boldsymbol{n}\\
    \boldsymbol{n}_\alpha=-b^\beta_\alpha\boldsymbol{r}_{\beta}\\
\end{cases}
$$
系数矩阵 $b^\beta_\alpha$ 是 Weingarten 变换在基下的矩阵
$$
b^\beta_\alpha=b_{\alpha\gamma}g^{\gamma\beta}\\
\mathscr{W}(\boldsymbol{r}_{\alpha})=-\boldsymbol{n}_{\alpha}$$
两类 Christoffel 符号
$$
\Gamma^\gamma_{\alpha\beta}=\frac{1}{2}g^{\gamma\xi}[\frac{\partial g_{\alpha\xi}}{\partial u^\beta}+\frac{\partial g_{\beta\xi}}{\partial u^\alpha}-\frac{\partial g_{\alpha\beta}}{\partial u^\xi}]\\
\Gamma_{\xi\alpha\beta}=g_{\gamma\xi}\Gamma^\gamma_{\alpha\beta}=\frac{1}{2}[\frac{\partial g_{\alpha\xi}}{\partial u^\beta}+\frac{\partial g_{\beta\xi}}{\partial u^\alpha}-\frac{\partial g_{\alpha\beta}}{\partial u^\xi}]\\
$$
在应用上式具体计算时,可以用 EFG LMN 记号表示.
当 $(u,v)$ 是正交参数时,F 恒等于 0

##<font color='red'>$\S 3$ </font>曲面的结构方程
Gauss-Codazzi 方程
$$
\begin{cases}
    \displaystyle\frac{\partial \Gamma^\xi_{\alpha\beta}}{\partial u^\gamma}-\frac{\partial \Gamma^\xi_{\alpha\gamma}}{\partial u^\beta}+\Gamma^\eta_{\alpha\beta}\Gamma^\xi_{\eta\gamma}-\Gamma^\eta_{\alpha\gamma}\Gamma^\xi_{\eta\beta}-b_{\alpha\beta}b^\xi_\gamma+b_{\alpha\gamma}b^\xi_\beta=0\\
    \ \\
    \displaystyle\frac{\partial b_{\alpha\beta}}{\partial u^\gamma}-\frac{\partial b_{\alpha\gamma}}{\partial u^\beta}+\Gamma^\xi_{\alpha\beta}b_{\xi\gamma}-\Gamma^\xi_{\alpha\gamma}b_{\xi\beta}=0
\end{cases}
$$
由于指标的存在, Gauss 方程和 Codazzi 方程都是方程组.
Gauss 方程组只有一个独立方程, Codazzi 方程组有两个独立方程.

引入 Riemann 记号:
$$
R_{\delta\alpha\beta\gamma}=g_{\delta\xi}(\frac{\partial \Gamma^\xi_{\alpha\beta}}{\partial u^\gamma}-\frac{\partial \Gamma^\xi_{\alpha\gamma}}{\partial u^\beta}+\Gamma^\eta_{\alpha\beta}\Gamma^\xi_{\eta\gamma}-\Gamma^\eta_{\alpha\gamma}\Gamma^\xi_{\eta\beta})
$$
Gauss 方程的独立方程为
$$
R_{1212}=-(b_{11}b_{22}-(b_{12})^2)
$$
Codazzi 方程的独立方程为
$$
\begin{cases}
    \displaystyle\frac{\partial b_{11}}{\partial u^2}-\frac{\partial b_{12}}{\partial u^1}=b_{1\xi}\Gamma^\xi_{12}-b_{2\xi}\Gamma^\xi_{21}\\
    \ \\
    \displaystyle\frac{\partial b_{21}}{\partial u^2}-\frac{\partial b_{22}}{\partial u^1}=b_{1\xi}\Gamma^\xi_{22}-b_{2\xi}\Gamma^\xi_{21}\\
\end{cases}
$$
对于正交参数系 ,方程可以简化为
$$
-\frac{1}{\sqrt{EG}}[(\frac{\sqrt{E}_v}{\sqrt{G}})_v+(\frac{\sqrt{G}_u}{\sqrt{E}})_u]=\frac{LN-M^2}{EG}\\
\ \\
\begin{cases}
    \displaystyle(\frac{L}{\sqrt{E}})_v-(\frac{M}{\sqrt{E}})_u-N\frac{\sqrt{E}_v}{G}-M\frac{\sqrt{G}_u}{\sqrt{EG}}=0\\
    \displaystyle(\frac{N}{\sqrt{G}})_u-(\frac{M}{\sqrt{G}})_v-L\frac{\sqrt{G}_u}{E}-M\frac{\sqrt{E}_v}{\sqrt{EG}}=0
\end{cases}
$$


##<font color='red'>$\S 4$ </font>曲面的存在唯一性定理
如果在某个参数域上的任意点两个曲面的两个基本形式都相同,那么两个曲面可以在相差一个刚体运动变换的意义下等同.

如果 $\Gamma^\gamma_{\alpha\beta},b_{\alpha\beta},b^\beta_\alpha$ 满足 Gauss-Codazzi 方程,那么对于参数域上任意点,存在一个邻域和定义在其上的曲面,使得 $g_{\alpha\beta}du^\alpha du^\beta$ 和 $b_{\alpha\beta}du^\alpha du^\beta$ 为曲面的两个基本形式.

自然标架的运动方程是一个一阶线性偏微分方程组,Gauss-Codazzi 方程组实际上是运动方程的可积性条件.

##<font color='red'>$\S 5$ </font>正交活动标架

设切平面有两组基, 基之间有变换矩阵, 可以写作
$$
\begin{vmatrix}
    r_u\\
    r_v
\end{vmatrix}=A\begin{vmatrix}
    e_1\\
    e_2
\end{vmatrix}
$$
记
$$
dr=r_udu+r_vdv=\omega_1e_1+\omega_2e_2\\
\ \\
\begin{cases}
    \omega_1=a_{11}du+a_{21}du\\
    \omega_2=a_{12}du+a_{22}du
\end{cases}\\
或者\\
\begin{vmatrix}
    \omega_1\\
    \omega_2
\end{vmatrix}=A\begin{vmatrix}
    du\\
    dv
\end{vmatrix}
$$
则 $\omega_1$ 和 $\omega_2$ 是定义在该参数区域上的一阶微分形式, 是 $dr$ 在标准基下的分量
利用微分形式, 曲面的第一基本形式可以表示为
$$
I=\langle dr,dr\rangle=\langle dr,e_1\rangle\langle e_1,dr\rangle+\langle dr,e_2\rangle\langle e_2,dr\rangle=\omega_1\omega_1+\omega_2\omega_2\\
I=|du,dv|AA^T\begin{vmatrix}
    du\\
    dv
\end{vmatrix}
$$
也就是说
$$
AA^T=\begin{vmatrix}
    E & F\\
    F & G
\end{vmatrix}
$$

对于空间正交标架求微分, $de_i=\omega_{i1}e_1+\omega_{i2}e_2+\omega_{i3}e_3$, 其中$\omega_{ij}=\langle de_i,e_j\rangle$
矩阵 $(\omega_{ij})$ 是反对称的

曲面的第二基本形式也可以写为
$$
II=\langle dr,de_3\rangle=\omega_1\omega_{13}+\omega_2\omega_{23}
$$

---
两个基本形式完全由正交标架的运动方程的系数决定, 并且第一基本形式与标架选取无关, 第二基本形式与法向正交标架选取无关

由于 $A$ 可逆, 所以 $du,dv$ 可以表示为 $\omega_1,\omega_2$ 的线性组合. 而一阶微分形式 $\omega_{13},\omega_{23}$ 也是 $du,dv$ 的线性组合, 所以可以用 $\omega_1,\omega_2$ 的线性组合表示.
$$
\begin{vmatrix}
    \omega_{13}\\
    \omega_{23}
\end{vmatrix}=B\begin{vmatrix}
    \omega_1\\
    \omega_2
\end{vmatrix}
$$
其中 $B$ 的系数矩阵记作 $h_{\alpha\beta}$
则曲面的第二基本形式为:
$$
II=|\omega_1,\omega_2|\begin{vmatrix}
    h_{11} & h_{21}\\
    h_{12} & h_{22}
\end{vmatrix}\begin{vmatrix}
    \omega_1\\
    \omega_2
\end{vmatrix}=|du,dv|\begin{vmatrix}
    L & M\\
    M & N
\end{vmatrix}\begin{vmatrix}
    du\\
    dv
\end{vmatrix}
$$
说明
$$
\begin{vmatrix}
    L & M\\
    M & N
\end{vmatrix}=A\begin{vmatrix}
    h_{11} & h_{21}\\
    h_{12} & h_{22}
\end{vmatrix}A^T=ABA^T
$$
而且 $B$ 是对称矩阵. $B$ 的特征值是曲面的主曲率, 行列式的值 $|B|$ 是曲面的 Gauss 曲率, 迹的一半 $(1/2)trB$ 是曲面的平均曲率. $B$ 还是 Weinggarten 变换在基 $\{e_1,e_2\}$ 下的矩阵.

当取曲面的主方向为 $\{e_1,e_2\}$ 时, $B$ 是对角矩阵,这时第二基本形式就是 $II=k_1\omega_1\omega_1+k_2\omega_2\omega_2$

##<font color='red'>$\S 6$ </font>外微分法得到的曲面结构方程

平面参数区域 $D$ 上的一阶外微分形式形如 $\theta=fdu+gdv$, 可以看作独立变量的微分张成的线性空间中的元素
定义两个外微分形式的外积 $\wedge$, 满足线性性,结合律和反交换律

反对称性 (antisymmetric), 其中 $\alpha, \beta$ 分别是 k-form l-form
$$
\alpha\wedge\beta=(-1)^{kl}\beta\wedge\alpha
$$

$\theta\wedge\phi=(f_1g_2-f_2g_1)du\wedge dv$, 其中 $fdu\wedge dv$ 可以视作张成的平行四边形有向面积微元, 称为二阶外微分形式. 同时函数 $f$ 称为零阶外微分形式.

微分形式间定义外微分运算 $d$ :
1. 对于零阶外微分 $df=\displaystyle\frac{\partial f}{\partial u}du+\frac{\partial f}{\partial v}dv$
2. 对于一阶外微分 $d\theta=df\wedge du+dg\wedge dv=\displaystyle(-\frac{\partial f}{\partial v}+\frac{\partial g}{\partial u})du\wedge dv$
3. 对于二阶外微分 $d\phi=df\wedge du\wedge dv=\displaystyle(\frac{\partial f}{\partial u}du+\frac{\partial f}{\partial v}dv)\wedge du\wedge dv$

**外微分的莱布尼茨公式**, $k$ 是 $\alpha$ 的阶数
$$
d(\alpha\wedge\beta)=d\alpha\wedge\beta+(-1)^k\alpha\wedge d\beta
$$

还具有以下性质:
1. $d(fg)=(df)g+f(dg)$
2. $d(f\wedge\theta)=df\wedge\theta+fd\theta$
3. $d(\theta\wedge f)=d\theta f-\theta\wedge df (因为 \theta 是 1-form)$
4. $d(df)=0$

---

对**正交标架的运动方程**
$$
\begin{cases}
    dr=\omega_1e_1+\omega_2e_2\\
    de_i=\omega_{ij}e^j
\end{cases}
$$
进行外微分, 得到:
$$
\begin{cases}
    \begin{cases}
        d\omega_1=\omega_2\wedge\omega_{21}\\
        d\omega_2=\omega_1\wedge\omega_{12}
    \end{cases}\\
    Gauss 方程:\\
    d\omega_{12}=\omega_{13}\wedge\omega_{32}\\
    Codazzi 方程:\\
    \begin{cases}
        d\omega_{13}=\omega_{12}\wedge\omega_{23}\\
        d\omega_{23}=\omega_{21}\wedge\omega_{13}
    \end{cases}
\end{cases}
$$
以上就是**曲面正交标架的结构方程组**

---

以下的量与正交标架的选取无关, 都是**曲面的几何量**:
1. 第一基本形式
   $I=\omega_1\omega_1+\omega_2\omega_2$
2. 面积元
   $dA=\omega_1\wedge\omega_2$
3. 第二基本形式
   $II=\omega_1\omega_{13}+\omega_2\omega_{23}$
4. 第三基本形式
   $III=\langle de_3,de_3\rangle=\omega_{13}\omega_{13}+\omega_{23}\omega_{23}$
5. Gauss 映射的面积元
   $d\sigma=\omega_{13}\wedge\omega_{23}=Kdu\wedge dv$
6. Hopf 不变式
   $\psi=\omega_1\omega_{23}-\omega_2\omega_{13}$