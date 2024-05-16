# Cp. V 等离子体波

任何周期性的扰动或波动, 总能分解为单一频率谐振波的叠加, 所以只需研究最简单的问题

非单色的波以某一频率为中心, 按振幅叠加构成波群, 合成波的包络线为波包. 波包的场只局限在小范围内, 波包实际上是一种振幅调制的波. 

相速度与群速度的关系:
$$
v_g=\frac{d}{dk}(v_pk)=v_p+k\frac{dv_p}{dk}\\
或\\
v_g=v_p-\lambda\frac{dv_p}{d\lambda}
$$

色散关系:
$$
\begin{cases}
    dv_p/d\lambda>0, v_g<v_p, 正常色散\\
    dv_p/d\lambda<0, v_g>v_p, 反常色散\\
    dv_p/d\lambda=0, v_g=v_p, 无色散\\
\end{cases}
$$

圆偏振波:右(左)
$$
E_x/E_y=\pm i\\
或\\
\boldsymbol{E}=\boldsymbol{E}_0(\boldsymbol{e_x}\pm i\boldsymbol{e_y})\\
$$

##<font color='red'>$\S 1$ </font>电子静电震荡与静电波

电子偏离平衡位置破坏电中性, 产生的静电场作为恢复力, 形成电子静电振荡. 
电子静电振荡是一种高频振荡. 
离子质量远大于电子, 所以对此几乎不响应, 可以视作均匀正电荷背景, 将电子作为单独流体研究. 
###电子静电振荡

假定等离子体温度极低 $(T_e\approx0)$ , 是冷等离子体, 忽略电子热运动, 即热压力 $\nabla p_e\approx0$. 再忽略电子离子的碰撞效应, 即 $R_{ei}$. 
这样写出电子流体的力学方程:
$$
\begin{cases}
    \displaystyle\frac{\partial n_e}{\partial t}+\nabla\cdot(n_e\boldsymbol{u}_e)=0\\
    m_en_e[\displaystyle\frac{\partial u_e}{\partial t}+(\boldsymbol{u}_e\cdot\nabla)\boldsymbol{u}_e]=-en_e\boldsymbol{E}
\end{cases}
$$
包括守恒性方程和动力学方程

电场由运动产生的电荷分离引起:
$$
\nabla\cdot \boldsymbol{E}=-e(n_e-n_0)/\epsilon_0
$$

只讨论小幅振荡, 将振荡量展开到一阶, 比如 $n_e=n_0+n_{e1}$
代入得线性化方程组:
$$
\begin{cases}
    \displaystyle\frac{\partial n_{e1}}{\partial t}+n_0\nabla\cdot\boldsymbol{u}_{e1}=0\\
    m_e\displaystyle\frac{\partial \boldsymbol{u_{e1}}}{\partial t}=-e\boldsymbol{E}_1\\
    \nabla\cdot \boldsymbol{E}_1=-en_{e1}/\epsilon_0
\end{cases}
$$
设扰动发生在z方向, 取平面波解:
$$
\frac{\partial }{\partial t}\rightarrow-i\omega, \nabla\rightarrow i\boldsymbol{k}
$$
三个未知量 $n_{e1}, u_{e1}, E$ 任意消去两个, 得到非零解条件, 也就是色散关系:
$$
\omega=\omega_{pe}=\displaystyle\sqrt{\frac{n_0e^2}{m_e\epsilon_0}}
$$
$\omega$与k无关, 说明群速度为0, 表明这种振荡不能传播, 是局域的. 该振荡频率也称为等离子体特征频率. 

---
###电子波
如果考虑电子热运动, 动力学方程右端变为:
$$
-en_e(E+u_e\times B)-\nabla p_e
$$
两个方程与麦克斯韦方程组联立,  同样的保留扰动量到一阶得线性化方程组

$\nabla p_e$ 由状态方程决定. 如果波长比一个周期内电子所走的距离大得多(长波近似), 也就是波的相速度比电子平均热运动速度大得多, 则可以认为过程是绝热的:
$$
p_en_e^{-\gamma}=Const
$$
微分得:
$$\nabla p_e=\gamma p_en_e^{-1}\nabla n_e=\gamma T_e\nabla n_e$$
利用$\gamma=(f+2)/f$, 一维绝热过程$f=1$
电子特征热速度$v_{te}=\sqrt{T_e/m_e}$:
$$
\nabla p_e=3m_ev_{te}^2\nabla n_{e1}
$$
###电子静电波
这样方程组(2+4)有三个封闭的方程与B无关, 表明存在$B=0$的纯静电解

