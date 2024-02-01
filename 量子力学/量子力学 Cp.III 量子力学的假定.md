# Cp.III 量子力学的假定
## <font color='red'>$\S 1$  </font>基本假设

1. 在一个确定的时刻 $t_0$，一个物理体系的态由态空间 $\mathscr{E}$ 中一个特定的右矢 $|\psi(t_0)\rangle$ 确定，给出这样一个右矢 $|\psi\rangle$ 等价于给出一个波函数 $\psi(r)=\langle \pmb{r}|\psi\rangle$

---

2. 每个可测量的物理量 $\mathscr{A}$ 都可以用在 $\mathscr{E}$ 空间的一个观察算符 A 来描述

在量子力学中，物理系统的状态称为量子态，可观测量用自伴算子表示。

---

3. 每次测量物理量 $\mathscr{A}$ 可能得到的结果只能是对应观察算符 A 的一个本征值，由于算符是厄米的，本征值必为实数，这也是符合客观事实的

在数学里，作用于一个有限维的内积空间，一个自伴算子 (self-adjoint operator) 等于自己的伴随算子；等价地说，表达自伴算子的矩阵是埃尔米特矩阵。埃尔米特矩阵等于自己的共轭转置。根据有限维的谱定理，必定存在着一个正交归一基，可以表达自伴算子为一个实值的对角矩阵。

---

4. 对非简并离散谱，若体系处于已归一化的态$|\psi\rangle$中，则测得$\mathscr{A}$的结果为A一个非简并本征值$a_n$的概率：$\mathscr{P}(a_n)=|\langle  u_n|\psi\rangle|^2$，$u_n$是A归一化的属于$a_n$本征矢

简并的情况：$\mathscr{P}(a_n)=\displaystyle\sum^{g_n}_{i=1}|\langle  u_n^i|\psi\rangle|^2$
本质是本征子空间的投影：
$$
\begin{aligned}
|\psi_n\rangle&=\displaystyle\sum^{g_n}_{i=1}|u^i_n\rangle\langle  u_n^i|\psi\rangle\\
&=P_n|\psi\rangle\\
&=\sum^{g_n}_{i=1}c^i_n|u^i_n\rangle\\
\end{aligned}
$$


连续谱：$d\mathscr{P}(\alpha)=|\langle  u_\alpha|\psi\rangle|^2d\alpha$，微分就是态密度
连续基的分解：$\displaystyle|\psi\rangle=\int d\alpha c(\alpha)|v_\alpha\rangle$

如果归一化不能满足，只需要另外除以$\langle  \psi|\psi\rangle$即可



两个右矢相差一个纯相位因子 $\alpha e^{i\theta}$（$\theta$是实数），仍表示同一物理状态，展开式中的相对相位才会产生实际影响

---

5. 对处于 $|\psi\rangle$ 态的体系测量得到结果 $a_n$，则测量后体系的态是原态在本征子空间上的归一化投影 $\displaystyle\frac{P_n|\psi\rangle}{\sqrt{\langle \psi |P_n|\psi\rangle}}$ ，测量后波包收缩到本征子空间

需要注意的是，测量后所得到的本征矢不是子空间$\mathscr{E_n}$的任意右矢，而是$|\psi\rangle$的属于$\mathscr{E_n}$的那一部分

---
6. 态矢量的演变遵从薛定谔方程：
$$
i\hbar\frac{d}{dt}|\psi(t)\rangle=H(t)|\psi(t)\rangle
$$

---

7. 粒子的任何一个物理量都可以表示为基本力学量$\pmb{r}$和$\pmb{p}$的函数$A(t)=\mathscr{A}(\pmb{R},\pmb{P},t)$

对非厄米算符的对称化操作：$\pmb{r}\cdot \pmb{p}\xrightarrow{}\frac{1}{2}(\pmb{R}\cdot\pmb{P}+\pmb{P}\cdot\pmb{R})$

要得到经典定义量对应的量子算符，只需要直接替换即可

## <font color='red'>$\S 2$  </font>可观察量与测量的物理诠释

在$|\psi\rangle$态中可观察量的平均值由$\langle A\rangle_\psi=\langle  \psi|A|\psi\rangle$给出
为了实际计算出均值，要先选定一个表象，例如
$$
\begin{aligned}
\langle x\rangle_\psi&=\langle  \psi|X|\psi\rangle\\
&=\displaystyle \int d^3r\langle\psi|\pmb{r}\rangle\langle  \pmb{r}|X|\psi\rangle\\
&=\displaystyle \int d^3r \psi(\pmb{r})^\ast x\psi(\pmb{r})
\end{aligned}
$$
还可以取动量表象，但是注意算符在不同表象的表示不同

