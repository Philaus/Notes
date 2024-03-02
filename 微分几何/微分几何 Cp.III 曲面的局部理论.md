# Cp.III 曲面的局部理论

## <font color='red'>$\S 1$  </font>曲面的概念

从平面区域 $D\{(u,v)\}$ 到 $E^3$ 的映射
$$
\boldsymbol{r}(u,v)=(x(u,v),y(u,v),z(u,v))
$$
满足: 
1. 每个分量无限阶连续可微
2. 切向量线性无关, 即 $\boldsymbol{r}_u\wedge\boldsymbol{r}_v\neq\boldsymbol{0}$

这时称 $\boldsymbol{r}$ 是 $E^3$ 的一个曲面(片), $(u,v)$是曲面的坐标参数
特别的,当由函数 $z=f(x,y)$ 描述曲面 $\boldsymbol{r}(u,v)=(x,y,z(x,y))$ 时, 称为函数 $f$ 的图

两个坐标切向量张成曲面在一点的切平面 $T_{P_0}S$ ,这一点上与切平面的垂线称为该点的法线
这样构成 $E^3$ 的一个自然定向的标架 $\{P_0;\boldsymbol{r}_u,\boldsymbol{r}_y,\boldsymbol{r}_u\wedge\boldsymbol{r}_y\}$

对曲面任意一点, 切平面是曲面上过该点的曲线在该点切向量的全体

$F(x,y,z)$ 是定义在 $E^3$ 的一个区域 $U$ 上的光滑函数
$$
S_c=\{(x,y,z)|F(x,y,z)=Const\}\neq \emptyset\\
$$
是 $F$ 的等值面,当 $F$ 的梯度不为零时, $S_c$ 是一个曲面, 在一点 $P_0=(x_0,y_0,z_0)$ 的切平面方程为:
$$
F_x(P_0)(x-x_0)+F_y(P_0)(y-y_0)+F_z(P_0)(z-z_0)=0
$$

## <font color='red'>$\S 2$  </font>曲面的第一基本形式

任何一个切向量都可以被坐标切向量线性表出, 切向量的长度平方可以表示为:
$$
\boldsymbol{v}=\lambda\boldsymbol{r}_u+\mu\boldsymbol{r}_v\\
\langle\boldsymbol{v},\boldsymbol{v}\rangle=\lambda^2\langle\boldsymbol{r}_u,\boldsymbol{r}_u\rangle+2\lambda\mu\langle\boldsymbol{r}_u,\boldsymbol{r}_v\rangle+\mu^2\langle\boldsymbol{r}_v,\boldsymbol{r}_v\rangle=\lambda^2E+2\lambda\mu F+\mu^2G
$$
以矩阵 $\begin{vmatrix}
E & F \\
F & G \\
\end{vmatrix}$ 为系数的二次型

考虑 $S$ 上曲线的弧长微元, 得到一个二次微分式:
$$
I=ds^2=Edu\cdot de+2Fdu\cdot dv+Gdv\cdot dv
$$
这就是**曲面的第一形式**, 是**曲面上曲线弧长微元的平方**, 与参数选取无关, 在 $E^3$ 合同变换下不变
$$
\begin{align}
I&=Edu\cdot du+2Fdu\cdot dv+Gdv\cdot dv\\
&=\langle\boldsymbol{r}_u,\boldsymbol{r}_u\rangle dudu+2\langle\boldsymbol{r}_u,\boldsymbol{r}_v\rangle du dv+\langle\boldsymbol{r}_v,\boldsymbol{r}_v\rangle dvdv\\
&=\langle d\boldsymbol{r},d\boldsymbol{r}\rangle
\end{align}
$$
在微分几何中，第一基本形式是三维欧几里得空间中一个曲面的切空间中的内积，由 $\mathscr{R}^3$ 中标准点积诱导, 它完全描述了曲面的度量性质, 使得曲面的曲率和度量性质（比如长度与面积）可与环绕空间一致地计算.