同样的, 对上述三个方程任意消去两个变量, 得到色散关系:
$$
\omega^2=\omega^2_{pe}+3v_{te}^2k^2
$$
电子静电波是纯静电纵波, 通过热压强提供恢复力. 电子密度, 电场和电子运动速度都以纵波形式传播. 
不难发现, 这种波存在截止频率$\omega_{pe}$. 
$$
k\rightarrow\infty时\\
v_p=v_g=\sqrt{3}v_{te}
$$
###电子横电磁波
从方程组消去$B_1, u_{e1}, n_{e1}$, 得到$E_1, \boldsymbol{k}$的方程
分两种情况:
$$
\begin{cases}
    \boldsymbol{E_1}\parallel\boldsymbol{k}, 色散关系表明这就是纯电子静电纵波\\
    \boldsymbol{E_1}\bot\boldsymbol{k}, 色散关系为\omega^2=\omega^2_{pe}+c^2k^2, 是横电磁波\\
    与无外磁场下等离子体中传播的电磁波色散关系相同
\end{cases}
$$
无外磁场时, 静电振荡和横电磁振荡不耦合. 有外磁场时, 运动方程增加一项洛伦兹力, 两种振荡是耦合的. 

---
讨论低频情况, 振荡频率低于离子等离子体频率. 
这时离子运动是主要的, 电子紧密跟随离子运动

写出双流体力学方程组, 做线性化(只保留一阶)
###离子声波
低频长波, 波长远大于电子德拜屏蔽距离. 离子受扰动时, 电子相应足够快, 可以视作准电中性$n_{n1}=n_{e1}$
同时忽略电子的惯性和运动, 电子守恒性方程忽略, 电子运动方程的惯性项忽略

解出色散关系;
$$
\omega=v_sk\\
离子声速\ v_s=\displaystyle\sqrt{\frac{\gamma_iT_i+\gamma_eT_e}{m_i}}
$$
离子声速的表达式与中性气体声速$c_s=\sqrt{\gamma p_0/\rho_0}=\sqrt{\gamma T/m}$的结构相似. 
离子声波由热压强和静电力驱动. 

当 $T_i\approx T_e$ 时, 离子声速和粒子特征热速度接近, 波与离子运动发生强烈相互作用, 声波受到强阻尼, 会很快衰减, 将能量释放给粒子
###离子静电波
低频短波, 存在电荷分离
$$
n_{e1}=\displaystyle\frac{1}{1+\gamma_ek^2\lambda^2_{De}}n_{i1}\\
\omega^2=k^2\displaystyle[\frac{\gamma_iT_i}{m_i}+\frac{\gamma_eT_e}{(1+\gamma_ek^2\lambda^2_{De})m_i}]
$$
取低频长波近似就是离子声波. 
根据 $k\lambda_{De}$ 与 1 的关系, 离子声波逐渐过渡到粒子静电波. 
现在取低频短波近似:
$$
\omega^2=\omega^2_{pi}+\gamma_i v_{ti}^2k^2\\
\omega^2_{pi}=T_e/m_i\lambda_{De}^2=n_0e^2/m_i\epsilon_0\ll\omega^2_{ei}
$$


##<font color='red'>$\S 2$ </font>垂直于外磁场的静电波

现在加入外磁场 $B_0$
如果外磁场与波传播方向平行, 由于静电波是纵波, 其振动速度也与磁场平行, 外磁场不产生作用. 

本节讨论外磁场与静电波方向垂直的情况

---
###高混杂静电振荡和高混杂波
高频情况, 离子不响应, 只考虑电子
由于外磁场的作用, 现在电子运动速度有两个分量
$$
\omega^2=\omega^2_{pe}+\omega^2_{ce}+k^2v_{te}^2=\omega^2_{HH}+k^2v_{te}^2\\
电子等离子体频率\omega^2_{pe}=n_0e^2/m_e\epsilon_0\\
电子回旋频率\omega_{ce}=eB_0/m_e
$$
当忽略电子热运动,  $\omega=\omega_{HH}$ , 这是一种比没有磁场时频率更高的静电振荡,  $\omega_{HH}$ 称高混杂频率

