# *Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT*

[中文](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README.md)｜[日本語](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README_JP.md)
｜[English](https://github.com/igarashikenshin/Hackintosh-MSI-Z690-EDGE-TWD4_i7-12700K_RX6800XT/blob/main/README_EN.md)

![System Info](https://s2.loli.net/2024/03/03/5HVdtn97mGwBaMu.png)


### 構成
1. マザーボード：MSI MPG Z690 EDGE TI WIFI DDR4
1. BIOSバージョン：7D31vAG
1. CPU：Intel® Core™ i7-12700K 12-Core Processor
1. コアグラフィックス：Intel® UHD Graphics 770
1. スタンドアロン：YestonRadeon RX 6800 XT SAKURA Edition
1. オンボードLAN：Intel® I225V 2.5Gbps LAN controlle
1. 内蔵WiFi/Bluetooth：BCM943602CS（BT4.2）
1. フロントパネルサウンドカード：Realtek® ALC897 Codec
1. リアパネルサウンドカード：Realtek® ALC4080 Codec
1. ソリッドステートドライブ：Western Digital SSD SN850 1TB

### BIOS設定
1. SR-IOV Support:[有効］
2. Fast Boot:[無効]
3. Secure Boot:[無效]
4. D.T.M: [有効]

**該当するOSバージョン：macOS Catalina 12.1〜macOS Monterey 14.4 RC **

1. OpenCoreバージョン：0.9.9 (03-02)
1. CPU周波数変換：正常。
![geekbench6](https://s2.loli.net/2023/06/19/6Wbvf9dog5K7SwB.png)
![cinebench](https://s2.loli.net/2023/06/19/CBetHYmy1RIanFS.png)
1. UHD770：駆動できません。BIOSシールド処理。
1. RX6800XT：正常。

![Graphics Card](https://s2.loli.net/2023/06/19/DYcQ9q1nNiM4PE6.png)
![luxmark](https://s2.loli.net/2023/06/19/T2QaOfgnqC8rSsG.png)
![gb opencl](https://s2.loli.net/2023/06/19/U1rCegOkSd4AGZJ.png)
![gb metal](https://s2.loli.net/2023/06/19/GmXQZcosb3FxPtJ.png)

1. 3.5mm オーディオと HDMI: AppleALC ドライバーを使用して、両方とも正常に動作します。
2. USB: OK。
3. 有線ネットワークカード: 正常。
4. Wi-Fi: OpenCore-Patcher を使用して。
5. スリープ: 正常。

![Power Saver](https://s2.loli.net/2023/06/19/DlKsPrtFmwVfEqU.png)

1. 電源のオフとオン：正常。
2. iCloud＆App Store＆iMessage＆FaceTime：ボードのシリアル番号、シリアル番号、SmUUIDを自分で生成し、SysPrameterシステムパラメーターの「カスタムUUID」と、それに応じてRtVariables変数設定のMLBとROMを変更してください。
3. AirDrop: 正常。
4. HandOff: 正常。
5. Continuity: 正常。
6. Apple Watch Unlock: 正常。

![Wi-Fi en1](https://s2.loli.net/2023/06/19/B5Gkdyuxq2aLpnN.png)
![BlueTooth](https://s2.loli.net/2023/06/19/KDIOSrLo2sQgb9a.png)
![Apple Watch](https://s2.loli.net/2023/06/19/wW8C5gl4HTyEGcD.png)

### チップ：

1. モデルは MAC RPO 7.1 に設定する必要があります (プリセット。インストール後に変更してください)。
1. 設定のデフォルトは冗長モードではありません。 詳細モードを有効にするには、config.plist で項目 NVRAM-Add-7C436110-AB2A-4BBB-A880-FE41995C9F82-boot-args を変更し、-v を追加する必要があります。
1. 構成ブート ディスク ポリシーの ScanPolicy 値は 0 に設定されます。 Windowsまたはその他のOS(Linux、Unix)の起動が可能ですが、検索パーティションの種類を指定する必要がある場合は、OC構成マニュアルを参照してください。
1. デフォルトでは、OC Picker メニューは表示されません。 メニュー表示を有効にするには、次のように設定します。 Misc-Boot-ShowPicker が true (plist エディターでは YES) です。
1. UTBMap.kext はマザーボードの配線に従ってカスタマイズされていますが、USB 関連のエラーがある場合は、UTBMap を自分でカスタマイズするか、kext をアンロードして、XhciPortLimit の値を true に変更します。

### 現在知られている問題：

1. RX6000シリーズグラフィックカードの通話戦略に問題があります。ウェグで駆動されているかどうかに関係なく、使用率は非常に低くなっています（適切な解決策がある場合は、問題を通じて提出してください。ありがとうございます。 ！）


![Boot Camp](https://s2.loli.net/2022/06/13/xAI8DQGXvZyFqwS.png)

**Donate:**[https://paypal.me/kenshinJP](https://paypal.me/kenshinJP)


[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/kenshinJP)
