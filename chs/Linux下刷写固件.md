

[开始页](../README.md) | [上一页](../README.md) | [English](../eng/Linux-Guide.md)

你需要以下的工具和设备：

* [BluePill开发板](https://camo.githubusercontent.com/a70b6639a020d201e1e1f0f582cd6374761a82d6/68747470733a2f2f642e726164696b616c2e72752f6433332f313931312f65382f6138666632313139636663372e6a7067)
* USB-UART转换模块
* [stm32flash](https://sourceforge.net/p/stm32flash/wiki/Home/)  STM32烧写程序 ([Debian](https://packages.debian.org/stm32flash), [Ubuntu](https://packages.ubuntu.org/stm32flash))
* [最新版本](https://github.com/vostrenkov/FreeJoy/releases)FreeJoy固件


## 使用USB-UART转换模块烧写固件

* 按照下图将USB-UART模块连接到BluePill开发板：

<img src="https://i.imgur.com/7xW4MOB.jpg">

* 将BOOT0跳线设置到位置1：

<img src="https://forum.movimentomaker.pt/uploads/default/original/1X/d2fec4547aef853b6331c7b8323b3beb324bc3ba.jpg" height=400>

* 将USB-UART模块连接到电脑
* 将二进制固件上传到板子
    - 确认选择了.bin格式的固件。
    - 如果你的USB端口不同请修改`ttyUSB0`。
    - 如果在连接板子时出现问题，尝试使用较低的波特率，比如`-b 9600`。

```sh
stm32flash -b 115200 -w build/FreeJoy.bin -v /dev/ttyUSB0
```

* 将BOOT0跳线设置到位置0，并拔掉所有的连接
* 使用USB线将BluePill设备连接到PC。现在应当可以在电脑系统上找到被识别为游戏控制器的FreeJoy设备。

## 配置

Windows/Linux上都可以使用这个配置程序[FreeJoyConfiguratorQt](https://github.com/FreeJoy-Team/FreeJoyConfiguratorQt)。Linux上的游戏（ubuntu，其它的没有进行测试）需要FreeJoy设备至少有一个逻辑按键和X、Y轴的有效输出。否则，游戏将不能识别控制器。

你可能想自己构建这个工程。这样的话，你需要[arm-toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads) ([Debian](https://packages.debian.org/gcc-arm-none-eabi), [Ubuntu](https://packages.ubuntu.com/gcc-arm-none-eabi)) 和`make`。详细的构建指南可以在工程的/armgcc目录下找到。

[开始页](../README.md) | [上一页](../README.md) | [English](../eng/Linux-Guide.md)
