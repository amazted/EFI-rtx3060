# 适用于msi B760 + nvidia RTX3060驱动macos 26 Tahoe

## 构建启动盘
1. 使用[nullmoth](https://github.com/nullmoth/1401)的1401工具构建启动盘
2. 引导安装后：
   - 格式化磁盘
   - recovery恢复系统（请插上网线，需要下载）

## 启动后存在以下问题
- 显卡未驱动
- wifi无法开启
- 声卡无法驱动


### 显卡
- 在mac桌面运行[nvidia-macos-driver](https://github.com/nullmoth/nvidia-macos-driver/releases)工具,一路下一步

### 声卡
- 根据chris111大佬的仓库guide，运行[VoodooHDA-Tahoe](https://github.com/chris1111/VoodooHDA-Tahoe)

### wifi
- 根据laobamac大佬的仓库guide，下载kext到EFI(可以使用diskgenius或者[OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools))，修改启动参数，添加itlwm_he=1，仓库地址[这里](https://github.com/laobamac/itlwm)