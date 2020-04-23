**This page may be outdated**

If you dont want to use graphical utility for some reason there is a way to set device configuration in source files. 

Device configuration is described in main.h file and it is loaded to the device at the first startup (or after chip erase).

## Advanced settings block

### .firmware version
**Do not change** this value, it is needed for proper device work.

### .device_name[]
This is how your device will be identificated. Maximum length is **20** bytes.

### .button_debounce_ms
Minimum time after button press when new button press can be detected. Recommended value is from 50ms to 100 ms. 

### .toggle_press_time_ms
Logical button will be pressed during this period at toggle switch state change. 

### .encoder_press_time_ms
Logical button will be pressed during this period at encoder step. Recommended value is from 5 to 20 ms.

### .exchange_period_ms
Time between two sequential USB packets from device to PC. Recommended value is from 2 to 5 ms.

## Pins block

Pins numeration starts from **A0** pin and ends at **PC15** pin. Total 30 pins of device can be used.

Pins **A0-A7** (**pins[0]-pins[7]**) can be set to **AXIS_ANALOG**, **BUTTON_GND**, **BUTTON_VCC**, **BUTTON_ROW**, **BUTTON_COLUMN**, **TLE5011_CS**, **SHIFT_REG_CS**, **SHIFT_REG_DATA**  modes.

All other pins can be set only to **BUTTON_GND**, **BUTTON_VCC**, **BUTTON_ROW**, **BUTTON_COLUMN**, **TLE5011_CS**, **SHIFT_REG_CS**, **SHIFT_REG_DATA** modes.

If using serial devices like shift registers SCK pin should be selected (PB3). For TLE501x data pin PD5 and generator pin PB6 available are only available.

## Axes block

### .axis_config.calib_min
Calibration value for axis minimum 

### .axis_config.calib_center

Calibration value for axis center

### .axis_config.calib_max

Calibration value for axis maximum

### .axis_config.out_enabled

Out enabling/disabling

### .axis_config.magnet_offset

Making axis output shifted by a half

### .axis_config.inverted

Inverts output

### .axis_config.curve_shape[i] 

10 Y values of curve points from 0% to 100%, where 0% is minimum calibrated value and 100% is maximum calibrated value 

### .axis_config.resolution

Sets maximum axis resolution (for analog axes 12 bit is maximum)

### .axis_config.dead_zone

Center dead zone (value * 0.1%)

### .axis_config.source_main

Pin number of axis source

### .axis_config.function

Function applied to secondary axis source

* 0 - None
* 1 - Plus absolute
* 2 - Plus relative
* 3 - Minus absolute
* 4 - Minus relative

### .axis_config.source_secondary

Number of axis (0 - 7) set as secondary source

### .axis_config.decrement_button

Number of logical button set as decrement button (for buttons to axes function)

### .axis_config.center_button

Number of logical button set as center button (for buttons to axes function)

### .axis_config.increment_button

Number of logical button set as increment button (for buttons to axes function)

### .axis_config.step

Step of incrementing/decrementing at button press. Values from 1 to 255

### .axis_config.filter 

Filter level. Available values from 0 to 3

## Buttons block

### .buttons[i]

Buttons configuration. Available values:
* BUTTON_NORMAL
* BUTTON_INVERTED
* BUTTON_TOGGLE
* TOGGLE_SWITCH
* TOGGLE_SWITCH_ON
* TOGGLE_SWITCH_OFF
* POV1_UP
* POV1_RIGHT
* POV1_DOWN
* POV1_LEFT
* POV2_UP
* POV2_RIGHT
* POV2_DOWN
* POV2_LEFT
* POV3_UP
* POV3_RIGHT
* POV3_DOWN
* POV3_LEFT
* POV4_UP
* POV4_RIGHT
* POV4_DOWN
* POV4_LEFT
* ENCODER_INPUT_A
* ENCODER_INPUT_B
* RADIO_BUTTON1
* RADIO_BUTTON2
* RADIO_BUTTON3
* RADIO_BUTTON4

## Axes to buttons

### .axes_to_buttons.points[i]

Point of ranges ends. Points count must be (buttons_cnt + 1)

### .axes_to_buttons.buttons_cnt

Number of buttons from axis

### .axes_to_buttons.is_enabled

Is axis to buttons function enabled

## Shifts

### .shift_config.button

Logical buttons set to shift

## HID config

### .vid

USB VID

### .pid

USB PID

### .is_dynamic_config

Enable/disable removing not used buttons and axes from HID descriptor 

## Applying configuration
**For successful configuration make full chip erase before flash programming!**