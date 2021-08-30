---
description: >-
  Compatibility between Nonlinear Compensation and Crosstalk Compensation Using
  MIMO Processing in Super-High-Density Multi-Carrier Transmission System
---

# 2015——非线性补偿+串扰补偿=联合。25/32——2-PDM-QPSK

两个子载波32GBaud信号的子载波间隔为25Ghz。非线性补偿和基于MIMO的串扰补偿实现了2-3dB的Q因子改善且互不干扰。

参考文献：【1】——【3】补偿数字相干系统中由光纤非线性引起的波形失真。子载波间隔小于波特率的传输系统。基于外差检测方案使用FDMIMO（频率分集多输入多输出）来补偿子载波之间的相邻串扰【4】【5】。基于零差检测方案的串扰补偿XTC【6】【7】.

本文：将数字反向传播（DSP）NLC应用于采用MIMO处理的超高密度多载波XTC传输系统。NLC=N级双偏振非线性控制【1】——【3】——补偿子载波之间的子相位调制SPM和部分交叉相位调制XPM。MIMO串扰补偿就和之前一样了，但是$$\tau$$是放在非线性里的。

![&#x975E;&#x7EBF;&#x6027;&#x548C;MIMO&#x8865;&#x507F;&#x56FE;](../../../.gitbook/assets/image%20%2813%29.png)

传输系统：发射光功率2dB/ch，传输480KM.每80KM分配一个光放大器。三个256Gbps的多载波信号以75Ghz的信道间隔传输，每个信道由128Gbps的PDM-QPSK信号组成，波特率为32Gbaud。副载波间隔为25Ghz，对应于78%的信号波特率。

![&#x4E09;&#x4E2A;&#x901A;&#x9053;&#x53D1;&#x9001;&#x56FE;](../../../.gitbook/assets/image%20%2812%29.png)

使用8通道数字示波器，以80GSample/s的速度接收信号转化为数字信号。重采样为64Gsample/s。自适应MIMO的抽头系数个数为31，T/2间隔FIR滤波器。抽头系数使用CMA算法。

