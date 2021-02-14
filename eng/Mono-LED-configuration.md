

[Start page](../README.md) | [Previous level](LED-connection.md)

## Mono LEDs connection

![L1](../images/L1.jpg)

FreeJoy allows you to connect the LEDs in a matrix and as single LEDs as shown in the figure. The value of the current limiting resistances is recommended to be calculated individually for the LEDs that you will use. You may want to use online calculator for this. At the same time, it should be taken into account that when all the LEDs in the line are turned on, the current flowing through them should not exceed 20 mA.

If you plan to turn on high-power LEDs, then you need to use the amplifier scheme as in the example [connecting RGB LEDs](RGB-LED-configuration.md).

The switching on of the LEDs can be mapped to the state of the logic button. In this case, you can additionally make the LED invert relative to the button state:

![L3](../images/L3.jpg)

In the figure, the right side of the LED tab is responsible for the assignment of single-color LEDs.

- No. - LED number;
- Input No. - the number of the logical button assigned to the LED;
- Function - the state of the LED relative to the button state (normal or inverted)

[Start page](../README.md) | [Previous level](LED-connection.md)

