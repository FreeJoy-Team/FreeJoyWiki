External ADC MCP3201/02/04/08 can be used for axes inputs. They should be powered from 3.3V bus.

## Configuration

MCP3201/02/04/08 sensors are connected to FreeJoy by 4 signal wires:

* **MCP320x_CS** pin (can be connected to any pin except B3, B4 and B5)
* **SPI_MOSI** pin (can be connected only to B5)
* **SPI_MISO** pin (can be connected only to B4)
* **SPI_SCK** pin (can be connected only to B3)

![](../images/mcp320x_adc/mcp320x_pins.png)

## Operation

MCP3201/02/04/08 are 1/2/4/8-channel ADC. Each channel can be set to axis individually:

![](../images/mcp320x_adc/mcp320x_channels.png)



