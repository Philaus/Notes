# 等离子体 Cp.III 单粒子轨道

##<font color='red'>$\S 1$ </font>均匀恒定磁场中的运动

设 $u=x+iy$, 这样运动方程为:
$$
u''+i\omega u'=0
$$

定义电子和粒子回旋频率 $\omega_{ce}=eB/m_e$ 和 $\omega_{ie}=ZeB/m_i$

定义电子和粒子回旋半径 $r_{ce}=v_{\bot}/\omega_{ce}$ 和 $r_{ie}=v_{\bot}/\omega_{ie}$

回旋运动会产生电流, 产生磁矩, 表示为:
$$
\boldsymbol{\mu}=I\pi r_{c}^2\boldsymbol{n}=-\frac{W_{\bot}}{B}\boldsymbol{b}
$$
这个磁矩与磁场方向反平行, 表明等离子体是抗磁性物质.

这个磁矩及回旋轨道所包围面积的磁通量都是守恒量.

##<font color='red'>$\S 2$ </font>电场漂移

磁约束中, 主要关心粒子回旋中心在垂直磁场方向的移动, 也就是漂移.
当磁场变化不大, 电场不大时 (都是对于时间和空间的相对尺度而言), 可以将粒子回旋中心的移动和回旋运动分离 (这种分离是有条件的), 并且这种近似称漂移近似.

假设存在一个垂直于磁场的较小的电场, 运动方程中将加入电场力的一项
如果将速度进行分解, 使得 $v=v_{\bot}'+v_D$, 其中 $v_D=E\times B/B^2$, 这个速度就是电场导致的漂移

同理, 其他外力 (比如重力) 也可以导致漂移, 但是很明显此时的漂移会导致极化
$$
v_D=F\times B/qB^2
$$

##<font color='red'>$\S 3$ </font>缓变电场中的运动
缓变电场意味着我们要关注电场随时间的一阶导, 而忽略高阶导. 由于纵向的电场不影响漂移, 所以默认电场是横向的.

处理上, 对运动方程先求导, 再将速度的一阶导带入二阶方程, 得到
$$
v_{\bot}''+\omega_{ce}^2 v_{\bot}=\omega_{ce}^2\frac{E\times B}{B^2}+\frac{q}{m}\frac{dE}{dt}
$$
速度阶展开, $v=v^{(0)}+v^{(1)}$

如果不存在电场, 运动方程应当为回旋运动
$$
{v_{\bot}^{(0)}}''+\omega_{ce}^2 v_{\bot}^{(0)}=0
$$
再利用一阶修正速度的时间二阶导为零
$$
v^{(1)}_{\bot}=\frac{E\times B}{B^2}+\frac{q}{mB^2}\frac{dE}{dt}
$$
第一项就是电场引起的漂移, 第二项是电场随时间的变化引起的漂移

---

注意到电场随时间的变化引起的漂移与电荷电性有关, 也就是说会导致正负电荷的分离, 产生极化电流
$$
j_P=\frac{\rho_M}{B^2}\frac{dE}{dt}
$$
$\rho_M$ 是等离子体质量密度

根据麦克斯韦方程
$$
\nabla\times H=(j+j_P)+\epsilon_0\frac{\partial E}{\partial t}=j+[\epsilon_0+\frac{\rho_M}{B^2}]\frac{\partial E}{\partial t}
$$
也就是说如果考虑极化电流, 等离子体的介电常量
$$
\epsilon=\epsilon_0[1+\frac{n(m_i+m_e)}{\epsilon_0B^2}]
$$
对于多数典型的等离子体, ${n(m_i+m_e)}/{\epsilon_0B^2}\gg1$
所以, 对于变化电场, 等离子体通常可以看作介电常量非常大的电介质