电子热运动不可忽略时得到可以在等离子体中传播的高混杂静电波

---
###低混杂静电振荡和低混杂波
低频考虑离子的相应, 等离子体保持准电中性. 
在离子声波的方程组中加入洛伦兹力项, 分别解出 $u_{ex}$ 和 $u_{ix}$ , 利用准中性条件,  $u_{ex}=u_{ix}$ , 得到:
$$
\omega^2=\omega_{ce}\omega_{ci}+k^2v_{s}^2=\omega^2_{LH}+k^2v_{s}^2\\
\omega_{LH}\ 称低混杂频率
$$
低混杂波当外磁场为 0 时就是离子声波

##<font color='red'>$\S 3$ </font>高频电磁波在等离子体中的传播
###无磁场
电磁波是横波, 它的传播只会引起电子的横向运动, 因此动力学方程不出现热压强项, 因为热压强只对纵向产生作用
$$
\begin{cases}
    m_e\displaystyle\frac{\partial \boldsymbol{u_{e1}}}{\partial t}=-e\boldsymbol{E}_1\\
    \nabla\times\boldsymbol{E}_1=\displaystyle
    -\frac{\partial \boldsymbol{B}_1}{\partial t}\\
    \nabla\times\boldsymbol{B}_1=\displaystyle\frac{1}{c^2}\frac{\partial \boldsymbol{E}_1}{\partial t}+\mu_0\boldsymbol{j}_1\\
    \boldsymbol{j}_1=-en_0\boldsymbol{u_{e1}}
\end{cases}
$$
电子只有横向运动, 在波传播方向电子密度不受扰动, 所以电子的连续性方程不需要列出. 方程组只有电子动力学和电磁场(1+3)
此外, 还忽略了二阶的洛伦兹力项和碰撞项(稀薄等离子体)
$$
\nabla\times\nabla\times\boldsymbol{E}_1=\nabla(\nabla\cdot\boldsymbol{E}_1)-\nabla^2\boldsymbol{E}_1=\displaystyle-\frac{1}{c^2}\frac{\partial^2 \boldsymbol{E}_1}{\partial t^2}-\mu_0\frac{\partial \boldsymbol{j}_1}{\partial t}\\
电磁波是横波, 所以\nabla\cdot\boldsymbol{E}_1=0\\
得到\\
\nabla^2\boldsymbol{E}_1-\frac{1}{c^2}\frac{\partial^2 \boldsymbol{E}_1}{\partial t^2}-\frac{\omega^2_{pe}}{c^2}\boldsymbol{E}_1=0\\
色散关系:\\
\omega^2=\omega^2_{pe}+c^2k^2
$$
这表明等离子体是一种色散介质, 且折射率小于1, $v_g<c<v_p$

可以用相移法测定等离子体密度

---
###波矢垂直磁场
有外磁场情况下, 电场可能有纵向分量, $\nabla\cdot\boldsymbol{E}_1$不一定为0. 

$$
\begin{cases}
    m_e\displaystyle\frac{\partial \boldsymbol{u_{e1}}}{\partial t}=-e\boldsymbol{E}_1-eu_{e1}\times\boldsymbol{B}_0\\
    \nabla^2\boldsymbol{E}_1-\nabla(\nabla\cdot\boldsymbol{E}_1)\displaystyle-\frac{1}{c^2}\frac{\partial^2 \boldsymbol{E}_1}{\partial t^2}=-en_0\mu_0\frac{\partial \boldsymbol{u_{e1}}}{\partial t}
\end{cases}
$$

电场可能有两种基本方向:
**寻常波**$\boldsymbol{E}_1\parallel\boldsymbol{B}_0$
此时电子速度与磁场平行, 磁场不产生作用, 等价于没有磁场(o波)

