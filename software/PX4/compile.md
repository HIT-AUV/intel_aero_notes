# PX4 Intel Aero 版本编译

## 固件

[GitHub - PX4 Firmware](https://github.com/PX4/Firmware)

## 编译环境

Ubuntu 16.04 x64 + VMware Workstation 14 Player

## 编译需求

测试环境不是干净的 Ubuntu 16.04，如果发现有遗漏请补充。仅列举原版 Ubuntu 16.04 不包含的部分。

因为 Ubuntu 源速度问题，建议使用国内源，比如：[清华大学开源软件镜像站 - Ubuntu](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/)。

- __Git__：PX4 Firmware 采用 Git submodule，编译时会同步代码。
- __CMake__：编译工具。
- __arm-none-eabi-gcc__，__arm-none-eabi-g++__：STM32 交叉编译工具链。
- __genromfs__
- __python-jinja2__
- __python-empy__
- __python-numpy__，__python-toml__：程序提示用 pip 方式安装，apt-get 实测也可以。如果 pip 报大段红字错误可以用 apt-get，貌似是一个 Linux bug。
- __catkin__
- __unzip__

## 编译

建议切到一个 Release 版本，然后再编译。

``` bash
git checkout v1.7.3
make aerofc-v1_default
```

## 全部命令行

```bash
sudo apt-get update
sudo apt-get install git cmake gcc-arm-none-eabi genromfs python-jinja2 python-empy python-numpy python-toml catkin unzip
mkdir -p PX4
cd PX4
git clone https://github.com/PX4/Firmware.git
cd Firmware
git checkout v1.7.3
make aerofc-v1_default
```
