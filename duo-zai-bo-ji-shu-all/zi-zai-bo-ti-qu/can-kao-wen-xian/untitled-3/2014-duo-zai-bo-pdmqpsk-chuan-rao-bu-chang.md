---
description: >-
  原作者——Experimental demonstration of crosstalk compensation for super
  high-density multi-carrier PDM-QPSK signal by MIMO processing——2
---

# 2014——双载波PDM-QPSK串扰补偿

两个PDM-QPSK信号可以进行子载波间隔为波特率78%的传输。

多载波传输系统中，例如奈奎斯特WDM系统【1】，是实现100Gbps以上光纤传输的候选系统。该作者之前研究过子载波系统，提出了具有MIMO补偿的多载波传输系统【2】（50bps的信号）。该文章证明了系统对两个128bps的PDM-QPSK的有效性。

![&#x4E24;&#x4E2A;PDM-QPSK&#x4FE1;&#x53F7;&#x7684;&#x63A5;&#x6536;&#x56FE;](../../../../.gitbook/assets/image%20%2835%29.png)

自适应MIMO均衡利用本振光频率间隔补偿PDM子载波之间的串扰。

![&#x5B9E;&#x9A8C;&#x88C5;&#x7F6E;](../../../../.gitbook/assets/image%20%2836%29.png)

子载波间隔设置为18.75、25、32、37.5和50GHZ。采样率为波特率的两倍。T/2间隔的均衡器31个抽头。

![&#x4E0E;&#x5948;&#x594E;&#x65AF;&#x7279;&#x7684;&#x5B9E;&#x9A8C;&#x6BD4;&#x8F83;](../../../../.gitbook/assets/image%20%2837%29.png)