**非寻常波**$\boldsymbol{E}_1\bot\boldsymbol{B}_0$
由于洛伦兹力的作用, 电子速度将在垂直于磁场的两个方向均有分量, 电场同理
写出写分量方程组, 消去两个速度量, 根据非零解条件行列式为0, 得到非寻常波(x波)的色散关系:
$$
(ck)^2=\omega^2\displaystyle[1-\frac{\omega^2_{pe}(\omega^2-\omega^2_{pe})}{\omega^2(\omega^2-\omega^2_{HH})}]
$$
非寻常波是横电磁波和静电纵波组成的混合波, 是椭圆偏振的

利用$k=0$, 发现频率有两个正根, 分别对应左旋和右旋椭圆偏振的截止频率, 相应的波模式只有在截止频率以上才能传播. 非寻常波有两个不相交的传播带. 

对于高密度等离子体, $\omega_{pe}\gg\omega_{ce}$, 所以$\omega_{R}>\omega_{L}$
$$
\omega_{L}<\omega_{pe}<\omega_{HH}<\omega_{R}
$$
此外, 左旋偏振波在$\omega_{HH}$处发散, 波的能量被等离子体强烈吸收, 称为共振. 

本节的计算基于高频近似, 当频率很低时离子的相应就不能忽略, 直接应用这里的结论是错误的

---
###波矢平行磁场
方程组的列法完全同理, 色散关系:
$$
\omega^2-(ck)^2-\omega^2_{pe}=\pm\displaystyle\frac{\omega_{ce}}{\omega}(\omega^2-(ck)^2)\\
$$
将这个结果代回电场的方程组, 发现$E_{1y}=\pm iE_{1x}$, 表明等离子体中平行于外磁场方向传播的电磁波是圆偏振波. 

由此色散关系可以改写为:
$$
k_{R(L)}=\displaystyle\frac{\omega}{c}\sqrt{1-\frac{\omega^2_{pe}}{\omega^2(1-\mp\omega_{ce}/\omega)}}
$$

L波和R波的高频分支都存在截止频率

R波的低频分支没有截止频率, 但在$\omega=\omega_{ce}$处存在共振, 因为电子回旋方向与电场矢量旋转方向相同, 称为电子回旋共振, R波的低频分支称为电子回旋波

对低频情况, 离子运动是主要的, 而离子回旋方向和L波相同, 在$\omega=\omega_{ci}$处也会存在共振, 称为离子回旋共振

频率很低时只有R波能传播, 这时的色散关系可以近似表示为
$$
\omega=\displaystyle\frac{\omega_{ce}c^2}{\omega^2_{pe}}k^2
$$
不难发现此时频率高的波传播速度(群速度)更大

**法拉第旋转**
一个线偏振波可以分解为左右旋偏振波的叠加, 而传播过程中两波波矢量(或相速度)不同, 相位差不恒定, 合成的线偏振波的偏振面会以磁力线为轴旋转, 法拉第旋转角为:
$$
\phi=arccot\frac{E_x}{E_y}=\frac{1}{2}(k_L-k_R)\Delta z
$$


##<font color='red'>$\S 4$ </font>磁流体力学波

对于低频的情况, 电子离子是耦合的, 可以用单磁流体力学方程来描述
方程组可以写为:
$$
\begin{cases}
    \displaystyle\frac{\partial \rho}{\partial t}+\nabla\cdot(\rho \boldsymbol{u})=0\\
    \displaystyle \rho\frac{d\boldsymbol{u}}{dt}=-\nabla p+\boldsymbol{j}\times\boldsymbol{B}\\
    \nabla\times(\boldsymbol{u}\times\boldsymbol{B})=\displaystyle\frac{\partial \boldsymbol{B}}{\partial t}\\
    \nabla\times\boldsymbol{B}=\mu_0\boldsymbol{j}\\
    p\rho^{-\gamma}=Const
\end{cases}
$$
利用只有外磁场的一阶近似, 得到方程组:
$$
\begin{cases}
    \displaystyle\frac{\partial \rho_1}{\partial t}+\rho_1\nabla\cdot\boldsymbol{u}_1=0\\
    \displaystyle \rho_0\frac{d\boldsymbol{u}_1}{dt}+v_s^2\nabla\rho_0+\frac{1}{\mu_0}\boldsymbol{B}_0\times(\nabla\times\boldsymbol{B}_1)=0\\
    \displaystyle\frac{\partial \boldsymbol{B}_1}{\partial t}-\nabla\times(\boldsymbol{u}_1\times\boldsymbol{B}_0)=0\\
