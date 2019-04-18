## 简介

这是一份适用于 Clevo P65xHP 的 Hackintosh EFI 配置，我的机型为 HASEE Z7-KP7D1，故 HASEE Z7-KP7S1 应该也是通用的。

## 说明

### 硬件

机器更换了以下配置：

- 无线网卡：DW1830 BCM943602BAED（会附送一根天线接到最右侧即可）
- 固态硬盘：SAMSUNG PM961
- 显示屏：SHARP SHP1430（10.13 及以上）

**关于显卡**

从 10.13 开始更换了夏普的 SHP1430 屏幕，所以核心显卡部分会不一样，可使用[黑果小兵](https://blog.daliansky.net/)镜像中较为纯净的 `config.list` 配合 Hackintool 驱动核显会达到一个很完美的效果。

VideoProc 中检测「H264」及「HEVC」显示激活，Photoshop 中「性能」中「图形处理器设置」检测为「Intel(R) HD Graphic 630」。

**关于声卡**

此类型号（Realtek ACL892）建议将 Clover 中「Devices」下「Audio」的「Inject」设置为「31」即可声卡和麦克风同时工作。

其他使用未见异常，基本完美。