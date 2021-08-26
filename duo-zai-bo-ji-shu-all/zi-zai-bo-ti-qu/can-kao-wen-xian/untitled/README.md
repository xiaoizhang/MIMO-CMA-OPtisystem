---
description: >-
  看34之前先看33  Experimental demonstration of crosstalk compensation for super
  highdensity multicarrier PDMQPSK signal by MIMO processing
---

# 34

双PDM-QPSK信号，子载波间隔可以降低到波特率的78%。使用MIMO处理补偿串扰。

\[1\]奈奎斯特WDM系统，100Gbps以上的光纤传输，子载波间隔受限于信号的波特率。\[2\]参考文献34.50Gbps单偏振正交QPSK，精确的子载波间隔被反馈到MIMO均衡中。**本文**：128Gbps偏振复用QPSK。子载波间隔小于波特率。\[3\]DSP处理的频域均衡的色散补偿功能。\[2\]FIR滤波器的自适应MIMO均衡功能。\[4\]载波相位恢复功能，\[6\]光学多载波产生技术产生LO连续波光源。

背靠背系统。不适用光学滤波器。载波间隔设置为18.75，25，32，37.50和50Ghz。接收带宽3db为20Ghz（信号32Gbaud），使用光学多载波产生技术产生两个光源。接收到的信号使用8通道数字滤波器以80Ghz的采样率转换为数字信号。数字信号重新被采样到64Ghz。T/2间隔FIR自适应MIMO滤波器使用31个抽头系数。算法采用CMA更新抽头系数。

对比奈奎斯特WDM系统：在耦合TXs输出的PDM子载波之前，使用**光学奈奎斯特滤波器**对每个子载波进行整型。

