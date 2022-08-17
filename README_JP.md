# *Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT*

[中文](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README.md)｜[日本語](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README_JP.md)
｜[English](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README_EN.md)

![System Info](https://s2.loli.net/2022/07/25/hD79bWJiNMklTj4.png)


### 構成
1. マザーボード：MSI MPG Z690 EDGE TI WIFI DDR4
1. BIOSバージョン：7D31vA7
1. CPU：Intel® Core™ i7-12700K 12-Core Processor
1. コアグラフィックス：Intel® UHD Graphics 770
1. スタンドアロン：YestonRadeon RX 6800 XT SAKURA Edition
1. オンボードLAN：Intel® I225V 2.5Gbps LAN controlle
1. 内蔵WiFi/Bluetooth：Intel® Wi-Fi 6 AX201
1. 外部WiFi/Bluetooth：BCM943602CS（BT4.2）
1. フロントパネルサウンドカード：Realtek® ALC897 Codec
1. リアパネルサウンドカード：Realtek® ALC4080 Codec
1. ソリッドステートドライブ：Western Digital SSD SN850 1TB

### BIOS設定
1. Settings\Advanced\PCIe/PCI Subsystem Settings: Re-Size BAR Support-Enable
2. Settings\Advanced\Integrated Peripherals: Onboard CNVi Module Control-Disable Integrated
3. Settings\Advanced\Integrated Graphics Configuration: Integrated Graphics Multi-Monitor - Disabled
4. Settings\Beta Runner: SR-IOV Support-Enable
5. Settings\Startup: Fast Boot-Disable; Post Screen Delay-Enable:
6. Settings\Security: Secure Boot - Disable
7. Overclocking\CPU Feature: CFG Lock-Disabled

**該当するOSバージョン：macOS Catalina 12.1〜macOS Monterey 13.0 Beta5 **

1. OpenCoreバージョン：0.8.4 (08-17)
1. CPU周波数変換：正常。
![geekbench](https://s2.loli.net/2022/06/13/vaGD3hfLCPKyoWj.png)
![cinebench](https://s2.loli.net/2022/06/13/TRtelkENgL1po3w.png)
1. UHD770：駆動できません。BIOSシールド処理。
1. RX6800XT：正常。

![Graphics Card](https://s2.loli.net/2022/07/25/IQXPB19CTHoJmcu.png)
![luxmark](https://s2.loli.net/2022/06/13/LgwxrvnWoph5fG6.png)
![gb opencl](https://s2.loli.net/2022/06/13/RTPGSE2O18n3Bf4.png)
![gb metal](https://s2.loli.net/2022/06/13/AYNQjR6FtUkhcCH.png)

1. 3.5mmサウンドとHDMI：どちらも正常、AppleALCドライバーを使用して使用されます。
1. USB：正常。
1. 有線ネットワークカード：理論的には正常です（テストされていません）。
1. 睡眠：正常。

![Power Saver](https://s2.loli.net/2022/06/13/7s6Ujidx2kOuNeI.png)

1. 電源のオフとオン：正常。
1. iCloud＆App Store＆iMessage＆FaceTime：ボードのシリアル番号、シリアル番号、SmUUIDを自分で生成し、SysPrameterシステムパラメーターの「カスタムUUID」と、それに応じてRtVariables変数設定のMLBとROMを変更してください。
1. AirDrop＆HandOff＆Continuity：正常。

![Wi-Fi en1](https://s2.loli.net/2022/06/13/iOyQp4lwjPUYzb5.png)
![BlueTooth](https://s2.loli.net/2022/06/13/X8wAmyiP2YfzMBc.png)
![Apple Watch](https://s2.loli.net/2022/06/13/DNup3iCf1nJ49Zr.png)

### チップ：

1. モデルをMACRPO7.1に設定する必要があります（すでにプリセットされています。インストールが完了したら変更してください）。
1. 構成のデフォルトは冗長モードなしです。詳細モードを有効にするには、config.plistで次のモードを変更する必要があります：NVRAM-Add-7C436110-AB2A-4BBB-A880-FE41995C9F82-boot-args、add-v。
1. 構成起動ディスクポリシーのScanPolicy値が0に設定されます。起動可能なWindowsまたはその他のOS（Linux、Unix）検索パーティションの種類を指定するには、OC構成マニュアルを参照してください。
1. この設定では、デフォルトではOCPickerメニューは表示されません。メニュー表示を有効にするには、次のように設定します。Misc-Boot-ShowPickerがtrue（plistエディターでYES）。
1. UTBMap.kextは、マザーボードの配線に応じてカスタマイズされています。USB関連のエラーがある場合は、UTBMapを自分でカスタマイズするか、kextの読み込みをキャンセルして、XhciPortLimit値をtrueに変更できます。
1. 内蔵のWIFI/BTモジュールはAirportItlwm.kext、IntelBluetoothFirmware.kext、IntelBluetoothInjector.kextですでに駆動でき、インターネットアクセスとリレー機能を実現できますが、エアドロップできないため、BIOSでシールドしました。外部（PCI-E転送）WIFI/BTモジュールを使用しました。組み込みのWIFI/BTモジュールを使用する場合は、次のリンク（[IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases)、[AirportItlwm](https://github.com/OpenIntelWireless/itlwm/releases)）、使用するためにOpencoreドライバーにロードされます。

### 現在知られている問題：

1. RX6000シリーズグラフィックカードの通話戦略に問題があります。ウェグで駆動されているかどうかに関係なく、使用率は非常に低くなっています（適切な解決策がある場合は、問題を通じて提出してください。ありがとうございます。 ！）
1. Apple Watchのロック解除機能はVenturabeta3ではロック解除できません（自分の例ですべてを表すことはできません）。


![Boot Camp](https://s2.loli.net/2022/06/13/xAI8DQGXvZyFqwS.png)

**Donate:**[https://paypal.me/kenshinJP](https://paypal.me/kenshinJP)


[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/kenshinJP)
