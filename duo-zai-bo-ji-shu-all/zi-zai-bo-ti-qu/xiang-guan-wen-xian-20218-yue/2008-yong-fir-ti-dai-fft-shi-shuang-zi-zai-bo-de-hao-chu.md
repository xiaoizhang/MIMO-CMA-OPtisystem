---
description: >-
  Novel no-guard-interval PDM CO-OFDM transmission  in 4.1 Tb/s (50 x 88.8-Gb/s)
  DWDM link over 800 km SMF including 50-GHz spaced ROADM nodes
---

# 2008——用FIR替代FFT时双子载波的好处

本文最开始提到，原始的PDM-CO-OFDM系统（双偏振相干OFDM）采用的不是FFT，而是在接收端用FIR滤波器进行接收。那么我们使用FIR有什么好处呢？1、减少了不必要的开销（这样就不会使速率没必要的提升了）2、本文使用了两个子载波的系统，将原本88.8Gbps的PDM-CO-QPSK的带宽缩减到了33Ghz。

使用该技术，我们使用5个基于WSS（波长选择开关）的最小间距为50Ghz的ROADM节点，在8000KM的SMFs上进行了50个通道的88.8GbpsPDM 双子载波OFDM信号的传输。