##<font color='red'>$\S 4$ </font>不均匀磁场中的漂移
现在假设磁场的不均匀性很小, 在一个回旋轨道中磁场基本不变, 这样仍然可以应用漂移近似.
$$
|r_c\cdot \nabla B|\ll B
$$
###梯度漂移
磁场满足缓变条件, 在回旋中心展开
$$
B\approx B_0+(r_c\cdot \nabla) B_0
$$
将速度分解为回旋运动和漂移运动, 连同磁场的展开是全部带入运动方程
发现 $r_c$ 和 $v_0$ 都是简谐量, 对运动方程取周期平均, 含奇数个周期因子的项平均值为 0. 得到:
$$
(v_D\times B_0)+\langle v_0\times (r_c\cdot \nabla) B_0\rangle=0
$$
漂移速度的一般形式
$$
\boldsymbol{v}_D=\frac{W_{\bot}}{qB^3}\boldsymbol{B}\times \nabla B=\frac{(-\mu\nabla B)\times \boldsymbol{B}}{qB^2}
$$
磁场梯度漂移看起来就像是一个作用在磁矩上的外力导致的漂移, $F=-\mu\nabla B$
带电粒子在磁场中运动时, 受到一个反向于磁场梯度的力, 指向弱磁场的方向, 也说明了等离子体粒子的反磁性

---
###曲率漂移

如果磁力线是弯曲的, 粒子会受到离心力, 离心力导致的曲率漂移速度
$$
v_D=\frac{2W_\parallel}{qB^2R^2}\boldsymbol{R}\times\boldsymbol{B}=\frac{2W_\parallel}{qB^2}\boldsymbol{B}\times(\boldsymbol{b}\cdot \nabla)\boldsymbol{b}
$$
如果研究的空间点不存在电流, $\nabla\times\boldsymbol{B}=0$, 则 $\nabla B/B=-\boldsymbol{R}/R^2$
$$
v_D=\frac{2W_\parallel}{qB^3}\boldsymbol{B}\times\nabla B
$$
由于磁场存在曲率时一定存在梯度, 两个效应合起来就是
$$
v_D=\frac{W_{\bot}+2W_\parallel}{qB^3}\boldsymbol{B}\times\nabla B=\frac{W_{\bot}+2W_\parallel}{qB^2R^2}\boldsymbol{R}\times\boldsymbol{B}
$$

##<font color='red'>$\S 5$ </font>浸渐不变量

为了便于求解微分方程, 最好能找到运动积分 (守恒量). 当某些参量变化足够缓慢时, 有些物理量近似为运动常量, 称为浸渐不变量

###磁矩不变量
当磁场随时间空间缓变时, 磁矩 $\mu=W_{\bot}/B$ 是浸渐不变量

利用这一点, 可以发现粒子横向动能与磁场成正比, 所以对于初始速度方向与磁场夹角足够大的粒子, 总有一个位置可以使得纵向动能为零, 使得粒子轨道在强磁场端折返.

假设磁场最大点磁场强度是初始点的 $\eta$ 倍, 则临界投射角为 $\theta_c=\arcsin\sqrt{1/\eta}$, 初始速度角小于临界角的粒子不能被磁镜束缚, 产生终端损失, 损失率 $p=1-\sqrt{1-1\eta}$.

由于存在溢出锥, 粒子速度分布将不再平衡, 会由碰撞趋于平衡, 从而继续溢出, 所以单一磁镜不能很好的维持粒子.
###纵向不变量

如果磁场满足缓变条件 $\displaystyle|\tau \frac{\partial B}{\partial t}|\ll B$, 可以证明纵向作用积分 $\displaystyle J=\oint mv_\parallel dz$ 是浸渐不变量. 粒子的纵向速度和在该方向的位移在相空间所包围的面积近似为一个守恒量.

根据这个不变量, 被磁镜捕获的粒子, 或是处在相向运动的磁镜中的粒子会加速, 纵向动能增大, 称为费米加速. 粒子的纵向速度不断增加, 最后会大于临界角, 从而从磁镜中逃逸.

##<font color='red'>$\S 6$ </font>环形磁场中的运动
简单环形磁场不能有效的约束等离子体.
假设磁场只有环向分量, 则磁场的梯度全部沿径向. 根据曲率漂移的理论, 这将会导致正负粒子沿竖直轴方向极化, 极化后的电场又产生电场漂移, 正负粒子都沿径向漂移并撞上容器壁.

