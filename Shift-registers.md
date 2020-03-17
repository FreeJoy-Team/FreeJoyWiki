FreeJoy supports two types of shift registers IC to extend number of connected buttons: 

* **74HC165**
* **CD4021**

You can choose if yout shift register input are pulled up or down.

## Connection

Only 3 signal wires and 2 power wires are used to connect shift registers to FreeJoy:

* **ShiftReg_LATCH** pin (can be connected to any pin of BluePill board except of B3)
* **ShiftReg_DATA** pin (can be connected to any pin of BluePill board except of B3)
* **SPI_SCK** pin (is always connected to B3 pin for all serial devices)
* **VCC** (or **VDD**) pin of shift registers should be connected to **3.3V** power bus for proper operation
* **GND** (or **VSS**) pin must be connected to BluePill's **GND**

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/shift_registers/shift_registers_tab.png)

Electrical connections of serial register **74HC165** are shown below:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/shift_registers/74hc165_connection.png)

Electrical connections of serial register **CD4021** are shown below:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/shift_registers/cd4021_connection.jpg)

## Shift registers settings

After setting proper pins for connection shift registers ICs you should change settings on **Shift Registers** tab:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/shift_registers/shift_register_setting.png)

## Saving changes

For applying pins configuration and saving it to the device press button **"Write Config to Device"** and wait for **"Config Written"** message appeared:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/config_written.png)
