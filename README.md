# *Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT*

## *交流QQ群：1071120659*

[中文](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README.md)｜[日本語](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README_JP.md)
｜[English](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README_EN.md)


![System Info](https://s2.loli.net/2023/06/19/JTV5tpZiK8vXCFg.png)


### 配置
1. 主板: MSI MPG Z690 EDGE TI WIFI DDR4
1. BIOS版本：7D31vAC
1. CPU: Intel® Core™ i7-12700K 12-Core Processor
1. 核显: Intel® UHD Graphics 770
1. 独显: Yeston Radeon RX 6800 XT SAKURA Edition
1. 板载网卡: Intel® I225V 2.5Gbps LAN controller
1. 内置 WiFi/蓝牙: Intel® Wi-Fi 6 AX201
1. 前置面板声卡：Realtek® ALC897 Codec
1. 后置面板声卡：Realtek® ALC4080 Codec
1. 固态硬盘: Western Digital SSD SN850 1TB

### BIOS设置
1. SR-IOV Support:[允许]
2. 快速开机:[禁止]
3. 安全启动：[禁止]
4. 集成显卡多显示器：禁止]
5. D.T.M:[允许]

**可适用操作系统版本：macOS Catalina 12.1～macOS Monterey 14.0 Beta1**

1. OpenCore版本：0.9.4 (06-18)
1. CPU变频：正常。
![geekbench6](https://s2.loli.net/2023/06/19/6Wbvf9dog5K7SwB.png)
![cinebench](https://s2.loli.net/2023/06/19/CBetHYmy1RIanFS.png)
1. UHD770：无法驱动，BIOS屏蔽处理。
1. RX6800XT：正常，原生驱动。

![Graphics Card](https://s2.loli.net/2023/06/19/DYcQ9q1nNiM4PE6.png)
![luxmark](https://s2.loli.net/2023/06/19/T2QaOfgnqC8rSsG.png)
![gb opencl](https://s2.loli.net/2023/06/19/U1rCegOkSd4AGZJ.png)
![gb metal](https://s2.loli.net/2023/06/19/GmXQZcosb3FxPtJ.png)

1. 3.5mm声音 & HDMI：均正常使用，使用AppleALC驱动。
2. USB：正常。
3. 有线网卡：正常。
4. Wi-Fi：使用itlwm.kext模拟有线网卡驱动，需要搭配HeliPort.app使用。
5. 睡眠唤醒：正常。

![Power Saver](https://s2.loli.net/2023/06/19/DlKsPrtFmwVfEqU.png)

1. 关机开机：正常。
2. iCloud & App Store & iMessage & FaceTime：请自行生成Board Serial Number、序列号、SmUUID，并相应的修改SysPrameter系统参数中的“自定义UUID”，和RtVariables变量设置中的MLB、ROM。
3. AirDrop:因模拟有线网卡的形式驱动，无法工作。
4. HandOff:正常。
5. Continuity：无法工作。
6. Apple Watch解锁：需要Wi-Fi及蓝牙同时打开才可使用（暂无法实现）。

![Wi-Fi en5](https://s2.loli.net/2023/06/19/B5Gkdyuxq2aLpnN.png)
![BlueTooth](https://s2.loli.net/2023/06/19/KDIOSrLo2sQgb9a.png)
![Apple Watch](https://s2.loli.net/2023/06/19/wW8C5gl4HTyEGcD.png)

### Tips：

1. 机型需设定为MAC RPO 7.1（现已预置，安装完成后请自行修改）。
1. 该config默认为无verbose模式。如需启用verbose模式，config.plist需要修改以下一项：NVRAM-Add-7C436110-AB2A-4BBB-A880-FE41995C9F82-boot-args，添加-v。
1. 该config启动盘策略 ScanPolicy 值设置为0。可引导Windows或Other OS（Linux、Unix）如需指定搜索分区类型，可参考OC配置手册。
1. 该config默认为不显示OC Picker菜单。如需开启菜单显示，设置如下：Misc-Boot-ShowPicker 值为true（plist编辑器中为YES）。
1. UTBMap.kext 为我根据主板接线定制，若你出现usb相关错误，可自行定制UTBMap，或取消加载该kext，将XhciPortLimit值变更为true。


### 目前已知问题：

1. RX6000系显卡调用策略有问题，无论是否通过weg驱动，利用率都表现很差（如果有好的解决方案，请通过issue提交给我，谢谢！）


![Boot Camp](https://s2.loli.net/2023/06/19/UpB186T3roGHkXJ.png)

![打赏](https://s3.bmp.ovh/imgs/2022/02/518d817d09e604ab.jpg)