---
可以同时完全确定的可观察量称为相容的，或对易的。测量这些量的顺序不影响测量结果，互相之间不会因为其他量的测量而丢失信息，反而会获得更多信息、
如果想由测量结果唯一获知此时的态，所测量的量必须是可对易观察量完全集(ECOC)

如果两个量不对易，第二次测量后态由第一个算符的本征态变为第二个算符的本征态，此时再测量第一个量，结果会是不确定的，表明第一次测量的信息完全被丢失

至少存在一个共同本征态$|a_n,b_p,i\rangle$，在这个态中测量A B一定是分别得到$a_n$和$b_p$
特别的，当A B不对易时，也可能存在右矢同时是A B的本征矢，但是这些右矢的数量不足以构成一个基

## <font color='red'>$\S 3$  </font>薛定谔方程的物理意义

###概率流

由哈密顿算符的厄米性，态矢量的模方与时间无关
展开 $\displaystyle\frac{d}{dt}\langle\psi(t)|\psi(t)\rangle$，带入薛定谔方程并利用 $H^{\dag}=H$

由于模方守恒，如果经过恰当的归一化，波函数模方可以作为一个测度分布，解释为粒子出现的概率密度

类比经典流体，可以给出概率的局域守恒方程：
$$
\displaystyle\frac{\partial }{\partial t}\rho(\pmb{r},t)+\bigtriangledown\pmb{J}(\pmb{r},t)=0
$$
用归一化波函数标示的概率流：
$$
\begin{aligned}
\pmb{J}(\pmb{r},t)&=\displaystyle\frac{\hbar}{2mi}[\psi^\ast\bigtriangledown\psi-\psi\bigtriangledown\psi^\ast]\\
&=\displaystyle\frac{1}{m}Re[\psi^\ast(\displaystyle\frac{\hbar}{i}\bigtriangledown\psi)]\\
(&=\displaystyle\frac{1}{m}Re[\psi^\ast[\displaystyle\frac{\hbar}{i}\bigtriangledown-q\pmb{A}]\psi])\\
\end{aligned}
$$
$\pmb{J}(\pmb{r},t)$还可以视作量子算符$\pmb{K}(\pmb{r})=\displaystyle\frac{1}{2m}[|\pmb{r}\rangle\langle\pmb{r}|\pmb{P}+\pmb{P}|\pmb{r}\rangle\langle\pmb{r}|]$，由概率密度和粒子速度之积经过对称化得到

---
海森堡绘景下平均值的演化
$$
\displaystyle\frac{d}{dt}\langle A\rangle=\displaystyle\frac{1}{i\hbar}\langle [A,H(t)]\rangle+\langle \displaystyle\frac{\partial A}{\partial t}\rangle
$$

薛定谔绘景中r与p对时间的依赖性转移到态矢量中，而不是在算符R和P中
当算符不依赖于时间，算符平均值的时间导数就是算符与哈密顿算符对易子时间平均值除以$i\hbar$

艾伦费斯特定理：
$$
\begin{aligned}
\displaystyle\frac{d}{dt}\langle R\rangle&=\displaystyle\frac{1}{m}\langle P\rangle\\
\displaystyle\frac{d}{dt}\langle P\rangle&=-\langle \nabla V(R)\rangle\\
\end{aligned}
$$
经典情况下退化为哈密顿-雅各比方程或牛顿方程

粒子坐标平均值$\langle R(t)\rangle$称为波包中心，粒子的态由波包整体描述
一般来说，$\langle \bigtriangledown V(R)\rangle\neq[\bigtriangledown V(\pmb{r})]_{r=\langle R\rangle}$，函数平均值不等于自变量取平均值时的函数值
若波包足够狭窄，其波函数值有显著值的区间线度小于势场有明显变化的距离，则可以认为二者相等，作为经典近似
极限情况是波函数是$\delta$函数

---
###保守体系的演化
如果一个体系的哈密顿函数不明显依赖于时间，则是保守的
保守体系态的演化：
1. 在 $\hat{H}$ 本征态基中展开 $|\psi(t_0)\rangle$
$$
|\psi(t_0)\rangle=\displaystyle \sum_n \sum_\tau c_{n,\tau}(t_0)|\phi_{n,\tau}\rangle\\
c_{n,\tau}(t_0)=\langle\phi_{n,\tau}|\psi(t_0)\rangle
$$
2. 乘时间演化因子：
$$
|\psi(t)\rangle=\displaystyle \sum_n \sum_\tau c_{n,\tau}(t_0)e^{-iE_n(t-t_0)/\hbar}|\phi_{n,\tau}\rangle
$$
对连续谱同理：
$$
|\psi(t)\rangle=\displaystyle \sum_n \int dE~c_{\tau}(E,t_0)e^{-iE(t-t_0)/\hbar}|\phi_{E,\tau}\rangle
$$

