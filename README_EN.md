# *Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT*

[中文](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README.md)｜[日本語](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README_JP.md)
｜[English](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README_EN.md)

![System Info](https://s2.loli.net/2022/07/25/hD79bWJiNMklTj4.png)


### Configuration
1. Motherboard: MSI MPG Z690 EDGE TI WIFI DDR4
1. BIOS version: 7D31vA4
1. CPU: Intel® Core™ i7-12700K 12-Core Processor
1. Core Graphics: Intel® UHD Graphics 770
1. Standalone: ​​Yeston Radeon RX 6800 XT SAKURA Edition
1. Onboard LAN: Intel® I225V 2.5Gbps LAN controller
1. Built-in WiFi/Bluetooth: Intel® Wi-Fi 6 AX201
1. External WiFi/Bluetooth: BCM943602CS (BT4.2)
1. Front panel sound card: Realtek® ALC897 Codec
1. Rear panel sound card: Realtek® ALC4080 Codec
1. Solid State Drive: Western Digital SSD SN850 1TB

### BIOS settings
1. Settings\Advanced\PCIe/PCI Subsystem Settings: Re-Size BAR Support-Enable
2. Settings\Advanced\Integrated Peripherals: Onboard CNVi Module Control-Disable Integrated
3. Settings\Advanced\Integrated Graphics Configuration: Integrated Graphics Multi-Monitor - Disabled
4. Settings\Beta Runner: SR-IOV Support-Enable
5. Settings\Startup: Fast Boot-Disable; Post Screen Delay-Enable:
6. Settings\Security: Secure Boot - Disable
7. Overclocking\CPU Feature: CFG Lock-Disabled

**Applicable OS version: macOS Catalina 12.1～macOS Monterey 13.0 Beta3**

1. OpenCore version: 0.8.3 (07-24)
1. CPU frequency conversion: Work.
![geekbench](https://s2.loli.net/2022/06/13/vaGD3hfLCPKyoWj.png)
![cinebench](https://s2.loli.net/2022/06/13/TRtelkENgL1po3w.png)
1. UHD770: Unable to drive, BIOS shield processing.
1. RX6800XT: Work, native driver.

![Graphics Card](https://s2.loli.net/2022/07/25/IQXPB19CTHoJmcu.png)
![luxmark](https://s2.loli.net/2022/06/13/LgwxrvnWoph5fG6.png)
![gb opencl](https://s2.loli.net/2022/06/13/RTPGSE2O18n3Bf4.png)
![gb metal](https://s2.loli.net/2022/06/13/AYNQjR6FtUkhcCH.png)

1. 3.5mm sound & HDMI: Work, using AppleALC driver.
1. USB: Work.
1. Wired network card: theoretically Work (not tested).
1. Sleep & Wake up: Work.

![Power Saver](https://s2.loli.net/2022/06/13/7s6Ujidx2kOuNeI.png)

1. Power off and on: Work.
1. iCloud & App Store & iMessage & FaceTime: Please generate the Board Serial Number, Serial Number, SmUUID by yourself, and modify the "Custom UUID" in the SysPrameter system parameters, and the MLB and ROM in the RtVariables variable settings accordingly.
1. AirDrop & HandOff & Continuity: Work.


![Wi-Fi en1](https://s2.loli.net/2022/06/13/iOyQp4lwjPUYzb5.png)
![BlueTooth](https://s2.loli.net/2022/06/13/X8wAmyiP2YfzMBc.png)
![Apple Watch](https://s2.loli.net/2022/06/13/DNup3iCf1nJ49Zr.png)

### Tips:

1. The model needs to be set to MAC RPO 7.1 (it is already preset, please modify it after the installation is complete).
1. The config defaults to no verbose mode. To enable verbose mode, config.plist needs to modify the following one: NVRAM-Add-7C436110-AB2A-4BBB-A880-FE41995C9F82-boot-args, add -v.
1. The config startup disk policy ScanPolicy value is set to 0. Bootable Windows or Other OS (Linux, Unix) To specify the search partition type, please refer to the OC configuration manual.
1. This config does not display the OC Picker menu by default. To enable menu display, set as follows: Misc-Boot-ShowPicker is true (YES in plist editor).
1. UTBMap.kext is customized for me according to the motherboard wiring. If you have usb-related errors, you can customize UTBMap by yourself, or cancel the loading of the kext, and change the XhciPortLimit value to true.
1. Although the built-in WIFI/BT module can already be driven by AirportItlwm.kext, IntelBluetoothFirmware.kext, IntelBluetoothInjector.kext to realize Internet access and relay functions, but because it cannot be air-dropped, I shielded it in the BIOS and used an external (PCI-E transfer) WIFI/BT module. If you want to use the built-in WIFI/BT module, you can download kext from the following links （[IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases)、[AirportItlwm](https://github.com/OpenIntelWireless/itlwm/releases)）, loaded into the OC driver for use.

### Currently known issues:

1. There is a problem with the calling strategy of the RX6000 series graphics card. Whether it is driven by weg or not, the utilization rate is very poor (if there is a good solution, please submit it to me through issue, thank you!)
1. The Apple Watch unlocking function cannot be unlocked in Ventura beta3 (myself example cannot represent all).


![Boot Camp](https://s2.loli.net/2022/06/13/xAI8DQGXvZyFqwS.png)

**Donate:**[https://paypal.me/kenshinJP](https://paypal.me/kenshinJP)


[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/kenshinJP)
