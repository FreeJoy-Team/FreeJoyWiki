MLX90393 3-axis magnetic field sensor can be used for axes inputs. MLX90393 should be powered from 3.3V bus.

## Configuration

MLX90393 sensors are connected to FreeJoy by 4 signal wires:

* **MLX90393_CS** pin (can be connected to any pin except B3, B4 and B5)
* **SPI_MOSI** pin (can be connected only to B5)
* **SPI_MISO** pin (can be connected only to B4)
* **SPI_SCK** pin (can be connected only to B3)

![](../images/mlx90393_sensors/mlx90393_pins.png)

## Operation

MLX90393 is a 3-axis sensor and each of 3 axes can be set to output axis individually. 3 channels correspond to 3 input axes:
* channel 0 - axis X
* channel 1 - axis Y
* channel 2 - axis Z

![](../images/mlx90393_sensors/mlx90393_channels.png)



