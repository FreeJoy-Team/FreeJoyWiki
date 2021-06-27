

[开始页](../README.md) | [上一页](Windows下刷写固件.md) | [English](../eng/Flashing-firmware-with-ST-Link-programmer.md)

1. 按照下图把ST-Link烧录器连接到控制板（注意检查烧录器和控制板引脚的标记）：

![](../images/1.jpg)

2. 将ST-Link v2烧录器连上电脑；

3. 在电脑上运行ST-Link烧录软件ST32 ST-LINK Utility；

4. 点击软件菜单上的“File-> Open File”，然后选择FreeJoy目录下的.hex文件，添加需要烧写的固件；

5. 现在可以看到二进制代码下载界面：

![](../images/2.jpg)

6. 点击“Target-> Connect”，等待软件连接设备。连接成功后可以在上方看到设备ID、闪存大小和设备系列等信息，在中间看到当前设备内部存储的内容。

![](../images/3.jpg)

7. 点击“Target-> Erase chip”，然后点击“OK”，擦除设备芯片；

![](../images/4.jpg)

8. 点击“Target-> Program & Verify”，在出现的对话框中点击“Start”，开始进行固件的烧写和验证：

![](../images/5.jpg)

9. 在成功向控制板烧录固件之后，断开所有的连接，重新用MicroUSB线将控制板连接到电脑上。

10. 现在可以电脑上看到一个显示为游戏控制器的FreeJoy设备。

[开始页](../README.md) | [上一页](Windows下刷写固件.md) | [English](../eng/Flashing-firmware-with-ST-Link-programmer.md)
