---
description: >-
  ICI Mitigation for Dual-Carrier Superchannel Transmission Based on m-PSK and
  m-QAM Formats
---

# 2016——双载波信道ICI抑制方案

使用改进的基于DD-LMS（decision directed least mean square）的MIMO处理。对于PDM-m-PSK和PDM-m-QAM格式，可以实现偏振解复用和ICI同时缓解。

引言：双载波超信道传输成为满足400G高SE传输要求的一种有吸引力的方法【1】——【5】.512Gbps双载波PDM-16QM在100Ghz带宽内实现传输734KM【1】，在RZ编码和光学滤波的帮助下，448Gbps的双载波PDM-16QAM在75Ghz带宽下成果传输678KM【2】，在奈奎斯特脉冲整型的应用下，512Gbps的双载波PDM-16QAM在75Ghz带宽内实现了传输630KM【3】，500Gbps双载波PDM-32QAM在75Ghz带宽内传输820KM【4】.奈奎斯特整形技术可以在理论上改善无ICI的SE【5】——【7】。但现实中由于非理想矩形滤波和频率偏移，奈奎斯特WDM信号仍可能遭受ICI。故使用ICI缓解技术的超密集多载波传输成为实现高SE的替代方法【8】——【14】.其中 ，最大后验检测MAP【8】，多级连续干扰消除M-SIC【9】和基于最小均方LMS或恒模算法CMA的自适应均衡器【10】——【14】.基于LMS的是【10】又可能降低FOC和CPE。基于CMA的可实现偏振解复用和ICI缓解【11】【12】，该方法被定义为FD-MIMO（频率分集MIMO）【13】然后将FD-MIMO扩展到PDM-16QAM【14】.

本文：使用LMS对双子载波PDM-16QAM同时实现偏振解复用和ICI解串扰。

色散补偿后，两载波通过带通滤波器分离，然后以每个符号两个样本对其重采样，由两个子载波的两个偏振分量组成的四个信号被引入提出的4×4MIMO自适应均衡器中。

