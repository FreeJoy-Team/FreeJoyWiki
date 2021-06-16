

[开始页](../README.md) | [上一页](./LED的连接.md) | [English](../eng/Mono-LED-configuration.md)

## 单色LED的连接

![L1](../images/L1.jpg)

像图中显示的，FreeJoy支持连接LED矩阵，也支持单个LEDs。建议为每个LEDs单独计算限流电阻的阻值。你可以使用在线计算器计算。同时需要考虑到当一根线上的所有LEDs点亮时，流过它们的电流应当不超过20 mA。

如果你打算使用高功率LEDs，那么你需要使用"[RGB LED的连接](./RGB-LED的连接.md)"这个例子中的放大器方案。

可以用LEDs的亮灭映射逻辑按键的状态。这样，你可以使得LED根据按键的状态改变亮灭状态：

![L3](../images/L3.jpg)

在图中，在右边的“LED”区域可以进行单色LEDs的分配。

- No. - LED的编号；
- Input No. - 分配给该LED的逻辑按键编号；
- Function - LED对应按键的状态（正常或者相反）。

[开始页](../README.md) | [上一页](./LED的连接.md) | [English](../eng/Mono-LED-configuration.md)
