### 简介

这是一份适用于 Clevo P65xHP 的 Hackintosh EFI 配置，我的机型为 HASEE Z7-KP7D1，故 HASEE Z7-KP7S1 应该也是通用的。

目前在 macOS Sierra 10.12.6 测试基本完美。

### 说明

**关于硬件**

机器更换了以下配置：

- 无线网卡：DW1830 BCM943602BAED
- 固态硬盘：SAMSUNG PM961

以上硬件都是完美兼容原生免驱的，特别说明 DW1830 会附送一根天线接到最右侧即可，否则 5G 可能会出现能搜索但是连不上的情况。

**关于其他**

需要 AppleIntelSKLGraphicsFramebuffer.kext，使用 [Kext Utility](http://cvad-mac.narod.ru/index/0-4) 安装。

EFI 已经开启 nvda_drv，所以替换后记得安装 NVIDIA CUDA Driver for MAC 以及 NVIDIA WebDriver 重启即可。