无需知道曲面的映射的具体形式, 就可以研究曲面的一些性质 (内蕴的 intrinsic), 也就是说不需要知道曲面是如何嵌入在 $\mathscr{R}^3$ 空间中的, 或者说, 直接把定义在参数区域上的一个正定二次微分式视为度量.

## <font color='red'>$\S 3$  </font>曲面的第二基本形式

单位法向量:
$$
\boldsymbol{n}=\displaystyle\frac{\boldsymbol{r}_u\wedge\boldsymbol{r}_v}{|\boldsymbol{r}_u\wedge\boldsymbol{r}_v|}
$$
第二基本形式定义为:
$$
\begin{align}
II&=-\langle d\boldsymbol{r},d\boldsymbol{n}\rangle\\
&=-\langle\boldsymbol{r}_udu+\boldsymbol{r}vdv,\boldsymbol{n}_udu+\boldsymbol{n}_vdv\rangle\\
&=Ldudu+2Mdudv+Ndvdv
\end{align}
$$
$$
\begin{align}
    L&=\langle \boldsymbol{r}_{uu},\boldsymbol{n}\rangle=-\langle \boldsymbol{r}_{u},\boldsymbol{n}_u\rangle\\
    M&=\langle \boldsymbol{r}_{uv},\boldsymbol{n}\rangle=-\langle \boldsymbol{r}_{u},\boldsymbol{n}_v\rangle=-\langle \boldsymbol{r}_{v},\boldsymbol{n}_u\rangle\\
    N&=\langle \boldsymbol{r}_{vv},\boldsymbol{n}\rangle=-\langle \boldsymbol{r}_{v},\boldsymbol{n}_v\rangle\\
\end{align}
$$
第二基本形式是一个二次微分形式, 是曲面上点 $(u_0+\Delta u,v_0+\Delta v)$ 到一点 $(u_0,v_0)$ 切平面有向距离的极限, 反映了曲面的形状.

第二基本形式就展现了曲面在母空间中的嵌入方式.

第二基本形式是关于 $(du,dv)$ 的二次型, 对 $LN-M^2$ ,这个表达式可以分为三种情形:
1. \>0,第二基本形式是正定或者负定的,在该点附近曲面是凸的(凹的)
2. <0,第二基本形式是不定的,附近是马鞍形
3. =0,第二基本形式是退化的

曲面在不同参数间变换时,如果变换同向, $II$ 不变,如果反向则变号.

---
第一基本形式反映了曲面上曲线的弧长微元, 第二基本形式反映了曲面在空间中的形状. 两个基本型都是关于参数微分 $du\ dv$ 的二次型, 通称二次微分式. 并且第一基本型是正定的.


## <font color='red'>$\S 4$  </font>法曲率与Weingarten变换

