


[Start page](../README.md) | [Previous level](Buttons-connection.md)

# Connecting buttons to shift registers using the shift register 74HC165 as an example
## Pin assignment:

An example of connecting a shift register board is shown below:

![](../images/S1.jpg)

PCB for shift registers may be bought pre-made or made by yourself. Purchased shift register pcb example:
![](../images/74hc165_pcb.jpg)

Files for DIY shift registers board may be found here:
https://github.com/FreeJoy-Team/FreeJoyWiki/blob/master/3rd-party/hardware/MMJoy2_74HC165.lay6

* SPI_SCK - Common for all TLE5011 and all shift register chains.
* ShiftReg_DATA - individual for each chain of shift registers (Here, the second chain of shift registers is connected to pins A7, A6)
* ShiftReg_LATCH - may be common or individual for all shift registers chains

It is recommended to connect shift registers VCC to +3.3V.

Different boards and shift registers have different pin names. See the table below:

| Name in configurator | 74HC165 pin | CD4021 pin | Alternative pin names |
|---------------------|------------------|-----------------|---------------|
|       SPI_SCK       |       CLK        |      CLOCK      |     SCK               |
|    ShiftReg_DATA    |        Qh        |        Q8       |     DATA/SERIAL_OUT/OUT |
|    ShiftReg_LATCH   |       SH/LD      | PAR/SER CONTROL |     LATCH             |
|         3.3V        |        VCC       |       VDD       |     5V/V+  |
|         GND         |        GND       |       VSS       |     V-        |
|    -------------    |        SER       |  SERIAL IN      |     INPUT/DATA_IN/IN |
|    -------------    |     CLK_INH      |    ------------ |     CE |

## Assigning the number of shift registers.

![](../images/S2.jpg)

Here 3 shift registers are connected to contacts A4, A5, one to contacts A6, A7. We set the number of physical buttons (the number of shift registers * 8). PullUp and PullDown - type of connection of buttons to the shift register. If you connected the shift register and all buttons in the pressed state on the Button Config tab when no buttons are pressed, then you need to change the type from PullUp to PullDown (or vice versa).

There are 74HC165 and CD4021 shift registers are supported. Both chips are available both in the DIP-16 package (for mounting in the board holes) and in the SO-16 package (for surface mounting) Drawings of the 74HC165 shift register in the SO-16 package, as in the example above, for Sprint Layout can be taken [here](../3rd-party/hardware/). Also (if you do not have the opportunity to make a board yourself), you can use a riser like this:

![SO-16](/images/SO-16.jpg)

All types of switches (buttons, toggle switches, encoders, etc.) can be connected to shift registers. Their setting is similar to [connecting buttons directly to the controller](Connecting-buttons-directly-to-controller.md)



[Start page](../README.md) | [Previous level](Buttons-connection.md)

