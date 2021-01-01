# IndoorLocation
室内定位



AOA+大致距离



基站

蓝牙芯片-天线-预处理-算法



## 蓝牙芯片

TI、Nordic、NXP

Nordic最准，TI方位角稍次

选型：

TI launchpad CC2640R2 Dev Kit

NORDIC nRF52833-DK

这个好用



The new flagship

nRF5340 SoC

[nRF5340 DK](https://www.nordicsemi.com/Software-and-tools/Development-Kits/nRF5340-DK)



## 天线

现有的：

TI launchpad AOA 2.4GHz BOOSTXL-AoA  

这个不太行，非极化天线

自己设计极化天线，参考[Quuppa](https://quuppa.cn/)的天线设计（日本专利已过期）



通信单独一个

相干效果好一点，同时接受，只测相位

最小二乘拟合

12ch同步，校准，定天线相位中心

## 算法

可以看看滤波等定位算法



## 前期调研

iBeacon工作原理（记得只有信号强度，没有角度）



## 整体路线

初步调研：调研市场，专利，论文。和实验室保持联系。

前期研究：在某一方面申专利，发论文。定位精度朝着20cm量级做，尽可能降低成本

军用合作——Pro：给钱多，推进快	Con：给钱慢（半年-两三年），资金链可能出问题，不好拿投资。需要保密，不能写个人or公司简历。

做自己的蓝牙芯片，专用芯片的研发。