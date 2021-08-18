---
description: 从SCI和IEEE上找的多载波技术相关文献
---

# 相关文献（2021-5月之前）

### A Novel Optical Fast OFDM with Reduced Channel Spacing Equal to Half of the Symbol Rate Per Carrier

传统的正交频分复用OFDM技术对符号周期为T的每个符号使用正交函数$$e^{j*2\pi* kt/T}$$,T是符号周期，K是子信道序号。这种情况下的最小信道间隔是载波的符号速率（图片上来看是子载波一半的带宽）。**然而**：如果子载波的相位可以被控制（使用正交函数$$cos(2\pi×kt/(2T))$$），最小频率间隔可以减小到1/\(2T\),相位控制的目的是保证子载波的正交性。——**光正交频分复用**。

### Advantage of Optical Fast OFDM Over OFDM in Residual Frequency Offset Compensation

基于上文中的FOFDM调制技术，该文章分析了FOFDM中由残余频偏（RFO）引起的载波间干扰。比较了补偿RFO的多抽头均衡器的性能。

### 20 Tbit/s Transmission Over 6860 km With Sub-Nyquist Channel Spacing

发射机带宽受限引起的调制记忆和多符号检测，可以降低欠奈奎斯特信道间隔系统的符号间干扰。本文章传输的是100G带宽受限的偏振分复用归零QPSK信号，频谱利用率为400%。————带宽受限（由信号的主动滤波产生，会导致严重的符号间干扰和复杂的信号星座，这可以解释为调制格式中的符号相关或记忆）的偏振复用RE-QPSK传输格式。**本文开发了一种算法（包括最大似然估计MLSE），利用符号相关性，减轻与严格预滤波相关的线性码间干扰损失。**

### 1.03-Exabit/s-km Super-Nyquist-WDM Transmission over 7,326-km Seven-Core Fiber

本文主要实现的是多芯光纤和超奈奎斯特波分复用相结合达到的记录，只看超奈奎斯特有用的部分：超密集WDM技术（又称为超奈奎斯特WDM）的频率间隔小于波特率。30Gbaud的波特率的载波间隔为25Ghz（83.3%）（有重叠，但是使用QDB能抑制）。对于超奈奎斯特WDM传输，**光信号的带宽必须限制在波特率之下**。还是使用的双二进制脉冲整形，信号的功率谱带宽为B/2（B为波特率），通过复用该类型信号，可以有效抑制载波重叠分量——可使用DAC直接生产双二进制DP-QPSK信号。

### Experimental investigation on the performance of closely spaced multi-carrier PDM-QPSK with digital coherent detection

两个PDM-QPSK子载波，载波间隔为波特率大小。该情况下，需要达到过采样系统为4和基于恒模算法CMA的具有1/4符号间隔抽头的数字均衡器一起。当载波符号对齐时，性能最佳，具有适当抗混叠滤波的大（如4倍）过采样有助于最小化相干串扰引起的损伤，并且使用适当的电子预滤波器进行载波分离是有益的。

### Achievement of Subchannel Frequency Spacing Less Than Symbol Rate and Improvement of Dispersion Tolerance in Optical OFDM Transmission

新的光正交频分复用传输（又叫光密集正交频分复用DOFDM），子信道的频率间隔小于符号率。在光正交频分复用传输中，子信道之间的频率正交性允许频率重叠，并且它实现了更窄的信号带宽和高色散容限。通过多采样或时间间隔为1/N▲f的MZI来实现对DOFDM的复用和解复用。该实验可实现80%波特率的子信道频率间隔。

### Experiment on Optical OFDM Transmission with Frequency Spacing of Subchannels at 80% of Symbol Rate

一种新的正交频分复用方案，子信道频率间隔为符号速率的80%。光正交复用频分复用系统可以窄化信号带宽。（光正交频分复用就是密集正交频分复用DOFDM）本文通过缩短时间窗来提取数据符号，即使频率间隔不等于符号率，频率正交也是满足的。

### 1.2 Tbit/s orthogonal PDM-RZ-QPSK DWDM signal transmission over 1040 km SMF-28

正交密集波分复用信号。每个信号大约25Gbaud的QPSK信号，载波间隔为25Ghz\(100%\)。1.2Tbps下实现传输1040KM.2010年之前最远。

