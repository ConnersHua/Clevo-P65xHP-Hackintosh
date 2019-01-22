## 简介

这是一份适用于 Clevo P65xHP 的 Hackintosh EFI 配置，我的机型为 HASEE Z7-KP7D1，故 HASEE Z7-KP7S1 应该也是通用的。

## 说明

### 硬件

机器更换了以下配置：

- 无线网卡：DW1830 BCM943602BAED(会附送一根天线接到最右侧即可)
- 固态硬盘：SAMSUNG PM961
- 显示屏：SHARP SHP1430（仅 10.13）

### 其他

Extra 目录下的文件均需要使用 [Kext Utility](http://cvad-mac.narod.ru/index/0-4) 安装。

**关于显卡**

10.13 因为我换了夏普的 SHP1430，所以核心显卡部分会不一样，如果你使用原装屏幕需基于 10.12 的版本做升级到 10.13 亦可。另外因为是高分屏为了完美开启 Hi-DPI 所以还需要使用[一键开启 macOS HiDPI](https://github.com/xzhih/one-key-hidpi/blob/master/README-zh.md)。

双显卡工作，VideoProc 中检测「H264」及「HEVC」显示激活，Photoshop 中「性能」中「图形处理器设置」检测为「Intel(R) HD Graphic 630」。

**关于声卡**

声卡偶发开机无法正常工作，重启即可。此类型号建议将 Clover 中「Devices」下「Audio」的「Inject」设置为「28」即可声卡和麦克风同时工作。

其他使用未见异常，基本完美。