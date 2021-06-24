# 多载波技术

## 多载波技术论文

### A Novel Optical Fast OFDM with Reduced Channel Spacing Equal to Half of the Symbol Rate Per Carrier

传统的正交频分复用OFDM技术对符号周期为T的每个符号使用正交函数$$e^{j*2\pi* kt/T}$$,T是符号周期，K是子信道序号。这种情况下的最小信道间隔是载波的符号速率（图片上来看是子载波一半的带宽）。**然而**：如果子载波的相位可以被控制（使用正交函数$$cos(2\pi×kt/(2T))$$），最小频率间隔可以减小到1/\(2T\),相位控制的目的是保证子载波的正交性。——**光正交频分复用**。

### Advantage of Optical Fast OFDM Over OFDM in Residual Frequency Offset Compensation

基于上文中的FOFDM调制技术，该文章分析了FOFDM中由残余频偏（RFO）引起的载波间干扰。比较了补偿RFO的多抽头均衡器的性能。

### 20 Tbit/s Transmission Over 6860 km With Sub-Nyquist Channel Spacing

发射机带宽受限引起的调制记忆和多符号检测，可以降低欠奈奎斯特信道间隔系统的符号间干扰。本文章传输的是100G带宽受限的偏振分复用归零QPSK信号，频谱利用率为400%。————带宽受限（由信号的主动滤波产生，会导致严重的符号间干扰和复杂的信号星座，这可以解释为调制格式中的符号相关或记忆）的偏振复用RE-QPSK传输格式。**本文开发了一种算法（包括最大似然估计MLSE），利用符号相关性，减轻与严格预滤波相关的线性码间干扰损失。**

### 1.03-Exabit/s-km Super-Nyquist-WDM Transmission over 7,326-km Seven-Core Fiber

本文主要实现的是多芯光纤和超奈奎斯特波分复用相结合达到的记录，只看超奈奎斯特有用的部分：超密集WDM技术（又称为超奈奎斯特WDM）的频率间隔小于波特率。30Gbaud的波特率的载波间隔为25Ghz（有重叠，但是使用QDB能抑制）。对于超奈奎斯特WDM传输，**光信号的带宽必须限制在波特率之下**。还是使用的双二进制脉冲整形，信号的功率谱带宽为B/2（B为波特率），通过复用该类型信号，可以有效抑制载波重叠分量——可使用DAC直接生产双二进制DP-QPSK信号。

### Experimental investigation on the performance of closely spaced multi-carrier PDM-QPSK with digital coherent detection



{% embed url="https://blog.csdn.net/qq\_40090859/article/details/103083595" caption="多载波和OFDM" %}

{% embed url="https://blog.csdn.net/dear\_father/article/details/95531134?ops\_request\_misc=%257B%2522request%255Fid%2522%253A%2522162450075616780366550342%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request\_id=162450075616780366550342&biz\_id=0&utm\_medium=distribute.pc\_search\_result.none-task-blog-2~all~sobaiduend~default-3-95531134.first\_rank\_v2\_pc\_rank\_v29&utm\_term=%E5%A4%9A%E8%BD%BD%E6%B3%A2&spm=1018.2226.3001.4187" caption="5G的三个相关调制技术" %}



**关于DQPSK的论文介绍**:

目前，业界已达成共识，将QPSK或DQPSK作为100G传输的调制格式，由于其恒包络特特点，可以有效降低DWDM传输中的交叉相位调制XPM效应，同时能够有效的提升频谱利用率。

## 多载波技术调研：

DWDM系统：指复用间隔比WDM的信道间隔小，复用波道数更多。复用和解复用与调制格式无关。

### Optical fast OFDM系统的调研

**传统OFDM**：1、将串行的高速数据转换为多个并行的低速数据，称之为子载波，OFDM可以通过再发送端加入循环前缀CP来解决色度色散CD和偏振模色散PMD引起的符号间干扰（只要CP长度大于色散引起的群速度时延即可完全将信号匹配回恢复出来）。2、频谱允许重叠且子载波正交。3、各子载波间的调制和解调可通过反快速傅里叶变换（IFFT）和快速傅里叶变换（FFT）来实现。接收端采用匹配滤波器或者相关器，当子载波数量多的时候采用IDFT和DFT可加快进度。

**快速OFDM**：1、前言：光正交频分复用技术作为一种多载波技术，与波分复用方式相比，有更高的频谱效率、良好的抵抗色散和非线性损伤能力等特点。但是传统的光OFDM技术已经比较成熟，但是对原理进行修改，它的子载波间距还能进一步压缩，提高传输效率。**这种能将子载波间距进一步缩小的技术叫做快速OFDM**。2、介绍：一般的OFDM系统都是通过离散傅里叶变换（DFT）来实现的，先阶段研究的快速OFDM系统主要集中在离散余弦变换（DCT）上来实现。

**全光OFDM：将电域FFT和IFFT过程搬移到光上来处理。**



