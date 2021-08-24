---
description: >-
  Experimental investigation on the performance of closely spaced multi-carrier
  PDM-QPSK with digital coherent detection
---

# 2009——载波间隔=波特率，CMA：4倍过采样+T/4间隔&gt;2倍+T/2，PDM-QPSK系统

整体的系统为100Gbps双子载波PDM-QPSK，其波特率为12.5GBaud。在满足子载波间隔等于波特率的情况下，3或5子载波PDM-QPSK系统的CMA采用4倍过采样+基于CMA的T/4抽头间隔抽头的数字均衡器＞2倍过采样+基于CMA的T/2间隔抽头。**除此之外，将载波间隔设置为80%的波特率下，损失小于0.001可忽略不计。**12.5\*80%==10Ghz。**最后，说明了如何将2-PDM-QPSK的波特率提高到25GBaud和28GBaud。**

值得注意的是：固有的采样速率为50Gsamples/s的情况下，从12.5GBaud扩展到25GBaud和28GBaud分别会产生2.8dB和4.8dB的额外串扰损失。这表明采样速率和发射机带宽需要提高。

引言：在参考文献【3】中提到：08年提出了一个新技术，两个同步调制的载波以波特率精确地间隔开或在OFDM条件下，目的是使总信道数据速率加倍，同时实现高频谱效率。该文献使用的是两个44.4Ghzbps地PDM-QPSK系统，载波间隔为11.1Ghz。该文章提出之后，该团队又陆续提出了各种出版物，【4】——【6】，其中就有2载波13.9GBaud地载波间隔为波特率的PDM-QPSK，ADC采用速率为50Gsamples/s或过采样为4，相干干扰最小。（该团队好像不是之前研究论文的团队）。

![&#x4EA7;&#x751F;&#x4E24;&#x4E2A;&#x5B50;&#x8F7D;&#x6CE2;&#x7684;&#x4E24;&#x79CD;&#x65B9;&#x6CD5;](../../../.gitbook/assets/image%20%2815%29.png)

第一种就是对每个载波使用独立的激光发射器产生。第二种是采用频率为波特率一半的正弦波驱动，通过MZM，再经过放大，使用载波分离滤波器（CSF）将其分离，可以得到精准的f0-fc和f0+fc的频率的载波。CSF是一个25/50Ghz的de-interleaver。

![&#x53CC;&#x5B50;&#x8F7D;&#x6CE2;&#x8C03;&#x5236;&#x8FC7;&#x7A0B;](../../../.gitbook/assets/image%20%2814%29.png)

PC是偏振控制，保持两组数据是同偏振。两组数据通过放置一个光学延迟来控制延迟，再通过3dB光学耦合器进行组合。PBC将两载波QPSK重新组合来形成2载波PDM-QPSK。

