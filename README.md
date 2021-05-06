# MIMO

**MIMO**_技术可以采取 DP-QPSK 技术的码型，但似乎已经确定其带宽了，然而在本次仿真过程中，112G的DQPSK主带宽为56G，加上旁瓣为448G，根据很多论文提到的56G，我有理由怀疑可以去掉旁瓣试试结果。—— 上文发生一周后：发现去掉不行_

**加上滤波器之后: 通过波形确实看到串扰减小了，但是得到的码型仍然不行，说明滤波器可能把有用的波形滤除了。**

## **名词介绍**

**WSS：动态可重构光加/减复用，支持任意端口波长任意上下行（可编程控制），可以进行功率平衡和滤波。**

**4×512Gbit/s四载波信号：共有四个信道，每个信道512Gbit/s，宽度100G（书上的是，这个可改）；【每个信道中采用间隔为25Ghz的子载波，每个子载波携带128Gbit/s的数据。】**

**AWG（阵列波导光栅）：波分复用系统的首选，它可以实现波长分配即解复用功能和复用功能。**

**PMC（光纤耦合器）：1、将输入光耦合到两根光纤中，2、把两根光纤的光耦合到一根光纤中。偏振态可以选择慢轴或快轴对准。保偏光纤耦合器在保持线偏振光的情况下，用来把高功率的线偏振光分离到多个通道中去。**

**PBS/PBC（光纤分束器）：1、可以把两个正交的偏振分量合成到一根光纤输出，2、可以把一个输入信号的两个正交偏振分量分开后耦合到两根光纤输出。**

**VOA（可变光衰减器）：通过衰减传输光功率来实现对信号的实时控制，精确地控制光信号的功率，为各通道波长提供稳定的衰减量。**

**PRBS：伪随机二进制序列**

### **论文：相干光传输的频率分集MIMO检测**

**该技术成功实现了分离10G波特率的双偏振QPSK信号（每信号40Gbps），间隔为6GHZ。**

**什么是频率分集MIMO（FD-MIMO）？空间分集MIMO百度有说明，它是部署在无线通信中以增加传输系统容量的。当前奈奎斯特整形技术和其他技术都在被研究，键控信号的频谱重叠部分也被成功恢复，并且最小均方也可消除符号间串扰，但是对间隔小于波特率的信号仍然有挑战性。此技术对重叠信号分离是可行的。**

**公式：假设传输两个信号**$$X_1$$和$$X_2$$两者载波间隔为2$$f_0$$,则接收信号Y为$$Y=aX_1(f-f_0)+bX_2(f+f_0)$$我们希望能够通过带通滤波器F来分开$$X_1$$和$$X_2$$如下：\(将Y带入\)$$ \begin{pmatrix} F(f-f_0)Y \\ F(f+f_0)Y \end {pmatrix}$$=$$ \begin{pmatrix} aF&bF(f-2f_0) \\ aF(f+2f_0) &bF \end {pmatrix}$$$$\begin {pmatrix} X_1 \\X_2 \end {pmatrix}$$=H$$\begin {pmatrix} X_1 \\X_2 \end {pmatrix}$$如果我们能找到矩阵H，那么传输的信号$$X_1$$和$$X_2$$就可以这样得到$$\begin {pmatrix} X_1 \\ X_2 \end {pmatrix}$$=$$H^{-1}$$$$ \begin{pmatrix} F(f-f_0)Y \\ F(f+f_0)Y \end {pmatrix}$$。类似于空间分集MIMO，矩阵H的多样决定了传输数据的最大量。很明显极端情况下，（即2信号完全重叠时H矩阵有0列，因此无法取逆）。**自适应均衡公式**：具有极化复用的两路信号公式。正两路交极化信号经过滤波后为$$y_h$$和$$y_v$$,$$\overrightarrow{y_1}=\overrightarrow{y_h}e^{-j2\pi f_0 \overrightarrow{t}}$$

$$\overrightarrow{y_2}=\overrightarrow{y_v}e^{-j2\pi f_0 \overrightarrow{t}}$$

$$\overrightarrow{y_3}=\overrightarrow{y_h}e^{+j2\pi f_0 \overrightarrow{t}}$$

$$\overrightarrow{y_4}=\overrightarrow{y_v}e^{+j2\pi f_0 \overrightarrow{t}}$$.

$$\begin {pmatrix} x_1 \\x_2 \\ x_3 \\x_4 \end {pmatrix}$$=$$ \begin {pmatrix} \overrightarrow{h_{11}} &\overrightarrow{h_{12}}&\overrightarrow{h_{13}} & \overrightarrow{h_{14}} \\ \overrightarrow{h_{21}} &\overrightarrow{h_{22}}&\overrightarrow{h_{23}} & \overrightarrow{h_{24}} \\  \overrightarrow{h_{31}} &\overrightarrow{h_{32}}&\overrightarrow{h_{33}} & \overrightarrow{h_{34}} \\  \overrightarrow{h_{41}} &\overrightarrow{h_{42}}&\overrightarrow{h_{43}} & \overrightarrow{h_{44}}   \end {pmatrix}$$$$\begin{pmatrix} \overrightarrow{y_1} \\  \overrightarrow{y_2} \\  \overrightarrow{y_3} \\  \overrightarrow{y_4}  \end {pmatrix}$$=$$\overrightarrow H$$$$\begin{pmatrix} \overrightarrow{y_1}  \\\overrightarrow{y_2}  \\\overrightarrow{y_3}  \\\overrightarrow{y_4}\\ \end {pmatrix}$$,向量符号指的是分组为多抽头向量。

\*\*\*\*

\*\*\*\*

\*\*\*\*