\end{cases}
$$
其中利用了绝热关系$\nabla p=\displaystyle\frac{\partial p}{\partial \rho}\nabla \rho_1=v_s^2\nabla \rho_1$, $v_s$是流体声速. 

联立消去$\rho$和$B_1$, 就得到关于$u_1$的波动方程:
$$
\displaystyle\frac{\partial^2 \boldsymbol{u}_1}{\partial^2 t}-v_s^2\nabla(\nabla\cdot\boldsymbol{u}_1)+\boldsymbol{v}_A\times\nabla\times[\nabla\times(\boldsymbol{u}_1\times\boldsymbol{v}_A)]=0\\
\boldsymbol{v}_A=\boldsymbol{B}_1/\sqrt{\mu_0\rho_0}
$$
分别研究平行和垂直于磁场两个方向的波, 再利用平面波假设, 可以得到化简的波动方程:
$$
-\omega^2\boldsymbol{u}_1+(v_s^2+v_A^2)(\boldsymbol{k}\cdot\boldsymbol{u}_1)\boldsymbol{k}+(\boldsymbol{v}_A\cdot\boldsymbol{k})[(\boldsymbol{v}_A\cdot\boldsymbol{k})\boldsymbol{u}_1-(\boldsymbol{v}_A\cdot\boldsymbol{u}_1)\boldsymbol{k}-(\boldsymbol{k}\cdot\boldsymbol{u}_1)\boldsymbol{v}_A]=0
$$

---
这个方程的一般性讨论比较复杂, 下面给出两种简单的情况:
###磁声波
设传播方向垂直于磁场, $\boldsymbol{k}\bot\boldsymbol{B}_0$, 方程的解$\boldsymbol{u}_1$平行于$\boldsymbol{k}$, 所以是纵波, 称为磁声波. 

色散关系$\omega^2/k^2=v_s^2+v_A^2$
扰动磁场方向与原磁场平行, $\boldsymbol{B}_1=\displaystyle\frac{k}{\omega}u_1\boldsymbol{B}_0$

此时原磁场的磁力线不发生扭曲, 但在磁声波传播方向产生疏密变化. 对于理想导电流体, 由于冻结效应, 磁流体完全跟随磁力线移动, 所以磁流体也会产生疏密波动. 

这种声波是磁压强和动力压强共同作用而传递的纵波. 

---
###阿尔文波
波传播方向平行于磁场, 这时可能存在两种波, 一种是纵波(普通声波), 一种是横波(阿尔文波). (取决于$\boldsymbol{u}_1$是平行还是垂直于$\boldsymbol{k}$)

两种波的色散关系都是 $\omega=kv$
其中, 声波的相速度就是声速$v_s$, 阿尔文波的相速度为$v_A$. 
先前已经定义的$v_A$因此也称为阿尔文速度. 
阿尔文波是一种纯磁流体现象. 

磁场作用于导电流体上相当于均匀各向同的磁压强 $B^2/2\mu_0$ 和沿磁力线的张力 $B^2/\mu_0$.  假设单位横截面上有 B 条磁力线, 则每条上的张力就是 $B/\mu_0$.  当流体元受横向扰动偏离平衡位置, 则磁力线随流体元一起运动,  相当于有质量的弹性弦,  平均等效质量为 $\rho/B$. 根据这个模型计算出的阿尔文速度与解方程所得的相同. 

事实上阿尔文波也可以与磁力线以任意锐角角度传播,  称为斜阿尔文波. 

---
###有限电导率时阿尔文波的衰减
这时磁力线与磁流体不完全冻结, 相对运动会导致波传播时的损耗. 
在第三个线性化方程右端增加一项阻尼 $\nu_m\nabla^2 \boldsymbol{B}_1$

色散关系:$(kv_A)^2=\omega^2(1+i\nu_mk^2/\omega)$

波矢可以近似为:$k=\displaystyle\frac{\omega}{v_A}+i\frac{\omega^2\nu_m}{2v_A^3}$

复数波矢显示出波随空间的衰减

最后说明, 对于频率低于电子回旋频率的波, 频率趋近 $\omega_{ce}$ 为电子回旋共振波, 频率趋近 $\omega_{ci}$ 为离子回旋共振波, 频率远小于 $\omega_{ci}$ 为阿尔文波

