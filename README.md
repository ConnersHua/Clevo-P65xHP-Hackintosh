### 简介

这是一份适用于 Clevo P65xHP 的 Hackintosh EFI 配置，我的机型为 HASEE Z7-KP7D1，故 HASEE Z7-KP7S1 应该也是通用的。

### 说明

**关于硬件**

关于机器本身我换了以下配置：

- 无线网卡：DW1830 BCM943602BAED
- 固态硬盘：SAMSUNG PM961

以上硬件都是完美兼容原生免驱的，特别说明 DW1830 会附送一根天线接到最右侧即可，否则 5G 可能会出现能搜索但是连不上的情况。

**关于其他**

需要 AppleIntelSKLGraphicsFramebuffer.kext，使用 Kext Utility 安装即可。