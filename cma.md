# CMA

**基于偏振模色散的CMA技术**

盲均衡的基本原理： 不需要借助训练数据就可以对信道进行自适应均衡。即将信道的方程与盲均衡器的方程相乘之后为单位脉冲序列$$ \delta$$\(n\).**最理想的均衡器是无限长的，盲均衡器的训练过程就是寻找一组最优的抽头系数，使得误差e\(n\)接近于零。**

经典CMA算法：对于相移键控m-PSK调制，$$J(Wn)=E[((\vert (x\widehat(n)) \vert)^2-R_2)]$$,$$R_2$$为收敛半径，目的是寻找最优的抽头系数W\(n\)使得J最小。利用最抖下降法求极值，得$$ W(n+1)=W(n)+ux\widehat(n)[R_2-\vert x\widehat(n) \vert^2]Y^*(n) $$,u通常选取较小的正数，它决定了算法收敛的速度和收敛的精确程度。当处理完接收信号$$x\widehat(n)$$后将得到原信号x\(n\)的相移，即$$X(n)=X(n)e^(j \theta_d)$$，$$\theta_d$$是固定的相位偏移。根据一系列推导得到$$R_2=\frac{E[\vert x\widehat(n) \vert ^4]}{E[\vert x\widehat(n) \vert ^2]} $$。单偏振QPSK的CMA的算法可以用这个实现（补偿高斯白噪声noise\(n\)和信道h\(n\)），可通过误差曲线来观察，步长小收敛慢但剩余误差小，步长大则收敛快但剩余误差大。

针对偏振复用信号的CMA算法：偏振复用时光纤的琼斯矩阵为T，会将两个偏振分量混合起来，因此需要数字处理技术。先将每个偏振分量进行归一化。即输入信号$$\vert E_x \vert ^2=\vert E_y \vert^2 =1$$。抽头系数分别为$$P_x^x P_x^y P_y^x P_y^y$$，更新算法如下：

$$P_x^x(n+1)=P_x^x(n)+u(1-\vert E_x(n)\vert ^2)E_x(n)E_x^*(n)$$$$P_x^y(n+1)=P_x^y(n)+u(1-\vert E_x(n)\vert ^2)E_x(n)E_y^*(n)$$$$P_y^y(n+1)=P_y^y(n)+u(1-\vert E_y(n)\vert ^2)E_y(n)E_y^*(n)$$$$P_y^x(n+1)=P_y^x(n)+u(1-\vert E_y(n)\vert ^2)E_y(n)E_x^*(n)$$

因为抽头系数之间相互独立，如果需要补偿偏振模色散，可以采用将单抽头变成多抽头，以补偿接收信号前后码元之间的相互作用。

$$
\ [  A= \begin {pmatrix} a_{11} & a_{12 } &a_{13}\\  0&a_{22} & a_{23} \\  0&0&a_{33} \end{pmatrix} \ ]
$$

$$
\alpha \beta \gamma \delta \epsilon \zeta \eta \theta\varGamma \varDelta \varTheta \varLambda \varXi
$$

$$
\bold{ w}  \boldsymbol{222} \mathbb{hhhh} \mathit{12345}
$$

$$
\left(\frac{a}{b}\right) \left. \frac{a}{b} \right] \left[ \frac{a}{b} \right. 
\begin{matrix}
a & b \\
c & d 
\end{matrix}
$$

$$
\sim\neq \approx \cong \simeq \equiv \overset{\rm{def}}= \cup \cap \in \notin \subset \supset \varnothing \perp
$$

$$
\sum_{k=1}^N {k^2},
\begin{matrix} \sum_{k=1}^N {k^2} \end{matrix}
\int_{-N}^{N} e^x dx,
\begin{matrix} \int_{-N}^{N} e^x dx \end{matrix} \\
$$

$$
\ddag  \dag  \\S \blacksquare \blacktriangle \blacklozenge \star \bigstar
$$

$$
f(n)=\begin{cases}
n/2, & \mbox{if   } n<0 \\
2n,  & \mbox{if   } n\ge 0
\end{cases} \tag{1}
$$

$$
\int_{-N}^{N} e^x dx,
\begin{matrix} \int_{-N}^{N} e^x dx \end{matrix} \\
$$

$$
\begin{align}
f(x) &=(a+b+c)^2   \\
      &=a^2+b^2+c^2 \\
      &+ 2ab+2ac+2bc 
\end{align}
$$

$$
f(n)=\begin{cases}
n/2, & \mbox{if   } n<0 \\
2n,  & \mbox{if   } n\ge 0
\end{cases} \tag{1}
$$



