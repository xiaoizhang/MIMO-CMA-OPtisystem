---
description: >-
  Phase noise tolerant inter-carrier-interference cancellation for WDM
  superchannels with sub-Nyquist channel spacing
---

# 2013——使用CMA消除ICI，56GBaud的间隔为50Ghz

采用CMA算法来消除欠奈奎斯特（sub-Qyquist）间隔的超载波。该方法对于56GBaudDP-QPSK信号的50Ghz间隔的ICI消除。

论文：使用DP-64QAM的64GBaud演示了320KM的1Tbps双载波传输【1】.为了提高传输距离和系统频谱效率SE，用DP-QPSK和DP-16QAM信号实现了具有一组多载波的Thz超信道【2】。因此多载波间隔紧密，由波特率分隔，甚至小于波特率间隔。但是也出现了严重的频谱重叠，即载波间干扰。OFDM【3】【4】，奈奎斯特WDM【5】【6】和sub-QyquistWDM【7】——【9】，这些是通过使用最大密集信道频谱同时保持频谱和时间正交性来实现Thz多载波超信道的有前途的方法。如果进行适当的滤波和脉冲整型，可以成功地抑制ICI。**然而，由于FFT和IFFT的计算复杂性，OFDM传输系统复杂且昂贵**。同时，奈奎斯特WDM和sub奈奎斯特WDM对频谱整型和光学滤波器也有严格的要求，这在现实中具有很高的复杂性【3】——【8】.提出了使用MIMO均衡在多个相邻载波之间联合消除ICI的概念【10】。基于CMA的MIMO放在频偏补偿前面，而基于LMS的MIMO算法放在载波相位恢复后。关于LMS的补偿算法【11】——【13】.

传输系统：光梳用作多载波源，多载波的波长间隔达到欠奈奎斯特间隔，信号由56GBaud的DP-QPSK组成。差分编码用来解决相位模糊的问题。每个载波都由一个4阶高斯滤波器滤波。接收端另一个光梳作为本振，在极化分集和相位分集相干接收之后，通过带宽为0.75倍波特率的五阶贝塞尔低通滤波器。

![](../../../.gitbook/assets/image%20%2830%29.png)

