# Cp.VIII �˶��������ӵķ���

##<font color='red'>$\S 1$ </font>����-άл����

����һ���е���Դ���˹Τ���̴��볡ǿ�������Եõ���ά��Դ�Ĳ�������:
$$
\partial_\mu F^{\mu\nu}=\frac{4\pi}{c}J^\nu\\
\ \\
\partial_\mu\partial^\mu A^\nu=\frac{4\pi}{c}J^\nu
$$

Ϊ�������������άЭ����ʽ�Ľ�, ������ʱ��������άЭ����ʽ�ĸ��ֺ���:
$$
\partial_\mu\partial^\mu D(x,x')=\delta^4(x-x')
$$
(��ʵ��, �κ�ֻ������ $x-x'=R$ �ĺ�������������д�����ֺ���)

Ȼ�����ø���Ҷ�任���, дΪ:
$$
D(x,x')=\int \frac{d^4k}{(2\pi)^4}\tilde{D}(k)e^{-ik\cdot (x-x')}
$$
���� $\delta$ �����ĸ���Ҷ�任
$$
\mathscr{F}\partial_\mu\partial^\mu D(x,x')=\mathscr{F}\delta^4(x-x')=1\\
\partial_\mu\partial^\mu\mathscr{F} D(x,x')=\partial_\mu\partial^\mu\tilde{D}(k)=-k^2\tilde{D}(k)\\
\ \\
\tilde{D}(k)=-(1/k^2)\ \ \ (k^2=k_\mu k^\mu)\\
D(x,x')=-\int \frac{d^4k}{(2\pi)^4}\frac{e^{-ik\cdot (x-x')}}{k^2}
$$
�������������ʵ���ϴ������, ��Ҫ��һ������һ��������Ķ���, Ҳ����Ϊ��ѡ����ʵ�·��. ����ֻ���Ƴٸ��ֺ������Ƿ�������Եĺ���, ��Ӧ��·������ʵ���ϲ��������ϰ�Բ. ���⻹Ӧ�ƿ�ʵ���ϵ��������.
$$
D^{(+)}(x,x')=-\int \frac{d^4k}{(2\pi)^4}\frac{e^{-ik\cdot (x-x')}}{(k_0+i\epsilon)^2-\boldsymbol{k}\cdot \boldsymbol{k}}
$$