如果给磁场加入圆环横截面极角方向的分量, 与原磁场合并为一个旋转磁场, 新的场线不是简单圆环, 其在截面的投影在一个空间周期内会旋转一定角度, 并且一般来说不闭合. 这种磁场结构能抵消磁漂移, 是托卡马克设计的基础.

---
设一个旋转磁场为 $B=B_\phi+B_\theta$, 并且 $B_\phi \gg B_\theta$. 其中 $\theta$ 是环截面角方向, $\phi$ 是大环角方向.

从一点出发的磁力线绕环一周后在截面的投影旋转角度设为 $\zeta$ .称为旋转变换角. 如果旋转变换角是 $2\pi$ 的无理数倍, 那么磁力线是不闭合的, 构成一个无理磁面. 从小圆中心出发的磁力线不发生旋转, 称为磁轴.

由旋转变换角引入一个参量 $q(r)=2\pi/\zeta$ ,表示一根磁力线绕磁轴一周在大环上所需要的圈数. 这个参数是衡量磁约束装置类型的一个重要参数, 对托卡马克装置, 需要 $q>1$, 这是抑制磁流体螺旋不稳定性的条件, 所以 q 也称为安全因子. 但是对于例如反向箍缩类型的装置, 则要求 $q<1$.

设旋转磁力线的螺距为 d , 磁力线到磁轴的距离为 r ,则 $\displaystyle\zeta=2\pi(\frac{2\pi R_0}{d})=\frac{2\pi R_0 B_\theta}{r B_\phi}$

假设等离子体的半径就是磁力线到磁轴的距离, 此时的安全因子就是 $q=\displaystyle\frac{2B_\phi}{R_0B_\theta}$

---
环形磁场的内侧强外侧弱, 构成一个磁镜, 纵向速度较低的粒子会在其中被捕获, 而速度较大的粒子能在投影截面完成一整个环形运动.

对于通行粒子, 由于漂移, 粒子运动中心实际运动的轨道会偏离磁力线. 忽略 $B_\theta$ 的梯度, 只考虑 $B_\phi$ 的梯度漂移 $v_D$ ,加上径向速度在环截面的投影 $v_\parallel B_\theta/B$, 得到
$$
\frac{dr}{dx}=\frac{v_DB}{v_\parallel B_\theta}\equiv\alpha_0\ll1
$$
方程的解表示 r 和 x 成线性关系, 平方后忽略二阶项, 说明投影的运动轨道是一个圆, 圆心偏离磁轴 $\alpha_0 r_0\approx r_cq(r_0)$, 由于 q 一般取 2~3, 所以偏移量大约就是 2~3 倍的粒子回转半径, 约束是很有效的.

对于捕获粒子, 其纵向动量在靠近环内侧的两个端点为 0 ,由于在一个周期内粒子速度会反向, 所以漂移导致的速度产生的效应也不同. 此时的方程为
$$
\frac{dr}{dx}=\pm\frac{v_DB}{v_\parallel B_\theta}
$$
正对应顺时针旋转, 负对应逆时针.
由磁矩不变量, $v_\parallel=v_0\sqrt{1-B/B_M}$
磁场近似关系, $B\approx B_\phi\approx B_0(1-x/R_0)$
$$
\frac{dr}{dx}=\pm\frac{v_DB_0}{v_0 B_\theta}\sqrt{R_0/(x-x_M)}
$$
因为偏离磁面不远, $B_\theta$ 取为常量, 因为 $v_\parallel\ll v_\bot$, $v_D$ 也近似为常量
直接积分可以得到
$$
r-r_0\approx \pm\frac{2v_DB_0}{v_0B_\theta}\sqrt{R_0r_0(\cos\theta-\cos\theta_M)}
$$
这个轨道在截面的投影就近似为一个香蕉形的闭合曲线, $\theta=0$ 处的半宽度 $\Delta r_T<2q(r_0)r_c/\sqrt{\varepsilon}\approx(10\sim 20)r_c$