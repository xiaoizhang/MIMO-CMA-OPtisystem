---
description: >-
  ICI Mitigation for Dual-Carrier Superchannel Transmission Based on m-PSK and
  m-QAM Formats
---

# 2016——双载波信道ICI抑制方案

使用改进的基于DD-LMS（decision directed least mean square）的MIMO处理。对于PDM-m-PSK和PDM-m-QAM格式，可以实现偏振解复用和ICI同时缓解。

引言：双载波超信道传输成为满足400G高SE传输要求的一种有吸引力的方法【1】——【5】.512Gbps双载波PDM-16QM在100Ghz信道载波间隔内实现传输734KM【1】，在RZ编码和光学滤波的帮助下，448Gbps的双载波PDM-16QAM在75Ghz信道载波间隔下成果传输678KM【2】，在奈奎斯特脉冲整型的应用下，512Gbps的双载波PDM-16QAM在75Ghz信道载波间隔实现了传输630KM【3】，500Gbps双载波PDM-32QAM在75Ghz信道载波间隔下传输820KM【4】.奈奎斯特整形技术可以在理论上改善无ICI的SE【5】——【7】。但现实中由于非理想矩形滤波和频率偏移，奈奎斯特WDM信号仍可能遭受ICI。故使用ICI缓解技术的超密集多载波传输成为实现高SE的替代方法【8】——【14】.其中 ，最大后验检测MAP【8】，多级连续干扰消除M-SIC【9】和基于最小均方LMS或恒模算法CMA的自适应均衡器【10】——【14】.基于LMS的是【10】又可能降低FOC和CPE。基于CMA的可实现偏振解复用和ICI缓解【11】【12】，该方法被定义为FD-MIMO（频率分集MIMO）【13】然后将FD-MIMO扩展到PDM-16QAM【14】.

本文：使用LMS对双子载波PDM-16QAM同时实现偏振解复用和ICI解串扰。

四电信号输出由ADC采样，并通过I/Q补偿和归一化来实现。ADC采样率为载波信号速率的2.5倍。色散补偿后，两载波通过带通滤波器分离，然后以每个符号两个样本对其重采样，由两个子载波的两个偏振分量组成的四个信号被引入提出的4×4MIMO自适应均衡器中。工作在T/2抽头的自适应均衡器有两个阶段，第一阶段，处于预收敛的目的，CMA具有19个抽头，预收敛之后，完成频偏估计；第二阶段，基于DD-LMS，通过在迭代循环中增加额外的频率偏移操作进行修改。频偏补偿和频移操作一起实施，之后具有32个测试相位的BPS算法进行载波相位恢复。BPS和DD-LMS可共享一个判决，且判决之前该MIMO算法对调制格式不敏感，自适应均衡器可切换相应的调制格式。判决结果可以反馈给均衡器，用于计算函数误差函数和更新抽头系数。

![](../../../.gitbook/assets/image%20%2823%29.png)

4×4 DD-LMS算法由19个抽头系数和T/2个间隔的FIR实现。

下图显示了现有的针对PDM-QPSK格式的基于DD-LMS的ICI缓解方案。【11】

![&#x53C2;&#x8003;&#x6587;&#x732E;&#x3010;11&#x3011;](../../../.gitbook/assets/image%20%2826%29.png)

本文结构有所改变，因此性能优越于上图。

![&#x4E09;&#x8DEF;10GBaudPDM-16QAM&#x4F20;&#x8F93;&#x56FE;&#xFF08;&#x5149;&#x8C31;&#x4E0D;&#x592A;&#x51C6;&#xFF09;](../../../.gitbook/assets/image%20%2828%29.png)

![&#x4E0A;&#x56FE;&#x7684;&#x5149;&#x8C31;&#x56FE;](../../../.gitbook/assets/image%20%2827%29.png)

三路160GbpsPDM-16QAM信号传输了640KM，两个子载波间距10Ghz，载波之间间距25Ghz。

