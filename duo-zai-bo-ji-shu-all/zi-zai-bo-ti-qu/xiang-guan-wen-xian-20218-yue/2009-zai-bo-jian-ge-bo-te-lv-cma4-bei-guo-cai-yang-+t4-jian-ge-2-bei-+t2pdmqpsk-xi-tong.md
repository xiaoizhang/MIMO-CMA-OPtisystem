---
description: >-
  Experimental investigation on the performance of closely spaced multi-carrier
  PDM-QPSK with digital coherent detection
---

# 2009——载波间隔=波特率，CMA：4倍过采样+T/4间隔&gt;2倍+T/2，PDM-QPSK系统

整体的系统为100Gbps双子载波PDM-QPSK，其波特率为12.5GBaud。在满足子载波间隔等于波特率的情况下，3或5子载波PDM-QPSK系统的CMA采用4倍过采样+基于CMA的T/4抽头间隔抽头的数字均衡器＞2倍过采样+基于CMA的T/2间隔抽头。**除此之外，将载波间隔设置为80%的波特率下，损失小于0.001可忽略不计。**12.5\*80%==10Ghz。**最后，说明了如何将2-PDM-QPSK的波特率提高到25GBaud和28GBaud。**

值得注意的是：固有的采样速率为50Gsamples/s的情况下，从12.5GBaud扩展到25GBaud和28GBaud分别会产生2.8dB和4.8dB的额外串扰损失。这表明采样速率和发射机带宽需要提高。

引言：在参考文献【3】中提到：08年提出了一个新技术，两个同步调制的载波以波特率精确地间隔开或在OFDM条件下，目的是使总信道数据速率加倍，同时实现高频谱效率。该文献使用的是两个44.4Ghzbps地PDM-QPSK系统，载波间隔为11.1Ghz。该文章提出之后，该团队又陆续提出了各种出版物，【4】——【6】，其中就有2载波13.9GBaud地载波间隔为波特率的PDM-QPSK，ADC采用速率为50Gsamples/s或过采样为4，相干干扰最小。（该团队好像不是之前研究论文的团队）。

可以收藏一波发送接收装备的图，明天吧，看懂之后。