曲面上有过点 $P_0$ 的曲线 $S$, 曲线在 $P_0$ 的单位切向量为:
$$
\displaystyle\frac{d\boldsymbol{r}}{ds}|_{s=0}=(\boldsymbol{r}_{u}\frac{du}{ds}+\boldsymbol{r}_{v}\frac{dv}{ds})|_{s=0}
$$
它在这一点的曲率向量是:
$$
\displaystyle\frac{d^2\boldsymbol{r}}{ds^2}|_{s=0}=[\boldsymbol{r}_{u}\frac{d^2u}{ds^2}+\boldsymbol{r}_{v}\frac{d^2v}{ds^2}+\boldsymbol{r}_{uu}(\frac{du}{ds})^2+2\boldsymbol{r}_{uv}\frac{du}{ds}\frac{dv}{ds}+\boldsymbol{r}_{vv}(\frac{dv}{ds})^2]_{s=0}
$$
前两项是切向分量, 后三项是法向分量, 下面仅考虑法向部分:
$$
\begin{align}
k_n&=\langle \displaystyle\frac{d^2\boldsymbol{r}}{ds^2},\boldsymbol{n}\rangle\\
&=L(\frac{du}{ds})^2+2M\frac{du}{ds}\frac{dv}{ds}+N(\frac{dv}{ds})^2
\end{align}
$$
这就是法曲率, 表示曲面沿那个方向的弯曲程度
任取一个单位切向量 $\boldsymbol{x}=\lambda \boldsymbol{r}_{u}+\mu\boldsymbol{r}_{v}$, 曲面在该点沿这个切向量方向的法曲率为:
$$
k_n(\boldsymbol{x})=L\lambda^2+2M\lambda\mu+N\mu^2
$$
如果所取的切向量不是单位向量, 而是 $\boldsymbol{w}=\xi \boldsymbol{r}_{u}+\eta\boldsymbol{r}_{v}$, 则法曲率表示为:
$$
\begin{align}
k_n(\boldsymbol{w})&=(L\xi^2+2M\xi\eta+N\eta^2)/(|\boldsymbol{w}|^2)\\
&=\displaystyle\frac{L\xi^2+2M\xi\eta+N\eta^2}{E\xi^2+2F\xi\eta+G\eta^2}\\
&=\displaystyle\frac{II(\boldsymbol{w},\boldsymbol{w})}{I(\boldsymbol{w},\boldsymbol{w})}
\end{align}
$$

1. $LN-M^2>0$ 时, 沿任何方向的法曲率同号, 曲面在任意方向的弯曲同向, 称为椭圆点
2. $LN-M^2<0$ 时 ,$k_n(\boldsymbol{x})=0$ 有两个线性无关的解, 这两个解称为曲面在该点的渐进方向, 两个渐进方向将切平面分割为四个区域, 在相对的两个区域法曲率同号, 称为双曲点
3. $LN-M^2=0$ 时, 称为抛物点. 当 $LMN$ 不全为零时, 仅有一个切方向时法曲率为零, 这个方向也称为渐进方向, 将切平面分为两个区域, 这两个区域内法曲率均不为零且符号相同. 特别的, 当$L=M=N=0$, 称为平点, 法曲率恒为零

---
曲面在每一点有一个确定的单位法向量
$$
\boldsymbol{n}=\displaystyle\frac{\boldsymbol{r}_u\wedge\boldsymbol{r}_v}{|\boldsymbol{r}_u\wedge\boldsymbol{r}_v|}
$$
平行移动 $\boldsymbol{n}$ 使之起点落在原点,则 $\boldsymbol{n}$ 的终点就落在 $E^3$ 的单位球面 $S^2$ 上, 这样得到一个映射
$$
S\rightarrow S^2\\
\boldsymbol{r}(u,v)\rightarrow\boldsymbol{n}(u,v)\\
$$
称为曲面 $S$ 的 Gauss 映射 $\boldsymbol{g}$ 

设 $\boldsymbol{r}(u(t),v(t))$ 是参数区域 $D$ 上曲面上一条曲线 ,Gauss 映射沿着曲线求微分
$$
\displaystyle\frac{d\boldsymbol{n}(t)}{dt}=\boldsymbol{n}_u\frac{du}{dt}+\boldsymbol{n}_v\frac{dv}{dt}
$$
由于 $\boldsymbol{n}$ 是单位向量,所以 $\langle \displaystyle\frac{d\boldsymbol{n}}{dt},\boldsymbol{n}\rangle=0$, 立即看出 $\displaystyle\frac{d\boldsymbol{n}}{dt}$ 也是曲面的切向量 ,这样可以定义一个切平面到切平面的线性变换 $\mathscr{W}$:
$$
\boldsymbol{x}=\lambda \boldsymbol{r}_{u}+\mu\boldsymbol{r}_{v}\rightarrow\mathscr{W}(\boldsymbol{x})=-(\lambda \boldsymbol{n}_{u}+\mu\boldsymbol{n}_{v})
$$
称为曲面的 Weingarten 变换, 这个变换与曲面的参数无关

