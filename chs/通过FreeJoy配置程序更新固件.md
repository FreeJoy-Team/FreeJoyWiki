

[开始页](../README.md) | [上一页](../README.md) | [English](../eng/Firmware-flasher.md)

FreeJoy配置程序的固件下载功能可以让你不用烧写器就可以进行固件更新。要实现这个功能需要控制板已经使用烧写器刷上了FreeJoy的固件。你可以在FreeJoy配置程序的“Advanced Settings”选项卡中的“Fireware flasher”找到这个功能：

![](../images/flasher_tab.png)

要使得控制板能够加载新的固件，你首先需要将你的控制板设置到bootloader模式（当设备处于bootloader模式时，设备会在电脑上被识别为“FreeJoy Flasher”，而且设备上的LED灯会闪烁）。进入bootloader模式有两种方法：

### 使用FreeJoy配置程序进入bootloader模式

* 使用USB线将设备连接到电脑上；
* 选择FreeJoy配置程序中的“Advanced settings”选项卡；
* 点击“Enter flasher mode”按钮，然后等待设备重新连接，被重新识别为“FreeJoy Flasher”（这个过程应该需要几秒钟）。

### 通过设置控制板跳线进入bootloader模式

如果你因为一些原因无法使用FreeJoy配置程序进入bootloader模式的话：

* 拔下设备的USB线和其它电源；
* 将跳线BOOT1（靠近BluePill板子底部）设置到位置1。同时需要注意把BOOT0跳线设置在位置0。

![](../images/flasher_jumper.jpg)

* 将设备通过USB线连接到电脑，确保被识别为“FreeJoy Flasher”。

### 加载固件

* 确保设备处于bootlader模式（设备上的LED灯在闪烁，设备在电脑上被识别为“FreeJoy Flasher”）；
* 在FreeJoy配置程序上点击“Flash fireware”；
* 从[FreeJoy](https://github.com/vostrenkov/FreeJoy/releases)代码库中选择你需要版本的.bin格式的固件文件。
* 点击“OK”，然后等待更新的进度条到达100%；
* 如果你是通过设置跳线进入bootloader模式的话，将所有的跳线还原到位置0，并且重新连接设备。

这之后你的控制板就有了新的固件，你可以开始配置它了。

[开始页](../README.md) | [上一页](../README.md) | [English](../eng/Firmware-flasher.md)
