TLE5011 and TLE5010 are single-channel digital Hall sensors. They operate on half-duplex SPI interface.

![](../images/A1.1.jpg)
 
** Attention: The TLE5010 Hall sensor should powered by a voltage of 4.5-5V. The operation of the sensor with STM32 is not guaranteed without using voltage level shifters, and we recommend you to use TLE5011! ** (Other sensors including TLE5011 are powered from 3.3V).

* SPI_SCK - Common for all SPI devices (TLE5011, MLX90393, MCP32XX and all shift register chains);
* SPI_MOSI - common to all SPI devices;
* TLE5011_GEN - common to all TLE5011;
* TLE5011_CS - individual for each TLE5011.

The cost of the TLE5010 and TLE5011 sensors is comparable to the Hall sensors. They are recommended to be used to control the most important axes of the controller, which are often used in simulators and when the highest accuracy of readings is required. The resource of TLE sensors is almost unlimited as they are contactless like Hall sensors.

Already mounted boards with TLE5011 are rare therefore we recommend manufacturing the board yourself. The drawing of the TLE 5011 board for Sprint Layout can be taken [here](../ 3rd-party / hardware /)

Or you can use a riser, for example this:

![](../images/SO-8.jpg)

The TLE5011/5010 sensors respond to a change in the direction of the axis of the magnetic field relative to the axis of the sensor. To do this, you can use rectangular (as in the figure), cubic magnets. Disc-shaped magnets and ring-shaped magnets can be used to ensure that they have ** diametral ** magnetization.

![](../images/A1.1.1.jpg)

The subsequent axis settings are described in the [Axis Settings] section (Axis-configuration.md)