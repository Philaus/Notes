# Cp.IV 电磁波的传播

## <font color='red'>$\S 1$  </font>均匀平面电磁波

均匀平面电磁波解中的关系:
$$
\boldsymbol{B}=\frac{1}{\omega}\boldsymbol{k}\times\boldsymbol{E}=\sqrt{\mu\epsilon}\boldsymbol{n}\times\boldsymbol{E}
$$
平面电磁波 E B 同相, 且振幅比为 v (高斯单位制下真空中这个比值就是 1).

如果对于一定的频率且满足电场散度为零, 波方程可以写为亥姆霍兹方程. 每一个符合条件的解称作一个波模.
$$
\begin{cases}
\nabla^2\boldsymbol{E}+k^2\boldsymbol{E}=0\\
\nabla\cdot \boldsymbol{E}=0\\
\displaystyle\boldsymbol{B}=-\frac{i}{\omega}\nabla\times\boldsymbol{E}\\
\end{cases}
$$
对于时谐电磁波, 麦克斯韦方程组不是独立的, 两个散度方程可以由其他两个得到. 所以边值关系也不是独立的, 只需要关注与 E 和 H 有关的两个即可.

正常色散关系：
$$
k^2\equiv\boldsymbol{k}\cdot \boldsymbol{k}=\mu\epsilon\omega^2
$$
单色平面电磁波在线性均匀绝缘介质中的波速是相速度，即相位保持相同的点在空间移动的速度：
$$
v=\displaystyle\frac{\omega}{k}=\displaystyle\frac{1}{\sqrt{\mu\epsilon}}=\displaystyle\frac{c}{n}
$$
真实介质在广阔的频谱内都是色散介质，折射率通过 $\mu\epsilon$ 依赖于 $\omega$。宽谱电磁波可以由傅里叶变换分解, 在窄频率范围内，如果忽略色散效应，可以认为折射率与频率无关，这时将平面波解 $\boldsymbol{\psi}=\boldsymbol{\psi_0}e^{i\boldsymbol{k}\cdot \boldsymbol{x}-i\omega t}$ 叠加就可以写出波动方程的通解.

介质的波阻抗 Z=$\displaystyle\sqrt{\frac{\mu}{\epsilon}}$, 对于真空, 这个值约为 376.7$\Omega$.

---
约定电场方向为偏振方向.
可以引入三个标准正交基来表示复振幅，其中第三个基沿电磁波波矢方向
$$
\boldsymbol{E}(\boldsymbol{x},t)=(E_1\boldsymbol{e_1}+E_2\boldsymbol{e_2})e^{i\boldsymbol{k}\cdot \boldsymbol{x}-i\omega t}
$$
一般来说，两个复相角是不同的（二者之比不是实数），如果相等，称为线偏振
如果$E_1/E_2=\pm i$，称为左旋或右旋圆偏振。对圆偏振，可以引入复单位矢量描述：
$$
\boldsymbol{e_\pm}=\displaystyle\frac{1}{\sqrt2}(\boldsymbol{e_1}\pm i\boldsymbol{e_2})
$$
满足正交归一关系：
$$
\begin{aligned}
\boldsymbol{e_\pm^*}=\boldsymbol{e_\pm^*}\cdot \boldsymbol{n}&=\boldsymbol{e_\pm^*}\cdot \boldsymbol{e_\mp}=0\\
\boldsymbol{e_\pm^*}\cdot\boldsymbol{e_\pm}&=1
\end{aligned}
$$

---
约定任何可测的物理量都用复表示的实部表示.

电磁场能量密度 $\omega=(\boldsymbol{E}\cdot\boldsymbol{D}+\boldsymbol{B}\cdot\boldsymbol{H})/2$

坡印廷矢量的时间平均值代表了一个周期中平均通过的能流：
$$
\boldsymbol{S}=\displaystyle\frac{1}{2}(\boldsymbol{E}\times\boldsymbol{H}^*)=\frac{1}{2}\sqrt{\frac{\epsilon}{\mu}}|\boldsymbol{E}|^2\boldsymbol{n}
$$
电磁波传播的平均效果是有静能流沿波矢方向传输.

两个周期复变量乘积的时间平均:
$$
\bar{fg}=\frac{1}{2}Re\{f^*g\}
$$

电磁波能量密度的时间平均：
$$
u=\displaystyle\frac{1}{4}[\epsilon\boldsymbol{E}\times\boldsymbol{E}^*+\frac{1}{\mu}\boldsymbol{B}\times\boldsymbol{B}^*]=\frac{\epsilon}{2}|\boldsymbol{E_0}|^2
$$
沿波矢方向传递的能流密度可以写为：
$$
\boldsymbol{S}=uv_p\boldsymbol{n}
$$