可见，演化后的态只相差一个相位因子，表明 $\hat{H}$ 的本征态体系的一切物理性质都不随时间改变，称为定态.


时间演化因子的选择来自于海森堡图像中时间演化算符的讨论.

随时间的演变只发生在态由多个本征右矢线性组合的情况下，这时会产生相对相位，便对实际物理效应产生影响，概率密度的变化来自于干涉项.

运动常量就是不明显依赖于时间，而且与 $\hat{H}$ 对易的可观察量
运动常量的平均值不随时间改变，其本征态是定态，而且其中的态都保持为固定本征值的本征态，这些本征值称为好量子数
任意态中测量运动常量得到某一个本征值的概率不随时间改变

## <font color='red'>$\S 4$  </font>叠加原理

态的叠加不是概率的加权和，也不是混合的态，而是波函数 (概率幅) 的线性加和，其概率是这个和的模方
展开叠加后的概率能得到干涉项，干涉项表明了 $\lambda_1 \lambda_2$ 相对相位的重要性：
$$
2Re\{\lambda_1 \lambda_2^\ast \langle u_n|\psi_1\rangle \langle u_n|\psi_2\rangle^\ast \}
$$
对应于同一末态的诸概率幅相加，对应于正交末态的诸概率相加
对于同一末态，体系实际上同时经过了所有可能的中间路径

## <font color='red'>$\S B$  </font>两个共轭可观察量的方均根偏差

如果两可观察量P、Q的对易子$[P,Q]$等于$i\hbar$，称其为共轭可观察量，无论体系态矢量如何，总有方均根偏差满足：
$$
\Delta P\cdot\Delta Q\geqslant\displaystyle\frac{\hbar}{2}
$$
推广到任意两个可观察量，这个结果就是一般的不确定性关系：
$$
\Delta A\cdot\Delta B\geqslant\displaystyle\frac{1}{2}|\langle[A,B]\rangle|
$$

对系统的某一个态，如果方均根之积恰好等于$\hbar/2$，则与这个态相联系的在$|q\rangle$表象中的波函数是一个高斯型波包（在$|p\rangle$表象中同样如此），具体形式是（$|q\rangle$表象）：
$$
\psi(q)=Ce^{\displaystyle i\langle P\rangle q/\hbar}\cdot e^{-[\displaystyle\frac{q-\langle Q\rangle}{2\Delta Q}]^2}\\
~\\
归一化系数：C=[2\pi (\Delta Q)^2]^{-1/4}
$$
因此傅里叶变换在实空间和在波数（频率）空间中的延展之积为 1/2

p 在 $|q\rangle$ 表象中的作用相当于 $\displaystyle\frac{\hbar}{i}\frac{d}{dq}$

---
###测量引起的扰动
对具有连续谱的可观察量的测量不可能是完全精确的，如果完全精确，测量后测量结果$x_0$的本征态用$\delta(x-x_0)$表示，但是这个本征态是不可能归一化的，对应的概率必然发散
所以$\delta $函数不能表示物理上可以实现的态
所以引入$\delta^{\epsilon}(x-x_0)$函数，表示仅在中心点周围直径$\epsilon$的区域内的函数值为$1/\epsilon$，其余为0

对于无限深势阱的粒子,利用这个函数来计算粒子处于本征态$E_n$的概率
$$
\begin{align} 
\varphi _n(x)&=\sqrt{\displaystyle\frac{2}{a}}sin(\frac{n\pi x}{a})\\
\mathscr{P}_n(E_n)&=|\displaystyle\int \varphi^\ast _n(x)\sqrt{\epsilon}\delta^{(\epsilon)}(x-a/2) dx|^2\\
&=\begin{cases}
\displaystyle\frac{8a}{\epsilon}(\frac{1}{n\pi})^2sin^2(\frac{n\pi\epsilon}{2a}),&n为奇数\\
0,&n为偶数 \\
\end{cases}
\end{align}
$$
这个概率分布说明,无论$\epsilon$多小,分布总是与之有关,而且$\epsilon$越小,分布曲线便向着n值越大的方向延伸.
这其实就是海森堡不确定关系所揭示的,对粒子位置测量的越准确,其动量受到的影响就越大,在测量时传递给粒子的能量越大.


## <font color='red'>$\S H$  </font>规范不变性

规范变换不会影响物理结果，规范变换涉及的标势和矢势都是运算工具

哈密顿表述形式中，正则动量会受到规范变换的影响：
$$
\pmb{p}'(t)=\pmb{p}(t)+q\nabla\chi[\pmb{r}(t),t]
$$

体系的真实物理量在任意时刻都不依赖于用以描述电磁场的规范,而非物理量在规范变换时会产生修正.

## <font color='red'>$\S M$  </font>任意形状势阱中粒子的束缚态

