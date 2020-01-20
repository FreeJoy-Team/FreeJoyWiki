FreeJoy supports two types of shift registers IC to extend number of connected buttons: 

* **74HC165**
* **CD4021**

In normal operation shift registers inputs should be pulled to **3.3V** and buttons should be connected to **GND**. Otherwise you will have inverted states output.

## Connection

Only 3 wires are used to connect shift registers to FreeJoy:

* **ShiftReg_LATCH** pin (can be connected to any pin of BluePill board except of B3)
* **ShiftReg_DATA** pin (can be connected to any pin of BluePill board except of B3)
* **SPI_SCK** pin (is always connected to B3 pin for all serial devices)

<img src="https://d.radikal.ru/d43/2001/6d/b46fe0d8b06e.png"/>

Electrical connections of serial register **74HC165** are shown below:

<img src="https://a.radikal.ru/a17/2001/2b/bcf0240c12fc.jpg"/>

Electrical connections of serial register **CD4021** are shown below:

<img src="https://c.radikal.ru/c21/2001/48/e6c6ed1fced3.jpg"/>

## Shift registers settings

After setting proper pins for connection shift registers ICs if should change settings on **Shift Registers** tab:

<img src="https://a.radikal.ru/a34/2001/1e/68cdb5679c94.png"/>

## Saving changes

For applying pins configuration and saving it to the device press button **"Write Config to Device"** and wait for **"Config Written"** message appeared:

<img src="https://d.radikal.ru/d33/2001/03/d9b2a553a823.png"/>
