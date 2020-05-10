## 简介

这是一份适用于 Clevo P65xHP 的 Hackintosh EFI 配置，我的机型为 HASEE Z7-KP7D1，故 HASEE Z7-KP7S1 应该也是通用的。

建议使用[黑果小兵](https://blog.daliansky.net/)镜像。

## 说明

### 硬件

机器更换了以下配置：

- 无线网卡：DW1830 BCM943602BAED（会附送一根天线接到最右侧即可）
- 固态硬盘：SAMSUNG PM961
- 显示屏：SHARP SHP1430（10.13 及以上）

**关于显卡**

从 10.13 开始更换了夏普的 SHP1430 屏幕，所以核心显卡部分会不一样，使用[黑果小兵](https://blog.daliansky.net/)镜像中较为纯净的 config.json 配合 Hackintool 驱动核显即可

![屏幕快照](https://i.loli.net/2020/02/05/yaCjYekqdm1tzFh.png)

在完成核显设置后，然后建议使用 [一键开启 macOS HiDPI](https://github.com/xzhih/one-key-hidpi/blob/master/README-zh.md) 再进行一次 EDID 修复，这样「系统偏好设置」中的图标就正常了。

**关于声卡**

本机型号（Realtek ACL892）不需要仿冒，直接使用 AppleALC 并将 Clover 中「Devices」>「Audio」>「Inject」设置为「28」即可声卡和麦克风同时工作。

**关于蓝牙**

DW1830 的蓝牙驱动使用 [BrcmPatchRAM](https://github.com/acidanthera/BrcmPatchRAM/releases)：

- BrcmBluetoothInjector.kext
- BrcmFirmwareData.kext
- BrcmPatchRAM2.kext（10.15 使用 BrcmPatchRAM3.kext）

将以上 3 个文件放置在「/Library/Extensions」

## 已知问题

- HDMI 无法使用（应该是需要独显，但是 macOS Mojave 开始无法驱动 N 卡）
- 拔掉电源后有可能出现暂时的声卡失效，稍等片刻或接回电源再拔出可解决