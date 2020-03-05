Device pins can be configured as buttons (digital inputs), analog inputs and digital outputs (LEDs). Pins are configured in the "Pin Config" tab:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/pins_configuration/pins_tab.png)

## Connection

Analog inputs can be connected to pins A0-A7. Digital pins can be connected to any of available pins.

There are three ways to connect digital inputs:

* Matrix of buttons
* Shift registes
* Single buttons

### Connecting single buttons

Single buttons can be connected as "active high" and "active low" buttons. The most common connection is "active low" when the first pin of button is connected to controller's pin and the second pin of button is connected to GND (shown at picture below)

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/pins_configuration/button_connect.png)

In this case select Button GND at expanding menu near needed pin.

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/pins_configuration/button_pin.png)

Controller will provide internal pull-up for chosen input and no external components are needed. 

In the other way the second pin on the button is connected to 3.3V, so Button VCC option must be selected. Controller will provide internal pull-down for selected pin

After setting up single buttons you will see its total count at "Current Config" panel:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/pins_configuration/single_buttons_config.png)

### Connecting matrix of buttons 

In case of connecting buttons in matrix it is highly recommended to use schematic with diodes:

<img src="https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/pins_configuration/button_matrix.png" height=400/>

This will help to avoid negative affects at pushing several buttons at the same time.

For setting up buttons in a matrix select some pins of device as Rows and some as Columns:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/pins_configuration/button_matrix_pins.png)

After setting up matrix buttons you will see total buttons count at "Current Config" panel:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/pins_configuration/maxtrix_buttons_config.png)

As you can see from the image above you can combine single and matrix buttons in your configuration.

## Connecting LEDs to PWM channels

There are three pins where you can connect your highlight LEDs and adjust their brightness:

* PB0
* PB1
* PB4 

RGB leds can be connected to these pin to set custom color of the highlight. If it is supposed to use more than 2-3 LEDs transistor connection is required to prevent damaging the board:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/pins_configuration/led_transistor.png)

Dont forget to use resistors to reduce current through the LEDs and not to damage BluePill board.

## Connecting mappable LEDs

Up to 24 LEDs can be connected to the board and mapped to logical buttons state. This LEDs can be connected as single LEDs or/and as LED matrix.

### Connecting single LEDs

BluePill board already has one single LED connected to pin PC13. You can connect single LEDs to any pin through resistor:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/pins_configuration/single_led_connection.png)

### Connecting LED matrix

LED matrix is similar to button matrix. You can connect Rows and Columns to any pins of BluePill:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/blob/master/images/pins_configuration/led_matrix.png)


## Saving changes

For applying pins configuration and saving it to the device press button **"Write Config to Device"** and wait for **"Config Written"** message appeared:

<img src="https://d.radikal.ru/d33/2001/03/d9b2a553a823.png"/>