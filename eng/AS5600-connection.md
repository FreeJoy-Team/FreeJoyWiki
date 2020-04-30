AS5600 is a digital single-channel Hall sensor. It works on the I2C interface.
![](../images/A1.3.jpg)
 
* I2C_SCL - Common for all I2C devices (AS5600 and ADS1115 ADCs)
* I2C_SDA - Common for all I2C devices (AS5600 and ADS1115 ADCs)

As you can see from the picture above, the sensors can be bought already soldered to the board. Due to the fact that the sensors have the same address assigned at the factory, only one sensor of this type ** can be connected to ** FreeJoy.

Installing a magnet for the sensor is similar to [installing magnets for the sensors TLE5010/5011](TLE501x-connection.md)

The cost of AS5600 sensors is comparable to Hall sensors. They can be used to control the most important axes of the controller, which are often used in simulators, and when the highest accuracy of readings is required. The life of the AS5600 sensors is almost unlimited, as they are contactless like Hall sensors. Their accuracy is slightly lower than the TLE5011 sensors.

The subsequent axis settings are described in the [Axis Settings](Axis-configuration.md) section 
