Analog or digital sensors can be used as sources of axes. Analog sensors can be connected directly to controller or using external ADC periphreals:

* [Connection of potentiometer](Potentiometer-connection.md)
* [Connection of Hall sensors](Hall-sensors-connection.md)
* [Connection of analog sensors to external ADC ADS1115](Connecting-analog-axes-to-ADS1115.md)
* [Connection of analog sensors to external ADC MCP32XX](Connecting-analog-axes-to-MCP320x.md)

Digital sensors are connected to the controller via SPI or I2C interface (depending on sensor type):

* [Connection of sensors TLE5010/5011](TLE501x-connection.md)
* [Connection of sensor AS5600](AS5600-connection.md)
* [Connection of sensors MLX90393](MLX90393-connection.md)

Once you connected your axes sources you can should set them up in accordance with your application:

* [Axis Settings](Axis-configuration.md)
* [Convert axis movement to button clicks](Axis-to-buttons-function.md)
* [Convert button presses to axis movement](Buttons-encoders-to-axis-function.md)