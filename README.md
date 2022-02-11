# *Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT*

## *交流QQ群：1071120659*


![System Info](https://s2.loli.net/2022/02/11/NE8vqsDHxrnzWhV.png)


### 配置
1. 主板: MSI MPG Z690 EDGE TI WIFI DDR4
1. BIOS版本：7D31vA1
1. CPU: Intel® Core™ i7-12700K 12-Core Processor
1. 核显: Intel® UHD Graphics 770
1. 独显: Yeston Radeon RX 6800 XT SAKURA Edition
1. 板载网卡: Intel® I225V 2.5Gbps LAN controller
1. 内置 WiFi/蓝牙: Intel® Wi-Fi 6E AX210
1. 外置 WiFi/蓝牙: BCM943602CS（BT4.2）
1. 前置面板声卡：Realtek® ALC897 Codec
1. 后置面板声卡：Realtek® ALC4080 Codec
1. 固态硬盘: Western Digital SSD SN850 1TB

### BIOS设置
1. Settings\高级\PCIe/PCI子系统设置：Re-Size BAR Support-允许
2. Settings\高级\整合周边设备：Onboard CNVi Module Control-Disable Integrated
3. Settings\高级\内建显示配置：集成显卡多显示器-禁止
4. Settings\高级\Beta Runner：选择Settings\高级\NVMe SSD Self-Test，选择取消即可进入，选择SR-IOV Support-允许
5. Settings\启动：快速开机-禁止
6. Overclocking\CPU 特征：Intel VT-D技术-允许；CFG锁定-禁止


**可适用操作系统版本：macOS Catalina 12.1～macOS Monterey 12.3 beta1**

1. OpenCore版本：0.7.9 (02-09)
1. CPU变频：正常。
1. UHD770：无法驱动，BIOS屏蔽处理。
1. RX6800XT：正常，原生驱动。

![Graphics Card](https://s2.loli.net/2022/02/09/AdihloJsO9jZcEG.png)

1. 3.5mm声音 & HDMI：均正常使用，使用AppleALC驱动。
1. USB：正常。
1. 有线网卡：正常。
1. 睡眠唤醒：正常。

![Power Saver](https://s2.loli.net/2022/02/09/f5PQ6731X2ukqIU.png)

1. 关机开机：正常。
1. iCloud & App Store & iMessage & FaceTime：请自行生成Board Serial Number、序列号、SmUUID，并相应的修改SysPrameter系统参数中的“自定义UUID”，和RtVariables变量设置中的MLB、ROM。
1. AirDrop & HandOff & Continuity：正常。

![Wi-Fi en1](https://s2.loli.net/2022/02/09/2XrCMNRca15oUYj.png)
![BlueTooth](https://s2.loli.net/2022/02/09/PLTa14XQ53ez7S6.png)
![Apple Watch](https://s2.loli.net/2022/02/09/qPAD1pdlZMU7hux.png)

### Tips：

1. 机型需设定为MAC RPO 7.1（现已预置，安装完成后请自行修改）。
1. 该config默认为无verbose模式。如需启用verbose模式，config.plist需要修改以下一项：NVRAM-Add-7C436110-AB2A-4BBB-A880-FE41995C9F82-boot-args，添加-v。
1. 该config启动盘策略 ScanPolicy 值设置为0。可引导Windows或Other OS（Linux、Unix）如需指定搜索分区类型，可参考OC配置手册。
1. 该config默认为不显示OC Picker菜单。如需开启菜单显示，设置如下：Misc-Boot-ShowPicker 值为true（plist编辑器中为YES）。
1. UTBMap.kext 为我根据主板接线定制，若你出现usb相关错误，可自行定制UTBMap，或取消加载该kext，将XhciPortLimit值变更为true。
1. 虽然内置WIFI/BT模块已经可以通过AirportItlwm.kext、IntelBluetoothFirmware.kext、IntelBluetoothInjector.kext进行驱动并实现上网、接力功能，但因无法隔空投送，故我在BIOS中进行了屏蔽，使用了外置（PCI-E 转接）WIFI/BT模块。如果你想要用内置WIFI/BT模块，可以在以下链接下载kext（[IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases)、[AirportItlwm](https://github.com/OpenIntelWireless/itlwm/releases)），载入到OC中驱动使用。

### 目前已知问题：

1. 无法远程VNC连接此机器（12.2版本存在该问题，12.2.1版本已经可用）
1. RX6000系显卡调用策略有问题，无论是否通过weg驱动，利用率都表现很差（如果有好的解决方案，请通过issue提交给我，谢谢！）

![Boot Camp](https://s2.loli.net/2022/02/09/2pdDMUnsmHl5J4B.png)

![打赏](https://s3.bmp.ovh/imgs/2022/02/518d817d09e604ab.jpg)

