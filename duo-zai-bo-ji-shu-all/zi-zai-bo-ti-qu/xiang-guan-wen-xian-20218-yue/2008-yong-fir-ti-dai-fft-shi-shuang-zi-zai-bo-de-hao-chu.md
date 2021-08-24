---
description: >-
  Novel no-guard-interval PDM CO-OFDM transmission  in 4.1 Tb/s (50 x 88.8-Gb/s)
  DWDM link over 800 km SMF including 50-GHz spaced ROADM nodes
---

# 2008——用FIR替代FFT时双子载波的好处

本文最开始提到，原始的PDM-CO-OFDM系统（双偏振相干OFDM）采用的不是FFT，而是在接收端用FIR滤波器进行接收。那么我们使用FIR有什么好处呢？1、减少了不必要的开销（这样就不会使速率没必要的提升了）2、本文使用了两个子载波的系统，将原本88.8Gbps的PDM-CO-QPSK的带宽缩减到了33Ghz。

使用该技术，我们使用5个基于WSS（波长选择开关）的最小间距为50Ghz的ROADM节点，在800KM的SMFs上进行了50个通道的88.8GbpsPDM 双子载波OFDM信号的传输。

发送装置：76个连续光载波信号。在L波段，31个在1578.69nm——1604.03nm的100Ghz间隔的偶信道，17个在1605.74nm——1619.62nm的100Ghz间隔和28个在1579.1nm到——601.88nm的100Ghz间隔的50Ghz移位奇数信道。连续的多载波信号的奇数和偶数信道分别被44.4Gbps的光路OFDM调制。一个OFDM的调制由两个MZM（这样产生两个子载波）和一个集成的OFDM-QPSK子载波调制器组成。MZM由5.5Ghz的正弦信号驱动产生11.1Ghz间隔的两个子载波信号。两个子载波信号再被送到OFDM-QPSK子载波调制器上。该子载波调制器由硅平面光波电路和LN波导的混合集成技术制造【11】，该调制器由一个光交织器IL和两个嵌套MZM结构的QPSK调制器组成。光交织器IL将两个滤波器分成两个QPSK滤波器，每个子载波被单独调制成不同的11.1GhzQPSK子载波信号。两子载波在输出端耦合，生成44.4Gbps的DWDM OFDM-QPSK信号。之后，奇数和偶数信道用IL合成。最后，DWDM 44.4Gbps的OFDM-QPSK信号被偏振复用为DWDM 88.8Gbps PDM OFDM-QPSK信号，偏振复用器由1.1分频器，10ns延迟器和偏振光束组合器组成。在传输之前，插入一根用于信号去相关的大色散光纤。

![PDM-OFDM&#x4FE1;&#x53F7;&#x4F20;&#x8F93;&#x88C5;&#x7F6E;](../../../.gitbook/assets/image%20%2821%29.png)

继续。。。。。

