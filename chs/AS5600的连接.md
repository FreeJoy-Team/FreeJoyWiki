


[Start page](../README.md) | [Previous level](Axes-connection.md)

The AS5600 is a digital single-channel hall sensor. It works on the I2C interface, and can also be used as an analog Hall sensor. The sensor can be purchased already soldered on the board (one of the board options is shown in the figure below). The sensor can be powered from both 5V and 3.3 V, so it is necessary to check whether the sensor power is properly diluted on the board. To do this you must check the connection between 1 and 2 contacts of the chip (as shown in the figure below, the first is the pin near the key pressed point on the body of the chip). If the resistance is large these pins should be shorted manually.

![](../images/A1.3.0.jpg)

### Connecting the AS5600 via the I2C interface

![](../images/A1.3.jpg)

* I2C_SCL-Common to all I2C devices (AS5600 and ADS1115 ADC)
* I2C_SDA-Common to all I2C devices (AS5600 and ADS1115 ADC)

As you can see from the picture above, the sensors can be purchased already soldered to the board. Due to the fact that the sensors have the same address assigned at the factory, only one sensor of this type can be connected to FreeJoy **in digital mode**.

Installing a magnet for the sensor is similar to [installing magnets for TLE5010/5011 sensors](TLE501x-connection.md)

The cost of the AS5600 sensors is comparable to Hall Sensors. They can be used to control the most important axes of the controller, which are often used in simulators, and when the highest accuracy of the readings is needed. The life of the AS5600 sensors is almost unlimited, since they are contactless, just like Hall sensors. Their accuracy is slightly lower than the TLE5011 sensors.

The subsequent axis setup is described in the section [Axis Setup] (Axis-configuration.md)

### Connecting the AS5600 as an analog sensor

![](../images/A1.3.1.jpg)

As you can see from the figure with this connection the AS5600 may work like a normal analog hall sensor and the signal level at the output (OUT) changes from 0 to 3.3 V, when the magnet is rotated 360 degrees. Thus you can connect up to 8 sensors to the contacts of the controller A0 - A7.

The AS6500 allows you to reprogram the angle of rotation of the magnet, so that the voltage change from 0 to 3.3 v occurs when the magnet is rotated by a smaller angle. This allows you to achieve much higher accuracy than a conventional Hall sensor. **Angle programming can be done only once. The sensor rotation angle cannot be reprogrammed.** Therefore, it is recommended to perform such programming on the sensor already installed in the device you are assembling.

#### Reprogramming the angle of rotation of the magnet for the AS5600:

1. Short the PGO (GPO) pin to the ground with a jumper when the power is off (this is necessary to enter the programming mode).

2. Short the DIR pin depending on where you plan to rotate the magnet during calibration from the initial position relative to the chip cover: to the ground - clockwise, to the power supply-counterclockwise.

3. Apply power.

4. Turn the magnet to the initial end position.

5. Short the output (OUT) to ground.

6. Turn the magnet to the other extreme position (the angle must be at least 18 degrees).

7. Short the output (OUT) to ground.

8. Check whether the output signal changes when the magnet is rotated. If there is a constant " 0 "or plus power supply, regardless of the position of the magnet, then there was a programming error (for example, "bouncing" while shorting pins). In this case try again starting from step 4.

9. Remove the jumper from the PGO (GPO).

10. The DIR input should remain shorted to ground or power after calibration like described at step 2.



[Start page](../README.md) | [Previous level](Axes-connection.md)