## <font color='red'>$\S 2$  </font>电磁波在介质表面的折射与反射

界面的反射折射本质是边值问题. 关注的对象是界面前后的振幅比, 相对相位, 波矢方向.

入射、折射、反射波的相因子必须在介质面上时时处处相等
$$
(\boldsymbol{k}\cdot\boldsymbol{x})_{z=0}=(\boldsymbol{k'}\cdot\boldsymbol{x})_{z=0}=(\boldsymbol{k''}\cdot\boldsymbol{x})_{z=0}
$$
由此可以发现三个波矢必须共面，这个面定义为入射面.

斯涅耳 (Snell) 定律：
i 是入射角，r 是折射角
$$
\displaystyle\frac{\rm{sin}\ i}{\rm{sin}\ r}=\frac{k'}{k}=\frac{n'}{n}
$$
无源情况下介质界面处电磁场边界条件：
k 是入射波矢，k' 是折射波矢，k'' 是反射波矢
$$
\begin{cases}
[\epsilon(\boldsymbol{E_0}+\boldsymbol{E_0}'')-\epsilon'\boldsymbol{E_0}']\cdot \boldsymbol{n}=0 \\
[\boldsymbol{k}\times\boldsymbol{E_0}+\boldsymbol{k}''\times\boldsymbol{E_0}''-\boldsymbol{k}'\times\boldsymbol{E_0}']\cdot \boldsymbol{n}=0 \\
(\boldsymbol{E_0}+\boldsymbol{E_0}''-\boldsymbol{E_0}')\times \boldsymbol{n}=0 \\
[\displaystyle\frac{1}{\mu}(\boldsymbol{k}\times\boldsymbol{E_0}+\boldsymbol{k}''\times\boldsymbol{E_0}'')-\frac{1}{\mu'}\boldsymbol{k}'\times\boldsymbol{E_0}']\times \boldsymbol{n}=0 \\
\end{cases}
$$
为了便于讨论，将电场垂直和平行于入射面的分量分开计算，得到两个分量的菲涅尔 (Fresnel) 公式：
$$
\begin{cases}
\displaystyle\frac{(\boldsymbol{E}_0')_\bot}{(\boldsymbol{E}_0)_\bot}=\frac{2n\ \rm{cos}\ i}{n\ \rm{cos}\ i+\displaystyle\frac{\mu}{\mu'}n'\rm{cos}\ r}=\frac{2\sin~r\cos~i}{\sin(i+r)}\\
\displaystyle\frac{(\boldsymbol{E}_0'')_\bot}{(\boldsymbol{E}_0)_\bot}=\frac{n\ \rm{cos}\ i-\displaystyle\frac{\mu}{\mu'}n'\rm{cos}\ r}{n\ \rm{cos}\ i+\displaystyle\frac{\mu}{\mu'}n'\rm{cos}\ r}=-\frac{\sin(i-r)}{\sin(i+r)}\\
\end{cases}
$$
$$
\begin{cases}
\displaystyle\frac{(\boldsymbol{E}_0')_\parallel}{(\boldsymbol{E}_0)_\parallel}=\frac{2n\ \rm{cos}\ i}{\displaystyle\frac{\mu}{\mu'}n'\ \rm{cos}\ i+n\rm{cos}\ r}=\frac{2\sin~r\cos~i}{\sin(i+r)\cos(i-r)}\\
\displaystyle\frac{(\boldsymbol{E}_0'')_\parallel}{(\boldsymbol{E}_0)_\parallel}=\frac{\displaystyle\frac{\mu}{\mu'}n'\ \rm{cos}\ i-n\rm{cos}\ r}{\displaystyle\frac{\mu}{\mu'}n'\ \rm{cos}\ i+n\rm{cos}\ r}=\frac{\tan(i-r)}{\tan(i+r)}\\
\end{cases}
$$
注：对可见光频段，一般而言磁导率随频率的变化可以忽略，即认为$\displaystyle\frac{\mu}{\mu'}=1$.
正入射的情形：(i=0)
$$
\begin{aligned}
\boldsymbol{E}_0'=\displaystyle\frac{2\boldsymbol{E}_0}{\sqrt{\displaystyle\frac{\mu\epsilon'}{\mu'\epsilon}}+1}\\
\boldsymbol{E}_0''=\boldsymbol{E}_0\displaystyle\frac{\sqrt{\displaystyle\frac{\mu\epsilon'}{\mu'\epsilon}}-1}{\sqrt{\displaystyle\frac{\mu\epsilon'}{\mu'\epsilon}}+1}\\
\end{aligned}
$$

---
对反射波振幅来说，当入射角取布儒斯特 (Brewster) 角时，反射波电场平行分量为 0，此时无论入射波的偏振方向，反射波偏振都会完全垂直于入射面
$$
i_B=\rm{tan}^{-1}(\displaystyle\frac{n'}{n})
$$
全反射角
$$
i_0=\rm{sin}^{-1}(\displaystyle\frac{n'}{n})
$$
当入射角大于全反射角，折射角的余弦会变为纯虚数
$$
\rm{cos}\ r=i\sqrt{(\displaystyle\frac{\rm{sin}\ i}{\rm{sin}\ i_0})^2-1}
$$
折射波相因子会出现沿 z 方向指数衰减的因子，称为隐失波，在 II 介质内不会传播能流:
$$
e^{i\boldsymbol{k}'\cdot \boldsymbol{x}}=e^{-k'|\rm{cos}\ r|z}e^{ik'(\rm{sin}\ i/\rm{sin}\ i_0)x}
$$

反射系数 $R=\displaystyle\frac{E''^2}{E^2}$
透射系数 $T=\displaystyle\frac{n_2\rm{cos}\ r}{n_1\rm{cos}\ i}\frac{E'^2}{E^2}$

## <font color='red'>$\S 3$  </font>电磁波在导电介质中的传播

假定所有的场都简谐地依赖于时间，那么 Maxwell 方程给出：
$$
\displaystyle\frac{1}{\mu}\nabla\times\boldsymbol{B}=-i\omega(\epsilon_b+i\frac{\sigma}{w})\boldsymbol{E}
$$
导电介质的等效介电常数：
$$
\epsilon(\omega)=\epsilon_b(\omega)+i\frac{\sigma(\omega)}{\omega}
$$
这个复电容率是由存在传导电流导致的, 是形式化定义.
耗散功率密度: $\displaystyle\frac{1}{2}\rm{Re}(\boldsymbol{J}^*\cdot\boldsymbol{E})=\frac{1}{2}\sigma E^2_0$
位移电流与电场有 90° 相差, 在介电常数的实数部分, 不贡献能量损耗.

介质作为良导体的条件: $\displaystyle\frac{\sigma}{\epsilon_b\omega}\gg 1$

---
如果场具有平面波的形式，那色散关系可以写为：
$$
k^2=\mu\epsilon(\omega)\omega^2=\mu\epsilon_b\omega^2(1+\displaystyle i\frac{\sigma}{\omega\epsilon_b})\\
\boldsymbol{k}=i\boldsymbol{\alpha}+\boldsymbol{\beta}\\
\beta^2-\alpha^2=\omega^2\epsilon\mu\\
\boldsymbol{\alpha}\cdot\boldsymbol{\beta}=\mu\sigma\omega/2
$$
电场符合亥姆霍兹方程且散度为 0, 其解的形式为 $ E_0e^{\displaystyle-\alpha\cdot x}e^{\displaystyle i\beta\cdot x}e^{\displaystyle -i\omega t}$. 需要注意的是, 这里的 $\alpha~\beta$ 都是矢量, 在分析问题时要注意不同分量的性质.

此时电磁波的波矢和频率不可能都是实数，下面是两种典型情况：
1. 在某个初始时刻，导体中已经存在真实电磁场，可以按三维空间分解为具有实波矢的平面波叠加，此时频率必须是复数，频率的虚部表示电磁场随时间指数衰减，这是因为存在欧姆电流的损耗
2. 外界有电磁波入射到导体，导体内部的场是受迫振动，其频率由外部电磁波决定，是实数，此时波数是负数，显示出在空间的指数衰减

第二种情况下可以令 $\boldsymbol{k}=i\boldsymbol{\alpha}+\boldsymbol{\beta}$，$2\alpha$ 是吸收系数

对不良导体，$\sigma/\omega\epsilon_b\ll1$，波矢频率关系近似为：
$$
k\approx\sqrt{\mu\epsilon_b}\omega+i\displaystyle\frac{1}{2}\sqrt{\frac{\mu}{\epsilon_b}}\sigma
$$
吸收系数几乎不依赖于频率
对良导体，$\sigma/\omega\epsilon_b\gg1$，波矢频率关系近似为：
$$
k\approx(1+i)\sqrt{\frac{\omega\mu\sigma}{2}}=(1+i)/\delta=\beta+i \alpha
$$
其中$\delta=\sqrt{\displaystyle\frac{2}{\omega\mu\sigma}}$称为趋肤深度，代表了电磁波能够进入导体的一个特征长度，它明显地依赖于频率，频率越高的电磁波越不容易穿透良导体

良导体中电磁场振幅关系：
$$
\boldsymbol{H}_0=\displaystyle\frac{1}{\mu\omega}k\boldsymbol{n}\times\boldsymbol{E}_0
$$
良导体中电磁场一般存在相位差，如果 $\sigma/\omega\epsilon_b\gg1$，$k^2$ 几乎是纯虚数，这时磁场与电场的相位差几乎为 $-\displaystyle\frac{\pi}{4}$.
对于良导体, 磁场值远大于电场, 电磁场的能量几乎全部由磁场携带, 而在真空和绝缘体中, 两者值相等.

利用上一小节的 Fresnel 公式, 如果假设导体的电导率极大, 近似得到电磁波反射率 $R=|\displaystyle\frac{E''}{E}|\approx1-2\sqrt{\frac{2\omega\epsilon}{\sigma}}$


波数为复数时相速度是角频率除以波数的实部.

---
准静态近似下导体中的电磁场
许多情况下传导电流远大于位移电流，忽略位移电流的贡献，磁场可以表示为：
$$
\mu\sigma\displaystyle\frac{\partial \boldsymbol{H}}{\partial t}=\nabla^2\boldsymbol{H}
$$
配合磁场强度和磁感应强度的边值条件，构成一个齐次扩散方程边值问题
对电场、磁感应强度、磁矢势、电流密度都满足这样的扩散方程.

这种方程的特点是对时间是一阶的而对空间是二阶的，因此其空间特征尺度的平方与时间特征尺度成比例，也直接给出了趋肤深度的估计.

准静态下导体内部的涡流耗散的平均功率：
$$
\begin{aligned}
W_{Joule}&=-\displaystyle\oint \langle \boldsymbol{E}\times\boldsymbol{H}\rangle\cdot d\boldsymbol{A}\\
&=\displaystyle\int d^3\boldsymbol{x}\langle \boldsymbol{E}\cdot(\nabla\times\boldsymbol{H})-\boldsymbol{H}\cdot(\nabla\times\boldsymbol{E})\rangle\\
&=\displaystyle\int d^3\boldsymbol{x}\langle \boldsymbol{J}\cdot\boldsymbol{E}\rangle\\
\end{aligned}
$$

## <font color='red'>$\S 4$  </font>介质色散的经典模型

假设介质中的束缚电子可以视作经典阻尼谐振子，有各自的本征频率和阻尼系数，在谐振平面波下做受迫振荡，偏离平衡位置产生平均电偶极矩：
$$
\boldsymbol{p}=\displaystyle\frac{e^2}{m}\frac{\boldsymbol{E}_0}{\omega_0^2-\omega^2-i\omega\gamma}
$$
一个原子中具有某个特定本征频率 $\omega_i$和阻尼系数 $\gamma_i$ 的电子数记为 $f_i$，称为具有频率 $\omega_i$ 的电子的振子强度。这样的体系在谐振电磁场中会产生平均电偶极矩，即介质极化 ,介电常数为：
$$
\displaystyle\frac{\epsilon(\omega)}{\epsilon_0}=1+\frac{Ne^2}{\epsilon_0m}\sum_i \frac{f_i}{\omega_i^2-\omega^2-i\omega\gamma_i}
$$

对导体，介质中部分电子几乎是自由的，其本征频率是 0。如果将其他所以非自由电子的贡献归入 $\epsilon_b$，那么可以写出：
$$
\epsilon(\omega)=\epsilon_b(\omega)+i\frac{Ne^2f_0}{m\omega(\gamma_0-i\omega)}
$$
立即得到德鲁德 (Drude) 公式：
$$
\sigma(\omega)=\frac{Ne^2f_0}{m(\gamma_0-i\omega)}
$$

---
可以看出，这种极化具有二阶极点的行为，可能与反常色散相关联

低频近似下可以忽略分母的虚部，电导基本是实数，固体物理中常记 $\gamma_0=1/\tau$，$\tau$ 称自由电子的弛豫时间

高频极限下，外场频率远远高于所有本征频率，介电常数具有非常简单的形式：
$$
\displaystyle\frac{\epsilon(\omega)}{\epsilon_0}\approx1-\frac{\omega^2_p}{\omega^2}，\  \omega^2_p=\frac{n_0Ze^2}{\epsilon_0m}
$$
这个近似对所有介质在极高频下都成立，$\omega_p$ 称为等离子体频率

假设电子速度远小于光速, 则忽略磁场对电子的影响, 只考虑电场力, 由运动方程解出电子速度, 然后得到电流密度, 进而电导率 $\sigma(\omega)=\displaystyle\frac{in_0e^2}{m\omega}$, 表明电流密度落后电场强度 $\pi/2$ 相位差. 进而 $\epsilon'=\epsilon_0-n_0e^2/m\omega$, $\displaystyle k=\omega\sqrt{\mu_0\epsilon'}=\frac{\omega}{c}\sqrt{1-\frac{\omega^2_p}{\omega^2}}$

如果介质完全极化（例如理想等离子体），并且忽略电子阻尼，那么这个近似公式实际上对任意频率成立，而不是仅对甚高频电磁波。此时，如果入射频率小于介质等离子体频率，那么波矢 k 为纯虚数，电磁波将不能进入介质

对一般频率而言，通常非导电介质的电子阻尼比较小，介电常数基本为实数。
复数的介电常数意味着耗散，只要频率不接近振子频率，电磁波吸收就很小，介质对电磁波透明性好。在振子频率附近，介电常数的虚部明显增强，这些频率区间称为共振吸收区

## <font color='red'>$\S 5$  </font>电磁信号在色散介质中的传播

一维波包的频谱叠加形式：
$$
u(x,t)=\displaystyle\frac{1}{\sqrt{2\pi}}\int^\infty _{-\infty}A(k)e^{ikx-i\omega(k) t}dk
$$
A 就表征了波包中不同频率单色波的成分 (频域)
$$
A(k)=\displaystyle\frac{1}{\sqrt{2\pi}}\int^\infty _{-\infty}u(x,0)e^{-ikx}dx
$$
如果t=0时刻是单色平面波，则傅里叶振幅 $A(k)=\sqrt{2\pi}\delta(k-k_0)$，则该波在之后仍是单色平面波

傅里叶变换的基本性质保证了 u(x,0) 在实空间的延展 $\Delta x$ 以及 A(k) 在 k 空间的延展 $\Delta k$ 满足：$\Delta x\Delta k\geq1/2$ （特别的，如果波函数在两个空间里是高斯型波包，那么二者成反比，且乘积恰好为 1/2）

---
如果波包的谱仅有比较小的延展，也就是假定其仅在 $k=k_0$ 周围的小邻域内有显著值，同时假设 $\omega(k)$ 是缓变的，那么可以展开为：
$$
\omega(k)\approx\omega_0+\displaystyle\frac{d\omega}{dk}|_{k=k_0}(k-k_0)
$$
将这个近似带入 A(K) 的表达式：
$$
u(x,t)\approx u(x-v_g t)e^{i(k_0v_g-\omega_0)t}
$$
在这种色散近似下，波包的形状并没有改变，而是以一定的速度移动了一段距离，这个速度就是群速度，正常情况下波包移动的速度，信息或能量传递的速度：
$$
v_g=\displaystyle\frac{d\omega}{dk}|_{k=k_0}
$$
只要存在色散，群速度就不等于相速度
$$
v_g=\displaystyle\frac{c}{n(\omega)+\omega(dn/d\omega)}=\frac{v_p}{1+\omega(dn/d\omega)/n}
$$
正常色散的情况，$dn/d\omega>0$，$v_g<v_p<c$
如果频率接近本征频率，折射率$n=\sqrt{\epsilon(\omega)}$会剧烈变化，往往伴随着反常色散，$dn/d\omega<0$，这时群速度可能超过相速度、超过光速、或是为负值

---
仅利用因果性，也能得到最一般情形下介电常数定性行为的不少推论

假设电位移与电场有以下的普遍线性关系：
电场与极化率表示成卷积的形式，在利用傅里叶变换得到（2）式时，卷积的变换为变换的乘积
$$
\begin{gather}
\boldsymbol{D}(\boldsymbol{x},t)=\epsilon _0[\boldsymbol{E}(\boldsymbol{x},t)+\displaystyle \int^\infty _{0}\chi(\tau)\boldsymbol{E}(\boldsymbol{x},t-\tau)d\tau]\\
\chi(\tau)=\displaystyle\frac{1}{2\pi}\int^\infty _{0}[\frac{\epsilon(\omega)}{\epsilon _0}-1]e^{-i\omega \tau}d\omega\\
\end{gather}
$$
因果性表现在积分从0开始，而不是负无穷，表示当前的状态不可能被未来所影响

再利用以下的几个假定：
1. $\chi(\tau)$对任意$\tau$有限，那么$\epsilon(\omega)$在复平面上半解析
2. 对非导体，$\chi(\tau \rightarrow\infty)\rightarrow0$，即无穷久远的电场对当前的极化没有影响，这样$\epsilon(\omega)$在实轴上也解析。对导体，$\displaystyle\lim_{\tau\to \infty}\chi(\tau)=\sigma/\epsilon_0$，这使得$\epsilon(\omega)$在原点存在一个极点，但其他区域的解析性保持
3. 大$\omega$处可以利用分部积分展开$\displaystyle\frac{\epsilon(\omega)}{\epsilon _0}=1-\frac{\chi'(0)}{\omega^2}+\cdots$
4. $\chi(\tau)$是实数，所以$\epsilon(-\omega)=\epsilon^*(\omega^*)$

得到上半平面介电常数的柯西公式，围道是实轴和上无穷大半圆：
$$
\epsilon(z)/\epsilon _0=1+\displaystyle\frac{1}{2\pi i}\oint _C\frac{(\epsilon(\omega')/\epsilon _0-1)}{\omega'-z}d\omega'
$$
半圆上积分贡献为0，写为实轴上的积分，用主值积分表示为：
$$
\begin{gather}
\displaystyle\frac{1}{\omega'-\omega-i\delta}=\mathscr{P}(\frac{1}{\omega'-\omega})+\pi i\delta(\omega'-\omega)\\
\epsilon(\omega)/\epsilon _0=1+\displaystyle\frac{1}{\pi i}\mathscr{P}\int^\infty _{-\infty}\frac{(\epsilon(\omega')/\epsilon _0-1)}{\omega'-\omega}d\omega'\\
\end{gather}
$$
可以写出复介电常数频谱的实部和虚部，也就是克拉默斯-克勒尼希关系，或者色散关系：
$$
\begin{gather}
Re[\epsilon(\omega)/\epsilon _0]=1+\displaystyle\frac{1}{\pi}\mathscr{P}\int^\infty _{-\infty}\frac{Im[\epsilon(\omega')/\epsilon _0]}{\omega'-\omega}d\omega'\\
Im[\epsilon(\omega)/\epsilon _0]=-\displaystyle\frac{1}{\pi}\mathscr{P}\int^\infty _{-\infty}\frac{Re[\epsilon(\omega')/\epsilon _0-1]}{\omega'-\omega}d\omega'\\
\end{gather}
$$

## <font color='red'>$\S 6$  </font>波导与谐振腔
###场的分离

如果不考虑边界条件，波导管内的电磁场满足的方程与无限介质中的情况相同，都是无源麦克斯韦方程组，如果假设场具有 $e^{-i\omega t}$ 的时间因子，那么电磁场满足三维亥姆霍兹方程：
$$
(\nabla^2+\mu\epsilon\omega^2)\begin{pmatrix}E\\ B\end{pmatrix} =0
$$
有了亥姆霍兹方程, 电场散度为 0 条件和边值条件, 就能解出电磁场量, 即可能存在的波模.

根据问题的对称性，可以将电磁场分为纵向分量和垂直分量：
$$
\boldsymbol{E}=E_z\boldsymbol{e_3}+\boldsymbol{E_\bot}=E_z\boldsymbol{e_3}+(\boldsymbol{e_3}\times\boldsymbol{E})\times\boldsymbol{e_3}
$$
从而四个麦克斯韦矢量方程可以用电磁场横纵向分量表示为：
(展开 E 和 B 的梯度和散度，左侧点乘或叉乘 e3)
$$
\displaystyle\frac{\partial \boldsymbol{E}_\bot}{\partial z}+i\omega\boldsymbol{e}_3\times\boldsymbol{B}_\bot=\nabla _\bot E_z\\
\boldsymbol{e}_3\cdot (\nabla _\bot\times\boldsymbol{E}_\bot)=i\omega\boldsymbol{B}_z\\
\displaystyle\frac{\partial \boldsymbol{B}_\bot}{\partial z}-i\mu\epsilon\omega\boldsymbol{e}_3\times\boldsymbol{E}_\bot=\nabla _\bot B_z\\
\boldsymbol{e}_3\cdot (\nabla _\bot\times\boldsymbol{B}_\bot)=-i\mu\epsilon\omega\boldsymbol{E}_z\\
\nabla _\bot\cdot\boldsymbol{E}_\bot=-\displaystyle\frac{\partial E_z}{\partial z}\\
\nabla _\bot\cdot\boldsymbol{B}_\bot=-\displaystyle\frac{\partial B_z}{\partial z}\\
$$
这表明其实只需要知道两个纵向场分量就可以完全确定场

由于问题具有纵向平移对称性，可以将场对z坐标的依赖分离
$$
\begin{pmatrix}\boldsymbol{E}\\ \boldsymbol{B}\end{pmatrix}=\begin{pmatrix}\boldsymbol{E}(x,y)\\ \boldsymbol{B}(x,y)\end{pmatrix}e^{\pm ikz-i\omega t}
$$
这样可以明确写出纵向场量表达的公式：
利用$\displaystyle\frac{\partial B_\bot}{\partial z}=ikB_\bot$
$$
\boldsymbol{E}_\bot=\displaystyle\frac{i}{k_\bot^2}[k\nabla_\bot E_z-\omega\boldsymbol{e}_3\times\nabla _\bot B _z]\\
\boldsymbol{B}_\bot=\displaystyle\frac{i}{k_\bot^2}[k\nabla_\bot B_z+\mu\epsilon\omega\boldsymbol{e}_3\times\nabla _\bot E_z]\\
$$\
这里就能看出, 单连通波导管不能传播横电磁模式, 如果纵向电磁场均为零, 则横向也均为零, 即不存在电磁场.

这样得到二维亥姆霍兹方程：
$$
(\nabla^2_\bot+k_\bot^2)\begin{pmatrix}\boldsymbol{E}(x,y)\\ \boldsymbol{B}(x,y)\end{pmatrix} =0\\
\mu\epsilon\omega^2=k^2+k_\bot^2
$$
波导管波数是待定参数，可以由波导管边值条件确定. 电场磁场解出一个即可, 另一个可根据法拉第方程得到.

注意此时的 $\boldsymbol{E}$ 仍然是矢量, 分解为三个分量方程, 每个分量方程分解出两个因子.

---
###边值问题的建立
假设波导管外壁是理想导体，则应当有边值条件：
$$
\boldsymbol{n}\times\boldsymbol{E}=\boldsymbol{n}\cdot\boldsymbol{B}=0\\
\downarrow\\
E_\bot|_S=\frac{\partial B_\parallel}{\partial n}|_S=0
$$
这样确定了二维边值问题：
$$
(\nabla^2_\bot+k_\bot^2)\psi=0\\
k_\bot^2=\mu\epsilon\omega^2-k^2\\
\psi_\bot|_S=0,\frac{\partial \psi_\parallel}{\partial n}|_S=0
$$
这样可以看出，金属波导中横电和横磁模式是完全分离的
$$
\psi\equiv E_z,\ B_z=0,\ \boldsymbol{E_\bot}=\pm \displaystyle\frac{ik}{k_\bot^2}\nabla _\bot \psi,\ TM\\
\ \\
\psi\equiv H_z,\ E_z=0,\ \boldsymbol{H_\bot}=\pm \displaystyle\frac{ik}{k_\bot^2}\nabla _\bot \psi,\ TE\\
$$
并且无论对什么模式总有电磁场关系：
$$
\boldsymbol{H_\bot}=\pm\frac{1}{Z}\boldsymbol{e}_3\times\boldsymbol{E}_\bot\\
或\\
\boldsymbol{E_\bot}=\pm Z\boldsymbol{H}_\bot\times\boldsymbol{e}_3\\
Z=\begin{cases}
\displaystyle\frac{k}{\epsilon\omega}=\frac{k}{k_0}\sqrt{\frac{\mu}{\epsilon}},\ TM \\
\displaystyle\frac{\mu\omega}{k}=\frac{k_0}{k}\sqrt{\frac{\mu}{\epsilon}},\ TE \\
\end{cases}
$$
Z 是波导中的波阻抗

---
二维边值问题的解是唯一的，并且相应的本征值 $k_\bot$ 一般是分立的正实数，那么波导中可以传播的电磁波的波数 $k$ 也是分立的
但是明显的，存在一个截止频率 $\omega_\gamma=\displaystyle\frac{k_\bot}{\mu\epsilon}$，如果电磁波频率小于这个频率，波数将是纯虚数，从而不能在波导管传播
由于本征值一般总是存在一个最小值，所以也有最小截止频率

横电磁模式下纵向的场分量恒为零，其行为完全类似于一个二维的静电场，而且它的波数-频率关系与无边界空间中平面电磁波完全相同，所以其横向波矢 $k_\bot=0$，其相速度等于该介质中的光速，而对一般的TE或TM模式，其相速度总大于介质光速

根据拉普拉斯方程的性质，如果场在单连通区域的边界上是0，那在该区域内必须恒为零，所以横电磁模式不能在单连通的波导管内传播（复连通的是可以的）

---
###金属波导的能量传输和损耗

如果金属不是理想导体，电磁场会进入金属表面约趋肤深度厚度的薄层，诱导金属中的欧姆损耗

根据坡印廷矢量可以计算出两种模式的能流密度：
$$
\boldsymbol{S}=\displaystyle\frac{\omega k}{k_\bot^4}\begin{cases}
\epsilon[\boldsymbol{e}_3\nabla _\bot|\psi|^2+i\displaystyle\frac{k_\bot^2}{k}\psi \nabla _\bot\psi^\ast],\ TM \\
\mu[\boldsymbol{e}_3\nabla _\bot|\psi|^2-i\displaystyle\frac{k_\bot^2}{k}\psi^\ast \nabla _\bot\psi],\ TE \\
\end{cases}
$$
注意波导中一个周期的平均能流密度由上式的实部给出，不考虑损耗，那么边值问题的解 $\psi$ 是实的，此时只有第一项有贡献

波导管传输的功率：
$$
P=\displaystyle\int _A \boldsymbol{S}\cdot d\boldsymbol{\sigma}
$$
利用二维格林第二公式：
$$
\displaystyle\iint _\Sigma(f\nabla g-g\nabla f)\cdot d\sigma=\oint _{\partial \Sigma}(f\frac{\partial g}{\partial n}-g\frac{\partial f}{\partial n})dl
$$
功率可以化为边界上的线积分 $\psi\partial\psi^\ast/\partial n$ 和 $\psi^\ast\nabla _\bot^2\psi$ 的面积分，第一项是 0，第二项再利用最初的拉普拉斯方程，得到：
$$
P=\displaystyle\frac{1}{2\sqrt{\mu\epsilon}}(\frac{\omega}{\omega_\lambda})^2\sqrt{1-(\frac{\omega_\lambda}{\omega})^2}\dbinom{\epsilon}{\mu}\int _A |\psi|^2 d\sigma
$$

此外还有关系 $P=Uv_g$，U 是电磁场能量密度，$v_g$ 是群速度

---
对有损耗的情况，可以假设对某个特定的模式 $\lambda$，其垂直波数：
$$
k_\bot=k_\bot^{(0)}+a_\lambda+ib_\lambda\\
(k^2=\mu\epsilon_b\omega^2(1+\displaystyle i\frac{\sigma}{\omega\epsilon_b}))
$$
波导管纵向传播的功率将会因能量损耗而指数衰减
$$
P(z)=P_0e^{-2b_\lambda z}\\
-\displaystyle\frac{dP}{dz}=\frac{1}{2\sigma\delta}\oint _C|\boldsymbol{n}\times\boldsymbol{H}|^2dl
$$

---
###介质波导

程函近似，又称准经典近似或温策尔-克拉默斯-布里渊近似，忽略光的波动性，在远大于波长特征尺度的线度上将系统作为几何光学处理

介质波导中纵向的电磁场一般是耦合的，无法分离，除非是平面介质波导

光纤的截面通常是由折射率不同的两层介质构成的同心圆，内层材料折射率略高于外侧

解场方程并根据边界条件可以确定不同电磁模式的截止频率
$$
\begin{cases}
(\nabla _\bot^2+\gamma^2)\psi=0,\ \rho<a\\
(\nabla _\bot^2-\beta^2)\psi=0,\ \rho<a
\end{cases}
$$
解的具体形式为$R(\rho)e^{ikz}e^{im\phi}$，径向函数R满足：
$$
\begin{cases}
(\displaystyle\frac{1}{\rho}\frac{d}{d\rho}(\rho\frac{d}{d\rho})-\frac{m^2}{\rho^2}+\gamma^2)R(\rho)=0,\ \rho<a\\
~\\
(\displaystyle\frac{1}{\rho}\frac{d}{d\rho}(\rho\frac{d}{d\rho})-\frac{m^2}{\rho^2}-\beta^2)R(\rho)=0,\ \rho>a\\
\end{cases}
$$
在柱坐标系中，恰当的解可以写为：
$$
\dbinom{E_z}{H_z}=\begin{cases}
\dbinom{A_e}{A_h}J_m(\gamma\rho)e^{ikz}e^{im\phi},\ \rho<a\\
~\\
\dbinom{B_e}{B_h}K_m(\beta\rho)e^{ikz}e^{im\phi},\ \rho>a\\
\end{cases}
$$
内部选择了贝塞尔函数，而外部选择了虚宗量贝塞尔函数，这样保证内部的值有界而外部的值随半径指数衰减.


