TLE501x magnetic field sensor can be used for axes inputs. You you are using TLE5010 be sure it is powered by 5V supply voltage. TLE5011 can be powered from 3.3V bus.

## Configuration

In most of cases TLE501x sensors are connected to FreeJoy by 4 signal wires:

* **TLE501x_CS** pin (can be connected to any pin except B3, B5 and B6)
* **TLE501x_DATA** pin (can be connected only to B5)
* **TLE501x_GEN** pin (can be connected only to B6)
* **SPI_SCK** pin (can be connected only to B3)

<img src="https://c.radikal.ru/c13/2001/d7/ec82f0832ec2.png"/>

If you are using TLE501x sensor with generator on board TLE501x_GEN connection is not required.

## Connection

In case of using several TLE501x sensors they should be connected in a bus:

<img src="https://d.radikal.ru/d30/2001/ef/18c9901ee15c.png"/>

Any pin except of B3, B5 and B6 can be used for CS connection.

## Operation

TLE501x operates as angle sensors in magnetic field. It has output values from **0** to **360** degrees (mapped to 0-4095 output). If your sensor's output cross from **4095** to **0** while calibration/operation you need to check **"Magnet offset"** on **"Axes Config"** tab:

<img src="https://a.radikal.ru/a13/2001/86/f85a809e3646.png"/>



