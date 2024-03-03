# *Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT*

[中文](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README.md)｜[日本語](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README_JP.md)
｜[English](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README_EN.md)

![System Info](https://s2.loli.net/2024/03/03/5HVdtn97mGwBaMu.png)


### Configuration
1. Motherboard: MSI MPG Z690 EDGE TI WIFI DDR4
1. BIOS version: 7D31vAG
1. CPU: Intel® Core™ i7-12700K 12-Core Processor
1. Core Graphics: Intel® UHD Graphics 770
1. Standalone: ​​Yeston Radeon RX 6800 XT SAKURA Edition
1. Onboard LAN: Intel® I225V 2.5Gbps LAN controller
1. Built-in WiFi/Bluetooth: BCM943602CS（BT4.2）
1. Front panel sound card: Realtek® ALC897 Codec
1. Rear panel sound card: Realtek® ALC4080 Codec
1. Solid State Drive: Western Digital SSD SN850 1TB

### BIOS settings
1. SR-IOV Support: [Enabled]
2. Fast Boot: [Disabled]
3. Secure Boot: [Disabled]
4. D.T.M: [Enabled]


**Applicable OS version: macOS Catalina 12.1～macOS Monterey 14.4 RC**

1. OpenCore version: 0.9.9 (03-02)
1. CPU frequency conversion: Work.
![geekbench6](https://s2.loli.net/2023/06/19/6Wbvf9dog5K7SwB.png)
![cinebench](https://s2.loli.net/2023/06/19/CBetHYmy1RIanFS.png)
1. UHD770: Unable to drive, BIOS shield processing.
1. RX6800XT: Work, native driver.

![Graphics Card](https://s2.loli.net/2023/06/19/DYcQ9q1nNiM4PE6.png)
![luxmark](https://s2.loli.net/2023/06/19/T2QaOfgnqC8rSsG.png)
![gb opencl](https://s2.loli.net/2023/06/19/U1rCegOkSd4AGZJ.png)
![gb metal](https://s2.loli.net/2023/06/19/GmXQZcosb3FxPtJ.png)

1. 3.5mm sound & HDMI: Work, using AppleALC driver.
2. USB: Work.
3. Wired network card: Work.
4. Wi-Fi: Use OpenCore-Patcher to driver.
5. Wake up from sleep: normal.

![Power Saver](https://s2.loli.net/2023/06/19/DlKsPrtFmwVfEqU.png)

1. Power off and on: Work.
2. iCloud & App Store & iMessage & FaceTime: Please generate the Board Serial Number, Serial Number, SmUUID by yourself, and modify the "Custom UUID" in the SysPrameter system parameters, and the MLB and ROM in the RtVariables variable settings accordingly.
3. AirDrop: work.
4. HandOff: work.
5. Continuity: work.
6. Apple Watch Unlock: work.


![Wi-Fi en1](https://s2.loli.net/2023/06/19/B5Gkdyuxq2aLpnN.png)
![BlueTooth](https://s2.loli.net/2023/06/19/KDIOSrLo2sQgb9a.png)
![Apple Watch](https://s2.loli.net/2023/06/19/wW8C5gl4HTyEGcD.png)

### Tips:

1. The model needs to be set to MAC RPO 7.1 (it is already preset, please modify it after the installation is complete).
1. The config defaults to no verbose mode. To enable verbose mode, config.plist needs to modify the following one: NVRAM-Add-7C436110-AB2A-4BBB-A880-FE41995C9F82-boot-args, add -v.
1. The config startup disk policy ScanPolicy value is set to 0. Bootable Windows or Other OS (Linux, Unix) To specify the search partition type, please refer to the OC configuration manual.
1. This config does not display the OC Picker menu by default. To enable menu display, set as follows: Misc-Boot-ShowPicker is true (YES in plist editor).
1. UTBMap.kext is customized for me according to the motherboard wiring. If you have usb-related errors, you can customize UTBMap by yourself, or cancel the loading of the kext, and change the XhciPortLimit value to true.

### Currently known issues:

1. There is a problem with the calling strategy of the RX6000 series graphics card. Whether it is driven by weg or not, the utilization rate is very poor (if there is a good solution, please submit it to me through issue, thank you!)

![Boot Camp](https://s2.loli.net/2023/06/19/UpB186T3roGHkXJ.png)

**Donate:**[https://paypal.me/kenshinJP](https://paypal.me/kenshinJP)


[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/kenshinJP)
