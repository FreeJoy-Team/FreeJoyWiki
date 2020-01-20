FreeJoy supports up to 8 analog 12bit (4096 samples) inputs and digital TLE501x sensors as inputs of axes. Every axis has such settings as:

* Output control
* Calibration
* Magnet offset feature
* Resolution
* Invertion
* Smoothing
* Curve shaping

Settings for analog inputs are represented at "Axes Config" and "Axes Curves" tabs.

<img src="https://d.radikal.ru/d29/2001/60/b5f00980733c.png">

Before axis configuration make sure the correct pins for analog inputs or digital sensors are chosen in "Pin Config" tab and configuration is written to the device.

## Calibration

By default all inputs calibrated to fullscale range 0-4095. You can choose one of two options for calibration:

* Manual calibration
* Automatic calibration

For axes calibration go to "Axis Config" tab. You will see 8 blocks for 8 analog inputs where 1st is mapped to the lowest number of pin at A port (A0 by default). Axes with digital sensors inputs have lowest number than axes with analog inputs.

### Manual calibration

In case of manual calibration set your axis to the lowest position and set the "Minimum" value to the current Raw value:

<img src="https://c.radikal.ru/c05/2001/44/21855b13911f.png">

Then set set axis to the highest position and set "Maximum" value to the current Raw value:

<img src="https://b.radikal.ru/b16/2001/c0/b744ca79bdf9.png">

In case you have asymmetrical axis input you can set center position. Do do this you need to check Center checkbox, set your axis to the neutral position and set "Center" value to current Raw value:

<img src="https://b.radikal.ru/b18/2001/23/b65baa2112f9.png">

After writing config to the device you will see that device now scaling input data to the lower and higher limits and logical center corresponds the physical neutral position.

### Automatic calibration

For automatic calibration: 

* Press button **"Start calibration"**
* Set your axis to **minimum** position, hold for a second
* Set your axis to **maximum** position, hold for a second
* Set your axis to **neutral** (center position) and press **"Stop calibration"** button

After this your calibration values are ready to be written to the board.

## Magnet offset

This feature allows you to shift axis output by half of its fullscale value. This may be helpful when your magnetic field sensor output crossing from **4095** to **0** while calibration.

## Resolution

It is possible to set axis resolution lower than 12 bit for some reasons (noise cancellation, etc.)
Axis resolution can be set from **1** bit to **12** bits.

## Invertion

Every axis can be logically inverted by checking "Inverted" checkbox for corresponding axis

## Smoothing

You can set smoothing for every axis by dragging "Smoothing" slider. There are 4 levels of smoothing:

* Off
* Low
* Medium
* High

## Curve shaping

You can set a custom curve shape for every axis. This settings and represented at "Axes Curves" tab:

<img src="https://d.radikal.ru/d20/1911/ed/b4a208040b8c.png">

There are 10 points you can drag for setting the custom curve shape:

<img src="https://d.radikal.ru/d23/1911/13/b5d81f378bd1.png">

For your convenience there are 4 presets available. To apply the preset just press on it: 

<img src="https://d.radikal.ru/d40/1911/23/26150c28d8d1.png">

## Saving changes

For applying pins configuration and saving it to the device press button **"Write Config to Device"** and wait for **"Config Written"** message appeared:

<img src="https://d.radikal.ru/d33/2001/03/d9b2a553a823.png"/>