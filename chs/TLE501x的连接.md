

[开始页](../README.md) | [上一页](轴的连接.md) | [English](../eng/TLE501x-connection.md)

TLE5011和TLE5010是单通道的数字霍尔传感器。它们工作在半双工的SPI接口。

![](../images/A1.1.jpg)
 
**注意：为了正确的操作，TLE501x的数据线需要有1k的上拉电阻**

* SPI_SCK - 时钟信号，对所有SPI设备都一样（TLE5011、MLX90393、MCP32XX和所有的移位寄存器）；
* SPI_MOSI - 主设备数据输出，从设备输入，对所有SPI设备都一样；
* TLE5011_GEN - 主设备数据输入，对所有的TLE5011都一样。在一些板子上可能会叫做MISO；
* TLE5011_CS - 片选信号，每个TLE5011单独连接。

TLE5010和TLE5011传感器的价格和霍尔传感器的差不多。建议使用它们控制控制器中最重要的轴，也就是在模拟器中使用最多的轴，同时需要最高精度的时候。因为TLE传感器像霍尔传感器一样是没有接触的，所以它的使用寿命几乎是无限的。

很少看到已经安装上了TLE5011的板子，所以我们建议你自己设计板子。Sprint Layout软件的TLE5011图纸可以在[这里](../3rd-party/hardware)找到

或者你可以使用像这样的转接板：

![](../images/SO-8.jpg)

[TLE5011/5010](https://www.infineon.com/cms/en/product/sensor/magnetic-sensors/magnetic-position-sensors/angle-sensors/tle5011/)传感器会响应磁场轴相对传感器轴的方向变化。要实现这样的情形，你可以使用矩形（像图中所示）立方磁体。圆盘状和圆环状的磁体可以用来确保有**径向**的磁化。

![](../images/A1.1.1.jpg)

[轴的配置](轴的配置.md)部分会说明接下来在FreeJoy的配置程序中如何配置轴。

[开始页](../README.md) | [上一页](轴的连接.md) | [English](../eng/TLE501x-connection.md)
