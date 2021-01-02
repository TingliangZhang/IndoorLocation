# IndoorLocation
室内定位



纠结：

是否需要设计天线（可否用手机本身的天线当基站。不改变原有的硬件，做手机为基站的指向性或距离定位。类似Tile）

精度优先or成本优先（是否要用同步相位测角，提高芯片成本高）



初步方案：

AOA+大致距离



基站

蓝牙芯片-天线-预处理-算法





## 市场调研



Bluetooth SIG 的综述

[How AoA & AoD Changed the Direction of Bluetooth Location Services](https://www.bluetooth.com/blog/new-aoa-aod-bluetooth-capabilities/) BLUETOOTH BLOG

>  [1901_Enhancing-Bluetooth-Location-Service_FINAL.pdf](1901_Enhancing-Bluetooth-Location-Service_FINAL.pdf) 

[New Bluetooth Direction Finding Feature Will Enhance Location Services Solutions](https://www.bluetooth.com/blog/new-direction-finding-feature/)

[Bluetooth is Moving Proximity Solutions in the Right Direction](https://www.bluetooth.com/blog/bluetooth-proximity-solutions/)

[Bluetooth is Getting Precise with Positioning Systems](https://www.bluetooth.com/blog/bluetooth-positioning-systems/)



市场

[2020 Bluetooth Market Update](https://www.bluetooth.com/bluetooth-resources/2020-bmu/?utm_campaign=bmu&utm_source=internal&utm_medium=web&utm_content=2020bmu-resourcepopup)

>  [2020_Market_Update-EN.pdf](2020_Market_Update-EN.pdf) 



案例

Museum with multiple exhibits

[National Gallery of Victoria Enhances Visitor Experience with Bluetooth Location Services](https://www.bluetooth.com/blog/ngv-bluetooth-location-services/)

[Van Gough Museum in Amsterdam](https://blog.bluetooth.com/smart-building-use-cases?utm_campaign=location-services&utm_source=internal&utm_medium=blog&utm_content=bluetooth-proximity-solutions)

Shopper in a store

[Bluetooth Beacons are on **Target** with a Major Retailer](https://www.bluetooth.com/blog/bluetooth-beacons-are-on-target-with-a-major-retailer/)

[How **Mall of America** is Leveraging the Power of Bluetooth Beacons](https://blog.bluetooth.com/mall-of-america?utm_campaign=location-services&utm_source=internal&utm_medium=blog&utm_content=AoA-AoD-direction-finding)

[Gatwick Airport](https://blog.bluetooth.com/a-new-way-to-navigate?utm_campaign=location-services&utm_source=internal&utm_medium=blog&utm_content=bluetooth-positioning-systems)

Item finding solutions

[Tile trackers](https://www.theverge.com/circuitbreaker/2018/10/2/17924312/tile-mate-pro-premium-subscription-launch-battery-range-price)

[Find Your Keys, Wallet & Phone with Tile’s App](https://www.thetileapp.com/en-us/)



品牌：

[Silicon Labs Bluetooth Direction Finding Solution](https://www.silabs.com/products/wireless/learning-center/bluetooth/bluetooth-direction-finding)

>  [ew-2018-understanding-advanced-bluetooth-angle-estimation-techniques-for-real-time-locationing.pdf](ew-2018-understanding-advanced-bluetooth-angle-estimation-techniques-for-real-time-locationing.pdf) 

[Quuppa](http://www.quuppa.com/)

[How Quuppa is Proving the New Direction of Bluetooth Location Services](https://www.bluetooth.com/blog/how-quuppa-is-proving-the-new-direction-of-bluetooth-location-services-and-remote-sensing-and-monitoring/)



技术细节

[Bluetooth Core Specifications](https://www.bluetooth.com/specifications/bluetooth-core-specification/)

> Bluetooth Core Specification Version 5.1 Feature Overview
>
>  [1901_Feature_Overview_Brief_FINAL.pdf](1901_Feature_Overview_Brief_FINAL.pdf) 

## 学习通信电路

[How does an Antenna work? | ICT #4](https://www.youtube.com/watch?v=ZaXm6wau-jc) 



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