TLE501x magnetic field sensor can be used for axes inputs. You you are using TLE5010 be sure it is powered by 4-5V supply voltage and you have voltage level converter from 3.3v to 5V for SCK and GEN pins. TLE5011 should be powered from 3.3V bus.

## Configuration

In most of cases TLE501x sensors are connected to FreeJoy by 4 signal wires:

* **TLE501x_CS** pin (can be connected to any pin except B3, B5 and B6)
* **TLE501x_DATA** pin (can be connected only to B5)
* **TLE501x_GEN** pin (can be connected only to B6)
* **SPI_SCK** pin (can be connected only to B3)

![](../images/tle501x_sensors/tle_config.png)

If you are using TLE501x sensor with generator on board TLE501x_GEN connection is not required.

## Connection

In case of using several TLE501x sensors they should be connected in a bus:

![](../images/tle501x_sensors/tle_connection.png)

Any pin except of B3, B5 and B6 can be used for CS connection.

## Operation

TLE501x operates as angle sensors in magnetic field. It has output values from **0** to **360** degrees (mapped to -32767-32767 output). If your sensor's output cross from **32767** to **-32767** while calibration/operation you need to set **"Offset"** on **"Axes Config"** tab:

![](../images/tle501x_sensors/offset.png)