##<font color='red'>$\S 5$ </font>波与粒子的相互作用

**朗道阻尼和朗道增长**
波可以与粒子发生能量交换. 
假设粒子群与波都沿着磁力线方向移动, 而且粒子的漂移速度和波传播速度相近, 这时就会产生明显能量传递. 
能量传递的结果是波的振幅和粒子平均速度发生变化. 

粒子群的漂移运动方程为:
$$
m\displaystyle\frac{dv}{dt}=qEcos(kz-\omega t)
$$
用逐级近似的方式来计算这种扰动
先假设静电波场是一个小量, 这样零级解是匀速直线运动:
$$
z=v_0t+z_0
$$
加入速度一级修正:
$$
m\displaystyle\frac{dv_1}{dt}=qEcos(kz_0+kv_0t-\omega t)=qEcos(kz_0+\alpha t)\\
v_1=\frac{qE}{m\alpha}[sin(kz_0+\alpha t)-sin(kz_0)]\\
z_1=\int_0^t v_1dt
$$
再引入速度二级修正, $v=v_0+v_1+v_2$ , $z=z_0+z_1$,  全部带入原始方程, 再利用 $kz_1\ll 1$ , 得到:
$$
m\displaystyle\frac{dv_2}{dt}=-qEsin(kz_0+\alpha t)kz_1
$$
二级修正下动能的变化:
$$
\frac{d}{dt}(\frac{1}{2}mv^2)=mv_0\frac{dv_1}{dt}+mv_1\frac{dv_1}{dt}+mv_0\frac{dv_2}{dt}
$$
表达式全部带入上式, 然后对 $z_0$ 取平均
$$
\langle\frac{d}{dt}(\frac{1}{2}mv^2)\rangle_{z_0}=\frac{q^2E^2}{m\alpha}(-\frac{\omega sin\alpha t}{\alpha^2}+tcos\alpha t+\frac{\omega tcos\alpha t}{\alpha})
$$
粒子从波得到的能还要对粒子初始速度分布取平均. 
设粒子初始速度分布为 $f(v_0)=\displaystyle f(\frac{\alpha+\omega}{k})=g(\alpha)$
归一化条件
$$
\int_{-\infty}^{\infty}f(v_0)dv_0=\frac{1}{k}\int g(\alpha)d\alpha=1
$$
$\displaystyle\langle\frac{d}{dt}(\frac{1}{2}mv^2)\rangle_{z_0}$ 对于这个 $v_0$ 的分布积分

积分的第二项 $\displaystyle\frac{1}{k}\int g(\alpha) tcos\alpha td\alpha=\frac{1}{k}\int g(x/t)cosxdx$ 在 $t\rightarrow\infty$ 时为0

积分的第三项同理, $g(\alpha)$ 的偶函数部分没有贡献, 奇函数部分在 $t\rightarrow\infty$ 时为0

只有第一项有贡献: $\displaystyle-\frac{\omega q^2E^2}{2mk}\int g(\alpha)\frac{ sin\alpha t}{\alpha^2}d\alpha$
这个积分主要在 0 附近有显著值, 因此对 $g(\alpha)$ 在 0 处展开
$$
g(\alpha)=g(0)+\alpha g'(0)+(\alpha^2/2)g''(0)
$$
因为 $\displaystyle\frac{ sin\alpha t}{\alpha^2}$ 是偶函数, 所以展开式只有第二项有贡献

从而对于较大的 t 值,  动能变化率的相空间平均值为
$$
\langle\frac{d}{dt}(\frac{1}{2}mv^2)\rangle_{z_0}=-\frac{\omega q^2E^2}{2mk}\int g'(0)\frac{ sin\alpha t}{\alpha}d\alpha=-\frac{\pi \omega q^2E^2}{2m|k|k}(\frac{\partial f(v_0)}{\partial v_0})_{v_0=\omega/k}
$$

可见, 能量是流向波还是粒子主要取决于粒子集体速度分布在 $v_0=v_p$ 点的走势

当粒子运动速度接近于相速度时, 由于粒子与波的共振作用, 速度大于相速度的粒子会将多余的能量交给波, 反之从波吸收能量. 