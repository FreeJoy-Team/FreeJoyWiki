


[Start page](../README.md) | [Previous level](Axes-connection.md)

A potentiometer is an analog signal source. It can be connected either directly to the controller or through external ADCs (analog-to-digital converters) MSP32XX and ADS1115.

An example of connecting a variable resistor directly to the controller:

![](../images/A1.jpg)

Recommened value of the potentiometer for the analog axis is 10K.

Potentiometers are the simplest, cheapest, and most affordable analog signal source for a game controller. They are recommended to be used to control non-critical axes in simulators and when high accuracy of axes is not very important. The resource of potentiometers is small and at the end of their lives (and sometimes at the beginning) they begin to "make noise", i.e. in the absence of movement of the handle, the resistance of the resistor changes randomly. The subsequent axis settings and methods for reducing its noise are described in the [Axis Settings section] (Axis-configuration.md)


[Start page](../README.md) | [Previous level](Axes-connection.md)

