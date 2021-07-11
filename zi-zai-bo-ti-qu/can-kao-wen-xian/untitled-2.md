# 26-28

## Frequency diversity MIMO detection for coherent optical transmission

讲述的是频率分集MIMO检测，成功分离了6Ghz载波间隔的10GBaudQPSK信号

\[1\]\[2\]描述了基于MIMO处理的先进DSP处理的干扰消除技术。【2】OOK信号频谱重叠成功恢复，【1】基于最小均方的符号间干扰消除。

本文：解释了频率分集多输入多输出处理的公式，应对频谱重叠的 多载波检测，并表明该信号分离的问题通常是可以解决的。我感觉就是在讲CMA可以补偿MIMO算法的事。

## Frequency Diversity MIMO Detection for Dual-Carrier DP-16QAM Transmission 

具有频率分集MIMO检测的双载波DP-16QAM系统的传输性能。

\[1\]--\[3\]:奈奎斯特脉冲整型及其他多通道均衡MCE（奈奎斯特整型是一种广泛使用的技术，用于传输具有相应矩形频谱的sinc形脉冲，以最小化线性串扰。通道均衡MCE是指接收机处应用多通道均衡器来补偿串扰。）MCE技术：【1】具有最小均方算法的自适应均衡器和maximum后验检测，【2】【3】频率分集多输入多输出检测。FD-MIMO产生了CMA极化分集MIMO；论述了DP-QPSK的理论和实验。

本文：使用FDMIMO来减轻双载波10GBaud-DP-16QAM的串扰，子载波间隔从80%变化到100%。该技术优于奈奎斯特传输。

技术：联合接收——本振为双载波的中心频率——4通道数模转换器——联合色散补偿——频率校正——重采样+带通滤波器——使用4×4MIMO均衡来恢复两载波的两种偏振状态

奈奎斯特整型：发射序列由滚降因子为0.1%的根生余弦滤波器整形——————该技术支持奈奎斯特整形信号的传输。

## Frequency Diversity MIMO Detection in Polarization Multiplexed Coherent Optical Transmission

使用FD-MIMO技术分离具有小于波特率间隔的偏振复用信号。

\[4\]-\[6\]：奈奎斯特脉冲整形和其他技术用于频谱高效传输。【5】：基于MIMO处理的DSP干扰消除。【6】：频谱重叠技术成功应用于OOK信号。

本文承接第一文，对间距为6G的10GBaudPDMQPSK信号的检测和分离。

