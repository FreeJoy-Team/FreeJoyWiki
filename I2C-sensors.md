I2C sensors like AS5600 or external ADC ADS1115 can be used for axes inputs. They should be powered from 3.3V bus.

## Configuration

I2C sensors are connected to FreeJoy by 2 signal wires:

* **I2C_SCL** pin (can be connected only to B8)
* **I2C_SDA** pin (can be connected only to B9)

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/i2c_sensors/i2c_pins.png)

## Operation

I2C devices have their own bus address (usually can be set by pulling pins up or down). For supported devices you can choose their address in combobox (last two digits correspond changable part address). If device have several channels they may be set also:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/i2c_sensors/i2c_channels.png)