---
�����������
$$
\begin{aligned}
    D^{(+)}(x,x')&=\frac{\eta(x_0-x_0')}{4\pi R}\delta(x_0-x_0'-R)\\
    &=\frac{\eta(x_0-x_0')}{2\pi}\delta[(x-x')^2]
\end{aligned}
$$
������
$$
\begin{aligned}
    \delta[(x-x')^2]&=\delta[(x_0-x_0')^2-(x-x')^2]\\
    &=\delta[(x_0-x_0')^2-R^2]\\
    &=\delta[(x_0-x_0'-|R|)(x_0-x_0'+|R|)]\\
    &�ڶ������,����\\
    &=\delta(x_0-x_0'-R)
\end{aligned}\\
��\ \ \delta[f(\tau)]=\sum_i \frac{\delta (\tau-\tau_i)}{|\displaystyle\frac{df}{d\tau}|_{\tau_i}}
$$

���ڿ���д���������άЭ���
$$
A^\mu(x)=\frac{4\pi}{c}\int d^4xD^{(+)}(x,x')J^\mu(x')
$$

��������������ȡΪ $r^\mu(\tau)$ , ����ɵ����ܶ���ʸ��Ϊ
$$
J^\mu(x)=ec^2\int d\tau u^\mu(\tau)\delta^4[(x-r(\tau))^2]=(\rho c,\rho \boldsymbol{v})
$$
���� $\delta$ �����Ĵ���, ����ֻ��ĳ���ض�ʱ���й���, �����׶����, ��ʱ���ӷ����Ų���۲��������¼�������, ������Ϊ 0. �����Ų�����������������۲���ȥ��׶�Ľ���.

---

**����-άл����:**
$$
A^\mu(x)=\frac{eu^\mu(\tau)}{u\cdot [x-r(\tau)]}|_{\tau=\tau_0}
$$
��������ʽд����ά��ʽ����ֱ��
$$
\Phi(\boldsymbol{x},t)=[\frac{e}{(1-\boldsymbol{\beta}\cdot\boldsymbol{n})R}]_{ret}\\
\ \\
\boldsymbol{A}(\boldsymbol{x},t)=[\frac{e\boldsymbol{\beta}}{(1-\boldsymbol{\beta}\cdot\boldsymbol{n})R}]_{ret}
$$
���� $\boldsymbol{n}$ �����ӷ����Ų�ʱ��λ��ָ��۲��ĵ�λʸ��

ԭ����, ��������ƾ���΢�־Ϳ��Եõ��˶���ɵĵ�ų�, ����������̱�����ȷ�����Ƴ�ЧӦ, ����Ƚϸ���.

**�˶���ɵĵ�ų�**
$$
\boldsymbol{E}=[\frac{e(\boldsymbol{n}-\boldsymbol{\beta})}{\gamma
^2(1-\boldsymbol{\beta}\cdot\boldsymbol{n})^3R^2}+\frac{e}{c}\frac{\boldsymbol{n}\times[(\boldsymbol{n}-\boldsymbol{\beta})\times\dot{\boldsymbol{\beta}}]}{(1-\boldsymbol{\beta}\cdot\boldsymbol{n})^3R}]_{ret}\\
\ \\
\boldsymbol{B}=(\boldsymbol{n}\times\boldsymbol{E})_{ret}
$$
�糡�ĵ�һ���ǵ��͵ľ���, ������ $R^{-2}$ ,�ڶ����ǵ��͵ķ��䳡, ������ $R^{-1}$ �������������Ӽ��ٶ�.

����-άл���� ����һ���Ƶ���ʽ�������ھ�ֹϵд�����׳�Ȼ���������ȱ任, ������Ԥ�ȼٶ��˵����ֻ���������ӵ��ٶ�, ���Եò����йؼ��ٶȵĵڶ���

##<font color='red'>$\S 2$ </font>��Ī����ʽ����ķ��ɢ��

�������ӷ���Ĺ���ֻ�����ڵ���Ƶĵڶ���. �� $\beta\ll1$ �Ľ����µ糡�ķ��䳡���ֿ���д��
$$
\boldsymbol{E}=[\frac{e}{c}\frac{\boldsymbol{n}\times[\boldsymbol{n}\times\dot{\boldsymbol{\beta}}]}{R}]_{ret}
$$
�����Ϳ���д�����䳡�Ĺ���
$$
\frac{dP}{d\Omega}=\frac{c}{4\pi}R[\boldsymbol{E}\times\boldsymbol{H}]=\frac{e^2}{4\pi c^3}|\dot{\boldsymbol{v}}|^2\sin^2\Theta
$$
����ǻ��ֵõ��ܹ���, ��һ�о��� **��Ī����ʽ**
$$
\begin{aligned}
    P&=\frac{2}{3}\frac{e^2}{c^3}|\dot{\boldsymbol{v}}|^2\\
    &=\frac{2}{3}\frac{e^2}{m^2c^3}\frac{d\boldsymbol{p}}{dt}\cdot\frac{d\boldsymbol{p}}{dt}\\
    &=-\frac{2}{3}\frac{e^2}{m^2c^3}\frac{dp^\mu}{d\tau}\cdot\frac{dp_\mu}{d\tau}\\
    &=\frac{2}{3}\frac{e^2}{c}\gamma^6[(\dot{\boldsymbol{\beta}})^2-(\boldsymbol{\beta}\times\dot{\boldsymbol{\beta}})^2]\\
    &(dt=\gamma d\tau)\\
\end{aligned}
$$
�����һ�о��� **���ɹ�ʽ**, ����Ī����ʽ����������ƹ�
����������ʱ�䶼����ʸ���������, ���Է��书����һ�������Ȳ�����

##<font color='red'>$\S 3$ </font>������Լ��ٵ�ɵķ���

�����˶��������ӵ糡��Զ����,д����ӡ͢ʸ���� $\boldsymbol{n}$ ��ͶӰ $(\boldsymbol{S}\cdot\boldsymbol{n})_{ret}$, ��ʾ�� $(t,\boldsymbol{x})$ �۲⵽������.
������ $t'=T_1$ �� $t'=T_2$ ֮������������
$$
E=\int_{T_1+R(T_1)/c}^{T_2+R(T_2)/c}(\boldsymbol{S}\cdot\boldsymbol{n})_{ret}dt=\int_{T_1}^{T_2}(\boldsymbol{S}\cdot\boldsymbol{n})\frac{dt}{dt'}dt'
$$
������֪������������ $\displaystyle(\boldsymbol{S}\cdot\boldsymbol{n})\frac{dt}{dt'}$, �� $dt'-dt=-\displaystyle\frac{d|\boldsymbol{x}=\boldsymbol{r}(t')|}{c}$, �õ� $dt=dt'(1-\boldsymbol{\beta}\cdot\boldsymbol{n})$

����**����������ӷ���ǹ���**Ϊ
$$
\frac{dP(t')}{d\Omega}=R^2\displaystyle(\boldsymbol{S}\cdot\boldsymbol{n})\frac{dt}{dt'}=\frac{e^2}{4\pi c}\frac{|\boldsymbol{n}\times[(\boldsymbol{n}-\boldsymbol{\beta})\times\dot{\boldsymbol{\beta}}]|^2}{(1-\boldsymbol{\beta}\cdot\boldsymbol{n})^5}\\
$$

����ֱ�߼��ٵ�����, ���ʽǷֲ������ýǶȱ�ʾΪ $\displaystyle\frac{e^2\dot{v}^2}{4\pi c^3}\frac{\sin\theta^2}{(1-\beta \cos\theta)^5}$ 
���ʼ���ֵ�ĽǶ�Ϊ $\cos\theta_m=\displaystyle\frac{\sqrt{1+15\beta^2}-1}{3\beta}$
�����ٶ�Խ��������, �����Խ�����������ٶȷ���.

Բ���˶���Ҳ���ü������ʾ���Ƿֲ�
$$
\frac{dP(t')}{d\Omega}=\frac{e^2}{4\pi c^3}\frac{\dot{v}^2}{(1-\beta \cos\theta)^3}[1-\frac{\sin^2\theta \cos^2\phi}{\gamma^2(1-\beta \cos\theta)^2}]
$$

��ͬ�����, �������Ӽ������ڷ�������ĵ�������ֱ�߼������� $\gamma^2$ ��, ����������൱�ɹ۵�.

##<font color='red'>$\S 4$ </font>���ӷ����Ƶ��

����Ƶ�׵ķ���һ����ù۲���ʱ�� t, ����������۲��߽Ƿֲ����� A(t).
$$
\frac{d P(t)}{d \Omega_{\mathbf{n}}}=\frac{e^2}{4 \pi c}\left[\frac{\mathbf{n} \times[(\mathbf{n}-\boldsymbol{\beta}) \times \dot{\boldsymbol{\beta}}]}{(1-\boldsymbol{\beta} \cdot \mathbf{n})^3}\right]_{\mathrm{ret}}^2 \equiv|\mathbf{A}(t)|^2
$$
Ҫ����Ƶ��, ��ʱ����������Ҷ�任
$$
\mathbf{A}(\omega)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty\mathbf{A}(t)e^{i\omega t}dt
$$
����Ƶ��������, ���� $\mathbf{A}(t)$ ��ʵʸ����.
$$
\mathbf{A}(\omega)=\mathbf{A}(-\omega)^*\\
\frac{d^2I}{d\Omega d\omega}\equiv|\mathbf{A}(\omega)|^2+|\mathbf{A}(-\omega)|^2=2|\mathbf{A}(\omega)|^2\\
~\\
\frac{dW}{d\Omega}=\int_{-\infty}^\infty|\mathbf{A}(t)|^2dt=\int_{-\infty}^\infty|\mathbf{A}(\omega)|^2d\omega=\int_{0}^\infty\frac{d^2I}{d\Omega d\omega}d\omega
$$
���� $\mathbf{A}(t)$ �ľ�����ʽ�õ�
$$
\mathbf{A}(\omega)=\sqrt{\frac{e^2}{8 \pi^2 c}} \int_{-\infty}^{\infty} e^{i \omega\left(t^{\prime}+R\left(t^{\prime}\right) / c\right)} \frac{\mathbf{n} \times[(\mathbf{n}-\boldsymbol{\beta}) \times \dot{\boldsymbol{\beta}}]}{(1-\boldsymbol{\beta} \cdot \mathbf{n})^2} d t^{\prime}
$$

##<font color='red'>$\S 5$ </font>ͬ�������Ƶ��