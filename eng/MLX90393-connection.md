MLX90393 is a digital 3-channel Hall sensor. It operates on the SPI interface.

![](../images/A1.4.jpg)
 
* SPI_SCK - Common for all SPI devices (TLE5011, MLX90393, MCP32XX and all shift register chains);
* SPI_MISO - common to all SPI devices;
* SPI_MOSI - common to all SPI devices;
* MLX90393_CS - individual for each MLX90393.

As hown at the figure above the sensors can be bought already soldered to the board which is subject to minimal development.

Installing a magnet for the sensor is similar to installing magnets for Hall sensors, but it must be taken into account that the sensor gives the magnet position along three axes (X, Y - magnet movement parallel to the sensor plane and Z - perpendicular to the sensor plane). Possible options for the relative positioning of the sensor and magnets see below:

![](../images/A1.4.1.jpg)

The MLX90393 sensor can be used to monitor the most important controller axes, which are often used in simulators, and when the highest accuracy of readings is required. Given that the sensor can read the movement of the magnet along two mutually perpendicular axes, it is possible to build a joystick stick using only one such sensor. The resource of the MLX90393 sensors is almost unlimited, as they are contactless like Hall sensors.

The subsequent axis settings are described in the [Axis Settings] section (Axis-configuration.md)