利用 Weingarten 变换可以给出法曲率的另一种描述:
$$
k_n(\boldsymbol{x})=\langle\mathscr{W}(\boldsymbol{x}),\boldsymbol{x}\rangle
$$
Weingarten 变换是曲面切平面到自身的自共轭变换,是对称变换
设 $\boldsymbol{v}$ 和 $\boldsymbol{w}$ 都属于 $T_{P}S$
$$
\langle\mathscr{W}(\boldsymbol{v}),\boldsymbol{w}\rangle=\langle\boldsymbol{v},\mathscr{W}(\boldsymbol{w})\rangle
$$

## <font color='red'>$\S 5$  </font>法曲率与 Gauss 曲率

由 Weingarten 变换的性质,可以发现变换对应的矩阵是一个**二阶埃尔米特矩阵**, 两个特征值都是实数
这两个特征值称为曲面在一点的**主曲率**, 对应的两个实特征方向称为主方向.
当两个主曲率不相等时, 两个主方向完全确定且正交; 当主曲率相等时, 任意切向都是主方向.

Weingarten变换的系数矩阵为:
$$
\begin{vmatrix}
a & b \\
c & d \\
\end{vmatrix}=
\begin{vmatrix}
L & M \\
M & N \\
\end{vmatrix}
\begin{vmatrix}
E & F \\
F & G \\
\end{vmatrix}^{-1}\\
~\\
=\displaystyle\frac{1}{EG-F^2}
\begin{vmatrix}
LG-MF & ME-LF \\
MG-NF & NE-MF \\
\end{vmatrix}
$$
主曲率满足特征方程. 把两个主曲率的平均值称为平均曲率, 两个主曲率的乘积称为 Gauss 曲率.
$$
\begin{align}
H&=(k_1+k_2)/2=\displaystyle\frac{1}{2}\frac{LG-2MF+NE}{EG-F^2}\\
G&=k_1k_2=\displaystyle\frac{LN-M^2}{EG-F^2}
\end{align}
$$
Gauss 曲率还满足:
$$
\boldsymbol{n}_u\wedge\boldsymbol{n}_v=K\boldsymbol{r}_u\wedge\boldsymbol{r}_v
$$

Euler 公式:
$$
k_n(\boldsymbol{x})=k_1cos^2\theta+k_2sin^2\theta
$$
其中 $\boldsymbol{x}$ 是切平面的单位向量, $\boldsymbol{x}$ 与主方向 $e_1$ 的夹角为 $\theta$ 
由这个公式可以看出, 当两个主曲率不等时, 法曲率在主方向取到最值.

满足在每一点的切向都是曲面在该点的主方向的曲面上的曲线称为曲率线.

当两个主曲率相等, 法曲率对任意方向恒等, 表示曲面沿任何方向弯曲程度是一样的. 这种情况下:
$$
\displaystyle\frac{L}{E}=\frac{M}{F}=\frac{N}{G}=k
$$
这样的点称为曲面的脐点. 特别的, k 不为零的点称为原点. $k=0$ 时, $L=M=N=0$, 这时该点是曲面的平点.

平面曲线的曲率是曲线的 Gauss 映像在单位圆上的位移速度

## <font color='red'>$\S 6$  </font>举例
###旋转曲面

对于旋转曲面 $\boldsymbol{r}(u,v)=(f(u)cos\ v,f(u)sin\ v,g(u))$(f>0)

则直接计算可得:
$$
\begin{gather}
E=f'^2+g'^2,F=0,G=f^2\\
L=\displaystyle\frac{f'g''-f''g'}{\sqrt{f'^2+g'^2}}\\
M=0,N=\frac{fg'}{\sqrt{f'^2+g'^2}}\\
K=\frac{(f'g''-f''g')g'}{(f'^2+g'^2)^2f}\\
H=\frac{1}{2}\{\frac{f'g''-f''g'}{(f'^2+g'^2)^{3/2}}+\frac{g'}{f\sqrt{f'^2+g'^2}}\}\\
k_1=\displaystyle\frac{f'g''-f''g'}{(f'^2+g'^2)^{3/2}}\\
k_2=\displaystyle\frac{g'}{f\sqrt{f'^2+g'^2}}\\
\end{gather}
$$
如果选取 u 为 xz 平面上曲线 $(f(u),g(u))$ 的弧长参数,则 $f'^2+g'^2=1$, 这时:
$$
\begin{gather}
K=-f''/f,H=1/2[g'/f-f''/g']\\
k_1=-f''/g',k_2=g'/f
\end{gather}
$$

---
###常 Gauss 曲率旋转曲面
1. $K=c^2>0$
   半径为 c 的球面
2. $K=0$
   $f=Au+b,g=\pm\sqrt{1-A^2}u+C$,$0\le A\le 1$
   A=0 为圆柱面, A=1 为平面, 其他为圆锥面
3. $K=-c^2<0$
   $$
   f=Acosh\ cu+Bsinh\ cu\\
   g=\pm\displaystyle\int\sqrt{1-c^2(Acosh\ cu+Bsinh\ cu)^2}du
   $$
   特别的, 当
   $$
   f=\displaystyle\frac{1}{c}e^{-cu}\\
   g=\pm\displaystyle\int^u_0\sqrt{1-e^{-2ct}}dt
   $$
   时, 曲面为伪球面

---
###常平均曲率旋转曲面
1. H=0, 这样的曲面称为极小曲面
   $$
   f=\sqrt{u^2+2Au+B}\\
   g=\pm \sqrt{\displaystyle\frac{B-A^2}{u^2+2Au+B}}
   $$
   当 $A=0,B=a^2$ 时, xz 的方程消去 u,得到 $x=acosh\frac{z}{a}$, 这恰好是一条悬链线, 这样的旋转曲面是悬链面
2. H 不为零时
   $$
   f=\displaystyle\frac{1}{2H}\sqrt{1+B^2+2Bsin2Hu}\\
   \ \\
   g=\displaystyle\int ^u_0\frac{1+2Bsin2Ht}{dt\sqrt{1+B^2+2Bsin2Ht}}dt
   $$
   旋转常平均曲率曲面又称 Delaunay 曲面

---
###直纹面
直纹面是由单参数曲线族构成的曲面, 参数表达式为:
$$
\boldsymbol{r}(u,v)=\boldsymbol{a}(u)+v\boldsymbol{b}(u)
$$
其中 $\boldsymbol{a}(u)$ 是一条空间曲线, $\boldsymbol{b}(u)$ 是随 u 变化的一个方向,固定 u 时,$\boldsymbol{a}(u)+v\boldsymbol{b}(u)$ 是过点 $\boldsymbol{a}(u)$ 沿方向 $\boldsymbol{b}(u)$ 的一条直线

直纹面的 Gauss 曲率不大于零

---
###可展曲面
Gauss 曲率恒为零的直纹面称为可展曲面

直纹面是可展曲面当且仅当:
1. $(\boldsymbol{a}',\boldsymbol{b},\boldsymbol{b}')=0$
2. 沿着直母线, 直纹面的法向量不变, 即 $\boldsymbol{n}(u,v_1)=\boldsymbol{n}(u,v_2)$

当 a 为常值, 可展曲面是以 a 为顶点的锥面 ,所有母线过定点
当 b 与 u 无关, 是柱面, 这时直母线均平行
$\boldsymbol{r}(t)$ 是空间一条正则曲线, 则它的切线全体构成一张曲面 $\boldsymbol{r}(v,t)=\boldsymbol{r}(t)+v\boldsymbol{r}'(t)$, 称为切线面

---
###全脐点曲面
曲面的每一个点都是脐点, 称为全脐点曲面, 当且仅当:
1. 曲面的两个基本形式满足 $II=kI$,$k$ 是曲面上的函数
2. 曲面是平面或球面